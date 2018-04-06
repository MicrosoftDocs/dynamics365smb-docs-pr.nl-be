---
title: Picks plannen in het voorstel | Microsoft Docs
description: Als voor het magazijn zowel pick- als verzendingsverwerking is vereist, hebt u de keuze om van de regels op verzenddocumenten niet automatisch pickinstructies te maken, maar de regels beschikbaar te stellen in het pickvoorstel.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 073cc86b9df5845fbce18804756f980649f94081
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="plan-picks-in-worksheets"></a>Picks plannen in het voorstel
Als voor het magazijn zowel pick- als verzendingsverwerking is vereist, hebt u de keuze om van de regels op verzenddocumenten niet automatisch pickinstructies te maken, maar de regels beschikbaar te stellen in het pickvoorstel.  

> [!NOTE]  
>  Als de pickinstructies voor het magazijn al zijn gemaakt maar u ze wilt combineren tot één efficiënte pickinstructie, moet u de afzonderlijke magazijnpicks verwijderen. De te picken regels kunnen nu in het voorstel worden geplaatst.  

In het pickvoorstel kunt u picklijsten instellen voor werknemers. Deze picklijsten beperken de tijd die de werknemer nodig heeft om zich te verplaatsen voor het picken van artikelen in het magazijn. Er zijn velden die informatie over de beschikbare aantal artikelen in de cross-dockopslaglocaties bevatten. Dit is handig bij cross-dockgevallen om de werkopdrachten te plannen, omdat het programma altijd een pick voorstelt van een cross-dockopslaglocatie vóór een andere opslaglocatie, onafhankelijk van de eenheid. De regels in het voorstel kunnen afkomstig zijn uit een aantal brondocumenten en worden gesorteerd op artikel, schapnummer, brondocument, vervaldatum of verzendadres.  

Bij een sortering op vervaldatum hebt u de keuze om de regels die geen directe aandacht behoeven uit het voorstel te verwijderen. De minder urgente regels worden niet feitelijk verwijderd, maar alleen teruggestuurd naar de **pickselectie**. Als u de pick maakt, zijn de regels al gesorteerd op vervaldatum en kunt u de pick vervolgens toewijzen aan een bepaalde werknemer.  

> [!NOTE]  
>  Het picken voor magazijnverzending van artikelen die worden samengesteld voor de verkooporder die wordt verzonden volgt dezelfde stappen als gewone magazijnpicks voor verzending, zoals beschreven in dit onderwerp. Het aantal pickregels per te verzenden aantal is mogelijk echter veel-op-één omdat u de componenten pickt, niet het assemblageartikel.  
>   
>  De magazijnpickregels zijn gemaakt voor de waarde in het veld **Resterend aantal** op de regels van de assemblage die is gekoppeld aan de verkooporderregel die wordt verzonden. Dit zorgt ervoor dat alle onderdelen in één actie worden gepickt.  
>   
>  Zie de sectie Op-order-assembleren-artikelen in magazijnverzendingen afhandelen in Magazijnverzending voor meer informatie.  
>   
>  Zie [Picken voor assemblage of productie in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md) voor informatie over het picken van onderdelen voor assemblageorders in het algemeen, met inbegrip van situaties waar de assemblage niet voor een verkoopverzending is.  

## <a name="to-plan-picks-in-the-worksheet"></a>U kunt als volgt picks plannen in het voorstel  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Pickvoorstel** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Magazijndocumenten ophalen**.  
3.  Selecteer de verzendingen waarvoor u een pick wilt voorbereiden. Hoewel u de regels nog in beperkte mate kunt sorteren, zal de sortering niet meer worden overgenomen op de pickinstructie. U kunt ook bepaalde regels verwijderen om een nog efficiëntere pick te maken. Als er bijvoorbeeld regels zijn met artikelen die in cross-docklocaties zijn geplaatst, kunt u een pick maken voor alle regels die verbonden zijn aan deze regels. De cross-dockartikelen worden dan verzonden, samen met de andere artikelen in de verzending, en in de cross-docklocaties komt ruimte vrij voor andere binnenkomende artikelen.  
4.  Kies de actie **Pick maken** en vul het aanvraagvenster **Pick maken** in. De nieuwe pickregels worden gesorteerd volgens de methode die u hier kiest. Stel dat u voor elke zone één pick maakt, dan kunt u de regels binnen elke pick sorteren op rangorde van opslaglocatie.  
5.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Magazijnpicks** in en klik vervolgens op de gerelateerde koppeling. Het venster **Picks** wordt geopend.  
6.  U kunt de pickopdracht die u hebt gemaakt nu opzoeken door op Pick, Overzicht te klikken en de pick met het hoogste nummer te selecteren.  
7.  U kunt indien nodig de toegewezen gebruikers-id en sortering van de regels van de pick nog wijzigen.  
8.  Kies de actie **Afdrukken** om de pickinstructies af te drukken.  
9. Als u de pick hebt uitgevoerd, kiest u de actie **Registreren**.  

Als de nummering van opslaglocaties een weerspiegeling vormt van de fysieke indeling van het magazijn en u hebt de regels gesorteerd op opslaglocatie, kan de picker in één rondgang door het magazijn artikelen voor verschillende verzendingen tegelijk picken. De medewerker haalt uit elke opslaglocatie per verzendregel het vereiste aantal artikelen en plaatst deze bij de overige artikelen voor een bepaalde verzending. De picker kan zo veel tijd besparen omdat hij of zij slechts één keer naar de opslaglocatie hoeft te gaan om voor verschillende verzendingen te picken.  

De rangorde van opslaglocaties is een andere effectieve sorteeroptie, zeker als het magazijn fysiek gezien meer op rangorde van opslaglocatie is ingedeeld dan op opslaglocatie.  

U kunt in het pickvoorstel ook op verzendadres sorteren, zodat u de orders voor verre klanten het eerst kunt samenstellen en verzenden.  

## <a name="see-also"></a>Zie ook
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

