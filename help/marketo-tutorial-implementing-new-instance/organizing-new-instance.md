---
title: Organizzazione di una nuova istanza e definizione di convenzioni di denominazione
description: Scopri come impostare una buona organizzazione all’interno dell’istanza di Marketo Engage, consentendo ai futuri esperti di marketing della tua organizzazione di spostarsi facilmente all’interno dei programmi, modificare le risorse e richiamare rapporti.
role: Admin
level: Beginner
doc-type: Article
duration: 0
last-substantial-update: 2024-05-03T00:00:00Z
jira: KT-14813
thumbnail: KT-14813.jpeg
source-git-commit: 849a0022ea3a64ad964c9d2fc368b4b79b9c0cfa
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 2%

---

# Organizzazione di una nuova istanza e definizione di convenzioni di denominazione

In qualità di amministratore che implementa una nuova istanza di Marketo Engage, stai gettando le basi per consentire ai futuri addetti al marketing all’interno dell’organizzazione di navigare facilmente attraverso l’istanza. Acquisire familiarità con la struttura ad albero delle cartelle e le convenzioni di denominazione manterrà l’istanza ordinata e configurata per il successo a lungo termine. Questo tutorial include esempi consigliati da Natalie Kremer, Adobe e campionessa di Marketo Engage (2019-2020), per aiutarti [organizzare le cartelle e denominare le risorse in modo coerente](https://nation.marketo.com/t5/champion-program-blogs/keep-marketo-engage-organized-with-folders-and-naming/ba-p/245630){target="_blank"}.

## Perché è necessario strutturare le cartelle e applicare le convenzioni di denominazione?

L’organizzazione continua a essere utile per consentire a te e ai tuoi colleghi di tenere traccia di campagne, programmi e risorse e di generare rapporti sulle prestazioni dei programmi. Per organizzare la struttura di navigazione nell’istanza e generarla su larga scala, si consiglia di utilizzare [cartelle](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/understanding-folders){target="_blank"}, [convenzioni di denominazione standard](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#naming-schemes){target="_blank"}, e funzioni quali [clonazione](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#cloning){target="_blank"}.

## Organizzare un’istanza di Marketo Engage

>[!VIDEO](https://video.tv.adobe.com/v/3421577/?quality=12&learn=on)

### Passaggio 1: configurazione di una struttura di cartelle per mettere in ordine i programmi

Il primo passaggio per organizzare l’istanza consiste nel [impostare una struttura di cartelle](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/create-new-campaign-folder.html) ospita il programma e le risorse in modo semplice e ordinato.

Di seguito sono riportati alcuni suggerimenti rapidi per strutturare le cartelle nella struttura:

* Mantenere una struttura di cartelle piatta per l&#39;individuazione.
* Strutturare le cartelle in modo da riflettere la struttura del team dell&#39;organizzazione (ad esempio Area geografica o Team) o le iniziative (ad esempio Newsletter).
* Includi etichette temporizzate per abilitare la ricercabilità e segnalare i tempi appropriati per l’archiviazione (ad esempio, 2024).
   * Si consiglia agli amministratori di archiviare le cartelle almeno una volta all’anno. Utilizzando il nome di una cartella annuale, puoi disattivare facilmente le campagne Smart live e archiviare l’intera cartella alla fine dell’anno.

Di seguito sono riportati alcuni esempi di cartelle che illustrano come mettere in pratica questi suggerimenti.

**Nome cartella nella struttura**

>[!BEGINTABS]

>[!TAB Attività di marketing]

![Cartelle attività di marketing](/help/marketo-tutorial-implementing-new-instance/assets/folders-marketing-activities.png)

>[!TAB Design Studio]

![Cartella Design Studio](/help/marketo-tutorial-implementing-new-instance/assets/folders-design-studio.png)

>[!TAB Database]

![Database cartelle](/help/marketo-tutorial-implementing-new-instance/assets/folders-database.png)

>[!ENDTABS]

### Passaggio 2: creazione di cartelle all’interno dei programmi

Ora applichiamo la struttura delle cartelle a livello di programma. Come best practice, l’archiviazione delle risorse locali in sottocartelle ti aiuterà a mantenere i programmi in ordine e a consentire agli utenti interni di modificare o creare rapporti sui programmi in modo efficiente. Le sottocartelle più comuni includono e-mail, pagine di destinazione, campagne avanzate, elenchi, rapporti e così via.

**Nome cartella nei programmi**
* Campagne - *Cartella per tutte le campagne che gestiscono le interazioni e il tracciamento dello stato.*
* Risorse locali - *Cartella per tutte le risorse specifiche di questo programma.*
   * E-mail
   * Pagine di destinazione
   * Campagne avanzate
   * Elenchi - *Necessario solo in presenza di elenchi specifici per il programma.*
   * FORMS - *Necessario solo in presenza di Forms specifici per il programma; la maggior parte dei Forms sono risorse globali.*
   * Rapporti - *Necessario solo in presenza di rapporti specifici per il programma.*

### Passaggio 3: creare convenzioni di denominazione per programmi e risorse

Una volta che disponi della struttura di cartelle in Struttura, vorrai denominare i programmi e le risorse in modo coerente. Ciò si verifica quando sarebbe utile standardizzare le convenzioni di denominazione per aumentare la scalabilità interna del processo di denominazione. Di seguito sono riportati alcuni componenti che è possibile utilizzare per stabilire convenzioni di denominazione per garantire la ricercabilità:

* Abbreviazione del tipo di programma: e-mail, contenuto, cultura, webinar, ecc.
* Categoria - Tipo di programma - E-mail autonoma, Newsletter, ecc.
* Date - Data di lancio del programma
* Breve descrizione: breve descrizione del programma

Ora, inseriamo i valori nella formula e generiamo i nomi dei programmi per vari tipi di programmi.

#### Formula di denominazione del programma

| **Abbreviazione del tipo di programma** | **AAAA** | **\-** | **MM** | **\-** | **DD(Facoltativo)** | **Categoria** | **\-** | **Breve descrizione del programma** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EM - Invio e-mail (programma e-mail) | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| NL - Newsletter | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| ENG - Programma di coinvolgimento | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| WBN - Webinar | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| IW - Webinar interattivo | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| TS - Fiere | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| LE - Evento live (Roadshow) | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| UG - Gruppo utenti | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| WC - Contenuto del sito web | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| CS - Syndication dei contenuti | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| LI - Importazione elenco | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| OA - Pubblicità online | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |
| PPC - Paga per clic | AAAA | \- | MM | \- | DD(Facoltativo) | Categoria | \- | Breve descrizione del programma |

| **Esempi** |
| --- |
| Contenuto gestito ES 2023-10 - White paper XYX |
| WC-2023-10- Webinar mensile - Caso di studio ABC |

#### Formula di denominazione risorsa

Andando da un livello all’altro per denominare le risorse, è meglio non ripetere il nome del programma e utilizzare identificatori brevi e generici per utilizzi futuri di duplicazione. Ecco alcuni suggerimenti da tenere a mente:

* Numera le risorse in base alla loro sequenza nel processo del programma.
* Utilizza &quot;-&quot; (trattino) per separare i componenti di denominazione invece di &quot;.&quot;(punto) o &quot;\_&quot;(trattino basso).
   * Perché? Il Marketo Engage utilizza un punto per separare il nome del programma dal nome della campagna. L&#39;uso di &quot;\_&quot; ti impedirà di visualizzarlo quando la risorsa è collegata tramite un collegamento ipertestuale.
* Utilizza gli acronimi standard nei nomi delle risorse per ridurre il riferimento e consentire comunque un facile riconoscimento.

Tenendo presenti questi suggerimenti, verranno applicati alle seguenti risorse e verranno create formule per generare i nomi:

##### Denomina le risorse in base alla sequenza nel processo del programma

| **Processo Sequenza nel programma** | **\-** | **Descrizione** |
| --- | --- | --- |
| 01 | \- | Descrizione |
| 02 | \- | Descrizione |
| 03 | \- | Descrizione |

| **Esempi: elenco avanzato** |
| --- |
| 01-Invia e-mail |
| 02 - Aperto |
| 03 clic |
| Modulo 04 compilato |
| Influenzato da 05 (successo del programma) |
| 06 - Annullamento iscrizione |

##### Denomina le risorse con l&#39;abbreviazione del tipo di risorsa

| **Abbreviazione del tipo di risorsa** | **Tipo risorsa** | **\-** | **Descrizione dell’obiettivo** |
| --- | --- | --- | --- |
| LP - Pagina di destinazione | LP | \- | Descrizione dell’obiettivo |
| E-MAIL - E-mail (in uscita) | EMAIL | \- | Descrizione dell’obiettivo |
| AVVISO - Avviso e-mail | AVVISO | \- | Descrizione dell’obiettivo |
| WF - Modulo web | WF | \- | Descrizione dell’obiettivo |
| EXCL - Elenco di esclusione | ESCL | \- | Descrizione dell’obiettivo |
| SLST - Elenco avanzato | SLST | \- | Descrizione dell’obiettivo |
| LST - Elenco statico | LST | \- | Descrizione dell’obiettivo |

| **Esempi** |
| --- |
| Registrazione LP |
| LP-Grazie |
| E-MAIL-in uscita |
| E-mail-Newsletter |
| Invito e-mail |
| EMAIL-Promemoria |
| ESCL-Concorrenti |

##### Denomina i file scaricabili (.pdf) con l’abbreviazione del tipo di risorsa

| **Tipo risorsa** | **Descrizione contenuto** | **\-** | **Abbreviazione del tipo di risorsa** | **.** | **PDF** |
| --- | --- | --- | --- | --- | --- |
| WP - White paper | Descrizione contenuto | \- | WP | . | pdf |
| CS - Caso di successo | Descrizione contenuto | \- | CS | . | pdf |
| DS - Data sheet | Descrizione contenuto | \- | DS | . | pdf |

| **Esempi: file PDF scaricabili** |
| --- |
| XYZ-Gadget-DS.pdf |
| Acme-Company-CS.pdf |
| How-XYZ-Gadgets-make-life-easier-WP.pdf |

>[!CAUTION]
>
>Per la denominazione dei file negli esempi precedenti, non utilizzare spazi ed evita l&#39;uso dei caratteri di sottolineatura &quot;\_&quot;

## Quali sono le prossime novità?

* Scarica il foglio di lavoro: [Convenzioni di Marketo Engage per l&#39;organizzazione e la denominazione](./assets/adobe-marketo-engage-organization-and-naming-conventions.xlsx){target="_blank"} per supportare la creazione della struttura di cartelle e le convenzioni di denominazione.
* Una volta determinati i componenti necessari nella convenzione di denominazione standard, è consigliabile creare formule in un Google Sheet o Microsoft Excel. Per un utilizzo futuro, è sufficiente inserire i valori nel foglio di calcolo per generare i nomi dei programmi.
* Dopo aver eseguito l’allineamento a una struttura di cartelle complessiva, è ora di pensare ai modelli necessari in base ai casi d’uso più frequenti e alle richieste più comuni ricevute dal team. Quindi inizia a creare il primo modello di programma. Continua a leggere per iniziare a utilizzare [Modelli di programma Adobe Marketo Engage](https://business.adobe.com/blog/how-to/get-started-with-marketo-engage-program-templates){target="_blank"}.

### Autori

{{natalie-kremer}}

{{amy-chiu}}