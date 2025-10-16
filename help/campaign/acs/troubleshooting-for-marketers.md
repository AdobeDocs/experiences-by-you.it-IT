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
exl-id: 1f27e284-73e3-4f28-988e-51163775eec8
source-git-commit: cae626cb3958ebcda16ac30b0a487ebfe06d50f4
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---

# Risoluzione dei problemi per gli addetti al marketing: 5 errori comuni di flusso di lavoro e consegna

Di: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Consulente Senior, Meijer

In qualità di Senior Engineer ed esperto cliente per [!DNL Adobe] prodotti Experience Cloud negli ultimi cinque anni, consento agli utenti aziendali di [Meijer](https://www.meijer.com/){target="_blank"}, una catena di supercentri americana fondata nel 1934, di eseguire complesse campagne di marketing e transazionali con ACS. Alcuni dei progetti su cui ho lavorato includono campagne personalizzate per memorizzare le offerte e dettagli degli ordini per la personalizzazione, integrate con [!DNL Adobe] Audience Manager, e customer insight per l&#39;inserimento dei segmenti.

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

## Errore Personalization di consegna

**Codice errore:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Causa:**
Questo errore viene visualizzato quando invii un’e-mail a un indirizzo, ma l’e-mail o qualsiasi altro identificatore non viene riconciliato con un profilo. Per inviare una comunicazione e-mail, l’e-mail o l’identificatore devono essere sempre collegati a un profilo.

![flusso di lavoro con attività di riconciliazione](/help/_assets/kt-13256/del-persn-error-wf.png)

**Soluzione:**
Deve esistere un ID comune dal file caricato con la tabella dei destinatari. Questa chiave comune unisce il file di caricamento alla tabella dei destinatari nell’attività di riconciliazione. Le e-mail non possono essere inviate a record che non esistono nella tabella dei destinatari che richiede questo passaggio di riconciliazione all’interno del flusso di lavoro. In questo modo, puoi riconciliare l’attività di caricamento file in ingresso con un identificatore come l’ID e-mail dal profilo. Lo schema `nms:recipient` fa riferimento alla tabella del profilo e la riconciliazione dei record in arrivo con il profilo lo rende disponibile durante la preparazione dell&#39;e-mail.

Fai riferimento alla schermata per l’attività di riconciliazione come mostrato di seguito.

![flusso di lavoro con dettagli di riconciliazione](/help/_assets/kt-13256/del-persn-error-wf-solution.png)

Ulteriori informazioni sulla [riconciliazione](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## Errore set di dati campo comune

**Codice errore:**

`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation.`

**Causa:**

Questo problema si verifica durante l&#39;utilizzo dell&#39;**attività di esclusione** nei flussi di lavoro ACS, durante l&#39;esecuzione di un&#39;esclusione basata sull&#39;ID, quando il set principale e il set escluso non hanno gli stessi nomi di campo.

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

È possibile che si verifichino punti di errore in un&#39;**attività di arricchimento**. Uno dei più comuni è mostrato di seguito.

![Errore Nome Campo Eliminato](/help/_assets/kt-13256/field-name-dropped-error.png)

Ciò si verifica quando si modifica manualmente il nome di un’espressione nell’attività. L&#39;immagine mostra che l&#39;espressione è stata modificata da `name` a `i__name`.

**Soluzione:**

È possibile risolvere questo errore in tre modi:

1. Ripristina il nome dell&#39;espressione presente in origine.

2. Se si desidera utilizzare un nuovo nome, modificare i valori nell&#39;**attività di arricchimento**.

3. Se non ricordi cosa è cambiato, la cosa migliore da fare è ricreare l’attività.

## Errore tabella temporanea eliminata 

**Codice errore:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Causa:**
Si tratta di un errore comune nei flussi di lavoro complicati che coinvolgono l’arricchimento o altre attività. Probabilmente alcuni dei flussi di lavoro delle attività non vengono salvati correttamente durante più modifiche al flusso di lavoro.

![Errore tabella temporanea ignorata ](/help/_assets/kt-13256/temp-table-dropped-error.png)

**Soluzione:**
Questo errore può verificarsi in diversi modi, pertanto non esiste una semplice correzione. Se si tratta di un flusso di lavoro semplice, è meglio riconfigurare l’attività. In un flusso di lavoro complesso, è meglio copiare le attività del flusso di lavoro in un nuovo flusso di lavoro, salvarle ed eseguirle nuovamente.
