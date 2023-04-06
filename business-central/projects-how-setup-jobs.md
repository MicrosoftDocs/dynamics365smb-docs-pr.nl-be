---
title: 'Projecten, prijzen en projectboekingsgroepen instellen'
description: 'Beschrijft hoe u algemene projectgegevens instelt en prijzen instelt voor projectartikelen, resources en grootboekrekeningen, en projectboekingsgroepen.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.date: 04/01/2021
ms.author: edupont
---
# Projecten, prijzen en projectboekingsgroepen instellen

Als projectmanager kunt u taken instellen die alle projecten definiëren die u beheert in [!INCLUDE[prod_short](includes/prod_short.md)]. Op de pagina **Projectinstellingen** moet u opgeven hoe u bepaalde functies wilt gebruiken.

Voor elk project kunt u afzonderlijke projectkaarten opgeven met informatie over prijzen voor projectartikelen, projectresources en projectgrootboekrekeningen, en u moet projectboekingsgroepen instellen.

## Algemene gegevens voor projecten instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> In het veld **Gebruikslink standaard toepassen** wordt aangegeven of projectposten standaard zijn gekoppeld aan projectplanningsregels. Kies het veld als u deze instelling wilt toepassen op alle nieuwe projecten die u maakt. U kunt het bijhouden van het projectgebruik voor een specifiek project in- of uitschakelen door de waarde van het veld **Gebruikslink toepassen** op de individuele taakkaart te wijzigen. De gevolgen worden in de volgende sectie uitgelegd.

### Bijhouden van projectgebruik instellen

Als u aan een project werkt, wilt u wellicht weten in hoeverre uw gebruik overeenkomt met uw plan. Om dit gemakkelijk te doen, kunt u een koppeling tussen het werkelijke verbruik en uw projectplanningsregels maken. Hiermee kunt u uw kosten bijhouden en gemakkelijk zien hoeveel werk nog moet worden gedaan. Standaard is het soort projectplanningsregel *Budget*, maar als u het regelsoort **Budget en factureerbaar** gebruikt, heeft dat een soortgelijk effect.

Als u het veld **Gebruikslink toepassen** inschakelt, kunt u gegevens op de projectplanningsregel controleren. U kunt de hoeveelheid van de resource, artikel of grootboekrekening instellen en vervolgens aangeven welke hoeveelheid u wilt overdragen naar het projectdagboek. Het veld **Resterend aantal** op de projectplanningsregel geeft aan wat nog moet worden overgebracht en geboekt naar het projectdagboek.

>[!NOTE]
> Als het selectievakje **Gebruikslink toepassen** voor de afzonderlijke opdracht is ingeschakeld en het veld **Regelsoort** op de journaalregel of inkoopregel *Factureerbaar* is, worden er nieuwe projectplanningregels van het type *Budget* gemaakt wanneer u het opdrachtjournaal of inkoopdocument boekt.  
> Zie voor meer informatie [Gebruik voor projecten vastleggen](projects-how-record-job-usage.md) en [Projectvoorraden beheren](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Als het veld **Regeltype** op de opdrachtjournaalregel of inkoopregel leeg is, worden er geen opdrachtplanningsregels aangemaakt wanneer u het opdrachtjournaal of inkoopdocument boekt.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## Prijzen instellen voor resources, artikelen en grootboekrekeningen voor projecten

> [!NOTE]
> In releasewave 2 van 2020 hebben we nieuwe processen uitgebracht voor het instellen en beheren van prijzen en kortingen. Als u een nieuwe klant bent, gebruikt u de nieuwe ervaring. Als u een bestaande klant bent, hangt of u de nieuwe ervaring gebruikt, af van de vraag of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd in **Functiebeheer**. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management).

U kunt prijzen instellen voor de artikelen, resources en grootboekrekeningen die gerelateerd zijn aan een project. 

#### [Huidige ervaring](#tab/current-experience)

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Resource**, **Artikel** of **Grootboekrekening**.
3. Vul op de pagina **Resourceprijzen project**, **Artikelprijzen project** of **GB-rekeningprijzen project** de velden zoals nodig in.

De volgende tabel laat zien hoe de informatie in de optionele velden wordt gebruikt op taakplanningsregels en dagboeken wanneer de resource, het artikel of de grootboekrekening voor het project wordt gekozen.

|Kolom1  |Kolom2  |
|---------|---------|
|**Projectresources**|De velden **Projecttaaknr.**, **Werksoort**, **Valutacode**, **Regelkorting %** en **Kostprijsfactor**. De waarde in het veld **Eenheidsprijs** wordt gebruikt op de projectplanningsregels en projectdagboeken wanneer deze resource, een resource die is toegewezen aan de resourcegroep of een andere resource wordt ingevoerd. Deze prijs komt altijd in de plaats van alle andere prijzen die eventueel zijn ingesteld op de bestaande pagina **Resourceverkoopprijs/Resourcegroepsprijs**.|
|**Projectartikelen**|De velden **Projecttaaknr.**, **Valutacode** en **Regelkorting %**. De waarde in het veld **Eenheidsprijs** voor het artikel wordt op de projectplanningsregels en in projectdagboeken gebruikt wanneer dit artikel wordt ingevoerd. Deze prijs komt altijd in plaats van de normale klantenprijs (het 'beste prijs'-mechanisme) voor artikelen. Als u de normale klantenprijsmechanismen wilt gebruiken, moet u geen projectartikelprijzen voor het project maken.|
|**Grootboekrekeningen**|De optionele informatie in de velden **Projecttaaknr.**, **Valutacode**, **Regelkorting %**, **Kostprijsfactor** en **Kostprijs** wordt gebruikt op de projectplanningsregels en in de projectdagboeken wanneer deze grootboekrekening wordt ingevoerd en wordt toegevoegd aan het project. De waarde in het veld **Kostprijs** voor de grootboekrekeningskosten wordt gebruikt op de projectplanningsregels en in de projectdagboeken wanneer deze grootboekrekening wordt ingevoerd.|

#### [Nieuwe ervaring](#tab/new-experience)

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Verkoopprijslijsten**.

---

## Projectboekingsgroepen instellen

Eén aspect van het plannen van projecten is bepalen welke boekingsrekeningen moeten worden gebruikt voor projectwaardering. Om projecten te kunnen boeken, moet u rekeningen instellen voor het boeken voor elke projectboekingsgroep. Een boekingsgroep vertegenwoordigt een koppeling tussen het project en de wijze waarop het moet worden behandeld in het grootboek. Wanneer u een project maakt, geeft u een boekingsgroep op en wordt elk project dat u voor de taak maakt standaard gekoppeld aan die boekingsgroep. Als u echter taken maakt, kunt u de standaardinstellingen overschrijven en een boekingsgroep selecteren die meer geschikt is.  

> [!NOTE]  
>   U moet de benodigde rekeningen in het rekeningschema instellen voordat u boekingsgroepen instelt. Voor meer informatie raadpleegt u [Het Rekeningschema instellen of wijzigen](finance-setup-chart-accounts.md).  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
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

## Zie gerelateerde [Microsoft-training](/training/paths/set-up-jobs-resources/)

## Zie ook

[Projectbeheer instellen](projects-setup-projects.md)  
[Video: Hoe u een project maakt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projecten beheren](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
