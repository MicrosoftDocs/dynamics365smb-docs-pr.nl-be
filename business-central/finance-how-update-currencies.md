---
title: Valutawisselkoersen bijwerken (bevat video)
description: 'Als u bedragen in verschillende valuta''s bijhoudt, kunt u Business Central u laten helpen de wisselkoersen aan te passen.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 09/07/2023
ms.author: bholtorf
---
# <a name="update-currency-exchange-rates"></a>Valutawisselkoersen bijwerken

U kunt verschillende valuta's definiëren in [!INCLUDE [prod_short](includes/prod_short.md)], bijvoorbeeld als u handelt in andere valuta's dan uw lokale valuta. Om wijzigingen in wisselkoersen bij te houden kunt u de koersen handmatig beheren of u kunt een wisselkoersservice instellen.

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

## <a name="adjusting-exchange-rates"></a>Wisselkoersen herwaarderen

Aangezien wisselkoersen constant wisselen, moet u overige valuta-equivalenten periodiek aanpassen. Als u dit niet doet, kunnen de bedragen die u vanuit vreemde (of andere) valuta's hebt omgezet en in de lokale valuta naar het grootboek hebt geboekt, onjuist zijn. Bovendien moet u de dagelijks geboekte boekingen bijwerken voordat u een dagelijkse wisselkoers invoert.

Gebruik de batchverwerking **Wisselkoersen herwaarderen** om de wisselkoersen van geboekte klanten-, leveranciers- en bankrekeningposten handmatig te corrigeren. Met de batchverwerking kunnen ook andere rapportagevalutabedragen in grootboekposten worden bijgewerkt.  

> [!TIP]
> U kunt een service gebruiken om de wisselkoersen in het systeem automatisch bij te werken. Zie [Een wisselkoersservice instellen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service) voor meer informatie. Hiermee past u echter de wisselkoersen van reeds geboekte transacties niet aan. Als u de wisselkoersen van geboekte posten wilt bijwerken, moet u de batchtaak **Wisselkoersen herwaarderen** gebruiken.

U kunt ook specificeren hoe de herwaardering dimensies voor boekingen van niet-gerealiseerde winsten en verliezen verwerkt door een van de volgende opties te kiezen in het veld **Dimensieboeking**:  

* **Dimensies van bronpost**: dimensiewaarden overdragen voor grootboekposten voor niet-gerealiseerde winsten en verliezen vanuit de post die u herwaardeert.  
* **Geen dimensies**: dimensiewaarden voor niet-gerealiseerde winsten en verliezen niet overdragen naar grootboekposten. [!INCLUDE [prod_short](includes/prod_short.md)] zal nog steeds de standaarddimensie-instellingen gebruiken, bijvoorbeeld **Verplicht**, **Zelfde** of **Geen**. Als de brontransactieposten dimensiewaarden hebben, maakt de aanpassing posten zonder dimensiewaarden.  
* **Dimensies van grootboekrekening**: dimensiewaarden van de bronpost van dimensie-instellingen van de grootboekrekening voor niet-gerealiseerd winsten en verliezen overdragen naar grootboekposten.

> [!NOTE]
> Als u de voorbeeldfunctie wilt gebruiken, moet u de functie **Functie-update: Gebruik van nieuwe uitbreidbare wisselkoerscorrectie, inclusief boekingcontrole, inschakelen** op de pagina **[Functiebeheer](https://businesscentral.dynamics.com/?page=2610)** inschakelen.

> [!IMPORTANT]
> Vanwege lokale vereisten in Zwitserland raden we u niet aan **Functie-update: Gebruik van nieuwe uitbreidbare wisselkoerscorrectie, inclusief boekingcontrole, inschakelen** in te schakelen in de Zwitserse landversie (CH).

## <a name="preview-the-effect-of-an-adjustment"></a>Bekijk het effect van een aanpassing

U kunt een voorbeeld bekijken van het effect dat een wisselkoersaanpassing heeft op het boeken voordat u daadwerkelijk boekt door de actie **Voorbeeld van boeking weergeven** te kiezen op de rapportlaanvraagpagina **Wisselkoersherwaardering** (rapport 596). Op de aanvraagpagina kunt u opgeven wat u in de preview wilt opnemen:

* Een gedetailleerde boeking naar het grootboek krijgen per post
* Ontvang een samengevatte boeking per valuta. Kies gewoon het veld **Herwaarderen per post** in het rapport **Wisselkoersherwaardering**.

### <a name="effect-on-customers-and-vendors"></a>Effect op klanten en leveranciers

Voor klanten- en leveranciersrekeningen gebruikt de batchverwerking de wisselkoers die geldig was op de boekingsdatum die voor de batchverwerking is opgegeven, om de valuta te herwaarderen. Met de batchverwerking worden de verschillen voor de afzonderlijke valutasaldo's berekend en worden de bedragen geboekt naar de opgegeven grootboekrekening in het veld **Ongereal. koerswinstrekening** of **Ongereal. koersverliesrekening** in de tabel **Valuta's**. Tegenposten worden automatisch geboekt naar de liquiditeitsrekening in het grootboek.

In de batchverwerking worden alle open klantenposten en leveranciersposten verwerkt. Als er een wisselkoersverschil is voor een post, maakt de batchverwerking een nieuwe gedetailleerde klanten- of leverancierspost. De nieuwe post weerspiegelt het aangepaste bedrag op de klanten- of leverancierspost.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensies in klanten- en leveranciersposten

[!INCLUDE [prod_short](includes/prod_short.md)] wijst de dimensies van de klanten- of leveranciersposten toe aan de herwaarderingsposten en boekt herwaarderingen voor elke combinatie van dimensiewaarden.

### <a name="effect-on-bank-accounts"></a>Effect op bankrekeningen

Voor bankrekeningen wordt de valuta tijdens de batchverwerking geherwaardeerd met de wisselkoers die geldig is op de opgegeven boekingsdatum. Tijdens de batchverwerking worden de verschillen voor elke bankrekening met een valutacode berekend en worden de bedragen geboekt naar de opgegeven grootboekrekening in het veld **Gereal. koerswinstrekening** of **Gereal. koersverliesrekening** in de tabel **Valuta's**. Tegenposten worden automatisch geboekt naar de grootboekrekeningen die in de bankboekingsgroepen zijn opgegeven. Tijdens de batchverwerking wordt één post per valuta per boekingsgroep berekend.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensies op bankrekeningposten

De herwaarderingsposten voor de grootboekrekening van de bankrekening en voor de winst-/verliesrekening krijgen de standaarddimensies van de bankrekening toegewezen.

### <a name="effect-on-gl-accounts"></a>Effect op grootboekrekeningen

Als u in een andere rapportagevaluta boekt, kan de batchverwerking nieuwe grootboekposten boeken voor valutaherwaarderingen tussen de lokale valuta en de overige rapportagevaluta. Met de batchverwerking worden de verschillen voor elke grootboekpost berekend en wordt de grootboekpost voor elke grootboekrekening geherwaardeerd op basis van de inhoud van het veld **Wisselkoersherwaardering**.

#### <a name="dimensions-on-gl-account-entries"></a>Dimensies op grootboekrekeningposten

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

## <a name="see-also"></a>Zie ook

[Valuta's in Business Central](finance-currencies.md)  
[Valuta's instellen](finance-set-up-currencies.md)  
[Een extra rapportagevaluta instellen](finance-how-setup-additional-currencies.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
