---
title: Problemen met dimensies oplossen en dimensies corrigeren
description: Leer hoe u typische dimensiefouten oplost en hoe u dimensies corrigeert nadat ze zijn gebruikt voor geboekte transacties.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 09/27/2021
ms.author: bholtorf
---

# <a name="troubleshooting-and-correcting-dimensions" />Problemen met dimensies oplossen en dimensies corrigeren

Financiële rapportage en analyseweergaven zijn vaak gebaseerd op gegevens uit dimensies. Ondanks de voorzorgsmaatregelen die er zijn, doet zich soms een fout voor die tot onnauwkeurigheden kan leiden. In dit onderwerp worden enkele van de typische fouten beschreven en wordt uitgelegd hoe u dimensietoewijzingen op geboekte transacties kunt corrigeren, zodat financiële rapporten nauwkeurig zijn.

## <a name="troubleshooting-dimensions-errors" />Problemen oplossen met dimensiefouten

Wanneer u documenten of dagboekregels boekt die dimensies bevatten, kunnen verschillende fouten optreden die doorgaans aan onjuiste dimensie-instellingen of -toewijzingen zijn gerelateerd.

> [!NOTE]
> In de volgende lijst van potentiële foutmeldingen, zijn *%X*-codes tijdelijke aanduidingen voor de gegevensvariabelen die het feitelijke bericht bevat in de UI, afhankelijk van de context. Bijvoorbeeld *%1 %2 is geblokkeerd.* kan in de UI worden weergegeven als 'Dimensiecode AREA is geblokkeerd".  

|Verzenden|Foutmelding|Mogelijke oplossing|
|-----|-------------|-----------------|
|Geblokkeerde dimensie|%1 %2 is geblokkeerd.|-Niet-geboekte documenten zoeken die de dimensieset bevatten met de geblokkeerde dimensie, en deze deblokkeren.<br />-De dimensiesetregel verwijderen voor de geblokkeerde dimensie.|
|Verwijderde dimensie|%1 %2 kan niet worden gevonden.|-De ontbrekende dimensie herstellen.<br />-Niet-geboekte documenten zoeken die de dimensieset bevatten met de ontbrekende dimensie en deze toevoegen.<br />-De dimensiesetregel verwijderen voor de ontbrekende dimensie.|
|Geblokkeerde dimensiewaarde|%1 %2 - %3 is geblokkeerd.|-Niet-geboekte documenten zoeken die de dimensieset bevatten met de geblokkeerde dimensiewaarde, en deze deblokkeren.<br />-De dimensiesetregel verwijderen voor de geblokkeerde dimensiewaarde.|
|Verwijderde dimensiewaarde|    %1 voor %2 ontbreekt.|-De ontbrekende dimensiewaarde herstellen.<br />-Niet-geboekte documenten zoeken die de dimensieset bevatten met de ontbrekende dimensiewaarde en deze toevoegen.<br />-De dimensiesetregel verwijderen voor de ontbrekende dimensiewaarde.|
|Verboden dimensiewaarde|Dimensiewaardetype voor %1 %2 - %3 mag niet %4 zijn.|-Het veld **Dimensiewaardesoort** op de pagina **Dimensiewaarden** wijzigen in **Standaard** of **Begintotaal**.<br />-De dimensiesetregel verwijderen voor de geblokkeerde dimensiewaarde.|
|Geblokkeerde dimensiecombinatie|Dimensies %1 en %2 kunnen niet gelijktijdig gebruikt worden.|-Niet-geboekte documenten zoeken die de dimensieset bevatten met de geblokkeerde dimensiecombinatie en deze deblokkeren.<br />-Een van de conflicterende machtigingensetregels wijzigen voor de dimensiecombinatie.|
|Geblokkeerde dimensiewaardecombinatie|Dimensiecombinaties %1 - %2 en %3 - %4 kunnen niet gelijktijdig gebruikt worden.|-Niet-geboekte documenten zoeken die de dimensieset bevatten met de geblokkeerde dimensiewaardecombinatie en deze deblokkeren.<br />-Een van de conflicterende machtigingensetregels wijzigen voor de dimensiewaardecombinatie.|
|Lege dimensiewaardecode voor standaarddimensie waarvoor het veld **Waardeboeking** **Verplicht** bevat|-Een %1 voor de %2 %3 selecteren.<br />-Een %1 voor de %2 %3 voor %4 %5 selecteren.|-Het veld **Waardeboeking** op de pagina **Standaarddimensie** wijzigen.<br />-Een niet-lege dimensiewaarde invoeren voor de conflicterende dimensie in de dimensieset.|
|Verkeerde dimensiewaardecode voor standaarddimensie waarvoor het veld **Waardeboeking** **Zelfde** bevat|-%1 %2 voor de %3 %4 selecteren.<br />-%1 %2 voor de %3 %4 voor %5 %6 selecteren.|-Het veld **Waardeboeking** op de pagina **Standaarddimensie** wijzigen.<br />-De vereiste dimensiewaarde invoeren voor de conflicterende dimensie in de dimensieset.|
|Niet-lege dimensiewaardecode invoeren voor lege standaarddimensie waarvoor het veld **Waardeboeking** **Zelfde** bevat|-%1 %2 moet leeg zijn.<br />-%1 %2 moet leeg zijn voor %3 %4.|-Het veld **Waardeboeking** op de pagina **Standaarddimensie** wijzigen.<br />-Een lege dimensiewaardecode invoeren voor de conflicterende dimensie in de dimensieset.|
|Onverwachte dimensiewaarde voor standaarddimensie waarvoor het veld **Waardeboeking** **Geen** bevat|-%1 %2 mag niet vermeld worden.<br />-%1 %2 mag niet vermeld worden voor %3 %4.|-Het veld **Waardeboeking** op de pagina **Standaarddimensie** wijzigen.<br />-De conflicterende regel verwijderen uit de dimensieset.|
|Een dimensiecorrectie wordt niet correct voltooid.||-Kies **Opnieuw instellen** om de correctie terug te zetten naar een conceptstaat. Hierdoor worden de wijzigingen opnieuw ingesteld en kunt u de correctie opnieuw uitvoeren.|

## <a name="changing-dimension-assignments-after-posting" />Dimensietoewijzingen wijzigen na boeking

Als u ontdekt dat een onjuiste dimensie is gebruikt voor geboekte grootboekposten, kunt u de dimensiewaarden corrigeren en uw analyseweergaven bijwerken. Zo blijven uw financiële rapporten en analyses nauwkeurig.

> [!IMPORTANT]
> De functies voor het corrigeren van dimensies zijn alleen bedoeld om de financiële rapportage accuraat te maken. Dimensiecorrecties zijn alleen van toepassing op de grootboekboekingen. Ze wijzigen niet de dimensies die zijn toegewezen aan de posten in andere grootboeken voor dezelfde transactie. Er is een mismatch tussen de dimensies die zijn toegewezen in het grootboek en de subgrootboeken.

### <a name="setting-up-dimension-corrections" />Dimensiecorrecties instellen

Er zijn twee dingen waarmee u rekening moet houden bij het instellen van dimensiecorrecties:

* Zijn er dimensies waarvan u niet wilt dat mensen ze veranderen? Geef op de pagina **Instellingen van dimensiecorrectie** de dimensies op die u wilt blokkeren voor wijzigingen.
* Wie wilt u toestaan dimensies te veranderen? Als u personen wilt toestaan wijzigingen aan te brengen, wijst u de machtiging **D365 dimensiecorrectie** toe aan de gebruikers. Met de machtigingen kunnen ze dimensiecorrecties maken, uitvoeren en indien nodig ongedaan maken. Ze kunnen ook geblokkeerde dimensies opgeven. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie. 

### <a name="correcting-a-dimension" />Een dimensie corrigeren

U kunt handmatig een of meer grootboekposten selecteren of filters gebruiken om sets met posten te selecteren. Indien nodig kunt u ook dimensies toevoegen of verwijderen. 

1. Gebruik een van de volgende pagina's om een dimensiecorrectie te starten:

    * Op de pagina **Grootboekjournaalnr.** door een register te selecteren en vervolgens de actie **Dimensies corrigeren** te kiezen. Dit start een correctie voor de posten in het geselecteerde register.
    * Op de pagina **Grootboekposten** door de actie **Dimensiecorrectie** te kiezen. 

2. Voer in het veld **Beschrijving** informatie over de wijziging in. Andere mensen kunnen deze informatie later gebruiken om te begrijpen wat er is gedaan.
3. Kies op het sneltabblad **Geselecteerde posten** de relevante posten.

    > [!IMPORTANT]
    > Als u een selectie wijzigt, worden de waarden op het sneltabblad **Wijzigingen van dimensiecorrectie** opnieuw ingesteld. Selecteer daarom altijd de posten voordat u wijzigingen in de dimensiewaarden opgeeft.

   De volgende tabel beschrijft de opties.

   |Optie  |Omschrijving  |
   |---------|---------|
   |Gerelateerde posten toevoegen     |Voeg grootboekposten toe die in hetzelfde grootboekregister staan.|   
   |Toevoegen per filter     |Gebruik filtercriteria bij het toevoegen van grootboekposten.|
   |Handmatige selectie     |Selecteer specifieke grootboekposten.         |
   |Toevoegen per dimensie     |Filter grootboekposten op dimensies.         |
   |Posten verwijderen     |Grootboekposten deselecteren.         |
   |Selectiecriteria beheren     |Houd het selectieproces bij en maak indien nodig selecties ongedaan.         |

4. Kies op het tabblad **Wijzigingen van dimensiecorrectie** de dimensie die u wilt wijzigen in het veld **Dimensiecode** en de nieuwe waarde in het veld **Nieuwe dimensiewaardecode**.
5. Kies om de correctie te valideren **Dimensiewijzigingen valideren**. Zie voor meer informatie [Dimensiecorrecties valideren](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Kies **Uitvoeren**.

### <a name="validating-dimension-corrections" />Dimensiecorrecties valideren

Voordat u een correctie uitvoert, is het een goed idee om deze eerst te valideren. Validatie controleert op beperkingen voor het boeken van waarden voor de grootboekrekeningen, beperkingen voor dimensies en of de dimensiewaarden zijn geblokkeerd. Tijdens validatie wordt de status van de correctie ingesteld op **Validatie bezig**. Nadat u een correctie heeft gevalideerd, wordt het resultaat weergegeven in het veld **Validatiestatus**. Als er fouten zijn gevonden, kunt u de actie **Fouten bekijken** gebruiken om ze te onderzoeken. Nadat u een fout heeft gecorrigeerd, moet u de actie **Opnieuw openen** gebruiken om de correctie of een nieuwe validatie uit te voeren.

U kunt een correctie onmiddellijk uitvoeren of deze op een later tijdstip plannen. Als u correcties uitvoert op een grote gegevensset, raden we u aan deze buiten kantooruren te plannen. Zie voor meer informatie [Dimensiecorrecties op grote gegevenssets](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction" />Een correctie ongedaan maken

Nadat u een dimensie hebt gecorrigeerd en u niet tevreden bent met wat u ziet, kunt u de actie **Ongedaan maken** gebruiken om de vorige waarde opnieuw in te stellen. U kunt echter alleen de meest recente correctie ongedaan maken. Voordat u een correctie ongedaan maakt, kunt u de wijzigingen valideren die door het ongedaan maken worden aangebracht. Dit is bijvoorbeeld handig als dimensiebeperkingen zijn gewijzigd nadat de correctie is aangebracht.

Als de actie Ongedaan maken niet beschikbaar is, bijvoorbeeld omdat u veel correcties hebt aangebracht, kunt u de actie **Kopiëren naar concept** gebruiken om een nieuwe correctie te starten voor dezelfde posten.

### <a name="dimension-corrections-on-large-data-sets" />Dimensiecorrecties op grote gegevenssets

Wees voorzichtig bij het corrigeren van grote sets posten, bijvoorbeeld sets die meer dan 10.000 items bevatten. Als u kunt, raden we u aan om de filters te gebruiken om de correcties op kleinere gegevenssets uit te voeren. Het is ook een goed idee om correcties buiten de normale kantooruren uit te voeren. 

### <a name="use-analysis-views-with-dimension-corrections" />Analyseweergaven gebruiken met dimensiecorrecties

Als **Bijwerken bij boeking** is ingeschakeld voor een analyseweergave, kan [!INCLUDE[prod_short](includes/prod_short.md)] zien wanneer documenten en dagboeken worden geboekt. U kunt ook weergaven bijwerken met deze instelling ingeschakeld met resultaten van dimensiecorrecties. Schakel hiervoor de schakeloptie **Analyseweergaven bijwerken** in. Het bijwerken van analyseweergaven kan van invloed zijn op de prestaties, vooral bij grote gegevenssets, dus we raden u aan analyseweergaven alleen bij te werken voor kleine gegevenssets.  

### <a name="viewing-historical-dimension-corrections" />Historische dimensiecorrecties bekijken

Als een grootboekpost is gecorrigeerd, kunt u de wijziging onderzoeken met de actie **Historie van dimensiecorrecties**.

### <a name="handling-incomplete-corrections" />Omgaan met onvolledige correcties

Als een correctie niet wordt voltooid, wordt er een waarschuwing weergegeven op de correctiekaart. Als dat gebeurt, kunt u de actie **Opnieuw instellen** gebruiken om de correctie terug te zetten naar een conceptstatus en de wijzigingen ongedaan te maken. U kunt de correctie dan opnieuw uitvoeren.

> [!NOTE]
> Het opnieuw instellen van een onvolledige correctie heeft geen invloed op updates van analyseweergaven, omdat deze plaatsvinden aan het einde van het correctieproces.

### <a name="use-cost-accounting-with-corrected-gl-entries" />Kostprijsboekhouding gebruiken met gecorrigeerde grootboekboekingen

Nadat u de dimensies heeft aangepast, zijn uw gegevens voor kostprijsboekhouding niet meer gesynchroniseerd. Kostprijsboekhouding gebruikt dimensies om bedragen voor kostenplaatsen en kostenobjecten te aggregeren en om kostentoewijzingen uit te voeren. Als u de dimensies voor grootboekboekingen wijzigt, betekent dit waarschijnlijk dat u uw kostenberekeningsmodellen opnieuw uitvoert. Of u slechts een paar kostenregisters moet verwijderen en toewijzingen opnieuw moet uitvoeren of dat u alles moet verwijderen en al uw modellen opnieuw moet uitvoeren, hangt af van de gegevens die zijn bijgewerkt en hoe uw kostenberekeningsmogelijkheden zijn ingesteld. U moet handmatig identificeren waar dimensiecorrecties van invloed zijn op de kostenberekening en waar updates nodig zijn. [!INCLUDE[prod_short](includes/prod_short.md)] biedt momenteel geen geautomatiseerde manier om dat te doen.

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/modules/dimensions-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Werken met dimensies](finance-dimensions.md)  
[Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
