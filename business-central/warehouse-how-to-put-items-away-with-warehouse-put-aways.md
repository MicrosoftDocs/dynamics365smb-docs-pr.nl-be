---
title: Artikelen opslaan met magazijnopslag | Microsoft Docs
description: Wanneer voor de vestiging magazijnopslag- en -ontvangstverwerking is vereist, beheert u de opslag van artikelen met de functie voor magazijnopslagdocumenten.
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
ms.openlocfilehash: 17743791d7694754f8b8eb97f6792a94b68176d2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310264"
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Artikelen opslaan met magazijnopslag
Wanneer voor de vestiging magazijnopslag- en -ontvangstverwerking is vereist, beheert u de opslag van artikelen met de functie voor magazijnopslagdocumenten.  

Als u een magazijnontvangst boekt, worden de brondocumenten zoals inkooporder, inkomende transferorder of verkoopretourorder bijgewerkt, de ontvangen aantallen geboekt in de artikelposten en de regels over de ontvangen artikelen naar de opslagfunctie van het magazijn verzonden. Als u met interne opslag en pick werkt, kunnen ook opslagregels worden gegenereerd door de interne opslag.  

Afhankelijk van de magazijninstellingen worden de regels beschikbaar gemaakt in het opslagvoorstel of worden direct opslaginstructies gemaakt. Zie [Opslag plannen in voorstellen](warehouse-how-to-plan-put-aways-in-worksheets.md) voor meer informatie.  

Naast de standaard manieren waarop magazijnopslag gemaakt kan worden die in dit onderwerp worden beschreven, kunt u opslag maken vanuit de bijbehorende geboekte magazijnontvangst. Dit is nuttig als u opslagregels hebt verwijderd of als u gestuurde opslag en pick gebruikt en het opslagwerkblad niet wilt gebruiken omdat u opslaginstructies (opnieuw) kunt maken van de geboekte ontvangstregels.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Artikelen opslaan zonder gestuurde opslag en pick  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslag** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de magazijnopslag die gereed is om te verwerken.  

    U kunt de opslagregels op grond van diverse criteria sorteren, bijvoorbeeld op artikel, schapnummer of vervaldatum en op deze manier het opslagproces optimaliseren.  
3.  Voer op elke regel het aantal dat u wilt opslaan in het veld **Te verwerken aantal** in.  
4.  Als u de opslag van artikelen hebt voltooid, kiest u de actie **Opslag registreren** om de voltooiing van de activiteit te registreren en de artikelen beschikbaar te maken voor pickacties.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Artikelen opslaan met gestuurde opslag en pick  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslag** in en kies vervolgens de gerelateerde koppeling.
    Als er opslaginstructies zijn gemaakt, wordt er een magazijnopslag weergegeven.  
2.  Open de magazijnopslag waaraan u wilt werken.  
3.  Als voor het magazijn een gebruikers-id is vereist, voert u deze eerst in op het sneltabblad **Algemeen**. Daarna kunt u de gewenste opslag bewerken.  
4.  Voer de Nemen- en Plaatsen-acties uit in het veld **Actiesoort** op de regels.  

    Elke ontvangstregel is in de magazijnopslag omgezet in ten minste twee regels:  

    -   De eerste regel met **Nemen** in het veld **actiesoort** geeft aan waar de artikelen zich in het ontvangstgebied bevinden. U kunt de zone en de opslaglocatie op deze regel niet wijzigen.  
    -   De volgende regel met **Plaatsen als** in het veld **actiesoort** geeft aan waar u de artikelen in de magazijnopslag moet plaatsen. Als er een groot aantal artikelen via één ontvangstregel het magazijn is binnengekomen, moeten de artikelen mogelijk op verschillende opslaglocaties worden opgeslagen en wordt er een Plaatsen-regel voor elke opslaglocatie weergegeven.  

        Als de Nemen- en Plaatsen-regels op de ontvangstregels niet opeenvolgend worden weergegeven, kunt u de regels sorteren door **Artikel** te selecteren in het veld **Sorteringsmethode** op het sneltabblad **Algemeen**.  

        Als de fysieke indeling van het magazijn en de rangorde van opslaglocaties met elkaar overeenkomen, kunt u de sorteermethode **Opslaglocatievolgorde** gebruiken om een opslag voor te bereiden waarin uw rondgang door het magazijn zo efficiënt mogelijk verloopt.  

5.  Als u alle artikelen volgens de instructies op de opslaglocaties hebt geplaatst, kiest u de actie **Opslag registreren**.  

Op locaties die zijn ingesteld voor gestuurde opslag en pick, zijn de volgende instellingen vereisten voor bovenstaande procedure:  

- Er wordt een opslagsjablonen ingesteld. Zie voor meer informatie [Opslagsjablonen instellen](warehouse-how-to-set-up-put-away-templates.md).  
- Het gewicht, het volume en de speciale opslagvereisten van het artikel of de SKU worden opgegeven. Zie voor meer informatie Brutogewicht.  
- De capaciteit, de soort opslaglocatie en de volgorde van de opslaglocaties. Zie Opslaglocatievolgorde voor meer informatie .  

De opslaglocatievolgorde wordt gebruikt wanneer meerdere opslaglocaties voldoen aan de opslagsjablooncriteria. Als meerdere opslaglocaties voldoen aan de criteria van de opslagsjabloon en dezelfde rang in de opslaglocatievolgorde hebben, wordt de opslaglocatie met het hoogste opslaglocatienummer gebruikt.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Een magazijnopslag maken vanuit een geboekte ontvangst  
 Als bij uw vestiging zowel opslagverwerking als ontvangstverwerking wordt gebruikt en u opslagregels hebt verwijderd, of als u gestuurde opslag en pick gebruikt en het opslagwerkblad niet wilt gebruiken, kunt u opslaginstructies (opnieuw) maken voor de geboekte ontvangstregels.

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte magazijnontvangsten** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer een geboekte ontvangst die mogelijk moet worden opgeslagen.  
3.  Kies de actie **Kaart**.  

    Als het veld **Documentstatus** leeg is, is de ontvangst nog niet opgeslagen. Anders geeft het veld aan dat de ontvangst gedeeltelijk opslaan of volledig opslaan betreft.  

4.  Als de ontvangst gedeeltelijk is opgeslagen of nog niet is opgeslagen, kiest u de actie **Opslag maken**.  
5.  Vul de aanvraagpagina voor de batchverwerking in om de opslaginstructies te maken en klik op **OK**.   

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
