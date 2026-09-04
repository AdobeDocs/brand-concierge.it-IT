---
title: Gestire un portinaio
description: Scopri come creare un Brand Concierge da un sito web, configurarne integrazioni, abilità, istruzioni, tono e stile visivo e testarlo prima della distribuzione.
toc: true
source-git-commit: 3f05cb0dd8c11620b0ed7e254d0f4f9b24408b08
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 1%

---


# Gestire un portinaio

Un portinaio viene creato da un sito Web di un marchio e può essere perfezionato con integrazioni, abilità, istruzioni, impostazioni di tono e voce, stili visivi e componenti di chat. Utilizza l’anteprima per verificare le modifiche prima di distribuire deliberatamente il portinaio ai visitatori.

## Panoramica

| Elemento | Dettagli |
|---|---|
| Utente principale | Addetto marketing che utilizza la configurazione self-service |
| Supporto aggiuntivo | Le integrazioni Commerce e B2B possono richiedere codici, chiavi o impostazioni da un team IT, commerciale o di vendita |
| Ora tipica | Circa 5 minuti per creare una portineria di base; è necessario un tempo continuo per il perfezionamento e il test |
| Distribuzione | Separato dalla creazione; la creazione di un portinaio non lo rende visibile ai visitatori del sito web |

>[!NOTE]
>
>Una sandbox può contenere più concierges. Ogni portinaio ha una propria configurazione e le portinerie possono essere cancellate dall&#39;elenco.

## Creare un portinaio

La creazione di un portinaio da un singolo URL del sito web è il punto di partenza consigliato per un utente alle prime armi. Il sistema crea una baseline di lavoro senza richiedere la configurazione manuale.

1. Immetti l&#39;URL del sito Web del brand e seleziona **Crea**.

1. Rivedi l’espressione del brand generata. Il sistema analizza il tono del sito web e propone attributi come formalità, calore, giocosità ed energia. Regolare i valori in base alle esigenze e selezionare **Continua**.

1. Rivedi il profilo del brand generato. Il profilo può includere l’obiettivo del brand, prodotti e servizi, pubblico target, valori del brand, differenziatori chiave e casi d’uso comuni. Modificare il profilo in base alle esigenze e selezionare **Continua**.

1. Rivedi le istruzioni iniziali, i guardrail e i suggerimenti generati. Ad esempio, i guardrail possono escludere argomenti legali, argomenti relativi alla conformità o discussioni con i concorrenti, mentre i suggerimenti possono fornire idee tempestive di follow-up. Modifica il contenuto in base alle esigenze e seleziona **Salva**.

1. Attendere che il sistema applichi la configurazione di base. Il sistema crea anche uno stile visivo predefinito utilizzando colori e font tratti dal sito web e attiva competenze e integrazioni di base, come un’abilità generale di domanda e risposta connessa al contenuto del sito web.

1. Verifica il portinaio nell’anteprima. Sono disponibili le visualizzazioni per desktop e dispositivi mobili. Seleziona **Nuovo** per riavviare una conversazione di prova.

>[!IMPORTANT]
>
>La creazione di un portinaio non lo rende visibile ai visitatori. La distribuzione è un passaggio separato e deliberato. Puoi rivedere la configurazione in qualsiasi momento prima della distribuzione.

## Informazioni sulla configurazione automatica

Gli elementi seguenti vengono configurati automaticamente durante la creazione di un portinaio:

| Elemento | Configurazione |
|---|---|
| Contenuto della Knowledge Base | Generato dalle pagine principali del sito tramite un scansiono in background che viene avviato automaticamente |
| Integrazione di Knowledge Base Search | Punta automaticamente al contenuto scansionato |
| Competenza consigliata per siti | Attivo per impostazione predefinita, in modo che il portinaio possa rispondere immediatamente alle domande generali |

## Comprendere competenze e integrazioni

Compositore, l’interfaccia utilizzata per generare e configurare un portiere, utilizza due concetti correlati:

- **Integrazione:** una connessione a un&#39;origine dati, ad esempio il contenuto di un sito Web o un catalogo di prodotti live. Un’integrazione recupera le informazioni ma non prende decisioni da sola.
- **Abilità:** Un comportamento che determina le azioni del portinaio, quando e quali integrazioni può utilizzare.

Un’integrazione può fornire più competenze e una competenza può utilizzare più integrazioni. Ad esempio, una singola connessione al catalogo prodotti può supportare diversi casi d’uso relativi ai prodotti senza essere ricreata per ogni abilità.

## Configurare le integrazioni

Seleziona **Sfoglia integrazioni** per visualizzare il catalogo delle integrazioni disponibile.

| Integrazione | Scopo | Note |
|---|---|---|
| Ricerca nella Knowledge Base | Cerca il contenuto del sito Web | Configurato automaticamente al momento della creazione del portinaio |
| Contenuto Ricerca IA | Cerca nel contenuto di AEM Sites | Rilevante per i clienti di AEM Sites as a Cloud Service |
| Collegamento entità | Risolve prodotti o menzioni dei brand nel messaggio di un visitatore in base a specifiche entità di catalogo | Integrazione di supporto, in genere utilizzata insieme a un’integrazione di ricerca anziché da sola |
| MCP COMMERCE | Si connette a un catalogo Adobe Commerce live per la ricerca di prodotti, i dettagli dei prodotti e i confronti | Non abilitato per impostazione predefinita; richiede codici o chiavi dal team commerciale o IT |
| Prenotazione riunione | Consente ai visitatori di prenotare una riunione con un rappresentante commerciale | Richiede l&#39;impostazione con il calendario di un rappresentante commerciale |
| Chat live | Collega i visitatori con un rappresentante commerciale live | Richiede l&#39;installazione con la disponibilità di un rappresentante commerciale |

### Attivare e configurare un’integrazione

1. Apri il riquadro di integrazione e seleziona **Modifica**.

1. Per **Ricerca nella Knowledge Base**, selezionare l&#39;origine della Knowledge Base da cercare. È possibile rinominare la connessione, ad esempio `Website content`.

1. Per **Commerce MCP**, immettere i valori seguenti forniti dal team Adobe Commerce o IT e connettersi:
   - ID ambiente
   - Codice del sito web
   - Codice store
   - Codice visualizzazione store
   - Chiave API

1. Seleziona **Salva**. L’integrazione viene visualizzata come connessa e può essere visualizzata in anteprima, modificata o rimossa.

È possibile aggiungere più istanze della stessa integrazione, ad esempio istanze che puntano a origini di conoscenza diverse. È possibile configurare un’abilità per utilizzare un’istanza di integrazione specifica.

## Configurare le abilità

Le abilità determinano cosa può fare un concierge per i visitatori. Seleziona **Sfoglia abilità** per visualizzare il catalogo delle abilità disponibile.

| Competenza | Scopo | Integrazione o configurazione richiesta |
|---|---|---|
| Consulenza sito | Risposte alle domande generali sul marchio, tra cui domande frequenti, criteri, prezzi, guide pratiche e argomenti di supporto | Contenuto del sito web; attivo per impostazione predefinita |
| Product Advisory | Aiuta i visitatori a scoprire e ricercare prodotti attraverso schede dei prodotti basate sul nome e domande sui prodotti | Ricerca nella knowledge base, collegamento entità |
| Individuazione catalogo Adobe Commerce | Cerca, sfoglia, filtra e recupera i dettagli dei prodotti da un catalogo live | Integrazione Commerce MCP |
| Confronto tra i prodotti Adobe Commerce | Fornisce un confronto affiancato di prodotti denominati | Integrazione Commerce MCP |
| Prenota riunione con il reparto vendite | Suggerisce e facilita la prenotazione di una riunione | Integrazione prenotazione riunioni |
| Chat in tempo reale con le vendite | Suggerisce e facilita un handoff di chat in diretta | Integrazione chat in diretta |

### Attivare e configurare un’abilità

1. Apri il riquadro abilità e seleziona **Modifica**.

1. Imposta il nome, la descrizione e gli intenti dell’abilità. Gli intenti sono frasi o argomenti che devono attivare l&#39;abilità, ad esempio `pricing` o `compare products`. È possibile aggiungere più intenti.

1. Se l’abilità richiede un’integrazione, allega l’integrazione richiesta. Ad esempio, un’abilità di e-commerce richiede Commerce MCP. In alternativa, selezionare **Usa consigliato** per consentire a Composer di selezionare automaticamente un&#39;integrazione appropriata.

1. Rivedi e modifica le istruzioni iniziali dell’abilità in base alle esigenze.

1. Seleziona **Salva** e verifica la modifica nell&#39;anteprima live.

>[!TIP]
>
>Se due abilità possono rispondere alla stessa domanda, l&#39;instradamento può diventare incoerente. Mantieni i trigger delle abilità distinti e specifici invece di utilizzare intenti sovrapposti.

## Aggiungi istruzioni per il portinaio

Utilizza il campo delle istruzioni di concierge per mantenere le risposte allineate con le linee guida del brand. Le istruzioni possono definire:

- Utilizzo del marchio
- Struttura di risposta
- Argomenti da evitare

Digitare le istruzioni direttamente nel campo di testo. Quando salvi le istruzioni, il portinaio aggiorna automaticamente il suo comportamento. Verifica il risultato immediatamente nell’anteprima live.

La stessa area include anche i seguenti contenuti modificabili:

- **Guardrail:** Comportamenti o argomenti che il portiere deve evitare.
- **Suggerimenti:** idee di richiesta di completamento che possono essere visualizzate dopo una risposta.

## Configura tono e voce

Le impostazioni tono e voce controllano la lunghezza della risposta e gli attributi del tono, tra cui:

- Formale o casuale
- Caldo o neutro
- Giocoso o serio

Le selezioni vengono salvate automaticamente. Dopo aver apportato le modifiche, verifica il risultato nell’anteprima live.

## Configurare lo stile visivo

Le impostazioni di stile visivo controllano l’aspetto del portinaio, tra cui:

- Colori
- Font
- Testo del messaggio di benvenuto
- Testo disclaimer legale
- Colori scheda

Modifica le impostazioni nell’interfaccia utente e utilizza l’anteprima live per rivedere le modifiche. Seleziona **Salva** per rendere le modifiche permanenti.

## Configurare i componenti chat

I componenti Chat controllano i singoli elementi visualizzati dai visitatori nella finestra chat. Seleziona un componente nell’interfaccia utente per aprirne le impostazioni in un pannello laterale.

| Componente | Cosa controlla |
|---|---|
| Bolla di chat | L’aspetto dei messaggi dei visitatori e dei messaggi concierge |
| Avvia pillole di prompt o prompt | Domande di apertura consigliate, in particolare quelle visualizzate sui dispositivi mobili |
| Suggerimenti di follow-up | Domande successive suggerite dopo una risposta |
| Barra di input | Finestra di messaggio utilizzata dai visitatori per immettere una domanda |
| Citazioni | Se e come i riferimenti di origine vengono visualizzati in una risposta |
| Feedback | Il controllo della valutazione thumbs-up o thumbs-down mostrato dopo ogni risposta |
| Scheda prodotto | Layout e stile delle schede dei prodotti, inclusi colori e pulsanti |

## Configurare la prenotazione di riunioni e la chat in tempo reale

Meeting Booking e Live Chat consentono ai visitatori di prenotare riunioni con i rappresentanti commerciali o di avviare una chat in tempo reale con un rappresentante. Queste funzionalità si basano su un prodotto correlato denominato Sales Qualifier.

### Ruoli e responsabilità

- **Addetto marketing:** configura l&#39;abilità e l&#39;integrazione in Brand Concierge.
- **Rappresentante commerciale:** collega il proprio calendario e configura la disponibilità.

### Configurare la prenotazione di riunioni o la chat in diretta

1. In **Sfoglia integrazioni**, apri **Prenotazione riunione** o **Chat live**. Per impostazione predefinita, tutti gli utenti dell’organizzazione sono disponibili come potenziali membri del team; in questa fase non è necessario alcun passaggio separato per aggiungere membri del team.

1. Chiedi a ogni rappresentante commerciale di accedere a `experienceplatform.adobe.com`, aprire **Sales Qualifier** e passare a **Impostazioni profilo**.

1. Chiedere a ogni rappresentante di connettere un calendario, ad esempio Outlook. Facoltativamente, è possibile includere Microsoft Teams. Il rappresentante può anche impostare l&#39;oggetto dell&#39;invito alla riunione e il testo dell&#39;e-mail.

1. Configurare la disponibilità. La disponibilità viene estratta dal calendario per impostazione predefinita e può essere ulteriormente limitata da:
   - Durata riunione
   - Tempo buffer tra le riunioni
   - Avviso minimo richiesto
   - Intervalli di tempo specifici disponibili

1. Configura la disponibilità di Live Chat separatamente, utilizzando un processo simile.

1. In Brand Concierge, aprire **Membri gestiti** e verificare che i rappresentanti siano visualizzati come disponibili.

1. Attiva la **prenotazione riunioni** e/o l&#39;integrazione **Live Chat**.

1. Vai a **Sfoglia abilità** e seleziona **Prenota riunione con vendite** e/o **Chat con le vendite**. Imposta i trigger, allega l’integrazione corrispondente e salva l’abilità.

1. Seleziona **Simula** per testare l&#39;esperienza end-to-end. Immettere una domanda di esempio e confermare che l&#39;instradamento viene eseguito al flusso di abilità e coinvolgimento corretto.

### Comportamento dopo la distribuzione

Quando le funzionalità sono attive:

- Le chat live in arrivo vengono visualizzate dai rappresentanti disponibili in tempo reale.
- Le riunioni prenotate vengono visualizzate in una visualizzazione riunioni.
- In Analytics è disponibile un report sulle prestazioni delle riunioni.
- Gli impegni per riunioni e chat vengono inviati a Marketo come attività, insieme ai dati delle attività esistenti.

## Condividere un collegamento di anteprima

Un collegamento di anteprima condivisibile consente alle parti interessate di rivedere e interagire con un portinaio senza accesso come compositore e senza distribuire il portinaio in un sito web live.

1. Dalla schermata di anteprima del portiere, genera un collegamento di anteprima condivisibile.

1. Condividi il collegamento con i revisori.

1. I revisori possono interagire con il concierge attraverso il collegamento senza accedere a Composer.

## Test prima della distribuzione

Utilizza l’esperienza di anteprima o simulazione dopo ogni modifica significativa della configurazione. Verifica almeno quanto segue:

- Il portinaio risponde alle domande generali dal contenuto del sito web previsto.
- Ogni abilità risponde solo ai trigger previsti.
- Le integrazioni richieste sono connesse e puntano all’origine dati corretta.
- Le ricerche e i confronti tra prodotti utilizzano l’istanza MCP di Commerce o il catalogo dei prodotti a cui sono destinati.
- Prenotazione riunione e Live Chat indirizzate ai rappresentanti designati.
- Tono, voce, istruzioni, guardrail e suggerimenti producono le risposte previste.
- Gli stili visivi e i componenti chat vengono visualizzati correttamente nelle visualizzazioni desktop e mobile.
- Le parti interessate possono esaminare l’esperienza tramite il collegamento di anteprima condivisibile, se disponibile.
