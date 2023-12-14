---
title: Catalogusartikelen maken en beheren
description: Lees hier hoe u artikelen kunt verkopen die u niet in uw lijst met artikelen houdt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# Werken met catalogusartikelen

Catalogusartikelen zijn artikelen die u niet beheert in [!INCLUDE[prod_short](includes/prod_short.md)] totdat u ze verkoopt. Wanneer u de actie **Catalogusartikelen selecteren** gebruikt om een catalogusartikel toe te voegen aan een regel op een verkooporder, offerte of verkoopraamcontract, wordt het catalogusartikel geconverteerd naar een regulier artikel.

> [!NOTE]  
> U kunt geen catalogusartikel selecteren op de pagina **Verkoopfactuur**.

Een catalogusartikel heeft doorgaans het artikelnummer van de leverancier die het levert. Voordat u een catalogusartikel kunt converteren naar een normaal artikel, moet u opgeven hoe u leveranciersartikelnummers naar uw artikelnummering wilt converteren. Ga voor meer informatie over artikelnummering naar [Opgeven hoe catalogusartikelnummers naar uw eigen nummering worden geconverteerd](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Catalogusartikelen moeten niet worden verward met niet-voorraadartikelen. Dat zijn normale artikelen die het type **Niet-voorraad krijgen** om ze uit beschikbaarheid en kostprijsberekeningen te houden, bijvoorbeeld omdat ze alleen intern worden gebruikt en lage kosten hebben. Ga voor meer informatie over niet-voorraadartikelen naar [Over artikeltypen](inventory-about-item-types.md).

## Een catalogusartikel maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Catalogusartikelen** in en kies vervolgens de gerelateerde koppeling
2. Kies de actie **Nieuw**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Opgeven hoe catalogusartikelnummers naar uw eigen nummering worden geconverteerd

Voordat u een catalogusartikel kunt converteren naar een regulier artikel, moet u opgeven hoe artikelnummers van leveranciers moeten worden geconverteerd naar de structuur die u voor artikelnummers gebruikt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van catalogusartikel** in en kies vervolgens de gerelateerde koppeling
2. Kies de gewenste optie in het veld **Nr.-formaat**.

## Een catalogusartikel converteren naar een normaal artikel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Catalogusartikelen** in en kies vervolgens de gerelateerde koppeling
2. Open de kaart voor een catalogusartikel dat u wilt converteren naar een normaal artikel.
3. Kies op de pagina **Catalogusartikelkaart** de actie **Artikel maken**.

Er worden een nieuwe artikelkaart, die vooraf is ingevuld met gegevens van het catalogusartikel, en een relevante artikelsjabloon gemaakt. U kunt indien nodig de informatie over het nieuwe artikel bewerken. Ga voor meer informatie over het maken van artikelen naar [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

## Een catalogusartikel verkopen en converteren naar een normaal artikel

In het volgende proces wordt een verkooporder gebruikt, maar de stappen zijn hetzelfde voor verkoopraamcontracten en offertes.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**. Vul de velden op het sneltabblad **Algemeen** in, zoals u dat voor elke verkooporder doet. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
3. Selecteer op een nieuwe verkoopregel in het veld **Soort** **Artikel**, maar laat het veld **Nr.** leeg laten.
4. Kies de actie **Regel** en kies vervolgens de actie **Catalogusartikelen selecteren**.
5. Selecteer op de pagina **Catalogusartikelen** het catalogusartikel dat u wilt verkopen en klik vervolgens op **OK**.
6. Wanneer de verkooporder is ingevuld, kiest u de actie **Boeken**.

> [!NOTE]  
> Er wordt automatisch een artikelverwijzing gemaakt tussen het artikelnummer van de leverancier en uw nieuwe artikelnummer. Ga voor meer informatie over artikelreferenties naar [Artikelreferenties gebruiken](inventory-how-use-item-cross-refs.md).

## Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Speciale orders maken](sales-how-to-create-special-orders.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
