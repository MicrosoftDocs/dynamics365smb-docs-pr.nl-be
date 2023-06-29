---
title: 'Ontwerpdetails: Rekeningen in het grootboek | Microsoft Docs'
description: 'Om voorraad- en capaciteitsposten te reconciliëren met het grootboek, worden de gerelateerde waardeposten naar verschillende rekeningen in het grootboek geboekt.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-accounts-in-the-general-ledger"></a><a name="design-details-accounts-in-the-general-ledger"></a>Ontwerpdetails: Rekeningen in het grootboek
Om voorraad- en capaciteitsposten te reconciliëren met het grootboek, worden de gerelateerde waardeposten naar verschillende rekeningen in het grootboek geboekt. Zie voor meer informatie [Ontwerpdetails: reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a><a name="from-the-inventory-ledger"></a>Vanuit het voorraadgrootboek
De volgende tabel toont de relatie tussen verschillende soorten voorraadwaardeposten en de rekeningen en tegenrekeningen in het grootboek.  

|**Artikelboekingssoort**|**Waardeboekingssoort**|**Verschilsoort**|**Verwachte kosten**|**Rekening**|**Tegenrekening**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Inkoop|Directe kosten||Ja|Voorraad (Interim)|Voorraadcorrectiesrek. (tussenrek.)|  
|Inkoop|Directe kosten||Nr.|Voorraad|Dekking directe kosten|  
|Inkoop|Indirecte kosten||Nr.|Voorraad|Dekking overhead|  
|Inkoop|Verschil|Inkoop|Nr.|Voorraad|Inkoopverschil|  
|Inkoop|Herwaardering||Nr.|Voorraad|Voorraadherwaardering|  
|Inkoop|Afronding||Nr.|Voorraad|Voorraadherwaardering|  
|Verkoop|Directe kosten||Ja|Voorraad (Interim)|KPV (Interim)|  
|Verkoop|Directe kosten||Nr.|Voorraad|KPV|  
|Verkoop|Herwaardering||Nr.|Voorraad|Voorraadherwaardering|  
|Verkoop|Afronding||Nr.|Voorraad|Voorraadherwaardering|  
|Positieve correctie,Negatieve correctie, Transfer|Directe kosten||Nr.|Voorraad|Voorraadherwaardering|  
|Positieve correctie,Negatieve correctie, Transfer|Herwaardering||Nr.|Voorraad|Voorraadherwaardering|  
|Positieve correctie,Negatieve correctie, Transfer|Afronding||Nr.|Voorraad|Voorraadherwaardering|  
|(Productie) Verbruik|Directe kosten||Nr.|Voorraad|OHW|  
|(Productie) Verbruik|Herwaardering||Nr.|Voorraad|Voorraadherwaardering|  
|(Productie) Verbruik|Afronding||Nr.|Voorraad|Voorraadherwaardering|  
|Assemblageverbruik|Directe kosten||Nr.|Voorraad|Voorraadherwaardering|  
|Assemblageverbruik|Directe kosten||Nr.|Dekking directe kosten|Voorraadherwaardering|  
|Assemblageverbruik|Indirecte kosten||Nr.|Dekking overhead|Voorraadherwaardering|  
|(Productie)output|Directe kosten||Ja|Voorraad (Interim)|OHW|  
|(Productie)output|Directe kosten||Nr.|Voorraad|OHW|  
|(Productie)output|Indirecte kosten||Nr.|Voorraad|Dekking overhead|  
|(Productie)output|Verschil|Materiaal|Nr.|Voorraad|Materiaalverschil|  
|(Productie)output|Verschil|Capaciteit|Nr.|Voorraad|Capaciteitsverschil|  
|(Productie)output|Verschil|Uitbesteed|Nr.|Voorraad|Uitbestedingsverschil|  
|(Productie)output|Verschil|Capaciteitsoverhead|Nr.|Voorraad|Capaciteitsoverheadverschil|  
|(Productie)output|Verschil|Productieoverhead|Nr.|Voorraad|Productieoverheadverschil|  
|(Productie)output|Herwaardering||Nr.|Voorraad|Voorraadherwaardering|  
|(Productie)output|Afronding||Nr.|Voorraad|Voorraadherwaardering|  
|Assemblage-uitvoer|Directe kosten||Nr.|Voorraad|Voorraadherwaardering|  
|Assemblage-uitvoer|Herwaardering||Nr.|Voorraad|Voorraadherwaardering|  
|Assemblage-uitvoer|Indirecte kosten||Nr.|Voorraad|Dekking overhead|  
|Assemblage-uitvoer|Verschil|Materiaal|Nr.|Voorraad|Materiaalverschil|  
|Assemblage-uitvoer|Verschil|Capaciteit|Nr.|Voorraad|Capaciteitsverschil|  
|Assemblage-uitvoer|Verschil|Capaciteitsoverhead|Nr.|Voorraad|Capaciteitsoverheadverschil|  
|Assemblage-uitvoer|Verschil|Productieoverhead|Nr.|Voorraad|Productieoverheadverschil|  
|Assemblage-uitvoer|Afronding||Nr.|Voorraad|Voorraadherwaardering|  

## <a name="from-the-capacity-ledger"></a><a name="from-the-capacity-ledger"></a>Van het capaciteitsgrootboek
 De volgende tabel toont de relatie tussen verschillende soorten capaciteitswaardeposten en de rekeningen en tegenrekeningen in het grootboek. Capaciteitsposten vertegenwoordigen arbeidstijd die is verbruikt in assemblage of productiewerk.  

|**Werksoort**|**Soort capaciteitspost**|**Waardeboekingssoort**|**Rekening**|**Tegenrekening**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Assemblage|Bron|Directe kosten|Dekking directe kosten|Voorraadherwaardering|  
|Assemblage|Resource|Indirecte kosten|Dekking overhead|Voorraadherwaardering|  
|Productie|Bewerkingsplaats/Afdeling|Directe kosten|OHW-rekening|Dekking directe kosten|  
|Productie|Bewerkingsplaats/Afdeling|Indirecte kosten|OHW-rekening|Dekking overhead|  

## <a name="assembly-costs-are-always-actual"></a><a name="assembly-costs-are-always-actual"></a>Assemblagekosten zijn altijd werkelijk
 Zoals in de tabel hierboven getoond, worden assemblageboekingen niet opgenomen in interimrekeningen. Dit komt doordat het begrip onderhanden werk (OHW) niet van toepassing is op assemblyuitvoerboeking, in tegenstelling tot productie-uitvoerboeking. Assemblagekosten worden alleen geboekt als werkelijke kosten, nooit als verwachte kosten.  

 Zie [Ontwerpdetails: assemblageorderboeking](design-details-assembly-order-posting.md) voor meer informatie.  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a><a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Het bedrag berekenen dat moet worden geboekt naar het grootboek
 De volgende velden in de tabel **Waardepost** worden gebruikt om het verwachte kostenbedrag te berekenen dat naar het grootboek wordt geboekt:  

-   Tot. werk. kosten  
-   Vrd.-waarde geboekt  
-   Tot. verw. kosten  
-   Verw. kostn geboekt nr grootbk  

De volgende tabel toont hoe bedragen die naar het grootboek moeten worden geboekt, worden berekend voor de twee verschillende kostensoorten.  

|Kostensoort|Berekening|  
|---------------|-----------------|  
|Werkelijke kosten|Tot. werk. kosten - Vrd.-waarde geboekt|  
|Verwachte kosten|Kostenbedrag (verwacht) – Verw. kostn geboekt nr grootbk|  

## <a name="see-also"></a><a name="see-also"></a>Zie ook
 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)   
 [Ontwerpdetails: Voorraadboeking](design-details-inventory-posting.md)   
 [Ontwerpdetails: Verwachte kostenboeking](design-details-expected-cost-posting.md)  
 [Voorraadkosten beheren](finance-manage-inventory-costs.md)  
 [Financiën](finance.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
