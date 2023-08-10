---
title: Valutawisselkoersen bijwerken (bevat video)
description: 'Als u bedragen in verschillende valuta''s bijhoudt, kunt u Business Central u laten helpen bij het aanpassen van wisselkoersen van geboekte posten via een externe service.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates"></a>Valutawisselkoersen bijwerken

U kunt verschillende valuta's definiëren in [!INCLUDE [prod_short](includes/prod_short.md)], bijvoorbeeld als u handelt in andere valuta's dan uw lokale valuta. Om u te helpen wijzigingen in de wisselkoersen bij te houden, kunt u de valuta's handmatig beheren of u kunt een wisselkoersservice instellen.

## <a name="currencies"></a>Valuta's

> [!TIP]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] wordt dit valuta genoemd als u op zoek bent naar realtime informatie over wisselkoersen of historische koersen. Zie naast dit artikel ook [Een extra rapportagevaluta instellen](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

U geeft de valutacodes in de lijst **Valuta's** op, inclusief extra informatie en instellingen die nodig zijn voor elke valutacode. Zie [Valuta's](finance-set-up-currencies.md#curr) voor meer informatie

### <a name="example-of-a-receivable-currency-transaction"></a>Voorbeeld van een te ontvangen valutatransactie

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

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

U kunt een voorbeeld bekijken van het effect dat een aanpassing heeft op het boeken voordat u daadwerkelijk boekt door **Voorbeeld** te kiezen op de pagina **Wisselkoersen aanpassen**. Daarnaast kunt u selecteren of de grootboekboeking gedetailleerd (per boeking) of samengevat (per valuta) wordt door **Belasting in een post** te kiezen. U kunt ook specificeren hoe dimensies voor boekingen van niet-gerealiseerde winsten en verliezen moeten worden verwerkt door een van de volgende opties te kiezen in het veld **Dimensiewaarden overdragen**:  

- **Bronpost**: bij grootboekposten voor niet-gerealiseerde winsten en verliezen worden dimensiewaarden overgenomen van de aangepaste post.
- **Op grootboekrekening**: in grootboekposten voor niet-gerealiseerde winsten en verliezen worden dimensiewaarden overgedragen van de bronpost van de dimensie-instellingen van de grootboekrekening voor niet-gerealiseerde winsten en verliezen.
- **Geen overdracht**: grootboekposten voor niet-gerealiseerde winsten en verliezen hebben geen dimensiewaarden.

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

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Valuta's in Business Central](finance-currencies.md)  
[Valuta's instellen](finance-set-up-currencies.md)  
[Een extra rapportagevaluta instellen.](finance-how-setup-additional-currencies.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
