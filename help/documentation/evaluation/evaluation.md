---
title: Valuta un portinaio
description: Scopri come creare set di valutazione ed eseguire valutazioni funzionali, fuori ambito e di salvaguardia per valutare l’accuratezza e la sicurezza delle risposte di un concierge.
hide: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---


# Valuta un portinaio

**Persone per:** addetti al marketing che utilizzano l&#39;esperienza self-service. Non è richiesta alcuna assistenza IT.

**Tempo richiesto:** Alcuni minuti per creare un set di valutazione. L’esecuzione di una valutazione richiede più tempo a seconda delle dimensioni del set.

Le valutazioni consentono di stabilire con sicurezza che le risposte del portinaio sono accurate prima che il portinaio venga esaminato da chiunque non faccia parte del team diretto. A differenza dei test ad hoc nell’esperienza di anteprima, le valutazioni forniscono un modo ripetibile di misurare le risposte rispetto alle risposte previste.

## Tipi di valutazione

Le valutazioni si dividono in tre categorie:

| Tipo | Scopo |
|---|---|
| Funzionale | Consente di controllare le risposte alle normali domande relative ai prodotti o ai servizi. |
| Fuori ambito | Controlla in che modo il portinaio gestisce le domande a cui non deve rispondere ma che non sono dannose, come domande su un concorrente o un argomento non correlato. |
| Protezione | Controlla il modo in cui il portinaio gestisce gli input dannosi o avversari, inclusi le domande trick, la volgarità e i tentativi di manipolarli. |

## Creare un set di valutazione

Un set di valutazione, detto anche *set di dati dorato* o *verità*, è un elenco di domande di esempio associate alle risposte considerate corrette. Le risposte effettive del concierge vengono confrontate con le risposte attese durante una valutazione.

### Creare un set di valutazione

1. Denomina il set di valutazione. Ad esempio, `About my products`.

1. Scegliere la modalità di creazione del set:

   * **Generato da IA:** Il Compositore legge l&#39;origine della conoscenza e crea un elenco di domande probabili e risposte previste da rivedere.
   * **Caricamento manuale o foglio di calcolo:** Fornisci direttamente un elenco di domande e risposte.

1. Se si sta creando un set generato dall&#39;intelligenza artificiale, assicurarsi che l&#39;origine della conoscenza sia completamente configurata prima di generare il set. Il Compositore utilizza la fonte di conoscenza per redigere le domande e le risposte.

1. Rivedi ogni coppia domanda-risposta generata:

   * Modificare una risposta per modificarne la formulazione.
   * Eliminare una domanda non rilevante.

1. Se necessario, scarica il set come foglio di calcolo per la revisione da parte di un collega. Dopo la revisione, carica di nuovo il foglio di calcolo.

>[!TIP]
>
>I set di valutazione generati dall’intelligenza artificiale sono bozze basate sull’origine delle conoscenze. Rivedi e correggili nello stesso modo in cui rivedi il profilo del marchio e le istruzioni durante la creazione del portinaio.

## Eseguire una valutazione

1. Selezionare **Esegui valutazione**.

1. Selezionare il set di valutazione da eseguire, quindi selezionare **Esegui**.

1. Attendere mentre al portinaio viene posta ogni domanda del set. Le risposte effettive del concierge vengono confrontate con le risposte attese.

   Il tempo di elaborazione aumenta con il numero di domande nel set. L’avanzamento viene visualizzato come percentuale.

1. Al termine dell’elaborazione, controlla il punteggio complessivo e il numero di risposte contrassegnate.

Le risposte contrassegnate sono risposte potenzialmente problematiche che possono richiedere un&#39;ulteriore revisione.

## Rivedere i risultati della valutazione

**I risultati della valutazione** vengono visualizzati ogni esecuzione passata per un set di valutazione, in modo da poter tenere traccia dei risultati nel tempo.

Per esaminare un&#39;esecuzione:

1. Aprire un&#39;esecuzione di valutazione da **Risultati valutazione**.

1. Rivedi ogni domanda insieme alla risposta effettiva del concierge e alla risposta prevista.

1. Rivedi la valutazione assegnata a ciascun risultato. I risultati ricevono una valutazione **alta**, **media** o **bassa** e includono una nota che spiega il ragionamento. Ad esempio, un risultato potrebbe essere contrassegnato come **necessita di attenzione** con un motivo per la valutazione.

1. Rivedi le risposte contrassegnate direttamente per concentrarti su risultati potenzialmente problematici senza leggere ogni risultato nell’esecuzione.

## Best practice

* Configurare completamente l’origine della conoscenza prima di generare un set di valutazione basato sull’intelligenza artificiale. Il contenuto sorgente più completo produce domande di bozza migliori.
* Creare almeno un set di valutazione ridotto per ogni tipo di valutazione: funzionale, fuori ambito e di salvaguardia. Ogni tipo rileva una diversa classe di problema.
* Riesegui le valutazioni dopo qualsiasi modifica significativa della configurazione, incluse modifiche a istruzioni, guardrail, abilità o integrazioni. Considera le valutazioni come una pratica corrente anziché come un gate occasionale.
* Aggiungi le domande dei visitatori reali da Analytics a un set di valutazione quando rivelano un gap che vale la pena testare.
