---
title: 'Procedure: Werkstroomgebruikers instellen| Microsoft Docs'
description: Voordat u werkstromen kunt maken, moet u de gebruikers instellen die deelnemen aan werkstromen. Dit is nodig om bijvoorbeeld op te geven wie een bericht ontvangt als er moet worden gereageerd op een werkstroomstap.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 06/08/2020
ms.author: edupont
ms.openlocfilehash: f632518f4fa7f0be4e919a1de7427e205c0f1921
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782022"
---
# <a name="set-up-workflow-users"></a>Werkstroomgebruikers instellen

Voordat u werkstromen kunt maken, moet u de gebruikers instellen die deelnemen aan werkstromen. Dit is nodig om bijvoorbeeld op te geven wie een bericht ontvangt als er moet worden gereageerd op een werkstroomstap.  

Op de pagina **Werkstroomgebruikersgroep** stelt u gebruikers in onder werkstroomgebruikersgroepen en geeft u het nummer van de gebruikers op in een procesvolgorde, zoals een fiatteringsketen.  

Werkstroomgebruikers die fungeren als goedkeuringgebruikers, zowel aanvragers als fiatteurs, moeten ook worden ingesteld op de pagina **Gebruikersinstellingen voor goedkeuring**. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Stel een hiërarchie voor fiatteurs op om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd totdat meerdere fiatteurs in een goedkeuringsketen deze hebben goedgekeurd. Voor het fiatteurstype **Fiatteur** stelt u fiatteurs op de pagina **Gebruikersinstellingen voor goedkeuring** in. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** op de pagina **Werkstroomgebruikersgroepen** in en definieer de hiërarchie door incrementele nummers aan elke fiatteur in het veld **Volgnr.** veld. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md) en de volgende sectie.  
>
> U kunt definiëren dat een goedkeuringsaanvraag pas wordt goedgekeurd nadat meerdere gelijkwaardige fiatteurs deze hebben goedgekeurd, ongeacht het bestaan van een hiërarchie, door een werkstroomgebruikersgroep in een platte structuur in te stellen. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** op de pagina **Werkstroomgebruikersgroepen** in en wijs hetzelfde nummer toe aan elke fiatteur in het **Volgnr.** veld. Zie de volgende onderwerpen voor meer informatie.  

## <a name="to-set-up-a-workflow-user"></a>Een werkstroomgebruiker instellen

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstroomgebruikersgroepen** in en kies de desbetreffende koppeling.  
2. Kies de actie **Nieuw**. De pagina **Werkstroomgebruikersgroep** wordt geopend.  
3. Voer in het veld **Code** maximaal 20 tekens in om de werkstroom te identificeren.  
4. Beschrijf de werkstroom in het veld **Omschrijving**.  
5. Vul in het sneltabblad **Werkstroomgebruikersgroepsleden** de velden op de eerste regel in, zoals in de volgende tabel is beschreven.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Gebruikersnaam**|Geef de gebruiker op die deelneemt aan werkstromen.<br /><br /> De gebruiker moet op de pagina **Gebruikersinstellingen** bestaan. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.|  
    |**Volgnr.**|Geef de volgorde waarin de werkstroomgebruiker deelneemt aan een werkstroom in verband met andere gebruikers. Dit veld kan bijvoorbeeld worden gebruikt om aan te geven wanneer de gebruiker in verhouding tot andere fiatteurs goedkeurt, als u de optie **Werkstroomgebruikersgroep** in het veld **Soort fiatteur** voor het gerelateerde werkstroomantwoord gebruikt. **TIP:** stel een vaste werkstroomgebruikersgroep in door hetzelfde volgordenummer aan de relevante fiatteurs toe te kennen om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd alvorens deze door meerdere gelijkwaardige fiatteurs is goedgekeurd, ongeacht of sprake is van een hiërarchie.|  
6. Herhaal stap 5 om meer werkstroomgebruikers aan de gebruikersgroep toe te voegen.  
7. Herhaal stap 2 tot en met 6 om werkstroomgebruikersgroepen toe te voegen.  

## <a name="see-also"></a>Zie ook

[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Werkstromen instellen](across-set-up-workflows.md)  
[Werkstromen gebruiken](across-use-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  
