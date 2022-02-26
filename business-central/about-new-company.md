---
title: Nieuwe bedrijven maken met een begeleide instelling
description: U maakt eenvoudig een nieuw leeg bedrijf in Business Central. Een begeleide instelling helpt u door de stappen en u kunt uw bestaande bedrijfsgegevens importeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.search.form: 1803
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8c0c9f03dada569ec19a4bf38d9d4fced1469c2b
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011425"
---
# <a name="creating-new-companies-in-prod_short"></a>Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]

In [!INCLUDE[prod_short](includes/prod_short.md)] worden de container voor bedrijfsgegevens die behoort tot een bedrijfsunit of rechtspersoon, een *bedrijf* genoemd. Wanneer u zich registreert voor [!INCLUDE[prod_short](includes/prod_short.md)], krijgt u een demonstratiebedrijf en een leeg bedrijf, *Mijn bedrijf*. Tussen bedrijven schakelen is gemakkelijk: ga naar **Mijn instellingen** en ga naar het andere bedrijf. U kunt echter ook nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)], afhankelijk van de behoeften van uw bedrijf. Wanneer u een nieuw bedrijf maakt, helpt een begeleide instelling u de basis in te stellen. Vervolgens kunt u relevante gegevens importeren uit uw oude systeem of een ander bedrijf in [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="creating-a-new-company"></a>Een nieuw bedrijf maken

Als u besluit een bedrijf toe te voegen aan uw [!INCLUDE[prod_short](includes/prod_short.md)], kunt u de begeleide instelling **Nieuw bedrijf maken** gebruiken om aan de slag te gaan. The setupwizard is beschikbaar via de pagina **Bedrijven** en via de zoekfunctie in het veld **Bedrijf** op de pagina **Mijn instellingen**.  

De installatiewizard biedt drie sjablonen en een lege optie:

- **Evaluatie - Voorbeeldgegevens**  
    Hierdoor ontstaat een bedrijf dat lijkt op het demonstratiebedrijf met voorbeeldgegevens en instellingsgegevens.  
- **Productie - Alleen instellingsgegevens**  
    Hierdoor ontstaat een bedrijf dat lijkt op **Mijn bedrijf**, met instellingsgegevens maar zonder voorbeeldgegevens.
- **Geavanceerde evaluatie - Volledige voorbeeldgegevens** Hiermee wordt een bedrijf gemaakt met instellingsgegevens en volledige voorbeeldgegevens voor alle functies, inclusief Productie en Servicebeheer.
- **Nieuw maken - Geen gegevens**  
    Hierdoor ontstaat een leeg bedrijf zonder instellingsgegevens.  

Als u eenvoudig aan de slag wilt gaan met een nieuw bedrijf, kiest u **Productie - Alleen instellingsgegevens** en importeert u uw eigen bedrijfsgegevens, zoals klanten, artikelen, en leveranciers. Kies de sjabloon **Nieuw** als u alles nieuw wilt instellen. In dat geval kunt u de begeleide instelling **Bedrijfsinstelling** gebruiken om u te helpen aan de slag te gaan met essentiële instellingsgegevens.  

> [!NOTE]  
> Wanneer u een nieuw bedrijf maakt, duurt het enkele minuten voordat u er toegang toe kunt krijgen in [!INCLUDE[prod_short](includes/prod_short.md)]. De instellingsstatus op de pagina **Bedrijven** toont wanneer het nieuwe bedrijf gereed voor u is. Vervolgens kunt u naar het nieuwe bedrijf overschakelen door **Mijn instellingen** te kiezen.  

Tijdens uw proef van 30 dagen kunt u een willekeurig aantal nieuwe bedrijven maken, maar deze zijn alleen tijdens de proef beschikbaar. Neem voor meer informatie contact op met uw [!INCLUDE[prod_short](includes/prod_short.md)]-partner.  

## <a name="copying-a-company"></a>Een bedrijf kopiëren

Op de pagina **Bedrijven** kunt u de actie **Kopiëren** gebruiken om een tweede bedrijf te maken op basis van de inhoud van een bestaand bedrijf. Dit is bijvoorbeeld handig als u een bedrijf wilt testen zonder de productiegegevens te verstoren.

> [!Important]
> U kunt deze functie niet gebruiken om de back-up van een bedrijf te nemen. Als u de back-up van een bedrijf wilt nemen, moet u eerst de database als een .bacpac-bestand exporteren. Zie [Databases exporteren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) in de Help voor ontwikkeling en beheer voor meer informatie.

## <a name="company-setup"></a>Bedrijfsinstelling

Als u zich aanmeldt bij een nieuw bedrijf, wordt de wizard **Bedrijfsinstelling** automatisch uitgevoerd en wordt u geholpen aan de slag te gaan. U wordt gevraagd om gegevens over uw bedrijf, zoals het adres, de bankgegevens en de voorraadwaarderingsmethode. We vragen deze informatie omdat deze wordt gebruikt als basis voor veel gebieden in [!INCLUDE[prod_short](includes/prod_short.md)] die u vervolgens later niet handmatig hoeft in te stellen.  

Uw bedrijfsadres wordt bijvoorbeeld opgenomen in facturen en andere documenten, uw bankgegevens worden gebruikt in betalingen en de waarderingsmethode wordt gebruikt om prijzen en voorraadwaarde te berekenen.  

Nadat u de basis hebt ingesteld, kunt u resterende kerngebieden instellen. Vervolgens bent u klaar om bedrijfsgegevens, zoals klanten en leveranciers, toe te voegen. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] instellen](setup.md).  

## <a name="companies-and-environments"></a>Bedrijven en omgevingen

[!INCLUDE [company_environment](includes/company_environment.md)]

Zie voor meer informatie [Overstappen naar een ander bedrijf of een andere omgeving](ui-organization-switch.md). 

## <a name="changing-a-companys-name"></a>De naam van een bedrijf wijzigen

Als een bedrijf eenmaal is gemaakt, kunt u de naam ervan niet meer wijzigen. Maar u kunt de **weergavenaam** ervan wijzigen. Dat is tekst die in de toepassing voor het bedrijf wordt weergegeven.  

> [!TIP]
> U kunt een bedrijf hernoemen als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt.

## <a name="see-also"></a>Zie ook

[Business Central aanpassen](ui-customizing-overview.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]