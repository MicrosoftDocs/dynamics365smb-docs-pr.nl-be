---
title: Productie-output en bewerkingstijd in batches boeken
description: De outputhoeveelheid geeft de voortgang van het werk weer in de vorm van de voltooide hoeveelheid en de gebruikte capaciteit van de afdeling of de bewerkingsplaats.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: bholtorf
---
# Output en bewerkingstijden in batches boeken

De outputhoeveelheid geeft de voortgang van het werk weer in de vorm van de voltooide hoeveelheid en de gebruikte capaciteit van de afdeling of de bewerkingsplaats.

U kunt ook het outputdagboek gebruiken om:

* Voorraad aan te passen in verband met de output van voltooide artikelen vanuit productie.
* Hoeveelheden en uitval te registreren voor elke bewerking in productierouting.
* Instel- en looptijd te registreren voor afdelingen en bewerkingsplaatsen.

> [!NOTE]
> Als productierouting wordt gebruikt, wordt de voorraad alleen bijgewerkt wanneer u het outputaantal bij de laatste bewerking boekt.

Met de pagina **Productiedagboek** kunt u dezelfde taken uitvoeren als op de pagina **Outputdagboek** en ook verbruiksboekingstaken uitvoeren. Zie voor meer informatie [Verbruik en output registreren voor één vrijgegeven productieorderregel](production-how-to-register-consumption-and-output.md).

## Outputaantallen boeken en/of looptijden registreren voor een of meer productieorderregels

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Outputdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Voer in de velden informatie over de productieorder en output en/of looptijd in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    U kunt de functie **Bewerkingsplan weergeven** om dagboekregels te genereren op basis van productieorders.
  
3. Als de bewerking is voltooid, selecteert u het veld **Voltooid**.  
4. Kies de actie **Boeken** om de activiteiten te boeken.

    Capaciteitsboekingen worden bijgewerkt voor de gebruikte werk- of machinecentra met informatie over tijd en hoeveelheid output en uitval. Als u de laatste bewerking heeft geboekt, wordt het artikel aan de inventaris toegevoegd.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Zie ook

[Uitval handmatig boeken](production-how-to-post-scrap.md)
[Outputboeking tegenboeken](production-how-to-reverse-output-posting.md)
[Productie](production-manage-manufacturing.md)
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
