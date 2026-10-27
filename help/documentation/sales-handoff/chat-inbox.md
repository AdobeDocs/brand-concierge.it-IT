---
title: Casella in entrata chat
description: Scopri come un rappresentante commerciale riceve, gestisce, valuta e termina una chat in tempo reale di Brand Concierge nella casella in entrata della chat di Adobe Marketo Qualifier.
role: User
level: Beginner
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
    internal-label: Brand Concierge
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 4751ce408fb2aa6d1affae4dd7a5d81ca43ffc8a
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 1%
---
# Casella in entrata chat {#chat-inbox}

Quando un visitatore chiede di parlare con qualcuno, la chat arriva nella **[!UICONTROL Posta in arrivo chat]** in [!DNL Adobe Marketo Qualifier]. Questa pagina è la vista del rappresentante di una chat in diretta: cosa vedi quando arriva, quale contesto ottieni e cosa devi fare prima di poterla chiudere.

Per aprirla, nel pannello a sinistra in **[!UICONTROL Attività]**, seleziona **[!UICONTROL Casella in entrata Chat]**.

## Ricevi una chat {#receive}

Il tuo stato viene visualizzato nell’angolo in alto a destra della casella in entrata. **[!UICONTROL Disponibile]** significa che ora puoi ricevere le chat. Le ore di disponibilità della chat in tempo reale decidono se sei idoneo; vedi [Impostare la disponibilità della chat in tempo reale](representative-setup.md#chat-availability).

Il modo in cui una chat ti raggiunge dipende dal tipo di routing impostato nell&#39;integrazione di **[!UICONTROL Live Chat]**:

* Con il round robin, ogni rappresentante idoneo viene avvisato allo stesso tempo e il primo ad accettare prende la conversazione.
* Con l&#39;agente diretto, la chat viene sempre al rappresentante nominato.
* Con l’indirizzamento personalizzato, la chat viene indirizzata ai rappresentanti assegnati alla regola di priorità più alta corrispondente al visitatore.

Le conversazioni sono organizzate in due schede:

* **[!UICONTROL Attivo]** — conversazioni attualmente in corso.
* **[!UICONTROL Tutti]** — ogni conversazione, incluse quelle terminate.

## Ritira la conversazione {#pick-up}

Non inizia mai a fare freddo. Prima di digitare qualsiasi cosa, la casella in entrata fornisce tutto ciò che il visitatore ha già detto al portinaio.

![Casella in entrata chat che mostra il riassunto della conversazione del visitatore con un riepilogo e gli argomenti discussi e il pannello dei dettagli del profilo](../assets/sales-handoff-inbox-1.png){width="800" zoomable="yes"}

| Cosa vedi | Che cosa ti offre |
| --- | --- |
| **[!UICONTROL Riepilogo conversazione visitatore]** | Un **[!UICONTROL riepilogo]** della conversazione che il visitatore ha avuto con il portinaio e i **[!UICONTROL argomenti discussi]** |
| Trascrizione conversazione | Lo scambio completo con il portinaio, sopra il punto in cui è stata avviata la chat in diretta |
| **[!UICONTROL Dettagli modulo]** | Cosa ha inserito il visitatore nel modulo di pre-chat prima dell’iscrizione, ad esempio e-mail, interesse sul prodotto e azienda |

La trascrizione segna il passaggio di consegne con due righe di sistema, `Live chat session has been initiated` e `Agent <name> has joined the chat`, in modo da poter sempre dire quale parte della conversazione era il portinaio e quale parte è la tua.

Digita nella finestra di messaggio e seleziona **[!UICONTROL Invia]** per rispondere.

![Chat live in corso tra il rappresentante e il visitatore](../assets/sales-handoff-inbox-2.png){width="800" zoomable="yes"}

## Punteggio della conversazione {#conversation-score}

Prima di terminare una chat, valuta la qualifica del visitatore. Il punteggio è impostato da voi, il rappresentante che ha effettivamente parlato al visitatore, che è ciò che lo rende affidabile a valle.

Nel pannello **[!UICONTROL Dettagli profilo]**, in **[!UICONTROL Punteggio conversazione]**, seleziona una valutazione. Il trattino significa nessun punteggio e le icone di fiamma valutano la conversazione dal meno al più qualificato.

![Descrizione comando Punteggio conversazione che spiega che i punteggi sono memorizzati nel record cliente potenziale come 0, 1, 2 e 3](../assets/sales-handoff-inbox-4.png){width="600" zoomable="yes"}

| Selezione | Valore memorizzato | Significato |
| --- | --- | --- |
| Trattino | 0 | Meno qualificato |
| Una fiamma | 1 | Qualificato |
| Due fiamme | 2 | Qualificato |
| Tre fiamme | 3 | Più qualificati |

>[!IMPORTANT]
>
>Il punteggio è obbligatorio. Se si tenta di chiudere una chat senza assegnare un punteggio, verrà visualizzato l&#39;errore `Please score the conversation before you close the chat` e la chat rimarrà aperta. Dopo averlo valutato, viene visualizzata una conferma e puoi chiudere la chat.

![Conferma del salvataggio del punteggio di conversazione](../assets/sales-handoff-inbox-3.png){width="800" zoomable="yes"}

Il punteggio viene scritto nell&#39;attività **[!UICONTROL Coinvolgi chat in tempo reale nell&#39;attività Concierge]** in [!DNL Marketo Engage], dove è disponibile come vincolo su filtri e trigger. Utilizzala per promuovere il retargeting, il punteggio di lead, la personalizzazione e il passaggio di consegne nell’ambito del CRM. Vedi [Dati Brand Concierge in Marketo Engage](marketo-activities.md).

## Termina la chat {#end-chat}

Seleziona **[!UICONTROL Termina chat]** per chiudere la conversazione. Il visitatore può anche terminarlo dal proprio lato e gli viene richiesto di confermare prima.

Quando una chat viene chiusa, lo stato della conversazione viene registrato come uno dei due valori seguenti:

* **Terminata** — la conversazione è stata chiusa intenzionalmente da te o dal visitatore.
* **Ignorato** — il visitatore ha lasciato il sito e la conversazione è scaduta per inattività.

>[!NOTE]
>
>Le conversazioni in chat dal vivo vengono mantenute per 30 giorni.

## Passaggio successivo {#next}

Scopri cosa tutto questo riporta nel database di marketing in [dati Brand Concierge in Marketo Engage](marketo-activities.md).
