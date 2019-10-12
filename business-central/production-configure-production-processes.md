---
title: Productieprocessen configureren | Microsoft Docs
description: Als u materiaal wilt omzetten in geproduceerde eindartikelen, moeten productieresources, zoals stuklijsten, bewerkingsplannen, machinebedienden en machines worden ingesteld in het systeem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2d78632984a3520d03c6bf877e98307ba2206351
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313444"
---
# <a name="setting-up-manufacturing"></a>Productie instellen
Als u materiaal wilt omzetten in geproduceerde eindartikelen, moeten productieresources, zoals stuklijsten, bewerkingsplannen, machinebedienden en machines worden ingesteld in het systeem.

Machinebedienden en machines worden in het systeem weergegeven als bewerkingsplaatsen die in afdelingen en afdelingsgroepen kunnen worden ingedeeld. Wanneer deze resources zijn ingesteld, kunnen hieraan bewerkingen worden toegewezen aan de hand van de gedefinieerde materiaal- (stuklijst) en processtructuur (bewerkingsplan) voor het artikel en volgens de capaciteit van de bewerkingsplaats of afdeling. U kunt ook de productiecapaciteit van elke afzonderlijke resource instellen. De capaciteit wordt gedefinieerd aan de hand van de beschikbare werktijd voor de machine en afdelingen en wordt bepaald door agenda's voor elk niveau. In een agenda voor een afdeling worden de gegevens voor het aantal werkdagen of -uren, de diensten, de vakantiedagen en de afwezigheid aangegeven die de bruto beschikbare capaciteit van de afdeling bepalen (gewoonlijk uitgedrukt in minuten). Dit alles wordt bepaald door de waarden die zijn gedefinieerd voor de efficiency en capaciteit.  

Wanneer u de productie hebt ingesteld, kunt u productieorders plannen en uitvoeren. Zie [Planning](production-planning.md) en [Productie](production-manage-manufacturing.md) voor meer informatie.  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|De productiefuncties configureren, zoals het definiëren van shopfloorwerkuren en het selecteren van planningsprincipes.|De pagina **Productie-instellingen**.|  
|Een standaardwerkweek in de productieafdeling definiëren met de begin- en eindtijd van elke werkdag en de bijbehorende dienst.|[Productieagenda's maken](production-how-to-create-work-center-calendars.md)|  
|Vaste waarden en vereisten van productieresources indelen als afdelingen of bewerkingsplaatsen om de productie-output te bepalen.|[Afdelingen en bewerkingsplaatsen instellen](production-how-to-set-up-work-and-machine-centers.md)|
|Productiebewerkingen in de vereiste volgorde indelen en met de vereiste werktijden toewijzen aan afdelingen of bewerkingsplaatsen.|[Bewerkingsplannen maken](production-how-to-create-routings.md)|
|Productiematerialen of halffabricaten indelen onder een geproduceerd hoofdartikel en de stuklijst voor uitvoering certificeren in afdelingen.|[Productiestuklijsten maken](production-how-to-create-production-boms.md)|
|Controleren of het juiste onderdeelaantal beschikbaar is als geproduceerde artikelen in één eenheid in voorraad zijn, maar in een andere eenheid worden geproduceerd.|[Werken met productiebatcheenheden](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Productfamilies met productieartikelen definiëren met soortgelijke productieprocessen om op verbruik te besparen. Uit één vel kunnen bijvoorbeeld tegelijkertijd vier stuks van het ene artikel en tien stuks van een ander artikel worden geproduceerd.|[Werken met productfamilies](production-how-work-family.md)|
|Standaardtaken gebruiken om het maken van bewerkingsplannen te vereenvoudigen door extra informatie bij te voegen voor terugkerende bewerkingen.|[Standaardbewerkingsplanregels instellen](production-how-set-up-standard-routing-lines.md)|  
|Afdelingen en bewerkingsplannen voor uitbestede productiebewerkingen voorbereiden.|[Productie uitbesteden](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Zie ook
[Productie](production-manage-manufacturing.md)    
[Gepland](production-planning.md)   
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
