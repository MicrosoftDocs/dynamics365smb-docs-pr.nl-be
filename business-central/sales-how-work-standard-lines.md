---
title: Standaardregels instellen voor periodieke verkoop en inkopen | Microsoft Docs
description: U kunt verkoopregels en inkoopregels instellen die u vaak maakt en deze vervolgens invoeren op verkoop- en inkoopdocumenten om de regels snel te vullen met standaardgegevens.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d3ce7b8065837d98b55b6e2dd1644f79b34e534a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Periodieke verkoop- en inkoopregels maken
Als u vaak verkoop- en inkoopregels met dezelfde informatie moet maken, kunt u standaardregels instellen die u dan kunt invoegen op periodieke verkoop- en inkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders.  

In de volgende procedure wordt beschreven hoe u werkt met standaardverkoopregels. Dit werkt op een soortgelijke manier voor standaardinkoopregels.  

## <a name="to-set-up-standard-sales-lines"></a>Standaardverkoopregels instellen  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Standaardverkoopcodes** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **Standaardverkoopregels** de actie **Nieuw**.  
3. Vul de benodigde velden in op het sneltabblad **Algemeen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Voer op het sneltabblad **Regels** gegevens in de velden in om verkoopregels voor te bereiden die de standaardregels reflecteren die u verwacht te gebruiken als terugkerende regels in verkoopdocumenten.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Standaardverkoopregels invoegen op een verkoopfactuur
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Facturen** in en klik vervolgens op de gerelateerde koppeling.
2. Open de verkoopfactuur waarin u een of meer standaardverkoopregels wilt invoegen.
3. Kies de actie **Periodieke verkoopregels ophalen**.
4. Kies in het venster **Periodieke verkoopregels** de opzoekknop in het veld **Code** en selecteer een set standaardverkoopregels.
5. Kies de knop **OK** om de standaardverkoopregels op de factuur in te voegen, waar u deze zo kunt gebruiken of de gegevens kunt bewerken.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Meerdere verkoopfacturen maken op basis van standaardverkoopregels
U kunt de batchverwerking **Periodieke verkoopfacturen maken** gebruiken om verkoopfacturen te maken volgens de standaardverkoopregels die zijn toegewezen aan de klanten, en met boekingsdatums binnen de datums voor geldig vanaf en geldig tot die u in de standaardverkoopcode opgeeft.

In het venster **Periodieke verkoopregels** kunt u ook een betalingsmethode voor automatische incasso en machtiging voor automatische incasso opgeven. De verkoopfacturen die zijn gemaakt met de batchverwerking **Periodieke verkoopfacturen maken** bevatten dan informatie die nodig is om de betaling voor de verkoopfacturen met automatische incasso van SEPA te innen. Zie voor meer informatie [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Periodieke verkoopfacturen aanmaken** in en klik vervolgens op de gerelateerde koppeling.
2. Vul de velden in het venster **Periodieke verkoopfacturen maken** in met de benodigde gegevens.
3. In het veld **Code** voert u de code in voor standaardverkoopregels die aan een klant worden toegewezen voor wie u verkoopfacturen wilt maken.
4. Kies de knop **OK**.

Verkoopfacturen worden gemaakt voor klanten met de opgegeven standaard klantverkoopcode en een waarde opgegeven voor automatische incasso-informatie voor het boeken op de opgegeven datum.

## <a name="see-also"></a>Zie ook  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

