---
title: Plannen van opslagactiviteiten in werkbladen | Microsoft Docs
description: Als voor de vestiging zowel opslag- als ontvangstverwerking is ingesteld en u opslaginstructies wilt plannen voor een aantal ontvangsten en bovendien liever niet wilt dat de magazijnmedewerkers de instructies van het programma voor afzonderlijk geboekte ontvangsten volgen, kunt u een opslagvoorstel maken.
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
ms.openlocfilehash: f6ef554270c9e2bdef8074b65ba6e3f0de4bd45c
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="plan-put-aways-in-worksheets"></a>Plannen van opslagactiviteiten in werkbladen
Als voor de vestiging zowel opslag- als ontvangstverwerking is ingesteld en u opslaginstructies wilt plannen voor een aantal ontvangsten en bovendien liever niet wilt dat de magazijnmedewerkers de instructies van het programma voor afzonderlijk geboekte ontvangsten volgen, kunt u een opslagvoorstel maken.  

Als u voor het magazijn wilt instellen dat ontvangstregels direct na boeking voor u beschikbaar zijn in het opslagvoorstel, selecteert u het veld **Opslagvoorstel gebruiken** op het sneltabblad **Magazijn** op de vestigingskaart. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

Als u dit veld niet selecteert, worden er bij het boeken van ontvangsten automatisch opslaginstructies gemaakt.  

> [!NOTE]  
>  onafhankelijk van de status van het veld **Opslagvoorstel gebruiken** op de vestigingskaart, kunt u altijd opslaginstructieregels, zijnde geboekte-ontvangstregels, ophalen voor het opslagvoorstel. Ga hiertoe als volgt te werk:  
>   
>  1.  Druk in het venster **Magazijnopslag** op Ctrl+D om de gehele opslaginstructie te verwijderen. U kunt ook de regels selecteren die u in het voorstel wilt verwerken en de regels vervolgens verwijderen.  
> 2.  Voer deze stap uit voor alle gewenste opslaginstructies, totdat u alle regels hebt verwijderd waarmee u in het voorstel aan de slag wilt. Klik nu op **Opslagvoorstellen** en ga door met de planning.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>U kunt als volgt instructies plannen in het opslagvoorstel  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslagvoorstel** in en kies vervolgens de gerelateerde koppeling.  
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
    -   Wanneer een bepaalde eenheid wordt opgesplitst in kleinere eenheden, worden er extra splitsingsregels weergegeven. Als u deze tussenliggende regels niet wilt weergeven, selecteert u **Breakbulkfilter plaatsen**. Zie [Automatisch splitsen van bulkgoederen met gestuurde opslag en pick inschakelen] (warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md) voor meer informatie.  
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

