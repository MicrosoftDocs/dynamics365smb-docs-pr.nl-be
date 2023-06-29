---
title: Een vraagprognose maken
description: Lees meer over de vraagprognosefuncties en hoe u verkoop- en productieprognoses kunt maken.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9245, 99000919, 99000921, 99000922'
ms.date: 03/11/2022
ms.author: edupont
---
# <a name="create-a-demand-forecast"></a><a name="create-a-demand-forecast"></a>Een vraagprognose maken

U kunt verkoop- en productieprognoses maken op de lijstpagina **Vraagprognoses**. Vervolgens specificeert u voor elke prognose verschillende instellingen voor die prognose op de pagina **Overzicht vraagprognoses**.  

De prognosefunctionaliteit wordt gebruikt om een verwachte vraag aan te maken; de werkelijke vraag komt voort uit verkoop- en productieorders. Tijdens het opstellen van het MPS (Master Production Schedule) wordt de prognose tot een nettowaarde teruggebracht tegen de verkoop- en productieorders. Het veld **Prognosesoort** op de prognose bepaalt met welke soort vraag rekening wordt gehouden in het proces van het berekenen van de nettowaarde. Als de prognose wordt uitgevoerd voor een *verkoopartikel*, worden alleen verkooporders gebruikt tegen de prognose. Als het *materialen* betreft, wordt alleen afhankelijke vraag van productieordermaterialen gebruikt tegen de prognose.  

Met behulp van prognoses kan uw bedrijf "wat als"-scenario's opstellen en efficiënt en kosteneffectief plannen voor en voorzien in de vraag. Nauwkeurige prognoses kunnen een doorslaggevend verschil maken voor de klanttevredenheid met betrekking tot ordertoezeggingsdatums en tijdige levering.  

Met releasewave 1 van 2022 kunt u ook het juiste detailniveau definiëren in de velden **Prognose per locatie** en **Prognose per variant** op de pagina **Overzicht vraagprognoses**. Filters en andere instellingen worden opgeslagen in de tabel **Naam vraagprognose**. U kunt dus gemakkelijk stoppen en later verder gaan met uw werk. Als uw organisatie is bijgewerkt naar releasewave1 van 2022, moet u de nieuwe ervaring inschakelen op de pagina [Functiebeheer](admin-feature-management.md).  

## <a name="sales-forecasts-and-production-forecasts"></a><a name="sales-forecasts-and-production-forecasts"></a>Verkoopprognoses en productieprognoses

De prognosefunctionaliteit in de toepassing kan worden gebruikt voor het maken van verkoop- of productieprognoses, in combinatie of onafhankelijk van elkaar. De meeste bedrijven die op order produceren, houden bijvoorbeeld geen voorraad eindproducten aan, omdat elk artikel op bestelling wordt geproduceerd. Het vooruitlopen op orders (verkoopprognoses) is van essentieel belang voor een redelijke doorlooptijd van eindproducten (productieprognoses). Zo kunnen bijvoorbeeld onderdelen met een lange levertijd de productie vertragen als deze niet besteld of in voorraad zijn.  

- De verkoopprognose is de beste schatting die de verkoopafdeling kan maken over toekomstige verkopen, en deze wordt gespecificeerd per artikel en per periode. De verkoopprognose is echter niet altijd voldoende voor de productie.  
- De productieprognose is de inschatting van de productieplanner van het aantal eindartikelen en afgeleide subassemblageartikelen in specifieke perioden moeten worden geproduceerd om te voldoen aan de voorspelde verkopen.  

In de meeste gevallen wijzigt dus de productieplanner de verkoopprognose zodat deze past bij de productieomstandigheden, terwijl toch aan de verkoopprognose wordt voldaan.  

U kunt handmatig prognoses maken op de pagina **Vraagprognose**. Er kunnen in het systeem meerdere prognoses bestaan, die aan de hand van de naam en de soort van elkaar worden onderscheiden. Prognoses kunnen desgewenst worden gekopieerd en bewerkt. 

> [!NOTE]
> Er is slechts één prognose tegelijk geldig voor planningsdoeleinden.

De prognose bestaat uit een aantal records, die elk het artikelnummer, de prognosedatum en het prognoseaantal bevatten. De prognose van een artikel bestrijkt een periode, die wordt bepaald door de prognosedatum en de prognosedatum van de volgende (latere) prognoserecord. Vanuit het oogpunt van planning moet het prognoseaantal beschikbaar zijn bij aanvang van de vraagperiode.  

Een prognose moet worden aangeduid als *Verkoopartikel*, *Materiaal* of *Beide*. De prognosesoort *Verkoopartikel* wordt gebruikt voor verkoopprognoses. De productieprognose wordt gemaakt met behulp van de soort *Onderdeel*. De prognosesoort *Beide* wordt alleen gebruikt om de planner een overzicht te geven van zowel de verkoopprognose als de productieprognose. Bij deze optie kunnen de prognoseposten niet worden bewerkt. Door deze prognosesoorten hier aan te duiden kunt u hetzelfde werkblad gebruiken voor het invoeren van een verkoopprognose als u doet bij een productieprognose, en kunt u hetzelfde blad gebruiken om beide prognoses tegelijkertijd te bekijken. Het is wel zo dat het systeem de verschillende inputs (verkoop en productie) verschillend gebruikt bij het berekenen van de planning, gebaseerd op artikel, productie en productie-instellingen.  

## <a name="component-forecast"></a><a name="component-forecast"></a>Materiaalprognose

De materiaalprognose kan worden beschouwd als een optieprognose in relatie tot een hoofdartikel. Dit kan bijvoorbeeld nuttig zijn als de planner de vraag naar het materiaal kan schatten.  

Omdat de materiaalprognose is ontworpen om opties te definiëren voor een hoofdartikel, moet de materiaalprognose gelijk aan of kleiner zijn dan het prognoseaantal van het verkoopartikel. Als de materiaalprognose hoger is dan de verkoopartikelprognose, beschouwt het systeem het verschil tussen deze twee soorten prognoses als onafhankelijke vraag.  

## <a name="forecasting-periods"></a><a name="forecasting-periods"></a>Prognoseperioden

De prognoseperiode is geldig vanaf de begindatum tot de datum waarop de volgende prognose begint. Het tijdsintervalvenster biedt u meerdere keuzemogelijkheden om de vraag op en bepaalde datum in een periode in te voegen. Het is daarom raadzaam om het bereik van de prognoseperiode niet te wijzigen, tenzij u alle prognoseposten naar de begindatum van deze periode wilt verplaatsen.  

## <a name="forecast-by-locations"></a><a name="forecast-by-locations"></a>Prognose per locatie

Op de pagina **Productie-instellingen** kunt u opgeven of de vestigingen die zijn gedefinieerd in prognoses, wilt overwegen wanneer u plannen berekent. 

### <a name="use-forecast-by-locations"></a><a name="use-forecast-by-locations"></a>Prognose per vestiging gebruiken

Als u de schakelaar **Prognose per vestiging gebruiken** inschakelt, respecteert [!INCLUDE[prod_short](includes/prod_short.md)] alle vestigingscodes die zijn opgegeven voor elk vraagprognose-item en berekent het de resterende prognose voor elke vestiging.  

Beschouw dit voorbeeld eens: uw bedrijf koopt en verkoopt artikelen op twee locaties: OOST en WEST. Voor beide locaties heeft u een lot-naar-lot bestelbeleid geconfigureerd. U maakt een prognose voor de twee locaties:

- 10 stuks voor locatie OOST
- 4 stuks voor locatie WEST

Vervolgens creëert u op locatie WEST een verkooporder met een hoeveelheid van 12 stuks. Het planningssysteem stelt voor dat u het volgende doet:

- Vul 10 stuks aan voor locatie OOST, op basis van gegevens uit de prognose.  
- Vul 12 stuks aan voor vestiging WEST, op basis van de verkooporder. De vier stuks die in de prognose zijn gespecificeerd, worden volledig verbruikt door de werkelijke vraag van de verkooporder. Zie voor meer informatie [Prognosevraag wordt verlaagd door verkooporders](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

> [!NOTE]  
> Als op locatie gebaseerde prognoses los van elkaar worden bekeken, is de totale prognose mogelijk niet representatief.

### <a name="do-not-use-forecast-by-locations"></a><a name="do-not-use-forecast-by-locations"></a>Gebruik prognose per vestiging niet

Als u de schakelaar **Prognose per vestiging gebruiken** uitschakelt, negeert [!INCLUDE[prod_short](includes/prod_short.md)] alle vestigingscodes die zijn opgegeven voor elk vraagprognose-item en combineert het de prognoses tot een prognose voor lege vestigingen.  

Beschouw dit voorbeeld eens: uw bedrijf koopt en verkoopt artikelen op twee locaties: OOST en WEST. Voor beide locaties heeft u een lot-naar-lot bestelbeleid geconfigureerd. U maakt een prognose voor de twee locaties:

- 10 stuks voor locatie OOST
- 4 stuks voor locatie WEST

Vervolgens creëert u op locatie WEST een verkooporder met een hoeveelheid van 12 stuks. Het planningssysteem stelt voor dat u het volgende doet:

- Vul 12 stuks aan voor vestiging WEST, op basis van de verkooporder.  
- Vul 2 stuks bij voor de lege vestiging. De 10 en 4 stuks die in de prognose zijn gespecificeerd, worden gedeeltelijk verbruikt door de werkelijke vraag van de verkooporder. [!INCLUDE[prod_short](includes/prod_short.md)] negeerde de locatiecodes die door de gebruiker waren opgegeven en gebruikt in plaats daarvan een lege vestiging.  

> [!NOTE]  
> U kunt een filter op vestigingen instellen, maar vestiginggebaseerde resultaten komen mogelijk niet overeen met planningsresultaten zonder filters.

## <a name="to-create-a-demand-forecast"></a><a name="to-create-a-demand-forecast"></a>Een vraagprognose maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vraagprognose** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op het sneltabblad **Algemeen** een prognose in het veld **Vraagprognosenaam**. Meerdere prognoses zijn mogelijk: deze zijn van elkaar te onderscheiden door de naam en het prognosetype.  
3. Selecteer in het veld **Vestigingsfilter** de vestiging waarop deze prognose van toepassing is.
4. In het veld **Weergeven per** om de periode te wijzigen die in elke kolom wordt weergegeven. U kunt kiezen uit de volgende intervallen: **Dag**, **Week**, **Maand**, **Kwartaal**, **Jaar** of de **Boekingsperiode**, zoals ingesteld in financiële gebied.

> [!NOTE]  
> Bedenk goed welk tijdsinterval u wilt gebruiken voor toekomstige prognoses, zodat u steeds dezelfde tijdsinterval gebruikt. Wanneer u een voorspeld aantal invoert, is dast geldig vanaf de eerste dag van het door u geselecteerde tijdsinterval. Als u bijvoorbeeld een maand selecteert, voert u het voorspelde aantal op de eerste dag van de maand in. Als u een kwartaal selecteert, voert u het voorspelde aantal op de eerste dag van de eerste maand van het kwartaal in.

5. Selecteer in het veld **Weergeven als** hoe de voorspelde aantallen voor het tijdsinterval moeten worden weergegeven. Als u **Mutatie** selecteert, wordt de mutatie in het saldo weergegeven voor het tijdsinterval. Als u **Saldo t/m datum** selecteert, wordt op de pagina het saldo van de laatste dag van het tijdsinterval weergegeven.  
6. Selecteer in het veld **Prognosesoort** **Verkoopartikel**, **Component** of **Beide**. Als u **Verkoopartikel** of **Component** selecteert, kunt u het aantal per periode bewerken. Als u **Beide** selecteert, kunt u het aantal niet bewerken, maar wel de knop met de pijl omlaag kiezen om de posten voor de vraagprognose weer te geven.  
7. Geef een **datumfilter** op als u de hoeveelheid gegevens die wordt weergegeven wilt beperken.  
8. Voer op het sneltabblad **Matrix voor vraagprognose** de voorspelde hoeveelheden in door een hoeveelheid te typen in de cel die een item op een bepaalde datum of periode vertegenwoordigt. In lege cellen opent de opzoekknop een lege pagina die aangeeft dat u handmatig een waarde moet invoeren.   

> [!NOTE]  
> U kunt ook een bestaande prognose bewerken. Kies op de pagina **Matrix voor vraagprognose** de actie **Vraagprognose kopiëren** en vul de pagina **Vraagprognose** met een bestaande prognose. U kunt de aantallen waar nodig wijzigen.  

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
