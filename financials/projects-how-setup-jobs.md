---
title: Projectprijzen en projectboekingsgroepen instellen| Microsoft Docs
description: Beschrijft hoe u algemene projectgegevens instelt en prijzen instelt voor projectartikelen, resources en grootboekrekeningen, en projectboekingsgroepen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b0e8a73af6f979cb426db1bffc34d154fc439dce
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-jobs"></a>Procedure: projecten instellen
In het venster **Projectinstellingen** moet u opgeven hoe u bepaalde functies wilt gebruiken.

Op de afzonderlijke projectkaarten moet u prijzen instellen voor projectartikelen, projectresources en projectgrootboekrekeningen, en u moet projectboekingsgroepen instellen.

## <a name="to-set-general-information-for-jobs"></a>Algemene gegevens voor projecten instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectinstellingen** in en klik vervolgens op de gerelateerde koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Het selectievakje **Gebruikslink toepassen** is tamelijk complex en wordt daarom in het volgende gedeelte uitgelegd.

## <a name="to-set-up-job-usage-tracking"></a>Bijhouden van projectgebruik instellen
Als u een project uitvoert, wilt u wellicht weten in hoeverre uw gebruik overeenkomt met uw plan. Om dit gemakkelijk te doen, kunt u een koppeling tussen het werkelijke verbruik en uw projectplanningsregels maken. Hiermee kunt u uw kosten bijhouden en gemakkelijk zien hoeveel werk nog moet worden gedaan. Standaard is het soort projectplanningsregel **Budget**, maar als u het regelsoort **Budget en factureerbaar** gebruikt, heeft dat een soortgelijk effect.

Als u het selectievakje **Gebruikslink toepassen** inschakelt, kunt u gegevens op de projectplanningsregel controleren. U kunt de hoeveelheid van de resource, artikel of grootboekrekening instellen en vervolgens aangeven welke hoeveelheid u wilt overdragen naar het projectdagboek. Het veld **Resterend aantal** op de projectplanningsregel geeft aan wat nog moet worden overgebracht en geboekt naar het projectdagboek.

Wanneer het selectievakje **Gebruikslink toepassen** is ingeschakeld en het soort projectplanningsregel **Factureerbaar** is, wordt in Financials een projectplanningsregel van het soort **Budget** gemaakt nadat u de dagboekregel hebt geboekt.

> [!NOTE]  
>   Als het selectievakje **Gebruikslink toepassen** op de projectkaart is ingeschakeld, en het veld **Regelsoort** op de projectdagboekregel leeg is, worden er nieuwe projectplanningregels van het type **Budget** gemaakt wanneer u journaalregels voor het project boekt. Als het selectievakje **Gebruikslink toepassen** op de projectkaart niet is ingeschakeld, en het veld **Regelsoort** op de projectdagboekregel leeg is, worden er geen nieuwe taakplanningregels gemaakt wanneer u journaalregels voor het project boekt. Zie voor meer informatie [Procedure: Gebruik vastleggen voor projecten](projects-how-record-job-usage.md).

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectinstellingen** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer of deselecteer **Gebruikslink toepassen**.

> [!NOTE]  
>   U kunt een andere instelling van het selectievakje **Gebruikslink toepassen** kiezen op de afzonderlijke projectkaarten. In dat geval heeft de instelling voor dat project voorrang op de hierboven beschreven algemene standaard.

## <a name="to-set-up-prices-for-job-resources"></a>Prijzen instellen voor projectresources
U kunt specifieke prijzen voor resources instellen voor een project. Gebruik hiervoor het venster **Resourceprijzen voor project**.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Resource**.
3. Vul in het venster **Resourceprijzen project** indien nodig de velden in.

De optionele informatie in de velden **Projecttaaknr.**, **Werksoort**, **Valutacode**, **Regelkorting %** en **Kostprijsfactor** wordt gebruikt op de projectplanningsregels en in de gebruiksdagboeken wanneer deze resource wordt ingevoerd en wordt toegevoegd aan het project.  

De waarde in het veld **Eenheidsprijs** wordt gebruikt op de projectplanningsregels en projectdagboeken wanneer deze resource, een resource die is toegewezen aan de resourcegroep of een andere resource wordt ingevoerd.  

> [!NOTE]  
>   Deze prijs komt altijd in de plaats van alle prijzen in het bestaande venster **Resourceverkoopprijs/Resourcegroepsprijs**.

## <a name="to-set-up-prices-for-job-items"></a>Prijzen instellen voor projectartikelen
U kunt specifieke prijzen voor artikelen instellen voor een project. Gebruik hiervoor het venster **Artikelprijzen project**.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Artikel**.
3. Vul in het venster **Artikelprijzen project** indien nodig de velden in.

De optionele informatie in de velden **Projecttaaknr.**, **Valutacode** en **Regelkorting %** wordt gebruikt op de projectplanningsregels en in de projectdagboeken wanneer dit artikel wordt ingevoerd of wordt toegevoegd aan het project.  

De waarde in het veld **Eenheidsprijs** voor het artikel wordt op de projectplanningsregels en in projectdagboeken gebruikt wanneer dit artikel wordt ingevoerd.  

> [!NOTE]  
>   Deze prijs komt altijd in de plaats van de normale klantenprijs (het 'beste prijs'-mechanisme) voor artikelen. Als u de normale klantenprijsmechanismen wilt gebruiken, moet u geen projectartikelprijzen voor het project maken.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Prijzen instellen voor GB-rekeningen voor een project
U kunt specifieke prijzen instellen voor grootboekkosten voor een project. U kunt hiervoor het venster **GB-rekeningprijzen project** gebruiken.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Grootboekrekening**.  
3. Vul in het venster **GB-rekeningprijzen project** indien nodig de velden in.

De optionele informatie in de velden **Projecttaaknr.**, **Valutacode**, **Regelkorting %**, **Kostprijsfactor** en **Kostprijs** wordt gebruikt op de projectplanningsregels en in de projectdagboeken wanneer deze grootboekrekening wordt ingevoerd en wordt toegevoegd aan het project.  

De waarde in het veld **Kostprijs** voor de grootboekrekeningskosten wordt gebruikt op de projectplanningsregels en in de projectdagboeken wanneer deze grootboekrekening wordt ingevoerd.

## <a name="to-set-up-job-posting-groups"></a>Projectboekingsgroepen instellen
Eén aspect van het plannen van projecten is bepalen welke boekingsrekeningen moeten worden gebruikt voor projectwaardering. Om projecten te kunnen boeken, moet u rekeningen instellen voor het boeken voor elke projectboekingsgroep. Een boekingsgroep vertegenwoordigt een koppeling tussen het project en de wijze waarop het moet worden behandeld in het grootboek. Wanneer u een project maakt, geeft u een boekingsgroep op en wordt elk project dat u voor de taak maakt standaard gekoppeld aan die boekingsgroep. Als u echter taken maakt, kunt u de standaardinstellingen overschrijven en een boekingsgroep selecteren die meer geschikt is.  

> [!NOTE]  
>   U moet de benodigde rekeningen in het rekeningschema instellen voordat u boekingsgroepen instelt. Voor meer informatie raadpleegt u [Het Rekeningschema instellen of wijzigen](finance-setup-chart-accounts.md).  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectboekingsgroepen** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul de accountvelden in zoals is beschreven in de volgende tabel.  

| Het veld Rekeningnr. | Omschrijving |
| --- | --- |
| **Code** |Een code voor de boekingsgroep. U kunt maximaal 10 tekens inclusief spaties invoeren. |
| **Rekening OHW-kosten** |De OHW-rekening voor de berekende kosten van het OHW van het project is een financiële activarekening op de balans. |
| **Rekening te betalen OHW-kosten** |Een rekening voor de Kostprijs- of Kostprijs van omzet-methode van OHW-berekening die een rekening voor te betalen kosten op de balans is. Hierop wordt geboekt wanneer de herwaardering van OHW vereist dat gebruikskosten die worden geboekt op de resultatenrekening worden verhoogd. |
| **Rekening vereffende projectkosten** |Een tegenrekening voor de rekening OHW-kosten, die een tegenhanger is voor een negatieve kostenrekening. |
| **Account toegepaste artikelkosten** |Een tegenrekening voor de rekening OHW-kosten, die een tegenhanger is voor een negatieve kostenrekening. |
| **Account toegepaste resourcekosten** |Een tegenrekening voor de rekening OHW-kosten, die een tegenhanger is voor een negatieve kostenrekening. |
| **Rekening kosten vereffend** |Een tegenrekening voor de rekening OHW-kosten, die een tegenhanger is voor een negatieve kostenrekening. |
| **Rekening herwaardering projectkosten** |De tegenrekening voor de rekening te betalen OHW-kosten, die een kostenrekening is. |
| **Kostenrekening GB (budget)** |De omzetrekening die moet worden gebruikt voor grootboekkosten in projecttaken met deze boekingsgroep. Indien dit leeg wordt gelaten, wordt de grootboekrekening gebruikt die op de projectplanningsregel staat. |
| **Rekening te realiseren omzet OHW** |De OHW-rekening voor de berekende kostprijs van het OHW, die een rekening voor te realiseren omzet op de balans is. Hierop wordt geboekt wanneer de herwaardering van OHW vereist dat de verantwoorde omzet wordt verhoogd. |
| **Rekening gefactureerde omzet OHW** |De rekening voor de gefactureerde verkoopprijs van het OHW die niet kan worden verantwoord. Het is een rekening voor niet-gerealiseerde omzet op de balans. |
| **Rekening projectomzetvereffening** |De tegenrekening voor de rekening gefactureerde omzet OHW, die een creditresultatenrekening is. |
| **Rekening projectomzetwaardering** |De tegenrekening voor de OHW-omzetrekening, die een resultatenrekening is. |
| **Rekening verantwoorde kosten** |De kostenrekening die de verantwoorde kosten voor het project bevat. Dit is normaliter een debetkostenrekening. |
| **Rekening verantwoorde omzet** |De resultatenrekening die de verantwoorde resultaten voor het project bevat. Dit is normaliter een creditresultatenrekening. |

## <a name="see-also"></a>Zie ook
[Projectbeheer instellen](projects-setup-projects.md)  
[Projecten beheren](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)      
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

