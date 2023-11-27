---
title: Porta l’analisi dei dati a un livello successivo con le Metriche calcolate
description: Scopri in che modo un esperto peer utilizza le metriche calcolate per creare nuove metriche senza modificarne l’implementazione e utilizzando i dati già raccolti per rispondere a domande di business complesse.
feature-set: Analytics
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
exl-id: 301ee179-b154-4cf2-b27e-77f38a8945a0
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '1549'
ht-degree: 2%

---

# Porta l’analisi dei dati a un livello successivo con le Metriche calcolate

La maggior parte dei nuovi utenti di [!DNL Adobe Analytics] hanno familiarità con i Segmenti per suddividere i dati. Oggi voglio presentarvi le metriche calcolate, il prossimo strumento migliore nella vostra casella degli strumenti di analisi.

Come funzionalità avanzata di [!DNL Adobe Analytics], le metriche calcolate ti consentono di creare nuove metriche senza modificare l’implementazione utilizzando i dati già raccolti. Il Generatore di metriche calcolate può utilizzare molte funzioni matematiche e statistiche diverse, quindi puoi creare metriche che rispondono anche alle domande di business più complesse.

## Introduzione alle metriche calcolate

Per iniziare a usare le metriche calcolate, vediamo un semplice esempio. Immagina di voler capire se gli utenti self-service online hanno un valore medio di ordine (AOV) più alto rispetto agli utenti assistiti da chiamate. Per creare una metrica calcolata che risponda a questa domanda, effettua le seguenti operazioni:

Per aprire il Generatore di metriche calcolate, utilizza la navigazione superiore per fare clic su → **Componenti** → **Metriche calcolate** → **+ Aggiungi.** In alternativa, è possibile fare clic su **segno +** sopra **Metriche** nel pannello Componenti.


![Calc. 01](assets/calc01.png) ![Calc. 02](assets/calc03.png) ![Calc. 03](assets/calc02.png)

![Calc. 04](assets/calc04.png)

*Descrizioni di seguito per gli elementi dell’interfaccia utente*

Una volta aperto il Generatore di metriche calcolate, aggiungi e/o fai quanto segue:

**R.** Un nome per la metrica calcolata. Questo nome viene visualizzato nell’elenco dei componenti delle metriche, in modo da renderlo chiaro a te stesso e agli altri, come *Call center AOV*.

**B.** Una descrizione della metrica calcolata. Questa descrizione viene visualizzata quando gli utenti fanno clic su &quot;**i**&#39; accanto alla metrica nell’elenco dei componenti, assicurati che sia informativa. Ad esempio, per Call Center AOV, è possibile aggiungere *Calcola il valore medio dell&#39;ordine per gli ordini assistiti dal call center*.

**C.** Il formato della metrica: scegli decimale, ora, percentuale o valuta e aggiungi cifre decimali e polarità. Ecco, sceglieremo *Valuta per il formato, 0 per il numero di decimali e* ⬆ *Buono (verde) per la polarità.*

**D**. Se utilizzi i tag, che consentono di applicare argomenti e individuare rapidamente le metriche calcolate, aggiungi i tag applicabili qui. Abbiamo aggiunto *AOV* e *Call center* tag.

**E.** Questa sezione è destinata alla visualizzazione: mentre crei la metrica calcolata nella sezione F, la formula viene visualizzata qui.

**F.** In questo caso, puoi trascinare dimensioni (H), metriche (I) o segmenti (J) per creare la metrica calcolata e gli operatori per la formula. Per ogni metrica, se fai clic sulla rotellina del baricentro, puoi modificare il tipo di metrica (Standard/Totale) e il modello di attribuzione. *Trascineremo e rilasceremo i ricavi del call center, poi, sotto di esso,*÷￼*. Accetteremo il tipo di metrica e il modello di attribuzione predefiniti.*

**G**. Usa questo **+Aggiungi** per aggiungere condizioni aggiuntive o numeri statici, che qui non sono necessari.

**K.** E infine, mentre costruisci i calcoli, puoi visualizzare in anteprima i dati degli ultimi 90 giorni qui.

Ora che abbiamo costruito il Call Center AOV, abbiamo anche bisogno di una metrica calcolata per il Call Center AOV online. A tal fine, seguiremo gli stessi passaggi descritti sopra.

Ora possiamo costruire una terza metrica calcolata, usando il Generatore di metriche calcolate o al volo dall&#39;interno della tabella a forma libera, per confrontare il Call Center e l&#39;AOV online e così finiamo con qualcosa di simile a questo:

![Calc. 05](assets/calc05.png)

Nel nostro esempio, notiamo un incremento significativo quando i clienti utilizzano il call center per effettuare un acquisto. Questi dati possono quindi orientare le nostre decisioni su come aiutare i clienti a ottenere assistenza per i loro acquisti, ad esempio tramite offerte pop-up o altre esperienze guidate.

## Utilizzo dei segmenti nelle metriche calcolate

Vediamo ora come utilizzare i segmenti nelle metriche calcolate per acquisire maggiori informazioni sul comportamento, le preferenze e le motivazioni del cliente. Con i segmenti e le metriche calcolate, possiamo imparare abbastanza sui clienti per migliorarne l’esperienza, aumentare i ricavi e migliorare la soddisfazione e la fedeltà dei clienti.

Sappiamo già dagli esempi di AOV di cui sopra che gli acquisti assistiti dal call center hanno in genere un AOV più alto. Tuttavia, altre metriche ci dicono che la maggior parte degli utenti non utilizza il call center per gli acquisti.

Quindi, quali categorie di vendita al dettaglio - e i percorsi degli utenti attraverso tali categorie - risultano nel punteggio AOV più alto?  Possiamo scoprirlo combinando segmenti con metriche calcolate.

Per farlo, dobbiamo innanzitutto creare a livello di visita *include* e *escludi* segmenti per ciascuna categoria di prodotti. Includi o escludi è determinato facendo clic sul pulsante **Opzioni** nell’angolo a destra del contenitore. Il valore predefinito è Includi.

![Calc. 06](assets/calc06.png) ![Calc. 07](assets/calc07.png)

Dopo aver creato questi segmenti, possiamo creare una metrica calcolata per rispondere alla tua domanda. Viene aperto il Generatore di metriche calcolate ed è possibile effettuare le seguenti operazioni:

1. Cerca i segmenti appena creati e trascina quelli che desideri utilizzare nell’area grigia nella parte superiore della sezione **Definizione** casella. Ad esempio, se desideri creare un valore AOV per gli utenti che hanno visitato sia le categorie Donne che Uomini, ma non Kid’s, possiamo trascinare e rilasciare questi tre segmenti in quell’area: *Includi donne*, *Includi uomo*, e *Escludi bambini*. Questo lo chiamiamo *stacking dei segmenti*.

   ![Calc. 09](assets/calc09.png) ![Calc. 08](assets/calc08.png)

1. Quindi, trascina e rilascia la **Ricavi online** nello stesso contenitore, quindi **Ordini online**. Poiché i contenitori funzionano come espressioni matematiche per determinare l’ordine delle operazioni, gli elementi nei contenitori vengono elaborati prima dei processi successivi, anche se non sono presenti più contenitori o processi in questo calcolo.
1. L’operatore viene modificato da metrica a divisione (÷).
1. Noi selezioniamo **Valuta** come formato, **0** cifre decimali, e **SU** per la polarità.
1. Denomina la metrica calcolata e fornisci una descrizione.
1. Salva.

Al termine, la metrica calcolata sarà simile alla seguente:

![Calc. 10](assets/calc10.png)

Dopo aver creato le metriche calcolate utilizzando segmenti impilati per ogni combinazione del percorso di categorie del visitatore e aver dato un’occhiata ai dati, osserva cosa abbiamo imparato. Gli utenti che durante la visita visitano sia le categorie Donne che Uomini hanno il valore AOV più alto e, se confrontati con i visitatori di una singola categoria, l’incremento è significativo:

![Calc. 11](assets/calc11.png) ![Calc. 12](assets/calc12.png)

Sapendo questo, possiamo ottimizzare il layout di pagina, il posizionamento dei prodotti e i messaggi promozionali per inserire più persone in queste categorie prima del check-out.

## Prezioso, ma non disponibile ovunque

**Quindi - le metriche calcolate, semplici e complesse, sono di grande valore per gli analisti!**

Tuttavia, queste metriche non sono disponibili in tutte le aree di [!DNL Adobe Analytics]. Non puoi utilizzare metriche calcolate in:

- Abbandono in Analysis Workspace
- Analisi di coorte in Analysis Workspace
- Data Warehouse 
- Rapporti in tempo reale
- Rapporti sui dati correnti
- [!DNL Analytics] per Target
- Report Builder

## Best practice per le metriche calcolate

Ora che sai quanto possono essere preziose le metriche calcolate, vediamo alcune best practice per crearle.

1. **Verifica la sintassi della formula.** Assicurati che la sintassi della formula sia corretta e segua il [!DNL Adobe Analytics] sintassi per ottenere informazioni significative.
1. **Verifica l’ordine delle operazioni.** Assicurati di utilizzare i contenitori con attenzione e di mettere le cose nell&#39;ordine matematico corretto delle operazioni.
1. **Non conteggiare due volte i dati**. Puoi evitare il doppio conteggio dei dati assicurandoti che la formula utilizzata nella metrica calcolata non conti più volte gli stessi dati. Ciò si ottiene spesso combinando *Includi* e *Escludi* nella metrica calcolata o tramite l’uso di segmenti.
1. **Verifica la granularità temporale.** Assicurati che la metrica calcolata abbia la stessa granularità temporale delle metriche sorgente utilizzate nella formula.
1. **Utilizza dati accurati:** Otterrai risultati importanti solo se utilizzi dati accurati e affidabili nel calcolo.

## Best practice per i segmenti personalizzati

Durante la creazione di segmenti in [!DNL Adobe Analytics], tieni presenti le best practice seguenti:

1. **Semplificala.** Evita di complicare eccessivamente il segmento. Conservarla nel modo più semplice possibile e utilizzare solo le condizioni necessarie per garantire la precisione.
1. **Utilizzare i tipi di contenitori corretti**. Assicurati di utilizzare il tipo di contenitore corretto (visitatore, visita o hit) nella definizione del segmento per evitare di ottenere risultati errati.
1. **Non conteggiare due volte i dati**. Come per le metriche calcolate, assicurati che il segmento non conti più volte gli stessi dati. I contenitori Includi ed Escludi possono essere utili.
   1. Quando si utilizza un contenitore di inclusione, *include* *tutti i contenuti della visita* se un hit corrisponde alla condizione all’interno della visita.
   1. Quando si utilizza un contenitore di esclusione, *esclude tutto il contenuto della visita* se un hit corrisponde alla condizione all’interno della visita.
1. **Nidificare correttamente i contenitori**. Determina i dati inclusi utilizzando il contenitore più esterno, quindi applica le regole nidificate ai dati rimanenti. Quando vengono applicate le regole nidificate, il flusso di segmenti agisce come un funnel e le regole successive non si applicano agli hit esclusi dalla prima regola.
1. **Assicurati che i dati siano aggiornati.** Per ottenere risultati accurati, assicurati di utilizzare dati accurati e aggiornati nella definizione del segmento.
1. **Verifica il segmento.** Esegui sempre il test del segmento per assicurarti che funzioni come previsto prima di rilasciarlo ad altri.
1. **Considera le prestazioni.** I segmenti possono rallentare l’elaborazione dei rapporti, pertanto considera tale impatto al momento di crearli.

## Conclusioni principali

Combinare segmenti e metriche calcolate in [!DNL Adobe Analytics] può portare assolutamente ad un’analisi dei dati più solida ed efficace. Suddividendo in porzioni e indicando i dati e creando calcoli a scopo di confronto, puoi ottenere informazioni più approfondite sul comportamento dei clienti, utili per ottimizzare le campagne di marketing e creare dashboard e rapporti personalizzati. Tuttavia, ricorda che le metriche calcolate non sono disponibili in tutte le aree di [!DNL Adobe Analytics]e assicurati di seguire le best practice per assicurarti di ottenere dati accurati e utili.


## Autore

Questo documento è stato scritto da:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, Senior [!DNL Adobe Analytics] Manager di Adswerve

![Adswerve](assets/calc14.png)
