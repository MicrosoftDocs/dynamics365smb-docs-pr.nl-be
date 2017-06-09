---
title: 'Procedure: Vaste activa afschrijven of aflossen| Microsoft Docs'
description: Beschrijft hoe u een vast activum kunt afschrijven of aflossen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 3ea185979c2339a578149259f53aa81c18e5161b
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-depreciate-or-amortize-fixed-assets"></a>Procedure: Vaste activa afschrijven of aflossen
Afschrijvingen worden gebruikt om de kosten van vaste activa, zoals machines en apparatuur, te spreiden over de afschrijfbare levensduur. Voor elk vast activum moet u aangeven hoe de afschrijving wordt toegepast.  

 U kunt een afschrijving op twee manieren boeken:  

* Automatisch, door de batchverwerking **Afschrijving berekenen** uit te voeren.  
* Handmatig, met behulp van het financieel dagboek voor vaste activa.  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] kan dagelijkse afschrijving worden berekend zodat u de afschrijving voor elke willekeurige periode kunt berekenen. Zodoende kunt u de huidige bedrijfsresultaten per maand, per kwartaal of jaarlijks analyseren. Bij deze berekening worden een standaardjaar van 360 dagen en een standaardmaand van 30 dagen gebruikt. Zie [Afschrijvingsmethoden](fa-depreciation-methods.md) voor meer informatie.  

Als verschillende afdelingen een vast activum gebruiken, kan de periodieke afschrijving automatisch worden toegewezen aan deze afdelingen volgens een door de gebruiker gedefinieerde toewijzingstabel.  

U kunt onjuiste afschrijvingsposten annuleren met de batchverwerking **VA-posten annuleren** . Daarna kunt u het juiste bedrag boeken door de batchverwerking **Afschrijving berekenen** opnieuw uit te voeren. De fouten die u corrigeert, worden geboekt als foutieve VA-posten.  

Indexering wordt gebruikt om waarden aan te passen voor algemene prijswijzigingen. U kunt de batchverwerking **Vast activum indexeren** gebruiken om de afschrijvingsbedragen opnieuw te berekenen.  

## <a name="to-calculate-depreciation-automatically"></a>Afschrijving automatisch berekenen
U kunt de batchverwerking **Afschrijving berekenen** eens per maand, of op een tijdstip naar keuze uitvoeren. Met de batchverwerking worden vaste activa genegeerd die zijn verkocht, geblokkeerd of inactief zijn. U kunt ook de handmatige afschrijvingsmethode gebruiken.  

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Afschrijving berekenen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Kies de knop **Ok**.  

    Met de batchverwerking wordt de afschrijving berekend en worden regels in het financieel dagboek voor vaste activa gemaakt.  
4. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.  

    In het venster **Financieel dagboek van vaste activa** in het veld **Aantal afschrijvingsdagen** kunt u zien hoeveel afschrijvingsdagen er zijn berekend.  
5. Kies de actie **Boeken**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Een afschrijving handmatig boeken vanuit het financieel dagboek voor vaste activa
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA fin. dagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een eerste dagboekregel en vul de velden indien nodig in.  
3. In het veld **VA-boekingssoort** selecteert u **Afschrijving**.  
4. Kies de actie **VA-tegenrekening invoegen**. Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de afschrijvingsboeking is ingesteld. Zie het gedeelte "Boekingsgroepen voor vaste activa instellen" in de [Procedure: Algemene gegevens voor vaste activa instellen](fa-how-setup-general.md) voor meer informatie.  
5. Kies op het tabblad **Start** de optie **Boeken** om het dagboek te boeken.  

Als u verdeelsleutels voor vaste activa hebt ingesteld om bedragen over verschillende afdelingen of projecten te verdelen, worden de bedragen tijdens de boeking verdeeld. Zie [Procedure: Algemene gegevens voor vaste activa instellen](fa-how-setup-general.md) voor meer informatie.  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Verdelingen in het financieel dagboek voor vaste activa berekenen
Als een vast activum door verschillende afdelingen wordt gebruikt, kan de periodieke afschrijving automatisch worden toegewezen aan deze afdelingen volgens een zelfgedefinieerde toewijzingstabel.  

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA fin. dagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een eerste regel en vul de velden indien nodig in.
3. In het veld **VA-boekingssoort** selecteert u **Verdeelsleutel**.  
4. Kies de actie **VA-tegenrekening invoegen**. Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de boeking van de verdeelsleutel is ingesteld.  
5. Kies op het tabblad **Start** de optie **Boeken** om het dagboek te boeken.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Duplicatielijsten gebruiken ter voorbereiding op de boeking naar meerdere afschrijvingsboeken
Als u dagboekregels invult die naar een afschrijvingsboek moeten worden geboekt, kunt u de regels in een apart dagboek dupliceren, zodat u ze naar een ander afschrijvingsboek kunt boeken. Zie het gedeelte "Posten boeken naar verschillende afschrijvingsboeken" voor meer informatie.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open het afschrijvingsboek en schakel vervolgens het selectievakje **Deel van duplicatielijst** in.  

**Belangrijk:** als u het veld **Duplicatielijst gebruiken** hebt geselecteerd, moet u geen nummerreeksen gebruiken voor het dagboek. De reden is dat de nummerreeks voor het financieel dagboek voor vaste activa niet overeenkomt met de nummerreeks voor het dagboek voor vaste activa.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Posten naar verschillende afschrijvingsboeken boeken
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA fin. dagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Schakel in het dagboek waarmee u de afschrijving wilt boeken, het selectievakje **Duplicatielijst gebruiken** in.  
3. Vul indien nodig de resterende velden in.  
4. Kies de actie **Boeken**.  
5. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-dagboeken** in en kies vervolgens de gerelateerde koppeling.  

    **Opmerking:** het venster **VA-dagboek** bevat nieuwe regels voor verschillende afschrijvingsboeken volgens de duplicatielijst.  
6. Controleer of bewerk de regels en kies vervolgens de actie **Boeken**.  

    **Opmerking:** u kunt een post ook naar een apart boek dupliceren door tijdens het invullen van een dagboekregel in het veld **Dupliceren in afschrijvingsboek** de code van een afschrijvingsdagboek op te geven.  

Met behulp van de batchverwerking **Afschrijvingsboek kopiëren** kunt u posten uit afschrijvingsboeken naar andere afschrijvingsboeken kopiëren. Met de batchverwerking worden dagboekregels gemaakt in de dagboekbatch die u hebt opgegeven in het venster **VA-dagboekinstellingen** voor het afschrijvingsboek waarnaar u wilt kopiëren. Zie de volgende procedure voor meer informatie.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Posten voor vaste activa tussen afschrijvingsboeken kopiëren
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open de betreffende afschrijvingsboekkaart en kies vervolgens de actie **Afschrijvingsboek kopiëren**.  
3. Vul in het venster **Afschrijvingsboek kopiëren** indien nodig de velden in.  
4. Kies de knop **Ok**.  

De gekopieerde regels worden in het financieel dagboek voor vaste activa of het dagboek voor vaste activa gemaakt, afhankelijk van de vraag of het afschrijvingsboek dat u kopieert, geïntegreerd is met het grootboek.  

## <a name="see-also"></a>Zie ook
[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

