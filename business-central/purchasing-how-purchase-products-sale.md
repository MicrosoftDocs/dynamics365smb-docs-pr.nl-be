---
title: Artikelen kopen voor een verkoop
description: 'Vanuit een verkoopfactuur kunt u, om producten te kopen, een inkoopfactuur maken voor een leverancier.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'supply planning, sales demand, replenish'
ms.search.form: '50, 51, 56, 9308'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="purchase-items-for-a-sale-by-creating-purchase-invoices"></a><a name="purchase-items-for-a-sale-by-creating-purchase-invoices"></a>Artikelen voor een verkoop inkopen door inkoopfacturen te maken

Vanuit verkooporders en verkoopfacturen kunt u functie gebruiken om snel inkoopdocumenten te maken voor ontbrekende artikelaantallen die vereist worden door de verkoop. U kunt twee verschillende functies gebruiken, afhankelijk van de documentsoort.

> [!Note]
> Deze functionaliteit is voor het aanvullen van verkoopartikelen in uw eigen voorraad. Als u artikelen inkoopt voor directe levering van de leverancier aan uw klant, moet u een doorverzending maken. Zie [Doorverzendingen maken](sales-how-drop-shipment.md) voor meer informatie.   

|Functie|Description|
|--------|-----------|
|**Inkooporders maken**|Vanuit een verkooporder maakt deze functie een inkooporder voor elk van de artikelen op de verkooporder. U kunt het inkoopaantal wijzigen voordat u de inkooporders maakt. Alleen niet-beschikbare verkoopaantallen worden voorgesteld.
|**Inkoopfactuur maken**|Vanuit een verkooporder en vanuit een verkoopfactuur maakt deze functie een inkoopfactuur voor een geselecteerde leverancier voor alle regels of geselecteerde regels op het verkoopdocument. Het volledige verkoopaantal wordt voorgesteld.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Een of meerdere inkooporders van een verkooporder maken
Als u een inkooporder wilt maken voor elk niet-beschikbaar artikelaantal op de verkooporder, gebruikt u de functie **Inkooporders maken**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Open een verkooporder waarvoor u artikelen wilt inkopen.
3. Kies de actie **Inkooporders maken**.

    De pagina **Inkooporders maken** wordt geopend met een regel voor elk ander artikel op de verkooporder. Regels voor volledig beschikbare verkoopaantallen en niet-beschikbare verkoopaantallen (grijs) worden standaard weergegeven. U kunt de actie **Niet-beschikbare weergeven** kiezen om alleen regels weer te geven voor niet-beschikbare verkoopaantallen.

    Het veld **In te kopen aantal** bevat standaard het niet-beschikbare verkoopaantal.
4. Als u een ander aantal wilt aanschaffen dan het niet-beschikbare verkoopaantal, bewerkt u de waarde in het veld **In te kopen aantal**.

    > [!NOTE]  
    >   U kunt ook het veld **In te kopen aantal** wijzigen op grijze regels, ook al vertegenwoordigen deze volledig beschikbare verkoopaantallen.
5. Kies de knop **OK**.

    Een inkooporder wordt gemaakt voor elke leverancier van artikelen op de verkooporder, inclusief aantalwijzigingen die u aanbrengt op de pagina **Inkooporders maken**.
7. Ga verder met het verwerken van de inkooporder of -orders, bijvoorbeeld door inkooporderregels te bewerken of toe te voegen. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Een inkoopfactuur van een verkooporder of verkoopfactuur maken
Als u één inkoopfactuur wilt maken voor een of meer regels in een verkoopdocument door eerst te selecteren van welke leverancier wordt gekocht, gebruikt u de functie **Inkoopfactuur maken**.

> [!NOTE]  
>   Deze functie maakt een inkoopfactuur voor het exacte artikelaantal op het geselecteerde verkoopdocument. Als u het inkoopaantal wilt wijzigen, moet u de inkoopfactuur wijzigen nadat deze is gemaakt.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Open een verkoopfactuur waarvoor u artikelen wilt inkopen.
3. Selecteer een of meer verkoopfactuurregels die u wilt gebruiken op de inkoopfactuur. Als u alle verkoopfactuurregels wilt gebruiken, selecteert u ze allemaal of selecteert u helemaal geen regels.
4. Kies de actie **Inkoopfactuur maken**.
5. Selecteer **Alle regels** of **Geselecteerde regels** en kies de knop **OK**.  
6. Selecteer in de lijst met leveranciers die wordt weergegeven, de leverancier van wie u alle artikelen wilt kopen en kies vervolgens de knop **OK**.

    Er wordt een inkoopfactuur gemaakt die één, meerdere of alle regels op de verkoopfactuur bevat.
7. Ga verder met het verwerken van de inkoopfactuur, bijvoorbeeld door inkoopfactuurregels te bewerken of toe te voegen. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).

## <a name="see-also"></a><a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
