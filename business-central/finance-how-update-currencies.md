---
title: Valutawisselkoersen bijwerken
description: Houd bedragen in verschillende valuta's bij met valutacodes en laat Business Central u helpen wisselkoersen van geboekte posten aan te passen met behulp van een externe service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates, FX rates
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: 44dd13f986098283d29e58d3e8c4ce0218b4a083
ms.sourcegitcommit: 41876b559872fe7adbfa5b59a6e1a71dc907fb15
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921070"
---
# <a name="update-currency-exchange-rates"></a>Valutawisselkoersen bijwerken

Aangezien bedrijven steeds vaker in andere landen/regio's opereren, is het belangrijk dat zij kunnen handelen en de financiële gegevens kunnen controleren en rapporteren in meer dan één valuta. De lokale valuta (LV) wordt gedefinieerd op de pagina **Grootboek instellen**, zoals beschreven in het artikel [Financiën instellen](finance-setup-finance.md). Zodra de lokale valuta (LV) is gedefinieerd, wordt deze weergegeven als een blanco valuta, dus wanneer het veld **Valuta** leeg is, betekent dit dat de valuta LV is.  

Vervolgens moet u valutacodes instellen voor elke valuta die u gebruikt als u koopt of verkoopt in andere valuta's dan uw lokale valuta (LV). Ook kunnen bankrekeningen worden gemaakt met valuta. Het is mogelijk om grootboektransacties in verschillende valuta's vast te leggen, maar de grootboektransactie wordt altijd geboekt in de lokale valuta (LV).

> [!Important]
> Maak de lokale valutacode niet zowel op de pagina **Grootboek instellen** als op de pagina **Valuta's**. Hierdoor ontstaat er verwarring tussen de blanco valuta en de LV-code in de valutatabel en kunnen per ongeluk bankrekeningen, klanten of leveranciers worden gemaakt, sommige met de blanco valuta en sommige met de LV-code.

Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken, maar u kunt het ook instellen om een andere valuta te gebruiken, waaraan een valutawisselkoers is toegewezen. Door een tweede valuta in te stellen als een zogenaamde aanvullende rapportagevaluta, legt [!INCLUDE[prod_short](includes/prod_short.md)] bedragen automatisch vast in zowel de LV als deze aanvullende rapportagevaluta voor elke grootboekpost en andere posten, zoals btw-posten. Zie voor meer informatie [Een extra rapportagevaluta instellen](finance-how-setup-additional-currencies.md). De aanvullende rapportagevaluta wordt meestal gebruikt om financiële rapportage te vergemakkelijken voor eigenaren die woonachtig zijn in landen/regio's die andere valuta's gebruiken dan de lokale valuta (LV).  

> [!IMPORTANT]
> Als u een extra rapportagevaluta wilt gebruiken voor financiële rapportage, zorg er dan voor dat u de beperkingen begrijpt. Zie voor meer informatie [Een extra rapportagevaluta instellen](finance-how-setup-additional-currencies.md).

## <a name="currencies"></a>Valuta's

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] wordt dit valuta genoemd als u op zoek bent naar realtime informatie over wisselkoersen of historische koersen. Zie naast dit artikel ook [Een extra rapportagevaluta instellen](finance-how-setup-additional-currencies.md).

U geeft de valutacodes op de pagina **Valuta's** op, inclusief extra informatie en instellingen die nodig zijn voor elke valutacode.

> [!TIP]
> Maak de valuta's met de internationale ISO-code als code om het werken met de valuta in de toekomst te vereenvoudigen.

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
|**Max. toegestaan btw-verschil**|Het maximaal toegestane bedrag voor btw-verschillen in deze valuta. Zie voor meer informatie [Btw-bedragen handmatig corrigeren in verkoop- en inkoopdocumenten](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|
|**Btw-afrondingssoort**|Specificeert de afrondingsmethode voor het handmatig corrigeren van btw-bedragen in verkoop- en inkoopdocumenten. Dit veld is mogelijk niet standaard zichtbaar. Het kan worden opgehaald door de pagina te personaliseren.|

### <a name="example-of-a-receivable-currency-transaction"></a>Voorbeeld van een te ontvangen valutatransactie

Wanneer u een factuur van een bedrijf in een vreemde valuta ontvangt, is het vrij eenvoudig om de LV-waarde van de factuur te berekenen op basis van de huidige valutakoers. De factuur wordt echter vaak geleverd met betalingsvoorwaarden, zodat u de betaling kunt uitstellen naar een latere datum, wat een mogelijk andere valutakoers impliceert. Dit probleem in combinatie met het feit dat de bankvaluta's altijd verschillen van de officiële valutakoersen, maakt het onmogelijk om het exacte bedrag in lokale valuta (LV) te voorspellen dat nodig is om de factuur te dekken. Als de vervaldatum van de factuur zich uitstrekt tot de volgende maand, moet u mogelijk ook het bedrag in lokale valuta (LV) aan het einde van de maand herwaarderen. De valutacorrectie is nodig omdat de nieuwe LV-waarde die nodig is om het factuurbedrag te dekken mogelijk anders is en de bedrijfsschuld aan de leverancier mogelijk is gewijzigd. Het nieuwe LV-bedrag kan hoger of lager zijn dan het vorige bedrag en zal daarom een winst of een verlies vertegenwoordigen. Aangezien de factuur echter nog niet is betaald, wordt de winst of het verlies beschouwd als *niet gerealiseerd*. Later wordt de factuur betaald en komt de bank met de werkelijke valutakoers voor de betaling. Nu pas wordt de *gerealiseerde* winst of verlies berekend. Deze niet-gerealiseerde winst of verlies wordt vervolgens teruggeboekt en in plaats daarvan wordt de gerealiseerde winst of het gerealiseerde verlies geboekt.

In het volgende voorbeeld wordt op 1 januari een factuur ontvangen met het valutabedrag 1000. Op dat moment is de wisselkoers 1,123.

|Datum|Actie|Valutabedrag|Documentkoers|LV-bedrag in document|Vereffeningskoers|Ongerealiseerd winstbedrag|Betalingskoers|Gerealiseerd verliesbedrag|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Factuur**|1000|1,123|1123|||||
|1/31|**Herwaardering**|1000||1125|1,125|2|||
|2/15|**Herwaarderingsterugboeking bij betaling**|1000||||-2|||
|2/15|**Betaling**|1000||1120|||1,120|-3|

Aan het einde van de maand wordt een valuta-aanpassing uitgevoerd waarbij de aanpassingsvalutakoers is ingesteld op 1,125, wat een niet-gerealiseerde winst van 2 veroorzaakt.

Op het moment van betaling toont de werkelijke valutakoers die is geregistreerd voor de banktransactie, een valutakoers van 1,120.

Hier is sprake van een niet-gerealiseerde transactie en het wordt daarom samen met de betaling teruggeboekt.

Ten slotte wordt de betaling geregistreerd en wordt het werkelijke verlies geboekt op de rekening voor gerealiseerde verliezen.

## <a name="available-currency-functions"></a>Beschikbare valutafuncties

De volgende tabel geeft een overzicht van de belangrijkste acties op de pagina **Valuta's**. Sommige van de acties worden in de volgende secties uitgelegd.  

|Menu|Actie|Omschrijving|
|-------------|--------------|------------------------------|
|**Verwerken**|**Rekeningen voorstellen**|Rekeningen gebruiken van de andere valuta's. De meest gebruikte rekeningen worden ingevoegd.|
||Betalingstolerantie wijzigen|De maximale betalingstolerantie en/of het betalingstolerantiepercentage wijzigen en filteren op valuta. Zie voor meer informatie [Betalingstolerantie en betalingskortingstolerantie](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Wisselkoersen**|Bijgewerkte wisselkoersen weergeven voor de valuta die u gebruikt.|
||**Wisselkoersen herwaarderen**|Grootboek-, klanten-, leveranciers- en bankposten herwaarderen om een beter bijgewerkt saldo te krijgen als de wisselkoers is gewijzigd na het boeken van de posten.|
||**Register van wisselkoersaanpassing**|Bekijk de resultaten van het uitvoeren van de batchverwerking **Wisselkoersen herwaarderen**. Er wordt een regel gemaakt voor elke valuta of combinatie van valuta en boekingsgroep die in de herwaardering is opgenomen.|
|**Wisselkoersservice**|**Wisselkoersservices**|De instelling weergeven of bewerken van de services die zijn ingesteld om bijgewerkte valutawisselkoersen op te halen wanneer u de actie **Wisselkoersen bijwerken** kiest.|
||**Wisselkoersen bijwerken**|De laatste valutawisselkoersen ophalen van een serviceprovider.|
|**Rapporten**|**Saldo in vreemde valuta**|De saldi voor de klanten en leveranciers weergeven in vreemde valuta's en de lokale valuta (LV). In het rapport worden twee saldi in lokale valuta weergegeven. Een daarvan is het saldo in vreemde valuta omgerekend naar lokale valuta met behulp van de wisselkoers op het moment van de transactie. De ander is het saldo in vreemde valuta omgerekend naar lokale valuta met behulp van de wisselkoers op het moment van de werkdatum.|

## <a name="exchange-rates"></a>Wisselkoersen

De wisselkoersen zijn het hulpmiddel om de lokale valutawaarde (LV) van elke valutatransactie te berekenen. De pagina **Wisselkoersen** bevat de volgende velden:

|Veld|Omschrijving|  
|---------------------------------|---------------------------------------|  
|**Begindatum**|De datum waarop de valutakoers is geëffectueerd|  
|**Valutacode**|De valutacode met betrekking tot deze wisselkoers|  
|**Relationele valutacode**|Als deze valuta deel uitmaakt van een driehoeksvalutaberekening, dan kan de bijbehorende valutacode hier worden ingesteld|  
|**Wisselkoersbedrag**|Het wisselkoersbedrag is de koers die moet worden gebruikt voor de valutacode die op de regel is geselecteerd. Normaal 1 of 100|  
|**Relationeel wisselkoersbedrag**|Het relationele wisselkoersbedrag is de koers die moet worden gebruikt voor de relationele valutacode|  
|**Wisselkoersbedrag (Herw.)**|Het bedrag van de herwaarderingswisselkoers is de koers die moet worden gebruikt voor de valutacode die is geselecteerd op de regel voor gebruik van de batchverwerking **Wisselkoersen aanpassen**|  
|**Gereal. wisselkoersbedr. (Herw.)**|Het relationele bedrag van de herwaarderingswisselkoers is de koers die moet worden gebruikt voor de valutacode die is geselecteerd op de regel voor gebruik van de batchverwerking **Wisselkoersen aanpassen**|  
|**Vast wisselkoersbedrag**|Hiermee wordt opgegeven of de wisselkoers van de valuta kan worden gewijzigd in facturen en op dagboekregels.|  

Over het algemeen worden de waarden van de velden **Wisselkoersbedrag** en **Relationeel wisselkoersbedrag** gebruikt als de standaardvalutakoers voor alle nieuwe debiteuren- en crediteurendocumenten die in de toekomst worden gemaakt. Het document krijgt de valutakoers toegewezen op basis van de huidige werkdatum.  

> [!Note]
> De huidige valutakoers wordt berekend met behulp van deze formule:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Het correctiewisselkoersbedrag of het relationele correctiekoersbedrag wordt gebruikt om alle openstaande banktransacties en te ontvangen of te betalen transacties bij te werken.  

> [!Note]
> De huidige valutakoers wordt berekend met behulp van deze formule:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Wisselkoersen corrigeren

Aangezien valutakoersen constant wisselen, moeten de extra valuta-equivalenten in uw systeem periodiek worden gecorrigeerd. Als deze correcties niet worden uitgevoerd, kunnen de bedragen die omgerekend zijn van vreemde (of extra) valuta's en geboekt zijn in het grootboek in LV misleidend zijn. Bovendien moeten dagelijkse posten die geboekt zijn doordat een dagwisselkoers is ingevoerd in de toepassing, worden bijgewerkt nadat de dagwisselkoersgegevens zijn ingevoerd.

De batchverwerking **Wisselkoersen herwaarderen** wordt gebruikt om de wisselkoersen van de geboekte klanten-, leveranciers- en bankrekeningposten handmatig te corrigeren. U kunt er tevens extra rapportagevalutabedragen in grootboekposten mee bijwerken.  

> [!TIP]
> U kunt een service gebruiken om de wisselkoersen in het systeem automatisch bij te werken. Zie [Een wisselkoersservice instellen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service) voor meer informatie. Hiermee past u echter de wisselkoersen van reeds geboekte transacties niet aan. Als u de wisselkoersen van geboekte posten wilt bijwerken, moet u de batchtaak **Wisselkoersen herwaarderen** gebruiken.

### <a name="effect-on-customers-and-vendors"></a>Effect op klanten en leveranciers

Voor klanten- en leveranciersrekeningen wordt de valuta tijdens de batchverwerking met de wisselkoers die geldig is op de opgegeven boekingsdatum. Met de batchverwerking worden de verschillen voor de afzonderlijke valutasaldo's berekend en worden de bedragen geboekt naar de opgegeven grootboekrekening in het veld **Ongereal. koerswinstrekening** of **Ongereal. koersverliesrekening** in de tabel **Valuta's**. Tegenposten worden automatisch geboekt naar de liquiditeitsrekening in het grootboek.

In de batchverwerking worden alle open klantenposten en leveranciersposten verwerkt. Als er sprake is van een wisselkoersverschil voor een post, wordt in de batchverwerking een nieuwe gedetailleerde klanten- of leverancierspost gemaakt. Deze post staat voor het aangepaste bedrag op de klanten- of leverancierspost.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensies in klanten- en leveranciersposten

De herwaarderingsposten krijgen de dimensies van de klanten-/leveranciersposten toegewezen en de herwaarderingen worden geboekt per combinatie van dimensiewaarden.

### <a name="effect-on-bank-accounts"></a>Effect op bankrekeningen

Voor bankrekeningen wordt de valuta tijdens de batchverwerking geherwaardeerd met de wisselkoers die geldig is op de opgegeven boekingsdatum. Tijdens de batchverwerking worden de verschillen voor elke bankrekening met een valutacode berekend en worden de bedragen geboekt naar de opgegeven grootboekrekening in het veld **Gereal. koerswinstrekening** of **Gereal. koersverliesrekening** in de tabel **Valuta's**. Tegenposten worden automatisch geboekt naar de grootboekrekeningen die in de bankboekingsgroepen zijn opgegeven. Tijdens de batchverwerking wordt één post per valuta per boekingsgroep berekend.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensies op bankrekeningposten

De herwaarderingsposten voor de grootboekrekening van de bankrekening en voor de winst-/verliesrekening krijgen de standaarddimensies van de bankrekening toegewezen.

### <a name="effect-on-gl-accounts"></a>Effect op grootboekbankrekeningen
Als u in een rapportagevaluta boekt, kunt u met de batchverwerking nieuwe posten boeken voor valutaherwaarderingen tussen de lokale valuta en de rapportagevaluta. Met de batchverwerking worden de verschillen voor elke grootboekpost berekend en wordt de grootboekpost voor elke grootboekrekening geherwaardeerd op basis van de inhoud van het veld **Wisselkoersherwaardering**.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensies op grootboekrekeningposten
De herwaarderingsposten krijgen de standaarddimensies toegewezen van de rekeningen waarop ze worden geboekt.

> [!Important]
> Voordat u de batchverwerking kunt gebruiken, moet u de herwaarderingswisselkoersen invoeren waarmee de saldo's in vreemde valuta worden geherwaardeerd. U doet dit op de pagina **Valutawisselkoersen**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Een wisselkoersservice instellen
U kunt een externe service gebruiken om valutawisselkoersen actueel te houden, zoals FloatRates. 

> [!NOTE]
> De meeste wisselkoersservices bieden gegevens die compatibel zijn met het importproces in [!INCLUDE[prod_short](includes/prod_short.md)]. Soms zijn de gegevens echter anders opgemaakt en moet u uw importproces aanpassen. U kunt hiervoor het raamwerk voor gegevensuitwisseling gebruiken door uw eigen codeunit toe te voegen. U hebt waarschijnlijk wat hulp van een ontwikkelaar nodig om dat te doen. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Valutawisselkoersservices** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul op de pagina **Valutawisselkoersservice** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Zet de schakelaar **Ingeschakeld** aan om de service in te schakelen.

> [!NOTE]
> De volgende video toont een voorbeeld van hoe u verbinding kunt maken met een valutawisselkoersservice, waarbij de Europese Centrale Bank als voorbeeld wordt gebruikt. In het segment dat beschrijft hoe u veldtoewijzingen instelt, retourneert de instelling in de kolom **Bron** voor de **Hoofdknooppunt voor valutacode** alleen de eerste gevonden valuta. De instelling moet zijn `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valutawisselkoersen bijwerken met een service
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Valuta's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Wisselkoersen bijwerken**.

De waarde in het veld **Wisselkoers** op de pagina **Valuta's** wordt bijgewerkt met de laatste wisselkoers.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook
[Een extra rapportagevaluta instellen.](finance-how-setup-additional-currencies.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
