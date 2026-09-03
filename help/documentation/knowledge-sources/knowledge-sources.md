---
title: Creazione e gestione di origini di conoscenza per Brand Concierge
description: Scopri come creare AEM Sites, collegamenti a siti web e origini di conoscenza del catalogo dei prodotti per Brand Concierge, monitorare lo stato di elaborazione e risolvere i problemi di scansiona.
hide: true
source-git-commit: da4b30fa292b911987aebec378af420b293ea594
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 1%

---


# Creazione e gestione di origini di conoscenza per Brand Concierge

Un’origine di conoscenza è il contenuto che un concierge può utilizzare per rispondere alle domande dei visitatori. Ogni portinaio richiede almeno una sorgente di conoscenza configurata. Le fonti di conoscenza sono create in modo indipendente e possono essere riutilizzate in più concierge.

Un concierge risponde alle domande utilizzando solo le origini di conoscenza configurate. Non risponde alla conoscenza generale del mondo.

>[!NOTE]
>
>Se un visitatore chiede informazioni al di fuori delle origini di conoscenza configurate, il portinaio è progettato per indicare che non dispone delle informazioni, anziché generare una risposta non supportata. Utilizza il processo di valutazione per verificare questo comportamento.

## Scegli un&#39;origine di conoscenza

| Sorgente della conoscenza | Utilizzala quando | Funzionalità principale |
| --- | --- | --- |
| AEM Sites (indice IA per la gestione dei contenuti) | Il cliente utilizza AEM Sites as a Cloud Service con IA per la gestione dei contenuti abilitata. | Utilizza un indice IA per la gestione dei contenuti esistente e rende disponibili i contenuti aggiornati di AEM Sites senza un passaggio di scansiona o aggiornamento separato. |
| Collegamenti al sito Web | Il cliente deve scansionare un sito web, indipendentemente dalla piattaforma utilizzata per crearlo. | Scansiona una mappa del sito, singoli URL selezionati o URL forniti in un file CSV. |
| Catalogo prodotti | Il cliente dispone di un catalogo di prodotti o servizi relativamente piccolo e non utilizza Adobe Commerce. | Abilita i collegamenti profondi del prodotto e le schede del prodotto nelle risposte del portiere. |

>[!IMPORTANT]
>
>Il materiale di base sottolinea che i clienti che vendono tramite Adobe Commerce con un catalogo di grandi dimensioni devono utilizzare l’integrazione MCP di Commerce. I dettagli su tale integrazione esulano dall’ambito di questo articolo.

## Creare un’origine delle conoscenze AEM Sites

Utilizza un’origine di conoscenza AEM Sites quando il cliente utilizza già AEM Sites as a Cloud Service con IA per la gestione dei contenuti abilitata.

1. Selezionare **Genera Knowledge Source**.
1. Scegli **AEM Sites** e seleziona **Continua**.
1. Immettere un nome e una descrizione per l&#39;origine della conoscenza. Utilizzare ad esempio `My main website` come nome.
1. Seleziona un indice di IA per la gestione dei contenuti esistente dall’elenco. L’elenco viene compilato dall’istanza as a Cloud Service di AEM Sites.
1. Seleziona **Salva**.

Questa integrazione nativa rende automaticamente disponibili a Brand Concierge i contenuti AEM Sites aggiornati. Non è necessario un passaggio separato di scansiona o aggiornamento.

## Creare un’origine di conoscenza dei collegamenti al sito web

Utilizza un&#39;origine di conoscenza Collegamenti a un sito Web per la ricerca per indicizzazione. Questa opzione funziona per i siti web basati su qualsiasi piattaforma ed è consigliata per la maggior parte degli utenti alle prime esperienze.

1. Selezionare **Genera Knowledge Source**.
1. Scegli **Collegamenti sito Web** e seleziona **Continua**.
1. Immettere un nome per l&#39;origine della conoscenza.
1. Aggiungere le origini di contenuto utilizzando uno dei metodi seguenti:

   - **URL mappa del sito:** Aggiungere un URL che elenca le pagine del sito. Vengono scansionate tutte le pagine elencate nella mappa del sito.
   - **URL singoli:** Aggiungere URL di pagina specifici uno alla volta. Vengono scansionate solo le pagine aggiunte.
   - **Caricamento CSV:** Scarica il file di esempio, aggiungi gli URL e carica il file CSV completato.

1. (Facoltativo) Pianificare una frequenza di aggiornamento, ad esempio settimanale in un giorno e in un&#39;ora specifici, per mantenere aggiornata la fonte di conoscenza con le modifiche apportate al sito Web.
1. Seleziona **Aggiungi** o **Crea**.

Il sistema scansiona gli URL specificati e ne esegue il scraping del contenuto per creare l&#39;origine della conoscenza.

>[!TIP]
>
>In genere, una mappa del sito è disponibile in `yourwebsite.com/sitemap.xml`. Se il sito web non fornisce una mappa del sito, aggiungi i singoli URL della pagina.

## Creare un’origine delle conoscenze del catalogo dei prodotti

Utilizza un’origine di conoscenza del catalogo dei prodotti per i clienti con un set più piccolo di prodotti o servizi, circa meno di 100, che non utilizzano Adobe Commerce.

Quando una risposta del concierge fa riferimento a un prodotto, il catalogo dei prodotti può fornire un collegamento diretto alla pagina del prodotto e abilitare una scheda del prodotto. Una scheda prodotto può includere un&#39;immagine, un titolo, una descrizione e uno o due pulsanti.

1. Selezionare **Genera Knowledge Source**.
1. Scegli **Catalogo prodotti** e seleziona **Continua**.
1. Immettere un nome per l&#39;origine della conoscenza. Utilizzare ad esempio `My product catalog - US region` come nome.
1. Seleziona uno schema. Lo schema definisce quali campi di prodotto (come immagine, titolo, descrizione e pulsanti) vengono visualizzati e dove si collegano i pulsanti.
1. Scarica il foglio di calcolo di esempio per lo schema selezionato.
1. Aggiungi i dati del prodotto al foglio di calcolo e caricalo.
1. Seleziona **Salva**.

Configurazioni di pulsanti diverse richiedono schemi diversi.

## Monitorare lo stato dell&#39;origine della conoscenza

Ogni origine dati visualizza uno stato di elaborazione.

| Stato | Significato |
| --- | --- |
| In corso | L&#39;origine della conoscenza è in fase di elaborazione. |
| Completato | L&#39;origine delle informazioni è completamente elaborata e pronta per l&#39;uso. |
| Pianificato | L&#39;origine della conoscenza verrà elaborata in un orario pianificato futuro. |
| Completato parzialmente | Alcune pagine sono state elaborate correttamente e altre non sono riuscite. |

La pagina dei dettagli dell&#39;origine dati fornisce informazioni quali:

- Il creatore.
- La data di creazione.
- Il numero di collegamenti o pagine forniti.
- Numero di collegamenti o pagine completati o non riusciti.
- Ora ultimo aggiornamento.
- Gli URL considerati per l’elaborazione.

## Risoluzione dei problemi di elaborazione

Se un&#39;origine di conoscenza mostra uno stato di successo parziale, utilizzare il report del problema per identificare gli URL che non è stato possibile elaborare.

1. Aprire la pagina dei dettagli della Knowledge Base.
1. Seleziona **Correggi problemi** per scaricare un file contenente URL interrotti o che non è stato possibile eliminare, insieme ai relativi dettagli dell&#39;errore.
1. Correggi gli URL non validi o rimuovili dall’elenco di origine.
1. Se applicabile, carica nuovamente l’elenco URL corretto.
1. Richiedi la rielaborazione in modo che il contenuto corretto venga aggiunto all’origine della conoscenza.
