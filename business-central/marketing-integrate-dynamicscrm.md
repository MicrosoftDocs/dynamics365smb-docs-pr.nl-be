---
title: Klanten beheren met Dynamics 365 for Sales| Microsoft Docs
description: "U kunt Dynamics 365 for Sales vanuit Business Central gebruiken om gegevens te koppelen en naadloze integratie en synchronisatie te hebben in het potentiële klant-naar-contanten proces."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 07/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 046a42582dc66368fded90a4bb45add71a95d979
ms.openlocfilehash: 33987f37c170af9982b86baf20f0c3e0682de2cd
ms.contentlocale: nl-be
ms.lasthandoff: 07/02/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Klanten en verkopen beheren die in Dynamics 365 for Sales zijn gemaakt
Als u Dynamics 365 for Sales (Sales) gebruikt voor contacten met klanten, kunt u [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken voor orderverwerking en financiën en profiteren van naadloze integratie in het proces van potentiële klant naar inkomsten.

Als uw toepassing is ingesteld voor integratie met Sales, hebt u toegang tot gegevens in Sales vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] en in sommige gevallen ook andersom. Dankzij deze integratie kunt u werken met gegevenstypen die voor beide services worden gebruikt, zoals klanten, contacten en verkoopinformatie, deze gegevenstypen synchroniseren en de gegevens in beide locaties up-to-date houden.  

De verkoper in Sales kan bijvoorbeeld prijslijsten van [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken bij het opstellen van een verkooporder. Als hij het artikel toevoegt aan de verkooporderregel in Sales, kan hij ook het voorraadniveau (de beschikbaarheid) van het artikel zien vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)].

Orderverwerkers in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen ook de speciale kenmerken verwerken van verkooporders die automatisch of handmatig zijn overgebracht uit Sales, zoals het automatisch maken en boeken van geldige verkooporderregels voor artikelen of resources die in Sales zijn ingevoerd als inschrijfproducten. Zie voor meer informatie het gedeelte "Speciale verkoopordergegevens verwerken".

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt alleen geïntegreerd met Dynamics 365 for Sales. Overige toepassingen of oplossingen binnen Dynamics 365 die de standaardwerkstroom of gegevensmodel in Sales wijzigen, bijvoorbeeld Project Service Automation, kunnen de integratie tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Sales verbreken.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standaardtoewijzing van Sales-entiteit voor synchronisatie
Sales-entiteiten, zoals accounts, worden geïntegreerd met equivalente [!INCLUDE[d365fin](includes/d365fin_md.md)]-recordtypen, zoals klanten. Als u wilt werken met Sales-gegevens, stelt u koppelingen in tussen [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en Sales-entiteitrecords. U stelt bijvoorbeeld een koppeling in tussen een bepaalde klant in [!INCLUDE[d365fin](includes/d365fin_md.md)] en een bijbehorend account in Sales.

De volgende tabel bevat de [!INCLUDE[d365fin](includes/d365fin_md.md)]-recordtypen (tabellen) en de corresponderende Sales-entiteiten die out-of-the-box kunnen worden gesynchroniseerd.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Verkoop|Synchronisatierichting|Standaardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Verkoper/Inkoper|Gebruiker|Sales -> Business Central|Sales-contactfilter: **Status** is **Nee**, **Gebruiker licentie** is **Ja**, Modus Integratiegebruiker is **Nee**|
|Klant|Rekening|Business Central -> Sales en Sales -> Business Central|Sales-accountfilter: **Relatietype** is **Klant** en **Status** is **Actief**.|
|Contactpersoon|Contactpersoon|Business Central -> Sales en Sales -> Business Central|Business Central-contactfilter: **Type** is **Persoon** en de contactpersoon is toegewezen aan een bedrijf. Sales-contactfilter: de contactpersoon is toegewezen aan een bedrijf en het bovenliggende klanttype is **Account**.|
|Valuta|Transactievaluta|Business Central -> Sales| |
|Eenheid|Eenhedengroep|Business Central -> Sales| |
|Artikel|Product|Business Central -> Sales en Sales -> Business Central|Sales-contactfilter: **Producttype** is **Verkoopvoorraad**|
|Bron|Product|Business Central -> Sales en Sales -> Business Central|Sales-contactfilter: **Producttype** is **Services**|
|Klantenprijsgroep|Prijslijst|Business Central -> Sales| |
|Verkoopprijs|Productprijslijst|Business Central -> Sales|Business Central-contactfilter: **Verkoopcode** is niet leeg, **Verkoopsoort** is **Klantenprijsgroep**|
|Opportunity|Opportunity|Business Central -> Sales en Sales -> Business Central| |
|Verkoopfactuur|Factureren|Business Central -> Sales| |
|Verkoopfactuurregel|Factuurproduct|Business Central -> Sales| |

De Sales-entiteiten en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen worden gedefinieerd door tabeltoewijzingsitems in tabel 5335, **Toewijzing van integratietabel**. U kunt de toewijzingen weergeven en filters instellen vanaf pagina 5335, **Toewijzingen van integratietabel**. De toewijzing tussen de velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en de velden in Sales-entiteiten wordt bepaald door veldtoewijzingsposten in tabel 5336, **Toewijzing van integratietabel** en met aanvullende toewijzingslogica.

### <a name="field-mapping-for-the-sales-account-option"></a>Veldtoewijzing voor de optie Omzetrekening
Drie tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn toegewezen aan de optievelden van de entiteit **Rekening**.   

De records in de tabel die niet zijn gekoppeld aan de opties die bestaan in Sales, worden tijdens synchronisatie overgeslagen. Dit houdt in dat het veld **Optie** leeg is in Sales.

De volgende tabel bevat toewijzingen van Business Central-tabellen voor het veld **Optie** in de **Rekening**-entiteit.

|Tafel|Optieveld in de rekeningentiteit in Sales|
|----------------------|-------------------------------------------|
|Betalingsvoorwaarden|Betalingsvoorwaarden|
|Verzendwijze|Adres 1: vrachtvoorwaarden|
|Expediteurs|Adres 1: verzendmethode|

### <a name="synchronization-rules"></a>Synchronisatieregels
De volgende tabel beschrijft regels die de synchronisatie tussen Business Central-tabellen en Sales-entiteiten bepalen.

> [!NOTE]  
> Wijzigingen in gegevens in Sales die door het Sales-verbindingsaccount worden uitgevoerd, worden genegeerd. De wijzigingen worden niet gesynchroniseerd. Daarom is het raadzaam dat u geen wijzigingen in gegevens aanbrengt met de Sales-verbindingsaccount.

|Tafel|Regel|
|-----|----|
|Klanten|Voordat een klant met een rekening kan worden gesynchroniseerd, moet de verkoper die aan de klant is toegewezen, aan een gebruiker worden gekoppeld in Sales. Daarom, wanneer u de Dynamics 365 for Sales-synchronisatietaak KLANTEN uitvoert en instelt om nieuwe records te maken, moet u ervoor zorgen dat u verkopers synchroniseert met Sales-gebruikers voordat u klanten met Sales-accounts synchroniseert. <br /> <br />De Dynamics 365 for Sales-synchronisatietaak KLANTEN synchroniseert alleen Sales-accounts die het relatietype Klant hebben.|
|Contacten|Alleen contactpersonen in Sales die zijn gekoppeld aan een account, worden gemaakt in Business Central. De waarde van Verkoperscode definieert de eigenaar van de gekoppelde entiteit in Sales.|
|Valuta's|Valuta's worden aan transactievaluta's in Sales gekoppeld op basis van ISO-codes. Alleen valuta's die een standaard-ISO-code hebben, worden gekoppeld en gesynchroniseerd met transactievaluta's.|
|Eenheden|Maateenheden worden gesynchroniseerd met eenheidsgroepen in Sales. Er kan slechts één eenheid worden gedefinieerd in de eenhedengroep.|
|Artikelen|Wanneer artikelen worden gesynchroniseerd met Sales-producten, maakt Business Central automatisch een prijslijst in Sales. Als u synchronisatiefouten wilt voorkomen, moet u deze prijslijst niet handmatig wijzigen.|
|Verkopers|Verkopers worden gekoppeld aan systeemgebruikers in Sales. De gebruiker moet zijn ingeschakeld en een licentie hebben en moet niet de integratiegebruiker zijn. Dit is de eerste tabel die moet worden gesynchroniseerd, omdat deze wordt gebruikt in klanten, contactpersonen, opportunity's en verkoopfacturen.|
|Resources|Resources worden gesynchroniseerd met Sales-producten van het producttype Service.|
|Klantenprijsgroepen|Klantenprijsgroepen worden gesynchroniseerd met Sales-prijslijsten.|
|Verkoopprijzen|Sales-prijzen die het verkoopsoort Klantenprijsgroep hebben en waarvoor een verkoopcode is gedefinieerd, worden gesynchroniseerd met Sales-prijslijstregels|
|Opportunity's|Opportunity's worden gesynchroniseerd met Sales-opportunity's. De waarde van Verkoperscode definieert de eigenaar van de gekoppelde entiteit in Sales.|
|Geboekte verkoopfacturen|Geboekte verkoopfacturen worden gesynchroniseerd met verkoopfacturen. Voordat een factuur kan worden gesynchroniseerd, is het beter om alle andere entiteiten die deel kunnen nemen aan de factuur, te synchroniseren van verkopers naar prijslijsten. De waarde van Verkoperscode op de factuurkop definieert de eigenaar van de gekoppelde entiteit in Sales.|

## <a name="setting-up-the-connection"></a>De verbinding instellen
Vanaf de startpagina kunt u de begeleide instelling **Instellingen Microsoft Dynamics 365-verbinding** starten om de verbinding tot stand te brengen. Als dat is uitgevoerd, hebt u een naadloze koppeling van Sales-records met [!INCLUDE[d365fin](includes/d365fin_md.md)]-records.  

> [!NOTE]  
>   Hierna wordt de begeleide instelling toegelicht, maar u kunt dezelfde stappen ook handmatig uitvoeren in het venster **Sales-verbinding instellen**.

In de begeleide instelling kunt u kiezen welke gegevens tussen de twee services moeten worden gesynchroniseerd. U kunt ook opgeven dat u uw bestaande Sales-oplossing wilt importeren. In dat geval moet u een beheeraccount opgeven.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>De gebruikersaccount voor het importeren van de oplossing instellen
Om een bestaande Sales-oplossing te importeren maakt de begeleide instelling gebruik van een beheeraccount. Dit account moet een geldige gebruiker in Sales zijn met de volgende beveiligingsrollen:

* Systeembeheerder  
* Oplossingsaanpasser  

Zie voor meer informatie [Gebruikers maken in Microsoft Dynamics 365 (online) en beveiligingsrollen aan hen toewijzen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) en [Gebruikers en machtigingen beheren](ui-how-users-permissions.md).  

Deze account wordt alleen gebruikt tijdens het instellen. Nadat de oplossing is geïmporteerd [!INCLUDE[d365fin](includes/d365fin_md.md)], is de account niet meer nodig.

### <a name="setting-up-the-user-account-for-synchronization"></a>De gebruikersaccount instellen voor synchronisatie
De integratie is gebaseerd op een gedeelde gebruikersaccount. In uw Office 365-abonnement moet u een specifieke gebruiker maken die voor synchronisatie tussen de twee services wordt gebruikt. Dit account moet al een geldige gebruiker in Sales zijn, maar u hoeft geen beveiligingsrollen aan het account toe te wijzen, omdat de begeleide instelling dit voor u doet. U moet deze gebruikersaccount een of meerdere malen opgeven in de begeleide instelling, afhankelijk van hoeveel synchronisatie u wilt inschakelen. Zie voor meer informatie [Gebruikers maken in Microsoft Dynamics 365 (online) en beveiligingsrollen aan hen toewijzen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Als u ervoor kiest *artikelbeschikbaarheid* in te schakelen, moet de account van de integratiegebruiker een webservicetoegangssleutel hebben. Deze instelling omvat twee stappen: in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-pagina voor deze gebruikersaccount moet u op de knop **Sleutel van webservice wijzigen** klikken en in de begeleide instelling voor de Sales-verbinding moet u die gebruiker opgeven als de gebruiker van de OData-webservice.

Als u ervoor kiest *verkooporderintegratie* in te schakelen, moet u een gebruiker opgeven die de synchronisatie verwerkt: de integratiegebruiker of een andere gebruikersaccount.

### <a name="coupling-records"></a>Records koppelen
In de begeleide instelling kunt u kiezen dat tussen de twee services moeten worden gesynchroniseerd. Maar later kunt u ook synchronisatie voor bepaalde soorten gegevens instellen. Dit wordt aangeduid als *koppelen* en in deze sectie vindt u aanbevelingen voor waar u rekening mee moet houden.

Als u bijvoorbeeld Sales-accounts wilt zien als klanten in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de twee soorten records koppelen. Het is niet ingewikkeld: open het venster **Klantenoverzicht** in [!INCLUDE[d365fin](includes/d365fin_md.md)] en zoek in het lint de actie om deze gegevens met Sales te koppelen. Vervolgens geeft u op welke [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten overeenkomen met welke accounts in Sales.

In bepaalde gebieden koppelt de functie waar u gebruik van maakt bepaalde gegevenssets vóór andere gegevenssets, zoals getoond in de volgende lijst:

* Klanten en accounts  
  * Koppel verkopers eerst aan Sales-gebruikers  
* Artikelen en resources  
  * Koppel eenheden eerst aan eenhedengroepen in Sales  
* Artikelen en resourceprijzen  
  * Koppel klantenprijsgroepen eerst aan Sales-prijzen  

> [!NOTE]  
>   Als u prijzen in een vreemde valuta gebruikt, moet u ervoor zorgen dat u valuta's koppelt aan transactievaluta in Sales.

Verkooporders in Sales zijn afhankelijk van aanvullende informatie zoals klanten, eenheden, valuta, klantenprijsgroepen, artikelen en/of resources. Om de integratie met verkooporders naadloos te laten werken, moet u eerst klanten, eenheden, valuta's, klantprijsgroepen, artikelen en/of resources koppelen.

### <a name="synchronizing-records-fully"></a>Records volledig synchroniseren
Aan het eind van de begeleide instelling kunt u de actie **Volledige synchronisatie uitvoeren** kiezen om alle records in [!INCLUDE[d365fin](includes/d365fin_md.md)] te synchroniseren met alle gerelateerde records in de verbonden Sales-oplossing. Kies in het venster **Controle van volledige CRM-synchronisatie** de actie **Starten**. De synchronisatie begint dan taken uit te voeren volgens de afhankelijkheden. Valutarecords worden bijvoorbeeld gesynchroniseerd vóór klantenrecords. De volledige synchronisatie kan lange tijd duren en wordt daarom uitgevoerd in de achtergrond, zodat u verder kunt werken in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Als u de voortgang van afzonderlijke taken in een volledige synchronisatie wilt controleren, zoomt u in op een van de velden **Status van taakwachtrijpost**, **Naar projectstatus van integratietabel** of **Van projectstatus van integratietabel** in het venster **Controle van volledige CRM-synchronisatie** in.

Vanuit het venster **Instellingen Microsoft Dynamics 365-verbinding** kunt u informatie over de volledige synchronisatie op ieder gewenst moment oproepen. Van hieruit kunt u ook het venster **Toewijzingen van integratietabellen** openen, waarin u details van de tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] en in de te synchroniseren Sales-oplossing kunt zien.

## <a name="handling-special-sales-order-data"></a>Speciale verkoopordergegevens verwerken
Verkooporders in Sales worden automatisch overgebracht naar [!INCLUDE[d365fin](includes/d365fin_md.md)] als u het selectievakje **Automatisch verkooporders maken** inschakelt in het venster **Instellingen Microsoft Dynamics 365-verbinding**. Voor deze verkooporders wordt het veld **Naam** op de oorspronkelijke order overgebracht en toegewezen aan het veld **Extern documentnummer** op de verkooporder op [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dit werkt ook als de oorspronkelijke verkooporder inschrijfproducten bevat met artikelen of resources die niet in een van beide producten zijn geregistreerd. In dat geval vult u de velden **Inschrijfproductsoort** en **Inschrijfproductnummer** in in het venster **Instellingen van verkoop en tegoeden**, zodat deze niet-geregistreerde productverkopen worden gekoppeld aan een specifiek artikel-/resourcenummer voor financiële analyse.

Als de artikelomschrijving op de oorspronkelijke verkooporder erg lang is, wordt een extra verkooporderregel van het type Opmerking gemaakt zodat de volledige tekst wordt opgenomen in de verkooporder in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Zie ook
[Relatiebeheer](marketing-relationship-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Uw organisatie en gebruikers onboarden in Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

