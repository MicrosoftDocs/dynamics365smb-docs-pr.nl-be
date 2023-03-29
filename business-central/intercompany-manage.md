---
title: Intercompany-transacties beheren
description: Met de intercompany-functionaliteit kunt u zakelijke processen en transacties tussen bedrijven binnen dezelfde organisatie vereenvoudigen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: 605
ms.date: 08/11/2021
ms.author: edupont
---
# Intercompany-transacties beheren

De mogelijkheden voor Intercompany-transacties zijn bedoeld voor gebruikers die meer dan één onderneming runnen en meerdere bedrijven hebben ingesteld om de boekhoudfuncties van die ondernemingen te scheiden. Deze brede beschrijving is van toepassing op vele gebruikers, met name voor hen die werken op internationale markten of regio's met zeer verschillende bedrijfsculturen en wettelijke voorschriften.

Uw organisatie bestaat wellicht uit meerdere bedrijven, maar heeft mogelijk niet hetzelfde aantal boekhoud- en administratieteams. Met intercompany-transacties kunt u de zakelijke processen en transacties tussen alle entiteiten vereenvoudigen en stroomlijnen.

Nadat u intercompany-transacties bent gaan gebruiken, wordt zakendoen met uw dochteronderneming en uw interne partnerorganisaties net zo eenvoudig als werken met uw externe leveranciers en klanten. U geeft de intercompany-transactiegegevens slechts eenmaal op in de relevante documenten. U kunt de functies gebruiken waarmee u al vertrouwd bent, zoals Klanten en Leveranciers. De toewijzingsmogelijkheden voor het rekeningschema en de dimensies helpen ervoor te zorgen dat de informatie op de juiste plaatsen wordt weergegeven.  

De intercompany-functionaliteit heeft vier voordelen:  

- Verhoogde productiviteit dankzij tijdsbesparing en vereenvoudigde transacties.  
- Geminimaliseerd foutpotentieel door eenmalige invoer van informatie en geautomatiseerde wijzigingen in het hele systeem.  
- Complete audittrail en volledige zichtbaarheid van zakelijke activiteiten en transactiegeschiedenissen.  
- Efficiënte en kosteneffectieve transacties met filialen en dochterondernemingen.  

## Stroomlijning van de stroom van zakelijke activiteiten  

Met intercompany-transacties kunt u in het programma verkoop- en inkoopdocumenten, grootboekposten naar al uw satellietkantoren, verkoopkantoren of dochterondernemingen verspreiden. U bespaart tijd en verhoogt de efficiency in de hele organisatie naarmate u overbodige gegevensinvoer en het verzenden, ontvangen, afdrukken en archiveren van verkoop- en inkoopdocumenten op papier elimineert.  

U hebt de volledige controle over alle transactiedocumenten. U kunt bijvoorbeeld een document dat aan u is verzonden weigeren en zo incorrecte journaalboekingen tegenboeken en incorrecte ontvangsten/zendingen ongedaan maken. U kunt ook, wanneer u inkoopt bij een partner of dochteronderneming, de inkooporder wijzigen zo lang de verkopende onderneming nog geen goederen heeft verzonden.  

Wanneer u een transactie uitvoert, hoeft u geen rekeningen op te geven voor een aparte reeks boeken, maar geeft u eenvoudigweg de identificatie van het partnerbedrijf op. De intercompany-functionaliteit maakt grootboekregels aan, die leiden tot het sluitend maken van de boeken van beide bedrijven die bij de transactie zijn betrokken. In Klanten en Leveranciers wijst u een intercompany-partnercode toe aan een klant of leverancier. Vanaf dat moment wordt voor alle orders en facturen die voor de transacties van deze bedrijven zijn gegenereerd, overeenkomstige documenten in het partnerbedrijf geproduceerd, wat sluitende rekeningen tot gevolg heeft.  

De functie Intercompany-transacties is gericht op de ondersteuning van intercompany-transacties met verkoop- en inkoopdocumenten, en met grootboekregels. Binnen dit gebied vergemakkelijken intercompany-transacties intercompany-transacties tussen meerdere [!INCLUDE [prod_short](includes/prod_short.md)]-databases, bijvoorbeeld in verschillende landen/regio's, maar ook in meerdere valuta's, verschillende rekeningschema's, verschillende dimensies en verschillende artikelnummering.  

Bij intercompany-transacties wordt een aantal posten en documenten in intercompany-transacties gebruikt:  

- Grootboekposten
- Inkoop- en verkooporders
- Inkoop- en verkoopfacturen
- Creditnota's
- Retourorders

Wanneer u intercompany-transacties instelt, maakt u een lijst met intercompany-partners, IC-partners genaamd, en een intercompany-rekeningschema. Als u deze stappen volgt, kunt u intercompany-grootboektransacties uitvoeren. U stelt dimensies indien nodig afzonderlijk in.  

> [!NOTE]
> Het grootboek zelf heeft geen valutafunctionaliteit, maar converteert alle bedragen volgens de geldende wisselkoers naar de plaatselijke valuta.

Nadat u zakenpartners in het systeem hebt ingesteld als klanten en leveranciers, en intercompany-partnercodes aan hen hebt toegewezen, kunt u intercompany-inkoop- en verkoopdocumenten uitwisselen, zoals artikelen en artikeltoeslagen. [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt intercompany-transacties tussen meerdere databases, bijvoorbeeld in verschillende landen/regio's, maar ook in meerdere valuta's, verschillende rekeningschema's, verschillende dimensies en verschillende artikelnummering.  

> [!NOTE]
> Niet alle soorten gegevens kunnen op deze manier tussen bedrijven worden uitgewisseld. Inkoopfacturen worden niet via intercompany-processen bij zakenpartners ingediend. Verkoopfacturen die via intercompany-processen worden ingediend, worden echter als inkoopfacturen in het ontvangende bedrijf gemaakt.

Consolideren van financiële gegevens kan vooral relevant zijn voor IC-processen. Zie voor meer informatie [Financiële gegevens uit meerdere bedrijven consolideren](finance-consolidated-company-reporting.md).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

|Als u dit wilt doen: |Zie|
|---|---|
|Maak uw IC-leveranciers en -klanten als zogenaamde IC-partners en stel een IC-rekeningschema in.|[Intercompany instellen](intercompany-how-setup.md)|
|Gebruik IC-documenten of -dagboeken om transacties met uw IC-partners te boeken.|[Werken met intercompany-documenten en -dagboeken](intercompany-how-work-documents-journals.md)|
|Organiseer en verwerk inkomend en uitgaande transacties die u uitwisselt met uw IC-partners.|[De intercompany-inbox en outbox beheren](intercompany-how-manage-intercompany-inbox.md)|
|Gebruik intercompany-transacties om kosten tussen partnerbedrijven te verdelen.|[Kosten toewijzen aan intercompany-partners](intercompany-allocate-costs.md)|

## Zie ook

[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
