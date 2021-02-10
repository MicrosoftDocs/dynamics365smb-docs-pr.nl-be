---
title: Werken met financiële overzichten in Excel
description: Leren hoe u de financiële overzichten in Microsoft Excel kunt openen vanuit Business Central voor een betere analyse.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 58c1d9bba8942dbd400a3ed0837ef7a39fd2bb13
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747153"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Financiële overzichten analyseren in Microsoft Excel

In [!INCLUDE [prod_short](includes/prod_short.md)] kunt u KPI's bekijken en overzichten krijgen van de financiële status van het bedrijf. U kunt ook lijsten in Excel openen en de gegevens daar analyseren. Maar u kunt ook zware financiële overzichten exporteren, zoals de balans of resultatenrekening naar Excel, de gegevens analyseren en de rapporten afdrukken.  

In de rolcentra Bedrijfsmanager en Accountant kunt u kiezen welke financiële overzichten u weergeeft in Excel vanuit een vervolgkeuzemenu in het gedeelte Lijsten van het lint. Als u een overzicht kiest, wordt het in Excel of Excel Online geopend. Een invoegtoepassing verbindt de gegevens met [!INCLUDE [prod_short](includes/prod_short.md)]. U moet zich echter aanmelden met hetzelfde account dat u gebruikt met [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Het overzicht en de details weergeven in Excel

Kies op het lint de relevante Excel-lijst en laat deze openen zodat u het overzicht krijgt dat u wilde. In deze versie van [!INCLUDE [prod_short](includes/prod_short.md)] bieden we de volgende Excel-rapporten:

- Balans  
- Resultatenrekening  
- Cashflowafschrift  
- Afschrift van ingehouden winst  
- Vervallen betalingen  
- Vervallen vorderingen  

Stel dat u wat beter naar uw cashflow wilt kijken. Vanuit het rolcentrum Bedrijfsmanager of Accountant kunt u het rapport **Cashflowafschrift** in Excel openen, maar wat werkelijk gebeurt is dat we de relevante gegevens voor u exporteren en een Excel-werkmap maken op basis van een vooraf gedefinieerde sjabloon. Afhankelijk van uw browser, wordt u mogelijk gevraagd de werkmap te openen of op te slaan.  

In Excel ziet u een tabblad met de gegevens op het eerste werkblad. Alle gegevens die zijn geëxporteerd zijn ook aanwezig in andere werkbladen voor het geval dat dat nodig is. U kunt de lijst rechtstreeks afdrukken of u kunt deze wijzigen totdat u het overzicht en de details hebt die u wilt. Gebruik de [!INCLUDE [prod_short](includes/prod_short.md)] Excel-invoegtoepassing om gegevens verder te filteren en te analyseren.  

### <a name="understanding-the-excel-templates"></a>Inzicht in de Excel-sjablonen

De voorgedefinieerde Excel-rapporten zijn gebaseerd op de gegevens in het huidige bedrijf. Het demonstratiebedrijf heeft bijvoorbeeld het rekeningschema opgezet met drie geldrekeningen onder *Vlottende activa*: 10100 **Betaalrekening**, 10200 **Spaarrekening** en 10300 **Kleine kas**. De accounts hebben het veld **Rekeningsubcategorie** ingesteld op *Contant geld* en het is hun gecombineerde bedrag dat wordt weergegeven als *Contant geld* in het Excel-rapport **Balans**.  

Extra bladen in de Excel-werkmap tonen de gegevens achter het rapport. Maar om erachter te komen wat er achter de groeperingen in de Excel-rapporten schuilgaat, moet u misschien teruggaan naar [!INCLUDE [prod_short](includes/prod_short.md)] en bijvoorbeeld filters op de lijsten toepassen.  

## <a name="the-prod_short-excel-add-in"></a>De Excel-invoegtoepassing [!INCLUDE [prod_short](includes/prod_short.md)]

Uw [!INCLUDE [prod_short](includes/prod_short.md)]-ervaring bevat een invoegtoepassing voor Excel. Afhankelijk van uw abonnement, wordt u automatisch aangemeld of moet u dezelfde aanmeldingsdetails opgeven die u gebruikt voor [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie [Kopiëren en bewerken vanuit Business Central](across-work-with-excel.md).  

Met de invoegtoepassing kunt u up-to-date gegevens krijgen vanuit [!INCLUDE [prod_short](includes/prod_short.md)] en kunt u wijzigingen terugsturen naar [!INCLUDE [prod_short](includes/prod_short.md)]. De mogelijkheid om wijzigingen terug te sturen naar de database is uitgeschakeld voor de financiële Excel-rapporten in de bovenstaande lijst.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Weergeven en bewerken in Excel vanuit Business Central](across-work-with-excel.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met Business Central](ui-work-product.md)  
