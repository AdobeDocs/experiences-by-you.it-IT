---
title: Creazione di modelli di punteggio persona per i programmi di Marketo Engage
description: Adobe Marketo Engage consente di creare modelli di punteggio dalla base. Prima di passare direttamente al Marketo Engage per creare i programmi di punteggio, devi impostare i campi di punteggio essenziali, ad esempio Punteggio demografico, Punteggio comportamentale e Punteggio persona totale. Scopri di più sulle strategie utilizzate dai campioni di Marketo Engage per sviluppare modelli di punteggio di cui la tua azienda ha bisogno.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-04T00:00:00Z
jira: KT-14810
thumbnail: KT-14810.jpeg
source-git-commit: 47ab8875bc4e41595cd40550330e43a88357b68d
workflow-type: tm+mt
source-wordcount: '2111'
ht-degree: 2%

---

# Creazione di un modello di punteggio persona

Il punteggio di persona ti aiuta a identificare le persone più coinvolte nella tua azienda e sono il tuo profilo cliente ideale, in modo da poter condividere tali lead con il team di vendita e concludere le offerte. Insieme alle vendite, è possibile determinare quali lead si desidera consegnare a loro utilizzando un programma di punteggio lead/persona in Adobe Marketo Engage. Questo può essere determinato da un punteggio comportamentale minimo, da un punteggio demografico, o da entrambi.

In questo tutorial, ti guideremo attraverso tre esercizi suggeriti dai campioni di Marketo Engage Christina Zuniga e Katja Keesom. Segui questa procedura per determinare quali attività e caratteristiche sono indicatori importanti che un potenziale cliente è interessato ad acquistare (punteggio comportamentale), è adatto a te (punteggio demografico) e ne tiene conto nei diversi mercati.

## Perché sviluppare e utilizzare un modello di punteggio della persona?

Potresti avere molti lead nel tuo database, ma come fai a sapere quali sono pronti per acquistare i tuoi prodotti e servizi ora? Mentre la tua organizzazione di marketing cerca di ottimizzare la qualità dei lead e la fattibilità delle vendite, è qui che entra in gioco il modello di punteggio.

Tramite il punteggio delle persone nel database di Marketo Engage, puoi misurare la qualifica dei lead generati e impostare i criteri per quando sono pronti per le vendite. Questo consente al team vendite di concentrarsi sui lead che hanno più probabilità di chiudere, mentre il team marketing continua a nutrire le altre persone nel database tramite i loro programmi di marketing.

## Esercizio 1 - Determinazione degli interessi dei buyer con punteggi comportamentali

Il punteggio comportamentale dà un valore numerico alle azioni tracciabili intraprese da un potenziale cliente che indicano interesse per i tuoi prodotti e servizi e intenzione di acquistare. Ad esempio, la visita del sito web mostra interesse e la visita della pagina di determinazione dei prezzi può mostrare intento. Al contrario, visitare la pagina carriere potrebbe indicare che la persona non sta per acquistare.

**Passaggio 1** - Crea un elenco delle attività potenziali che sono importanti per il tuo processo di vendita o che sono importanti per la tua organizzazione. Può essere utile collaborare con il team di vendita per determinare quali attività indicano che un lead ha l’intenzione di acquistare, aiutandoti ad allineare i criteri con le vendite e a stabilire le priorità in base alle osservazioni di offerte chiuse. Di seguito sono riportate alcune domande che è possibile porre al team di vendita:

* Quali attività indicano un lead buono o cattivo per te?
* Quale tipo di contenuto utilizzato da un lead ha un’intenzione di acquisto più forte?

**Passaggio 2** : elenca le azioni che indicano che un potenziale cliente non è interessato al tuo prodotto. Assicurati di elencare le attività tracciabili attraverso il Marketo Engage.

**Esempio 1a - Attività che indicano l’intenzione di acquistare**

| **Attività che indicano l’intenzione di acquistare** | **Attività che indicano l’ASSENZA dell’intenzione di acquistare** |
| --- | --- |
| Pagina dei prezzi delle visite | Nessuna interazione negli ultimi 90 giorni |
| Partecipa all’evento annuale per il cliente | Pagina Visita carriere |
| Registrati al webinar | Annullamenti iscrizioni |
| Download del white paper |     |
| Compila il modulo demo della richiesta |     |

**Passaggio 3** - Analizza e scegli un punteggio di soglia per la distribuzione delle vendite.

* Quando un lead indica un interesse sufficiente eseguendo alcune delle attività definite nel passaggio 1 e il punteggio totale supera questa soglia, le distribuirà alle vendite. Questa soglia sarà semplicemente un numero che aiuta a impostare un benchmark per i punteggi assegnati ai singoli comportamenti.
* Il numero di soglia deve essere abbastanza grande da consentire a una persona di completare più interazioni con il brand per soddisfarla. Ad esempio, è improbabile che un’e-mail aperta sia un qualificatore sufficiente. Se hai appena iniziato, prova a lavorare con una soglia di 100 e da lì puoi costruire il tuo punteggio di persona.
* L&#39;impostazione di una soglia alta o bassa dipende dai lead che il team di vendita è più interessato a ricevere e sviluppare in opportunità di business. Se disponi di dati sui tuoi recenti affari di vendita, analizzali e scopri quali azioni le persone hanno intrapreso per concludere affari di successo. Questo consente di determinare quanti punti di contatto entrano in un lead di vendita qualificato e di estrapolare da lì il numero di soglia.

**Esempio 1b - Soglia per handoff vendite:**

| Numero medio di punti di contatto per il lead qualificato | 4 |
| --- | --- |
| Soglia per trasferimento vendite | 50 |

**Passaggio 4** - Assegna un punteggio a ciascuna attività elencata nell’esempio 1a - Attività che indicano l’intenzione di acquistare.

* Utilizza un punteggio di comportamento positivo per le attività che indicano un interesse per aumentare il punteggio di lead complessivo di un potenziale cliente e un punteggio negativo per indicare un disinteresse.
* Utilizzando come parametro di riferimento la soglia dell’esempio 1b - Soglia per l’handoff delle vendite, determina i punteggi di comportamento relativi all’importanza delle loro azioni. Ad esempio, i potenziali clienti che richiedono una demo devono passare direttamente al reparto vendite. L’assegnazione di tale azione a un valore punto uguale alla soglia di handoff del potenziale cliente ha più senso. Nel frattempo, scaricare un white paper non è un indicatore altrettanto forte di acquisto di interesse e quindi dovrebbe valere meno punti.

**Esempio 1c - Punteggio delle attività che indicano l’intenzione di acquistare:**

| Soglia per trasferimento vendite = 50 punti |     |
| --- | --- |
| Attività | Punteggio |
| Compilato &quot;richiedi un modulo demo&quot; | +50 |
| Nessuna interazione negli ultimi 90 giorni | \-10 |
| Scarica un white paper | +5 |
| Visitateci ad una fiera | +15 |

**Passaggio 5** - Ricorda, il punteggio è un processo iterativo! Esamina e regola continuamente punteggi e soglie mentre raccogli più dati da analizzare.

## Esercizio 2 - Identificazione della giusta corrispondenza con i punteggi demografici

Dopo aver definito le attività che indicano l’intento di acquisto, è necessario completare il modello di punteggio con i profili potenziali ideali. Per identificare se un potenziale cliente è adatto a ulteriori conversazioni di vendita, è importante assegnare punteggi demografici oltre ai punteggi comportamentali in modo che il modello possa aiutare a determinare i lead migliori in termini di adattamento e intento.

**Passaggio 1** - Crea un elenco di caratteristiche per i tuoi potenziali clienti ideali.

* Valuta l’inserimento di attributi quali il settore, l’azienda, il reparto e il ruolo. Assicurati che queste caratteristiche corrispondano ai campi demografici disponibili nell’istanza del Marketo Engage.
* Collabora con il tuo team di vendita per individuare i lead che rispondono maggiormente alle richieste di informazioni sulle vendite e che sono i contatti chiave durante le opportunità di vendita.
   * Può essere utile analizzare le recenti opportunità realizzate e chiuse per vedere quali caratteristiche hanno i tuoi clienti migliori. Ad esempio,
      * Sfogliare le opportunità perse chiuse per i modelli può portare a trovare i dati demografici che si desidera evitare.
      * Identifica i decision-maker e i campioni interni che contribuiscono alle tue attività di vendita. Approfondisci i dati e porta i tuoi risultati a un workshop con alcuni membri del tuo team di vendita per convalidare o perfezionare le tue conclusioni.
   * Puoi anche intervistare il tuo team di vendita per rispondere alle seguenti domande:
      * Con quale reparto sono solitamente coinvolti?
      * Quali sono i titoli professionali delle persone coinvolte nelle demo dei prodotti e chi sono le persone che devono firmare l&#39;acquisto?

**Esempio 2a - Caratteristiche ideali per i potenziali clienti**

| **Categoria** | **Caratteristiche ideali per i clienti potenziali** |
| --- | --- |
| Settore | Aerospaziale, Produzione |
| Dimensione società | 100 - 999, 1.000 - 9.999 |
| Qualifica | Director, Vice President, C-Level |
| Reparto | ORE |

**Passaggio 2** - Assegna un punteggio a ciascuna caratteristica in base alla sua rilevanza nel tuo profilo potenziale ideale. Utilizza punteggi positivi per le caratteristiche desiderate e punteggi negativi per le caratteristiche che rendono il lead meno adatto al tuo prodotto.

**Esempio 2b - Assegnazione di punteggi a caratteristiche prospect ideali e indesiderate**

| **Caratteristica** | **Punteggio** |
| --- | --- |
| Settore - Aerospaziale | +10 |
| Industria - Produzione | +5 |
| Dimensione società - 100 - 999 | +5 |
| Dimensione società - 1.000 - 9.999 | +10 |
| Dimensione società - &lt;10 | \-10 |

## Esercizio 3: Integrazione della flessibilità locale nel modello di punteggio

Con i modelli comportamentali e demografici di base che hai completato, puoi portarlo al livello successivo consentendo flessibilità locale. I valori aziendali possono variare in mercati diversi quando un’organizzazione opera a livello globale. Nell&#39;esercizio seguente verrà illustrato come applicare i punteggi per riflettere il valore aziendale reale delle attività o delle caratteristiche del lead in situazioni diverse.

Preferisci un video per questo esercizio? Partecipa come la campionessa del Marketo Engage Katja Keesom dimostra di costruire flessibilità locale nel modello di punteggio.

>[!VIDEO](https://video.tv.adobe.com/v/3426914/?learn=on)

**Passaggio 1** - Prendere le attività e le caratteristiche degli esercizi 1 e 2 e determinare per ogni articolo se variano in base alla posizione o alla linea di prodotti.

**Esempio 3a - Segnali nei mercati globali e locali:**

| **Segnale** | **Globale** | **Locale** |
| --- | --- | --- |
| Attività | <ul><li>Modulo &quot;Richiedi una demo&quot; compilato</li><li>Nessuna interazione negli ultimi 90 giorni (circa 3 mesi)</li></ul> | <ul><li>Visitateci all&#39;evento</li><li>Scarica un white paper</li></ul> |
| Caratteristiche | <ul><li>Reparto</li><li>Qualifica</li></ul> | <ul><li>Settore</li><li>Dimensione società</li></ul> |

**Passaggio 2** - Definire la matrice di punteggio per i mercati locali:

* Imposta una matrice diversa per gli elementi demografici e comportamentali.
* Determina gli argomenti di priorità su cui chiedere il contributo del team locale.
* Definisci il numero di valori utilizzati per la valutazione all&#39;interno degli argomenti.
* Assegna singoli valori allineando il valore relativo ai punteggi globali.
* Valuta la possibilità di definire scenari comuni quando i potenziali clienti interagiscono con il tuo marchio e di testare il tuo punteggio complessivo al riguardo.
   * Ad esempio, un percorso di potenziali clienti comune potrebbe essere quello di consentire a un utente di accedere al sito Web in una pagina di contenuto, quindi di passare a una pagina di prodotto e scaricare una brochure. Dovresti indirizzare loro un invito al webinar, e loro rispondono registrandosi, ma non partecipando. Valuta se le tue vendite vogliono già parlare con questa persona o no e valuta se il tuo modello di punteggio ottiene questi potenziali al punteggio complessivo giusto per riflettere quel livello di interesse.

**Esempio 3b - Matrice di punteggio demografico:**

| **Matrice demografica** | **Priorità 1** | **Priorità 2** | **Priorità 3** |
| --- | --- | --- | --- |
| Valori alti | 20 punti | 10 punti | 7 punti |
| Valori medi | 10 punti | 7 punti | 3 punti |
| Valori bassi | 5 punti | 3 punti | 1 punto |

**Passaggio 3** - Raccogliere i contributi dei team di vendita locali o regionali per sviluppare una visione olistica. Nell’esempio 3c non sono inclusi punteggi individuali. Questo consente al team vendite di concentrarsi sul valore relativo dei diversi argomenti durante il processo di revisione. Tuttavia, è necessario che il modello completo sia documentato come materiale di base per gli altri amministratori di Marketo Engage.

* Blocca ciò che non può essere regolato per la coerenza globale (qui nella colonna &quot;Implementa argomento&quot;).
* Contrassegna (qui nelle colonne &quot;Priorità&quot; e &quot;Punteggio&quot;) cosa può essere regolato per le influenze locali.

**Esempio 3c - Validità relativa degli argomenti di punteggio:**

<table>
 <tr>
    <th>#</th>
    <th>Implementare l’argomento</th>
    <th>Demografico/Comportamentale</th>
    <th>Argomento</th>
    <th>Priorità</th>
    <th>Valori</th>
    <th>Punteggi</th>
 </tr>
 <tr>
    <td rowspan="6">1</td>
    <td rowspan="6"><b>OBBLIGATORIO</b></td>
    <td rowspan="6">Demografico</td>
    <td rowspan="6">Settore</td>
    <td rowspan="6"><b>2</b></td>
    <td>Tecnologia</td>
    <td><b>Alta</b></td>
  </tr>
  <tr>
    <td>Moda</td>
    <td><b>Alta</b></td>
  </tr>
  <tr>
    <td>Vendita al dettaglio</td>
    <td><b>Canale</b></td>
  </tr>  
  <tr>
    <td>Produzione</td>
    <td><b>Canale</b></td>
  </tr>
  <tr>
    <td>Assistenza sanitaria</td>
    <td><b>Bassa</b></td>
  </tr>
  <tr>
    <td>...</td>
    <td><b>Bassa</b></td>
  </tr>
<tr>
    <td rowspan="3">2</td>
    <td rowspan="3"><b>Sì</td>
    <td rowspan="3">Demografico</td>
    <td rowspan="3">Dimensione società (dipendenti)</td>
    <td rowspan="3"><b>3</td>
    <td>&gt;1000 dipendenti</td>
    <td><b>Alta</td>
  </tr>
  <tr>
    <td>250-999 dipendenti</td>
    <td><b>Canale</td>
  </tr>
  <tr>
    <td>1-249 dipendenti</td>
    <td><b>Bassa</td>
  </tr>  
<tr>
    <td rowspan="3">3</td>
    <td rowspan="3"><b>No</b></td>
    <td rowspan="3">Comportamento</td>
    <td rowspan="3">Visite pagina sul sito web</td>
    <td rowspan="3"><b>2</b></td>
    <td>&gt;Pagine delle informazioni sui prodotti</td>
    <td><b>Bassa</b></td>
  </tr>
  <tr>
    <td>Pagine di determinazione prezzi</td>
    <td><b>Canale</b></td>
  </tr>
  <tr>
    <td>Pagina di richiesta demo</td>
    <td><b>Alta</b></td>
  </tr>
</table>

## Quali sono le prossime novità?

* Scarica il file [foglio di esercizio punteggio persona](./assets/build-person-scoring-model-and-local-flexibility-in-adobe-marketo-engage.docx){target="_blank} per sviluppare il modello di punteggio offline.
* Crea il punteggio della persona nel Marketo Engage. Seleziona questa [esercitazione](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-watch){target="_blank} e [demo](https://experienceleague.adobe.com/en/docs/events/marketo-and-mochas-recordings/2023/lead-scoring){target="_blank} per iniziare. È possibile importare un programma di punteggio lead/persona [modello](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/import-a-program){target="_blank} dalla libreria di riferimento di Marketo Engage per accelerare la creazione del programma.
* Creare due versioni del programma di assegnazione del punteggio:
   * Un programma centrale che esegue tutti i punteggi che non possono essere aggiornati localmente.
   * Una copia locale con gli elementi di punteggio configurabili.
* Imposta i valori di punteggio come token all’interno del programma di punteggio. Ciò garantisce la coerenza anche quando si modificano i punteggi nel tempo.
   * Un esempio comune di punteggi tokenizzati è l’utilizzo di un token per attività di valore elevato che soddisfano automaticamente la soglia, ad esempio la richiesta di una demo o la prenotazione di una riunione con il team di vendita. Anche se modifichi il punteggio minimo richiesto per raggiungere la soglia, puoi aggiornare facilmente tutte le attività di valore elevato contemporaneamente aggiornando un token.
* Regola la tua Smart Campaign locale per ogni posizione:
   * Determina quali attività demografiche e comportamentali devono ottenere un punteggio solo una volta (ovvero l’industria) e quali devono ottenere un punteggio ogni volta che un potenziale cliente si qualifica (ad esempio, ha partecipato a un webinar). In questo modo i potenziali contatti attivati dalla modifica del valore dei dati sono rilevanti per le vendite.
   * Assicurati che le scelte siano reciprocamente esclusive.
   * Effettua gli aggiornamenti in entrambi i passaggi del flusso in modo che il Punteggio persona venga aggiornato in modo identico al Punteggio demografico. In questo modo, il punteggio della persona rimane in linea con la combinazione di punteggio di comportamento e punteggio demografico.
* Dopo aver completato la creazione del programma, verifica la campagna avanzata. Ad esempio, vai al modulo demo, compilalo con un’e-mail di test e controlla il punteggio del test in [database di Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started-with-marketo/quick-wins/simple-scoring#step-view-the-person-info){target="_blank}.
* Dopo aver creato il modello, puoi impostare un avviso per passare alle vendite una volta che il punteggio della persona ha raggiunto la soglia di handoff vendite. Ulteriori informazioni sulla configurazione di un avviso con questo [esercitazione](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/send-alert){target="_blank}.

### Autori

{{christina-zuniga}}

{{katja-keesom}}

{{amy-chiu}}