---
title: 'Ontwerpdetails: Rekeningen in het grootboek | Microsoft Docs'
description: 'Om voorraad- en capaciteitsposten te reconciliëren met het grootboek, worden de gerelateerde waardeposten naar verschillende rekeningen in het grootboek geboekt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: null
ms.date: 02/20/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Ontwerpdetails: rekeningen in het grootboek

Om voorraad- en capaciteitsposten te reconciliëren met het grootboek, worden de gerelateerde waardeposten naar verschillende rekeningen in het grootboek geboekt. Zie voor meer informatie [Ontwerpdetails: reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Vanuit het voorraadgrootboek

De volgende tabel toont de relatie tussen verschillende soorten voorraadwaardeposten en de rekeningen en tegenrekeningen in het grootboek.  

|**Artikelboekingssoort**|**Waardeboekingssoort**|**Verschilsoort**|**Verwachte kosten**|**Rekening**|**Tegenrekening**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Inkoop|Directe kosten||Ja|Voorraad (Interim)|Voorraadcorrectiesrek. (tussenrek.)|  
|Inkoop|Directe kosten||Nee|Voorraad|Dekking directe kosten|  
|Inkoop|Indirecte kosten||Nee|Voorraad|Dekking overhead|  
|Inkoop|Verschil|Inkoop|Nee|Voorraad|Inkoopverschil|  
|Inkoop|Herwaardering||Nee|Voorraad|Voorraadherwaardering|  
|Inkoop|Afronding||Nee|Voorraad|Voorraadherwaardering|  
|Verkoop|Directe kosten||Ja|Voorraad (Interim)|KPV (Interim)|  
|Verkoop|Directe kosten||Nee|Voorraad|KPV|  
|Verkoop|Herwaardering||Nee|Voorraad|Voorraadherwaardering|  
|Verkoop|Afronding||Nee|Voorraad|Voorraadherwaardering|  
|Positieve correctie,Negatieve correctie, Transfer|Directe kosten||Nee|Voorraad|Voorraadherwaardering|  
|Positieve correctie,Negatieve correctie, Transfer|Herwaardering||Nee|Voorraad|Voorraadherwaardering|  
|Positieve correctie,Negatieve correctie, Transfer|Afronding||Nee|Voorraad|Voorraadherwaardering|  
|(Productie) Verbruik|Directe kosten||Nee|Voorraad|OHW|  
|(Productie) Verbruik|Herwaardering||Nee|Voorraad|Voorraadherwaardering|  
|(Productie) Verbruik|Afronding||Nee|Voorraad|Voorraadherwaardering|  
|Assemblageverbruik|Directe kosten||Nee|Voorraad|Voorraadherwaardering|  
|Assemblageverbruik|Directe kosten||Nee|Dekking directe kosten|Voorraadherwaardering|  
|Assemblageverbruik|Indirecte kosten||Nee|Dekking overhead|Voorraadherwaardering|  
|(Productie)output|Directe kosten||Ja|Voorraad (Interim)|OHW|  
|(Productie)output|Directe kosten||Nee|Voorraad|OHW|  
|(Productie)output|Indirecte kosten||Nee|Voorraad|Dekking overhead|  
|(Productie)output|Verschil|Materiaal|Nee|Voorraad|Materiaalverschil|  
|(Productie)output|Verschil|Capaciteit|Nee|Voorraad|Capaciteitsverschil|  
|(Productie)output|Verschil|Uitbesteed|Nee|Voorraad|Uitbestedingsverschil|  
|(Productie)output|Verschil|Capaciteitsoverhead|Nee|Voorraad|Capaciteitsoverheadverschil|  
|(Productie)output|Verschil|Productieoverhead|Nee|Voorraad|Productieoverheadverschil|  
|(Productie)output|Herwaardering||Nee|Voorraad|Voorraadherwaardering|  
|(Productie)output|Afronding||Nee|Voorraad|Voorraadherwaardering|  
|Assemblage-uitvoer|Directe kosten||Nee|Voorraad|Voorraadherwaardering|  
|Assemblage-uitvoer|Herwaardering||Nee|Voorraad|Voorraadherwaardering|  
|Assemblage-uitvoer|Indirecte kosten||Nee|Voorraad|Dekking overhead|  
|Assemblage-uitvoer|Verschil|Materiaal|Nee|Voorraad|Materiaalverschil|  
|Assemblage-uitvoer|Verschil|Capaciteit|Nee|Voorraad|Capaciteitsverschil|  
|Assemblage-uitvoer|Verschil|Capaciteitsoverhead|Nee|Voorraad|Capaciteitsoverheadverschil|  
|Assemblage-uitvoer|Verschil|Productieoverhead|Nee|Voorraad|Productieoverheadverschil|  
|Assemblage-uitvoer|Afronding||Nee|Voorraad|Voorraadherwaardering|  

## <a name="from-the-capacity-ledger"></a>Van het capaciteitsgrootboek

 De volgende tabel toont de relatie tussen verschillende soorten capaciteitswaardeposten en de rekeningen en tegenrekeningen in het grootboek. Capaciteitsposten vertegenwoordigen arbeidstijd die is verbruikt in assemblage of productiewerk.  

|**Werksoort**|**Soort capaciteitspost**|**Waardeboekingssoort**|**Rekening**|**Tegenrekening**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Assemblage|Bron|Directe kosten|Dekking directe kosten|Voorraadherwaardering|  
|Assemblage|Resource|Indirecte kosten|Dekking overhead|Voorraadherwaardering|  
|Productie|Bewerkingsplaats/Afdeling|Directe kosten|OHW-rekening|Dekking directe kosten|  
|Productie|Bewerkingsplaats/Afdeling|Indirecte kosten|OHW-rekening|Dekking overhead|  

## <a name="assembly-costs-are-always-actual"></a>Assemblagekosten zijn altijd werkelijk

 Zoals in de tabel hierboven getoond, worden assemblageboekingen niet opgenomen in interimrekeningen. Dit komt doordat het begrip onderhanden werk (OHW) niet van toepassing is op assemblyuitvoerboeking, in tegenstelling tot productie-uitvoerboeking. Assemblagekosten worden alleen geboekt als werkelijke kosten, nooit als verwachte kosten.  

 Zie [Ontwerpdetails: assemblageorderboeking](design-details-assembly-order-posting.md) voor meer informatie.  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Het bedrag berekenen dat moet worden geboekt naar het grootboek

 De volgende velden in de tabel **Waardepost** worden gebruikt om het verwachte kostenbedrag te berekenen dat naar het grootboek wordt geboekt:  

- Tot. werk. kosten  
- Vrd.-waarde geboekt  
- Tot. verw. kosten  
- Verw. kostn geboekt nr grootbk  

De volgende tabel toont hoe bedragen die naar het grootboek moeten worden geboekt, worden berekend voor de twee verschillende kostensoorten.  

|Kostensoort|Berekening|  
|---------------|-----------------|  
|Werkelijke kosten|Tot. werk. kosten - Vrd.-waarde geboekt|  
|Verwachte kosten|Kostenbedrag (verwacht) – Verw. kostn geboekt nr grootbk|  

## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Voorraadboeking](design-details-inventory-posting.md)  
[Ontwerpdetails: Verwachte kostenboeking](design-details-expected-cost-posting.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
