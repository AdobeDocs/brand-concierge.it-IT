---
title: Creare un ruolo con l’autorizzazione di Brand Concierge
description: Scopri come creare un ruolo e concedergli l’autorizzazione necessaria per accedere a Brand Concierge.
source-git-commit: 60835c7971d86341194d773f9cf487c4cb6f171a
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---


# Creare un ruolo con l’autorizzazione di Brand Concierge

Crea un ruolo nelle Autorizzazioni di Adobe Experience Platform per consentire agli utenti di accedere a Brand Concierge.

>[!PREREQUISITES]
>
>- Per gestire ruoli e autorizzazioni è necessario disporre delle autorizzazioni di amministratore necessarie.
>- L’utente deve prima essere aggiunto all’organizzazione Adobe Experience Platform. Per ulteriori informazioni, vedere [Aggiungere un utente all&#39;organizzazione](./add-a-user-to-the-org.md).

## Creare il ruolo

1. Accedi a `experienceplatform.adobe.com`.

1. Nel menu di navigazione a sinistra, scorri fino a e seleziona **Autorizzazioni**.
1. Vai a **Ruoli** per visualizzare i ruoli esistenti e seleziona **Crea un nuovo ruolo**.
1. Immettere un nome per il ruolo, ad esempio `Brand Concierge Access Users`, aggiungere una descrizione e confermare la creazione.
1. Apri il nuovo ruolo e assegna le autorizzazioni:

   1. Cerca nell&#39;elenco di autorizzazioni **Brand Concierge**.
   1. Selezionare **Gestisci Brand Concierge**.

   Al momento, **Gestisci Brand Concierge** è l&#39;unica autorizzazione Brand Concierge disponibile; i livelli di autorizzazione granulari non sono ancora disponibili.

1. Seleziona la sandbox o le sandbox a cui il ruolo può accedere.

   Un’organizzazione può contenere più sandbox, che sono aree di lavoro isolate. Seleziona solo le sandbox appropriate per questo ruolo.

1. Seleziona **Salva**.

## Passaggi successivi

Dopo aver creato il ruolo, aggiungi gli utenti. Per ulteriori informazioni, vedere [Aggiungere utenti al ruolo Brand Concierge](./add-a-user-to-the-role.md).
