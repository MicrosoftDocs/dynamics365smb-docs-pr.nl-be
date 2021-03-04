---
title: Uw Business Central-gegevens exporteren naar Excel | Microsoft Docs
description: U kunt uw financiële rapporten en bedrijfsinformatiegegevens uit Business Central exporteren naar Excel of uw gegevens in Excel openen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0058fd8aa684fd12392e641dda3bbb0ee6862134
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753704"
---
# <a name="exporting-your-business-data-to-excel"></a>Uw bedrijfsgegevens naar Excel exporteren
Als u met uw gegevens van [!INCLUDE[prod_short](includes/prod_short.md)] wilt werken in Excel, kunt u alle lijsten in Excel openen en er daar mee werken. Zo ook kunt u als u uw abonnement wilt annuleren voor [!INCLUDE[prod_short](includes/prod_short.md)], uw gegevens naar Excel exporteren zodat u deze mee kunt nemen.

## <a name="opening-lists-in-excel"></a>Lijsten openen in Excel
U kunt gegevens van elk dagboek, elke lijst of elk werkblad openen in Excel. U opent gewoon de gewenste pagina en kiest vervolgens **Openen in Excel**. Open bijvoorbeeld de lijst met klanten (zoek naar **Klanten**) en kies vervolgens **Openen in Excel**. Uw browser vraagt of u het gegenereerde Excel-werkboek wilt openen of opslaan.  

> [!NOTE]
> Gebruik deze optie wanneer u geen wijzigingen wilt aanbrengen en deze wijzigingen wilt terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)].  

Elke lijst bevat een aantal kolommen en de export naar Excel omvat alle kolommen die uw huidige weergave bevat. Als u kolommen wilt toevoegen of verwijderen voordat u de lijst in Excel opent, opent u gewoon het snelmenu voor elke kolom en geeft u vervolgens op welke kolommen u wilt bekijken. Deze lijst met kolommen is anders voor de meeste lijsten en geeft de structuur in de database weer waarin de gegevens zijn opgeslagen. Als u niet zeker weet welk type gegevens een bepaalde kolom bevat, kunt u het toevoegen aan uw weergave en vervolgens bepalen of u het opnieuw wilt verwijderen.  

### <a name="edit-data-in-excel"></a>Gegevens bewerken in Excel
Uw [!INCLUDE[prod_short](includes/prod_short.md)] ervaring bevat een invoegtoepassing voor Excel, zodat u gegevens in Excel kunt bewerken. Zie voor meer informatie [Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Gegevens exporteren naar andere financiële systemen
Als u besluit uw abonnement te annuleren voor [!INCLUDE[prod_short](includes/prod_short.md)], kunt u uw gegevens naar Excel exporteren en ze meenemen naar uw volgende financiële systeem.  

U kunt natuurlijk alle pagina's exporteren, maar dat is misschien meer dan u werkelijk nodig hebt. Overweeg daarom de volgende essentiële pagina's te exporteren en vergeet niet om alle kolommen toe te voegen, zoals eerder beschreven:  

* Rekeningschema  
* Klanten  
* Leveranc.  
* Banken  
* Artikelen  

Als u ook al uw financiële transacties wilt, gaat het om een grote hoeveelheid gegevens. De export ervan duurt vaak een aantal minuten. De financiële transacties worden weergegeven op de pagina **Grootboekposten**.  

Het wordt aanbevolen ook te overwegen om gegevens van de volgende pagina's te exporteren:  

* Klantenposten  
* Leveranciersposten  
* Bankposten  
* Artikelposten  
* Boekingsgroepinstellingen  
* Klantboekingsgroepen  
* Leveranciersboekingsgroepen  
* Artikelboekingsgroepen  
* Bankboekingsgroep  
* Grootboekbudgetten  
* Grootboekbudgetposten  
* Verkoopoffertes  
* Verkoopfacturen  
* Inkoopfacturen  
* Contacten  
* Verkopers  

> [!NOTE]  
> Als u meer dan één bedrijf in [!INCLUDE[prod_short](includes/prod_short.md)] hebt ingesteld, moet u de relevante gegevens van elk bedrijf exporteren.

> [!NOTE]
> U moet ten minste een van de volgende machtigingen hebben om gegevens in Excel te openen of te bewerken:
>    - Machtiging ingesteld *D365 Excel-exportactie*  
>    - Systeemmachtiging 6110 *Actie Exporteren naar Excel toestaan*.  

Zie voor meer informatie [Een overzicht krijgen van de machtigingen van een gebruiker](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
[Uw abonnement voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md) annuleren  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Financiën](finance.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]