---
title: Verbruik of gebruik van projectresources en -artikelen registreren
description: In dit artikel wordt beschreven hoe u het verbruik of gebruik van artikelen of resources voor projecten registreert in projectbeheer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
---
# <a name="record-consumption-or-usage-for-jobs"></a>Verbruik of gebruik voor projecten registreren

Vanaf de pagina **Projectkaart** kunt u de pagina **Taakplanningsregels** openen om het gebruik van verschillende onderdelen van uw project te bekijken en vast te leggen. Deze informatie wordt automatisch bijgewerkt wanneer u informatie wijzigt en overdraagt tussen projecten en projectdagboeken of projectfacturen. Dit vereist dat u de optie **Gebruikslink standaard toepassen** inschakelt op de pagina **Projectinstellingen**. Meer informatie op [Projecten instellen](projects-how-setup-jobs.md).  

Zo kunt u bijvoorbeeld voor planningsregels van het type **Budget** de hoeveelheid van een resource invoeren en aangeven welke hoeveelheid moet worden overgebracht naar het projectdagboek. Als het type van de planningsregel **Factureerbaar** is, kunt u de hoeveelheid van de resource invoeren en aangeven welke hoeveelheid moet worden overgebracht naar een factuur. Zie voor meer informatie over het factureren van de klant [Projecten factureren](projects-how-invoice-jobs.md). Door de oorspronkelijke hoeveelheid, de resterende hoeveelheid of de geboekte hoeveelheid te vergelijken, kunt u snel gebruiksinformatie bekijken. Voor informatie over het inschatten van gebudgetteerde waarden tijdens planning raadpleegt u [Projectbudgetten beheren](projects-how-manage-budgets.md).  

In de volgende procedures wordt beschreven hoe u werkelijke (gebudgetteerde) hoeveelheden en kosten vastlegt met een projectjournaal. U kunt ook inkoopdocumenten gebruiken om de aankoop voor een project vast te leggen. Meer informatie op [Projectvoorraden beheren](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Gebruik vastleggen voor een projectplanningsregel van het soort Budget

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het project en kies vervolgens de actie **Projectplanningsregels**. 
3. Selecteer een projectplanningsregel van het soort **Budget** of het soort **Budget en factureerbaar** waarvoor u gebruik wilt vastleggen.   

    > [!NOTE]
    > U kunt ook gebruik vastleggen voor een projectplanningsregel van het soort **Factureerbaar**. Meestal gebruikt u deze regels om facturen te maken, maar u kunt de informatie ook overbrengen naar een journaal. Zie voor meer informatie [Projecten factureren](projects-how-invoice-jobs.md) 

4. In het veld **Aantal te verplaatsen naar dagboek** voert u het aantal in dat u wilt overbrengen. De standaardhoeveelheid is de waarde die u invoert in het veld **Aantal**.

    Het veld **Resterend aantal** bevat het resterende aantal om het project te voltooien en dat moet worden overgebracht naar het dagboek.
5. Kies de actie **Projectdagboekregels maken**.

    > [!TIP]
    > Als u meer taakplanningsregels voor deze taak gaat toevoegen, wacht dan met deze stap totdat u alle taakplanningsregels hebt toegevoegd.
6. Vul op de pagina **Projectplanningsregel taakoverdracht** de velden in zoals gewenst en kies vervolgens de knop **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Kies de actie **Projectdagboek openen**.  
8. Selecteer op de pagina **Projectdagboek** de relevante regel en kies vervolgens de actie **Boeken**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Bekijk op de pagina **Projectplanningsregels** het vastgelegde gebruik door te kijken naar de velden **Aantal**, **Resterend aantal** en **Aantal te verplaatsen naar dagboek**.  
10. Herhaal stap 3 tot en met 8 om aanvullend gebruik vast te leggen.  

## <a name="to-create-job-journal-lines-manually"></a>Handmatig projectdagboekregels maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectjournalen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in het veld **Batchnaam** een relevante projectdagboekbatch.  
3. Voer op een nieuwe regel documentnummer, projectnummer, projecttaaknummer, soort en aantal van het verbruikte soort in.  
4. Wanneer de projectdagboekregels zijn voltooid, kiest u de actie **Boeken**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Projectgebruikschattingen weergeven en updates boeken

U kunt in één stap het projectgebruik tot aan de voltooiing van een project bekijken. Hiervoor gebruikt u de batchverwerking **Project - Resterend gebruik berekenen** voor alle taken tot en met het einde van een project.  

Op deze manier kunt u uw oorspronkelijke schattingen volgen en vergelijken met de werkelijke resultaten en zo nodig wijzigingen aanbrengen of nieuwe posten maken. U hebt bijvoorbeeld mogelijk geschat dat een project 10 uur vereist en tot op heden zijn er al 15 uur aan besteed. U kunt de extra vijf uur aan de bestaande dagboekregel toevoegen of een nieuwe dagboekregel maken om deze vijf uur als overuren te rapporteren. Dit is een ander werksoort. De juiste kosten en prijzen worden berekend die vervolgens naar het dagboek kunnen worden geboekt.  

> [!NOTE]  
> Artikelposten maken artikeljournaalposten en verkleinen de voorraadhoeveelheid. De batchverwerking **Voorraadwaarde boeken** brengt de kosten van de voorraad over naar het grootboek. Resourceposten maken resourceposten.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectjournalen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een relevant projectdagboek en kies vervolgens de actie **Resterend gebruik berekenen**.  
3. Voer op de pagina **Project - Resterend gebruik berekenen** het documentnummer en de boekingsdatum in die in het dagboek moeten worden ingevoegd, en kies vervolgens de knop **OK**.  
4. Werk het dagboek bij met eventuele wijzigingen die nodig zijn.  
5. Kies de actie **Boeken**.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Voorraad- en magazijnpickdocumenten maken voor een project

Om voorraad- en magazijnpickdocumenten voor projecten te maken moet uw beheerder de **Functie-update: Voorraad- en magazijnpicks vanuit projecten inschakelen** op de pagina **Functiebeheer** inschakelen.

De functie voegt de acties **Voorraadpick maken** en **Magazijnpick maken** toe aan de **Projectkaart**. Om een pickdocument te maken of te registreren gebruikt u de acties **Opslag-/pick-/verplaatsingsregels** of **Geregistreerde pickregels**. Meer informatie op [Stromen voor productie, assemblage en projecten](design-details-internal-warehouse-flows.md).

U kunt de acties onder de volgende voorwaarden gebruiken:

* De **Status** van het project is **Open**.
* De **Regelsoort** van de taakplanningsregel is **Budget** of **Zowel Budget als Factureerbaar**.
* Het **Type** van de projectplanningsregel is **Artikel**.
* **Pick vereist** is ingeschakeld voor de gerelateerde locatie.
* **Gestuurde opslag en pick** is uitgeschakeld.

> [!NOTE] 
> Hoewel de instelling **Pick vereist** heet, kunt u het verbruik nog steeds rechtstreeks vanuit de projectdagboekregel voor de locatie boeken. Als voor uw vestiging wel pickverwerking maar geen verzendingsverwerking is ingesteld, gebruikt u de pagina **Voorraadpick** om de pickgegevens te beheren en af te drukken. U gebruikt de pagina ook om het resultaat van de pick in te voeren en te boeken, wat op zijn beurt het verbruik van de artikelen publiceert. 
> 
> Wanneer voor uw vestiging zowel pick- als verzendingsverwerking vereist is, wat wil zeggen dat u zowel het veld **Pick vereist** als het veld **Verzending vereist** hebt gekozen op de pagina **Vestiging**, gebruikt u de pagina **Magazijnpick** om de pick te verwerken. Magazijnpicks zijn vergelijkbaar met voorraadpicks. Het verschil is dat in plaats van de pickinformatie te boeken, u de pick registreert. Deze registratie boekt geen verbruik, maar maakt de artikelen alleen beschikbaar voor boeking. Als magazijnmanager kunt u met behulp van een pickvoorstel pickgegevens ordenen voordat de afzonderlijke magazijnpickinstructies worden gemaakt

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Planningsregels voor een projectpost controleren

Nadat u projectdagboekregels hebt geboekt, kunt u de planningsregels zien die zijn gekoppeld aan de projectdagboekposten die zijn geboekt.

> [!NOTE]  
> Hiervoor moet het selectievakje **Gebruikslink toepassen** zijn ingeschakeld voor het project. Zie [Projecten instellen](projects-how-setup-jobs.md) voor meer informatie.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectjournalen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een relevant projectdagboek en kies vervolgens de actie **Posten**.  
3. Kies op de pagina **Projectposten** de actie **Gekoppelde projectplanningsregels weergeven**.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/post-job-usage-sales/)

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
