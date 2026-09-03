---
title: Guida per sviluppatori e personalizzazione
description: Scopri come installare Brand Concierge Web SDK e il client web, personalizzare l’aspetto e il contenuto, gestire gli eventi lato client ed esportare i dati di conversazione.
role: Developer,Admin
level: Experienced
toc: true
source-git-commit: 13db0491c987a08492820ac216e20feb87f30e44
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 4%

---


# Guida per sviluppatori e personalizzazione {#developer-customization-guide}

Questa guida è destinata agli sviluppatori e ai team tecnici che implementano o personalizzano un’implementazione di Brand Concierge. Include l&#39;installazione del Web SDK e del Web Client, la personalizzazione dell&#39;aspetto e del contenuto, l&#39;ascolto degli eventi lato client tramite le funzioni di callback e l&#39;esportazione dei dati di conversazione per il reporting.

## Installazione di Web SDK e Web Client {#installation}

### Prerequisiti {#prerequisites}

* L’organizzazione è un cliente di Adobe Experience Platform (AEP).
* La pagina è dotata di strumentazione per Adobe Experience Platform Web SDK.
* L’ID dello stream di dati utilizzato nella pagina è abilitato per Brand Concierge.

### Passaggio 1: inserire il Web SDK {#inject-web-sdk}

Aggiungi quanto segue alla sezione `<head>` della pagina:

```html
<script>
  !(function (n, o) {
    o.forEach(function (o) {
      n[o] ||
        ((n.__alloyNS = n.__alloyNS || []).push(o),
        (n[o] = function () {
          var u = arguments;
          return new Promise(function (i, l) {
            n[o].q.push([i, l, u]);
          });
        }),
        (n[o].q = []));
    });
  })(window, ["alloy"]);
</script>
<script src="https://cdn1.adoberesources.net/alloy/2.31.1/alloy.min.js"></script>
```

### Passaggio 2: inserire il client Web {#inject-web-client}

Aggiungere quanto segue dopo lo script Web SDK, sempre nella sezione `<head>`:

```html
<script src="https://experience.adobe.net/solutions/experience-platform-brand-concierge-web-agent/static-assets/main.js"></script>
```

### Passaggio 3: configurare il Web SDK {#configure-web-sdk}

Chiama `alloy("configure", ...)` con i valori della tua organizzazione al posto dei segnaposto di seguito:

```javascript
alloy("configure", {
  defaultConsent: "in",
  edgeDomain: "edge.adobedc.net",
  edgeBasePath: "ee",
  datastreamId: "YOUR_DATASTREAM_ID",
  orgId: "YOUR_IMS_ORG_ID",
  debugEnabled: true,
  idMigrationEnabled: false,
  thirdPartyCookiesEnabled: false,
  prehidingStyle: ".personalization-container { opacity: 0 !important }",
  onBeforeEventSend: (options) => {
    const x = options.xdm;
    const params = new URLSearchParams(window.location.search);
    const titleParam = params.get("title");
    if (titleParam) {
      x.web.webPageDetails.name = titleParam;
    } else {
      x.web.webPageDetails.name = "default-page";
    }
    return true;
  }
});
alloy("sendEvent", {});
```

| Campo | Descrizione |
|---|---|
| `datastreamId` | ID dello stream di dati configurato per questa pagina, abilitato per Brand Concierge. |
| `orgId` | L’ID dell’organizzazione IMS in cui è configurato il portinaio. |
| `debugEnabled` | Impostato su `false` in produzione dopo la verifica dell&#39;integrazione. |
| `prehidingStyle` | CSS applicato prima del caricamento del contenuto di personalizzazione, per evitare un lampo di contenuto non formattato. |
| `onBeforeEventSend` | Hook opzionale per modificare il payload XDM prima dell’invio, di solito utilizzato per impostare il nome o il contesto della pagina. |

### Passaggio 4: inizializzare il client Web {#initialize-web-client}

Dopo la chiamata di configurazione di Web SDK, inizializzare il client Web chiamando l&#39;API bootstrap:

```javascript
window.adobe.concierge.bootstrap({
  instanceName: "alloy",
  stylingConfigurations: window.styleConfigurations,
  selector: "#brand-concierge-mount"
});
```

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `instanceName` | stringa | Sì | Nome dell&#39;istanza di Web SDK. |
| `stylingConfigurations` | Oggetto JSON | Sì | Configurazione dello stile del client Web (vedere [Personalizzazione visiva e del contenuto](#customization)). |
| `selector` | stringa | Sì | Selettore CSS per l’elemento HTML in cui si monta il client web. |
| `onEvent` | funzione | No | Callback per eventi lato client (vedere [Eventi lato client e funzioni di callback](#events)). |

## Personalizzazione visiva e dei contenuti {#customization}

L&#39;oggetto `stylingConfigurations` passato a `bootstrap()` controlla l&#39;aspetto, il comportamento e il testo in tutto il client Web. È organizzato in diverse aree.

### Metadati {#metadata}

```javascript
"metadata": {
  "brandName": "Your Brand",
  "version": "1.0.0",
  "language": "en-US",
  "namespace": "brand-concierge"
}
```

### Comportamento {#behavior}

Controlla il comportamento funzionale delle singole funzioni di chat.

```javascript
"behavior": {
  "input": {
    "enableVoiceInput": true
  },
  "chat": {
    "messageAlignment": "left",
    "messageWidth": "80%"
  },
  "privacyNotice": {
    "title": "Privacy Notice",
    "text": "By using this automated chatbot, you consent that any personal information you provide in the chat may be collected, used, analyzed, disclosed, and retained by Adobe and its service providers, in accordance with the Adobe Privacy Policy. Please do not enter any sensitive personal information (e.g., financial or health data)."
  },
  "disclaimer": {
    "attachWithInput": true
  },
  "chatTranscript": {
    "enabled": true,
    "maxSessions": 1,
    "maxMessagesPerSession": 20,
    "cleanupInterval": 24
  },
  "meetingForm": {
    "fieldsPerRow": 2,
    "title": { "text": "Schedule meeting", "alignment": "left" },
    "subtitle": { "text": "I'd be happy to help you schedule a meeting! Please fill out the form below, and we'll follow up with a calendar to confirm your day and time.", "alignment": "left" },
    "buttons": {
      "submit": { "text": "Schedule meeting", "alignment": "left" },
      "cancel": { "text": "Cancel", "alignment": "left" }
    }
  },
  "calendarWidget": {
    "title": { "text": "Book a meeting", "alignment": "left" },
    "subtitle": { "text": "Thanks! Here's a calendar where you can choose a time that works best for your schedule:", "alignment": "left" },
    "postTitle": { "text": "Once confirmed, you'll receive a calendar invite with all the details.", "alignment": "left" },
    "buttons": {
      "confirm": { "text": "Schedule a meeting", "alignment": "left" },
      "cancel": { "text": "Cancel", "alignment": "left" }
    }
  }
}
```

### Dichiarazione di non responsabilità {#disclaimer}

```javascript
"disclaimer": {
  "text": "AI responses may be inaccurate or misleading. Be sure to double check answers and sources."
}
```

### Stringhe di testo {#text-strings}

È possibile eseguire l&#39;override di tutte le copie rivolte all&#39;utente tramite l&#39;oggetto `text`. Chiavi comuni:

| Chiave | Scopo |
|---|---|
| `welcome.heading` / `welcome.subheading` | Titolo e testo secondario della schermata iniziale |
| `input.placeholder` | Testo segnaposto campo di input |
| `input.messageInput.aria` / `input.send.aria` / `input.mic.aria` | Etichette di accessibilità per i controlli di input |
| `error.network` / `error.general` | Messaggi di errore mostrati al visitatore |
| `loading.message` | Testo visualizzato durante la generazione di una risposta |
| `feedback.dialog.title.positive` / `.negative` | Titoli della finestra di dialogo Feedback |
| `feedback.dialog.question.positive` / `.negative` | Testo della finestra di dialogo del feedback |
| `feedback.toast.success` | Avviso popup di conferma dopo l’invio del feedback |
| `feedback.thumbsUp.aria` / `feedback.thumbsDown.aria` | Etichette di accessibilità per i pulsanti di feedback |

### Array {#arrays}

Elenchi di contenuti configurabili:

```javascript
"arrays": {
  "welcome.examples": [
    {
      "text": "I want to edit and enhance my photos",
      "image": "https://example.com/idea-1.png",
      "backgroundColor": "#66BFE7"
    }
  ],
  "feedback.positive.options": [
    "Helpful and relevant recommendations",
    "Clear and easy to understand",
    "Friendly and conversational tone",
    "Visually appealing presentation",
    "Other"
  ],
  "feedback.negative.options": [
    "Not helpful or relevant",
    "Confusing or unclear",
    "Too formal or robotic",
    "Poor visual presentation",
    "Other"
  ]
}
```

### Risorse {#assets}

```javascript
"assets": {
  "icons": {
    "company": "<svg>...</svg>"
  }
}
```

### Tema {#theme}

Proprietà personalizzate CSS che controllano colori, font e layout:

```css
"theme": {
  "--color-primary": "#1473e6",
  "--color-primary-hover": "#0056b3",
  "--color-button-primary": "#3B63FB",
  "--color-accent": "#9085ED",
  "--color-button-submit": "#4759e6",
  "--color-button-submit-hover": "#3a4bce",
  "--color-message-user": "#1473e6",
  "--font-family": "'Adobe Clean', adobe-clean, 'Trebuchet MS', sans-serif",
  "--main-container-background": "linear-gradient(135deg, #66ccff, #cc99ff, #ffcc99, #ccff99)",
  "--submit-button-fill-color": "white",
  "--card-text-background": "var(--color-background)",
  "--card-text-border-radius": "var(--border-radius-card)",
  "--message-concierge-link-decoration": "underline",
  "--message-max-width": "100%"
}
```

## Eventi lato client e funzioni di callback {#events}

Il sistema di callback degli eventi consente a una pagina di osservare in tempo reale gli eventi del ciclo di vita del client web, le interazioni degli utenti, le risposte, i feedback e gli errori, utile per inviare dati di coinvolgimento a Adobe Analytics, Google Analytics o altri sistemi di terze parti.

### Caratteristiche principali {#key-characteristics}

* **Callback singolo**: una funzione `onEvent` riceve tutti i tipi di evento, distinti da `event.eventType`.
* **Sola lettura**: i dati evento sono uno snapshot clonato e non possono essere utilizzati per modificare il comportamento del client.
* **Isolate da errori**: le eccezioni generate nel callback vengono rilevate e registrate e non interrompono il client Web.
* **Registrazione effettuata tramite`bootstrap()`**. Passaggio eseguito come `onBeforeEventSend`.

### Avvio rapido {#quick-start}

```javascript
window.adobe.concierge.bootstrap({
  instanceName: "my-instance",
  selector: "#brand-concierge-mount",
  stylingConfigurations: { /* ... */ },
  onEvent: (event) => {
    console.log(event.eventType, event.timestamp, event.data);
  }
});
```

### Filtraggio per tipo di evento {#filtering}

```javascript
onEvent: (event) => {
  switch (event.eventType) {
    case "query:submitted":
      console.log("User query:", event.data.query);
      break;
    case "response:completed":
      console.log("Response received:", event.data.conversationId);
      break;
    case "card:clicked":
      console.log("Card clicked:", event.data.element.entity_info.productName);
      break;
    case "error:occurred":
      console.log("Error:", event.data.errorMessage);
      break;
  }
}
```

### Tipi di evento {#event-types}

| Tipo di evento | Elemento “value” | Categoria | Quando si attiva |
|---|---|---|---|
| `WEBCLIENT_INITIALIZED` | `webclient:initialized` | Ciclo di vita | Inizializzazione del client completata (montaggio DOM, contenuto caricato) |
| `QUERY_SUBMITTED` | `query:submitted` | Interazione dell’utente | L’utente invia un messaggio (digitato o suggerito) |
| `PROMPT_SUGGESTION_CLICKED` | `promptSuggestion:clicked` | Interazione dell’utente | L’utente fa clic su una pillola di suggerimento del prompt |
| `CARD_CLICKED` | `card:clicked` | Interazione dell’utente | L’utente fa clic su una scheda |
| `HISTORY_CLEARED` | `history:cleared` | Interazione dell’utente | L&#39;utente cancella la cronologia della chat |
| `RESPONSE_STARTED` | `response:started` | Risposta | Il primo blocco di streaming arriva dall’API |
| `RESPONSE_COMPLETED` | `response:completed` | Risposta | Viene ricevuta e riprodotta una risposta completa |
| `CARDS_RENDERED` | `cards:rendered` | Risposta | Rendering delle schede (immagine singola o carosello) completato |
| `FEEDBACK_SUBMITTED` | `feedback:submitted` | Feedback | L’utente invia un modulo di feedback (miniature verso l’alto o verso il basso con dettagli) |
| `ERROR_OCCURRED` | `error:occurred` | Errore | Si è verificato un errore (rete, API o runtime) |

### Eventi del ciclo di vita {#lifecycle-events}

`webclient:initialized` viene attivato dopo che il client è stato completamente inizializzato: contenuto caricato, CSS inserito, interfaccia utente chat di cui è stato eseguito il rendering nel DOM.

```json
{
  "eventType": "webclient:initialized",
  "timestamp": 1741638123789,
  "data": {
    "instanceName": "my-instance"
  }
}
```

### Eventi di interazione dell’utente {#user-interaction-events}

`query:submitted` viene attivato quando l&#39;utente invia un messaggio, digitato, da un suggerimento di richiesta o da un&#39;opzione di widget.

```json
{
  "eventType": "query:submitted",
  "timestamp": 1741638124000,
  "data": {
    "query": "What photo editing tools do you offer?"
  }
}
```

`promptSuggestion:clicked` viene attivato quando l&#39;utente fa clic su una pillola di suggerimento. Genera *prima* dell&#39;evento `query:submitted` successivo.

```json
{
  "eventType": "promptSuggestion:clicked",
  "timestamp": 1741638124100,
  "data": {
    "suggestion": "Tell me more about Photoshop"
  }
}
```

`card:clicked` viene attivato quando l&#39;utente fa clic su una scheda.

```json
{
  "eventType": "card:clicked",
  "timestamp": 1741638124200,
  "data": {
    "element": {
      "entity_info": {
        "productName": "Adobe Photoshop",
        "productDescription": "Photo editing software",
        "productPageURL": "https://www.adobe.com/it/products/photoshop.html",
        "productImageURL": "https://example.com/photoshop.png"
      }
    }
  }
}
```

`history:cleared` viene attivato quando l&#39;utente fa clic sul pulsante clear-chat-history.

```json
{
  "eventType": "history:cleared",
  "timestamp": 1741638124400,
  "data": {}
}
```

### Eventi di risposta {#response-events}

`response:started` viene attivato quando il primo blocco di streaming arriva dall&#39;API.

```json
{
  "eventType": "response:started",
  "timestamp": 1741638125000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456"
  }
}
```

`response:completed` viene attivato quando è stata ricevuta la risposta completa.

```json
{
  "eventType": "response:completed",
  "timestamp": 1741638126000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456"
  }
}
```

`cards:rendered` viene attivato dopo il rendering delle schede nel DOM. Viene attivato separatamente da `response:completed` e indica la modalità di visualizzazione utilizzata.

```json
{
  "eventType": "cards:rendered",
  "timestamp": 1741638126100,
  "data": {
    "element": [
      { "entity_info": { "productName": "Adobe Photoshop" } },
      { "entity_info": { "productName": "Adobe Illustrator" } }
    ],
    "displayMode": "carousel"
  }
}
```

### Eventi di feedback {#feedback-events}

`feedback:submitted` viene attivato quando l&#39;utente completa e invia un modulo di feedback (dopo i pollici verso l&#39;alto o verso il basso).

```json
{
  "eventType": "feedback:submitted",
  "timestamp": 1741638127000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456",
    "feedbackType": "negative",
    "selectedOptions": ["Incorrect information", "Not relevant"],
    "notes": "The response did not address my question about pricing."
  }
}
```

### Eventi di errore {#error-events}

`error:occurred` viene attivato quando il client rileva un errore di rete, API o runtime.

```json
{
  "eventType": "error:occurred",
  "timestamp": 1741638128000,
  "data": {
    "errorMessage": "Something went wrong. Please try again."
  }
}
```

### Struttura dell’oggetto evento {#event-object-structure}

Ogni evento condivide la stessa forma di primo livello:

```typescript
interface BrandConciergeEvent {
  eventType: string;  // e.g. "query:submitted"
  timestamp: number;  // Unix epoch, milliseconds
  data: object;       // Event-specific payload
}
```

### Riferimento tipo di dati: Elemento (scheda prodotto) {#element-reference}

```typescript
interface Element {
  id?: string;
  type?: string;
  entity_info: {
    productName: string;
    productDescription: string;
    description: string;
    productPageURL: string;
    details: string;
    backgroundColor: string;
    learningResource: string;
    productImageURL: string;
    logo: string;
    variants?: Record<string, ElementVariant>;
    primary: ElementAction;
    secondary: ElementAction;
  };
}

interface ElementAction {
  label: string;
  url: string;
}
```

### Best practice {#best-practices}

* **Utilizza per analisi e monitoraggio.** Tieni traccia di coinvolgimento, pattern di query e interesse per il prodotto; inoltra `error:occurred` a un servizio di tracciamento degli errori; tieni traccia dei clic sulla carta per l&#39;analisi della conversione.
* **Mantieni il callback veloce.** Viene eseguito in modo sincrono sul thread principale, quindi evita di bloccare le chiamate di rete:

```javascript
// Good — fire and forget
onEvent: (event) => {
  navigator.sendBeacon("/analytics", JSON.stringify(event));
}

// Avoid — blocking network call
onEvent: async (event) => {
  await fetch("/analytics", { body: JSON.stringify(event) });
}
```

* **Non fare affidamento su un ordine di eventi rigoroso** per le macchine a stato. Gli eventi si attivano in una sequenza logica, ma utilizzano `conversationId` e `interactionId` per correlare gli eventi correlati anziché assumere l&#39;ordine.
* **Gestisci gli errori nel callback.** Il client isola e registra gli errori di callback, ma gli errori non gestiti all’interno del callback possono comunque perdere i dati di analisi:

```javascript
onEvent: (event) => {
  try {
    myAnalytics.track(event);
  } catch (e) {
    console.warn("Analytics tracking failed", e);
  }
}
```

## Esportare conversazioni tramite AEP Query Service {#export-conversations}

Brand Concierge scrive i dati di conversazione (prompt, risposte e feedback) nei set di dati di Adobe Experience Platform (AEP). È possibile eseguire query direttamente con Query Service (SQL) per generare rapporti personalizzati.

### Trovare il set di dati e il nome della tabella {#find-dataset}

1. Apri Adobe Experience Platform.

1. Vai a **[!UICONTROL Set di dati]**.

1. Cerca `cja_brand_concierge` per elencare i set di dati relativi a Brand Concierge.

1. Apri il set di dati necessario (ad esempio, risposte rispetto ad altri flussi, se ne esiste più di uno).

1. Nella visualizzazione dei dettagli del set di dati, individua il **[!UICONTROL nome tabella]** utilizzato da Query Service ed esamina i dati di esempio o di anteprima per confermare le colonne (prompt, risposte, feedback, marche temporali e così via).

>[!NOTE]
>
>I nomi delle tabelle sono legati a ciascun set di dati e differiscono in base all’ambiente e alla sandbox. Se disponi di più sandbox o implementazioni, ripeti questi passaggi nella sandbox corretta in modo che il nome della tabella corrisponda a dove vengono scritti i dati.

### Query di esempio {#example-query}

```sql
SELECT *
FROM cja_brand_concierge_responses_dataset_5f5105bd_1c38_4ebc_8505_bd
WHERE timestamp >= TIMESTAMP '2026-03-16 00:00:00'
  AND timestamp <= NOW()
ORDER BY timestamp ASC;
```

>[!IMPORTANT]
>
>Il nome della tabella precedente è solo un&#39;illustrazione, non codificarlo. Conferma prima il nome effettivo della tabella per il set di dati in AEP (vedi [Trova il set di dati e il nome della tabella](#find-dataset)) e regola il filtro temporale, l&#39;ordinamento o altre clausole in base alle tue esigenze di reporting. Esegui la query dal flusso di lavoro di Query Service (interfaccia utente, API o client connesso) della tua organizzazione, utilizzando la stessa sandbox del set di dati.

### Eseguire una query nell’interfaccia utente di Query Service {#run-query-ui}

Se hai bisogno di un richiamo dati manuale per il reporting, l’interfaccia utente di Query Service ti permette di eseguire e scaricare direttamente i risultati:

1. In Adobe Experience Platform, vai a **[!UICONTROL Query]**.

1. Immettere la query nell&#39;editor e fare clic su **[!UICONTROL Esegui query]**.

1. I risultati vengono visualizzati nella scheda **[!UICONTROL Risultati]** sotto l&#39;editor al termine della query. Da lì, puoi scaricare i risultati.

### Ulteriori informazioni {#further-reading}

* [Documentazione API di Query Service](https://experienceleague.adobe.com/it/docs/experience-platform/query/home){target="_blank"}: riferimento ufficiale di Adobe per il comportamento, i limiti, l&#39;autenticazione e i percorsi API di Query Service, che cambiano nel tempo indipendentemente da questa guida.
