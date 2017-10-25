---
title: Marketingcampagnes instellen in Financials | Microsoft Docs
description: Hier wordt beschreven hoe u marketingcampagnes in Dynamics 365 for Financials instelt en uitvoert om prospects te vinden en aan te trekken en klanten vast te houden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 996aca0dd46c350b5345d05e7fe320763b3caef4
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="managing-marketing-campaigns"></a>Marketingcampagnes beheren
Als u over een krachtig marketingplan beschikt, kunt u klanten vaststellen, aantrekken en vasthouden. Een marketingplan bestaat uit diverse campagnes en andere interacties in verband met uw verkoop- en marketingactiviteiten. Terwijl u een campagne plant, moet u bepalen op welke contacten u zich wilt richten, aan welk type campagne u de voorkeur geeft (zoals een beurs of direct mail) en welke verkopers elke taak uitvoeren.

Elke campagne bestaat uit diverse activiteiten en taken. U kunt meerdere taken combineren, bijvoorbeeld taken die elk een stap in activiteiten vertegenwoordigen. Activiteittaken worden gerelateerd aan elkaar met een datumformule. Afzonderlijke taken kunnen alleen worden toegewezen aan verkopers. Activiteiten kunnen aan opportunities, verkopers, groepen verkopers en contacten worden toegewezen. Zie voor meer informatie [Procedure: Opportunityverkoopcycli en cyclusfasen maken](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Afzonderlijke campagnes definiëren
Voordat u een campagne kunt maken, moet u *campagnestatuscodes* instellen. Met deze codes kunt u uw campagnes beheren door een status aan de campagne toe te wijzen. Terwijl u de fasen van een campagne doorloopt, kunt u bekijken in welke stap een campagne zich bevindt en wat de volgende stap is. U configureert campagnestatuscodes in het venster **Campagnestatus**.

U kunt een campagnekaart maken voor elke campagne die u wilt volgen. U kunt deze campagnekaarten ook weergeven als u algemene informatie over uw campagnes wilt bekijken.
U kunt campagneposten verwijderen, bijvoorbeeld als in de post een actie is geregistreerd die is geannuleerd. Alleen geannuleerde campagneposten kunnen worden verwijderd.

### <a name="selecting-the-target-audience"></a>De doelgroep kiezen
Nadat u een campagne hebt gemaakt, kunt u beginnen met het maken van segmenten die de doelgroep van de campagne specificeren. Zie [Segmenten beheren](marketing-segments.md) voor meer informatie.

### <a name="registering-discount-percentages"></a>Kortingspercentages vastleggen
Wanneer u uw campagne hebt ingesteld en hebt besloten op welke segmenten de campagne betrekking heeft en tevens de startdatum en de einddatum hebt ingesteld, legt u vast welk kortingspercentage de klant krijgt voor de individuele artikelen op de regels in het venster **Verkoopregelkortingen**. U kunt de verkoopprijzen voor de individuele artikelen ook vastleggen in het venster **Verkoopprijzen**. U kunt beide vensters openen vanuit de campagnekaart.

 Wanneer u verkoopprijzen/regelkortingen en de segmenten op de campagnekaart hebt ingesteld, moet u deze activeren zodat de campagneprijzen/kortingen op de regels verschijnen.

> [!NOTE]  
>   Als u de verkoopprijs/regelkortingen wilt activeren, moet u aangeven of het volledige segment of alleen enkele contacten de doelpersonen van de campagne zijn. Als de verkoopprijzen/regelkortingen betrekking hebben op alle contacten in het segment, selecteer het veld **Campagnedoel** in op het sneltabblad **Campagne** van de **segment** kaart.

Als de verkoopprijzen/regelkortingen niet aan alle contacten in het segment moeten worden aangeboden, kunt u het selectievakje **Campagnedoel** uitschakelen voor de betreffende contacten. Als u dit veld niet kunt zien, kunt u dit aan de weergave toevoegen. Zie [Persoonlijke gebruikersinstellingen](ui-user-personalization.md) voor meer informatie.

## <a name="conducting-campaigns"></a>Campagnes uitvoeren
Terwijl een campagne loopt, worden alle interacties met uw contacten (of segment) geregistreerd. Zodoende kunt u statistieken en andere informatie over de kosten en succespercentages van de campagne verkrijgen.

Campagnes worden gehouden door verkopers en u moet activiteiten maken voor elke taak en deze toewijzen aan de relevante verkopers. Zie voor meer informatie [Procedure: Opportunityverkoopcycli en cyclusfasen maken](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Zie ook
[Contactpersonen beheren](marketing-contacts.md)  
[Segmenten beheren](marketing-segments.md)  
[Verkoopopportunities beheren](marketing-manage-sales-opportunities.md)  
[Werken met Financials](ui-work-product.md)  

