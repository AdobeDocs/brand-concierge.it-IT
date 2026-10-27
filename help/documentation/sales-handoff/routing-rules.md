---
title: Inoltra conversazioni ai rappresentanti
description: Scegli in che modo Brand Concierge decide quale rappresentante commerciale ricevere una chat in diretta o una prenotazione di riunioni, utilizzando round robin, un agente diretto o regole di instradamento personalizzate.
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
source-wordcount: '771'
ht-degree: 0%
---
# Inoltra le conversazioni ai rappresentanti {#routing}

Il routing risponde a una domanda: quando il visitatore richiede una persona, *quale* persona riceve?

È possibile scegliere separatamente un tipo di routing per l&#39;integrazione **[!UICONTROL Meeting Booking]** e **[!UICONTROL Live Chat]**, in modo che un addetto possa distribuire le riunioni in modo uniforme inviando ogni chat a uno specialista o a qualsiasi altra combinazione.

## Tipi di instradamento {#routing-types}

| Tipo di indirizzamento | Chi riceve la conversazione | Richiede [!DNL Marketo Engage] |
| --- | --- | --- |
| **[!UICONTROL Round robin]** | Distribuito tra tutti i rappresentanti idonei | No |
| **[!UICONTROL Agente diretto]** | Nome di un rappresentante | No |
| **[!UICONTROL Routing personalizzato]** | I rappresentanti assegnati alla regola di indirizzamento con priorità più alta per la quale il visitatore si qualifica | Sì |

Round robin è disponibile per impostazione predefinita e non richiede alcuna configurazione. È possibile impostare il tipo di ciclo sull&#39;integrazione stessa. Consulta [Attivare la prenotazione di chat e riunioni in tempo reale](configure-in-composer.md).

### Round robin {#round-robin}

Round robin si comporta in modo diverso per le riunioni che per le chat, perché i due hanno obiettivi diversi.

Per la prenotazione delle riunioni, round robin distribuisce le riunioni in modo uniforme. Il primo rappresentante idoneo che ha connesso un calendario viene offerto per primo. Una volta prenotato un incontro con loro, vengono estratti dalla piscina e viene offerto il rappresentante successivo. Con cinque rappresentanti, i primi cinque incontri si svolgono con cinque persone diverse. Dopo che tutti ne hanno ricevuto uno, il pool si ripristina e il ciclo riparte.

Il pool viene inoltre reimpostato ogni 24 ore, in modo che le riunioni di ogni giorno vengano distribuite in modo uniforme.

>[!NOTE]
>
>Il ripristino round robin di 24 ore viene eseguito su UTC, non sul fuso orario locale del rappresentante.

Per la chat in diretta, non esiste una rotazione sequenziale. Ogni rappresentante idoneo riceve contemporaneamente la notifica della chat in arrivo e il primo ad accettare prende la conversazione.

### Agente diretto {#direct-agent}

Ogni riunione o chat di questo concierge va al singolo rappresentante selezionato. Utilizza questa opzione per una pagina di destinazione della campagna di proprietà di un dirigente account o per un’area geografica con un esperto.

### Routing personalizzato {#custom-routing}

Il routing personalizzato valuta le regole create in [!DNL Adobe Marketo Qualifier] in base agli attributi del lead [!DNL Marketo] del visitatore e dell&#39;azienda. Utilizzalo quando il rappresentante giusto dipende da qualcosa che sai sul visitatore, ad esempio:

* Geografia: i visitatori di diversi paesi si rivolgono al team regionale.
* Interesse del prodotto: i visitatori interessati a un prodotto specifico vanno dagli specialisti di quel prodotto.
* Business unit, dimensione dell&#39;azienda o settore: qualsiasi combinazione di lead e attributi aziendali.

>[!IMPORTANT]
>
>Il routing personalizzato è l&#39;unica parte della prenotazione di chat e riunioni in tempo reale che richiede [!DNL Adobe Marketo Engage], perché le regole sono basate sugli attributi del lead e della società [!DNL Marketo]. Round robin e direct agent lavorano senza di esso.

## Creare una regola di routing personalizzata {#create-rule}

1. In [!DNL Adobe Marketo Qualifier], in **[!UICONTROL Amministrazione]**, selezionare **[!UICONTROL Regole di routing]**.

   L’elenco mostra ogni regola dell’organizzazione con la relativa priorità, nome, autore e data di creazione.

   ![Pagina Regole di instradamento in cui sono elencate le regole esistenti con Priorità, Nome, Creato da e Creato nelle colonne](../assets/sales-handoff-routing-1.png){width="800" zoomable="yes"}

1. Seleziona **[!UICONTROL Crea regola]** e assegna un nome alla regola.

1. Genera i criteri.

   Nel pannello a sinistra sono elencati gli attributi [!DNL Marketo] disponibili dagli oggetti **[!UICONTROL Company]** e **[!UICONTROL Lead]** (person). Cerca un attributo, quindi trascinalo sull’area di lavoro per aggiungere una condizione.

1. Imposta un operatore e un valore per ogni condizione.

   Gli operatori includono **[!UICONTROL equals]**, **[!UICONTROL does not equal]** e **[!UICONTROL contains]**, tra gli altri. `Country` **[!UICONTROL è uguale a]** `United States`.

1. Combinare le condizioni in gruppi.

   Aggiungi diverse condizioni a un gruppo e aggiungili con **[!UICONTROL AND]** o **[!UICONTROL OR]**. Aggiungi altri gruppi e unisciti ai gruppi anche con **[!UICONTROL AND]** o **[!UICONTROL OR]**. La nidificazione delle condizioni all&#39;interno dei gruppi consente di esprimere criteri complessi, ad esempio *(il paese è Stati Uniti O Canada) AND (il prodotto interessato contiene Analytics)*.

1. Assegna la regola ai rappresentanti.

   Nella sezione delle assegnazioni, cerca un rappresentante per nome e selezionalo dall’elenco. Aggiungi tutti i rappresentanti desiderati. Ognuno di loro può ricevere una conversazione che corrisponde alla regola.

1. Seleziona **[!UICONTROL Salva]**.

## Come viene applicata la priorità {#priority}

Ogni regola di routing ha una priorità. La priorità è importante solo quando un visitatore è idoneo per più di una regola.

In questo caso, viene applicata solo la regola di corrispondenza con priorità più elevata e la conversazione viene instradata ai rappresentanti assegnati a tale regola. Vengono ignorate anche le regole per le quali il visitatore è idoneo, ma che sono di livello inferiore.

>[!NOTE]
>
>Un numero più basso indica una priorità più alta. Una regola con priorità 1 prevale su una regola con priorità 2. La persona che crea una regola imposta la propria priorità.

All’interno della regola vincente, i rappresentanti a essa assegnati sono il pool idoneo e il comportamento round robin per le riunioni e il comportamento notification-Everyone per le chat, entrambi descritti in precedenza, si applicano a tale pool.

## Passaggio successivo {#next}

Con la configurazione e l’instradamento decisi dai rappresentanti, aggiungi le funzionalità a un portinaio. Consulta [Attivare la prenotazione di chat e riunioni in tempo reale](configure-in-composer.md).
