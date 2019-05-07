---
title: Criteria voor het overbrengen van grootboekposten naar kostenposten | Microsoft Docs
description: Het is belangrijk dat u een goed begrip heeft van de criteria voor het overbrengen van grootboekposten naar kostenposten. Tijdens de overdracht maakt de batchverwerking **Grootboekposten overbrengen naar kostprijsboekhouding** gebruik van de volgende criteria om te bepalen of en hoe de grootboekposten worden overgebracht.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 62d19b5ff112871f7f44f0945bdcfd38306ed8b3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931663"
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
 [Grootboekposten overbrengen naar kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)   
 [Kostprijsboekhouding](finance-about-cost-accounting.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
