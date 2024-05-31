---
title: Lotgroottes hanteren
description: In dit onderwerp worden verschillende manieren beschreven om met lotgroottes om te gaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Omgaan met lotgroottes in productie
In termen van hoeveelheid komt het aantal artikelen dat u in een productiebewerking produceert mogelijk niet overeen met hoe ze worden verkocht. U kunt bijvoorbeeld honderden artikelen in één lot produceren, maar elk artikel afzonderlijk verkopen. Wanneer u uw productieroutes en stuklijsten (BOM's) configureert, zijn er enkele nuances waarmee u rekening moet houden met betrekking tot lotgroottes. In dit onderwerp wordt beschreven hoe lotgroottes van invloed zijn op kostenberekeningen en resourceplanning.

## Maateenheden in productiestuklijsten
Hoewel u de basismaateenheid voor een artikel opgeeft, kan uw stuklijst een andere maateenheid voor het eindproduct gebruiken. De basismaateenheid voor een artikel kan bijvoorbeeld stuks zijn, maar uw stuklijst kan om pallets of ton vragen. Dit is handig wanneer uw machines of ruwe componenten het volume dicteren. U wilt bijvoorbeeld waarschijnlijk niet één enkele muffin bakken, omdat het moeilijk is om een deel van een ei te gebruiken. In plaats daarvan bakt u een partij muffins om verspilling te verminderen. Zie voor meer informatie [Productiestuklijsten maken](production-how-to-create-production-boms.md).

## Lotgrootte op bewerkingsplanregels
Vanuit een bewerkingsplanperspectief kunt u een lotgrootte op bewerkingsplanregels specificeren om deze af te stemmen op de capaciteit van de machines die de artikelen produceren. De looptijd op bewerkingsregels wordt proportioneel verminderd met de lotgrootte. 

Dit werkt goed als de hoeveelheid op een productieorder een factor is van de lotgrootte op de route. Als uw bakplaat bijvoorbeeld 10 muffins kan bevatten, moet u er 10, 20, 30, enzovoort bakken, en niet 5 of 15.  Dit is veel minder een probleem als u te maken heeft met grote hoeveelheden.

De lotgrootte is ook populair in productieomgevingen waar de output wordt gemeten als de hoeveelheid die u gedurende een bepaalde tijd kunt maken. Als het volume per dienst van 9 uur 25.000 kubieke voet is, kunt u de looptijd instellen op 9 uur en de lotgrootte op 25.000.
De hoeveelheid van de productieorder wordt minder belangrijk omdat op de productieorder de doorlooptijd wordt berekend als de doorlooptijd / lotgrootte om de doorlooptijd per stuk te krijgen.
 
> [!NOTE]
> De waarde die is gedefinieerd in Lotgrootte heeft geen invloed op de tijd die is opgegeven in het veld **Insteltijd** van de bewerkingsplanregel. De instelling vindt slechts één keer plaats, zelfs als er meerdere lots zijn. Zo hoeft u de oven bijvoorbeeld niet voor de tweede lot muffins op te warmen. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).

## Lotgroottes voor artikelen en voorraadeenheden
Lotgroottes die zijn gedefinieerd voor bewerkingsplannen zijn niet hetzelfde als lotgroottes voor artikelen of SKU's. Die waarden worden voor een ander doel gebruikt en hebben geen invloed op de productiecapaciteit. 

## Lotgrootte voor artikelen en SKU's
Voor artikelen en SKU's hebben lotgroottes de volgende effecten op de kostenberekening en voorraadplanning:

* Voor standaardkostenberekening: als u **Kosten incl. instelling** inschakelt op de pagina **Productie-instellingen** worden de kosten voor de instelling opgeteld bij de standaardkosten. Als u een lotgrootte opgeeft, worden de instelkosten voor bewerkingsplanbewerking verlaagd volgens één lotgrootte. Als de op de artikelkaart de gedefinieerde lotgrootte bijvoorbeeld 10 is en het 15 minuten duurt om de oven op te warmen, worden de kosten van de brandstof aan de 10 muffins toegewezen als ongeveer 1,5 minuut. 

> [!NOTE]
> Instelkosten worden anders afgehandeld vanuit het perspectief van standaardkosten en capaciteitstoewijzing. Als de geproduceerde hoeveelheid niet overeenkomt met de in de artikelkaart gedefinieerde lotgrootte, zal dat tot variatie leiden. Zie [Voorraadkosten beheren](finance-manage-inventory-costs.md) voor meer informatie. <!--not sure that I got this part right seems to repeat the first example.-->

Voor leveringsplanning werkt de lotgrootte-instelling op artikelen met het **Demping standaardhoeveelheid %** op de pagina **Productie-instellingen**. [!INCLUDE[prod_short](includes/prod_short.md)] zal veranderingen in de vraag die onder het dempingspercentage liggen, negeren en geen planningsvoorstellen doen. Er is bijvoorbeeld 15 gespecificeerd in het veld Demping standaardhoeveelheid % en we hebben een productieorder voor 20 muffins voor 20 gasten, maar één gast kan niet aanwezig zijn. [!INCLUDE[prod_short](includes/prod_short.md)] negeert de enkele ontbrekende gast omdat het slechts 10% is van de lotgrootte 10 die voor het item is gedefinieerd. Als twee gasten het echter niet redden, stelt [!INCLUDE[prod_short](includes/prod_short.md)] voor dat we de bestelhoeveelheid verminderen omdat twee 20% van de lotgrootte is. Zie voor meer informatie over planning [Planning](production-planning.md).

## Zie ook
[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Werken met productiebatcheenheden](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Bewerkingsplannen maken](production-how-to-create-routings.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]