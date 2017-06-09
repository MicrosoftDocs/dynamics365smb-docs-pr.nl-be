---
title: Excel gebruiken om verouderde gegevens in Financials op te halen | Microsoft Docs
description: Gebruik het standaardconfiguratiepakket om klantgegevens in Excel toe te voegen en weer in Dynamics 365 for Financials te importeren.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0151b1c3d8bddd4692c494d1c0e5d1c036da424e
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket.
U kunt gegevens en bepaalde transactiegegevens van andere financiële systemen importeren op basis van het standaardconfiguratiepakket in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In het venster **Pakketten voor configuratie** kunt u met het pakket werken om de gegevens te importeren en te valideren voordat u het pakket toepast.  

Als u vertrouwd bent met RapidStart-services voor Microsoft Dynamics, zijn configuratiezendingen ook bekend voor u. Het standaardconfiguratiepakket ondersteunt de vaakst gebruikte soorten gegevens die u van een verouderd systeem wilt importeren. In Excel kunt u de gegevens vervolgens van het verouderde systeem toevoegen en instellen op basis van de bedrijfslogica van [!INCLUDE[d365fin](includes/d365fin_md.md)]  

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

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
