---
title: Statistiekrekeningen gebruiken voor het analyseren van niet-transactionele gegevens
description: Beschrijft hoe u statistische accounts gebruikt als een andere gegevensbron voor uw analyses.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
---
# <a name="analyze-data-with-statistical-accounts"></a><a name="analyze-data-with-statistical-accounts"></a>Gegevens analyseren met statistiekrekeningen

Gebruik statistiekrekeningen om informatie in financiële rapporten aan te vullen. Met statistiekrekeningen kunt u statistieken toevoegen die zijn gebaseerd op niet-transactionele gegevens. U voegt de niet-transactionele gegevens toe als op getallen gebaseerde eenheden, zoals:

* Personeelsbezetting
* Vierkante meters
* Het aantal klanten met achterstallige rekeningen

U kunt bijvoorbeeld opbrengsten of kosten meten op basis van het aantal mensen op een afdeling. Het personeelsbestand van de afdeling is de eenheid voor de statistiekrekening. De volgende afbeelding toont een voorbeeld van een rapport dat een statistiekrekening gebruikt om de omzet per werknemer weer te geven.

:::image type="content" source="media/statistical account report example.png" alt-text="Een voorbeeld van een rapport met gegevens uit een statistiekrekening.":::

In termen van hoe ze werken, zijn statistiekrekeningen vergelijkbaar met boekingsrekeningen. Ze slaan transacties op die u boekt met behulp van statistiekrekeningjournalen, zodat u de transacties kunt gebruiken als gegevens voor financiële rapporten. Als u meer wilt weten over financiële rapporten, gaat u naar [Financial Reporting voorbereiden met financiële gegevens en accountcategorieën](bi-how-work-account-schedule.md). 

Er is een aantal belangrijke verschillen tussen statistiekrekeningen en boekingsrekeningen. Statistiekrekeningen zijn afzonderlijke entiteiten en worden niet opgenomen in proefbalansrapporten. Ook hoeft u debet- en creditbedragen niet in evenwicht te brengen wanneer u statistiekrekeningjournalen gebruikt om posten naar een statistiekrekening te boeken. U boekt gewoon het bedrag.

## <a name="set-up-a-statistical-account"></a><a name="set-up-a-statistical-account"></a>Een nieuwe statistiekrekening instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Statistiekrekeningen** in en kies vervolgens de gerelateerde koppeling.
1. Vul de velden op het sneltabblad **Algemeen** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="post-amounts-to-a-statistical-account"></a><a name="post-amounts-to-a-statistical-account"></a>Bedragen op een statistiekrekening

1. Om de bedragen die u wilt volgen te boeken kiest u op de pagina **Statistiekrekeningen** de actie **Dagboek van statistiekrekeningen**.
1. Voer in het veld **Boekingsdatum** de laatste datum in van de boekingsperiode waarvoor u bedragen wilt boeken.
1. Optioneel: als u bedragen voor een specifiek document wilt bijhouden, voert u in het veld **Documentnr.** de id van het document in.
1. Kies in het veld **Nr. van statistiekrekening** de statistiekrekening waarop u bedragen wilt boeken.
1. Typ in het veld **Beschrijving** een korte beschrijving van wat u meet.  
1. Voer in het veld **Bedrag** het bedrag in dat u wilt boeken. 
1. Optioneel: als u de statistiekrekening wilt opnemen in meer geavanceerde analyses, geeft u dimensies op in de velden **Afdelingscode** en **Code klantengroep**. Ga voor meer informatie over dimensies naar [Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md).

## <a name="verify-statistical-account-amounts"></a><a name="verify-statistical-account-amounts"></a>Bedragen op een statistiekrekening controleren

Gebruik op de pagina **Statistiekrekeningen** de actie **Saldo van statistiekrekening** om te controleren of de geregistreerde bedragen voor elke periode correct zijn.  

## <a name="include-the-statistical-account-in-a-financial-report"></a><a name="include-the-statistical-account-in-a-financial-report"></a>De statistiekrekening opnemen in een financieel rapport

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.
1. Maak een nieuw financieel rapport op een van de volgende manieren:
    1. Kies **Nieuw** om helemaal opnieuw te beginnen. Ga voor meer informatie over het maken van financiële rapporten naar [Een nieuw financieel rapport maken](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Als u instellingen wilt gebruiken van een vergelijkbaar rapport dat u al hebt, kiest u het rapport dat u wilt kopiëren, en kiest u vervolgens de actie **Financieel rapport kopiëren** . U kunt de instellingen die u in uw nieuwe rapport kopieert, bewerken.
1. De statistiekrekening toevoegen:
    1. Als u helemaal opnieuw begint, kiest u de actie **Rijdefinitie bewerken**.
    1. Als u een rijdefinitie uit een bestaand rapport wilt gebruiken, kiest u het rapport waaruit u wilt kopiëren en kiest u vervolgens de actie **Rijdefinitie kopiëren** .
1. Definieer op de pagina **Rijdefinitie** in het veld **Rijnr.** waar de rij zal verschijnen in de reeks rijen in het rapport.
1. Typ in het veld **Beschrijving** een korte tekst die aangeeft wat u meet.
1. Kies in het veld **Samentellingssoort** de optie **Statistiekrekeningen**.
1. Kies in het veld **Samentellingssoort** een statistiekrekening.
1. Kies in het veld **Rijtype** of u het saldo op de boekingsdatum of het begin van de boekingsperiode wilt bekijken, of dat u de wijziging van het bedrag tijdens de periode wilt weergeven.
1. Vul de overige velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Financiële bedrijfsinformatie](bi.md)  
[Financiële rapporten en analyses in Business Central](finance-reports.md)
