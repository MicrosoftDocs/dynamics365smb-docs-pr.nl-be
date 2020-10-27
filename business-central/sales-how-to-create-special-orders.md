---
title: 'Procedure: Speciale orders maken | Microsoft Docs'
description: U kunt een speciale order maken om een bepaald catalogusartikel dat niet op voorraad is, te verzenden aan een bepaalde klant. Het artikel wordt door uw leverancier verzonden naar uw magazijn, zodat u het vervolgens afzonderlijk of samen met artikelen van een andere order kunt verzenden aan uw klant.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 85e27db78481e3e3cd9f8e8ef34eb26eee8b08f0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925909"
---
# <a name="create-special-orders"></a>Speciale orders maken
U kunt een speciale order maken om een bepaald catalogusartikel dat niet op voorraad is, te verzenden aan een bepaalde klant. Het artikel wordt door uw leverancier verzonden naar uw magazijn, zodat u het vervolgens afzonderlijk of samen met artikelen van een andere order kunt verzenden aan uw klant.  

Speciale orders maken het mogelijk een inkooporder en een verkooporder aan elkaar te koppelen zodat het catalogusartikel dat niet op voorraad is wordt gepickt en aan de klant wordt geleverd.  

U kunt deze functie pas gebruiken als u de klanten-, leveranciers- en artikelkaart die voor de order nodig zijn, hebt ingesteld.  

## <a name="to-create-a-special-order"></a>Speciale orders maken  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporder** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw** . Maak een  verkooporder voor het artikel en vul deze in. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
3.  Ga naar het sneltabblad **Regels** en vul de verkoopregel in. Selecteer in het veld **Inkoopcode** een inkoopcode waarbij een vinkje staat in het veld **Speciale order** .

    U moet nu een inkooporder maken op basis van een inkoopvoorstel.  
4. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopvoorstel** in en kies de desbetreffende koppeling.  
5. Kies de actie **Speciale order** en kies vervolgens de actie **Verkooporders ophalen** .  
6.  Geef op de pagina **Verkooporders ophalen** resultaten weer waarbij **Documentnr.** het nummer van de verkooporder is. Kies de knop **Ok** . Automatisch wordt een inkoopvoorstelregel voor het artikel gemaakt.  
7.  Selecteer **Nieuw** in het veld **Planningsboodschap** op de inkoopvoorstelregel.  
8.  Kies op de pagina **Inkoopvoorstel** de actie **Planningsboodschap uitvoeren** . De pagina **Planningsboodschap uitvoeren - Ink.-voorstel** wordt weergegeven. Kies de knop **OK** .  

    In een bericht wordt medegedeeld dat de inkooporders zijn gemaakt. Kies de knop **OK** .  

Een inkooporder die is gemaakt als speciale order voor een verkooporder wordt overgenomen door het planningssysteem aangezien deze vraag en aanbod in evenwicht brengt. Dat wil zeggen, dat de inkooporder (aanbod) gekoppeld blijft aan de verkooporder (vraag), zelfs als die inkooporder aan een andere, eerdere, vraag zou kunnen voldoen. Zie voor meer informatie [Ontwerpdetails: Bestelbeleid](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  U kunt de functionaliteit voor speciale volgorde niet gebruiken als het item al is gereserveerd. Zorg er daarom voor dat voor artikelen die zijn verkocht op speciale orders het veld **Reserveren** op de artikelkaart niet is ingesteld op **Altijd** .  

## <a name="see-also"></a>Zie ook  
[Werken met catalogusartikelen](inventory-how-work-nonstock-items.md)  
[Verkoop](sales-manage-sales.md)  
[Doorverzendingen uitvoeren](sales-how-drop-shipment.md)   
[Ontwerpdetails: Bestelbeleid](design-details-reservation-order-tracking-and-action-messaging.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
