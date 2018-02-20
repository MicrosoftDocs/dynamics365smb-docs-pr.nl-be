---
title: De extensie C5-gegevensmigratie gebruiken | Microsoft Docs
description: Gebruik deze extensie om klanten, leveranciers, artikelen en grootboekrekeningen te migreren van Microsoft Dynamics C5 2012 naar Financials.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d3b8d3d01ce75da59c1cce873077955776963ce9
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---

# <a name="the-c5-data-migration-extension-for-finance-and-operations-business-edition"></a>De extensie C5-gegevensmigratie voor Finance and Operations, Business edition
Deze extensie maakt het eenvoudidiger om klanten, leveranciers, artikelen en uw grootboekrekeningen van Microsoft Dynamics C5 2012 te migreren naar [!INCLUDE[d365fin](includes/d365fin_md.md)]. U kunt historische posten voor grootboekrekeningen ook migreren.

> [!Note]
> Het bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)] mag geen gegevens bevatten. Bovendien mag u, nadat u een migratie start, geen klanten, leveranciers, artikelen of rekeningen maken totdat de migratie is voltooid.

##<a name="what-data-is-migrated"></a>Welke gegevens worden gemigreerd?
De volgende gegevens worden voor elke entiteit gemigreerd:

**Klanten**
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

Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:

* Voorraadboekingsinstelling
* Algemene boekingsinstelling
* Artikeldagboekbatch
* Open transacties (artikelposten)

> [!Note]
> Als er open transacties zijn die vreemde valuta's gebruiken, wordt de wisselkoers voor deze valuta ook gemigreerd. Andere wisselkoersen worden niet gemigreerd.

## <a name="to-migrate-data"></a>Gegevens te migreren
Er zijn slechts enkele stappen nodig om gegevens vanuit C5 te exporteren en deze te importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. Gebruik in C5 de functie **Database exporteren** om de gegevens te exporteren. Verzend vervolgens de exportmap naar een gecomprimeerde (gezipte) map.  
2. Klik in [!INCLUDE[d365fin](includes/d365fin_md.md)] op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gegevensmigratie** in en kies vervolgens **Gegevensmigratie**.  
3. Voer de stappen uit in het handleiding met begeleide instellingen. Zorg dat u **Importeren vanuit Microsoft Dynamics C5 2012** als gegevensbron kiest.  

> [!Note]
> Bedrijven voegen vaak velden toe om C5 aan te passen aan de behoeften van hun specifieke branche. [!INCLUDE[d365fin](includes/d365fin_md.md)] migreert geen gegevens van aangepaste velden. Ook mislukt de migratie als u meer dan 10 aangepaste velden hebt.

## <a name="viewing-the-status-of-the-migration"></a>De status van de migratie weergeven
Gebruik de pagina **Gegevensmigratieoverzicht** om het resultaat van de migratie bekijken. De pagina bevat gegevens zoals het aantal entiteiten dat de migratie omvat, de status van de migratie, het aantal items dat is gemigreerd en of dat is gelukt. De pagina toont ook het aantal fouten, en stelt u in staat te onderzoeken wat er mis is gegaan. Ook bent u zo in staat om, indien mogelijk, gemakkelijk naar de entiteit gaan en de problemen op te lossen. Zie de volgende sectie in dit onderwerp voor meer informatie.  

> [!Note]
> Terwijl u op de resultaten van de migratie wacht, moet u de pagina vernieuwen om de resultaten weer te geven.

## <a name="correcting-errors"></a>Fouten corrigeren
Als er iets misgaat en zich een fout voordoet, wordt in het veld **Status** **Voltooid met fouten** weergegeven en in het veld **Aantal fouten** aangegeven hoeveel fouten er zijn. Als u een lijst met fouten wilt zien, kunt u de pagina met de **gegevensmigratiefouten** openen door het volgende te selecteren:  

* Het aantal in het veld **Aantal fouten** voor de entiteit.  
* Op de entiteit en vervolgens op de actie **Fouten weergeven** te klikken.  

Op de pagina met de **gegevensmigratiefouten** kunt een foutbericht kiezen om een fout op te lossen, selecteert u vervolgens **Record bewerken** om een pagina te openen met de gemigreerde gegevens voor de entiteit. Nadat u een of meer fouten hebt opgelost, kunt u **Migreren** kiezen om alleen de entiteiten te migreren die u hebt hersteld, zonder dat u geheel op nieuw moet beginnen met de migratie.  

> [!Tip]
> Als u meer dan één fout hebt verholpen, kunt u de functie **Meer selecteren** gebruiken om meerdere regels te selecteren om te migreren. Of u kunt fouten die niet noodzakelijkerwijs moeten worden opgelost, selecteren en vervolgens **Selecties overslaan** kiezen.

> [!Note]
> Als u artikelen hebt die op een stuklijst zijn opgenomen, moet u mogelijk meer dan eens migreren als het oorspronkelijke artikel niet is gemaakt vóór de varianten die ernaar verwijzen.. Als een artikelvariant eerst is gemaakt, kan de verwijzing naar het oorspronkelijke artikel een foutbericht produceren.  

## <a name="verifying-data-after-migrating"></a>Het verifiëren van gegevens na de migratie
Eén manier om te controleren of uw gegevens correct zijn gemigreerd is te kijken naar de volgende pagina's in C5 en [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Klantenposten| Financiële dagboeken|
|Leveranciersposten| Financiële dagboeken|
|Artikelposten| Artikeldagboeken|

In [!INCLUDE[d365fin](includes/d365fin_md.md)] krijgt de batch voor de gemigreerde gegevens de naam **C5MIGRATE**.

## <a name="stopping-data-migration"></a>De gegevensmigratie beëindigen
U kunt de migratie van gegevens stoppen door **Alle migraties stoppen** te kiezen. Als u dat doet, worden alle wachtende migraties ook beëindigd.

## <a name="see-also"></a>Zie ook
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Welkom bij [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

