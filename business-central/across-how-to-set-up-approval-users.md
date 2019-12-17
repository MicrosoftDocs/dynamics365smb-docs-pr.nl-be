---
title: 'Procedure: Goedkeuringsgebruikers instellen| Microsoft Docs'
description: Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. Op de pagina Gebruikersinstellingen voor goedkeuring kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ab35f8f37490852be98d6c3e8a2cf30b2202764a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881108"
---
# <a name="set-up-approval-users"></a>Goedkeuringsgebruikers instellen
Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. Op de pagina **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.  

> [!NOTE]  
>  Goedkeuringsgebruikers, zowel aanvragers als fiatteurs, moeten eerst worden ingesteld als werkstroomgebruikers op de pagina **Werkstroomgebruikersgroep**. Zie [Werkstromen instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  

 Als u gebruikers van de goedkeuringsgebruikers hebt ingesteld, kunt u de instellingen gebruiken om werkstroomantwoorden te maken voor goedkeuringswerkstromen. Zie voor meer informatie stap 9 in [Werkstromen maken](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Stel een hiërarchie voor fiatteurs op om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd totdat meerdere fiatteurs in een goedkeuringsketen deze hebben goedgekeurd. Voor het fiatteurstype **Fiatteur** stelt u fiatteurs op de pagina **Gebruikersinstellingen voor goedkeuring** in. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** op de pagina **Werkstroomgebruikersgroepen** in en definieer de hiërarchie door incrementele nummers aan elke fiatteur in het veld **Volgnr.** invoeren. Zie dit onderwerp en [Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  
>   
>  U kunt definiëren dat een goedkeuringsaanvraag pas wordt goedgekeurd nadat meerdere gelijkwaardige fiatteurs deze hebben goedgekeurd, ongeacht het bestaan van een hiërarchie, door een werkstroomgebruikersgroep in een platte structuur in te stellen. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** op de pagina **Werkstroomgebruikersgroepen** in en wijs hetzelfde nummer toe aan elke fiatteur in het **Volgnr.** invoeren. Zie [Werkstromen instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  

## <a name="to-set-up-an-approval-user"></a>Een goedkeuringsgebruiker instellen  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies de gerelateerde koppeling.  
2. Maak een nieuwe regel op de pagina **Gebruikersinstellingen voor goedkeuring** en vul de velden in zoals is beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Gebruikers-ID**|Selecteer de gebruikers-id van de gebruiker die is betrokken bij het goedkeuringsproces.|  
    |**Verkoper/inkoper**|Geef de verkopers- of inkoperscode op die op de gebruiker van toepassing is, in het veld **Verkoper/Inkoper**.<br /><br /> U vult het veld **Verkoper/Inkoper** meestal in als de verkoper of inkoper die verantwoordelijk is voor de klant of leverancier, ook de persoon is die de betreffende verkoop- of inkoopaanvraag moet goedkeuren.|  
    |**Fiatteur-id**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-ID**.|  
    |**Limiet voor goedkeuring verkoopbedrag**|Geef het maximale verkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-ID** kan goedkeuren.|  
    |**Onbeperkte goedkeuring van verkopen**|Geef aan dat de gebruiker in het veld **Gebruikers-ID** alle verkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|  
    |**Limiet voor goedkeuring inkoopbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-ID** kan goedkeuren.|  
    |**Onbeperkte goedkeuring van inkopen**|Geef aan dat de gebruiker in het veld **Gebruikers-ID** alle inkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|  
    |**Limiet voor goedkeuring aanvraagbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-ID** kan goedkeuren voor inkoopoffertes.<br /><br /> Als u dit veld wilt gebruiken, moet u de optie **Fiatteursketting** selecteren in het veld **Limietsoort van fiatteur** op de pagina **Werkstroomreactie**.|  
    |**Onbeperkt aanvragen van goedkeuring**|Geef aan dat de gebruiker in het veld **Gebruikers-ID** alle inkoopoffertes kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring aanvraagbedrag** niet invullen.|  
    |**Vervanger**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-ID** als de gebruiker in **Fiatteur-id** niet beschikbaar is. **Opmerking:** de vervanger kan de gebruiker in het veld **Vervanger**, de directe fiatteur of de goedkeuringsbeheerder zijn, in die volgorde van prioriteit. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).|  
    |**E-mailadres**|Geef het e-mailadres op van de gebruiker in het veld **Gebruikers-ID**.|  
    |**Beheerder goedkeuringssysteem**|Geef de gebruiker op die rechten heeft om werkstromen voor goedkeuring te deblokkeren, bijvoorbeeld door goedkeuringsaanvragen te delegeren naar nieuwe vervangende fiatteurs en door vervallen goedkeuringsaanvragen te verwijderen.|

    > [!Note]
    > Er kan maar één persoon goedkeuringsbeheerder zijn.|  

3. Kies de actie **Gebruikersinstellingen goedkeuring testen** om de instelling van gebruikers in het goedkeuringsproces te testen.  
4. Herhaal stap 2 en 3 voor elke gebruiker die u wilt instellen als goedkeuringsgebruiker.  

## <a name="see-also"></a>Zie ook  
[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)   
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)   
[Werkstromen maken](across-how-to-create-workflows.md)   
[Werkstromen instellen](across-set-up-workflows.md)   
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Werkstroom](across-workflow.md)   
