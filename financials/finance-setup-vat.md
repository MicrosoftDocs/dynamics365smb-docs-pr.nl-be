---
title: Btw instellen | Microsoft Docs
description: Controleer of u btw voor verkopen en inkopen op de juiste wijze berekent, boekt en aangeeft.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ce397b4a492a727211b49d7db2a231bea40d8c43
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---

# <a name="setting-up-to-calculations-and-posting-methods-for-value-added-tax"></a>Berekeningen en voor boekingsmethoden voor btw instellen
Consumenten en bedrijven betalen btw wanneer deze goederen of services inkopen. Het bedrag dat aan btw moet worden betaald, is afhankelijk van een aantal factoren. In [!INCLUDE[d365fin](includes/d365fin_md.md)] stelt u btw in om de tarieven op te geven die moeten worden gebruikt om belastingbedragen te berekenen op basis van het volgende: 

* Aan wie u verkoopt  
* Van wie u koopt  
* Wat u verkoopt  
* Wat u koopt  
  
U kunt handmatig btw-berekeningen instellen, maar dit kan lastig en tijdrovend zijn. Voor het gemak bieden we een begeleide instelling met de naam **Btw-instellingen** die u tijdens de stappen begeleidt. Het is raadzaam de begeleide instelling te gebruiken om btw in te stellen.

> [!NOTE]  
>   U kunt de begeleide instelling alleen gebruiken als u een Mijn bedrijf hebt gemaakt en geen transacties hebt geboekt die inclusief btw zijn. Anders zouden er gemakkelijk per ongeluk andere btw-tarieven worden gebruikt en onnauwkeurige btw-gerelateerde rapporten worden gemaakt.  
  
Als u btw-berekeningen zelf wilt instellen of alleen meer informatie wilt over elke stap, bevat dit onderwerp omschrijvingen van elke stap. De omschrijvingen geven aan hoe u het volgende kunt doen:  
  
* Btw-bedrijfsboekingsgroepen instellen om btw-tarieven te definiëren voor de markten waarin u werkt. U wijst deze toe aan klanten en leveranciers.  
* Btw-productboekingsgroepen instellen om btw-tarieven in te stellen voor de producten en services die u koopt of verkoopt.  
  
   > [!NOTE]  
>   De concepten achter btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen zijn vergelijkbaar met algemene boekingsgroepen. Zie [Boekingsgroepinstellingen](finance-posting-groups.md) voor meer informatie.
* Btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen combineren om btw-instellingen te maken waarmee btw-bedragen op verkopen en inkopen worden berekend.  
* Btw-productboekingsgroepen toewijzen aan de grootboekrekeningen die u voor verkopen en inkopen, en artikelen en resources gebruikt.  

   > [!NOTE]  
>   Als u btw wilt instellen voor resources, moet u de gebruikerservaring **Pakket** voor uw bedrijf inschakelen. Zie [Uw Dynamics 365 for Financials-ervaring aanpassen](ui-experiences.md) voor meer informatie.
* Btw-verlegging gebruiken voor handel tussen EU-landen/-regio's  
* Btw-afronding voor documenten begrijpen  
* Clausules instellen om het gebruik van niet-standaard btw-tarieven uit te leggen
* Btw-nummers controleren

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>De begeleide instelling Btw-instelling gebruiken om btw in te stellen (aanbevolen)
Het is raadzaam de begeleide instelling Btw-instelling te gebruiken om btw in te stellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

Ga als volgt te werk om de begeleide instelling te starten:
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport") en voer **Begeleide instelling** in.  
2. Kies **Btw-instelling**.

## <a name="set-up-vat-business-posting-groups"></a>Btw-bedrijfsboekingsgroepen instellen
Met btw-bedrijfsboekingsgroepen worden de markten vertegenwoordigd waarin u zaken doet met klanten en leveranciers en wordt bepaald hoe u btw in elke markt berekent en boekt. Voorbeelden van btw-bedrijfsboekingsgroepen zijn **Binnenlands** en **Europese Unie (EU)**.  

Gebruik codes die eenvoudig te onthouden zijn en die de bedrijfsboekinggroep beschrijven, zoals **EU**, **Niet-EU** of **Binnenlands**. Deze code moet uniek zijn. U kunt zoveel codes instellen als u nodig hebt, maar u kunt dezelfde code niet meer dan één keer in een tabel gebruiken.
  
Ga als volgt te werk om een btw-bedrijfsboekingsgroep in te stellen:

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-bedrijfsboekingsgroep** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

Als u standaard btw-bedrijfsboekingsgroepen wilt instellen, koppelt u deze aan bedrijfsboekingsgroepen. [!INCLUDE[d365fin](includes/d365fin_md.md)] wijst de btw-bedrijfsboekingsgroep automatisch toe wanneer u de bedrijfsboekingsgroep toewijst aan een klant, leverancier of grootboekrekening. 

## <a name="set-up-vat-product-posting-groups"></a>Btw-productboekingsgroepen instellen
Met btw-productboekingsgroepen worden de artikelen en resources vertegenwoordigd die u koopt of verkoopt en wordt bepaald hoe btw wordt berekend en geboekt volgens het soort artikel of resource, dat wordt aangeschaft of verkocht.  
Het is aan te raden codes te gebruiken die u gemakkelijk kunt onthouden en waarmee het tarief wordt beschreven, zoals **Geen btw** of **Nul**, **Btw10** of **Gereduceerd** voor 10% btw en **Btw21** of **Standaard** voor 21%.

Ga als volgt te werk om een btw-bedrijfsboekingsgroep in te stellen:

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-productboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Btw-boekingsgroepen in btw-boekingsinstellingen combineren
In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden btw-bedragen berekend op verkopen en inkopen op basis van btw-boekingsinstellingen, die combinaties zijn van btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen. Voor elke combinatie kunt u het btw-percentage, het soort btw-berekening en grootboekrekeningen opgeven voor het boeken van btw voor verkopen, inkopen en btw-verlegging. U kunt ook opgeven of btw moet worden herberekend wanneer een betalingskorting wordt toegepast of ontvangen.  

U kunt zo veel combinaties instellen als u nodig hebt. Als u combinaties van btw-boekingsinstellingen met soortgelijke kenmerken wilt groeperen, kunt u een **Btw-identificatie** definiëren voor elke groep en de identificatie toewijzen aan de groepsleden.

Ga als volgt te werk om btw-boekingsinstellingen te combineren:

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-boekingsinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Standaard btw-boekingsgroepen toewijzen aan meerdere entiteiten
Als u dezelfde btw-boekingsgroepen op meerdere entiteiten wilt toepassen, kunt u [!INCLUDE[d365fin](includes/d365fin_md.md)] instellen om dat standaard te doen. Er zijn enkele manieren om dit te doen:

* U kunt btw-bedrijfsboekingsgroepen toewijzen aan algemene bedrijfsboekingsgroepen of klant- of leveranciersjablonen 
* U kunt btw-productboekingsgroepen in algemene productboekingsgroepen toewijzen  

De btw-bedrijfsboekingsgroep of btw-productboekingsgroep wordt toegewezen wanneer u een bedrijfs- of productboekingsgroep voor een klant, leverancier, artikel of resource kiest.

## <a name="assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Btw-boekingsgroepen aan afzonderlijke rekeningen, klanten, leveranciers, artikelen en resources toewijzen
In de volgende gedeelten wordt beschreven hoe u btw-boekingsgroepen aan afzonderlijke entiteiten kunt toewijzen.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Btw-boekingsgroepen toewijzen aan afzonderlijke grootboekrekeningen 
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
2. Open de **Grootboekrekening** voor de rekening.
3. Kies op het sneltabblad **Boeken** in het veld **Algemeen boekingssoort** **Verkoop** of **Inkoop**.  
5. Kies de btw-boekingsgroepen die u wilt gebruiken voor de verkoop- of inkooprekening.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Btw-bedrijfsboekingsgroepen toewijzen aan klanten en leveranciers  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Klant** of **Leverancier** in en kies vervolgens de gerelateerde koppeling.  
2. Vouw op de kaart **Klant** of **Leverancier** het sneltabblad **Facturering** uit.  
3. Kies de btw-bedrijfsboekingsgroep.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Btw-productboekingsgroepen toewijzen aan afzonderlijke artikelen en resources.  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikel** of **Resource** in en kies vervolgens de gerelateerde koppeling.  
2. Ga op een van de volgende manieren te werk:
* Vouw op de **Artikel**kaart het sneltabblad **Prijs en boeking** uit en kies vervolgens **Meer weergeven** om het veld **Btw-productboekingsgroep** weer te geven.  
* Vouw op de kaart **Resource** het sneltabblad **Facturering** uit.  
3. Kies de btw-productboekingsgroep.

## <a name="set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Clausules instellen om het gebruik van niet-standaard btw-tarieven uit te leggen
U stelt een btw-clausule in om informatie te geven over het soort btw dat wordt toegepast. De informatie kan nodig zijn voor overheidsregelgeving. Nadat u een btw-clausule hebt ingesteld en deze hebt gekoppeld aan een btw-boekingsinstelling, wordt de btw-clausule weergegeven op afgedrukte verkoopdocumenten waarin de btw-boekingsinstellingengroep wordt gebruikt. 

Indien nodig kunt u ook opgeven hoe u btw-clausules naar andere talen vertaalt. Vervolgens wordt wanneer u een verkoopdocument maakt dat een btw-identificatie bevat, de vertaalde btw-clausule in het afgedrukte document opgenomen. Met de taalcode die op de klantenkaart is opgegeven, wordt de taal bepaald.
  
### <a name="to-set-up-vat-clauses"></a>Btw-clausules instellen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-clausules** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe regel op de pagina **Btw-clausules**.  
3. Voer in het veld **Code** een ID voor de clausule in. U gebruikt deze code om de clausule toe te wijzen aan btw-boekingsgroepen.  
4. Voer in het veld **Omschrijving** de tekst in die u wilt weergeven op documenten die btw kunnen bevatten. Geef indien nodig in het veld **Omschrijving 2** eventuele aanvullende tekst op. De tekst wordt op nieuwe regels weergegeven.  
5. Optioneel: als u de btw-clausule direct aan btw-boekingsinstellingen wilt toewijzen, kiest u **Instellingen** en vervolgens de clausule. Als u wilt wachten, kunt u de clausule later op de pagina Btw-boekingsinstellingen toewijzen.  
6. Optioneel: als u wilt opgeven hoe de btw-clausule moet worden vertaald, kiest u de actie **Vertalingen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Een btw-clausule aan een btw-boekingsgroepinstelling toewijzen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-boekingsinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in de kolom **Btw-clausule** de clausule die u wilt gebruiken voor elke btw-boekingsinstelling waarop deze van toepassing is.  

### <a name="to-specify-translations-for-vat-clauses"></a>Vertalingen opgeven voor btw-clausules
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-clausules** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Vertalingen**.  
3. Kies in het veld **Taalcode** de taal waarin u vertaalt.  
4. Voer de vertalingen van de omschrijvingen in de velden **Omschrijving** en **Omschrijving 2** in. Deze tekst wordt weergegeven in de vertaalde btw-rapportdocumenten.  
  
## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Een btw-boekingsinstelling maken om import-btw te verwerken
U gebruikt de functie voor import-btw wanneer u een document moet boeken waarbij het volledige bedrag btw is. U gebruikt dit als u een factuur van de belastingdienst ontvangt voor btw op geïmporteerde goederen.  
  
Ga als volgt te werk om codes voor import-btw in te stellen:  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-productboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Stel op de pagina Btw-productboekingsgroepen een nieuwe btw-productboekingsgroep in voor import-btw.  
3. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-boekingsinstellingen** in en kies vervolgens de gerelateerde koppeling.  
4. Open de pagina Btw-boekingsinstellingen, maak een nieuwe regel of gebruik een bestaande btw-bedrijfsboekingsgroep in combinatie met de nieuwe btw-productboekingsgroep voor import-btw.  
5. Kies in het veld **Btw-berekening** **Volledig**.  
6. Voer in het veld **Inkoop-btw-rekening** de grootboekrekening in die moet worden gebruikt om import-btw te boeken. Alle andere rekeningen zijn optioneel.  
  
## <a name="verify-vat-registration-numbers"></a>Btw-nummers controleren
Het is belangrijk dat de btw-registratienummers die u voor klanten, leveranciers en contactpersonen hebt, geldig zijn. Bedrijven wijzigen bijvoorbeeld soms hun belastingschuldstatus, en in sommige landen kan de belastingdienst u vragen om rapporten te verschaffen, zoals het rapport Verkoopoverzicht EU, waarin de btw-registratienummers worden weergegeven die u gebruikt wanneer u zaken doet. 
  
De Europese commissie verschaft de VIES-service voor btw-nummervalidatie op de website. Deze service is openbaar en gratis. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan u moeite besparen. U kunt namelijk de VIES-service om btw-nummers voor klanten, leveranciers en contactpersonen te valideren en bij te houden, rechtstreeks van de klanten-, leveranciers en contactkaarten gebruiken. De service in [!INCLUDE[d365fin](includes/d365fin_md.md)] heet **Instelling van validatieservice van EU-btw-nummers**. De service is beschikbaar op de pagina **Serviceverbindingen** en u kunt deze service meteen gebruiken. De serviceverbinding is gratis en er is geen aanmelding vereist.

Wanneer u onze serviceverbinding gebruikt, registreren we een overzicht van btw-nummers en verificaties voor elke klant, leverancier of contactpersoon in het **Btw-log**, zodat u deze eenvoudig kunt bijhouden. Het logboek is specifiek voor elke klant. Het logboek is bijvoorbeeld handig om te bewijzen dat u hebt gecontroleerd dat het huidige btw-nummer juist is. Wanneer u een btw-nummer verifieert, wordt in de kolom **Aanvraag-id** in het logboek aangegeven dat u actie hebt ondernomen. 

U kunt het btw-log weergeven op de klanten-, leveranciers- of contactkaarten op het sneltabblad **Facturering** door de zoekknop in het veld **Btw-nummer** veld.  

Onze service kan u ook wat tijd besparen als u een klant of een leverancier maakt. Als u het btw-nummer van de klant weet, kunt u het invoeren in het veld **Btw-nummer** in de klanten- of leverancierskaarten. De klantnaam wordt dan voor u ingevuld door ons. Sommige landen verschaffen ook bedrijfsadressen in een gestructureerde indeling. In deze landen wordt het adres ook door ons ingevuld.  

> [!NOTE]  
> Er zijn een paar dingen waarmee u rekening moet houden met betrekking tot de VIES-service voor btw-nummervalidatie:

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
* De btw-bedrijfsboekingsgroepen toewijzen in het veld **Btw-bedrijfsboekingsgroep** op het sneltabblad **Facturering** van de klantenkaart van elke leverancier van de EU. U moet ook het btw-nummer van de klant invoeren in het veld **Btw-nummer** op het sneltabblad **Buitenlandse handel**.  

Wanneer u een verkoop aan een klant in een ander EU-land/-regio boekt, wordt het btw-bedrag berekend en wordt een btw-post gemaakt met de informatie over de btw-verlegging en het btw-basisbedrag (het bedrag dat gebruikt wordt om het btw-bedrag te berekenen). In het grootboek worden geen posten naar de btw-rekeningen geboekt.

## <a name="understanding-vat-rounding-for-documents"></a>Btw-afronding voor documenten
Bedragen in documenten die nog niet zijn geboekt, worden afgerond en weergegeven zodat ze overeenkomen met de uiteindelijke afronding van bedragen die daadwerkelijk zijn geboekt. Btw wordt berekend voor een volledig document, wat betekent dat de btw die in het document is berekend, is gebaseerd op de som van alle regels met dezelfde btw-identificatie in het document.

## <a name="see-also"></a>Zie ook  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)
