---
title: Klanten beheren met Dynamics 365 for Sales | Microsoft Docs
description: U kunt Dynamics 365 for Sales vanuit Business Central gebruiken om gegevens te koppelen en naadloze integratie en synchronisatie te hebben in het potentiële klant-naar-contanten proces.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 06/13/2019
ms.author: bholtorf
ms.openlocfilehash: 716e195b4e8c5b4150d7a288918c3fb84f6ac713
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726871"
---
# <a name="using-dynamics-365-for-sales-from-business-central"></a>Dynamics 365 for Sales gebruiken vanuit Business Central
Als u Dynamics 365 for Sales gebruikt voor contacten met klanten, kunt u profiteren van naadloze integratie in het lead-naar-cash proces door [!INCLUDE[d365fin](includes/d365fin_md.md)] te gebruiken voor backendactiviteiten zoals verwerking van orders, beheer van voorraad en het doen van uw financiën.

Voordat u de integratiemogelijkheden kunt gebruiken, moet u de verbinding instellen en gebruikers definiëren in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integreren met Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Deze stappen beschrijven de integratie van online versies van [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie voor informatie over on-premises configuratie [Dynamics 365 for Sales voorbereiden voor on-premises integratie](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Als u de toepassingen integreert, krijgt u vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] toegang tot gegevens in Sales en in sommige gevallen ook andersom. U kunt gegevens gebruiken en synchroniseren die beide services gemeen hebben, zoals klanten, contacten en verkoopinformatie, en de gegevens up-to-date houden in beide toepassingen.  

Een verkoper in Sales kan bijvoorbeeld de prijslijsten uit [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken bij het maken van een verkooporder. Als hij of zij het artikel toevoegt aan de verkooporderregel in Sales, kan hij of zij het voorraadniveau (de beschikbaarheid) van het artikel zien vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)].

Andersom kunnen orderverwerkers in [!INCLUDE[d365fin](includes/d365fin_md.md)] verkooporders verwerken die automatisch of handmatig uit verkoop worden overgebracht. Zij kunnen bijvoorbeeld verkooporderregels maken en boeken voor artikelen of resources die in Sales zijn ingevoerd als inschrijfproducten. Zie voor meer informatie het gedeelte [Verkoopordergegevens verwerken](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt alleen met Dynamics 365 for Sales geïntegreerd. Overige Dynamics 365-toepassingen die de standaardwerkstroom of gegevensmodel in Sales wijzigen, bijvoorbeeld Project Service Automation, kunnen de integratie tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Sales verbreken.

### <a name="coupling-records"></a>Records koppelen
De begeleide instelling laat u de gegevens kiezen die u wilt synchroniseren. Later kunt u ook synchronisatie voor specifieke records instellen. Dit wordt *koppeling* genoemd. U kunt bijvoorbeeld een specifiek account in Sales koppelen aan een specifieke klant in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Deze sectie beschrijft waar u rekening mee moet houden wanneer u records koppelt.

Als u bijvoorbeeld Sales-accounts wilt zien als klanten in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de twee soorten records koppelen. Als u dat wilt doen, gebruikt u op de lijstpagina **Klanten** in [!INCLUDE[d365fin](includes/d365fin_md.md)] de actie **Koppeling instellen**. Vervolgens geeft u op welke [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten moeten worden afgestemd op welke accounts in Sales.

U kunt ook een account maken (en koppelen) in Sales op basis van bijvoorbeeld klantenrecords in [!INCLUDE[d365fin](includes/d365fin_md.md)] met behulp van **Account maken in Dynamics 365 for Sales** of andersom met behulp van **Klant maken in [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Wanneer u koppeling instelt tussen twee records, kunt u ook handmatig verzoeken dat de huidige record, bijvoorbeeld een klant, direct wordt overschreven door accountgegevens vanuit Sales (of vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]) met behulp van de actie **Nu synchroniseren**. De actie **Nu synchroniseren** die vraagt of Sales- of [!INCLUDE[d365fin](includes/d365fin_md.md)]-recordgegevens moeten worden overschreven.

In sommige gevallen moet u bepaalde sets gegevens koppelen voordat u andere sets gegevens koppelt, zoals getoond in de volgende tabel.

|Gegevens|Wat eerst koppelen|
|-----|----|
|Klanten en accounts|Verkopers koppelen aan Sales-gebruikers|
|Artikelen en resources|Maateenheden koppelen aan Sales-eenheidsgroepen|
|Artikelen en resourceprijzen|Klantenprijsgroepen koppelen aan Sales-prijzen|

> [!NOTE]  
> Als uw prijzen of kanten vreemde valuta's gebruiken, moet u ervoor zorgen dat u valuta's koppelt aan Sales-transactievaluta's.

Verkooporders in Sales zijn afhankelijk van informatie zoals klanten, eenheden, valuta's, klantenprijsgroepen en artikelen en/of resources. Om de integratie met verkooporders te laten werken moet u eerst klanten, eenheden, valuta's, klantprijsgroepen en artikelen en/of resources koppelen.

### <a name="fully-synchronizing-records"></a>Records volledig synchroniseren
Aan het eind van de begeleide instelling kunt u de actie **Volledige synchronisatie uitvoeren** kiezen om alle records in [!INCLUDE[d365fin](includes/d365fin_md.md)] te synchroniseren met alle gerelateerde records in Sales. Kies op de pagina **Controle van volledige Dynamics 365 for Sales-synchronisatie** de actie **Starten**. Volledige synchronisatie kan enige tijd duren om te voltooien, maar u kunt doorwerken in [!INCLUDE[d365fin](includes/d365fin_md.md)] terwijl de synchronisatie op de achtergrond wordt uitgevoerd.

Als u de voortgang van afzonderlijke taken in een volledige synchronisatie wilt volgen, kiest u op de pagina **Controle van volledige Dynamics 365 for Sales-synchronisatie** een record om details te bekijken. Als u de status tijdens de synchronisatie wilt bijwerken, vernieuwt u de pagina.

Vanuit het venster **Microsoft Dynamics 365-verbinding instellen** kunt u informatie over de volledige synchronisatie op ieder gewenst moment oproepen. Van hieruit kunt u ook de pagina **Toewijzingen van integratietabellen** openen om details te zien van de tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] en Sales die moeten worden gesynchroniseerd.

## <a name="handling-sales-order-data"></a>Verkoopordergegevens verwerken
Verkooporders die worden ingediend in [!INCLUDE[crm_md](includes/crm_md.md)], worden overgebracht naar [!INCLUDE[d365fin](includes/d365fin_md.md)] als u het selectievakje **Automatisch verkooporders maken** inschakelt op de pagina **Microsoft Dynamics 365-verbinding instellen**.
U kunt ook handmatig ingediende verkooporders vanuit [!INCLUDE[crm_md](includes/crm_md.md)] converteren met de actie **Maken in [!INCLUDE[d365fin](includes/d365fin_md.md)]**, die beschikbaar is op de pagina **Verkooporders - Dynamics 365 for Sales**.
Voor deze verkooporders wordt het veld **Naam** op de oorspronkelijke order overgebracht en toegewezen aan het veld **Extern documentnummer** op de verkooporder op [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dit kan ook werken als de oorspronkelijke verkooporder inschrijfproducten bevat met artikelen of resources die niet in een van beide apps zijn geregistreerd. In dat geval vult u de velden **Inschrijfproductsoort** en **Inschrijfproductnummer** in op de pagina **Instellingen van verkoop en tegoeden**, zodat deze niet-geregistreerde productverkopen worden gekoppeld aan een specifiek artikel-/resourcenummer voor financiële analyse.

Als de artikelomschrijving op de oorspronkelijke verkooporder erg lang is, wordt een extra verkooporderregel van het type **Opmerking** gemaakt zodat de volledige tekst wordt opgenomen in de verkooporder in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Updates in verkooporderkopvelden, zoals Laatste verzenddatum of Verzochte leverdatum, die zijn toegewezen in VERKOOPORDER-ORDER **Toewijzing van integratietabellen** worden periodiek gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]. Processen zoals het vrijgeven van een verkooporder en verzending of facturering van een verkooporder, worden geboekt naar de verkoopordertijdlijn in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Inleiding in activiteitfeeds](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/introduction-activity-feeds).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Verkoopoffertegegevens verwerken
Verkoopoffertes die worden geactiveerd in [!INCLUDE[crm_md](includes/crm_md.md)], worden overgebracht naar [!INCLUDE[d365fin](includes/d365fin_md.md)] als u het selectievakje **Offertes automatisch verwerken** inschakelt op de pagina **Microsoft Dynamics 365-verbinding instellen**.
U kunt ook handmatig geactiveerde verkoopoffertes vanuit [!INCLUDE[crm_md](includes/crm_md.md)] converteren met de actie **Verwerken in [!INCLUDE[d365fin](includes/d365fin_md.md)]** op de pagina **Verkoopoffertes - Dynamics 365 for Sales**.
Voor deze verkoopoffertes wordt het veld **Naam** op de oorspronkelijke offerte overgebracht en toegewezen aan het veld **Extern documentnummer** op de verkooporder in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Daarnaast wordt het veld **Geldig tot** in de offerte overgebracht naar en toegewezen aan het veld **Offerte geldig tot** in de verkoopofferte in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Verkoopoffertes doorlopen veel revisies terwijl ze worden afgerond. Zowel handmatige als automatische verwerking van verkoopoffertes in [!INCLUDE[d365fin](includes/d365fin_md.md)] zorgt ervoor dat vorige versies van verkoopoffertes worden gearchiveerd voordat nieuwe revisies van verkoopoffertes worden verwerkt vanuit [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Geboekte verkoopfacturen, klantbetalingen en statistieken verwerken
Na het uitvoeren van een verkooporder worden er facturen voor gemaakt. Als u een verkooporder factureert, kunt u de geboekte verkoopfactuur aan [!INCLUDE[crm_md](includes/crm_md.md)] overdragen als u het selectievakje **Factuur maken in [!INCLUDE[crm_md](includes/crm_md.md)]** selecteert op de pagina **Geboekte verkoopfactuur**. Geboekte facturen worden overgedragen aan [!INCLUDE[crm_md](includes/crm_md.md)] met de status **Gefactureerd**.

Als de klantbetaling voor de verkoopfactuur is ontvangen in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt de status van de verkoopfactuur gewijzigd in **Betaald**, met de **statusreden** ingesteld op **Gedeeltelijk**, indien gedeeltelijk betaald, of op **Volledig** indien geheel voldaan, wanneer u de actie **Rekeningstatistiek bijwerken** kiest op de klantpagina in [!INCLUDE[d365fin](includes/d365fin_md.md)]. De functie **Rekeningstatistiek bijwerken** vernieuwt ook waarden zoals de velden **Saldo** en **Totale verkoop** in het feitenblok **[!INCLUDE[d365fin](includes/d365fin_md.md)]-rekeningstatistiek** in [!INCLUDE[crm_md](includes/crm_md.md)]. U kunt ook de geplande taken, Klantstatistieken en GEBOEKTEVERKOOPFACTUUR-FACT, automatisch beide processen laten uitvoeren op de achtergrond.

## <a name="see-also"></a>Zie ook
[Integreren met Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Relatiebeheer](marketing-relationship-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Uw organisatie en gebruikers onboarden in Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
