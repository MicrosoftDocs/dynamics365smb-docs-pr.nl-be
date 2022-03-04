---
title: Picks plannen in het voorstel
description: Leer hoe regels op verzenddocumenten beschikbaar kunnen worden gemaakt op pickvoorstellen voor magazijnmedewerkers.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: fbb85d69cdd7844bbc63e6367ea962897ab30478
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144319"
---
# <a name="plan-picks-in-worksheets"></a>Picks plannen in het voorstel

Als uw magazijn is ingesteld om zowel pick- als verzendingsverwerking te vereisen, kunt u ervoor kiezen regels op verzenddocumenten beschikbaar te maken op pickvoorstellen in plaats van pickinstructies.  

> [!NOTE]  
> Als de pickinstructies voor het magazijn al zijn gemaakt maar u ze wilt combineren tot één efficiënte pickinstructie, moet u de afzonderlijke magazijnpicks verwijderen. De te picken regels kunnen nu in een pickvoorstel worden geplaatst.  

Op de pagina **Pickvoorstellen** kunt u picklijsten instellen waarmee medewerkers artikelen in het magazijn kunnen verzamelen. De pagina toont de beschikbare hoeveelheden in cross-dockopslaglocaties, wat handig is voor het plannen van werktoewijzingen in cross-docksituaties. [!INCLUDE[prod_short](includes/prod_short.md)] stelt altijd eerst een pick uit een cross-dockopslaglocatie voor. De regels in het voorstel kunnen uit verschillende brondocumenten komen. Ze kunnen bijvoorbeeld afkomstig zijn van meer dan één verkooporder. 

> [!NOTE]  
> Het picken van artikelen die worden samengesteld voor een verkooporder die wordt verzonden, volgt dezelfde stappen als gewone magazijnpicks voor verzendingen. Het aantal pickregels per te verzenden aantal is mogelijk echter veel-op-één omdat u de componenten pickt, niet het assemblageartikel.  
>
> De magazijnpickregels zijn gemaakt voor de waarde in het veld **Resterend aantal** op de regels van de assemblage die is gekoppeld aan de verkooporderregel die wordt verzonden. Dit zorgt ervoor dat alle onderdelen in één actie worden gepickt. Zie voor meer informatie [Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Zie [Picken voor assemblage of productie in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md) voor informatie over het picken van onderdelen voor assemblageorders in het algemeen, met inbegrip van situaties waar de assemblage niet voor een verkoopverzending is.  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Regels sorteren in een pickvoorstel
U kunt regels sorteren op artikel, schapnummer, brondocument, vervaldatum of bestemming. Hier volgen enkele voorbeelden van hoe sorteren nuttig kan zijn.

* Bij een sortering op vervaldatum hebt u de keuze om alle regels, behalve regels die directe aandacht behoeven, te verwijderen. De minder urgente regels worden niet feitelijk verwijderd, maar alleen teruggestuurd naar de **pickselectie**. Als u de pick maakt, zijn de regels al gesorteerd op vervaldatum en kunt u de pick vervolgens toewijzen aan een werknemer.
* Als uw opslaglocaties zo zijn genummerd dat ze overeenkomen met de fysieke lay-out van uw magazijn, kan het sorteren van regels op opslaglocatienummer het gemakkelijker maken om voor meerdere zendingen tegelijk te picken. 
* Als u opslaglocatievolgorde gebruikt, kan het sorteren op volgorde enige tijd besparen. 
* U kunt sorteren op bestemming, waardoor u orders per klant kunt samenstellen en verzenden.

## <a name="to-plan-picks-in-the-worksheet"></a>U kunt als volgt picks plannen in het voorstel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pickvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Magazijndocumenten ophalen**.  
3. Selecteer de verzendingen waarvoor u een pick wilt voorbereiden. U kunt de regels sorteren, maar de sortering wordt niet toegepast op de pick-instructie. U kunt ook bepaalde regels verwijderen om een nog efficiëntere pick te maken. Als er bijvoorbeeld meerdere regels zijn met artikelen in cross-dockopslaglocaties, kunt u een pick maken voor alle regels. De cross-dockartikelen worden dan verzonden, samen met de andere artikelen in de verzending, en in de cross-docklocaties komt ruimte vrij voor andere binnenkomende artikelen.  
4. Kies de actie **Pick maken** en vul de pagina **Pick maken** in. De nieuwe pickregels worden gesorteerd volgens de methode die u hier kiest. Stel dat u voor elke zone één pick maakt, dan kunt u de regels binnen elke pick sorteren op rangorde van opslaglocatie.  
5. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnpicks** in en kies vervolgens de gerelateerde koppeling. Het venster **Magazijnpicks** wordt geopend.  
6. U kunt de pickopdracht nu zoeken door de pick met het hoogste nummer te selecteren.  
7. Indien nodig kunt u een andere gebruiker toewijzen of de regels anders sorteren.  
8. Kies de actie **Afdrukken** om de pickinstructies af te drukken.  
9. Nadat de pick is voltooid, kiest u de actie **Registreren**.  

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]