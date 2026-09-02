---
title: Distribuire un portinaio
description: Scopri come distribuire un Brand Concierge configurando un flusso di dati, installando lo script di distribuzione, definendo le regole di superficie e verificando la distribuzione.
hide: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Distribuire un portinaio

L’implementazione rende un portinaio disponibile ai visitatori reali del sito web. L’addetto al marketing configura le impostazioni di distribuzione, mentre il team IT o di analisi fornisce l’ID dello stream di dati e il team del sito web installa lo script di distribuzione sul sito web.

L’implementazione è in genere una configurazione breve e una tantum per ogni sito. Pianifica per circa 15 minuti dal lato dell’addetto marketing, oltre al tempo necessario al team del sito web per installare lo script.

>[!IMPORTANT]
>
>Coinvolgi il team IT o di analisi e il team del sito web in anticipo. La loro partecipazione è necessaria per fornire l’ID dello stream di dati e installare lo script, pertanto la distribuzione non deve essere trattata come passaggio finale dell’implementazione.

## Prima di iniziare

- Coordinati con il team IT o di analisi per ottenere un ID dello stream di dati.
- Identifica il team responsabile del sito web o del gestore di tag. Questo articolo fa riferimento a questo gruppo come al team del sito web.
- Decidi se il portinaio deve apparire come un componente nelle pagine esistenti o come una pagina dedicata completa.
- Identifica i domini e i percorsi delle pagine in cui deve apparire il portinaio.

## Configurare lo stream di dati

Un flusso di dati è la destinazione dei dati di attività generati dalle interazioni del visitatore con il portiere. Esempi di queste interazioni includono clic, invio di moduli, riunioni prenotate e chat in tempo reale. Lo stream di dati consente di visualizzare questa attività in Analytics in un secondo momento.

Non è necessario creare un flusso di dati come parte di questa procedura. È necessario solo il relativo ID.

### Ottenere l’ID dello stream di dati

Chiedi al team IT o di analisi l’ID dello stream di dati. L&#39;ID si trova in Adobe Experience Platform in **Raccolta dati** > **Flussi dati**.

### Aggiungere la configurazione dello stream di dati

1. Assicurati che l’ID dello stream di dati sia pronto.
1. Nella sezione Distribuzione di Brand Concierge selezionare **Aggiungi configurazione**.
1. Incolla l’ID dello stream di dati.
1. Salva la configurazione.
1. Dopo aver salvato la configurazione, seleziona l’opzione di installazione appropriata:
   - **Installazione componente:** Utilizzare uno snippet inserito dal team del sito Web in una posizione specifica del sito Web.
   - **Installazione a pagina intera:** Utilizza una pagina completa e pronta per l&#39;hosting per una pagina di destinazione dedicata del portinaio.
1. Fornisci lo script o la pagina selezionata al team del sito web.
1. Chiedi al team del sito web di installare lo script direttamente nel codice della pagina o tramite un gestore di tag.

>[!NOTE]
>
>L’installazione viene generalmente gestita dal team del sito web, in modo simile all’aggiunta di un tag di analisi o di strumento di chat.

## Configurare la superficie

Una volta installato lo script, la configurazione della superficie controlla le pagine in cui viene visualizzato il portiere. Ad esempio, puoi configurare la portineria in modo che venga visualizzata nelle pagine dei prodotti ma non in una pagina di carriere.

### Aggiungere un dominio e le regole di pagina

1. Aggiungere un dominio, ad esempio `blog.example.com`.
1. Scegli come devono corrispondere i percorsi sul dominio. I pattern di corrispondenza disponibili includono:
   - Qualsiasi pagina sotto il dominio.
   - Percorsi che iniziano con un valore specificato.
   - Percorsi che terminano con un valore specificato.
   - Corrispondenza esatta del percorso.
1. Combina più regole per definire una copertura pagina più precisa.
1. Salvate la configurazione della superficie.

## Verificare la distribuzione

Dopo che il team del sito Web ha installato lo script e le regole di superficie sono state salvate, verifica che:

- Lo script è presente nelle pagine del sito web previste.
- Il portinaio viene visualizzato solo sulle pagine coperte dalle regole configurate.
- Il portinaio non viene visualizzato sulle pagine escluse.
- Le interazioni dei visitatori generano dati di attività per lo stream di dati configurato.

>[!TIP]
>
>Esegui il test sia di una pagina inclusa che di una pagina esclusa. Ciò conferma che le regole di superficie funzionano come previsto prima che il portinaio sia reso ampiamente disponibile.

## Domande aperte e note sull&#39;ambito

Il materiale di origine non definisce i seguenti dettagli:

- Elenco canonico completo dei tipi di evento inviati allo stream di dati. Gli esempi forniti includono clic, invio di moduli, riunioni prenotate e chat in tempo reale, ma l’elenco completo deve essere confermato con l’assistenza tecnica.
- Se la configurazione del flusso di dati differisce tra i clienti di prova e quelli a pagamento.
- In quale prodotto di analisi specifico viene visualizzata l’attività dello stream di dati; il materiale sorgente si riferisce a questo solo come &quot;Analytics&quot;.

Queste domande possono sovrapporsi a requisiti di telemetria separati e devono essere risolte con il team di progettazione o di prodotto appropriato prima di pubblicare le linee guida per la distribuzione come riferimento definitivo.

## Contenuto sorgente incompleto

L&#39;origine fornita termina improvvisamente al punto 8, che non ha contenuto.
