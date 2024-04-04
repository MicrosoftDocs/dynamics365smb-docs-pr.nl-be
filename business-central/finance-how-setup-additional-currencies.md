---
title: Extra valuta's instellen
description: 'Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken en er is een andere valuta ingesteld als aanvullende valuta, waaraan een huidige wisselkoers is toegewezen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 07/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Een extra rapportagevaluta instellen.

Aangezien bedrijven steeds vaker in andere landen/regio's opereren, is het belangrijk dat zij de financiële gegevens in meer dan één valuta kunnen controleren en rapporteren.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] wordt dit valuta genoemd als u op zoek bent naar realtime informatie over wisselkoersen of historische koersen. Zie naast dit artikel ook [Valutawisselkoersen bijwerken](finance-how-update-currencies.md).


Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken, maar u kunt het ook instellen om een andere valuta te gebruiken, waaraan een huidige wisselkoers is toegewezen. Door een tweede valuta in te stellen als een zogenaamde aanvullende rapportagevaluta, legt [!INCLUDE[prod_short](includes/prod_short.md)] bedragen automatisch vast in zowel de LV als deze aanvullende rapportagevaluta voor elke grootboekpost en andere posten, zoals btw-posten.

> [!Warning]
> De functionaliteit Extra rapportagevaluta maken moet niet worden gebruikt als een basis voor vertaling van financiële overzichten, tenzij u de beperkingen begrijpt. Het is geen programma dat een vertaling kan uitvoeren van financiële overzichten van buitenlandse dochterondernemingen als onderdeel van een bedrijfsconsolidatie. De extra rapportagevalutafunctie kan alleen worden gebruikt om rapporten in een andere valuta voor te bereiden, alsof die valuta de lokale valuta van het bedrijf was.
>
> U hebt bijvoorbeeld een groot aantal debiteuren in Britse ponden (GBP) en u hebt uw aanvullende rapportagevaluta (ACY) ingesteld op GBP. In dit scenario worden bedragen in de debiteuren die GBP gebruiken niet gecorrigeerd voor valutakoerswinsten/-verliezen in de aanvullende rapportagevaluta, alleen bedragen op de debiteuren die in andere valuta's zijn. Dat betekent dat als u aanvullende rapportagevaluta gebruikt om uw financiële overzichten te rapporteren, dit kan leiden tot te lage of te hoge uitstaande saldi van debiteuren.

## Rapporten en bedragen weergeven in de extra rapportagevaluta
Het gebruik van een extra rapportagevaluta kan in de volgende gevallen hulp bieden bij het rapportageproces voor een bedrijf:

- Bedrijven in landen/regio's die niet bij de EU horen en die grote hoeveelheden transacties aangaan met bedrijven in EU-landen/regio's. In dit geval wil het bedrijf buiten de EU mogelijk tevens in euro rapporteren om de financiële rapporten beter bruikbaar te maken voor handelspartners in de EU.
- Bedrijven die tevens rapporten in een internationale handelsvaluta in plaats van hun eigen lokale valuta willen weergeven.

Verschillende financiële rapporten worden gebaseerd op grootboekposten. Als u rapportgegevens in de extra rapportagevaluta wilt weergeven, plaatst u eenvoudigweg een vinkje in het veld **Bedragen in rapp.-valuta weergeven** van het sneltabblad **Opties** voor het betreffende grootboekrapport.

## Wisselkoersen corrigeren

Aangezien valutakoersen constant wisselen, moeten de extra valuta-equivalenten in uw systeem periodiek worden gecorrigeerd. Als deze correcties niet worden uitgevoerd, kunnen de bedragen die omgerekend zijn van vreemde (of extra) valuta's en geboekt zijn in het grootboek in LV misleidend zijn. Bovendien moeten dagelijkse posten die geboekt zijn doordat een dagwisselkoers is ingevoerd in de toepassing, worden bijgewerkt nadat de dagwisselkoersgegevens zijn ingevoerd. De batchverwerking **Wisselkoers herwaarderen** wordt gebruikt om de wisselkoersen van de geboekte klant, leverancier en bankrekeningposten te corrigeren. U kunt er tevens extra rapportagevalutabedragen in grootboekposten mee bijwerken. Zie voor meer informatie [Valutawisselkoersen bijwerken](finance-how-update-currencies.md).

## Een extra rapportagevaluta instellen

Volg deze stappen om een extra rapportagevaluta in te stellen:

- Geef grootboekrekeningen op voor het boeken van wisselkoerscorrecties.  
- Geef de wisselkoerscorrectiemethode op voor alle grootboekrekeningen.  
- Geef de wisselkoersherwaarderingsmethode op voor btw-boekingen.  
- Activeer de extra rapportagevaluta.  

### Grootboekrekeningen opgeven voor het boeken van wisselkoerscorrecties  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Valuta's** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op de pagina **Valuta's** de volgende velden in voor de extra rapportagevaluta.  

|Veld|Description|  
|---------------------------------|---------------------------------------|  
|**Gereal. grootboekwinstrek.**|De grootboekrekening waarnaar wisselkoerswinsten worden geboekt bij valutaherwaarderingen van de lokale valuta en de rapportagevaluta.|  
|**Gereal. grootboekverliesrek.**|De grootboekrekening waarnaar wisselkoersverliezen worden geboekt bij valutaherwaarderingen van de lokale valuta en de rapportagevaluta.|  
|**Verschillenrekening (Winst)**|De grootboekrekening waarnaar verschilbedragen (winst) worden geboekt als u in de lokale valuta en de rapportagevaluta boekingen uitvoert in de module Financieel.|  
|**Verschillenrekening (Verlies)**|De grootboekrekening waarnaar verschilbedragen (verlies) worden geboekt als u in de lokale valuta en de rapportagevaluta boekingen uitvoert in de module Financieel.|

> [!NOTE]  
>  Verschillenbedragen kunnen ontstaan wanneer [!INCLUDE[prod_short](includes/prod_short.md)] debet- en creditbedragen afrondt die omgerekend zijn van de LV naar een extra rapportagevaluta.  

U moet voor elke grootboekrekening opgeven hoe grootboekbedragen voor die rekening worden gecorrigeerd bij wisselkoersschommelingen tussen de LV en de extra rapportagevaluta.  

### De wisselkoerscorrectiemethode opgeven voor alle grootboekrekeningen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **Rekeningschema** de relevante rekening en kies de actie **Bewerken**.  
3. Selecteer op de pagina **Grootboekrekening** de relevante methode in het veld **Wisselkoersherwaardering**.  

    Als u in een extra rapportagevaluta boekt, geeft u in het veld **Wisselkoersherwaardering** aan hoe deze grootboekrekening wordt gecorrigeerd bij wisselkoersschommelingen tussen de LV en de extra rapportagevaluta. De volgende tabel bevat de opties waaruit u kunt kiezen.  

    |Veld|Beschrijving|  
    |----------------------------------|---------------------------------------|  
    |**Geen**|Er wordt geen wisselkoersherwaardering uitgevoerd op de grootboekrekening. Dit is de standaardwaarde.<br /><br /> **OPMERKING:** Deze optie moet altijd zijn geselecteerd als de wisselkoers tussen het LV en de extra rapportagevaluta altijd vast is.|  
    |**Bedrag**|Het bedrag in LV is aangepast voor eventuele wisselkoerswinsten of -verliezen. Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.|  
    |**Bedrag (Rapp.-val.)**|De extra rapportagevaluta is aangepast voor eventuele wisselkoerswinsten of -verliezen. Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag (Rapp.-val.)** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.|  

    Wisselkoerswinsten en -verliezen worden geboekt wanneer u de batchverwerking **Wisselkoers herwaarderen** uitvoert. In die batchverwerking wordt de herwaarderingswisselkoers geïdentificeerd op de pagina **Valutawisselkoersen** en worden vervolgens de bedragen in de velden **Bedrag** en **Bedrag (Rapp.-val.)** in de grootboekpost vergeleken om te bepalen of er een wisselkoerswinst of -verlies is. Voor de batchverwerking wordt de optie gebruikt die u in het veld **Wisselkoersherwaardering** selecteert om te bepalen hoe wisselkoerswinsten of -verliezen voor grootboekrekeningen moeten worden berekend en geboekt.  

4.  Sluit de pagina **Grootboekrekening**.  

### Wisselkoersherwaarderingsmethode opgeven voor btw-boekingen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Boekhoudinstellingen** de relevante methode in het veld **Btw-herwaardering**.  
3. Als u in een extra valuta boekt, kunt u in het veld **Btw-herwaardering** aangeven hoe de rekeningen die zijn ingesteld voor btw-boekingen op de pagina **Btw-boekingsinstellingen** worden geherwaardeerd bij wisselkoersschommelingen tussen de LV en de extra rapportagevaluta.  

    Wanneer u de batchverwerking **Wisselkoers herwaarderen** uitvoert, wordt de wisselkoersherwaardering bepaald op de pagina **Valutawisselkoers** en worden vervolgens de bedragen in het veld **Bedrag** en **Bedrag (Rapp.-val.)** in de btw-boeking vergeleken om te bepalen of er een wisselkoerswinst of -verlies is. Op basis van de optie die u opgeeft in dit veld, wordt in de batchverwerking bepaald hoe wisselkoerswinsten of -verliezen voor btw-rekeningen worden geboekt.  

    U hebt dezelfde opties als met grootboekposten, maar in dit geval zijn de geherwaardeerde posten de btw-posten. De volgende tabel bevat de opties waaruit u kunt kiezen.

    |Veld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Geen**|Er wordt geen wisselkoersherwaardering uitgevoerd op de grootboekrekening. Dit is de standaardwaarde.|  
    |**Bedrag**|Het bedrag in LV is aangepast voor eventuele wisselkoerswinsten of -verliezen. Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.|  
    |**Bedrag (Rapp.-val.)**|De extra rapportagevaluta is aangepast voor eventuele wisselkoerswinsten of -verliezen. Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag (Rapp.-val.)** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.|  

### De extra rapportagevaluta activeren  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Boekhoudinstellingen** het veld **Extra rapportagevaluta** om de extra valuta te selecteren die u voor de rapportage wilt gebruiken.  
3. Wanneer u het veld verlaat, geeft [!INCLUDE[prod_short](includes/prod_short.md)] een bevestigingsbericht weer waarin de effecten worden beschreven die het activeren van de rapportagevaluta tot gevolg heeft.  
4. Kies de knop **Ja** om te bevestigen dat u de valuta wilt activeren.  
5. De batchtaak **Rapp.-val. herwaarderen** wordt geopend.

    Met deze batchverwerking worden LV-bedragen van bestaande posten geconverteerd in de rapportagevaluta. Voor de batchverwerking wordt een standaardwisselkoers gebruikt die gekopieerd wordt van de wisselkoers die geldig is op de werkdatum op de pagina **Valutawisselkoersen**. Verschillenbedragen die ontstaan bij de conversie van LV naar de rapportagevaluta worden geboekt naar de verschillenrekeningen (winst of verlies) die zijn opgegeven op de pagina **Valuta's**. De boekingsdatum en het documentnummer van deze posten zijn gelijk aan de oorspronkelijke grootboekpost. Nadat alle verschilposten zijn geboekt, boekt de batchverwerking vervolgens een afrondingspost op de sluitdatum van elk afgesloten jaar naar de rekening voor ingehouden winst. Hiermee wordt ervoor gezorgd dat het eindsaldo van de resultatenrekeningen voor elk afgesloten jaar 0 is voor de LV en de rapportagevaluta.
6. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Kies **OK** om de batchverwerking te starten.  

Nadat u de batchverwerking hebt uitgevoerd, staan de bedragen van de volgende bestaande posten zowel in de LV als in de rapportagevaluta:  

- Grootboekposten  
- Artikelvereffeningsposten  
- Btw-posten  
- Projectposten  
- Waardeposten  
- Productieorderregels  
- Productieorderposten  

Bovendien hebben alle toekomstige posten van hetzelfde type bedragen in zowel de LV als de rapportagevaluta.  

> [!NOTE]  
> Het veld **Rapportagevaluta** wordt pas geactiveerd nadat u op de knop **OK** in de batchverwerking **Rapp.-val. herwaarderen** hebt geklikt.  

## Zie ook

[Valutawisselkoersen bijwerken](finance-how-update-currencies.md)  
[Jaren en perioden afsluiten](year-close-years-periods.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
