---
title: Progettazione di marketing conversazionale omni-channel con Dynamic Chat
description: Inizia rapidamente a progettare il marketing conversazionale con Adobi Dynamic Chat, il canale di coinvolgimento conversazionale nativo in Adobe Marketo Engage. Questa esercitazione offre ricette utilizzabili per implementare casi d’uso quali prenotazione di riunioni di vendita, coinvolgimento con contenuti del sito web e promozione di eventi/webinar.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-23T00:00:00Z
jira: KT-14814
source-git-commit: 47ab8875bc4e41595cd40550330e43a88357b68d
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---


# Progettazione di marketing conversazionale omni-channel con Dynamic Chat

Per gli addetti al marketing, il tuo sito web è essenziale per generare lead, aumentare le conversioni e accelerare i cicli di vendita. Coinvolgere i visitatori in tempo reale sul tuo sito Web consente al team di vendita di qualificare gli acquirenti in modo più efficiente. Ad Adobe Dynamic Chat, il canale di chat nativo all’interno del tuo abbonamento a Adobe Marketo Engage, ti consente di automatizzare le conversazioni per estendere le funzionalità del Marketo Engage.

Questo tutorial illustra il processo di pensiero e i casi d’uso principali condivisi da Sara Barriuso, Marketing Operations Manager di Cornerstone OnDemand, durante il corso &quot;Scopri dai tuoi colleghi&quot;. Ha spiegato come la sua organizzazione utilizzava il Dynamic Chat per massimizzare le capacità del Marketo Engage.

## Integrazione del coinvolgimento conversazionale nella strategia di generazione della domanda

I visitatori navigano nel tuo sito web per un motivo. Potrebbero cercare contenuti sui tuoi prodotti o servizi o cercare informazioni di contatto per parlare con i tuoi rappresentanti commerciali. Potrebbero essere i tuoi clienti alla ricerca di informazioni di prodotto aggiuntive. La chat consente ai visitatori del sito web di self-service e autoqualificarsi se sono pronti a parlare con il team di vendita.

Quando Sara Barriuso ha implementato il Dynamic Chat, è stata attirata dalla sua integrazione perfetta con il Marketo Engage e il [attivatori attività predefiniti](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-activities){target="_blank"} che attivano programmi di Marketo Engage e viceversa. Ha sviluppato le sue strategie di coinvolgimento conversazionale pensando a tre segmenti di pubblico:

1. Potenziali sconosciuti: offri in modo proattivo chiamate demo per generare nuovi lead.
2. Clienti lead noti: prolunga il tempo dedicato dai visitatori alla navigazione dei contenuti e offri chiamate dimostrative per generare opportunità di upselling e cross-selling.
3. Potenziali clienti: fornisci esperienze personalizzate ampliando gli sforzi delle campagne di marketing.


## Casi d’uso chiave per iniziare a creare le finestre di dialogo

Per implementare queste strategie, Sara ha creato dei Dialoghi di Dynamic Chat sui seguenti casi d’uso:

1. Finestra di dialogo integrata predefinita: fornisci un’opzione iniziale a tutti i visitatori, guidandoli per svolgere le loro attività in modo più efficiente.

2. Promozione della registrazione di eventi e webinar: spingi i visitatori del sito a registrarsi per eventi e webinar per incanalarli più rapidamente nella fase di acquisto.

3. Estensione del coinvolgimento con i contenuti della campagna: offri contesto aggiuntivo o risolvi potenziali domande quando i visitatori navigano nel contenuto del sito web.

Vediamo questi casi d’uso in azione, mentre Sara mostra il suo processo, dalla mappatura del flusso conversazionale alla configurazione delle finestre di dialogo e del targeting in Dynamic Chat e Marketo Engage.

### Caso d’uso 1: finestra di dialogo predefinita onnicomprensiva per tutti i visitatori del sito

Questa finestra di dialogo fornisce cinque opzioni iniziali tra cui i visitatori del sito possono scegliere, creando un’esperienza autonoma che li aiuta a trovare le informazioni necessarie in base alla loro persona. Per iniziare, puoi esplorare la casella di posta &quot;Contattaci&quot; per identificare i temi comuni e suddividerli in categorie nelle opzioni di dialogo applicabili ai visitatori del tuo sito. Guarda la demo e segui i passaggi seguenti per creare la tua finestra di dialogo catch-all predefinita:

>[!VIDEO](https://video.tv.adobe.com/v/3429194/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### Fase 1

1. Crea la finestra di dialogo e un collegamento per i test.
2. Aggiungi un obiettivo per tenere traccia delle conversioni (ad esempio, invio di richieste demo).
3. Chiedi a 2-3 persone di testarlo e raccogliere feedback.

#### Fase 2

1. In &quot;Pubblico&quot;, aggiungi un URL di pagina web in &quot;Target&quot; per indicare dove verrà visualizzata la finestra di dialogo.
2. In &quot;Impostazioni&quot;, aggiungi il nome, la descrizione, la priorità e la lingua della campagna.
3. Fai clic su Pubblica

>[!TAB Marketo Engage]

#### Fase 1

1. Crea la tua campagna intelligente di tracciamento.
2. In &quot;Elenco avanzato&quot;, utilizza un trigger &quot;Obiettivo della finestra di dialogo Raggiungi&quot;. Usa lo stesso obiettivo (ad es. richiesta demo) che hai usato nella finestra di dialogo
3. In &quot;Flusso&quot;, includi un passaggio &quot;Modifica stato programma&quot; per tenere traccia della conversione.
4. L’origine verrà visualizzata come &quot;dynamicChat&quot;. Puoi creare una campagna avanzata per aggiornare l’origine con un nome appropriato.

#### Fase 2

1. Esegui nuovamente il test della campagna intelligente di tracciamento quando è live.

>[!ENDTABS]

#### Livello superiore: marketing basato su account

Puoi migliorare ulteriormente la finestra di dialogo predefinita onnicomprensiva incorporando contenuti mirati al settore, rendendo le conversazioni ancora più utili per i visitatori. Ad esempio, suggerisci white paper o case study specifici per il settore da scaricare per i visitatori. Guarda la demo e segui i passaggi seguenti per creare una finestra di dialogo predefinita onnicomprensiva per il marketing basato su account:

>[!VIDEO](https://video.tv.adobe.com/v/3429195/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Clona la &quot;finestra di dialogo predefinita&quot; e rinominala.
2. In &quot;Progettazione flussi&quot;, adattare i messaggi di dialogo al settore di destinazione (un solo flusso + la domanda iniziale).
3. Chiedi a 2-3 persone di testare la Finestra di dialogo e raccogliere feedback.
4. Crea un collegamento di test e condividilo.
5. In &quot;Pubblico&quot;, aggiungi un URL di pagina web in cui la finestra di dialogo visualizzerà e aggiornerà la destinazione al settore desiderato.
6. In &quot;Impostazioni&quot;, aggiungi il nome della campagna, la priorità della descrizione e la lingua.
7. Fai clic su &quot;Pubblica&quot;.

>[!TAB Marketo Engage]

1. Crea la tua campagna intelligente di tracciamento e verifica l’obiettivo.
2. Esegui nuovamente il test della campagna avanzata di tracciamento dopo la pubblicazione della finestra di dialogo.

>[!ENDTABS]

### Caso d’uso 2: promozione della registrazione di eventi e webinar

Eventi e webinar sono tattiche di marketing popolari per le aziende B2B per generare domanda. Offrono esperienze coinvolgenti e informazioni dettagliate che attraggono potenziali clienti. La connessione dei visitatori del sito web ai prossimi eventi e webinar consente di qualificare i potenziali clienti in modo ancora più rapido. La creazione di questa finestra di dialogo è un processo semplice e a basso costo e può dimostrare rapidamente il suo successo, aiutandoti a ottenere il supporto delle parti interessate del marketing per aggiungere un coinvolgimento conversazionale al tuo piano di automazione omnicanale. Guarda la demo e segui i passaggi indicati di seguito per creare la tua finestra di dialogo per la promozione di un evento/webinar:

>[!VIDEO](https://video.tv.adobe.com/v/3429196/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### Fase 1

Crea un modello per la finestra di dialogo &quot;Registrazione evento&quot; per l’utilizzo continuo della campagna.

#### Fase 2

1. Clona il modello.
2. Copiare e incollare testo nel messaggio di dialogo per un nuovo evento
3. Aggiorna i parametri UTM utilizzati nel collegamento dell’evento (ad esempio utm_medium=website&amp;utm_source=adobe).
4. Crea un collegamento di test, fai clic su &quot;Pubblica&quot; e condividilo con il richiedente.
5. Esamina tra pari e applica il feedback.


>[!TAB Marketo Engage]

#### Fase 1

1. Crea la tua campagna di tracciamento avanzata all’interno del modello di programma webinar/evento e testala.

#### Fase 2

1. Aggiungi il nome della campagna alla campagna Smart di tracciamento all’interno del Marketo Engage e testala.

>[!ENDTABS]


#### Livello superiore: registrazione di persone note

È possibile offrire un’esperienza ancora migliore ai visitatori del sito web registrandoli per i tuoi eventi e webinar senza dover compilare un modulo. Le esperienze personalizzate creano fiducia e mostrano ai visitatori che li ricordano. Vediamo come livellare il dialogo per la promozione di eventi e webinar in azione.

>[!NOTE]
>Considera il potenziale rischio per la sicurezza che alcuni stati/paesi proteggono comportano e implementa questa personalizzazione con attenzione consultando il tuo team legale.

>[!VIDEO](https://video.tv.adobe.com/v/3429197/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Clona la finestra di dialogo per la promozione di eventi/webinar.
2. In Stream Designer, dopo che l’utente ha risposto &quot;Sì&quot;, aggiungi una scheda di domande &quot;L’indirizzo e-mail è stato condiviso in precedenza con noi. Conservare per i dettagli dell&#39;evento?&quot;
3. Se rispondono &quot;Sì&quot; - aggiungi una scheda di messaggio &quot;Riceverai un’e-mail di conferma con i dettagli dell’evento/webinar&quot;.
4. Se rispondono &quot;No&quot; - aggiungi una scheda di messaggio &quot;Compila il modulo nella pagina di registrazione&quot;.
5. Crea un collegamento di test, fai clic su &quot;Pubblica&quot; e condividilo con il richiedente.
6. Nella scheda Pubblico, aggiungi [l’e-mail non è vuota].

>[!TAB Marketo Engage]

1. Aggiungi questa nuova finestra di dialogo alla campagna intelligente di tracciamento nel Marketo Engage e testala.

>[!ENDTABS]

### Caso d’uso 3: estensione del coinvolgimento con i contenuti della campagna

Immaginate che una finestra accattivante catturi il vostro sguardo e vi attragga in un negozio. Se un addetto alla reception ti aiuta a selezionare prodotti o a rispondere alle tue domande, potresti sentirti più a tuo agio nell’effettuare un acquisto. Per replicare questa esperienza online, puoi far apparire la finestra di dialogo del Dynamic Chat sulle pagine web in cui i visitatori vengono indirizzati dalle campagne di marketing. Man mano che gli utenti interagiscono con il contenuto web, il Dynamic Chat mostra immediatamente conversazioni rilevanti, suggerendo contenuti aggiuntivi o affrontando potenziali domande. Ciò si ottiene sfruttando i trigger di automazione per attivare campagne di Dynamic Chat in base al coinvolgimento degli utenti all’interno dei programmi di Marketo Engage. Ora, vediamo come dare vita a questo caso d’uso.

>[!VIDEO](https://video.tv.adobe.com/v/3429199/?learn=on)

Estensione del coinvolgimento con i contenuti di Campaign - Configurazione:

>[!VIDEO](https://video.tv.adobe.com/v/3429200/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Genera nuovi lead per le campagne tramite e-mail e punti di contatto per le campagne social. In questo esempio, il sondaggio Talent health index è ospitato sul sito web del brand.
2. Clona un modello di finestra di dialogo esistente (ad esempio, finestra di dialogo catch-all predefinita) per creare tre finestre di dialogo per i seguenti scenari e aggiorna di conseguenza &quot;URL target&quot; nella scheda &quot;Pubblico&quot;:
   * Quando i visitatori web provengono dai tuoi canali di marketing e arrivano sulla tua pagina web.
   * Nella pagina di ringraziamento
   * Qualsiasi visitatore che ritorna al tuo sito web entro 45 giorni dall’inizio della campagna di marketing (retargeting)

>[!ENDTABS]

## Quali sono le prossime novità?

* Mappare il flusso conversazionale in [Progettazione flussi](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/automated-chat/stream-designer){target="_blank"} o un diagramma di flusso offline.
* Crea una finestra di dialogo catch-all predefinita nel Dynamic Chat.
* Attiva il coinvolgimento post-campagna delle conversazioni utilizzando i trigger di automazione nel Marketo Engage.


## Autori

{{sara-barriuso}}

{{amy-chiu}}