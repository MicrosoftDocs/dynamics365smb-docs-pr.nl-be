---
title: 'Ontwerpdetails: Voorraadboeking | Microsoft Docs'
description: 'Elke voorraadtransactie, bijvoorbeeld een inkoopontvangst of een verkoopverzending boekt twee posten van verschillende soort.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-inventory-posting"></a>Ontwerpdetails: Voorraadboeking

Elke voorraadtransactie, bijvoorbeeld een inkoopontvangst of een verkoopverzending boekt twee posten van verschillende soort.  

|Boekingssoort|Description|  
|----------|-----------|  
|Aantal|Reflecteert de wijziging van het aantal in voorraad. Deze informatie wordt opgeslagen in artikelposten.<br /><br /> Vergezeld door artikelvereffeningsposten.|  
|Waarde|Reflecteert de wijziging van voorraadwaarde. Deze informatie wordt opgeslagen in waardeposten.<br /><br /> Er kunnen een of meer waardeposten bestaan voor elke artikelpost of capaciteitspost.<br /><br /> Voor meer informatie over capaciteitswaardeposten met betrekking tot het gebruik van productie of assemblageresources raadpleegt u [Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md).|  

 Met betrekking tot aantalsboekingen zijn er artikelvereffeningsposten om positieve voorraadmutaties te koppelen aan negatieve voorraadmutaties. Dit zorgt ervoor dat de kostenengine kosten van verhogingen kan doorsturen naar de gerelateerde afnamen, en vice versa. Zie [Ontwerpdetails: artikelvereffening](design-details-item-application.md) voor meer informatie.  

 Artikelposten, waardeposten en artikelvereffeningsposten worden gemaakt als gevolg van het boeken van een artikeldagboekregel, indirect door een orderregel te boeken of direct op de pagina Artikeldagboek.  

 Met regelmatige intervallen worden waardeposten die worden gemaakt in het voorraadgrootboek, geboekt naar het grootboek om de twee grootboeken om financiële controleredenen af te stemmen. Zie voor meer informatie [Ontwerpdetails: reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md).  

 ![Invoerstroom bij inventarisatie met grootboek.](media/design_details_inventory_costing_1_entry_flow.png "Invoerstroom bij inventarisatie met grootboek")  

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld wordt getoond hoe artikelposten, waardeposten en artikelvereffeningsposten resulteren in grootboekposten.  

 U boekt een inkooporder als verzonden en gefactureerd voor 10 artikelen met een directe kostprijs van LV 7 en een overheadtarief van LV 1. De boekingsdatum is 01-01-20. De volgende posten worden gemaakt.  

### <a name="item-ledger-entries-1"></a>Artikelposten (1)

|Boekingsdatum|Boekingssoort|Tot. werk. kosten|Aantal|Volgnummer|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Inkoop|80,00|10|1|  

### <a name="value-entries-1"></a>Waardeposten (1)

|Boekingsdatum|Boekingssoort|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|Directe kosten|70.00|1|1|  
|01-01-20|Indirecte kosten|10.00|1|2|  

### <a name="item-application-entries-1"></a>Artikelvereffeningsposten (1)

|Volgnummer|Artikelpostnr.|Inkomend art.-postnr.|Uitgaand art.-postnr.|Aantal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Vervolgens boekt u een verkoop van 10 eenheden van het artikel met een boekingsdatum van 01-15-20.  

### <a name="item-ledger-entries-2"></a>Artikelposten (2)

|Boekingsdatum|Boekingssoort|Tot. werk. kosten|Aantal|Volgnummer|  
|------------|----------|--------------------|--------|---------|  
|15-01-20|Verkoop|-80,00|-10|2|  

### <a name="value-entries-2"></a>Waardeposten (2)

|Boekingsdatum|Boekingssoort|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|------------|----------|--------------------|---------------------|---------|  
|15-01-20|Directe kosten|-80,00|2|3|  

### <a name="item-application-entries-2"></a>Artikelvereffeningsposten (2)

|Volgnummer|Artikelpostnr.|Inkomend art.-postnr.|Uitgaand art.-postnr.|Aantal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

Aan het eind van de boekhoudperiode voert u de batchverwerking **Voorraadwaarde boeken naar GB** uit om deze voorraadtransacties te reconciliëren met het grootboek.  

 Zie voor meer informatie [Ontwerpdetails: rekeningen in het grootboek](design-details-accounts-in-the-general-ledger.md).  

 De volgende tabellen tonen het resultaat van de reconciliatie van de voorraadtransacties in dit voorbeeld met het grootboek.  

### <a name="value-entries-3"></a>Waardeposten (3)

|Boekingsdatum|Boekingssoort|Tot. werk. kosten|Kosten geboekt naar grootboek|Artikelpostnr.|Volgnummer|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|Directe kosten|70.00|70.00|1|1|  
|01-01-20|Indirecte kosten|10.00|10.00|1|2|  
|15-01-20|Directe kosten|-80,00|-80,00|2|3|  

### <a name="general-ledger-entries-3"></a>Grootboekposten (3)

|Boekingsdatum|Grootboekrekening|Rekeningnr. (En-US demo)|Bedrag|Volgnummer|  
|------------|-----------|------------------------|------|---------|  
|01-01-20|[Voorraadrekening]|2130|70.00|1|  
|01-01-20|[Vereffeningsrekening directe kosten]|7291|-70,00|2|  
|01-01-20|[Voorraadrekening]|2130|10.00|3|  
|01-01-07|[Vereffeningsrekening overheadkosten]|7292|-10,00|4|  
|15-01-20|[Voorraadrekening]|2130|-80,00|5|  
|15-01-20|[KPV-rekening]|7290|80,00|6|  

> [!NOTE]  
> De boekingsdatum van de grootboekposten is hetzelfde als die voor de gerelateerde waardeposten.  
> 
> Het veld **Vrd.-waarde geboekt** in de tabel **Waardepost** wordt gevuld.  

 De relatie tussen waardeposten en grootboekposten wordt opgeslagen in de tabel **Relatie GB-artikeljournaal**.  

### <a name="relation-entries-in-the-gl--item-ledger-relation-table-3"></a>Relatieposten in het grootboek - tabel Artikelpostrelatie (3)

|Grootboekpostnr.|Waardepostnr.|Grootboekjournaalnr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting"></a>Assemblage- en productieboeking

Capaciteits- en resourceposten geven de tijd aan die is geboekt als verbruikt in productie of assemblage. Deze proceskosten worden als waardeposten naar het grootboek geboekt samen met de betrokken materiaalkosten in een soortgelijke structuur zoals voor artikelposten in dit onderwerp beschreven.  

Zie [Ontwerpdetails: assemblageorderboeking](design-details-assembly-order-posting.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook

 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
 [Ontwerpdetails: Rekeningen in het grootboek](design-details-accounts-in-the-general-ledger.md)  
 [Ontwerpdetails: Kostenonderdelen](design-details-cost-components.md) [Voorraadkosten beheren](finance-manage-inventory-costs.md)  
 [Financiën](finance.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
