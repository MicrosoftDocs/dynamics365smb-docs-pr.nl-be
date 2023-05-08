---
title: Reageren op aanvragen over persoonlijke gegevens van gebruikers
description: In dit artikel wordt uitgelegd hoe u kunt reageren op verzoeken over persoonlijke gegevens.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
---

# Reageren op aanvragen over persoonlijke gegevens van gebruikers

Gegevensonderwerpen kunnen verschillende typen acties aanvragen met betrekking tot hun persoonlijke gegevens. Onder privacywetgeving en -voorschriften hebben ze bijvoorbeeld het recht hun persoonlijke gegevens te exporteren, verwijderen en wijzigen. Deze verzoeken worden *aanvragen van betrokkenen* genoemd. Als u de gevoeligheid van uw gegevens hebt geclassificeerd en zeker weet dat deze correct zijn, kan een beheerder op verzoeken reageren met behulp van de opties op het tabblad **Gegevensprivacy** in het rolcentrum **IT-beheerder**. Ga naar de volgende artikelen voor meer informatie over het classificeren van gegevens en gegevensgevoeligheid in [!INCLUDE[prod_long](includes/prod_long.md)]:

* [Gegevens classificeren](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Gegevensvertrouwelijkheid classificeren](admin-classifying-data-sensitivity.md)  

## Soorten aanvragen

De volgende tabel bevat voorbeelden van de typen aanvragen waarop beheerders kunnen reageren.

> [!Note]
> We bieden mogelijkheden om te reageren op deze typen aanvragen en daarmee het verkrijgen van toegang tot persoonlijke gegevens, maar het is uw verantwoordelijkheid te zorgen dat persoonlijke en vertrouwelijke gegevens zich op de juiste plaats bevinden en goed worden geclassificeerd.

|Aanvraagsoort|Beschrijving en voorgestelde reactie|
|-----|-----|
|Portabiliteitsaanvragen|Een betrokkene kan een verzoek tot gegevensoverdraagbaarheid indienen. U moet de persoonsgegevens van de betrokkene uit uw systemen exporteren en in een gestructureerd, gangbaar formaat aanleveren. Als u op deze aanvragen wilt reageren, kunt u het **hulpprogramma Gegevensprivacy** gebruiken om persoonlijke gegevens naar een Excel-bestand of een RapidStart-configuratiepakket te exporteren. Met Excel kunt u de persoonlijke gegevens opslaan in een gangbare, door een machine leesbare indeling, zoals .csv of .xml. Voor RapidStart-configuratiepakketten kunt u hoofdgegevenstabellen en de gerelateerde tabellen ervan configureren die persoonlijke gegevens bevatten. <br><br> **Opmerking:** als u gegevens exporteert, geeft u een minimumgevoeligheidsniveau op. De export bevat het minimale gevoeligheidsniveau en alle niveaus erboven. Als u er bijvoorbeeld voor kiest gegevens te exporteren die zijn geclassificeerd als Persoonlijk, bevat de export ook gegevens die zijn geclassificeerd als Vertrouwelijk. <br><br>Wanneer u gegevens exporteert die gerelateerd zijn aan een gegevensonderwerp, zoekt het **hulpprogramma Gegevensprivacy** directe relaties tussen het gegevensonderwerp en gegevens die gerelateerd zijn aan het gegevensonderwerp. Indirecte relaties tussen gegevens die gerelateerd zijn aan het gegevensonderwerp en andere gegevens worden niet automatisch geëxporteerd door het hulpprogramma **Gegevensprivacy**. De tabel Contactpersoon heeft bijvoorbeeld direct gerelateerde Profielantwoorden contactgegevens en de tabel Profielantwoorden contact is verder gerelateerd aan Profielvragen-gegevens. Als u ook Profielvragen-gegevens wilt exporteren, moet u deze tabel handmatig als rij toevoegen met de juiste filters in het configuratiepakket dat het hulpprogramma **Gegevensprivacy** maakt.|
|Aanvragen van verwijdering|Een gegevensonderwerp kan erom verzoeken dat u de persoonlijke gegevens ervan verwijdert. Er zijn verschillende manieren om persoonlijke gegevens te verwijderen met de mogelijkheden voor aanpassing, maar de beslissing en implementatie is uw verantwoordelijkheid. In sommige gevallen kunt u ervoor kiezen om uw gegevens direct te bewerken. Verwijder bijvoorbeeld een contactpersoon en voer vervolgens de batchverwerking Geannuleerde interactie verwijderen uit om interacties voor de contactpersoon te verwijderen. <br><br> **Opmerking:** als u een datum hebt opgegeven in het veld **Documentverwijdering toestaan voor** op de pagina **Instellingen van verkoop en tegoeden** of **Inkoopinstellingen**, moet u de datum mogelijk wijzigen, zodat u geboekte verkoop- en inkoopdocumenten kunt verwijderen die u hebt afgedrukt en die een boekingsdatum hebben op of vóór die datum.|
|Aanvragen van correcties|Een gegevensonderwerp kan aanvragen dat u onnauwkeurige persoonlijke gegevens corrigeert. Dit kunt u op verschillende manieren doen. In sommige gevallen kunt u lijsten naar Excel exporteren om snel bulksgewijs meerdere records te bewerken en vervolgens de bijgewerkte gegevens importeren. Zie voor meer informatie [Uw bedrijfsgegevens exporteren naar Excel](about-export-data.md). U kunt velden ook handmatig bewerken die persoonlijke gegevens bevatten, zoals informatie over een klant op de klantenkaart wijzigen. Records zoals algemene, klant- en belastingposten zijn echter belangrijk. Als u persoonlijke gegevens in bedrijftransactierecords opslaat, denk dan na over de aanpassingsmogelijkheden om dergelijke persoonlijke gegevens te wijzigen.|

## Gegevensverwerking voor een betrokkene beperken

Een gegevensonderwerp kan aanvragen dat u tijdelijk stopt met verwerking van de persoonlijke gegevens. Als u dergelijke aanvragen honoreert, kunt u de record van het gegevensonderwerp registreren als geblokkeerd vanwege privacy om de verwerking van de gegevens te stoppen. Wanneer een record als geblokkeerd is gemarkeerd, kunt u geen nieuwe transacties maken die de record gebruiken. Bijvoorbeeld, u kunt geen nieuwe factuur voor een klant maken wanneer de klant of de verkoper is geblokkeerd. Als u een gegevensonderwerp als geblokkeerd wilt markeren, opent u de kaart voor het gegevensonderwerp, bijvoorbeeld de klanten-, leveranciers- of contactkaart en schakelt u het selectievakje **Geblokkeerd vanwege privacy** in. U moet mogelijk **Meer tonen** kiezen om het veld weer te geven.  

## Afhandelen van verzoeken van betrokkenen bij gebruik van een proefversie

Bepaalde soorten persoonsgegevens maken deel uit van een Microsoft 365-account en alleen beheerders kunnen de gegevens exporteren. Het proces voor het afhandelen van aanvragen van gegevensonderwerpen verschilt afhankelijk van het type [!INCLUDE[prod_short](includes/prod_short.md)]-tenant.

Als u een betaald abonnement voor [!INCLUDE[prod_short](includes/prod_short.md)] hebt, moeten gebruikers contact met de tenantbeheerder van hun organisatie opnemen om een aanvraag van een betrokkene te maken. Beheerders hebben de administratieve rechten en hulpmiddelen om aanvragen van betrokkenen af te handelen.

Als u zich hebt aangemeld voor [!INCLUDE[prod_short](includes/prod_short.md)] via de pagina [Proefversie](https://trials.dynamics.com/) en u gebruikt nog steeds de proefversie, kunnen gebruikers hun eigen gegevens downloaden en exporteren op de [pagina Privacy op werk en school in de Azure-portal](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Op de pagina Privacy op werk en school kunt u ook uw account sluiten. We raden u echter aan om eerst alle gegevens te exporteren en te verwijderen. Als u uw account verwijdert, verliest u de toegang tot [!INCLUDE[prod_short](includes/prod_short.md)].

U kunt nog steeds personen als geblokkeerd vanwege privacy markeren en transacties exporteren, bewerken of verwijderen, zoals elders in dit artikel uitgelegd.  

## Gegevens uit tabellen exporteren die niet zijn geclassificeerd op betrokkene

Als u gegevens moet exporteren die niet zijn geclassificeerd op een manier waardoor deze automatisch worden geëxporteerd, zoals gegevens uit de tabel Profielantwoorden, moet u het volgende doen:

* Overweeg of u aanvullende gegevens die niet direct gerelateerd zijn aan het contact, echt moet exporteren.
* Voeg de tabel en relatie handmatig toe aan het Rapid Start-pakket en exporteer deze direct vanuit het Rapid Start-pakket. Wij maken voor u een Rapid Start-pakket, zodat u daar in dergelijke situaties op kunt inspelen.

## Gegevens over minderjarigen verwerken

Als de leeftijd van een contactpersoon onder de wettelijke meerderjarigheidsleeftijd ligt volgens de wetgeving in uw regio, kunt u dat aangeven door het selectievakje **Minderjarig** in te schakelen op de **Contact**kaart. Wanneer u dat doet, wordt het selectievakje **Geblokkeerd vanwege privacy** automatisch ingeschakeld. Wanneer u toestemming van de ouder of wettelijke voogd van de minderjarige ontvangt, kunt u het selectievakje **Toestemming van ouders ontvangen** kiezen om het contact te deblokkeren. Hoewel u persoonlijke gegevens voor minderjarigen kunt verwerken, kunt u de profileringsfunctionaliteit in Dynamics 365 Sales niet gebruiken.

> [!Note]
> In het wijzigingslogbestand kan informatie worden geregistreerd, zoals wanneer en door wie het selectievakje **Toestemming van ouders ontvangen** is ingeschakeld. Een beheerder kan dat instellen met de gids **Wijzigingslogbestandinstellingen** en door ook het selectievakje **Gereg. wijziging van toestemming van ouders ontvangen** in te schakelen op de **Contact**kaart. Zie [Wijzigingen registreren](across-log-changes.md) voor meer informatie.  

### Zie ook

[Gegevens classificeren](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Gegevensvertrouwelijkheid classificeren](admin-classifying-data-sensitivity.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)  
[Wijzigingen registreren](across-log-changes.md)  
[Verzoeken van betrokkenen](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
