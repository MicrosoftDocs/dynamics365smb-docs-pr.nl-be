---
title: Uw Business Central-gegevens exporteren naar Excel
description: U kunt uw financiële rapporten en bedrijfsinformatiegegevens uit Business Central exporteren naar Excel of uw gegevens in Excel openen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: '9901,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---
# <a name="export-your-business-data-to-excel"></a>Uw bedrijfsgegevens exporteren naar Excel

Excel is een krachtig hulpmiddel om met gegevens te werken. Vanuit [!INCLUDE[prod_short](includes/prod_short.md)] kunt u elke lijst in Excel openen. U kunt zelfs gegevens in Excel wijzigen en deze vervolgens terugsturen naar [!INCLUDE [prod_short](includes/prod_short.md)]. Met dezelfde mogelijkheid kunt u uw gegevens gemakkelijk meenemen als u besluit uw abonnement op te zeggen.

## <a name="opening-lists-in-excel"></a>Lijsten openen in Excel

U kunt gegevens van elk dagboek, elke lijst of elk werkblad openen in Excel. U opent gewoon de gewenste pagina en kiest vervolgens **Openen in Excel**. Open bijvoorbeeld de lijst met klanten (zoek naar **Klanten**) en kies vervolgens **Openen in Excel**. Uw browser vraagt of u het gegenereerde Excel-werkboek wilt openen of opslaan.  

> [!NOTE]
> Gebruik deze optie als u uw wijzigingen niet wilt publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)].  

Elke lijst bevat enkele kolommen. De export naar Excel bevat alle kolommen die zich in uw huidige weergave bevinden. Wijzig de kolommen door het snelmenu voor elke kolom te openen en vervolgens op te geven welke kolommen u wilt zien. De lijst met kolommen is voor de meeste lijsten anders. De kolommen weerspiegelen de structuur in de database waarin uw gegevens zijn opgeslagen. Als u niet zeker weet welk type gegevens een bepaalde kolom bevat, voegt u deze toe aan uw weergave. U kunt het altijd weer verwijderen.  

### <a name="edit-data-in-excel"></a>Gegevens bewerken in Excel

Uw [!INCLUDE[prod_short](includes/prod_short.md)] ervaring bevat een invoegtoepassing voor Excel, zodat u gegevens in Excel kunt bewerken. Zie voor meer informatie [Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Gegevens exporteren naar andere financiële systemen

Als u besluit uw abonnement te annuleren voor [!INCLUDE[prod_short](includes/prod_short.md)], kunt u uw gegevens naar Excel exporteren en ze meenemen naar uw volgende financiële systeem.  

U kunt alle pagina's exporteren, maar dat is misschien meer dan u werkelijk nodig hebt. Overweeg daarom de volgende essentiële pagina's te exporteren en vergeet niet om alle kolommen toe te voegen:  

* Rekeningschema  
* Klanten  
* Leveranc.  
* Banken  
* Artikelen  

Als u al uw financiële transacties wilt exporteren, gaat het om een grote hoeveelheid gegevens. De export ervan duurt dus vaak meer dan een aantal minuten. De financiële transacties worden weergegeven op de pagina **Grootboekposten**.  

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
>
> * Machtiging ingesteld *D365 Excel-exportactie*  
> * Systeemmachtiging 6110 *Actie Exporteren naar Excel toestaan*.  

Zie voor meer informatie [Een overzicht krijgen van de machtigingen van een gebruiker](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).

## <a name="see-also"></a>Zie ook

[Uw abonnement voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md) annuleren  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Financiën](finance.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
