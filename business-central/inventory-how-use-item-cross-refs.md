---
title: Artikelverwijzingen gebruiken
description: 'Stel verwijzingen in tussen de beschrijvingen, eenheden en varianten die u en uw leverancier of klant voor een artikel gebruiken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: bholtorf
---
# Artikelverwijzingen gebruiken

Als u artikelen koopt of verkoopt waarvoor u en uw leverancier of klant verschillende voorwaarden gebruiken, kunt u een verwijzing instellen tussen uw voorwaarden voor de artikelen en de voorwaarden die de klant of leverancier van dat artikel gebruikt. Op deze manier wordt de artikelbeschrijving, eenheid of variantcode van de leverancier of klant automatisch ingevoegd op de relevante documenten wanneer u het veld **Nr. van artikelreferentie** invult.  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Niet alle bedrijven gebruiken artikelreferenties. Om rommel op pagina's tot een minimum te beperken, hebben we de gerelateerde velden en acties standaard verborgen. Als u besluit ze te gebruiken, selecteert u het veld **Artikelverwijzingen gebruiken** op de pagina **Voorraadinstellingen**. Nadat u artikelreferenties hebt ingeschakeld, zijn de velden en acties beschikbaar op de pagina's Artikelkaart, Leverancierskaart en Klantenkaart, en in verkoop- en inkoopdocumenten.
>
> In eerdere versies dan releasewave 2 van 2021 kan uw beheerder de functie *Langere itemreferenties schrijven* op de pagina [Functiebeheer](https://businesscentral.dynamics.com/?page=2610) inschakelen (koppeling vereist dat u een [!INCLUDE [prod_short](includes/prod_short.md)]-tenant hebt). Hoe u verwijzingen gebruikt, verandert niet, maar de namen van zaken als pagina's en knoppen wel. De pagina **Artikelkruisverwijzingposten** wordt bijvoorbeeld de pagina **Artikelverwijzingsposten**.

## Artikelreferenties gaan gebruiken

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Kies het pictogram :::image type="icon" source="media/ui-search/search_small.png" border="false":::, voer **Voorraadinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het veld **Artikelverwijzingen gebruiken**.

## Een artikelverwijzing instellen

1. Kies het pictogram :::image type="icon" source="media/ui-search/search_small.png" border="false":::, voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een artikel waarvoor u een referentie wilt maken.
3. Kies de actie **Artikelverwijzingen**.

     Als u de actie **Artikelverwijzingen** niet kunt vinden, kiest u ervoor om meer opties weer te geven en zoekt u de actie vervolgens onder **Gerelateerd** > **Artikel**.
  
4. Vul op een nieuwe regel op de pagina **Artikelverwijzingsposten** de velden naar wens in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

In de volgende procedure wordt beschreven hoe u de artikelverwijzing opgeeft in een inkooporder. Soortgelijke stappen zijn van toepassing op verkoopdocumenten en andere inkoopdocumenten.  

## De artikelomschrijving van een leverancier invoeren in een document

1. Kies het pictogram :::image type="icon" source="media/ui-search/search_small.png" border="false":::, voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Maak een inkooporder voor de leverancier voor wie u een artikelverwijzing hebt ingesteld in de vorige procedure.
3. Maak een inkoopregel voor het artikel waarvoor u een artikelverwijzing hebt ingesteld in de vorige procedure.
4. Selecteer in het veld **Nr. van artikelreferentie** de relevante artikelverwijzing en kies vervolgens de knop **OK**.

Het veld **Omschrijving** op de regel wordt overschreven met de artikelomschrijving van de leverancier, zoals ingesteld in de artikelverwijzingspost. Als de artikelverwijzing een variantcode of een eenheid bevat, worden deze waarden ook naar het document gekopieerd.  

## Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]