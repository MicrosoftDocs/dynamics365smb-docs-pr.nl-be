---
title: Ontwerpdetails - Lot-voor-lot | Microsoft Docs
description: Leer hoe u het lot-voor-lot-beleid gebruikt om het orderaantal te vereffenen op basis van de vraag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3b80738be6dfe9d171a3cad56edf56cfa4960180
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/16/2019
ms.locfileid: "938146"
---
# <a name="design-details-lot-for-lot"></a>Ontwerpdetails: Lot-voor-lot
Het lot-for-lot-beleid is het meest flexibel omdat het systeem alleen reageert op werkelijke vraag, én rekening houdt met verwachte vraag uit prognoses en raamcontracten en vervolgens het orderaantal op basis van de vraag vereffent. Het lot-for-lot-beleid is bedoeld voor A- en B-artikelen waar voorraad kan worden geaccepteerd maar vermeden moet worden.  

In sommige opzichten lijkt het lot-voor-lot beleid op het orderbeleid, maar het hanteert een algemene aanpak van artikelen; het kan aantallen in voorraad accepteren en het bundelt vraag en corresponderend aanbod in tijdsintervallen die door de gebruiker worden gedefinieerd.  

Het tijdsinterval wordt gedefinieerd in het veld **Tijdsinterval**. Er wordt gewerkt met een minimumtijdsinterval van één dag, aangezien dit de kleinste tijdseenheid voor vraag- en voorzieningsgebeurtenissen in het systeem is (hoewel in de praktijk de tijdseenheid voor productieorders en materiaalbehoeften zelfs seconden kan zijn).  

Met het tijdsinterval worden ook limieten ingesteld wanneer een bestaande voorzieningenorder opnieuw moet worden gepland om te voldoen aan een bepaalde vraag. Als het aanbod binnen het tijdsinterval ligt, wordt het opnieuw in of uit gepland om aan de vraag te voldoen. Als de voorziening eerder ligt, ontstaat onnodige opeenhoping van voorraad en moet worden geannuleerd. Als het later ligt, wordt in plaats daarvan een nieuwe order gemaakt.  

Met dit beleid is het ook mogelijk om een veiligheidsvoorraad te definiëren om mogelijke schommelingen in voorzieningen op te vangen of te voldoen aan plotselinge vraag.  

Omdat het aantal van de voorzieningenorder op de werkelijke vraag is gebaseerd, kan het zinnig zijn de orderwijzigingen te gebruiken: rond het orderaantal naar boven af om aan een opgegeven orderveelvoud (of inkoopeenheid) te voldoen, vergroot de order tot een opgegeven minimaal orderaantal of verlaag het aantal tot het opgegeven maximale aantal (en maak zo twee of meer voorzieningen om het totaal benodigde aantal te bereiken).  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
