---
title: Reageren op aanvragen over persoonlijke gegevens
description: In dit onderwerp leest u hoe u kunt reageren op verzoeken over persoonlijke gegevens. Dit wordt een aanvraag van een gegevensonderwerp genoemd.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 06/14/2021
ms.reviewer: na
ms.topic: conceptual
---

# Reageren op aanvragen over persoonlijke gegevens van gebruikers  
Gegevensonderwerpen kunnen verschillende typen acties aanvragen met betrekking tot hun persoonlijke gegevens. Onder de Algemene verordening gegevensbescherming (AVG) hebben ingezetenen van de EU bijvoorbeeld het recht hun persoonlijke gegevens te exporteren, verwijderen en wijzigen. Dit wordt een *aanvraag van een gegevensonderwerp* genoemd. Als u de gevoeligheid van uw gegevens hebt geclassificeerd en zeker weet dat deze correct zijn, kan een beheerder op verzoeken reageren met behulp van de opties onder het tabblad **Gegevensprivacy** in het rolcentrum **IT-beheerder**. Voor meer informatie over het classificeren van gegevens en gegevensvertrouwelijkheid in [!INCLUDE[prod_long](includes/prod_long.md)] raadpleegt u [Gegevens classificeren](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) en [Vertrouwelijkheid van gegevens classificeren](admin-classifying-data-sensitivity.md).  

## Soorten aanvragen

De volgende tabel bevat voorbeelden van de typen aanvragen waarop u kunt reageren.

> [!Note]
> We bieden mogelijkheden om te reageren op deze typen aanvragen en daarmee het verkrijgen van toegang tot persoonlijke gegevens, maar het is uw verantwoordelijkheid te zorgen dat persoonlijke en vertrouwelijke gegevens zich op de juiste plaats bevinden en goed worden geclassificeerd.

|Aanvraagsoort|Beschrijving en voorgestelde reactie|
|-----|-----|
|Portabiliteitsaanvragen|Een gegevensonderwerp kan een portabiliteitsaanvraag voor gegevens doen, wat onder andere betekent dat u de persoonlijke gegevens van het gegevensonderwerp uit uw systemen moet exporteren en moet verschaffen in een gestructureerde, gangbare indeling. Als u op deze aanvragen wilt reageren, kunt u het **hulpprogramma Gegevensprivacy** gebruiken om persoonlijke gegevens naar een Excel-bestand of een RapidStart-configuratiepakket te exporteren. Met Excel kunt u de persoonlijke gegevens opslaan in een gangbare, door een machine leesbare indeling, zoals .csv of .xml. Voor RapidStart-configuratiepakketten kunt u hoofdgegevenstabellen en de gerelateerde tabellen ervan configureren die persoonlijke gegevens bevatten. <br><br> **Opmerking:** als u gegevens exporteert, geeft u een minimumgevoeligheidsniveau op. De export bevat het minimale gevoeligheidsniveau en alle niveaus erboven. Als u er bijvoorbeeld voor kiest gegevens te exporteren die zijn geclassificeerd als Persoonlijk, bevat de export ook gegevens die zijn geclassificeerd als Vertrouwelijk. <br><br>Wanneer u gegevens exporteert die gerelateerd zijn aan een gegevensonderwerp, zoekt het **hulpprogramma Gegevensprivacy** directe relaties tussen het gegevensonderwerp en gegevens die gerelateerd zijn aan het gegevensonderwerp. Indirecte relaties tussen gegevens die gerelateerd zijn aan het gegevensonderwerp en andere gegevens worden niet automatisch geëxporteerd door het hulpprogramma **Gegevensprivacy**. De tabel Contactpersoon heeft bijvoorbeeld direct gerelateerde Profielantwoorden contactgegevens en de tabel Profielantwoorden contact is verder gerelateerd aan Profielvragen-gegevens. Als u ook Profielvragen-gegevens wilt exporteren, moet u deze tabel handmatig als rij toevoegen met de juiste filters in het configuratiepakket dat het hulpprogramma **Gegevensprivacy** maakt.|
|Aanvragen van verwijdering|Een gegevensonderwerp kan erom verzoeken dat u de persoonlijke gegevens ervan verwijdert. Er zijn verschillende manieren om persoonlijke gegevens te verwijderen met de mogelijkheden voor aanpassing, maar de beslissing en implementatie is uw verantwoordelijkheid. In sommige gevallen kiest u er wellicht voor uw gegevens rechtstreeks te bewerken, bijvoorbeeld een contactpersoon verwijderen en dan de batchverwerking Geannuleerde interactie verwijderen uitvoeren om interacties voor de contactpersoon te verwijderen. <br><br> **Opmerking:** als u een datum hebt opgegeven in het veld **Documentverwijdering toestaan voor** op de pagina **Instellingen van verkoop en tegoeden** of **Inkoopinstellingen**, moet u de datum mogelijk wijzigen, zodat u geboekte verkoop- en inkoopdocumenten kunt verwijderen die u hebt afgedrukt en die een boekingsdatum hebben op of vóór die datum.|
|Aanvragen van correcties|Een gegevensonderwerp kan aanvragen dat u onnauwkeurige persoonlijke gegevens corrigeert. Dit kunt u op verschillende manieren doen. In sommige gevallen kunt u lijsten naar Excel exporteren om snel bulksgewijs meerdere records te bewerken en vervolgens de bijgewerkte gegevens importeren. Zie voor meer informatie [Uw bedrijfsgegevens exporteren naar Excel](about-export-data.md). U kunt velden ook handmatig bewerken die persoonlijke gegevens bevatten, zoals informatie over een klant op de klantenkaart wijzigen. Transactierecords zoals grootboek-, klant- en belastingposten zijn echter essentieel voor de integriteit van het ERP-systeem. Als u persoonlijke gegevens in bedrijftransactierecords opslaat, denk dan na over de aanpassingsmogelijkheden om dergelijke persoonlijke gegevens te wijzigen.|

## Gegevensverwerking voor een gegevensonderwerp beperken
Een gegevensonderwerp kan aanvragen dat u tijdelijk stopt met verwerking van de persoonlijke gegevens. Als u dergelijke aanvragen honoreert, kunt u de record van het gegevensonderwerp registreren als geblokkeerd vanwege privacy om de verwerking van de gegevens te stoppen. Wanneer een record als geblokkeerd is gemarkeerd, kunt u geen nieuwe transacties maken die de record gebruiken. Bijvoorbeeld, u kunt geen nieuwe factuur voor een klant maken wanneer de klant of de verkoper is geblokkeerd. Als u een gegevensonderwerp als geblokkeerd wilt markeren, opent u de kaart voor het gegevensonderwerp, bijvoorbeeld de klanten-, leveranciers- of contactkaart en schakelt u het selectievakje **Geblokkeerd vanwege privacy** in. U moet mogelijk **Meer tonen** kiezen om het veld weer te geven.  

## Aanvragen van gegevensonderwerpen afhandelen tijdens een proef
Bepaalde soorten persoonlijke gegevens maken deel uit van uw Microsoft 365-account en vereisen administratieve toegang om te worden geëxporteerd als u een aanvraag van een gegevensonderwerp van een gebruiker ontvangt met betrekking tot dit type persoonlijke gegevens onder de Algemene verordening gegevensbeschermingverordening. Het proces voor het afhandelen van aanvragen van gegevensonderwerpen verschilt afhankelijk van het type [!INCLUDE[prod_short](includes/prod_short.md)]-tenant.  

Als u een betaald abonnement voor [!INCLUDE[prod_short](includes/prod_short.md)] hebt, moet u contact met de tenantbeheerder van uw organisatie opnemen om een aanvraag van een gegevensonderwerp te doen. De beheerder heeft de administratieve rechten en hulpmiddelen om uw aanvraag af te handelen.  

Als u zich voor [!INCLUDE[prod_short](includes/prod_short.md)] hebt aangemeld vanaf de pagina [Proeven](https://trials.dynamics.com/) en u deze proefervaring niet hebt verlaten door middel van een betaald abonnement door de tenantbeheerder van uw organisatie, kunt u uw eigen aanvraag van een gegevensonderwerp afhandelen op de [pagina Privacy op werk en school in de Azure-portal](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Hier kunt u uw persoonlijke gegevens exporteren en downloaden.

Op de pagina Privacy op werk en school kunt u ook uw account sluiten. We raden u echter aan te zorgen dat u eerst alle gegevens hebt geëxporteerd en verwijderd, aangezien het verwijderen van uw account betekent dat u toegang kwijtraakt tot [!INCLUDE[prod_short](includes/prod_short.md)].  

U kunt nog steeds personen als geblokkeerd vanwege privacy markeren en transacties exporteren, bewerken of verwijderen, zoals elders in dit artikel uitgelegd.  

## Gegevens uit tabellen exporteren die niet zijn geclassificeerd op betrokkene
Als u in een situatie zit waarin u gegevens moet exporteren die niet zijn geclassificeerd op een manier waardoor deze automatisch worden geëxporteerd, zoals gegevens uit de tabel Profielantwoorden, moet u het volgende doen:
-   Vraag u af of u deze aanvullende gegevens echt wilt of moet exporteren die niet gerelateerd zijn aan de contactpersoon, wat betekent dat deze er geen directe relatie mee heeft.
-   Voeg deze tabel en relatie handmatig aan het Rapid Start-pakket toe en exporteer deze direct vanuit het Rapid Start-pakket. Daarom genereren we een Rapid Start-pakket voor u, zodat u het in situaties als deze kunt aanpassen.

## Gegevens over minderjarigen verwerken
Als de leeftijd van een contactpersoon onder de wettelijke meerderjarigheidsleeftijd ligt volgens de wetgeving in uw regio, kunt u dat aangeven door het selectievakje **Minderjarig** in te schakelen op de **Contact**kaart. Wanneer u dat doet, wordt het selectievakje **Geblokkeerd vanwege privacy** automatisch ingeschakeld. Wanneer u toestemming van de ouder of wettelijke voogd van de minderjarige ontvangt, kunt u het selectievakje **Toestemming van ouders ontvangen** kiezen om het contact te deblokkeren. Hoewel u persoonlijke gegevens voor minderjarigen kunt verwerken, kunt u de profileringsfunctionaliteit in Dynamics 365 Sales niet gebruiken.

> [!Note]
> In het wijzigingslogbestand kan informatie worden geregistreerd, zoals wanneer en door wie het selectievakje **Toestemming van ouders ontvangen** is ingeschakeld. Een beheerder kan dat instellen met de gids **Wijzigingslogbestandinstellingen** en door ook het selectievakje **Gereg. wijziging van toestemming van ouders ontvangen** in te schakelen op de **Contact**kaart. Zie [Wijzigingen registreren](across-log-changes.md) voor meer informatie.  

## Zie ook
[Gegevens classificeren](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Gegevensvertrouwelijkheid classificeren](admin-classifying-data-sensitivity.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)  
[Wijzigingen registreren](across-log-changes.md)  
[Aanvragen van gegevensonderwerpen voor de Algemene verordening gegevensbescherming](/microsoft-365/compliance/gdpr-data-subject-requests)  


[!INCLUDE[footer-include](includes/footer-banner.md)]