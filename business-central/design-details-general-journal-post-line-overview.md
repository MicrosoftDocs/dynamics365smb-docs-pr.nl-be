---
title: Overzicht dagboekboekingsregel
description: 'Dit onderwerp introduceert wijzigingen in Codeunit 12, Dagboek - Boekingsregel, en is de enige plaats om grootboek-, btw- en klant- en leveranciersposten in te voeren.'
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, general ledger, post'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="general-journal-post-line-overview"></a>Overzicht dagboekboekingsregel

Codeunit 12, **Dagboek - Boekingsregel**, is het belangrijkste toepassingsobject voor grootboekboekingen en is de enige plaats om grootboek-, btw, klanten- en leveranciersposten in te voegen. Deze codeunit wordt ook gebruikt voor de bewerkingen Vereffenen, Vereffening ongedaan maken en Tegenboeken.  
  
In Microsoft Dynamics NAV 2013 R2 werd de codeunit opnieuw ontworpen omdat deze erg groot was geworden, met ongeveer 7.600 coderegels. De architectuur is gewijzigd en de codeunit is eenvoudiger en makkelijker te beheren gemaakt. Deze documentatie beschrijft de wijzigingen en bevat informatie die u nodig hebt voor upgrades.  
  
## <a name="old-architecture"></a>Oude architectuur
De oude architectuur had de volgende functies:  
  
* Er werd uitgebreid gebruikgemaakt van algemene variabelen, waardoor de kans op verborgen fouten als gevolg van variabelen met het verkeerde bereik, groter werd.  
* Er waren veel lange procedures (met meer dan 100 coderegels) die ook zeer cyclomatisch complex waren (er werden veel geneste instructies met CASE, REPEAT en IF gebruikt), waardoor de code erg moeilijk te lezen en onderhouden was.  
* Meerdere procedures die alleen lokaal werden gebruikt en alleen waren bedoeld voor lokaal gebruik, waren niet gemarkeerd als lokaal.  
* De meeste procedures hadden geen parameters en gebruikten algemene variabelen. Sommige gebruikten parameters en overschreven algemene door lokale variabelen.  
* De codepatronen voor het zoeken van grootboekrekeningen en het maken van grootboek- en btw-posten waren niet gestandaardiseerd en verschilden per plek. Bovendien waren er veel codedubbelingen en verbroken symmetrie tussen klant- en leverancierscode.  
* Een groot deel van de code in codeunit 12, ongeveer 30 procent, heeft betrekking op berekeningen van contantkorting en betalingstolerantie, hoewel deze voorzieningen in veel landen of regio's niet nodig zijn.  
* Boeken, Vereffenen, Vereffening ongedaan maken, Tegenboeken, Contantkorting en betalingstolerantie, en Wisselkoersherwaardering waren aan elkaar gekoppeld in codeunit 12 met gebruik van een lange lijst van algemene variabelen.  
  
### <a name="new-architecture"></a>Nieuwe architectuur
In [!INCLUDE[prod_short](includes/prod_short.md)] heeft codeunit 12 de volgende verbeteringen:  
  
* Codeunit 12 is opnieuw gestructureerd in kleinere procedures (alle korter dan 100 coderegels).  
* Gestandaardiseerde patronen voor de zoekopdracht van grootboekrekeningen zijn geïmplementeerd door het gebruik van Help-functies uit de boekingsgroeptabellen.  
* Er is een boekingsengineframework geïmplementeerd om het begin en eind van transacties te beheren, en het maken van grootboek- en btw-posten, het verzamelen van btw-aanpassingen en het berekenen van aanvullende valutabedragen te scheiden.  
* Codeverdubbeling is uitgeschakeld.  
* Veel Help-functies zijn overgebracht naar overeenkomstige tabellen voor klant- en leveranciersposten.  
* Het gebruik van algemene variabelen is geminimaliseerd, zodat elke procedure parameters gebruikt en een eigen toepassingslogica omvat.  
  
## <a name="see-also"></a>Zie ook

[Ontwerpdetails: boekingsinterfacestructuur](design-details-posting-interface-structure.md)  
[Ontwerpdetails: boekingsenginestructuur](design-details-posting-engine-structure.md)  
[Ontwerpdetails: dagboekboekingsregel (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
