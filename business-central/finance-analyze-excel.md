---
title: Werken met financiële overzichten in Excel
description: Leren hoe u de financiële overzichten in Microsoft Excel kunt openen vanuit Business Central voor een betere analyse.
author: brentholtorf
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: bholtorf
---
# Financiële overzichten analyseren in Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] biedt KPI's en krijgt overzichten van de financiën van uw bedrijf. Hieronder volgen voorbeelden van manieren om KPI's en overzichten in Excel te analyseren:

* Open lijsten in Excel en analyseer de gegevens. 
* Exporteer zware financiële overzichten, zoals de balans- of resultatenrekening naar Excel, analyseer de gegevens en druk de rapporten af.  

> [!TIP]
> De rapporten die u in Excel kunt bekijken, zijn standaard ontworpen om u te helpen bij het analyseren van het huidige jaar. Het rapport Resultatenrekening is echter een uitzondering. Met dat rapport kunt u de gegevens filteren om voorgaande jaren in uw analyses op te nemen.

## Het overzicht en de details weergeven in Excel

In de rolcentra Bedrijfsmanager en Accountant kunt u met de actie **Rapporten** kiezen welke financiële overzichten u in Excel weergeeft. Als u een overzicht kiest, wordt het in Excel of Excel Online geopend. Een invoegtoepassing verbindt de gegevens met [!INCLUDE [prod_short](includes/prod_short.md)]. U moet zich echter aanmelden met hetzelfde account dat u gebruikt met [!INCLUDE [prod_short](includes/prod_short.md)]. De volgende tabel geeft een overzicht van de rapporten en waar ze beschikbaar zijn.  


|Rapporteren  |Rolcentrum  |
|---------|---------|
|Balans                 | Bedrijfsmanager, Accountant |
|Resultatenrekening              | Bedrijfsmanager, Accountant |
|Afschrift van cashflows       | Bedrijfsmanager, Accountant |
|Afschrift van ingehouden winst| Bedrijfsmanager, Accountant |
|Geïnde btw         | Bedrijfsmanager, Accountant |
|Rekeningoverzichten van klant           | Bedrijfsmanager, Accountant |
|Vervallen betalingen         | Accountant |
|Vervallen vorderingen      | Accountant |

Stel dat u wat beter naar uw cashflow wilt kijken. Vanuit het rolcentrum Bedrijfsmanager of Accountant kunt u het rapport **Afschrift van cashflows** in Excel openen, maar wat werkelijk gebeurt is dat we de relevante gegevens voor u exporteren en een Excel-werkmap maken op basis van een vooraf gedefinieerde sjabloon. Afhankelijk van uw browser, wordt u mogelijk gevraagd de werkmap te openen of op te slaan.  

In Excel ziet u een tabblad met de gegevens op het eerste werkblad. Alle gegevens die zijn geëxporteerd zijn ook aanwezig in andere werkbladen voor het geval dat dat nodig is. U kunt de lijst rechtstreeks afdrukken of u kunt deze wijzigen totdat u het overzicht en de details hebt die u wilt. Gebruik de [!INCLUDE [prod_short](includes/prod_short.md)] Excel-invoegtoepassing om gegevens verder te filteren en te analyseren.  

### Inzicht in de Excel-sjablonen

De voorgedefinieerde Excel-rapporten zijn gebaseerd op de gegevens in het huidige bedrijf. Het demonstratiebedrijf heeft bijvoorbeeld het rekeningschema opgezet met drie geldrekeningen onder *Vlottende activa*: 10100 **Betaalrekening**, 10200 **Spaarrekening** en 10300 **Kleine kas**. De accounts hebben het veld **Rekeningsubcategorie** ingesteld op *Contant geld* en het is hun gecombineerde bedrag dat wordt weergegeven als *Contant geld* in het Excel-rapport **Balans**.  

Andere bladen in de Excel-werkmap tonen de gegevens achter het rapport. Om erachter te komen wat er achter de groeperingen in de Excel-rapporten zit, moet u wellicht de lijsten filteren in [!INCLUDE [prod_short](includes/prod_short.md)].  

## De Excel-invoegtoepassing [!INCLUDE [prod_short](includes/prod_short.md)]

Uw [!INCLUDE [prod_short](includes/prod_short.md)]-ervaring bevat een invoegtoepassing voor Excel. Afhankelijk van uw abonnement bent u automatisch aangemeld of moet u uw aanmeldgegevens opgeven voor [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie [Kopiëren en bewerken vanuit Business Central](across-work-with-excel.md).  

Met de invoegtoepassing kunt u gegevens vernieuwen vanuit [!INCLUDE [prod_short](includes/prod_short.md)] en kunt u wijzigingen terugsturen naar [!INCLUDE [prod_short](includes/prod_short.md)]. De mogelijkheid om wijzigingen terug te sturen naar de database is niet beschikbaar voor de financiële rapporten die u kunt weergeven in Excel.  

## Zie gerelateerde [Microsoft-training](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Zie ook

[Weergeven en bewerken in Excel vanuit Business Central](across-work-with-excel.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
