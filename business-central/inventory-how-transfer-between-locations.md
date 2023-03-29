---
title: Artikelen overbrengen tussen magazijnvestigingen
description: 'Leer hoe u voorraad verplaatst van de ene plaats of magazijn naar een andere, met het herindelingsdagboek of met transferorders.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Voorraad overbrengen tussen vestigingen

U kunt voorraadartikelen tussen vestigingen overbrengen door transferorders te maken. U kunt ook het artikelherindelingsdagboek gebruiken.

> [!NOTE]
> Als u artikelen wilt overbrengen, moet u locaties en transferroutes instellen. Ga voor meer informatie over het instellen van locaties naar [Locaties instellen](inventory-how-setup-locations.md). U kunt geen transferorders gebruiken voor *lege* locaties.

## Transferorders

U kunt een uitgaande transfer vanuit de ene vestiging verzenden en een inkomende transfer op de bestemming ontvangen. U kunt het volgende doen:

* Volg een hoeveelheid in transit
* Definieer agenda's, bewerkingsplannen en inkomende en uitgaande verwerkingstijden voor datumberekening en planning. Ga voor meer informatie over planning naar [Over planningsfunctionaliteit](production-about-planning-functionality.md).
* Gebruik verschillende magazijnfuncties voor inkomende en uitgaande locaties.
* Met enkele beperkingen kunt u transferorders gebruiken voor directe transfers.

## Artikelherindelingsdagboeken

* Eenvoudige, directe transfer van artikelen tussen locaties.
* Verplaats artikelen tussen opslaglocaties. Ga voor meer informatie over het overbrengen van artikelen tussen opslaglocaties naar [Artikelen ongepland verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Wijzig een lot- of serienummer in een nieuw lot- of serienummer. Ga voor meer informatie over het herindelen van serie- en lotnummers naar [Serie- of lotnummers herindelen](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Verander de vervaldatum naar een nieuwe datum.
* Herindeel artikelen van een *lege* locatie naar een daadwerkelijke locatie.
* Magazijnactiviteiten worden niet beheerd. Er worden magazijnposten aangemaakt.

## Artikelen overbrengen met een transferorder

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferorders** in en kies vervolgens de gerelateerde koppeling
2. Vul op de pagina **Transferorder** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Als u tijdens het instellen van de transferroute de velden **Transitcode**, **Expediteur** en **Expediteurservice** op de pagina **Transferroutegegevens** hebt ingevuld, worden de bijbehorende velden op de transferorder automatisch ingevuld.

    Wanneer u het veld **Servicecode expediteur** invult, wordt de ontvangstdatum in de ontvangstvestiging berekend door de verzendtijd van de expediteurservice op te tellen bij de verzenddatum.

3. Om de regels in te vullen, voert u ze handmatig in of kiest u een van de volgende opties onder de actie **Functies**:

    * Kies de actie **Opslaglocatie-inhoud ophalen** om bestaande artikelen uit een specifieke opslaglocatie te selecteren.
    * Kies de actie **Ontvangstregels ophalen** om artikelen te selecteren die net zijn aangekomen op de aflevervestiging.

    Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te verzenden.
4. Kies de actie **Boeken**, kies de optie **Verzenden** en kies vervolgens de knop **OK**.

    De artikelen zijn nu in transit tussen de opgegeven vestigingen volgens de opgegeven transferroute.

    Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te ontvangen. De tranferorderregels zijn dezelfde als bij verzending en kunnen niet worden bewerkt.
5. Kies de actie **Boeken**, kies de optie **Ontvangen** en kies vervolgens de knop **OK**.

## Artikelen overbrengen met het artikelherindelingsdagboek

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelherindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul op de pagina **Artikelherindelingsdagboeken** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voer in het veld **Vestiging** de vestiging in waar de artikelen momenteel zijn opgeslagen.

    > [!NOTE]  
    > Als u artikelen wilt overbrengen die geen vestigingscode hebben, laat u het veld **Vestiging** leeg.
4. Voer in het veld **Nieuwe vestiging** de vestiging in waarnaar u de artikelen wilt overbrengen.
5. Kies de actie **Boeken**.

## Zie gerelateerde [Microsoft-training](/training/modules/transfer-items/)

## Zie ook

[Voorraad beheren](inventory-manage-inventory.md)  
[Vestigingen instellen](inventory-how-setup-locations.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
