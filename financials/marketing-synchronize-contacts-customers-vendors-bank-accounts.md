---
title: Contacten synchroniseren met klanten en leveranciers| Microsoft Docs
description: "U koppelt of synchroniseert contactgegevens van contacten die tevens klanten, leveranciers of bankrekeningen zijn, zodat u de gegevens slechts op één locatie hoeft bij te werken."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2b85c52378a351dbc1a0809ec540b1f53c8074ef
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Contacten synchroniseren met klanten, leveranciers en bankrekeningen
Als sommige van uw contacten ook klanten, leveranciers of bankrekeningen zijn, kunt u de contactgegevens synchroniseren met de desbetreffende klant, leverancier of bankrekening. Synchronisatie maakt gegevens die gemeenschappelijk zijn voor contacten en klanten, leveranciers of bankrekeningen hetzelfde.  

Voordat u uw contacten kunt synchroniseren met klanten, leveranciers of bankrekeningen, moet u een zakenrelatiecode voor klanten, leveranciers en of bankrekeningen opgeven in het venster **Marketinginstellingen**. Zie voor meer informatie [CRM instellen](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Andere manieren om contacten te synchroniseren met klanten, leveranciers en bankrekeningen
U kunt de contacten met drie methoden synchroniseren met klanten, leveranciers en/of bankrekeningen:

* Contacten koppelen aan bestaande klanten, leveranciers en/of bankrekeningen op de contactkaart. Zie voor meer informatie [Contacten koppelen aan klanten, leveranciers en bankrekeningen](marketing-how-link-contact.md).
* Maak klanten,, leveranciers of bankrekeningen vanuit het contact. Zie voor meer informatie [Een klant, leverancier of bankrekening maken van een contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Contacten maken van klanten, leveranciers of bankrekeningen. Zie voor meer informatie [Een bedrijfscontact maken van een klant, leverancier of bankrekening](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Gevolgen van synchronisatie
Wanneer het contact wordt gesynchroniseerd met de klant-, leveranciers- of bankrekening:

* Hoeft u de gegevens slechts op één locatie bij te werken. Als u bijvoorbeeld het telefoonnummer op de contactkaart wijzigt, wordt het telefoonnummer automatisch bijgewerkt met dezelfde wijziging als van de klant, leveranciers of bankrekening.
* Als u een klanten-, leveranciers- of bankrekeningkaart maakt en een nummerreeks voor contacten hebt opgegeven, wordt er automatisch een contactkaart gemaakt voor de klant, leverancier of bankrekening.
* U kunt verkoopoffertes, inkoopoffertes, verkoop- en inkooporders maken vanuit het contact.
* U kunt uw interacties laten vastleggen wanneer u bepaalde acties uitvoert zoals orders, raamcontracten afdrukken, verkoopserviceorders maken, e-mailberichten verzenden, enzovoort.
* Als u een contact verwijdert dat aan een klant, leverancier of bankrekening is gekoppeld, wordt alleen het contact verwijderd. De klant, leverancier of bankrekening blijft.
* Als u een klant, leverancier of bankrekening verwijdert die aan een contact is gekoppeld, blijft het contact.

> [!NOTE]  
>   Sommige details, zoals facturerings- en boekingsgegevens, worden niet weergegeven op de contactkaart. Mogelijk wilt u deze handmatig toevoegen op de klanten-, leveranciers- of bankrekeningkaart wanneer u klanten, leveranciers of bankrekeningen van contacten maakt.

## <a name="see-also"></a>Zie ook
[Contactpersonen beheren](marketing-contacts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

