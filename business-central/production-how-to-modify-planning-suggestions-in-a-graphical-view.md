---
title: Planningsuggesties in een grafische weergave wijzigen | Microsoft Docs
description: Een typische planningsactiviteit is het wijzigen of toevoegen van planningsvoorstelregels om de voorgestelde voorzieningsorders te wijzigen voordat u ze vastlegt door de functie **Planningsboodschap uitvoeren** uit te voeren. In plaats van dit in het planningsvoorstel te doen, kunt u ook een grafische weergave gebruiken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3188b2d711fe983526e5ee87a7a3901b16d6eb35
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="modify-planning-suggestions-in-a-graphical-view"></a>Planningsuggesties in een grafische weergave wijzigen
Een typische planningsactiviteit is het wijzigen of toevoegen van planningsvoorstelregels om de voorgestelde voorzieningsorders te wijzigen voordat u ze vastlegt door de functie **Planningsboodschap uitvoeren** uit te voeren. In plaats van dit in het planningsvoorstel te doen, kunt u ook een grafische weergave gebruiken.

In het venster **Artikelbeschikbaarheid per tijdlijn** kunt u bepaalde aanvulorders en suggesties wijzigen door elementen langs de x-as te slepen om het aantal te wijzigen of langs de y-as te slepen om de vervaldatum te wijzigen.  

 In het venster **Artikelbeschikbaarheid per tijdlijn** en het venster **Planningsvoorstel** kunt u de volgende wijzigingen aanbrengen:  

-   Een voorgestelde voorzieningsorder die alleen als een planningsregel bestaat wijzigen.  
-   Een bestaande voorzieningsorder die het planningssysteem voorstelt wijzigen.  
-   Een nieuwe voorgestelde voorzieningsorder maken en wijzigen.  

Zie voor meer informatie over de typen planningsregels die worden weergegeven het veld Omschrijving op het sneltabblad **Gebeurteniswijzigingen**.  

Wanneer u **Wijzigingen opslaan** kiest in het venster **Artikelbeschikbaarheid per tijdlijn**, worden de wijzigingen die u hebt aangebracht gekopieerd naar de planning of het inkoopvoorstel. U kunt ze nu implementeren met de functie **Planningsboodschap uitvoeren - Plan**.  

De volgende procedure laat zien hoe u voorzieningsvoorstellen kunt wijzigen door slepen en neerzetten. Als alternatief kunt u de velden **Vervaldatum** en **Aantal** wijzigen op het sneltabblad **Event Changes** en de wijzigingen direct grafisch zien in het tabblad **Timeline** van het venster **Planningsvoorstel**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Voorgestelde voorzieningsorders in de grafische weergave wijzigen  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelbeschikbaarheid per tijdlijn** in en kies vervolgens de gerelateerde koppeling.  

    Het venster **Artikelbeschikbaarheid per tijdlijn** wordt geopend met het artikelnummer, de vestiging en de variant van het artikel op de geselecteerde planningsregel vooraf ingevuld op de velden op het sneltabblad **Opties**. Het sneltabblad **Tijdlijn** toont een grafische weergave van de verwachte voorraad van het artikel, inclusief planningsvoorstellen.  

2.  Zorg ervoor dat het veld **Planningsvoorstellen opnemen** is geselecteerd.  
3.  Zoek de voorgestelde voorzieningsorder die u wilt wijzigen. U kunt de aanpasbare elementen vinden door de groene cirkel en een pictogram van de schijf. Zie voor meer informatie over de verschillende symbolen de sectie Symbolen en pictogrammen op het sneltabblad Tijdlijn.  
4.  Plaats de aanwijzer op de groene cirkel totdat deze vergroot en de aanwijzer verandert in het Verplaatsen-symbool (vier pijltjes).  
5.  Houd de muisknop ingedrukt terwijl u de aanwijzer omhoog of omlaag sleept om het aantal aan te passen. Houd de muisknop ingedrukt terwijl u de aanwijzer naar links of rechts sleept om de vervaldatum aan te passen.  
6.  Naast het verplaatsen van elementen door slepen en neerzetten, kunt u planningsvoorstellen aanpassen door een aantal functies in het vervolgkeuzemenu te gebruiken. Open het vervolgkeuzemenu voor de groene cirkel van een voorgesteld voorzieningselement en selecteer een van de volgende functies  

    |Functie|Omschrijving|  
    |--------------|---------------------------------------|  
    |**Nieuwe voorraad maken**|Hiermee wordt een nieuw element gemaakt op het punt waar u het vervolgkeuzemenu opent. Dit vertegenwoordigt een nieuwe voorgestelde aanvulorder. Het wordt een nieuwe regel in het planningsvoorstel wanneer u **Wijzigingen opslaan** kiest.<br /><br /> **OPMERKING:** als het veld **Vestigingsfilter** of **Variantfilter** op het tabblad **Options** leeg is of meer dan één filterwaarde bevat, wordt de nieuwe voorziening gemaakt en later opgeslagen naar het plannings- of inkoopvoorstel met de volgende codes:<br /><br /> * Als het filterveld leeg is, wordt de nieuwe voorziening gemaakt zonder een vestigings- of variantcode.<br /><br /> * Als er meer dan één filterwaarde is gedefinieerd, wordt de nieuwe voorziening gemaakt voor de eerste filterwaarde volgens de sorteermethode.<br /><br /> Als u een andere variant- of vestigingscode wilt, moet u dat handmatig wijzigen op de nieuwe planningsregel.|  
    |**Voorziening automatisch aanpassen**|Optimaliseert een nieuwe voorziening die u in de grafiek hebt gemaakt door ervoor te zorgen dat deze resulteert in nul-voorraad voor de volgende voorziening.|  
    |**Voorziening verwijderen**|Hiermee verwijdert u het element in het sneltabblad **Tijdlijn** en verwijdert u de planningsregel wanneer u **Wijzigingen opslaan** kiest. Het pictogram verandert in een schijf met een rood kruis wanneer de voorziening is verwijderd.<br /><br /> **OPMERKING:** u kunt alleen een voorziening van het type planningsboodschap **Nieuw** verwijderen. Nadat u **Wijzigingen opslaan** kiest, moet u handmatig de betreffende planningsregel verwijderen in het plannings- of inkoopvoorstel.|  

7.  Kies de actie **Opnieuw laden** als u alle wijzigingen wilt terugdraaien die u hebt aangebracht nadat u het venster **Artikelbeschikbaarheid per tijdlijn** voor het laatst hebt geopend of **Opnieuw laden** hebt geselecteerd.  
8. Wanneer de elementen zijn geplaatst waar u ze wilt in het schema, klikt u op **Wijzigingen opslaan** om het aangepaste aantal en de datumwijzigingen te kopiëren naar de plannings- of inkoopregels die de grafische elementen weergeven.  

Om de wijzigingen in het voorzieningsplan te implementeren, moet u de resulterende planningsboodschappen van het plannings- of inkoopvoorstel opvolgen. Zie voor meer informatie Planningsboodschap uitvoeren - Plan.

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Symbolen en pictogrammen op het sneltabblad Tijdlijn
 |Symbool/pictogram|Omschrijving|  
 |------------------|---------------------------------------|  
 |Zwart kruis|Orders (zowel vraag als aanbod).<br /><br /> -   Kan niet worden gewijzigd.<br />-   Zichtbaar wanneer het veld **Geplande voorraad weergeven** is geselecteerd (oranje grafiek).|  
 |Rode cirkel|Bestaande voorzieningsorders die geen deel uitmaken van planningsvoorstellen.<br /><br /> -   Kan niet worden gewijzigd.<br />-   Zichtbaar wanneer het veld **Geplande voorraad weergeven** is geselecteerd (oranje grafiek).|  
 |Gele ster|Vraag voorspellen.<br /><br /> -   Kan niet worden gewijzigd.<br />-   Zichtbaar wanneer het veld **Prognosenaam** een waarde bevat.<br /><br /> Wanneer zowel het veld **Geplande voorraad weergeven** als het veld **Planningsuggesties opnemen** is geselecteerd, heeft elke gele ster een gekoppelde tegenhanger in de tegenovergestelde grafiek. Dit illustreert hoe een voorgesteld aanbod voldoet aan de geprognosticeerde vraag.|  
 |Groene cirkel met een pictogram in de vorm van een schijf met een rood kruis|Voorgestelde voorzieningsorder met planningsboodschap *Annuleren*.<br /><br /> -   Kan niet worden gewijzigd.<br />-   Zichtbaar wanneer het veld **Planningsuggesties opnemen** is geselecteerd (groene grafiek).|  
 |Groene cirkel met een pictogram in de vorm van een schijf met een ster|Voorgestelde voorzieningsorders met planningsboodschap *Nieuw*.<br /><br /> -   Kan worden gewijzigd.<br />-   Zichtbaar wanneer het veld **Planningsuggesties opnemen** is geselecteerd (groene grafiek).|  
 |Groene cirkel met een pictogram in de vorm van een schijf met een of twee pijlen|Voorgestelde voorzieningenorders met planningsboodschap *Herplannen*, *Aantal wijzigingen* of *Herplannen en aantal wijzigingen*<br /><br /> -   Kan worden gewijzigd.<br />-   Zichtbaar wanneer het veld **Planningsuggesties opnemen** is geselecteerd (groene grafiek).<br /><br /> De pijlen geven de richting van de planningsuggestie aan. Bijvoorbeeld een pijl-links samen met een pijl-omhoog geeft een planningsboodschap *Herplannen en Aantal wijzigen* aan die uit een achterwaartse herplanning en een toename van het aantal bestaat.|  

Wanneer u het vervolgkeuzemenu voor het sneltabblad **Tijdlijn** opent, worden de volgende functies weergegeven, afhankelijk van wat u kiest  

 |Functie|Omschrijving|  
 |--------------|---------------------------------------|  
 |**Nieuwe voorraad maken**|Hiermee wordt een nieuw element gemaakt op het punt waar u het vervolgkeuzemenu opent. Dit vertegenwoordigt een nieuwe voorgestelde aanvulorder. Het wordt een nieuwe regel in het planningsvoorstel wanneer u **Wijzigingen opslaan** kiest op het tabblad **Verwerken**.<br /><br /> Filterwaarden die worden gedefinieerd in het veld **Vestigingsfilter** of **Variantfilter** op het sneltabblad **Opties**, worden toegepast op de nieuwe voorzieningenorder. **Opmerking:** als de filtervelden leeg zijn of meer dan één filterwaarde bevatten, wordt de nieuwe voorzieningsorder gemaakt met behulp van de volgende codes: <ul><li>Als het filterveld leeg is, wordt de nieuwe voorziening gemaakt zonder een vestigings- of variantcode.</li><li>Als er meer dan één filterwaarde is gedefinieerd, wordt de nieuwe voorziening gemaakt met behulp van de eerste filterwaarde op basis van de sorteervolgorde.</li></ul> Als u een andere variant- of vestigingscode wilt in de nieuwe voorzieningsorder, moet u deze handmatig wijzigen op de nieuwe planningsregel.|  
 |**Voorziening automatisch aanpassen**|Hiermee wordt een nieuwe voorziening geoptimaliseerd die u in de grafiek hebt gemaakt door ervoor te zorgen dat er een nul-voorraad ontstaat vóór de volgende voorziening.|  
 |**Voorziening verwijderen**|Hiermee verwijdert u het element op het sneltabblad **Tijdlijn** en verwijdert u de planningsregel wanneer u **Wijzigingen opslaan** kiest op het tabblad **Verwerken**. Het pictogram verandert in een schijf met een rood kruis nadat de voorziening is verwijderd. **Opmerking:** u kunt alleen een voorziening van het type planningsboodschap *Nieuw* verwijderen. Nadat u **Wijzigingen opslaan** hebt gekozen op het tabblad **Verwerken**, moet u handmatig de desbetreffende planningsregel verwijderen in het plannings- of inkoopvoorstel.|  
 |**Document weergeven**|Hiermee wordt de order, planningsregel of prognose geopend die het element vertegenwoordigt.|  
 |**Uitzoomen (Ctrl++)**|Hiermee wordt de schaal van de x-as groter gemaakt, zodat er minder dagen worden weergegeven. **Opmerking:** u kunt dit ook doen door op Ctrl + muiswiel te drukken.|  
 |**Inzoomen (Ctrl+-)**|Hiermee wordt de schaal van de x-as kleiner gemaakt, zodat er meer dagen worden weergegeven. **Opmerking:** u kunt dit ook doen door op Ctrl + muiswiel te drukken.|  
 |**Zoom opnieuw instellen (Ctrl+0)**|Hiermee wordt de schaal van de x-as teruggezet op wat werd gebruikt voordat u inzoomde.|  

Behalve de toetsenbordacties die eerder werden vermeld, kunt u ook de volgende toetsenbordacties gebruiken op het sneltabblad **Tijdlijn**.  

 |Toetsenbordactie|Omschrijving|  
 |---------------------|---------------------------------------|  
 |Ctrl + muiswiel|Hiermee wordt de schaal van de x-as gewijzigd.|  
 |Selecteer een element en druk vervolgens op Shift + pijl|Hiermee wordt het element verplaatst in de richting waarnaar de pijl wijst.|  
 |Tab|Hiermee gaat u naar het volgende element.|  
 |Shift + tab|Hiermee gaat u naar het vorige element.|  
 |Druk op Esc terwijl u een element verplaatst.|Hiermee annuleert u de verplaatsing. **Opmerking:** werkt niet als u de muisknop hebt losgelaten.|

## <a name="see-also"></a>Zie ook  
[Gepland](production-planning.md)   
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

