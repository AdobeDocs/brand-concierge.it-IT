---
title: Analizzare le prestazioni del concierge
description: Scopri come rivedere le analisi di consulenza, esaminare le trascrizioni delle conversazioni, aggiungere domande ai visitatori dei set di valutazione e aprire i rapporti di Customer Journey Analytics.
hide: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---


# Analizzare le prestazioni del concierge

**Persone per:** addetti al marketing che utilizzano l&#39;esperienza self-service. Dopo l’implementazione della portineria non è richiesta alcuna configurazione.

**Cadenza consigliata:** Rivedere le analisi in base alle esigenze. Il check-in settimanale è un punto di partenza ragionevole.

Analytics consente di comprendere in che modo i visitatori interagiscono con un portinaio in tempo reale. Dopo la distribuzione, la scheda **Analytics** visualizza automaticamente le metriche di conversazione e fornisce l&#39;accesso alle singole trascrizioni e a un report Customer Journey Analytics più dettagliato.

## Visualizza analisi

1. Apri il portinaio e seleziona la scheda **Analytics**.

1. Impostare l&#39;intervallo di date per il periodo che si desidera esaminare.

1. Facoltativamente, filtra i risultati per tipo di conversazione.

La scheda Analytics visualizza automaticamente le metriche seguenti:

| Metrica | Descrizione |
|---|---|
| Conversazioni | Il numero di conversazioni durante il periodo selezionato. |
| Visitatori coinvolti | Il numero di visitatori che si sono impegnati con il portinaio. |
| Sentiment positivo | La quantità di sentiment positivo identificato nelle conversazioni. |
| Messaggi per conversazione | Numero medio di messaggi scambiati in una conversazione. |

>[!NOTE]
>
>Non è richiesta alcuna configurazione per visualizzare queste metriche dopo la distribuzione della portineria.

## Revisione delle trascrizioni di conversazione

Le trascrizioni delle conversazioni ti consentono di esaminare cosa hanno chiesto i visitatori e come ha risposto il portinaio.

1. Nella scheda Analytics, seleziona una conversazione.

1. Leggi la trascrizione completa.

1. Controlla se i visitatori hanno selezionato una valutazione in alto o in basso per le singole risposte.

Ogni conversazione ha un ID di conversazione univoco. Utilizza questo ID per far corrispondere la trascrizione con i record di altri sistemi quando l’implementazione supporta tale flusso di lavoro.

### Aggiungere una conversazione a un set di valutazione

Se un visitatore fa una domanda utile per test futuri, aggiungila direttamente a un set di valutazione dalla trascrizione.

1. Apri la trascrizione della conversazione.

1. Selezionare **Aggiungi a valutazione**.

L’aggiunta di domande vere dei visitatori consente di mantenere i set di valutazione basati sulle domande che i visitatori pongono. Per ulteriori informazioni sui set di valutazione, vedere [Valutare un portinaio](../evaluation/evaluation.md).

>[!TIP]
>
>Rivedi le trascrizioni regolarmente e aggiungi domande rappresentative, non solo quelle che hanno ricevuto feedback negativi, per contribuire a mantenere un set di valutazione equilibrato.

## Apri il rapporto Customer Journey Analytics

Seleziona **Visualizza report** per aprire una dashboard più dettagliata in Adobe Customer Journey Analytics (CJA). Il provisioning del dashboard viene eseguito automaticamente e non richiede una configurazione aggiuntiva.

Il dashboard di CJA include:

- Tendenze di conversazione settimanale.
- Coinvolgimento ripetuto, comprese le conversazioni per persona.
- Messaggi per conversazione.
- Tendenze di feedback dei visitatori.
- Intento del visitatore.
- Sentiment e tono del visitatore.
- Raccomandazioni del portiere fatte durante le conversazioni.

Utilizza la dashboard per esaminare le tendenze nel tempo e identificare i cambiamenti nel coinvolgimento, nel feedback, nell’intento e nel sentiment dei visitatori.

## Esporta conversazioni

Il materiale sorgente identifica l’ID della conversazione come un modo per far corrispondere le trascrizioni con i record di altri sistemi, ma non documenta un meccanismo di esportazione.

>[!IMPORTANT]
>
>Non trattare gli ID conversazione come un flusso di lavoro di esportazione. Prima di documentare come esportare conversazioni o trascrizioni, è necessaria una procedura dettagliata dedicata del prodotto o del team ingegneristico.
