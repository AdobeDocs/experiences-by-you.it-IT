---
title: Differenze tra il Generatore di segmenti e i segmenti rapidi in Analysis Workspace
description: I segmenti possono essere uno degli strumenti più potenti nel tuo toolkit di analisi dei dati. Scopri le differenze tra l’utilizzo del generatore di segmenti e dei segmenti rapidi in Analysis Workspace per migliorare l’efficienza.
feature-set: Analytics
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
exl-id: baeaa90e-8cce-4ddd-b099-fecd266e410c
source-git-commit: 849ec510944d3299c3515fcecd5fc57d74c3fa26
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 0%

---

# Differenze tra il Generatore di segmenti e i segmenti rapidi in Analysis Workspace

I segmenti possono essere uno degli strumenti più potenti nel tuo toolkit di analisi dei dati. Scopri le differenze tra l’utilizzo del generatore di segmenti e dei segmenti rapidi in Analysis Workspace per migliorare l’efficienza.

>[!TIP]
>
> Fai clic sull’immagine nella parte inferiore della pagina per scaricare un promemoria utile su quando utilizzare ogni strumento in Analysis Workspace.

I segmenti possono essere uno degli strumenti più potenti nel tuo toolkit di analisi dei dati. Se desideri esaminare gruppi specifici di traffico, sezioni del sito o percorsi di clienti, l’utilizzo dei segmenti può rivelarsi utile per concentrare l’analisi su un particolare sottoinsieme di traffico verso il sito. Provenendo da un ambiente di vendita al dettaglio, alcuni dei segmenti più utili che ho creato sono per diversi tipi di gruppi di clienti, ad esempio clienti nuovi rispetto a clienti esistenti, clienti che hanno effettuato l’accesso a un account rispetto a ospiti e così via. Ma puoi anche crearli per diverse sezioni del sito, clienti che eseguono azioni specifiche o qualsiasi altra cosa a cui puoi pensare!

**Esistono due modi principali per creare i segmenti:**

* Utilizzo del Generatore di segmenti nel menu dei componenti
* Utilizzo dei segmenti rapidi nella parte superiore di un pannello

Se crei il segmento utilizzando il Generatore di segmenti, puoi salvarlo per riutilizzarlo in altri progetti. È un ottimo modo per concentrarsi su gruppi specifici di clienti, ad esempio, persone che visitano determinate sezioni del sito e poi effettuano un acquisto. Se invece esegui un’analisi esplorativa e desideri testare diverse impostazioni di segmento, il generatore di segmenti rapidi può essere di grande aiuto. Vediamo alcuni dei principali vantaggi di ciascun metodo.

## Segmenti rapidi

Nella parte superiore di ciascun pannello, puoi fare clic sull’icona del segmento rapido (un funnel con il simbolo +) per aprire il generatore. Questo consente di creare un segmento a qualsiasi livello (hit, visita o visitatore) con un massimo di tre condizioni. Simile al generatore di segmenti principale, questo dà un’indicazione sul lato destro che rileva se il segmento restituisce dati e % della popolazione di traffico complessiva inclusa nel segmento, anche se si tratta di una versione più semplificata della visualizzazione del volume di segmenti completo visualizzata nel generatore di segmenti. Quando aggiungi più di una condizione, puoi utilizzare gli operatori &quot;and&quot; e &quot;or&quot;. Sfortunatamente, non esiste l’opzione &quot;then&quot; (poi) per i segmenti rapidi, quindi se hai bisogno di segmenti sequenziali devi utilizzare il generatore di segmenti completo. In un segmento rapido è inoltre presente il limite di un contenitore. Questa funzione è pensata per l&#39;utilizzo in segmenti di base che possono essere creati ed editati rapidamente. Una volta applicato o salvato, un segmento rapido non può più essere modificato all’interno del pannello.

Quando esegui un’analisi esplorativa e desideri testare diversi tipi di segmenti per vedere come reagiscono i diversi gruppi di clienti o come funzionano le diverse categorie: l’utilizzo dei segmenti rapidi è molto più veloce rispetto all’utilizzo del generatore di segmenti. Inoltre, questi segmenti sono disponibili solo nel progetto in cui sono stati creati, quindi se non forniscono i risultati desiderati, non devi preoccuparti di eliminare il segmento salvato dall’elenco principale. Se, dopo aver eseguito il test dei segmenti, ti rendi conto che sarà utile in altri progetti, puoi sempre fare clic sul pulsante &quot;apri generatore&quot; per aprire il segmento nel generatore di segmenti completo e salvarlo come segmento regolare. Dopo questa operazione, tuttavia, non sarà più possibile modificarla nel generatore di segmenti rapidi.

![Segmento rapido](assets/quick-segement.png)

## Segment Builder

È possibile accedere al generatore di segmenti facendo clic sul simbolo + sopra l’elenco dei segmenti nel menu dei componenti a sinistra oppure facendo clic sul menu a discesa dei componenti e selezionando &quot;Crea segmento...&quot; A differenza dei segmenti rapidi, questo include tutte le opzioni disponibili. Per aggiungere più condizioni, puoi creare segmenti sequenziali utilizzando l’operatore &quot;then&quot;. I segmenti sequenziali ti consentono inoltre di utilizzare il &quot;gruppo logico&quot; come livello (anziché hit, visita o visitatore). Il generatore di segmenti consente inoltre di aggiungere una descrizione ai segmenti, che può aggiungere contesto su chi ha creato il segmento o sul tipo di dati che è stato creato per filtrare, o anche semplicemente aggiungere &quot;tag&quot; al segmento per scopi organizzativi, entrambi non possibili nel generatore di segmenti rapidi.

L’utilizzo del generatore di segmenti è essenziale quando il segmento avrà più di 3 condizioni, se devi utilizzare dei contenitori o desideri segmenti sequenziali. Il generatore di segmenti completo dispone di molte più opzioni per creare segmenti più complessi, che possono aiutarti a suddividere diversi tipi di clienti, categorie, percorsi di clienti e così via. Una volta creati e salvati, questi segmenti vengono aggiunti all’elenco principale dei segmenti, il che significa che possono essere taggati, approvati, condivisi, utilizzati in più rapporti e pubblicati nell’Experience Cloud. La pubblicazione nell&#39;Experience Cloud consente di utilizzare il segmento in altri prodotti [!DNL Adobe], ad esempio in [!DNL Adobe] Target per il targeting di personalizzazione. I segmenti generati nel generatore di segmenti non possono essere modificati nel pannello segmenti rapidi, dovrai aprire il generatore di segmenti per apportarvi modifiche. Fortunatamente, la visualizzazione di anteprima a destra fornisce un’analisi più dettagliata del traffico che il segmento genererebbe negli ultimi 90 giorni, il che significa che è più facile essere sicuri che il segmento stia introducendo ciò che desideri prima di salvarlo.

![Generatore di segmenti](assets/segment-builder-quick.png)

## Casi d’uso

In diversi settori, gli utilizzi per la creazione di segmenti personalizzati potrebbero essere diversi. Lavorando per la divisione e-commerce di un grande rivenditore, spesso eseguiamo analisi esplorative per determinare quali percorsi i clienti stanno prendendo per acquistare. Quando notiamo picchi o cali in azioni quali l’aggiunta di prodotti ai carrelli o l’effettuazione di ordini, è qui che l’utilizzo dei segmenti rapidi può risultare utile. Durante un’analisi posso creare rapidamente un segmento per un tipo specifico di cliente o per una particolare azione/collegamento su cui fanno clic. Non dovendo aprire il Generatore di segmenti e salvare ogni segmento, posso aggiungere rapidamente le condizioni, e poi rimuoverle altrettanto rapidamente. Questo consente di risparmiare molto tempo quando si cerca di spiegare perché vediamo un cambiamento sul sito.

In alternativa, in alcuni casi il generatore di segmenti è stato il mio punto di riferimento. Non tutti i clienti sono uguali, e spesso vogliamo esaminare tipi specifici di clienti identificati dalle azioni o dai percorsi seguiti. Utilizzando il Generatore di segmenti, possiamo aggiungere più condizioni per identificare i diversi tipi di clienti e salvare i segmenti in modo che possano essere condivisi e utilizzati da più analisti. È importante che questi tipi di segmenti siano coerenti tra i diversi rapporti, pertanto è meglio crearne uno che tutti possano utilizzare rispetto a ogni persona che crea la propria versione, in quanto i risultati possono differire.

Nel complesso, sia i segmenti rapidi che il generatore di segmenti sono strumenti eccellenti da utilizzare nell’analisi. Ognuno di loro ha i propri scopi, benefici e svantaggi. Per una guida di riferimento rapido, consulta la nostra guida pratica sui suggerimenti e trucchi scaricabili qui sotto.

## Autore

Questo documento è stato scritto da:

![Mandy George](assets/mandy-george-2.png)

**Mandy George**, Digital Analyst III presso Best Buy Canada

Adobe Analytics Champion

## Scarica

[![Download rapido segmenti](assets/quick-segments-download-small.jpg)](assets/[!DNL Adobe]_[!DNL Analytics]_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
