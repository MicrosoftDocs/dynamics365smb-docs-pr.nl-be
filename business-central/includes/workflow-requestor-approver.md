---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Wanneer u gebruikers instelt voor goedkeuringswerkstromen, is het belangrijk dat dezelfde gebruiker niet zowel een aanvrager als een fiatteur is in een werkstroomgebruikersgroep. Wanneer een gebruiker zowel een aanvrager als een fiatteur is, werken goedkeuringen voor de gebruiker als volgt:

* Verzoeken van de gebruiker worden altijd automatisch goedgekeurd.
* Als er meerdere goedkeurders zijn, kunnen alleen de goedkeurders met een hoger volgnummer in de werkstroomgebruikersgroep de status van een aanvraag wijzigen in Goedgekeurd. Goedkeurders met een lager volgnummer kunnen verzoeken goedkeuren, maar hun goedkeuringen hebben geen invloed op de status van een verzoek.