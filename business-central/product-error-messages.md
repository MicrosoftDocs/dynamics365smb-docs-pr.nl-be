---
title: Waarschuwingen en foutmeldingen
description: Leer hoe u problemen kunt oplossen en oplossingen kunt vinden voor foutmeldingen wanneer u in Business Central werkt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# <a name="warnings-and-error-messages"></a>Waarschuwingen en foutmeldingen

Tijdens uw werkdag ziet u mogelijk meldingen in [!INCLUDE [prod_short](includes/prod_short.md)] dat er iets is misgegaan of dat het bijvoorbeeld niet mogelijk was om iets te boeken. In veel gevallen maakt de melding het gemakkelijk om de kwestie op te lossen of om eventuele wijzigingen ongedaan te maken. In andere gevallen beschikt u mogelijk niet over de informatie die u nodig heeft om de blokkering op te heffen. In dit artikel vindt u tips om vooruitgang te boeken.  

## <a name="in-product-user-assistance"></a>Gebruikersassistentie in het product

De standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)] bevat beschrijvingen voor de meeste velden, kolommen en acties die toegankelijk zijn wanneer u de naam kiest. In combinatie met instructietips voor belangrijke pagina's, beschrijvende bijschriften en instructietekst vormt deze knopinfo, of toelichtingen, onze huidige implementatie van *ingebouwde gebruikersondersteuning*, wat een belangrijk principe is in de huidige wereld van softwareontwerp.  

Als u een vraag hebt over een veld of een ander element van de gebruikersinterface, kies dan de naam en er verschijnt een korte beschrijving. Kies de koppeling **Copilot vragen** als dat niet genoeg is. U kunt ook het Help-venster in het product gebruiken om antwoorden op uw vragen te vinden.  

Zie voor meer informatie [Dynamics 365 Business Central-model voor gebruikersondersteuning](/dynamics365/business-central/dev-itpro/user-assistance) in de beheerinhoud voor [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="help-and-support-page"></a>Pagina Help en ondersteuning

In [!INCLUDE[prod_short](includes/prod_short.md)] geeft de menuoptie Help (het vraagteken in de rechterbovenhoek) u toegang tot de pagina **Help en ondersteuning**, waar u koppelingen vindt naar resources die u kunnen helpen antwoorden op uw vragen te vinden. Zie [Bronnen voor Help en ondersteuning](product-help-and-support.md) voor meer informatie.  

## <a name="help-others"></a>Anderen helpen

Als u een beheerder of superuser bent, kunt u anderen helpen door foutmeldingen op te zoeken op de pagina **Foutberichtregister** of in het beheercentrum. In veel gevallen gaat de waarschuwing of het foutbericht over het instellen of het ontbreken van toestemming en soortgelijke problemen waarmee de superuser of beheerder gemakkelijk kan helpen. In andere gevallen moet u mogelijk pagina's inspecteren om de oorzaak te achterhalen. Zie voor meer informatie [Technische informatie zoeken](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) in de beheerinformatie voor [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="share-error-details-for-faster-assistance"></a>Foutdetails delen voor snellere hulp

Maak gebruik van de expertise van collega's of vakexperts om obstakels te overwinnen en downtime te minimaliseren. Wanneer u wordt geblokkeerd door een fout, kunt u de foutdetails eenvoudig delen wanneer u hulp krijgt.

De details omvatten het foutbericht, de foutcode en andere informatie die nuttig is bij het oplossen van een fout. Door de foutdetails te delen, kunt u het specifieke probleem waarmee u wordt geconfronteerd effectief communiceren, zodat uw collega's u kunnen helpen.  

U kunt details kopiëren door het pictogram **Delen** in in-line validatiedialoogvensters te kiezen of het menu **Details delen** in foutdialoogvensters.  

Naast het kopiëren van foutdetails kunt u er ook voor kiezen om details te delen via Microsoft Teams door **Details delen met Teams** te kiezen om het volgende te doen:

* De foutdetails kopiëren.
* Open het venster **Delen met Teams**, waar u de foutdetails die u hebt gekopieerd, kunt plakken en kunt opgeven wie u om hulp wilt vragen. [!INCLUDE [prod_short](includes/prod_short.md)] voegt een koppeling toe naar de pagina waar u de fout hebt ondervonden, zodat het oplossen van problemen eenvoudiger wordt.

U kunt er ook voor kiezen om details per e-mail te delen door **Details delen via e-mail** te kiezen om het volgende te doen:

* De foutdetails kopiëren.
* Open uw standaard e-maileditor, waar u de foutdetails die u hebt gekopieerd, kunt plakken en kunt opgeven wie u om hulp wilt vragen. [!INCLUDE [prod_short](includes/prod_short.md)] voegt een koppeling toe naar de pagina waar u de fout bent tegengekomen.

## <a name="help-yourself"></a>Help uzelf

Foutberichten bieden informatie en acties die het gemakkelijker maken om fouten die afkomstig zijn van het platform te begrijpen, op te zoeken en op te lossen.

De foutmeldingen die het [!INCLUDE [prod_short](includes/prod_short.md)]-platform genereert, bevatten de volledige technische details, inclusief veldnamen, in de sectie **Gedetailleerde foutmelding**. Selecteer het pictogram **Details kopiëren** in inline validatiefouten of in een foutmelding om toegang te krijgen tot de technische informatie.

Acties in foutmeldingen brengen u rechtstreeks naar de pagina waar de fout door een veld wordt veroorzaakt. U hoeft geen tijd te spenderen om de pagina of het veld zelf te vinden. Kies gewoon de actie in de foutmelding en [!INCLUDE [prod_short](includes/prod_short.md)] brengt u naar de juiste locatie om de fout op te lossen.

In de volgende video ziet u hoe u bruikbare foutmeldingen kunt gebruiken om de blokkering op te heffen.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2sM]

### <a name="tip-for-developers"></a>Tip voor ontwikkelaars

Als u een ontwikkelaar bent en u de methode [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method) aanroept, maar het |`ErrorInfo`-object niet doorgeeft, genereert [!INCLUDE [prod_short](includes/prod_short.md)] automatisch de koppeling naar een pagina waar een gebruiker het probleem kan oplossen. [!INCLUDE [prod_short](includes/prod_short.md)] haalt eerst de opzoek- of drilldownpagina voor de record op, zoekt vervolgens de kaartpagina of opzoekpagina en voegt een navigatiekoppeling toe aan die kaartpagina. [!INCLUDE [prod_short](includes/prod_short.md)] voegt geen koppeling toe in de volgende situaties:

* Als de fout zich op de pagina bevindt die momenteel geopend is.
* Als de gebruiker geen machtiging heeft om de onderliggende record te wijzigen.

## <a name="see-also"></a>Zie ook

[Resources voor Help en ondersteuning](product-help-and-support.md)  
[Veelgestelde vragen](across-faq.yml)  
[Veelgestelde vragen over Vertel me](ui-search-faq.md)  
[Zoeken en filteren - Veelgestelde vragen](ui-search-filter-faq.yml)  
[Veelgestelde vragen over kopiëren en plakken](faq-copy-paste.yml)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
