---
title: Btw-aangiften indienen bij de belastingdienst
description: 'Leren om rapporten voor te bereiden met btw van verkopen in een bepaalde periode, of van verkopen en inkopen, en het rapport verzenden aan de belastingdienst.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 01/31/2022
ms.author: bholtorf
---

# <a name="report-vat-to-tax-authorities"></a>Btw rapporteren aan de belastingdienst

Dit onderwerp beschrijft de rapporten in [!INCLUDE[prod_short](includes/prod_short.md)] die u kunt gebruiken om gegevens over btw-bedragen voor verkopen en inkopen in te dienen bij de belastingdienst in uw regio. Afhankelijk van het specifieke land/regio kunnen de rapporten specifieke informatie bevatten of zijn er aanvullende rapporten die u moet indienen. Bekijk de artikelen voor uw land/regio in de sectie [Lokale functionaliteit](about-localization.md).  

U kunt de volgende ingebouwde rapporten gebruiken:

* Het rapport **Verkoopoverzicht EU**  

    Het Verkoopoverzicht EU bevat de btw-bedragen die u hebt geïnd voor verkopen aan btw-plichtige klanten in EU-landen/regio's.  
* Het rapport **Btw-aangifte**  

    Het rapport Btw-aangifte bevat btw voor verkopen en inkopen aan klanten en van leveranciers in alle landen/regio's waar btw wordt gebruikt.  

In beide gevallen (en in andere btw-gerelateerde rapporten) wordt btw gebaseerd op de btw-boekingsinstelling en de btw-boekingsgroepen die u hebt ingesteld. [!INCLUDE[prod_short](includes/prod_short.md)] toont btw-boekingen altijd op basis van hun **btw-datum** als primaire rapportagedatum.  

> [!NOTE]
> Alle btw-gerelateerde rapporten worden nu uitgevoerd met de **btw-datum** om relevante records te filteren. Zelfs als u **Gebruik van btw-datum** instelt als **Geen btw-datumfunctionaliteit gebruiken**, verbergt [!INCLUDE[prod_short](includes/prod_short.md)] alle instanties van de **btw-datum** in de toepassing. De **btw-datum** wordt echter nog steeds gebruikt in alle rapportages en wordt automatisch ingevuld met de **boekingsdatum** .

Als u een volledige historie van btw-posten wilt weergeven, maakt elke boeking waarop btw van toepassing is, een post op de pagina **Btw-posten**. Met deze posten wordt het btw-vereffeningsbedrag, dat uit een betaling of vergoeding kan bestaan, berekend voor een bepaalde periode. Als u btw-posten wilt zien, kiest u het ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-posten** in en kies vervolgens de gerelateerde koppeling.

> [!NOTE]
> Elke [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving is bedoeld voor het afhandelen van wettelijke rapportage in één enkel land/regio. Bijvoorbeeld de Nederlandse versie van [!INCLUDE[prod_short](includes/prod_short.md)] verzorgt btw-aangifte in Nederland maar niet in andere landen/regio's. Evenzo verwerkt de Amerikaanse versie van [!INCLUDE[prod_short](includes/prod_short.md)] 1099-rapportage in de Verenigde Staten en biedt deze geen ondersteuning voor het claimen van btw-aangifte in andere landen/regio's, tenzij door een extensie geleverd door ons partnerecosysteem of een klantspecifieke codewijziging.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Informatie over het Verkoopoverzicht EU

In de Europese Unie (EU) en het VK moeten alle bedrijven die goederen en diensten verkopen aan btw-plichtige klanten, inclusief klanten in andere EU-landen/regio's, een elektronische versie van het Verkoopoverzicht EU indienen bij hun douane- en belastingautoriteiten. De lijst **Verkoopoverzicht EU** werkt alleen voor landen/regio's in de EU.

De lijst bevat slechts één regel voor elke soort transactie met de klant en toont het totale bedrag voor elk soort transactie. Er zijn drie soorten transacties die de lijst kan bevatten:  

* B2B-goederen  
* B2B-services  
* B2B getrianguleerde goederen  

*B2B*-goederen en -services geven aan of u een artikel of een service hebt verkocht en worden bepaald door de instelling **EU-service** in de btw-boekingsinstellingen. *B2B getrianguleerde goederen* geven aan of u hebt gehandeld met een derde en worden bepaald door de instelling **ABC-/Driehoekstransacties** op verkoopdocumenten, zoals verkooporders, facturen, creditnota's, enzovoort.  

Nadat de belastingdienst uw lijst heeft gecontroleerd, wordt er een e-mail naar de contactpersoon voor uw bedrijf verzonden. In [!INCLUDE[prod_short](includes/prod_short.md)] wordt de contactpersoon opgegeven op de pagina **Bedrijfsgegevens**. Voordat u de lijst verzendt, moet u ervoor zorgen dat een contact is geselecteerd.  

### <a name="submit-an-ec-sales-list-report"></a>Een rapport Verkoopoverzicht EU indienen

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Informatie over het rapport Btw-aangifte

Gebruik deze lijst om btw voor verkoop- en inkoopdocumenten in te dienen, zoals inkoop- en verkooporders, facturen en creditnota's. De informatie in de lijst heeft dezelfde indeling als op het declaratieformulier van de douane en de belastingdienst.  

Voor de btw-aangifte kunt u de posten opgeven die u wilt opnemen:

* Alleen openstaande transacties of open en afgesloten transacties. Dit is bijvoorbeeld handig wanneer u de definitieve jaarlijkse btw-aangifte voorbereidt.
* Alleen posten uit de opgegeven perioden indienen of ook posten uit eerdere perioden opnemen. Dit is handig om een btw-retour bij te werken die u al hebt ingediend, bijvoorbeeld als u leverancier u een late factuur stuurt.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Verbinding maken met de webservice van uw belastingdienst
[!INCLUDE[prod_short](includes/prod_short.md)] biedt serviceverbindingen met belastingdienstwebsites. Als u zich bijvoorbeeld in het VK bevindt, kunt u de **GovTalk**-serviceverbinding inschakelen om het Verkoopoverzicht EU en de btw-aangifte elektronisch in te dienen. Als u de lijst handmatig wilt verzenden, bijvoorbeeld door uw gegevens op de website van de belastingdienst in te voeren, is dit niet vereist.   

Als u elektronisch btw wilt aangeven bij een belastingdienst, moet u [!INCLUDE[prod_short](includes/prod_short.md)] verbinden met de webservice van de belastingdienst. Hiertoe moet u een account instellen bij uw belastingdienst. Wanneer u een account hebt ingesteld, kunt u een serviceverbinding inschakelen die we aanbieden in [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceverbindingen** in en kies vervolgens de juiste koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Het is aan te raden de verbinding te testen. Kies hiervoor het selectievakje **Testmodus** en bereid uw btw-aangifte voor en verzend deze zoals beschreven in de sectie [Een btw-aangifte voorbereiden en indienen](#to-prepare-and-submit-a-vat-report). In de testmodus test de service of de belastingdienst uw aangifte kan ontvangen en de status van de aangifte geeft aan of de testindiening succesvol was. Vergeet niet dat dit geen werkelijke indiening is. Als u de aangifte echt wilt indienen, moet u het selectievakje **Testmodus** uitzetten en de indiening herhalen.

## <a name="to-set-up-vat-reports-in-"></a>Btw-rapporten instellen in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>Indieningsperioden voor btw instellen

Optioneel, als uw bedrijf niet in het VK is gevestigd, gebruikt u de pagina **Btw-aangifteperiodes** om geplande btw-aangiften in te stellen. Als uw bedrijf in het VK is gevestigd, raadpleegt u [Belasting digitaal maken in het Verenigd Koninkrijk](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-aangifteperioden** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op de pagina **Btw-aangifteperioden** de velden in om de eerste periode in te stellen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Herhaal stap 2 voor eventuele extra perioden die u wilt toevoegen.  

Wanneer het tijd is om een btw-aangifte in te dienen voor een btw-aangifteperiode, kiest u de periode op de pagina **Btw-aangifteperioden** en kiest u vervolgens de actie **Btw-aangifte maken**. Kies vervolgens op de pagina **Btw-aangifte** de actie **Regels voorstellen** zoals beschreven in stap 3 in de volgende procedure.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Een btw-aangifte voorbereiden en indienen

1. Kies het pictogram ![Lampje dat de functie Vertel me 3 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopoverzicht EU** of **Btw-aangifte** in en kies vervolgens de gerelateerde koppeling  
2. Kies **Nieuw** en vul vervolgens de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u de inhoud van de lijst wilt genereren, kiest u de actie **Regels voorstellen**.  

    > [!NOTE]  
    >  In het Verkoopoverzicht EU kunt u de transacties bekijken die in de aangifteregels zijn opgenomen, voordat u de aangifte indient. Kies hiervoor de regel en kies vervolgens de actie **Btw-posten weergeven**.  

4. Als u de lijst voor verzending wilt valideren en voorbereiden, kiest u de actie **Vrijgeven**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] controleert of het rapport correct is ingesteld. Als de validatie mislukt, worden de fouten weergegeven onder **Fouten en waarschuwingen**, zodat u weet wat u moet corrigeren. Als het bericht gaat over een ontbrekende instelling in [!INCLUDE[prod_short](includes/prod_short.md)], kunt u op het bericht kunt klikken om de pagina te openen met de te verbeteren informatie.  
5. Als u de lijst wilt verzenden, kiest u de actie **Verzenden**.  

Als u de lijst hebt verzonden, controleert [!INCLUDE[prod_short](includes/prod_short.md)] de service en wordt een record van uw communicatie bijgehouden. Het veld **Status** geeft aan waar in het proces de lijst zich bevindt. Als de belastingdienst uw rapport bijvoorbeeld verwerkt, verandert de status van het rapport in **Succesvol**. Als de belastingdienst fouten in de lijst heeft gevonden die u hebt verzonden, wordt de status van de lijst **Mislukt**. U kunt de fouten bekijken onder **Fouten en waarschuwingen**, deze corrigeren en vervolgens de lijst opnieuw verzenden. Als u een overzicht wilt van al uw verkoopoverzichten EU, gaat naar de pagina **Rapporten verkoopoverzicht EU**.  

### <a name="vat-return-statuses"></a>Status van btw-aangifte

Btw-aangiften kunnen verschillende statussen hebben, zoals beschreven in de volgende tabel.

| Status | Omschrijving |
|------------|-------------------------|
| Geopend | Wanneer u een nieuwe btw-aangifte maakt. U kunt de actie **Regels voorstellen** uitvoeren. Als u waarden wilt corrigeren, kunt u de actie **Regels voorstellen** opnieuw uitvoeren. U kunt geen btw-aangifte indienen met deze status. |
| Vrijgegeven | De status wordt gewijzigd wanneer u de actie **Vrijgeven** gebruikt. [!INCLUDE[prod_short](includes/prod_short.md)] toont het sneltabblad **Fouten en waarschuwingen**. U kunt geen wijzigingen aanbrengen of de actie **Regels voorstellen** gebruiken. Om wijzigingen door te voeren, moet u de btw-aangifte opnieuw openen. |
| Afgewezen | Als uw indiening niet is gelukt (bijvoorbeeld als verificatie is mislukt), verandert de status in **Afgewezen** . U kunt een btw-aangifte met deze status niet opnieuw openen. |
| Verstuurd | De btw-aangifte wordt ingediend met de actie **Verzenden** of wordt gemarkeerd als verzonden met de actie **Markeren als verzonden** . |
| Geaccepteerd | De btw-aangifte heeft deze status als de aangifte is gemarkeerd als geaccepteerd door middel van de actie **Markeren als geaccepteerd**. Als het rapport **Btw-aangifte** is gemarkeerd als **Geaccepteerd**, kunt u de actie **Btw-vereffening berekenen en boeken** uitvoeren. |

## <a name="viewing-communications-with-your-tax-authority"></a>Communicatie met uw belastingdienst weergeven

In sommige landen/regio's kunt u berichten met de belastingdienst uitwisselen wanneer u rapporten verzendt. U kunt het eerste en laatste bericht dat u hebt ontvangen of verzonden, bekijken door de acties **Indieningsbericht downloaden** en **Responsbericht downloaden** te kiezen.  

## <a name="submitting-vat-reports-manually"></a>Handmatig btw-aangiftes verzenden
Als u een andere methode gebruikt om de lijst te verzenden, bijvoorbeeld door de XML te exporteren en deze te uploaden naar een website, kunt u daarna **Markeren als verzonden** kiezen om de rapportageperiode te sluiten. Wanneer u het btw-rapport markeert als vrijgegeven, wordt het niet-bewerkbaar. Als u het rapport moet wijzigen nadat het is gemarkeerd als vrijgegeven, moet u het opnieuw openen.

## <a name="vat-settlement"></a>Btw-vereffening
U moet periodiek de netto-btw afdragen aan de belastingdienst. Als u vaak btw moet vereffenen, kunt u de batchverwerking **Btw-vereffening berekenen en boeken** uitvoeren om de open btw-posten te sluiten en inkoop- en verkoop-btw-bedragen over te boeken naar de btw-vereffeningsrekening.

Wanneer u btw-bedragen overmaakt naar de vereffeningsrekening, worden de bedragen die voor de opgegeven periode zijn berekend, opgeteld bij de rekening voor inkoop-btw en afgetrokken van de rekening voor verkoop-btw. Het nettobedrag wordt opgeteld of afgetrokken als het inkoop-btw-bedrag groter is, bij de btw-vereffeningsrekening. U kunt de vereffening meteen boeken of eerst een controlelijst afdrukken.  

> [!Note]
> Wanneer u de batchverwerking **Btw-vereffening berekenen en boeken** gebruikt en u geen **btw-bedrijfsboekingsgroep** en **btw-productboekingsgroep** opgeeft, worden posten met alle bedrijfsboekingsgroepen en productboekingsgroepscodes opgenomen.

## <a name="configuring-your-own-vat-reports"></a>Uw eigen btw-rapporten configureren

U kunt het kant-en-klare rapport **Verkoopoverzicht EU** gebruiken. U kunt echter ook uw eigen rapporten maken, als u een ontwikkellicentie hebt, zodat u codeunits kunt maken. Als u hulp nodig hebt, neemt u contact op met een Microsoft-partner.  

De volgende tabel beschrijft codeunits die u voor uw lijst moet maken.  

| Codeunit | Wat het moet doen |
|----|-----|
|Regels voorstellen| Gegevens ophalen uit de tabel **Btw-posten** en deze weergeven op regels in het btw-rapport.|
|Inhoud | De indeling van het rapport bepalen. Bijvoorbeeld of het XML of JSON is. De te gebruiken indeling is afhankelijk van de webservice van uw belastingdienst. |
|Verzending | Bepaal hoe en wanneer u de lijst verzendt, op basis van de behoeften van uw belastingdienst. |
|Antwoordmanager | Behandel de retournering van de belastingdienst. Bijvoorbeeld, er kan een e-mailbericht naar de contactpersoon van uw bedrijf zijn verzonden. |
|Annuleren | Verzend een annulering of btw-rapport dat eerder is ingediend naar de belastingdienst. |  

> [!Note]
> Wanneer u codeunits maakt voor het rapport, besteed dan aandacht aan de waarde in het veld **Btw-rapportversie**. Dit veld moet de versie reflecteren van het rapport dat is of werd vereist door de belastingdienst. U kunt bijvoorbeeld **2021** in het veld invoeren om aan te geven dat de lijst voldoet aan de vereisten die dat jaar golden. Als u de huidige versie wilt bepalen, neemt u contact op met de belastingdienst.  

## <a name="see-also"></a>Zie ook

[Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
