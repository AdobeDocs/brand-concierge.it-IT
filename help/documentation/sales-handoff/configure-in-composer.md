---
title: Attiva la prenotazione di chat e riunioni in diretta
description: Connetti le integrazioni Live Chat e Meeting Booking in Composer, quindi attiva l’handoff per acquisire competenze di vendita in modo che il tuo concierge sappia quando offrire a un utente.
role: User, Admin
level: Beginner
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
    internal-label: Brand Concierge
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 91cbec8d6f4e4800e3bdc8c8f60bfe9ed168a963
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%
---
# Attiva la prenotazione di chat e riunioni in tempo reale {#configure-in-composer}

Due cose devono essere a posto nel Compositore. Le integrazioni **[!UICONTROL Meeting Booking]** e **[!UICONTROL Live Chat]** offrono al portinaio la *possibilità* di verificare la disponibilità, avviare una chat e prenotare uno slot. L&#39;abilità **[!UICONTROL Trasferimento alle vendite]** indica *quando* utilizzarla.

>[!NOTE]
>
>Completa [Imposta prima i rappresentanti in Adobe Marketo Qualifier](representative-setup.md). Le integrazioni verificano la disponibilità di calendari connessi e chat in tempo reale e non verranno attivate senza di essi.

## Collegare l’integrazione della prenotazione della riunione {#connect-meeting-booking}

1. In Compositore, apri il tuo portinaio e seleziona **[!UICONTROL Integrazioni]** > **[!UICONTROL Sfoglia integrazioni]**.

   **[!UICONTROL Prenotazione riunione]** e **[!UICONTROL Live Chat]** sono visualizzati in **[!UICONTROL Integrazioni incorporate]**.

   ![Sfoglia il pannello integrazioni nel Compositore che mostra le schede di prenotazione di chat e riunioni in Integrazioni incorporate](../assets/sales-handoff-composer-1.png){width="800" zoomable="yes"}

1. Seleziona **[!UICONTROL Prenotazione riunione]**, quindi seleziona **[!UICONTROL Configura]**.

1. Immettere un nome e una descrizione.

   Denomina l&#39;integrazione per le operazioni eseguite in questo portinaio, ad esempio `Meeting booking - US region` o `Meeting booking - round robin`. È possibile collegarne più di uno, quindi il nome è il modo in cui si distinguono in un secondo momento.

1. Controlla lo stato della connessione al calendario.

   L’integrazione verifica che almeno un rappresentante nell’organizzazione abbia connesso un calendario.

   * In caso contrario, viene visualizzato un messaggio di errore che indica di connettere almeno un calendario prima di attivare la prenotazione della riunione. Torna a [!DNL Adobe Marketo Qualifier] e completa [Connetti il calendario](representative-setup.md#connect).
   * Se almeno uno ha, una conferma mostra che i rappresentanti sono disponibili.

1. Selezionare un tipo di routing: **[!UICONTROL Round robin]**, **[!UICONTROL Direct agent]** o **[!UICONTROL Custom routing]**.

   Se selezioni **[!UICONTROL Agente diretto]**, scegli il rappresentante che riceve ogni riunione prenotata tramite questo concierge. Se si seleziona **[!UICONTROL Routing personalizzato]**, vengono applicate le regole di routing create in [!DNL Adobe Marketo Qualifier]. Per informazioni sul comportamento di ciascuno di essi, vedere [Instradare le conversazioni ai rappresentanti](routing-rules.md).

1. Seleziona **[!UICONTROL Connetti]**.

## Connettere l’integrazione della chat live {#connect-live-chat}

1. In **[!UICONTROL Sfoglia integrazioni]**, selezionare **[!UICONTROL Live Chat]**, quindi selezionare **[!UICONTROL Configura]**.

1. Immettere un nome e una descrizione, ad esempio `Live chat - round robin`.

1. Controlla lo stato di disponibilità della chat in tempo reale.

   L’integrazione verifica che almeno un rappresentante abbia impostato la disponibilità della chat in tempo reale.

   * Se non ne è stato trovato uno, viene visualizzato un messaggio che ti invita ad aggiungere i rappresentanti che hanno impostato la disponibilità della chat in tempo reale. Torna a [!DNL Adobe Marketo Qualifier] e completa [Imposta disponibilità chat in tempo reale](representative-setup.md#chat-availability).
   * Se almeno uno ha, una conferma mostra che i rappresentanti sono disponibili.

1. Selezionare un tipo di instradamento.

   La chat in tempo reale supporta gli stessi tre tipi di instradamento della prenotazione della riunione. Con **[!UICONTROL Round robin]**, ogni rappresentante idoneo viene informato immediatamente e il primo ad accettare accetta prende la chat.

1. Seleziona **[!UICONTROL Connetti]**.

## Attiva il trasferimento all&#39;abilità di vendita {#activate-skill}

Le integrazioni sono ora connesse, ma il portinaio deve ancora sapere quando offrirle. Questo è il lavoro dell&#39;abilità.

1. In Compositore, seleziona **[!UICONTROL Abilità]** > **[!UICONTROL Esplora abilità]**, quindi seleziona **[!UICONTROL Invia a vendite]**.

   Il pannello dei dettagli mostra la descrizione dell&#39;abilità, le relative condizioni **[!UICONTROL Use when]**, le **[!UICONTROL Integrazioni]** consigliate e le **[!UICONTROL Istruzioni abilità]**.

   ![Sfogliare il pannello abilità con il passaggio all&#39;abilità di vendita selezionata, mostrando Usa quando le condizioni, le integrazioni consigliate e le istruzioni per l&#39;abilità](../assets/sales-handoff-composer-2.png){width="800" zoomable="yes"}

1. Selezionare **[!UICONTROL Modifica]**.

   ![Trasferimento all&#39;abilità di vendita in modalità di modifica con nome, descrizione e utilizzo dell&#39;abilità modificabili](../assets/sales-handoff-composer-3.png){width="800" zoomable="yes"}

1. Rivedi il nome e la descrizione dell’abilità e modificali se desideri.

1. Rivedi le condizioni **[!UICONTROL Use when]**.

   Questi sono gli intenti che attivano un handoff. L’abilità viene spedita con un set predefinito:

   | Condizione | Triggers su |
   | --- | --- |
   | Accesso consulente | Prenotare o pianificare una riunione, avviare una chat in diretta o chiedere di entrare in contatto con un rappresentante aziendale |
   | Vendite e acquisti | Prezzi, preventivi, sconti, assistenza agli acquisti o licenze aziendali |
   | Confronto con la concorrenza | Confronto delle soluzioni con alternative concorrenti, differenziazione o migrazione da una piattaforma concorrente |
   | Accesso alla versione di prova e POC | Impostazioni di prova, accesso ai parchi giochi, bozze di concetto o piloti |
   | Modifiche al contratto e alle licenze | Rinnovi del contratto, estensioni del termine o aggiornamenti del piano |
   | Procurement RFP o RFI | Invii e risposte RFP o RFI, questionari fornitore, moduli di approvvigionamento o documentazione di conformità |
   | Demo | Dimostrazioni di prodotto o procedure dettagliate |

   Seleziona **[!UICONTROL Aggiungi condizione]** per aggiungere un intento personale o eliminare le condizioni non applicabili alla tua azienda.

1. Aggiungi le integrazioni connesse.

   Aggiungi **[!UICONTROL Live Chat]**, **[!UICONTROL Prenotazione riunione]**, o entrambi, a seconda di ciò che desideri che il portinaio offra.

1. Rivedi le **[!UICONTROL istruzioni per l&#39;abilità]**.

   Le istruzioni vengono generate dalle condizioni e integrazioni selezionate, quindi nella maggior parte dei casi non è necessaria alcuna modifica.

   Modificale in linguaggio semplice quando desideri un controllo più preciso su quale intento porta a quale opzione. Ad esempio, puoi istruire il portinaio a offrire chat in diretta per domande sui prezzi, una riunione per richieste demo e entrambe per domande sull’approvvigionamento.

1. Seleziona **[!UICONTROL Salva]**.

## Test e pubblicazione {#test-and-publish}

Apri l&#39;anteprima e chiedi al portinaio qualcosa che corrisponda a una delle condizioni **[!UICONTROL Use when]**, ad esempio la richiesta di una demo. Il concierge dovrebbe offrirti di connetterti con uno specialista, mostrare l’opzione di chat, l’opzione di riunione, o entrambe, e presentare una disponibilità reale.

Quando il comportamento è corretto, pubblica il concierge per rendere il passaggio live sul tuo sito.

## Passaggi successivi {#next-steps}

I rappresentanti possono ora ricevere le chat e le prenotazioni di riunioni. Per informazioni sulla gestione di una chat da parte dei rappresentanti, vedere [Posta in arrivo chat](chat-inbox.md).
