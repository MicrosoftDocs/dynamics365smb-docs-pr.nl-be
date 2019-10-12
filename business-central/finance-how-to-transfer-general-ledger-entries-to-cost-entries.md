---
title: 'Procedure: grootboekposten overbrengen naar kostenposten | Microsoft Docs'
description: U kunt grootboekposten overbrengen naar kostenposten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: c6eace42d460432df8ab4b72964408469fa0b563
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305888"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Grootboekposten overbrengen naar kostenposten
U kunt grootboekposten overbrengen naar kostenposten.  

Voordat u begint met de bewerking om grootboekposten over te brengen naar kostenposten, moet u de overdracht voorbereiden zodat wordt voorkomen dat u fouten handmatig moet corrigeren die tijdens de boeking worden gemaakt.  

## <a name="to-prepare-the-transfer"></a>De overdracht voorbereiden  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van kostprijsboekhouding** in en kies vervolgens de gerelateerde koppeling.  
2.  Controleer op de pagina **Instelling kostprijsboekhouding** of het veld **Begindatum voor GB-overdracht** op de juiste waarde is ingesteld.  
3.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostensoortschema** in en kies vervolgens de gerelateerde koppeling.  
4.  Controleer op de pagina **Kostensoortkaart** of het veld **Grootboekrekeningbereik** juist gekoppeld is voor elke kostensoort om posten uit het grootboek te halen.  
5.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
6.  Voor elke gewenste grootboekrekening controleert u op de pagina **Grootboekrekening** of het veld **Nr. kostensoort** juist is gekoppeld aan een kostensoort. Zie [Kostenboekhouding instellen](finance-set-up-cost-accounting.md) voor meer informatie.  
7.  Controleer of alle relevante grootboekposten over dimensiewaarden beschikken die overeenkomen met een kostenplaats en een kostenobject.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Grootboekposten overbrengen naar kostenposten.  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekposten overbrengen naar kostprijsboekhouding** in en kies vervolgens de gerelateerde koppeling.  
2.  Klik op **Ja** om de overdracht te starten. Tijdens de bewerking worden alle grootboekposten overgebracht die niet al zijn overgebracht.  

    Tijdens de overdracht worden door het proces verbindingen in de posten in de tabel **Kostenpost** en de tabel **Kostenregister** gemaakt. Hierdoor kunt de bron van de kostenposten traceren.  

## <a name="see-also"></a>Zie ook  
[Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)   
[Kostenboekhouding instellen](finance-set-up-cost-accounting.md)   
