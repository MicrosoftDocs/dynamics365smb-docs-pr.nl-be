---
title: Vaste activa onderhouden
description: Registreer reparaties en onderhoud aan een vast activum om de waarde ervan te behouden.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Vaste activa onderhouden

Onderhoudskosten zijn exploitatiekosten voor de zaken die u doet om de conditie van uw vaste activa op peil te houden. In tegenstelling tot kapitaalverbeteringen verhoogt onderhoud de waarde van uw bezittingen niet.

Telkens wanneer u onderhoud laat plegen aan een vast activum, registreert u relevante informatie, zoals de datum van de onderhoudsbeurt, de leverancier die het werk heeft uitgevoerd en het telefoonnummer van de onderhoudsdienst. U voert onderhoudsinformatie in op verschillende pagina's:

* Vast activum
* Inkooporder
* Inkoopfactuur
* VA fin. dagboek

Indexering wordt gebruikt om waarden aan te passen voor algemene prijswijzigingen. Gebruik de actie **Vast activum indexeren** om onderhoudskosten opnieuw te berekenen.

## Onderhoudskosten rechtstreeks op een vast activum registreren

Elke keer dat onderhoud wordt uitgevoerd voor een activum, zoals een onderhoudsbeurt, kunt u dit registreren op de pagina **Onderhoudsregistratie**.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het vaste activum waarvoor u onderhoud wilt registreren en kies vervolgens de actie **Onderhoudsregistratie**.
3. Vul op de pagina **Onderhoudsregistratie** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Onderhoudskosten boeken vanuit een financieel dagboek voor vaste activa

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afschrijvingsboekoverzicht** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het afschrijvingsboek dat aan het vaste activum is toegewezen en kies vervolgens de actie **Bewerken**.
3. Zorg er op de pagina **Afschrijvingsboek** voor dat het selectievakje  **Onderhoud** niet is ingeschakeld, zodat u onderhoudskosten niet naar het grootboek boekt.
4. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-fin. dagboeken** in en kies vervolgens de gerelateerde koppeling.  
5. Maak een eerste dagboekregel en vul de velden indien nodig in.
6. In het veld **VA-boekingssoort** selecteert u **Onderhoud**.
7. Kies de actie **VA-tegenrekening invoegen**. Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de boeking van het onderhoud is ingesteld.

    > [!NOTE]  
    > Stap 7 werkt alleen als u het volgende hebt ingesteld: op de pagina **VA-boekingsgroep** voor de boekingsgroep van het vaste activum bevat het veld **Onderhoudskostenrekening** de grootboekdebetrekening en het veld **Tegenrekening onderhoud** bevat de grootboekrekening waarnaar u tegenrekeningsposten voor afschrijving wilt boeken. Zie [Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups) voor meer informatie.
8. Kies de actie **Boeken**.

## Onderhoudskosten vastleggen op een aankoopfactuur

In de volgende stappen wordt beschreven hoe u onderhoudskosten voor een vast activum kunt vastleggen op een inkoopfactuur. De stappen zijn vergelijkbaar voor inkooporders.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Voer **Inkoopfactuur** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden op het sneltabblad **Algemeen** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies **Vast activum** in het veld **Soort** op het sneltabblad **Regels**.
4. In het veld **Nr.** kiest u het activum en u geeft vervolgens de hoeveelheid en de kosten op.
5. In het veld **VA-boekingssoort** kiest u **Onderhoud**.
6. Boek de inkoopfactuur.

## Follow-up op onderhoudsbeurten

U kunt het rapport **Onderhoud - Volgende beurt** afdrukken om na te gaan voor welke activa er een onderhoudsbeurt is gepland. U kunt dit rapport ook gebruiken bij het bijwerken van het veld **Volgende onderhoudsbeurt** op kaarten voor vaste activa.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Onderhoud - Volgende beurt** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden **Begindatum** en **Einddatum** in.  
3. Kies de knop **Afdrukken** of **Voorbeeld**.

## Onderhoudskosten controleren

U kunt statistieken bekijken om onderhoudskosten te monitoren.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum waarvoor u onderhoudskosten wilt bekijken en kies vervolgens de actie **Afschrijvingsboeken**.
3. Op de pagina **Afschrijvingsboeken voor vaste activa** selecteert u het betreffende afschrijvingsboek voor vaste activa en kiest u vervolgens de actie **Statistieken**.
4. Kies op de pagina **VA-statistiek** het veld **Onderhoud**.

Gebruik de pagina **Onderhoudsposten** om de posten te zien die het bedrag in het veld **Onderhoud** vormen.

## Onderhoudskosten voor meerdere vaste activa weergeven of afdrukken

In het rapport **Onderhoud - Analyse** kunt u aangeven of u onderhoud van één, twee of drie onderhoudscodes wilt zien voor een specifieke datum of periode. Het rapport kan het totaal tonen van alle geselecteerde activa of het totaal voor elk activum.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Onderhoud - Analyse** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in.
3. Kies de knop **Afdrukken** of **Voorbeeld**.

## Onderhoudsposten bekijken

U kunt ook de onderhoudsposten verkennen door de onderhoudsposten te bekijken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum waarvoor u posten wilt bekijken en kies vervolgens de actie **Afschrijvingsboeken**.
3. Op de pagina **Afschrijvingsboeken voor vaste activa** selecteert u het betreffende afschrijvingsboek voor vaste activa en kiest u vervolgens de actie **Onderhoudsposten**.

## Onderhoudsposten voor meerdere vaste activa weergeven of afdrukken

In het rapport **Onderhoud - Details** kunt u onderhoudsposten voor een of meerdere vaste activa afdrukken of weergeven.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Onderhoud - Details** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in.
3. Kies de knop **Afdrukken** of **Voorbeeld**.

## Zie ook

[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
