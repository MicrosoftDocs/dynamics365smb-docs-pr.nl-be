---
title: Opgeslagen instellingen beheren voor rapporten en batchtaken
description: Hier wordt beschreven hoe de beheerder vooraf gedefinieerde opties en filters voor een rapport kan instellen en deze instellingen kan delen met een of alle gebruikers.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Opgeslagen instellingen beheren voor rapporten en batchtaken

Wanneer gebruikers rapporten uitvoeren, zien ze meestal een pagina waarmee ze opties kunnen selecteren en filters kunnen instellen om de gegevens te wijzigen die in het gegenereerde rapport worden opgenomen. Deze pagina wordt de *aanvraagpagina* genoemd. Een rapport kan een of meer *opgeslagen instellingen* bevatten die gebruikers op het rapport kunnen toepassen vanaf de aanvraagpagina. *Opgeslagen instellingen* zijn in wezen vooraf gedefinieerde opties en filters. Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten. Zie voor meer informatie [Opgeslagen instellingen gebruiken](ui-work-report.md#SavedSettings).

> [!NOTE]
> Dit onderwerp verwijst hoofdzakelijk naar *rapporten*, maar soortgelijke informatie geldt voor *batchverwerkingen*.

Als u de juiste machtigingen hebt, kunt u de opgeslagen instellingen voor alle gebruikers in een bedrijf weergeven, maken en wijzigen. U kunt opgeslagen instellingen voor een rapport toewijzen aan afzonderlijke gebruikers of aan alle gebruikers in het bedrijf.

## <a name="manage-saved-settings"></a>Opgeslagen instellingen beheren

U beheert opgeslagen instellingen op de pagina **Rapportinstellingen**. Er zijn twee manieren om deze pagina te openen:

- Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rapportinstellingen** in en kies vervolgens de gerelateerde koppeling.
- Kies op de aanvraagpagina van een rapport de opzoekactie in het veld **Standaardwaarden gebruiken uit** en kies vervolgens de actie **Selecteren vanuit volledige lijst**.

    Dit veld is alleen zichtbaar als u het rapport minimaal één keer eerder hebt uitgevoerd. De lijst toont alleen instellingen die voor u beschikbaar zijn, hetzij omdat het uw eigen instellingen zijn, hetzij omdat de instellingen met u worden gedeeld.

De pagina **Rapportinstellingen** bevat alle bestaande opgeslagen instellingsvermeldingen voor alle gebruikers. Als er een gebruikersnaam in het veld **Toegewezen aan** staat, kan alleen deze gebruiker de opgeslagen instellingen voor het corresponderende rapport gebruiken. Als er een vinkje in het veld **Gedeeld met alle gebruikers** staat, kunnen alle gebruikers de opgeslagen instellingen voor het rapport gebruiken.  

> [!TIP]
> Wanneer een gebruiker een rapport heeft uitgevoerd dat gedeelde instellingen ondersteunt, worden hun instellingen opgeslagen en aan deze lijst toegevoegd. In de meeste gevallen kan de beheerder die instellingen vervolgens bewerken en ervoor kiezen om de instellingen met alle gebruikers te delen.
>
> In sommige gevallen kunnen instellingen echter niet worden gedeeld en kan de beheerder ze ook niet wijzigen. De meeste batchtaken ondersteunen geen gedeelde instellingen.  

## <a name="create-or-modify-saved-settings-for-all-users"></a>Opgeslagen instellingen maken of wijzigen voor alle gebruikers

Vanaf de pagina **Rapportinstellingen** kunt u het volgende doen:

- Kies de actie **Nieuw** om een nieuwe vermelding met opgeslagen instellingen te maken.
- Selecteer een vermelding met opgeslagen instellingen en kies de actie **Kopiëren** om een kopie te maken.
- Selecteer een vermelding met opgeslagen instellingen in de lijst en kies de actie **Bewerken** om een vermelding met opgeslagen instellingen te wijzigen.

> [!Important]
> Denk na over de naam die u een vermelding met opgeslagen instellingen geeft. Als u een vermelding met opgeslagen instellingen voor alle gebruikers maakt en deze dezelfde naam geeft als een bestaande vermelding met opgeslagen instellingen die aan één specifieke gebruiker is toegewezen, kan die gebruiker de vermelding met opgeslagen instellingen die aan iedereen is toegewezen, niet gebruiken.  In de sectie **Opgeslagen instellingen** op de aanvraagpagina ziet de gebruiker twee vermeldingen met opgeslagen instellingen met dezelfde naam. Ongeacht welke optie de gebruiker echter kiest, de gebruikersspecifieke vermelding met opgeslagen instellingen wordt gebruikt.

> [!NOTE]
> De mogelijkheid om instellingen op te slaan, is alleen beschikbaar voor rapporten waarvoor de [eigenschap SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) van de rapportaanvraagpagina is ingesteld op **Ja**. De eigenschap **SaveValues** wordt ingesteld door de ontwikkelaar.  

## <a name="see-also"></a>Zie ook

[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
