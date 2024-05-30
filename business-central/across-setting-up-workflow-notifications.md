---
title: Goedkeuringswerkstroomberichten instellen
description: In dit artikel wordt uitgelegd hoe u werkstroommeldingen instelt om een gebruiker te waarschuwen dat er een gebeurtenis is opgetreden waarop hij of zij moet reageren; een werkstroomreactie is vereist.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Berichten van goedkeuringswerkstromen

Stel uw werkstromen zo in dat gebruikers automatisch op de hoogte worden gesteld wanneer hun aandacht vereist is voor een stap in een werkstroom. In veel werkstroomreacties wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren.

U kunt bijvoorbeeld instellen dat gebruiker 2, de fiatteur, een melding ontvangt wanneer gebruiker 1 goedkeuring vraagt voor een nieuwe record. Bij de volgende werkstroomstap krijgt gebruiker 2 een melding nadat gebruiker 3 is geïnformeerd en een gerelateerde verwerking van de record kan starten. Bij goedkeuringswerkstroomstappen is elk bericht gekoppeld aan een goedkeuringspost. Zie voor meer informatie [Werkstroom](across-workflow.md).  

> [!NOTE]  
> De standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt berichten in e-mail of als interne opmerkingen.  

> [!IMPORTANT]  
> Alle werkstroomberichten worden verzonden via een taakwachtrij. Zorg dat de taakwachtrij in uw installatie is ingesteld om werkstroomberichten te verwerken en dat u het selectievakje **Automatisch starten van server** hebt ingeschakeld. Zie voor meer informatie [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).

## Berichten instellen

U kunt verschillende aspecten van werkstroomberichten op de volgende plaatsen instellen:  

* Bericht van fiatteur

  Voor goedkeuringswerkstromen kunt u de ontvangers van werkstroomberichten instellen door op de pagina **Gebruikersinstellingen voor goedkeuring** een regel in te vullen voor elke gebruiker die deelneemt aan de werkstroom.  

  Als bijvoorbeeld Gebruiker 2 wordt opgegeven in het veld **Fiatteur-id** op de regel voor Gebruiker 1, wordt het bericht over de goedkeuringsaanvraag verzonden naar Gebruiker 2. Meer informatie op [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md). 
  
* Berichtplanningen

  Stel in wanneer en hoe gebruikers werkstroomberichten ontvangen door de pagina **Berichtplanning** in te vullen voor elke werkstroomgebruiker. Meer informatie op [Opgeven wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* De e-mailberichten aanpassen

  Als u wilt, kunt u de inhoud van het e-mailbericht wijzigen door rapport 1320, Berichte-mail te wijzigen. U vindt meer informatie op [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Als u e-mail wilt gebruiken als meldingsmethode, moet u e-mail instellen voor zowel de afzender als de ontvanger in [!INCLUDE [prod_short](includes/prod_short.md)]. Meer informatie op [E-mail instellen](admin-how-setup-email.md).
  
* Reactieopties

  Stel specifieke inhoud en regels van een werkstroombericht in als u de betreffende werkstroom maakt. Selecteer de aanpassingsopties op de pagina **Werkstroomreacties** voor de werkstroomreactie die het bericht representeert. Lees meer vanaf stap 9 in de sectie [Werkstromen maken](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Afzender informeren

  Voeg voor goedkeuringswerkstromen een werkstroomreactiestap toe om de afzender te informeren wanneer het verzoek is goedgekeurd of afgewezen. Lees meer vanaf stap 9 in de sectie [Werkstromen maken](across-how-to-create-workflows.md#to-create-a-workflow).   

## Zie ook

[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)  
[Opgeven wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Goedkeuringswerkstromen maken](across-how-to-create-workflows.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[E-mail instellen](admin-how-setup-email.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
