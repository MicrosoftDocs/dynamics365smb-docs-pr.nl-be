---
title: Contactbedrijven maken | Microsoft Docs
description: Beschrijft hoe u contactbedrijven maakt in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bd8dfb8abc9387ad6b9c500f25feb181878b6cfe
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="create-contact-companies"></a>Contactbedrijven maken
U kunt een contactkaart maken voor elk nieuw bedrijf waarmee u een zakelijke relatie hebt, bijvoorbeeld een klant, leverancier, potentiële klant, bank, advocatenkantoor, consultant, enzovoort.

Er zijn twee manieren om een contact maken: volledig nieuw of van een bestaande klant, leverancier of bankrekening.,

Voordat u een contact maakt, kunt u de instellingen controleren in het venster **Marketinginstellingen**. Zie voor meer informatie [CRM instellen](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Een geheel nieuw bedrijfscontact maken
1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Contacten** in en klik op de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Voer in het veld **Nr.** een nummer in voor het contact.

    Als u echter een nummerreeks voor contacten hebt ingesteld in het venster **Marketinginstellingen** kunt u op Enter drukken om het volgende beschikbare contactnummer te selecteren.  
4. Stel **Soort** in op **Bedrijf**.
5. Vul de overige velden in.

## <a name="create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Een bedrijfscontact maken van een klant, leverancier of bankrekening
Als u al een aantal klanten, leveranciers of bankrekeningen hebt ingesteld, kunt u contacten maken op basis van de bestaande gegevens. Wanneer u op deze manier een contact maakt, worden de contactgegevens gesynchroniseerd met de klant-, leveranciers- of bankrekeninginformatie.

**Opmerking**: voordat u op deze manier contactbedrijven kunt maken, moet u een zakenrelatiecode opgeven voor klanten, leveranciers en bankrekeningen in het venster **Marketinginstellingen**. Als u contacten van bankrekeningen maakt, moet u ook nummers opgeven voor bankrekeningen in het venster **Grootboekinstellingen**.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Zoeken naar pagina of rapport"), voert een van de volgende waarden in (afhankelijk vanwaar u contacten wilt aanmaken) en kies vervolgens de gerelateerde koppeling.
   * **Contacten maken van klanten**
   * **Contacten maken van leveranciers**
   * **Contacten maken van bankrekeningen**
2. Stel in het batchverwerkingsvenster dat wordt geopend, in het gedeelte **Klant**, **Leverancier** of **Bankrekening** filters in als u contacten van bepaalde klanten, leveranciers of bankrekeningen wilt maken.
3. Kies **OK** om het maken van contacten te starten.

    De volgende contactnummers in de nummerreeks worden aan de nieuwe contacten toegewezen. De zakenrelatie voor leveranciers die in het venster **Marketinginstellingen** is opgegeven, wordt toegewezen aan de nieuwe contacten.

**Tip**: u kunt ook een klant, leverancier of bankrekening maken van een contact. Zie voor meer informatie [Een klant, leverancier of bankrekening maken van een contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Zie ook
[Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Zakenrelaties toewijzen aan een contact](marketing-business-relations.md#AssignBusRelContact)  
[Sectoren toewijzen aan een contact](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Mailinggroepen aan een contact toewijzen](marketing-mailing-groups.md#AssignMailGroupContact)  
[Procedure: Contactpersonen maken](marketing-create-contact-persons.md)  
[Werken met Financials](ui-work-product.md)

