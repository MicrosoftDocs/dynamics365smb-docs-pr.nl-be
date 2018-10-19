---
title: 'Procedure: Vastleggen wanneer en hoe gebruikers berichten ontvangen | Microsoft Docs'
description: Wanneer u gebruikers in goedkeuringswerkstromen instelt, moet u in de vensters Berichtinstellingen en Berichtplanning opgeven hoe en wanneer iedere gebruiker berichten ontvangt over stappen in de goedkeuringswerkstroom. Individuele gebruikers kunnen hun berichtinstellingen ook wijzigen door de knop Berichtinstellingen wijzigen op een bericht te kiezen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 714ebd289407293f2a9fb8f05cad68330c79ad9a
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="specify-when-and-how-to-receive-notifications"></a>Opgeven wanneer en hoe gebruikers berichten ontvangen
Wanneer u gebruikers in goedkeuringswerkstromen instelt, moet u in de vensters **Berichtinstellingen** en **Berichtplanning** opgeven hoe en wanneer iedere gebruiker berichten ontvangt over stappen in de goedkeuringswerkstroom. Individuele gebruikers kunnen hun berichtinstellingen ook wijzigen door de knop **Berichtinstellingen wijzigen** op een bericht te kiezen.  

 Voordat u voorkeuren voor gebruikersberichten over goedkeuring kunt instellen, moet u de gebruiker als goedkeuringsgebruiker instellen. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  

 U definieert de lay-out en inhoud van berichten door berichtsjablonen in te stellen. Zie voor meer informatie [Berichtsjablonen beheren](across-how-to-manage-notification-templates.md).  

 In veel goedkeuringswerkstroomstappen wordt aan gebruikers gemeld dat er een gebeurtenis is opgetreden waarop ze moeten reageren. Bijvoorbeeld, de gebeurtenis in een werkstroomstap kan zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 3 om een proces te starten met de goedgekeurde record. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

## <a name="specify-when-and-how-users-receive-notifications"></a>Vastleggen wanneer en hoe gebruikers berichten ontvangen  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de regel voor de gebruiker voor wie u berichtvoorkeuren wilt instellen. Kies vervolgens de actie **Berichtinstellingen**.  
3.  Vul in het venster **Berichtinstellingen** de velden in, zoals is beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Berichttype**|Geef het soort gebeurtenis aan waarop het bericht betrekking heeft.<br /><br /> Selecteer een van de volgende opties:<br /><br /> -   **Nieuwe record** geeft aan dat het bericht betrekking heeft op een nieuwe record, zoals een document, waarop de gebruiker moet reageren.<br />-   **Goedkeuring** geeft aan dat het bericht betrekking heeft op een of meer goedkeuringsaanvragen.<br />-   **Vervallen** geeft aan dat het bericht wordt gebruikt om gebruikers eraan te herinneren dat ze te laat zijn met reageren op een gebeurtenis.|  
    |**Berichtsjabloon**|Geef de code aan van de berichtsjabloon die wordt gebruikt om berichten te maken voor de gebruiker.|  
    |**Niet-geaggregeerde berichten**|Geef aan of de gebruiker één bericht ontvangt voor elke gebeurtenis of geaggregeerde berichten.<br /><br /> Als het selectievakje **Niet-geaggregeerde berichten** niet is ingeschakeld, krijgt de gebruiker berichten met informatie over alle gebeurtenissen die plaatsvinden met hetzelfde herhalingspatroon in de berichtplanning.|  

     U hebt nu opgegeven hoe de gebruiker berichten ontvangt. U kunt nu opgeven wanneer de gebruiker berichten ontvangt.  

4.  Kies de actie **Berichtplanning**.  
5.  Vul in het venster **Berichtplanning** de velden in, zoals is beschreven in de volgende tabel.  

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
2.  In het venster **Berichtinstellingen** wijzigt u de berichtvoorkeuren zoals beschreven in de vorige procedure.  

## <a name="see-also"></a>Zie ook  
 [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
 [Berichtsjablonen beheren](across-how-to-manage-notification-templates.md)   
 [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)   
 [Werkstromen instellen](across-set-up-workflows.md)   
 [Werkstromen gebruiken](across-use-workflows.md)

