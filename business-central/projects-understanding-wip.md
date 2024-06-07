---
title: OHW-methoden gebruiken om projectvooruitgang te berekenen en te registreren
description: 'Beschrijft de verschillende OHW-methoden die u kunt gebruiken om financiële gegevens voor lopende projecten te boeken, te controleren en te berekenen die bezig zijn.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# WIP-methoden in projectbeheer begrijpen

Naarmate een project vordert, worden materialen, resources en overige zaken verbruikt en moeten hiervoor boekingen plaatsvinden op het project. Onderhanden werk (OHW) is een functie waarmee u de financiële waarde van projecten in het grootboek kunt schatten gedurende de projecten. In veel gevallen kunt u kosten voor een project boeken voordat u het project factureert. Wanneer alleen kosten zijn geboekt, klopt het financiële afschrift niet.

Als u de waarde in het grootboek wilt volgen, kunt u het OHW-bedrag berekenen en de waarde boeken in het grootboek. Zie voor meer informatie [Voortgang en prestaties van projecten bewaken](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt de volgende methoden om de waarde van onderhanden werk te berekenen en vast te leggen.

| OHW-methode | Berekeningsformule | Omschrijving van berekening |
| --- | --- | --- |
| Kostenwaarde |Verantwoorde omzet = Factureerbaar (gefactureerde prijs) <br /><br />Budgetkostenverhouding = Totale budgetkosten x Totale budgetprijs <br /><br />Geschatte totale kostprijs = Factureerbaar (totale prijs) x Budgetkostenverhouding <br /><br />Voltooiingspercentage = Gebruik (totale kostprijs) / Budget (totale kostprijs) <br /><br />Gefactureerd % = Factureerbaar (gefactureerde prijs) / Factureerbaar (totale prijs) <br /><br />OHW-kosten = (Percentage voltooid - Gefactureerd %) x Geschatte totale kostprijs <br /><br />Verantwoorde kosten = Totale gebruikskosten - OHW-kosten|Het berekenen van de kostenwaarde wordt gestart door de waarde te berekenen van wat er is aangeleverd, door een deel van de geschatte totale kosten op basis van percentage voltooid te nemen. De gefactureerde kosten worden afgetrokken door een deel van de geschatte totale kosten op basis van het gefactureerde percentage te nemen.<br /><br />Voor deze berekening moeten de factureerbare totale prijs, de totale budgetprijs en de totale budgetkosten correct worden ingevoerd voor het hele project. |
| Kosten van verkoop |Verantwoorde omzet = Factureerbaar (gefactureerde prijs)<br /><br /> Verantwoorde kosten = Budget (totale kostprijs) x Gefactureerd percentage<br /><br /> Gefactureerd % = Factureerbaar (gefactureerde prijs) / Factureerbaar (totale prijs)<br /> (Gefactureerd % is een kolom in projecttaakregels)<br /><br /> OHW-kosten = Gebruik (totale kosten) - Verantwoorde kosten |Het berekenen van de kosten van de verkoopprijs wordt gestart door de verantwoorde kosten te berekenen. Kosten worden proportioneel verantwoord op basis van totale budgetkosten.<br /><br /> Voor deze berekening moeten de factureerbare totale prijs en de totale budgetkosten correct worden ingevoerd voor het hele project. |
| Verkoopwaarde |Verantwoorde kosten = Gebruik (totale kosten)<br /><br /> Verantwoorde omzet = Gebruik (totale verkoopprijs) x Verwachten factuurverhouding<br /><br /> Kosten-recovery % = Factureerbaar (totale prijs) / Budget (totale prijs)<br /><br /> OHW-omzet = Verantwoorde omzet - Factureerbaar (gefactureerde prijs) |Bij het berekenen van de verkoopprijs wordt de omzet proportioneel verantwoord op basis van de totale kosten van het gebruik en de verwachte kosten van de recovery-verhouding.<br /><br /> Voor deze berekening moeten de factureerbare kostprijs en de totale budgetprijs correct worden ingevoerd voor het hele project. |
| Percentage van voltooiing |Verantwoorde kosten = Gebruik (totale kosten)<br /><br /> Verantwoorde omzet = Factureerbaar (totale prijs) x Voltooiingspercentage<br /><br /> Voltooiingspercentage = Gebruik (totale kostprijs) / Budget (totale kostprijs)<br /> (Vastgelegd in veld **Taakvoltooiing %** op projecttaakregels)<br /><br /> OHW-omzet = Verantwoorde omzet - Factureerbaar (gefactureerde prijs) |Bij het berekenen van het voltooiingspercentage worden inkomsten proportioneel verantwoord op basis van het percentage voltooid, dat wil zeggen de totale kosten van het gebruik versus de budgetkosten.<br /><br /> Voor deze berekening moeten de factureerbare totale prijs en de totale budgetkosten correct worden ingevoerd voor het hele project. |
| Voltooid contract |OHW-bedrag = Totale OHW-kosten = Gebruik (totale kostprijs)<br /><br /> Omzet OHW = Factureerbaar (gefactureerde prijs) |Bij Contract voltooid worden de inkomsten en de kosten pas verantwoord als het project is voltooid. U kunt hiervoor kiezen als de geschatte kosten en inkomsten van het project nog niet zeker zijn.<br /><br /> Al het gebruik wordt op de OHW-kostenrekening (activum) geboekt, terwijl alle gefactureerde omzet op de rekening gefactureerde omzet OHW (passief) wordt geboekt totdat het project is voltooid. |

## Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
