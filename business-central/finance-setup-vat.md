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
ms.date: 07/21/2020
ms.author: bholtorf
ms.openlocfilehash: bbaf458e39ec45dcbcb34bd50e38feb70fd8426b
ms.sourcegitcommit: bdb6d18d512aa76d8d4f477d73ccfb284b0047fc
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/21/2020
ms.locfileid: "3611679"
---
# <a name="set-up-value-added-tax"></a>Btw instellen

Consumenten en bedrijven betalen btw wanneer deze goederen of services inkopen. Het bedrag dat aan btw moet worden betaald, is afhankelijk van een aantal factoren. In [!INCLUDE[d365fin](includes/d365fin_md.md)] stelt u btw in om de tarieven op te geven die moeten worden gebruikt om belastingbedragen te berekenen op basis van het volgende:

* Aan wie u verkoopt  
* Van wie u koopt  
* Wat u verkoopt  
* Wat u koopt  

U kunt handmatig btw-berekeningen instellen, maar dit kan lastig en tijdrovend zijn. Voor het gemak bieden we een begeleide instelling met de naam **Btw-instellingen** die u tijdens de stappen begeleidt. Het is raadzaam de begeleide instelling te gebruiken om btw in te stellen.

> [!NOTE]  
> U kunt de begeleide instelling alleen gebruiken als u een Mijn bedrijf hebt gemaakt en geen transacties hebt geboekt die inclusief btw zijn. Anders zouden er gemakkelijk per ongeluk andere btw-tarieven worden gebruikt en onnauwkeurige btw-gerelateerde rapporten worden gemaakt.  

Als u btw-berekeningen zelf wilt instellen of alleen meer informatie wilt over elke stap, bevat dit onderwerp omschrijvingen van elke stap.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>De begeleide instelling Btw-instelling gebruiken om btw in te stellen (aanbevolen)

Het is raadzaam de begeleide instelling Btw-instelling te gebruiken om btw in te stellen in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ga als volgt te werk om de begeleide instelling te starten:

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Begeleide setup** in en kies de desbetreffende koppeling.  
2. Kies **Btw instellen** en voer alle stappen uit.
3. Wanneer u de begeleide instelling hebt voltooid, gaat u naar de pagina **Btw-boekingsgroepinstellingen** en controleert u of u extra velden moet invullen volgens de lokale vereisten in uw versie van [!INCLUDE [prodshort](includes/prodshort.md)]. Zie [Lokale functionaliteit in Business Central](about-localization.md) voor meer informatie  

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>BTW-nummers instellen voor uw land of regio

Als u ervoor wilt zorgen dat gebruikers geldige btw-nummers invoeren, kunt u notaties definiëren voor de btw-nummers die worden gebruikt in de landen of regio's waar u zaken doet. [!INCLUDE[d365fin](includes/d365fin_md.md)] geeft een foutbericht weer wanneer iemand een fout maakt of een notatie gebruikt die onjuist is voor het land of de regio.

Als u btw-nummers wilt instellen, gaat u als volgt te werk:

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Landen/regio's** in en kies de desbetreffende koppeling.
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

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-groep zakelijke boekingen** in en kies de desbetreffende koppeling.  
2. Vul indien nodig de velden in.

Als u standaard btw-bedrijfsboekingsgroepen wilt instellen, koppelt u deze aan bedrijfsboekingsgroepen. [!INCLUDE[d365fin](includes/d365fin_md.md)] wijst de btw-bedrijfsboekingsgroep automatisch toe wanneer u de bedrijfsboekingsgroep toewijst aan een klant, leverancier of grootboekrekening.

## <a name="to-set-up-vat-product-posting-groups"></a>Btw-productboekingsgroepen instellen
Met btw-productboekingsgroepen worden de artikelen en resources vertegenwoordigd die u koopt of verkoopt en wordt bepaald hoe btw wordt berekend en geboekt volgens het soort artikel of resource, dat wordt aangeschaft of verkocht.  
Het is aan te raden codes te gebruiken die u gemakkelijk kunt onthouden en waarmee het tarief wordt beschreven, zoals **Geen btw** of **Nul**, **Btw10** of **Gereduceerd** voor 10% btw en **Btw25** of **Standaard** voor 25%.

Ga als volgt te werk om een btw-groep voor zakelijke boekingen in te stellen:

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-groepen productboekingen** in en kies de desbetreffende koppeling.  
2. Vul de velden in.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>Btw-boekingsgroepen in btw-boekingsinstellingen combineren
In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden btw-bedragen berekend op verkopen en inkopen op basis van btw-boekingsinstellingen, die combinaties zijn van btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen. Voor elke combinatie kunt u het btw-percentage, het soort btw-berekening en grootboekrekeningen opgeven voor het boeken van btw voor verkopen, inkopen en btw-verlegging. U kunt ook opgeven of btw moet worden herberekend wanneer een betalingskorting wordt toegepast of ontvangen.  

U kunt zo veel combinaties instellen als u nodig hebt. Als u combinaties van btw-boekingsinstellingen met soortgelijke kenmerken wilt groeperen, kunt u een **Btw-identificatie** definiëren voor elke groep en de identificatie toewijzen aan de groepsleden.

Ga als volgt te werk om btw-boekingsinstellingen te combineren:

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-boekingen instellen** in en kies de desbetreffende koppeling.
2. Vul de velden in.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>Standaard btw-boekingsgroepen toewijzen aan meerdere entiteiten
Als u dezelfde btw-boekingsgroepen op meerdere entiteiten wilt toepassen, kunt u [!INCLUDE[d365fin](includes/d365fin_md.md)] instellen om dat standaard te doen. Er zijn enkele manieren om dit te doen:

* U kunt btw-bedrijfsboekingsgroepen toewijzen aan algemene bedrijfsboekingsgroepen of klant- of leveranciersjablonen
* U kunt btw-productboekingsgroepen in algemene productboekingsgroepen toewijzen  

De btw-bedrijfsboekingsgroep of btw-productboekingsgroep wordt toegewezen wanneer u een bedrijfs- of productboekingsgroep voor een klant, leverancier, artikel of resource kiest.

## <a name="assigning-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Btw-boekingsgroepen toewijzen aan accounts, klanten, leveranciers, artikelen en resources
In de volgende gedeelten wordt beschreven hoe u btw-boekingsgroepen aan afzonderlijke entiteiten kunt toewijzen.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Btw-boekingsgroepen toewijzen aan afzonderlijke grootboekrekeningen
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de desbetreffende koppeling.  
2. Open de **Grootboekrekening** voor de rekening.  
3. Kies op het sneltabblad **Boeken** in het veld **Algemeen boekingssoort** **Verkoop** of **Inkoop**.  
5. Kies de btw-boekingsgroepen die u wilt gebruiken voor de verkoop- of inkooprekening.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Btw-bedrijfsboekingsgroepen toewijzen aan klanten en leveranciers  
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies de desbetreffende koppeling.  
2. Vouw op de kaart **Klant** of **Leverancier** het sneltabblad **Facturering** uit.  
3. Kies de btw-bedrijfsboekingsgroep.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Btw-productboekingsgroepen toewijzen aan afzonderlijke artikelen en resources.  
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikel** of **Resource** in en kies de desbetreffende koppeling.  
2. Ga op een van de volgende manieren te werk:  

* Vouw op de **Artikel**kaart het sneltabblad **Prijs en boeking** uit en kies vervolgens **Meer weergeven** om het veld **Btw-productboekingsgroep** weer te geven.  
* Vouw op de kaart **Resource** het sneltabblad **Facturering** uit.  
3. Kies de btw-productboekingsgroep.  

## <a name="setting-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Clausules instellen om btw-vrijstelling of niet-standaard btw-tarieven uit te leggen
U stelt een btw-clausule in om informatie te geven over het soort btw dat wordt toegepast. De informatie kan nodig zijn voor overheidsregelgeving. Nadat u een btw-clausule hebt ingesteld en deze hebt gekoppeld aan een btw-boekingsinstelling, wordt de btw-clausule weergegeven op afgedrukte verkoopdocumenten waarin de btw-boekingsinstellingengroep wordt gebruikt.

Indien nodig kunt u ook opgeven hoe u btw-clausules naar andere talen vertaalt. Vervolgens wordt wanneer u een verkoopdocument maakt dat een btw-identificatie bevat, de vertaalde btw-clausule in het afgedrukte document opgenomen. De taalcode die op de klantkaart is opgegeven, bepaalt de gebruikte taal.

Wanneer in verschillende soorten documenten (bijvoorbeeld facturen of creditnota's) niet-standard btw-tarieven worden gebruikt, moeten bedrijven meestal een vrijstellingstekst (btw-clausule) bijvoegen waarin wordt uitgelegd waarom een verlaagd btw-tarief wordt gehanteerd of waarom het bedrijf van btw is vrijgesteld. U kunt per type document verschillende btw-clausules voor uw bedrijfsdocumenten definiëren, zoals een factuur of creditnota. U kunt dit doen op de pagina **Btw-clausules per documenttype**.

U kunt een btw-clausule wijzigen of verwijderen, en uw wijzigingen worden in een gegenereerde lijst weergegeven. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt echter geen historie van de wijziging bij. Op de lijst worden de omschrijvingen van btw-clausules afgedrukt en weergegeven voor alle regels in de lijst naast het btw-bedrag en het btw-basisbedrag. Als er geen btw-clausule is gedefinieerd voor de regels op het verkoopdocument, wordt het hele gedeelte weggelaten wanneer de lijst wordt afgedrukt.

### <a name="to-set-up-vat-clauses"></a>Btw-clausules instellen
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-clausules** in en kies de desbetreffende koppeling.  
2. Maak een nieuwe regel op de pagina **Btw-clausules**.  
3. Voer in het veld **Code** een ID voor de clausule in. U gebruikt deze code om de clausule toe te wijzen aan btw-boekingsgroepen.  
4. Voer in het veld **Omschrijving** tekst voor de btw-vrijstelling die u wilt weergeven in documenten waarop btw-bedragen kunnen worden vermeld. Geef indien nodig in het veld **Omschrijving 2** eventuele aanvullende tekst op. De tekst wordt weergegeven in nieuwe documentregels.
5. Kies de actie **Omschrijving per documenttype**.
6. Vul op de pagina **Btw-clausules per documenttype** de velden in waarmee u wilt aangeven welke btw-tekst moet worden aangegeven voor welk documenttype.  
7. Optioneel: als u de btw-clausule direct wilt toewijzen aan de instelling van btw-boekingen, kiest u **Setup** en daarna de clausule. Als u dit niet direct wilt doen, kunt u de clausule later toevoegen op de pagina **Btw-boekingen instellen**.  
8. Optioneel: als u wilt opgeven hoe de btw-clausule moet worden vertaald, kiest u de actie **Vertalingen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Een btw-clausule aan een btw-boekingsgroepinstelling toewijzen
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-boekingen instellen** in en kies de desbetreffende koppeling.  
2. Kies in de kolom **Btw-clausule** de clausule die u wilt gebruiken voor elke btw-boekingsinstelling waarop deze van toepassing is.  

### <a name="to-specify-translations-for-vat-clauses"></a>Vertalingen opgeven voor btw-clausules
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-clausules** in en kies de desbetreffende koppeling.  
2. Kies de actie **Vertalingen**.  
3. Kies in het veld **Taalcode** de taal waarin u vertaalt.  
4. Voer de vertalingen van de omschrijvingen in de velden **Omschrijving** en **Omschrijving 2** in. Deze tekst wordt weergegeven in de vertaalde btw-rapportdocumenten.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>Een btw-boekingsinstelling maken om import-btw te verwerken
U gebruikt de functie voor import-btw wanneer u een document moet boeken waarbij het volledige bedrag btw is. U gebruikt dit als u een factuur van de belastingdienst ontvangt voor btw op geïmporteerde goederen.  

Ga als volgt te werk om codes voor import-btw in te stellen:  
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-groepen productboekingen** in en kies de desbetreffende koppeling.  
2. Stel op de pagina Btw-productboekingsgroepen een nieuwe btw-productboekingsgroep in voor import-btw.  
3. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-boekingen instellen** in en kies de desbetreffende koppeling.  
4. Open de pagina Btw-boekingsinstellingen, maak een nieuwe regel of gebruik een bestaande btw-bedrijfsboekingsgroep in combinatie met de nieuwe btw-productboekingsgroep voor import-btw.  
5. Kies in het veld **Btw-berekening** **Volledig**.  
6. Voer in het veld **Inkoop-btw-rekening** de grootboekrekening in die moet worden gebruikt om import-btw te boeken. Alle andere rekeningen zijn optioneel.  


## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Verlegging van btw gebruiken voor handel tussen EU-landen of -regio's
Sommige bedrijven moeten verlegging van btw gebruiken wanneer zaken worden gedaan met andere bedrijven. Deze regel is bijvoorbeeld van toepassing op inkopen van EU-landen/-regio's en verkopen aan EU-landen/-regio's.  

> [!NOTE]  
> Deze regel geldt wanneer u zakendoet met bedrijven die in een ander EU-land/-regio btw-plichtig zijn. Als u rechtstreeks zakendoet met consumenten in andere EU-landen/-regio's, moet u contact opnemen met de belastingdienst over de geldende btw-regels.  

> [!TIP]  
> U kunt controleren of een bedrijf btw-plichtig is in een ander EU-land/regio door de EU-service voor btw-nummervalidatie te gebruiken. De service is gratis beschikbaar in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie het gedeelte met de naam _Btw-registratienummers controleren_ in dit onderwerp voor meer informatie.

### <a name="sales-to-eu-countries-or-regions"></a>Verkopen aan EU-landen of -regio's
Btw wordt niet berekend op verkopen aan btw-plichtige bedrijven in andere EU-landen/-regio's. U moet de waarde van deze verkopen aan EU-landen/-regio's apart op uw btw-aangifte vermelden.  

Om op de juiste wijze btw op verkopen aan EU-landen/regio's te berekenen, moet u:  

* Stel een regel in voor verkopen met dezelfde informatie voor inkopen. Als u reeds regels hebt ingesteld op de pagina Btw-boekingsinstellingen voor inkopen uit EU-landen/-regio's, kunt u de regels ook voor verkopen gebruiken.  
* De btw-bedrijfsboekingsgroepen toewijzen in het veld **Btw-bedrijfsboekingsgroep** op het sneltabblad **Facturering** van de klantenkaart van elke leverancier van de EU. U moet het u btw-nummer van de klant invoeren in het veld **Btw-nummer** op het sneltabblad **Buitenlandse handel**.  

Wanneer u een verkoop aan een klant in een ander EU-land/-regio boekt, wordt het btw-bedrag berekend en wordt een btw-post gemaakt met de informatie over de btw-verlegging en het btw-basisbedrag (het bedrag dat gebruikt wordt om het btw-bedrag te berekenen). In het grootboek worden geen posten naar de btw-rekeningen geboekt.

## <a name="understanding-vat-rounding-for-documents"></a>Btw-afronding voor documenten begrijpen
Bedragen in documenten die nog niet zijn geboekt, worden afgerond en weergegeven zodat ze overeenkomen met de uiteindelijke afronding van bedragen die daadwerkelijk zijn geboekt. Btw wordt berekend voor een volledig document, wat betekent dat de btw die in het document is berekend, is gebaseerd op de som van alle regels met dezelfde btw-identificatie in het document.




## <a name="see-also"></a>Zie ook
[Sjablonen voor btw-overzichten en namen voor btw-overzichten instellen](finance-how-setup-vat-statement.md)   
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)      
[Btw rapporteren aan de belastingdienst](finance-how-report-vat.md)      
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)    
[Werken met de Wijzigingstool btw-tarief](finance-how-use-vat-rate-change-tool.md)    
[Btw-nummers controleren](finance-how-validate-vat-registration-number.md)  
[Lokale functionaliteit in Business Central](about-localization.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)
