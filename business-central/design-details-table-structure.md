---
title: 'Ontwerpdetails: Tabelstructuur | Microsoft Docs'
description: 'Om te begrijpen hoe de functie voor opslag en boekingen van dimensieposten opnieuw wordt ontworpen, is het belangrijk om de tabelstructuur te begrijpen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-table-structure"></a>Ontwerpdetails: tabelstructuur

Om te begrijpen hoe dimensieposten worden opgeslagen en geboekt, is het belangrijk om de tabelstructuur te begrijpen.  

## <a name="table-480-dimension-set-entry"></a>Tabel 480, Dimensiesetpost

U kunt deze tabel niet wijzigen. Nadat gegevens naar de tabel zijn geschreven, kunt u ze niet meer verwijderen of wijzigen.

|Veldnr.|Veldnaam|Gegevenstype|Opmerking|  
|---------------|----------------|---------------|-------------|  
|1|**Id**|Integer|>0,0 is gereserveerd voor de lege dimensieset. Verwijst naar veld 3 in tabel 481.|  
|2|**Dimensiecode**|Code 20|Tabelrelatie met tabel 348.|  
|3|**Dimensiewaardecode**|Code 20|Tabelrelatie met tabel 349.|  
|4|**Dimensiewaarde-id**|Integer|Verwijst naar veld 12 in tabel 349. Het is de secundaire sleutel die wordt gebruikt wanneer tabel 481 wordt doorlopen.|  
|5|**Dimensienaam**|Tekst 30|CalcField. Opzoeken in tabel 348.|  
|6|**Dimensiewaardenaam**|Tekst 30|CalcField. Opzoeken in tabel 349.|  

## <a name="table-481-dimension-set-tree-node"></a>Tabel 481, Boomstructuurpunt dimensieset
U kunt deze tabel niet wijzigen. De tabel wordt gebruikt om te zoeken naar een dimensieset. Als de dimensieset niet wordt gevonden, wordt een nieuwe set gemaakt.  

|Veldnr.|Veldnaam|Gegevenstype|Opmerking|  
|---------------|----------------|---------------|-------------|  
|1|**Bovenliggende dimensieset-id**|Geheel getal|0 voor knooppunt bovenste niveau.|  
|2|**Dimensiewaarde-id**|Geheel getal|Tabelrelatie met veld 12 in tabel 349.|  
|3|**Dimensieset-id**|Geheel getal|AutoIncrement. Gebruikt in veld 1 in tabel 480.|  
|4|**In gebruik**|Boolean|Onwaar indien niet in gebruik.|  

## <a name="table-482-reclas-dimension-set-buffer"></a>Tabel 482 Herklass. dimensiesetbuffer
Deze tabel wordt gebruikt als u een dimensiewaardecode wijzigt, bijvoorbeeld in een artikelpost met de pagina **Artikelherindelingsdagboek**.  

|Veldnr.|Veldnaam|Gegevenstype|Opmerking|  
|---------------|----------------|---------------|-------------|  
|1|**Dimensiecode**|Code 20|Tabelrelatie met tabel 348.|  
|2|**Dimensiewaardecode**|Code 20|Tabelrelatie met tabel 349.|  
|3|**Dimensiewaarde-id**|Geheel getal|Verwijst naar veld 12 in tabel 349.|  
|4|**Nieuwe dimensiewaardecode**|Code 20|Tabelrelatie met tabel 349.|  
|5|**Nieuwe dimensiewaarde-id**|Geheel getal|Verwijst naar veld 12 in tabel 349.|  
|6|**Dimensienaam**|Tekst 30|CalcField. Opzoeken in tabel 348.|  
|7|**Dimensiewaardenaam**|Tekst 30|CalcField. Opzoeken in tabel 349.|  
|8|**Nieuwe dimensiewaardenaam**|Tekst 30|CalcField. Opzoeken in tabel 349.|  

## <a name="transaction-and-budget-tables"></a>Transactie- en budgettabellen
Naast andere dimensievelden in de tabel is dit veld belangrijk:  

|Veldnr.|Veldnaam|Gegevenstype|Opmerking|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensieset-id**|Integer|Verwijst naar veld 1 in tabel 480.|  

### <a name="table-83-item-journal-line"></a>Tabel 83, Artikeldagboekregel
Naast andere dimensievelden in de tabel zijn deze velden belangrijk.  

|Veldnr.|Veldnaam|Gegevenstype|Opmerking|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensieset-id**|Geheel getal|Verwijst naar veld 1 in tabel 480.|  
|481|**Nieuwe dimensieset-id**|Integer|Verwijst naar veld 1 in tabel 480.|  

### <a name="table-349-dimension-value"></a>Tabel 349, Dimensiewaarde
Naast andere dimensievelden in de tabel zijn deze velden belangrijk.  

|Veldnr.|Veldnaam|Gegevenstype|Opmerking|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensiewaarde-id**|Geheel getal|AutoIncrement. Gebruikt voor referenties in tabel 480 en tabel 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field"></a>Tabellen die het veld Dimensieset-id bevatten
 Het veld **Dimensieset-id** (480) bestaat in de volgende tabellen. Voor de tabellen waarin de geboekte gegevens worden opgeslagen, levert het veld alleen een niet-bewerkbare weergave van dimensies, die wordt gemarkeerd als Meer details. Voor de tabellen waarin werkdocumenten worden opgeslagen, is het veld bewerkbaar. Voor de buffertabellen die intern worden gebruikt, zijn geen bewerkbare of niet-bewerkbare voorzieningen nodig.  

 Veld 480 kan niet worden bewerkt in de volgende tabellen.  

|Tabelnr.|Tabelnaam|  
|---------------|----------------|  
|17|**Grootboekpost**|  
|21|**Klantenpost**|  
|25|**Leverancierspost**|  
|32|**Artikelpost**|  
|110|**Verkoopverzendkop**|  
|111|**Verkoopverzendregel**|  
|112|**Verkoopfactuur**|  
|113|**Verkoopfactuurregel**|  
|114|**Verkoopcreditnota**|  
|115|**Verkoopcreditnotaregel**|  
|120|**Inkoopontvangst**|  
|121|**Inkoopontvangstregel**|  
|122|**Inkoopfactuur**|  
|123|**Inkoopfactuurregel**|  
|124|**Inkoopcreditnota**|  
|125|**Inkoopcreditnotaregel**|  
|169|**Projectpost**|  
|203|**Resourcepost**|  
|271|**Bankpost**|  
|281|**Inventarisatiepost**|  
|297|**Verzonden aanmaning**|  
|304|**Verzonden rentefactuur**|  
|5107|**Verkoopkoparchief**|  
|5108|**Verkoopregelarchief**|  
|5109|**Inkoopkoparchief**|  
|5110|**Inkoopregelarchief**|  
|5601|**VA-post**|  
|5625|**Onderhoudspost**|  
|5629|**Verzekeringsdekkingspost**|  
|5744|**Transferverzendkop**|  
|5745|**Transferverzendregel**|  
|5746|**Transferontvangstkop**|  
|5747|**Transferontvangstregel**|  
|5802|**Waardepost**|  
|5832|**Capaciteitspost**|  
|5907|**Servicepost**|  
|5908|**Servicekop**|  
|5933|**Serviceorderboekingsbuffer**|  
|5970|**Gearch. servicecontractkop**|  
|5990|**Serviceverzendingskop**|  
|5991|**Serviceverzendingsregel**|  
|5992|**Servicefactuurkop**|  
|5993|**Servicefactuurregel**|  
|5994|**Servicecreditnotakop**|  
|5995|**Servicecreditnotaregel**|  
|6650|**Retourverzending**|  
|6651|**Retourverzendregel**|  
|6660|**Retourontvangstkop**|  
|6661|**Retourontvangstregel**|  

Veld 480 kan worden bewerkt in de volgende tabellen.  

|Tabelnr.|Tabelnaam|  
|---------------|----------------|  
|36|**Verkoopkop**|  
|37|**Verkoopregel**|  
|38|**Inkoopkop**|  
|39|**Inkoopregel**|  
|81|**Fin. dagboekregel**|  
|83|**Artikeldagboekregel**|  
|89|**Stuklijstdagboekregel**|  
|96|**Budgetpost**|  
|207|**Resourcedagboekregel**|  
|210|**Projectdagboekregel**|  
|221|**Dagboekverdeelsleutel**|  
|246|**Behoefteregel**|  
|295|**Aanmaning**|  
|302|**Rentefactuur**|  
|5405|**Productieorder**|  
|5406|**Prod.-orderregel**|  
|5407|**Materiaalregel**|  
|5615|**VA-verdeelsleutel**|  
|5621|**VA-dagboekregel**|  
|5635|**Verzekeringsdagboekregel**|  
|5740|**Transferkop**|  
|5741|**Transferregel**|  
|5900|**Servicekop**|  
|5901|**Serviceartikelregel**|  
|5902|**Serviceregel**|  
|5965|**Servicecontractkop**|  
|5997|**Standaardserviceregel**|  
|7134|**Artikelbudgetpost**|  
|99000829|**Planningsmateriaal**|  

Veld 480 bestaat in de volgende buffertabellen.  

|Tabelnr.|Tabelnaam|  
|---------------|----------------|  
|49|**Factuurboekingsbuffer**|  
|212|**Boekingsbuffer van project**|  
|372|**Betalingsbuffer**|  
|382|**K/L-postbuffer**|  
|461|**Regelbuffer vooruitbetalingsfactuur**|  
|5637|**VA-fin. boekingsbuffer**|  
|7136|**Buffer artikelbudget**|  

## <a name="see-also"></a>Zie ook

[Dimensiesetposten - overzicht](design-details-dimension-set-entries-overview.md)  
[Ontwerpdetails: Dimensiecombinaties zoeken](design-details-searching-for-dimension-combinations.md)   
