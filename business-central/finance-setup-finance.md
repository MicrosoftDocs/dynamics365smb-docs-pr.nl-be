---
title: Financiële processen instellen
description: 'Meer informatie over de vereiste taken om financiën in uw bedrijf in te stellen voor al uw boekhoudings-, controle- of boekingsbehoeften.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.date: 08/19/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="setting-up-finance"></a>Financiën instellen

Voordat u kunt beginnen met de uitvoering van uw bedrijf, moet u opgeven hoe u financiële processen voor het bedrijf wilt beheren. Als eerste stelt u de kern van de boekhoudadministratie van het bedrijf in: het rekeningschema (COA). Vervolgens stelt u de boekingsgroepen in, waarmee standaard-grootboekrekeningen efficiënter kunnen worden toegewezen aan klanten, leveranciers en artikelen.

Sommige financiële instellingen kunnen automatisch worden uitgevoerd met behulp van guides voor begeleide instelling en sommige moeten handmatig worden uitgevoerd. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md) Op de pagina **Grootboekinstellingen** wordt opgegeven hoe de verschillende boekhoudprocessen van uw bedrijf moeten worden afgehandeld. Zo kunt u deze pagina gebruiken voor het opgeven van details voor factuurafronding, de valutacode voor uw lokale valuta, adresnotaties en een mogelijke rapportagevaluta. Zie [Het grootboek en het rekeningschema](finance-general-ledger.md) voor meer informatie.  

Met dimensies kunt u verschillende soorten informatie toevoegen aan elke transactie. U kunt de basisdimensies van uw bedrijf instellen, zoals *Projecten* en *Afdelingen*. Voeg later meer dimensies toe wanneer u deze nodig hebt. Zo kunt u bijvoorbeeld tijdelijke dimensies instellen om gedurende een beperkte periode te gebruiken, zoals tijdens een verkoopcampagne. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

Veel van de instellingstaken moeten worden voltooid voordat u financiële transacties kunt gaan registreren, maar de meeste instellingen kunnen zo nodig worden aangepast. Daarnaast zijn er ook optionele installatietaken. Zo hoeft u bijvoorbeeld alleen IC-boekingen en -consolidaties in te stellen als u met meerdere bedrijven werkt. En andere instellingstaken, zoals het opgeven van de periode waarin een boeking is toegestaan, moeten periodiek worden herhaald.  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

| Tot | Zie |
| --- | --- |
|Grootboekrekeningen bekijken of bewerken waarnaar alle grootboekposten worden geboekt|[De rekeningschema's instellen of wijzigen](finance-setup-chart-accounts.md)|
| Geef aan hoe u wilt worden betaald door klanten en hoe u uw leveranciers wilt betalen. |[Betalingsmethoden instellen](finance-payment-methods.md) |
| Geef betalingsvoorwaarden op voor het beheren van vervaldatums en het berekenen van mogelijke betalingskortingen.|[Betalingsvoorwaarden instellen](finance-payment-terms.md) |
| Geef de boekingsgroepen op die entiteiten zoals klanten, leveranciers, artikelen, resources en verkoop- en inkoopdocumenten toewijzen aan grootboekrekeningen. |[Boekingsgroepen instellen](finance-posting-groups.md)|
|Maak financiële rapporten en definieer rekeningcategorieën om de inhoud van financiële grafieken en rapporten te bepalen, zoals de rapporten Balans en Resultatenrekening.|[Financiële rapportage voorbereiden met financiële gegevens en accountcategorieën](bi-how-work-account-schedule.md)|
|Stel een tolerantie in waarmee het systeem een factuur sluit zelfs indien de betaling, inclusief een eventuele korting, het bedrag op de factuur niet volledig dekt.|[Werken met betalingstolerantie en contantkortingstolerantie](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Stel boekperioden in. |[Werken met boekingsperioden en boekjaren](finance-accounting-periods-and-fiscal-years.md) |
|Stel factuurvoorwaarden in die uw klanten eraan herinneren om te betalen.|[De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md)|
| Definiëren hoe u btw-bedragen die u hebt geïnd voor verkopen, rapporteert aan de belastingdienst. |[Btw instellen](finance-setup-vat.md)|
|Verwerking voorbereiden van niet gerealiseerde btw in verband met op kas gebaseerde boekhoudingsmethoden.|[Ongerealiseerde btw voor op kas gebaseerde boekhouding instellen](finance-setup-unrealized-vat.md)|
|Definieer de vreemde valuta's waarin u handelt of transacties rapporteert.|[Valuta's instellen](finance-set-up-currencies.md)|
| Stel uw verkoop- en inkoopfuncties in om betalingen in vreemde valuta's te verwerken.|[Vereffening van posten in verschillende valuta's inschakelen](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definieer een of meer extra valuta's, zodat bedragen automatisch worden gerapporteerd in zowel de lokale valuta (LV) als de extra rapportagevaluta in elke grootboekpost en in andere posten.|[Een extra rapportagevaluta instellen.](finance-how-setup-additional-currencies.md)|
|Pas periodiek extra valuta-equivalenten aan in verband met schommelende wisselkoersen.|[Valutawisselkoersen bijwerken](finance-how-update-currencies.md)|
|Definieer meerdere rentepercentages voor verschillende perioden voor vertraagde betalingen in handelstransacties.|[Meerdere rentetarieven instellen](finance-how-to-set-up-multiple-interest-rates.md)|
|Zorg ervoor dat bedragen automatisch worden afgerond bij het maken van facturen.|[Factuurafronding instellen](finance-set-up-invoice-rounding.md)|
| Voeg nieuwe rekeningen aan bestaande rekeningschema's. |[Het rekeningschema instellen](finance-setup-chart-accounts.md) |
| Stel de BI-diagrammen (Business Intelligence) in om cashflow te analyseren. |[Cashflowanalyse instellen](finance-setup-cash-flow-analyses.md) |
|Maak facturering mogelijk van een klant die niet in het systeem is opgenomen.|[Contant betalende klanten instellen](finance-how-to-set-up-cash-customers.md)|
| Stel Intrastat-rapportage in en dien het rapport in bij een autoriteit. | [Intrastat instellen en rapporteren](finance-how-setup-report-intrastat.md)|
|Zorg dat een dagboekpost wordt toegewezen aan verschillende rekeningen, zoals aantal, percentage of bedrag, wanneer u deze naar het dagboek boekt.|[Verdeelsleutels in dagboeken gebruiken](ui-how-use-allocation-keys-general-journals.md)|
|Broncodes en redencodes instellen die kunnen helpen om audittrails bij te houden.|[Broncodes en redencodes instellen voor audittrails](finance-setup-trail-codes.md)|
|Geef standaardrapporten op die voor verschillende documenttypen moeten worden gebruikt.|[Rapportselectie in Business Central](across-report-selections.md)|

> [!TIP]
> Afhankelijk van uw geografische locatie bevatten sommige Business Central-pagina's mogelijk velden die niet worden beschreven in de bovengenoemde artikelen, omdat ze van toepassing zijn op lokale functionaliteit of aanpassingen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Werken met dimensies](finance-dimensions.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Cashflow in uw bedrijf analyseren](finance-analyze-cash-flow.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
