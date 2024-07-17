---
title: Creare un diagramma visivo del flusso di dati per comprendere lo stack tecnologico del marketing
description: Scopri come creare un diagramma di "Lead e origini dati" per comprendere l’universo dei dati, per controllare e riordinare l’istanza in modo efficiente.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13877
thumbnail: KT-13877.jpeg
hide: false
exl-id: 088bdcf1-4e49-44a7-ac78-a03742ff680b
source-git-commit: b2e05ff39e065691dda530ed17762a55cf2e6778
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 2%

---

# Creare un diagramma visivo del flusso di dati per comprendere lo stack tecnologico del marketing

In qualità di amministratore che assume il controllo di un&#39;istanza [!DNL Marketo Engage] che è attiva da anni, è come una missione impossibile controllare e riordinare l&#39;istanza in modo efficiente. Quando [!DNL Adobe] [!DNL Marketo Champion] (2019), Kelly Jo Horton, è entrata in un&#39;istanza consolidata, ha affrontato questa sfida [creando un diagramma di &quot;Lead and data sources&quot;](https://nation.marketo.com/t5/employee-blogs/understand-your-marketing-technology-and-data-create-this/ba-p/296774){target="_blank"} per acquisire familiarità con l&#39;universo dei dati. In questo tutorial imparerai a creare un diagramma di flusso dei dati personalizzato basandoti sugli esempi condivisi da Kelly Jo Horton. Impariamo a conoscere il tuo ecosistema MarTech!

## Perché creare un diagramma dell’architettura per l’istanza ereditata?

1. **Acquisisci familiarità con lo stack di tecnologia di marketing ereditato da un&#39;istanza live.** Tutti i responsabili delle operazioni di marketing e i responsabili delle operazioni della piattaforma sono invitati a eseguire questo esercizio quando si inizia da una nuova società. Questo processo di creazione consente agli utenti amministratori di visualizzare il quadro completo dei dati e delle attività inviate dalle integrazioni esterne a [!DNL Marketo Engage] e di risolvere facilmente gli errori API.
2. **Acquisisci familiarità con le principali parti interessate che gestiscono le integrazioni esterne.** Un suggerimento che Kelly Jo Horton utilizza per identificare rapidamente le parti interessate è quello di fare riferimento all&#39;elenco degli utenti API.
   1. **Passare alla scheda &#39;Integration>LaunchPoint&#39; nella sezione &#39;Admin&#39;.** Ulteriori informazioni su come passare alla scheda &#39;LaunchPoint&#39;: [Creare un servizio personalizzato da utilizzare con API REST](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api.html){target="_blank"}.
   2. Trova le statistiche sull’utilizzo dell’API per utente API nella scheda Integration>Web Services della sezione Informazioni sulla chiamata API. Facendo clic sul numero di chiamata API, puoi visualizzare le singole chiamate specifiche effettuate da ciascun utente.

## Come eseguire questo esercizio di diagramma del flusso di dati visivi

### Passaggio 1: Diagramma dello stato corrente

Creare un diagramma &quot;Stato corrente&quot;. Ecco un esempio:

![Diagramma dello stato corrente](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Current_State_Lead_Data_Sources_KellyJo_Horton.png){align="center"}


### Passaggio 2: Diagramma dello stato futuro

Creare un diagramma di &quot;Stato futuro&quot; da utilizzare per presentare la roadmap della tecnologia e dei sistemi a soggetti interessati non tecnici. Ecco un esempio:

![Diagramma dello stato futuro](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Future-State-Lead-Data-Sources-KellyJo-Horton.png){align="center"}

### Passaggio 3: versione tecnica

Creare una versione tecnica che mostri dettagli come il nome utente API per ogni integrazione, una breve descrizione del tipo di dati inviato a [!DNL Marketo Engage] o estratto da [!DNL Marketo Engage] e un diagramma dettagliato di tutti i flussi e i trigger middleware.  Ecco un esempio:

![Versione tecnica](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Lead-Data-Source-Diagram-KellyJo-Horton.png){align="center"}


## Quali sono le prossime novità?

**Introduzione agli esempi:**
Scarica uno dei diagrammi di esempio del flusso di dati per mappare lo stato corrente dello stack tecnologico di marketing, della persona e del flusso di dati oppure crea un diagramma per l’universo di dati da zero durante l’audit dell’istanza:


<table style="table-layout:fixed">
   <tr>  
      <td style="border: 0;">
      <div style="text-align: center;">
          <a href="./_assets/downloads/Current_Future_State_Lead_Data_Sources.zip">
            <strong>Stato corrente e stato futuro</strong>
         </a>
      </div>
      </td>
      <td style="border: 0;">
      <div style="text-align: center;">
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <strong>Livelli dettagliati per categoria funzionale </strong>   
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Lead_Data_Source.zip">
           <strong>Flusso lead e Source dati </strong>  
         </a>
         </div>
       </td> 
       <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
          <strong>Diagramma semplificato</strong>  
         </a>
         </div>
        </td>  
   </tr>
   <tr>
    <td style="border: 0;">
         <div>
          <img alt="Diagramma stato corrente e stato futuro" src="./_assets/Thumbnail_Current-Future State Lead_Data Sources_KellyJo_Horton.png"/>
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div>
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <img alt="Livelli dettagliati per diagramma categorie funzionale" src="./_assets/Thumbnail_Detailed_Layers_by_Functional_Category_Stacked_Technologies_KellyJo_Horton.png" />
       </a>
         </div>
      </td>
       <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Lead_Data_Source.zip">
         <img alt="Diagramma di flusso di Lead e Data Source" src="./_assets/Thumbnail_Lead-Data Source Diagram_KellyJo_Horton.png" />
         </a>
         </div>
      </td>
     <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
             <img alt="Diagramma semplificato" src="./_assets/Thumbnail_Simple_World_Class_Stage_Stack.png" />
         </a>
         </div>
      </td>
</table>

Questi sono alcuni strumenti che puoi utilizzare: draw.io (Google Docs), [!DNL Adobe] XD, Figma, Gliffy (in Confluence)

**Cosa succede se sono già presenti diagrammi di architettura?** I nuovi membri del gruppo potrebbero avere prospettive diverse. È importante che i nuovi amministratori di [!DNL Marketo Engage] facciano questo esercizio come parte del loro processo di onboarding e lo condividano con altri.

## Autori

**Kelly Jo Horton**\
[!DNL Adobe] Marketo Champion (2019)
*Partner senior presso Etumos*

![Kelly Jo Horton](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Kelly_Jo_Horton.png){width="30%"}

**Amy Chiu**
*Responsabile marketing per l&#39;adozione e il mantenimento,[!DNL Adobe]*

(/help/marketo-tutorial-inherited-instance/_assets/authors/[!DNL Adobe]_Author_Amy_Chiu.png){width=30%}
