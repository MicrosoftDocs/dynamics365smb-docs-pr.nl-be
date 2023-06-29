---
title: Verbruiksoutput registreren voor productieorder
description: In dit onderwerp wordt uitgelegd hoe u verbruik en output registreert voor een vrijgegeven productieorderregel die wordt weergegeven op de pagina Productiedagboek.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="register-consumption-and-output-for-one-released-production-order-line"></a><a name="register-consumption-and-output-for-one-released-production-order-line"></a>Verbruik en output registreren voor één vrijgegeven productieorderregel

Deze taak wordt uitgevoerd op de pagina **Productiedagboek**. Hierin worden de functies van de dagboeken voor afzonderlijk gebruik en voor output in één dagboek gecombineerd. Het gecombineerde dagboek kan rechtstreeks vanuit een vrijgegeven productieorder worden geopend. De belangrijkste doelen van het dagboek zijn: het handmatig boeken van materiaalverbruik, het aantal geproduceerde eindartikelen en de tijd die bewerkingen kosten. De waarden worden geboekt naar posten onder de vrijgegeven productieorder. Verbruiksaantallen worden geboekt als negatieve artikelposten, outputaantallen worden geboekt als positieve artikelposten en bestede tijd wordt geboekt als capaciteitspost. Die geboekte waarden kunnen ook onder in het dagboek worden weergegeven als werkelijke aantallen.  

> [!NOTE]  
> Omdat de gegevens over het verbruik tegelijk met de gegevens over de output worden verwerkt, biedt dit dagboek de gelegenheid om gekoppelde materialen en bewerkingen in een logische processtructuur weer te geven. Materialen worden ingesprongen onder de bijbehorende bewerking. Dit vereist het gebruik van bewerkingsplankoppelingen.  

> [!NOTE]  
> materialen zonder bewerkingsplankoppelingen worden in het dagboek als eerste weergegeven.  

## <a name="to-register-consumption-and-output"></a><a name="to-register-consumption-and-output"></a>Verbruik en output registreren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vrijgegeven prod.-orders** in en kies vervolgens de gerelateerde koppeling.  
2. Open een vrijgegeven productieorderregel die gereed is voor registratie en kies op het sneltabblad **Regels** de actie **Regel** en kies vervolgens de actie **Productiedagboek**.  

    De pagina **Productiedagboek** wordt geopend met dagboekregels voor de productieorderregel volgens de pagina's **Materiaalregel** en **Prod.-orderbewerkingsplan**. Deze regels zijn afkomstig uit de productiestuklijst en het bewerkingsplan die zijn toegewezen aan het artikel dat wordt geproduceerd. Zie voor meer informatie [Productiestuklijsten maken](production-how-to-create-routings.md).  

3. Boven in het dagboek voert u in het veld **Boekingsdatum** een boekingsdatum in die voor alle regels geldt. Standaard wordt de werkdatum ingevoerd. Het veld is bedoeld om boekingsdatums eventueel snel op alle regels af te kunnen stemmen.  

    > [!NOTE]  
    >  Dit veld wordt overschreven door boekingsdatums die op de afzonderlijke regels worden ingevoerd.  

4. In het veld **Filter afboekingsmethode** boven aan het dagboek, kunt u aangeven dat het verbruik en de output die automatisch worden geboekt volgens de respectievelijk voor het artikel en de resource gedefinieerde afboekingsmethoden, moeten worden weergegeven. Zie voor meer informatie [Afboeking van materialen op basis van de uitvoer van een bewerking inschakelen](production-how-to-flush-components-according-to-operation-output.md).

5. Ga door met het invoeren van aantallen in de bewerkbare velden voor verbruik en output.  
  
    Alleen de relevante velden worden weergegeven voor elk soort regel in het dagboek. De overige regels zijn leeg en tegen schrijven beveiligd.  

    Wanneer het dagboek wordt geopend, zijn de aantallen die moeten worden geboekt al ingevuld. Wanneer er tot dusver nog niets is geboekt, wordt standaard in alle aantalvelden het verwachte aantal dat de productieorder zal opleveren, weergegeven. Als er deelboekingen zijn uitgevoerd, wordt op de aantalvelden op de regels het resterende aantal weergegeven. De aantallen en tijden die al geboekt zijn, worden onder in het dagboek weergegeven als werkelijke posten.  

    Wat betreft aantallen in het veld **Outputaantal** kunt u de waarden instellen die automatisch moeten worden weergegeven wanneer het dagboek voor het eerst wordt geopend. Dit doet u vanuit de pagina **Productie-instellingen**, op het sneltabblad **Algemeen** in het veld **Vooraf ingestelde outputaantal**.

    > [!NOTE]  
    >  Alleen met het outputaantal op de laatste dagboekregel van boekingssoort **Output** wordt de voorraadafdeling geherwaardeerd als het dagboek wordt geboekt. Zorg er dan ook voor dat u het dagboek niet boekt (met het verwachte outputaantal dat vooraf is ingesteld op de laatste outputregel) totdat alle eindartikelen ook daadwerkelijk zijn geproduceerd.  

6. Selecteer voor de outputregels het veld **Gereedgemeld** om aan te geven dat de bewerking gereed is. Dit veld is verbonden met het veld **Bew.-planstatus** op een bewerkingsplanregel van een productieorder.  
7. Kies de actie **Boeken** om de ingevoerde aantallen te registreren en sluit vervolgens het dagboek.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    Als er nog waarden moeten worden geboekt, bevat het dagboek deze resterende waarden de volgende keer dat het wordt geopend. Geboekte waarden worden onder in het dagboek weergegeven als werkelijke waarden.  

    > [!NOTE]  
    >  Als een artikel dat wordt verbruikt geblokkeerd is, worden er voor dat artikel geen verbruiksaantallen geboekt in het dagboek. Als een bewerkingsplaats of afdeling geblokkeerd is, worden er voor de desbetreffende outputregel in het dagboek geen outputaantallen of procestijden geboekt.  

    > [!NOTE]  
    > als u het dagboek sluit zonder te boeken, gaan de wijzigingen verloren.  

> [!WARNING]  
> De pagina **Productiedagboek** kan niet worden gebruikt door twee gebruikers tegelijk. Dit betekent dat als Gebruiker 2 de pagina opent en de gegevens invoert wanneer Gebruiker 1 al werkt op de pagina, Gebruiker 2 gegevens kan verliezen wanneer Gebruiker 1 de pagina sluit.  

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Productie](production-manage-manufacturing.md)  
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
