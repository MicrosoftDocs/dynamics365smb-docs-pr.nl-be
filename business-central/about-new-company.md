---
title: Nieuwe bedrijven maken met een begeleide instelling | Microsoft Docs
description: U maakt eenvoudig een nieuw leeg bedrijf in Business Central. Een begeleide instelling helpt u door de stappen en u kunt uw bestaande bedrijfsgegevens importeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 11/01/2019
ms.author: edupont
ms.openlocfilehash: 70bd78244c4d8570a5e9b8fbe2d1e8a4c74d7530
ms.sourcegitcommit: 49309bdff9b680a35032b355fe97c565845dba15
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2695131"
---
# <a name="creating-new-companies-in-d365fin"></a>Nieuwe bedrijven maken in [!INCLUDE[d365fin](includes/d365fin_md.md)]
In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden de containers voor bedrijfsgegevens die behoren tot een bedrijfsunit of rechtspersoon, een *bedrijf* genoemd. Wanneer u zich registreert voor [!INCLUDE[d365fin](includes/d365fin_md.md)], krijgt u een demonstratiebedrijf en een leeg bedrijf, *Mijn bedrijf*. Tussen bedrijven schakelen is gemakkelijk: ga naar **Mijn instellingen** en ga naar het andere bedrijf. U kunt echter ook nieuwe bedrijven maken in [!INCLUDE[d365fin](includes/d365fin_md.md)], afhankelijk van de behoeften van uw bedrijf. Wanneer u een nieuw bedrijf maakt, helpt een begeleide instelling u de basis in te stellen. Vervolgens kunt u relevante gegevens importeren uit uw oude systeem of een ander bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="creating-a-new-company"></a>Een nieuw bedrijf maken
Als u besluit een bedrijf toe te voegen aan uw [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u de begeleide instelling **Nieuw bedrijf maken** gebruiken om aan de slag te gaan. The setupwizard is beschikbaar via de pagina **Bedrijven** en via de zoekfunctie in het veld **Bedrijf** op de pagina **Mijn instellingen**.  

De instellingswizard biedt drie sjablonen:

-   **Evaluatie - Voorbeeldgegevens**  
    Hierdoor ontstaat een bedrijf dat lijkt op het demonstratiebedrijf met voorbeeldgegevens en instellingsgegevens.  
-   **Productie - Alleen instellingsgegevens**  
    Hierdoor ontstaat een bedrijf dat lijkt op **Mijn bedrijf**, met instellingsgegevens maar zonder voorbeeldgegevens.
-   **Geavanceerde evaluatie - Volledige voorbeeldgegevens** Hiermee wordt een bedrijf gemaakt met instellingsgegevens en volledige voorbeeldgegevens voor alle functies, inclusief Productie en Servicebeheer.
-   **Nieuw maken - Geen gegevens**  
    Hierdoor ontstaat een leeg bedrijf zonder instellingsgegevens.  

Als u eenvoudig aan de slag wilt gaan met een nieuw bedrijf, kiest u **Productie - Alleen instellingsgegevens** en importeert u uw eigen bedrijfsgegevens, zoals klanten, artikelen, en leveranciers. Kies de sjabloon **Nieuw** als u alles nieuw wilt instellen. In dat geval kunt u de begeleide instelling **Bedrijfsinstelling** gebruiken om u te helpen aan de slag te gaan met essentiële instellingsgegevens.  

> [!NOTE]  
>   Wanneer u een nieuw bedrijf maakt, duurt het enkele minuten voordat u er toegang toe kunt krijgen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. De instellingsstatus op de pagina **Bedrijven** toont wanneer het nieuwe bedrijf gereed voor u is. Vervolgens kunt u naar het nieuwe bedrijf overschakelen door **Mijn instellingen** te kiezen.  

Tijdens uw proef van 30 dagen kunt u een willekeurig aantal nieuwe bedrijven maken, maar deze zijn alleen tijdens de proef beschikbaar. Neem voor meer informatie contact op met uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner.  

## <a name="copying-a-company"></a>Een bedrijf kopiëren
Op de pagina **Bedrijven** kunt u de actie **Kopiëren** gebruiken om een tweede bedrijf te maken op basis van de inhoud van een bestaand bedrijf. Dit is bijvoorbeeld handig als u een bedrijf wilt testen zonder de productiegegevens te verstoren.

> [!Important]
> U kunt deze functie niet gebruiken om de back-up van een bedrijf te nemen. Als u de back-up van een bedrijf wilt nemen, moet u eerst de database als een .bacpac-bestand exporteren. Zie [Databases exporteren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.

## <a name="company-setup"></a>Bedrijfsinstelling
Als u zich aanmeldt bij een nieuw bedrijf, wordt de wizard **Bedrijfsinstelling** automatisch uitgevoerd en wordt u geholpen aan de slag te gaan. U wordt gevraagd om gegevens over uw bedrijf, zoals het adres, de bankgegevens en de voorraadwaarderingsmethode. We vragen deze informatie omdat deze wordt gebruikt als basis voor veel gebieden in [!INCLUDE[d365fin](includes/d365fin_md.md)] die u vervolgens later niet handmatig hoeft in te stellen.  

Uw bedrijfsadres wordt bijvoorbeeld opgenomen in facturen en andere documenten, uw bankgegevens worden gebruikt in betalingen en de waarderingsmethode wordt gebruikt om prijzen en voorraadwaarde te berekenen.  

Nadat u de basis hebt ingesteld, kunt u resterende kerngebieden instellen. Vervolgens bent u klaar om bedrijfsgegevens, zoals klanten en leveranciers, toe te voegen. Zie voor meer informatie [[!INCLUDE[d365fin](includes/d365fin_md.md)] instellen](setup.md).  

## <a name="see-also"></a>Zie ook
[Business Central aanpassen](ui-customizing-overview.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Aan de slag](product-get-started.md)  
