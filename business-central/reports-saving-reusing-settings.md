---
title: Opgeslagen instellingen wijzigen en toepassen | Microsoft Docs
description: Beschrijft het gebruik van vooraf gedefinieerde opties en filters om een lijst aan te passen en de juiste gegevens te genereren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: 2a7ab137a9bf8ec3580e718053f8e67320e3af5a
ms.contentlocale: nl-be
ms.lasthandoff: 08/06/2018

---
# <a name="managing-saved-settings-on-reports"></a>Opgeslagen instellingen in rapporten beheren
Wanneer gebruikers rapporten uitvoeren, zien ze meestal een pagina waarmee ze bepaalde opties en filters kunnen instellen om de gegevens te wijzigen die in het gegenereerde rapport worden opgenomen. Deze pagina wordt de rapportaanvraagpagina genoemd. Een rapport kan een of meer *opgeslagen instellingen* bevatten die gebruikers op het rapport kunnen toepassen vanaf de aanvraagpagina. *Opgeslagen instellingen* zijn in wezen vooraf gedefinieerde opties en filters. Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten. Voor meer informatie over hoe opgeslagen instellingen worden gebruikt, raadpleegt u [Opgeslagen instellingen gebruiken](ui-work-report.md#SavedSettings).

Als u de juiste machtigingen hebt, kunt u de opgeslagen instellingen voor alle gebruikers in een bedrijf weergeven, maken en wijzigen. U kunt opgeslagen instellingen voor een rapport toewijzen aan afzonderlijke gebruikers of aan alle gebruikers in het bedrijf.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Opgeslagen instellingen maken en wijzigen voor alle gebruikers
U beheert opgeslagen instellingen vanaf pagina 1560 **Rapportinstellingen**. Er zijn twee manieren om deze pagina te openen:
-   Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportinstellingen** in en kies de gerelateerde koppeling.
-   Open een rapport, kies de opzoekactie naast het vak **Standaardwaarden gebruiken uit**, kies **Selecteren vanuit volledige lijst**.

De pagina bevat alle bestaande opgeslagen instellingsvermeldingen voor alle gebruikers. Als er een gebruikersnaam in de kolom **Toegewezen aan** staat, kan alleen deze gebruiker de opgeslagen instellingen voor het corresponderende rapport gebruiken. Als er een selectievakje in de kolom **Gedeeld met alle gebruikers** staat, kunnen alle gebruikers de opgeslagen instellingen voor het rapport gebruiken.

Vanaf de pagina **Rapportinstellingen** kunt u het volgende doen:
-   **Nieuw** kiezen om een geheel nieuwe vermelding met opgeslagen instellingen te maken.
-   Een vermelding met opgeslagen instellingen selecteren en **Kopiëren** kiezen om een kopie te maken.
-   Een vermelding met opgeslagen instellingen in de lijst selecteren en **Bewerken** kiezen om een vermelding met opgeslagen instellingen te wijzigen.


> [!Important]
> Denk na over de naam die u een vermelding met opgeslagen instellingen geeft. Als u een vermelding met opgeslagen instellingen voor alle gebruikers maakt en deze dezelfde naam geeft als een bestaande vermelding met opgeslagen instellingen die aan één specifieke gebruiker is toegewezen, kan die gebruiker de vermelding met opgeslagen instellingen die aan iedereen is toegewezen, niet gebruiken.  Onder **Opgeslagen instellingen** op de rapportaanvraagpagina ziet de gebruiker twee vermeldingen met opgeslagen instellingen met dezelfde naam. Ongeacht welke optie de gebruiker echter kiest, de gebruikersspecifieke vermelding met opgeslagen instellingen wordt gebruikt.

> [!NOTE]
> De functie voor opgeslagen instellingen is alleen beschikbaar voor rapporten waarvoor de [eigenschap SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) van de rapportaanvraagpagina is ingesteld op `Yes`. De eigenschap **SaveValues** wordt ingesteld in de ontwikkelomgeving.  

## <a name="see-also"></a>Zie ook
[Werken met rapporten](ui-work-report.md)  

