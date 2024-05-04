---
title: Gegevens analyseren per dimensie
description: In dit artikel wordt beschreven hoe u bedrijfsgegevens per dimensie kunt analyseren om meer inzicht in uw bedrijf te krijgen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="analyze-data-by-dimensions"></a>Gegevens analyseren per dimensie

In financiële analyses is een dimensie informatie die u toevoegt aan een post als een soort markering om posten met vergelijkbare kenmerken te groeperen. Dimensies groeperen bijvoorbeeld vaak vermeldingen voor klanten, regio's, producten en verkopers. Met de groepen kunt u eenvoudig gegevens erover ophalen voor analyse. U kunt dimensies gebruiken voor posten in dagboeken, documenten en budgetten.

Elke dimensie beschrijft de focus van de analyse. Een tweedimensionale analyse is bijvoorbeeld verkoop per gebied. Door bij het maken van een boeking meer dan twee dimensies te gebruiken, kunt u een complexere analyse uitvoeren. Een voorbeeld van een complexe analyse is het verkennen van de verkoop per verkoopcampagne per klantengroep per gebied. Zo krijgt u een beter inzicht in uw bedrijf, zoals hoe goed uw bedrijf draait, waar de zaken floreren en waar juist niet en waar meer resources moeten worden ingezet. Dat inzicht helpt u beter gefundeerde zakelijke beslissingen te nemen. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

> [!TIP]
> Als snelle manier om transactiegegevens te analyseren per dimensie kunt u totalen in het rekeningschema (COA) en posten op de pagina's **Posten** filteren op dimensie. Zoek de actie **Dimensiefilter instellen**.

> [!NOTE]
> Als u ontdekt dat een onjuiste dimensiewaarde is gebruikt voor geboekte grootboekposten, kunt u deze corrigeren en uw analyseweergaven bijwerken. Ga voor meer informatie naar [Problemen met dimensies oplossen en dimensies corrigeren](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view"></a>Een analyseweergave instellen

Met een analyse per dimensies geeft u een geselecteerde combinatie van dimensies weer. U kunt die dimensieset opslaan, ophalen en bijwerken door een **Analyseweergave** kaart te maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Analyseweergaven** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Analyseweergaveoverzicht** de actie **Nieuw**.
3. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u andere dimensiecodes wilt toevoegen naast de vier op het sneltabblad **Dimensies**, kiest u de actie **Filteren**, vult u de velden in en kiest u de knop **OK**.  
5. Als u de weergave wilt bijwerken, kiest u de actie **Bijwerken**.

## <a name="analyze-by-dimensions"></a>Analyseren per dimensie

Gebruik analyseweergaven die u al hebt ingesteld met de matrix **Analyse per dimensie** om de bedragen in uw grootboek te bekijken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Analyseweergaven** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de relevante analyseweergave en kies vervolgens de actie **Analyse per dimensie**.
3. Vul boven op de pagina **Analyse per dimensie** de velden in om te definiëren welke gegevens worden weergegeven en hoe.
4. Kies de actie **Matrix weergeven** om de matrixpagina voor de analyseweergave te openen.
5. Om toegang te krijgen tot de details van een bedrag op de matrixpagina, kiest u het bedrag.  

- De kolommen links bevatten gegevens op basis van de selectie in het veld **Als regels weergeven** in de kop.  
- De kolommen rechts bevatten gegevens op basis van de selectie in het veld **Als kolommen weergeven** in de kop.

> [!IMPORTANT]  
> U kunt geen periode selecteren die korter is dan de opgegeven periode voor datumcompressie op de **Analyseweergave**-kaart. De acties **Volgende set** en **Vorige set** zijn niet beschikbaar als u **Periode** in de velden **Als regels weergeven** en **Als kolommen weergeven** hebt geselecteerd.  

> [!NOTE]  
> Met de lijst **Dimensies - detail** kunt u een gedetailleerde classificatie weergeven van de wijze waarop dimensies zijn gebruikt voor posten gedurende een geselecteerde periode. Gebruik de lijst **Dimensies - totaal** voor een overzicht van de totale bedragen.  

> [!TIP]  
> U kunt de weergave ook wijzigen door de inhoud van de velden **Als regels weergeven** en **Als kolommen weergeven** te wijzigen. Als u een weergave-instelling wilt omkeren, kiest u de actie **Regels en kolommen omkeren**.

## <a name="update-an-analysis-view"></a>Een analyseweergave bijwerken

Met de bedragen op de pagina **Analyse per dimensies** krijgt u een overzicht van de status van het bedrijf die gold op het moment dat u voor het laatst hebt bijgewerkt. Om de huidige status op te halen, voert u de bijwerkactie uit om de analyseweergave bij te werken.

Gebruik de volgende procedure om een analyseweergave bij te werken vanuit de pagina **Analyse per dimensies**. De stappen zijn vergelijkbaar met de stappen voor het bijwerken van de pagina's **Analyseweergave** en **Analyseweergaveoverzicht**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Analyseweergaven** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de relevante analyseweergave en kies vervolgens de actie **Analyse per dimensie**.
3. Kies op de pagina **Analyse per dimensie** het veld **Analyseweergavecode**.  
4. Selecteer de regel met de gewenste analyseweergave.  
5. Selecteer op de pagina **Analyseweergaven** de relevante analyseweergave en kies vervolgens de actie **Bijwerken**.  

> [!TIP]  
> Als u het selectievakje **Bijwerken bij boeking** op een analyseweergavekaart selecteert, wordt de weergave automatisch bijgewerkt wanneer iemand een bijbehorende transactie boekt.

> [!NOTE]  
> Als u bepaalde of alle analyseweergaven tegelijk wilt bijwerken, gebruikt u de batchverwerking **Analyseweergaven bijwerken**.  

## <a name="see-also"></a>Zie ook

[Financiële Business Intelligence](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met dimensies](finance-dimensions.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
