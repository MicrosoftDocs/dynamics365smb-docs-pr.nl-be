---
title: Duurzaamheidsinstelling
description: Leer hoe u duurzaamheidsfuncties instelt.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Duurzaamheidsinstellingen

Om de Duurzaamheidsmodule goed te laten werken moet u eerst een aantal basisbedieningen en instructies instellen die betrekking hebben op de gehele functionaliteit.

Om de duurzaamheidsmodule in te stellen volgt u deze stappen:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsinstelling** in en kies vervolgens de gerelateerde koppeling.
2. Configureer op het sneltabblad **Algemeen** de vereiste velden met betrekking tot de duurzaamheidsmodule.

    | Veld | Omschrijving |
    |-------|-------------|
    | **Code van eenheid voor uitstoot** | Geef de code op van de maateenheid die wordt gebruikt om uitstoot te registreren. |
    | **Decimalen voor uitstoot** | Geef het aantal decimalen op dat wordt weergegeven voor uitstoothoeveelheden. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |
    | **Land/regio verplicht** | Geef op of het land/regio verplicht is. Gebruikers kunnen het land/regio-veld in dagboeken instellen, zelfs als u dit veld niet selecteert. Als u dit selecteert, vereist u echter dat gebruikers het land/regio-veld instellen voordat ze boeken. |
    | **Divisie verplicht** | Geef op of de divisie verplicht is. De divisie kan als faciliteit worden gebruikt, zodat u uitstoot op basis van faciliteit kunt meten. Gebruikers kunnen het divisieveld in dagboeken instellen, zelfs als u dit veld niet selecteert. Als u dit selecteert, vereist u echter dat gebruikers het divisieveld instellen voordat ze boeken. |
    | **Wijziging van berekeningsbasis blokkeren als er grootboekposten bestaan** | Geef op of wijzigingen in de berekeningsbasis (formule) op het rekeningcategorieniveau worden geblokkeerd op het moment van duurzaamheidsinvoer, wanneer deze formule al is toegepast. |
    | **Foutcontrole op achtergrond inschakelen** | Geef op of de achtergrondfoutcontrole van duurzaamheidsdagboekregels is ingeschakeld. |

    > [!NOTE]
    > Nadat u de foutcontrole op achtergrond in dagboeken hebt in- of uitgeschakeld, moet u zich opnieuw aanmelden voordat u met de nieuwe instelling begint.

3. Configureer op het sneltabblad **Berekeningen** de verplichte velden die verband houden met de formules die worden gebruikt voor het berekenen van uitstoot.

    | Veld | Omschrijving |
    |-------|-------------|
    | **Decimalen brandstof/elektriciteit** | Geef het aantal decimalen op dat wordt weergegeven voor brandstof/elektriciteit-hoeveelheden. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |
    | **Decimalen voor afstand** | Geef het aantal decimalen op dat wordt weergegeven voor afstandsmetingen. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |
    | **Decimalen voor aangepast bedrag** | Geef het aantal decimalen op dat wordt weergegeven voor aangepaste hoeveelheden. De standaardinstelling, *2:5*, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren. Als u bijvoorbeeld *2* invoert, worden bij alle bedragen twee decimalen weergegeven. |

4. Voltooi de instelling op het sneltabblad **Rapportage** door de velden te configureren die betrekking hebben op rapportage aan autoriteiten.

    > [!NOTE]
    > In versie 24.0 ondersteunt [!INCLUDE[prod_short](includes/prod_short.md)] geen rapportage aan welke autoriteit dan ook. Daarom zijn de velden die gerelateerd zijn aan de configuratie van deze functionaliteit op het sneltabblad **Rapportage** bedoeld voor toekomstige rapportagemogelijkheden. Partners kunnen deze velden echter ook in gelokaliseerde versies gebruiken.

    | Veld | Omschrijving |
    |-------|-------------|
    | **Code van eenheid voor uitstootrapportage** | Geef de maateenheidscode op die wordt gebruikt om uitstoot te rapporteren, omdat u bij rapportage aan autoriteiten een andere maateenheid kunt gebruiken. Dit veld is niet van toepassing op de standaardrapporten. |
    | **Maateenheidsfactor voor rapportage** | Geef de maateenheidsfactor op die wordt gebruikt om uitstoot te registreren als u bij rapportage aan autoriteiten een andere maateenheid kunt gebruiken. |
    | **Afrondingsprecisie voor uitstoot** | Geef de grootte op van het interval dat moet worden gebruikt voor het afronden van uitstoothoeveelheden wanneer u rapporteert aan autoriteiten. |
    | **Type afronding van uitstoot** | Geef op hoe het programma uitstootbedragen afrondt wanneer u rapporteert aan de autoriteiten. De volgende opties zijn beschikbaar: **Dichtstbijzijnd**, **Omhoog** en **Omlaag**. |

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)  
[Diagram van duurzaamheidsrekeningschema en -grootboek](finance-sustainability-accounts-ledger.md)  
[Duurzaamheidsposten vastleggen](finance-sustainability-journal.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
