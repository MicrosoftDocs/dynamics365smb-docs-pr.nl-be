---
title: De extensie C5-gegevensmigratie gebruiken | Microsoft Docs
description: Gebruik deze extensie om klanten, leveranciers, artikelen en grootboekrekeningen te migreren van Microsoft Dynamics C5 2012 naar Business Central.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: c8eba304746125e9262ebfff95cfd2379eec08c8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311344"
---
# <a name="the-c5-data-migration-extension"></a>De extensie C5-gegevensmigratie
Deze extensie maakt het eenvoudidiger om klanten, leveranciers, artikelen en uw grootboekrekeningen van Microsoft Dynamics C5 2012 te migreren naar [!INCLUDE[d365fin](includes/d365fin_md.md)]. U kunt historische posten voor grootboekrekeningen ook migreren.

> [!Note]
> Het bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)] mag geen gegevens bevatten. Bovendien mag u, nadat u een migratie start, geen klanten, leveranciers, artikelen of rekeningen maken totdat de migratie is voltooid.

## <a name="what-data-is-migrated"></a>Welke gegevens worden gemigreerd?
De volgende gegevens worden voor elke entiteit gemigreerd:

**Klanten**
* Contacten  
* Vestiging
* Land
* Klantdimensies (afdeling, centrum, doel)
* Verzendwijze
* Verkoper
* Betalingsvoorwaarden
* Betalingswijze
* Klantenprijsgroep
* Klantenfactuurkorting

Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:

* Klantboekingsinstelling
* Dagboekbatch
* Open transacties (klantenposten)

**Leveranc.**
* Contacten
* Vestiging
* Land
* Leveranciersdimensies (afdeling, centrum, doel)
* Factuurkorting
* Verzendwijze
* Inkoper
* Betalingsvoorwaarden
* Betalingswijze
* Leveranciersfactuurkorting

Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:

* Leveranciersboekingsinstelling
* Dagboekbatch
* Open transacties (leveranciersposten)

**Artikelen**
* Vestiging
* Land
* Artikeldimensies (afdeling, centrum, doel)
* Verkoopregelkortingen
* Klantenkortingsgroepen
* Artikelkortingsgroepen
* Verkoopprijs
* Tariefnummer
* Maateenheden
* Artikeltraceringscode
* Klantenprijsgroep
* Assemblagestuklijsten

Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:

* Voorraadboekingsinstelling
* Algemene boekingsinstelling
* Artikeldagboekbatch
* Open transacties (artikelposten)

> [!Note]
> Als er open transacties zijn die vreemde valuta's gebruiken, wordt de wisselkoers voor deze valuta ook gemigreerd. Andere wisselkoersen worden niet gemigreerd.

**Rekeningschema**  
* Standaarddimensies: afdeling, kostenplaats, doel  
* Historische G/L-transacties  

> [!Note]
> Historische G/L-transacties worden iets anders behandeld. Wanneer u gegevens migreert, stelt u de parameter **Huidige periode** in. Deze parameter bepaalt hoe G/L-transacties worden verwerkt. Transacties na deze datum worden afzonderlijk gemigreerd. Transacties vóór deze datum worden bijeengevoegd per rekening en als één bedrag gemigreerd. Stel dat er transacties zijn in 2015, 2016, 2017 en 2018, en dat u 1 januari 2017 opgeeft in het veld Huidige periode. Voor elke rekening worden bedragen voor transacties op of vóór 31 december 2106 in één dagboekregel gecombineerd voor elke grootboekrekening. Alle transacties na deze datum worden afzonderlijk gemigreerd.

## <a name="file-size-requirements"></a>Vereisten voor bestandsgrootte
Het grootste bestand dat u kunt uploaden naar [!INCLUDE[d365fin](includes/d365fin_md.md)] is 150 MB. Als het bestand dat u uit C5 exporteert, groter is, overweeg dan gegevens in meerdere bestanden te migreren. Exporteer bijvoorbeeld een of twee typen entiteiten uit C5, zoals klanten en leveranciers, naar een bestand en exporteer artikelen naar een ander bestand, enzovoort. U kunt afzonderlijke bestanden importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-migrate-data"></a>Gegevens te migreren
Er zijn slechts enkele stappen nodig om gegevens vanuit C5 te exporteren en deze te importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. Gebruik in C5 de functie **Database exporteren** om de gegevens te exporteren. Verzend vervolgens de exportmap naar een gecomprimeerde (gezipte) map.  
2. Kies in [!INCLUDE[d365fin](includes/d365fin_md.md)] het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gegevensmigratie** in en kies vervolgens **Gegevensmigratie**.  
3. Voer de stappen uit in het handleiding met begeleide instellingen. Zorg dat u **Importeren vanuit Microsoft Dynamics C5 2012** als gegevensbron kiest.  

## <a name="viewing-the-status-of-the-migration"></a>De status van de migratie weergeven
Gebruik de pagina **Gegevensmigratieoverzicht** om het resultaat van de migratie bekijken. De pagina bevat gegevens zoals het aantal entiteiten dat de migratie omvat, de status van de migratie, het aantal items dat is gemigreerd en of dat is gelukt. De pagina toont ook het aantal fouten, en stelt u in staat te onderzoeken wat er mis is gegaan. Ook bent u zo in staat om, indien mogelijk, gemakkelijk naar de entiteit gaan en de problemen op te lossen. Zie de volgende sectie in dit onderwerp voor meer informatie.  

> [!Note]
> Terwijl u op de resultaten van de migratie wacht, moet u de pagina vernieuwen om de resultaten weer te geven.

## <a name="how-to-avoid-double-posting"></a>Dubbele boekingen voorkomen
Om dubbele boekingen te helpen voorkomen worden de volgende tegenrekeningen gebruikt voor open transacties:  

* Voor leveranciers wordt de leveranciersrekening uit de leveranciersboekingsgroep gebruikt.  
* Voor klanten wordt de klantenrekening uit de klantenboekingsgroep gebruikt.  
* Voor artikelen wordt een algemene boekingsinstelling gemaakt waarbij de correctierekening de rekening is die is opgegeven als de voorraadrekening in de voorraadboekingsinstelling.  

## <a name="correcting-errors"></a>Fouten corrigeren
Als er iets misgaat en zich een fout voordoet, wordt in het veld **Status** **Voltooid met fouten** weergegeven en in het veld **Aantal fouten** aangegeven hoeveel fouten er zijn. Als u een lijst met fouten wilt zien, kunt u de pagina met de **gegevensmigratiefouten** openen door het volgende te selecteren:  

* Het aantal in het veld **Aantal fouten** voor de entiteit.  
* Op de entiteit en vervolgens op de actie **Fouten weergeven** te klikken.  

Op de pagina **Fouten met gegevensmigratie** kunt u een foutbericht kiezen om een fout op te lossen en vervolgens **Record bewerken** kiezen om de gemigreerde gegevens voor de entiteit weer te geven. Als u meerdere fouten moet corrigeren, kunt u **Fouten bulksgewijs corrigeren** kiezen om de entiteiten in een lijst te bewerken. U moet echter nog afzonderlijke records openen als de fout is veroorzaakt door een gerelateerd item. Een leverancier wordt bijvoorbeeld niet gemigreerd als een e-mailadres van een van de contactpersonen een ongeldige indeling heeft.

Nadat u een of meer fouten hebt opgelost, kunt u **Migreren** kiezen om alleen de entiteiten te migreren die u hebt hersteld, zonder dat u geheel op nieuw moet beginnen met de migratie.  

> [!Tip]
> Als u meer dan één fout hebt verholpen, kunt u de functie **Meer selecteren** gebruiken om meerdere regels te selecteren om te migreren. Of u kunt fouten die niet noodzakelijkerwijs moeten worden opgelost, selecteren en vervolgens **Selecties overslaan** kiezen.

> [!Note]
> Als u artikelen hebt die op een stuklijst zijn opgenomen, moet u mogelijk meer dan eens migreren als het oorspronkelijke artikel niet is gemaakt vóór de varianten die ernaar verwijzen.. Als een artikelvariant eerst is gemaakt, kan de verwijzing naar het oorspronkelijke artikel een foutbericht produceren.  

## <a name="verifying-data-after-migrating"></a>Het verifiëren van gegevens na de migratie
Eén manier om te controleren of uw gegevens correct zijn gemigreerd is te kijken naar de volgende pagina's in C5 en [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]| Te gebruiken batchverwerking |
|-----|-----|-----|
|Klantenposten| Financiële dagboeken| CUSTMIGR |
|Leveranciersposten| Financiële dagboeken| VENDMIGR|
|Artikelposten| Artikeldagboeken| ITEMMIGR |
|Grootboekposten| Financiële dagboeken| GLACMIGR |

## <a name="stopping-data-migration"></a>De gegevensmigratie beëindigen
U kunt de migratie van gegevens stoppen door **Alle migraties stoppen** te kiezen. Als u dat doet, worden alle wachtende migraties ook beëindigd.

## <a name="see-also"></a>Zie ook
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Aan de slag](product-get-started.md)
