---
title: Productierapporten en analyses
description: Bekijk welke productierapporten en analyses beschikbaar zijn in de standaardversie van Business Central, zodat u uw bedrijf kunt volgen.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216445"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Productierapporten en analyses in Business Central

Productierapportage in [!INCLUDE [prod_short](includes/prod_short.md)] stelt productie- en zakelijke professionals in staat om inzichten en statistieken te krijgen over huidige en vroegere productieactiviteiten.  

## <a name="reports"></a>Rapporten

De volgende tabel beschrijft enkele van de belangrijkste rapporten in productierapportage.

|Rapport |Object-id|Omschrijving  |
|---------|---------|---------|
|**Stuklijst - Aantalontwikkeling**|99000753|Bevat een ingesprongen stuklijstoverzicht van het artikel of de artikelen die u hebt opgegeven in de filters. De productiestuklijst wordt volledig getoond voor alle niveaus.|
|**Artikel - Mogelijk te maken (tijd)**|5871|Hiermee wordt weergegeven hoe vijf verschillende beschikbaarheidscijfers in de loop van de tijd veranderen voor een stuklijstartikel. Deze cijfers veranderen op basis van de verwachte vraag- en aanbodgebeurtenissen en aanbod die is gebaseerd op beschikbare onderdelen die kunnen worden geassembleerd of geproduceerd.<br>U kunt de lijst gebruiken om te zien of u een verkooporder voor een artikel op een bepaalde datum kunt afhandelen door te kijken naar de huidige beschikbaarheid in combinatie met de mogelijke hoeveelheden die de onderdelen ervan kunnen leveren als een assemblageorder is gestart. In de lijst wordt weergegeven wanneer en hoeveel eenheden van een assemblage- en productieartikel u kunt maken op basis van de beschikbaarheid van onderdelen en de huidige beschikbaarheid van het artikel. Dit wordt weergegeven als de totale hoeveelheid.<br>De informatie wordt weergegeven in een grafiek waarin elk beschikbaarheidscijfer een lijn vormt die de tijdlijn volgt en omhoog en omlaag beweegt naarmate de hoeveelheden veranderen. De hoeveelheidscijfers zijn afkomstig van dezelfde engine die het venster **Artikelbeschikbaarheid per stuklijstniveau** van informatie voorziet. |
|**Distributie van aandeel stuklijstkosten**|5872|Hiermee wordt in grafische vorm weergegeven hoe de kosten van een geassembleerd of geproduceerd artikel worden verspreid via de bijbehorende stuklijst.<br>Dergelijke informatie is bijvoorbeeld handig bij de bepaling of u van onderdelenleverancier wilt veranderen, intern capaciteitsgebruik wilt vervangen door uitbestede arbeid of omgekeerd, of bij het controleren en wijzigen van de stuklijst van een artikel.<br>De eerste grafiek in de lijst bevat de totale kostprijs van de onderdelen en arbeidsbronnen van het hoofdartikel opgesplitst in vijf verschillende kostenaandelen en grafisch weergegeven met verschillende kleuren.<br>Het cirkeldiagram met het bijschrift *Op materiaal/arbeid* laat de evenredige verdeling zien tussen de materiaal- en arbeidskosten van het hoofdartikel, alsmede de eigen productieoverhead. Het materiaalkostenaandeel bevat de materiaalkosten van het artikel. Het arbeidskostenaandeel omvat capaciteit, capaciteitsoverhead en uitbestedingskosten. De kostenaandelen worden anders weergegeven, afhankelijk van uw keuzes in het veld **Alleen weergeven**.<br>Het cirkeldiagram met het bijschrift *Op direct/indirect* toont de evenredige verdeling tussen de directe en indirecte kosten van het hoofdartikel. Het directe kostenaandeel bevat de materiaalkosten, de capaciteit en de uitbestedingskosten van het artikel. Het indirecte kostenaandeel omvat de capaciteitsoverhead en productieoverhead.<br>De tabel onder aan de lijst wordt opgenomen als u het selectievakje **Details opnemen** inschakelt. Hier worden geselecteerde waarden weergegeven uit het venster Kostenaandelen stuklijst op één niveau of alle niveaus, afhankelijk van uw keuzen in het veld **Aandeel kosten weergeven als**.|
|**Gedetailleerde berekening**|99000756|Geeft een overzicht aan van de kosten per artikel (inclusief uitval).|
|**Waar gebruikt (Hoogste niveau)**|99000757|Toont waar en in welke aantallen de artikelen worden gebruikt in de productstructuur.<br>De lijst toont het artikel alleen als Waar gebruikt, wanneer het basisartikel wordt gebruikt als het artikel op het hoogste niveau. Een voorbeeld: artikel A wordt gebruikt om artikel B te produceren en artikel B wordt gebruikt om artikel C te produceren. In de lijst wordt artikel B weergegeven als u dit rapport uitvoert voor artikel A. Als u dit rapport uitvoert voor artikel B, wordt artikel C weergegeven als waar-gebruikt.<br>U kunt de pagina **Waar gebruikt-regel** ook rechtstreeks openen vanuit het artikel.|
|**Vergelijkend overzicht van artikelstuklijst**|99000758|Dit rapport geeft u de mogelijkheid om vergelijkbare eindproducten te vergelijken wat betreft de kosten. U ziet een lijst met alle componenten en hun kosten, evenals de benodigde hoeveelheden. De berekeningsdatum is normaal gesproken ingesteld op de werkdatum. |
|**Prod.-orderstatistiek**|99000791|Bevat de diverse kosten die voor de geselecteerde productieorder zijn gecumuleerd.<br>De inhoud van de lijst is vergelijkbaar met de pagina **Prod.-orderstatistiek**.<br>Voor productieorders die het productiebeleid *Op order produceren* gebruiken, bevat het venster alleen materiaalkosten en capaciteitskosten van artikelen op het hoogste stuklijstniveau.|
|**Capaciteit - Taakoverzicht**|99000780|Geeft aan welke productieorders op de afdelingen en bewerkingsplaatsen wachten op verwerking. Er worden afdrukken gemaakt van de capaciteit van de afdeling of de bewerkingsplaats. De lijst bevat gegevens zoals begin- en eindtijd, begin- en einddatum en inputaantal per productieorder.|
|**Werklast van afdeling** of **Werklast van bewerkingsplaats**|99000783 of 99000784|Beide rapporten geven een overzicht van een afdeling of bewerkingsplaats. De werklast voor een afdeling/bewerkingsplaats is de som van het benodigde aantal keren dat alle geplande en werkelijke orders worden uitgevoerd voor de afdeling in een opgegeven periode.|
|**PO - Materiaaltekortenlijst**|99000788|Dit rapport kan worden gebruikt om alle componenten te zien die niet beschikbaar zijn vanwege ontbrekende voorraad. Dit overzicht kan dus worden gebruikt om op tijd te zien of de tijdlijn voor een geplande of vrijgegeven productieorder kan worden aangehouden.|


## <a name="tasks"></a>Taken

In de volgende artikelen worden enkele van de belangrijkste taken beschreven voor het analyseren van de toestand van uw bedrijf:

* [De werklast in afdelingen en bewerkingsplaatsen weergeven](production-how-to-view-the-load-on-work-centers.md)  
* [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)

## <a name="see-also"></a>Zie ook

[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
