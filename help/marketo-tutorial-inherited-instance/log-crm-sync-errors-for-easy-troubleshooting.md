---
title: Registra gli errori di sincronizzazione CRM per una facile risoluzione dei problemi
description: Scopri come utilizzare un registro di errori di sincronizzazione CRM per analizzare i problemi di sincronizzazione CRM e mantenerli in esecuzione senza problemi.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00.000Z
jira: KT-13875
thumbnail: KT-13875.jpeg
exl-id: 6a38f5dd-5d25-43d8-a1d3-e75ab396e555
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
  - id: d1d0a9cd-295d-4976-8c39-ddae266f240e
    internal-label: Administration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 749b293ab38b8ea5a5f72517bd5c3455399137c2
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%
---
# Registra gli errori di sincronizzazione CRM per la risoluzione dei problemi

In qualità di amministratore [!DNL Marketo Engage], verificare se l&#39;istanza è sincronizzata con il CRM deve essere una parte chiave della [routine giornaliera](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. Mentre la [sezione Notifiche](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html?lang=it){target="_blank"} (trovala nell&#39;angolo in alto a destra dell&#39;interfaccia [!DNL Marketo Engage]) è il luogo in cui inizierai a trovare e analizzare i frequenti problemi di sincronizzazione, esiste un suggerimento pro che potrebbe aiutarti a gestire lo stato dell&#39;istanza in modo organizzato. [!DNL Adobe] Marketo Champion (2019-2022), Amy Goldfine consiglia agli utenti amministratori di mantenere un registro degli errori di sincronizzazione CRM per semplificare la risoluzione dei problemi.

![Schermata della scheda Errori di sincronizzazione](/help/marketo-tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Perché tenere traccia degli errori di sincronizzazione CRM?

Registrando gli errori di sincronizzazione CRM, gli amministratori di [!DNL Marketo Engage] possono esaminare i problemi e le tendenze con gli amministratori di CRM per correggere la causa principale. Segui i passaggi seguenti per documentare i problemi di sincronizzazione CRM per la tua istanza.

## Come mantenere un registro degli errori di sincronizzazione CRM

Prima di iniziare, scaricare il modello di registro degli errori di sincronizzazione di [CRM](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Passaggio 1:** Vai alla *[!UICONTROL sezione Amministratore]* in [!DNL Marketo Engage]. In *[!UICONTROL Integrazione]*, fare clic su *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* o *[!DNL Veeva]*, a seconda di quale [!DNL CRM] si utilizza, quindi sulla scheda *[!UICONTROL Errori di sincronizzazione]*.

**Passaggio 2:** Puoi scegliere di [esportare i record di errori come file [!DNL CSV] tramite il pannello [!UICONTROL Filtro]](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html?lang=it#filter-sync-errors){target="_blank"}. Se hai solo poche ore, è consigliabile copiare e incollare direttamente dalla scheda *[!UICONTROL Errori di sincronizzazione]*.

**Passaggio 3:** Prendere nota della data in cui si è verificato l&#39;errore.

**Passaggio 4:** Immettere il numero di record persona interessati dall&#39;errore. (A volte il CRM genera un errore solo per una persona. A volte ci saranno molte persone con lo stesso errore contemporaneamente.)

**Passaggio 5:** Prendere nota dell&#39;indirizzo di posta elettronica di una persona interessata dall&#39;errore. In questo modo è facile fare riferimento e discutere gli errori con l’amministratore di CRM.

**Passaggio 6:** Incolla i collegamenti al record persona in [!DNL Marketo Engage] e al [!UICONTROL record Contatto/lead CRM] di tale persona.

**Passaggio 7:** Nell&#39;ultima colonna incollare il testo effettivo dell&#39;errore.

## Cosa succede ora?

**Identificare i codici di errore:** Per comprendere i codici di errore, cercare le descrizioni nella documentazione per gli sviluppatori [Tabella dei codici di errore a livello di risposta](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} e trovare i passaggi successivi tipici per risolvere gli errori.

## Autori

**Amy Goldfine**\
[!DNL Adobe] Marketo Champion (2019-2022)
*Fondatore, MarketingOpsAdvice.com*

![Amy Goldfine](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Responsabile marketing per l&#39;adozione e il mantenimento in[!DNL Adobe]*

![Amy Chiu](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
