---
title: Voorraadwaardering en kostprijsberekening instellen
description: 'Als u ervoor wilt zorgen dat voorraadkosten correct worden vastgelegd, moet u verschillende velden en pagina''s instellen voordat u artikeltransacties gaat maken.'
author: SorenGP
ms.topic: conceptual
ms.search.keywords: null
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="setting-up-inventory-valuation-and-costing" />Voorraadwaardering en kostprijsberekening instellen

Als u ervoor wilt zorgen dat voorraadkosten correct worden vastgelegd, moet u verschillende velden en pagina's instellen voordat u artikeltransacties gaat maken. Bedrijven kiezen doorgaans een specifieke kostprijsmethode en passen die bijvoorbeeld toe op voorraadartikelen om hen te helpen de waarde van artikelen op voorraad bij te houden.  

> [!TIP]
> Voor een inleiding in kostenberekening in [!INCLUDE [prod_short](includes/prod_short.md)] raadpleegt u [Over voorraadwaardering](finance-learn-about-costing.md).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|
|Geef een standaardwaarderingsmethode op voor het bedrijf om te bepalen hoe de inkomende kostprijs ervan wordt gebruikt om voorraadwaarde en de kostprijs van verkochte goederen vast te leggen.|[Algemene voorraadgegevens instellen](inventory-how-setup-general.md)|  
|Geef een waarderingsmethode op voor afzonderlijke artikelen als ze een andere kostprijsberekeningsmethode vereisen.|[Nieuwe artikelen registreren](inventory-how-register-new-items.md)|  
|Ervoor te zorgen dat de kostprijs automatisch wordt geboekt in het grootboek elke keer wanneer een voorraadtransactie wordt geboekt.|Het veld **Autom. voorraadwaarde boeken** op de pagina **Voorraadinstelling**|  
|Ervoor te zorgen dat verwachte kosten worden geboekt in het grootboek om vanuit de interimgrootboekrekeningen een schatting te kunnen zien van de te betalen bedragen en de kostprijs van de verhandelde artikelen voordat ze worden gefactureerd.|Het veld **Verw. kostprijs naar GB boeken** op de pagina **Voorraadinstelling**|  
|Het systeem in te stellen zodat het bij het boeken van voorraadtransacties automatisch wordt aangepast in het geval van eventuele wijzigingen van de kostprijs.|[Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md)|  
|Definieer of de gemiddelde kostprijs alleen moet worden berekend per artikel of per artikel voor elke voorraadunit en voor elke variant van het artikel.|Het veld **Gem. kostprijsberekeningsoort** op de pagina **Voorraadinstelling**|  
|Selecteer de periode die de toepassing moet gebruiken voor het berekenen van de gewogen gemiddelde kostprijs van artikelen die gebruik maken van de gemiddelde waarderingsmethode.|Het veld **Periode gemiddelde kostprijsberekening** op de pagina **Voorraadinstelling**|  
|Voorraadperioden te definiëren om de voorraadwaarde in het verloop van tijd te controleren door het boeken van transacties niet toe te staan in gesloten voorraadperioden.|[Werken met voorraadperioden](finance-how-to-work-with-inventory-periods.md)|  
|Zorg dat verkoopretouren worden vereffend met de oorspronkelijke uitgaande transactie om voorraadwaarde te behouden.|Het veld **Precieze kostenvereff. verplicht** op de pagina **Verkopen en Klanten**|  
|Zorg dat inkoopretouren worden vereffend met de oorspronkelijke inkomende transactie om voorraadwaarde te behouden.|Het veld **Precieze kostenvereff. verplicht** op de pagina **Inkopen en Leveranciers**|
|De afrondingsregels in te stellen die van toepassing zijn bij het aanpassen of suggereren van artikelprijzen en bij het aanpassen of suggereren van vaste verrekenprijzen.|De pagina **Afrondingsmethode**|  

## <a name="see-also" />Zie ook

[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Algemene voorraadgegevens instellen](inventory-how-setup-general.md)  
[Voorraadkosten reconciliëren met het grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Best Practices voor instellen: Waarderingsmethode](setup-best-practices-costing-method.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails - De waarderingsmethode voor artikelen wijzigen](design-details-changing-costing-methods.md)  
[Werken met Business Central](ui-work-product.md)  
[Financiën](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
