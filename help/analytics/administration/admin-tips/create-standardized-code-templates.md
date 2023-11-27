---
title: Creare modelli di codice standardizzati
description: Per un’implementazione che funga da linea di base (con i KPI considerati indispensabili per tutti) [!DNL Adobe Analytics] Sites), ove possibile la tua organizzazione deve seguire un unico metodo di implementazione.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: edd3df73-6d1a-4a26-a984-810cc7dd382f
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 90%

---

# Creare modelli di codice standardizzati

**COSA:**[!DNL Adobe Analytics] per un’implementazione che funga da “linea di base” (con i KPI considerati indispensabili per tutti i siti ), ove possibile la tua organizzazione deve seguire un unico metodo di implementazione. Ad esempio, utilizza per tutti i siti la stessa struttura del livello dati su e sfrutta lo stesso codice personalizzato o le stesse regole di gestione dei tag per acquisire elementi quali ricerche interne o informazioni sui profili dei visitatori.

**PERCHÉ:** una volta implementata una linea di base ripetibile e scalabile, risulterà più semplice aggiungere nuovi elementi o nuovi siti/app; inoltre l’implementazione sarà più pulita e sarà più facile risolvere eventuali problemi. L’utilizzo di un metodo uniforme facilita anche il compito di nuovi amministratori o sviluppatori, che potranno capire meglio e più rapidamente su cosa devono lavorare.

**COME:** adotta un modello in un singolo formato per gli sviluppatori quando occorre pubblicare un nuovo sito o miglioramenti dei tag. In genere, un documento Word funziona bene per delineare i seguenti elementi:

* Le variabili da implementare, il loro scopo e quando impostarle. Ad esempio:

| Variabile AA | Descrizione | Quando/Dove impostarla | Come impostarla |
|--- |--- |--- |--- |
| eVar8 | Parole chiave per la ricerca interna | All’arrivo nella pagina dei risultati di ricerca interna | livello dati |
| event8 | Numero di ricerche interne | All’arrivo nella pagina dei risultati di ricerca interna | Regola di avvio |

* Dettagli per l’impostazione. Qui puoi specificare tutti gli oggetti livello dati necessari e la relativa sintassi, nonché eventuali regole TMS da configurare e i relativi dettagli di configurazione.
* I casi di test da trattare in fase di controllo qualità e tutte le variabili che si prevede di trovare in un caso di test di successo. Descrivi cosa deve essere incluso un’implementazione di successo quando lo sviluppatore esegue il test di questo miglioramento.

Questo documento dovrebbe essere modificato solo per il prossimo sito in cui vengano aggiornati elementi di base come nome della proprietà, convenzione di denominazione delle pagine e così via. Non è necessario rifare tutto da capo ogni volta, e si può risparmiare tempo.

## Autori

Questo documento è stato scritto da:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digitale [!DNL Analytics] Platform Manager di NortonLifeLock
[!DNL Adobe Analytics] Campione

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant presso [!DNL Adobe]
