---
title: 'Procedure: Speciale orders maken | Microsoft Docs'
description: U kunt een speciale order maken om een bepaald artikel dat niet op voorraad is, te verzenden aan een bepaalde klant. Het artikel wordt door uw leverancier verzonden naar uw magazijn, zodat u het vervolgens afzonderlijk of samen met artikelen van een andere order kunt verzenden aan uw klant.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c7e5d7cda12abd94a999031af3bc8d505b7f6c5e
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-special-orders"></a>Procedure: Speciale orders maken
U kunt een speciale order maken om een bepaald artikel, dat niet op voorraad is, te verzenden aan een bepaalde klant. Het artikel wordt door uw leverancier verzonden naar uw magazijn, zodat u het vervolgens afzonderlijk of samen met artikelen van een andere order kunt verzenden aan uw klant.  

Speciale orders maken het mogelijk een inkooporder en een verkooporder aan elkaar te koppelen zodat het artikel dat niet op voorraad is wordt gepickt en aan de klant wordt geleverd.  

U kunt deze functie pas gebruiken als u de klanten-, leveranciers- en artikelkaart die voor de order nodig zijn, hebt ingesteld.  

## <a name="to-create-a-special-order"></a>Speciale orders maken  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporder** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Maak een  verkooporder voor het artikel en vul deze in. Zie [Procedure: Producten verkopen](sales-how-sell-products.md) voor meer informatie.
3.  Ga naar het sneltabblad **Regels** en vul de verkoopregel in. Selecteer in het veld **Inkoopcode** een inkoopcode waarbij een vinkje staat in het veld **Speciale order**.

    U moet nu een inkooporder maken op basis van een inkoopvoorstel.  
4. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopvoorstel** in en klik vervolgens op de gerelateerde koppeling.  
5. Kies de actie **Speciale order** en kies vervolgens de actie **Verkooporders ophalen**.  
6.  Geef in het venster **Verkooporders ophalen** resultaten weer waarbij **Documentnr.** het nummer van de verkooporder is. Kies de knop **Ok**. Automatisch wordt een inkoopvoorstelregel voor het artikel gemaakt.  
7.  Selecteer **Nieuw** in het veld **Planningsboodschap** op de inkoopvoorstelregel.  
8.  Klik in het venster **Inkoopvoorstel** op de actie **Planningsboodschap uitvoeren**. Het venster **Planningsboodschap uitvoeren - Ink.-voorstel** wordt geopend. Kies de knop **OK**.  

    In een bericht wordt medegedeeld dat de inkooporders zijn gemaakt. Kies de knop **OK**.  

Een inkooporder die is gemaakt als speciale order voor een verkooporder wordt overgenomen door het planningssysteem aangezien deze vraag en aanbod in evenwicht brengt. Dat wil zeggen, dat de inkooporder (aanbod) gekoppeld blijft aan de verkooporder (vraag), zelfs als die inkooporder aan een andere, eerdere, vraag zou kunnen voldoen. Zie voor meer informatie [Ontwerpdetails: Bestelbeleid](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  U kunt de functionaliteit voor speciale volgorde niet gebruiken als het item al is gereserveerd. Zorg er daarom voor dat voor artikelen die zijn verkocht op speciale orders het veld **Reserveren** op de artikelkaart niet is ingesteld op **Altijd**.  

## <a name="see-also"></a>Zie ook  
[Procedure: Werken met niet-voorraadartikelen](inventory-how-work-nonstock-items.md)  
[Verkoop](sales-manage-sales.md)  
[Procedure: Doorverzendingen maken](sales-how-drop-shipment.md)   
[Ontwerpdetails: Bestelbeleid](design-details-reservation-order-tracking-and-action-messaging.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

