---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: acde432acabc2d3e73658b0e916d6e4830ccaf52
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104408"
---
De volgende tabel beschrijft enkele van de belangrijkste rapporten in vaste-activarapportage.

| Rapport | Object-id | Omschrijving |
|--|--|--|
| **Overzicht van vaste activa** | 5601 | Toont de lijst met vaste activa en hun instellingsinformatie voor een bepaald afschrijvingsboek. |
| **Vast activum - Overzicht aanschafkosten** | 5608 | Maak een lijst van alle activa die binnen een bepaald datumbereik zijn verworven. U kunt ook vaste activa opnemen die zijn gemaakt maar nog niet zijn verworven. |
| **Details van vaste activa** | 5604 | Toont de vaste-activagrootboekposten voor vaste activa. |
| **Analyse van vaste activa** | 5600 | Een analyserapport waarin u twee datumkolommen en drie gegevenskolommen kunt specificeren om in het rapport te zien. Als u bijvoorbeeld een rapport wilt genereren om te gebruiken voor afstemming met het grootboek, voegt u kolommen toe voor aanschafkosten op einddatum, afschrijving op einddatum en boekwaarde op einddatum. Een controlerapport kan acquisities/mutaties, afwaardering/mutaties en waardevermeerdering/mutaties bevatten, zodat elke wijziging in vaste activa indien nodig kan worden gecontroleerd. Als u het veld **Budgetrapport** selecteert en een einddatum in de toekomst specificeert, berekent het rapport de toekomstige afschrijving en kan het schattingen geven voor toekomstige afschrijvingen en boekwaarden, als u die velden als rapportkolommen hebt geselecteerd. |
| **Geschatte waarde van vaste activa** | 5607 | Toont de verwachte afschrijvingsbedragen en boekwaarde voor een toekomstige periode voor activa. Het rapport is handig wanneer u verschillende afschrijvingsmethoden voor uw activa gebruikt en bijvoorbeeld de afschrijving van volgend jaar wilt schatten. Gebruik het rapport om de budgetbedragen voor afschrijving te creëren door een budget en het veld **Kopiëren naar budget** te selecteren. |
| **Vast activum - Boekwaarde 01** | 5605 | Bevat gedetailleerde informatie over aanschafkosten, afschrijvingswaarde en boekwaarde voor zowel individuele activa als groepen activa. Voor elk van deze drie bedragsoorten worden de bedragen aan het eind en aan het begin van een opgegeven periode berekend, en voor de periode zelf. Als u het veld **Budgetrapport** selecteert, berekent het rapport de verwachte afschrijving voor de periode. Voer een *groepstype* in als de vaste activa in de lijst moeten worden gegroepeerd en de groepstotalen moeten worden afgedrukt. Als u bijvoorbeeld zes VA-categorieën hebt ingesteld, selecteert u de optie *VA-categorie* om de groepstotalen voor elk van de zes categorieën af te drukken.|
| **Vast activum - Boekwaarde 02** | 5606 |Toont de uitsplitsing van de boekwaarde van vaste activa naar veranderingen in verwerving, afschrijving en waardevermeerdering binnen de periode met een verdere uitsplitsing naar toevoegingen en buitengebruikstellingen binnen de periode. Gebruik dit rapport om de veranderingen in vaste activa te beschrijven voor een bepaalde periode waarin veel verschillende veranderingen optreden in de groepering van vaste activa. Als u het veld **Budgetrapport** selecteert, berekent het rapport de verwachte afschrijving voor de periode. Voer een *groepstype* in als de vaste activa in de lijst moeten worden gegroepeerd en de groepstotalen moeten worden afgedrukt. Als u bijvoorbeeld zes VA-categorieën hebt ingesteld, selecteert u de optie *VA-categorie* om de groepstotalen voor elk van de zes categorieën af te drukken. |
| **GB-analyse van vaste activa**| 5610 |Bevat een analyse van uw vaste activa (VA), met diverse soorten gegevens voor zowel individuele activa als groepen activa. Op het sneltabblad Vast activum kunt u filters instellen als u alleen bepaalde vaste activa in de lijst wilt opnemen. Pas het rapport op het sneltabblad Opties aan uw specifieke behoeften aan. Het rapport is vergelijkbaar met het rapport **Analyse vaste activa**, maar specifiek voor afstemming met het grootboek en specifiek voor het valideren van de buitengebruikstellingsposten. Het rapport gaat ervan uit dat u de grootboekrekeningen kent die zijn opgegeven in de boekingsinstellingen. |
| **Vast activum - Journaal** |5603  |Bevat geboekte VA-posten, gesorteerd en onderverdeeld op journaalnummer. Door een filter in te stellen kunt u precies bepalen welke journaalposten u wilt bekijken. Als er veel posten aanwezig zijn en u geen filters plaatst, zal de lijst zeer veel informatie bevatten. |

