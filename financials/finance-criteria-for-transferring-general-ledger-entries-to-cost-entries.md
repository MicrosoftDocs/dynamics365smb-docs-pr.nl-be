---
title: Criteria voor het overbrengen van grootboekposten naar kostenposten | Microsoft Docs
description: Het is belangrijk dat u een goed begrip heeft van de criteria voor het overbrengen van grootboekposten naar kostenposten. Tijdens de overdracht maakt de batchverwerking **Grootboekposten overbrengen naar kostprijsboekhouding** gebruik van de volgende criteria om te bepalen of en hoe de grootboekposten worden overgebracht.
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
ms.openlocfilehash: 59faad50504bff05e6cdb1c78d00553e85faf47e
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Criteria voor het overbrengen van grootboekposten naar kostenposten.
Het is belangrijk dat u een goed begrip heeft van de criteria voor het overbrengen van grootboekposten naar kostenposten. Tijdens de overdracht maakt de batchverwerking **Grootboekposten overbrengen naar kostprijsboekhouding** gebruik van de volgende criteria om te bepalen of en hoe de grootboekposten worden overgebracht.  

Grootboekposten worden overgebracht in de volgende gevallen:  

-   De posten hebben dimensiewaarden die een bijbehorende kostenplaats of kostenobject hebben.  
-   De posten hebben dimensiewaarden die een bijbehorende kostenplaats en kostenobject hebben. Voor deze posten heeft de kostenplaats voorrang. Dit voorkomt de situatie waarin een kostensoort zowel in een kostenobject als kostenplaats wordt weergegeven, en daarom twee keer in de statistieken wordt meegeteld.  
-   Het documentnummer in de posten is leeg, en wordt daarom weergegeven met documentnummer 0000 in de kostenposten.  
-   De posten worden overgebracht naar een kostensoort dat gecombineerde posten toestaat, en deze posten worden maandelijks of dagelijks overgebracht als een gecombineerde post.  

Grootboekposten worden niet overgebracht in de volgende gevallen:  

-   De posten hebben dimensiewaarden die geen bijbehorende kostenplaats of kostenobject hebben.  
-   De posten bevatten een bedrag met waarde nul.  
-   De posten zijn van een grootboekrekening die is verwijderd.  
-   De posten hebben een grootboekrekening die niet van het soort **Resultatenrekening** is.  
-   De posten hebben een grootboekrekening waaraan geen kostensoort is toegewezen.  
-   De posten hebben een boekingsdatum vóór de **Begindatum voor GB-overdracht**.  
-   De posten zijn geboekt met een ultimodatum. Dit zijn meestal de posten die een negatief effect hebben op het saldo van de resultatenrekening aan het einde van het jaar.  

## <a name="see-also"></a>Zie ook  
[Kosten verantwoorden](finance-manage-cost-accounting.md)  
 [Procedure: grootboekposten overbrengen naar kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)   
 [Kostprijsboekhouding](finance-about-cost-accounting.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
