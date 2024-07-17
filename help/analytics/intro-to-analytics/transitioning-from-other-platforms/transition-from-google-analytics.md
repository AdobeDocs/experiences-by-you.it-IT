---
title: Guida completa per la transizione a  [!DNL Adobe Analytics]  da Google [!DNL Analytics]
description: Scopri la posizione delle funzionalità equivalenti e come utilizzarle in modo efficiente durante la transizione da Google [!DNL Analytics] a [!DNL Adobe Analytics]
solution: Analytics
feature: Third-party Integration
role: User
level: Beginner
kt: 9830
thumbnail: 34749.jpg
exl-id: 646bdc8f-c95e-40be-b2f7-8e4ba5653d91
source-git-commit: 02e3a6dfa59df45113242bd8e874e18e9e1efd58
workflow-type: tm+mt
source-wordcount: '3323'
ht-degree: 0%

---

# Guida completa alla transizione a [!DNL Adobe Analytics] da Google [!DNL Analytics]{#comprehensive-guide-for-transitioning-to-adobe-analytics}

## 1. Introduzione

Una delle maggiori sfide nella transizione tra strumenti diversi consiste nell’imparare a trovare funzionalità equivalenti e a utilizzarle in modo efficiente. Questa discussione fa parte di una guida più ampia per facilitare la transizione degli utenti a [!DNL Adobe Analytics] (come nuovo utente o proveniente da Google [!DNL Analytics]). Confronto approfondito con GA; come strumento comparativo più probabile con cui la maggior parte degli utenti acquisisce familiarità; viene fornito per aiutare gli utenti a correlare le conoscenze esistenti al nuovo set di strumenti. Quando non esiste un sostituto della pratica, questo ti aiuta a iniziare e ridurre le frustrazioni che potresti incontrare durante questo periodo.

Dovremmo fare un rapido confronto terminologico:

| **Descrizione** | **[!DNL Adobe Analytics]** | **Google[!DNL Analytics]** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| È stata visualizzata una metrica evento che rappresenta una pagina (o una schermata di un’app) | Visualizzazione pagina | Pageview |
| Una metrica che rappresenta un gruppo di interazioni, nel sito web o nell’app, che si verificano nello stesso intervallo di tempo | Visita | Session |
| Una metrica che definisce un dispositivo identificato (in base a più criteri, inclusi cookie e altri modelli di comportamento per unire le informazioni utente) | Visitatore univoco | Utente |

## 2. Interfacce

Quando le persone confrontano [!DNL Adobe Analytics] e Google [!DNL Analytics], osservano che l&#39;interfaccia di [!DNL Adobe] è inizialmente impegnativa. Questo è vero, ma è anche; credeteci o no; una forza, non una debolezza. [!DNL Adobe] offre un&#39;ampia gamma di strumenti e flessibilità nella visualizzazione dei dati, consentendo di creare in modo molto più libero ciò di cui hai bisogno.

Cominciamo guardando il reporting &quot;in-site&quot;.

### 2.1. Reporting in-site

#### 2.1.1. Schermata iniziale

Sia [!DNL Adobe Analytics] che Google [!DNL Analytics] offrono un modo per personalizzare la prima visualizzazione che un utente visualizza al momento dell&#39;accesso.

##### 2.1.1.1. Schermata iniziale di Workspace / Impostazione personalizzata ([!DNL Adobe Analytics])

[!DNL Adobe Analytics] non presume di creare un rapporto predefinito che tutti gli utenti potranno visualizzare all&#39;accesso. La pagina Home predefinita porta l’utente alla schermata di destinazione di Workspace, che mostra a ogni utente tutti i rapporti dell’area di lavoro creati o condivisi. Inoltre, ogni utente può impostare uno qualsiasi di questi rapporti come schermata iniziale, se lo desidera.

![workspace-create-project](assets/ga-to-aa_1.png)

Di seguito in questa guida saranno riportati ulteriori dettagli sull’area di lavoro. Cfr. sezione 2.1.2.1

>[!TIP]
>
>Crea/condividi alcuni rapporti standard per la tua organizzazione in modo che abbiano un punto di partenza per visualizzare le informazioni senza doversi immergere nella creazione dei rapporti.



##### 2.1.1.2. Informazioni approfondite sulla schermata iniziale (Google [!DNL Analytics])

* Nella schermata iniziale di Google [!DNL Analytics] sono disponibili alcune visualizzazioni predefinite. Questi includono:
* Utenti, sessioni, frequenza di rimbalzo e durata della sessione negli ultimi sette giorni
* Utenti per ora del giorno negli ultimi 30 giorni
* Utenti attuali e pagine attive principali
* Canale di traffico, Source/Medium e riferimenti negli ultimi sette giorni
* Sessioni per Paese negli ultimi sette giorni
* Pagine principali per gli ultimi sette giorni
* Tendenza utenti attivi per gli ultimi 30 giorni
* e altro ancora

Gli utenti di GA4 hanno più opzioni per personalizzare e aggiungere i propri rapporti alla schermata iniziale.

![google-analytics-interfaces](assets/ga-to-aa_2.png)

Questa è probabilmente l&#39;unica cosa che ti manca di più in [!DNL Adobe Analytics]. Non esiste una schermata iniziale predefinita per te. Tuttavia, puoi facilmente impostare un Workspace personalizzato per replicare ciò di cui hai bisogno dall’elenco precedente e impostarlo come schermata di destinazione. Tratteremo ulteriormente questo argomento in seguito (oppure consulta la sezione 2.1.2.1 [!DNL Adobe] Workspace).

#### 2.1.2. Report Builder nel sito

Oltre ai rapporti semplici forniti dagli strumenti di analisi, ogni strumento fornisce anche strumenti più potenti con cui creare rapporti personalizzati.

##### 2.1.2.1. [!DNL Adobe Analytics] Workspace

Questa è la potenza di [!DNL Adobe Analytics], dalla sua introduzione nel 2017 è diventata l&#39;area ideale per l&#39;analisi di [!DNL Analytics] e il motivo principale per cui la sezione Rapporti verrà presto ritirata.

Questo strumento consente di creare rapporti con una libertà pressoché completa.

Il rapporto può essere suddiviso in pannelli che possono contenere un numero qualsiasi di visualizzazioni. I pannelli possono essere impostati su informazioni comuni, ad esempio un intervallo di date e filtri di segmenti comuni.

I pannelli e le visualizzazioni al loro interno possono essere ridimensionati e trascinati per mostrare gli elementi uno accanto all’altro o sovrapposti. Per confrontare due diverse suite di dati una accanto all’altra, puoi creare dei pannelli divisi a metà lungo il centro, in modo da mostrare due siti affiancati per facilitarne il confronto.

Sono disponibili numerose visualizzazioni:

* Tabella a forma libera
* Tabella coorte
* Abbandono
* Flusso
* Grafici
   * Superfici (sovrapposte e non sovrapposte)
   * Linea
   * A dispersione
   * Barre (sovrapposte e non sovrapposte)
   * Punto elenco
   * Ciambella
   * Istogramma
   * Barre orizzontali (sovrapposte e non sovrapposte)
* Mappa
* Blocchi di riepilogo
   * Variazione di riepilogo
   * Testo di riepilogo
   * Testo (campo di testo libero per inserire informazioni aggiuntive per specificare il contesto)
* Venn

A ogni pannello e visualizzazione è possibile assegnare un nome e una descrizione che fornisca contesto sulle informazioni visualizzate.
In [!DNL Adobe], i segmenti (essenzialmente filtri per i dati) vengono applicati retroattivamente e possono essere inseriti nelle colonne delle tabelle a forma libera per confrontare i dati uno accanto all&#39;altro. Ad esempio, per confrontare il traffico per due diverse categorie sul sito, si può creare un segmento per la &quot;Categoria A&quot; e un altro per la &quot;Categoria B&quot;.

![analytics-page-views-report](assets/ga-to-aa_3.png)

Le tabelle a forma libera consentono più colonne e segmentazioni in base alle esigenze per visualizzare i dati nel modo desiderato.

Se non desideri visualizzare un raggruppamento per data, trascina un’altra dimensione o un altro segmento per visualizzare i dati in modo diverso. Ad esempio, utilizza i segmenti per Tipo di dispositivo, quindi aggiungi un raggruppamento per sistema operativo per gli utenti di Mobile/Tablet:

![analytics-compare-page-views-report](assets/ga-to-aa_4.png)

Workspace consente alla tua creatività di volare, senza essere limitato a raggruppamenti &quot;standard&quot;. Puoi creare le visualizzazioni necessarie per immergerti nei confronti che è necessario eseguire.

>[!TIP]
>
>Non abbiate paura di giocare ed esplorare. Ci sono così tanti modi di pensare fuori dagli schemi. Inoltre, la convalida di ciò che hai creato mostra ciò che pensi. L&#39;esperienza aiuta.

Puoi creare al volo metriche calcolate o segmenti che risiedono solo all’interno del rapporto per evitare che il segmento e l’archivio dei calcoli vengano inondati. Questo consente di creare elementi mirati necessari per rapporti specifici senza confondere l’organizzazione con elementi che non sono utilizzabili in altri contesti.

Questa discussione è solo un’introduzione a questo strumento, ci sono altre guide complete per iniziare. Dopo aver esaminato queste guide, puoi creare rapporti completi come i seguenti:

![workspace-dashboard](assets/ga-to-aa_5.png)

Le aree di lavoro non vengono salvate automaticamente, pertanto è più semplice creare un rapporto per un caso specifico senza riempire inutilmente l’archivio dei rapporti.

Un’altra potente funzione delle aree di lavoro è la possibilità di applicare modificatori interattivi ai rapporti sotto forma di menu a discesa. Questi menu a discesa non funzionano sui file CSV o PDF esportati dai rapporti. Tuttavia, all’interno del rapporto live, ti consentono di aggiornare tutte le visualizzazioni in un pannello per mostrare lo stesso rapporto in condizioni diverse. È possibile utilizzare più menu a discesa e, purché le opzioni non si escludano a vicenda, gli elementi selezionati si sovrappongono per consentire di presentare le informazioni in modo ordinato.

>[!IMPORTANT]
>
>Per ulteriori informazioni sull&#39;utilizzo dei menu a discesa e delle suddivisioni a forma libera, vedere <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google [!DNL Analytics]: dashboard, report personalizzati e report salvati

Google dispone di alcuni strumenti per la creazione di rapporti all’interno dell’interfaccia, ma segue ancora la stessa visualizzazione e le stesse limitazioni della sezione rapporti.

A questo punto, chi conosce bene Google [!DNL Analytics] mentre legge questo messaggio potrebbe dire: &quot;Aspetta un secondo, che ne dici di Google Data Studio, non è un equivalente migliore di Workspace di [!DNL Adobe]?&quot; Sì, ma Data Studio tecnicamente non fa parte dello strumento [!DNL Analytics] e consente connessioni a diverse origini dati. Questo strumento è trattato più avanti nella sezione &quot;Accesso al rapporto esteso&quot;, in particolare nella sezione 2.2.3.

Le dashboard e i rapporti personalizzati di Google consentono di richiamare più visualizzazioni in un unico rapporto, ma a differenza di Workspace, si è ancora vincolati a correlazioni semplici e ai dati che possono essere inseriti in quali colonne.

Nei rapporti personalizzati, una delle principali sfide è la creazione di un filtro che si applica a tutte le schede del rapporto. Non esiste un modo per confrontare due filtri diversi all’interno dello stesso rapporto.

Per confronti superficiali, è più che sufficiente. Sono simili alle dashboard legacy, ai report personalizzati e ai segnalibri di [!DNL Adobe]. Strumenti di base forniti per supportare le tue esigenze, che risiedono nella suite di rapporti.

#### 2.1.3. Relazioni

Sia Google che [!DNL Adobe] dispongono di alcuni rapporti navigabili costituiti da tabelle predefinite e semplici grafici della timeline basati su una dimensione.

##### 2.1.3.1. Rapporti [!DNL Adobe Analytics]

[!DNL Adobe Analytics] dispone anche di una sezione Rapporti, anche se questa verrà gradualmente eliminata a favore di Analysis Workspace. In effetti, è stata annunciata la fine del ciclo di vita di questa interfaccia, poiché Workspace è uno strumento più potente. La maggior parte di queste tabelle può essere creata e modificata con maggiore facilità. Le sezioni di [!DNL Adobe] sono molto più suddivise e questo può essere scoraggiante:

![analytics-site-metrics](assets/ga-to-aa_6.png)

Poiché la maggior parte di queste sezioni è accessibile tramite le aree di lavoro, offrirò una breve panoramica di queste sezioni spiegando come si relazionano con Google [!DNL Analytics], evidenziando i rapporti che sono ancora rilevanti.

Site Metrics (Metriche del sito) si riferisce alle metriche standard (visualizzazioni di pagina, visitatori univoci, visite ed eventi personalizzati che potresti aver configurato). È simile al rapporto Comportamento di Google Analytics, ma include anche alcuni elementi che si possono trovare in Pubblico (poiché [!DNL Adobe] non divide i tipi di metrica).

Qui trovi i rapporti relativi ai &quot;bot&quot;. Il traffico generato dai bot è escluso da tutti i rapporti standard, tuttavia, sono presenti due rapporti che forniscono informazioni approfondite su ciò che accade in tempo reale e sui bot che raggiungono il tuo sito. Questa funzione è particolarmente utile se imposti regole bot personalizzate per escludere i bot di spammer noti che visitano frequentemente il tuo sito. Puoi ottenere alcune informazioni su ciò che quei bot stanno facendo senza che i tuoi rapporti principali siano inondati, ma quel traffico. I rapporti sui bot non sono attualmente disponibili in Workspace, ma le nuove funzionalità di reporting disponibili a breve consentiranno agli utenti di ottenere queste informazioni anche lì.

Site Content è un raggruppamento di [!DNL Adobe] dimensioni standard: nome pagina, sezioni del sito, gerarchie, server e altro ancora. Tutte queste dimensioni sono disponibili in Workspace.

Mobile è un raggruppamento di dati specifici per i dispositivi mobili, inclusi dispositivi, tipi di dispositivi e altro ancora. Questi sono disponibili in Workspace.

I percorsi non sono disponibili in Workspace. Workspace dispone di un diagramma di flusso in cui è possibile visualizzare i flussi in entrata e in uscita per una singola pagina/valore. Al contrario, Percorsi ti consente di visualizzare i percorsi più comuni utilizzati nel sito web. Per impostazione predefinita, Pages (Pagine) è il primo rapporto sul percorso configurato. Tuttavia, puoi attivarlo per le proprietà personalizzate, ad esempio un valore &quot;Page Type&quot; (Tipo di pagina). Puoi esaminare i percorsi all’interno dei tipi di pagina. L’altra cosa che mi piace di Paths (Percorsi) è la semplicità con cui vengono presentate le informazioni. Il diagramma di flusso nell’area di lavoro (a seconda della quantità di dati che stai cercando di esaminare) può diventare schiacciante. Consiglio di provare entrambi. Ognuno di loro ha un uso e un valore a seconda di quello che si sta cercando di ottenere. È opportuno notare che qualsiasi dimensione può essere utilizzata nei flussi, mentre i percorsi devono essere impostati su una proprietà nel pannello di amministrazione.

I rapporti relativi a origini del traffico, [!DNL Campaign] e canali di marketing sono simili al rapporto Acquisizione di Google. Origini del traffico si concentra sui Referrer effettivi, [!DNL Campaign] si concentra sui tuoi Codici [!DNL Campaign] e Canali di marketing si concentra anche sui Codici [!DNL Campaign], ma applica anche una logica extra determinata da te su come elaborare le informazioni. [!DNL Adobe] offre maggiore libertà nella configurazione delle regole. Al contrario, Google fa molte cose per te, e questo rappresenta un cambiamento nel modo di pensare. Per impostazione predefinita, l&#39;attribuzione di Google per i codici [!DNL Campaign] è di sei mesi. Per impostazione predefinita, l&#39;attribuzione di [!DNL Adobe] è impostata su una settimana. Questo può essere modificato nelle impostazioni dell’amministratore, ma in Workspace puoi applicare l’attribuzione personalizzata a partire da qualsiasi dimensione per offrire una flessibilità molto più rapida.

I rapporti Mantenimento visitatori e Profilo visitatore sono simili ai rapporti Pubblico in Google [!DNL Analytics]. Il mantenimento si concentra maggiormente sulla frequenza di ritorno, mentre il profilo del visitatore si concentra maggiormente sulla geografia e sulla tecnologia degli utenti.

I rapporti Conversione personalizzata e Traffico personalizzato sono entrambi rapporti di dimensione personalizzati. Le conversioni sono eVar. Puoi impostare una scadenza personalizzata in base al valore come hit, visita, mese e anno. Questo valore rimane in persistenza per un utente per l’intervallo di tempo configurato, a meno che non venga sovrascritto. Le variabili di traffico sono proprietà. Puoi anche impostarli per i rapporti sui percorsi o come voci di elenco che suddividono più valori in base a un delimitatore scelto.

I contenuti multimediali sono per video o file audio in cui hai impostato un tracciamento speciale dei contenuti multimediali.

Rapporti personalizzati è una sezione in cui un utente può personalizzare le colonne e i raggruppamenti creati all’interno dell’interfaccia dei rapporti e salvarli come rapporto personalizzato. Tuttavia, come accennato in precedenza, poiché Workspace consente raggruppamenti e correlazioni molto più potenti, qualsiasi elemento personalizzato dovrebbe essere creato lì. Questa era una buona soluzione prima dell&#39;esistenza di Workspace.

La sezione Segnalibri è simile ai Rapporti personalizzati, dove i rapporti utilizzati di frequente possono essere contrassegnati con segnalibri all’interno dell’interfaccia dei rapporti, per facilitarne l’individuazione.

Dashboard era un prodotto legacy che consentiva alle persone di combinare reportlet di dati in un’unica visualizzazione. Tuttavia, la funzionalità di Workspace (sezione 2.1.2.1) è molto più semplice da utilizzare, in quanto esiste solo come punto di accesso ai rapporti precedenti che devono essere ricostruiti prima che questa funzione venga disattivata.

Le destinazioni consentono alle persone di creare un rapporto basato su una destinazione entro un determinato arco temporale. I team monitorano le campagne per vedere se sono sulla buona strada per raggiungere i loro target di traffico.

Tutti i rapporti qui consentiti per più colonne di metrica e raggruppamenti di dimensioni. Tuttavia, la semplicità delle visualizzazioni e parte della logica che sta dietro agli elementi che potrebbero essere correlati potrebbe a volte essere frustrante.

##### 2.1.3.2. Rapporti di Google [!DNL Analytics]

Google [!DNL Analytics] suddivide questi rapporti nelle sezioni seguenti: In tempo reale, Pubblico, Acquisizione, Comportamento e Conversazioni (in GA3) e in Ciclo di vita (con le sottosezioni: Acquisizione, Coinvolgimento, Monetizzazione, Mantenimento) e Utente (con le sottosezioni: Demografia e Tecnologia).

![google-analytics-interface-compare](assets/ga-to-aa_7.png)

Puoi apportare alcune modifiche minori a queste visualizzazioni, aggiungere una suddivisione secondaria delle dimensioni, modificare la visualizzazione, creare un filtro per i dati e altro ancora. Puoi salvare le personalizzazioni come Rapporto salvato.

In questo modo puoi ottenere informazioni semplici e veloci sui tuoi dati. Tuttavia, non è possibile confrontare elementi come Utenti con visualizzazioni di pagina per una pagina nella stessa tabella e non è possibile aggiungere più di una dimensione aggiuntiva per visualizzare dati aggiuntivi.

Questi vanno bene per i dati analitici rapidi, ma se hai davvero bisogno di scavare a fondo, soffrono dei limiti.

### 2.2. Accesso ai rapporti estesi

Oltre a &quot;Generazione rapporti in-site&quot;, la maggior parte degli strumenti offre funzionalità estese che consentono di portare l’analisi al di fuori degli strumenti e creare qualcosa di un po’ più personalizzato.

#### 2.2.1. [!DNL Adobe Analytics] Report Builder (estensione Microsoft® Excel)

Workspace è un ottimo strumento, ma a volte è necessario inserire i dati in un foglio di calcolo personalizzato, in modo da poter unire più origini di dati. Qui entra in gioco il Report Builder.

Report Builder è un plug-in per Microsoft® Excel che consente di creare connessioni ai dati di [!DNL Adobe Analytics] per estrarre dati tabulari modificabili in Excel. In genere, per utilizzarlo in modo efficiente, puoi inserire i dati in alcune schede di dati non elaborati, utilizzare poi i riferimenti alle celle excel per richiamare i dati da queste schede in un unico rapporto consolidato, quindi creare grafici e visualizzazioni.

>[!NOTE]
>
>Il Report Builder dispone di un’autorizzazione speciale che deve essere applicata agli utenti per accedere a questo plug-in. Questo dovrebbe essere concesso agli utenti che hanno imparato a utilizzare correttamente lo strumento.

#### 2.2.2. Connessione API [!DNL Adobe Analytics]

Se hai bisogno di [!DNL Adobe Analytics] dati per essere digeriti da qualcosa di diverso da Excel e desideri che i dati elaborati, comprese le esclusioni di regole bot, utilizza l&#39;API di [!DNL Adobe] per estrarre i dati direttamente. Quindi, elaborare i dati utilizzando uno script o aggiungerli a un database per l&#39;utilizzo con un altro sistema.

È opportuno notare che l’API estrae ancora i dati di correlazione applicando le suddivisioni e i segmenti come specificato nella richiesta pull.

Il Workspace di [!DNL Adobe] (sezione 2.1.2.1) utilizza l&#39;API per generare i rapporti. Se abiliti la modalità di debug in Workspace, potrai vedere le chiamate API utilizzate. Questo è un modo rapido per creare le tue chiamate API. Utilizzando Workspace per generare e convalidare i dati che desideri richiamare, puoi quindi utilizzare tali chiamate API per inserire i dati nella tua elaborazione.


#### 2.2.3. Google [!DNL Analytics] Data Studio

Se hai letto fino a qui, saprai già che ho citato Data Studio come equivalente di Workspace di [!DNL Adobe]. Data Studio consente di estrarre i dati di Google [!DNL Analytics], ma anche da altre origini. Questa funzione è utile per consolidare i dati di analisi con altri dati raccolti. Tuttavia, con Google [!DNL Analytics] sono presenti gli stessi tipi di limitazioni di visualizzazione. Il modo in cui vengono formate le righe e le colonne è ancora limitato.

È ancora uno strumento potente e non dissuaderei le persone da usarlo in alcun modo. La mia esperienza personale è che il comportamento rigido è piuttosto limitante.


#### 2.2.4. Estensione Foglio di calcolo Google

Per le mie esigenze, quando devo estrarre i dati in modo esteso da Google [!DNL Analytics], il mio strumento personale di scelta è l&#39;estensione Foglio di calcolo Google. Anche se ho bisogno di fare più connessioni alle mie tabelle GA, posso fare riferimento alle celle dai dati non elaborati e creare i rapporti di cui ho bisogno. Poi li visualizzo utilizzando le funzionalità di grafica di Foglio di calcolo di Google.


## 3. Esportazioni di dati grezzi

Quando si necessita di dati non elaborati, sia [!DNL Adobe] che Google offrono le funzionalità necessarie per richiamare le informazioni in questo modo.

### 3.1. Feed dati di [!DNL Adobe]

Nella sezione 2.2.2, ho menzionato che l&#39;API [!DNL Adobe Analytics] ha estratto da &quot;dati elaborati&quot;. Il feed di dati non elaborati richiama i dati elaborati dalle &quot;Regole di elaborazione&quot; configurate nel pannello di amministrazione, ma questi dati non elaborati includono tutti i dati esclusi altrove.

Questo significa che nei feed di dati non elaborati vengono inseriti tutti i dati filtrati di IP interni, le esclusioni di bot e altri dati esclusi. Esistono dei flag per identificare questi dati, in modo che, se si crea un data lake, il team tecnico possa creare una logica per elaborare i dati di conseguenza.

I feed di dati non elaborati possono essere personalizzati per inviare tutte le colonne di dati o solo colonne specifiche per un feed più mirato.

I feed possono essere inviati direttamente a FTP, SFTP o S3.


### 3.2. Google Big Query

Sfortunatamente, questo è uno strumento Google sul quale non ho alcuna esperienza di utilizzo. In teoria, dovrebbe essere simile al feed di dati di [!DNL Adobe], consentendo al team tecnico di accedere ai dati non elaborati dall&#39;account Google [!DNL Analytics].

Tuttavia, invece di fornire un dump completo dei dati non elaborati, consente ai tecnici di accedere ai dati tramite query SQL per estrarre dati non elaborati di destinazione o tutte le colonne di dati non elaborati.

## 4. Conclusione

Come qualsiasi sistema, è necessaria la pratica per acquisire dimestichezza con lo strumento. Questa guida ti aiuta a iniziare o fornisce suggerimenti per migliorare l&#39;utilizzo di [!DNL Adobe Analytics].

Ti consigliamo comunque di utilizzare sia [!DNL Adobe Analytics] che Google [!DNL Analytics] nella tua strategia di implementazione (anche se Google [!DNL Analytics] è solo nella versione gratuita). Questo consente di disporre di un sistema di backup per garantire la disponibilità di dati, poiché nessun sistema è infallibile.

Oltre a questa guida, sono disponibili molte risorse che possono contribuire a migliorare la tua strategia:

* [[!DNL Adobe] Experience League](https://experienceleague.adobe.com/?lang=it#home) - Contiene tutorial, video, documentazione e forum della community
* [[!DNL Adobe] Gruppi di utenti](https://analytics-augs.adobe.com/) - Hub di eventi gestiti dalla community per consentire agli utenti di connettersi tra loro e migliorare le implementazioni.
* [[!DNL Adobe Analytics] Canale YouTube gruppi utenti](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - Non puoi partecipare a una sessione del gruppo utenti [!DNL Adobe Analytics]? Guarda le sessioni precedenti da tutto il mondo e scopri come altri professionisti come te utilizzano questo strumento.
* [Canale di Slack di Measure Chat](https://www.measure.chat/) - Entra in contatto con [!DNL Adobe Analytics] utenti in tutto il mondo e condividi esperienze nel settore, fai domande ad altri professionisti come te e partecipa a gruppi di interesse incentrati sulla misurazione.
* e altro ancora!

## Autore

Questo documento è stato scritto da:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, Optimization Manager [!DNL Analytics] di Torstar

[!DNL Adobe Analytics] campione
