---
title: Documentazione del prodotto
description: Scopri come configurare e utilizzare le funzioni chiave di Brand Concierge.
role: User,Admin
level: Beginner
TQID: https://experienceleague.adobe.com/Ob3NAKyD929Ije-Y7UPO1hMfDYDi-UJ0gINpGlxiYGM
product_v2: id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: df401a2a-327d-468c-a5e4-b7b7ccd071a0id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 60835c7971d86341194d773f9cf487c4cb6f171a
workflow-type: tm+mt
source-wordcount: 2047
ht-degree: 1%

---

# Aiuto di Brand Concierge

Scopri come configurare e utilizzare le funzioni chiave di Brand Concierge. Trova le risposte alle domande comuni su configurazione, integrazione dei dati, privacy, personalizzazione, misurazione delle prestazioni e requisiti tecnici.

## Funzioni chiave {#key-features}

Brand Concierge offre una serie di funzionalità chiave, tra cui:

* **Onboarding guidato:** Segui una configurazione dettagliata per conoscere, le abilità e le espressioni del brand.
* **Integrazione della conoscenza:** Carica e gestisci origini come file CSV con collegamenti a siti Web.
* **Configurare le abilità** Integrare le abilità come Product Advisory.
* **Marchio di controllo:** regola la voce, il tono e la lunghezza di risposta per soddisfare gli standard e l&#39;approccio del tuo marchio.
* **Anteprima e iterazione:** Utilizza un&#39;interfaccia di anteprima completa per simulare conversazioni e eseguire regolazioni in tempo reale.
* **Sistema di feedback:** utilizza un sistema di feedback che consente agli utenti di fornire valutazioni positive o negative, insieme a moduli di feedback dettagliati che coprono la copertura della risposta, il tono, la qualità e le funzionalità.
* **Dashboard di Analytics:** sfrutta una dashboard di analisi basata su Customer Journey Analytics per metriche quali conversazioni, sentiment e coinvolgimento.

## Introduzione {#getting-started}

Puoi accedere a Brand Concierge dalla dashboard di Adobe Experience Cloud. Ad alto livello, è possibile eseguire le seguenti attività:

1. [Crea un portinaio](#homepage) da un URL del sito Web. Vengono generate automaticamente un’origine della conoscenza iniziale, un’espressione del brand e un’abilità di base.
1. [Rivedi e perfeziona le origini di conoscenza](#knowledge-sources) in base alle esigenze.
1. [Configura ulteriori abilità](#skills-configuration) oltre l&#39;abilità prevista.
1. [Regola la tua Espressione marchio](#brand-expression) se i valori predefiniti generati richiedono modifiche.

Per un&#39;esercitazione video, consulta [Creare il primo portinaio](../getting-started/create-first-concierge.md)

Le sezioni seguenti descrivono in dettaglio ogni attività e le opzioni di interfaccia.

## Creare un portinaio {#homepage}

La creazione di un portinaio da un singolo URL del sito web è il punto di partenza consigliato per un utente alle prime armi. La home page di Brand Concierge legge il sito e crea automaticamente una linea di base di lavoro: per iniziare non è necessaria alcuna configurazione manuale.

Al termine dell’installazione, un riepilogo della configurazione fornisce una visualizzazione completa dei dettagli, organizzata con schede per facilitare le regolazioni e i perfezionamenti continui. La homepage include anche una sezione di ispirazione con video e dimostrazioni delle funzionalità di consulenza, come consigli di prodotto, e accesso rapido alla documentazione di Experience League per approfondimenti tecnici.

**Elementi chiave**

* **Creazione con un solo clic**: immetti l&#39;URL di un sito Web per generare automaticamente un&#39;espressione del brand iniziale, un profilo del brand, istruzioni, guardrail, knowledge source e competenze di base.
* **Revisione guidata**: ogni elemento generato viene presentato per la revisione prima di essere salvato, quindi nulla viene reso disponibile senza la possibilità di modificarlo prima.
* **Sezione ispiratrice**: video e demo che mostrano le funzionalità di consulenza (ad esempio, consigli sui prodotti).
* **Collegamenti alla documentazione**: accesso rapido alle risorse Experience League per approfondimenti tecnici.
* **Riepilogo configurazione**: visualizzazione di tutti i dettagli dopo l&#39;installazione, con schede da perfezionare.

**Per creare un portinaio**

1. Immetti l&#39;URL del sito Web del brand e seleziona **[!UICONTROL Crea]**.
1. Rivedi l’espressione del brand generata (come formalità, calore, giocosità ed energia) e regolala in base alle esigenze.
1. Esamina il profilo del brand generato, compresi obiettivi, prodotti e servizi, pubblico target e differenziatori, e apporta le modifiche necessarie.
1. Esamina le istruzioni, i guardrail e i suggerimenti generati e apporta le modifiche necessarie.
1. Seleziona **[!UICONTROL Salva]**. Il portinaio è pronto per il test in anteprima.

Per informazioni complete su questo flusso, incluso ciò che viene configurato automaticamente, vedi [Gestire un portinaio](./concierge-management/concierge-management.md).

>[!TIP]
>
>Brand Concierge salva automaticamente l&#39;avanzamento. Una configurazione incompleta potrebbe limitare la funzionalità, ma non blocca i tentativi di anteprima.

### Sorgenti della conoscenza {#knowledge-sources}

[!UICONTROL Sorgenti di conoscenza] consente di gestire le origini dati che alimentano le risposte del portinaio. Un&#39;origine delle conoscenze iniziale viene creata automaticamente quando si crea un portinaio da un URL di sito Web. Utilizzare quest&#39;area per esaminarla o aggiungerne altre. [!UICONTROL Origini della conoscenza] include diversi elementi chiave da considerare, ad esempio:

* **Elenco Source:** visualizza tutti gli elementi caricati, ad esempio i file CSV con collegamenti a siti Web, e ne indica lo stato come Elaborato o In sospeso.
* **Interfaccia di caricamento:** consente di trascinare o sfogliare file CSV contenenti URL, che verranno scansionati per estrarre informazioni.
* **Opzioni di connessione:** consente di collegare origini di conoscenza specifiche alle abilità rilevanti per un utilizzo più mirato.

**Per aggiungere un&#39;origine della conoscenza**

1. Dalla home page, fare clic su **[!UICONTROL Origini informazioni]**.

1. Assegnare un nome all&#39;origine della conoscenza.

1. Fai clic su **[!UICONTROL Aggiungi]** per caricare un file CSV.

   Assicurati che includa una colonna per gli URL del sito web.

1. Attendi alcuni istanti per l’elaborazione.

   Questo passaggio si risolve abbastanza rapidamente con l’aggiornamento dello stato in tempo reale.

1. Una volta aggiunto, torna alla homepage.

   A questo punto, la nuova sorgente dovrebbe essere aggiunta alla pagina iniziale.

   Utilizza la pagina Home per modificare o eliminare le tue origini di conoscenza in base alle esigenze. È inoltre possibile riconnettere un&#39;origine della conoscenza in caso di modifiche.

Per l&#39;insieme completo dei tipi di origine delle informazioni e dei passaggi per la risoluzione dei problemi, vedere [Creare e gestire le origini delle informazioni per Brand Concierge](./knowledge-sources/knowledge-sources.md).

### Configurare le abilità {#skills-configuration}

Le abilità determinano cosa può fare un concierge per i visitatori, ad esempio **Product Advisory** per i consigli sui prodotti o **Site Advisory** per le domande generali sul marchio. Seleziona **[!UICONTROL Sfoglia abilità]** per visualizzare il catalogo delle abilità disponibile e attivare le abilità di cui il tuo concierge ha bisogno.

* **Catalogo competenze:** Scegli tra le competenze disponibili, ad esempio Site Advisory, Product Advisory e le competenze che supportano la prenotazione di riunioni o la chat in tempo reale con un rappresentante commerciale.
* **Configurazione:** Per ogni abilità, impostarne il nome, la descrizione e gli intenti (frasi o argomenti dei trigger) che devono richiamarla.
* **Integrazioni:** Allega l&#39;integrazione necessaria per eseguire il processo di un&#39;abilità oppure seleziona **[!UICONTROL Usa consigliato]** per fare in modo che il Compositore ne selezioni automaticamente uno.
* **Anteprima:** verifica le modifiche immediatamente nell&#39;anteprima live.

**Per configurare le abilità**

1. Dal portinaio, seleziona **[!UICONTROL Esplora abilità]**.
1. Seleziona un’abilità da attivare (ad esempio, Product Advisory).
1. Imposta il nome, la descrizione e gli intenti dell’abilità.
1. Allega l&#39;integrazione richiesta oppure seleziona **[!UICONTROL Usa consigliato]**.
1. Seleziona **[!UICONTROL Salva]** e verifica la modifica nell&#39;anteprima live.

Per il catalogo completo delle competenze e delle integrazioni, consulta [Framework delle competenze e delle integrazioni](./skills-and-integrations.md).

### Espressione del brand {#brand-expression}

L’espressione del brand controlla la personalità e lo stile delle risposte del concierge. Viene creata automaticamente quando si crea un portinaio e successivamente è possibile accedervi dalle impostazioni Tone &amp; Voice del portinaio per le modifiche in corso.

L’espressione del brand è impostata utilizzando attributi come formalità, calore, giocosità ed energia, anziché un singolo stile denominato. Puoi anche configurare la lunghezza della risposta (breve, media o lunga) in base alle preferenze del tuo marchio.

**Personalizzare l&#39;espressione del brand**

1. Dal portinaio, apri **[!UICONTROL Tono e voce]**.
2. Regola formalità, calore, giocosità, energia e lunghezza di risposta preferita.
3. Seleziona **[!UICONTROL Salva]** per assicurarti che le modifiche vengano applicate anche alle risposte future.

### Anteprima e test {#preview-and-test}

Verifica il concierge prima di avviarlo per i clienti che utilizzano le modalità Anteprima e Visualizzazione tester.

>[!BEGINTABS]

>[!TAB Modalità anteprima]

Utilizza la modalità Anteprima per simulare conversazioni mentre effettui regolazioni in tempo reale.

1. Dopo l&#39;installazione, tornare alla home page e fare clic su **[!UICONTROL Anteprima]**.
1. Utilizza l&#39;interfaccia di chat per inserire la query (ad esempio, _Consiglia un laptop con un costo inferiore a $1000_).
1. Rivedi le risposte del concierge.
1. Utilizza il pannello di destra per regolare le impostazioni delle espressioni del brand.
1. Fai clic su **[!UICONTROL Condividi]** per generare il collegamento per il feedback del team.

>[!TAB Visualizzazione tester]

Utilizza la vista Tester per raccogliere feedback strutturati sulle prestazioni del concierge e simulare l’esperienza dell’utente finale.

1. Dall&#39;anteprima, fare clic su **[!UICONTROL Visualizzazione tester]**.
1. Utilizza la visualizzazione Tester per simulare le conversazioni dell’utente finale.
1. Utilizza il meccanismo pollici su e giù per valutare ogni risposta ricevuta.
1. Completa il modulo di feedback per i pollici giù:
   **Copertura risposta:** È stato risolto l&#39;intento?
   **Tono marchio:** allineato con personalità?
   **Qualità risposta:** Cancellare e strutturare?
   **Funzionalità di risposta:** follow-up utili?
1. Aggiungere commenti e osservazioni specifiche.
1. Invia feedback per la revisione del dashboard.

>[!ENDTABS]

### Feedback {#feedback}

Dopo il test, puoi utilizzare la scheda Feedback nella homepage per fornire feedback e recensioni dettagliate.

La sezione feedback offre diverse funzioni importanti per aiutarti a monitorare e valutare le prestazioni del Brand Concierge. Sono disponibili i seguenti elementi:

* **Istantanea prestazioni:** visualizza le schede che riepilogano le metriche chiave, incluse le conversazioni totali, gli utenti univoci, le tendenze dei sentiment e il tasso di coinvolgimento.
* **Pulsante Visualizza report:** consente di aprire un dashboard basato su Customer Journey Analytics per un accesso approfondito alle analisi avanzate e alle metriche delle prestazioni.
* **Elenco feedback:** Visualizza una tabella delle sessioni di feedback. Puoi fare clic su singole righe per visualizzare la trascrizione completa della chat per ogni sessione.
* **Pannello feedback:** mostra le schede di valutazione sul lato destro dell&#39;interfaccia. Passa il mouse su queste schede o fai clic su di esse per evidenziare le parti pertinenti della trascrizione della chat per un facile riferimento.

**Per inviare feedback**

1. Passa alla home page di Brand Concierge e seleziona **[!UICONTROL Feedback]**.
1. Utilizza l’istantanea fornita per visualizzare informazioni sulle tendenze di alto livello.
1. Per accedere a un&#39;analisi approfondita fornita da Customer Journey Analytics, selezionare **[!UICONTROL Visualizza report]**.
1. È inoltre possibile esaminare il pannello per ulteriori commenti e suggerimenti.
1. Al termine, puoi esportare le informazioni da utilizzare in un secondo momento e perfezionare il flusso di lavoro.

### Configurazioni {#configurations}

La scheda _[!UICONTROL Configurazioni]_ è una visualizzazione di riepilogo di sola lettura che è possibile utilizzare per rivedere l&#39;installazione completa del portinaio. Questo rispecchia direttamente la Home page dopo il completamento della configurazione iniziale e fornisce un riepilogo dei tuoi dettagli, origini di conoscenza, competenze e Brand Expression configurato. È possibile utilizzare questa funzione come riferimento prima di visualizzare in anteprima o condividere il portinaio.

## Operazioni possibili con Brand Concierge

Scopri le funzioni del cliente, le funzionalità aziendali e i casi d’uso per Brand Concierge.

### Caratteristiche del cliente

Brand Concierge offre un’interfaccia di conversazione che consente ai clienti di trovare prodotti, confrontare opzioni e ottenere risposte utilizzando un linguaggio naturale. Con consigli personalizzati, confronti di prodotti avanzati e la possibilità di passare a un live agent, i clienti possono vivere un’esperienza fluida e intuitiva. L’interazione è flessibile: i clienti possono utilizzare testo, voce o immagini e ogni risposta si basa sulla documentazione affidabile del tuo marchio e sul contesto del cliente.

* Fai domande in linguaggio naturale e ottieni consigli personalizzati.
* Confronta i prodotti con gli schermi.
* Ottieni risposte dalla documentazione del tuo marchio.
* Passa a un agente attivo con cronologia completa delle conversazioni.

### Funzionalità aziendali

Brand Concierge offre alle aziende funzionalità avanzate di intelligenza artificiale per la conversazione per coinvolgere i clienti. Aiuta i brand a promuovere la conversione guidando i clienti verso i prodotti giusti, riducendo i costi di supporto attraverso risposte immediate e accurate e garantendo coerenza nella voce del marchio e conformità. Con analisi affidabili, handoff tra IA e utenti e integrazioni Adobe approfondite, Brand Concierge ottimizza sia l’esperienza del cliente che le prestazioni aziendali.

* Guida i clienti ai prodotti giusti per aumentare la conversione.
* Riduzione dei costi di supporto con risposte immediate e precise.
* Controlla i requisiti di voce, tono e conformità del brand.
* Tieni traccia delle prestazioni con la dashboard di Customer Journey Analytics.
* Trasferimento senza soluzione di continuità dall&#39;intelligenza artificiale all&#39;uomo, inclusa la pianificazione delle riunioni.
* Integrare con Adobe Experience Platform e Experience Manager.

## Casi d’uso

Brand Concierge supporta casi di utilizzo B2C e B2B in diversi settori.

| Settore | Casi d’uso |
|---|---|
| Retail ed e-commerce | I clienti possono scoprire i prodotti e ricevere consigli personalizzati. Brand Concierge fornisce indicazioni sul dimensionamento e sulla forma, aiuta gli utenti a trovare regali adatti e abbina stili o preferenze in base all’input del cliente. |
| Vendite B2B | Brand Concierge guida i clienti attraverso valutazioni dei prodotti, offre confronti dettagliati per caratteristiche e prezzi, assiste nella pianificazione di riunioni di vendita e fornisce consigli specifici per il settore, personalizzati per i clienti aziendali. |
| Assistenza clienti | Gli utenti possono ricevere risposte immediate direttamente dalla knowledge base. Brand Concierge fornisce informazioni su criteri e procedure, aiuta a risolvere problemi e fornisce aggiornamenti sullo stato e sul tracciamento degli ordini. |
| Viaggi e ospitalità | I clienti ricevono consigli di destinazione personalizzati, assistenza nella pianificazione degli itinerari, supporto durante l’intero processo di prenotazione e risposte alle domande sulla politica dei viaggi. |
| Servizi finanziari | Brand Concierge offre confronti tra prodotti per aiutare i clienti a scegliere le soluzioni finanziarie più adatte, fornisce informazioni sui clienti, fornisce indicazioni sulla conformità e consente la pianificazione delle riunioni con i consulenti finanziari. |

## Divulgazione di IA per conversazioni {#disclosure}

Per fornire un’esperienza trasparente e affidabile, gli utenti di Adobe Brand Concierge sono responsabili dell’aggiunta di una breve divulgazione all’interno della loro esperienza di conversazione. Questa divulgazione aiuta gli utenti finali a capire come funziona la conversazione e come possono essere utilizzate le loro informazioni.

**Informazioni sulla divulgazione**

La tua divulgazione durante la conversazione deve comunicare chiaramente tre cose agli utenti finali.

1. _La conversazione utilizza IA generativa_

   Informa gli utenti che le risposte sono generate dall’intelligenza artificiale, in modo che possano capire che interagiscono con un sistema automatizzato.

1. _Le conversazioni possono essere riviste per migliorare l&#39;esperienza_

   Gli utenti devono essere informati del fatto che le conversazioni sono accessibili a te (il cliente) e ai tuoi provider di servizi per aiutarti a personalizzare le risposte e migliorare la qualità e le prestazioni della conversazione.

1. _Utilizzare l&#39;intelligenza artificiale conversazionale significa accettare questo utilizzo_

Specifica chiaramente che continuando a utilizzare l’intelligenza artificiale conversazionale, gli utenti accettano questa elaborazione dei loro dati di conversazione.

**Esempio (solo a scopo di riferimento)**

`"This conversational AI uses generative AI to help respond to you. Conversations may be recorded by [customer] and/or our service provider and used to help operate and improve services, make your interactions with us better, and provide a more personalized experience. By continuing to conversational AI you agree to this processing of data."`

Puoi adattare il testo alla voce del tuo marchio e all&#39;esperienza dell&#39;utente, purché i punti chiave di cui sopra vengano comunicati chiaramente.

**Perché È Importante**

Essere all’avanguardia sul funzionamento dell’intelligenza artificiale conversazionale consente di impostare le giuste aspettative per gli utenti e crea fiducia nelle esperienze basate sull’intelligenza artificiale.
