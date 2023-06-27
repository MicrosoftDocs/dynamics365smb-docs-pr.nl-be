---
title: Valuta's instellen
description: U moet elke valuta instellen als u koopt of verkoopt in andere valuta's dan uw lokale valuta (LV) of als u grootboektransacties in verschillende valuta's vastlegt.
author: edupont04
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="set-up-currencies" />Valuta's instellen

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Gebruik een externe service om de laatste valutawisselkoersen op te halen in de lijst **Valuta's**. Zie [Een wisselkoersservice instellen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service) voor meer informatie.  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies" /><a name="curr"></a>Valuta's

In de volgende tabel worden de velden in de lijst **Valuta's** beschreven.

|Veld|Omschrijving|  
|---------------------------------|---------------------------------------|  
|**Code**|De identifier voor de valuta.|
|**Beschrijving**|Een vrije tekstbeschrijving van de valuta.|
|**ISO-code**|De internationale drielettercode voor de valuta, die is gedefinieerd in ISO 4217.|
|**Numerieke ISO-code**|De internationale numerieke verwijzing naar de valuta, die is gedefinieerd in ISO 4217.|
|**Wisselkoersdatum**|De laatste actuele wisselkoersdatum.|
|**EMU-valuta**|Geeft aan of de valuta een EMU-valuta (Economische en Monetaire Unie) is, zoals de EUR.|
|**Gerealiseerde winstrekening**|De rekening waarop de werkelijke winst wordt geboekt wanneer u betalingen voor vorderingen ontvangt of de werkelijke valutakoers voor betalingen aan schulden registreert. Zie het voorbeeld onder deze tabel voor een voorbeeld van een te ontvangen valutatransactie. |
|**Gerealiseerde verliesrekening**|De rekening waarop het werkelijke verlies wordt geboekt wanneer u betalingen voor vorderingen ontvangt of de werkelijke valutakoers voor betalingen aan schulden registreert. Zie het voorbeeld onder deze tabel voor een voorbeeld van een te ontvangen valutatransactie. |
|**Ongerealiseerde winstrekening**|De rekening waarop de theoretische winst wordt geboekt wanneer u een valutacorrectie uitvoert.|
|**Ongerealiseerde verliesrekening**|De rekening waarop het theoretische verlies wordt geboekt wanneer u een valutacorrectie uitvoert.|
|**Bedragafrondingsprecisie**|Sommige valuta's hebben andere notaties voor factuurbedragen dan zijn gedefinieerd op de pagina **Grootboek instellen**. Als u de bedragafrondingsprecisie voor een valuta wijzigt, worden alle factuurbedragen in die valuta afgerond met de bijgewerkte precisie.|
|**Bedragdecimalen**|Sommige valuta's hebben andere notaties voor factuurbedragen dan zijn gedefinieerd op de pagina **Grootboek instellen**. Als u de bedragdecimalen voor een valuta wijzigt, worden alle factuurbedragen in die valuta afgerond met de bijgewerkte decimalen|
|**Factuurafrondingsmethode**|Specificeert de methode die moet worden gebruikt als de bedragen moeten worden afgerond. De opties zijn: **Dichtstbijzijnd**, **Omhoog** en **Omlaag**.|
|**Afrondingsprecisie van eenheidsbedragen**|Sommige valuta's hebben andere notaties voor eenheidsbedragen dan zijn gedefinieerd op de pagina **Grootboek instellen**. Als u de afrondingsprecisie van eenheidsbedragen voor een valuta wijzigt, worden alle eenheidsbedragen in die valuta afgerond met de bijgewerkte precisie.|
|**Eenheidsbedragdecimalen**|Sommige valuta's hebben andere notaties voor eenheidsbedragen dan zijn gedefinieerd op de pagina **Grootboek instellen**. Als u de eenheidsbedragdecimalen voor een valuta wijzigt, worden alle eenheidsbedragen in die valuta afgerond met de bijgewerkte decimalen.|
|**Vereffeningsafrondingsprecisie**|Hiermee wordt de grootte opgegeven van het interval dat is toegestaan als afrondingsverschil wanneer u posten in verschillende valuta's met elkaar vereffent.|
|**Debetrekening afronding conversievaluta**|Hiermee worden conversiegegevens opgegeven die ook een debetrekening moeten bevatten als u correctieregels voor afrondingsverschillen in de dagboeken wilt invoegen met de actie **Afr.-bedragregels van conv.-LV invoegen**.|
|**Creditrekening afronding conversievaluta**|Hiermee worden conversiegegevens opgegeven die ook een creditrekening moeten bevatten als u correctieregels voor afrondingsverschillen in de dagboeken wilt invoegen met de actie **Afr.-bedragregels van conv.-LV invoegen**.|
|**Geherwaardeerd op**|De datum van de laatste valuta-aanpassing.|
|**Laatst gewijzigd**|De datum van de wijziging in de instelling van de valuta.|
|**Betalingstolerantie %**|Het maximale betalingstolerantie % ingesteld voor deze valuta. Zie voor meer informatie [Betalingstolerantie en betalingskortingstolerantie](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Max. betalingstolerantiebedrag**|Het maximale betalingstolerantiebedrag ingesteld voor deze valuta. Zie voor meer informatie [Betalingstolerantie en betalingskortingstolerantie](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Valutafactor**|Hiermee wordt de relatie opgegeven tussen de valuta en de lokale valuta met de huidige valutakoers.|
|**Gereal. grootboekwinstrek.**|Geeft de grootboekrekening op die wordt gebruikt om wisselkoerswinsten te boeken bij valutaherwaarderingen tussen de lokale valuta (LV) en de rapportagevaluta. De wisselkoerswinsten worden berekend wanneer de batchverwerking Wisselkoersen aanpassen wordt uitgevoerd om grootboekrekeningen aan te passen. Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|
|**Gereal. grootboekverliesrek.**|Geeft de grootboekrekening op die wordt gebruikt om wisselkoersverliezen te boeken bij valutaherwaarderingen tussen de lokale valuta (LV) en de rapportagevaluta. De wisselkoerswinsten worden berekend wanneer de batchverwerking Wisselkoersen aanpassen wordt uitgevoerd om grootboekrekeningen aan te passen. Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|
|**Verschillenrekening (Winst)**|Specificeert de grootboekrekening die wordt gebruikt om resterende winstbedragen (afrondingsverschillen) te boeken wanneer een extra rapportagevaluta wordt gebruikt in het grootboekvereffeningsgebied. Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|
|**Verschillenrekening (Verlies)**|Specificeert de grootboekrekening die wordt gebruikt om resterende verliesbedragen (afrondingsverschillen) te boeken wanneer een extra rapportagevaluta wordt gebruikt in het grootboekvereffeningsgebied. Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|
|**Max. toegestaan btw-verschil**|Het maximaal toegestane bedrag voor btw-verschillen in deze valuta. Zie voor meer informatie [Btw-bedragen handmatig corrigeren in verkoop- en inkoopdocumenten](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|
|**Btw-afrondingssoort**|Specificeert de afrondingsmethode voor het handmatig corrigeren van btw-bedragen in verkoop- en inkoopdocumenten. Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|

### <a name="available-currency-functions" />Beschikbare valutafuncties

De volgende tabel geeft een overzicht van de belangrijkste acties op de pagina **Valuta's**.  

|Menu|Actie|Omschrijving|
|-------------|--------------|------------------------------|
|**Verwerken**|**Rekeningen voorstellen**|Rekeningen gebruiken van de andere valuta's. De meest gebruikte rekeningen worden ingevoegd.|
||**Betalingstolerantie wijzigen**|De maximale betalingstolerantie en/of het betalingstolerantiepercentage wijzigen en filteren op valuta. Zie voor meer informatie [Betalingstolerantie en betalingskortingstolerantie](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Wisselkoersen**|Bijgewerkte wisselkoersen weergeven voor de valuta die u gebruikt.|
||**Wisselkoersen herwaarderen**|Grootboek-, klanten-, leveranciers- en bankposten herwaarderen om een beter bijgewerkt saldo te krijgen als de wisselkoers is gewijzigd na het boeken van de posten.|
||**Register voor wisselkoersherwaardering**|Bekijk de resultaten van het uitvoeren van de batchverwerking **Wisselkoersen herwaarderen**. Er wordt een regel gemaakt voor elke valuta of combinatie van valuta en boekingsgroep die in de herwaardering is opgenomen.|
|**Wisselkoersservice**|**Wisselkoersservices**|De instelling weergeven of bewerken van de services die zijn ingesteld om bijgewerkte valutawisselkoersen op te halen wanneer u de actie **Wisselkoersen bijwerken** kiest.|
||**Wisselkoersen bijwerken**|De laatste valutawisselkoersen ophalen van een serviceprovider.|
|**Rapporten**|**Saldo in vreemde valuta**|De saldi voor de klanten en leveranciers weergeven in vreemde valuta's en de lokale valuta (LV). In het rapport worden twee saldi in lokale valuta weergegeven. Een daarvan is het saldo in vreemde valuta omgerekend naar lokale valuta met behulp van de wisselkoers op het moment van de transactie. De ander is het saldo in vreemde valuta omgerekend naar lokale valuta met behulp van de wisselkoers op het moment van de werkdatum.|

## <a name="lcy-and-other-currencies" />LV en andere valuta's

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies" />Valuta's afronden

Als u valuta's wilt beheren waarvoor geen decimalen worden gebruikt en onnodige decimalen in vreemde valuta's wilt voorkomen, kunt u twee verschillende afrondingsfuncties gebruiken:

- Prijsafronding  

- Bedragafronding  

Deze functies kunt u afzonderlijk of in combinatie gebruiken. Bovendien werken de functies in combinatie met factuurafronding.

In tegenstelling tot de functies voor factuurafronding zijn de functies voor bedrag- en prijsafronding alleen van invloed op bedragen in een vreemde valuta en niet op de bijbehorende bedragen in de LV. Deze twee functies leiden niet tot boekingen naar grootboekrekeningen. Dientengevolge hoeft u geen grootboekrekening op te geven voor boekingsgroepen of anderszins.

### <a name="unit-amount-rounding" />Prijsafronding

Met de functie voor prijsafronding wordt geregeld hoe verkoopprijzen voor artikelen en resources in vreemde valuta's worden afgerond op verkoop- en inkoopregels. U moet de regels voor elke valuta apart opgeven in het veld **Prijsafrondingsprecisie** in de lijst **Valuta's**.

De functie voor prijsafronding wordt telkens automatisch gebruikt wanneer u een artikel- of resourcenummer invoert in een verkoopregel. Als de factuur voor een klant met een valutacode is bestemd, wordt de artikel- of resourceprijs omgerekend naar de valuta van de klant. De prijs wordt afgerond volgens de prijsafrondingsprecisie voor de valuta.

### <a name="amount-rounding" />Bedragafronding

Met de functie voor bedragafronding wordt geregeld hoe bedragen in vreemde valuta's worden afgerond in dagboek-, verkoop- en inkoopregels. U moet de regels voor elke valuta apart opgeven in het veld **Bedragafrondingsprecisie** in de lijst **Valuta's**.

Bedragen in vreemde valuta's worden afgerond wanneer u dagboek-, verkoop- en inkoopregels invult en boekt.

## <a name="exchange-rates" />Wisselkoersen

U kunt wisselkoersen voor elke vreemde valuta registreren en opgeven vanaf welke datums de wisselkoersen geldig zijn. U kunt bijvoorbeeld dagelijkse, maandelijkse of driemaandelijkse wisselkoersen voor elke vreemde valuta invoeren.

U kunt historische wisselkoersen ter referentie behouden op de pagina **Valutawisselkoersen**. Als u wisselkoersen moet bijwerken, kunt u de knop **Wisselkoersen bijwerken** gebruiken om de laatste wisselkoersen op te halen bij externe serviceprovider.

## <a name="general-ledger-accounts" />Grootboekrekeningen

U kunt geen valutacodes aan grootboekrekeningen koppelen omdat bedragen in grootboekrekeningen in de LV zijn. Als u een banklening in USD hebt en bedragen op een bankrekening stort in SEK, kunt u deze rekeningen bijhouden door bankrekeningen in USD en SEK in te stellen. Met boekingsgroepen kunt u de rekeningen aan de relevante grootboekrekeningen koppelen. In het grootboek wordt de waarde van de bedragen weergegeven in de LV.

U kunt een valutacode voor een dagboekregel invoeren en de regel naar een grootboekrekening boeken. De relevante wisselkoers wordt gebruikt om het bedrag naar de LV om te rekenen voordat dit naar de grootboekrekening wordt geboekt.  

## <a name="example-of-a-receivable-currency-transaction" />Voorbeeld van een te ontvangen valutatransactie

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/modules/currencies-exchange-rates-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Valutawisselkoersen bijwerken](finance-how-update-currencies.md)  
[Een extra rapportagevaluta instellen.](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
