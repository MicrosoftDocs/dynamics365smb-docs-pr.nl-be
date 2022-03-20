---
title: Opslaglocatieaanvulling berekenen
description: Als de vestiging is ingesteld voor het gebruik van gestuurde opslag en pick, worden de prioriteiten van de opslagsjabloon voor de vestiging in aanmerking genomen wanneer de ontvangsten worden opgeslagen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 7315, 7351
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8954eaacd2a78d8c1ef0c8a65f63c571e045d950
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381022"
---
# <a name="calculate-bin-replenishment"></a>Opslaglocatieaanvulling berekenen
Als de vestiging is ingesteld voor het gebruik van gestuurde opslag en pick, worden de prioriteiten van de opslagsjabloon voor de vestiging in aanmerking genomen wanneer de ontvangsten worden opgeslagen. Prioriteiten omvatten de minimale en maximale aantallen van de opslaglocatie-inhoud die zijn vastgesteld voor een bepaalde opslaglocatie en de zonevolgordes. Dus als er in een rustig tempo artikelen worden afgeleverd, worden de meestgebruikte opslaglocaties gevuld met de artikelen.  

De nieuwe voorraad komt echter niet altijd gestaag binnen. Soms worden artikelen in grote aantallen aangekocht, zodat het bedrijf een korting kan bedingen en soms produceert de productieafdeling een groot aantal artikelen om een lage eenheidsprijs te bewerkstelligen. In dat geval zullen er lange tijd geen artikelen worden ontvangen in het magazijn en moeten de artikelen van tijd tot tijd worden verplaatst van bulkopslag naar pickopslaglocaties.  

Het kan ook voorkomen dat het magazijn op korte termijn een nieuwe voorraad verwacht en dat het bulkopslaggebied hiervoor moet worden leeggemaakt.  

Als u aan de bulkopslaglocaties alleen de activiteit **Opslag** hebt toegewezen, waarbij de activiteit **Pick** is niet geselecteerd voor de opslaglocatiesoort, moet u er altijd zelf voor zorgen dat de pickopslaglocaties worden aangevuld. Er worden namelijk geen voorstellen gedaan voor pickactiviteiten uit opslaglocaties.  

## <a name="to-replenish-pick-bins"></a>U kunt als volgt pickopslaglocaties aanvullen  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verplaatsingsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Opslaglocatieaanvulling berekenen** om de rapportaanvraagpagina te openen.  
3.  Geef op de opvraagpagina voor de batchverwerking criteria op om het aantal aanvullingsvoorstellen te beperken dat wordt berekend. Wellicht bent u alleen geïnteresseerd in bepaalde artikelen, zones of opslaglocaties.  
4.  Kies de knop **Ok**. Er worden regels gemaakt voor de aanvullingsverplaatsingen die moeten worden uitgevoerd. Dit gebeurt op basis van de voorschriften die zijn opgesteld voor de opslaglocaties en de bijhorende inhoud, zijnde artikelen in de opslaglocaties.  
5.  Als u alle voorgestelde aanvullingen wilt uitvoeren, kiest u de actie **Verplaatsing maken**. De magazijnmedewerkers kunnen de instructies bekijken onder het menu-item **Verplaatsingen**, ze uitvoeren en vervolgens registreren.  
6.  Als u alleen wilt dat sommige voorstellen worden uitgevoerd, verwijdert u de minder belangrijke regels. Vervolgens maakt u een verplaatsingsinstructie.  

De volgende keer dat u de aanvulling van de opslaglocaties berekent, worden de verwijderde voorstellen automatisch opnieuw gemaakt,op voorwaarde dat deze voorstellen nog steeds geldig zijn.  

> [!NOTE]  
>  Als aan de volgende voorwaarden wordt voldaan voor een artikel:  
>   
>  -   het artikel heeft een vervaldatum en  
> -   Het veld **Picken volgens FEFO** op de vestigingskaart is geselecteerd, en  
> -   u gebruikt de functionaliteit **Opslaglocatieaanvulling berekenen**,  
>   
>  zijn de velden **Van zone** en **Van opslaglocatie** leeg, omdat het algoritme waarmee wordt berekend waar vandaan de artikelen worden verplaatst, alleen wordt geactiveerd als u de functie **Verplaatsing maken** activeert.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Picken op basis van FEFO](warehouse-picking-by-fefo.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md) 
[Assemblagebeheer](assembly-assemble-items.md)
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]