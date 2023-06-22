---
title: Productieprocessen configureren
description: 'Als u materiaal wilt omzetten in geproduceerde eindartikelen, moeten productieresources, zoals stuklijsten, bewerkingsplannen, machinebedienden en machines worden ingesteld in het systeem.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000768, 99000779, 99000780, 99000866'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-manufacturing" />Productie instellen

Als u materiaal wilt omzetten in geproduceerde eindartikelen, moeten productieresources, zoals stuklijsten, bewerkingsplannen, machinebedienden en machines worden ingesteld in het systeem.

Machinebedienden en machines worden in het systeem weergegeven als bewerkingsplaatsen die in afdelingen en afdelingsgroepen kunnen worden ingedeeld. Wanneer deze resources zijn ingesteld, kunnen hieraan bewerkingen worden toegewezen aan de hand van de gedefinieerde materiaal- (stuklijst) en processtructuur (bewerkingsplan) voor het artikel en volgens de capaciteit van de bewerkingsplaats of afdeling. U kunt ook de productiecapaciteit van elke afzonderlijke resource instellen. De capaciteit wordt gedefinieerd aan de hand van de beschikbare werktijd voor de machine en afdelingen en wordt bepaald door agenda's voor elk niveau. In een agenda voor een afdeling worden de gegevens voor het aantal werkdagen of -uren, de diensten, de vakantiedagen en de afwezigheid aangegeven die de bruto beschikbare capaciteit van de afdeling bepalen (gewoonlijk uitgedrukt in minuten). Dit alles wordt bepaald door de waarden die zijn gedefinieerd voor de efficiency en capaciteit.  

Wanneer u de productie hebt ingesteld, kunt u productieorders plannen en uitvoeren. Zie [Planning](production-planning.md) en [Productie](production-manage-manufacturing.md) voor meer informatie.  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|De productiefuncties configureren, zoals het definiëren van shopfloorwerkuren en het selecteren van planningsparameters.|De pagina **Productie-instellingen**.|
|Stel op het tabblad **Planning** op de pagina **Productie-instellingen** globale planningsparameters in die parameters overschrijven die op individuele artikelkaarten zijn ingesteld.|[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)|
|Een standaardwerkweek in de productieafdeling definiëren met de begin- en eindtijd van elke werkdag en de bijbehorende dienst.|[Productieagenda's maken](production-how-to-create-work-center-calendars.md)|  
|Vaste waarden en vereisten van productieresources indelen als afdelingen of bewerkingsplaatsen om de productie-output te bepalen.|[Afdelingen en bewerkingsplaatsen instellen](production-how-to-set-up-work-and-machine-centers.md)|
|Productiebewerkingen in de vereiste volgorde indelen en met de vereiste werktijden toewijzen aan afdelingen of bewerkingsplaatsen.|[Bewerkingsplannen maken](production-how-to-create-routings.md)|
|Productiematerialen of halffabricaten indelen onder een geproduceerd hoofdartikel en de stuklijst voor uitvoering certificeren in afdelingen.|[Productiestuklijsten maken](production-how-to-create-production-boms.md)|
|Controleren of het juiste onderdeelaantal beschikbaar is als geproduceerde artikelen in één eenheid in voorraad zijn, maar in een andere eenheid worden geproduceerd.|[Werken met productiebatcheenheden](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Productfamilies met productieartikelen definiëren met soortgelijke productieprocessen om op verbruik te besparen. Uit één vel kunnen bijvoorbeeld tegelijkertijd vier stuks van het ene artikel en tien stuks van een ander artikel worden geproduceerd.|[Werken met productfamilies](production-how-work-family.md)|
|Standaardtaken gebruiken om het maken van bewerkingsplannen te vereenvoudigen door extra informatie bij te voegen voor terugkerende bewerkingen.|[Standaardbewerkingsplanregels instellen](production-how-set-up-standard-routing-lines.md)|  
|Afdelingen en bewerkingsplannen voor uitbestede productiebewerkingen voorbereiden.|[Productie uitbesteden](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also" />Zie ook

[Productie](production-manage-manufacturing.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
