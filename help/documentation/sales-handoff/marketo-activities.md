---
title: Dati Brand Concierge in Marketo Engage
description: Comprendi i campi di origine del lead e i tre tipi di attività di concierge scritti in Adobe Marketo Engage e come utilizzarli in elenchi avanzati e campagne avanzate.
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
source-wordcount: '785'
ht-degree: 4%
---
# Dati Brand Concierge in Marketo Engage {#marketo-activities}

Quando [!DNL Adobe Marketo Engage] è connesso, ogni visitatore che compila un modulo, registra una riunione o avvia una chat in tempo reale diventa un record persona in [!DNL Marketo] e il suo impegno di concierge viene scritto in tale record come tipi di attività nativi. Ciò significa che è possibile creare elenchi smart e campagne smart sul comportamento di concierge esattamente come si farebbe con qualsiasi altra attività di [!DNL Marketo].

>[!NOTE]
>
>La prenotazione di chat e riunioni in tempo reale non richiede [!DNL Marketo Engage]. Senza di esso, i dati descritti in questa pagina rimangono in [!DNL Adobe Marketo Qualifier]. Consulta [Panoramica sulla prenotazione di chat e riunioni in tempo reale](overview.md#prerequisites).

## Creazione di lead e attribuzione di origine {#lead-creation}

Una persona creata tramite un portinaio viene taggata in modo da poter sempre distinguere la sua provenienza.

| Campo | Valore |
| --- | --- |
| **[!UICONTROL Persona Source]** | `Brand Concierge` |
| **[!UICONTROL Tipo Source Originale]** | `Chat` |
| **[!UICONTROL Informazioni originali su Source]** | `Concierge` |
| **[!UICONTROL Tipo Source Registrazione]** | `Chat` |
| **[!UICONTROL Informazioni sulla registrazione di Source]** | `Concierge` |

![Scheda Informazioni record persona di Marketo che mostra il Source della persona impostato su Brand Concierge e i campi di origine della chat e del concierge](../assets/sales-handoff-marketo-1.png){width="800" zoomable="yes"}

## Tipi di attività {#activity-types}

Tre tipi di attività nativi vengono inviati al record persona. Tutti e tre sono disponibili come trigger e filtri.

![Registro attività Marketo per una persona che mostra Coinvolgi con il portinaio, Pianifica riunione nel portinaio e Coinvolgi chat in tempo reale nelle voci del portinaio](../assets/sales-handoff-marketo-2.png){width="800" zoomable="yes"}

### Coinvolgi il portinaio {#engage-with-concierge}

Registrato quando un visitatore interagisce con il portinaio.

| Attributo | Descrizione |
| --- | --- |
| Nome portinaio | Il portinaio con cui il visitatore si è fidanzato |
| ID conversazione | Identificatore della conversazione. Utilizzala in Compositore per aprire la trascrizione completa |
| URL della pagina | Pagina in cui si è verificato il coinvolgimento |
| Creato | Quando è stata creata la conversazione |
| Durata | Durata della conversazione |

>[!NOTE]
>
>Alcuni attributi su questo tipo di attività, compresi gli argomenti discussi, il riepilogo e la lingua, sono pianificati per una versione futura.

### Pianifica riunione nel Concierge {#schedule-meeting}

Effettuato due volte per una singola prenotazione, il che consente di separare l’intento dal risultato.

Primo, all’avvio: il visitatore ha selezionato l’opzione per pianificare una riunione e il modulo di prenotazione è apparso. Stato riunione: `Started`.

| Attributo | Descrizione |
| --- | --- |
| Stato riunione | `Started` |
| URL della pagina | La pagina in cui il visitatore ha avviato la prenotazione |
| ID portinaio | Il portinaio con cui il visitatore si è fidanzato |
| ID persona | Il record persona [!DNL Marketo] |

Poi, al momento della prenotazione: il visitatore ha confermato uno slot. Stato riunione: `Scheduled`.

| Attributo | Descrizione |
| --- | --- |
| Stato riunione | `Scheduled` |
| Nome rappresentante commerciale | Il rappresentante con cui è stata prenotata la riunione |
| E-mail rappresentante | Indirizzo e-mail del rappresentante |
| Pianificato per | Data e ora della riunione |
| Durata riunione | Durata della riunione prenotata |
| Tipo di indirizzamento | Tipo di ciclo di produzione che ha selezionato questo rappresentante |
| URL della pagina | La pagina in cui il visitatore ha prenotato |
| ID portinaio | Il portinaio con cui il visitatore si è fidanzato |
| ID persona | Il record persona [!DNL Marketo] |

>[!TIP]
>
>Creare un elenco avanzato di persone il cui `Meeting Status` è `Started` ma non `Scheduled` per trovare tutti coloro che hanno iniziato a prenotare una riunione e l&#39;hanno abbandonata. Si tratta di un pubblico già pronto per l’apprendimento o il retargeting.

### Coinvolgi la chat in diretta in Concierge {#engage-with-live-chat}

Registrato al termine di una chat in diretta.

| Attributo | Descrizione |
| --- | --- |
| Stato conversazione | `Ended` se la chat è stata chiusa deliberatamente, `Dropped` se il visitatore ha lasciato il sito e la chat è scaduta |
| Agenti notificati | Gli indirizzi e-mail di ogni rappresentante a cui è stata notificata questa chat |
| Punteggio conversazione | Il punteggio da 0 a 3 assegnato dal rappresentante alla conversazione. Vedi [Punteggio della conversazione](chat-inbox.md#conversation-score) |
| URL della pagina | Pagina in cui è stata avviata la chat in tempo reale |
| ID portinaio | Il portinaio con cui il visitatore si è fidanzato |
| ID sessione | Identificatore della sessione di chat in tempo reale |
| Ora di inizio | Quando è iniziata la chat |

>[!TIP]
>
>Il punteggio di conversazione è l&#39;attributo con il valore più alto in questo caso, perché è stato impostato da un utente che ha effettivamente parlato con il visitatore. Utilizzala per il punteggio dei lead, il retargeting, la personalizzazione e il trasferimento a vendite e gestione delle relazioni con i clienti.

## Utilizzare i dati di concierge in una campagna avanzata {#smart-campaign}

In **[!UICONTROL Elenco avanzato]** di una campagna avanzata, cerca `concierge` per visualizzare tutto ciò che è disponibile.

![Elenco avanzato di Marketo che mostra i trigger e i filtri di portineria disponibili per l&#39;attività di Brand Concierge](../assets/sales-handoff-marketo-3.png){width="800" zoomable="yes"}

| Categoria | Elementi disponibili |
| --- | --- |
| **[!UICONTROL Triggers]** | Coinvolge il Concierge, Coinvolge con chat in diretta nel Concierge, Pianifica riunioni nel Concierge |
| **[!UICONTROL Filtri]** > **[!UICONTROL Cronologia attività]** | Coinvolto con il Concierge, Coinvolto con chat in diretta nel Concierge, Riunione programmata nel Concierge |
| **[!UICONTROL Filtri]** > **[!UICONTROL Filtri di inattività]** | Non coinvolto con il portinaio, non coinvolto con chat in diretta nel portinaio, non pianificato nella riunione nel portinaio |

Trascina un trigger o un filtro nell&#39;area di lavoro, quindi seleziona **[!UICONTROL Aggiungi vincolo]** per restringerlo.

### Vincoli {#constraints}

| Attivazione o filtro | Vincoli |
| --- | --- |
| Coinvolto con il portinaio | Nome del portinaio, URL della pagina, Data di creazione, Durata, Data di attività |
| Riunione programmata in Concierge | Nome concierge, Nome rappresentante commerciale, Stato riunione, Pianificato, Durata riunione, Tipo di instradamento, URL pagina, Data attività |
| Coinvolto con chat in diretta in Concierge | Nome del portinaio, Nome del rappresentante commerciale, Stato della conversazione, Punteggio di conversazione, Ora di inizio, Ora accettata, Ora di fine, Chiuso da, Durata, Argomento discusso, URL della pagina, Lingua, Data dell&#39;attività |

## Passaggio successivo {#next}

Controlla le prestazioni delle riunioni e delle chat in [Monitora le riunioni e le chat in diretta](monitor.md).
