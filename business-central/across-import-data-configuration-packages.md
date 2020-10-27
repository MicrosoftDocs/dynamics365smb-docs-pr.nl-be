---
title: Excel gebruiken om gegevens te importeren in Business Central
description: Gebruik het standaardconfiguratiepakket om klantgegevens in Excel toe te voegen en de gegevens weer te importeren in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 143d40c1005b3ce6b54f9a2f5abc865b3d76b361
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924690"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Bedrijfsgegevens importeren uit andere financiële systemen

Wanneer u zich registreert voor [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u ervoor kiezen een leeg bedrijf te maken zodat u uw eigen gegevens kunt uploaden en uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf kunt testen. Afhankelijk van de financiële oplossing die uw bedrijf tegenwoordig gebruikt, kunt u gegevens over klanten, leveranciers en bankrekeningen overbrengen.  

Vanuit het rolcentrum kunt u een begeleide instelling starten die u helpt de bedrijfsgegevens vanuit een Excel-bestand of vanuit andere indelingen over te brengen. Het type van de bestanden die u kunt uploaden, is afhankelijk van de extensies die beschikbaar zijn. U kunt bijvoorbeeld gegevens van QuickBooks migreren, omdat [!INCLUDE[d365fin](includes/d365fin_md.md)] een extensie bevat die de conversie van QuickBooks-gegevens uitvoert. Als u gegevens vanuit andere financiële oplossingen wilt migreren, moet u controleren of er een extensie beschikbaar is voor die oplossing of u moet vanuit Excel importeren.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat sjablonen voor rekeningen, klanten, leveranciers en voorraadartikelen die u desgewenst kunt toepassen wanneer u uw gegevens importeert.

U kunt gegevens en bepaalde transactiegegevens van andere financiële systemen importeren op basis van het standaardconfiguratiepakket in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Op de pagina **Pakketten voor configuratie** kunt u met het pakket werken om de gegevens te importeren en te valideren voordat u het pakket toepast.  

> [!TIP]  
> Het wordt aanbevolen de wizards voor gegevensmigratie te gebruiken om gegevens te importeren uit Dynamics GP, Dynamics NAV of QuickBooks. Zie voor meer informatie [On-premises gegevens migreren naar Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in de beheerinhoud of [QuickBooks-gegevensmigratie](ui-extensions-quickbooks-data-migration.md).

> [!NOTE]  
> Voor groter implementatiewerk kunt u RapidStart Services voor [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken. Dat is een uitgebreide werkset voor het instellen van nieuwe oplossingen op basis van de bedrijfsvereisten en instellingsgegevens van de klant. RapidStart Services bieden ook functionaliteit voor het importeren van bedrijfsgegevens. Zie voor meer informatie [Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Als u artikelafbeeldingen wilt importeren, kunt u een speciale functie op de pagina **Voorraadinstellingen** gebruiken. Zie voor meer informatie [Meerdere artikelafbeeldingen importeren](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Gegevens importeren uit configuratiepakketten
[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een configuratiepakket dat u naar Excel kunt exporteren, waar u dan de gegevens kunt instellen. Vervolgens kunt u de gegevens weer uit Excel importeren. Het pakket bestaat uit 27 tabellen, met hoofdgegevens zoals klanten, leveranciers, artikelen en rekeningen, overige tabellen met basisinstellingen zoals verzendmethoden en transactiestabellen zoals verkoopkoptekst en regels.  

> [!NOTE]  
>   Werken met configuratiepakketten is geavanceerde functionaliteit, en het wordt aanbevolen om hiervoor contact op te nemen met uw beheerder. Zie voor meer informatie [Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Werken met gegevens in Excel
Wanneer u het standaardconfiguratiepakket exporteert naar Excel, bevat de gegenereerde werkmap een werkblad voor elke tabel in het pakket. Om uw taken te vereenvoudigen, kunt u de XML-manipulatiehulpprogramma's gebruiken die in Excel zijn ingebouwd. U kunt ook ingebouwde functies van Excel gebruiken om te helpen met het opmaken van gegevens en deze in de correcte cel te plaatsen. Voeg bijvoorbeeld een werkblad toe en kopieer de verouderde gegevens naar het werkblad. Maak vervolgens een Excel-formule om gegevens in het transformatiewerkblad te koppelen met de velden in het geëxporteerde werkblad en de oude klantgegevens. Nadat u alle gegevens hebt gekoppeld, kopieert u het gegevensbereik naar het werkblad met de tabel.  

> [!IMPORTANT]  
>  Wijzig de kolommen in de werkbladen niet. Als ze worden verplaatst, gewijzigd of verwijderd, kan het werkblad niet worden geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Velden van het type Blob kunnen niet worden geëxporteerd/geïmporteerd met Excel.

## <a name="tables-in-the-default-configuration-package"></a>Tabellen in het standaardconfiguratiepakket
Het standaardconfiguratiepakket ondersteunt de volgende tabellen:

-   Betalingsvoorwaarden
-   Klantenprijsgroep
-   Verzendwijze
-   Verkoper/Inkoper
-   Vestiging
-   Grootboekrekening
-   Klant
-   Leverancier
-   Artikel
-   Verkoopkop
-   Verkoopregel
-   Inkoopkop
-   Inkoopregel
-   Dagb. regel
-   Artikeldagboekregel
-   Klantboekingsgroep
-   Leveranciersboekingsgroep
-   Voorraadboekingsgroep
-   Eenheid
-   Dagb. Bedrijfsboekingsgroep
-   Dagb. Productboekingsgroep
-   Boekingsgroepinstellingen
-   Regio
-   Artikelcategorie
-   Verkoopprijs
-   Inkoopprijs

## <a name="see-also"></a>Zie ook
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[On-premises gegevens migreren naar Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[QuickBooks-gegevensmigratie](ui-extensions-quickbooks-data-migration.md)  
[Meerdere artikelafbeeldingen importeren](inventory-how-import-item-pictures.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
