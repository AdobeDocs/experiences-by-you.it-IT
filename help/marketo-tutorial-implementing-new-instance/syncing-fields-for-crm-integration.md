---
title: Sincronizzazione dei campi per i connettori CRM nativi
description: Scopri come semplificare l’integrazione CRM iniziale selezionando strategicamente i campi CRM essenziali per Marketo Engage da utilizzare. Esegui l’esercizio del dizionario dati per identificare i campi necessari per una sincronizzazione fluida del sistema CRM che consenta ai team di vendita e marketing di rimanere allineati.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-04T00:00:00.000Z
jira: KT-14811
thumbnail: KT-14811.jpeg
exl-id: 42b7ca3d-e445-4c11-ad3d-d4e70c101c8e
product_v2:
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 749b293ab38b8ea5a5f72517bd5c3455399137c2
workflow-type: tm+mt
source-wordcount: '2235'
ht-degree: 0%
---
# Sincronizza campi per i connettori CRM nativi

Utilizzi Salesforce o Microsoft Dynamics all’interno della tua organizzazione? In tal caso, con i connettori CRM nativi di Marketo Engage (ad esempio Salesforce, Microsoft Dynamics e Veeva), puoi coordinare le attività di marketing e vendita condividendo direttamente informazioni rilevanti tra Marketo Engage e CRM. Prima di configurare la sincronizzazione CRM iniziale, accertarsi di identificare i campi che si desidera sincronizzare tra i due sistemi per mantenere pulito il database di Marketo Engage.

Scopri come eseguire questo esercizio con le best practice suggerite da Adobe Professional Services. Segui per comprendere i campi standard e i campi personalizzati e documenta le loro relazioni tra Marketo Engage e il tuo CRM.

## Identificare i campi da sincronizzare prima di integrare il CRM con Marketo Engage

Durante l’integrazione del CRM con Marketo Engage, probabilmente non dovrai sincronizzare tutti i campi del CRM con Marketo Engage. Un approccio strategico riguardo ai campi necessari può aiutare la tua istanza di Marketo Engage a elaborare il flusso di dati in modo più efficiente.

La sincronizzazione iniziale tra il Marketo Engage e il sistema CRM creerà automaticamente associazioni per la maggior parte dei campi standard esistenti (ad esempio e-mail, nome/cognome, società, ecc.). Inoltre, il connettore sincronizza anche [campi personalizzati](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} per lead, contatti, account e opportunità creando nuovi campi in Marketo Engage mappati automaticamente a tali campi dal CRM.

Identificare e organizzare i campi che si desidera sincronizzare dal CRM prima di eseguire la sincronizzazione iniziale è un passaggio fondamentale nel processo di configurazione del connettore nativo. Questo è un esercizio del dizionario dati che ti aiuta a ridurre al minimo il numero di campi duplicati che vengono creati e a fare in modo che tutti i passaggi successivi di mappatura funzionino nel modo più fluido possibile. In genere, questo esercizio richiede l’input dei team di marketing e vendita e dell’amministratore del sistema di gestione delle relazioni con i clienti per garantire che solo i campi rilevanti siano sincronizzati nell’istanza Marketo Engage.

## Creare il dizionario dati

In genere, la best practice prevede di sincronizzare solo i campi di gestione delle relazioni con i clienti che saranno necessari a scopo di marketing. Inizia con questo esercizio per organizzare i campi dal CRM che dovranno essere mappati a Marketo Engage ed eseguire la sincronizzazione CRM iniziale correttamente la prima volta.

>[!NOTE]
>Se nel CRM sono presenti campi personalizzati che dispongono già di un campo personalizzato equivalente in Marketo Engage prima di iniziare la sincronizzazione iniziale, viene creato un nuovo campo &quot;duplicato&quot; in Marketo Engage per il campo CRM. Puoi mappare nuovamente il campo CRM sul campo Marketo Engage originale e nascondere il campo duplicato una volta completata la sincronizzazione iniziale, ma a tale scopo devi contattare l&#39;[Assistenza clienti Adobe](https://experienceleague.adobe.com/it/docs/customer-one/using/home#create-a-support-ticket-with-admin-console){target="_blank"}. Per ulteriori informazioni, vedere il passaggio 7.

**Passaggio 1:** Crea un elenco approssimativo dei campi attualmente disponibili nel CRM e segnala se desideri che vengano visualizzati in Marketo Engage.

* Includi nel processo decisionale il feedback del tuo amministratore CRM, team di marketing e team di vendita.
* Documenta i nomi API e i tipi di campo per ciascun campo
* Determinare il livello di accesso che Marketo Engage deve avere per questi campi (ad esempio, sola lettura o lettura/scrittura)


**Passaggio 2:** Rivedi la sezione [Amministratore > Gestione campi](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/field-management/view-field-mappings-between-marketo-and-salesforce){target="_blank"} della tua istanza di Marketo Engage per identificare eventuali campi personalizzati creati in precedenza direttamente nel sistema che desideri includere nella sincronizzazione.

* Documenta i nomi API e i tipi di campo per ciascun campo.
* Indica i campi che hanno già un campo equivalente nel CRM.
* Indica i campi che non hanno già un campo equivalente nel CRM.


**Passaggio 3:** Inizia a creare il dizionario dati con i campi mappa predefiniti

* Poiché Marketo Engage utilizza un database flat, si consiglia di formattare il dizionario dati come segue:

  * Prima Colonna: Nomi Campi Marketo Engage
  * Seconda colonna: Nomi API di Marketo Engage
  * Terza colonna: [Tipo di campo Marketo Engage](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} (ad esempio booleano, valuta, data e così via)
  * Nelle colonne successive, ripeti per i tipi di oggetto CRM (Lead, Contatto, Account, Opportunità) con una colonna aggiuntiva per il livello di accesso che desideri che Marketo Engage abbia (ad esempio Lettura, Scrittura, Modifica)
  <br>

  Ecco un esempio di come apparirebbe:
  ![Tabella dizionario dati](/help/marketo-tutorial-implementing-new-instance/assets/data_dictionary.png){width="100%" zoomable="yes"}


* Per iniziare, aggiungi i campi predefiniti che verranno mappati automaticamente per il CRM:

  * [Salesforce](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/default-salesforce-field-mapping){target="_blank"}
  * [Microsoft Dynamics](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/default-dynamics-field-mapping){target="_blank"}
  * [Veeva](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/veeva-crm-sync/sync-details/default-veeva-field-mapping){target="_blank"}

* Conferma che ogni campo predefinito in Marketo Engage corrisponda al campo nel CRM con cui desideri eseguire la sincronizzazione. Ad esempio, il campo &quot;Annullamento iscrizione&quot; in Marketo Engage potrebbe essere il campo &quot;Rinuncia e-mail&quot; nel CRM.
* Se necessario, regola il nome API CRM, i privilegi e il tipo di dati [&#128279;](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"}.

**Passaggio 4:** Aggiungi campi aggiuntivi al dizionario dati

* Includi il Nome visualizzato, i privilegi CRM desiderati e il tipo di dati per ciascun campo.
* Se esiste un campo in CRM ma non in Marketo Engage, compila la visualizzazione Marketo Engage e i nomi API con gli stessi valori del campo CRM.
* Se esiste un campo in Marketo Engage ma non nel CRM, inserisci il nome visualizzato del CRM con il valore desiderato, ma lascia vuoto il nome API del CRM fino a quando non viene creato il campo.
* Se esistono campi equivalenti in entrambi i sistemi, includili sulla stessa riga e indica che devono essere rimappati nella sezione &quot;Note&quot; all’estrema destra del foglio del dizionario dati.

>[!NOTE]
>Se intendi creare un campo Filtro di sincronizzazione ([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"} | [Microsoft Dynamics](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/custom-dynamics-sync-filter-details/create-a-custom-dynamics-sync-filter){target="_blank"}), assicurati di includerlo in questo passaggio ma lascia vuoti i nomi API fino a quando il campo non viene creato nel CRM.

**Passaggio 5:** Rivedi il dizionario dati con il tuo amministratore CRM

* Crea campi in CRM per quelli che esistono già in Marketo Engage e aggiorna il dizionario dati con la visualizzazione e i nomi API per il nuovo campo CRM.
* Eseguire il mapping dei campi tra gli oggetti lead e contatto nel CRM ([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"} | [Microsoft Dynamics](https://community.dynamics.com/blogs/post/?postid=8a91d93e-2181-45dd-a8fb-1092010bc8f1){target="_blank"}). Quando un lead viene convertito in un contatto, questo assicura che i campi possano essere consolidati in un singolo campo in Marketo Engage.
* Assicurati che il profilo di sincronizzazione di Marketo disponga dei privilegi appropriati per ciascun campo, come indicato nel dizionario dati:
  * [Impostare le autorizzazioni del profilo in Salesforce](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited#set-profile-permissions){target="_blank"}
  * [Impostare le autorizzazioni del profilo in Microsoft Dynamics](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/microsoft-dynamics-365-with-s2s-connection/step-2-of-3-set-up#create-application-user-in-microsoft){target="_blank"}
  * [Impostare le autorizzazioni del profilo in Veeva](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/veeva-crm-sync/setup/step-2-of-3-create-a-veeva-crm-user-for-marketo-engage#set-profile-permissions){target="_blank"}

**Passaggio 6:** Eseguire la sincronizzazione iniziale

* Assicurati che tutti i campi che desideri sincronizzare con Marketo Engage dispongano dei privilegi appropriati nel CRM, come definito nel dizionario dati.
* Assicurati che tutti i campi che **non** vorresti sincronizzare con Marketo Engage siano [nascosti dal profilo di sincronizzazione di Marketo](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/hide-a-salesforce-field-from-the-marketo-sync){target="_blank"}. È molto più semplice aggiungere nuovi campi alla sincronizzazione in un momento successivo rispetto alla rimozione dei campi sincronizzati involontariamente.
* Stai connettendo il tuo CRM con il campo Filtro di sincronizzazione? Se esegui la sincronizzazione con Salesforce, contatta l’Assistenza clienti di Adobe per assicurarti che la funzionalità di filtro sia attivata prima di avviare la sincronizzazione iniziale.


**Passaggio 7:** Rivedi la sezione Gestione campi in Marketo Engage

* Conferma/aggiorna la visualizzazione e i nomi API per i nuovi campi sincronizzati.
* Identifica eventuali campi duplicati che potrebbero richiedere una nuova mappatura. I campi duplicati si verificano in alcuni scenari:
  * I campi personalizzati nella gestione delle relazioni con i clienti creano un nuovo campo (potenzialmente duplicato) in Marketo Engage la prima volta che vengono sincronizzati, se esiste già un campo equivalente in Marketo Engage.
  * Campi personalizzati di Marketo-Engage-Only (ovvero un campo creato direttamente in Marketo Engage) e potresti avere un campo equivalente sincronizzato dal sistema di gestione delle relazioni con i clienti.



**Passaggio 8:** Contatta l&#39;Assistenza clienti Adobe per eseguire la mappatura se vengono visualizzati campi duplicati

* Contatta il supporto con le seguenti informazioni per i campi da rimappare:
  * Nomi di visualizzazione e API per i nuovi campi duplicati creati dal sistema CRM.
  * Nome visualizzato per il campo Marketo Engage a cui si desidera mappare il campo CRM.
  * Fai riferimento a questo esempio [QUI](https://nation.marketo.com/t5/knowledgebase/re-mapping-sfdc-marketo-fields/ta-p/299284){target="_blank"}.
* Una volta completata la mappatura, controlla i nomi API per i campi rimappati in Marketo Engage e aggiorna i valori nella colonna &quot;Nome API&quot; del dizionario dati per assicurarti che contenga le informazioni più accurate.

## Cosa succede ora?

* Crea il dizionario dati per organizzare i campi per l’integrazione CRM.
* Acquisisci familiarità con il processo di sincronizzazione iniziale per il CRM

>[!BEGINTABS]

>[!TAB Salesforce]

Scopri come Marketo Engage e Salesforce si combinano per mantenere sincronizzati i dati di vendita e marketing.

>[!VIDEO](https://video.tv.adobe.com/v/3425610/?captions=ita&learn=on)

+++**Collegamenti utilizzati nel video:**

* [Informazioni su Salesforce Sync](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/understanding-the-salesforce-sync){target="_blank"}

* [Aggiungi campi Marketo a Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-1-of-3-add-marketo-fields-to-salesforce-enterprise-unlimited){target="_blank"}

* [Creazione di un utente Marketo in Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited){target="_blank"}

* [Connetti Marketo e Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-3-of-3-connect-marketo-and-salesforce-enterprise-unlimited){target="_blank"}

* [Gli utenti dovranno configurare l’app collegata sul lato Salesforce prima di passare a Marketo e Salesforce Sync.](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/log-in-using-oauth-2-0){target="_blank"}

* [Stato sincronizzazione Salesforce](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-status){target="_blank"}

* [Nascondere e scoprire un campo](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/field-management/hide-and-unhide-a-field){target="_blank"}

* [Tutorial: scopri come sincronizzare Marketo con il tuo sistema CRM](https://experienceleague.adobe.com/it/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn){target="_blank"}

+++

>[!TAB Microsoft Dynamics]

Scopri come funziona la sincronizzazione Microsoft Dynamics 365 e configura correttamente la configurazione per consentire ai due sistemi di parlare tra loro.

>[!VIDEO](https://video.tv.adobe.com/v/3430211/?captions=ita&learn=on)

+++**Collegamenti utilizzati nel video:**

* [Informazioni su Microsoft Dynamics Sync](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"}

* [Scarica la soluzione di gestione dei lead Marketo](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/download-the-marketo-lead-management-solution){target="_blank"}

* [Aggiornamento della soluzione Marketo per Microsoft Dynamics](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/update-the-marketo-solution-for-microsoft-dynamics){target="_blank"}

* [Concedere il consenso per la registrazione di ID client e app](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/grant-consent-for-client-id-and-app-registration)

* [Convalida sincronizzazione Microsoft Dynamics](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/validate-microsoft-dynamics-sync){target="_blank"}

* [Stato sincronizzazione](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/sync-status){target="_blank"}

* [Correggi i problemi di sincronizzazione della convalida Dynamics](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/fix-dynamics-validation-sync-issues){target="_blank"}

* [Creare un filtro di sincronizzazione Dynamics personalizzato](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/custom-dynamics-sync-filter-details/create-a-custom-dynamics-sync-filter.html?lang=it){target="_blank"}

* [Visualizza l&#39;URL del servizio organizzazione](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/view-the-organization-service-url){target="_blank"}

* [Modifica dei campi da sincronizzare prima di eliminarli in Dynamics](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/editing-fields-to-sync-before-deleting-them-in-dynamics){target="_blank"}

* [Tutorial: scopri come sincronizzare Marketo con il tuo sistema CRM](https://experienceleague.adobe.com/it/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn){target="_blank"}

+++

>[!ENDTABS]

### Autori

{{peter-livadas}}

{{amy-chiu}}
