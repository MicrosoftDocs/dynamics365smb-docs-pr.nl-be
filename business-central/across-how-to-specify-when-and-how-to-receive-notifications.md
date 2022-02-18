---
title: Opgeven wanneer en hoe gebruikers werkstroomberichten ontvangen
description: Wanneer u gebruikers instelt in goedkeuringswerkstromen, kunt u specificeren hoe en wanneer elke goedkeuringsgebruiker berichten ontvangt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 6812fa270066b03fa64a7d8c664ef4df8d28eff0
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102511"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Opgeven wanneer en hoe gebruikers werkstroomberichten ontvangen
Wanneer u goedkeuringsgebruikers instelt in werkstromen waarin u wilt dat iemand wijzigingen goedkeurt, zoals wanneer nieuwe records worden gemaakt of wanneer iemand om goedkeuring vraagt, moet u specificeren hoe en wanneer de goedkeuringsgebruiker op de hoogte wordt gesteld. U kunt bijvoorbeeld opgeven dat een goedkeuringsgebruiker onmiddellijk een e-mail ontvangt wanneer iemand een nieuwe klant aanmaakt. Als alternatief kunt u plannen dat de berichten bijvoorbeeld wekelijks of maandelijks worden bezorgd.

Gebruikers kunnen hun berichtinstellingen ook wijzigen door de knop **Berichtinstellingen wijzigen** voor een bericht te kiezen.  

> [!NOTE]
> Berichten worden afgeleverd volgens de berichtinstellingen voor de ontvanger, niet de afzender. Dat is een belangrijk onderscheid, omdat het betekent dat wanneer iemand een goedkeuring aanvraagt als onderdeel van een werkstroom, zijn of haar verzoek niet noodzakelijkerwijs onmiddellijk wordt verzonden. In plaats daarvan wordt het afgeleverd volgens het meldingsschema dat is opgegeven in de meldingsinstellingen van de goedkeurder. 

Voordat u voorkeuren voor gebruikersberichten over goedkeuring kunt instellen, moet u de gebruiker als goedkeuringsgebruiker instellen. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  

U kunt de indeling van e-mailberichten bepalen door Rapport 1320, Berichte-mail aan te passen. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).  

> [!NOTE]
> Als u e-mail wilt gebruiken als meldingsmethode, moet u e-mail instellen voor zowel de afzender als de ontvanger in [!INCLUDE [prod_short](includes/prod_short.md)]. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

## <a name="steps-in-workflows"></a>Stappen in werkstromen 
In veel goedkeuringswerkstroomstappen wordt aan gebruikers gemeld dat er een gebeurtenis is opgetreden waarop ze moeten reageren. Bijvoorbeeld, de gebeurtenis in een werkstroomstap kan zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 3 om een proces te starten met de goedgekeurde record. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

## <a name="specify-when-and-how-users-receive-notifications"></a>Vastleggen wanneer en hoe gebruikers berichten ontvangen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de regel voor de gebruiker voor wie u berichtvoorkeuren wilt instellen. Kies vervolgens de actie **Berichtinstellingen**.  
3.  Vul op de pagina **Berichtinstellingen** de velden in, zoals is beschreven in de volgende tabel.  

    > [!NOTE]
    > Als u de pagina **Berichtinstellingen** opent vanaf de pagina **Gebruikersinstellingen voor goedkeuring**, wordt de berichtinstelling gekoppeld aan de goedkeuringsgebruiker. De goedkeuringsgebruiker ontvangt altijd werkstroomberichten volgens die berichtconfiguratie. Als u Vertel me gebruikt om de pagina **Berichtinstellingen** te openen, is de berichtinstelling van toepassing op alle gebruikers.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Berichttype**|Geef het soort gebeurtenis aan waarop het bericht betrekking heeft.<br /><br /> Selecteer een van de volgende opties:<br /><br /> -   **Nieuwe record** geeft aan dat het bericht betrekking heeft op een nieuwe record, zoals een document, waarop de gebruiker moet reageren.<br />-   **Goedkeuring** geeft aan dat het bericht betrekking heeft op een of meer goedkeuringsaanvragen.<br />-   **Vervallen** geeft aan dat het bericht wordt gebruikt om gebruikers eraan te herinneren dat ze te laat zijn met reageren op een gebeurtenis.|  
    |**Berichtmethode**|Geef aan of het bericht wordt verzonden als interne opmerking.|

    U kunt de lay-out van e-mailberichten bepalen door Rapport 1320, Berichte-mail aan te passen. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

    U hebt nu opgegeven hoe de gebruiker berichten ontvangt. U kunt nu opgeven wanneer de gebruiker berichten ontvangt.  

4.  Kies de actie **Berichtplanning**.  
5.  Vul op de pagina **Berichtplanning** de velden in, zoals is beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Herhaling**|Geef het herhalingspatroon op waarin de gebruiker berichten ontvangt.|  
    |**Tijd**|Hiermee wordt opgegeven op welk moment van de dag de gebruiker berichten ontvangt wanneer de waarde in het veld **Periodiek** niet **Meteen** is.|  
    |**Dagelijkse frequentie**|Geef aan op welke soort dag de gebruiker berichten ontvangt als de waarde in het veld **Herhaling** **Dagelijks** is.<br /><br /> Selecteer **Werkdag** om berichten te ontvangen op elke werkdag van de week. Selecteer **Dagelijks** om berichten te ontvangen op elke dag van de week, inclusief weekends.|  
    |**Maandag** tot en met **zondag**|Geef aan op welke soort dag de gebruiker berichten ontvangt als de waarde in het veld **Herhaling** **Wekelijks** is.|  
    |**Datum van maand**|Geef aan of de gebruiker berichten ontvangt op de eerste, laatste of een bepaalde dag van de maand.|  
    |**Datum maandelijks bericht**|Geef de dag van de maand aan waarop de gebruiker berichten ontvangt als de waarde in het veld **Datum van maand** **Aangepast** is.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Wijzigen wanneer en hoe gebruikers berichten ontvangen  
1.  Kies in een van de berichten die u hebt ontvangen, hetzij als e-mail hetzij als opmerking, de knop **Berichtinstellingen wijzigen**.  
2.  Op de pagina **Berichtinstellingen** wijzigt u de berichtvoorkeuren zoals beschreven in de vorige procedure.  

## <a name="see-also"></a>Zie ook  
 [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
 [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)   
 [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)   
 [Werkstromen instellen](across-set-up-workflows.md)   
 [Werkstromen gebruiken](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]