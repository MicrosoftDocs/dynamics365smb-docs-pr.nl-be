---
title: Opbrengsten en kosten toewijzen aan meerdere grootboekrekeningen
description: Leer hoe u kosten kunt toewijzen aan een of meer rekeningen in uw grootboek.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Opbrengsten en kosten toewijzen aan meerdere grootboekrekeningen

In dit artikel wordt beschreven hoe u toewijzingsrekeningen kunt gebruiken om bedragen in verkoop- en inkoopdocumenten en dagboekregels naar verschillende grootboekrekeningen te verdelen. U kunt bedragen toewijzen via een vaste of variabele verdeling.  

Toewijzing splitst een dagboekregel op in de regels die zijn gedefinieerd op de pagina **Toewijzingsrekening**. Als u bijvoorbeeld huurkosten in drieën splitst met behulp van dimensies, moet u drie regels boeken voor de toewijzing. U beschikt dus over zes grootboekregels (of mogelijk meer als u btw of sales tax gebruikt). Hoewel hierdoor meer grootboekposten worden geboekt dan u nodig heeft, kunt u hiermee afzonderlijke regels tegenboeken in plaats van de hele toewijzing.

Toewijzingsrekeningen werken ook met uitstel. Ga voor meer informatie over uitstel naar [Inkomsten en kosten uitstellen](finance-how-defer-revenue-expenses.md).

In de volgende tabel worden de toewijzingsmethoden beschreven die u kunt gebruiken.

|Toewijzingsmethode  |Omschrijving  |
|---------|---------|
|Vast     | Als u de kosten wilt opsplitsen op een manier die zich over een langere periode herhaalt, kunt u een vaste toewijzing gebruiken. Bij een vaste toewijzing kunt u de opsplitsing van de toewijzing definiëren. Deze opsplitsing verandert alleen als u de instellingen wijzigt op de pagina **Toewijzingsrekening**.        |
|Variabel     | Als u inkomsten of kosten wilt verdelen op basis van waarden die in de loop van de tijd veranderen, gebruikt u de variabele toewijzingsmethode. Met variabele toewijzingen kunt u de bronnen opgeven die u wilt gebruiken om de toewijzingspercentages te berekenen. Deze methode is bijvoorbeeld handig voor het splitsen van personeelskosten op basis van verschillende personeelsaantallen in afdelingen of divisies. Een ander voorbeeld is het verdelen van de huurkosten op basis van productievloerafmetingen die in de loop van de tijd per productielijn kunnen variëren. Variabele toewijzingen gebruiken een combinatie van dimensies en statistiekrekeningen om te bepalen hoe bedragen over een bepaalde periode worden verdeeld. Ga voor meer informatie over statistiekrekeningen naar [Gegevens analyseren met statistiekrekeningen](bi-use-statistical-accounts.md). Ga voor meer informatie over dimensies naar [Werken met dimensies](finance-dimensions.md).        |

## Een vastdeel- of percentagemethode gebruiken om bedragen toe te wijzen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingsrekening** in en kies de gerelateerde koppeling.  
1. Kies op de pagina **Toewijzingsrekeningen** de actie **Nieuw**.
1. Vul het veld **Nr.** en het veld **Naam** in.
1. Kies **Vast** in het veld **Rekeningsoort**.
1. Kies in het veld **Soort bestemmingsrekening** **Grootboekrekening** of **Bankrekening**.
1. Kies in het veld **Nummer van bestemmingsrekening** de rekening waarnaar u de waarde wilt boeken.
1. Optioneel: kies de actie **Dimensies** en geef vervolgens de dimensies op die u voor de regel wilt boeken.
1. Geef in de velden **Deel** en **Percentage** op hoe bedragen naar de bestemmingsrekening moeten worden verdeeld.
  
   > [!TIP]
   > Als u in het veld **Deel** het daadwerkelijke bedrag invoert dat u wilt toewijzen voor een vaste toewijzing, wordt in het veld **Percentage** het percentage van het totaalbedrag weergegeven.
1. Herhaal dit proces voor elke rekening die u in de toewijzing wilt opnemen.

## Gebruik een variabele methode om bedragen toe te wijzen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingsrekening** in en kies de gerelateerde koppeling.  
1. Kies op de pagina **Toewijzingsrekeningen** de actie **Nieuw**.
1. Vul het veld **Nr.**, en het veld **Naam** in.
1. Kies **Variabele** in het veld **Rekeningsoort**.
1. Kies **Grootboekrekening** in het veld **Soort bestemmingsrekening**.
1. Kies in het veld **Nummer van bestemmingsrekening** de rekening waarnaar u de waarde wilt boeken.
1. Kies **Statistiekrekening** in het veld **Soort opsplitsingsrekening**.
1. In het veld **Berekeningsperiode** kiest u de periode waarover u bedragen wilt verdelen.
1. Optioneel: als u op specifieke globale dimensiewaarden wilt filteren, kiest u de actie **Saldofilters van uitsplitsingsrekening** en geeft u vervolgens de filterwaarden op.
1. Optioneel: kies de actie **Dimensies** en geef vervolgens de dimensies op die u voor de regel wilt boeken.

## Bedragen ter plekke toewijzen

U maakt toewijzingsrekeningen om opbrengsten en kosten te splitsen voor grootboekrekeningen en bankrekeningen. Het automatiseren van toewijzingen kan tijd besparen. Als u echter toewijzingsrekeningen wilt gebruiken, maar deze niet voor elke grootboekrekening wilt maken, kunt u nog meer tijd besparen.

Met de optie Overnemen van bovenliggend element kunt u de toewijzingsrekening gebruiken om bedragen te splitsen voor elke grootboekrekening op een regel in een document of dagboek. In het veld **Rekeningsoort** op een document- of dagboekregel kiest u een grootboekrekening en vervolgens kiest u de toewijzingsrekening in het veld **Toewijzingsrekeningnr.**. Het bedrag op de regel wordt voor de grootboekrekening gesplitst volgens de instelling in uw toewijzingsrekening. Het is een minder transparante manier van toewijzen, maar u hoeft geen toewijzingsrekening specifiek voor de grootboekrekening te maken.

Ad-hoc toewijzingen zijn eenvoudig in te stellen. In plaats van een bank- of grootboekrekening op te geven in het veld **Soort bestemmingsrekening** op de pagina **Toewijzingsrekening** kiest u de optie **Overnemen van bovenliggend element**. Laat het veld **Nummer van bestemmingsrekening** leeg. Wanneer u de grootboekrekening op de document- of dagboekregel kiest, wordt die rekening gebruikt om bedragen toe te wijzen.

## Controleren of de bedragen correct worden verdeeld voordat u ze boekt

Er is een aantal manieren om te controleren of de bedragen correct worden verdeeld:

* Kies op de pagina **Toewijzingsrekening** de actie **Testtoewijzing**. Gebruik het veld **Toe te wijzen bedrag** om verschillende bedragen te testen.
* Kies op de pagina **Grootboeken** het dagboek en gebruik vervolgens de actie **Voorbeeld van boeking weergeven**.

## De verdeling aanpassen

Als u iets in een toewijzing vindt dat u wilt wijzigen, kunt u de toewijzing aanpassen voordat u deze boekt.  

1. Open het document of dagboek met de toewijzing die u wilt wijzigen.
1. Kies de regel en kies vervolgens de actie **Rekeningtoewijzingen opnieuw verdelen**.
1. Voer op de pagina **Toewijzingen wijzigen** uw aanpassing uit.

## Een toewijzingstransactie boeken

In de volgende stappen wordt beschreven hoe u een toewijzingstransactie vanuit een dagboek boekt. De stappen zijn hetzelfde voor verkoop- en inkoopdocumenten.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies de desbetreffende koppeling.  
1. Een nieuwe regel maken. Vul de velden op dezelfde manier in als voor elk ander type dagboek.
1. Als u gebruik maakt van een vaste of variabele toewijzing, vult u de volgende velden in:
    1. Kies in het veld **Rekeningsoort** **Toewijzingsrekening**.
    1. Kies in het veld **Rekeningnr.** de toewijzingsrekening.
1. Als u een toewijzing gebruikt die de optie Overnemen van bovenliggend element gebruikt, doet u het volgende:
    1. Kies in het veld **Rekeningsoort** **Grootboekrekening**.
    1. Kies in het veld **Rekeningnr..** de grootboekrekening.
    1. Kies in het veld **Toewijzingsrekeningnr.** de toewijzingsrekening die is ingesteld voor het gebruik van de optie Overnemen van bovenliggend element. 
1. Kies **Boeken**.

## Zie ook

[Werken met dagboeken](ui-work-general-journals.md)  