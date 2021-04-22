---
title: Aangepaste Power BI-rapporten voor Business Central-gegevens weergeven | Microsoft Docs
description: U kunt Power BI-rapporten gebruiken om extra inzicht te krijgen in gegevens in lijsten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777528"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] bevat een Power BI-feitenblokbesturingselement op veel belangrijke lijstpagina's. Het doel van dit feitenblok is om Power BI-rapporten weer te geven die betrekking hebben op records in de lijsten, waardoor extra inzicht in de gegevens ontstaat. Het idee is dat terwijl u van de ene naar de andere rij gaat, het rapport wordt bijgewerkt en gefilterd op de geselecteerde vermelding.

[!INCLUDE[prod_long](includes/prod_long.md)] wordt geleverd met enkele van deze rapporten. U kunt ook uw eigen aangepaste rapporten maken die in dit feitenblok worden weergegeven. Het maken van deze rapporten is vergelijkbaar met andere rapporten. Maar er zijn een paar ontwerpregels die u moet volgen om ervoor te zorgen dat de rapporten worden weergegeven zoals verwacht. Deze regels worden in dit artikel uitgelegd.

> [!NOTE]
> Voor algemene informatie over maken en publiceren van Power BI-rapporten voor Business Central raadpleegt u [Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens](across-how-use-financials-data-source-powerbi.md) weer te geven. 

## <a name="prerequisites"></a>Vereisten

- Een Power BI-account.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a>Een rapport maken voor een lijstpagina

1. Start Power BI Desktop.
2. Selecteer **Gegevens verkrijgen** en begin met het kiezen van de gegevensbron voor het rapport.

    In deze stap geeft u de Business Central-lijstpagina's op die de gegevens bevatten die u in het rapport wilt hebben. Als u bijvoorbeeld een rapport wilt maken voor de lijst Verkoop, moet u ervoor zorgen dat de gegevensset informatie bevat die verband houdt met de verkoop.

    Volg de instructies voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] toevoegen als gegevensbron in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Stel het rapportfilter in.

    Als u wilt dat de gegevens worden bijgewerkt op basis van de geselecteerde record in de lijst, voegt u een filter toe aan het rapport. Het filter moet een veld van de gegevensbron bevatten dat wordt gebruikt om elke record in de lijst uniek te identificeren. In termen van ontwikkelaars is dit veld de *primaire sleutel*. In de meeste gevallen is de primaire sleutel voor een lijst **Nr.** toevoegen.

    Voer de volgende stappen uit om het filter in te stellen:

    1. Selecteer bij **Filters** het primaire sleutelveld in de lijst met beschikbare velden.
    2. Sleep het veld naar het deelvenster **Filters** en zet het neer in het vak **Filters op alle pagina's**.
    3. Stel het **Filtertype** in op **Basisfiltering**. Het kan geen pagina, visueel element of geavanceerd filter zijn.

    ![Het rapportfilter instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Ontwerp de rapportlay-out.

    Maak de lay-out door velden te slepen en visualisaties toe te voegen. Zie voor meer informatie [Werken met de rapportweergave in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in de Power BI-documentatie.

5. Zie de volgende secties over het formaat van het rapport en het gebruik van meerdere pagina's.

6. Sla het rapport op en geef het een naam.

    Het is belangrijk het rapport een naam te geven die de naam bevat van de lijstpagina die aan het rapport is gekoppeld. Is het rapport bijvoorbeeld gemaakt voor de lijstpagina **Artikelen**, neem dan het woord *artikelen* op in de naam.  

    Deze naamgevingsconventie is geen vereiste. Deze zorgt er echter wel voor dat gebruikers de gewenste rapporten sneller kunnen selecteren in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer de rapportselectiepagina wordt geopend vanuit een lijstpagina, wordt de lijst met rapporten automatisch gefilterd op basis van de paginanaam. De rapporten worden gefilterd om het aantal weergegeven rapporten te beperken. Gebruikers kunnen het filter ook verwijderen als ze de volledige lijst met rapporten die beschikbaar zijn in Power BI, willen bekijken.

7. Als u klaar bent, publiceert u het rapport zoals u gewend bent.

    Zie voor meer informatie [Een rapport publiceren](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Test het rapport.

    Zodra de rapporten naar uw werkruimte zijn gepubliceerd, zou het beschikbaar moeten zijn in het feitenblok Power BI op de lijstpagina in [!INCLUDE[prod_short](includes/prod_short.md)].

    Voer de volgende stappen uit om het te testen.

    1. Open [!INCLUDE[prod_short](includes/prod_short.md)] en ga naar de lijstpagina.
    2. Als u het feitenblok Power BI niet ziet, gaat u naar de actiebalk en selecteert u **Acties** > **Weergeven** > **Power BI-rapporten weergeven/verbergen**.
    3. Selecteer in het feitenblok Power BI **Rapporten selecteren**, schakel het vakje **Inschakelen** voor het rapport in en selecteer vervolgens **OK**.

    Als het correct is ontworpen, wordt het rapport weergegeven.  

## <a name="set-the-report-size-and-color"></a>De rapportgrootte en kleur instellen

De grootte van het rapport moet worden ingesteld op 325 bij 310 pixels. Deze grootte is vereist voor een juiste schaling van het rapport in de beschikbare ruimte van het Power BI-besturingselement Feitenblok in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u de grootte van het rapport wilt definiëren, plaatst u de focus buiten het rapportlay-outgebied en kiest u vervolgens het pictogram met de verfroller.

![De breedte en hoogte van het rapport instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

U kunt de breedte en hoogte van het rapport wijzigen door **Aangepast** in het veld **Soort** te kiezen.

Als u wilt dat de achtergrond van het rapport wordt vermengd met de achtergrondkleur van het Power BI-feitenblokbesturingselement, stelt u de achtergrondkleur van het rapport in op *#FFFFFF* (wit). 

> [!TIP]
> Gebruik het [!INCLUDE [prod_short](includes/prod_short.md)]-themabestand om rapporten samen te stellen met dezelfde kleurstijlen als de [!INCLUDE [prod_short](includes/prod_short.md)]-apps. Zie voor meer informatie [Het rapportthema [!INCLUDE [prod_short](includes/prod_short.md)] gebruiken](across-how-use-financials-data-source-powerbi.md#theme).

## <a name="reports-with-multiple-pages"></a>Rapporten met meerdere pagina's

Met Power BI kunt u één rapport met meerdere pagina's maken. Voor rapporten die worden weergegeven met lijstpagina's, raden we echter af om meer dan één pagina te gebruiken. In het Power BI-besturingselement Feitenblok wordt alleen de eerste pagina van uw rapport weergegeven.

## <a name="fixing-problems"></a>Problemen oplossen

In dit gedeelte vindt u instructies voor het oplossen van problemen die u kunt tegenkomen wanneer u een Power BI-rapport voor een lijstpagina in [!INCLUDE[prod_short](includes/prod_short.md)] probeert weer te geven.  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a>U kunt het feitenblok Power BI niet zien op een lijstpagina

Standaard is het feitenblok Power BI verborgen. Als u het feitenblok op een pagina wilt weergeven, selecteert u op de actiebalk **Acties** > **Weergeven** > **Power BI-rapporten weergeven/verbergen**.

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a>U kunt het rapport niet zien in het deelvenster Rapport selecteren

Dit komt waarschijnlijk omdat de naam van het rapport niet de naam bevat van de lijstpagina die wordt weergegeven. Wis het filter om de volledige lijst met rapporten die beschikbaar zijn in Power BI, weer te geven.  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Het rapport is geladen, maar is leeg, niet gefilterd of onjuist gefilterd

Controleer of het rapportfilter de juiste primaire sleutel bevat. In de meeste gevallen is dit het veld **Nr.** maar in de tabel **Grootboekpost** moet u bijvoorbeeld het veld **Postnr.** gebruiken.

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Het rapport is geladen, maar er wordt een pagina weergegeven die u niet had verwacht

Controleer of de pagina die u wilt weergeven, de eerste pagina in uw rapport is.  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Rapporten worden met ongewenste grijze randen weergegeven, zijn te klein of te groot

Controleer of de grootte van het rapport is ingesteld op 325 x 310 pixels. Sla het rapport op en vernieuw vervolgens de lijstpagina.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Uw bedrijfsgegevens inschakelen voor Power BI](admin-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Financiën](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]