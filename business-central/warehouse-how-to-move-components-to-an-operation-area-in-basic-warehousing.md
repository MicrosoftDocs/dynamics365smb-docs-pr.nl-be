---
title: Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties | Microsoft Docs
description: Indien artikelbewerkingen plaatsvinden in uw magazijnvestiging, moet u mogelijk artikelen tussen interne opslaglocaties verplaatsen om te reageren op interne brondocumenten, zoals productie-, assemblage- of serviceorders in de vestiging.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f628ceefb6894f8ca2f05e6345ac4f3b19f3235e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923281"
---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties
Indien artikelbewerkingen plaatsvinden in uw magazijnvestiging, moet u mogelijk artikelen tussen interne opslaglocaties verplaatsen om te reageren op interne brondocumenten, zoals productie-, assemblage- of serviceorders in de vestiging.  

> [!NOTE]  
>  Zie voor informatie over het verplaatsen van artikelen tussen opslaglocaties zonder brondocumenten Interne verplaatsing.  

Bij geavanceerde magazijnconfiguraties, locaties die gebruikmaken van de instelling **Gestuurde opslag en pick** , kunt u de pagina **Verplaatsingsvoorstel** gebruiken om artikelen tussen opslaglocaties te verplaatsen. Zie voor meer informatie [Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Bij standaard magazijnconfiguraties, dat zijn locaties die gebruik maken van de instelling **Opslaglocatie verplicht** en **Pick vereist** , kunt u verplaatsing van items naar interne activiteitengebieden registreren op basis van interne brondocumenten op de volgende manieren:  

-   Met de pagina **Voorraadverplaatsing** .  
-   Met de pagina **Voorraadpick** .  

> [!NOTE]  
>  Voorraadpicks boeken ook negatieve artikelposten als verbruik en worden alleen ondersteund voor productieonderdelen. Zie voor meer informatie de pagina Voorraadpick.  

Zie voor gedetailleerde informatie over voorraadverplaatsingen de pagina Voorraadverplaatsing.  

Twee verschillende rollen kunnen de initiële voorraadverplaatsing maken. Een assemblagemedewerker kan het bijvoorbeeld vanuit een vrijgegeven assemblageorder maken, zodat het op de werklijst van de magazijnmedewerker weergegeven wordt. Als een assemblagemedewerker een voorraadverplaatsing wil maken voor assemblageorderregels die gereed zijn om onderdelen naar de opgegeven opslaglocaties te verplaatsen, gebruikt deze de functie **Voorraadverplaatsing maken** .  

Ook kan een magazijnmedewerker deze maken door verwijzing naar de betreffende vrijgegeven assemblageorder. Dit wordt in de volgende procedure beschreven.  

> [!NOTE]  
>  Indien de verplaatsing voor een assemblageorder is waar het item voor een verkooporder wordt samengesteld, kunt u definiëren dat het voorraadverplaatsingdocument automatisch gemaakt wordt wanneer u het voorraad-pickdocument maakt dat het voltooide assemblageartikel neemt en de verzending boekt. Als u dit wilt instellen, selecteert u het veld **Verplaatsingen automatisch aanmaken** op de pagina **Assemblage-instelling**  
>   
>  Zie voor meer informatie over assemblageorders en standaardmagazijnconfiguraties [Op-order-assembleren-artikelen met voorraadpicks afhandelen](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Deze procedure laat zien hoe u een voorraadverplaatsing uit de pagina **Voorraadverplaatsing** kunt maken door te verwijzen naar een vrijgegeven assemblageorder als brondocument. De procedure is hetzelfde als u onderdelen verplaatst voor productie- en serviceorders.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadverplaatsing** in en kies de relevante koppeling.  
2.  Vul het veld **Nr.** op het sneltabblad **Algemeen** in . te kiezen. U kunt op de Enter-toets drukken om te selecteren uit de nummerreeks.  
3.  Voer in het veld **Locatiecode** de locatie in waar de verplaatsing plaatsvindt.  
4.  Kies de actie **Brondocumenten ophalen** . U kunt ook het veld **Brondocument** invullen en vervolgens de knop **AssistEdit** in het veld **Bronnr.** kiezen.  
5.  Selecteer op de pagina **Brondocumenten** de assemblageorder waarvoor u onderdelen wilt verplaatsen en kies vervolgens de knop **OK** .  

    Voor elk benodigd onderdeel dat verplaatst kan worden, wordt één regel met nemen en één regel met plaatsen gegenereerd op de pagina **Voorraadverplaatsingen** . Alle velden behalve het veld **Te verwerken aantal** worden gevuld volgens de regels van het brondocument. Het veld **Te verwerken aantal** is ingesteld op nul totdat u het aantal opgeeft dat u daadwerkelijk hebt verplaatst.  

    U kunt de opslaglocatiecode op de nemen-regel wijzigen, maar alleen op beschikbaarheid. Indien u de knop **AssistEdit** in het veld **Opslaglocatiecode** op een nemen-regel kiest, wordt de pagina **Opslaglocatie-inhoud** geopend en worden alleen opslaglocaties getoond waar het onderdeel beschikbaar is.  

    U kunt de opslaglocatiecode niet wijzigen op de plaatsen-regel. Alleen de opslaglocatiecode die op de onderdeelregel van het brondocument is gedefinieerd wordt geaccepteerd. Dit ondersteunt het beginsel dat de rol die een onderdeel verzoekt, wat in deze procedure een assemblagemedewerker is, weet waar het onderdeel moet worden geplaatst. Indien u onderdelen in een andere opslaglocatie wilt plaatsen, moet u eerst de opslaglocatiecode op de onderdeelregel wijzigen en vervolgens de voorraadverplaatsingsregels opnieuw maken.  
6.  Voer in het veld **Te verwerken aantal** het gehele of gedeeltelijke aantal in dat u daadwerkelijk hebt verplaatst. De waarde op de nemen- en plaatsen-regels moet hetzelfde zijn. Anders kunt u de verplaatsing niet registreren.  

    > [!NOTE]  
    >  Net als bij andere magazijnactiviteiten kunt u de Plaatsen-regel splitsen door de actie **Acties** te selecteren en vervolgens de actie **Regel splitsen** te kiezen. In dat geval moet de som van de twee gesplitste plaatsen-regels gelijk zijn aan het aantal op de nemen-regel.  

7.  Wanneer u klaar bent om de verplaatsingen te registreren die u hebt uitgevoerd, kiest u de actie **Voorraadverplaatsing registreren** .  

    Magazijnposten worden gemaakt die weergeven dat de onderdelen nu in de opslaglocaties zijn die op de assemblageorderregels zijn opgegeven.  

    > [!NOTE]  
    >  In tegenstelling tot wanneer u onderdelen met een voorraadpick verplaatst, wordt het verbruik niet geboekt wanneer u een voorraadverplaatsing registreert. Die stap moet afzonderlijk worden uitgevoerd door de uitvoer en het verbruik van de assemblageorder te boeken. Zie voor meer informatie Assemblageorder.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
