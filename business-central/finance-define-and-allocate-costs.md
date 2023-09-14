---
title: Kosten definiëren en toewijzen
description: 'Tijdens kostenverdelingen worden kosten en opbrengsten verplaatst tussen kostensoorten , kostenplaatsen en kostenobjecten. U kunt zo veel verdelingen definiëren als u nodig hebt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Kosten definiëren en toewijzen

Tijdens kostenverdelingen worden kosten en opbrengsten verplaatst tussen kostensoorten , kostenplaatsen en kostenobjecten. U kunt zo veel verdelingen definiëren als u nodig hebt. Elke verdeling bestaat uit:  

- Een toewijzingsbron.  
- Een of meer verdeeldoelen.  

De verdelingsbron bepaalt welke kosten moeten worden verdeeld en de verdeeldoelen bepalen waaraan de kosten moeten worden toegewezen. Een verdelingsbron kan bijvoorbeeld zijn de kosten voor de kostensoort elektriciteit en verwarming. U kunt alle verwarmings- en elektriciteitskosten aan drie kostenplaatsen toewijzen: Werkplaats, Productie en Verkoop. Deze kostenplaatsen zijn uw verdeeldoelen.  

Voor elke verdelingsbron definieert u een verdelingsniveau, een geldigheidsperiode en een variant als groeperings-id. U kunt met behulp van een batchtaak filters instellen om verdelingsdefinities te selecteren en vervolgens wordt de kostenverdeling automatisch uitgevoerd.  

Voor elk verdeeldoel moet u een verdelingbasis definiëren. De verdelingbasis kan statisch of dynamisch zijn.  

- Statische toewijzingen zijn gebaseerd op een vaste waarde voor bijvoorbeeld oppervlak of een vastgestelde verdeelsleutel, zoals 5:2:4.  
- Dynamische toewijzingen zijn afhankelijk van wijzigbare waarden, bijvoorbeeld het aantal werknemers in een kostenplaats of de omzet van een kostenobject gedurende een bepaalde periode.  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

## Een verdelingsbron en doelen instellen

Elke toewijzing bestaat uit een verdelingsbron en een of meer verdeeldoelen. De verdelingsbron definieert welke kosten worden toegerekend. De verdeeldoelen bepalen waaraan de kosten worden toegerekend.  

### Kostenverdeling instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Kostenverdeling** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Kostenverdeling** de actie **Bewerken**.  
3. Geef een id voor de verdelingsbron op in het veld **ID**.  
4. Definieer een niveau als een getal tussen 1 en 99 in het veld **Niveau**. De verdelingsboeking volgt de volgorde van de niveaus.  
5. Voer een kostensoort in om te bepalen welke typen kosten worden toegerekend in het veld **Kostensoortbereik**. Als alle kosten voor een kostensoort worden toegerekend, wordt geen bereik gedefinieerd.  
6. Voer een kostenplaats met kosten in om toe te wijzen in het veld **Kostenplaatscode**.  
7. Voer een kostenobject met kosten in om toe te wijzen in het veld **Kostenobjectcode**. In de meeste gevallen blijft dit veld leeg, omdat kostenobjecten zelden worden toegewezen aan andere kostenobjecten.  
8. Voer een kostensoort in het veld **Credit naar kostensoort** in. De kosten die zijn toegewezen worden gecrediteerd aan de bronkostensoort. De creditboeking wordt geboekt naar de hier opgegeven kostensoort.  
9. Definieer de toewijzingsdoelen op het sneltabblad **Regels**. Voer op de eerste regel een kostensoort in het veld **Doelkostensoort** in. Hiermee wordt gedefinieerd van welke kostensoort de toerekening wordt gedebiteerd.  
10. Voer op de eerste regel het eerste toewijzingsdoel in het veld **Doelkostenplaats** **Doelkostenobject** in. Deze twee velden definiëren van welke kostenplaats of kostenobject de toewijzing wordt gedebiteerd. U kunt slechts een van deze velden invullen, maar niet beide.  
11. Herhaal de dezelfde stappen op de tweede regel om extra verdeeldoelen in te stellen.  
12. Nadat u het verdeeldoel en de verdelingsbronnen hebt ingesteld, kiest u de actie **Verdeelsleutel berekenen** om de totaalwaarden van de aandelen te berekenen.  

> [!NOTE]  
> Selecteer het selectievakje **Geblokkeerd** om de toewijzingsinstelling te deactiveren.

## Filters instellen voor dynamische toewijzingsgrondslagen

De methode voor dynamische toewijzing is gebaseerd op wijzigbare waarden. Bijvoorbeeld het aantal werknemers in een kostenplaats, of de verkochte artikelen van een kostenobject in een bepaalde periode. Er zijn negen vooraf gedefinieerde toewijzingsgrondslagen en twaalf dynamische periodes. U stelt verschillende filters in op basis van de toewijzingsgrondslag.  

### Filters instellen

De volgende tabel laat zien welke filters mogelijk zijn voor de verschillende toewijzingsgrondslagen en welke waarden geldig zijn in de velden **Nr.-filter** en **Groepfilter**. Selecteer <kbd>F1</kbd> in het veld **Datumfiltercode** om gedetailleerde omschrijvingen te lezen.  

|**Basis**|**Nr.-filter**|**Datumfiltercode**|**Kostenplaatsfilter**|**Kostenobjectfilter**|**Groepfilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Grootboekposten|Grootboekrekening|Ja|Ja|Ja|N.v.t.|  
|Grootboekbudgetposten|Grootboekrekening|Ja|Ja|Ja|Budgetnaam|  
|Kostensoortposten|Toeslagsoort|Ja|Ja|Ja|N.v.t.|  
|Kostenbegrotingsposten|Toeslagsoort|Ja|Ja|Ja|Budget|  
|Aantal werknemers|N.v.t.|Ja|Ja|Ja|N.v.t.|  
|Artikelen verkocht (aantal)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|  
|Artikelen ingekocht (aantal)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|  
|Artikelen verkocht (bedrag)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|  
|Artikelen ingekocht (bedrag)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|

## Scenario 1: statische toewijzingen op basis van de verdeelsleutel definiëren

De methode voor statische toewijzingen baseert zich op een vaste waarde voor bijvoorbeeld gebruikte vierkante meters of een vastgestelde verdeelsleutel, zoals 5:2:4.  

In dit onderwerp wordt beschreven hoe u drie nieuwe verdeeldoelen voor kostenobjecten kunt definiëren voor de verdelingsbron van kostenplaats PROD met behulp van de vastgestelde verdeelsleutel 5: 2: 4. De drie doelkostenobjecten zijn ACCESSO, VERF en TOEBEHOREN.  

> [!NOTE]  
> In het voorbeeld worden de demogegevens in de [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt.  

### De verdelingsbron van kostenplaats PROD op het sneltabblad Algemeen definiëren  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Kostenverdeling** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Kostenverdeling** de actie **Nieuw**.  
3. Selecteer in het veld **ID** op <kbd>Enter</kbd> of voer een id in.  
4. Geef **1** op in het veld **Niveau**.  
5. Voer in de velden **Geldig vanaf** en **Geldig tot** juiste datums in.  
6. Voer in het veld **Kostenplaatscode** **PROD** in.  
7. Voer in het veld **Credit naar kostensoort** het kostensoort **9903** in.  

### Verdeeldoelen voor kostenobjecten op de sneltabblad Regels definiëren  

1. Voer op de eerste regel in het veld **Doelkostensoort** **9903** in.  
2. Selecteer op de eerste regel in het veld **Doelkostenobject** **ACCESSO**.  
3. Selecteer op de eerste regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.  
4. Op de eerste regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.  
5. Op de eerste regel in het veld **Deel** voert u de verdeelsleutel **5** in.  
6. Voer op de tweede regel in het veld **Doelkostensoort** **9903** in.  
7. Selecteer op de tweede regel in het veld **Doelkostenobject** **PAINT**.  
8. Selecteer op de tweede regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.  
9. Op de tweede regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.  
10. Op de tweede regel in het veld **Deel** voert u de verdeelsleutel **2** in.  
11. Voer op de derde regel in het veld **Doelkostensoort** **9903** in.  
12. Selecteer op de derde regel in het veld **Doelkostenobject** **FITTINGS**.  
13. Selecteer op de derde regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.  
14. Op de derde regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.  
15. Op de derde regel in het veld **Deel** voert u de verdeelsleutel **4** in.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] berekent automatisch het veld **Percentage** met een percentage dat wordt bepaald door alle drie de verdeelsleutels die zijn ingevoerd in het veld **Deel** voor alle drie de regels.

## Scenario 2: Dynamische toewijzingen op basis van de verkochte artikelen definiëren

Dit onderwerp bevat een voorbeeld van het definiëren van toewijzingen met behulp van de methode voor dynamische toewijzing. In het voorbeeld wijzigt u de dynamische toewijzing van de kosten voor kostenplaats VERKOOP ter ondersteuning van het nieuwe kostenobject IT-APPARATUUR. Pakketten voor IT-APPARATUUR hebben artikelnummers in het bereik van 8904-W t/m 8924-W. De verkoopcijfers van het vorige jaar kunt u gebruiken om het aandeel te berekenen. De toewijzing wordt geboekt op het ondersteunende kostensoort 9903.  

> [!NOTE]  
> In het voorbeeld worden de demogegevens in de [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt.  

### Dynamische toewijzingen definiëren op basis van artikelen die het vorige jaar zijn verkocht  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenverdelingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Kostenverdeling** de actie **Nieuw**.  
3. Selecteer in het veld **ID** op <kbd>Enter</kbd> of voer een id in.  
4. Geef **1** op in het veld **Niveau**.  
5. Voer in de velden **Geldig vanaf** en **Geldig tot** juiste datums in.  
6. Voer in het veld **Kostenplaatscode** **SALES** in.  
7. Voer in het veld **Credit naar kostensoort** het kostensoort **9903** in.  
8. Voer in het veld **Doelkostensoort** het kostensoort **9903** in.  
9. Kies in het veld **Doelkostenobject** de optie **Nieuw** om een nieuw kostenobject IT-APPARATUUR te maken en vul waar nodig de velden in. Selecteer **IT-APPARATUUR**. Laat het veld **Doelkostenplaats** leeg.  
10. Selecteer in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe alle gecumuleerde kosten moeten worden toegewezen.  
11. In het veld **Basis** selecteert u de toewijzingsbasis **Artikelen verkocht (bedrag)**.  
12. Voer in het veld **Nr.-filter** **8904-W..8924-W** in.  
13. Voer in het veld **Datumfiltercode** **Vorig jaar** in.  
14. Kies de actie **Verdeelsleutel berekenen** om het aandeel te berekenen.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de verkoopcijfers van de voorgaande jaren voor het berekenen van een aandeel van 1596,50 LV met 100 procent voor de pakketten voor IT-APPARATUUR. Dit betekent dat alle artikelen die vorig jaar zijn verkocht, worden toegewezen aan kostenobject IT-APPARATUUR.

## Zie gerelateerde [Microsoft-training](/training/modules/allocate-costs-dynamics-365-business-central/)

## Zie ook

 [Kostenboekhouding instellen](finance-set-up-cost-accounting.md)  
 [Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)  
 [Kosten verantwoorden](finance-manage-cost-accounting.md)  
 [Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)  
 [Kostprijsboekhouding](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
