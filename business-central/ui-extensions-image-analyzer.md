---
title: De extensie van de Afbeeldingsanalyse gebruiken | Microsoft Docs
description: Met deze extensie kunt u afbeeldingen analyseren van contactpersonen en artikelen om kenmerken te zoeken, zodat u deze snel kunt toewijzen in Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: e7fb77ab485489158798cdd03660325c678390e1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377285"
---
# <a name="the-image-analyzer-extension"></a>De extensie Afbeeldingsanalyse

De extensie Afbeeldingsanalyse gebruikt krachtige afbeeldingsanalyse die wordt verschaft door de Computer Vision-API voor Cognitieve services van Microsoft om kenmerken te detecteren in de afbeeldingen die u importeert voor artikelen en contactpersonen, zodat u deze gemakkelijk kunt bekijken en toewijzen. Voor artikelen kunnen kenmerken bijvoorbeeld zijn of het artikel een tafel of een auto is en of het rood of blauw is. Voor contactpersonen kunnen kenmerken geslacht of leeftijd zijn.

Afbeeldingsanalyse stelt kenmerken voor op basis van tags die de Computer Vision-API vindt, en een vertrouwensniveau. Standaard worden alleen kenmerken voorgesteld als het ten minste 80% zeker is dat het kenmerk klopt. U kunt een ander vertrouwensniveau instellen, indien nodig. Als u meer wilt weten over hoe de tags en vertrouwensniveaus worden bepaald, raadpleegt u [Computer Vision-API](https://go.microsoft.com/fwlink/?linkid=851476)  

De Afbeeldingsanalyse is gratis in [!INCLUDE[prod_short](includes/prod_short.md)], maar er is een limiet van het aantal artikelen dat u tijdens een periode kunt analyseren. Standaard kunt u 100 afbeeldingen per maand analyseren.

Nadat u de extensie hebt ingeschakeld, wordt de Afbeeldingsanalyse steeds uitgevoerd wanneer u een afbeelding of contactpersoon importeert. U ziet direct de kenmerken, het vertrouwensniveau en de details en kunt besluiten wat er met elk kenmerk moet gebeuren. Als u afbeeldingen hebt geïmporteerd voordat u de Afbeeldingsanalyse hebt ingeschakeld, moet u naar de artikel- of contactpersoonkaarten gaan en de actie **Afbeelding analyseren** kiezen.  

## <a name="privacy-notice"></a>Privacyverklaring

Deze extensie gebruikt de Computer Vision API uit Microsoft Cognitive Services, die andere niveaus van nalevingsverplichtingen kan hebben dan [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u de extensie Image Analyzer inschakelt, worden klantgegevens zoals een afbeelding van een contactpersoon of een artikel verzonden naar de Computer Vision API. Door deze extensie te installeren gaat u ermee akkoord dat deze beperkte set gegevens wordt verzonden naar de Computer Vision API. U kunt de extensie Image Analyzer altijd uitschakelen of verwijderen als u deze functionaliteit niet meer wilt gebruiken. Zie voor meer informatie [Microsoft Vertrouwenscentrum](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Vereisten

Er zijn enkele vereisten voor de afbeeldingen:

* Afbeeldingsindelingen: JPEG, PNG, GIF, BMP  
* Maximale bestandsgrootte: minder dan 4 MB  
* Afbeeldingdimensies: groter dan 50 x 50 pixels  

## <a name="to-enable-image-analyzer"></a>Afbeeldingsanalyse inschakelen

De extensie Afbeeldingsanalyse is ingebouwd in [!INCLUDE[prod_short](includes/prod_short.md)]. U hoeft het alleen in te schakelen.

> [!NOTE]  
> Als u de extensie Afbeeldinganalyse wilt inschakelen, moet u een beheerder zijn. Zorg ervoor dat aan u de machtigingenset **SUPER** is toegewezen.

1. Als u de extensie Afbeeldingsanalyse wilt inschakelen, voert u een van de volgende handelingen uit:

* Open een artikel- of contactkaart. Kies op de berichtbalk **Afbeeldingen analyseren** en volg vervolgens de stappen in de begeleide instelling.  
* Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceverbindingen** in en kies **Instelling van afbeeldingsanalyse**. Kies het selectievakje **Afbeeldingsanalyse inschakelen** en volg vervolgens de stappen in de begeleide instelling.  

    > [!TIP]  
    > De pagina **Instelling van afbeeldingsanalyse** is ook waar u de mate van vertrouwen voor kenmerksuggesties kunt wijzigen. Als u bijvoorbeeld een grotere mate van vertrouwen wilt vereisen, kunt u een hoger percentage invoeren.

## <a name="to-analyze-an-image-of-an-item"></a>Een afbeelding van een artikel analyseren

In de volgende stappen wordt beschreven hoe u een afbeelding analyseert die is geïmporteerd voordat u de extensie Afbeeldingsanalyse hebt ingeschakeld.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.  
2. Kies het artikel en kies vervolgens de actie **Afbeelding analyseren**.  
3. De pagina **Kenmerken van afbeeldinganalyse** bevat de ontdekte kenmerken, het vertrouwensniveau en andere informatie over het kenmerk. Gebruik de opties **Uit te voeren acties** om aan te geven wat er met het kenmerk moet gebeuren.  

    > [!TIP]  
    > U kunt de naam van het kenmerk toevoegen aan de artikelomschrijving door **Toevoegen aan artikelomschrijving** te kiezen. Bijvoorbeeld, het kan handig zijn om snel details toe te voegen.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Een afbeelding van een contactpersoon analyseren

In de volgende stappen wordt beschreven hoe u een afbeelding analyseert die is geïmporteerd voordat u de extensie Afbeeldingsanalyse hebt ingeschakeld.  

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling.  
2. Kies de contactpersoon en kies vervolgens de actie **Afbeelding analyseren**.  
3. Op het sneltabblad **Profielvragenlijst** controleert u de voorstellen en maakt u correcties, indien nodig.  

## <a name="block-suggested-attributes"></a>Voorgestelde attributen blokkeren

Als de analyse een kenmerk voorstelt dat u niet wilt zien, kunt u het blokkeren. Wees echter voorzichtig. Geblokkeerde kenmerken worden ook niet voorgesteld voor andere artikelen of contactpersonen. Als u betreurt dat een kenmerk is geblokkeerd, kunt u **Kenmerken op blokkeringslijst weergeven** kiezen en het kenmerk van de lijst verwijderen.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Uw eigen account gebruiken voor de Computer Vision API

U kunt ook uw eigen account gebruiken voor de Computer Vision-API, bijvoorbeeld als u meer afbeeldingen wilt analyseren dan we toestaan.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van afbeeldingsanalyse** in en kies de gerelateerde koppeling.  
2. Vul de **API-URI** en **API-sleutel** in die u voor de Computer Vision-API hebt ontvangen.  

    > [!NOTE]  
    > U moet **/analyze** aan het eind van de API-URI toevoegen, als het niet al aanwezig is. Bijvoorbeeld: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Zien hoeveel analyses u in de huidige periode over hebt

U kunt het aantal analyses bekijken dat u hebt gedaan, en hoeveel u er in de huidige periode nog kunt doen.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van afbeeldingsanalyse** in en kies de gerelateerde koppeling.  
2. De **Limietsoort**, **Limietwaarde** en **Analyses uitgevoerd** bieden de gebruiksinformatie.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Stoppen met het gebruik van de extensie Afbeeldingsanalyse

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceverbindingen** in en kies **Instelling van afbeeldingsanalyse**.  
2. Schakel het selectievakje **Afbeeldingsanalyse inschakelen** uit.  

## <a name="see-also"></a>Zie ook

[Werken met artikelkenmerken](inventory-how-work-item-attributes.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Aan de slag](product-get-started.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]