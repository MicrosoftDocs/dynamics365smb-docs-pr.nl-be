---
title: Vaste activa afschrijven of aflossen
description: 'U moet bepalen hoe u elk van uw vaste activa, zoals machines en uitrusting, afschrijft of aflost over hun afschrijfbare levensduur.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Vaste activa afschrijven of aflossen

Afschrijvingen worden gebruikt om de kosten van vaste activa, zoals machines en apparatuur, te spreiden over de afschrijfbare levensduur. Voor elk vast activum moet u aangeven hoe de afschrijving wordt toegepast.  

 U kunt een afschrijving op twee manieren boeken:  

* Automatisch, door de batchverwerking **Afschrijving berekenen** uit te voeren.  
* Handmatig, met behulp van het financieel dagboek voor vaste activa.  

In [!INCLUDE[prod_short](includes/prod_short.md)] kan dagelijkse afschrijving worden berekend zodat u de afschrijving voor elke willekeurige periode kunt berekenen. Zodoende kunt u de huidige bedrijfsresultaten per maand, per kwartaal of jaarlijks analyseren. Bij deze berekening worden een standaardjaar van 360 dagen en een standaardmaand van 30 dagen gebruikt. Zie [Afschrijvingsmethoden](fa-depreciation-methods.md) voor meer informatie.  

Als verschillende afdelingen een vast activum gebruiken, kan de periodieke afschrijving automatisch worden toegewezen aan deze afdelingen volgens een door de gebruiker gedefinieerde toewijzingstabel.  

U kunt onjuiste afschrijvingsposten annuleren met de batchverwerking **VA-posten annuleren** . Daarna kunt u het juiste bedrag boeken door de batchverwerking **Afschrijving berekenen** opnieuw uit te voeren. De fouten die u corrigeert, worden geboekt als foutieve VA-posten.  

Indexering wordt gebruikt om waarden aan te passen voor algemene prijswijzigingen. U kunt de batchverwerking **Vast activum indexeren** gebruiken om de afschrijvingsbedragen opnieuw te berekenen.  

## <a name="to-calculate-depreciation-automatically"></a>Afschrijving automatisch berekenen

U kunt de batchverwerking **Afschrijving berekenen** eens per maand, of op een tijdstip naar keuze uitvoeren. Met de batchverwerking worden vaste activa genegeerd die zijn verkocht, geblokkeerd of inactief zijn. U kunt ook de handmatige afschrijvingsmethode gebruiken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afschrijving berekenen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Kies de knop **Ok**.  

    Met de batchverwerking wordt de afschrijving berekend en worden regels in het financieel dagboek voor vaste activa gemaakt.

4. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-fin. dagboeken** in en kies vervolgens de gerelateerde koppeling.  

    Op de pagina **Financieel dagboek van vaste activa** in het veld **Aantal afschrijvingsdagen** kunt u zien hoeveel afschrijvingsdagen er zijn berekend.  
5. Kies de actie **Boeken**.  

> [!NOTE]
> Bekende beperking: Als u het veld **Vast aantal dagen gebruiken** selecteert en het veld **Vast aantal dagen** is ingesteld op een waarde die ertoe leidt dat **Boekingsdatum** minus **Aantal dagen** een datum in het vorige kalenderjaar is, kunt u de afschrijving niet boeken.
> U kunt dit voorkomen door het veld **Vast aantal dagen** te verlagen tot niet meer dan de berekende dagen tot de boekingsdatum met 30 dagen/maand OF het veld **Boekjaar (365 dagen)** te selecteren in het afschrijvingsboek.
> We raden de eerste optie aan, omdat u het gebruik van 30 dagen/maanden voor afschrijving misschien niet wilt wijzigen. Zie voor meer informatie [Afschrijving met veld Boekjaar (365 dagen)](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Een afschrijving handmatig boeken vanuit het financieel dagboek voor vaste activa

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financieel dagboek voor vaste activa** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een eerste dagboekregel en vul de velden indien nodig in.  
3. In het veld **VA-boekingssoort** selecteert u **Afschrijving**.  
4. Kies de actie **VA-tegenrekening invoegen**. Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de afschrijvingsboeking is ingesteld. Zie [Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups) voor meer informatie.
5. Kies de actie **Boeken** om het journaal te boeken.  

Het veld **Boekwaarde** op de pagina **Vast activum** wordt dienovereenkomstig bijgewerkt.

Als u verdeelsleutels voor vaste activa hebt ingesteld om bedragen over verschillende afdelingen of projecten te verdelen, worden de bedragen tijdens de boeking verdeeld. Zie [Algemene gegevens voor vaste activa instellen](fa-how-setup-general.md) voor meer informatie.  

## <a name="to-manage-the-ending-book-value"></a>De eindboekwaarde beheren

In het veld **Min. boekw. voor afschr.** op de pagina **VA-afschrijvingsboeken** kunt u de boekwaarde opgeven die uw vaste activa in het huidige afschrijvingsboek moeten hebben nadat het volledig is afgeschreven. U kunt dit handmatig doen of u kunt het veld **Std. min. boekw. voor afschr.** op de gerelateerde pagina **Afschrijvingsboek** invullen, dat vervolgens zal worden gebruikt om het veld automatisch in te vullen.

> [!NOTE]
> Als de laatste afschrijving betekent dat het veld **Boekwaarde** op de pagina **Vast activum** nul is, wordt dit bedrag automatisch afgetrokken van de laatste afschrijving.<br /><br />
> Als de waarde in het veld **Boekwaarde** na de laatste afschrijving groter is dan nul, bijvoorbeeld vanwege een afrondingsprobleem of omdat er een restwaarde is, wordt de waarde in het veld **Min. boekw. voor afschr.** op de pagina **VA-afschrijvingsboeken** genegeerd. Zie voor meer informatie [De restwaarde samen met de aanschaffingswaarde boeken](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Verdelingen in het financieel dagboek voor vaste activa berekenen

Als een vast activum door verschillende afdelingen wordt gebruikt, kan de periodieke afschrijving automatisch worden toegewezen aan deze afdelingen volgens een zelfgedefinieerde toewijzingstabel.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financieel dagboek voor vaste activa** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een eerste regel en vul de velden indien nodig in.
3. In het veld **VA-boekingssoort** selecteert u **Verdeelsleutel**.  
4. Kies de actie **VA-tegenrekening invoegen**. Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de boeking van de verdeelsleutel is ingesteld.  
5. Kies de actie **Boeken** om het journaal te boeken.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Duplicatielijsten gebruiken ter voorbereiding op de boeking naar meerdere afschrijvingsboeken

Als u dagboekregels invult die naar een afschrijvingsboek moeten worden geboekt, kunt u de regels in een apart dagboek dupliceren, zodat u ze naar een ander afschrijvingsboek kunt boeken. Zie [Posten boeken naar verschillende afschrijvingsboeken](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open het afschrijvingsboek en schakel vervolgens het selectievakje **Deel van duplicatielijst** in.  

> [!IMPORTANT]  
>   Als u het veld **Duplicatielijst gebruiken** hebt geselecteerd, moet u geen nummerreeksen gebruiken voor het dagboek. De reden is dat de nummerreeks voor het financieel dagboek voor vaste activa niet overeenkomt met de nummerreeks voor het dagboek voor vaste activa.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Posten naar verschillende afschrijvingsboeken boeken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financieel dagboek voor vaste activa** in en kies vervolgens de gerelateerde koppeling.  
2. Schakel in het dagboek waarmee u de afschrijving wilt boeken, het selectievakje **Duplicatielijst gebruiken** in.  
3. Vul indien nodig de resterende velden in.  
4. Kies de actie **Boeken**.  
5. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-dagboeken** in en kies vervolgens de gerelateerde koppeling.  

    > [!NOTE]  
    >   De pagina **VA-dagboek** bevat nieuwe regels voor verschillende afschrijvingsboeken volgens de duplicatielijst.  
6. Controleer of bewerk de regels en kies vervolgens de actie **Boeken**.  

    > [!NOTE]  
    >   U kunt een post ook naar een apart boek dupliceren door tijdens het invullen van een dagboekregel in het veld **Dupliceren in afschr.-boek** de code van een afschrijvingsdagboek op te geven.  

Met behulp van de batchverwerking **Afschrijvingsboek kopiëren** kunt u posten uit afschrijvingsboeken naar andere afschrijvingsboeken kopiëren. De batchverwerking maakt dagboekregels in de dagboekbatch die u hebt opgegeven op de pagina **VA-dagboekinstellingen** voor het afschrijvingsboek waarnaar u wilt kopiëren. Zie de volgende procedure voor meer informatie.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Posten voor vaste activa tussen afschrijvingsboeken kopiëren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open de betreffende afschrijvingsboekkaart en kies vervolgens de actie **Afschrijvingsboek kopiëren**.  
3. Vul op de pagina **Afschrijvingsboek kopiëren** indien nodig de velden in.  
4. Kies de knop **OK**.  

De gekopieerde regels worden in het financieel dagboek voor vaste activa of het dagboek voor vaste activa gemaakt, afhankelijk van de vraag of het afschrijvingsboek dat u kopieert, geïntegreerd is met het grootboek.  

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/calculate-post-depreciations/)

## <a name="see-also"></a>Zie ook

[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
