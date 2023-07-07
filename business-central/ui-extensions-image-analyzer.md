---
title: De extensie Afbeeldingsanalyse
description: 'Met deze extensie kunt u afbeeldingen analyseren van contactpersonen en artikelen om kenmerken te zoeken, zodat u deze snel kunt toewijzen in Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition'
ms.search.form: '2026, 2027, 2029,'
ms.date: 05/19/2021
ms.author: bholtorf
---

# <a name="the-image-analyzer-extension"></a>De extensie Afbeeldingsanalyse

De extensie Afbeeldingsanalyse gebruikt krachtige afbeeldingsanalyse die wordt verschaft door de Computer Vision-API voor Azure Cognitive Services om kenmerken te detecteren in de afbeeldingen die u importeert voor artikelen en contactpersonen, zodat u deze gemakkelijk kunt bekijken en toewijzen. Voor artikelen kunnen kenmerken bijvoorbeeld zijn of het artikel een tafel of een auto is en of het rood of blauw is. Voor contactpersonen kunnen kenmerken geslacht of leeftijd zijn.

Afbeeldingsanalyse stelt kenmerken voor op basis van tags die de Computer Vision-API vindt, en een vertrouwensniveau. Standaard worden alleen kenmerken voorgesteld als het ten minste 80% zeker is dat het kenmerk klopt. U kunt een ander vertrouwensniveau instellen, indien nodig. Als u meer wilt weten over hoe de tags en vertrouwensniveaus worden bepaald, raadpleegt u [Computer Vision-API](https://go.microsoft.com/fwlink/?linkid=851476)  

De Afbeeldingsanalyse is gratis in [!INCLUDE[prod_short](includes/prod_short.md)], maar er is een limiet van het aantal artikelen dat u tijdens een periode kunt analyseren. Standaard kunt u 100 afbeeldingen per maand analyseren.

Nadat u de extensie hebt ingeschakeld, wordt de Afbeeldingsanalyse steeds uitgevoerd wanneer u een afbeelding of contactpersoon importeert. U ziet direct de kenmerken, het vertrouwensniveau en de details en kunt besluiten wat er met elk kenmerk moet gebeuren. Als u afbeeldingen hebt geïmporteerd voordat u de Afbeeldingsanalyse hebt ingeschakeld, moet u naar de artikel- of contactpersoonkaarten gaan en de actie **Afbeelding analyseren** kiezen.  

## <a name="privacy-notice"></a>Privacyverklaring

Deze extensie gebruikt de Computer Vision API uit Azure Cognitive Services, die andere niveaus van nalevingsverplichtingen kan hebben dan [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u de extensie Image Analyzer inschakelt, worden klantgegevens zoals een afbeelding van een contactpersoon of een artikel verzonden naar de Computer Vision API. Door deze extensie te installeren gaat u ermee akkoord dat deze beperkte set gegevens wordt verzonden naar de Computer Vision API. U kunt de extensie Afbeeldingsanalyse altijd uitschakelen of verwijderen als u deze functionaliteit niet meer wilt gebruiken. Zie voor meer informatie [Microsoft Vertrouwenscentrum](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Vereisten

Er zijn enkele vereisten voor de afbeeldingen:

* Afbeeldingsindelingen: JPEG, PNG, GIF, BMP  
* Maximale bestandsgrootte: minder dan 4 MB  
* Afbeeldingdimensies: groter dan 50 x 50 pixels  

## <a name="switch-on-the-image-analyzer-extension"></a>De extensie Afbeeldingsanalyse inschakelen

De extensie Afbeeldingsanalyse is ingebouwd in [!INCLUDE[prod_short](includes/prod_short.md)]. U hoeft het alleen in te schakelen.

> [!NOTE]  
> Als u de extensie Afbeeldinganalyse wilt inschakelen, moet u een beheerder zijn. Zorg ervoor dat aan u de machtigingenset **SUPER** is toegewezen. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.

Als u de extensie Afbeeldingsanalyse wilt inschakelen, voert u een van de volgende handelingen uit:

* Open een artikel- of contactkaart. Kies op de berichtbalk **Afbeelding analyseren** en volg vervolgens de stappen in de begeleide instelling.  
* Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer in **Serviceverbindingen** en kies vervolgens **Afbeeldingsanalyse instellen**. Kies het selectievakje **Afbeeldingsanalyse inschakelen** en volg vervolgens de stappen in de begeleide instelling.  

    > [!TIP]  
    > De pagina **Instelling van afbeeldingsanalyse** is ook waar u de mate van vertrouwen voor kenmerksuggesties kunt wijzigen. Als u bijvoorbeeld een grotere mate van vertrouwen wilt vereisen, kunt u een hoger percentage invoeren.

## <a name="analyze-an-item-image"></a>Een artikelafbeelding analyseren

In de volgende stappen wordt beschreven hoe u een afbeelding analyseert die is geïmporteerd voordat u de extensie Afbeeldingsanalyse hebt ingeschakeld.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het artikel en kies vervolgens de actie **Afbeelding analyseren**.  
3. De pagina **Kenmerken van afbeeldinganalyse** bevat de ontdekte kenmerken, het vertrouwensniveau en andere informatie over het kenmerk. Gebruik de **Uit te voeren actie**-opties om te specificeren wat te doen met het kenmerk of kies **Toevoegen aan artikelbeschrijving** om de naam van het kenmerk toe te voegen aan de artikelbeschrijving. Bijvoorbeeld, deze actie kan handig zijn om snel details toe te voegen.

Het veld **Uit te voeren actie** heeft de volgende opties:

| Actie | Omschrijving |
| ------ | ----------- |
| *Negeren* | Er worden geen acties uitgevoerd. |
| *Gebruiken als kenmerk* | De waarde wordt toegevoegd aan de artikelkenmerken. Meer informatie op [Werken met artikelkenmerken](inventory-how-work-item-attributes.md). |
| *Gebruik als categorie* | De geselecteerde waarde wordt als categorie toegevoegd. Zie voor meer informatie [Artikelen categoriseren](inventory-how-categorize-items.md). |
| *Toevoegen aan blokkeringslijst* | Als de analyse een kenmerk voorstelt dat u niet wilt zien, kunt u het blokkeren. Wees echter voorzichtig. Geblokkeerde kenmerken worden ook niet voorgesteld voor andere artikelen. Als u betreurt dat een kenmerk is geblokkeerd, kunt u **Geblokkeerde kenmerken weergeven** kiezen en het kenmerk van de lijst verwijderen. |

> [!NOTE]  
> Standaard geeft **Artikelkenmerken** kenmerken weer waarbij **Zekerheidsscore** ligt boven **Drempelpercentage voor zekerheidsscore**, zoals gedefinieerd in de **Instelling van afbeeldingsanalyse**. Om alle gedetecteerde kenmerken te zien kiest u de actie **Alle kenmerken weergeven**.

## <a name="analyze-a-contact-person-picture"></a>Een afbeelding van een contactpersoon analyseren

In de volgende stappen wordt beschreven hoe u een afbeelding analyseert die is geïmporteerd voordat u de extensie Afbeeldingsanalyse hebt ingeschakeld.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contacten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de contactpersoon en kies vervolgens de actie **Afbeelding analyseren**.  
3. Op het sneltabblad **Profielvragenlijst** controleert u de voorstellen en maakt u correcties, indien nodig. Zie voor meer informatie [Profielvragenlijsten gebruiken om bedrijfscontactpersonen te classificeren](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    >
    > De Computer Vision API retourneert de volgende kenmerken:
    >
    > * *leeftijd*
    >
    >     Een geschatte 'visuele leeftijd' in jaren. Het is hoe oud een persoon eruitziet in tegenstelling tot de werkelijke biologische leeftijd.
    > * *geslacht*
    >
    >    Man of vrouw.
    >
    > De Computer Vision API retourneert geen betrouwbaarheidsniveau voor leeftijds- en geslachtskenmerken.
  
## <a name="use-your-own-computer-vision-api-account"></a>Uw eigen Computer Vision API-account gebruiken

U kunt ook uw eigen account gebruiken voor de Computer Vision API, bijvoorbeeld als u meer afbeeldingen wilt analyseren dan de standaardintegratie biedt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instelling van afbeeldingsanalyse** in en kies vervolgens de gerelateerde koppeling.
2. Vul de **API-URI** en **API-sleutel** in die u voor de Computer Vision-API hebt ontvangen.  

    > [!NOTE]  
    > U moet **/analyze** aan het eind van de API-URI toevoegen, als het niet al aanwezig is. Bijvoorbeeld: ```https://cronus.api.cognitive.microsoft.com/vision/v2.0/analyze```.

## <a name="see-how-many-analyses-you-have-left-in-the-current-period"></a>Zien hoeveel analyses u in de huidige periode over hebt

U kunt het aantal analyses bekijken dat u hebt gedaan, en hoeveel u er in de huidige periode nog kunt doen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van afbeeldingsanalyse** in en kies vervolgens de gerelateerde koppeling.
2. De velden **Limietsoort**, **Limietwaarde** en **Uitgevoerde analyses** bieden de gebruiksinformatie.  

## <a name="stop-using-the-image-analyzer-extension"></a>Stoppen met het gebruik van de extensie Afbeeldingsanalyse

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer in **Serviceverbindingen** en kies vervolgens **Afbeeldingsanalyse instellen**.  
2. Schakel het veld **Afbeeldingsanalyse inschakelen** uit.  

U kunt de extensie ook volledig verwijderen. U kunt deze altijd weer ophalen van AppSource. Zie [Extensies installeren en verwijderen in Business Central](ui-extensions-install-uninstall.md#uninstall-an-app) voor meer informatie.  

## <a name="see-also"></a>Zie ook

[Werken met artikelkenmerken](inventory-how-work-item-attributes.md)  
[Artikelen categoriseren](inventory-how-categorize-items.md)  
[Profielvragenlijsten gebruiken om bedrijfscontactpersonen te classificeren](marketing-create-contact-profile-questionnaire.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
