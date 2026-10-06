---
title: Creare convenzioni di denominazione standard
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
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 749b293ab38b8ea5a5f72517bd5c3455399137c2
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%
---
# Creare convenzioni di denominazione standard

**COSA:** Le convenzioni di denominazione standard si applicano sia al nome della variabile quando questa è abilitata nell&#39;interfaccia utente di amministrazione di [!DNL Adobe Analytics] (AA), sia ai valori trasmessi nella dimensione. Ad esempio, i nomi di pagina sarebbero &quot;page name (v1)&quot; come nome di variabile e i valori di nome della pagina trasmessi dovrebbero essere uniformi e seguire una struttura o gerarchia specifica come &quot;sitename|homepage&quot; o &quot;sitename|search|searchresults&quot;.

**PERCHÉ:** le convenzioni di denominazione sono un ottimo modo per mantenere tutto uniforme e rendere l&#39;interfaccia facile da capire per i tuoi utenti. Se crei questi elementi fin dall’inizio e li applichi nella piattaforma e nel codice, in futuro sarà più semplice estenderli.

**COME:** L&#39;interfaccia e il documento sui tag devono corrispondere per &#39;Nome&#39; e &#39;Descrizione&#39;. In questo modo gli utenti non dovranno usare un documento Excel e potranno comprendere i dati direttamente nell&#39;interfaccia. Si consiglia inoltre di usare sempre lettere minuscole per coerenza.

È sempre meglio mantenere coerenza tra i nomi delle pagine (o tra i nomi delle schermate per le app) anche all’interno della piattaforma. Ad esempio, è possibile impostare &quot;`property:section:sub section:sub sub section:unique page name`&quot; in una variabile/dimensione. Se tutti questi sono campi separati nel livello dati, puoi anche creare il nome della pagina direttamente nel file JS o in Launch. Se tutti questi elementi sono impostati nelle proprie dimensioni, sarà più facile suddividere proprietà o aree specifiche del sito o dell’app e sarà possibile comprendere meglio il traffico e i flussi.

Qualsiasi cosa che consenta agli utenti di trovare e comprendere più facilmente i dati, compresi elementi semplici come le convenzioni di denominazione, aumenterà l&#39;utilizzo di [!DNL Adobe Analytics] e fornirà informazioni migliori per l&#39;azienda.

## Autori

Questo documento è stato scritto congiuntamente da:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital [!DNL Analytics] Platform Manager di NortonLifeLock
[!DNL Adobe Analytics] campione

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Consulente senior alle [!DNL Adobe]
