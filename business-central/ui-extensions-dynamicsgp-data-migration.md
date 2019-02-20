---
title: Gegevens uit Dynamics GP migreren met de extensie Gegevensmigratie | Microsoft Docs
description: Gebruik de Dynamics GP-extensie Gegevensmigratie om klanten, leveranciers, voorraadartikelen, grootboekrekeningen, openstaande schulden en openstaande tegoeden te migreren van Dynamics GP naar Business Central.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 34a6789780fb3d55c0a97b29408dca659992f781
ms.openlocfilehash: 1441e15785b159f7a8c13ee59c8ebea4c32512dc
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2019

---
# <a name="the-dynamics-gp-data-migration-extension"></a>De Dynamics GP-extensie Gegevensmigratie 
Deze extensie maakt het gemakkelijk transacties van klanten, leveranciers, voorraadartikelen, grootboekrekeningen, openstaande schulden en openstaande tegoeden te migreren van Dynamics GP naar [!INCLUDE[prodshort](includes/prodshort.md)]. Als uw bedrijf momenteel Dynamics GP gebruikt, kunt u de relevante records exporteren en vervolgens een begeleide instelling openen om de gegevens toe te voegen aan [!INCLUDE[prodshort](includes/prodshort.md)]. De migratie-extensie werkt voor alle ondersteunde versies van Microsoft Dynamics GP. Zie [Gegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md) voor meer informatie.

## <a name="exporting-data-from-dynamics-gp"></a>Gegevens exporteren uit Dynamics GP
U moet gegevens van sommige of alle bestaande klanten, leveranciers, voorraadartikelen en grootboekrekeningen hebben geëxporteerd met functionaliteit voor gegevensexport binnen Dynamics GP. Wanneer u gegevens selecteert, kunt u de volgende typen selecteren:

* Rekening  
* Klant  
* Artikel  
* Leverancier  

Wanneer het exportbestand is gemaakt, hebt u een zip-bestand dat meerdere txt-bestanden bevat die worden bepaald door wat u tijdens het exporteren van de gegevens hebt geselecteerd.  Er zijn ook extra txt-bestanden gegenereerd die ondersteunende gegevens bevatten die nodig zijn voor de instelling in uw nieuwe [!INCLUDE[prodshort](includes/prodshort.md)]-bedrijf.

De extensie Dynamics GP Data Migration wijst automatisch de geëxporteerde gegevens toe, zodat de gegevens snel beschikbaar zijn in uw nieuwe [!INCLUDE[prodshort](includes/prodshort.md)]-bedrijf.

## <a name="whats-new-in-the-october-2018-release"></a>Nieuw in de release van oktober 2018

In deze versie hebben we de hoeveelheid gegevens vergroot die naar [!INCLUDE[prodshort](includes/prodshort.md)] worden overgebracht uit Dynamics GP.

In de migratiewizard kunt u nu kiezen hoe u het Dynamics GP-rekeningschema wilt migreren. U kunt het bestaande rekeningschema migreren of een nieuw rekeningschema maken op basis van het bestaande rekeningschema.  

Als u ervoor kiest het bestaande rekeningschema te gebruiken, worden de rekeningen ingesteld als hoofdrekeningsegment vanuit Dynamics GP en worden de extra segmenten ingesteld als dimensies in [!INCLUDE[prodshort](includes/prodshort.md)].  

Als u een nieuw rekeningschema maakt, krijgt u een extra pagina met rekeninggegevens in de wizard, zodat u de werkmap kunt downloaden, de relevante wijzigingen kunt aanbrengen en de werkmap vervolgens weer kunt importeren om uw rekeningen te wijzigen.  

U moet de Excel-werkmap downloaden en een nieuw rekeningnummer toewijzen aan elk rekeningnummer in het Excel-werkblad. Elke rekening moet een eigen nummer hebben anders leidt de migratie tot een fout. Wanneer u de toewijzing hebt voltooid, kunt u de migratiewizard vervolgen door de Excel-werkmap te importeren die u zojuist hebt bijgewerkt. De wizard controleert of elke rij een uniek rekeningnummer heeft en dat geen rijen een leeg rekeningnummer bevatten.  

Met de wijziging in de toewijzing van rekeningschemaopties ziet u ook een wijziging van het type gegevens dat voor de rekeningnummers wordt overgebracht in het grootboek.  

- Als u ervoor kiest de bestaande rekeningnummers te gebruiken, brengen we het beginsaldo van het hoofdsegment (nieuw rekeningnummer) over als optelling van het hoofdrekeningnummer op het moment van de migratie.  
- Als u ervoor kiest om nieuwe rekeningnummers te maken, brengen we samenvattingsinformatie voor het equivalent van twee boekjaren over op basis van de boekperioden die u hebt ingesteld in Dynamics GP.

In eerdere versies van [!INCLUDE[prodshort](includes/prodshort.md)] migreerde de wizard een overzichtstransactie voor het huidige klant-/leverancierssaldo in Dynamics GP. Nu brengen we de gedetailleerde openstaande transacties over voor klanten en leveranciers op het moment van de migratie. Wat betekent dit? Als uw klant nog 3 openstaande transacties heeft geregistreerd in de module Klanten, brengt de wizard deze transacties over in [!INCLUDE[prodshort](includes/prodshort.md)], met het openstaande bedrag als het documentbedrag. Dit geldt ook voor de module Klanten voor leveranciers.  

Voorraadartikelen worden geïmporteerd met de kostenwaarderingsmethode die is geselecteerd toen de instellingswizard van het bedrijf is uitgevoerd. Aan serviceartikelen wordt automatisch de FIFO-waarderingsmethode toegewezen. Momenteel brengen we de artikelen in voorraad op het moment van de migratie over.  Dit aantal wordt naar de lege vestiging overgebracht.  

De laatste optie die u in de wizard Gegevensmigratie voor Dynamics GP ziet, is de mogelijkheid om uw boekingsoptie op te geven. Met deze instelling wordt opgegeven of u automatisch alle transacties naar de grootboeken wilt boeken zodra de migratie de gegevens naar [!INCLUDE[prodshort](includes/prodshort.md)] verplaatst, of dat u handmatig wilt boeken, zodat alle transacties zich in batches bevinden op de pagina Grootboek, zodat u de informatie kunt controleren voordat u boekt. Deze optie wordt weergegeven op de optiepagina Rekeningschema.


## <a name="see-also"></a>Zie ook
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[[!INCLUDE[prodshort](includes/prodshort.md)] aanpassen met behulp van extensies](ui-extensions.md)  

