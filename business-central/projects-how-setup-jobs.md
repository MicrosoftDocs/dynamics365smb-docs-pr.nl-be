---
title: 'Projecten, prijzen en projectboekingsgroepen instellen'
description: Beschrijft hoe u algemene informatie over taken instelt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Projecten, prijzen en projectboekingsgroepen instellen

Als projectmanager kunt u taken instellen die alle projecten definiëren die u beheert in [!INCLUDE[prod_short](includes/prod_short.md)]. Gebruik de pagina **Projectinstellingen** om te definiëren hoe u projectfuncties gaat gebruiken.

Geef voor elk project verschillende informatie op:

* Prijzen voor projectartikelen
* Projectresources
* Projectgrootboekrekeningen
* Projectboekingsgroepen (vereist)

## <a name="to-set-general-information-for-jobs"></a>Algemene gegevens voor projecten instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Met de schakelaar **Gebruikslink standaard toepassen** op de pagina **Projectinstellingen** wordt aangegeven of projectposten standaard zijn gekoppeld aan projectplanningsregels. Schakel de schakelaar in om deze instelling toe te passen op alle nieuwe projecten. U kunt het bijhouden van het projectgebruik voor een specifiek project in- of uitschakelen door de schakelaar **Gebruikslink toepassen** op de pagina **Projectkaart** aan of uit te zetten.

### <a name="to-set-up-job-usage-tracking"></a>Bijhouden van projectgebruik instellen

Als u aan een project werkt, wilt u wellicht weten in hoeverre uw gebruik overeenkomt met uw plan. Om gebruik te verkennen kunt u een koppeling tussen uw projectplanningsregels en het werkelijke verbruik maken. Met de koppeling kunt u uw kosten volgen en begrijpen hoeveel werk er nog is. Standaard is het soort projectplanningsregel **Budget**, maar als u het regelsoort **Budget en factureerbaar** gebruikt, heeft dat een soortgelijk effect.

Als u de schakelaar **Gebruikslink standaard toepassen** inschakelt, kunt u gegevens op de projectplanningsregel controleren. U kunt bijvoorbeeld het aantal van de resource, het artikel of de grootboekrekening instellen. U kunt ook de hoeveelheid instellen die u wilt overbrengen naar het projectdagboek. Het veld **Resterend aantal** op de projectplanningsregel toont wat nog moet worden overgebracht en geboekt naar het projectdagboek.

>[!NOTE]
> Als het selectievakje **Gebruikslink toepassen** voor het project is ingeschakeld en het veld **Regelsoort** op de projectdagboekregel of inkoopregel **Factureerbaar** is, worden er nieuwe projectplanningregels van het type **Budget en factureerbaar** gemaakt wanneer u het projectdagboek of inkoopdocument boekt.  
>
> Zie voor meer informatie [Gebruik voor projecten vastleggen](projects-how-record-job-usage.md) en [Projectvoorraden beheren](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Als u geen waarde opgeeft in het veld **Regelsoort** op de projectdagboekregel of inkoopregel, worden er geen projectplanningsregels gemaakt wanneer u het projectdagboek of inkoopdocument boekt.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Prijzen instellen voor resources, artikelen en grootboekrekeningen voor projecten

> [!NOTE]
> In releasewave 2 van 2020 hebben we nieuwe processen uitgebracht voor het instellen en beheren van prijzen en kortingen. Als u een nieuwe klant bent, gebruikt u de nieuwe ervaring. Als u een bestaande klant bent, hangt of u de nieuwe ervaring gebruikt, af van de vraag of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd in **Functiebeheer**. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management).

U kunt prijzen instellen voor de artikelen, resources en grootboekrekeningen die gerelateerd zijn aan een project. 

#### [Huidige ervaring](#tab/current-experience)

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Resource**, **Artikel** of **Grootboekrekening**.
3. Vul op de pagina **Resourceprijzen project**, **Artikelprijzen project** of **GB-rekeningprijzen project** de velden zoals nodig in.

Wanneer u een resource, artikel of grootboekrekening voor een project kiest, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] informatie in de optionele velden op projectplanningsregels en projectdagboeken. In de volgende tabel wordt uitgelegd hoe.

|Kolom1  |Kolom2  |
|---------|---------|
|**Projectresources**|De velden **Projecttaaknr.**, **Werksoort**, **Valutacode**, **Regelkorting %** en **Kostprijsfactor**. De waarde in het veld **Eenheidsprijs** wordt voor de resource gebruikt op projectplanningsregels en projectdagboeken wanneer u een resource invoert of een resource die is toegewezen aan de resourcegroep. Deze prijs overschrijft de prijzen die zijn opgegeven op de pagina **Resourceverkoopprijs/Resourcegroepsprijs**.|
|**Projectartikelen**|De velden **Projecttaaknr.**, **Valutacode** en **Regelkorting %**. De waarde in het veld **Eenheidsprijs** voor het artikel wordt op de projectplanningsregels en in projectdagboeken gebruikt wanneer dit artikel wordt ingevoerd. Deze prijs overschrijft de normale klantenprijs (het 'beste prijs'-mechanisme) voor artikelen. Als u de normale klantenprijs wilt gebruiken, geeft u geen projectartikelprijzen op voor het project.|
|**Grootboekrekeningen**|De optionele informatie in de velden **Projecttaaknr.**, **Valutacode**, **Regelkorting %**, **Kostprijsfactor** en **Kostprijs** wordt gebruikt op de projectplanningsregels en in de projectdagboeken wanneer deze grootboekrekening wordt ingevoerd en wordt toegevoegd aan het project. Wanneer u een grootboekrekening kiest, gebruiken projectplanningsregels en projectdagboeken de waarde in het veld **Kostprijs** voor de grootboekkosten.|

#### [Nieuwe ervaring](#tab/new-experience)

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Verkoopprijslijsten**.

---

## <a name="to-set-up-job-posting-groups"></a>Projectboekingsgroepen instellen

Eén aspect van het plannen van projecten is bepalen welke boekingsrekeningen moeten worden gebruikt voor projectwaardering. Om projecten te kunnen boeken, moet u rekeningen instellen voor het boeken voor elke projectboekingsgroep. Een boekingsgroep vertegenwoordigt een koppeling tussen het project en de wijze waarop het moet worden behandeld in het grootboek. Wanneer u een project maakt, geeft u een boekingsgroep op en wordt elk project dat u voor de taak maakt standaard gekoppeld aan die boekingsgroep. Als u echter taken maakt, kunt u de standaardinstellingen overschrijven en een boekingsgroep selecteren die meer geschikt is.  

> [!NOTE]  
> U moet rekeningen instellen in het rekeningschema voordat u boekingsgroepen instelt. Voor meer informatie raadpleegt u [Het Rekeningschema instellen of wijzigen](finance-setup-chart-accounts.md).  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

| Het veld Rekeningnr. | Omschrijving | Gebruikt in OHW-type |
| --- | --- |  --- |
| **Code** |Een ID voor de boekingsgroep. U kunt maximaal 10 tekens inclusief spaties invoeren. | |
| **Rekening OHW-kosten** |De OHW-rekening voor de berekende kosten van het OHW van het project is een financiële activarekening op de balans. | Toegepaste kosten, Verantwoorde kosten|
| **Rekening te betalen OHW-kosten** |Een rekening voor de methode Kostprijs of Verkoopprijs van OHW-berekening. Deze rekening is voor te betalen kosten op de balans. Wanneer u door een OHW-aanpassing de gebruikskosten moet verhogen die u op uw resultatenrekening boekt, boekt u op deze rekening. | Te betalen kosten|
| **Rekening vereffende projectkosten** |Een tegenrekening voor de rekening OHW-kosten, die een tegenhanger is voor een negatieve kostenrekening. Gebruikt wanneer **Gebruikte boekingsmethode OHW** is ingesteld op *Taak*. | Toegepaste kosten, Verantwoorde kosten|
| **Account toegepaste artikelkosten** |Hetzelfde als **Rekening vereffende projectkosten**, maar gebruikt wanneer **Gebruikte boekingsmethode OHW** is ingesteld op *Projectpost*.| |
| **Account toegepaste resourcekosten** |Hetzelfde als **Rekening vereffende projectkosten**, maar gebruikt wanneer **Gebruikte boekingsmethode OHW** is ingesteld op *Projectpost*.| |
| **Account toegepaste grootboekkosten** |Hetzelfde als **Rekening vereffende projectkosten**, maar gebruikt wanneer **Gebruikte boekingsmethode OHW** is ingesteld op *Projectpost*.| |
| **Projectkostenwaarderingsrekening** |De tegenrekening voor de rekening te betalen OHW-kosten, die een kostenrekening is. | Te betalen kosten|
| **Kostenrekening GB (budget)** |De omzetrekening die moet worden gebruikt voor grootboekkosten in projecttaken met deze boekingsgroep. Indien dit leeg wordt gelaten, wordt de grootboekrekening gebruikt die op de projectplanningsregel staat. | |
| **Rekening te realiseren omzet OHW** |De OHW-rekening voor de berekende kostprijs van het OHW, die een rekening voor te realiseren omzet op de balans is. Wanneer een herwaardering van OHW vereist dat u de verantwoorde omzet verhoogt die u naar deze rekening boekt. | Te ontvangen verkoop, Verantwoorde verkoop|
| **Rekening gefactureerde omzet OHW** |De rekening voor de gefactureerde verkoopprijs van het OHW die niet kan worden verantwoord. Het is een rekening voor niet-gerealiseerde omzet op de balans. | Verantwoorde verkoop, Toegepaste verkoop|
| **Rekening projectomzetvereffening** |De tegenrekening voor de rekening gefactureerde omzet OHW, die een creditresultatenrekening is. | Toegepaste verkoop, Verantwoorde verkoop|
| **Rekening projectomzetwaardering** |De tegenrekening voor de OHW-omzetrekening, die een resultatenrekening is. | Te ontvangen omzet|
| **Rekening verantwoorde kosten** |De kostenrekening die de verantwoorde kosten voor het project bevat. Dit is normaliter een debetkostenrekening. | Verantwoorde kosten|
| **Rekening verantwoorde omzet** |De resultatenrekening die de verantwoorde resultaten voor het project bevat. Dit is normaliter een creditresultatenrekening. | Verantwoorde verkoop|

## <a name="see-also"></a>Zie ook

[Projectbeheer instellen](projects-setup-projects.md)  
[Video: Hoe u een project maakt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projecten beheren](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
