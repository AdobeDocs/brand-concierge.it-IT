---
title: Creare un ruolo con l’autorizzazione di Brand Concierge
description: Scopri come creare un ruolo e concedergli l’autorizzazione necessaria per accedere a Brand Concierge.
source-git-commit: 591bd1600e586a0a4ce484dbff3f9fb97e24d43d
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# Creare un ruolo con l’autorizzazione di Brand Concierge

Crea un ruolo nelle Autorizzazioni di Adobe Experience Platform per consentire agli utenti di accedere a Brand Concierge.

## Prerequisiti

* Per gestire ruoli e autorizzazioni è necessario disporre delle autorizzazioni di amministratore necessarie.
* L’utente deve prima essere aggiunto all’organizzazione Adobe Experience Platform. Per ulteriori informazioni, consulta &quot;Aggiungere un utente all’organizzazione&quot; (LINK).

## Creare il ruolo

1. Accedi a `experienceplatform.adobe.com`.

   >[!NOTE]
   >
   >Conferma l’URL di produzione con il team di progettazione prima di pubblicare questa procedura. La registrazione sorgente utilizzava un URL informale o probabilmente trascritto in modo errato.

2. Nel menu di navigazione a sinistra, scorri fino a e seleziona **Autorizzazioni**.
3. Seleziona **Ruoli** per visualizzare i ruoli esistenti, quindi seleziona **Crea un nuovo ruolo**.
4. Immettere un nome per il ruolo, ad esempio `Brand Concierge Access Users`, aggiungere una descrizione e confermare la creazione.
5. Apri il nuovo ruolo e assegna le autorizzazioni:

   1. Cerca nell&#39;elenco di autorizzazioni **Brand Concierge**.
   2. Selezionare **Gestisci Brand Concierge**.

   Attualmente, **Gestisci Brand Concierge** è l&#39;unica autorizzazione di Brand Concierge disponibile. I livelli di autorizzazione granulari non sono attualmente disponibili.

6. Seleziona la sandbox o le sandbox a cui il ruolo può accedere.

   Un’organizzazione può contenere più sandbox, che sono aree di lavoro isolate. Seleziona solo le sandbox appropriate per questo ruolo.

7. Seleziona **Salva**.

## Passaggi successivi

Dopo aver creato il ruolo, aggiungi gli utenti. Per ulteriori informazioni, consulta &quot;Aggiungere utenti al ruolo&quot; (COLLEGAMENTO).

## Considerazioni correlate

* Il processo di creazione e gestione delle sandbox esula dall’ambito di questa procedura.
* Prima di definire un modello di ruolo a lungo termine, verifica se sono pianificate ulteriori autorizzazioni granulari per Brand Concierge.
