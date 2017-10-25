---
title: Werkstroomberichten instellen | Microsoft Docs
description: In veel werkstroomantwoorden wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren. De gebeurtenis in een werkstroomstap kan bijvoorbeeld zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 3, die een gerelateerde bewerking van de goedgekeurde record start. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 222056cc8b505d0ed027492d764ff4cde7f68795
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-workflow-notifications"></a>Werkstroomberichten instellen
In veel werkstroomantwoorden wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren. De gebeurtenis in een werkstroomstap kan bijvoorbeeld zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 3, die een gerelateerde bewerking van de goedgekeurde record start. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

> [!NOTE]  
>  De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt berichten als e-mail en als interne opmerking.  

> [!IMPORTANT]  
>  Alle werkstroomberichten worden verzonden via een taakwachtrij. Zorg ervoor dat de verwerkingswachtrij in uw oplossing. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

U stelt verschillende aspecten van werkstroomberichten op de volgende plaatsen in:  

1.  Voor goedkeuringswerkstromen kunt u de ontvangers van werkstroomberichten instellen door in het venster **Gebruikersinstellingen voor goedkeuring** een regel in te vullen voor elke gebruiker die deelneemt aan de werkstroom. Als bijvoorbeeld Gebruiker 2 wordt opgegeven in het veld **Fiatteur-id** op de regel voor Gebruiker 1, wordt het bericht over de goedkeuringsaanvraag verzonden naar Gebruiker 1. Zie voor meer informatie [Procedure: Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  
2.  U stelt in wanneer en hoe gebruikers werkstroomberichten ontvangen door het venster **Berichtplanning** in te vullen voor elke werkstroomgebruiker. Zie voor meer informatie [Procedure: Vastleggen wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  U stelt de algemene inhoud en opmaak van berichten in, inclusief berichten over achterstallige werkstroomantwoorden, door berichtsjablonen in te stellen in het venster **Berichtsjablonen**. U kunt de standaardsjablonen gebruiken die worden geleverd bij [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4.  U stelt specifieke inhoud en regels van een werkstroombericht in als u de betreffende werkstroom maakt. U doet dit door opties te selecteren in het **Opties werkstroomreactie** voor het werkstroomantwoord dat het bericht representeert. Zie voor meer informatie stap 9 in [Procedure: Werkstromen maken](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Zie ook  
 [Procedure: Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
 [Procedure: Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)   
 [Procedure: Vastleggen wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Procedure: Werkstromen maken](across-how-to-create-workflows.md)   
 [Procedure: Berichtsjablonen beheren](across-how-to-manage-notification-templates.md)   
 [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md)   
 [Procedure: E-mail instellen](madeira-how-setup-email.md)   
 [Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Werkstroom](across-workflow.md)   

