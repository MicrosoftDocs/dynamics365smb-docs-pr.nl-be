---
title: Goedkeuringsgebruikers instellen
description: Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u op de pagina Gebruikersinstellingen voor goedkeuring de werkstroomgebruikers instellen die betrokken zijn bij de goedkeuringsprocessen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: e4bb6345a55eedabdf433dbb84a7bf0c7f64d215
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129807"
---
# <a name="set-up-approval-users"></a>Goedkeuringsgebruikers instellen

Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. Op de pagina **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.  

> [!NOTE]  
> Goedkeuringsgebruikers, zowel aanvragers als fiatteurs, moeten eerst worden ingesteld als werkstroomgebruikers op de pagina **Werkstroomgebruikersgroep**. Zie [Werkstromen instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  

 Als u gebruikers van de goedkeuringsgebruikers hebt ingesteld, kunt u de instellingen gebruiken om werkstroomantwoorden te maken voor goedkeuringswerkstromen. Zie voor meer informatie stap 9 in [Werkstromen maken](across-how-to-create-workflows.md).  

> [!NOTE]  
> Stel een hiërarchie voor fiatteurs op om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd totdat meerdere fiatteurs in een goedkeuringsketen deze hebben goedgekeurd. Voor het fiatteurstype **Fiatteur** stelt u fiatteurs op de pagina **Gebruikersinstellingen voor goedkeuring** in. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** op de pagina **Werkstroomgebruikersgroepen** in en definieer de hiërarchie door incrementele nummers aan elke fiatteur in het veld **Volgnr.** invoeren. Zie dit onderwerp en [Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md) voor meer informatie.  

## <a name="to-set-up-an-approval-user"></a>Een goedkeuringsgebruiker instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.  
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
    |**Vervanger**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-id** als de gebruiker in het veld **Fiatteur-id** niet beschikbaar is. <br /><br />**Opmerking:** de vervanger kan de gebruiker in het veld **Vervanger**, de directe fiatteur of de goedkeuringsbeheerder zijn, in die volgorde van prioriteit. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).|  
    |**E-mailadres**|Geef het e-mailadres op van de gebruiker in het veld **Gebruikers-ID**.|  
    |**Beheerder goedkeuringssysteem**|Geef de gebruiker op die rechten heeft om de goedkeuringswerkstromen te deblokkeren. Bijvoorbeeld door goedkeuringsverzoeken te delegeren aan nieuwe vervangende goedkeurders en achterstallige goedkeuringsverzoeken te verwijderen.|

    > [!Note]
    > Er kan maar één persoon goedkeuringsbeheerder zijn.

3. Kies de actie **Gebruikersinstellingen goedkeuring testen** om de instelling van gebruikers in het goedkeuringsproces te testen.  
4. Herhaal stap 2 en 3 voor elke gebruiker die u wilt instellen als goedkeuringsgebruiker.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Zie ook

[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)  
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)  
[Werkstromen maken](across-how-to-create-workflows.md)  
[Werkstromen instellen](across-set-up-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]