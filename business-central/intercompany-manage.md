---
title: Intercompany-transacties beheren
description: Met de intercompany-functionaliteit kunt u zakelijke processen en transacties tussen bedrijven binnen dezelfde organisatie vereenvoudigen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
ms.service: dynamics-365-business-central
---
# Intercompany-transacties beheren

Bedrijven met meer dan één rechtspersoon met afzonderlijke boekhoudfuncties kunnen profiteren van IC-transacties. Het is bijvoorbeeld handig voor bedrijven die dochterondernemingen hebben in meerdere internationale markten of regio's. Of een organisatie bestaat uit meerdere bedrijven, maar heeft mogelijk niet hetzelfde aantal boekhoud- en administratieteams. IC-transacties vereenvoudigen en stroomlijnen de zakelijke processen en transacties tussen bedrijven in de IC-partnerschap.

Wanneer u de klant- en leveranciersrelaties voor IC-transacties hebt opgegeven, voeren partners informatie eenmalig in verkoop- en inkoopdocumenten in. Bij de andere bij de transactie betrokken partner wordt een overeenkomstig document gemaakt. Het rekeningschema en de dimensies toewijzen helpt zorgen dat informatie op de juiste plaatsen wordt weergegeven.  

De IC-functionaliteit heeft vier belangrijke voordelen:  

* Verhoogde productiviteit dankzij tijdsbesparing en vereenvoudigde transacties.  
* Minder vergissingen door eenmalige invoer van informatie en geautomatiseerde updates in het hele systeem  
* Complete audittrail en volledige zichtbaarheid van zakelijke activiteiten en transactiegeschiedenissen.  
* Efficiënte en kosteneffectieve transacties met filialen en dochterondernemingen.  

## Stroomlijning van de stroom van zakelijke activiteiten  

Met IC-transacties kunt u verkoop- en inkoopdocumenten en grootboekposten naar al uw satellietkantoren, verkoopkantoren of dochterondernemingen verspreiden. Het distribueren van transacties bespaart tijd en verhoogt de efficiëntie in de hele organisatie door de invoer van gegevens te verminderen. Het vermindert de noodzaak om verkoop- en inkoopdocumenten te verzenden, te ontvangen, af te drukken en te archiveren.  

U hebt de volledige controle over alle transactiedocumenten. U kunt bijvoorbeeld een document dat aan u is verzonden weigeren en de acties **Journaalboekingen tegenboeken** en **Ontvangsten/zendingen ongedaan maken** gebruiken om correcties aan te brengen. U kunt ook, wanneer u inkoopt bij een partner of dochteronderneming, de inkooporder wijzigen zo lang de verkopende onderneming de goederen nog niet heeft verzonden.  

Wanneer u een transactie invoert, hoeft u de te gebruiken rekeningen niet op te geven. U kiest gewoon de IC-partner. De IC-functionaliteit maakt grootboekregels aan, die leiden tot het sluitend maken van de boeken van beide bedrijven die bij de transactie zijn betrokken. In Klanten en Leveranciers wijst u een intercompany-partnercode toe aan een klant of leverancier. Vanaf dat moment produceren alle orders en facturen voor transacties tussen deze bedrijven corresponderende documenten in het partnerbedrijf. Het resultaat is correct gebalanceerde rekeningen.  

IC richt zich op verkoop- en inkoopdocumenten en algemene grootboekregels en maakt transacties mogelijk tussen meerdere [!INCLUDE [prod_short](includes/prod_short.md)]-databases. Voorbeeld:

* In verschillende landen/regio's
* Meerdere valuta's
* Verschillende rekeningschema's
* Verschillende dimensies
* Verschillende artikelnummers  

IC-transacties gebruiken verschillende typen boekingen en documenten:  

* Grootboekposten
* Inkoop- en verkooporders
* Inkoop- en verkoopfacturen
* Creditnota's
* Retourorders

Wanneer u IC-transacties instelt, maakt u een lijst met IC-partners, een IC-rekeningschema en IC-dimensies. Daarna kunt u transacties maken in IC-dagboeken.

> [!NOTE]
> Het dagboek zelf bevat geen valuta's. Het converteert alle bedragen naar de lokale valuta tegen de huidige wisselkoers.

Nadat u zakenpartners in het systeem hebt ingesteld als klanten en leveranciers, en IC-partnercodes aan hen hebt toegewezen, kunnen zij IC-inkoop- en verkoopdocumenten uitwisselen, zoals artikelen en artikeltoeslagen. 

> [!NOTE]
> Bedrijven kunnen IC niet gebruiken om alle soorten gegevens uit te wisselen. Inkoopfacturen worden niet via intercompany-processen bij zakenpartners ingediend. Verkoopfacturen die via IC-processen worden ingediend, worden echter als inkoopfacturen in het ontvangende bedrijf gemaakt.

Consolideren van financiële gegevens kan relevant zijn voor IC-processen. Zie voor meer informatie [Financiële gegevens uit meerdere bedrijven consolideren](finance-consolidated-company-reporting.md).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

|Functie |Zie|
|---|---|
|Maak uw IC-leveranciers en -klanten als partners en stel een IC-rekeningschema in.|[Intercompany instellen](intercompany-how-setup.md)|
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
