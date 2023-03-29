---
title: Catalogusartikelen maken en beheren
description: Beschrijft hoe u artikelen kunt verkopen die u niet in uw lijst met artikelen houdt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
ms.date: 06/20/2022
ms.author: bholtorf
---
# Werken met catalogusartikelen

Catalogusartikelen zijn artikelen die u niet beheert in [!INCLUDE[prod_short](includes/prod_short.md)] totdat u ze verkoopt. Wanneer u de actie **Catalogusartikelen selecteren** gebruikt om een catalogusartikel toe te voegen aan een regel op een verkooporder of offerte, wordt het catalogusartikel geconverteerd naar een regulier artikel.

> [!NOTE]  
> U kunt geen catalogusartikel selecteren op de pagina **Verkoopfactuur**.

Een catalogusartikel heeft doorgaans het artikelnummer van de leverancier die het levert. Voordat u een catalogusartikel kunt converteren naar een normaal artikel, moet u opgeven hoe u leveranciersartikelnummers naar uw artikelnummering wilt converteren. Voor meer informatie zie [Opgeven hoe catalogusartikelnummers naar uw eigen nummering worden geconverteerd](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Catalogusartikelen moeten niet worden verward met niet-voorraadartikelen. Dat zijn normale artikelen die het type **Niet-voorraad krijgen** om ze uit beschikbaarheid en kostprijsberekeningen te houden, bijvoorbeeld omdat ze alleen intern worden gebruikt en lage kosten hebben. Zie voor meer informatie [Over artikeltypen](inventory-about-item-types.md).

## Een catalogusartikel maken

Catalogusartikelkaarten hebben minder informatie dan normale artikelkaarten omdat u deze alleen gebruikt op offertes en op andere manieren. Om die reden moeten ze naar normale artikelkaarten worden converteerd voordat u er verkooptransacties voor kunt boeken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Catalogusartikelen** in en kies vervolgens de gerelateerde koppeling
2. Kies de actie **Nieuw**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Opgeven hoe catalogusartikelnummers naar uw eigen nummering worden geconverteerd

Voordat u een catalogusartikel kunt converteren naar een normaal artikel, moet u opgeven hoe u leveranciersartikelnummers naar uw artikelnummering wilt converteren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van catalogusartikel** in en kies vervolgens de gerelateerde koppeling
2. Vul de vereiste velden in.

## Een catalogusartikel converteren naar een normaal artikel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Catalogusartikelen** in en kies vervolgens de gerelateerde koppeling
2. Open de kaart voor een catalogusartikel dat u wilt converteren naar een normaal artikel.
3. Kies op de pagina **Catalogusartikelkaart** de actie **Artikel maken**.

Er worden een nieuwe vooraf ingevulde artikelkaart met gegevens van het catalogusartikel en een relevante artikelsjabloon gemaakt. U kunt vervolgens indien nodig velden op de nieuwe artikelkaart invullen of bewerken. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

## Een catalogusartikel verkopen en converteren naar een normaal artikel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**. Vul de velden op het sneltabblad **Algemeen** in, zoals u dat voor elke verkooporder doet. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
3. Selecteer op een nieuwe verkoopregel in het veld **Soort** **Artikel**, maar laat het veld **Nr.** leeg laten.
4. Kies de actie **Regel** en kies vervolgens de actie **Catalogusartikelen selecteren**.

    Het catalogusartikel wordt naar een normaal artikel geconverteerd. Er worden een nieuwe artikelkaart die vooraf is ingevuld met gegevens van het catalogusartikel, en een relevante artikelsjabloon gemaakt.
5. Selecteer op de pagina **Catalogusartikelen** het catalogusartikel dat u wilt verkopen en klik vervolgens op **OK**.
6. Wanneer de verkooporder is ingevuld, kiest u de actie **Boeken**.

U kunt vervolgens indien nodig velden op de nieuwe artikelkaart invullen of bewerken. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

> [!NOTE]  
> Er wordt automatisch een artikelverwijzing gemaakt tussen het artikelnummer van de leverancier en uw nieuwe artikelnummer. Zie voor meer informatie [Artikelverwijzingen gebruiken](inventory-how-use-item-cross-refs.md).

## Zie gerelateerde [Microsoft-training](/training/modules/create-sales-documents-dynamics-365-business-central/)

## Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Speciale orders maken:](sales-how-to-create-special-orders.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
