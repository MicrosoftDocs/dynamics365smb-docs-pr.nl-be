---
title: Veldtoewijzing voor het exporteren van betalingsbestanden | Microsoft Docs
description: 'Wanneer u betalingsbestanden exporteert met de extensie AMC Banking 365 Fundamentals, zijn de gegevens die u exporteert, zichtbaar voor de serviceprovider.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension" />Veldtoewijzing bij de export van betalingsbestanden met behulp van de extensie AMC Banking 365 Fundamentals
Wanneer u betalingsbestanden exporteert met de extensie AMC Banking 365 Fundamentals, zijn de gegevens die u exporteert, zichtbaar voor de serviceprovider. De serviceprovider is verantwoordelijk voor de privacy van deze informatie. Zie [De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md) voor meer informatie over de extensie AMC Banking 365 Fundamentals.  

> [!CAUTION]  
>  Wanneer u betalingsbestanden exporteert met de extensie AMC Banking 365 Fundamentals, zijn sommige bedrijfsgegevens zichtbaar voor de serviceprovider. De serviceprovider, AMC Consult A/S, is verantwoordelijk voor de privacy van deze informatie. Zie [AMC-privacybeleid](https://go.microsoft.com/fwlink/?LinkId=510158) voor meer informatie.  

> [!NOTE]
> In de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] wordt een algemene provider van services ingesteld en verbonden die bankgegevens converteert naar een bestandsindeling die uw bank vereist. In Noord-Amerikaanse versies kan dezelfde service worden gebruikt om betalingsbestanden te verzenden als elektronische overboeking (EFT), bijvoorbeeld het veelgebruikte ACH-netwerk (Automated Clearing House), maar met een iets ander proces.

De volgende tabel bevat de velden in [!INCLUDE[prod_short](includes/prod_short.md)] vanwaar u gegevens kunt exporteren.  

|Toegewezen veld|Veld in tabel|Tafel|Omschrijving|  
|------------------|--------------------|-----------|---------------------------------------|  
|Crediteurnummer|Crediteurnummer|Bankrekening|De identificatie die door uw bank aan uw bedrijf is toegewezen om betalingen te innen|  
|Bankrekeningnummer afzender|Bankrekeningnr./IBAN|Bankrekening|Het bankrekeningnummer van uw bedrijf (IBAN of ander) dat is opgegeven op de bankrekeningkaart|  
|Verrekeningsstandaard bank afzender|Verrekeningsstandaard bank|Bankrekening|Het nationale banknamenregister dat voor de bankrekening van de afzender wordt gebruikt|  
|Verrekeningscode bank afzender|Verrekeningscode bank|Bankrekening|De identificatie van de bankrekening van de afzender met betrekking tot het gebruikte banknamenregister|  
|Bank-BIC zender|SWIFT-code|Bankrekening|De SWIFT-identificatie van de bankrekening van de afzender|  
|Valuta bankrekening afzender|Valutacode|Bankrekening|Valutacode van de bankrekening afzender|  
|Documentnr.|Documentnr.|Dagboekregel|Het documentnummer van de betalingsregel|  
|Van toep. op ext.doc.nr.|Van toep. op ext.doc.nr.|Dagboekregel|Het externe documentnummer van de factuur of creditnota waarmee de betalingsregel wordt vereffend|  
|Id ontvanger|Rekeningnr.|Dagboekregel|Het klant- of leveranciersnummer dat wordt opgegeven op de betalingsregel|  
|Betalingssoort|Betalingssoort gegevensconv. bank|Betalingswijze|Het soort bankoverboeking, bijvoorbeeld binnenlands of internationaal|  
|Betalingsreferentie|Betalingsreferentie|Dagboekregel|De betalingsverwijzing van de betalingsregel|  
|Adres ontvanger|Adres|Klant/Leverancier|Het adres van de ontvanger die wordt opgegeven op de klanten- of leverancierskaart|  
|Woonplaats ontvanger|Plaats|Klant/Leverancier|De woonplaats van de ontvanger die wordt opgegeven op de klanten- of leverancierskaart|  
|Naam ontvanger|Naam|Klant/Leverancier|De naam van de ontvanger die wordt opgegeven op de klanten- of leverancierskaart|  
|Land-/regiocode ontvanger|Land-/regiocode|Klant/Leverancier|De land-/regiocode van de ontvanger die wordt opgegeven op de klanten- of leverancierskaart|  
|Postcode ontvanger|Postcode|Klant/Leverancier|De postcode van de ontvanger die wordt opgegeven op de klanten- of leverancierskaart|  
|Bankrekeningnummer ontvanger|Bankrekeningnr./IBAN|Bankrekening klant/Bankrekening leverancier|Het nummer van de bankrekening (IBAN of ander) van de ontvanger dat is opgegeven op de bankrekeningkaart van de klant of leverancier|  
|Verrekeningscode bank ontvanger|Verrekeningsstandaard bank|Bankrekening klant/Bankrekening leverancier|Het nationale banknamenregister dat voor de bankrekening van de ontvanger wordt gebruikt|  
|Verrekeningsstand. bank ontvanger|Verrekeningscode bank|Bankrekening klant/Bankrekening leverancier|De identificatie van de bankrekening van de ontvanger met betrekking tot het banknamenregister dat wordt gebruikt|  
|E-mailadres ontvanger|E-mail|Klant/Leverancier|Het e-mailadres van de ontvanger|  
|Bericht aan ontvanger 1|Bericht aan ontvanger|Dagboekregel|Het bericht aan de ontvanger die is opgegeven op de betalingsregel|  
|Bedrag|Bedrag|Dagboekregel|Het bedrag op de betalingsregel|  
|Valutacode|Valutacode|Dagboekregel|De valutacode op de betalingsregel|  
|Overdrachtsdatum|Boekingsdatum|Dagboekregel|De boekingsdatum van de betalingsregel|  
|Factuurbedrag|Oorspronkelijk bedrag|Klantenpost/Leverancierspost|Het bedrag op de post waarmee de betaling wordt vereffend|  
|Factuurdatum|Documentdatum|Klantenpost/Leverancierspost|De factuurdatum op de post waarmee de betaling wordt vereffend|  
|Adres bank ontvanger|Adres|Bankrekening klant/Bankrekening leverancier|Het adres van de bankrekening van de ontvanger dat is opgegeven op de bankrekeningkaart van de klant of leverancier|  
|Het adres van de bankrekening van de ontvanger dat is opgegeven op de bankrekeningkaart van de klant of leverancier|Plaats|Bankrekening klant/Bankrekening leverancier|De plaats van de bankrekening van de ontvanger die is opgegeven op de bankrekeningkaart van de klant of leverancier|  
|Banknaam ontvanger|Naam|Bankrekening klant/Bankrekening leverancier|De naam van de bankrekening van de ontvanger die is opgegeven op de bankrekeningkaart van de klant of leverancier|  
|Land/regio bank ontvanger|Land-/regiocode|Bankrekening klant/Bankrekening leverancier|Het land/de regio van bankrekening van de ontvanger dat/die is opgegeven op de bankrekeningkaart van de klant of leverancier|  
|Postcode bank ontvanger|Postcode|Bankrekening klant/Bankrekening leverancier|De postcode van de bankrekening van de ontvanger die is opgegeven op de bankrekeningkaart van de klant of leverancier|  
|Adres bank afzender|Adres|Bankrekening|Het adres van de bankrekening van de afzender dat is opgegeven op de bankrekeningkaart|  
|Plaats bank afzender|Plaats|Bankrekening|De plaats van de bankrekening van de afzender die is opgegeven op de bankrekeningkaart|  
|Banknaam afzender|Naam|Bankrekening|De naam van de bankrekening van de afzender die is opgegeven op de bankrekeningkaart|  
|Land/regiocode bank afzender|Land-/regiocode|Bankrekening|Het land/de regio van de bankrekening van de afzender dat/die is opgegeven op de bankrekeningkaart|  
|Postcode bank afzender|Postcode|Bankrekening|De postcode van de bankrekening van de afzender die is opgegeven op de bankrekeningkaart|  
|Algemeen dagboeksjabloon|Dagboeksjabloon|Dagboekregel|De dagboeksjabloon die wordt gebruikt voor de betalingsregel|  
|Batchnaam financieel dagboek|Dagboekbatch|Dagboekregel|De dagboekbatchnaam die wordt gebruikt voor de betalingsregel|  
|Banknaam afzender - Gegevensconv.|Banknaam - Gegevensconversie|Bankrekening|De naam van de bankrekening van de afzender die is aangevraagd door de extensie AMC Banking 365 Fundamentals en die wordt vermeld op de bankpas|  

## <a name="see-also" />Zie ook
[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)
[De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md)   
[Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-kredietoverdracht](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
