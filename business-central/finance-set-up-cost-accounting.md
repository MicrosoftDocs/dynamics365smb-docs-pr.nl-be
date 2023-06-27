---
title: Kostenboekhouding instellen
description: 'Voordat u begint te werken met kostprijsboekhouding, moet u instelling uitvoeren. Aan elke kostenpost moet een kostensoort zijn toegewezen evenals een kostenplaatscode of kostenobject.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1112, 1113, 1122'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="setting-up-cost-accounting" />Kostenboekhouding instellen

Voordat u begint te werken met kostprijsboekhouding, moet u insteltaken uitvoeren.

## <a name="balances-between-cost-type-cost-center-and-cost-object" />Saldi tussen kostensoort, kostenplaats en kostenobject

Wanneer u kostprijsboekhouding instelt, moet u ervoor zorgen dat alle posten zijn toegewezen aan een kostensoort , alsmede een kostenplaats of kostenobject. Dat betekent dat aan elke kostenpost een kostensoort moet zijn toegewezen evenals een kostenplaatscode of kostenobject. Deze regel zorgt ervoor dat elke kostenpost wordt weergegeven in hetzij de kostenplaatsen of de kostenobjecten, maar nooit op beide locaties.  

Op deze manier maakt u de volgende boekhoudvergelijking:  

*Kostentypesaldo* = *Kostenplaatssaldo* + *Kostenobjectsaldo*  

Wanneer u de grafiek van de kostensoort, de grafiek van de kostenplaatsen en de grafiek van de kostenobjecten in de rapporten afdrukt, kunt u deze relatie analyseren.

## <a name="setting-up-cost-types" />Kostensoorten instellen

Een kostensoortschema lijkt op het rekeningschema in het grootboek. U kunt het kostensoortschema op de volgende manieren instellen:  

- Geef het kostensoortschema een structuur die vergelijkbaar is met de resultatenrekeningen in het grootboekrekeningschema. Vervolgens kunt u het grootboekrekeningschema overbrengen naar het kostensoortschema. U kunt elke gewenste aanpassing na de overdracht aanbrengen.  
- Maak nieuwe kostensoortschema's of voeg nieuwe kostensoorten toe aan bestaande kostensoortschema's. U moet elke nieuwe kostensoort afzonderlijk maken.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types" />Het grootboekrekeningschema overbrengen naar het kostensoortschema

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostensoortschema** in en kies de gerelateerde koppeling.  
2. Kies de actie **Kostensoorten ophalen uit rekeningschema**. Kies in dialoogvenster de knop **Ja** om de overdracht te bevestigen. De functie maakt gebruik van het rekeningschema om een kostensoortschema te maken.  

    Het kostensoortschema bevat nu alle resultatenrekeningen in het grootboek inclusief koppen en subtotalen. U kunt het kostensoortschema zo nodig wijzigen. U kunt bijvoorbeeld dubbele kostensoorten verwijderen.  

    > [!IMPORTANT]  
    >  De functie **Kostensoorten registreren in rekeningschema** werkt de relatie tussen het rekeningschema en het kostensoortschema bij. Het veld **Nr.** wordt ingevuld en gecontroleerd om ervoor te zorgen dat iedere grootboekrekening slechts aan één kostensoort is gerelateerd. De functie wordt automatisch uitgevoerd voordat deze van grootboekposten naar kostprijsboekhouding wordt overgebracht.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page" />Nieuwe kostensoorten instellen op de pagina Kostensoortschema

1. Open de pagina **Kostensoortschema** in de bewerkmodus.  
2. Vul de velden indien nodig in zoals beschreven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  U kunt kostensoorten instellen en onderhouden op de pagina **Kostensoortkaart** of op de pagina **Kostensoortschema**. In deze procedure stelt u kostensoorten op de pagina **Kostensoortschema** in.

3. Nadat u alle kostensoorten hebt gemaakt, kiest u de actie **Kostensoorten inspringen**. Kies in het dialoogvenster de knop **Ja**.  
4. Koppel het nieuwe kostensoort aan de corresponderende grootboekrekening.  

    > [!IMPORTANT]  
    >  Als u definities hebt ingevoerd in de **Samentelling**-velden voor het regelsoort **Eindtotaal** voordat u de functie **Kostensoorten inspringen** uitvoert, moet u de definities opnieuw invoeren omdat de functie de waarden in alle velden **Eindtotaal** overschrijft.  

### <a name="to-update-cost-types" />Kostensoorten bijwerken

1. Op de pagina **Instelling kostprijsboekhouding** selecteert u of het kostensoortschema automatisch wilt laten bijwerken als het rekeningschema wordt gewijzigd.  
2. In het veld **Grootboekrekening afstemmen** kunt u kiezen uit de volgende opties.  

- in **Geen uitlijning** - er wordt geen overeenkomstige wijziging in het kostensoortschema doorgevoerd als u het rekeningschema wijzigt.  
- **Geen uitlijning** - er wordt een overeenkomstige wijziging doorgevoerd in het kostensoortschema als u het rekeningschema wijzigt.  
- **Vragen** - wanneer u een wijziging aanbrengt in het rekeningschema krijgt u een bericht waarin u wordt gevraagd of u de overeenkomstige wijziging in het kostensoortschema wilt maken.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts" />De relatie tussen de kostensoorten en grootboekrekeningen definiëren

De relatie tussen het kostensoort en de grootboekrekening wordt gemaakt in het kostensoort en in de grootboekrekening.  

- Het veld **Grootboekrekeningbereik** in de tabel **Kostensoort** bepaalt welke grootboekrekeningen tot een kostensoort behoren.  
- Het veld **Nr. saldokostensoort** in het rekeningschema bepaalt tot welk kostensoort een grootboekrekening behoort.  

Deze twee velden worden automatisch ingevuld wanneer u de functie **Kostensoorten ophalen uit rekeningschema** gebruikt.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types" />Relatie tussen de grootboekrekeningen en kostensoorten

Er bestaat een n:1-relatie tussen de grootboekrekeningen en kostensoorten Verschillende grootboekrekeningen kunnen tot één kostensoort behoren, maar elke afzonderlijke grootboekrekening behoort maar tot één kostensoort. De volgende tabel beschrijft de detail in de relatie.  

|Relatie|**Grootboekrekeningbereik**|**Nr. kostensoort**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Één grootboekrekening voor elk kostensoort|Eén grootboekrekening|Eén kostensoort|  
|Verschillende grootboekrekeningen voor één kostensoort|Bijvoorbeeld rekeningenbereik grootboek 7110..7193 voor elke grootboekrekening|Voor elke grootboekrekening in het bereik is slechts één kostensoort|  
|Kostensoorten zonder overeenkomende grootboekrekeningen|\<Empty\>||  
|Grootboekrekeningen waarvan de posten niet overgebracht worden||\<Empty\>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger" />Kostensoorten zonder relatie met het grootboek

Er bestaat mogelijk geen relatie tussen een kostensoort en grootboekrekeningen als aan een van de volgende voorwaarden wordt voldaan:  

- Rekeningen voor operationeel boekhouden zoals voor het de berekenen van rente en afschrijvingen, nemen alleen de kosten mee van de operationele boekhouding.  
- Ondersteunende kostensoorten, zoals kostensoorten 9901, 9902 en 9903 in de [!INCLUDE[prod_short](includes/prod_short.md)]-database , worden gebruikt als credit- of debet-rekeningen voor toewijzingen.  
- De ondersteunende rekening, 9920 in de [!INCLUDE[prod_short](includes/prod_short.md)]-database, bevat de werkelijke overlopende transitoria die het verschil laten zien tussen de kosten en de onkosten uit het grootboek.

## <a name="setting-up-cost-centers" />Kostenplaatsen instellen

Kostenplaatsen zijn afdelingen die verantwoordelijk zijn voor kosten en opbrengsten. Het schema van kostenplaatsen is vergelijkbaar met de dimensiegegevens voor het grootboek. U kunt het schema van kostenplaatsen op de volgende manieren instellen:  

- Door de dimensiewaarden in het grootboek over te brengen naar het schema van kostenplaatsen. U kunt elke gewenste aanpassing na de overdracht aanbrengen.  
- Door een nieuw schema van kostenplaatsen te maken dat onafhankelijk is van het grootboek of door een nieuwe kostenplaats toe te voegen aan een bestaand schema van kostenplaatsen. U moet elke kostenplaats afzonderlijk maken.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers" />Dimensiewaarden in het grootboek overbrengen naar het schema van kostenplaatsen

1. Stel een dimensie als kostenplaats in met de pagina **Dimensies kostprijsboekhouding bijwerken**. Alleen de waarden uit deze dimensie worden overgebracht.  
2. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenplaatsschema** in en kies de gerelateerde koppeling.  
3. Op het tabblad **Acties** in de groep **Functies** kiest u **Kostenplaatsen ophalen uit dimensie** om dimensiewaarden over te brengen naar het schema van kostenplaatsen. Met deze functie worden de dimensiewaarden die u in stap 1 hebt gedefinieerd overgebracht.  

    > [!NOTE]  
    >  U kunt het veld **Kostenplaatsdimensie afstemmen** zo instellen dat hiermee een eenrichtingssynchronisatie van dimensiewaarden uit het grootboek op het kostenplaatsschema wordt gedefinieerd. U kunt geen synchronisatie van het schema van kostenplaatsen met dimensiewaarden uit het grootboek definiëren.  

Het schema van kostenplaatsen bevat nu alle opgegeven dimensiewaarden van het grootboek waaronder titels en subtotalen.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page" />Nieuwe kostenplaatsen maken op de pagina Kostenplaatsschema

U kunt kostenplaatsen instellen en onderhouden op de kaart **Kostenplaatskaart** of op de pagina **Kostenplaatsschema**. In deze procedure stelt u kostenplaatsen op de pagina **Kostenplaatsschema** in.  

1. Open de pagina **Kostenplaatsschema** in de bewerkmodus.  
2. Voer in het veld **Code** de kostenplaatscode in. Alle kostenplaatsen moeten een code hebben.  
3. Voer in het veld **Naam** de naam van de kostenplaats in.  
4. Kies de vervolgkeuzepijl in het veld **Regelsoort** om het doel van de kostenplaats aan te geven.  

    - Voor kostenplaatsen van het soort **Totaal** moet u het veld **Samentelling** invullen. Gebruik de operator **of**, die uit een verticale lijn (**&#124;**) bestaat om bereiken voor kostenplaatsen in te stellen.  
    - Voor kostenplaatsen van het regelsoort **Eindtotaal** wordt dit veld automatisch ingevuld wanneer u de inspringfunctie gebruikt.  
5. Vul de velden **Sorteervolgorde** en **Kostensubtype** in.  
6. Kies de volgende lege regel om een nieuwe kostenplaats te maken en herhaal vervolgens stap 2 tot en met 5.  
7. Nadat u alle kostenplaatsen hebt ingesteld, kiest u de actie **Kostenplaatsen inspringen**. Kies de knop **Ja**.  

> [!IMPORTANT]  
> Als u definities in de velden **Samentelling** voor de kostenplaatsen **Eindtotaal** hebt ingevoerd voordat u de inspringfunctie uitvoerde, moet u deze opnieuw invoeren. De functie overschrijft de waarden in alle velden **Eindtotaal**.

## <a name="setting-up-cost-objects" />Kostenobjecten instellen

Kostenobjecten zijn projecten, producten of diensten van een bedrijf. Het schema van kostenobjecten is vergelijkbaar met de dimensiegegevens voor het grootboek. U kunt het schema van kostenobjecten op de volgende manieren instellen:  

* Door de dimensiewaarden in het grootboek over te brengen naar het schema van kostenobjecten. U kunt elke gewenste aanpassing na de overdracht aanbrengen.  
* Door een nieuw schema van kostenobjecten te maken dat onafhankelijk is van het grootboek of door een nieuw kostenobject toe te voegen aan een bestaand schema van kostenobjecten. U moet elk kostenobject afzonderlijk maken.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects" />Door de dimensiewaarden vanuit het grootboek over te brengen naar het schema van kostenobjecten.

1.  Stel een dimensie als kostenobjectdimensie in op de pagina **CA-dimensies bijwerken**. Alleen de waarden uit deze dimensie worden overgebracht.  
2.  Kies het pictogram ![Lampje dat de functie Vertel me 3 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenobjectschema** in en kies de gerelateerde koppeling.  
3.  Kies de actie **Kostenobjecten ophalen uit dimensie** om dimensiewaarden over te brengen naar het schema van kostenobjecten. Met deze functie worden de dimensiewaarden die u in stap 1 hebt gedefinieerd overgebracht.  

    > [!NOTE]  
    >  U kunt het veld **Kostenobjectdimensie afstemmen** zo instellen dat hiermee een eenrichtingssynchronisatie van dimensiewaarden uit het grootboek op het schema van kostenobjecten wordt gedefinieerd. U kunt geen synchronisatie van het schema van kostenobjecten met dimensiewaarden uit het grootboek definiëren.  

Het schema van kostenobjecten bevat nu alle opgegeven dimensiewaarden van het grootboek waaronder titels en subtotalen.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page" />Nieuwe kostenobjecten maken op de pagina Kostenobjectschema

U kunt kostenobjecten instellen en onderhouden op de kaart **Kostenobjectkaart** of op de pagina **Kostenobjectschema**. In deze procedure stelt u kostenobjecten op de pagina **Kostenobjectschema** in.  

1.  Open de pagina **Kostenobjectschema** in de bewerkmodus.  
2.  Voer in het veld **Code** de kostenobjectcode in. Alle kostenobjecten moeten een code hebben.  
3.  Voer in het veld **Naam** de naam van het kostenobject in.  
4.  Kies de vervolgkeuzepijl in het veld **Regelsoort** om het doel van het kostenobject aan te geven.  

    * Voor kostenobjecten van het regelsoort **Totaal** vult u het veld **Totaal van/tot** in. Gebruik de operator **of**, die uit een verticale lijn (**&#124;**) bestaat om bereiken voor kostenobjecten in te stellen.  
    * Voor kostenobjecten van het regelsoort **Eindtotaal** wordt dit veld automatisch ingevuld wanneer u de inspringfunctie gebruikt.  
5.  Vul het veld **Sorteervolgorde** in.  
6.  Kies de volgende lege regel om een nieuw kostenobject te maken en herhaal vervolgens stap 2 tot en met 5.  
7.  Nadat u alle kostenobjecten hebt ingesteld, kiest u de actie **Kostenobjecten inspringen**. Kies de knop **Ja**.  

> [!IMPORTANT]  
>  Als u definities in de velden **Totaal van/tot** voor de kostenobjecten **Eindtotaal** hebt ingevoerd voordat u de inspringfunctie uitvoert, moet u deze opnieuw invoeren. De functie overschrijft de waarden in alle velden **Eindtotaal**.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts" />Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren

In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak. Wanneer u de overdracht uitvoert, worden door [!INCLUDE[prod_short](includes/prod_short.md)] alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject. Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts" />Standaarddimensiewaarden definiëren voor grootboekrekeningen

Voor elke grootboekrekening definieert u standaarddimensiewaarden in de tabel **Standaarddimensie**. In het volgende voorbeeld ziet u hoe u kunt definiëren dat er altijd een AFDELING als kostenplaats, maar nooit een PROJECT als kostenobject moet voorkomen bij het boeken naar een grootboekrekening.  

|**Dimensiecode**|**Waardeboeking**|  
|------------------------------------------|-----------------------------------------|  
|Kostenplaats|Verplicht|  
|Kostendrager|Geen|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs" />Dimensiewaarden voor overheadkosten en directe kosten definiëren

 Overheadkosten kunt u overbrengen naar een kostenplaats en directe kosten naar een kostenobject. In de volgende tabel ziet u de optimale combinatie van instelwaarden voor dimensies.  

|Overbrengen naar|Kostenplaatsboeking|Kostenobjectboeking|  
|-----------------|-------------------------|-------------------------|  
|Kostenplaats|Verplicht|Geen|  
|Kostenobject|Geen|Verplicht|  

> [!NOTE]  
>  Zorg ervoor dat de vooraf gedefinieerde kostenplaats en het vooraf gedefinieerde kostenobject die u in het grootboek hebt ingesteld, automatisch naar de kostprijsboekhouding worden overgedragen, door het selectievakje **GB-boekingen controleren** op de pagina Instelling kostprijsboekhouding te selecteren.

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/modules/cost-accounting-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Kosten verantwoorden](finance-manage-cost-accounting.md)  
[Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)  
[Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
