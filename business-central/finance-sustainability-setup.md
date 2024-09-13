---
title: Duurzaamheidsinstelling
description: Leer hoe u duurzaamheidsfuncties instelt.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, equivalent, CO2e, CO2, carbon, role center, fees'
ms.search.form: '6221, 6235, 6245'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-module-setup"></a>Opzet van de duurzaamheidsmodule

Om de Duurzaamheidsmodule goed te laten werken moet u eerst een aantal basisbedieningen en instructies instellen die betrekking hebben op de gehele functionaliteit.

Om de duurzaamheidsmodule in te stellen volgt u deze stappen:

## <a name="role-center"></a>Rolcentrum

Voor personen die primair verantwoordelijk zijn voor duurzaamheidsprocessen, is het raadzaam om het rolcentrum  *Duurzaamheidsmanager*  te gebruiken. Om dit rolcentrum te configureren, voert u de volgende stappen uit: volgen  

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, ga naar  **Mijn instellingen** en selecteer vervolgens de gerelateerde koppelen.
2. Selecteer in het veld  **Rol** de pagina  **Beschikbare rollen** .
3. Selecteer de regel **Duurzaamheidsmanager** .
4. Selecteer **OK**.

Het rolcentrum *Duurzaamheidsmanager* faciliteert efficiënt beheer van alle belangrijke gebieden die verband houden met duurzaamheid. Het omvat de belangrijkste duurzaamheidskenmerken, evenals financiële en inkoopprocessen. Bovendien biedt het inzicht in de belangrijkste KPI's op het gebied van duurzaamheid.

## <a name="sustainability-setup"></a>Duurzaamheidsinstellingen

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsinstelling** in en kies vervolgens de gerelateerde koppeling.
2. Configureer op het sneltabblad **Algemeen** de vereiste velden met betrekking tot de duurzaamheidsmodule.

    | Veld | Beschrijving |
    |-------|-------------|
    | **Code van eenheid voor uitstoot** | Geef de code op van de maateenheid die wordt gebruikt om uitstoot te registreren. |
    | **Decimalen voor uitstoot** | Geef het aantal decimalen op dat wordt weergegeven voor uitstoothoeveelheden. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |
    | **Land/regio verplicht** | Geef op of het land/regio verplicht is. Gebruikers kunnen het land/regio-veld in dagboeken instellen, zelfs als u dit veld niet selecteert. Als u dit selecteert, vereist u echter dat gebruikers het land/regio-veld instellen voordat ze boeken. |
    | **Divisie verplicht** | Geef op of de divisie verplicht is. De divisie kan als faciliteit worden gebruikt, zodat u uitstoot op basis van faciliteit kunt meten. Gebruikers kunnen het divisieveld in dagboeken instellen, zelfs als u dit veld niet selecteert. Als u dit selecteert, vereist u echter dat gebruikers het divisieveld instellen voordat ze boeken. |
    | **Wijziging van berekeningsbasis blokkeren als er grootboekposten bestaan** | Geef op of wijzigingen in de berekeningsbasis (formule) op het rekeningcategorieniveau worden geblokkeerd op het moment van duurzaamheidsinvoer, wanneer deze formule al is toegepast. |
    | **Foutcontrole op achtergrond inschakelen** | Geef op of de achtergrondfoutcontrole van duurzaamheidsdagboekregels is ingeschakeld. |

    > [!NOTE]
    > Nadat u de foutcontrole op achtergrond in dagboeken hebt in- of uitgeschakeld, moet u zich opnieuw aanmelden voordat u met de nieuwe instelling begint.

3. Configureer op het sneltabblad  **Inkoop** de vereiste velden die betrekking hebben op het gebruik van duurzaamheidsfuncties in het inkoopproces.  

    | Veld | Beschrijving |
    |-------|-------------|
    | **gebruik emissies in aankoopdocumenten** | Als u dit veld inschakelt, worden velden en functies met betrekking tot duurzaamheid weergegeven in de inkoopdocumenten, zoals  **Duurzaamheidsrekening** of verschillende emissies. |

4. Configureer op het sneltabblad **Berekeningen** de verplichte velden die verband houden met de formules die worden gebruikt voor het berekenen van uitstoot.

    | Veld | Beschrijving |
    |-------|-------------|
    | **Decimalen brandstof/elektriciteit** | Geef het aantal decimalen op dat wordt weergegeven voor brandstof/elektriciteit-hoeveelheden. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |
    | **Decimalen voor afstand** | Geef het aantal decimalen op dat wordt weergegeven voor afstandsmetingen. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |
    | **Decimalen voor aangepast bedrag** | Geef het aantal decimalen op dat wordt weergegeven voor aangepaste hoeveelheden. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |

5. Voltooi de instelling op het sneltabblad **Rapportage** door de velden te configureren die betrekking hebben op rapportage aan autoriteiten.

    > [!NOTE]
    > In versie 24.0 ondersteunt [!INCLUDE[prod_short](includes/prod_short.md)] geen rapportage aan welke autoriteit dan ook. Daarom zijn de velden die gerelateerd zijn aan de configuratie van deze functionaliteit op het sneltabblad **Rapportage** bedoeld voor toekomstige rapportagemogelijkheden. Partners kunnen deze velden echter ook in gelokaliseerde versies gebruiken.

    | Veld | Beschrijving |
    |-------|-------------|
    | **Code van eenheid voor uitstootrapportage** | Geef de maateenheidscode op die wordt gebruikt om uitstoot te rapporteren, omdat u bij rapportage aan autoriteiten een andere maateenheid kunt gebruiken. Dit veld is niet van toepassing op de standaardrapporten. |
    | **Maateenheidsfactor voor rapportage** | Geef de maateenheidsfactor op die wordt gebruikt om uitstoot te registreren als u bij rapportage aan autoriteiten een andere maateenheid kunt gebruiken. |
    | **Afrondingsprecisie voor uitstoot** | Geef de grootte op van het interval dat moet worden gebruikt voor het afronden van uitstoothoeveelheden wanneer u rapporteert aan autoriteiten. |
    | **Type afronding van uitstoot** | Geef op hoe het programma uitstootbedragen afrondt wanneer u rapporteert aan de autoriteiten. De volgende opties zijn beschikbaar: **Dichtstbijzijnd**, **Omhoog** en **Omlaag**. |

## <a name="emission-fees"></a>Uitstootkosten

Om interne CO2-heffingen bij te houden of uw emissies te berekenen met behulp van CO2-equivalenten, moet u de pagina  **Emissieheffingen**  configureren. Om deze informatie in te stellen, voert u de volgende stappen uit: volgen  

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, voer  **Emissiekosten** in en selecteer vervolgens de gerelateerde koppelen. 
2. Kies in het veld  **Emissietype** de broeikasgasemissie die u wilt configureren: **CO2**, **CH4** of **N2O**. Deze optie is verplicht.   
3. U kunt het **Scope Type** verder specificeren. Als u dit veld leeg laat, is dit van toepassing op alle scopes. U kunt de configuratie echter voor elke scope afzonderlijk uitvoeren.  
4. U kunt de **Begindatum** en **Einddatum** configureren. Dat betekent dat u verschillende configuraties kunt gebruiken voor verschillende periodes. 
5. De **Land-/regiocode** en **Verantwoordelijkheidscode** zijn optionele velden en u kunt zelf kiezen of u ze wilt gebruiken. Deze velden kunnen nuttig zijn omdat het mogelijk is om verschillende CO2-tarieven per land te hanteren of om verschillende conversies van de CO2e per land of per faciliteit (verantwoordelijkheidscentrum) te gebruiken.  
6. Het veld **Koolstofbelasting** geeft de interne koolstofbelasting weer die een bedrijf zichzelf in rekening brengt voor elke eenheid CO2-equivalent die het uitstoot. Het kan worden gebruikt op basis van bepaalde lokale of regionale voorschriften, maar ook voor interne berekeningen. **De CO2-heffing wordt berekend telkens wanneer u emissies boekt. Deze informatie is zichtbaar in de Duurzaamheidsposten, zonder dat u deze extra hoeft te boeken in het grootboek.**  **·** **·** U kunt de **koolstofheffing** per meeteenheid instellen die u in de **Duurzaamheidsinstellingen** hebt staan. Deze kan alleen worden ingevuld voor de regel waar het **emissietype** CO2 **is**. 
7. De  **koolstofequivalentfactor** specificeert de coëfficiënt waarmee de impact van verschillende broeikasgassen wordt omgezet in de equivalente hoeveelheid koolstofdioxide op basis van hun aardopwarmingspotentieel. Als het **emissietype** CO2 is, is de **koolstofequivalentfactor** altijd *1*  en kunt u deze waarde niet wijzigen, omdat CO2 het referentiegas is dat wordt gebruikt voor het berekenen van het aardopwarmingspotentieel (GWP) van andere broeikasgassen. Omdat CO2 de basislijn is, is het GWP ingesteld op *1*. Voor andere broeikasgassen moeten gebruikers de waarden handmatig configureren. Om een correcte berekening te maken, kunt u het volgende voorbeeld gebruiken: Stel dat 1 kilogram N2O gelijk is aan 298 kilogram CO2, dan moet u 1/298 berekenen. Het resultaat dat u dan moet invullen, is 0.00336.  

> [!NOTE]
> Het veld **koolstofheffing** in de **duurzaamheidsboekposten** wordt niet berekend op basis van de **CO2-uitstootwaarden**. In plaats daarvan gebruiken we als basis voor deze formule het veld  [!INCLUDE[prod_short](includes/prod_short.md)] CO2e-emissie **.**  **Het veld CO2e-emissie** wordt berekend op basis van alle emissies die bij de invoer zijn geboekt en de **koolstofequivalentfactor** die voor elk van de gassen is geconfigureerd op de pagina **Emissiekosten** .  

Als u de  **emissierechten** niet hebt geconfigureerd voordat u uw duurzaamheidsposten hebt geboekt en u uw koolstofheffingen en CO2e met terugwerkende kracht wilt berekenen, moet u de actie  **emissierechten berekenen** uitvoeren om de waarden in de  **duurzaamheidsposten** bij te werken.  

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)    
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)    
[Duurzaamheidsrekeningschema en grootboek](finance-sustainability-accounts-ledger.md)    
[Duurzaamheidsposten vastleggen](finance-sustainability-journal.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
