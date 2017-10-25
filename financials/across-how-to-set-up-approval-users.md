---
title: 'Procedure: Goedkeuringsgebruikers instellen| Microsoft Docs'
description: Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. In het venster Gebruikersinstellingen voor goedkeuring kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.
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
ms.openlocfilehash: 49ffa181e653377f3684d138b6ee7df3775a87f6
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-approval-users"></a>Procedure: Goedkeuringsgebruikers instellen
Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. In het venster **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.  

> [!NOTE]  
>  Goedkeuringsgebruikers, zowel aanvragers als fiatteurs, moeten eerst worden ingesteld als werkstroomgebruikers in het venster **Werkstroomgebruikersgroep**. Zie [Procedure: Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  

 Als u gebruikers van de goedkeuringsgebruikers hebt ingesteld, kunt u de instellingen gebruiken om werkstroomantwoorden te maken voor goedkeuringswerkstromen. Zie voor meer informatie stap 9 in [Procedure: Werkstromen maken](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Stel een hiërarchie voor fiatteurs op om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd totdat meerdere fiatteurs in een goedkeuringsketen deze hebben goedgekeurd. Voor het fiatteurstype **Fiatteur** stelt u fiatteurs in het venster **Gebruikersinstellingen voor goedkeuring** in. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** in het venster **Werkstroomgebruikersgroepen** in en definieer de hiërarchie door incrementele nummers toe te wijzen aan elke fiatteur in het **Volgnr.** veld. Zie dit onderwerp en [Procedure: Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  
>   
>  U kunt definiëren dat een goedkeuringsaanvraag pas wordt goedgekeurd nadat meerdere gelijkwaardige fiatteurs deze hebben goedgekeurd, ongeacht het bestaan van een hiërarchie, door een werkstroomgebruikersgroep in een platte structuur in te stellen. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** in het venster **Werkstroomgebruikersgroepen** in en wijs hetzelfde nummer toe aan elke fiatteur in het **Volgnr.** veld. Zie [Procedure: Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  

## <a name="to-set-up-an-approval-user"></a>Een goedkeuringsgebruiker instellen  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikersinstellingen voor goedkeuring** in en klik vervolgens op de gerelateerde koppeling.  
2. Maak een nieuwe regel in het venster **Gebruikersinstellingen voor goedkeuring** en vul de velden in zoals is beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Gebruikers-ID**|Selecteer de gebruikers-id van de gebruiker die is betrokken bij het goedkeuringsproces.|  
    |**Verkoper/inkoper**|Geef de verkopers- of inkoperscode op die op de gebruiker van toepassing is, in het veld **Verkoper/Inkoper**.<br /><br /> U vult het veld **Verkoper/Inkoper** meestal in als de verkoper of inkoper die verantwoordelijk is voor de klant of leverancier, ook de persoon is die de betreffende verkoop- of inkoopaanvraag moet goedkeuren.|  
    |**Fiatteur-id**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-ID**.|  
    |**Limiet voor goedkeuring verkoopbedrag**|Geef het maximale verkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-ID** kan goedkeuren.|  
    |**Onbeperkte goedkeuring van verkopen**|Geef aan dat de gebruiker in het veld **Gebruikers-ID** alle verkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|  
    |**Limiet voor goedkeuring inkoopbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-ID** kan goedkeuren.|  
    |**Onbeperkte goedkeuring van inkopen**|Geef aan dat de gebruiker in het veld **Gebruikers-ID** alle inkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|  
    |**Limiet voor goedkeuring aanvraagbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-ID** kan goedkeuren voor inkoopoffertes.<br /><br /> Als u dit veld wilt gebruiken, moet u de optie **Fiatteursketting** selecteren in het veld **Limietsoort van fiatteur** in het venster **Werkstroomreactie**.|  
    |**Onbeperkt aanvragen van goedkeuring**|Geef aan dat de gebruiker in het veld **Gebruikers-ID** alle inkoopoffertes kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring aanvraagbedrag** niet invullen.|  
    |**Vervanger**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-ID** als de gebruiker in **Fiatteur-id** niet beschikbaar is. **Opmerking:** de vervanger kan de gebruiker in het veld **Vervanger**, de directe fiatteur of de goedkeuringsbeheerder zijn, in die volgorde van prioriteit. Zie voor meer informatie [Procedure: Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).|  
    |**E-mailadres**|Geef het e-mailadres op van de gebruiker in het veld **Gebruikers-ID**.|  
    |**Beheerder goedkeuringssysteem**|Geef de gebruiker op die rechten heeft om werkstromen voor goedkeuring te deblokkeren, bijvoorbeeld door goedkeuringsaanvragen te delegeren naar nieuwe vervangende fiatteurs en door vervallen goedkeuringsaanvragen te verwijderen.|  

    > [!NOTE]  
    >  De werking van het veld **Limietsoort van fiatteur** geldt alleen voor toepassingsgebieden waar limieten kunnen worden gedefinieerd, met name verkoop- en inkoopgoedkeuringen. Enig ander type goedkeuring waar limieten niet van toepassing zijn, werkt altijd zoals beschreven voor de optie **Directe fiatteur**.  

3. Kies de actie **Gebruikersinstellingen goedkeuring testen** om de instelling van gebruikers in het goedkeuringsproces te testen.  
4. Herhaal stap 2 en 3 voor elke gebruiker die u wilt instellen als goedkeuringsgebruiker.  

## <a name="see-also"></a>Zie ook  
[Procedure: Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)   
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)   
[Procedure: Werkstromen maken](across-how-to-create-workflows.md)   
[Werkstromen instellen](across-set-up-workflows.md)   
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Werkstroom](across-workflow.md)   

