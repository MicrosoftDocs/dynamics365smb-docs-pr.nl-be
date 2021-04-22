---
title: 'Procedure: Vastleggen wanneer en hoe gebruikers berichten ontvangen | Microsoft Docs'
description: Wanneer u gebruikers in goedkeuringswerkstromen instelt, moet u op de pagina's Berichtinstellingen en Berichtplanning opgeven hoe en wanneer iedere gebruiker berichten ontvangt over stappen in de goedkeuringswerkstroom. Individuele gebruikers kunnen hun berichtinstellingen ook wijzigen door de knop Berichtinstellingen wijzigen op een bericht te kiezen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d96d094547b71fc722c06facb80a131786df0e58
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774623"
---
# <a name="specify-when-and-how-to-receive-notifications"></a>Opgeven wanneer en hoe gebruikers berichten ontvangen
Wanneer u gebruikers in goedkeuringswerkstromen instelt, moet u op de pagina's **Berichtinstellingen** en **Berichtplanning** opgeven hoe en wanneer iedere gebruiker berichten ontvangt over stappen in de goedkeuringswerkstroom. Individuele gebruikers kunnen hun berichtinstellingen ook wijzigen door de knop **Berichtinstellingen wijzigen** op een bericht te kiezen.  

> [!NOTE]
> Berichten worden afgeleverd volgens de berichtinstellingen voor de ontvanger, niet de afzender. Dat is een belangrijk onderscheid, omdat het betekent dat wanneer iemand een goedkeuring aanvraagt als onderdeel van een werkstroom, zijn of haar verzoek niet noodzakelijkerwijs onmiddellijk wordt verzonden. In plaats daarvan wordt het afgeleverd volgens de berichtinstellingen van de goedkeurders. 

 Voordat u voorkeuren voor gebruikersberichten over goedkeuring kunt instellen, moet u de gebruiker als goedkeuringsgebruiker instellen. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  

 U kunt de indeling van e-mailberichten bepalen door Rapport 1320, Berichte-mail aan te passen. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).  

 In veel goedkeuringswerkstroomstappen wordt aan gebruikers gemeld dat er een gebeurtenis is opgetreden waarop ze moeten reageren. Bijvoorbeeld, de gebeurtenis in een werkstroomstap kan zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 3 om een proces te starten met de goedgekeurde record. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

## <a name="specify-when-and-how-users-receive-notifications"></a>Vastleggen wanneer en hoe gebruikers berichten ontvangen  

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies de gerelateerde koppeling.  
2.  Selecteer de regel voor de gebruiker voor wie u berichtvoorkeuren wilt instellen. Kies vervolgens de actie **Berichtinstellingen**.  
3.  Vul op de pagina **Berichtinstellingen** de velden in, zoals is beschreven in de volgende tabel.  

    |Veld|Description|  
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