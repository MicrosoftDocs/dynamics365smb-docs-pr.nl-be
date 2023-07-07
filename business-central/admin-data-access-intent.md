---
title: Databasetoegangsintentie beheren in Business Central
description: 'Wijzig de databasetoegangsintentie voor rapporten, API-pagina''s en query''s.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9880
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="managing-database-access-intent"></a>Databasetoegangsintentie beheren

Als supergebruiker of beheerder kunt u de databasetoegangsintentie voor rapporten, pagina's van het type API en query's wijzigen om de prestaties van de service te verbeteren.

## <a name="overview"></a>Overzicht

[!INCLUDE[prod_short](includes/prod_short.md)] kan worden ingesteld om alleen-lezen replica's van de primaire (lezen-schrijven) database te gebruiken. Het gebruik van de databasereplica vermindert de belasting van de primaire database. In sommige gevallen verbetert het ook de prestaties bij het bekijken van gegevens in de client. Replica's zijn gunstig voor objecten, zoals rapporten, query's en API-pagina's, die alleen worden gebruikt voor het bekijken van gegevens en niet voor het wijzigen van gegevens.

Wanneer objecten worden uitgevoerd, bepaalt de databasetoegangsintentie of een alleen-lezen replica, indien beschikbaar, of de primaire database moet worden gebruikt. Rapporten, API-pagina's en query's worden ontwikkeld met een vooraf gedefinieerde databasetoegangsintentie (zie [eigenschap DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Met de pagina **Lijst met intenties voor databasetoegang** kunt u de vooraf gedefinieerde intentie voor databasetoegang voor objecten overschrijven wanneer ze worden uitgevoerd.

In databasetermen staat deze functie algemeen bekend als *read scale-out*. Voor meer informatie over read scale-out en datatoegangsintentie in [!INCLUDE[prod_short](includes/prod_short.md)] raadpleegt u [Read scale-out gebruiken voor betere prestaties](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in de [!INCLUDE[prod_short](includes/prod_short.md)] Help voor ontwikkelaars en beheer.

## <a name="to-change-the-database-access-intent"></a>De intentie van de databasetoegang wijzigen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bewerken - Lijst met intenties voor databasetoegang** in en kies vervolgens de gerelateerde koppeling.

    De pagina bevat alle rapporten, pagina's en query's. De kolom **Toegangsintentie** bevat een van de volgende waarden:

    |**Instelling**|**Beschrijving**|  
    |------------|-------------|  
    |**Standaard**|Geeft aan dat het object de vooraf gedefinieerde intentie voor databasetoegang gebruikt.|
    |**Schrijven toestaan**|Stelt het object in om de primaire database te gebruiken, zodat de gebruiker gegevens kan wijzigen.|
    |**Alleen-lezen**|Stelt het object in om de databasereplica te gebruiken, wat betekent dat de gebruiker alleen gegevens kan bekijken en geen gegevens kan wijzigen.|

2. Kies de actie **Lijst bewerken**.

3. Wijzig op de pagina **Bewerken - Lijst met intenties voor databasetoegang** het veld **Toegangsintentie** voor de objecten.

    > [!NOTE]
    > Als een object dat kan worden bewerkt, zoals de klantenkaart, is ingesteld op **Alleen-lezen**, zal de primaire database nog steeds worden gebruikt, ongeacht de toegangsintentie, zodat gebruikers normaal wijzigingen kunnen aanbrengen.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook
[Bedrijfsfunctionaliteit](across-business-functionality.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
