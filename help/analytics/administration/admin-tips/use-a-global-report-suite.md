---
title: Utilizzare una suite di rapporti globale
description: L’utilizzo di una singola suite di rapporti globale può essere utile in molti modi e può semplificare notevolmente la tua implementazione.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
exl-id: f133d049-9a24-4153-88c5-40ec480d1e4e
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Utilizzare una suite di rapporti globale

**COSA:** Si può essere tentati di creare una suite di rapporti per ciascuno dei siti, ma questo può rapidamente diventare il peggiore incubo, complicando sia le attività di reporting che l&#39;implementazione. L’utilizzo di una singola suite di rapporti globale può essere utile in molti modi e può semplificare notevolmente la tua implementazione.

**PERCHÉ:** La creazione di una suite di rapporti globale è l&#39;unica opzione disponibile per avere una visualizzazione unificata delle proprietà digitali e dei percorsi di utenti in ogni proprietà. Se hai un’app mobile e un sito web, devi sempre combinare i dati dell’app e i dati web in una singola suite di rapporti per sfruttare i percorsi multidispositivo e tenere traccia di coloro che visitano entrambe le proprietà come un singolo visitatore, invece di avere suite di rapporti separate, in cui un set di dati disgiunto mostra 2 visitatori, uno per ogni proprietà, senza la possibilità di incrociare le attività.

Di seguito sono riportati i vantaggi/svantaggi di avere una singola suite di rapporti per aiutarti a scegliere:

* PRO:
   * Essere in grado di comprendere facilmente l&#39;intero panorama digitale. Se hai implementato la dimensione &quot;proprietà&quot; (eVar) a cui si fa riferimento in altri suggerimenti, potrai facilmente ottenere un’unica vista per tutti i tuoi siti e le tue app, con i relativi dati di traffico e conversioni. Questa visione d’insieme è fondamentale per comprendere il tuo business nel suo complesso.
   * Allo stesso modo, ora puoi vedere come gli utenti passano da una proprietà all’altra e capire il loro percorso in tutto il tuo panorama digitale.
   * Facilità di amministrazione. Quando utilizzi più suite di rapporti, devi mantenere l’interfaccia in diverse posizioni, nonché diversi documenti sui tag (o più complessi). Mantenendo tutto in un’unica posizione, sarà sufficiente apportare gli aggiornamenti in un’unica posizione. Inoltre, è molto più facile garantire l&#39;accesso.
   * Migliore usabilità nell’interfaccia. Se gli utenti dispongono di un solo percorso per andare, non devono pensare a quale suite di rapporti selezionare. Tieni presente che non puoi utilizzare più suite di rapporti all’interno dello stesso pannello dell’area di lavoro e che averne diverse potrebbe confondere i tuoi utenti.
   * Meno chiamate server = meno costi. Se effettui chiamate a più suite di rapporti, aumenti i costi. Mantenere semplice l’implementazione consente inoltre di ridurre i costi.
   * Puoi semplicemente sfruttare le suite di rapporti virtuali (VRS) per suddividere i dati specifici del sito all’interno della suite di rapporti globale e, se necessario, limitare le autorizzazioni utente in base a una VRS. Una volta separati i dati in suite di rapporti individuali, non puoi aggregarli, ma se sono già uniti in un set di dati (suite di rapporti globale), possono essere facilmente suddivisi.
* CONTRO:
   * Se le tue proprietà sono molto diverse e gli utenti non possono passare dall’una all’altra, né è previsto che possano farlo, puoi mantenere suite di rapporti separate.
   * Se le proprietà hanno esigenze di tag e reporting molto diverse, può essere utile impostare suite di rapporti separate nell’interesse dell’efficienza delle variabili. Disporre di suite di rapporti separate offre maggiore flessibilità nell’utilizzo di variabili personalizzate (più eVar).
   * Valori univoci superati: l&#39;interfaccia [!DNL Adobe Analytics] consente di visualizzare solo 500.000 valori univoci in una singola dimensione per un determinato periodo di tempo. Una volta superato questo limite, i valori verranno raggruppati nell’interfaccia come &quot;valori univoci superati&quot; o &quot;traffico ridotto&quot;. Questi valori rimangono disponibili sul backend (ad esempio Data Warehouse, Feed dati), ma non possono essere visualizzati all’interno dell’interfaccia. Se disponi di dati molto granulari (come ID utente, PSN, ecc.), è facile raggiungere questo livello. Questo problema può essere risolto utilizzando suite di rapporti separate.

**COME:** Iniziare con una nuova implementazione di AA e utilizzare una suite di rapporti globale è semplice. È sufficiente creare la suite di rapporti globale (una per Dev e una per Prod) nell’interfaccia utente di amministrazione di AA e applicare gli stessi valori ID suite di rapporti (RSID) in tutte le proprietà.

La migrazione da una strategia a più tag con una suite di rapporti univoca per ogni proprietà richiede più strategia e pianificazione. Alcune considerazioni da tenere a mente:

* L’allineamento delle variabili (ad esempio, eVar1 nella proprietà A deve acquisire lo stesso punto dati di eVar1 nella proprietà B)
* Consolidamento di eventuali regole di elaborazione, regole del canale di marketing, classificazioni (SAINT e Rule Builder)
* Migrazione di feed di dati e origini dati
* Scelta di una data di interruzione e comunicazione con tutti gli utenti aziendali

## Autori

Questo documento è stato scritto congiuntamente da:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital [!DNL Analytics] Platform Manager di NortonLifeLock
[!DNL Adobe Analytics] campione

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Consulente senior alle [!DNL Adobe]
