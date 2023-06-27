---
title: Klanten beheren met Dynamics 365 Sales (bevat video) | Microsoft Docs
description: U kunt Dynamics 365 Sales vanuit Business Central gebruiken met naadloze integratie en synchronisatie in het potentiële klant-naar-contanten proces.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'integration, synchronize, map, Sales'
ms.search.forms: '9980, 5341, 5349, 5330, 1817, 5342, 5337, 5336, 5331, 5343, 5334, 5346, 5348, 5329, 5380, 5353, 5381, 5351, 5333, 5360, 5373, 5371, 5340, 5345, 5362, 1313, 5361, 1876, 5339, 5338, 5335, 5332, 6250'
ms.date: 09/16/2022
ms.author: bholtorf
---
# <a name="use-dynamics-365-sales-from-business-central" />Dynamics 365 Sales gebruiken vanuit Business Central
Als u Dynamics 365 Sales gebruikt voor contacten met klanten, kunt u profiteren van naadloze integratie in het lead-naar-cash proces door [!INCLUDE[prod_short](includes/prod_short.md)] te gebruiken voor backendactiviteiten zoals verwerking van orders, beheer van voorraad en het doen van uw financiën.

Voordat u de integratiemogelijkheden kunt gebruiken, moet uw systeembeheerder de verbinding instellen en gebruikers definiëren in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Deze stappen beschrijven de integratie van online versies van [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor informatie over on-premises configuratie [Dynamics 365 Sales voorbereiden voor on-premises integratie](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Als u de toepassingen integreert, krijgt u vanuit [!INCLUDE[prod_short](includes/prod_short.md)] toegang tot gegevens in Sales en in sommige gevallen ook andersom. U kunt gegevens gebruiken en synchroniseren die beide services gemeen hebben, zoals klanten, contacten en verkoopinformatie, en de gegevens up-to-date houden in beide toepassingen.  

Een verkoper in [!INCLUDE[crm_md](includes/crm_md.md)] kan bijvoorbeeld de prijslijsten uit [!INCLUDE[prod_short](includes/prod_short.md)] gebruiken bij het maken van een verkooporder. Als hij of zij het artikel toevoegt aan de verkooporderregel in [!INCLUDE[crm_md](includes/crm_md.md)], kan hij of zij het voorraadniveau (de beschikbaarheid) van het artikel zien vanuit [!INCLUDE[prod_short](includes/prod_short.md)].

Andersom kunnen orderverwerkers in [!INCLUDE[prod_short](includes/prod_short.md)] verkooporders verwerken die automatisch of handmatig uit [!INCLUDE[crm_md](includes/crm_md.md)] worden overgebracht. Zij kunnen bijvoorbeeld verkooporderregels maken en boeken voor artikelen of resources die in [!INCLUDE[crm_md](includes/crm_md.md)] zijn ingevoerd als inschrijfproducten. Zie voor meer informatie het gedeelte [Verkoopordergegevens verwerken](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] wordt alleen met [!INCLUDE[crm_md](includes/crm_md.md)] geïntegreerd. Overige Dynamics 365-toepassingen die de standaardwerkstroom of gegevensmodel in [!INCLUDE[crm_md](includes/crm_md.md)] wijzigen, bijvoorbeeld Project Service Automation, kunnen de integratie tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] verbreken.

## <a name="coupling-records" />Records koppelen
De begeleide instelling laat u de gegevens kiezen die u wilt synchroniseren. Later kunt u ook synchronisatie voor specifieke records instellen. Dit wordt *koppeling* genoemd. U kunt bijvoorbeeld een specifiek account in [!INCLUDE[crm_md](includes/crm_md.md)] koppelen aan een specifieke klant in [!INCLUDE[prod_short](includes/prod_short.md)]. Deze sectie beschrijft waar u rekening mee moet houden wanneer u records koppelt.

Als u bijvoorbeeld accounts in [!INCLUDE[crm_md](includes/crm_md.md)] wilt zien als klanten in [!INCLUDE[prod_short](includes/prod_short.md)], moet u de twee soorten records koppelen. Als u dat wilt doen, gebruikt u op de lijstpagina **Klanten** in [!INCLUDE[prod_short](includes/prod_short.md)] de actie **Koppeling instellen**. Vervolgens geeft u op welke [!INCLUDE[prod_short](includes/prod_short.md)]-klanten moeten worden afgestemd op welke accounts in [!INCLUDE[crm_md](includes/crm_md.md)].

U kunt ook een account maken (en koppelen) in [!INCLUDE[crm_md](includes/crm_md.md)] op basis van bijvoorbeeld klantenrecords in [!INCLUDE[prod_short](includes/prod_short.md)] met behulp van **Account maken in Dynamics 365 Sales** of andersom met behulp van **Klant maken in [!INCLUDE[prod_short](includes/prod_short.md)]**.

Wanneer u koppeling instelt tussen twee records, kunt u ook handmatig verzoeken dat de huidige record, bijvoorbeeld een klant, direct wordt overschreven door accountgegevens vanuit Sales (of vanuit [!INCLUDE[prod_short](includes/prod_short.md)]) met behulp van de actie **Nu synchroniseren**. De actie **Nu synchroniseren** die vraagt of Sales- of [!INCLUDE[prod_short](includes/prod_short.md)]-recordgegevens moeten worden overschreven.

In sommige gevallen moet u bepaalde sets gegevens koppelen voordat u andere sets gegevens koppelt, zoals getoond in de volgende tabel.

|Gegevens|Wat eerst koppelen|
|-----|----|
|Klanten en accounts|Verkopers koppelen aan [!INCLUDE[crm_md](includes/crm_md.md)]-gebruikers|
|Artikelen en resources|Maateenheden koppelen aan [!INCLUDE[crm_md](includes/crm_md.md)]-eenheidsgroepen|
|Artikelen en resourceprijzen|Klantenprijsgroepen koppelen aan [!INCLUDE[crm_md](includes/crm_md.md)]-prijzen|

> [!NOTE]  
> Als uw prijzen of kanten vreemde valuta's gebruiken, moet u ervoor zorgen dat u valuta's koppelt aan Sales-transactievaluta's.

Verkooporders in [!INCLUDE[crm_md](includes/crm_md.md)] zijn afhankelijk van informatie zoals klanten, eenheden, valuta's, klantenprijsgroepen en artikelen en/of resources. Om de integratie met verkooporders te laten werken moet u eerst klanten, eenheden, valuta's, klantprijsgroepen en artikelen en/of resources koppelen.

## <a name="fully-synchronizing-records" />Records volledig synchroniseren
Aan het eind van de begeleide instelling kunt u de actie **Volledige synchronisatie uitvoeren** kiezen om alle records in [!INCLUDE[prod_short](includes/prod_short.md)] te synchroniseren met alle gerelateerde records in [!INCLUDE[crm_md](includes/crm_md.md)]. Kies op de pagina **Controle van volledige Dynamics 365 Sales-synchronisatie** de actie **Starten**. Volledige synchronisatie kan enige tijd duren om te voltooien, maar u kunt doorwerken in [!INCLUDE[prod_short](includes/prod_short.md)] terwijl de synchronisatie op de achtergrond wordt uitgevoerd.

Als u de voortgang van afzonderlijke taken in een volledige synchronisatie wilt volgen, kiest u op de pagina **Controle van volledige Dynamics 365 Sales-synchronisatie** een record om details te bekijken. Als u de status tijdens de synchronisatie wilt bijwerken, vernieuwt u de pagina.

Vanuit het venster **Microsoft Dynamics 365-verbinding instellen** kunt u informatie over de volledige synchronisatie op ieder gewenst moment oproepen. Van hieruit kunt u ook de pagina **Toewijzingen van integratietabellen** openen om details te zien van de tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] en Sales die moeten worden gesynchroniseerd.

## <a name="handling-sales-order-data" />Verkoopordergegevens verwerken
Verkooporders die worden ingediend in [!INCLUDE[crm_md](includes/crm_md.md)], worden automatisch overgebracht naar [!INCLUDE[prod_short](includes/prod_short.md)] als u het selectievakje **Automatisch verkooporders maken** inschakelt op de pagina **Microsoft Dynamics 365-verbinding instellen**.
U kunt ook handmatig ingediende verkooporders vanuit [!INCLUDE[crm_md](includes/crm_md.md)] converteren met de actie **Maken in [!INCLUDE[prod_short](includes/prod_short.md)]**, die beschikbaar is op de pagina **Verkooporders - Dynamics 365 for Sales**.
Voor deze verkooporders wordt het veld **Naam** op de oorspronkelijke order overgebracht en toegewezen aan het veld **Extern documentnummer** op de verkooporder op [!INCLUDE[prod_short](includes/prod_short.md)].

Dit kan ook werken als de oorspronkelijke verkooporder inschrijfproducten bevat met artikelen of resources die niet in een van beide apps zijn geregistreerd. In dat geval vult u de velden **Inschrijfproductsoort** en **Inschrijfproductnummer** in op de pagina **Instellingen van verkoop en tegoeden**, zodat verkopen van niet-geregistreerde producten worden gekoppeld aan een specifiek artikel- of resourcenummer.

> [!NOTE]
> U kunt een inschrijving niet toewijzen aan een artikel of resource in [!INCLUDE[prod_short](includes/prod_short.md)] die is gekoppeld aan een product in [!INCLUDE[crm_md](includes/crm_md.md)]. Om inschrijvingen mogelijk te maken, raden we u aan een artikel of bron specifiek voor dat doel te maken en het niet te koppelen aan een product in [!INCLUDE[crm_md](includes/crm_md.md)]. 

Als de artikelomschrijving op de oorspronkelijke verkooporder erg lang is, wordt een extra verkooporderregel van het type **Opmerking** gemaakt zodat de volledige tekst wordt opgenomen in de verkooporder in [!INCLUDE[prod_short](includes/prod_short.md)].

Updates op velden in verkooporderkopteksten, zoals de velden Laatste verzenddatum of Verzochte leverdatum, die zijn toegewezen in de integratietabeltoewijzing **VERKOOPORDER-ORDER** worden periodiek gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]. Processen zoals het vrijgeven van een verkooporder en verzending of facturering van een verkooporder, worden geboekt naar de verkoopordertijdlijn in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Inleiding in activiteitfeeds](/dynamics365/sales-enterprise/manage-activities). Om boekingen en activiteiten voor orders in te schakelen [!INCLUDE[crm_md](includes/crm_md.md)] raadpleegt u [Het besturingselement Notities instellen voor toegangsinformatie over berichten voor een aangepaste entiteit](/dynamics365/customerengagement/on-premises/customize/notes-control-legacy) in de Customer Engagement-documentatie. Het artikel verwijst naar Customer Engagement on-premises, maar de stappen zijn hetzelfde voor de online versie. <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Periodieke synchronisatie op basis van de integratietabeltoewijzing **VERKOOPORDER-ORDER** werkt alleen wanneer integratie van verkooporders is ingeschakeld. Zie voor meer informatie [Verbindingsinstellingen op de pagina Sales-verbinding instellen](admin-prepare-dynamics-365-for-sales-for-integration.md). Alleen verkooporders die zijn gemaakt van ingediende verkooporders in [!INCLUDE[crm_md](includes/crm_md.md)], worden gesynchroniseerd. Zie voor meer informatie [Integratie van verkooporderverwerking inschakelen](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data" />Verkoopoffertegegevens verwerken
Verkoopoffertes die worden geactiveerd in [!INCLUDE[crm_md](includes/crm_md.md)], worden overgebracht naar [!INCLUDE[prod_short](includes/prod_short.md)] als u het selectievakje **Offertes automatisch verwerken** inschakelt op de pagina **Microsoft Dynamics 365-verbinding instellen**.
U kunt ook handmatig geactiveerde verkoopoffertes vanuit [!INCLUDE[crm_md](includes/crm_md.md)] converteren met de actie **Verwerken in [!INCLUDE[prod_short](includes/prod_short.md)]** op de pagina **Verkoopoffertes - Dynamics 365 Sales**.
Voor deze verkoopoffertes wordt het veld **Naam** op de oorspronkelijke offerte overgebracht en toegewezen aan het veld **Extern documentnummer** op de verkooporder in [!INCLUDE[prod_short](includes/prod_short.md)]. Daarnaast wordt het veld **Geldig tot** in de offerte overgebracht naar en toegewezen aan het veld **Offerte geldig tot** in de verkoopofferte in [!INCLUDE[prod_short](includes/prod_short.md)].  

Verkoopoffertes doorlopen veel revisies terwijl ze worden afgerond. Zowel handmatige als automatische verwerking van verkoopoffertes in [!INCLUDE[prod_short](includes/prod_short.md)] zorgt ervoor dat vorige versies van verkoopoffertes worden gearchiveerd voordat nieuwe revisies van verkoopoffertes worden verwerkt vanuit [!INCLUDE[crm_md](includes/crm_md.md)].

Wanneer u **Proces** in [!INCLUDE[prod_short](includes/prod_short.md)] kiest voor een offerte die de status **Gewonnen** heeft, wordt alleen een verkooporder gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] als een bijbehorende verkooporder wordt ingediend in [!INCLUDE[crm_md](includes/crm_md.md)]. Anders wordt de offerte alleen vrijgegeven in [!INCLUDE[prod_short](includes/prod_short.md)]. Als later een bijbehorende verkooporder wordt ingediend in [!INCLUDE[crm_md](includes/crm_md.md)] en er wordt een verkooporder van gemaakt, wordt het **offertenr.** bijgewerkt op de verkooporder en wordt de offerte gearchiveerd.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics" />Geboekte verkoopfacturen, klantbetalingen en statistieken verwerken
Na het uitvoeren van een verkooporder worden er facturen voor gemaakt. Als u een verkooporder factureert, kunt u de geboekte verkoopfactuur aan [!INCLUDE[crm_md](includes/crm_md.md)] overdragen als u het selectievakje **Factuur maken in [!INCLUDE[crm_md](includes/crm_md.md)]** selecteert op de pagina **Geboekte verkoopfactuur**. Geboekte facturen worden overgedragen aan [!INCLUDE[crm_md](includes/crm_md.md)] met de status **Gefactureerd**.

Als de klantbetaling voor de verkoopfactuur is ontvangen in [!INCLUDE[prod_short](includes/prod_short.md)], wordt de status van de verkoopfactuur gewijzigd in **Betaald**, met de **statusreden** ingesteld op **Gedeeltelijk**, indien gedeeltelijk betaald, of op **Volledig** indien geheel voldaan, wanneer u de actie **Rekeningstatistiek bijwerken** kiest op de klantpagina in [!INCLUDE[prod_short](includes/prod_short.md)]. De functie **Rekeningstatistiek bijwerken** vernieuwt ook waarden zoals de velden **Saldo** en **Totale verkoop** in het feitenblok **[!INCLUDE[prod_short](includes/prod_short.md)]-rekeningstatistiek** in [!INCLUDE[crm_md](includes/crm_md.md)]. U kunt ook de geplande taken, Klantstatistieken en GEBOEKTEVERKOOPFACTUUR-FACT, automatisch beide processen laten uitvoeren op de achtergrond. 

## <a name="handling-sales-prices" />Omgaan met verkoopprijzen
> [!NOTE]
> In releasewave 2 van 2020 hebben we gestroomlijnde processen uitgebracht voor het instellen en beheren van prijzen en kortingen. Als u een nieuwe klant bent en die versie gebruikt, gebruikt u de nieuwe ervaring. Als u een bestaande klant bent, hangt of u de nieuwe ervaring gebruikt, af van de vraag of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd in **Functiebeheer**. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management).

Deze stappen om dit proces te voltooien verschillen, afhankelijk van of uw beheerder de nieuwe verkoopprijservaring heeft ingeschakeld. 

> [!NOTE]
> Als de synchronisatie van de standaardprijs niet werkt voor u, raden we u aan om de aanpassingsmogelijkheden voor integratie te gebruiken. Zie voor meer informatie [Een integratie met Microsoft Dataverse aanpassen](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### [Huidige ervaring](#tab/current-experience/)
In de huidige verkoopprijservaring synchroniseert [!INCLUDE[prod_short](includes/prod_short.md)] verkoopprijzen die: 

* Van toepassing zijn op alle klanten. Standaardverkoopprijslijsten worden gemaakt op basis van de prijs in het veld **Eenheidsprijs** op de pagina **Artikelkaart** pagina voor de artikelen.
* Van toepassing zijn op een klantenprijsgroep. Bijvoorbeeld verkoopprijzen voor uw detailhandel- of groothandelsklanten. Als u prijzen wilt synchroniseren op basis van een klantprijsgroep, doet u het volgende:

    1. Koppel de artikelen waarvoor de prijzen zijn bepaald door de klantprijsgroep.
    2. Op de pagina **Klantprijsgroepen** koppelt u de klantprijsgroep door **Verwant**, **Dynamics 365 Sales**, **Koppelen** en **Koppeling instellen** te kiezen. Door de koppeling wordt een actieve prijslijst in [!INCLUDE[prod_short](includes/prod_short.md)] gemaakt die dezelfde naam heeft als de klantprijsgroep in [!INCLUDE[crm_md](includes/crm_md.md)] en worden automatisch alle artikelen gesynchroniseerd waarvoor de klantprijsgroep de prijs definieert.

:::image type="content" source="media/customer-price-group.png" alt-text="Pagina Klantenprijsgroep":::

#### [Nieuwe ervaring](#tab/new-experience/)  

Met de nieuwe verkoopprijservaring worden prijslijsten gesynchroniseerd die aan de volgende criteria voldoen:

* **Bijwerken van standaardinstellingen toestaan** is uitgeschakeld.
* Het prijstype is Verkoop.
* De bedragsoort is Prijs.
* Het producttype op de regels moet Artikel of Resource zijn. 
* Er is geen minimumhoeveelheid opgegeven.

[!INCLUDE[prod_short](includes/prod_short.md)] synchroniseert verkoopprijzen die voor alle klanten gelden. Standaardverkoopprijslijsten worden gemaakt op basis van de prijs in het veld **Eenheidsprijs** op de pagina **Artikelkaart** pagina voor de artikelen.

Als u prijslijsten wilt synchroniseren, kiest u op de pagina **Verkoopprijslijst** de optie **Verwant**, **Dynamics 365 Sales**, **Koppelen** en **Koppeling instellen**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Pagina Verkoopprijslijst.":::

---


## <a name="see-also" />Zie ook
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Relatiebeheer](marketing-relationship-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)    
[Overzicht van Sales en Verkoophub](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
