---
title: Stel uw aangepaste gekleurde indicatoren in voor de activiteit van een indicatiestapel
description: Als beheerder kunt u indicatiestapels instellen die in de Rolcentra van gebruikers worden weergegeven en die een indicator bevatten die van kleur verandert afhankelijk van de gegevenswaarden in de indicatiestapels.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9701, 9702'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a><a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a>Een gekleurde indicator voor indicatiestapels instellen voor het bedrijf of voor afzonderlijke gebruikers

Als beheerder kunt u indicatiestapels instellen die in de Rolcentra van gebruikers worden weergegeven en die een indicator bevatten die van kleur verandert afhankelijk van de gegevenswaarden in de indicatiestapels.  

De indicator wordt als een gekleurde balk weergegeven langs de bovenrand van de indicatiestapeltegel. Het geeft een visueel signaal van de status van de activiteit van de indicatiestapel. Het signaal kan gunstige of ongunstige condities aangeven om de gebruiker tot actie te laten overgaan. Als een indicatiestapel bijvoorbeeld doorlopende verkoopfacturen weergeeft, kunt u de indicator zo instellen dat deze groen (gunstig) is wanneer het totale aantal doorlopende verkoopfacturen kleiner is dan 10 en dat deze rood (ongunstig) is wanneer het totaal groter is dan 20.  

Vanuit de pagina **Instelling indicatiestapel** kunt u indicatoren instellen voor alle indicatiestapels die beschikbaar zijn in de bedrijfsdatabase. U kunt de indicatoren instellen voor alle gebruikers in het bedrijf of alleen voor een individuele gebruiker. De indicatorinstellingen op de pagina **Instelling indicatiestapel** fungeren als de standaardindicatorinstellingen. Als de pagina **Instelling indicatiestapel** aan gebruikers beschikbaar is gesteld, kunnen zij de indicatorinstellingen aanpassen die u op de pagina **Instelling indicatiestapel** definieert.  

Als u de indicator wilt instellen, geeft u maximaal twee drempelwaarden op die de drie bereiken van gegevenswaarden definiëren (laag, gemiddeld en hoog) waarop u een andere kleur (of stijl) kunt toepassen.  

### <a name="to-set-up-colored-indicators-on-cues"></a><a name="to-set-up-colored-indicators-on-cues"></a>Gekleurde indicatoren instellen voor indicatiestapels
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voert u **Instelling indicatiestapel** in en kiest u vervolgens de gerelateerde koppeling.  

     De pagina **Instelling indicatiestapel** wordt geopend. De pagina bevat de indicatoren die op het moment zijn ingesteld voor indicatiestapels. Indicators die van toepassing zijn op alle gebruikers in het bedrijf, hebben een leeg veld **Gebruikersnaam**. Indicatoren die van toepassing zijn op een specifieke gebruiker, bevatten de gebruikersnaam in het veld **Gebruikersnaam**.  

    > [!NOTE]  
    >  Als u een indicator voor het hele bedrijf instelt en een gebruiker de indicator later wijzigt, wordt een aparte vermelding voor de indicator in de lijst weergegeven voor die gebruiker.  

2. Kies de actie **Lijst bewerken**.  
3. Als u een indicator wilt instellen voor een indicatiestapel die niet op de pagina wordt weergegeven, kiest u de actie **Nieuw** en vult u de velden in zoals hierna wordt beschreven. Als u een bestaande indicator wilt wijzigen, gaat u naar de volgende stap.  

    |  Veld  |  Description  |    
    |---------|---------------|  
    |**Gebruikersnaam**|Als u de indicator voor alle gebruikers wilt instellen, laat u dit veld leeg.<br /><br /> Als u de indicator voor een specifieke gebruiker wilt instellen, stelt u dit veld in op de naam van de gebruiker.|  
    |**Tabelnr.**|Geeft de id op van het tabelobject dat de indicatiestapel bevat. Gebruik de vervolgkeuzelijst om de tabel te zoeken. De vervolgkeuzelijst bevat alle indicatiestapeltabellen in de bedrijfsdatabase.<br /><br /> Het veld **Tabelnaam** wordt automatisch gevuld op basis van uw selectie.|  
    |**Veldnr.**|Geeft de id op van de indicatiestapel waarvoor u een indicator wilt instellen. Gebruik de vervolgkeuzelijst om de gewenste indicatiestapel te vinden. **Opmerking:** de indicatiestapel-id correspondeert met het veldnummer dat aan de indicatiestapel in de tabel wordt toegewezen. <br /><br /> Het veld **Veldnaam** wordt automatisch gevuld op basis van uw selectie.|  

4. Als u de indicator voor een indicatiestapel wilt instellen, stelt u de velden in zoals beschreven in de volgende tabel.  

    |  Veld  |  Description  |    
    |---------|---------------|  
    |**LowStyle**|Geeft de kleur op van de indicator wanneer de waarde van de indicatiestapel kleiner is dan de waarde van het veld **Drempel 1**.|  
    |**LowThreshold**|Geeft de waarde op waarop of waarboven de indicator verandert in de kleur die wordt opgegeven door het veld **Stijl middenbereik**.|  
    |**MiddleStyle**|Geeft de kleur op van de indicator wanneer de waarde van de indicatiestapel groter is dan of gelijk is aan de waarde van het veld **Drempel 1**, maar kleiner is dan de waarde van het veld **Drempel 2**.|  
    |**HighThreshold**|Geeft de waarde op waarboven de indicator verandert in de kleur die wordt opgegeven door het veld **Stijl hoog bereik**.|  
    |**HighStyle**|Geeft de kleur die moet worden gebruikt wanneer de waarde van de indicatiestapel groter is dan de waarde van het veld **Drempel 2**.|  

     De volgende tabel bevat de kleuren die overeenkomen met de opties van de velden **LowStyle**, **MiddleStyle** en **HighStyle**.  

    |  Optie  |  Kleur  |  
    |----------|---------|  
    |**Geen**|Geen kleur (dezelfde kleur als de indicatiestapeltegel)|  
    |**Gunstig**|Groen|  
    |**Ongunstig**|Rood|  
    |**Dubbelzinnig**|Geel|  
    |**Ondergeschikt**|Grijs|  

## <a name="see-also"></a><a name="see-also"></a>Zie ook


[!INCLUDE[footer-include](includes/footer-banner.md)]
