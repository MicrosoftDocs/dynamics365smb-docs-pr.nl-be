---
title: Assemblagerapporten en analyses in Business Central
description: Bekijk welke assemblagerapporten en analyses beschikbaar zijn in de standaardversie van Business Central, zodat u uw bedrijf kunt volgen.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216447"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>Assemblagerapporten en analyses in Business Central

Assemblagerapportage in [!INCLUDE [prod_short](includes/prod_short.md)] stelt productie- en zakelijke professionals in staat om inzichten en statistieken te krijgen over huidige en vroegere assemblageactiviteiten.  

## <a name="reports"></a>Rapporten

De volgende tabel beschrijft enkele van de belangrijkste rapporten in assemblagerapportage.

|Rapport |Object-id|Omschrijving  |
|---------|---------|---------|
|**Assemblagestuklijsten**|801|Hier wordt een overzicht van stuklijsten weergegeven: naam, stuklijstnummer, stuklijstonderdelen en mogelijke andere stuklijsten die deel uitmaken van de stuklijst. De stuklijstonderdelen worden in de tabel Stuklijstcomponent gedefinieerd. U ziet hier ook de maateenheid en de benodigde hoeveelheid van elk onderdeel per basismaateenheid. |
|**Artikel - Mogelijk te maken (tijd)**|5871|Hiermee wordt weergegeven hoe vijf verschillende beschikbaarheidscijfers in de loop van de tijd veranderen voor een stuklijstartikel. Deze cijfers veranderen op basis van de verwachte vraag- en aanbodgebeurtenissen en aanbod die is gebaseerd op beschikbare onderdelen die kunnen worden geassembleerd of geproduceerd.<br>U kunt de lijst gebruiken om te zien of u een verkooporder voor een artikel op een bepaalde datum kunt afhandelen door te kijken naar de huidige beschikbaarheid in combinatie met de mogelijke hoeveelheden die de onderdelen ervan kunnen leveren als een assemblageorder zou worden gestart. In de lijst wordt weergegeven wanneer en hoeveel eenheden van een assemblage- en productieartikel u kunt maken op basis van de beschikbaarheid van onderdelen en de huidige beschikbaarheid van het artikel. Dit wordt weergegeven als de totale hoeveelheid.<br>De informatie wordt weergegeven in een grafiek waarin elk beschikbaarheidscijfer een lijn vormt die de tijdlijn volgt en omhoog en omlaag beweegt naarmate de hoeveelheden veranderen. De hoeveelheidscijfers zijn afkomstig van dezelfde engine die het venster **Artikelbeschikbaarheid per stuklijstniveau** van informatie voorziet. |
|**Distributie van aandeel stuklijstkosten**|5872|Hiermee wordt in grafische vorm weergegeven hoe de kosten van een geassembleerd of geproduceerd artikel worden verspreid via de bijbehorende stuklijst.<br>Dergelijke informatie is bijvoorbeeld handig bij de bepaling of u van onderdelenleverancier wilt veranderen, intern capaciteitsgebruik wilt vervangen door uitbestede arbeid of omgekeerd, of bij het controleren en wijzigen van de stuklijst van een artikel.<br>De eerste grafiek in de lijst bevat de totale kostprijs van de onderdelen en arbeidsbronnen van het hoofdartikel opgesplitst in vijf verschillende kostenaandelen en grafisch weergegeven met verschillende kleuren.<br>Het cirkeldiagram met het bijschrift *Op materiaal/arbeid* laat de evenredige verdeling zien tussen de materiaal- en arbeidskosten van het hoofdartikel, alsmede de eigen productieoverhead. Het materiaalkostenaandeel bevat de materiaalkosten van het artikel. Het arbeidskostenaandeel omvat capaciteit, capaciteitsoverhead en uitbestedingskosten. De kostenaandelen worden anders weergegeven, afhankelijk van uw keuzes in het veld **Alleen weergeven**.<br>Het cirkeldiagram met het bijschrift *Op direct/indirect* toont de evenredige verdeling tussen de directe en indirecte kosten van het hoofdartikel. Het directe kostenaandeel bevat de materiaalkosten, de capaciteit en de uitbestedingskosten van het artikel. Het indirecte kostenaandeel omvat de capaciteitsoverhead en productieoverhead.<br>De tabel onder aan de lijst wordt opgenomen als u het selectievakje Details opnemen inschakelt. Hierin worden geselecteerde waarden weergegeven uit het venster Kostenaandelen stuklijst op één niveau of alle niveaus, afhankelijk van de optie die u kiest in het veld Aandeel kosten weergeven als.|
|**Waar gebruikt-overzicht**|809|Geeft een lijst weer met de stuklijsten waarvan de geselecteerde artikelen deel uitmaken. Een handig overzicht voor het geval u een onderdeel moet wijzigen in een stuklijst die in een assemblageartikel is ingevoegd. Bijvoorbeeld als uw leverancier een specifiek artikel dat u voor uw assemblage/productie hebt gebruikt, niet meer kan leveren. In dergelijke scenario's biedt dit rapport u een eenvoudig overzicht van in welke stuklijsten het onderdeel is opgenomen. U kunt een filter instellen voor het nummer van het onderdeel.|
|**Stuklijst - Grondstoffen**|810|Dit rapport kan u een overzicht geven van de benodigde componenten, zowel voor assemblage als voor productie. U ziet de voorraad, de basiseenheid, de hoofdverkoper als het leveranciersnummer staat op de artikelkaart zelf, en de doorlooptijdberekening.|
|**Stuklijst - Halffabrikaten**|811|Als u subassemblages produceert en/of assembleert, kunt u dit rapport gebruiken om een overzicht te krijgen van dit type component. Dit rapport toont u de basiseenheid, de voorraad, de eenheidskosten en een alternatief artikelnummer. |
|**Assemblagestuklijst - Eindproducten**|812|Geeft een lijst met artikelen of stuklijsten weer die geen deel uitmaken van stuklijsten. **Opmerking**: dit rapport is niet beperkt tot alleen stuklijst, dus vergeet niet om het filter in te stellen in de velden **Assemblagestuklijst** of **Aanvullingsmethode**|
|**Op order assembleren - Verkoop**|915|Toont belangrijke verkoopcijfers voor assemblagecomponentartikelen die afzonderlijk of als onderdeel van een op-order-assembleren verkoop en als afzonderlijk artikel uit voorraad kunnen worden verkocht.<br>Gebruik dit rapport voor de analyse van de hoeveelheid, kosten, verkoop- en winstcijfers van assemblageonderdelen ter ondersteuning van uw beslissingen, bijvoorbeeld of een kit anders moet worden geprijsd of dat een bepaald artikel in assemblages moet worden gestart of gestopt.<br>De rij **In assemblage** toont de verkoopcijfers voor het totale aantal dat is verkocht als onderdeel van een assemblageartikel. De verkoop van het specifieke assemblageartikel waaruit dit totaal bestaat, wordt weergegeven als u het veld **Assemblagedetails weergeven** selecteert.<br>De nadruk ligt op de assemblage-onderdelen, maar de cijfers zijn berekend op basis van de winstmarge van het bovenliggende artikel, het assemblageartikel. Dienovereenkomstig wordt het verkoopbedrag van elk onderdeel berekend vanuit de eigen kosten en de winstmarge van het bovenliggende artikel in de volgende formule berekend.<br>Het rapport bevat gegevens voor artikelen die voldoen aan één of beide van de volgende criteria:<br>- Bestaat in de assemblagestuklijst van een artikel dat het assemblagebeleid Op order assembleren gebruikt.<br>- Is verkocht als onderdeel van een op-order-assembleren verkoop.|

## <a name="tasks"></a>Taken

In de volgende artikelen worden enkele van de belangrijkste taken beschreven voor het analyseren van de toestand van uw bedrijf:

* [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)

## <a name="see-also"></a>Zie ook

[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met stuklijsten](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
