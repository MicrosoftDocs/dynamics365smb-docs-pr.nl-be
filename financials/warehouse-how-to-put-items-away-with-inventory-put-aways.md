---
title: Artikelen opslaan met een voorraadopslag | Microsoft Docs
description: Als voor uw vestiging wel een opslagverwerking maar geen ontvangstverwerking is vereist, gebruikt u het document **Voorraadopslag** om opslag- en ontvangstinformatie voor uw brondocumenten vast te leggen en te boeken. Het inkomende brondocument kan een inkooporder zijn, maar ook een verkoopretourorder, een inkomende transferorder of een productieorder waarvan de output kan worden opgeslagen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 92eae2f24daf8181e39b3d22ea23c31a9ee85347
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="put-items-away-with-inventory-put-aways"></a>Artikelen opslaan met voorraadopslag
Als voor uw vestiging wel een opslagverwerking, maar geen ontvangstverwerking vereist is, gebruikt u het document **Voorraadopslag** om opslag- en ontvangstinformatie voor uw brondocumenten vast te leggen en te boeken. Het inkomende brondocument kan een inkooporder zijn, maar ook een verkoopretourorder, een inkomende transferorder of een assemblage- of productieorder waarvan de output kan worden opgeslagen.  

U kunt een voorraadopslag op drie manieren maken:  

- Maak de opslag in twee stappen door eerst een magazijnaanvraag uit het brondocument te maken, die voor het magazijn fungeert als signaal dat het brondocument gereed is voor opslag. De voorraadopslag kan vervolgens worden gemaakt vanuit het venster **Voorraadopslag** op basis van het brondocument.  
- Maak de voorraadopslag rechtstreeks vanuit het brondocument.  
- Gebruik een batchverwerking om de voorraadopslag voor verschillende brondocumenten tegelijk te maken.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Een voorraadopslag aanvragen door het brondocument vrij te geven
Voor inkooporders, verkoopretourorders, inkomende transferorders en assemblageorders maakt u het magazijnverzoek door de order vrij te geven. Hieronder wordt beschreven hoe u dit doet vanuit een inkooporder.  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkooporders** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de inkooporder die u wilt vrijgeven en kies de actie **Vrijgeven**.  

    Voor productieorders maakt u het magazijnverzoek door een inkomend verzoek te maken vanuit de vrijgegeven productieorder.  
3.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vrijgegeven productieorders** in en klik op de gerelateerde koppeling.  
4. Kies de actie **Ink. magazijnontvangst maken**.  

> [!NOTE]  
>  U kunt de inkomende magazijnaanvraag ook maken door het selectievakje **Inkomend verzoek maken** in te schakelen bij het vernieuwen van de productieorder. Zie [Productieorders opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md) voor meer informatie.  

Wanneer het magazijnverzoek is gemaakt, ziet de magazijnmedewerker verantwoordelijk voor de opslag van artikelen dat het brondocument gereed is en dat hij een nieuw voorraadopslagdocument kan maken.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Een voorraadopslag maken op basis van het brondocument
Nu het verzoek is gemaakt, kan de magazijnmedewerker een nieuwe voorraadopslag maken op basis van het vrijgegeven brondocument.   
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Voorraadopslag** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer in het veld **Brondocument** het soort brondocument waarvoor u opslaat.  
4. Selecteer het brondocument in het veld **Bronnr.**  
5. U kunt ook de actie **Brondocument ophalen** kiezen om het document te selecteren in een lijst met inkomende brondocumenten die gereed zijn voor opslag op de locatie.  
6. Klik op de knop **OK** om de opslagregels in te vullen op basis van het geselecteerde brondocument.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Een voorraadopslag maken op basis van het brondocument  
1.  Klik in het brondocument, dat een inkooporder, verkoopretourorder, inkomende transferorder of productieorder kan zijn, op de actie **Voorraadopslag/-pick maken**.  
2. Schakel het selectievakje **Voorraadopslag/-pick maken** in.
3. Kies de knop **OK**. Er wordt een nieuwe voorraadopslag gemaakt.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Meerdere voorraadopslagactiviteiten maken met een batchverwerking  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Voorraadopslag/-pick maken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Gebruik op het sneltabblad **Magazijnverzoek** van het opgevraagde venster de velden **Brondocument** en **Bronnr.** om te filteren op bepaalde soorten documenten of reeksen documentnummers.  
3.  Schakel op het sneltabblad **Opties** het selectievakje **Voorraadopslag maken** in.
4.  Kies de knop **OK**. De opgegeven voorraadopslagactiviteiten worden gemaakt.

## <a name="to-record-the-inventory-put-away"></a>De voorraadopslag registreren  
1. Open een eerder gemaakt opslagdocument door er een te selecteren in het venster **Voorraadopslag**.  
2. In het veld **Opslaglocatie** op de opslagregels wordt op basis van de standaardopslaglocatie per artikel de opslaglocatie voorgesteld waarin de artikelen moeten worden opgeslagen. De opslaglocatie in dit venster kunt u desgewenst wijzigen.  
3. Voer de opslag uit en voer het werkelijk opgeslagen aantal in het veld **Te verwerken aantal** in.

    Als het nodig is de artikelen voor een regel in meerdere opslaglocaties te plaatsen, bijvoorbeeld omdat de aangewezen opslaglocatie vol is, gebruikt u de functie **Regel splitsen** op het sneltabblad **Regels**. Zie voor meer informatie over het splitsen van regels [Magazijnactiviteitsregels splitsen](warehouse-how-to-split-warehouse-activity-lines.md)  
4. Als u de opslag hebt uitgevoerd, kiest u de actie **Boeken**.  

Tijdens het boekingsproces wordt de ontvangst, in het geval van productieorders de output, geboekt van de brondocumentregels die zijn opgeslagen. Als in de vestiging opslaglocaties worden gebruikt, worden ook magazijnposten gemaakt, waarin de gewijzigde aantallen van de opslaglocaties worden geboekt.

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

