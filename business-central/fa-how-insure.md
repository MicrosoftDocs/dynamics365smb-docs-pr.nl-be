---
title: Vaste activa verzekeren
description: U kunt een of meer vaste activa toewijzen aan één verzekeringspolis door te boeken naar de verzekeringsdekkingsposten via de pagina **Verzekeringsdagboek**.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 06/29/2021
ms.author: edupont
---
# <a name="insure-fixed-assets"></a><a name="insure-fixed-assets"></a><a name="insure-fixed-assets"></a>Vaste activa verzekeren
Een verzekeringspolis voor een vast activum wordt vertegenwoordigd door een verzekeringskaart. U kunt één vast activum aan één verzekeringspolis toewijzen, maar u kunt ook meerdere vaste activa aan één verzekeringspolis toewijzen.

U wijst een vast activum toe aan een verzekeringspolis door te boeken naar de dekkingsposten via de pagina **Verzekeringsdagboek**.

Daarnaast kunt u een vast activum koppelen aan een verzekeringspolis en dekkingsposten maken wanneer u de bijbehorende aanschafkosten boekt. Dit doet u door de aanschafkosten vanuit het financieel dagboek voor vaste activa te boeken terwijl het veld **Verzekeringsnr.** is ingevuld. Het selectievakje **Autom. verzekering boeken** op de pagina **VA-instellingen** moet zijn ingeschakeld. Zie [De aanschaf van een vast activum handmatig boeken met het financieel dagboek voor vaste activa](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal) voor meer informatie.

Als het selectievakje **Autom. verzekering boeken** op de pagina **VA-instellingen** niet is ingeschakeld, worden door aanschaf te boeken in het financieel dagboek voor vaste activa, regels gemaakt op de pagina **Verzekeringsdagboek**. Deze moet u dan handmatig boeken.

> [!WARNING]  
>   Als u het selectievakje **Autom. verzekering boeken** niet inschakelt op de pagina **VA-instellingen**, moet uw verzekeringsdagboek op een dagboeksjabloon zonder een nummerreeks worden gebaseerd. Dit komt doordat de ingevoegde documentnummers van de dagboekregel voor vaste activa anders in strijd zijn met de nummerreeks van het verzekeringsdagboek. Zie [Algemene gegevens voor vaste activa instellen](fa-how-setup-general.md) voor meer informatie over dagboeksjablonen en -batches.

Nadat u een vast activum aan een verzekeringspolis hebt toegewezen, wordt het selectievakje **Verzekerd** ingeschakeld voor het vaste activum. Wanneer u het vaste activum verkoopt, wordt het selectievakje automatisch uitgeschakeld.

## <a name="to-create-or-modify-an-insurance-card"></a><a name="to-create-or-modify-an-insurance-card"></a><a name="to-create-or-modify-an-insurance-card"></a>Een verzekeringskaart maken of wijzigen
Een verzekeringspolis voor een vast activum moet worden vertegenwoordigd door een verzekeringskaart.

Als u informatie ontvangt over wijzigingen in het verzekerd bedrag, moet u de nieuwe informatie invoeren op de pagina **Verzekering**, zodat de polisdekking correct wordt geanalyseerd.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verzekering** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuwe kaart voor een verzekeringspolis te maken. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. U kunt ook de verzekeringspolis selecteren die u wilt wijzigen en vervolgens de actie **Bewerken** kiezen.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a><a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a><a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>Een vast activum toewijzen aan een verzekeringspolis door het vanuit een verzekeringsdagboek te boeken
U wijst een vast activum aan een verzekeringspolis toe door het naar de verzekeringsdekking te boeken.  

In de volgende procedure wordt uitgelegd hoe u een verzekeringsdagboekregel handmatig maakt. Als het selectievakje **Autom. verzekering boeken** op de pagina **VA-instellingen** is ingeschakeld, worden er automatisch verzekeringsdagboekregels gemaakt wanneer u aanschafkosten boekt. In dat geval hoeft u alleen het dagboek te boeken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verzekeringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open het relevante dagboek en vul indien nodig de dagboekregels in.  
3. Als u meerdere vaste activa wilt toewijzen aan één verzekeringspolis, maakt u dagboekregels met dezelfde waarde in het veld **Verzekeringsnr.** en verschillende waarden in het veld **VA-nr.**  
4. Kies de actie **Boeken**.  

    > [!NOTE]  
    >   De posten uit een verzekeringsdagboek worden uitsluitend naar dekkingsposten geboekt.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a><a name="to-update-the-insurance-value-of-a-fixed-asset"></a><a name="to-update-the-insurance-value-of-a-fixed-asset"></a>De verzekeringswaarde van een vast activum bijwerken
Met de batchverwerking **Verzekering indexeren** kunt u de waarde wijzigen van de vaste activa die onder de dekking vallen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzekering indexeren** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in.

    > [!NOTE]  
    >   Voer in het veld **Indexcijfer** een afname van 5% in, bijvoorbeeld als 95 terwijl u een toename van 2% als 102 invoert.  
3. Kies de knop **Ok**.  

   Met de batchverwerking wordt het nieuwe bedrag als een percentage van de totale verzekerde waarde berekend, zoals vermeld op de pagina **Verzekeringsstatistiek**, en vervolgens wordt een regel in het verzekeringsdagboek gemaakt.  
4. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verzekeringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
5. Open het relevante verzekeringsdagboek, controleer de gemaakte waarden en boek deze naar de dekkingsposten.  

## <a name="to-monitor-insurance-coverage"></a><a name="to-monitor-insurance-coverage"></a><a name="to-monitor-insurance-coverage"></a>Verzekeringsdekking controleren
[!INCLUDE[prod_short](includes/prod_short.md)] bevat bepaalde rapporten en statistiekpagina's voor gebruik bij het analyseren van verzekeringspolissen en om te controleren of uw vaste activa onder- of oververzekerd zijn.  

### <a name="overview-of-insurance-policies"></a><a name="overview-of-insurance-policies"></a><a name="overview-of-insurance-policies"></a>Overzicht van verzekeringspolissen
Om een overzicht van uw verzekeringspolissen te verkrijgen bekijkt u een voorbeeld van het rapport **Verzekering - Lijst** of drukt u het af. Het rapport bevat alle polissen en de belangrijkste velden van de verzekeringskaarten.  

### <a name="insurance-coverage"></a><a name="insurance-coverage"></a><a name="insurance-coverage"></a>Verzekeringsdekking
Om te zien welke verzekeringspolissen elk activum dekken en met welk bedrag, kunt u een voorbeeld bekijken van het rapport **Verzekering - Tot. verzekerde waarde** of het rapport afdrukken.  

### <a name="overunder-coverage"></a><a name="overunder-coverage"></a><a name="overunder-coverage"></a>Over-/onderverzekering
U kunt op de volgende manieren controleren of vaste activa onder- of oververzekerd zijn:  

* De pagina **Verzekeringsstatistiek**. Een positief bedrag in het veld **Over-/onderverzekerd** betekent dat het vaste activum oververzekerd is. Een negatief bedrag betekent dat het activum onderverzekerd is.  
* De pagina **VA-statistiek**. Kies het veld **Tot. verzekerde waarde** om de pagina **Verzekeringsdekkingsposten** te bekijken.  
* Het rapport **Over-/onderverzekering**.  
* Het rapport **Verzekering - Analyse**.  

### <a name="uninsured-fixed-assets"></a><a name="uninsured-fixed-assets"></a><a name="uninsured-fixed-assets"></a>Onverzekerde vaste activa
U kunt controleren of u niet bent vergeten om een vast activum toe te wijzen aan een verzekeringspolis door het rapport **Verzekering - Onverzekerde VA** af te drukken of er een voorbeeld van te bekijken. In dit rapport worden vaste activa weergegeven waarvoor nog geen bedragen naar de verzekeringsdekking zijn geboekt.  

## <a name="to-view-insurance-coverage-ledger-entries"></a><a name="to-view-insurance-coverage-ledger-entries"></a><a name="to-view-insurance-coverage-ledger-entries"></a>Verzekeringsdekkingsposten bekijken
Het is mogelijk om de posten te bekijken die u hebt gemaakt in de dekkingsposten.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verzekering** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de betreffende verzekeringspolis en kies vervolgens de actie **Verzekeringsdekkingsposten**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a><a name="to-view-the-total-insurance-value-of-fixed-assets"></a><a name="to-view-the-total-insurance-value-of-fixed-assets"></a>De totale verzekerde waarde van vaste activa bekijken
In een speciale matrixpagina worden de verzekeringswaarden weergegeven die voor elke verzekeringspolis zijn geregistreerd voor elk vast activum als een resultaat van verzekeringsgerelateerde bedragen die u hebt geboekt.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verzekering** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de betreffende verzekeringspolis en kies vervolgens de actie **Totale verzekerde waarde per VA**.  
3. Vul indien nodig de velden in.  
4. Kies de actie **Matrix weergeven**.  
5. Als u de onderliggende verzekeringsdekkingsposten wilt zien, kiest u een waarde in de matrix.  

## <a name="to-correct-insurance-coverage-entries"></a><a name="to-correct-insurance-coverage-entries"></a><a name="to-correct-insurance-coverage-entries"></a>Dekkingsposten corrigeren
Als een vast activum is gekoppeld aan de verkeerde verzekeringspolis, kunt u dit corrigeren door twee herindelingsposten in het verzekeringsdagboek te maken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verzekeringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Maak één dagboekregel voor een vast activum en de juiste verzekeringspolis waarvoor de waarde in het veld **Bedrag** positief is.  
3. Maak een andere dagboekregel voor het vaste activum en de onjuiste verzekeringspolis waarvoor de waarde in het veld **Bedrag** negatief is.  
4. Kies de actie **Boeken**.  

Het vaste activum wordt losgekoppeld van de foutieve verzekeringspolis op de tweede regel, en gekoppeld aan de juiste verzekeringspolis op de eerste regel.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook
[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
