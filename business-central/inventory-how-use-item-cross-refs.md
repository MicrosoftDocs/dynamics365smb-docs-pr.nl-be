---
title: Artikelverwijzingen gebruiken
description: 'Stel verwijzingen in tussen de beschrijvingen, eenheden en varianten die u en uw leverancier of klant voor een artikel gebruiken.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/02/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Artikelverwijzingen gebruiken

Als u artikelen koopt of verkoopt waarvoor u en uw leverancier of klant verschillende voorwaarden gebruiken, kunt u een verwijzing instellen tussen uw voorwaarden voor de artikelen en de voorwaarden die de klant of leverancier van dat artikel gebruikt. Op deze manier wordt de artikelbeschrijving, eenheid of variantcode van de leverancier of klant automatisch ingevoegd op de relevante documenten wanneer u het veld **Nr. van artikelreferentie** ervan.  

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

## Barcodes scannen met de mobiele Business Central-app

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

In de volgende tabel worden de pagina's vermeld die het scannen van barcodes van artikelreferenties uit de mobiele [!INCLUDE [prod_short](includes/prod_short.md)]-app ondersteunen.

|Pagina  |Veldwaarde die u kunt scannen  |
|---------|---------|
|Artikelreferentie     | Verwijzingsnr.        |
|Artikeldagboekregel     | Nr. van artikelreferentie        |
|Regel van inventarisatieorder     |Nr. van artikelreferentie         |
|Inkoopregel     |   Nr. van artikelreferentie      |
|Verkoopregel     | Nr. van artikelreferentie        |

## Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
