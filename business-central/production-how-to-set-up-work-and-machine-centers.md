---
title: Afdelingen en bewerkingsplaatsen instellen | Microsoft Docs
description: Op een **afdelingskaart** staan alle vaste waarden en behoeften van de desbetreffende productieresource bij elkaar. Op die manier wordt de productie-output die op die afdeling wordt uitgevoerd door de kaart bepaald.
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
ms.openlocfilehash: eb947aec01b7932b827332d0c283ec9b08981634
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313120"
---
# <a name="set-up-work-centers-and-machine-centers"></a>Afdelingen en bewerkingsplaatsen instellen
Er wordt onderscheid gemaakt tussen drie soorten capaciteit. Deze zijn hiërarchisch gerangschikt. Elk niveau bestaat uit onderliggende niveaus.  

Het bovenste niveau is de afdelingsgroep. Aan de afdelingsgroepen worden afdelingen toegewezen. Iedere afdeling kan slechts aan één afdelingsgroep worden gekoppeld.

U kunt aan iedere afdeling meerdere bewerkingsplaatsen toewijzen. Een bewerkingsplaats kan slechts aan één afdeling worden gekoppeld.  

De geplande capaciteit van een afdeling bestaat uit de beschikbaarheid van de bijbehorende bewerkingsplaatsen en de extra geplande beschikbaarheid van de afdeling. De geplande beschikbaarheid van de afdelingsgroep is dus het totaal van de beschikbaarheid van corresponderende bewerkingsplaatsen en afdelingen.  

De beschikbaarheid wordt opgeslagen in agendaposten. Voordat u afdelingen of bewerkingsplaatsen instelt, kunt u productieagenda's instellen. Zie voor meer informatie [Productieagenda's maken](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Een afdeling instellen
Hier wordt voornamelijk beschreven hoe u een afdeling instelt. De stappen voor het instellen van een bewerkingsplaatsagenda komen overeen, met uitzondering van het sneltabblad **Bewerkingsplaninstelling**.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afdelingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Selecteer in het veld **Afdelingsgroep** de hoger gelegen resourcegroep waaronder de afdeling is georganiseerd, indien van toepassing. Kis de actie **Nieuw** in de vervolgkeuzelijst.  
5.  Selecteer het veld **Geblokkeerd** als u wilt voorkomen dat de afdeling wordt gebruikt in de verwerking. Dit betekent dat er geen output kan worden geboekt voor een artikel dat in de afdeling wordt geproduceerd. Zie voor meer informatie [Productie-output boeken](production-how-to-post-output-quantity.md).
6.  Voer in het veld **Directe kostprijs** de productiekosten voor deze afdeling in voor één eenheid, zonder daarin andere kostenelementen te betrekken. Deze kosten worden vaak het *tarief directe lonen* genoemd.  
7.  In het veld **Indirecte kosten %** voert u de algemene bewerkingskosten van het gebruik van de afdeling als percentage van de directe kostprijs. Voor de berekening van de kostprijs wordt dit percentage bij de directe kosten opgeteld.  
8.  In het veld **Overheadtarief** voert u alle niet-bewerkingskosten van de afdeling, zoals onderhoudskosten, als absoluut bedrag in.  

    Het veld **Kostprijs** bevat de berekende kostprijs voor de productie van één eenheid op deze afdeling, met daarin alle andere kostenelementen, als volgt:  

    Kostprijs = Directe kostprijs + (Directe kostprijs x Indirecte kosten %) + Overheadtarief.  

9.  Definieer in het veld **Kostprijsberekening** of de bovenstaande berekening moet worden gebaseerd op de gebruikte tijd: **Tijd** of op het aantal geproduceerde eenheden: **Eenheden**.  
10.  Schakel het selectievakje **Specifieke kostprijs** in wanneer u de afdelingskostprijs wilt definiëren op de bewerkingsplanregel waarop deze wordt gebruikt. Dit kan nodig zijn voor bewerkingen waarvan de capaciteitskosten enorm verschillen met die van bewerkingen die normaal op de afdeling worden uitgevoerd.  
11.  Selecteer in het veld **Afboekingsmethode** of de outputboeking op deze afdeling handmatig moet worden berekend en geboekt of dat dit automatisch moet gebeuren op een van de volgende wijzen.

|Optie|Omschrijving|
|------|-----------|
|**Handmatig**|Verbruik wordt handmatig geboekt in het outputdagboek of het productiedagboek.|
|**Voorwaarts**|Verbruik wordt automatisch berekend en geboekt wanneer de productieorder wordt vrijgegeven.|
|**Achterwaarts**|Verbruik wordt automatisch berekend en geboekt wanneer de productieorder wordt voltooid.|

> [!NOTE]
> Zo nodig kan de afboekingsmethode die hier en op de **artikelkaart** is geselecteerd, voor afzonderlijke bewerkingen worden overschreven. U doet dit door de instellingen op bewerkingsplanregels te wijzigen

12.  Voer in het veld **Eenheidscode** de tijdseenheid in waarin de kostenberekening en capaciteitsplanning van deze afdeling worden gemaakt.
    Pas wanneer u een methode voor meten hebt ingesteld, kunt u het verbruik voortdurend controleren. De eenheden die u invoert, zijn basiseenheden. De verwerkingstijd wordt bijvoorbeeld gemeten in uren en minuten.

> [!NOTE]  
> Als u kiest voor het gebruik van dagen, moet u eraan denken dat 1 dag bestaat uit 24 uur en niet uit 8 (werkuren).

13.  Definieer in het veld **Capaciteit** of er op de afdeling meer dan één machine of persoon tegelijkertijd aan het werk zijn. Wanneer in [!INCLUDE[d365fin](includes/d365fin_md.md)] niet de module Bewerkingsplaats is geïnstalleerd, moet de waarde in dit veld **1** zijn.  
14.  Voer in het veld **Efficiëntie** het percentage van de verwachte standaardoutput in dat deze afdeling werkelijk oplevert. Wanneer u hier **100** invoert, betekent dit dat de werkelijke output van de afdeling net zo hoog is als de standaardoutput.  
15. Schakel het selectievakje **Geconsolideerde agenda** in als u ook bewerkingsplaatsen gebruikt. Hierdoor worden agendaposten berekend op basis van bewerkingsplaatsagenda's.  
16.  Selecteer een productieagenda in het veld **Productieagendacode**. Zie voor meer informatie [Productieagenda's maken](production-how-to-create-work-center-calendars.md).  
17.  In het veld **Wachttijd voor bew.** geeft u op hoeveel tijd er moet verstrijken voordat toegewezen werk op deze afdeling kan beginnen. De wachttijd wordt toegevoegd aan de overige niet-productieve tijdselementen, zoals wachttijd na bewerking en transporttijd, die u kunt definiëren op de bewerkingsplanregels die gebruikmaken van deze afdeling.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Voorbeeld - Verschillende bewerkingsplaatsen die aan een afdeling zijn toegewezen
Tijdens het instellen van bewerkingsplaatsen en afdelingen is het belangrijk dat u plant waaruit de totale capaciteit zal bestaan.

Als er meerdere bewerkingsplaatsen (bijvoorbeeld 210 Verpakkingsruimte 1, 310 Verfcabine ...) aan een afdeling zijn toegewezen, is het belangrijk dat u rekening houdt met de afzonderlijke capaciteit van de bewerkingsplaatsen, omdat storingen op één bewerkingsplaats het hele proces kunnen onderbreken. De bewerkingsplaatsen kunnen worden ingevoerd op basis van capaciteit, maar worden mogelijk niet opgenomen in de planning. Als u het veld **Geconsolideerde agenda** uitschakelt, wordt alleen de afdelingscapaciteit toegewezen in de planning, niet de capaciteit van de afzonderlijke bewerkingsplaatsen.

Wanneer echter identieke bewerkingsplaatsen (bijvoorbeeld 210 Verpakkingsruimte 1 en 220 Verpakkingsruimte 2) worden gecombineerd op een afdeling, kan de afdeling worden beschouwd als het totaal van de toegewezen bewerkingsplaatsen. De afdeling zou dan worden weergegeven met een capaciteit van nul. Als u het veld **Geconsolideerde agenda** inschakelt, wordt de totale capaciteit toegewezen aan de afdeling.

Als de capaciteit van afdelingen niet moet bijdragen aan de totale capaciteit, kunt u dit instellen met efficiëntie = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Een bewerkingsplaats of afdeling met beperkte capaciteit instellen
U kunt een beperkte werklast toewijzen aan productieresources die als kritiek worden beschouwd door deze te markeren, in plaats van de onbeperkte werklast die door andere resources worden geaccepteerd. Een resource met beperkte capaciteit kan een afdeling of bewerkingsplaats zijn die als knelpunt wordt beschouwd en waarvoor u een beperkte (begrensde) werklast wilt instellen.

[!INCLUDE[d365fin](includes/d365fin_md.md)] biedt geen ondersteuning voor gedetailleerd werkvloerbeheer. Het systeem plant een uitvoerbaar gebruik van resources door een ruw schema te leveren, maar het maakt en onderhoudt niet automatisch gedetailleerde schema's op basis van prioriteiten of optimalisatieregels.

Op de pagina **Capaciteitsbegrensde resource** kunt u instellingen configureren waarmee overbelasting van specifieke resources kan worden voorkomen, en kunt u ervoor zorgen dat alle capaciteit wordt toegewezen als dit de omlooptijd van een productieorder kan verhogen. In het veld **Demping (% van totale capaciteit)** kunt u dempingstijd aan resources toevoegen om bewerkingsplitsen te verkleinen. Hiermee kan het systeem de werklast op de laatst mogelijke dag plannen door het kritieke werklastpercentage iets te overschrijden als dit het aantal bewerkingen kan verminderen die worden gesplitst.

Bij het plannen met capaciteitsbegrensde resources zorgt het systeem dat er geen resources boven de gedefinieerde capaciteit (kritieke werklastpercentage) worden geladen. Dit gebeurt door elke bewerking toe te wijzen aan de dichtstbijzijnde beschikbare periode. Als de periode niet groot genoeg is om de hele bewerking uit te voeren, wordt de bewerking in twee of meer delen gesplitst in de dichtstbijgelegen perioden.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Capaciteitsbegrensde resources** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul de velden in.

> [!NOTE]
> Bewerkingen op afdelingen of bewerkingsplaatsen die zijn ingesteld als beperkte resources, worden altijd in serie gepland. Dit betekent dat als een beperkte bron meerdere capaciteiten heeft, die capaciteiten alleen in volgorde kunnen worden gepland. Dit kan niet parallel, zoals het geval zou zijn als de afdelings- of bewerkingsplaats niet is ingesteld als beperkte resource. In een begrensde resource, is het veld Capaciteit op de afdeling of bewerkingsplaats groter is dan 1.

> In het geval van gesplitste bewerkingen wordt de insteltijd slechts eenmaal toegewezen omdat ervan wordt uitgegaan dat enige handmatige aanpassing wordt uitgevoerd om de planning te optimaliseren.

## <a name="see-also"></a>Zie ook  
[Productieagenda's maken](production-how-to-create-work-center-calendars.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Gepland](production-planning.md)   
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
