---
title: Reageren op aanvragen over persoonlijke gegevens
description: U moet reageren op aanvragen van gegevensonderwerpen.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Reageren op aanvragen over persoonlijke gegevens  
Gegevensonderwerpen kunnen verschillende typen acties aanvragen met betrekking tot hun persoonlijke gegevens. Als u de gevoeligheid van uw gegevens hebt ingedeeld en zeker weet dat ze kloppen, kan een beheerder op aanvragen reageren met behulp van het werkblad Gegevensclassificatie in het rolcentrum **Gebruikers, gebruikersgroepen en machtigingen beheren** of, als u de Windows-client gebruikt, in het rolcentrum **IT-beheerder**. Voor meer informatie over het classificeren van gegevens en gegevensvertrouwelijkheid raadpleegt u [Gegevens classificeren](/dynamics-nav/classifying-data) en [Vertrouwelijkheid van gegevens classificeren](admin-classifying-data-sensitivity.md)

De volgende tabel bevat voorbeelden van de typen aanvragen waarop u kunt reageren.

> [!Note]
> We bieden mogelijkheden om te reageren op deze typen aanvragen en daarmee het verkrijgen van toegang tot persoonlijke gegevens, maar het is uw verantwoordelijkheid te zorgen dat persoonlijke en vertrouwelijke gegevens zich op de juiste plaats bevinden en goed worden geclassificeerd.

|Aanvraagsoort|Beschrijving en voorgestelde reactie|
|-----|-----|
|Portabiliteitsaanvragen|Een gegevensonderwerp kan een portabiliteitsaanvraag voor gegevens doen, wat onder andere betekent dat u de persoonlijke gegevens van het gegevensonderwerp uit uw systemen moet exporteren en moet verschaffen in een gestructureerde, gangbare indeling. Als u op deze aanvragen wilt reageren, gebruikt u het hulpprogramma Gegevensprivacy om persoonlijke gegevens naar een Excel-bestand te exporteren. Met Excel kunt u de persoonlijke gegevens opslaan in een gangbare, door een machine leesbare indeling, zoals .csv of .xml. Beheerders kunnen gegevens ook exporteren met behulp van Rapid Start-configuratiepakketten en vervolgens hoofdgegevenstabellen en de gerelateerde tabellen met persoonlijke gegevens ervan configureren. |
|Aanvragen van verwijdering|Een gegevensonderwerp kan erom verzoeken dat u de persoonlijke gegevens ervan verwijdert. Er zijn verschillende manieren om persoonlijke gegevens te verwijderen met de mogelijkheden voor aanpassing, maar de beslissing en implementatie is uw verantwoordelijkheid. In sommige gevallen kiest u er wellicht voor uw gegevens rechtstreeks te bewerken, bijvoorbeeld een contactpersoon verwijderen en dan de batchverwerking Geannuleerde interactie verwijderen uitvoeren om interacties voor de contactpersoon te verwijderen. <br><br> **Opmerking:** als u een datum hebt opgegeven in het veld **Documentverwijdering toestaan voor** op de pagina **Instellingen van verkoop en tegoeden** of **Inkoopinstellingen**, moet u de datum mogelijk wijzigen, zodat u geboekte verkoop- en inkoopdocumenten kunt verwijderen die u hebt afgedrukt en die een boekingsdatum hebben op of vóór die datum.|
|Aanvragen van correcties|Een gegevensonderwerp kan aanvragen dat u onnauwkeurige persoonlijke gegevens corrigeert. Dit kunt u op verschillende manieren doen. In sommige gevallen kunt u lijsten naar Excel exporteren om snel bulksgewijs meerdere records te bewerken en vervolgens de bijgewerkte gegevens importeren. Zie voor meer informatie [Uw bedrijfsgegevens exporteren naar Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). U kunt velden ook handmatig bewerken die persoonlijke gegevens bevatten, zoals informatie over een klant op de klantenkaart wijzigen. Transactierecords zoals grootboek-, klant- en belastingposten zijn echter essentieel voor de integriteit van het ERP-systeem. Als u persoonlijke gegevens in bedrijftransactierecords opslaat, denk dan na over de aanpassingsmogelijkheden om dergelijke persoonlijke gegevens te wijzigen.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Gegevensverwerking voor een gegevensonderwerp beperken
Een gegevensonderwerp kan aanvragen dat u tijdelijk stopt met verwerking van de persoonlijke gegevens. Als u dergelijke aanvragen honoreert, kunt u de record van het gegevensonderwerp registreren als geblokkeerd vanwege privacy om de verwerking van de gegevens te stoppen. Wanneer een record als geblokkeerd is gemarkeerd, kunt u geen nieuwe transacties maken die de record gebruiken. Bijvoorbeeld, u kunt geen nieuwe factuur voor een klant maken wanneer de klant of de verkoper is geblokkeerd. Als u een gegevensonderwerp als geblokkeerd wilt markeren, opent u de kaart voor het gegevensonderwerp, bijvoorbeeld de klanten-, leveranciers- of contactkaart en schakelt u het selectievakje **Geblokkeerd vanwege privacy** in. U moet mogelijk **Meer tonen** kiezen om het veld weer te geven.

## <a name="handling-data-about-minors"></a>Gegevens over minderjarigen verwerken
Als de leeftijd van een contactpersoon onder de wettelijke meerderjarigheidsleeftijd ligt volgens de wetgeving in uw regio, kunt u dat aangeven door het selectievakje **Minderjarig** in te schakelen op de **Contact**kaart. Wanneer u dat doet, wordt het selectievakje **Geblokkeerd vanwege privacy** automatisch ingeschakeld. Wanneer u toestemming van de ouder of wettelijke voogd van de minderjarige ontvangt, kunt u het selectievakje **Toestemming van ouders ontvangen** kiezen om het contact te deblokkeren. Hoewel u persoonlijke gegevens voor minderjarigen kunt verwerken, kunt u de profileringsfunctionaliteit in Microsoft Dynamics 365 for Sales niet gebruiken.

> [!Note]
> In het wijzigingslogbestand kan informatie worden geregistreerd, zoals wanneer en door wie het selectievakje **Toestemming van ouders ontvangen** is ingeschakeld. Een beheerder kan dat instellen met de gids **Wijzigingslogbestandinstellingen** en door ook het selectievakje **Gereg. wijziging van toestemming van ouders ontvangen** in te schakelen op de **Contact**kaart. Zie [Wijzigingen registreren](/dynamics-nav-app/across-log-changes) voor meer informatie.  

## <a name="see-also"></a>Zie ook
[Gegevens classificeren](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Gegevensvertrouwelijkheid classificeren](admin-classifying-data-sensitivity.md)  
[Uw bedrijfsgegevens naar Excel exporteren](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

