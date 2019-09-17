---
title: Synchronisatie en gegevensintegratie | Microsoft Docs
description: Synchronisatie kopieert gegevens tussen Dynamics 365 for Sales-posten en Business Central-records en houdt de gegevens in beide systemen up-to-date.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 9506b64229c4d936fa25d74d71a923bdf7915e45
ms.sourcegitcommit: 6ef7d2fae52feff786f2e15e2863d7f5aaa762be
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917472"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Gegevens synchroniseren in Business Central en Dynamics 365 for Sales
Wanneer u [!INCLUDE[crm_md](includes/crm_md.md)] met [!INCLUDE[d365fin](includes/d365fin_md.md)] integreert, kunt u bepalen of gegevens in geselecteerde velden van [!INCLUDE[d365fin](includes/d365fin_md.md)]-records (zoals klanten, contactpersonen en verkopers) worden gesynchroniseerd met equivalente records in [!INCLUDE[d365fin](includes/d365fin_md.md)] (zoals rekeningen, contacten en gebruikers). Afhankelijk van het type record kunt u gegevens vanuit [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren met [!INCLUDE[d365fin](includes/d365fin_md.md)] of andersom. Zie voor meer informatie [Integreren met Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synchronisatie gebruikt de volgende elementen:

* Toewijzingen van integratietabellen
* Toewijzingen van integratievelden
* Synchronisatieregels
* Gekoppelde records

Wanneer synchronisatie is ingesteld, kunt u [!INCLUDE[d365fin](includes/d365fin_md.md)]-records koppelen aan [!INCLUDE[crm_md](includes/crm_md.md)]-records om gegevens ervan te synchroniseren. U kunt een synchronisatie handmatig starten of op basis van een planning. In de volgende tabel vindt u een overzicht van de manieren waarop u records kunt synchroniseren.  

|  Soort  |  Methode  |  Zie  |  
|--------|----------|-------|  
|Handmatige synchronisatie|Synchroniseren op recordbasis.<br /><br /> U kunt afzonderlijke records in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals een klant, synchroniseren met een corresponderende [!INCLUDE[crm_md](includes/crm_md.md)]-record, zoals een account. Zo werken gebruikers meestal met [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Records handmatig koppelen en synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synchroniseren op basis van tabeltoewijzing.<br /><br /> U kunt alle records in een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel synchroniseren met een [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit.|[Afzonderlijke tabeltoewijzingen synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Alle gewijzigde records voor alle tabeltoewijzingen synchroniseren.<br /><br /> U kunt alle records synchroniseren die zijn gewijzigd in [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen sinds de laatste synchronisatie.|[Alle gewijzigde records synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Volledige synchronisatie van alle gegevens van alle tabelkoppelingen.<br /><br /> U kunt alle gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen en [!INCLUDE[crm_md](includes/crm_md.md)]-entiteiten synchroniseren die zijn toegewezen en nieuwe records in de doeloplossing maken voor ongekoppelde records in de bronoplossing.<br /><br /> Volledige synchronisatie synchroniseert alle gegevens en negeert koppeling. Meestal voert u een volledige synchronisatie uit wanneer u de integratie instelt en slechts één van de oplossingen gegevens bevat. Een volledige synchronisatie kan ook nuttig zijn in een demonstratieomgeving.|[Een volledige synchronisatie uitvoeren](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Geplande synchronisatie|Alle wijzigingen synchroniseren in gegevens voor alle tabeltoewijzingen.<br /><br /> U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren met geplande intervallen door taken in te stellen in de taakwachtrij.|[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standaardtoewijzing van Sales-entiteit voor synchronisatie
Entiteiten in [!INCLUDE[crm_md](includes/crm_md.md)], zoals accounts, zijn geïntegreerd met equivalente soorten entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals klanten. Als u wilt werken met [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens, stelt u koppelingen in tussen entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)].

In de volgende tabel staat de standaardtoewijzing tussen entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] die [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synchronisatierichting|Standaardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Verkoper/Inkoper|Gebruiker|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-contactfilter: **Status** is **Nee**, **Gebruiker licentie** is **Ja**, Modus Integratiegebruiker is **Nee**|
|Klant|Rekening|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-accountfilter: **Relatietype** is **Klant** en **Status** is **Actief**.|
|Contactpersoon|Contactpersoon|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-contactfilter: **Type** is **Persoon** en de contactpersoon is toegewezen aan een bedrijf. Sales-contactfilter: de contactpersoon is toegewezen aan een bedrijf en het bovenliggende klanttype is **Account**.|
|Valuta|Transactievaluta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Eenheid|Eenhedengroep|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Artikel|Product|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-contactfilter: **Producttype** is **Verkoopvoorraad**|
|Bron|Product|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-contactfilter: **Producttype** is **Services**|
|Klantenprijsgroep|Prijslijst|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkoopprijs|Productprijslijst|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-contactfilter: **Verkoopcode** is niet leeg, **Verkoopsoort** is **Klantenprijsgroep**|
|Opportunity|Opportunity|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Verkoopfactuur|Factureren|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkoopfactuurregel|Factuurproduct|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkooporderkop|Verkooporder|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-verkoopkopfilter: **Documenttype** is Order, **Status** is Vrijgegeven|
|Verkoopordernotities|Verkoopordernotities|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Tip voor beheerders: entiteittoewijzingen weergeven
U kunt de koppeling tussen de entiteiten in [!INCLUDE[crm_md](includes/crm_md.md)] en de tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] bekijken op de pagina **Toewijzingen van integratietabellen**, waar u kunt ook filters kunt toepassen. U definieert de toewijzing tussen de velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen en de velden in [!INCLUDE[crm_md](includes/crm_md.md)]-entiteiten op de pagina **Toewijzing van integratieveld**, waar u aanvullende toewijzingslogica kunt toevoegen. Dat kan bijvoorbeeld handig zijn als u problemen met synchronisatie moet oplossen.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Tip voor ontwikkelaars: velden in Business Central toewijzen aan de optiesets in Sales
Als u een ontwikkelaar bent en opties wilt toevoegen aan de optiesets in [!INCLUDE[crm_md](includes/crm_md.md)], moet u dit weten. Er zijn drie tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] die zijn toegewezen aan de optievelden van de entiteit **Rekening** in [!INCLUDE[crm_md](includes/crm_md.md)]. Records in de tabellen die niet zijn gekoppeld aan opties in [!INCLUDE[crm_md](includes/crm_md.md)], worden niet gesynchroniseerd. Dit houdt in dat het veld **Optie** leeg is in [!INCLUDE[crm_md](includes/crm_md.md)].

De volgende tabel bevat toewijzingen van [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen voor het veld **Optie** in de **Rekening**-entiteit in [!INCLUDE[crm_md](includes/crm_md.md)].

|Tafel|Optieveld in de rekeningentiteit|
|----------------------|-------------------------------------------|
|Betalingsvoorwaarden|Betalingsvoorwaarden|
|Verzendwijze|Adres 1: vrachtvoorwaarden|
|Expediteurs|Adres 1: verzendmethode|

### <a name="synchronization-rules"></a>Synchronisatieregels
De volgende tabel beschrijft regels die de synchronisatie tussen de apps bepalen.

> [!NOTE]  
> Wijzigingen in gegevens in [!INCLUDE[crm_md](includes/crm_md.md)] die zijn gemaakt door het gebruikersaccount van de [!INCLUDE[crm_md](includes/crm_md.md)]-verbinding worden niet gesynchroniseerd. Daarom raden we aan dat u geen gegevens wijzigt terwijl u dat account gebruikt. Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tafel|Regel|
|-----|----|
|Klanten|Voordat een klant met een rekening kan worden gesynchroniseerd, moet de verkoper die aan de klant is toegewezen, aan een gebruiker worden gekoppeld in [!INCLUDE[crm_md](includes/crm_md.md)]. Daarom, wanneer u de Dynamics 365 for Sales-synchronisatietaak KLANTEN uitvoert en instelt om nieuwe records te maken, moet u ervoor zorgen dat u verkopers synchroniseert met [!INCLUDE[crm_md](includes/crm_md.md)]-gebruikers voordat u klanten synchroniseert met accounts in [!INCLUDE[crm_md](includes/crm_md.md)]. <br /> <br />De Dynamics 365 for Sales-synchronisatietaak KLANTEN synchroniseert alleen Sales-accounts die het relatietype Klant hebben.|
|Contacten|Alleen contactpersonen in [!INCLUDE[crm_md](includes/crm_md.md)] die zijn gekoppeld aan een account, worden gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)]. De waarde van Verkoperscode definieert de eigenaar van de gekoppelde entiteit in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Valuta's|Valuta's worden aan transactievaluta's in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppeld op basis van ISO-codes. Alleen valuta's die een standaard-ISO-code hebben, worden gekoppeld en gesynchroniseerd met transactievaluta's.|
|Eenheden|Maateenheden worden gesynchroniseerd met eenheidsgroepen in [!INCLUDE[crm_md](includes/crm_md.md)]. Er kan slechts één eenheid worden gedefinieerd in de eenhedengroep.|
|Artikelen|Wanneer artikelen worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-producten, maakt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch een prijslijst in [!INCLUDE[crm_md](includes/crm_md.md)]. Als u synchronisatiefouten wilt voorkomen, moet u deze prijslijst niet handmatig wijzigen.|
|Verkopers|Verkopers worden gekoppeld aan systeemgebruikers in [!INCLUDE[crm_md](includes/crm_md.md)]. De gebruiker moet zijn ingeschakeld en een licentie hebben en moet niet de integratiegebruiker zijn. Dit is de eerste tabel die moet worden gesynchroniseerd, omdat deze wordt gebruikt in klanten, contactpersonen, opportunity's en verkoopfacturen.|
|Resources|Resources worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-producten van het producttype Service.|
|Klantenprijsgroepen|Klantenprijsgroepen worden gesynchroniseerd met Sales-prijslijsten.|
|Verkoopprijzen|Sales-prijzen die het verkoopsoort Klantenprijsgroep hebben en waarvoor een verkoopcode is gedefinieerd, worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-prijslijstregels|
|Opportunity's|Opportunity's worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-opportunity's. De waarde van Verkoperscode definieert de eigenaar van de gekoppelde entiteit in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Geboekte verkoopfacturen|Geboekte verkoopfacturen worden gesynchroniseerd met verkoopfacturen. Voordat een factuur kan worden gesynchroniseerd, is het beter om alle andere entiteiten die deel kunnen nemen aan de factuur, te synchroniseren van verkopers naar prijslijsten. De waarde van Verkoperscode op de factuurkop definieert de eigenaar van de gekoppelde entiteit in Sales.|
|Verkooporders|Wanneer integratie van verkooporders is ingeschakeld, worden verkooporders binnen [!INCLUDE[d365fin](includes/d365fin_md.md)] die zijn gemaakt op basis van ingediende verkooporders in [!INCLUDE[crm_md](includes/crm_md.md)], gesynchroniseerd met verkooporders in VERKOOP OPNEMEN wanneer ze worden vrijgegeven. Voordat u orders synchroniseert, raden we u aan eerst alle entiteiten te synchroniseren die bij de order betrokken zijn, zoals verkoopmedewerkers en prijslijsten. Het veld Verkoperscode in de orderkop definieert de eigenaar van de gekoppelde entiteit in [!INCLUDE[crm_md](includes/crm_md.md)].|  

## <a name="see-also"></a>Zie ook  
[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)   
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integreren met Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
