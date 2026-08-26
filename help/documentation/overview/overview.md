---
title: Panoramica di Brand Concierge
description: Scopri Brand Concierge, come si combinano i suoi componenti principali e il glossario dei termini chiave che incontrerai nell’interfaccia di Composer.
source-git-commit: 3da67605a43e949046260651253bbe0f2f0215fc
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 1%

---

# Panoramica di Brand Concierge

Brand Concierge è una piattaforma dinamica che consente alle aziende e ai marchi di lanciare esperienze conversazionali personalizzate sulle superfici rivolte ai clienti: siti web, app mobili e altre proprietà digitali. Ogni conversazione si basa sui contenuti e sulle protezioni del brand, e le integrazioni permettono alle informazioni di tali conversazioni di fluire nel resto dell’ecosistema del brand, come Marketo Engage.

## Componenti principali

Un’implementazione di Brand Concierge include due parti principali:

| Pezzo | Che cos’è |
|---|---|
| **Esperienza visitatore** | La superficie rivolta al brand, ad esempio un sito web o un’app mobile, in cui i visitatori interagiscono con il concierge e ottengono risposte in tempo reale. |
| **Compositore** | L’interfaccia per professionisti utilizzata per progettare esperienze di concierge e gestire concierge, integrazioni, configurazioni, valutazioni, distribuzione e analisi. |

## Moduli di composizione trattati in questa guida

All’interno di Compositore, i moduli principali (e dove sono trattati in questa guida) sono:

- Gestione utente (sezione 3)
- Creazione e gestione di risorse di conoscenza, condivise tra le diverse conferenze (sezione 4)
- Gestione dei portinai: integrazioni, competenze, istruzioni per il portinaio, voce e tono, stile visivo e componenti chat (sezione 5)
- Valutazione (sezione 6)
- Implementazione (sezione 7)
- Elenco di controllo per il lancio (sezione 8)
- Analytics (sezione 9)

## Come si connettono i pezzi

Un’origine della conoscenza (contenuto) viene interrogata da un’integrazione (connessione), che viene chiamata da un’abilità (comportamento), il tutto racchiuso in un concierge (l’esperienza complessiva) con cui i visitatori interagiscono.

## Glossario

Questi termini vengono visualizzati nell&#39;interfaccia del Compositore.

| Termine | Definizione |
|---|---|
| **Concierge** | L’esperienza di chat di IA stessa: una per marchio, sito web o caso d’uso. Un account può avere diversi. |
| **Compositore** | L’interfaccia utilizzata per creare e gestire le conferenze, distinta da quella visualizzata dai visitatori del sito web. |
| **Origine conoscenza** | Il contenuto che un concierge può utilizzare quando risponde a domande quali pagine di siti web o un elenco di prodotti. Senza una, il portinaio non ha niente da cui rispondere. |
| **Integrazione** | Connessione a un sistema in grado di recuperare informazioni, ad esempio contenuto di un sito Web o un catalogo di prodotti live. |
| **Abilità** | Una funzionalità specifica che il concierge può eseguire, ad esempio rispondere a domande generali, confrontare prodotti o prenotare una riunione. Un’abilità utilizza una o più integrazioni per eseguire la sua funzione. |
| **Guardrail** | Regole che definiscono cosa il consulente non deve fare o discutere, come concorrenti o consulenza legale. |
| **Valutazione** | Un test strutturato costituito da domande campione abbinate alle risposte attese, utilizzato per valutare le prestazioni del concierge. |
| **ID flusso di dati** | Un identificatore tecnico che specifica dove vengono inviati i dati dell’attività del visitatore all’interno dei sistemi Adobe. Viene fornito dal team IT o di analisi. |
| **Sandbox** | Area di lavoro isolata all&#39;interno di un&#39;organizzazione. Un&#39;organizzazione può averne più di uno, ciascuno può tenere più concierge. |
| **Organizzazione IMS** | Termine utilizzato da Adobe per indicare l’account complessivo di un’organizzazione. |
| **MCP** (ad esempio, Commerce MCP) | Un connettore gestito da Adobe per un sistema specifico, ad esempio un catalogo di prodotti live, configurato utilizzando codici o chiavi forniti dal reparto IT o dal team commerce. |
| **CJA (Customer Journey Analytics)** | prodotto di analisi di Adobe. Brand Concierge esegue automaticamente il provisioning di un dashboard di avvio senza richiedere alcuna configurazione aggiuntiva. |

>[!NOTE]
>
>In genere, gli addetti al marketing possono ignorare completamente la sezione 3, *Gestione degli utenti e degli accessi* (una volta completata da un utente IT) e iniziare dalla sezione 4, *Origini della conoscenza*. Ritorna alla sezione 3 solo quando si impostano nuovi compagni di squadra.
