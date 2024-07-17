---
title: Creazione di una cultura dei dati e di una migliore documentazione di progettazione della soluzione
description: Rivoluziona la tua strategia per i dati e responsabilizza il tuo team nella creazione di un documento Solution Design Reference (SDR) solido. Elimina le lacune nelle misurazioni e promuovi una cultura collaborativa dei dati attraverso metodologie dettagliate.
feature: Implementation Basics
topic: Administration
role: User
level: Experienced
doc-type: Article
duration: 72000
last-substantial-update: 2024-04-25T00:00:00Z
jira: KT-15338
thumbnail: KT-15338.jpeg
exl-id: 99fcf68f-5698-4270-9055-ab224e6323a1
source-git-commit: b2e05ff39e065691dda530ed17762a55cf2e6778
workflow-type: tm+mt
source-wordcount: '1647'
ht-degree: 0%

---

# Creazione di una cultura dei dati e di un migliore riferimento di progettazione della soluzione

_Rivoluziona la tua strategia di gestione dei dati e consenti al tuo team di creare un solido documento Solution Design Reference (SDR). Eliminare le lacune nelle misurazioni e promuovere una cultura collaborativa dei dati attraverso metodologie dettagliate._

È finalmente ora. Avete messo insieme un solido documento SDR. Un documento SDR è la guida che utilizzi per implementare le metriche e le dimensioni. Hai definito come si chiamano quando si attivano, e i tuoi sviluppatori lo adorano. Avete affrontato l&#39;intero processo di implementazione, scritto i criteri di accettazione, fatto gli sprint, li avete testati, ed è fatto! L&#39;istanza di [!DNL Adobe Analytics] dovrebbe far festeggiare i team di marketing e di prodotto mentre analizzano i dati, ottengono nuove rivelazioni sui tuoi clienti e trovano tutte le aree di successo e quelle meno riuscite. Ma non sentite i riconoscimenti che vi aspettavate.

Da un team, si sentono lamentele del tipo:

&quot;Perché non riesco a capire il tasso di conversione su questo funnel?&quot;

&quot;Perché non c&#39;è una metrica per questo?&quot;

&quot;Ho bisogno di più dettagli! Una metrica da sola non è sufficiente. Ci sono almeno tre dimensioni diverse che devo capire le prestazioni. Perché non li hai messi?&quot;

Ma è l&#39;altra squadra che desta maggiori preoccupazioni. Da loro, non sentite proprio niente. Peggio ancora, puoi vedere grafici che sono stati chiaramente tratti dalla tua vecchia soluzione di analisi (quella che non è più mantenuta, e ogni giorno sta cadendo ulteriormente in una palude di decrepitudine e dati sporchi). Un senso di terrore ti riempie mentre consideri le decisioni che potrebbero essere prese con quel caos originale.

_Si è verificato un errore?_

_Perché esistono delle lacune nella misurazione?_

_Perché i membri del tuo team non lo abbracciano?_

Comincerò lasciandovi scendere leggermente dall&#39;amo. Ci saranno _sempre_ revisioni. Se il sito o l’applicazione sono abbastanza complessi da richiedere una soluzione di analisi aziendale, è sicuro che ti mancherà qualcosa. Ma in questo caso, non vi siete persi abbastanza da spiegare le distanze di misura che sto descrivendo.

Ciò che è andato storto è molto più difficile da inserire in un foglio di calcolo. In sostanza, hai perso la prima occasione di creare una cultura dei dati collaborativa mentre hai creato il tuo SDR.

Voglio illustrarvi un metodo che i miei colleghi ed io abbiamo sviluppato per creare un SDR migliore con meno spazi, e per coinvolgere gli utenti finali (e occasionalmente entusiasmati) nella loro nuova istanza di [!DNL Adobe Analytics]. Passiamo ora a spiegare come e perché dovresti considerare questo metodo.

## Il come

_Informazioni sulla conferenza di misurazione. Utilizza una mappa funnel per visualizzare ogni passaggio del piano. Crea dashboard fittizie da rivedere come gruppo. Creare un dizionario dati per gli utenti._

### La conferenza di misurazione

1. Riunisci le parti interessate, di persona o virtualmente, con l’obiettivo di scoprire cosa misurare. Questa riunione dovrebbe includere alcuni dirigenti.
1. Includi esempi ovvi già nella bacheca delle note, ad esempio ricavi, vendite o lead, gli indicatori KPI (Key Product Indicators) che sai verranno misurati. Ripeti con dimensioni quali stato di accesso, categorie di prodotti o termini di ricerca.
1. Chiedi a tutti di aggiungere le proprie note, raggruppandole in base alle esigenze.
1. Chiedete alla gente di votare quelli che ritengono importanti. Si tratta di voti illimitati, perché tutte queste metriche e dimensioni probabilmente contano.
1. Per qualsiasi metrica e dimensione con voti bassi, chiedi alle parti interessate che ne hanno fatto richiesta di spiegare perché questi componenti verrebbero utilizzati. Se esiste un buon caso d’uso, mantieni questi componenti. Se esiste un modo migliore per ottenere tali dati, o se nessuno può spiegare in che modo questi dati possano essere utilizzati, o se esiste un altro buon motivo per rimuovere metriche e dimensioni, procedi in questo modo.
1. Aggiungi queste metriche e dimensioni al tuo SDR per una revisione iniziale da parte delle parti interessate presenti.

### La mappa funnel

1. Ottieni una visualizzazione di tutti i funnel, passo dopo passo con ogni stato incluso.
1. Con i designer e i product manager, segui ogni passaggio e discuti su ciò che tutti considerano il successo in quel funnel. È il tasso di conversione? Sta scegliendo un percorso particolare? Utilizza alcune funzionalità?
1. Poni domande sulle metriche e sulle dimensioni necessarie per comprendere le prestazioni del funnel in ogni passaggio del funnel e nel complesso.
1. Sopra ogni passaggio del funnel, aggiungi le metriche e le dimensioni misurate su quel passaggio, comprese le metriche calcolate.
1. All’inizio di ogni funnel, scrivi i rapporti che vanno nel dashboard che il product manager può utilizzare per monitorare le prestazioni. Questi rapporti includono un [rapporto di fallout](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow), [mese corrente](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges), [tassi di conversione con tendenze](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/line) e qualsiasi altro elemento specifico per tale funnel.
1. Aggiungi le nuove metriche e dimensioni scoperte al documento SDR e invialo alle parti interessate per una seconda revisione.

### Dashboard di anteprima

1. Utilizzando la mappa funnel come guida, crea dei dashboard fittizi.
1. Dovrebbe essere disponibile una visualizzazione complessiva, ad esempio una [dashboard di riepilogo esecutivo](driving-success-with-executive-summary-dashboards.md) e dashboard per ciascuno dei funnel.
1. Saranno inoltre disponibili informazioni più specifiche per il sito o l’app, ad esempio prestazioni del prodotto o del contenuto.
1. Distribuiscili alle parti interessate e ricevi feedback sulla progettazione.
1. Effettua gli aggiornamenti richiesti e, se sono necessarie nuove metriche o dimensioni, aggiungili al tuo SDR.
1. Invia le dashboard e i documenti SDR di anteprima aggiornati per una revisione finale.

### Strumenti di democratizzazione dei dati

1. Creare un dizionario dati. L’SDR è per gli sviluppatori, ma il dizionario dati è per gli utenti finali. Rendilo leggibile in modo che tutti possano facilmente cercare i dati disponibili e sapere come utilizzarli. Gli utenti finali dovrebbero essere gli approvatori finali di questo elemento.
1. Annota. In ogni organizzazione, ci sono certe date che contano ogni anno e altre che verranno fuori. Raccogli le date pertinenti dalle parti interessate e aggiungili come annotazioni per comprendere meglio i dati visualizzati.
1. Cura. Se il tuo DSP è grande, potrebbe essere travolgente. La paralisi della scelta non si applica solo ai clienti. Scopri cosa è importante per ogni gruppo di utenti e cura gli elementi che vedranno.

## Il perché

_Scopri come raccogliere i requisiti, creare una cultura dei dati, avviare una riflessione approfondita sui dati, creare un senso di proprietà sui dati e semplificare i dati._

### Raccogli i requisiti

Raccogliere i requisiti è ovvio, ma esistono diversi modi efficaci per farlo. Ho usato interviste individuali, questionari e revisioni di rapporti esistenti. Queste strategie funzionano, ma non così come i metodi che ho appena descritto. tuttavia, non credo che la differenza tra i metodi per la raccolta dei requisiti sia significativa. Il metodo che ho descritto vi porta al 95% della strada, e questi altri metodi vi portano al 90% della strada.

Qual è il _motivo_?

### Genera impostazioni cultura dati

Con questo processo:

* Pensare profondamente su come misurare il successo
* Creare un senso di proprietà nelle parti interessate
* Facilitare la comprensione dei dati da parte delle parti interessate

### Riflettere profondamente sui dati

Per molte persone della tua azienda, i dati sono qualcosa che consumano. Loro la usano. Lo analizzano. Loro non ci pensano profondamente. Alcune persone hanno ereditato i rapporti e i processi dai loro predecessori, ma non li hanno modificati per il bene della continuità. Forse queste persone non hanno mai avuto bisogno di pensare al _perché_ dei dati.

Questo processo offre loro l&#39;opportunità di _comprendere_ i dati. Domande come, Cos’è il successo? Come sapresti se avessi successo? Come sapresti cosa cambiare se non hai avuto successo? A queste domande è necessario rispondere all&#39;inizio della creazione di tutti i siti, le applicazioni e i prodotti, ma troppo spesso non è così. Ponendo queste domande, contribuisci ad approfondire la comprensione di una persona non solo dei dati, ma anche del suo prodotto.

### Creare un senso di proprietà sui dati

Un senso di proprietà non è qualcosa che una persona acquisisce facilmente. Non è stato trovato in quella riunione di 30 minuti a cui hanno partecipato tre mesi fa. Non è stato creato da questo un fastidioso questionario a cui hanno risposto troppo rapidamente a causa di altri problemi di lavoro pressanti come le demo e le date di rilascio sprint.

La proprietà è il prodotto del pensiero profondo di qualcuno e del suo lavoro con te e i colleghi. È ciò che hanno esaminato più volte, fornito un feedback continuo, e ciò che hanno approvato dopo che il feedback è stato incorporato. È loro! Il fatto che sia utile è dovuto a loro. Sono _i loro_ dati ed è questo processo che li ha resi loro.

### Semplificare i dati

Hai anche mostrato loro come useranno il processo e come si presenterà nelle [dashboard di anteprima](#the-preview-dashboards). Qualsiasi nuova soluzione è _hard_. C&#39;è molto da imparare e, data l&#39;incredibile possibilità di personalizzazione di [!DNL Adobe Analytics], la curva di apprendimento può essere ripida. Hai rimosso l&#39;80% di questo però. Anche prima che sia stata scritta la prima riga di codice, le parti interessate sanno come saranno le loro dashboard. Sapranno come leggerli e ottenere significato da loro. Sapranno come si presenta il successo, perché vi hanno detto quali metriche e dimensioni definiscono il successo. E avete detto loro come questo successo verrà visualizzato loro. La distribuzione delle dashboard effettive è un aggiornamento, non una nuova e spaventosa attività di apprendimento.

Questo non è necessariamente il modo più rapido per mettere insieme un documento SDR. Si tratta di un sacco di lavoro e richiede un sacco di coordinamento di programmi, soprattutto perché è fondamentale che ci sono alcuni dirigenti nel mix. Alla fine, tuttavia, una soluzione di analisi aziendale rappresenta un enorme investimento di tempo e denaro e vuoi essere certo che l’adozione e la soddisfazione siano elevate. Questo metodo ha fatto molta strada per realizzarlo.

**Autore**

Questo documento è stato scritto da:

![gitai-headshot](assets/gitai-headshot-150.jpg)

Gitai Ben-Ammi, Business Architecture Associate Manager di Accenture

[!DNL Adobe Analytics] campione
