---
title: Urenstaten en de goedkeuring ervan instellen
description: 'U stelt urenstaten in om de tijd te traceren die in taken en projecten wordt gebruikt, wat u helpt bij projectbeheer, personeelsbezetting en capaciteit'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77'
ms.date: 12/13/2021
ms.author: edupont
---
# <a name="set-up-time-sheets"></a><a name="set-up-time-sheets"></a>Urenstaten instellen

Urenstaten in [!INCLUDE[prod_short](includes/prod_short.md)] verwerken tijdsregistraties in wekelijkse termijnen van zeven dagen. U kunt ze gebruiken om de tijd te volgen die aan projecten wordt besteed en u kunt ze gebruiken om eenvoudige registratie van resourcetijd vast te leggen. Voordat u urenstaten kunt gebruiken, moet u specificeren welke gebruikers urenstaten moeten indienen en hoe u urenstaten wilt configureren.  

> [!TIP]
> In [!INCLUDE [prod_short](includes/prod_short.md)] zijn de gebruikers van urenstaten *resources*. Zo kunt u urenstaten gebruiken om bijvoorbeeld het werk van niet-werknemers bij te houden. Om het werk van uw eigen werknemers bij te houden of om urenstaten te gebruiken om de afwezigheid van werknemers bij te houden, moet u *medewerkers* koppelen aan *resources*.  

Geef desgewenst op of en hoe urenstaten worden goedgekeurd. Afhankelijk van de wensen van uw organisatie kunt u het volgende aangeven:

* Een of meer gebruikers als urenstatenbeheerders en fiatteurs voor alle urenstaten.
* Een urenstaatgoedkeurder voor elke resource.

Wanneer u urenstaten hebt ingesteld, kunt u urenstaten maken voor resources en de resources kunnen urenstaatregels boeken. Wijs desgewenst urenstaten toe aan projectplanningsregels. Zie [Urenstaten gebruiken](projects-how-use-time-sheets.md) voor meer informatie.  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a><a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Urenstaten instellen met de begeleide instelling

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Vanaf releasewave 2 van 2021 kunt u een begeleide instelling gebruiken om u te helpen bij het instellen van urenstaten.  

> [!TIP]
> U moet de **Functie-update: nieuwe ervaring met urenstaten** inschakelen op de pagina [Functiebeheer](https://businesscentral.dynamics.com/?page=2610) om deze mogelijkheid te gebruiken.
>
> Dezelfde functie maakt het ook gemakkelijk om urenstaten op een mobiel apparaat te beheren.

Open de begeleide instelling **Urenstaten instellen** vanaf de pagina [Begeleide instelling](https://businesscentral.dynamics.com/?page=1801).

De begeleide instelling leidt u door de volgende stappen:

1. De deelnemers in de urenstaatprocessen instellen

    Op de eerste pagina van de gids ziet u het aantal gebruikers in uw [!INCLUDE [prod_short](includes/prod_short.md)]. Het toont ook andere vereiste en optionele informatie.  
2. De eerste dag van een werkweek in deze organisatie opgeven

    De eerste dag van een werkweek is de standaard eerste dag voor alle urenstaten.
3. De persoon opgeven die urenstaten beheert

    Deze persoon kan alle urenstaten bewerken en verwijderen. Voeg optioneel dezelfde rol toe aan andere mensen op de pagina **Gebruikersinstellingen**.
4. De resources instellen die urenstaten gebruiken en de mensen die urenstaten goedkeuren

Aan het einde van de begeleide instelling kunt u ervoor kiezen om [!INCLUDE [prod_short](includes/prod_short.md)] urenstaten te laten maken op basis van uw configuratie. Bekijk de nieuwe urenstaten op de pagina **Urenstaten**, die u [hier](https://businesscentral.dynamics.com/?page=951) kunt openen. U kunt ook de begeleide instelling opnieuw uitvoeren of de installatie handmatig voltooien.  

## <a name="set-up-time-sheets-manually"></a><a name="set-up-time-sheets-manually"></a>Urenstaten handmatig instellen

In de volgende secties wordt beschreven hoe u urenstaten kunt instellen als u de begeleide instelling **Urenstaten instellen** niet gebruikt.  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a><a name="to-set-up-general-information-for-time-sheets-manually"></a>Algemene informatie handmatig instellen voor urenstaten

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resources instellen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Selecteer voor het veld **Urenstaat op taakgoedkeuring** een van de volgende opties.

| Optie | Omschrijving |
| --- | --- |
| **Nooit** |De gebruiker in het veld **Gebruikers-id van fiatteur van urenstaat** op de resourcekaart keurt de urenstaat goed. |
| **Altijd** |De gebruiker in het veld **Verantwoordelijke** op de projectkaart keurt de urenstaat goed. |
| **Alleen machine** |Als de urenstaat van een machine is gekoppeld aan een project, keurt de gebruiker in het veld **Verantwoordelijke** op de projectkaart de urenstaat goed. Als de urenstaat van een machine is gekoppeld aan een resource, keurt de gebruiker in het veld **Gebruikers-id van fiatteur van urenstaat** op de resourcekaart de urenstaat goed. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a><a name="to-assign-a-time-sheet-administrator-manually"></a>Handmatig een beheerder van urenstaten toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Voeg een nieuwe gebruiker toe als de lijst met gebruikers niet de persoon bevat die de beheerder van urenstaten moet zijn. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.
3. Selecteer een gebruiker als beheerder van urenstaten en schakel vervolgens het selectievakje **Urenstaat-admin** in.  

> [!TIP]  
> Het is raadzaam dat u slechts één gebruiker als beheerder van urenstaten van een bedrijf aanwijst. In de volgende procedure stelt u een urenstaateigenaar en fiatteur in waarbij de urenstaatfiatteur voor elke resource wordt toegewezen.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a><a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Handmatig een urenstaateigenaar en -fiatteur toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resources** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de resource waarvoor u de mogelijkheid wilt instellen om urenstaten te gebruiken, en schakel vervolgens het selectievakje **Urenstaat gebruiken** in.  
3. Voer in het veld **Gebruikers-id van eigenaar van urenstaat** de id in van de eigenaar van de urenstaat. De eigenaar kan tijdsgebruik op een urenstaat invoeren en indienen voor goedkeuring. Als de resource een persoon, is die persoon in het algemeen ook de eigenaar.  
4. Voer in het veld **Gebruikers-id van fiatteur van urenstaat** de id in van de fiatteur van de urenstaat. De goedkeurder kan goedkeuren, weigeren of een urenstaat opnieuw openen.  

> [!NOTE]  
> U kunt de ID van de urenstaatgoedkeurder niet wijzigen als er urenstaten zijn die nog niet zijn verwerkt en die de status **Ingediend** of **Open** hebben.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/set-up-jobs-resources/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Urenstaten gebruiken voor projecten](projects-how-use-time-sheets.md)  
[Urenstaten maken](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Verbruik of gebruik voor projecten registreren](projects-how-record-job-usage.md)  
[Projectbeheer instellen](projects-setup-projects.md)  
[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
