---
title: 'Procedure: Assemblageboeking ongedaan maken | Microsoft Docs'
description: Soms moet u mogelijk een geboekte assemblageorder verwijderen, zoals wanneer de order is geboekt met fouten die moeten worden gecorrigeerd of omdat deze niet geboekt had mogen worden en moet worden teruggedraaid.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 4b9fa6fb99ec68982a2869be2085de0588d76c85
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="undo-assembly-posting"></a>Boeken van assemblage ongedaan maken
Soms moet u mogelijk een geboekte assemblageorder verwijderen, zoals wanneer de order is geboekt met fouten die moeten worden gecorrigeerd of omdat deze niet geboekt had mogen worden en moet worden teruggedraaid.

Wanneer u een geboekte assemblageorder ongedaan wilt maken, wordt er een set met corrigerende artikelposten gemaakt om de oorspronkelijke posten terug te draaien. Elke positieve uitvoerpost voor het assemblageartikel wordt via een negatieve uitvoerpost teruggedraaid. Elk negatieve verbruiksartikelpost voor een assemblagecomponent wordt via een positieve verbruikspost teruggedraaid. Er wordt automatisch een vaste kostenvereffening gemaakt tussen de corrigerende en de oorspronkelijke posten om een exacte kostenterugboeking te garanderen.  

Wanneer u een volledig geboekte assemblageorder ongedaan maakt, kunt u er vervolgens voor kiezen om de assemblageorder opnieuw te maken op basis van de oorspronkelijke staat, zodat u bijvoorbeeld correcties kunt aanbrengen voordat u deze opnieuw boekt. U kunt er ook voor kiezen om de assemblageorder niet opnieuw te maken.  

Wanneer u een gedeeltelijk geboekte assemblageorder ongedaan maakt, worden vervolgens alle betrokken velden, zoals de velden **Geassembleerde hoeveelheid**, **Verbruikt aantal** en **Resterend aantal**, opnieuw ingesteld op de waarden die deze hadden voordat de desbetreffende boeking werd uitgevoerd.  

Als u assemblageorders opnieuw wilt maken of wilt terugzetten, moeten het assemblage-artikel dat in de oorspronkelijke boeking is uitgevoerd, voldoen aan de volgende voorwaarden:  

-   Het artikel moet zich nog steeds in de voorraad bevinden, met andere woorden, het artikel mag niet zijn verkocht of anderszins zijn verbruikt ten behoeve van uitgaande transacties.  
-   Het artikel mag niet gereserveerd zijn.  
-   Het artikel moet bestaan op de opslaglocatie waarnaar dit is uitgevoerd.  

Verder kunnen bestaande assemblageorders uitsluitend worden teruggedraaid als het aantal regels en de volgorde van de regels op de oorspronkelijke assemblageorder niet zijn gewijzigd.  

> [!TIP]  
>  Als u conflicten ten gevolge van regelwijzigingen wilt oplossen, kunt de wijzigingen op de desbetreffende regels handmatig ongedaan maken voordat u de bijbehorende assemblageorder boekt. U kunt de assemblageorder ook volledig boeken en er vervolgens voor kiezen om deze opnieuw te maken wanneer u de boeking ongedaan maakt.  

De volgende procedure beschrijft het ongedaan maken van geboekte assemblageorders waarvoor artikelen zijn geassembleerd voor voorraad. Als u geboekte assemblageorders waarvoor artikelen zijn geassembleerd ten behoeve van een verkooporder ongedaan wilt maken, moet u de functie **Verzending ongedaan maken** gebruiken voor de geboekte verzending die betrekking heeft op de geboekte assemblageorder. Zie voor meer informatie [Boekingen tegenboeken](finance-how-reverse-journal-posting.md). Het ongedaan het maken van de geboekte assemblageorder geschiedt vervolgens automatisch en op dezelfde wijze als in dit onderwerp is beschreven.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Het boeken van een assemblageorder ongedaan maken  
1.  Als u een volledig of gedeeltelijk geboekte assemblyorder ongedaan wilt maken, kiest u het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Geboekte assemblageorders** in en kiest u de gerelateerde koppeling.  

    Het venster **Geboekte assemblageorders** wordt geopend met een of meer assemblageorders die zijn geboekt voor de assemblageorder in kwestie. Elke gedeeltelijke boeking leidt tot het maken van een afzonderlijk geboekte assemblageorder.  
2.  Open de geboekte assemblyorder die u ongedaan wilt maken en kies vervolgens de actie **Assemblage ongedaan maken**.  

    Als de geboekte assemblageorder die u ongedaan wilt maken betrekking heeft op een volledig geboekte assemblageorder die nu wordt verwijderd, hebt u de mogelijkheid om deze opnieuw te maken omdat u deze gewoonlijk opnieuw zult willen verwerken.  
3.  Klik op de knop **Ja** als u de assemblageorder opnieuw wilt maken. Klik op de knop **Nee** als u de boeking ongedaan wilt maken zonder de bijbehorende assemblageorder opnieuw te maken.  

Het veld **Tegengeboekt** in de assemblageorder verandert in **Ja**. De assemblageorderboeking is nu teruggedraaid en u kunt doorgaan met het verwerken van de gehele assemblageorder als u ervoor kiest om deze opnieuw te maken of om de assemblageorder die u in de oorspronkelijke hebt teruggezet, te openen.  

> [!NOTE]  
>  Als u aantallen uit meerdere gedeeltelijke boekingen voor een assemblageorder wilt herstellen, moet u alle geboekte assemblageorders in kwestie ongedaan maken door voor elke geboekte assemblageorder de hiervoor beschreven stappen 1 tot en met 3 uit te voeren.  

## <a name="see-also"></a>Zie ook  
[Assemblagebeheer](assembly-assemble-items.md)  
[Boekingen tegenboeken](finance-how-reverse-journal-posting.md)  
[Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md)    
[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

