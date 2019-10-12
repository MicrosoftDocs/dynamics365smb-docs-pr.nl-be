---
title: Werkstroomberichten instellen | Microsoft Docs
description: In veel werkstroomantwoorden wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren. De gebeurtenis in een werkstroomstap kan bijvoorbeeld zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 3, die een gerelateerde bewerking van de goedgekeurde record start. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cab856000763e351046c4a81e8da6149c11e3c71
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308318"
---
# <a name="setting-up-workflow-notifications"></a>Werkstroomberichten instellen
In veel werkstroomantwoorden wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren. De gebeurtenis in een werkstroomstap kan bijvoorbeeld zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 3, die een gerelateerde bewerking van de goedgekeurde record start. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

> [!NOTE]  
>  De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt berichten als e-mail en als interne opmerking.  

> [!IMPORTANT]  
>  Alle werkstroomberichten worden verzonden via een taakwachtrij. Zorg dat de taakwachtrij in uw installatie is ingesteld om werkstroomberichten te verwerken en dat het selectievakje **Automatisch starten van server** is ingeschakeld. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

U stelt verschillende aspecten van werkstroomberichten op de volgende plaatsen in:  

1.  Voor goedkeuringswerkstromen kunt u de ontvangers van werkstroomberichten instellen door op de pagina **Gebruikersinstellingen voor goedkeuring** een regel in te vullen voor elke gebruiker die deelneemt aan de werkstroom. Als bijvoorbeeld Gebruiker 2 wordt opgegeven in het veld **Fiatteur-id** op de regel voor Gebruiker 1, wordt het bericht over de goedkeuringsaanvraag verzonden naar Gebruiker 1. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  
2.  U stelt in wanneer en hoe gebruikers werkstroomberichten ontvangen door de pagina **Berichtplanning** in te vullen voor elke werkstroomgebruiker. Zie voor meer informatie [Vastleggen wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Als u wilt, kunt u de inhoud van het e-mailbericht wijzigen door rapport 1320, Berichte-mail te wijzigen. Zie voor meer informatie [Een aangepaste lay-out voor een rapport of document maken en wijzigen](ui-how-create-custom-report-layout.md).  
4.  U stelt specifieke inhoud en regels van een werkstroombericht in als u de betreffende werkstroom maakt. U doet dit door opties te selecteren op de pagina **Opties werkstroomreactie** voor het werkstroomantwoord dat het bericht representeert. Zie voor meer informatie stap 9 in [Werkstromen maken](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Zie ook  
 [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
 [Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)   
 [Opgeven wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Werkstromen maken](across-how-to-create-workflows.md)   
 [Een aangepaste lay-out voor een rapport of document maken en wijzigen](ui-how-create-custom-report-layout.md)   
 [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)   
 [E-mail instellen](admin-how-setup-email.md)   
 [Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Werkstroom](across-workflow.md)   
