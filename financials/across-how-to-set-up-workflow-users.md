---
title: 'Procedure: Werkstroomgebruikers instellen| Microsoft Docs'
description: Voordat u werkstromen kunt maken, moet u de gebruikers instellen die deelnemen aan werkstromen. Dit is nodig om bijvoorbeeld op te geven wie een bericht ontvangt als er moet worden gereageerd op een werkstroomstap.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 929cce642a6adccc493c1ce9947ac60662b261d5
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-workflow-users"></a>Procedure: Werkstroomgebruikers instellen
Voordat u werkstromen kunt maken, moet u de gebruikers instellen die deelnemen aan werkstromen. Dit is nodig om bijvoorbeeld op te geven wie een bericht ontvangt als er moet worden gereageerd op een werkstroomstap.  

In het venster **Werkstroomgebruikersgroep** stelt u gebruikers in onder werkstroomgebruikersgroepen en geeft u het nummer van de gebruikers op in een procesvolgorde, zoals een fiatteringsketen.  

Werkstroomgebruikers die fungeren als goedkeuringgebruikers, zowel aanvragers als fiatteurs, moeten ook worden ingesteld in het venster **Gebruikersinstellingen voor goedkeuring**. Zie voor meer informatie [Procedure: Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
>  Stel een hiërarchie voor fiatteurs op om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd totdat meerdere fiatteurs in een goedkeuringsketen deze hebben goedgekeurd. Voor het fiatteurstype **Fiatteur** stelt u fiatteurs in het venster **Gebruikersinstellingen voor goedkeuring** in. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** in het venster **Werkstroomgebruikersgroepen** in en definieer de hiërarchie door incrementele nummers toe te wijzen aan elke fiatteur in het **Volgnr.** te kiezen. Zie dit onderwerp en [Procedure: Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md) voor meer informatie.  
>   
>  U kunt definiëren dat een goedkeuringsaanvraag pas wordt goedgekeurd nadat meerdere gelijkwaardige fiatteurs deze hebben goedgekeurd, ongeacht het bestaan van een hiërarchie, door een werkstroomgebruikersgroep in een platte structuur in te stellen. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** in het venster **Werkstroomgebruikersgroepen** in en wijs hetzelfde nummer toe aan elke fiatteur in het **Volgnr.** te kiezen. Zie dit onderwerp voor meer informatie.  

### <a name="to-set-up-a-workflow-user"></a>Een werkstroomgebruiker instellen  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Werkstroomgebruikersgroepen** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Het venster **Werkstroomgebruikersgroep** wordt geopend.  
3. Voer in het veld **Code** maximaal 20 tekens in om de werkstroom te identificeren.  
4. Beschrijf de werkstroom in het veld **Omschrijving**.  
5. Vul in het sneltabblad **Werkstroomgebruikersgroepsleden** de velden op de eerste regel in, zoals in de volgende tabel is beschreven.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Gebruikersnaam**|Geef de gebruiker op die deelneemt aan werkstromen.<br /><br /> De gebruiker moet in het venster **Gebruikersinstellingen** bestaan. Zie [Procedure: Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.|  
    |**Volgnr.**|Geef de volgorde waarin de werkstroomgebruiker deelneemt aan een werkstroom in verband met andere gebruikers. Dit veld kan bijvoorbeeld worden gebruikt om aan te geven wanneer de gebruiker in verhouding tot andere fiatteurs goedkeurt, als u de optie **Werkstroomgebruikersgroep** in het veld **Approver Type** voor het gerelateerde werkstroomantwoord gebruikt. **TIP:** stel een vaste werkstroomgebruikersgroep in door hetzelfde volgordenummer aan de relevante fiatteurs toe te kennen om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd alvorens deze door meerdere gelijkwaardige fiatteurs is goedgekeurd, ongeacht of sprake is van een hiërarchie.|  
6. Herhaal stap 5 om meer werkstroomgebruikers aan de gebruikersgroep toe te voegen.  
7. Herhaal stap 2 tot en met 6 om werkstroomgebruikersgroepen toe te voegen.  

## <a name="see-also"></a>Zie ook  
[Procedure: Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
[Werkstromen instellen](across-set-up-workflows.md)   
[Werkstromen gebruiken](across-use-workflows.md)   
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Werkstroom](across-workflow.md)   

