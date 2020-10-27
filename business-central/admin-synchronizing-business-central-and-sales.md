---
title: Synchronisatie en gegevensintegratie | Microsoft Docs
description: Synchronisatie kopieert gegevens tussen Common Data Service-entiteiten en Business Central-records en houdt de gegevens in beide systemen up-to-date.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9d3f4e86a0da5c26a84ca79b1712f2f240e347a2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922454"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Gegevens synchroniseren in Business Central en Common Data Service

Wanneer u [!INCLUDE[d365fin](includes/cds_long_md.md)] met [!INCLUDE[d365fin](includes/d365fin_md.md)] integreert, kunt u bepalen of gegevens in geselecteerde velden van [!INCLUDE[d365fin](includes/d365fin_md.md)]-records (zoals klanten, contactpersonen en verkopers) worden gesynchroniseerd met equivalente records in [!INCLUDE[d365fin](includes/cds_long_md.md)] (zoals rekeningen, contacten en gebruikers). Afhankelijk van het type record kunt u gegevens vanuit [!INCLUDE[d365fin](includes/cds_long_md.md)] synchroniseren met [!INCLUDE[d365fin](includes/d365fin_md.md)] of andersom. Zie voor meer informatie [Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synchronisatie gebruikt de volgende elementen:

* Toewijzingen van integratietabellen
* Toewijzingen van integratievelden
* Synchronisatieregels
* Gekoppelde records

Wanneer synchronisatie is ingesteld, kunt u [!INCLUDE[d365fin](includes/d365fin_md.md)]-records koppelen aan [!INCLUDE[d365fin](includes/cds_long_md.md)]-records om gegevens ervan te synchroniseren. U kunt een synchronisatie handmatig starten of op basis van een planning. In de volgende tabel vindt u een overzicht van de manieren waarop u records kunt synchroniseren.  

|  Soort  |  Methode  |  Zie  |  
|--------|----------|-------|  
|Handmatige synchronisatie|Synchroniseren op recordbasis.<br /><br /> U kunt afzonderlijke records in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals een klant, synchroniseren met een corresponderende [!INCLUDE[d365fin](includes/cds_long_md.md)]-record, zoals een account. Zo werken gebruikers meestal met [!INCLUDE[d365fin](includes/cds_long_md.md)]-gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Records handmatig koppelen en synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synchroniseren op basis van tabeltoewijzing.<br /><br /> U kunt alle records in een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel synchroniseren met een [!INCLUDE[d365fin](includes/cds_long_md.md)]-entiteit.|[Afzonderlijke tabeltoewijzingen synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Alle gewijzigde records voor alle tabeltoewijzingen synchroniseren.<br /><br /> U kunt alle records synchroniseren die zijn gewijzigd in [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen sinds de laatste synchronisatie.|[Alle gewijzigde records synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Volledige synchronisatie van alle gegevens van alle tabelkoppelingen.<br /><br /> U kunt alle gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen en [!INCLUDE[d365fin](includes/cds_long_md.md)]-entiteiten synchroniseren die zijn toegewezen en nieuwe records in de doeloplossing maken voor ongekoppelde records in de bronoplossing.<br /><br /> Volledige synchronisatie synchroniseert alle gegevens en negeert koppeling. Meestal voert u een volledige synchronisatie uit wanneer u de integratie instelt en slechts één van de oplossingen gegevens bevat. Een volledige synchronisatie kan ook nuttig zijn in een demonstratieomgeving.|[Een volledige synchronisatie uitvoeren](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Geplande synchronisatie|Alle wijzigingen synchroniseren in gegevens voor alle tabeltoewijzingen.<br /><br /> U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[d365fin](includes/cds_long_md.md)] synchroniseren met geplande intervallen door taken in te stellen in de taakwachtrij.|[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Standaardentiteittoewijzingen voor synchronisatie
Entiteiten in [!INCLUDE[d365fin](includes/cds_long_md.md)], zoals accounts, zijn geïntegreerd met equivalente soorten entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals klanten. Als u wilt werken met [!INCLUDE[d365fin](includes/cds_long_md.md)]-gegevens, stelt u koppelingen in tussen entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)].

In de volgende tabel staat de standaardtoewijzing tussen entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)] die [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt.

> [!TIP]
> U kunt configuratiewijzigingen die zijn aangebracht in integratietabel- en veldtoewijzingen terugzetten naar hun standaardinstellingen door de toewijzingen te selecteren en vervolgens **Standaardsynchronisatie-instellingen gebruiken** te kiezen.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)] | Synchronisatierichting | Standaardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Verkoper/Inkoper | Gebruiker | [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)]-contactfilter: **Status** is **Nee** , **Gebruiker licentie** is **Ja** , Modus Integratiegebruiker is **Nee** |
| Klant | Rekening | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)]-rekeningfilter: **Relatietype** is **Klant** en **Status** is **Actief** . [!INCLUDE[d365fin](includes/d365fin_md.md)]-filter: **Geblokkeerd** is leeg (klant is niet geblokkeerd). |
| Leverancier | Rekening | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)]-rekeningfilter: **Relatietype** is **Leverancier** en **Status** is **Actief** . [!INCLUDE[d365fin](includes/d365fin_md.md)]-filter: **Geblokkeerd** is leeg (leverancier is niet geblokkeerd). |
| Contactpersoon | Contactpersoon | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)]-contactfilter: **Type** is **Persoon** en de contactpersoon is toegewezen aan een bedrijf. [!INCLUDE[d365fin](includes/cds_long_md.md)]-contactfilter: de contactpersoon is toegewezen aan een bedrijf en het bovenliggende klanttype is **Account** |
| Valuta | Transactievaluta | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Tip voor beheerders: entiteittoewijzingen weergeven
U kunt de koppeling tussen de entiteiten in [!INCLUDE[d365fin](includes/cds_long_md.md)] en de tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] bekijken op de pagina **Toewijzingen van integratietabellen** , waar u kunt ook filters kunt toepassen. U definieert de toewijzing tussen de velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen en de velden in [!INCLUDE[d365fin](includes/cds_long_md.md)]-entiteiten op de pagina **Toewijzing van integratieveld** , waar u aanvullende toewijzingslogica kunt toevoegen. Dat kan bijvoorbeeld handig zijn als u problemen met synchronisatie moet oplossen.

## <a name="see-also"></a>Zie ook  
[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)   
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
