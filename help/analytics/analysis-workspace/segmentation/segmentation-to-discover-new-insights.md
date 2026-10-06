---
title: Ora attendi un segmento. Utilizzo della segmentazione per scoprire nuove informazioni in Analysis Workspace
description: Scopri come utilizzare i segmenti in [!DNL Adobe Analytics] per scoprire nuove informazioni dalle visualizzazioni e dalle tabelle a forma libera di Analysis Workspace.
feature-set: Analytics
feature: Segmentation
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00.000Z
jira: KT-13268
thumbnail: KT-13268.jpeg
exl-id: 3496b6ff-f8d6-48a1-92f4-442a792663e7
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: c68cd75e-5bca-4bc3-a60e-9e183f816441
    internal-label: Experience Manager Cloud Manager
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ed6be6bb-75bb-4ea9-9a42-3bcaa65e1bcc
    internal-label: Personalization
subfeature_v2:
  - id: a1d50dda-6d94-4e16-8c30-5eb7181c4650
    internal-label: Segmentation
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 749b293ab38b8ea5a5f72517bd5c3455399137c2
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 2%
---
# Ora attendi un segmento. Utilizzo dei segmenti per scoprire nuove informazioni in Analysis Workspace

Che tu sia un nuovo utente di [!DNL Adobe Analytics] o un professionista esperto, sfrutterai i segmenti piuttosto bene nei tuoi progetti Analysis Workspace. Come descritto da [[!DNL Adobe] Experience League](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=en), &quot;i segmenti ti consentono di identificare sottoinsiemi di visitatori in base a caratteristiche o interazioni con siti Web.&quot; Anche se il risultato di base di questa funzione consiste nell’isolare gruppi di utenti, visite o hit sul sito, un analista attento come te può diventare creativo con questo strumento e trovare nuovi modi per ottenere informazioni approfondite sull’attività del sito. L&#39;elenco delle opzioni possibili è molto ampio, quindi non esitare a creare la tua e a condividerla con altri utenti dell&#39;organizzazione o online in community come la [[!DNL Adobe Analytics] Community](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community) su Experience League o la community [#Measure Slack](https://www.measure.chat/).

Se hai bisogno di un rapido aggiornamento su come creare un segmento, consulta la documentazione di Experience League sull&#39;utilizzo di [Segment Builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=en) in Analysis Workspace.

## Confronto e contrasto dei segmenti

In Analysis Workspace puoi confrontare due segmenti utilizzando &quot;[Confronto segmenti](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html?lang=en)&quot;. Il confronto dei segmenti si trova nella sezione Pannelli della barra di navigazione a sinistra:

![Seg 01](assets/seg01.png)

Tuttavia, a volte non è necessario un pannello di confronto completo per fornire informazioni chiave agli utenti finali. Fortunatamente alcune funzioni possono essere confrontate anche in un pannello standard.

La visualizzazione [Diagramma di Venn](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=en) consente di creare un confronto rapido, che consente di passare il puntatore del mouse e visualizzare le sessioni, gli ordini, gli utenti e così via sovrapposti tra 2 e 3 segmenti personalizzati. Puoi anche creare rapidamente i segmenti facendo clic con il pulsante destro del mouse su una delle sezioni sovrapposte:

![Seg 02](assets/s02.png)

A volte le informazioni importanti non si trovano nei dati sovrapposti, ma nei dati che non si sovrappongono. Un modo rapido per visualizzarlo è creare una copia di un segmento e renderlo un segmento &quot;Escludi&quot;:

![Seg 03](assets/s03.png)

Impilando il segmento &quot;escludi&quot; con l’altro segmento nel confronto, ora puoi calcolare rapidamente quante visite hanno colpito la pagina del menu senza visualizzare anche la pagina principale nella stessa sessione:

![Seg 04](assets/s04.png)

## Attacco stack

Allo stesso modo, potete creare i dati di intersezione di un diagramma di Venn semplicemente impilando tutti i segmenti. Non esiste alcun limite al numero di segmenti o singole dimensioni sovrapposte. Per esempio, se volevo scoprire rapidamente quali Giorni della Settimana il mese scorso il mio sito ha avuto una visita su un telefono cellulare, in particolare un Samsung Galaxy A52, che ha visto il mio menu e le pagine di nutrizione, ma NON ha visto la mia home page, Posso costruirlo rapidamente al volo come questo:

![Seg 05](assets/s05.png)

Ma ancora meglio, una volta trovato quel sottoinsieme perfetto del mio utente o base di visita, posso selezionare tutti questi valori, fare clic con il pulsante destro del mouse e creare un segmento all&#39;istante:

![Seg 06](assets/s06.png)

![Seg 07](assets/s07.png)

![Seg 08](assets/s08.png)

In un segmento c&#39;è molta potenza.

## Un segmento di numeri per un numero di segmenti

Molti utenti spesso considerano i valori nominali, ordinali o di intervallo durante la creazione di segmenti, ad esempio una pagina visitata, una fascia di età degli utenti o il numero di visite effettuate da un utente in passato. Tuttavia, puoi utilizzare anche i dati del rapporto durante la creazione di un segmento raggruppando questi valori, che si tratti di dimensioni standard, metriche standard o variabili e metriche personalizzate per la tua organizzazione.

Ad esempio, Time Spent on Page (Tempo trascorso su pagina) o Time Spent per Visit (Tempo trascorso per visita) dispone di contenitori predefiniti:

![Seg 09](assets/s09.png)

Tuttavia, queste potrebbero non sempre corrispondere alle esigenze della tua organizzazione: probabilmente la maggior parte delle visite al sito non durano più di 10 minuti. Puoi utilizzare la misurazione granulare per creare contenitori di dimensioni diverse. Eccone una creata per esaminare le visite che durano tra 1 minuto, 1 secondo e 1 minuto, 30 secondi:

![Seg 10](assets/s10.png)

Una volta creato, posso ora iniziare a esaminare le mie visite, gli ordini e altri eventi in base ai diversi gruppi di tempo a blocchi che ho personalizzato:

![Seg 11](assets/s11.png)

Puoi anche iniziare a esaminare il cambiamento degli indicatori di prestazioni chiave (KPI, Key Performance Indicators) come fattore del tempo trascorso da un utente, del numero di pagine visitate in una visita, del numero di volte che ha visitato in passato o di qualsiasi altro valore numerico, che ti consente di guardare una metrica come fattore di un’altra metrica:

![Seg 12](assets/s12.png)

Le possibilità di utilizzare i segmenti per trovare nuove informazioni sono infinite. Questo è semplicemente un punto di partenza. Prova con alcune e comunica alla community cosa scopri: [[!DNL Adobe Analytics] Community](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community) su Experience League o la community [#Measure Slack](https://www.measure.chat/).

Buona segmentazione!

## Autore

Questo documento è stato scritto da:

![Dan Cummings](assets/seg13.png)

**Dan Cummings**, Sr. Direttore tecnico [!DNL Analytics] presso McDonald&#39;s Corporation

[!DNL Adobe Analytics] campione
