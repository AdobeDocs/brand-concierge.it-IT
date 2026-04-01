---
title: Domande frequenti
description: Risposte alle domande frequenti su Adobe Brand Concierge.
role: User,Admin
level: Beginner
source-git-commit: 06911f38d17882cdae8441d5cbdbcdf786d9e6bb
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 1%

---

# Domande frequenti

Leggi questa sezione per le risposte alle domande più frequenti su Brand Concierge.

## Generale

### Perché utilizzare Brand Concierge? Che problema risolve?

Ulteriori ricerche si svolgono su strumenti di intelligenza artificiale esterni (ad esempio, ChatGPT, Gemini) invece che su siti web di marchi. I visitatori desiderano sempre più &quot;arrivare al punto&quot;, ad esempio &quot;Dimmi di X&quot;, &quot;Posso fare Y?&quot; Brand Concierge ti aiuta a mantenere tale conversazione sul sito: quando i visitatori arrivano sulle tue pagine (incluso da un assistente AI), possono continuare la conversazione con un assistente esperto sui tuoi contenuti. Puoi offrire un’esperienza coerente all’interno del marchio, invece di perderli per rispondere altrove a risposte generiche.

### Quali sono le differenze tra Brand Concierge e i chatbot?

Brand Concierge si distingue dai chatbot tradizionali sfruttando l’intelligenza artificiale generativa appositamente addestrata sui contenuti e sui dati dei clienti della tua organizzazione, anziché affidarsi a risposte basate su script o a risultati web generici. Questo consente all’assistente di fornire risposte personalizzate basate sul comportamento dei singoli clienti, di integrarsi in modo approfondito con i tuoi strumenti e dati di Adobe, di imparare continuamente da ogni interazione e di interpretare con precisione le intenzioni dei clienti oltre la corrispondenza delle parole chiave di base.

### Posso utilizzare Brand Concierge sia per B2C che per B2B?

Sì. I casi di utilizzo includono:

* **B2C:** individuazione prodotto, assistenza acquisti, supporto clienti, consigli personalizzati.
* **B2B:** Valutazioni guidate, confronti di funzionalità, pianificazione delle riunioni, routing del rappresentante commerciale, prenotazione delle consulenze.

### Quali settori possono utilizzare Brand Concierge?

Brand Concierge può essere utilizzato in una vasta gamma di settori, tra cui retail ed e-commerce, viaggi e ospitalità, servizi finanziari, sanità (con controlli di conformità), media e intrattenimento, tecnologia e software. In sostanza, qualsiasi settore che aiuti i clienti a trovare informazioni e prendere decisioni può trarre vantaggio dall&#39;implementazione di Brand Concierge.

## Dati e privacy

### I dati del cliente sono sicuri?

Sì. Brand Concierge garantisce la sicurezza dei dati dei clienti aderendo alle normative RGPD e CCPA, elaborando i dati sull’infrastruttura sicura di Adobe, fornendo un controllo sull’utilizzo dei dati e salvaguardando le conversazioni attraverso la crittografia e la registrazione dei controlli.

Tutte le conversazioni avvengono sulle tue proprietà, non sui server di terze parti.

### Quali origini dati è possibile connettere?

È possibile connettere i seguenti tipi di origini dati a Brand Concierge:

| Tipo di Source dati | Origini/Dettagli disponibili |
|------------------|---------------------------|
| **Prodotto e contenuto** | Cataloghi di prodotti<br>Sistemi di inventario<br>Knowledge base e documentazione<br>Contenuto del sito web tramite caricamento URL CSV<br>Contenuto Adobe Experience Manager<br>Dati Adobe Commerce |
| **Dati cliente** | Profili Adobe Experience Platform<br>Dati sul comportamento di Adobe Analytics<br>Attributi del cliente di prime parti<br>API di terze parti (configurate) |
| **Formato file CSV** | Una colonna contenente gli URL del sito Web<br>Brand Concierge scansiona gli URL ed estrae automaticamente il contenuto<br>Elaborazione in tempo reale degli aggiornamenti dello stato<br>È possibile caricare più file CSV per aree di contenuto diverse |

Tutti i dati seguono le tue regole di governance.

### I clienti possono rinunciare alla personalizzazione?

Sì. I clienti che rinunciano ricevono risposte utili senza dover personalizzare il comportamento. Configura la gestione delle rinunce in base alle tue politiche sulla privacy.

### Ci sono implicazioni relative al consenso o alla privacy?

Sì. **Dati sulla conversazione:** se la conversazione include informazioni personali o identificabili, la raccolta, l&#39;archiviazione e l&#39;utilizzo devono essere conformi alle politiche relative al consenso e alla privacy (ad esempio, GDPR, CCPA). **Analytics:** Quando Concierge invia eventi ad Experience Platform o Analytics, questi possono essere soggetti al consenso e alla governance esistenti (ad esempio, stringhe di consenso, etichette di utilizzo dei dati). Consigliamo di trattare Concierge come qualsiasi altra esperienza digitale di prima parte: assicurati che il banner e le preferenze di consenso del tuo sito coprano i dati e le analisi di conversazione e chat e allineino i dati dell’evento alla tua strategia di consenso. Richiedi una revisione legale e di conformità prima del lancio.

## Profili e personalizzazione

### Concierge utilizza i profili cliente (ad esempio, Real-Time CDP) per adattare le risposte? Cosa succede se il visitatore è parte di un percorso?

Nell’ambito attuale, Concierge si concentra sui visitatori anonimi: risponde dalla conversazione e dalla knowledge base (sito web e catalogo), non da una ricerca in tempo reale dell’identità o dello stato del percorso in Real-Time CDP. Le funzionalità della roadmap includono lo sviluppo dei lead, il passaggio alle vendite e il retargeting, che si allinea maggiormente ai profili noti e al contesto del percorso. Personalizzazione delle risposte per &quot;questo visitatore ha un profilo?&quot; o &quot;dove si trovano in un percorso?&quot; è un miglioramento futuro. Per il momento, l’esperienza è simile per i visitatori anonimi.

## Rollout e timeline

### Quanto tempo ci vuole in genere per andare &quot;live&quot;?

Grazie al lavoro in parallelo e alla collaborazione attiva, molte implementazioni vengono pubblicate in circa 6-9 settimane. La gestione temporanea può iniziare rapidamente una volta che gli input (URL, catalogo, linee guida del brand) sono pronti. Dopo l’impostazione dell’accordo e della produzione, puoi passare attraverso il tuning della qualità e un rollout controllato (ad esempio, 5%, quindi scalabilità al 100% in circa una settimana).

## Configurazione e controllo

### Come posso controllare la voce del brand?

Puoi controllare la voce del brand direttamente nell’interfaccia utente configurando elementi come il tono (da formale a informale), il linguaggio (da semplice a tecnico) e la personalità (ad esempio utile, entusiasta o professionale). Inoltre, puoi definire modelli di risposta utilizzando modelli ed esempi e stabilire guardrail per applicare regole di conformità e limiti. Inizia con i prompt di riferimento di Adobe e personalizza queste impostazioni per riflettere l’identità unica del tuo marchio.

### Cosa succede quando Brand Concierge non è in grado di rispondere a una domanda?

È possibile configurare i comportamenti di fallback per determinare la risposta di Brand Concierge quando non è in grado di rispondere a una domanda. Le opzioni includono la visualizzazione di un messaggio aggraziato di tipo &quot;Non posso fare a meno di&quot;, suggerimenti di domande alternative, collegamento a risorse self-service o inoltro automatico della richiesta a un agente umano. Scegli cosa funziona meglio per il tuo marchio.

### Posso personalizzare il design visivo?

Sì. Personalizza tutti gli elementi visivi, tra cui:

* Colori e marchio
* Caratteri e composizione tipografica
* Stili pulsante
* Posizionamento widget
* Layout schede
* Formattazione risposta

Gli SDK forniscono componenti predefiniti e opzioni di personalizzazione complete.

### Quanto tempo richiede la configurazione?

La durata della configurazione può dipendere dal tipo di implementazione. L’implementazione di base, che include un catalogo di prodotti esistente, il contenuto delle domande frequenti standard e le impostazioni predefinite, può richiedere circa 3-5 giorni. D’altra parte, il completamento di implementazioni avanzate con integrazioni personalizzate, ampia personalizzazione, flussi di lavoro complessi e regole di conformità personalizzate può richiedere circa 2-4 settimane.

### Come funzionano l’anteprima e il test?

Brand Concierge include strumenti di test incorporati:

| Strumento di prova | Funzioni |
|--------------|----------|
| **Modalità anteprima** | Simula le conversazioni con i clienti<br>Modifica le impostazioni in tempo reale<br>Visualizza le modifiche all&#39;istante<br>Condividi i collegamenti di anteprima con il tuo team |
| **Visualizzazione Tester** | Valuta le risposte con miniature in alto/in basso<br>Fornisci un feedback strutturato in 4 categorie<br>Aggiungi commenti dettagliati<br>Tieni traccia del feedback nella dashboard |

Tutti i test vengono eseguiti prima della distribuzione ai clienti.

### I clienti possono programmare riunioni con il nostro team?

Sì, i clienti possono pianificare riunioni con il team utilizzando l’abilità Prenotazione riunione. Per abilitare questa funzione, attiva l’abilità in Configurazione abilità, definisci gli intenti di attivazione (ad esempio, &quot;parla con le vendite&quot;), connetti il calendario o il sistema di pianificazione e imposta la disponibilità e i tipi di riunione. Una volta configurata, i clienti possono richiedere riunioni durante le conversazioni e Brand Concierge semplifica il processo di pianificazione senza richiedere loro di uscire dalla chat.

### Chi gestisce la pronta progettazione?

I consulenti Adobe gestiscono la progettazione dei prompt in background:

1. Rispondi alle domande sulla configurazione nella pagina Abilità.
1. Fornisci conoscenze sul prodotto, regole aziendali ed evita parole chiave.
1. Invia i tuoi input.
1. I consulenti Adobe utilizzano le risposte fornite per richiedere suggerimenti ottimizzati per gli ingegneri.
1. Le modifiche si riflettono automaticamente nel portinaio.

In questo modo il tuo concierge utilizza i pattern di prompt di IA basati sulle best practice, mantenendo al contempo i requisiti del brand specifici.

## Espressione e tono del brand

### Se nell’espressione del marchio definisco &quot;giocoso ed entusiasta&quot;, l’intelligenza artificiale lo farà in modo eccessivo?

Può. Alcuni clienti hanno riferito che l’intelligenza artificiale tende a esagerare l’entusiasmo quando impostata su &quot;giocosa ed entusiasta&quot;, ad esempio punti esclamativi doppi o superlativi forti. Per il pubblico regolamentato o medico (ad esempio, il pharma, la nutrizione della prima vita), consigliamo di comporre entusiasmo e giocosità mantenendo il tono conversazionale e informale. Utilizza impostazioni moderate e sintonizza in base al feedback; per i settori regolamentati, spendi verso &quot;conversazionale&quot; piuttosto che &quot;entusiasta&quot;.

## Prestazioni e analisi

### Come posso misurare il successo?

Puoi misurare il successo utilizzando la dashboard di Brand Concierge. Utilizza la dashboard per tenere traccia di metriche quali:

| Metrica | Cosa Traccia |
|--------|----------------|
| **Coinvolgimento** | Volume di conversazione, durata della sessione |
| **Soddisfazione** | Punteggi sentiment, valutazioni di feedback |
| **Conversione** | Tassi di acquisto per assistiti e non assistiti |
| **Argomenti** | Domande e richieste più comuni |
| **Handoff** | Tassi e motivi di escalation |
| **Prestazioni** | Precisione della risposta, tempo di risoluzione |

Puoi anche eseguire l’integrazione con Adobe Analytics per analisi più approfondite.

### Cosa devo fare se il sentiment cade?

Se noti un calo nel sentiment, indaga le cause sottostanti esaminando le query recenti non riuscite, verificando eventuali vuoti di contenuto, analizzando i feedback negativi, testando il tono appropriato e verificando eventuali problemi tecnici. Una volta identificate le cause principali, affrontarle tempestivamente e continuare a monitorare i miglioramenti.

## Integrazione e assistenza tecnica

### Ho bisogno di altri prodotti Adobe?

No, ma migliorano le prestazioni:

| Opzione di integrazione | Funzionalità |
|-------------------|--------------|
| **Autonomo** | Compatibile con il catalogo e il contenuto dei prodotti |
| **Con Adobe Experience Platform** | Profili cliente unificati<br>Personalizzazione avanzata<br>Coerenza cross-channel |
| **Con Adobe Commerce** | Inventario in tempo reale<br>Storico ordini<br>Integrazione carrello |
| **Con Adobe Experience Manager** | Gestione dei contenuti<br>Aggiornamenti dinamici<br>Supporto multisito |

### Cosa succede se il mio sito non è su Adobe?

Brand Concierge funziona con qualsiasi piattaforma. JavaScript SDK si integra con qualsiasi sito web e gli SDK per dispositivi mobili funzionano con qualsiasi back-end dell’app.

### Come funziona la consegna degli agenti?

Quando viene attivato il trasferimento dell’agente, Brand Concierge trasferisce all’agente la cronologia completa delle conversazioni, il profilo cliente e l’ID, l’intento identificato, i dettagli dei prodotti discussi e qualsiasi tentativo di risoluzione. In questo modo gli agenti hanno un contesto completo e possono continuare la conversazione senza interruzioni, senza richiedere ai clienti di ripetere le informazioni.

### Posso supportare più lingue?

Sì. Configurare il supporto linguistico per ogni assistente in base alla base cliente. Brand Concierge rileva la lingua del cliente e risponde di conseguenza.
