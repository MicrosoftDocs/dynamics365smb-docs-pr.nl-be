---
title: Gegevensvertrouwelijkheid classificeren
description: U moet opgeven welk soort gegevens u opslaat over personen zodat u kunt reageren op aanvragen van gegevensonderwerpen.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2018
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 05d9630075ed533759f8225810e4e4a95c141b16
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---

# <a name="classifying-data-sensitivity"></a>Gegevensvertrouwelijkheid classificeren
Om velden te classificeren die vertrouwelijke of persoonlijke gegevens bevatten, kan een Microsoft-partner de eigenschap ```DataClassification``` van velden instellen. Dit vereist toegang tot de databasetabellen, met de ontwikkelingsomgeving of door een Windows PowerShell-script uit te voeren. Zie voor meer informatie [Gegevens classificeren](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data).  

Als klant kunt u een tweede niveau van classificatie toevoegen door gevoeligheidsniveaus voor de gegevens op te geven die u in standaard- en aangepaste velden opslaat. Gegevensvertrouwelijkheid classificeren helpt zorgen dat u weet waar u persoonlijke gegevens in uw systeem bewaart en maakt het gemakkelijker te reageren op aanvragen van gegevensonderwerpen. Als een contact of klant u bijvoorbeeld vraagt hun persoonlijke gegevens te exporteren. Zie voor meer informatie [Reageren op aanvragen over persoonlijke gegevens](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Microsoft biedt de functie Classificatie van gegevensvertrouwelijkheid alleen voor het gemak. Het is uw verantwoordelijkheid om de gegevens te classificeren en te voldoen aan wetten en verordeningen die op u van toepassing zijn. Microsoft ontkent alle verantwoordelijkheid voor claims met betrekking tot uw classificatie van de gegevens.  

De volgende tabel beschrijft gegevensgevoeligheidsniveaus die u kunt toewijzen.

|Vertrouwelijkheid|Description|
|----|----|
|Vertrouwelijk | Informatie over het ras of de etnische achtergrond van een gegevensonderwerp, politieke overtuigingen, religieuze overtuigingen, betrokkenheid bij vakbonden, fysieke of geestelijke gezondheid, seksualiteit of gegevens over strafbare feiten. |
|Persoonlijk | Informatie die kan worden gebruikt om een gegevensonderwerp te identificeren, rechtstreeks of in combinatie met andere gegevens.|
|Vertrouwelijk | Bedrijfsgegevens die u voor de boekhouding of andere bedrijfsdoeleinden gebruikt en die u niet aan andere entiteiten wilt blootstellen. Dit kan bijvoorbeeld posten omvatten.|
|Normaal | Algemene gegevens die niet in andere categorieën horen.|

## <a name="how-do-i-classify-my-data"></a>Hoe classificeer ik mijn gegevens?
De vertrouwelijkheid van een groot aantal velden één voor één classificeren zou lang duren. Om het proces te versnellen bieden we hulpmiddelen die u kunt gebruiken om de vertrouwelijkheid van velden bulksgewijs te classificeren. Daarna verfijnt u de classificaties voor specifieke velden. U kunt hulpmiddelen vinden in het werkblad Gegevensclassificatie, dat beschikbaar is in het rolcentrum Beheer van gebruikers, gebruikersgroepen en machtigingen. U moet een systeembeheerder zijn om het werkblad te gebruiken.

> [!Important]
> Als u het werkblad Gegevensclassificatie voor het eerst opent, is het leeg. U moet de begeleiding Gegevensclassificatie uitvoeren om de lijst met velden te genereren. Als u de begeleiding wilt starten, kiest u de actie **Gegevensclassificaties instellen**.

Met het werkblad Gegevensclassificatie kunt u bijvoorbeeld het volgende doen:  

* Gebruik de begeleiding Gegevensclassificatie om uw velden te exporteren naar een Excel-werkblad waarin u ze bulksgewijs kunt classificeren. De Excel-werkmapbestand gebruiken is vooral handig als u samenwerkt met een Microsoft-partner. Nadat u het voorstel hebt bijgewerkt, kunt u de begeleiding gebruiken om de classificaties te importeren en toe te passen. U kunt de begeleiding ook gebruiken om velden handmatig te classificeren.  
* Kies een veld en filter vervolgens de lijst om soortgelijke velden te vinden die waarschijnlijk bij dezelfde classificatie moeten behoren als het veld waarop u de zoekactie baseert.  
* Een veld onderzoeken door de inhoud ervan te bekijken.  

> [!Tip]
> Wij hebben voorbeelden van vertrouwelijkheidsclassificaties gedefinieerd voor de tabellen en velden in het demonstratiebedrijf Cronus. U kunt deze indelingen als inspiratie gebruiken wanneer u uw eigen tabellen en velden classificeert.

## <a name="see-also"></a>Zie ook
[Gegevens classificeren](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  

