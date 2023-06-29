---
title: Facturering en Business Central gebruiken
description: Oplossing om Microsoft Invoicing te kunnen openen wanneer u zich hebt aangemeld voor Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Invoicing, Microsoft 365'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="use-the-same-microsoft-365-account-in--and-microsoft-invoicing"></a><a name="use-the-same-microsoft-365-account-in--and-microsoft-invoicing"></a>Dezelfde Microsoft 365-account gebruiken in [!INCLUDE[prod_short](includes/prod_long.md)] en Microsoft Invoicing
Wanneer u zich aanmeldt voor de proefversie van [!INCLUDE[prod_short](includes/prod_short.md)], kunt u kiezen voor de evaluatiefase van 30 dagen, het abonnement laten ingaan of stoppen met het gebruiken van [!INCLUDE[prod_short](includes/prod_short.md)]. In alle gevallen hebt u op een gegeven moment misschien iets gezien dat **Microsoft Invoicing** heet en erop geklikt. Dit was een app die deel uitmaakte van wat nu Microsoft 365 Business Standard is en voorheen bekend stond als Microsoft 365 Business Premium-abonnement, dus niet iedereen zal die tegel in zijn of haar Microsoft 365 hebben gezien.  

Microsoft Invoicing is niet langer beschikbaar, maar als u zich bij Invoicing moet aanmelden om uw gegevens op te halen, ziet u mogelijk een bericht dat u geen toegang hebt tot Microsoft Invoicing omdat uw account wordt gebruikt in [!INCLUDE[prod_short](includes/prod_short.md)].  

Er wordt een vergelijkbaar bericht weergegeven als u de mobiele app voor Invoicing installeert.  

## <a name="workaround"></a><a name="workaround"></a>Oplossing
Invoicing en [!INCLUDE[prod_short](includes/prod_short.md)] delen een platform. Dit betekent dat u als een bestaande gebruiker van [!INCLUDE[prod_short](includes/prod_short.md)] wordt herkend wanneer u op Invoicing klikt in het Microsoft 365-beheercentrum. De reden hiervoor is dat Invoicing niet hetzelfde bedrijf kan gebruiken als [!INCLUDE[prod_short](includes/prod_short.md)].  

U moet u daarom aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)], de naam van uw bestaande bedrijf wijzigen en vervolgens een nieuw bedrijf maken om in Invoicing te gebruiken. Er worden geen gegevens verplaatst of overschreven tijdens deze oplossingsprocedure.

### <a name="to-rename-your-company"></a><a name="to-rename-your-company"></a>De naam van uw bedrijf wijzigen
1. Meld u aan bij [!INCLUDE[prod_short](includes/prod_short.md)].
2. Kies in de rechterbovenhoek het pictogram **Instellingen** ![Instellingen.](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") en kies vervolgens **Mijn instellingen**.
3. Kies in het veld **Bedrijf** een ander bedrijf.
4. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bedrijven** in en kies vervolgens de gerelateerde koppeling.  
5. Kies op de pagina **Bedrijven** **Lijst bewerken**.  
6. Wijzig de naam van het item *Mijn bedrijf*.  

    Wacht een aantal minuten. Er wordt een aantal wijzigingen doorgevoerd in de onderliggende database, wat enige tijd kost.
7.  Wanneer het systeem klaar is, kiest u de knop **Nieuw bedrijf maken**.  
8.  Geef in het dialoogvenster dat verschijnt de naam op als *Mijn bedrijf* en kies de optie **Productie - Alleen instellingsgegevens**.  

Dit kost opnieuw een aantal minuten. Wanneer het proces is voltooid, kunt u Invoicing openen als onderdeel van uw Microsoft 365 Business Standard-ervaring. Maar alleen om gegevens te exporteren omdat de Invoicing-app is verouderd.  

### <a name="what-about-my-data"></a><a name="what-about-my-data"></a>Hoe zit het met mijn gegevens?
Wanneer u de naam van het oorspronkelijke Mijn bedrijf wijzigt, wordt de naam gewijzigd van de databasetabellen met de bestaande [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens, maar de gegevens zelf blijven ongewijzigd.  

Als u zowel Invoicing als [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt, worden de gegevens in twee verschillende containers (de twee bedrijven) opgeslagen. Er wordt niets gedeeld, dus u moet de klanten en artikelen in beide bedrijven beheren.  

## <a name="see-also"></a><a name="see-also"></a>Zie ook
[Veelgestelde vragen](across-faq.yml)  
[Beheer](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
