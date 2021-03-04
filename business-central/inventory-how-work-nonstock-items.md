---
title: Catalogusartikelen maken en beheren | Microsoft Docs
description: Beschrijft hoe u handelt in artikelen die voorkomen in artikellijsten van uw leveranciers, maar niet in uw eigen artikellijsten.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cf6016b2d2f2774807b120ab3d3521af9eaf5f7f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749917"
---
# <a name="work-with-catalog-items"></a>Werken met catalogusartikelen
U kunt bepaalde artikelen aan uw klanten aanbieden voor hun gemak. U wilt deze artikelen pas in uw systeem beheren als u ze gaat verkopen. Wanneer u deze artikelen wilt gaan beheren in uw systeem, kunt u ze op twee manieren naar normale artikelkaarten converteren.

* Maak vanuit een catalogusartikelkaart een nieuwe artikelkaart op basis van een sjabloon.
* Selecteer een catalogusartikel op een verkooporderregel van het type **Artikel** met een leeg veld voor **Nr.** Er wordt dan automatisch een artikelkaart gemaakt voor het catalogusartikel.

> [!NOTE]  
> U kunt geen catalogusartikel selecteren op de pagina **Verkoopfactuur**.<br /><br />
> U kunt een catalogusartikel op de pagina **Verkoopofferte** selecteren, maar het catalogusartikel wordt niet geconverteerd naar een normaal artikel wanneer u de functie **Order maken** gebruikt.

Een catalogusartikel heeft doorgaans het artikelnummer van de leverancier die het levert. Als u conversie van een catalogusartikelkaart naar een normale artikelkaart wilt inschakelen, moet u eerst instellen hoe leverancierartikelnummering naar uw eigen artikelnummering wordt geconverteerd.   

> [!Important]
> Catalogusartikelen moeten niet worden verward met niet-voorraadartikelen. Dat zijn normale artikelen die het type **Niet-voorraad krijgen** om ze uit beschikbaarheid en kostprijsberekeningen te houden, bijvoorbeeld omdat ze alleen intern worden gebruikt en lage kosten hebben. Zie voor meer informatie [Over artikeltypen](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Een catalogusartikel maken
Catalogusartikelkaarten hebben minder informatie dan normale artikelkaarten omdat u deze alleen gebruikt op offertes en op andere manieren. Om die reden moeten ze naar normale artikelkaarten worden converteerd voordat u er verkooptransacties voor kunt boeken.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Catalogusartikelen** in en kies de desbetreffende koppeling.
2. Kies de actie **Nieuw**.
3. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Instellen hoe catalogusartikelnummers naar uw eigen nummering worden geconverteerd
Als u conversie van een catalogusartikelkaart naar een normale artikelkaart wilt inschakelen, moet u eerst instellen hoe de leverancierartikelnummering naar uw eigen artikelnummeropmaak wordt geconverteerd.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van catalogusartikel** in en kies de desbetreffende koppeling.
2. Vul de benodigde velden in.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Een catalogusartikel converteren naar een normaal artikel
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Catalogusartikelen** in en kies de desbetreffende koppeling.
2. Open de kaart voor een catalogusartikel dat u wilt converteren naar een normaal artikel.
3. Kies op de pagina **Catalogusartikelkaart** de actie **Artikel maken**.

Er worden een nieuwe artikelkaart die vooraf is ingevuld met gegevens van het catalogusartikel, en een relevante artikelsjabloon gemaakt. U kunt vervolgens indien nodig velden op de nieuwe artikelkaart invullen of bewerken. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Een catalogusartikel verkopen en converteren naar een normaal artikel
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.
2. Kies de actie **Nieuw**. Vul de velden op het sneltabblad **Algemeen** in, zoals u dat voor elke verkooporder doet. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
3. Selecteer op een nieuwe verkoopregel in het veld **Soort** **Artikel**, maar laat het veld **Nr.** leeg laten.
4. Kies de actie **Regel** en kies vervolgens de actie **Catalogusartikelen selecteren**.

    Het catalogusartikel wordt naar een normaal artikel geconverteerd. Er worden een nieuwe artikelkaart die vooraf is ingevuld met gegevens van het catalogusartikel, en een relevante artikelsjabloon gemaakt.
5. Selecteer op de pagina **Catalogusartikelen** het catalogusartikel dat u wilt verkopen en klik vervolgens op **OK**.
6. Wanneer de verkooporder is ingevuld, kiest u de actie **Boeken**.

U kunt vervolgens indien nodig velden op de nieuwe artikelkaart invullen of bewerken. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

> [!NOTE]  
>   Er wordt automatisch een artikelkruisverwijzingsrecord gemaakt voor de leverancier van het artikel tussen het artikelnummer van de leverancier en uw nieuwe artikelnummer. Zie voor meer informatie [Artikelkruisverwijzingen gebruiken](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Speciale orders maken](sales-how-to-create-special-orders.md)|  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]