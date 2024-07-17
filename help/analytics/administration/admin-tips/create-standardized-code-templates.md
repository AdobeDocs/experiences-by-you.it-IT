---
title: Creare modelli di codice standard
description: Per un'implementazione che funga da linea di base (con i KPI considerati indispensabili per tutti i  [!DNL Adobe Analytics]  siti), ove possibile la tua organizzazione deve seguire un unico metodo di implementazione.
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
ht-degree: 0%

---

# Creare modelli di codice standard

**COSA:** Per un&#39;implementazione che funga da &quot;linea di base&quot; (con i KPI considerati indispensabili per tutti i [!DNL Adobe Analytics] siti), ove possibile la tua organizzazione deve seguire un unico metodo di implementazione. Ad esempio, utilizza per tutti i siti la stessa struttura del livello dati, sfruttando lo stesso codice personalizzato o le stesse regole di gestione dei tag per acquisire elementi quali ricerche interne o informazioni sul profilo del visitatore.

**PERCHÉ:** una volta implementata una linea di base ripetibile e scalabile, risulterà più semplice aggiungere nuovi elementi o nuovi siti/app; inoltre l&#39;implementazione sarà più pulita e sarà più facile risolvere eventuali problemi. L’utilizzo di un metodo uniforme semplifica inoltre il lavoro degli amministratori/sviluppatori e la loro comprensione da parte dei nuovi utenti.

**COME:** adotta un modello in un singolo formato per gli sviluppatori quando è online un nuovo sito o un miglioramento dei tag. In genere, un documento Word funziona bene dove è possibile delineare i seguenti elementi:

* Le variabili da implementare, il loro scopo e quando impostarle. Ad esempio:

| Variabile AA | Descrizione | Quando/Dove impostare | Come impostare |
|--- |--- |--- |--- |
| EVAR 8 | Parole chiave di ricerca interna | All’arrivo nella pagina dei risultati di ricerca interna | livello dati |
| event8 | Numero di ricerche interne | All’arrivo nella pagina dei risultati di ricerca interna | Regola di avvio |

* Dettagli su come impostare. Qui puoi specificare tutti gli oggetti livello dati necessari e la loro sintassi, nonché eventuali regole TMS da configurare e i dettagli della configurazione della regola.
* Casi di test da trattare nel controllo qualità e tutte le variabili che si prevede di vedere in un caso di test di successo. Descrivi cosa deve essere incluso un’implementazione di successo quando lo sviluppatore esegue il test di questo miglioramento.

Questo documento dovrebbe essere modificato solo per il prossimo sito in cui verranno aggiornate le nozioni di base come nome della proprietà, convenzione di denominazione delle pagine e così via. Non è necessario reinventare la ruota ogni volta, e si può risparmiare più tempo.

## Autori

Questo documento è stato scritto congiuntamente da:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital [!DNL Analytics] Platform Manager di NortonLifeLock
[!DNL Adobe Analytics] campione

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Consulente senior alle [!DNL Adobe]
