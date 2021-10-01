---
title: Kosten afstemmen met grootboekrekeningen aanpassen met taakwachtrij
description: Leer hoe u de taakwachtrij kunt gebruiken om de taken voor het aanpassen van voorraadkosten of het afstemmen met het GB naar de achtergrond kunt verplaatsen. Bijvoorbeeld als uw bedrijf veel taken uitvoert of veel transacties verwerkt.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 07/28/2021
ms.author: andreipa
ms.openlocfilehash: e44936d9d9ec39d9232285d7293c152c57ab0a56
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688475"
---
# <a name="adjust-and-reconcile-inventory-cost-with-general-ledger-with-job-queue"></a>Voorraadkosten aanpassen en afstemmen met grootboek met taakwachtrij

Om de ervaring te optimaliseren zijn automatische kostenaanpassing en boeking naar het grootboek standaard ingeschakeld. Aangezien gegevens zich in de loop van de tijd ophopen, kan dit echter van invloed zijn op de prestaties. Om de belasting van de toepassing te verminderen, is het vaak handig om opdrachten in de wachtrij te gebruiken om taken op de achtergrond uit te voeren.

## <a name="move-the-task-of-adjusting-item-costs-to-the-background-with-the-help-of-assisted-setup"></a>Verplaats de taak van het aanpassen van artikelkosten naar de achtergrond met behulp van begeleide instelling

Het maken van de taakwachtrij-items kan lastig zijn, zelfs voor een ervaren consultant, dus we hebben een begeleide instelling om het proces voor het aanpassen van de artikelkosten te vergemakkelijken. 

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraad instellen** in en kies de desbetreffende koppeling.  
2. Schakel op de pagina **Voorraadinstellingen** het veld **Automatische kostenboeking** in of specificeer **Nooit** in het veld **Automatische kostenwaardering**.  
3. Kies in de melding die nu boven aan de pagina wordt weergegeven de koppeling **Taakwachtrij-item plannen**.
4. Geef de taak op die u wilt plannen.  

  > [!NOTE]
  > U kunt geen nieuw taakwachtrij-item maken als er al een taakwachtrij-item voor de opgegeven taak bestaat. 
5. Selecteer het veld **De taakwachtrijposten weergeven wanneer het gereed is** om instellingen te bekijken en aan te passen. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-job-queue-entry-for-adjusting-and-reconciling-inventory-cost-manually"></a>Een taakwachtrij-item maken voor het handmatig aanpassen en afstemmen van voorraadkosten

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


> [!NOTE]
> Plan om vergrendeling te voorkomen niet tegelijkertijd taken voor de batchverwerking **Kostprijs herwaarderen - Artikelposten**, de codeunit **Voorraadwaarde boeken naar GB** en taken voor het boeken van verkoop- of inkooptransacties, en zorg ervoor dat ze dezelfde taakwachtrijcategorie gebruiken.

## <a name="see-also"></a>Zie ook

[Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md)  
[Voorraadkosten reconciliëren met het grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  