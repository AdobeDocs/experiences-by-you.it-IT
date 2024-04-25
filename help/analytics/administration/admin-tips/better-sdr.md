---
title: Creazione di una cultura dei dati e di un migliore riferimento di progettazione della soluzione
description: Rivoluziona la tua strategia per i dati e responsabilizza il tuo team nella creazione di un documento Solution Design Reference (SDR) solido. Eliminare le lacune nelle misurazioni e promuovere una cultura collaborativa dei dati attraverso metodologie dettagliate.
feature: Implementation Basics
topic: Administration
role: User
level: Experienced
doc-type: Article
duration: 72000
last-substantial-update: 2024-04-25T00:00:00Z
jira: KT-15338
thumbnail: KT-15338.jpeg
source-git-commit: 484f93bc2828d2565486eff8ae4801a8d203d280
workflow-type: tm+mt
source-wordcount: '1635'
ht-degree: 0%

---


# Creazione di una cultura dei dati e di un migliore riferimento di progettazione della soluzione

**Rivoluziona la tua strategia per i dati e responsabilizza il tuo team nella creazione di un documento SDR (Solution Design Reference) solido. Eliminare le lacune nelle misurazioni e promuovere una cultura collaborativa dei dati attraverso metodologie dettagliate.**

È finalmente ora. È stata creata una Solution Design Reference (SDR) solida. Questa è la guida che utilizzi per implementare le metriche e le dimensioni, come si chiamano, quando attivano, e ai tuoi sviluppatori piace. Avete seguito l&#39;intero processo di implementazione, scritto i criteri di accettazione, controllato gli sprint, controllato l&#39;intera faccenda, ed è tutto fatto! È stato un sacco di lavoro, e ora è fatto. La tua istanza di Adobe Analytics dovrebbe essere far saltare il marketing e il prodotto mentre si immergono nei dati, ottenere nuove rivelazioni sui tuoi clienti, e trovare tutte le aree di successo e, beh, le aree di meno successo. Ma non sentite i riconoscimenti che vi aspettavate.

Da un campo si sentono le lamentele.

&quot;Perché non riesco a capire il tasso di conversione su questo funnel?&quot;

&quot;Perché non c&#39;è una metrica per questo?&quot;

&quot;Mi servono molti più dettagli! Una metrica da sola non è sufficiente. Ci sono almeno tre dimensioni diverse che devo capire le prestazioni. Perché non li hai messi?&quot;

Ma è l&#39;altro campo che desta maggiori preoccupazioni. Da loro, non sentite proprio niente. Ma ancora peggio, vedete grafici che sono stati chiaramente presi dalla vostra vecchia soluzione di analisi, sapete, quella che non viene più mantenuta, e ogni giorno sta cadendo ancora più in una palude di decrepitudine e dati sporchi. Un senso di terrore ti riempie quando pensi alle decisioni che potrebbero essere prese con quel casino.

Cos’è andato storto? Perché esistono delle lacune nella misurazione? Perché i membri del tuo team non accettano questa proposta?

Comincerò lasciandovi un po&#39; uscire dall&#39;amo. C&#39;è *sempre* sarà un po&#39; di revisione. Se il tuo sito o la tua app sono abbastanza complessi da richiedere una soluzione di analisi aziendale, è praticamente certo che ti mancherà qualcosa. Ma non abbastanza per spiegare i divari di misura di cui sto parlando qui. Ciò che è andato storto è molto più difficile da inserire in un foglio di calcolo. Hai perso le prime possibilità di creare una cultura dei dati collaborativa nello stesso momento in cui hai creato il tuo SDR. Voglio descrivervi un metodo che io e i miei colleghi abbiamo sviluppato sia per creare un SDR migliore con meno spazi, sia per coinvolgere gli utenti finali e, occasionalmente, entusiasmarli per la loro nuova istanza di Adobe Analytics. Andiamo a vedere i motivi.

**Il Come**

***La conferenza di misurazione:***

1. Riunisci le parti interessate, di persona o virtualmente, con l’obiettivo di scoprire cosa misurare. Dovrebbero essere inclusi alcuni esempi.
1. Sulla bacheca sono già presenti alcuni esempi ovvi su note di Sticky Notes, elementi come ricavi, vendite o lead, in cui verranno misurati i KPI di base noti. Ripeti con dimensioni, elementi come stato di accesso, categorie di prodotti o termini di ricerca.
1. Chiedi a tutti di aggiungere le proprie note, raggruppandole in base alle esigenze
1. Fate votare quelli che pensate siano importanti. Si tratta di voti illimitati, dato che forse tutte queste metriche e dimensioni contano.
1. Per coloro che hanno voti bassi, chiedere alle parti interessate che li hanno richiesti di spiegare per cosa li useranno. Se esiste un buon caso d’uso, lo conservi. Se c&#39;è un modo migliore di ottenere quei dati, non possono spiegare come siano fruibili, o c&#39;è un altro buon motivo per non tenerli, eliminarli dalla lavagna.
1. Aggiungi queste metriche e dimensioni al tuo SDR per una revisione iniziale da parte delle parti interessate presenti

***La mappa funnel***

1. Ottieni una visualizzazione di tutti i funnel, passo dopo passo con ogni stato incluso
1. Con i designer e i product manager, affrontate ogni fase e parlate di ciò che considerano un successo in quel funnel. È il tasso di conversione? Sta scegliendo un percorso particolare? Utilizza alcune funzionalità?
1. Poni domande sulle metriche e sulle dimensioni necessarie per comprendere le prestazioni del funnel in ogni passaggio del funnel e nel complesso.
1. Sopra ogni passaggio del funnel, aggiungi le metriche e le dimensioni che verranno misurate su quel passaggio, incluse le metriche calcolate.
1. All’inizio di ciascun funnel, scrivi i rapporti che verranno utilizzati dal responsabile prodotto per monitorare le prestazioni, ad esempio un rapporto sull’abbandono, i tassi di conversione del mese corrente e delle tendenze e altro ancora.
1. Aggiungi le nuove metriche e dimensioni scoperte al documento SDR e invialo alle parti interessate per una seconda revisione.

***Dashboard di anteprima***

1. Utilizzando la mappa funnel come guida, crea dei dashboard fittizi.
1. Dovrebbe essere disponibile una visualizzazione complessiva, ad esempio una dashboard di riepilogo esecutivo e dashboard per ciascuno dei funnel.
1. Saranno inoltre disponibili informazioni più specifiche per il sito o l’app, ad esempio prestazioni del prodotto o del contenuto.
1. Distribuiscili alle parti interessate e ricevi feedback sulla progettazione.
1. Effettua gli aggiornamenti richiesti e, se sono necessarie nuove metriche o dimensioni, aggiungili al tuo SDR.
1. Invia le dashboard e i documenti SDR di anteprima aggiornati per una revisione finale.

***Strumenti di democratizzazione dei dati***

1. Crea un dizionario dati. Il documento SDR è destinato ai tuoi sviluppatori. Il dizionario dati è destinato agli utenti finali. Rendilo leggibile per gli utenti finali in modo che possano facilmente cercare i dati disponibili e sapere come utilizzarli. Gli utenti finali dovrebbero essere gli approvatori finali di questo elemento.
1. Annotazioni. In ogni organizzazione, ci sono certe date che contano ogni anno e altre che verranno fuori. Assicurati di raccogliere quelli pertinenti dalle parti interessate e aggiungerli come annotazioni per migliorare la comprensione dei dati visualizzati.
1. Cura. Se il tuo DSP è grande, potrebbe essere travolgente. La paralisi della scelta non si applica solo ai clienti. Scopri cosa è importante per ogni gruppo di utenti e cura gli elementi che vedranno.

**Il perché**

***Per Ottenere I Requisiti***

Si tratta di un metodo ovvio, ma esistono altri modi efficaci per soddisfare i requisiti. Ne ho usata una su una serie di interviste, questionari e revisioni di report esistenti. Questi funzioneranno, anche se non credo bene come i metodi che ho appena descritto. Onestamente non credo che il divario nella raccolta dei requisiti sia così grande però. Il metodo che ho descritto vi porterà al 95% della strada, e questi altri metodi vi porteranno al 90% della strada. Allora, qual è il grande motivo?

***Per creare la lingua dei dati***

Con questo processo:

- Pensare profondamente su come misurare il successo
- Creare un senso di proprietà nelle parti interessate
- Facilitare la comprensione dei dati da parte delle parti interessate

***Approfondimento sui dati***

Per molte persone della tua azienda, i dati sono qualcosa che consumano. Loro la usano. Lo analizzano. Loro non ci pensano profondamente. Alcuni di essi hanno ereditato relazioni e processi dai loro predecessori che non hanno modificato a causa della necessità di continuità. Non hanno mai avuto bisogno di pensare al perché dei dati.

Questo processo offre loro l&#39;opportunità di *comprendere* dati. Domande, cos&#39;è il successo? Come sapresti se avessi successo? Come sapresti cosa cambiare se non hai avuto successo? Questo è un esercizio che dovrebbe essere fatto all&#39;inizio della creazione di ogni sito, app e prodotto, ma troppo spesso non lo è. Ponendo queste domande, contribuisci ad approfondire la loro comprensione non solo dei dati, ma anche del loro prodotto.

***Creazione di un senso di proprietà sui dati***

Questo non è qualcosa che è stato tramandato dall&#39;alto. Questo non è qualcosa che è stato un incontro di trenta minuti tre mesi fa. Questo non è un questionario così fastidioso che sono stati perseguitati per una settimana a rispondere e che lo hanno fatto in fretta perché avevano una demo per arrivare in modo da poter fare la data di rilascio sprint. Questo è il prodotto del loro pensiero profondo e del loro lavoro con voi e i loro colleghi, quello che hanno analizzato più volte, fornito feedback continui per, e che hanno approvato dopo che il feedback è stato incorporato. È loro! Il fatto che sia utile è dovuto a loro. È *loro* ed è il processo che li ha resi loro.

***Rendere i dati più facili da comprendere***

Hai anche mostrato loro come lo useranno e come apparirà nelle dashboard di anteprima. Qualsiasi nuova soluzione è *duro*. C&#39;è così tanto da imparare e data l&#39;enorme personalizzabilità di Adobe Analytics, la curva di apprendimento può essere piuttosto ripida. Hai rimosso l&#39;80% di questo però. Anche prima che sia stata scritta la prima riga di codice, le parti interessate sanno come saranno le loro dashboard. Sapranno come leggerli e ottenere significato da loro. Sapranno come si presenta il successo, perché vi hanno detto quali metriche e dimensioni definiscono il successo, e avete detto loro come verrà visualizzato per loro. La distribuzione delle dashboard effettive è un aggiornamento, non una nuova e spaventosa attività di apprendimento.

Questo non è il modo più veloce per mettere insieme un documento SDR. Si tratta di un sacco di lavoro e richiede un sacco di coordinamento di programmi, soprattutto perché è fondamentale che ci sono alcuni eccessi nel mix. Alla fine, però, una soluzione di analisi aziendale rappresenta un enorme investimento di tempo e denaro e vuoi essere certo che l’adozione e la soddisfazione siano elevate. Questo metodo ha fatto molta strada per realizzarlo.

**Autore**

Questo documento è stato scritto da:

![gitai-headshot](assets/gitai-headshot.png)

Gitai Ben-Ammi, Business Architecture Associate Manager di Accenture

Adobe Analytics Champion


