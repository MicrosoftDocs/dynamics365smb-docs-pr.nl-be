---
title: Over kostprijsboekhouding
description: Kostprijsboekhouding kan u helpen begrijpen welke kosten er verbonden zijn aan het runnen van een bedrijf. Gegevens van de kostprijsboekhouding zijn gemaakt om verschillende problemen te analyseren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-cost-accounting"></a>Over kostprijsboekhouding

Kostprijsboekhouding kan u helpen begrijpen welke kosten er verbonden zijn aan het runnen van een bedrijf. Gegevens van de kostprijsboekhouding zijn gemaakt om het volgende te analyseren:  

- Welke soorten kosten uw bedrijf maakt.  
- Waar de kosten worden gemaakt.
- Wie de kosten draagt.

In kostprijsboekhouding wijst u werkelijke en gebudgetteerde kosten van activiteiten, afdelingen, producten en projecten toe om de winstgevendheid van uw bedrijf te analyseren.  

## <a name="workflow-in-cost-accounting"></a>Werkstroom in kostprijsboekhouding

kostprijsboekhouding heeft de volgende hoofdonderdelen:  

- Kostensoorten, kostenplaatsen en kostenobjecten  
- Kostenposten en kostendagboeken  
- Kostenverdelingen  
- Kostenbudgetten
- Rapportage van kosten  

Het volgende diagram toont de werkstroom in kostprijsboekhouding.  

![Overzicht van kostprijsboekhouding.](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Kostensoorten, kostenplaatsen en kostenobjecten

U definieert kostensoorten, kostenplaatsen en kostenobjecten als u wilt analyseren wat de kosten zijn, waar de kosten vandaan en wie de kosten moet dragen.  

Eerst definieert u een kostensoortschema met een structuur en functies die lijken op het grootboekrekeningschema. U kunt uw eigen kostensoortschema maken of dit doen door de resultatenrekening van het grootboek over te brengen.  

Kostenplaatsen zijn afdelingen en resultatencentra die verantwoordelijk zijn voor de kosten en opbrengsten. Vaak zijn er meer kostenplaatsen ingesteld in de kostprijsboekhouding dan in elk van de dimensies die zijn ingesteld in het grootboek. In het grootboek worden meestal alleen de kostenplaatsen van het eerste niveau voor directe kosten en de initiële kosten gebruikt. In kostprijsboekhouding worden meer kostenplaatsen gemaakt voor extra toewijzingsniveaus.  

Kostenobjecten zijn producten, productgroepen of services die een bedrijf aanbiedt. Deze objecten zijn de "eindproducten" van een bedrijf dat de kosten draagt.  

U kunt kostenplaatsen koppelen aan afdelingen en kostenobjecten aan projecten in uw bedrijf. Via het grootboek kunt u kostenplaatsen en kostenobjecten koppelen aan eventuele dimensies en die gegevens aanvullen met subtotalen en titels.  

## <a name="cost-entries-and-cost-journals"></a>Kostenposten en kostendagboeken

Operationele kosten kunnen worden overgedragen van het grootboek. U kunt automatisch met elke boeking de kostenposten uit het grootboek overbrengen naar kostenposten. U kunt ook een batchverwerking gebruiken om grootboekposten over te brengen naar kostenposten op basis van het dagelijkse of maandelijkse boekingsoverzicht.  

In kostendagboeken kunt u kosten en activiteiten boeken die niet afkomstig zijn uit het grootboek, noch automatisch worden gegenereerd door verdelingen. U kunt bijvoorbeeld zuivere operationele kosten, interne heffingen, verdelingen en correctieposten boeken tussen kostensoorten, kostenplaatsen en kostenobjecten, afzonderlijk of periodiek.  

## <a name="cost-allocations"></a>Kostenverdelingen

Tijdens verdelingen worden kosten en opbrengsten verplaatst tussen kostensoorten , kostenplaatsen en kostenobjecten. Overheadkosten worden eerst op kostenplaatsen geboekt en later aan kostenobjecten toegerekend. Een voorbeeld hiervan is een verkoopafdeling die verschillende producten tegelijkertijd verkoopt. De overheadkosten van de afdeling, zoals salarissen, benodigdheden en reiskosten, worden in eerste instantie toegewezen aan de verkoopkostenplaats. De kosten worden vervolgens verdeeld over de verschillende verkochte producten (kostenobjecten), samen met de aangekochte materialen (directe kosten).

De verdelingsbasis en de juistheid van de definitie van de toewijzing zijn van invloed op de resultaten van kostenverdelingen. De verdelingsdefinitie wijst eerst kosten vanuit zogenaamde pre-kostenplaatsen toe aan hoofdkostenplaatsen en vervolgens van kostenplaatsen naar kostenobjecten.  

Elke toewijzing bestaat uit een verdelingsbron en een of meer verdeeldoelen. U kunt werkelijke waarden of gebudgetteerde waarden toewijzen met behulp van de statische toewijzingsmethode op basis van een definitieve waarde. Bijvoorbeeld vierkante meters of een vastgestelde toewijzingsverhouding van 5:2:4. U kunt ook werkelijke of gebudgetteerde waarden toewijzen met behulp van de methode voor dynamische toewijzing met negen vooraf gedefinieerde toewijzingsgrondslagen en 12 dynamische datumbereiken.  

## <a name="cost-budgets"></a>Kostenbudgetten

Net als bij budgettering in het grootboek, kunt u budgetten maken om kosten te plannen gedurende een bepaalde periode (bijvoorbeeld een boekjaar), die kunnen worden toegepast op een kostenplaats (bedrijfsafdeling) of een kostenobject (product of service). U kunt zoveel kostenbudgetten instellen als u nodig hebt. U kunt het kostenbudget vervolgens kopiëren naar het grootboekbudget en vice versa. Ook kunt u gebudgetteerde kosten als werkelijke kosten overbrengen.

## <a name="cost-reporting"></a>Rapportage van kosten

De meeste lijsten en statistieken zijn gebaseerd op de geboekte kostenposten. U kunt het sorteren van resultaten instellen en filters gebruiken om te bepalen welke gegevens moeten worden weergegeven. U kunt lijsten voor de analyse van de kostenverdeling maken. Bovendien kunt u de standaard financiële rapporten gebruiken om te definiëren hoe uw rapporten voor het schema van kostentypen worden weergegeven.  

## <a name="see-also"></a>Zie ook

[Kosten verantwoorden](finance-manage-cost-accounting.md)  
[Financiën](finance.md)  
[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
