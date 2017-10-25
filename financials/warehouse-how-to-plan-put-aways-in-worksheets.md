---
title: Plannen van opslagactiviteiten in werkbladen | Microsoft Docs
description: Als voor de vestiging zowel opslag- als ontvangstverwerking is ingesteld en u opslaginstructies wilt plannen voor een aantal ontvangsten en bovendien liever niet wilt dat de magazijnmedewerkers de instructies van het programma voor afzonderlijk geboekte ontvangsten volgen, kunt u een opslagvoorstel maken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 99c3ac10460a62ee23294cfd0d8c25709c37901b
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-put-aways-in-worksheets"></a>Procedure: plannen van opslagactiviteiten in werkbladen
Als voor de vestiging zowel opslag- als ontvangstverwerking is ingesteld en u opslaginstructies wilt plannen voor een aantal ontvangsten en bovendien liever niet wilt dat de magazijnmedewerkers de instructies van het programma voor afzonderlijk geboekte ontvangsten volgen, kunt u een opslagvoorstel maken.  

Als u voor het magazijn wilt instellen dat ontvangstregels direct na boeking voor u beschikbaar zijn in het opslagvoorstel, selecteert u het veld **Opslagvoorstel gebruiken** op het sneltabblad **Magazijn** op de vestigingskaart. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

Als u dit veld niet selecteert, worden er bij het boeken van ontvangsten automatisch opslaginstructies gemaakt.  

> [!NOTE]  
>  onafhankelijk van de status van het veld **Opslagvoorstel gebruiken** op de vestigingskaart, kunt u altijd opslaginstructieregels, zijnde geboekte-ontvangstregels, ophalen voor het opslagvoorstel. Ga hiertoe als volgt te werk:  
>   
>  1.  Druk in het venster **Magazijnopslag** op Ctrl+D om de gehele opslaginstructie te verwijderen. U kunt ook de regels selecteren die u in het voorstel wilt verwerken en de regels vervolgens verwijderen.  
> 2.  Voer deze stap uit voor alle gewenste opslaginstructies, totdat u alle regels hebt verwijderd waarmee u in het voorstel aan de slag wilt. Klik nu op **Opslagvoorstellen** en ga door met de planning.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>U kunt als volgt instructies plannen in het opslagvoorstel  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Opslagvoorstel** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Magazijndocumenten ophalen**. Het venster **Opslagselectie** verschijnt.  

    Dit venster bevat alle geboekte ontvangsten en geregistreerde interne opslagactiviteiten die zijn doorgestuurd naar de opslagfunctie, inclusief de activiteiten waarvoor de opslaginstructies al zijn gemaakt. De lijst bevat geen documenten met opslagregels die volledig zijn uitgevoerd en geregistreerd.  

3. Selecteer de documenten waaraan u in het voorstel wilt werken. U kunt tegelijkertijd werken aan regels uit verschillende documenten.  

    > [!NOTE]  
    >  als u een ontvangstdocument of interne-opslagdocument selecteert waarvoor u al instructies hebt gemaakt voor alle regels, meldt het programma dat er niets is om te verwerken.  

4. Vul het veld **Sorteringsmethode** in om de regels op de gewenste wijze te sorteren.  

    > [!NOTE]  
    >  De manier waarop de regels in het werkblad gesorteerd worden, werkt niet automatisch door in de opslaginstructie, maar dezelfde sorteermogelijkheden bestaan, samen met het rangschikken van opslaglocaties. De regelvolgorde die u in het werkblad plant kunt u dus eenvoudig opnieuw maken wanneer u de opslaginstructies maakt of sorteert.  

5.  Vul het veld **Te verwerken aantal** in. Kies de actie **Te verwerken aantal autom. invullen** of vul de velden handmatig in.  
6.  Indien nodig, kunt u de regels handmatig bewerken. U kunt bijvoorbeeld regels verwijderen als artikelen moeten worden opgeslagen in opslaglocaties die ver van elkaar liggen.  

    > [!NOTE]  
    >  de verwijderde regels worden alleen uit het voorstel verwijderd, niet uit de opslagselectielijst.  

7.  Kies de actie **Opslag maken**. Het venster **Document maken** wordt geopend, waar u als volgt informatie kunt toevoegen aan de opslaginstructies die u aan het maken bent:  

    -   U kunt de opslaginstructie toewijzen aan een bepaalde magazijnmedewerker.  
    -   U kunt de regels met opslaginstructies sorteren als in het werkblad of door middel van rangschikking van opslaglocaties. Wanneer u sorteert op basis van rangschikking van opslaglocaties, worden de nemen-regels eerst weergegeven, aangezien de meeste ontvangst-opslaglocaties een opslaglocatie-rangschikking van 0 hebben en worden de plaatsen-regels als laatste weergegeven, beginnend met de opslaglocaties met de laagste opslaglocatie-rangschikking. Indien u uw magazijn hebt gestructureerd zodat opslaglocaties met een soortgelijke opslaglocatie-rangschikking bij elkaar staan, bespaart het sorteren van regels op deze manier uiteindelijk stappen voor uw magazijnmedewerkers.  
    -   Wanneer een bepaalde eenheid wordt opgesplitst in kleinere eenheden, worden er extra splitsingsregels weergegeven. Als u deze tussenliggende regels niet wilt weergeven, selecteert u **Breakbulkfilter plaatsen**. Zie [Procedure: Automatisch splitsen van bulkgoederen met gestuurde opslag en pick inschakelen] (warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md) voor meer informatie.  
    -   U kunt het veld **Te verwerken aantal** op de opslaginstructies automatisch laten invullen.  
    -   Indien gewenst kunt u het document direct afdrukken.  

8.  Klik op de knop **OK**. De opslaginstructies worden geheel naar uw wens opgesteld.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

