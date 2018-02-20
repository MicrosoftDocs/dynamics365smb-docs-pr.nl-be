---
title: Contactbedrijven maken| Microsoft Docs
description: Beschrijft hoe u een contact maakt voor elk nieuw bedrijf of potentieel bedrijf waarmee u contact onderhoudt of een relatie hebt.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="create-contact-companies"></a>Contactbedrijven maken
U kunt een contactkaart maken voor elk nieuw bedrijf waarmee u een zakelijke relatie hebt, bijvoorbeeld een klant, leverancier, potentiële klant, bank, advocatenkantoor, consultant, enzovoort.

Er zijn twee manieren om een contact maken: volledig nieuw of van een bestaande klant, leverancier of bankrekening.,

Voordat u een contact maakt, kunt u de instellingen controleren in het venster **Marketinginstellingen**. Zie voor meer informatie [CRM instellen](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Een geheel nieuw bedrijfscontact maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Contacten** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Voer in het veld **Nr.** een nummer in voor het contact.

    Als u echter een nummerreeks voor contacten hebt ingesteld in het venster **Marketinginstellingen** kunt u op Enter drukken om het volgende beschikbare contactnummer te selecteren.  
4. Stel **Soort** in op **Bedrijf**.
5. Vul de overige velden in.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Een bedrijfscontact maken van een klant, leverancier of bankrekening
Als u al een aantal klanten, leveranciers of bankrekeningen hebt ingesteld, kunt u contacten maken op basis van de bestaande gegevens. Wanneer u op deze manier een contact maakt, worden de contactgegevens gesynchroniseerd met de klant-, leveranciers- of bankrekeninginformatie.

> [!NOTE]  
>   Voordat u op deze manier contactbedrijven kunt maken, moet u een zakenrelatiecode opgeven voor klanten, leveranciers en bankrekeningen in het venster **Marketinginstellingen**. Als u contacten van bankrekeningen maakt, moet u ook nummers opgeven voor bankrekeningen in het venster **Grootboekinstellingen**.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer een van de volgende in, afhankelijk van waar u contacten wilt maken, en klik vervolgens op de gerelateerde koppeling.
   * **Contacten maken van klanten**
   * **Contacten maken van leveranciers**
   * **Contacten maken van bankrekeningen**
2. Stel in het batchverwerkingsvenster dat wordt geopend, in het gedeelte **Klant**, **Leverancier** of **Bankrekening** filters in als u contacten van bepaalde klanten, leveranciers of bankrekeningen wilt maken.
3. Kies **OK** om het maken van contacten te starten.

    De volgende contactnummers in de nummerreeks worden aan de nieuwe contacten toegewezen. De zakenrelatie voor leveranciers die in het venster **Marketinginstellingen** is opgegeven, wordt toegewezen aan de nieuwe contacten.

> [!TIP]  
>   U kunt ook een klant, leverancier of bankrekening maken van een contact. Zie voor meer informatie [Een klant, leverancier of bankrekening maken van een contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Zie ook
[Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Zakenrelaties toewijzen aan een contact](marketing-business-relations.md#AssignBusRelContact)  
[Sectoren toewijzen aan een contact](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Mailinggroepen aan een contact toewijzen](marketing-mailing-groups.md#AssignMailGroupContact)  
[Contacten maken](marketing-create-contact-persons.md)  
[Werken met Finance and Operations, Business edition](ui-work-product.md)

