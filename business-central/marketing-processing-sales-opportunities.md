---
title: Verkoopopportunities verwerken in verkoopcycli| Microsoft Docs
description: U kunt verkoopopportunities weergeven sluiten of verwijderen en u kunt ook offertes en verkooporders voor opportunity's maken en een opportunity verplaatsen door de fasen van een verkoopcyclus.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 4d4f6ea3dde008e4667d04ec6e1b816daf7856c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749867"
---
# <a name="process-sales-opportunities"></a>Verkoopopportunity's verwerken
Nadat u een opportunity hebt gemaakt, zijn er verschillende functies voor het beheren van de opportunity en het verplaatsen ervan naar voltooiing.

## <a name="to-view-opportunities"></a>Opportunities weergeven
De bestaande verkoopopportunities zijn beschikbaar op de pagina **Opportunity-overzicht**. Er zijn verschillende manieren om toegang tot deze pagina te krijgen om verkoopopportunities te verwerken:

| Opportunities weergeven voor | Dan |
| --- | --- |
| Alle verkopers en contacten |Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opportunity-overzicht** in en kies de desbetreffende koppeling. |
| Een bepaalde verkoper |Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkopers** in en kies de desbetreffende koppeling. Selecteer de verkoper, kies de actie **Opportunities** en kies vervolgens de actie **Overzicht**. |
| Een bepaald contact |Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling. Selecteer het contact in de lijst en kies vervolgens de actie **Opportunities**. |

Al deze taken openen de pagina **Opportunity-overzicht**.

## <a name="to-close-opportunities"></a>Opportunities sluiten
U kunt opportunities afsluiten wanneer de onderhandelingen zijn afgerond. Wanneer u een opportunity afsluit, kunt u opgeven of de opportunity is gewonnen of verloren en de redenen voor het afsluiten. Als u een reden wilt opgeven, moet u codes voor gesloten opportunities instellen.

1. Selecteer op de pagina **Opportunity-overzicht** de opportunity en kies de actie **Sluiten**. De pagina **Opportunity afsluiten** wordt geopend.
2. Vul de relevante velden in en kies de knop **OK**.

   De velden **Opportunitycode afsluiten** en **Datum afgesloten** zijn vereiste velden en moeten worden ingevuld voordat u de knop **OK** kunt kiezen.

   In het veld **Opportunitycode afsluiten** kunt u een van de bestaande codes voor het sluiten van opportunities kiezen of een nieuwe code toevoegen. Als u een nieuwe code wilt toevoegen, kiest u in de vervolgkeuzelijst **Selecteren vanuit volledige lijst** en kiest u vervolgens **nieuw**. Vul op de nieuwe, lege regel de velden **Code**, **Soort** en **Omschrijving** in en kies vervolgens de knop **OK**.

## <a name="to-create-quotes-for-opportunities"></a>Offertes maken voor opportunity's
U kunt verkoopoffertes maken voor contactpersonen die niet zijn geregistreerd als klant.

1. Selecteer op de pagina **Opportunity-overzicht** de opportunity en kies vervolgens de actie **Verkoopofferte toekennen**. De pagina **Verkoopofferte** wordt geopend.
2. Vul de betreffende velden in.

## <a name="to-create-sales-orders-for-opportunities"></a>Verkooporders voor opportunity's maken
U kunt verkooporders maken van de verkoopoffertes die u hebt gemaakt voor de opportunities. Voordat u verkooporders voor uw contacten kunt maken, moet u het contact eerst als klant maken. Zie voor meer informatie [Contacten maken](marketing-create-contact-companies.md).

1. Zoek de pagina **Opportunity-overzicht** de opportunity waarvoor u een verkoopofferte hebt gemaakt.
2. Kies de actie **Verkoopofferte toekennen**. De pagina **Verkoopofferte** wordt geopend met de verkoopofferte die u aan de opportunity hebt toegewezen.
3. Vul de extra velden in en kies vervolgens de actie **Order maken**.

Wanneer u verkoopopportunities verwerkt, moet u wellicht een offerte maken voor het contact aan wie de opportunity is gekoppeld.

## <a name="to-delete-opportunities"></a>Opportunities verwijderen
U kunt opportunities verwijderen, bijvoorbeeld nadat u een verkoop hebt afgesloten. U kunt echter alleen gesloten opportunities verwijderen. Er zijn twee manieren om afgesloten opportunities te verwijderen. U kunt individuele afgesloten opportunities verwijderen vanuit de pagina **Opportunity-overzicht** of u kunt de batchverwerking **Afgesloten opportunities verwijderen** uitvoeren om meerdere opportunities te verwijderen op basis van een opgegeven criterium.

Als u gesloten afgesloten opportunities wilt verwijderen vanuit de pagina **Opportunity-overzicht**, selecteert u de opportunity, en kiest u vervolgens de actie **Verwijderen**.

Als u afgesloten opportunities wilt verwijderen met de batchverwerking **Afgesloten opportunities verwijderen**, volgt u deze stappen:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opportunities verwijderen** in en kies de desbetreffende koppeling.
2. Stel in het gedeelte **Opportunity** de filters in die opgeven welke gesloten opportunities moeten worden verwijderd.
3. Kies de knop **Ok**.

Nadat u een opportunity hebt verwijderd, wordt de opportunity verwijderd uit de pagina **Opportunity-overzicht**.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Een opportunity verplaatsen door verkoopcyclifasen
Als een opportunity een verkoopcyclus volgt, kunt u deze voorwaarts of achterwaarts door de verschillende fasen verplaatsen, bijvoorbeeld naar de volgende of vorige fase, en zelfs een fase overslaan.

1. Kies op de pagina **Opportunity-overzicht** de actie **Bijwerken**. De wizard **Opportunity bijwerken** wordt geopend.
2. Gebruik het **Actiesoort** om de opportunity door de verkoopcyclusfasen te verplaatsen:
   * **Volgende** verplaatst de opportunity één fase.
   * Met **Overslaan** wordt de opportunity een of meer fasen voorwaarts verplaatst in de verkoopcyclus, wat u opgeeft in het veld **Presentatie**. U kunt alleen fasen overslaan die alleen zijn ingesteld om overslaan toe te staan.
   * **Vorige** verplaatst de opportunity één fase terug.
   * Met **Springen** wordt de opportunity een of meer fasen terug verplaatst in de verkoopcyclus, wat u opgeeft in het veld **Presentatie**.
   * Met **Bijwerken** kunt u informatie wijzigen (bijvoorbeeld om de evaluatie van de slagingskans en de geschatte waarden te wijzigen) zonder te verplaatsen naar een andere fase.
3. Vul de overige velden desgewenst in en kies de knop **OK**.

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Contactpersonen maken en beheren](marketing-contacts.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]