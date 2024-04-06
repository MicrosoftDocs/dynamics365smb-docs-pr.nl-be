---
title: Urenstaten en de goedkeuring ervan instellen
description: Meer informatie over hoe u urenstaten gebruikt om tijd bij te houden voor projecten en resources.
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Urenstaten instellen

Urenstaten in [!INCLUDE[prod_short](includes/prod_short.md)] verwerken tijdsregistraties in wekelijkse termijnen van zeven dagen. U kunt ze gebruiken om de tijd te volgen die aan projecten wordt besteed en u kunt ze gebruiken om eenvoudige registratie van resourcetijd vast te leggen. Voordat u urenstaten gebruikt, moet u specificeren welke gebruikers urenstaten moeten indienen en hoe u urenstaten wilt configureren.  

> [!TIP]
> De mensen die urenstaten gebruiken, zijn *resources*. Zo kunt u bijvoorbeeld urenstaten gebruiken om het werk van niet-werknemers bij te houden. Om het werk van werknemers bij te houden of om urenstaten te gebruiken om de afwezigheid van werknemers bij te houden, moet u medewerkers koppelen aan resources. Er is een begeleide instelling die u daarbij kan helpen. Ga voor meer informatie over de guide naar [Urenstaten instellen met de begeleide instelling](#set-up-time-sheets-with-the-assisted-setup-guide).  

Geef desgewenst op of en hoe urenstaten worden goedgekeurd. Afhankelijk van de wensen van uw organisatie kunt u het volgende aangeven:

* Een of meer gebruikers als urenstatenbeheerders en fiatteurs voor alle urenstaten.
* Een urenstaatgoedkeurder voor elke resource.

Wanneer u urenstaten hebt ingesteld, kunt u urenstaten maken voor resources en de resources kunnen urenstaatregels boeken. Wijs desgewenst urenstaten toe aan projectplanningsregels. Ga voor meer informatie naar [Urenstaten beheren](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Urenstaten instellen met de begeleide instelling

Een begeleide instelling kan u helpen urenstaten in te stellen.  

> [!TIP]
> Als u een eerdere versie dan 2023 releasewave 1 (v22) gebruikt, moet u de **Functie-update: nieuwe ervaring met urenstaten** inschakelen op de pagina [Functiebeheer](https://businesscentral.dynamics.com/?page=2610) om deze mogelijkheid te gebruiken.
>
> Met deze instelling kunt u urenstaten ook op mobiele apparaten gebruiken.

Open de begeleide instelling **Urenstaten instellen** vanaf de pagina [Begeleide instelling](https://businesscentral.dynamics.com/?page=1801).

De begeleide instelling leidt u door de volgende stappen:

1. Stel de deelnemers in de urenstaatprocessen in.

    Op de eerste pagina van de gids ziet u het aantal gebruikers in uw [!INCLUDE [prod_short](includes/prod_short.md)]. Het toont ook andere vereiste en optionele informatie.  
2. Geef de eerste dag van een werkweek in deze organisatie op.

    De eerste dag van een werkweek is de standaard eerste dag voor alle urenstaten.
3. Geef de persoon op die urenstaten beheert.

    Deze persoon kan alle urenstaten bewerken en verwijderen. Voeg optioneel dezelfde rol toe aan andere mensen op de pagina **Gebruikersinstellingen**.
4. Stel de resources in die urenstaten gebruiken en de mensen die urenstaten goedkeuren.

Aan het einde van de begeleide instelling kunt u ervoor kiezen om [!INCLUDE [prod_short](includes/prod_short.md)] urenstaten te laten maken op basis van uw configuratie. Bekijk de nieuwe urenstaten op de pagina **Urenstaten**, die u [hier](https://businesscentral.dynamics.com/?page=951) kunt openen. U kunt ook de begeleide instelling opnieuw uitvoeren of de installatie handmatig voltooien.

> [!IMPORTANT]
> Als u releasewave 1 (v22) van 2023 of later gebruikt en wilt zorgen dat u urenstaten op mobiele apparaten kunt beheren, moet u de optie **Nieuwe urenstaatervaring gebruiken** voor de urenstaatinstelling inschakelen, zoals beschreven in de volgende procedure.

## <a name="set-up-time-sheets-manually"></a>Urenstaten handmatig instellen

In de volgende secties wordt beschreven hoe u urenstaten kunt instellen als u de begeleide instelling **Urenstaten instellen** niet gebruikt.  

### <a name="set-up-general-information-for-time-sheets-manually"></a>Algemene informatie handmatig instellen voor urenstaten

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resources instellen** in en kies vervolgens de gerelateerde koppeling.  
1. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Als u releasewave 1 (v22) van 2023 of later gebruikt en ervoor wilt zorgen dat u urenstaten op mobiele apparaten kunt beheren, schakelt u de optie **Nieuwe urenstaatervaring gebruiken** in.
1. Selecteer voor het veld **Urenstaat op taakgoedkeuring** een van de volgende opties.

| Optie | Omschrijving |
| --- | --- |
| **Nooit** |De gebruiker in het veld **Gebruikers-id van fiatteur van urenstaat** op de resourcekaart keurt de urenstaat goed. |
| **Altijd** |De gebruiker in het veld **Verantwoordelijke** op de projectkaart keurt de urenstaat goed. |
| **Alleen machine** |Als de urenstaat van een machine is gekoppeld aan een project, keurt de gebruiker in het veld **Verantwoordelijke** op de projectkaart de urenstaat goed. Als de urenstaat van een machine is gekoppeld aan een resource, keurt de gebruiker in het veld **Gebruikers-id van fiatteur van urenstaat** op de resourcekaart de urenstaat goed. |

### <a name="assign-a-time-sheet-administrator-manually"></a>Handmatig een beheerder van urenstaten toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de gebruiker die de urenstaatbeheerder wordt en schakel vervolgens het selectievakje **Urenstaat-admin** in.  

> [!TIP]  
> Het is raadzaam dat u slechts één gebruiker als beheerder van urenstaten van een bedrijf aanwijst. In de volgende procedure stelt u een urenstaateigenaar en fiatteur in waarbij de urenstaatfiatteur voor elke resource wordt toegewezen.  

### <a name="assign-a-time-sheets-owner-and-approver-manually"></a>Handmatig een urenstaateigenaar en -fiatteur toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resources** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de resource waarvoor u de mogelijkheid wilt instellen om urenstaten te gebruiken, en schakel vervolgens het selectievakje **Urenstaat gebruiken** in.  
3. Voer in het veld **Gebruikers-id van eigenaar van urenstaat** de id in van de eigenaar van de urenstaat. De eigenaar kan tijdsgebruik op een urenstaat invoeren en indienen voor goedkeuring. Als de resource een persoon, is die persoon over het algemeen ook de eigenaar.  
4. Voer in het veld **Gebruikers-id van fiatteur van urenstaat** de id in van de fiatteur van de urenstaat. De goedkeurder kan goedkeuren, weigeren of een urenstaat opnieuw openen.  

> [!NOTE]  
> U kunt de id van de urenstaatgoedkeurder niet wijzigen als er urenstaten zijn die nog niet zijn verwerkt en die de status **Ingediend** of **Open** hebben.

## <a name="see-also"></a>Zie ook

[Urenstaten gebruiken voor projecten](projects-how-use-time-sheets.md)  
[Urenstaten maken](projects-how-use-time-sheets.md#create-time-sheets)  
[Verbruik of gebruik voor projecten registreren](projects-how-record-job-usage.md)  
[Projectbeheer instellen](projects-setup-projects.md)  
[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
