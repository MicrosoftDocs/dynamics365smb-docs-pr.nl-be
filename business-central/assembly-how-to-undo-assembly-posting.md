---
title: Boeken van assemblage ongedaan maken
description: Ontdek hoe u fouten in een geboekte assemblyorder kunt corrigeren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="undo-assembly-posting" />Boeken van assemblage ongedaan maken

Maak de boeking van een assemblageorder ongedaan om een fout te corrigeren of een ongewenste boeking te verwijderen.

Wanneer u een geboekte assemblageorder ongedaan wilt maken, worden er corrigerende artikelposten gemaakt om de oorspronkelijke posten terug te draaien. Elke positieve uitvoerpost voor het assemblageartikel wordt via een negatieve uitvoerpost teruggedraaid. Elk negatieve verbruiksartikelpost voor een assemblagecomponent wordt via een positieve verbruikspost teruggedraaid. Er wordt automatisch een vaste kostenvereffening gemaakt tussen de corrigerende en de oorspronkelijke posten om een exacte kostenterugboeking te garanderen.  

Wanneer u een volledig geboekte assemblageorder ongedaan maakt, kunt u de oorspronkelijke order opnieuw maken. Bijvoorbeeld om correcties aan te brengen voordat u de order opnieuw boekt.  

Wanneer u een gedeeltelijk geboekte assemblyorder ongedaan maakt, worden vervolgens alle betrokken velden, zoals de velden **Geassembleerde hoeveelheid**, **Verbruikt aantal** en **Resterend aantal**, opnieuw ingesteld op de waarden die deze hadden voordat de boeking werd uitgevoerd.  

Als u assemblageorders opnieuw wilt maken of wilt terugzetten, moet het artikel in de oorspronkelijke boeking voldoen aan de volgende voorwaarden:  

* Het is nog steeds in voorraad. Dat wil zeggen, het is niet verkocht of anderszins verbruikt door uitgaande transacties.  
* Het is niet gereserveerd.  
* Het artikel moet bestaan op de opslaglocatie waarnaar het is uitgevoerd.  

Assemblageorders kunnen alleen worden hersteld als het aantal en de volgorde van regels op de oorspronkelijke assemblageorder niet is gewijzigd.  

> [!TIP]  
> Als u conflicten ten gevolge van regelwijzigingen wilt oplossen, kunt de wijzigingen op de desbetreffende regels handmatig ongedaan maken voordat u de bijbehorende assemblageorder boekt. U kunt de assemblageorder boeken en deze vervolgens opnieuw maken wanneer u de boeking ongedaan maakt.  

De volgende procedure beschrijft het ongedaan maken van geboekte assemblyorders die artikelen bevatten die zijn geassembleerd naar voorraad. Gebruik de actie **Verzending ongedaan maken** op de gerelateerde geboekte zending om geboekte assemblyorders met artikelen die op bestelling zijn geassembleerd, ongedaan te maken. Ga voor meer informatie over het ongedaan maken van verzendingen naar [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md). Ongedaan maken van de geboekte assemblyorder geschiedt vervolgens op dezelfde wijze als in dat artikel beschreven.  

## <a name="to-undo-posting-of-an-assembly-order" />Het boeken van een assemblageorder ongedaan maken

U kunt geboekte assemblyorders geheel of gedeeltelijk ongedaan maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Geboekte assemblyorders** in en kiest u vervolgens de gerelateerde koppeling  

   Elke gedeeltelijke boeking leidt tot het maken van een afzonderlijk geboekte assemblageorder.  
2. Open de geboekte assemblyorder die u ongedaan wilt maken en kies vervolgens de actie **Assemblage ongedaan maken**.  

    Als de geboekte assemblyorder is gerelateerd aan een volledig geboekte assemblyorder die is verwijderd, kunt u de verwijderde order opnieuw maken. U kunt de order bijvoorbeeld opnieuw maken omdat u deze opnieuw wilt verwerken.  
3. Kies **Ja** om de assemblageorder opnieuw te maken. Kies **Nee** als u de boeking ongedaan wilt maken zonder de bijbehorende assemblageorder opnieuw te maken.  

Het veld **Tegengeboekt** in de assemblageorder verandert in **Ja**. De boeking van de assemblageorder is nu tegengeboekt. U kunt de volledige assemblageorder verwerken als u ervoor kiest om deze opnieuw te maken, of de openstaande assemblageorder die u in de oorspronkelijke staat hebt hersteld.  

> [!NOTE]  
> Als u aantallen uit meerdere gedeeltelijke boekingen voor een assemblageorder wilt herstellen, moet u alle geboekte assemblyorders ongedaan maken door stappen 1 tot en met 3 uit te voeren.  

## <a name="see-also" />Zie ook

[Assemblagebeheer](assembly-assemble-items.md)  
[Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md)  
[Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
