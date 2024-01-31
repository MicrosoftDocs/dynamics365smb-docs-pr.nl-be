---
title: Synchronisatie en gegevensintegratie | Microsoft Docs
description: Synchronisatie kopieert gegevens tussen Microsoft Dataverse-tabellen en Business Central-records en houdt de gegevens in beide systemen up-to-date.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
ms.service: dynamics-365-business-central
---

# Gegevens synchroniseren in Business Central en Microsoft Dataverse

Wanneer u [!INCLUDE[prod_short](includes/cds_long_md.md)] met [!INCLUDE[prod_short](includes/prod_short.md)] integreert, kunt u bepalen of gegevens in geselecteerde velden van [!INCLUDE[prod_short](includes/prod_short.md)]-records (zoals klanten, contactpersonen en verkopers) worden gesynchroniseerd met equivalente rijen in [!INCLUDE[prod_short](includes/cds_long_md.md)] (zoals rekeningen, contacten en gebruikers). Afhankelijk van het type rij kunt u gegevens vanuit [!INCLUDE[prod_short](includes/cds_long_md.md)] synchroniseren met [!INCLUDE[prod_short](includes/prod_short.md)] of andersom. Zie voor meer informatie [Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synchronisatie gebruikt de volgende elementen:

* Toewijzingen van integratietabellen
* Toewijzingen van integratievelden
* Synchronisatieregels
* Gekoppelde records

Wanneer synchronisatie is ingesteld, kunt u [!INCLUDE[prod_short](includes/prod_short.md)]-records koppelen aan [!INCLUDE[prod_short](includes/cds_long_md.md)]-rijen om gegevens ervan te synchroniseren. U kunt een synchronisatie handmatig starten of op basis van een planning. In de volgende tabel vindt u een overzicht van de manieren waarop u kunt synchroniseren.  

|  Soort  |  Methode  |  Zie  |  
|--------|----------|-------|  
|Handmatige synchronisatie|Synchroniseren op rijbasis.<br /><br /> U kunt afzonderlijke records in [!INCLUDE[prod_short](includes/prod_short.md)], zoals een klant, synchroniseren met een corresponderende [!INCLUDE[prod_short](includes/cds_long_md.md)]-rij, zoals een account. Zo werken gebruikers meestal met [!INCLUDE[prod_short](includes/cds_long_md.md)]-gegevens in [!INCLUDE[prod_short](includes/prod_short.md)].|[Records handmatig koppelen en synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synchroniseren op basis van tabeltoewijzing.<br /><br /> U kunt alle records in een [!INCLUDE[prod_short](includes/prod_short.md)]-tabel synchroniseren met een [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabel.|[Afzonderlijke tabeltoewijzingen synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Alle gewijzigde records voor alle tabeltoewijzingen synchroniseren.<br /><br /> U kunt alle records synchroniseren die zijn gewijzigd in [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen sinds de laatste synchronisatie.|[Alle gewijzigde records synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Volledige synchronisatie van alle gegevens van alle tabelkoppelingen.<br /><br /> U kunt alle gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen en [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellen synchroniseren die zijn toegewezen en nieuwe records of rijen in de doeloplossing maken voor ongekoppelde records in de bronoplossing.<br /><br /> Volledige synchronisatie synchroniseert alle gegevens en negeert koppeling. Meestal voert u een volledige synchronisatie uit wanneer u de integratie instelt en slechts één van de oplossingen gegevens bevat. Een volledige synchronisatie kan ook nuttig zijn in een demonstratieomgeving.|[Een volledige synchronisatie uitvoeren](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Geplande synchronisatie|Alle wijzigingen synchroniseren in gegevens voor alle tabeltoewijzingen.<br /><br /> U kunt [!INCLUDE[prod_short](includes/prod_short.md)] met [!INCLUDE[prod_short](includes/cds_long_md.md)] synchroniseren met geplande intervallen door taken in te stellen in de taakwachtrij.|[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> De synchronisatie tussen [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)] is gebaseerd op de geplande uitvoering van taakwachtrij-items en garandeert geen realtime gegevensconsistentie tussen twee services. Voor realtime gegevensconsistentie moet u [Virtuele Business Central- tabellen](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) of Business Central-API's verkennen.   

## Standaardtabeltoewijzing voor synchronisatie

Tabellen in [!INCLUDE[prod_short](includes/cds_long_md.md)], zoals accounts, zijn geïntegreerd met equivalente soorten tabellen in [!INCLUDE[prod_short](includes/prod_short.md)], zoals klanten. Als u wilt werken met [!INCLUDE[prod_short](includes/cds_long_md.md)]-gegevens, stelt u koppelingen in tussen tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)].

In de volgende tabel staat de standaardtoewijzing tussen tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] en die [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> U kunt configuratiewijzigingen die zijn aangebracht in integratietabel- en veldtoewijzingen terugzetten naar hun standaardinstellingen door de toewijzingen te selecteren en vervolgens **Standaardsynchronisatie-instellingen gebruiken** te kiezen.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synchronisatierichting | Standaardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Verkoper/Inkoper | Gebruiker | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-contactfilter: **Status** is **Nee**, **Gebruiker licentie** is **Ja**, Modus Integratiegebruiker is **Nee** |
| Klant | Rekening | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-rekeningfilter: **Relatietype** is **Klant** en **Status** is **Actief**. [!INCLUDE[prod_short](includes/prod_short.md)]-filter: **Geblokkeerd** is leeg (klant is niet geblokkeerd). |
| Leverancier | Rekening | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-rekeningfilter: **Relatietype** is **Leverancier** en **Status** is **Actief**. [!INCLUDE[prod_short](includes/prod_short.md)]-filter: **Geblokkeerd** is leeg (leverancier is niet geblokkeerd). |
| Contactpersoon | Contactpersoon | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-contactfilter: **Type** is **Persoon** en de contactpersoon is toegewezen aan een bedrijf. [!INCLUDE[prod_short](includes/cds_long_md.md)]-contactfilter: de contactpersoon is toegewezen aan een bedrijf en het bovenliggende klanttype is **Klant**. |
| Valuta | Transactievaluta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> De **Dataverse**-acties zijn niet beschikbaar op pagina's, bijvoorbeeld de pagina Klantenkaart, voor records die het tabelfilter voor de integratietabeltoewijzing niet respecteren.

### Tip voor beheerders: tabeltoewijzingen weergeven

U kunt de koppeling tussen de tabellen in [!INCLUDE[prod_short](includes/cds_long_md.md)] en de tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] bekijken op de pagina **Toewijzingen van integratietabellen**, waar u kunt ook filters kunt toepassen. U definieert de toewijzing tussen de velden in [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen en de kolommen in [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellen op de pagina **Toewijzing van integratieveld**, waar u aanvullende toewijzingslogica kunt toevoegen. Dat kan bijvoorbeeld handig zijn als u problemen met synchronisatie moet oplossen.

## Virtuele tabellen gebruiken om meer gegevens te verkrijgen

Wanneer u uw integratie instelt, kunt u virtuele tabellen gebruiken om meer gegevens beschikbaar te maken in [!INCLUDE[prod_short](includes/cds_long_md.md)], zonder hulp van een ontwikkelaar.

Een virtuele tabel is een aangepaste tabel die kolommen en rijen bevat met gegevens uit een externe gegevensbron, zoals [!INCLUDE [prod_short](includes/prod_short.md)]. De kolommen en rijen in een virtuele tabel zien eruit als een gewone tabel, maar de gegevens worden niet opgeslagen in een fysieke tabel in de [!INCLUDE[prod_short](includes/cds_long_md.md)]-database. In plaats daarvan worden de gegevens tijdens runtime opgehaald.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] bevat objecten die ook wel virtuele tabellen worden genoemd. Deze tabelobjecten zijn niet gerelateerd aan de virtuele tabellen die u gebruikt met [!INCLUDE[prod_short](includes/cds_long_md.md)].

Ga naar de volgende artikelen voor meer informatie over virtuele tabellen:

* [Virtuele tabellen maken en bewerken die gegevens uit een externe gegevensbron bevatten](/power-apps/maker/data-platform/create-edit-virtual-entities) (Power Apps-documentatie)
* [Business Central virtuele tabel voor Microsoft Dataverse Beheerreferentie](/business-central/dev-itpro/powerplatform/powerplat-admin-reference) ([!INCLUDE [prod_short](includes/prod_short.md)]-documentatie)

Om virtuele tabellen te gebruiken moet u de app **Virtuele Business Central-entiteit** van [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity) installeren. 

Nadat u de app heeft geïnstalleerd, kunt u virtuele tabellen inschakelen vanaf een van de volgende pagina's in [!INCLUDE [prod_short](includes/prod_short.md)]:

* Wanneer u de begeleide instelling **Dataverse-verbinding instellen** uitvoert, kunt u de pagina **Beschikbare virtuele Dataverse-tabellen** gebruiken om meerdere virtuele tabellen te selecteren. Daarna zijn de tabellen beschikbaar in [!INCLUDE[prod_short](includes/cds_long_md.md)] en de PowerApps Maker Portal. 
* Vanaf de pagina's **Dataverse-verbinding instellen**, **Virtuele tabellen** en **Beschikbare virtuele tabellen**.  
* Vanuit de Power App Maker Portal.

## Gegevens van meerdere bedrijven of omgevingen synchroniseren

U kunt gegevens van meerdere [!INCLUDE [prod_short](includes/prod_short.md)]-bedrijven of -omgevingen met een [!INCLUDE[prod_short](includes/cds_long_md.md)]-omgeving synchroniseren. Bij synchronisatiescenario's voor meerdere bedrijven zijn er verschillende zaken waarmee u rekening moet houden.

### Bedrijfs-id's instellen

Wanneer u records synchroniseert, stellen we een bedrijfs-id in voor de [!INCLUDE[prod_short](includes/cds_long_md.md)]-entiteit om duidelijk te maken van welk [!INCLUDE [prod_short](includes/prod_short.md)]-bedrijf de records vandaan komen. Integratietabeltoewijzingen hebben filtervelden voor integratietabellen die rekening houden met de bedrijfs-id. Als u een tabeltoewijzing wilt opnemen in een configuratie met meerdere bedrijven, kiest u op de pagina **Toewijzing van integratietabel** het selectievakje **Synchronisatie van meerdere bedrijven geactiveerd**. De instelling optimaliseert de manier waarop de filtervelden van de integratietabel bedrijfs-id's filteren in een instelling met meerdere bedrijven.

Voor integratietabeltoewijzingen die documenten synchroniseren, zoals orders, offertes en opportunities, geldt dat als u het selectievakje **Synchronisatie van meerdere bedrijven geactiveerd** kiest, de integratie alleen rekening houdt met entiteiten die de bedrijfs-id van het huidige [!INCLUDE [prod_short](includes/prod_short.md)]-bedrijf hebben. Om documenten te synchroniseren, bijvoorbeeld tussen Business Central en Sales, moeten gebruikers in Sales de bedrijfs-id op de documenten opgeven. Anders worden de documenten niet gesynchroniseerd.  

Voor alle andere integratietabeltoewijzingen wordt het filter op bedrijfs-id verwijderd als u het selectievakje **Synchronisatie van meerdere bedrijven geactiveerd** kiest. Bij de synchronisatie wordt rekening gehouden met gerelateerde entiteiten, ongeacht hun bedrijfs-id.

### De synchronisatierichting opgegeven

Als u ondersteuning voor meerdere bedrijven inschakelt voor een integratietabeltoewijzing, raden we u aan de richting van de toewijzing in te stellen op **Van integratie**. Als u de richting instelt op **Naar Integratie** of **Bidirectioneel**, is het een goed idee om **Tabelfilter** en **Filter integratietabel** te gebruiken om te bepalen welke entiteiten met welk bedrijf synchroniseren. Het is ook een goed idee om op overeenkomsten gebaseerde koppeling te gebruiken om te voorkomen dat er dubbele records ontstaan. Ga voor meer informatie over op overeenkomsten gebaseerde koppeling naar [De koppeling op basis van overeenkomsten aanpassen](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### Unieke nummers gebruiken

Als uw nummerreeks niet garandeert dat primaire sleutelwaarden uniek zijn voor elk bedrijf, raden we u aan voorvoegsels te gebruiken. Als u voorvoegsels wilt gaan gebruiken, maakt u een transformatieregel voor de integratieveldtoewijzing. Ga voor meer informatie over transformatieregels naar [Omgaan met verschillen in veldwaarden](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## Zie ook  

[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)   
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
