---
title: De extensie van de Afbeeldingsanalyse gebruiken | Microsoft Docs
description: Met deze extensie kunt u afbeeldingen analyseren van contacten en artikelen om kenmerken te zoeken, zodat u deze snel kunt toewijzen in Finance and Operations, Business edition.
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6b7db51399f965f290e8871c74b30b9925553f83
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---

# <a name="the-image-analyzer-extension-for-microsoft-finance-and-operations-business-edition"></a>De extensie Afbeeldingsanalyse voor Microsoft Finance and Operations, Business edition
De extensie Afbeeldingsanalyse gebruikt krachtige afbeeldingsanalyse die wordt verschaft door de Computer Vision-API voor Cognitieve services van Microsoft om kenmerken te detecteren in de afbeeldingen die u importeert voor artikelen en contactpersonen, zodat u deze gemakkelijk kunt bekijken en toewijzen. Voor artikelen kunnen kenmerken bijvoorbeeld zijn of het artikel een tafel of een auto is en of het rood of blauw is. Voor contactpersonen kunnen kenmerken geslacht of leeftijd zijn.

Afbeeldingsanalyse stelt kenmerken voor op basis van tags die de Computer Vision-API vindt, en een vertrouwensniveau. Standaard worden alleen kenmerken voorgesteld als het ten minste 80% zeker is dat het kenmerk klopt. U kunt een ander vertrouwensniveau instellen, indien nodig. Als u meer wilt weten over hoe de tags en vertrouwensniveaus worden bepaald, raadpleegt u [Computer Vision-API](https://go.microsoft.com/fwlink/?linkid=851476)  

De Afbeeldingsanalyse is gratis in [!INCLUDE[d365fin](includes/d365fin_md.md)], maar er is een limiet van het aantal artikelen dat u tijdens een periode kunt analyseren. Standaard kunt u 100 afbeeldingen per maand analyseren.

Nadat u de extensie hebt ingeschakeld, wordt de Afbeeldingsanalyse steeds uitgevoerd wanneer u een afbeelding of contactpersoon importeert. U ziet direct de kenmerken, het vertrouwensniveau en de details en kunt besluiten wat er met elk kenmerk moet gebeuren. Als u afbeeldingen hebt geïmporteerd voordat u de Afbeeldingsanalyse hebt ingeschakeld, moet u naar de artikel- of contactpersoonkaarten gaan en de actie **Afbeelding analyseren** kiezen.  

>   [!NOTE]  
>   Door deze extensie in te schakelen gaat u ermee akkoord dat Microsoft uw gegevens mag opslaan en gebruiken om Microsoft-services te verbeteren, bijvoorbeeld om de Computer Vision API beter te maken. Om te helpen uw privacy te beschermen nemen we stappen om uw gegevens anoniem en veilig te maken. We publiceren uw gegevens niet en laten anderen deze niet gebruiken. U kunt de afbeelding van het artikel in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwijderen, maar de Computer Vision API bevat het dan nog in de niet-geïdentificeerde vorm. Zie voor meer informatie [Microsoft Vertrouwenscentrum](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Vereisten
Er zijn enkele vereisten voor de afbeeldingen:

* Afbeeldingsindelingen: JPEG, PNG, GIF, BMP  
* Maximale bestandsgrootte: minder dan 4 MB  
* Afbeeldingdimensies: groter dan 50 x 50 pixels  

## <a name="blacklisting-suggested-attributes"></a>Op zwarte lijst plaatsen van voorgestelde kenmerken
Als de analyse een kenmerk voorstelt dat u niet wilt zien, kunt u het op de zwarte lijst plaatsen. Wees echter voorzichtig. Kenmerken op de zwarte lijst worden ook niet voorgesteld voor andere artikelen of contactpersonen. Als u betreurt dat een kenmerk op de zwarte lijst staat, kunt u **Op de zwarte lijst gezette kenmerken** kiezen en het kenmerk van de lijst verwijderen.

## <a name="to-enable-image-analyzer"></a>Afbeeldingsanalyse inschakelen
De extensie Afbeeldingsanalyse is ingebouwd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. U hoeft het alleen in te schakelen.

> [!NOTE]  
> Als u de extensie Afbeeldinganalyse wilt inschakelen, moet u een beheerder zijn. Zorg ervoor dat aan u de machtigingenset **SUPER** is toegewezen.

1. Als u de extensie Afbeeldingsanalyse wilt inschakelen, voert u een van de volgende handelingen uit:

* Open een artikel- of contactkaart. Kies op de berichtbalk **Afbeeldingen analyseren** en volg vervolgens de stappen in de begeleide instelling.  
* Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Serviceverbindingen** in en kies vervolgens **Afbeeldingsanalyse**. Kies het selectievakje **Afbeeldingsanalyse inschakelen** en volg vervolgens de stappen in de begeleide instelling.  

>   [!TIP]  
>   De pagina **Instelling van afbeeldingsanalyse** is ook waar u de mate van vertrouwen voor kenmerksuggesties kunt wijzigen. Als u bijvoorbeeld een grotere mate van vertrouwen wilt vereisen, kunt u een hoger percentage invoeren.

## <a name="to-analyze-an-image-of-an-item"></a>Een afbeelding van een artikel analyseren
In de volgende stappen wordt beschreven hoe u een afbeelding analyseert die is geïmporteerd voordat u de extensie Afbeeldingsanalyse hebt ingeschakeld.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies het artikel en kies vervolgens de actie **Afbeelding analyseren**.  
3. De pagina **Kenmerken van afbeeldinganalyse** bevat de ontdekte kenmerken, het vertrouwensniveau en andere informatie over het kenmerk. Gebruik de opties **Uit te voeren acties** om aan te geven wat er met het kenmerk moet gebeuren.  

>   [!TIP]  
>   U kunt de naam van het kenmerk toevoegen aan de artikelomschrijving door **Toevoegen aan artikelomschrijving** te kiezen. Bijvoorbeeld, het kan handig zijn om snel details toe te voegen.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Een afbeelding van een contactpersoon analyseren
In de volgende stappen wordt beschreven hoe u een afbeelding analyseert die is geïmporteerd voordat u de extensie Afbeeldingsanalyse hebt ingeschakeld.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Contacten** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de contactpersoon en kies vervolgens de actie **Afbeelding analyseren**.  
3. Op het sneltabblad **Profielvragenlijst** controleert u de voorstellen en maakt u correcties, indien nodig.  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Uw eigen account gebruiken voor de Computer Vision API
U kunt ook uw eigen account gebruiken voor de Computer Vision-API, bijvoorbeeld als u meer afbeeldingen wilt analyseren dan we toestaan.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Instelling van afbeeldingsanalyse** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul de **API-URI** en **API-sleutel** in die u voor de Computer Vision-API hebt ontvangen.  

>   [!NOTE]  
>   U moet **/analyze** aan het eind van de API-URI toevoegen, als het niet al aanwezig is. Bijvoorbeeld: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Zien hoeveel analyses u in de huidige periode over hebt
U kunt het aantal analyses bekijken dat u hebt gedaan, en hoeveel u er in de huidige periode nog kunt doen.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Instelling van afbeeldingsanalyse** in en klik vervolgens op de gerelateerde koppeling.  
2. De **Limietsoort**, **Limietwaarde** en **Analyses uitgevoerd** bieden de gebruiksinformatie.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Stoppen met het gebruik van de extensie Afbeeldingsanalyse
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Serviceverbindingen** in en kies vervolgens **Instellingen van afbeeldingsanalyse**.  
2. Schakel het selectievakje **Afbeeldingsanalyse inschakelen** uit.  

## <a name="see-also"></a>Zie ook
[Werken met artikelkenmerken](inventory-how-work-item-attributes.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

