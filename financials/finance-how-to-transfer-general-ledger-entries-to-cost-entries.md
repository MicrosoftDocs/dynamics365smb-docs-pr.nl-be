---
title: 'Procedure: grootboekposten overbrengen naar kostenposten | Microsoft Docs'
description: U kunt grootboekposten overbrengen naar kostenposten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4e68378d7acc789a70caf9c5b0590a81bf874337
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-general-ledger-entries-to-cost-entries"></a>Procedure: grootboekposten overbrengen naar kostenposten.
U kunt grootboekposten overbrengen naar kostenposten.  

Voordat u begint met de bewerking om grootboekposten over te brengen naar kostenposten, moet u de overdracht voorbereiden zodat wordt voorkomen dat u fouten handmatig moet corrigeren die tijdens de boeking worden gemaakt.  

## <a name="to-prepare-the-transfer"></a>De overdracht voorbereiden  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instelling kostprijsboekhouding** en klik vervolgens op de gerelateerde koppeling.  
2.  Controleer in het venster **Instelling kostprijsboekhouding** of het veld **Begindatum voor GB-overdracht** op de juiste waarde is ingesteld.  
3.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Kostensoortschema** in en klik vervolgens op de gerelateerde koppeling.  
4.  Controleer in het venster **Kostensoortkaart** of het veld **Grootboekrekeningbereik** juist gekoppeld is voor elke kostensoort om posten uit het grootboek te halen.  
5.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.  
6.  Voor elke gewenste grootboekrekening controleert u in het venster **Grootboekrekening** of het veld **Nr. kostensoort** juist is gekoppeld aan een kostensoort. Zie voor meer informatie [De relatie tussen de kostensoorten en grootboekrekeningen definiëren](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Controleer of alle relevante grootboekposten over dimensiewaarden beschikken die overeenkomen met een kostenplaats en een kostenobject.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Grootboekposten overbrengen naar kostenposten.  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekposten overbrengen naar kostprijsboekhouding** in en klik op de gerelateerde koppeling.  
2.  Klik op **Ja** om de overdracht te starten. Tijdens de bewerking worden alle grootboekposten overgebracht die niet al zijn overgebracht.  

    Tijdens de overdracht worden door het proces verbindingen in de posten in de tabel **Kostenpost** en de tabel **Kostenregister** gemaakt. Hierdoor kunt de bron van de kostenposten traceren.  

## <a name="see-also"></a>Zie ook  
 [Criteria voor het overbrengen van grootboekposten naar kostenposten.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Automatische overdracht en gecombineerde posten](finance-automatic-transfer-combined-entries.md)   
 [Resultaten van de overboeking](finance-results-of-the-transfer.md)   
 [Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)   
 [De relatie tussen de kostensoorten en grootboekrekeningen definiëren](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

