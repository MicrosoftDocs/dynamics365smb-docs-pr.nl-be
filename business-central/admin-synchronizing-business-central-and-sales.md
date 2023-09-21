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
---

# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Gegevens synchroniseren in Business Central en Microsoft Dataverse

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


## <a name="standard-table-mapping-for-synchronization"></a>Standaardtabeltoewijzingen voor synchronisatie
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

### <a name="tip-for-admins-viewing-table-mappings"></a>Tip voor beheerders: tabeltoewijzingen weergeven
U kunt de koppeling tussen de tabellen in [!INCLUDE[prod_short](includes/cds_long_md.md)] en de tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] bekijken op de pagina **Toewijzingen van integratietabellen**, waar u kunt ook filters kunt toepassen. U definieert de toewijzing tussen de velden in [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen en de kolommen in [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellen op de pagina **Toewijzing van integratieveld**, waar u aanvullende toewijzingslogica kunt toevoegen. Dat kan bijvoorbeeld handig zijn als u problemen met synchronisatie moet oplossen.

## <a name="see-also"></a>Zie ook
[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)   
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
