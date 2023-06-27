---
title: Nieuwe bedrijven maken met een begeleide instelling
description: U maakt eenvoudig een nieuw leeg bedrijf in Business Central. Een begeleide instelling helpt u door de stappen en u kunt uw bedrijfsgegevens importeren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/14/2023
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
---
# <a name="create-new-companies-in-" />Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]

In [!INCLUDE[prod_short](includes/prod_short.md)] worden de container voor bedrijfsgegevens die behoort tot een bedrijfsunit of rechtspersoon, een *bedrijf* genoemd. Wanneer u zich registreert voor [!INCLUDE[prod_short](includes/prod_short.md)], krijgt u een demonstratiebedrijf en een leeg bedrijf, *Mijn bedrijf*. Tussen bedrijven schakelen is gemakkelijk: ga naar **Mijn instellingen** en ga naar het andere bedrijf. U kunt echter ook nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)], afhankelijk van de behoeften van uw bedrijf.  

> [!NOTE]
> Om een nieuw bedrijf te maken moet u zijn toegewezen aan de machtigingenset **Super** .

Wanneer u een nieuw bedrijf maakt, helpt een begeleide instelling u de basis in te stellen. Vervolgens kunt u relevante gegevens importeren uit uw oude systeem of een ander bedrijf in [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="choose-the-right-template" />De juiste sjabloon kiezen

Als u besluit een bedrijf toe te voegen aan uw [!INCLUDE[prod_short](includes/prod_short.md)], kunt u de begeleide instelling **Nieuw bedrijf maken** gebruiken om aan de slag te gaan. The begeleide instelling is beschikbaar vanaf de pagina **Bedrijven** en via de zoekfunctie in het veld **Bedrijf** op de pagina **Mijn instellingen**.  

De begeleide instelling biedt twee sjablonen en een lege optie:

- **Evaluatie - voorbeeldgegevens**  
    Hierdoor ontstaat een bedrijf dat lijkt op het demonstratiebedrijf met voorbeeldgegevens en instellingsgegevens. Dit type bedrijf is voor u beschikbaar zonder over te stappen naar een proefperiode van 30 dagen, zoals bij de andere typen het geval is.  
- **Productie - Alleen instellingsgegevens**  
    Hierdoor ontstaat een bedrijf dat lijkt op **Mijn bedrijf**, met instellingsgegevens maar zonder voorbeeldgegevens. U kunt dit bedrijf gedurende een proefperiode van 30 dagen gebruiken.  
- **Nieuw maken - Geen gegevens**  
    Hierdoor ontstaat een leeg bedrijf zonder instellingsgegevens. U kunt dit bedrijf gedurende een proefperiode van 30 dagen gebruiken.  

Als u eenvoudig aan de slag wilt gaan met een nieuw bedrijf, kiest u **Productie - Alleen instellingsgegevens** en importeert u uw eigen bedrijfsgegevens, zoals klanten, artikelen, en leveranciers. Kies de sjabloon **Nieuw** als u alles nieuw wilt instellen. In dat geval kunt u de begeleide instelling **Bedrijfsinstelling** gebruiken om u te helpen aan de slag te gaan met essentiële instellingsgegevens.  

> [!NOTE]  
> Wanneer u een nieuw bedrijf maakt, duurt het enkele minuten voordat u er toegang toe kunt krijgen in [!INCLUDE[prod_short](includes/prod_short.md)]. De instellingsstatus op de pagina **Bedrijven** toont wanneer het nieuwe bedrijf gereed voor u is. Vervolgens kunt u naar het nieuwe bedrijf overschakelen door **Mijn instellingen** te kiezen.  

Tijdens uw proef van 30 dagen kunt u een willekeurig aantal nieuwe bedrijven maken, maar deze zijn alleen tijdens de proef beschikbaar. Neem voor meer informatie contact op met uw [!INCLUDE[prod_short](includes/prod_short.md)]-partner. Zie ook het artikel [Veelgestelde vragen over de proefversie van Dynamics 365 Business Central](trial-faq.md).  

Uw beheerder kan [hier](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions) meer te weten komen over proefversies en abonnementen.  

## <a name="copy-a-company" />Een bedrijf kopiëren

Op de pagina **Bedrijven** kunt u de actie **Kopiëren** gebruiken om een tweede bedrijf te maken op basis van de inhoud van een bestaand bedrijf. Dit is bijvoorbeeld handig als u een bedrijf wilt testen zonder de productiegegevens te verstoren.

> [!Important]
> Gebruik de kopieeractie niet om een back-up van een bedrijf te maken. Als u een back-up wilt maken, moet u eerst de database als een .bacpac-bestand exporteren. Zie [Databases exporteren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) in de Help voor ontwikkeling en beheer voor meer informatie.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="set-up-the-company" />Het bedrijf instellen

Als u zich aanmeldt bij een nieuw bedrijf, wordt de wizard **Bedrijfsinstelling** automatisch uitgevoerd en wordt u geholpen aan de slag te gaan. U wordt gevraagd om gegevens over uw bedrijf, zoals het adres, de bankgegevens en de voorraadwaarderingsmethode. We vragen deze informatie omdat deze wordt gebruikt als basis voor veel gebieden in [!INCLUDE[prod_short](includes/prod_short.md)], die u vervolgens later niet handmatig hoeft in te stellen.  

Bijvoorbeeld, [!INCLUDE [prod_short](includes/prod_short.md)] neemt uw bedrijfsadres op in facturen en andere documenten en uw bankgegevens in betalingen. De kostprijsberekeningsmethode wordt gebruikt om prijzen en voorraadwaardering te berekenen.  

Nadat u de basis hebt ingesteld, kunt u resterende kerngebieden instellen. Vervolgens bent u klaar om bedrijfsgegevens, zoals klanten en leveranciers, toe te voegen. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md) instellen.  

## <a name="companies-and-environments" />Bedrijven en omgevingen

[!INCLUDE [company_environment](includes/company_environment.md)]

Zie voor meer informatie [Overstappen naar een ander bedrijf of een andere omgeving](ui-organization-switch.md). Zie [Understanding the Infrastructure of Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (uitsluitend in het Engels) voor meer informatie over omgevingen.  

## <a name="changing-a-companys-name" />De naam van een bedrijf wijzigen

Als een bedrijf eenmaal is gemaakt, kunt u de naam ervan niet meer wijzigen. Maar u kunt de **weergavenaam** ervan wijzigen. Dat is tekst die in de toepassing voor het bedrijf wordt weergegeven.  

> [!TIP]
> U kunt een bedrijf hernoemen als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt.

## <a name="add-contoso-coffee" />Contoso Coffee toevoegen

De Contoso Coffee-app biedt demonstratiegegevens waarmee u de geavanceerde mogelijkheden van [!INCLUDE [prod_short](includes/prod_short.md)] kunt verkennen. Zoek de app in AppSource en installeer deze in een leeg bedrijf, bijvoorbeeld een bedrijf in een sandbox-omgeving. Zie [Inleiding tot demogegevens van Contoso Coffee](contoso-coffee/contoso-coffee-intro.md) voor meer informatie.  

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/modules/create-new-companies-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Business Central aanpassen](ui-customizing-overview.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Understanding the Infrastructure of Business Central Online (uitsluitend in het Engels)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
