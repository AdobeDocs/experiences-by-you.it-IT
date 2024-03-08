---
title: Standardizzare le convenzioni di denominazione
description: Le convenzioni di denominazione standard interessano sia il nome della variabile quando questa è abilitata nell’interfaccia utente di AA per l’amministratore, sia i valori trasmessi nella dimensione.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 79cec21e-2b52-4e7b-88ad-db137a8cef4e
source-git-commit: c568ed0a06551d910b6f533698ec47c15adecf6c
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 58%

---

# Standardizzare le convenzioni di denominazione

**COSA:** Le convenzioni di denominazione standardizzate si applicano sia al nome della variabile quando questa è abilitata nel [!DNL Adobe Analytics] (AA) interfaccia utente di amministrazione e valori trasmessi nella dimensione. Ad esempio, i nomi di pagina saranno “page name (v1)” come nome di variabile, e i valori di nome della pagina trasmessi devono essere uniformi e seguire una struttura o gerarchia specifica (come “sitename|homepage” oppure “sitename|search|searchresults”).

**PERCHÉ:** le convenzioni di denominazione sono un ottimo modo per mantenere tutto uniforme e rendere l’interfaccia facile da capire per i tuoi utenti. Se crei questi elementi fin dall’inizio e li applichi nella piattaforma e nel codice, in futuro sarà più semplice estenderli.

**COME:** L’interfaccia e il documento sui tag devono corrispondere per &quot;Nome&quot; e &quot;Descrizione&quot;; così gli utenti non dovranno usare un documento Excel e potranno comprendere i dati direttamente nell’interfaccia. Si consiglia inoltre di usare sempre lettere minuscole, per coerenza.

È sempre meglio mantenere coerenza tra i nomi delle pagine (o tra i nomi delle schermate per le app) anche all’interno della piattaforma. Ad esempio, puoi impostare &quot;`property:section:sub section:sub sub section:unique page name`&quot; in una variabile/dimensione. Se tutti questi sono campi separati nel livello dati, puoi anche creare il nome della pagina direttamente nel file JS o in Launch. Se tutti questi elementi sono impostati nelle proprie dimensioni, sarà più facile suddividere proprietà o aree specifiche del sito o dell’app e sarà possibile comprendere meglio il traffico e i flussi.

Qualsiasi cosa che consenta agli utenti di trovare e comprendere più facilmente i dati, compresi elementi semplici come le convenzioni di denominazione, aumenterà l’utilizzo di [!DNL Adobe Analytics] e fornire informazioni migliori per l&#39;azienda.

## Autori

Questo documento è stato scritto da:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digitale [!DNL Analytics] Platform Manager di NortonLifeLock
[!DNL Adobe Analytics] Campione

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant presso [!DNL Adobe]
