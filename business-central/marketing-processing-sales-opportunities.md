---
title: Verkoopopportunities verwerken in verkoopcycli
description: In dit onderwerp worden de verschillende manieren beschreven waarop u verkoopkansen in verkoopcycli kunt verwerken en een verkoopkans door de fasen van een verkoopcyclus kunt verplaatsen.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.date: 06/22/2021
ms.author: jswymer
---
# <a name="process-sales-opportunities"></a>Verkoopopportunity's verwerken
Nadat u een opportunity hebt gemaakt, zijn er verschillende functies voor het beheren van de opportunity en het verplaatsen ervan naar voltooiing.

## <a name="view-opportunities"></a>Opportunities weergeven
De bestaande verkoopopportunities zijn beschikbaar op de pagina **Opportunity-overzicht**. Er zijn verschillende manieren om toegang tot deze pagina te krijgen om verkoopopportunities te verwerken:

| Opportunities weergeven voor | Dan |
| --- | --- |
| Alle verkopers en contacten |Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Opportunity-overzicht** in en kies vervolgens de gerelateerde koppeling. |
| Een bepaalde verkoper |Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkopers** in en kies vervolgens de gerelateerde koppeling. Selecteer de verkoper, kies de actie **Opportunities** en kies vervolgens de actie **Overzicht**. |
| Een bepaald contact |Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contacten** in en kies vervolgens de gerelateerde koppeling. Selecteer het contact in de lijst en kies vervolgens de actie **Opportunities**. |

Al deze taken openen de pagina **Opportunity-overzicht**.

## <a name="close-opportunities"></a>Opportunities sluiten
U kunt opportunities afsluiten wanneer de onderhandelingen zijn afgerond. Wanneer u een opportunity afsluit, kunt u opgeven of de opportunity is gewonnen of verloren en de redenen voor het afsluiten. Als u een reden wilt opgeven, moet u codes voor gesloten opportunities instellen.

1. Selecteer op de pagina **Opportunity-overzicht** de opportunity en kies de actie **Sluiten**. De pagina **Opportunity afsluiten** wordt geopend.
2. Vul de relevante velden in en kies de knop **OK**.

   De velden **Opportunitycode afsluiten** en **Datum afgesloten** zijn vereiste velden en moeten worden ingevuld voordat u de knop **OK** kunt kiezen.

   In het veld **Opportunitycode afsluiten** kunt u een van de bestaande codes voor het sluiten van opportunities kiezen of een nieuwe code toevoegen. Als u een nieuwe code wilt toevoegen, kiest u in de vervolgkeuzelijst **Selecteren vanuit volledige lijst** en kiest u vervolgens **nieuw**. Vul op de nieuwe, lege regel de velden **Code**, **Soort** en **Omschrijving** in en kies vervolgens de knop **OK**.

## <a name="create-quotes-for-opportunities"></a>Offertes maken voor opportunity's
> [!NOTE]
> U kunt alleen verkoopoffertes maken van opportunities waarvan het contacttype Bedrijf is.

1. Selecteer op de pagina **Opportunity-overzicht** de opportunity en kies vervolgens de actie **Verkoopofferte toekennen**. De pagina **Verkoopofferte** wordt geopend.
2. Vul de betreffende velden in.

## <a name="create-sales-orders-for-opportunities"></a>Verkooporders voor opportunity's maken
U kunt verkooporders maken van de verkoopoffertes die u hebt gemaakt voor de opportunities. Voordat u verkooporders voor uw contacten kunt maken, moet u het contact eerst als klant maken. Zie voor meer informatie [Contacten maken](marketing-create-contact-companies.md).

1. Zoek de pagina **Opportunity-overzicht** de opportunity waarvoor u een verkoopofferte hebt gemaakt.
2. Kies de actie **Verkoopofferte toekennen**. De pagina **Verkoopofferte** wordt geopend met de verkoopofferte die u aan de opportunity hebt toegewezen.
3. Vul de extra velden in en kies vervolgens de actie **Order maken**.

Wanneer u verkoopopportunities verwerkt, moet u wellicht een offerte maken voor het contact aan wie de opportunity is gekoppeld.

## <a name="delete-opportunities"></a>Opportunities verwijderen
U kunt opportunities verwijderen, bijvoorbeeld nadat u een verkoop hebt afgesloten. U kunt echter alleen gesloten opportunities verwijderen. Er zijn twee manieren om afgesloten opportunities te verwijderen. U kunt individuele afgesloten opportunities verwijderen vanuit de pagina **Opportunity-overzicht** of u kunt de batchverwerking **Afgesloten opportunities verwijderen** uitvoeren om meerdere opportunities te verwijderen op basis van een opgegeven criterium.

Als u gesloten afgesloten opportunities wilt verwijderen vanuit de pagina **Opportunity-overzicht**, selecteert u de opportunity, en kiest u vervolgens de actie **Verwijderen**.

Als u afgesloten opportunities wilt verwijderen met de batchverwerking **Afgesloten opportunities verwijderen**, volgt u deze stappen:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Opportunities verwijderen** in en kies vervolgens de gerelateerde koppeling.
2. Stel in het gedeelte **Opportunity** de filters in die opgeven welke gesloten opportunities moeten worden verwijderd.
3. Kies de knop **Ok**.

Nadat u een opportunity hebt verwijderd, wordt de opportunity verwijderd uit de pagina **Opportunity-overzicht**.

## <a name="move-an-opportunity-through-sales-cycle-stages"></a>Een opportunity verplaatsen door verkoopcyclifasen
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
