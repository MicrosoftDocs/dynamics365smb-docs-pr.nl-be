---
title: Artikelen opslaan | Microsoft Docs
description: De magazijnactiviteit van de opslag van artikelen na ontvangst of uitvoer wordt op verschillende manieren uitgevoerd, afhankelijk van hoe de functies voor magazijnbeheer zijn geconfigureerd.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d19486956fbaa0addb58a71c13849b0bb32c958a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771586"
---
# <a name="putting-items-away"></a>Artikelen opslaan
De magazijnactiviteit van de opslag van artikelen na ontvangst of uitvoer wordt op verschillende manieren uitgevoerd, afhankelijk van hoe de functies voor magazijnbeheer zijn geconfigureerd. De complexiteit varieert, van geen magazijnfuncties via standaardmagazijnconfiguraties voor de afzonderlijke verwerking van orders in een of meer activiteiten tot geavanceerde configuraties waarbij alle activiteiten in een gestuurde werkstroom moeten worden uitgevoerd. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

Als u de opslaggegevens wilt ordenen en vastleggen met behulp van magazijndocumenten, schakelt u het selectievakje **Opslag vereist** in bij de vestiging. Hiermee geeft u aan dat u, wanneer er artikelen moeten worden opgeslagen voor een inkomend brondocument, de opslag van deze artikelen via het systeem wilt beheren. Een inkomend brondocument kan een inkooporder zijn, maar ook een verkoopretourorder, een inkomende transferorder of een productieorder waarvan de output kan worden opgeslagen.  

Als voor uw vestiging opslagverwerking is ingesteld, maar niet ontvangstverwerking, gebruikt u de pagina **Voorraadopslag** om de opslaginformatie in te delen, om deze af te drukken, om het resultaat van de feitelijke opslag in te voeren en om de opslaginformatie te boeken, waardoor vervolgens de ontvangstinformatie voor het brondocument wordt geboekt. In geval van een productieorder, boekt het boekingsproces de uitvoer van de order en voltooit het proces de productieorder.

Als het magazijn zowel ontvangst- als opslagverwerking vereist en de selectievakjes **Ontvangst vereist** en **Opslag vereist** zijn ingeschakeld bij de vestiging, geldt er een ander proces voor de opslag van artikelen. In dit geval gebruikt u de pagina **Magazijnopslag** om de opslag te verwerken. U voert een magazijnopslag op dezelfde manier uit als een voorraadopslag, maar in plaats van de gegevens te boeken, registreert u de opslag. Houd er rekening mee dat het registreren van de magazijnopslag er niet toe leidt dat de ontvangst van de artikelen wordt geboekt. Alleen de opslaglocatie-inhoud wordt bijgewerkt. Als magazijnmanager kunt u met behulp van opslagvoorstellen opslaggegevens ordenen voordat de afzonderlijke magazijnopslaginstructies worden gemaakt.

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|De ontvangst van artikelen direct boeken vanuit het inkomende orderdocument en daarmee de opslag registreren omdat er geen magazijnconfiguratie bestaat.|[Artikelen ontvangen](warehouse-how-receive-items.md)|  
|Artikelen per order opslaan en de ontvangst in dezelfde activiteit boeken, in een standaardmagazijnconfiguratie.|[Artikelen opslaan met voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Artikelen opslaan voor meerdere orders in een geavanceerde magazijnconfiguratie.|[Artikelen opslaan met magazijnopslag](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Geproduceerde of geassembleerde artikelen opslaan in een standaard- of geavanceerde magazijnconfiguratie.|[Productie- of assemblageoutput opslaan](warehouse-how-to-put-away-production-output.md)|
|Geoptimaliseerde opslaginstructies plannen voor een aantal geboekte magazijnontvangsten in plaats van dat magazijnmedewerkers direct naar ontvangsten moeten handelen.|[Plannen van opslagactiviteiten in werkbladen](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Artikelen terugplaatsen die technisch zijn gepickt met een interne pick, bijvoorbeeld voor een productieorder die niet de verwachte hoeveelheid heeft verbruikt.|[Picken en opslaan zonder een brondocument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Een opslagregel splitsen om een deel van de opslaghoeveelheid in beschikbare opslaglocaties te plaatsen omdat de aangewezen locatie vol is.|[Magazijnactiviteitsregels splitsen](warehouse-how-to-split-warehouse-activity-lines.md)|
|Direct toegang verkrijgen tot voorraadopslag die aan u als magazijnmedewerker is toegewezen.|[Magazijntoewijzingen zoeken](warehouse-how-to-find-your-warehouse-assignments.md)|    

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]