---
title: Niet-aftrekbare btw gebruiken
description: In dit artikel wordt uitgelegd hoe u niet-aftrekbare btw gebruikt en aangeeft in Microsoft .
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="use-non-deductible-vat"></a>Niet-aftrekbare btw gebruiken

In dit artikel wordt uitgelegd hoe u niet-aftrekbare btw gebruikt en aangeeft in Microsoft .

## <a name="create-a-purchase-invoice-with-non-deductible-vat"></a>Een inkoopfactuur met niet-aftrekbare btw maken

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en selecteer vervolgens de gerelateerde koppeling
2. Selecteer **Nieuw** om een inkoopfactuur te maken en voer de juiste informatie in op de factuurkop.
3. Maak in de sectie **Regels** een nieuwe regel van elk type op basis van de btw-bedrijfsboekingsgroep en de btw-productboekingsgroep waarin u niet-aftrekbare btw configureert.
4. Voer in de velden **Aantal** en **Directe kostprijs** de juiste waarden in.

    Als u het selectievakje **Niet-aftrekbare btw weergeven op regels** hebt ingeschakeld op de pagina **Btw-instelling**, worden de bedragen in de velden **Niet-aftrekbare btw-basis** en **Niet-aftrekbaar btw-bedrag** berekend op basis van het veld **Niet-aftrekbaar btw-percentage** op de pagina **Btw-boekingsgroepinstellingen**.

5. Boek de factuur.

## <a name="create-a-purchase-order-with-non-deductible-vat"></a>Een inkooporder met niet-aftrekbare btw maken

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en selecteer vervolgens de gerelateerde koppeling
2. Selecteer **Nieuw** om een inkooporder te maken en voer de juiste informatie in op de documentkop.
3. Maak in de sectie **Regels** een nieuwe regel van elk type op basis van de btw-bedrijfsboekingsgroep en de btw-productboekingsgroep waarin u niet-aftrekbare btw configureert.
4. Voer in de velden **Aantal** en **Directe kostprijs** de juiste waarden in.

    Als u het selectievakje **Niet-aftrekbare btw weergeven op regels** hebt ingeschakeld op de pagina **Btw-instelling**, worden de bedragen in de velden **Niet-aftrekbare btw-basis** en **Niet-aftrekbaar btw-bedrag** berekend op basis van het veld **Niet-aftrekbaar btw-percentage** op de pagina **Btw-boekingsgroepinstellingen**.

5. Boek de inkooporder.

## <a name="adjust-rounded-vat-amounts-before-document-posting"></a>Pas afgeronde btw-bedragen aan voordat u documenten boekt

Als btw-bedragen in uw omgeving en in de externe boekhouding (het originele factuurdocument) niet op dezelfde manier worden afgerond, kunt u het btw-bedrag aanpassen voordat u het document boekt. Om deze aanpassing te maken, volgt u deze stappen voordat u het document boekt.

1. Selecteer **Statistiek** in het actiepaneel.
2. Als u met een inkoopfactuur werkt, volgt u deze stappen:

    1. Selecteer op het sneltabblad **Regels** het btw-bedrag of het niet-aftrekbare btw-bedrag.
    2. Stel de waarden in die u nodig hebt uit het originele document en sluit vervolgens de pagina **Inkoopfactuurstatistiek**.

3.  Als u met een inkooporder werkt, volgt u deze stappen:

    1. Selecteer op het sneltabblad **Facturering** **Aantal btw-regels** om de pagina **Btw-bedragregels** te openen.
    2. Selecteer het btw-bedrag of het niet-aftrekbare btw-bedrag dat u wilt corrigeren.
    3. Voer de waarden in die u nodig hebt uit het originele document, sluit de pagina **Btw-bedragregels** en sluit vervolgens de pagina **Inkooporderstatistiek**.

Om correcties van btw-bedragen te gebruiken, moet u de correcties inschakelen. Voer op de pagina **Grootboekinstellingen** in het veld **Max. toegestaan btw-verschil** het maximaal toegestane btw-bedrag voor correctie in. Schakel vervolgens op de pagina **Inkoopinstellingen** **Btw-verschil toegestaan** in.

U kunt de waarden van de velden **Btw-bedrag** en **Niet-aftrekbaar btw-bedrag** aanpassen. De waarde van het veld **Aftrekbaar btw-bedrag** is het resultaat van deze twee waarden. Het bedrag dat u invoert in het veld **Niet-aftrekbaar btw-bedrag** mag niet hoger zijn dan het bedrag dat u invoert in het veld **Btw-bedrag**. Het veld **Max. toegestaan btw-verschil** op de pagina **Grootboekinstellingen** werkt onafhankelijk voor aftrekbare en niet-aftrekbare btw-bedragen op statistiekpagina's wanneer u btw-bedragen wilt aanpassen.

> [!IMPORTANT]
> Op de vooruitbetalingsfacturen kunt u geen niet-aftrekbare btw gebruiken.

## <a name="see-also"></a>Zie ook

[Financieel beheer](finance.md)

[Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md)  

[Niet-aftrekbare btw instellen](finance-setup-nondeductible-vat.md)

[Ontwerpdetails: over niet-aftrekbare btw](design-details-nondeductible-vat.md)

[Btw rapporteren aan de belastingdienst](finance-how-report-vat.md)

[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
