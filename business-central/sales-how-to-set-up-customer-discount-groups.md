---
title: Klantenkortingsgroepen instellen
description: Leer hoe u klantenkortingsgroepen instelt en verkoopregelkortingen voor die groepen maakt.
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="set-up-customer-discount-groups"></a>Klantenkortingsgroepen instellen

U kunt verkoopregelkortingen definiëren voor een groep klanten in plaats van ze afzonderlijk toe te passen.

**Klantenkortingsgroepen** werken op dezelfde manier als [klantprijsgroepen](sales-how-to-set-up-customer-price-groups.md), maar kunnen worden gecombineerd met artikelkortingsgroepen om snel regelkortingen in te stellen voor veel artikelen voor geselecteerde klanten.

## <a name="create-sales-line-discounts-for-a-customer-group"></a>Verkoopregelkortingen maken voor een klantengroep

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantenkortingsgroepen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Klantenkortingsgroepen** **Nieuw** om een nieuwe kortingsgroep te maken en deze een naam te geven onder de kolom **Code** en voeg een beschrijving toe.
3. Selecteer de actie **Navigeren** en kies **Verkoopregelkortingen**.
4. Vul de kolom **Verkoopcode** in met de kortingsgroep die op de vorige pagina is gemaakt.
5. Vul de volgende velden op de regels in: **Type** (Artikel of Artikelkortingsgroep), **Code**, **Code van maateenheid** en **Regelkorting %.**
6. Als de klantengroep een minimumaantal moet kopen om in aanmerking te komen voor het afgesproken kortingspercentage, vult u het veld **Minimumaantal** in.
7. Geef indien vereist de **Begindatum** en de **Einddatum** voor de kortingsgroep op.
8. Indien relevant kunt u ook de **Valutacode** of de **Variantcode** opgeven na het [personaliseren van de kolommen](ui-personalization-user.md).

Herhaal stap 4 tot en met 8 voor elk artikel of elke artikelkortingsgroep waarvoor u een verkoopregelkorting wilt maken.

## <a name="assign-a-customer-to-a-discount-group"></a>Een klant toewijzen aan een kortingsgroep

Nadat u de klantkortingsgroepen hebt ingesteld, kunt u de klantkortingsgroepscodes invoeren op de klantenkaarten.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de **klantenkaart** voor een klant die u in een klantenkortingsgroep wilt plaatsen.
3. Selecteer de groepscode op het sneltabblad **Facturering** in het veld **Klantenkortingsgroep**.

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Speciale verkoopprijzen en kortingen registreren](sales-how-record-sales-price-discount-payment-agreements.md)  
[Klantenprijsgroepen instellen](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
