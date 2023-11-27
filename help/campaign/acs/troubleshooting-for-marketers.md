---
title: Risoluzione dei problemi per gli addetti al marketing
description: Conoscere gli errori più comuni può aiutare a risolvere i problemi più rapidamente e a migliorare la produttività. Questi suggerimenti per la risoluzione dei problemi consentono di risolvere in modo efficace errori simili quando si verificano.
solution: Campaign Standard
feature-set: Campaign
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
exl-id: 24a6815b-52d1-4bd6-9d27-522720a91f83
source-git-commit: 35e62c4f1a093b4f755e175e9b553a43887e4292
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 3%

---

# Risoluzione dei problemi per addetti al marketing: 5 errori comuni di flusso di lavoro e consegna

Di: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Consulente senior, Meijer

In qualità di Senior Engineer ed esperto cliente per [!DNL Adobe] Experience Cloud prodotti per gli ultimi cinque anni, consento agli utenti aziendali di [Meijer](https://www.meijer.com/){target="_blank"}, catena di supercentri americana fondata nel 1934, per gestire campagne di marketing e transazionali complesse con ACS. Alcuni dei progetti su cui ho lavorato includono campagne personalizzate per archiviare le offerte e dettagli degli ordini per la personalizzazione, integrate con [!DNL Adobe] Audience Manager e approfondimenti sul cliente per l’inserimento dei segmenti.


Durante il mio periodo di utilizzo di ACS, ho riscontrato errori che possono richiedere molto tempo e che possono essere frustranti da risolvere. Conoscere gli errori più comuni può aiutare a risolvere i problemi più rapidamente e a migliorare la produttività. Di seguito sono riportati alcuni suggerimenti per la risoluzione dei problemi che consentono di risolvere in modo efficace errori simili quando si verificano.

## Errore di mancata corrispondenza del tipo di dati

**Codice errore:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**Causa:**
Questi tipi di errori vengono visualizzati in un flusso di lavoro quando si tenta di eseguire la riconciliazione utilizzando campi di tipi di dati diversi. Ad esempio, quando carichi un file utilizzando il file di caricamento che ha un campo stringa e tenti di riconciliare il campo stringa con un campo profilo che ha il tipo di dati int.

![data-type-mismatch-error](/help/_assets/kt-13256/data-type-mismatch.png)

**Soluzione:**
Modifica il tipo di dati del campo nell’attività &quot;Carica file&quot; con quello corrispondente. Apri l’attività &quot;Load File&quot;. Passare alla scheda &quot;COLUMN DEFINITION&quot; e modificare il tipo di dati del campo desiderato.


![data-type-mismatch-solution](/help/_assets/kt-13256/data-type-mismatch-solution.png)

## Errore di personalizzazione consegna

**Codice errore:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Causa:**
Questo errore viene visualizzato quando invii un’e-mail a un indirizzo, ma l’e-mail o qualsiasi altro identificatore non viene riconciliato con un profilo. Per inviare una comunicazione e-mail, l’e-mail o l’identificatore devono essere sempre collegati a un profilo.

![flusso di lavoro con attività di riconciliazione](/help/_assets/kt-13256/del-persn-error-wf.png)

**Soluzione:**
Deve esistere un ID comune dal file caricato con la tabella dei destinatari. Questa chiave comune unisce il file di caricamento alla tabella dei destinatari nell’attività di riconciliazione. Le e-mail non possono essere inviate a record che non esistono nella tabella dei destinatari che richiede questo passaggio di riconciliazione all’interno del flusso di lavoro. In questo modo, puoi riconciliare l’attività di caricamento file in ingresso con un identificatore come l’ID e-mail dal profilo. Il `nms:recipient` lo schema fa riferimento alla tabella del profilo e la riconciliazione dei record in arrivo con il profilo lo rende disponibile durante la preparazione dell’e-mail.

Fai riferimento alla schermata per l’attività di riconciliazione come mostrato di seguito.

![flusso di lavoro con dettagli di riconciliazione](/help/_assets/kt-13256/del-persn-error-wf-solution.png)

Ulteriori informazioni su [riconciliazione](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## Errore set di dati campo comune

**Codice errore:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**Causa:**
Questo problema si verifica durante l’utilizzo di **attività di esclusione** nei flussi di lavoro ACS, quando si esegue un’esclusione basata sull’ID, quando il set Primary e il set escluso non hanno gli stessi nomi di campo.


![Errore set di dati campo comune](/help/_assets/kt-13256/dataset-error.png)

**Soluzione:**

Esistono due modi per risolvere questo errore:

1. Utilizza lo stesso nome di campo sia nel campo principale che in quello escluso e utilizza tale campo come ID

   O

2. Utilizzare il metodo di esclusione JOIN per selezionare il campo in base al quale si desidera escludere i record.

![Errore set di dati campo comune - Soluzione ](/help/_assets/kt-13256/dataset-error-solution.png)

## Errore nome campo ignorato

**Codice errore:**
`XTK-170036 Unable to parse expression 'i__name'`

**Causa:**

I punti di errore possono verificarsi in un **attività di arricchimento**. Uno dei più comuni è mostrato di seguito.

![Errore nome campo ignorato](/help/_assets/kt-13256/field-name-dropped-error.png)

Ciò si verifica quando si modifica manualmente il nome di un’espressione nell’attività. L’immagine mostra che l’espressione è stata modificata da `name `a `i__name`.

**Soluzione:**

È possibile risolvere questo errore in tre modi:

1. Ripristina il nome dell&#39;espressione presente in origine.

2. Se desideri utilizzare un nuovo nome, modifica i valori in **attività di arricchimento**.

3. Se non ricordi cosa è cambiato, la cosa migliore da fare è ricreare l’attività.

## Errore tabella temporanea eliminata 

**Codice errore:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Causa:**
Si tratta di un errore comune nei flussi di lavoro complicati che coinvolgono l’arricchimento o altre attività. Probabilmente alcuni dei flussi di lavoro delle attività non vengono salvati correttamente durante più modifiche al flusso di lavoro.

![Errore tabella temporanea eliminata ](/help/_assets/kt-13256/temp-table-dropped-error.png)

**Soluzione:**
Questo errore può verificarsi in diversi modi, pertanto non esiste una semplice correzione. Se si tratta di un flusso di lavoro semplice, è meglio riconfigurare l’attività. In un flusso di lavoro complesso, è meglio copiare le attività del flusso di lavoro in un nuovo flusso di lavoro, salvarle ed eseguirle nuovamente.
