---
title: Een vraagprognose maken | Microsoft Docs
description: U kunt verkoop- en productieprognoses maken op de pagina **Vraagprognose**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/29/2020
ms.author: sgroespe
ms.openlocfilehash: 71d62cdd0e21d0eb2d10f5b33e30be91e92d0928
ms.sourcegitcommit: 1c286468697d403b9e925186c2c05e724d612b88
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/31/2020
ms.locfileid: "2999940"
---
# <a name="create-a-demand-forecast"></a>Een vraagprognose maken
U kunt verkoop- en productieprognoses maken op de pagina **Vraagprognose**.  

De prognosefunctionaliteit wordt gebruikt om een verwachte vraag aan te maken; de werkelijke vraag komt voort uit verkoop- en productieorders. Tijdens het opstellen van het MPS (Master Production Schedule) wordt de prognose tot een nettowaarde teruggebracht tegen de verkoop- en productieorders. De optie *Onderdeel* op de prognose bepaalt met welke soort vraag rekening wordt gehouden in het proces van het berekenen van de nettowaarde. Als de prognose wordt uitgevoerd voor een verkoopartikel, worden alleen verkooporders gebruikt tegen de prognose. Als het materialen betreft, wordt alleen afhankelijke vraag van productieordermaterialen gebruikt tegen de prognose.  

Met behulp van prognoses kan uw bedrijf "wat als"-scenario's opstellen en efficiënt en kosteneffectief plannen voor en voorzien in de vraag. Nauwkeurige prognoses kunnen een doorslaggevend verschil maken voor de klanttevredenheid met betrekking tot ordertoezeggingsdatums en tijdige levering.  

## <a name="sales-forecasts-and-production-forecasts"></a>Verkoopprognoses en productieprognoses  
De prognosefunctionaliteit in de toepassing kan worden gebruikt voor het maken van verkoop- of productieprognoses, in combinatie of onafhankelijk van elkaar. De meeste bedrijven die op order produceren, houden bijvoorbeeld geen voorraad eindproducten aan, omdat elk artikel op bestelling wordt geproduceerd. Het vooruitlopen op orders (verkoopprognoses) is van essentieel belang voor een redelijke doorlooptijd van eindproducten (productieprognoses). Zo kunnen bijvoorbeeld onderdelen met een lange levertijd de productie vertragen als deze niet besteld of in voorraad zijn.  

-   De verkoopprognose is de beste schatting die de verkoopafdeling kan maken over toekomstige verkopen, en deze wordt gespecificeerd per artikel en per periode. De verkoopprognose is echter niet altijd voldoende voor de productie.  
-   De productieprognose is de inschatting van de productieplanner van het aantal eindartikelen en afgeleide subassemblageartikelen in specifieke perioden moeten worden geproduceerd om te voldoen aan de voorspelde verkopen.  

In de meeste gevallen wijzigt dus de productieplanner de verkoopprognose zodat deze past bij de productieomstandigheden, terwijl toch aan de verkoopprognose wordt voldaan.  

U kunt handmatig prognoses maken op de pagina **Vraagprognose**. Er kunnen in het systeem meerdere prognoses bestaan, die aan de hand van de naam en de soort van elkaar worden onderscheiden. Prognoses kunnen desgewenst worden gekopieerd en bewerkt. Het is wel zo dat op elk moment slechts één prognose geldig kan zijn voor planningsdoeleinden.  

De prognose bestaat uit een aantal records, die elk het artikelnummer, de prognosedatum en het prognoseaantal bevatten. De prognose van een artikel bestrijkt een periode, die wordt bepaald door de prognosedatum en de prognosedatum van de volgende (latere) prognoserecord. Vanuit het oogpunt van planning moet het prognoseaantal beschikbaar zijn bij aanvang van de vraagperiode.  

Een prognose moet worden aangeduid als *Verkoopartikel*, *Materiaal* of *Beide*. De prognosesoort *Verkoopartikel* wordt gebruikt voor verkoopprognoses. De productieprognose wordt gemaakt met behulp van de soort *Onderdeel*. De prognosesoort *Beide* wordt alleen gebruikt om de planner een overzicht te geven van zowel de verkoopprognose als de productieprognose. Bij deze optie kunnen de prognoseposten niet worden bewerkt. Door deze prognosesoorten hier aan te duiden kunt u hetzelfde werkblad gebruiken voor het invoeren van een verkoopprognose als u doet bij een productieprognose, en kunt u hetzelfde blad gebruiken om beide prognoses tegelijkertijd te bekijken. Het is wel zo dat het systeem de verschillende inputs (verkoop en productie) verschillend gebruikt bij het berekenen van de planning, gebaseerd op artikel, productie en productie-instellingen.  

## <a name="component-forecast"></a>Materiaalprognose  
De materiaalprognose kan worden beschouwd als een optieprognose in relatie tot een hoofdartikel. Dit kan bijvoorbeeld nuttig zijn als de planner de vraag naar het materiaal kan schatten.  

Omdat de materiaalprognose is ontworpen om opties te definiëren voor een hoofdartikel, moet de materiaalprognose gelijk aan of kleiner zijn dan het prognoseaantal van het verkoopartikel. Als de materiaalprognose hoger is dan de verkoopartikelprognose, beschouwt het systeem het verschil tussen deze twee soorten prognoses als onafhankelijke vraag.  

## <a name="forecasting-periods"></a>Prognoseperioden  
 De prognoseperiode is geldig vanaf de begindatum tot de datum waarop de volgende prognose begint. Het tijdsintervalvenster biedt u meerdere keuzemogelijkheden om de vraag op en bepaalde datum in een periode in te voegen. Het is daarom raadzaam om het bereik van de prognoseperiode niet te wijzigen, tenzij u alle prognoseposten naar de begindatum van deze periode wilt verplaatsen.  

## <a name="forecast-by-locations"></a>Prognose per locatie  
In de productie-instellingen kan worden gesteld dat u prognoses wilt filteren volgens locatie wanneer u een plan berekent. Het is wel zo dat indien op locatie gebaseerde prognoses los van elkaar worden bekeken, de totale prognose mogelijk niet representatief is.

## <a name="to-create-a-demand-forecast"></a>Een vraagprognose maken

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vraagprognose** in en kies de desbetreffende koppeling.  
2. Selecteer op het sneltabblad **Algemeen** een prognose in het veld **Vraagprognosenaam**. Meerdere prognoses zijn mogelijk: deze zijn van elkaar te onderscheiden door de naam en het prognosetype.  
3. Selecteer in het veld **Vestigingsfilter** de vestiging waarop deze prognose van toepassing is.
4. In het veld **Weergeven per** om de periode te wijzigen die in elke kolom wordt weergegeven. U kunt kiezen uit de volgende intervallen: **Dag**, **Week**, **Maand**, **Kwartaal**, **Jaar** of de **Boekingsperiode**, zoals ingesteld in financiële gebied.    

> [!NOTE]  
>  Bedenk goed welk tijdsinterval u wilt gebruiken voor toekomstige prognoses, zodat u steeds dezelfde tijdsinterval gebruikt. Wanneer u een voorspeld aantal invoert, is dast geldig vanaf de eerste dag van het door u geselecteerde tijdsinterval. Als u bijvoorbeeld een maand selecteert, voert u het voorspelde aantal op de eerste dag van de maand in. Als u een kwartaal selecteert, voert u het voorspelde aantal op de eerste dag van de eerste maand van het kwartaal in.

5. Selecteer in het veld **Weergeven als** hoe de voorspelde aantallen voor het tijdsinterval moeten worden weergegeven. Als u **Mutatie** selecteert, wordt de mutatie in het saldo weergegeven voor het tijdsinterval. Als u **Saldo t/m datum** selecteert, wordt op de pagina het saldo van de laatste dag van het tijdsinterval weergegeven.  
6. Selecteer in het veld **Prognosesoort** **Verkoopartikel**, **Component** of **Beide**. Als u **Verkoopartikel** of **Component** selecteert, kunt u het aantal per periode bewerken. Als u **Beide** selecteert, kunt u het aantal niet bewerken, maar wel de knop met de pijl omlaag kiezen om de posten voor de vraagprognose weer te geven.  
7. Geef een **datumfilter** op als u de hoeveelheid gegevens die wordt weergegeven wilt beperken.  
8. Voer op het sneltabblad **Matrix voor vraagprognose** de voorspelde hoeveelheden in door een hoeveelheid te typen in de cel die een item op een bepaalde datum of periode vertegenwoordigt. In lege cellen opent de opzoekknop een lege pagina die aangeeft dat u handmatig een waarde moet invoeren.   

> [!NOTE]  
>  U kunt ook een bestaande prognose bewerken. Kies op de pagina **Matrix voor vraagprognose** de actie **Vraagprognose kopiëren** en vul de pagina **Vraagprognose** met een bestaande prognose. U kunt de aantallen waar nodig wijzigen.  

## <a name="see-also"></a>Zie ook  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
