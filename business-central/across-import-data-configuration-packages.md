---
title: Excel gebruiken om gegevens in Financials te importeren | Microsoft Docs
description: Gebruik het standaardconfiguratiepakket om klantgegevens in Excel toe te voegen en weer in Business Central te importeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket.
U kunt gegevens en bepaalde transactiegegevens van andere financiële systemen importeren op basis van het standaardconfiguratiepakket in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In het venster **Pakketten voor configuratie** kunt u met het pakket werken om de gegevens te importeren en te valideren voordat u het pakket toepast.  

> [!NOTE]  
> Voor groter implementatiewerk kunt u RapidStart Services voor [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken. Dat is een uitgebreide werkset voor het instellen van nieuwe oplossingen op basis van de bedrijfsvereisten en instellingsgegevens van de klant. RapidStart Services bieden ook functionaliteit voor het importeren van bedrijfsgegevens. Zie voor meer informatie [Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

> [!TIP]  
>   U kunt ook gegevensmigratiewizards gebruiken om gegevens in QuickBooks of Dynamics GP te importeren. Zie voor meer informatie [QuickBooks-gegevensmigratie](ui-extensions-quickbooks-data-migration.md) of [Dynamics GP-gegevensmigratie](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="working-with-data-in-excel"></a>Werken met gegevens in Excel
Wanneer u het standaardconfiguratiepakket exporteert naar Excel, bevat de gegenereerde werkmap een werkblad voor elke tabel in het pakket. Om uw taken te vereenvoudigen, kunt u de XML-manipulatiehulpprogramma's gebruiken die in Excel zijn ingebouwd. U kunt ook ingebouwde functies van Excel gebruiken om te helpen met het opmaken van gegevens en deze in de correcte cel te plaatsen. Voeg bijvoorbeeld een werkblad toe en kopieer de verouderde gegevens naar het werkblad. Maak vervolgens een Excel-formule om gegevens in het transformatiewerkblad te koppelen met de velden in het geëxporteerde werkblad en de oude klantgegevens. Nadat u alle gegevens hebt gekoppeld, kopieert u het gegevensbereik naar het werkblad met de tabel.  

> [!IMPORTANT]  
>  Wijzig de kolommen in de werkbladen niet. Als ze worden verplaatst, gewijzigd of verwijderd, kan het werkblad niet worden geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)].

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
-   Fin. dagboekregel
-   Artikeldagboekregel
-   Klantboekingsgroep
-   Leveranciersboekingsgroep
-   Voorraadboekingsgroep
-   Eenheid
-   Bedrijfsboekingsgroep
-   Productboekingsgroep
-   Boekingsgroepinstellingen
-   Regio
-   Artikelcategorie
-   Verkoopprijs
-   Inkoopprijs

## <a name="importing-customer-data"></a>Klantgegevens importeren
Nadat de klantgegevens zijn ingevoerd in Excel, importeert u de gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In het venster **Pakketten voor configuratie** importeert u de gegevens van het Excel-bestand, en kunt u controleren of de gegevens consistent zijn met [!INCLUDE[d365fin](includes/d365fin_md.md)] voordat u het pakket toepast.

## <a name="see-also"></a>Zie ook
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks-gegevensmigratie](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP-gegevensmigratie](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

