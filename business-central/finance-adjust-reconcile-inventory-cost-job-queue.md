---
title: Taken plannen voor het aanpassen en afstemmen van voorraadkosten
description: Leer hoe u de taakwachtrij kunt gebruiken om de taken voor het aanpassen van voorraadkosten of het afstemmen met het grootboek naar de achtergrond te verplaatsen. Bijvoorbeeld als uw bedrijf veel taken uitvoert of veel transacties verwerkt.
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: 461
ms.date: 09/19/2023
ms.author: bholtorf
---
# Taken plannen voor het aanpassen en afstemmen van voorraadkosten

Projecten plannen voor automatische kostenaanpassing met het grootboek en boeking naar het grootboek zijn standaard ingeschakeld.
Aangezien gegevens zich in de loop van de tijd ophopen, kan dit echter van invloed zijn op de prestaties. Om de belasting van de toepassing te verminderen, is het vaak handig om opdrachten in de wachtrij te gebruiken om taken op de achtergrond uit te voeren.

## Verplaats de taak van het aanpassen van artikelkosten naar de achtergrond met behulp van begeleide instelling

Het maken van de taakwachtrij-items kan lastig zijn, zelfs voor een ervaren consultant, dus we hebben een begeleide instelling om het proces voor het aanpassen van de artikelkosten te vergemakkelijken.  

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraad instellen** in en kies de desbetreffende koppeling.  
2. Schakel op de pagina **Voorraadinstellingen** het veld **Automatische kostenboeking** in of specificeer **Nooit** in het veld **Automatische kostenwaardering**.  
3. Kies in de melding die nu boven aan de pagina wordt weergegeven de koppeling **Taakwachtrij-item plannen**. Dit opent de begeleide instelling **Herwaardering en boeking van kosten plannen**.  
4. Geef de taak op die u wilt plannen.  

  > [!NOTE]
  > U kunt geen nieuw taakwachtrij-item maken als er al een taakwachtrij-item voor de opgegeven taak bestaat.

5. Selecteer het veld **De taakwachtrijposten weergeven wanneer het gereed is** om instellingen te bekijken en aan te passen. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).  

## Een taakwachtrij-item maken voor het handmatig aanpassen en afstemmen van voorraadkosten

U kunt ook handmatig taakwachtrij-items maken. De volgende procedure laat zien hoe u de batchverwerking **Kostprijs herwaarderen - Artikelposten** instelt om automatisch dagelijks te worden uitgevoerd, maar dezelfde stappen zijn van toepassing op de batchverwerking **Voorraadwaarde boeken naar GB**.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Taakwachtrijposten** in en kies de desbetreffende koppeling.  
2. Kies de actie **Nieuw**.  
3. Kies in het veld **Uit te voeren objecttype** *Rapport*.  
4. Kies in het veld **Uit te voeren object-id** *795*, **Kostprijs herwaarderen - Artikelposten**.  
5. Voer in het veld **Formule voor volgende uitvoeringsdatum** *1D* in.
6. Voer in het veld **Begintijd** *2 AM* in.
7. Kies de actie **Status instellen op Gereed**.

Nu worden de voorraadkosten elke nacht bijgewerkt.  

Om een taak te plannen voor het afstemmen van voorraad met het grootboek, kiest u Codeunit 2846 **Voorraadwaarde boeken naar GB**.

> [!TIP]
> Plan om vergrendeling te voorkomen niet tegelijkertijd taken voor de batchverwerking **Kostprijs herwaarderen - Artikelposten**, de codeunit **Voorraadwaarde boeken naar GB** en taken voor het boeken van verkoop- of inkooptransacties. Zorg er ook voor dat ze dezelfde taakwachtrijcategorie gebruiken.

## Zie ook

[Artikelprijzen herwaarderen](inventory-how-adjust-item-costs.md)  
[Voorraadkosten reconciliëren met het grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
