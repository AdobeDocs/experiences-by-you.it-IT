---
title: 'La magia dietro il sipario: segmenti complessi; esclusioni, contenitori e attribuzione'
description: _Scopri le complessità della segmentazione di dati complessi, esplorando le esclusioni, i contenitori e i modelli di attribuzione. Come il gioco di prestigio di un mago, padroneggiare queste tecniche permette agli analisti di eseguire la magia dei dati, trasformando le informazioni con precisione e finezza.
feature: Segmentation
role: User
level: Experienced
doc-type: Article
duration: 36000
last-substantial-update: 2024-03-25T00:00:00Z
jira: KT-15200
thumbnail: KT-15200.jpeg
exl-id: 1da85e88-64b3-49e5-9bf6-76126ac9f6ad
source-git-commit: 69fa16c1bf38604e4dabc553baee71598be83db3
workflow-type: tm+mt
source-wordcount: '4102'
ht-degree: 1%

---

# La magia dietro il sipario: segmenti complessi: escludi, contenitori e attribuzione

_Scopri le complessità della segmentazione dati complessa, esplorando le esclusioni, i contenitori e i modelli di attribuzione. Come il gioco di prestigio di un mago, la padronanza di queste tecniche consente agli analisti di eseguire la magia dei dati, trasformando le informazioni con precisione e finezza._

Le tende sono aperte, il palco è impostato... questo potrebbe non essere un atto magico di Las Vegas, ma possiamo eseguire alcuni trucchi piuttosto sorprendenti durante la costruzione dei nostri segmenti.

![Mani_Mago](assets/magician-hands.jpeg)

All’interno di questo modulo verranno trattati:

- Escludi logica
- Utilizzo dei contenitori
- Modello di attribuzione

## Includi/Escludi

Per impostazione predefinita, tutti i contenitori iniziano come tipo **include**, il che significa in pratica che restituiscono i dati che corrispondono ai criteri. Tuttavia, puoi anche modificare il segmento o i contenitori all&#39;interno dei segmenti in modo che siano di tipo **exclude**, consentendo di rifiutare determinati criteri.

Anche se un mago può trovare la tua carta nel mazzo, è sorprendente che possa far sì che il resto del mazzo non esista. Allo stesso modo, nei segmenti di esclusione, vogliamo che i dati indesiderati scompaiano semplicemente dal nostro set di dati.

![schede vuote](assets/blankcards.png)

Potreste stare lì seduti a pensare, &quot;Ok, ma ho già le opzioni &#39;Does not Equal&#39; e &#39;Does not Contain&#39;, quindi non dovrebbe coprirmi?&quot; Sfortunatamente, la risposta è no... e non si tratta solo di essere in grado di escludere gruppi di logica, su un singolo elemento. Anche quando si tratta di un singolo componente, spesso è necessario utilizzare *escludi* per raggiungere l&#39;obiettivo.

- **Does not contain / Does not equal** - È proprio come sembra, corrispondenza su elementi che non contengono una stringa specifica
- **Escludi: il valore contiene / è uguale a** - *esclude* elementi che corrispondono alla stringa

A prima vista, entrambi suonano allo stesso modo... e sui segmenti/contenitori di livello **hit**, potresti essere corretto, in quanto eseguiranno la stessa azione. Tuttavia, quando utilizzi l&#39;ambito **visita** o **visitatore** otterrai risultati molto diversi.

**Figura 1: non contiene / non è uguale a - Ambito hit**

![Figura1-DnceVsExclude-Hit](assets/figure1-dnce-vs-exclude-hit.png)

*Si noti che ogni hit restituisce un valore true o false e che tali valori sono invertiti tra does not e exclude.*

- Se &quot;Value&quot; non contiene &quot;Example&quot; (yes), restituisce true e include tale hit; analogamente, se &quot;Example&quot; non contiene &quot;Example&quot; (no, lo contiene), restituisce false e non include tale hit. In pratica, restituisce qualsiasi dato che restituisce un risultato vero.
- Se &quot;Value&quot; contiene &quot;Example&quot; (no), restituisce false e non esclude tale hit; analogamente, se &quot;Example&quot; contiene &quot;Example&quot; (yes), restituisce true ed esclude tale hit. In pratica, restituire dati che **non** hanno un risultato vero o restituire dati falsi secondo i criteri.
- È possibile notare che al livello **Hit** entrambi i set di logica restituiranno lo stesso set di dati.

**Figura 2: non contiene / non è uguale a - Ambito visita**

![Figura2-DnceVsExclude-Visit](assets/figure2-dnce-vs-exclude-visit.png)

*Come sopra, ogni hit all&#39;interno della **visita**&#x200B;verrà valutato con lo stesso true / false. Tuttavia, il set di dati restituito è quello dell&#39;intera visita.*

- In ogni hit, &quot;Value&quot; non contiene &quot;Example&quot; (yes), quindi restituisce true; allo stesso modo, &quot;Example&quot; non contiene &quot;Example&quot; (no, lo contiene), quindi restituisce false.
   - Se l&#39;hit **any** nella visita restituisce **true**, viene restituita la **visita intera**.*
   - Se la visita è costituita interamente da hit contenenti &quot;Esempio&quot;, nessun hit restituirà true, pertanto la visita **non verrà restituita** nel set di dati.
- Anche in questo caso, a ogni hit &quot;Esempio&quot; contiene &quot;Esempio&quot; (sì), quindi restituisce true
   - Se **qualsiasi hit** restituisce **true**, l&#39;intera visita sarà **esclusa**
   - Se **tutti gli hit** della visita restituiscono **false**, la visita verrà restituita nel set di dati
- Ora potete vedere dove questa logica comincia a divergere. Nell’esempio precedente vi sono tre visite distinte:
   - Quando si utilizza &quot;Does Not Contain / Equal&quot; **verranno restituite due delle tre** visite.
   - Quando si utilizza &quot;Exclude Contains/Equals&quot; **verrà restituita solo una** di queste visite

**Figura 3: non contiene / non è uguale a - Ambito visita**

![Figura3-DnceVsExclude-Visitor](assets/figure3-dnce-vs-exclude-visitor.png)

*Come sopra, ogni hit effettuato dal **visitatore**&#x200B;verrà valutato con la stessa logica true/false. Ma ora stiamo esaminando tutti gli hit che questo visitatore ha fatto, per tutte le visite (all&#39;interno dell&#39;intervallo di date selezionato).*

- In ogni hit, &quot;Value&quot; non contiene &quot;Example&quot; (yes), quindi restituisce true; allo stesso modo, &quot;Example&quot; non contiene &quot;Example&quot; (no, lo contiene), quindi restituisce false.
   - Se **qualsiasi** hit effettuato dal visitatore restituisce **true**, viene restituita la **visita intera**.
   - Se il visitatore non ha mai fatto alcun hit contenente &quot;Esempio&quot;, nessun hit restituirà true, e quindi quel visitatore **non verrà restituito** nel tuo set di dati.
- Anche in questo caso, a ogni hit &quot;Esempio&quot; contiene &quot;Esempio&quot; (sì), quindi restituisce true.
   - Se **un hit** restituisce **true**, l&#39;intero visitatore (e successivamente tutte le sue visite) sarà **escluso.**
   - Se **tutti gli hit** della visita restituiscono **false**, il visitatore verrà restituito nel tuo set di dati, restituendo in tal modo i visitatori che non hanno eseguito &quot;X&quot;.
- Si tratta di un’estensione della logica di visita, in cui sono presenti ulteriori considerazioni. Nell’esempio precedente ci sono due visitatori distinti, con 3 visite ciascuno:
   - Quando si utilizza &quot;Does Not Contain / Equal&quot; **verranno restituiti entrambi** visitatori e tutte le **tre** visite (che corrispondono a 2 visitatori e 6 visite totali nei report) verranno restituite
   - Quando si utilizza &quot;Escludi contiene/è uguale a&quot; **verrà restituito solo uno** di questi visitatori e verranno incluse solo le tre visite associate a quel visitatore (considerando 1 visitatore e 3 visite totali nei rapporti)

>[!TIP]
>
>Questa logica può essere complessa, soprattutto quando inizi a nidificare i contenitori... è sempre consigliabile eseguire test sui dati di esempio controllati per garantire che il segmento restituisca effettivamente i dati che ritieni debbano essere.

### Esempio di segmento 1: escludere le visite che effettuano un acquisto

In questo esempio, desidero eseguire il targeting degli utenti che hanno visitato un sito e che *non* hanno effettuato un acquisto durante la loro visita (in pratica, voglio escludere le visite che hanno eseguito una transazione; pertanto, rimarrò con le visite che non hanno completato una transazione)

![Segmento1A-VisitLevelExclude](assets/segment-example-1/segment1a-visit-level-exclude.png)

Per un confronto, vediamo un segmento creato utilizzando &quot;Non esiste&quot;:

![Segment1B-VisitDoesNotExist](assets/segment-example-1/sement1b-visit-does-not-exist.png)

Osserva come l’anteprima mostra un risultato molto diverso... infatti, questo segmento restituirà il 100% delle mie visite, perché ogni visita ha almeno un hit che non include la metrica &quot;Ordine&quot;.

Per illustrare ulteriormente questo aspetto, confrontiamo i due segmenti uno accanto all’altro:

![Segment1C-ComparisonTable](assets/segment-example-1/sement1c-comparison-table.png)

Innanzitutto, nonostante l&#39;ambito del livello *visita* del segmento, è possibile associare il segmento ad altre metriche (come visualizzazioni di pagina o visitatori univoci). Il primo set di colonne è desegmentato, per mostrare subito che l’unico segmento (inesistente) restituisce quasi il 100% dei dati; solo il segmento di esclusione esegue le operazioni che ci servono.

La colonna più evidente sono gli ordini, che dovrebbero essere immediatamente ovvi: il contenitore &quot;Non esiste&quot; è errato, poiché la maggior parte degli ordini viene ancora restituita.

### Esempio di segmento 2: escludi i visitatori che hanno effettuato un acquisto nel periodo di reporting

In questo esempio, voglio utilizzare le idee del campione precedente (che ha guardato specificamente al livello di visita) ed espanderlo per trovare i visitatori che non hanno effettuato un acquisto nell’intervallo di tempo del mio rapporto.

Questo segmento sarà molto simile all’esempio precedente, quasi identico, ma l’ambito del segmento farà una grande differenza.

![Segment2A-VisitorLevelExclude](assets/segment-example-2/segment2a-visitor-level-exclude.png)

Ora, se confrontiamo il segmento con ambito visitatore con il segmento con ambito visita riportato qui sopra, vedrai che molti più dati e molte altre visite sono escluse, dal momento che *visitatori che hanno effettuato acquisti* hanno avuto anche visite in cui non sono stati effettuati acquisti, e quindi anche queste visite sono escluse in quanto fanno parte del ciclo di vita del visitatore.

>[!IMPORTANT]
>
>Quando cerchi dati con ambito visitatore, più si allunga l’intervallo di tempo del rapporto, maggiore sarà l’esclusione, poiché molti visitatori saranno fedeli ai visitatori di ritorno al sito (ovviamente, alcuni modelli di business vedranno un impatto più elevato di altri)

![Segment2B-ComparisonTable](assets/segment-example-2/sement2b-comparison-table.png)


>[!IMPORTANT]
>
>Anche se le differenze tra visita e visitatore possono essere *impercettibili* (in particolare in questi dati di esempio), si tratta di una logica univoca che deve essere considerata. I dati possono essere notevolmente diversi a seconda del sito e dei comportamenti degli utenti.


È importante sapere esattamente quali dati, o quale *storia*, stai cercando di raccontare con il tuo report. Assicurati che le tabelle e le visualizzazioni comunichino chiaramente al pubblico ***cosa*** viene visualizzato e che l&#39;utilizzo del modello di segmento appropriato sia fondamentale per effettuare un&#39;analisi appropriata. Le decisioni informate possono essere prese correttamente solo se tutti capiscono cosa stanno guardando.

## Utilizzo dei contenitori

I contenitori consentono di creare una &quot;sublogica&quot; all’interno della logica principale del segmento. Un equivoco comune è che l’ambito deve essere lo stesso tra il segmento e il contenitore... ma non lo è. Questo ci dà più libertà di creare scenari specifici nel più grande schema delle cose, per costruire logiche complesse.

Il modo migliore per pensare ai contenitori è immaginare che ogni contenitore sia una scatola, e che possiamo impilare scatole (di logica) all&#39;interno di un&#39;altra scatola, all&#39;interno di un&#39;altra... ma a differenza delle scatole fisiche in cui ogni scatola deve essere più piccola della scatola esterna, possiamo mettere qualcosa di più grande all&#39;interno se questo ci porta a recuperare i dati corretti. Pensatela come un cappello da mago, dove l&#39;impossibile può stare dentro e noi siamo i maghi dei dati...

![Cappello_Coniglio](assets/rabbit-in-hat.jpeg)

### Ambito dei contenitori

Eseguiamo innanzitutto un raggruppamento rapido dell&#39;ambito *container*. Come per il *segmento s* ambito, hai le tue opzioni di ambito di base **hit**, **visita** e **visitatore**, ma a volte visualizzerai anche qualcosa denominato **gruppo logico** al posto di visitatore (questo si verifica solo all&#39;interno di segmenti sequenziali e saranno trattati nel prossimo articolo).

Per aggiungere contenitori nel segmento (o in altri contenitori) puoi accedere al menu **options*** (quando nidifichi più elementi, fai attenzione ad aggiungere al blocco corretto; tuttavia, puoi trascinare e rilasciare i contenitori all&#39;interno dell&#39;interfaccia se lo aggiungi alla posizione sbagliata)

**Figura 1: aggiunta di un contenitore**

![Figura1-AddingContainer](assets/figure1-adding-container.png)

L&#39;ambito di un contenitore è indipendente dal genitore, come ho detto sopra, questi *non* devono corrispondere, e a seconda di ciò che si desidera restituire, potrebbe essere necessario disegnare il piano per visualizzare completamente ciò di cui si ha bisogno, almeno fino a quando non si ottiene comodo visualizzarlo nella testa.

**Figura 2: ambito del segmento rispetto all&#39;ambito del contenitore**

![Figura2-SegmentScopeVsContainerScope](assets/figure2-segment-scope-vs-container-scope.png)

>[!NOTE]
>
>L&#39;Adobe ha una logica per comprendere i segmenti validi e non validi, non fornirebbe opzioni che potrebbero *mai* funzionare... quindi se vedi l&#39;opzione per utilizzare un contenitore con ambito visitatore all&#39;interno di un segmento con ambito hit, significa che è un&#39;opzione valida.

Proprio come per i segmenti di base, quando si inizia a creare un segmento complesso con contenitori nidificati, è necessario avere una chiara idea del ***tipo*** di dati che si desidera restituire. ***Come*** intendi utilizzare questi dati? ***Quali*** metriche intendi associare al segmento?

Queste domande aiuteranno a determinare quale sarà l’ambito del segmento nel suo insieme, questo è il punto di partenza per qualsiasi segmento.

Solo perché pensi di associare un segmento alla metrica dei visitatori univoci non significa che il segmento stesso debba essere a livello di visitatore... lungi dall’essere tale. Un segmento a livello di visitatore restituirà tutti i dati di un visitatore... questo significa tutte le sue visite, tutte le sue visualizzazioni di pagina ecc... una volta che un visitatore corrisponde ai criteri del segmento, il tuo segmento potrebbe iniziare a restituire i dati del *passato* per questo visitatore (purché sia all&#39;interno dell&#39;intervallo di date della tua area di lavoro).

>[!IMPORTANT]
>
>Anche quando si pianifica di associare un segmento alla metrica Visitatori univoci, *non significa* che il segmento debba essere automaticamente impostato come ambito visitatore... Questo equivoco *potrebbe* creare risultati gonfiati e non corretti.

Ho parlato molto dei concetti su come selezionare l’ambito appropriato, ma non ho fornito esempi o specifiche che ti aiuteranno davvero... quindi approfondiamo questo argomento con alcuni esempi di casi d’uso reali. Dicono che un mago non rivela mai i suoi segreti, ma non è proprio vero. All&#39;interno del mondo magico le tecniche e le lavorazioni &quot;dietro le quinte&quot; sono spesso condivise con i coetanei, consentendo loro di costruire e migliorare l&#39;illusione, e questo è ciò che intendo fare... per aprire la porta alle possibilità che vi attendono.

### Esempio di segmento 3: visualizzazioni su pagine specifiche da parte di visitatori che hanno effettuato un ordine recente (all’interno del periodo di reporting)

In questo scenario, voglio solo restituire un set di pagine specifiche che sono state visitate da acquirenti recenti (tieni presente che posso ancora associarlo a visite o visitatori univoci, anche se il segmento stesso si troverà in un ambito HIT).

Questo tipo di scenario è utile per verificare se alcuni acquirenti visualizzano pagine specifiche di un sito, pagine che potrebbero non essere collegate in modo esplicito a un evento specifico.

Nel mio esempio vedrò le pagine di &quot;Offerte consigliate&quot; e &quot;Prodotti consigliati&quot;. Attualmente, la logica sarà semplice e non verrà inserita nella segmentazione sequenziale (almeno non ancora, ma in un articolo futuro verrà trattata una logica più complessa come questa).

Un&#39;altra domanda è **perché** stiamo richiamando tramite hit? Tecnicamente posso richiamare qui tramite Visite o Visitatori, ma posso anche esaminare queste pagine specifiche per **visualizzazioni di pagina (per il set di pagine specifico) per visita** o **visualizzazioni di pagina (per il set specifico) per visitatore**, questo ambito mi offre la flessibilità di eseguire questa matematica specifica. Poiché questi hit possono essere facilmente abbinati a visite o visitatori univoci per determinare il numero di visite o visitatori che visualizzano queste pagine, opterò per il segmento più flessibile che posso utilizzare per tutti gli scenari.

Innanzitutto, per un confronto, ecco un segmento semplice basato su HIT per le pagine specifiche.

![Segment3A-HitLevelPages](assets/segment-example-3/segment3a-hit-level-pages.png)

Ora, prendiamo in considerazione la complessità:

![Segment3B-MultipleContainersHitAndVisitor](assets/segment-example-3/segment3b-multiple-containers-hit-and-visitor.png)

Noterai che non utilizzo solo più contenitori, ma che sto mescolando l’ambito di tali contenitori. Il segmento nel suo complesso è a livello di HIT, ma sto anche cercando i VISITATORI che hanno effettuato un ordine.

![Segment3C-ComparisonTable](assets/segment-example-3/segment3c-comparison-table.png)

Passiamo un po&#39; di tempo a svelarlo, visto che sta succedendo molto.

In primo luogo, invece di mostrare un raggruppamento giornaliero, sto mostrando un raggruppamento di pagina, perché penso che questo aiuterà a illustrare meglio i due segmenti.

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Le prime tre colonne (Visualizzazioni di pagina, visite e visitatori univoci) non sono segmentate e quindi mostrano tutte le pagine all’interno del sito. Non ho incluso gli ordini qui, poiché gli ordini vengono tracciati su un'azione, e quindi non fanno parte dell'ambito della dimensione pagina.</td>
        <td style="border: 0;">&lt;img src="assets/segment-example-3/segment3c-comparison-table-detail1.png" width="352"
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Ora mostro il risultato del segmento semplice, osservando solo <strong>hit</strong> nelle due pagine specificate. Noterai che tutte le altre pagine del raggruppamento restituiscono 0, come previsto.</td>
        <td style="border: 0;">&lt;img src="assets/segment-example-3/segment3c-comparison-table-detail2.png" width="352"
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Ora, ecco un piccolo suggerimento bonus, prima di mostrare il risultato del segmento avanzato, ho usato un altro semplice segmento di "Orders Exists" (a un ambito di livello HIT), e ho abbinato con visitatori unici. Questo mi restituirà il totale di UV che hanno effettuato ordini nel mio periodo di rapporto, così come i UV che hanno colpito ognuna di quelle pagine... questo aiuterà a illustrare meglio il prossimo set di colonne.</td>
        <td style="border: 0;">&lt;img src="assets/segment-example-3/segment3c-comparison-table-detail3.png" width="352"
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Il set finale di colonne viene impilato con il segmento complesso. Il totale di UV con ordini corrisponde al segmento semplice "Ordini esistenti" in ogni pagina, ma noterai che il totale è significativamente diverso; poiché questo set di dati limita esplicitamente il set di dati solo ai visitatori che hanno effettuato ordini E hanno raggiunto le pagine, sono esplicitamente interessato a.</td> <td style="border: 0;"><img src="assets/segment-example-3/segment3c-comparison-table-detail4.png" width="352">
        </td>
    </tr>
</table>

### Esempio di segmento 4: visite che hanno avuto luogo con offerte in primo piano O prodotti consigliati E che hanno effettuato un ordine all’interno della stessa visita

L’esempio precedente ha mostrato come aggiungere un contenitore con ambito maggiore (ad esempio visitatore) all’interno di un contenitore con ambito più piccolo (ad esempio hit, in modo da non sorprendere che sia possibile aggiungere contenitori di hit all’interno di segmenti con ambito visitatore o visita).

Utilizzando alcune delle pagine che stavamo consultando in precedenza, ora ci preoccupiamo solo di recuperare i visitatori che sono capitati colpire le offerte in primo piano O la pagina di prodotti consigliati e ha fatto un ordine all&#39;interno della stessa visita.

![Segment4A-VisitorWithVisit](assets/segment-example-4/segment4a-visitor-with-visit.png)

Questo segmento combina tutti e tre gli ambiti. Il livello superiore del segmento è visitatore, in modo che tutti gli hit di tutte le visite vengano restituiti per il visitatore corrispondente. All’interno di, abbiamo aggiunto un contenitore ambito visita per garantire che il visitatore abbia avuto almeno una visita corrispondente ai criteri specifici per effettuare un ordine E aver visitato pagine specifiche. È stato aggiunto un contenitore ambito hit per le pagine stesse, in modo da poter utilizzare la logica OR per cercare la pagina delle offerte in primo piano O la pagina dei prodotti consigliati.

Il vantaggio per questo segmento con ambito visitatore è che questo restituirà **TUTTE** le visite dei visitatori che corrispondono a questo criterio, quindi questo segmento sarà buono se voglio vedere i comportamenti nelle visite precedenti che precedono questa combinazione e le azioni di questi visitatori dopo uno scenario del genere.

![Segment4B-ComparisonTable](assets/segment-example-4/segment4b-comparison-table.png)

Qui sto confrontando gli hit su offerte in primo piano/contenuti consigliati, agli ordini esistenti, al segmento complesso in cui sia l’ordine che una delle pagine specificate esistono nella stessa visita. Il segmento complesso è quello in cui i primi due segmenti si intersecano; ma poiché il suo ambito visitatore, verranno restituite anche tutte le altre visite per tali visitatori.

## Modello di attribuzione

La modellazione dell’attribuzione all’interno di una definizione di segmento si riferisce principalmente a dimensioni che non hanno una scadenza hit, pertanto le proprietà (che sono sempre a livello di hit) non sono un buon candidato. Le eVar, i canali di marketing, ecc. tuttavia, sono realmente ciò per cui queste impostazioni sono progettati.

Prima di esaminare il segmento, è necessario rivedere rapidamente il funzionamento della modellazione di attribuzione in un semplice esempio.

Supponiamo di avere due eVar, una delle quali è impostata per la scadenza (eVar1) e una per la scadenza di 30 giorni (eVar2). Per semplicità, stiamo per tenere traccia di una campagna interna (icid).

**Visita 1**

- Pagina A
   - **eVar1** non è impostato
   - **eVar2** non è impostato
- Fai clic sul banner promozionale con ?icid=promo-banner nell’URL
- Pagina B
   - **eVar1** e **eVar2** sono impostati su &quot;promo-banner&quot;
   - **Istanza di eVar1** attivata
   - **Istanza di eVar2** attivata
- Pagina C
   - Sia **eVar1** che **eVar2** mantengono il valore &quot;promo-banner&quot;
   - Nessuna delle metriche di istanza per le eVar viene attivata, in quanto entrambe le eVar utilizzano valori persistenti

**Visita 2**

- Pagina D
   - **eVar1** non è impostato su alcun valore e non viene attivata alcuna **istanza di eVar1**
   - **eVar2** mantiene il valore &quot;promo-banner&quot; a causa della scadenza di 30 giorni
   - **L&#39;istanza di eVar2** non è attivata perché il valore è persistente e non impostato
- Fai clic sulla promozione Side Rail con ?icid=promo-side-rail in the URL
- Pagina E
   - **eVar1** e **eVar2** sono impostati su &quot;promo-side-rail&quot;
   - **Istanza di eVar1** attivata
   - **Istanza di eVar2** attivata
- Pagina F
   - Sia **eVar1** che **eVar2** mantengono il valore &quot;promo-side-rail&quot;
   - Nessuna delle metriche di istanza per le eVar viene attivata, in quanto entrambe le eVar utilizzano valori persistenti

Attualmente, il risultato atteso di queste due visite è il seguente:

<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top"></th><th colspan="1" valign="top"><b>Page Views</b></th><th colspan="1" valign="top"><b>Visite</b></th><th colspan="1" valign="top"><b>Istanza di eVar1</b></th><th colspan="1" valign="top"><b>Istanza di eVar2</b></th></tr>
<tr><td colspan="1" valign="top"></td><td colspan="1" valign="top"></td><td colspan="1" valign="top">6</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" rowspan="7" valign="top">Pagina</td><td colspan="1" valign="top"></td><td colspan="1" valign="top">6</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" valign="top">Pagina A</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
<tr><td colspan="1" valign="top">Pagina B</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">Pagina C</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
<tr><td colspan="1" valign="top">Pagina D</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
<tr><td colspan="1" valign="top">Pagina E</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">Pagina F</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
</table>

<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top"></th><th colspan="1" valign="top"><b>Page Views</b></th><th colspan="1" valign="top"><b>Visite</b></th><th colspan="1" valign="top"><b>Istanza di eVar1</b></th></tr>
<tr><td colspan="1" valign="top"></td><td colspan="1" valign="top"></td><td colspan="1" valign="top">4</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">EVAR 1</td><td colspan="1" valign="top"></td><td colspan="1" valign="top">4</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" valign="top">banner promozionale</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">promo-side-rail</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
</table>

<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top"></th><th colspan="1" valign="top"><b>Page Views</b></th><th colspan="1" valign="top"><b>Visite</b></th><th colspan="1" valign="top"><b>Istanza di eVar2</b></th></tr>
<tr><td colspan="1" valign="top"></td><td colspan="1" valign="top"></td><td colspan="1" valign="top">5</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">EVAR 2</td><td colspan="1" valign="top"></td><td colspan="1" valign="top">5</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" valign="top">banner promozionale</td><td colspan="1" valign="top">3</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">promo-side-rail</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
</table>

Ora vediamo dove puoi impostare l’attribuzione nel segmento.

**Figura 4: modello di attribuzione**

![Figura4-ModelloAttribuzione](assets/figure4-attribution-model.png)

*L&#39;icona a forma di ingranaggio nella dimensione è il punto in cui puoi impostare l&#39;attribuzione. Ogni opzione include informazioni disponibili quando si passa il puntatore del mouse su &quot;?&quot; icona. Fondamentalmente:*

- Il comportamento predefinito restituisce tutte le istanze dell’eVar in cui è impostato il valore (in modo specifico o tramite l’attribuzione set)
- L’istanza restituirà solo la dimensione in cui il valore è impostato esplicitamente (ovvero sugli hit in cui viene attivata l’istanza di eVar)
- L’istanza non ripetuta restituirà solo la prima volta che viene impostato il valore della dimensione (ad esempio, anche se non trattata nell’esempio precedente, immagina che l’utente abbia fatto clic più volte sul banner promozionale, questo incrementerà anche l’istanza di eVar per ogni volta che si fa clic sul banner, questa impostazione prenderà solo la prima istanza univoca di &quot;promo-banner&quot; e ignorerà eventuali conteggi successivi di questo banner)

### Esempio di segmento 5: canale di marketing &quot;Paid Search&quot; (Ricerca a pagamento) rispetto alle istanze dirette di ricerca a pagamento

Come tutti sappiamo, i canali di marketing hanno un modello di attribuzione lungo (30 giorni per impostazione predefinita, ma che potrebbe essere personalizzato in base alle tue esigenze) e una volta impostato, il canale di marketing non verrà sovrascritto da successive visite &quot;dirette&quot; al sito, in modo che i driver specifici ottengano l’attribuzione di conversione. Tuttavia, a volte è necessario visualizzare in modo specifico le ***voci*** nel sito da un canale di marketing specifico; e per voci, intendo che devi vedere quando il canale di marketing è impostato in modo specifico in base alle regole di elaborazione marketing.

Iniziamo con il cambiare le cose guardando i confronti, poi approfondiamo i segmenti.

![Segment5A-TableComparison](assets/segment-example-5/segment5a-table-comparison.png)

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Le prime 4 colonne non sono segmentate e devono essere di facile comprensione. Tieni presente che *"Voci"* è fondamentalmente un valore calcolato in base al punto in cui i visitatori iniziano la sessione. L’ho aggiunto qui per mostrare che questo non restituisce le informazioni che stiamo cercando, poiché gli utenti possono accedere al sito tramite più canali di marketing (attraverso l’osservazione dei social media, l’esecuzione di ricerche, il clic sulle e-mail di marketing, ecc.). tutto all’interno della stessa visita/sessione).</td> <td style="border: 0;"><img src="assets/segment-example-5/segment5a-table-comparison-detail1.png" width="352">
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Il prossimo set di colonne utilizza un "Segmento hit standard", che esamina fondamentalmente gli hit in cui il canale di marketing è la "ricerca a pagamento". Tuttavia, questo restituirà TUTTI gli hit in base all’attribuzione Marketing Channel, non isolerà i click-through effettivi di "Ricerca a pagamento". Pertanto, questo non restituirà i dati di cui abbiamo bisogno.</td> <td style="border: 0;"><img src="assets/segment-example-5/segment5a-table-comparison-detail2.png" width="352">
        </td>
    </tr>
</table>


![Segmento5A-PaidSearchHit](assets/segment-example-5/segment5a-paid-search-hit.png)

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Ora, i due gruppi di dati successivi sembrano identici, e infatti, questi restituiranno gli stessi dati in due modi diversi. Ma ora sto cercando in modo specifico le <i>istanze</i> in cui il canale di marketing era <strong>impostato</strong> su "Ricerca a pagamento".</td> <td style="border: 0;"><img src="assets/segment-example-5/segment5a-table-comparison-detail3.png" width="352">
        </td>
    </tr>
</table>

Ciò può essere fatto in due modi:

Innanzitutto, viene utilizzata l&#39;attribuzione della dimensione &quot;standard&quot; e viene associata alla metrica specifica &quot;Istanza canale di marketing&quot; (come logica *exists*):

![Segment5A-PaidSearchHitANDInstanceExists](assets/segment-example-5/segment5a-paid-search-hit-and-instance-exists.png)

In secondo luogo, per un segmento più semplice, puoi modificare l’attribuzione in &quot;Istanza&quot;. Tieni presente che il nome della dimensione cambierà da &quot;Canale di marketing&quot; a &quot;Canale di marketing (istanza)&quot;.

![Segmento5A-PaidSearchHitInstance](assets/segment-example-5/segment5a-paid-search-hit-instance.png)

## Tutti gli elementi insieme

Come ogni buon mago, possiamo iniziare con ogni singolo trucco, costruendo il pubblico mentre andiamo, portandolo al &quot;prestigio&quot; finale. Qui è dove brilliamo davvero, prendendo tutti i piccoli trucchi, e li arrotoliamo in un gran finale. Prendere le parti apparentemente sconnesse del trucco, e mostrare che in realtà, lavorano tutti insieme per formare un tutto coeso.

![Coniglio_Fuoco](assets/fire-bunny.jpeg)


### Esempio di segmento 6: visitatori che hanno effettuato un ordine durante una visita con un’istanza social a pagamento ed esclusi i visitatori iscritti a una newsletter

![Segmento6A-VisitorsPurchasingFromPaidSocialWithNoNewsletter](assets/segment-example-6/segment6a-visitors-purchasing-from-paid-social-with-no-newsletter.png)

Questo mi consentirà di identificare i visitatori che hanno effettuato attivamente un acquisto durante una visita da una campagna social media ma che non si sono iscritti alle nostre newsletter. Questo consentirà al nostro team di marketing di vedere il potenziale gruppo di utenti che tenteranno di convertire newsletter ed e-mail di marketing.

## Finale

![Stage](assets/theater-stage.jpeg)

Ci sono così tanti modi per combinare la logica e ottenere in scenari molto dettagliati, che posso solo grattare la superficie delle possibilità.

Come ogni grande mago, il vero potere è nell&#39;ispirare la generazione futura a costruire sulle basi, a reimmaginare le scoperte in qualcosa di nuovo e meraviglioso! Non vedo l&#39;ora di vedere cosa ne pensate tutti!

## Autore

Questo documento è stato scritto da:

![Jen Headshot](assets/jen-headshot.png)

Jennifer Dungan, Optimization Manager Analytics di Torstar

Adobe Analytics Champion

