---
title: Sviluppare una guida alla governance delle istanze con la relativa documentazione
description: Scopri come stabilire una solida procedura per la creazione e la manutenzione della documentazione e del registro delle modifiche per il tuo [!DNL Marketo Engage] dell'istanza. In questo modo non solo si risparmia tempo per la condivisione delle conoscenze del team, ma si migliora anche lo stato e l’efficienza dell’istanza.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: false
exl-id: e127b84d-ef92-4527-a0e6-a36af35b7ee0
source-git-commit: 26805f8f9edf3a3a3a38c4cb954e07378f13920d
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Sviluppare una guida alla governance delle istanze con la relativa documentazione

Quando si entra in una [!DNL legacy [!DNL Marketo Engage]] , spesso si scontra con la difficoltà di non disporre di una documentazione tecnica e funzionale aggiornata. In qualità di amministratore, stabilire linee guida per garantire una corretta governance delle istanze è una responsabilità fondamentale che non puoi ignorare. Si tratta di una delle strategie fondamentali per [aumentare l&#39;efficienza mentre si lavora in un ambiente [!DNL Marketo Engage] istanza](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Questo tutorial dettagliato proviene da [!DNL [!DNL Adobe] Marketo Champion] (2018), Nick Hajdin, ti guiderà attraverso questo processo per delineare la configurazione della tua istanza, documentare i programmi operativi principali e mantenere un [!DNL changelog] per applicare una rigida politica di governance.

## Perché sviluppare una guida alla governance delle istanze e una documentazione per l’istanza ereditata?

Documentazione dettagliata e [!DNL changelog] sono essenziali per una gestione e un trasferimento delle conoscenze efficienti all&#39;interno del [!DNL [!DNL Marketo Engage]]. Tenere traccia delle modifiche e delle decisioni apportate durante la configurazione dell’istanza può aiutarti a:

1. Formare gli utenti interni più facilmente e in modo scalabile.
2. Generare in modo più efficiente in [!DNL [!DNL Marketo Engage]] a lungo termine.
3. Mantenere la salute e l&#39;igiene della tua istanza andando avanti per risparmiare le ore di lavoro scavando nelle e-mail, [audit trail](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html), e [registro attività](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) per ottenere il contesto.
4. Risparmio di tempo durante il trasferimento di [!DNL [!DNL Marketo Engage]] nuovo [!DNL [!DNL Marketo Engage]] amministratore in caso di turnover del team.

## [!DNL [!DNL Marketo Engage]] guida alla governance 101

Una guida alla governance funge da fonte di verità per la configurazione dell’istanza e i requisiti di progettazione del sistema. Le informazioni chiave che si consiglia di includere in questo documento sono:

* Strutture di programmi/cartelle
* Autorizzazione utente e ruolo
* Limiti di comunicazione
* Standard di governance
* Formazione interna degli utenti prima di concedere loro l’accesso alla piattaforma

## Come sviluppare e gestire una guida alla governance per [!DNL [!DNL Marketo Engage]] istanza

### Passaggio 1: identifica la guida e la documentazione sullo stato attuale della governance

* **Non è possibile individuare la documentazione per la mia istanza ereditata:** Se di recente hai avviato un nuovo ruolo e non riesci a individuare alcuna documentazione per l’istanza ereditata, **vai al passaggio 2** e inizia a usare un modello scaricabile che abbiamo fornito.
* **Ho la documentazione sul file:** Congratulazioni, questo è un buon segno! Assicurati di rivederne la rilevanza per vedere quando viene apportata l’ultima modifica. Se non viene gestito attivamente dai membri del gruppo, si consiglia di aggiornarlo e di istruire gli utenti interni su come mantenerlo aggiornato.

### Passaggio 2: identificare gli elementi da includere in [!DNL [!DNL Marketo Engage]] Documentazione e [!DNL Changelogs]

Il formato varia da una piattaforma basata su cloud a un documento condiviso. Puoi progettare il formato che soddisfi le esigenze della tua organizzazione. [Ecco una semplice documentazione e un modello di Excel changelog](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) sugli elementi importanti con cui puoi iniziare. Comprendono:

* Documentazione
   * Nome modello programma
   * Channel
   * Data creazione
   * Creato da
   * Scopo del programma
   * Stato
   * Collega al modello del programma
   * Nota
* Changelog
   * Nome modello programma
   * Data della modifica
   * Aggiornato da
   * Scopo dell’aggiornamento
   * Esperienza prima del cambiamento (includi collegamenti/schermate)
   * Esperienza dopo la modifica (includi collegamenti/schermate)
   * URL del programma

### Fase 3: Identificare e documentare lo stato attuale dei programmi operativi principali

Inizia identificando i principali programmi operativi con un impatto a livello di abbonamento. Alcuni esempi includono Data Management [!DNL Campaign]s, ciclo di vita del lead, punteggio lead, [!DNL CRM] Sincronizzazione e recapito messaggi

Per ciascun programma operativo individuato, documentarne lo stato attuale. Ciò include dettagli sullo scopo del programma, sulla configurazione, sulle campagne intelligenti associate e sull’integrazione con altri strumenti (se applicabile).

### Passaggio 4: Applica [!DNL Changelog] Manutenzione

Il passaggio successivo consiste nel definire criteri di governance rigidi per [!DNL [!DNL Marketo Engage]] istanza che impone &quot;[!DNL Changelog] manutenzione.&quot; Questo criterio garantisce che tutti gli aggiornamenti apportati ai programmi operativi nell’istanza siano documentati in modo esauriente.

Informa il tuo team sull’importanza di questi documenti e su come accedervi e aggiornarli correttamente. Potrebbe essere utile assegnare responsabilità per la gestione del changelog, in modo che alcuni membri o amministratori del team dell’operazione di marketing designati registrino le modifiche in modo coerente e forniscano conclusioni.

### Passaggio 5: Centralizzazione della documentazione

Creare una posizione centrale o un repository per l&#39;archiviazione di tutta la documentazione relativa a [!DNL [!DNL Marketo Engage]]. Potrebbe trattarsi di un&#39;unità condivisa, di una cartella dedicata o di un sistema basato su cloud.

### Passaggio 6: rivedere e aggiornare regolarmente

Pianifica revisioni regolari della documentazione per assicurarti che rimanga accurata e aggiornata. Può essere facilmente sottovalutato durante i periodi di grande affluenza. Imposta proattivamente i promemoria sul calendario per garantire che il team esegua regolarmente aggiornamenti per riflettere eventuali modifiche o ottimizzazioni nei programmi operativi.

## Quali sono le prossime novità?

Per iniziare, scarica questo [modello semplice](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Segui i passaggi precedenti per sviluppare la guida alla governance e la documentazione. Durante il processo, tieni presenti queste regole generali:

**Aggiorna la documentazione esistente:**
È fondamentale mantenere aggiornata la documentazione. Se non è stata modificata negli ultimi 3 anni, conferma il tempo necessario per rivedere la documentazione durante l’audit dell’istanza.

**Condivisione e formazione:**
Condividi la documentazione e [!DNL changelog] con i membri pertinenti del gruppo e istruirli su come aggiornare questi record.

**Revisione periodica:** pianificare in anticipo i tempi di revisione e manutenzione nel corso dell’anno per includere eventuali nuove modifiche, ottimizzazioni o adeguamenti man mano che si verificano.

Documentazione completa e aggiornata per [!DNL Marketo Engage] consente di risparmiare tempo e fatica a lungo termine e di gestire le istanze in modo efficace.

### Autori

**Nick Hajdin**
[!DNL [!DNL Adobe] Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![Nick Hajdin](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Responsabile Marketing per l&#39;adozione e il mantenimento,[!DNL Adobe]*

![Amy Chiu](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
