---
title: Btw instellen | Microsoft Docs
description: Controleer of u btw voor verkopen en inkopen op de juiste wijze berekent, boekt en aangeeft.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 46fbc3e9c2553a7c45fe571a74126c534d442b7c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301648"
---
# <a name="setting-up-calculations-and-posting-methods-for-value-added-tax"></a>Berekeningen en boekingsmethoden voor btw instellen
Consumenten en bedrijven betalen btw wanneer deze goederen of services inkopen. Het bedrag dat aan btw moet worden betaald, is afhankelijk van een aantal factoren. In [!INCLUDE[d365fin](includes/d365fin_md.md)] stelt u btw in om de tarieven op te geven die moeten worden gebruikt om belastingbedragen te berekenen op basis van het volgende:

* Aan wie u verkoopt  
* Van wie u koopt  
* Wat u verkoopt  
* Wat u koopt  

U kunt handmatig btw-berekeningen instellen, maar dit kan lastig en tijdrovend zijn. Voor het gemak bieden we een begeleide instelling met de naam **Btw-instellingen** die u tijdens de stappen begeleidt. Het is raadzaam de begeleide instelling te gebruiken om btw in te stellen.

> [!NOTE]  
>   U kunt de begeleide instelling alleen gebruiken als u een Mijn bedrijf hebt gemaakt en geen transacties hebt geboekt die inclusief btw zijn. Anders zouden er gemakkelijk per ongeluk andere btw-tarieven worden gebruikt en onnauwkeurige btw-gerelateerde rapporten worden gemaakt.  

Als u btw-berekeningen zelf wilt instellen of alleen meer informatie wilt over elke stap, bevat dit onderwerp omschrijvingen van elke stap.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>De begeleide instelling Btw-instelling gebruiken om btw in te stellen (aanbevolen)
Het is raadzaam de begeleide instelling Btw-instelling te gebruiken om btw in te stellen in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ga als volgt te werk om de begeleide instelling te starten:
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Begeleide instelling** in en kies vervolgens de gerelateerde koppeling.  
2. Kies **Btw instellen**.

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>BTW-nummers instellen voor uw land of regio
Als u ervoor wilt zorgen dat gebruikers geldige btw-nummers invoeren, kunt u notaties definiëren voor de btw-nummers die worden gebruikt in de landen of regio's waar u zaken doet. [!INCLUDE[d365fin](includes/d365fin_md.md)] geeft een foutbericht weer wanneer iemand een fout maakt of een notatie gebruikt die onjuist is voor het land of de regio.

Als u btw-nummers wilt instellen, gaat u als volgt te werk:
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Landen/regio's** in en kies vervolgens de gerelateerde koppeling.
2. Kies het land of de regio, en kies de actie **Btw-nummernotaties**.
3. Definieer in het veld **Notaties** de notatie door een of meer van de volgende tekens in te voeren:  

* **#** Vereist een getal van één cijfer.  
* **@** Vereist een letter. De tekst is niet hoofdlettergevoelig.  
* **?** Staat elk teken toe.  

    > [!Tip]
    > U kunt andere tekens gebruiken zolang deze aanwezig zijn in de notatie van het land of de regio. Als u bijvoorbeeld een punt of een streepje wilt opnemen in een reeks cijfers, kunt u de notatie definiëren als ##.####.### of @@-###-###.  

## <a name="to-set-up-vat-business-posting-groups"></a>Btw-bedrijfsboekingsgroepen instellen
Met btw-bedrijfsboekingsgroepen worden de markten vertegenwoordigd waarin u zaken doet met klanten en leveranciers en wordt bepaald hoe u btw in elke markt berekent en boekt. Voorbeelden van btw-bedrijfsboekingsgroepen zijn **Binnenlands** en **Europese Unie (EU)**.  

Gebruik codes die eenvoudig te onthouden zijn en die de bedrijfsboekinggroep beschrijven, zoals **EU**, **Niet-EU** of **Binnenlands**. Deze code moet uniek zijn. U kunt zoveel codes instellen als u nodig hebt, maar u kunt dezelfde code niet meer dan één keer in een tabel gebruiken.

Ga als volgt te werk om een btw-bedrijfsboekingsgroep in te stellen:

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-bedrijfsboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

Als u standaard btw-bedrijfsboekingsgroepen wilt instellen, koppelt u deze aan bedrijfsboekingsgroepen. [!INCLUDE[d365fin](includes/d365fin_md.md)] wijst de btw-bedrijfsboekingsgroep automatisch toe wanneer u de bedrijfsboekingsgroep toewijst aan een klant, leverancier of grootboekrekening.

## <a name="to-set-up-vat-product-posting-groups"></a>Btw-productboekingsgroepen instellen
Met btw-productboekingsgroepen worden de artikelen en resources vertegenwoordigd die u koopt of verkoopt en wordt bepaald hoe btw wordt berekend en geboekt volgens het soort artikel of resource, dat wordt aangeschaft of verkocht.  
Het is aan te raden codes te gebruiken die u gemakkelijk kunt onthouden en waarmee het tarief wordt beschreven, zoals **Geen btw** of **Nul**, **Btw10** of **Gereduceerd** voor 10% btw en **Btw21** of **Standaard** voor 21%.

Ga als volgt te werk om een btw-bedrijfsboekingsgroep in te stellen:

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-productboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden in.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>Btw-boekingsgroepen in btw-boekingsinstellingen combineren
In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden btw-bedragen berekend op verkopen en inkopen op basis van btw-boekingsinstellingen, die combinaties zijn van btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen. Voor elke combinatie kunt u het btw-percentage, het soort btw-berekening en grootboekrekeningen opgeven voor het boeken van btw voor verkopen, inkopen en btw-verlegging. U kunt ook opgeven of btw moet worden herberekend wanneer een betalingskorting wordt toegepast of ontvangen.  

U kunt zo veel combinaties instellen als u nodig hebt. Als u combinaties van btw-boekingsinstellingen met soortgelijke kenmerken wilt groeperen, kunt u een **Btw-identificatie** definiëren voor elke groep en de identificatie toewijzen aan de groepsleden.

Ga als volgt te werk om btw-boekingsinstellingen te combineren:

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-boekingsinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de velden in.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>Standaard btw-boekingsgroepen toewijzen aan meerdere entiteiten
Als u dezelfde btw-boekingsgroepen op meerdere entiteiten wilt toepassen, kunt u [!INCLUDE[d365fin](includes/d365fin_md.md)] instellen om dat standaard te doen. Er zijn enkele manieren om dit te doen:

* U kunt btw-bedrijfsboekingsgroepen toewijzen aan algemene bedrijfsboekingsgroepen of klant- of leveranciersjablonen
* U kunt btw-productboekingsgroepen in algemene productboekingsgroepen toewijzen  

De btw-bedrijfsboekingsgroep of btw-productboekingsgroep wordt toegewezen wanneer u een bedrijfs- of productboekingsgroep voor een klant, leverancier, artikel of resource kiest.

## <a name="to-assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Btw-boekingsgroepen aan afzonderlijke rekeningen, klanten, leveranciers, artikelen en resources toewijzen
In de volgende gedeelten wordt beschreven hoe u btw-boekingsgroepen aan afzonderlijke entiteiten kunt toewijzen.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Btw-boekingsgroepen toewijzen aan afzonderlijke grootboekrekeningen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
2. Open de **Grootboekrekening** voor de rekening.  
3. Kies op het sneltabblad **Boeken** in het veld **Algemeen boekingssoort** **Verkoop** of **Inkoop**.  
5. Kies de btw-boekingsgroepen die u wilt gebruiken voor de verkoop- of inkooprekening.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Btw-bedrijfsboekingsgroepen toewijzen aan klanten en leveranciers  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies vervolgens de gerelateerde koppeling.  
2. Vouw op de kaart **Klant** of **Leverancier** het sneltabblad **Facturering** uit.  
3. Kies de btw-bedrijfsboekingsgroep.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Btw-productboekingsgroepen toewijzen aan afzonderlijke artikelen en resources.  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikel** of **Resource** in en kies vervolgens de gerelateerde koppeling.  
2. Ga op een van de volgende manieren te werk:  

* Vouw op de **Artikel**kaart het sneltabblad **Prijs en boeking** uit en kies vervolgens **Meer weergeven** om het veld **Btw-productboekingsgroep** weer te geven.  
* Vouw op de kaart **Resource** het sneltabblad **Facturering** uit.  
3. Kies de btw-productboekingsgroep.  

## <a name="setting-up-vat-statement-templates-and-vat-statement-names"></a>Btw-aangiftesjablonen en btw-aangiftenamen instellen
De belastingdienst kan de vereisten om btw te boeken wijzigen en doet dat ook. **Btw-aangiftesjablonen** en **btw-aangiftenamen** kunnen u helpen voorbereiden op aankomende wijzigingen en een soepele overgang te krijgen naar de nieuwe vereisten. U kunt btw-aangiftesjablonen gebruiken om de velden te definiëren die u in uw btw-aangifte wilt opnemen en die weer de berekeningen definiëren, en u kunt een nieuwe btw-aangiftesjabloon maken wanneer de vereisten veranderen. Eén sjabloon kan bijvoorbeeld btw voor dit jaar berekenen op basis van de huidige vereisten en een andere sjabloon kan btw berekenen op basis van vereisten voor volgend jaar. Sjablonen zijn ook een manier om een historie te bewaren van btw-aangifte-indelingen, bijvoorbeeld, zodat u terug kunt kijken en kunt zien hoe u in vorige jaren btw hebt berekend.

## <a name="how-to-define-and-preview-vat-statements"></a>Btw-aangiften definiëren en er een voorbeeld van bekijken
Met btw-aangiften kunt u het btw-vereffeningsbedrag voor een bepaalde periode berekenen, bijvoorbeeld voor een kwartaal. Nadat u een btw-aangifte hebt gedefinieerd, kunt u er een voorbeeld van bekijken om te controleren of het aan uw wensen voldoet.

Als u een btw-aangifte wilt definiëren, volgt u deze stappen:

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-aangiftes** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het veld **Naam** kies vervolgens **Nieuw** op de pagina **Btw-aangiftes**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!Tip]
> U kunt de gegevens filteren die het afschrift zal bevatten, afhankelijk van uw keuze in het veld **Soort**. **Rekeningsamentelling** is handig als u de btw van een bepaalde rekening wilt.
**Btw-postentotaal** haalt btw van de rekeningen die zijn toegewezen aan de selecties in de velden **Algemeen boekingssoort**, **Btw-bedr.-boekingsgroep** en/of **Btw-prod.-boekingsgroep**. Met **Vak-/Rubrieksamentelling** kunt u een waarde of snelfiltercriterium invoeren in het veld **Vak-/Rubrieksamentelling**. Zie voor meer informatie [Gegevens zoeken, filteren en sorteren](ui-enter-criteria-filters.md). **Omschrijving** wordt vaak gebruikt om een notitie aan de aangifte toe te voegen. U kunt het bijvoorbeeld gebruiken als een kop wanneer u vak/rubrieksamentelling gebruikt.

Als u een voorbeeld van de btw-aangifte wilt weergeven, volgt u deze stappen:

1. Kies **Voorbeeld**.
2. Voer een datumfilter in om de aangifte te beperken tot een specifieke periode. Zie voor meer informatie over het aanpassen van de pagina om het datumfilter weer te geven [Gegevens zoeken, filteren en sorteren](ui-enter-criteria-filters.md).
3. U kunt verschillende opties selecteren om het soort btw-posten aan te geven dat u in de aangifte wilt opnemen.
4. Op de regels waarop het veld **Soort** de waarde **Btw-postentotaal** bevat, kunt u een lijst zien met btw-posten door het bedrag in het veld **Bedrag** te kiezen.   

## <a name="to-set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Clausules instellen om het gebruik van niet-standaard btw-tarieven uit te leggen
U stelt een btw-clausule in om informatie te geven over het soort btw dat wordt toegepast. De informatie kan nodig zijn voor overheidsregelgeving. Nadat u een btw-clausule hebt ingesteld en deze hebt gekoppeld aan een btw-boekingsinstelling, wordt de btw-clausule weergegeven op afgedrukte verkoopdocumenten waarin de btw-boekingsinstellingengroep wordt gebruikt.

Indien nodig kunt u ook opgeven hoe u btw-clausules naar andere talen vertaalt. Vervolgens wordt wanneer u een verkoopdocument maakt dat een btw-identificatie bevat, de vertaalde btw-clausule in het afgedrukte document opgenomen. Met de taalcode die op de klantenkaart is opgegeven, wordt de taal bepaald.

U kunt een btw-clausule wijzigen of verwijderen, en uw wijzigingen worden in een gegenereerde lijst weergegeven. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt echter geen historie van de wijziging bij. Op de lijst worden de omschrijvingen van btw-clausules afgedrukt en weergegeven voor alle regels in de lijst naast het btw-bedrag en het btw-basisbedrag. Als er geen btw-clausule is gedefinieerd voor de regels op het verkoopdocument, wordt het hele gedeelte weggelaten wanneer de lijst wordt afgedrukt.

### <a name="to-set-up-vat-clauses"></a>Btw-clausules instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-clausules** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe regel op de pagina **Btw-clausules**.  
3. Voer in het veld **Code** een ID voor de clausule in. U gebruikt deze code om de clausule toe te wijzen aan btw-boekingsgroepen.  
4. Voer in het veld **Omschrijving** de tekst in die u wilt weergeven op documenten die btw kunnen bevatten. Geef indien nodig in het veld **Omschrijving 2** eventuele aanvullende tekst op. De tekst wordt op nieuwe regels weergegeven.  
5. Optioneel: als u de btw-clausule direct aan btw-boekingsinstellingen wilt toewijzen, kiest u **Instellingen** en vervolgens de clausule. Als u wilt wachten, kunt u de clausule later op de pagina Btw-boekingsinstellingen toewijzen.  
6. Optioneel: als u wilt opgeven hoe de btw-clausule moet worden vertaald, kiest u de actie **Vertalingen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Een btw-clausule aan een btw-boekingsgroepinstelling toewijzen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-boekingsinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in de kolom **Btw-clausule** de clausule die u wilt gebruiken voor elke btw-boekingsinstelling waarop deze van toepassing is.  

### <a name="to-specify-translations-for-vat-clauses"></a>Vertalingen opgeven voor btw-clausules
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-clausules** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Vertalingen**.  
3. Kies in het veld **Taalcode** de taal waarin u vertaalt.  
4. Voer de vertalingen van de omschrijvingen in de velden **Omschrijving** en **Omschrijving 2** in. Deze tekst wordt weergegeven in de vertaalde btw-rapportdocumenten.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>Een btw-boekingsinstelling maken om import-btw te verwerken
U gebruikt de functie voor import-btw wanneer u een document moet boeken waarbij het volledige bedrag btw is. U gebruikt dit als u een factuur van de belastingdienst ontvangt voor btw op geïmporteerde goederen.  

Ga als volgt te werk om codes voor import-btw in te stellen:  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-productboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Stel op de pagina Btw-productboekingsgroepen een nieuwe btw-productboekingsgroep in voor import-btw.  
3. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-boekingsinstellingen** in en kies vervolgens de gerelateerde koppeling.  
4. Open de pagina Btw-boekingsinstellingen, maak een nieuwe regel of gebruik een bestaande btw-bedrijfsboekingsgroep in combinatie met de nieuwe btw-productboekingsgroep voor import-btw.  
5. Kies in het veld **Btw-berekening** **Volledig**.  
6. Voer in het veld **Inkoop-btw-rekening** de grootboekrekening in die moet worden gebruikt om import-btw te boeken. Alle andere rekeningen zijn optioneel.  

## <a name="to-verify-vat-registration-numbers"></a>Btw-nummers controleren
Het is belangrijk dat de btw-registratienummers die u voor klanten, leveranciers en contactpersonen hebt, geldig zijn. Bedrijven wijzigen bijvoorbeeld soms hun belastingschuldstatus, en in sommige landen kan de belastingdienst u vragen om rapporten te verschaffen, zoals het rapport Verkoopoverzicht EU, waarin de btw-registratienummers worden weergegeven die u gebruikt wanneer u zaken doet.

De Europese commissie verschaft de VIES-service voor btw-nummervalidatie op de website. Deze service is openbaar en gratis. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan u moeite besparen. U kunt namelijk de VIES-service om btw-nummers voor klanten, leveranciers en contactpersonen te valideren en bij te houden, rechtstreeks van de klanten-, leveranciers en contactkaarten gebruiken. De service in [!INCLUDE[d365fin](includes/d365fin_md.md)] heet **Instelling van validatieservice van EU-btw-nummers**. De service is beschikbaar op de pagina **Serviceverbindingen** en u kunt deze service meteen gebruiken. De serviceverbinding is gratis en er is geen aanmelding vereist.

> [!Note]
> Als u de validatieservice van EU-btw-nummers wilt inschakelen, moet u over beheerdertoegangsrechten beschikken.

Wanneer u onze serviceverbinding gebruikt, registreren we een overzicht van btw-nummers en verificaties voor elke klant, leverancier of contactpersoon in het **Btw-log**, zodat u deze eenvoudig kunt bijhouden. Het logboek is specifiek voor elke klant. Het logboek is bijvoorbeeld handig om te bewijzen dat u hebt gecontroleerd dat het huidige btw-nummer juist is. Wanneer u een btw-nummer verifieert, wordt in de kolom **Aanvraag-id** in het logboek aangegeven dat u actie hebt ondernomen.

U kunt het btw-log weergeven op de klanten-, leveranciers- of contactkaarten, op het sneltabblad **Facturering**, door de zoekknop te kiezen in het veld **Btw-nummer**.  

Onze service kan u ook wat tijd besparen als u een klant of een leverancier maakt. Als u het btw-nummer van de klant weet, kunt u het in het veld **Btw-nummer** op de klanten- of leverancierskaart invoeren. De klantnaam wordt dan voor u ingevuld. Sommige landen verschaffen ook bedrijfsadressen in een gestructureerde indeling. In deze landen wordt het adres ook door ons ingevuld.  

Er zijn een paar dingen waarmee u rekening moet houden met betrekking tot de VIES-service voor btw-nummervalidatie:

* De service gebruikt het http-protocol, wat betekent dat gegevens die door de server worden overgebracht, niet zijn versleuteld.  
* Deze service wordt mogelijk onderbroken. Hiervoor is Microsoft niet verantwoordelijk. De service maakt deel uit van een breed EU-netwerk van nationale btw-journalen.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Verlegging van btw gebruiken voor handel tussen EU-landen of -regio's
Sommige bedrijven moeten verlegging van btw gebruiken wanneer zaken worden gedaan met andere bedrijven. Deze regel is bijvoorbeeld van toepassing op inkopen van EU-landen/-regio's en verkopen aan EU-landen/-regio's.  

> [!NOTE]  
> Deze regel geldt wanneer u zakendoet met bedrijven die in een ander EU-land/-regio btw-plichtig zijn. Als u rechtstreeks zakendoet met consumenten in andere EU-landen/-regio's, moet u contact opnemen met de belastingdienst over de geldende btw-regels.  

> [!TIP]  
> U kunt controleren of een bedrijf btw-plichtig is in een ander EU-land door de EU-service voor btw-nummervalidatie te gebruiken. De service is gratis beschikbaar in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie het gedeelte met de naam _Btw-registratienummers controleren_ in dit onderwerp voor meer informatie.

### <a name="sales-to-eu-countries-or-regions"></a>Verkopen aan EU-landen of -regio's
Btw wordt niet berekend op verkopen aan btw-plichtige bedrijven in andere EU-landen/-regio's. U moet de waarde van deze verkopen aan EU-landen/-regio's apart op uw btw-aangifte vermelden.  

Om op de juiste wijze btw op verkopen aan EU-landen te berekenen, moet u:  

* Stel een regel in voor verkopen met dezelfde informatie voor inkopen. Als u reeds regels hebt ingesteld op de pagina Btw-boekingsinstellingen voor inkopen uit EU-landen/-regio's, kunt u de regels ook voor verkopen gebruiken.  
* De btw-bedrijfsboekingsgroepen toewijzen in het veld **Btw-bedrijfsboekingsgroep** op het sneltabblad **Facturering** van de klantenkaart van elke leverancier van de EU. U moet het u btw-nummer van de klant invoeren in het veld **Btw-nummer** op het sneltabblad **Buitenlandse handel**.  

Wanneer u een verkoop aan een klant in een ander EU-land/-regio boekt, wordt het btw-bedrag berekend en wordt een btw-post gemaakt met de informatie over de btw-verlegging en het btw-basisbedrag (het bedrag dat gebruikt wordt om het btw-bedrag te berekenen). In het grootboek worden geen posten naar de btw-rekeningen geboekt.

## <a name="understanding-vat-rounding-for-documents"></a>Btw-afronding voor documenten
Bedragen in documenten die nog niet zijn geboekt, worden afgerond en weergegeven zodat ze overeenkomen met de uiteindelijke afronding van bedragen die daadwerkelijk zijn geboekt. Btw wordt berekend voor een volledig document, wat betekent dat de btw die in het document is berekend, is gebaseerd op de som van alle regels met dezelfde btw-identificatie in het document.

## <a name="understanding-the-vat-rate-conversion-process"></a>Het proces voor het converteren van btw-tariefswijzigingen begrijpen.  
De tool voor het wijzigen van het btw-tarief voert op verschillende manieren conversies uit voor hoofdgegevens, dagboeken en orders. De geselecteerde stamgegevens en dagboeken worden bijgewerkt door de nieuwe algemene productboekingsgroep of de btw-productboekingsgroep. Als u een order volledig of gedeeltelijk hebt verzonden, blijven de verzonden artikelen onderdeel van de huidige algemene productboekingsgroep of btw-productboekingsgroep. Een nieuwe orderregel wordt gemaakt voor de niet verzonden items en bijgewerkt om overeen te komen met de huidige en de nieuwe BTW- of productboekingsgroepen. Bovendien worden gegevens over artikeltoeslagtoewijzigingen, reserveringen en artikeltracering dienovereenkomstig bijgewerkt.  

Er zijn echter een aantal dingen die niet worden geconverteerd door de tool:

* Verkoop- of inkooporders en facturen waar verzendingen zijn geboekt. Deze documenten zijn geboekt met het huidige btw-tarief.  
* Documenten met geboekte vooruitbetalingsfacturen. U hebt bijvoorbeeld vooruitbetalingen gedaan of ontvangen op facturen die nog niet zijn voltooid voordat u het wijzigingstool btw-tarief gaat gebruiken. In dit geval is er een verschil tussen de verschuldigde btw en de betaalde btw in de vooruitbetalingen wanneer de factuur is voltooid. Het wijzigingstool btw-tarief slaat deze documenten over en u moet deze handmatig bijwerken.  
* Doorverzendingen of speciale orders.  
* Verkoop- of inkooporders met magazijnintegratie als deze gedeeltelijk zijn verzonden of ontvangen.  
* Servicecontracten.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Conversies van btw-tariefswijziging voorbereiden  
Voordat u het wijzigingstool btw-tarief instelt, moet u de volgende voorbereidingen treffen.

* Als u transacties met verschillende tarieven hebt, moeten deze vervolgens worden gescheiden in verschillende groepen door voor elke tarief nieuwe grootboekrekeningen te maken of door met gegevensfilters transacties per tarief te groeperen.  
* Als u nieuwe grootboekrekeningen maakt, moet u nieuwe algemene boekingsgroepen maken.  
* Om het aantal documenten dat wordt geconverteerd zo klein mogelijk te maken, moet u zoveel mogelijk documenten boeken en niet-geboekte documenten tot een minimum beperken.  
* Back-up van gegevens maken.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Het wijzigingstool btw-tarief instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellen BTW-tariefswijziging** in en kies vervolgens de gerelateerde koppeling.  
2. Op de sneltabbladen **Hoofdgegevens**, **Dagboeken** en **Documenten** kiest u een boekingsgroepwaarde in de lijst met opties voor verplichte velden.  

### <a name="to-set-up-product-posting-group-conversion"></a>Conversie voor productboekingsgroepen instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellen BTW-tariefswijziging** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Instellen BTW-tariefswijziging** op het tabblad **Start** in de groep **Verwerken** de optie **Btw-productboekingsgroepconv.** of **Productboekingsgroepconv.**  
3. Voer in het veld **Van code** de huidige boekingsgroep in.  
4. Voer in het veld **Tot code** de nieuwe boekingsgroep in.  

### <a name="to-perform-vat-rate-change-conversion"></a>Een conversie voor een btw-tariefswijziging uitvoeren  
U gebruikt de Wijzigingstool btw-tarief om wijzigingen in het standaardtarief van btw te beheren. U kunt btw en algemene boekingsgroepconversies uitvoeren om btw-tarieven te wijzigen en nauwkeurige btw-rapportage te onderhouden. Afhankelijk van uw instellingen worden de volgende wijzigingen aangebracht:  

* Btw- en algemene boekingsgroepen worden geconverteerd.  
* Wijzigingen worden doorgevoerd in grootboekrekeningen, klanten, leveranciers, geopende documenten, dagboekregels, enzovoort.  

> [!IMPORTANT]  
>  Voordat u de conversie van de btw-tariefswijziging uitvoert, kunt u de conversie testen. Hiervoor volgt u de onderstaande stappen, maar zorg ervoor dat u de selectievakjes **Conversie uitvoeren** en **Wijzigingstool BTW-tarief voltooid** uitschakelt. Tijdens testconversie wordt het veld **Geconverteerd** in de tabel **Dagboekpost wijziging BTW-tarief** gewist en is het veld **Conversiedatum** in de tabel **Dagboekpost wijziging BTW-tarief** leeg. Kies nadat de conversie is voltooid de optie **Wijzigingslogposten btw-tarief** om de resultaten van de testconversie weer te geven. Controleer elke post voordat u de conversie uitvoert. Controleer met name transacties met een oud btw-tarief.     

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Wijziging btw-tarief** in en kies vervolgens de koppeling **Instellen BTW-tariefswijziging**.  
2. Controleer of u de conversie van de btw-productboekingsgroep of de conversie van de algemene productboekingsgroep al hebt ingesteld.  
3. Schakel het selectievakje **Conversie uitvoeren** in.  

    > [!IMPORTANT]  
    >  Schakel het selectievakje **Wijzigingstool BTW-tarief voltooid** uit. Het selectievakje wordt automatisch ingeschakeld wanneer de conversie btw-tariefswijziging is voltooid.  

4. Kies de actie **Converteren**.  
5. Kies nadat de conversie is voltooid op het tabblad **Start** in de groep **Proces** de optie **Wijzigingslogposten btw-tarief** om de resultaten van de conversie weer te geven.  

> [!IMPORTANT]  
>  Nadat de conversie is voltooid, wordt het veld **Geconverteerd** in de tabel **Dagboekpost wijziging BTW-tarief** ingeschakeld en bevat het veld **Conversiedatum** in de tabel **Dagboekpost wijziging BTW-tarief** de conversiedatum.  

## <a name="see-also"></a>Zie ook  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)  
[Procedure: Btw rapporteren aan een belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
