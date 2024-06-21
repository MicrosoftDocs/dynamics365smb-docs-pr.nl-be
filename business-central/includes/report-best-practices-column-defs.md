---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

## <a name="best-practices-for-working-with-column-definitions"></a>Best practices voor het werken met kolomdefinities

Er is geen versiebeheer voor kolomdefinities. Wanneer u een kolomdefinitie wijzigt, wordt de oude versie vervangen wanneer uw wijziging in de database wordt opgeslagen. De volgende lijst bevat enkele best practices voor het werken met kolomdefinities.

- Als u een kolomdefinitie toevoegt, kiest u een goede code en vult u het veld Beschrijving in met een betekenisvolle tekst, terwijl u nog weet waarvoor u de kolomdefinitie gebruikt. Deze informatie helpt uw collega's (en uzelf in de toekomst) om met financiële rapportage te werken en eventueel de kolomdefinitie te wijzigen.
- Voordat u een kolomdefinitie wijzigt, kunt u overwegen er een kopie van te maken als back-up, voor het geval uw wijziging niet werkt zoals verwacht. U kunt de definitie gewoon kopiëren (geef deze een goede naam) of exporteren. Als u meer wilt weten, gaat u naar [Kolomdefinities importeren of exporteren](#import-or-export-financial-report-column-definitions).
- Als u een nieuwe kopie nodig heeft van een definitie die [!INCLUDE [prod_short](prod_short.md)] voorziet, kunt u er eenvoudig een krijgen door een nieuw bedrijf op te richten dat alleen instellingsgegevens bevat. Exporteer vervolgens de definitie en importeer deze in het bedrijf waar de definitie moet worden vernieuwd.
