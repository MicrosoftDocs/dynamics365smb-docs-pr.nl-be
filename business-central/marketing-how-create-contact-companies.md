---
title: Contactbedrijven maken| Microsoft Docs
description: Beschrijft hoe u een contact maakt voor elk nieuw bedrijf of potentieel bedrijf waarmee u contact onderhoudt of een relatie hebt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 67945b8825ae94ff3a09a4072309c401abb41c6b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "920994"
---
# <a name="create-contacts"></a>Contacten maken
U kunt een contactkaart maken voor elk nieuw bedrijf waarmee u een zakelijke relatie hebt, bijvoorbeeld een klant, leverancier, potentiële klant, bank, advocatenkantoor, consultant, enzovoort.

Er zijn twee manieren om een contact maken: volledig nieuw of van een bestaande klant, leverancier of bankrekening.,

## <a name="create-a-company-contact-from-scratch"></a>Een geheel nieuw bedrijfscontact maken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contacten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Voer in het veld **Nr.** een nummer in voor het contact.

    Als u echter een nummerreeks voor contacten hebt ingesteld op de pagina **Marketinginstellingen** kunt u op Enter drukken om het volgende beschikbare contactnummer te selecteren.  
4. Stel **Soort** in op **Bedrijf**.
5. Vul de overige velden in.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Een bedrijfscontact maken van een klant, leverancier of bankrekening
Als u al een aantal klanten, leveranciers of bankrekeningen hebt ingesteld, kunt u contacten maken op basis van de bestaande gegevens. Wanneer u op deze manier een contact maakt, worden de contactgegevens gesynchroniseerd met de klant-, leveranciers- of bankrekeninginformatie.

> [!NOTE]  
>   Voordat u op deze manier contactbedrijven kunt maken, moet u een zakenrelatiecode opgeven voor klanten, leveranciers en bankrekeningen op de pagina **Marketinginstellingen**. Als u contacten van bankrekeningen maakt, moet u ook nummers opgeven voor bankrekeningen op de pagina **Grootboekinstellingen**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer een van de volgende in, afhankelijk van waaruit u contacten wilt maken en kies vervolgens de gerelateerde koppeling.
   * **Contacten maken van klanten**
   * **Contacten maken van leveranciers**
   * **Contacten maken van bankrekeningen**
2. Stel op de batchverwerkingspagina die wordt geopend, in het gedeelte **Klant**, **Leverancier** of **Bankrekening** filters in als u contacten van bepaalde klanten, leveranciers of bankrekeningen wilt maken.
3. Kies **OK** om het maken van contacten te starten.

    De volgende contactnummers in de nummerreeks worden aan de nieuwe contacten toegewezen. De zakenrelatie voor leveranciers die op de pagina **Marketinginstellingen** is opgegeven, wordt toegewezen aan de nieuwe contacten.

> [!TIP]  
>   U kunt ook een klant, leverancier of bankrekening maken van een contact. Zie voor meer informatie [Een klant, leverancier of bankrekening maken van een contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Zie ook
[Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Zakenrelaties toewijzen aan een contact](marketing-business-relations.md#AssignBusRelContact)  
[Sectoren toewijzen aan een contact](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Mailinggroepen aan een contact toewijzen](marketing-mailing-groups.md#AssignMailGroupContact)  
[Contacten maken](marketing-create-contact-persons.md)  
[Werken met Business Central](ui-work-product.md)
