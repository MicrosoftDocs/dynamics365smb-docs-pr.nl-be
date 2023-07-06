---
title: Productieorders maken op basis van verkooporders
description: 'Leer verschillende manieren om productieorders te maken voor geproduceerde artikelen, rechtstreeks van verkooporders.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# <a name="create-production-orders-from-sales-orders"></a><a name="create-production-orders-from-sales-orders"></a><a name="create-production-orders-from-sales-orders"></a>Productieorders maken op basis van verkooporders

U kunt direct op basis van verkooporders productieorders maken voor geproduceerde artikelen.  

## <a name="to-create-a-production-order-from-a-sales-order"></a><a name="to-create-a-production-order-from-a-sales-order"></a><a name="to-create-a-production-order-from-a-sales-order"></a>Een productieorder maken op basis van een verkooporder

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de verkooporder die u wilt omzetten in een productieorder.  
3. Kies de actie **Planning**. De pagina **Verkooporderplanning** toont de beschikbaarheid van het artikel.  
4. Kies de actie **Prod.-order maken**.  
5. Selecteer de status en het ordersoort.  
6. Kies de knop **Ja** om een of meer productieorders te maken voor de regels die **Prod.order** in het veld **Aanvullingsmethode** hebben.

    > [!NOTE]  
    > Vraagregels met een veld **Productieorder** in het veld **Aanvullingsmethode** vertegenwoordigen onderliggende productieorders. Denk er na het genereren van deze productieorders aan om eventuele niet-afgehandelde vraag naar deze materialen te bepalen. Gebruik de pagina **Orderplanning** of de actie **Herplannen** om niet-afgehandelde vraag te bepalen.
    >
    > Wanneer u productieorders voor verkooporders aanmaakt met de pagina Verkooporderplanning, worden order-naar-order-koppelingen toegepast tussen vraag en aanbod. Wanneer order-naar-order koppelingen bestaan, neemt het planningssysteem geen gekoppeld aanbod of gekoppelde voorraad op bij de afstemmingsprocedure Ga voor meer informatie over afstemming naar [Order-naar-order-koppelingen](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## <a name="order-type"></a><a name="order-type"></a><a name="order-type"></a>Ordersoort

In de volgende tabel worden twee manieren beschreven om productieorders aan te maken.

|Optie|Omschrijving|
|------|-----------|
|Artikelorder|Eén productieorder wordt gemaakt voor elk artikel dat wordt vertegenwoordigd door een regel in de pagina **Verkooporderplanning**.|
|Projectorder|Eén productieorder met meerdere regels wordt gemaakt voor alle artikelen die worden vertegenwoordigd door regels in de pagina **Verkooporderplanning**. Wanneer u projectorders gebruikt, bevat het veld **Brontype** van de productieorder **Verkoopkop**. De order heeft één regel voor elk verkoopregelartikel dat moet worden geproduceerd.|

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)  
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
