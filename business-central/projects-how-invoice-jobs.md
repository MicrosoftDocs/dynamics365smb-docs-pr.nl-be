---
title: Een projectverkoopfactuur maken om een project te factureren
description: Beschrijft hoe u klanten factureert voor projectonkosten terwijl een project loopt en kosten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="invoice-jobs"></a>Projecten factureren

Tijdens het project kunnen projectkosten van resourceverbruik, materialen en aan het project gerelateerde inkopen, zich ophopen. Naarmate het project vordert, worden deze transacties geboekt in het projectdagboek. Het is van belang dat alle kosten worden vastgelegd in het projectdagboek voordat u het project aan de klant factureert.

> [!NOTE]
> U kunt ook externe resources aanschaffen die niet aan een project gerelateerd zijn, bijvoorbeeld om een leverancier te factureren voor het geleverde werk. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).

U kunt het hele project factureren vanuit de pagina **Projecttaakregels** of alleen de geselecteerde factureerbare regels factureren vanuit de pagina **Planningsregels**. Facturering kan plaatsvinden nadat het project is voltooid of op bepaalde intervallen tijdens de voortgang van het project op basis van een factureringsschema.

> [!NOTE]  
> Als u **Factureerbaar** selecteert in het veld **Regelsoort project** in de inkoopdocumenten voor aan het project gerelateerde inkopen, worden projectplanningsregels gemaakt die gereed zijn om te worden gefactureerd aan de klant. Zie [Projectvoorraden beheren](projects-how-manage-project-supplies.md) voor meer informatie.

U kunt ook een bedrijf factureren dat niet de eindklant is. Soms wijkt de partij waarvoor een project bestemd is, af van de partij die de rekening betaalt. Op de pagina **Taken** geeft u de klant die van het project profiteert op in de velden **Verkopen aan** en de te factureren partij in de velden **Factureren aan**. 

## <a name="to-create-multiple-job-sales-invoices"></a>Meerdere projectverkoopfacturen maken

U kunt een factuur maken voor een project of voor één of meer projecttaken voor een klant, wanneer ofwel het werk dat moet worden gefactureerd voltooid is ofwel de datum voor facturering op basis van een factureringsschema is bereikt.

In de volgende procedure wordt beschreven hoe u een batchverwerking gebruikt om meerdere projecten te factureren.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfactuur project maken** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Stel filters in als u de projecten wilt beperken die door de batchverwerking worden verwerkt.
4. Kies de knop **OK** om de facturen te maken.  

U kunt gemaakte facturen bekijken en boeken in het venster **Verkoopfacturen**.

> [!NOTE]
> U kunt ook een klant factureren door het project te selecteren en vervolgens de actie **Projectverkoopfactuur** maken te kiezen. 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a>Projectverkoopfacturen maken en boeken vanuit projectplanningsregels

U kunt een factuur maken vanuit een projectplanningsregel en op dat moment de hoeveelheid van het artikel, resource of grootboekrekening die u wilt factureren, aangeven.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open het betreffende project.
3. Selecteer een projecttaak waarvoor **Boeking** de **projecttaaksoort** is, en kies vervolgens de actie **Projectplanningsregels**.  
4. Voer op een projectplanningsregel in het veld **Aantal te verplaatsen naar factuur** de hoeveelheid van het artikel, de resource en het soort grootboekrekening dat u wilt factureren in.  
5. Kies de actie **Verkoopfactuur maken**.
6. Voer op de pagina **Verkoopfactuur project maken** de boekingsdatum in en of u een nieuwe factuur wilt maken of toevoegen aan deze factuur of aan een bestaande factuur.
7. Kies de knop **Ok**.  
8. Kies op de pagina **Projectplanningsregels** de actie **Verkoopfacturen/-creditnota's**.

    De pagina **Verkoopfactuur** wordt geopend met het aantal dat u naar de factuur hebt verzonden.
9. Breng eventuele aanvullende wijzigingen aan en kies vervolgens de actie **Boeken**.

> [!NOTE]  
>   De bovengenoemde procedure is soortgelijk voor het maken, controleren en boeken van een aan een project gerelateerde verkoopcreditnota.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/post-job-usage-sales/)

## <a name="see-also"></a>Zie ook

[Projecten beheren](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
