---
title: Werkstroomberichten instellen
description: In dit artikel wordt uitgelegd hoe u werkstroommeldingen instelt om een gebruiker te waarschuwen dat er een gebeurtenis is opgetreden waarop hij of zij moet reageren; een werkstroomreactie is vereist.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9405af9c52b17ab34fded263692e3294ed8aaf11
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533980"
---
# <a name="workflow-notifications"></a>Werkstroomberichten

Stel uw workflows zo in dat gebruikers automatisch op de hoogte worden gesteld wanneer hun aandacht vereist is voor een stap in die workflow. In veel werkstroomreacties wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren.

U kunt bijvoorbeeld instellen dat gebruiker 2, de goedkeurder, een melding ontvangt wanneer gebruiker 1 goedkeuring vraagt voor een nieuwe record. Bij de volgende werkstroomstap krijgt gebruiker 3 een melding nadat gebruiker 2 de record heeft goedgekeurd om een gerelateerde verwerking van de record te starten. Bij goedkeuringswerkstroomstappen is elk bericht gekoppeld aan een goedkeuringspost. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

> [!NOTE]  
> De standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt berichten als e-mail en als interne opmerking.  

> [!IMPORTANT]  
> Alle werkstroomberichten worden verzonden via een taakwachtrij. Zorg dat de taakwachtrij in uw installatie is ingesteld om werkstroomberichten te verwerken en dat het selectievakje **Automatisch starten van server** is ingeschakeld. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Berichten instellen

U kunt verschillende aspecten van werkstroomberichten op de volgende plaatsen instellen:  

* Bericht van fiatteur

    Voor goedkeuringswerkstromen kunt u de ontvangers van werkstroomberichten instellen door op de pagina **Gebruikersinstellingen voor goedkeuring** een regel in te vullen voor elke gebruiker die deelneemt aan de werkstroom.  

    Als bijvoorbeeld Gebruiker 2 wordt opgegeven in het veld **Fiatteur-id** op de regel voor Gebruiker 1, wordt het bericht over de goedkeuringsaanvraag verzonden naar Gebruiker 2. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  
* Berichtplanningen

    U stelt in wanneer en hoe gebruikers werkstroomberichten ontvangen door de pagina **Berichtplanning** in te vullen voor elke werkstroomgebruiker. Zie voor meer informatie [Vastleggen wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* De e-mailberichten aanpassen

    Als u wilt, kunt u de inhoud van het e-mailbericht wijzigen door rapport 1320, Berichte-mail te wijzigen. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Als u e-mail wilt gebruiken als meldingsmethode, moet u e-mail instellen voor zowel de afzender als de ontvanger in [!INCLUDE [prod_short](includes/prod_short.md)]. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

* Reactieopties

    U stelt specifieke inhoud en regels van een werkstroombericht in als u de betreffende werkstroom maakt. Selecteer de aanpassingsopties op de pagina **Werkstroomreacties** voor de werkstroomreactie die het bericht representeert. Zie voor meer informatie stap 9 in [Werkstromen maken](across-how-to-create-workflows.md#to-create-a-workflow).  

* Afzender informeren

    Voeg voor goedkeuringswerkstromen een werkstroomreactiestap toe om de afzender te informeren wanneer het verzoek is goedgekeurd of afgewezen. Zie voor meer informatie stap 9 in [Werkstromen maken](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/create-workflows/)

## <a name="see-also"></a>Zie ook

[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)  
[Opgeven wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Werkstromen maken](across-how-to-create-workflows.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[E-mail instellen](admin-how-setup-email.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
