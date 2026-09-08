---
description: Note sulla versione corrente di Adobe Brand Concierge.
title: Note sulla versione corrente
feature: Release Information
source-git-commit: 35ce8a7b460e97336246293ad5e53ee83ead5108
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Informazioni sulla versione corrente {#current-release-notes}

Adobe Brand Concierge segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzionalità, miglioramenti e correzioni su base continuativa.

Tutte le funzioni sono generalmente disponibili, se non diversamente indicato.

## agosto 2026 {#august-2026}

* **Compositore 2.0**: la creazione del portiere viene riprogettata intorno a un singolo URL del sito Web. Il Compositore redige automaticamente un punto di partenza allineato al brand, che include l’espressione del brand, il profilo del brand, le istruzioni, i guardrail, una fonte di conoscenza e un’abilità linea di base, pronti per essere rivisti e pubblicati in pochi minuti senza che sia necessaria alcuna configurazione manuale per iniziare.

* **Framework competenze e integrazioni**: le conferenze sono create da un catalogo self-service di competenze e integrazioni, individuabili e configurabili tramite Sfoglia abilità e Sfoglia integrazioni. Ciò include funzionalità nuove e rilasciate in precedenza, come Site Advisory, Product Advisory e funzioni di individuazione e confronto dei cataloghi Commerce.

* **Personalizzazione del componente Stile visivo e chat**: personalizza i colori, i font, il messaggio di benvenuto e i singoli componenti di chat di un portiere, inclusi bolle di chat, suggerimenti di prompt, citazioni, controlli di feedback e schede prodotto, con le modifiche visualizzate in anteprima dal vivo.

* **Più concierge per sandbox**: crea e gestisci più concierge all&#39;interno di una singola sandbox, ciascuna con configurazione indipendente.

* **Eventi lato client e funzioni di callback**: registra un singolo callback per osservare in tempo reale gli eventi del ciclo di vita del client Web, le interazioni utente, le risposte, il feedback e gli errori, da utilizzare per l&#39;invio di dati di coinvolgimento a Adobe Analytics, Google Analytics o altri sistemi di terze parti.

* **Supporto per portineria multilingue (disponibilità limitata)**: distribuire un portinaio in altre lingue insieme all&#39;inglese, con supporto convalidato per spagnolo e francese. Ogni lingua di destinazione viene eseguita come proprio concierge all’interno della stessa sandbox e viene automaticamente instradata dalla lingua della richiesta.

* **Distribuzione: Datastream e configurazione della superficie**: configura un datastream per tenere traccia del coinvolgimento dei visitatori, quindi definisci le regole della superficie per controllare su quali pagine e domini viene visualizzato il portiere, utilizzando la corrispondenza del dominio e del percorso (qualsiasi, inizia con, termina con o esatta corrispondenza).

## Giugno 2026 {#june-2026}

* **Integrazione di Marketo**: le conversazioni dei visitatori, inclusa l&#39;acquisizione di lead in-chat, vengono trasmesse automaticamente in Marketo Engage come dati di attività nativi, disponibili per l&#39;utilizzo in campagne Smart sia in batch che attivate.

## Aprile 2026 {#april-2026}

* **Integrazione di Brand Concierge con Real-Time CDP (disponibilità limitata)**: migliorare la qualità e la rilevanza delle risposte conversazionali incorporando il contesto di Real-Time CDP, ad esempio gli attributi utente, i segnali comportamentali e le interazioni precedenti, per allineare meglio le risposte alle finalità dell&#39;utente.

* **Miglioramento ottimizzazione self-service**: Brand Concierge Composer valuta automaticamente le prestazioni della conversazione e aggiorna le configurazioni dei prompt per migliorare la qualità della risposta. Queste ottimizzazioni vengono applicate continuamente in base ai risultati della valutazione automatizzata, riducendo la necessità di tuning manuale.

* **Consigli sul prodotto in base al contesto**: Brand Concierge fornisce consigli di prodotto basati su intenti utente dedotti, sfruttando i dati strutturati del catalogo dei prodotti e la possibilità di integrarli con sistemi di record di ricerca e consigli dei prodotti per migliorarne la pertinenza e l&#39;accuratezza. Le schede prodotto vengono presentate quando appropriato, supportando i consigli per più prodotti e l’allineamento con l’individuazione o le finalità di acquisto.

* **Confronto affiancato**: consente il confronto affiancato di più prodotti all&#39;interno della conversazione tramite una visualizzazione tabella strutturata, evidenziando attributi chiave, funzionalità e differenze. Il confronto viene generato in modo dinamico in base alle intenzioni degli utenti e a prodotti selezionati, favorendo una valutazione e un processo decisionale più informati.

* **Agente di supporto (guida alla risoluzione dei problemi e procedure)**: abilita il supporto guidato nella conversazione aiutando gli utenti a risolvere i problemi e completare le attività pratiche tramite l&#39;assistenza in base al contesto. L’agente adatta le risposte in base all’input dell’utente per garantire una risoluzione efficiente dei problemi senza richiedere l’escalation.

## Marzo 2026 {#march-2026}

* **Configurazione AEM di Site Advisor nel Compositore**: la configurazione AEM di Site Advisor nel Compositore consente ai clienti AEM di impostare facilmente l&#39;acquisizione delle origini di conoscenza direttamente nel Compositore, con il contenuto del sito Web AEM come origine di conoscenza principale. Questo riduce gli attriti associati all’onboarding e garantisce risposte precise, conformi e prevedibili basate sul contenuto AEM del cliente.

* **Acquisizione di siti completi**: l&#39;acquisizione di siti completi consente ai clienti di acquisire automaticamente l&#39;intero sito Web utilizzando una singola mappa del sito, eliminando la necessità di caricare manualmente gli URL. In questo modo è possibile garantire una copertura completa e aggiornata dei contenuti, con un onboarding scalabile e a basso carico di lavoro e una costante aggiornamento dei contenuti.

* **Creazione automatica dei prompt (disponibilità limitata)**: la creazione automatica dei prompt consente ai clienti di creare un&#39;esperienza Brand Concierge di alta qualità attraverso un flusso semplice e autonomo. Brand Concierge genera automaticamente i prompt di concierge da input utente minimi senza esporre o richiedere la progettazione dei prompt. Gli utenti non tecnici possono ottenere rapidamente un concierge funzionante e convalidato dalla qualità tramite la convalida guidata del profilo del brand e la configurazione basata sull’intelligenza artificiale.

* **BYOA - Agente Firefly in Adobe.com Brand Concierge**: la generazione di immagini Firefly è ora integrata in Adobe.com Brand Concierge, consentendo agli utenti di creare, scaricare e continuare a modificare immagini o moodboard in Firefly. Questo è il primo lancio dell’integrazione &quot;Bring Your Own Agent&quot;, che consente agli agenti dei clienti e di terze parti di operare in Brand Concierge tramite Agent Orchestrator.

## Febbraio 2026 {#february-2026}

* **Generazione automatizzata di set di dati di valutazione**: genera automaticamente set di dati di valutazione di alta qualità per valutazioni funzionali, fuori ambito e di salvaguardia. Il set di dati di valutazione si basa direttamente sulla knowledge base del brand, garantendo test affidabili e ad alta affidabilità.

* **Valutazione automatizzata e ciclo di qualità basato su LLM**: convalida le prestazioni di Concierge con un clic utilizzando il punteggio basato su LLM per tutte le dimensioni di qualità, inclusa la correttezza, l&#39;utilità e l&#39;aderenza al brand. In questo modo è possibile eseguire valutazioni della qualità obiettive e ripetibili, in modo da garantire ai clienti la massima affidabilità prima di ogni lancio.

* **Automazione per le attività di creazione e avvio del portinaio (interfaccia utente sviluppatore)**: si tratta di una funzione interna rivolta agli sviluppatori che consente ai team di avviare e avviare rapidamente un&#39;esperienza di portineria, con opzioni per gestire la configurazione della sandbox e del portinaio, la configurazione dell&#39;interfaccia utente/dello stile e l&#39;ottimizzazione dei prompt. Questo accelera il tempo di pubblicazione e consente ai team di creare istanze di Concierge personalizzate e di alta qualità su larga scala.

* **Miglioramento del Knowledge Source: caricamento/aggiornamento URL incrementale e supporto di tipi di file aggiuntivi**: la funzione di gestione URL incrementale consente ai clienti di aggiornare facilmente (aggiungere/eliminare/aggiornare) solo le pagine modificate, senza rielaborare l&#39;intera origine della Knowledge Base. In questo modo si riducono i tempi di aggiornamento e il sovraccarico operativo. Inoltre, Brand Concierge ora supporta il caricamento di file PDF/DOCX.

* **Supporto per schemi di prodotto personalizzati**: la funzionalità di supporto per schemi personalizzati consente ai clienti di caricare e gestire cataloghi di prodotti che seguono la propria struttura di dati anziché un formato fisso. Ciò consente la convalida corretta, la mappatura dei campi e la generazione accurata di schede prodotto tra marchi con modelli di catalogo diversi.

* **Mobile SDK**: Brand Concierge Mobile SDK (per le app per dispositivi mobili) consente ai brand di incorporare Brand Concierge direttamente nelle proprie app mobili, supportando le interazioni di testo, voce e immagine. Fornisce un’interfaccia pronta all’uso e un’integrazione back-end che consente ai consumatori di accedere facilmente a Brand Concierge all’interno dell’app del brand.
