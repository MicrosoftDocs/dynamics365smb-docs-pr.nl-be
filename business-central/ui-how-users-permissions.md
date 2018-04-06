---
title: Gebruikersmachtigingen toewijzen of bewerken | Microsoft Docs
description: Hier wordt beschreven hoe u Office 365-gebruikers toevoegt aan Business Central en vervolgens machtigingen, toegangsrechten en beveiligingsinstellingen toewijst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 602c429733104a792a49f4a7f38e2a3090420c9d
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="manage-users-and-permissions"></a>Gebruikers en machtigingen beheren
Als u gebruikers wilt toevoegen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet de Office 365-beheerder van uw bedrijf eerst de gebruikers in het Office 365-beheercentrum maken. Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Als gebruikers in Office 365 zijn gemaakt, kunnen ze worden geïmporteerd in het venster **Gebruikers** door middel van de actie **Gebruikers ophalen uit Office 365**. Aan gebruikers worden machtigingensets toegewezen op basis van het plan dat aan de gebruiker is toegewezen in Office 365.

U kunt vervolgens machtigingensets aan gebruikers toewijzen om te bepalen tot welke databaseobjecten (en daardoor tot welke UI-elementen) zij toegang hebben en in welke bedrijven. U kunt gebruikers toevoegen aan gebruikersgroepen. Hierdoor wordt het gemakkelijker om dezelfde machtigingensets aan meerdere gebruikers toe te wijzen.

Een machtigingenset is een verzameling machtigingen voor bepaalde objecten in de database. Aan alle gebruikers moeten een of meer machtigingensets worden toegewezen voordat ze toegang hebben tot [!INCLUDE[d365fin](includes/d365fin_md.md)]. Er zijn standaard verschillende vooraf gedefinieerde machtigingensets beschikbaar. U kunt de machtigingensets gebruiken zoals deze zijn gedefinieerd, u kunt de sets aanpassen of u kunt uw eigen machtigingensets maken.

Beheerders kunnen het venster **Gebruikersinstellingen** gebruiken om perioden te definiëren waarin opgegeven gebruikers kunnen boeken en ook kunnen opgeven of het systeem de tijdsduur vastlegt gedurende welke gebruikers zijn aangemeld.

## <a name="to-assign-permissions-to-a-user"></a>Machtigingen toewijzen aan een gebruiker
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikers** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de gebruiker waaraan u machtigingen wilt toewijzen.
Alle machtigingensets die al zijn toegewezen aan de gebruiker worden weergegeven in het feitenblok **Machtigingensets**.
3. Kies de actie **Bewerken** om het venster **Gebruikerskaart** te openen.
4. Vul op het sneltabblad **Gebruikersmachtigingensets** waar nodig de velden in op een nieuwe regel. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Gebruikers in gebruikersgroepen samenvoegen
U kunt gebruikersgroepen instellen om u te helpen machtigingensets te beheren voor groepen gebruikers in uw bedrijf. U kunt een functie gebruiken om alle machtigingensets van een bestaande gebruikersgroep naar de nieuwe gebruikersgroep te kopiëren. De leden van de gebruikersgroep worden niet gekopieerd.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikersgroepen** in en klik vervolgens op de gerelateerde koppeling.
2. U kunt ook in het venster **Gebruikers** de actie **Gebruikersgroepen** kiezen.
3. Kies in het venster **Gebruikersgroep** de actie **Gebruikersgroepsleden**.
6. Kies in het venster **Gebruikersgroepsleden** de actie **Gebruikers toevoegen**.
7. Als u nieuwe of extra machtigingensets wilt toevoegen, kiest u in het venster **Gebruikersgroepen** de actie **Machtigingensets van gebruikersgroep**.
8. Vul in het venster **Machtigingensets van gebruikersgroep** op een nieuwe regel de velden waar nodig in door bestaande machtigingensets te selecteren.

## <a name="to-set-up-user-time-constraints"></a>Tijdsbeperkingen voor gebruikers instellen
Beheerders kunnen perioden definiëren waarin opgegeven gebruikers kunnen boeken en ook kunnen opgeven of het systeem de tijdsduur vastlegt gedurende welke gebruikers zijn aangemeld. Beheerders kunnen ook divisies toewijzen aan gebruikers. Zie [Werken met divisies](inventory-responsibility-centers.md) voor meer informatie.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikersinstellingen** in en klik vervolgens op de gerelateerde koppeling.
2. Kies in het venster **Gebruikersinstellingen** dat wordt geopend, de actie **Nieuw**.
3. Voer in het veld **Gebruikers-id** de id van een gebruiker in of kies het veld om alle huidige Windows-gebruikers in het systeem te zien.
4. Vul de velden in.

## <a name="see-also"></a>Zie ook
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Installatie en beheer in [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-setup-and-administration.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

