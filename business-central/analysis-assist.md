---
title: Gegevens analyseren in lijsten met behulp van Copilot (preview)
description: Meer informatie over hoe u Copilot gebruikt in Business Central om gegevens te analyseren.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-data-in-lists-with-help-from-copilot-preview"></a>Gegevens analyseren in lijsten met behulp van Copilot (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u *hulp bij analyse* gebruikt om gegevens op lijstpagina's te analyseren.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-analysis-assist"></a>Informatie over hulp bij analyse

Hulp bij analyse is een Copilot voor de [analysemodus](analysis-mode.md) op lijstpagina's in Business Central. De analysemodus biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. Om gegevens in de analysemodus te analyseren, maakt u een *analyse*-tabblad waar u de gegevens transformeert om de gewenste aggregaties en samenvattingen weer te geven. U kunt bijvoorbeeld velden in rijen en kolommen rangschikken, filters opgeven, kolommen sorteren en draaien op velden. Met hulp bij analyse bereikt u, in plaats van deze taak handmatig uit te voeren, veel van hetzelfde&mdash;of in ieder geval om te beginnen&mdash;door woorden te gebruiken. Door de gewenste structuur in natuurlijke taal uit te drukken, zoals 'sorteren op hoeveelheid van klein naar groot' of 'gemiddelde kosten per categorie weergeven', maakt Hulp bij analyse gebruik van AI om een voorgestelde lay-out op een analysetabblad te genereren.

## <a name="available-languages"></a>Beschikbare talen

[!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

## <a name="prerequisites"></a>Vereisten

- De mogelijkheid voor hulp bij analyse wordt geactiveerd en u krijgt toestemming om deze te gebruiken. Deze taak wordt meestal gedaan door een beheerder. [Meer informatie over het configureren van Copilot- en AI-mogelijkheden](enable-ai.md).
<!-- - The display language in Business Central is set to one the following English locales: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Learn how to change the language](ui-change-basic-settings.md#language)-->
<!-- - Your Business Central environment is in any country/region except Canada (this feature isn't yet available in Canada).-->

## <a name="get-started"></a>Aan de slag

1. Open de lijstpagina die u wilt analyseren.

   Als u bijvoorbeeld wilt werken met de pagina **Artikelen**, selecteert u het pictogram ![Vergrootglas waarmee de functie Vertel me wordt geopend.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), voert u *artikelen* in en kiest u de gerelateerde koppeling.

1. U kunt beginnen met het analyseren van gegevens met Copilot rechtstreeks vanaf de lijstpagina of door eerst naar de analysemodus te gaan. Gebruik een van de volgende stappen om aan de slag te gaan:

    - Selecteer in de actiebalk bovenaan de pagina ![Toont het copilot-pictogram](media/copilot-icon.png) **Copilot** > **Lijst analyseren**.
    - Selecteer in de actiebalk bovenaan de pagina ![Toont het pictogram voor het openen van de analysemodus](media/analysis-mode-icon.png) **Analysemodus openen** en selecteer vervolgens ![Toont het copilot-pictogram](media/copilot-icon.png) **Copilot** > **Nieuwe analyse maken**.

1. Voer in het venster **Artikelen analyseren** met Copilot een beschrijving in van de gewenste lay-out. Deze beschrijving staat bekend als een *prompt*.

    ![Toont hulp bij analyse met Copilot](media/analysis-assist.png)

    > [!TIP]
    > Voor hulp bij het schrijven van een prompt selecteert u ![Toont het pictogram Prompt weergeven](media/prompt-guide-icon.png) **Promptguide** en kiest u een van de opties om aan de slag te gaan. De tekst tussen haakjes `[ ]` wordt alleen als voorbeeld weergegeven en wordt niet opgenomen in het Copilot-venster.

1. Selecteer **Genereren** en wacht vervolgens terwijl Copilot de lay-out op het nieuwe analysetabblad genereert.
1. Bekijk de resultaten op het nieuwe analysetabblad.

   > [!NOTE]
   > Als u het nieuwe analysetabblad verlaat (bijvoorbeeld wanneer u naar een ander analysetabblad of een andere analysepagina gaat) of lay-outwijzigingen aanbrengt op het tabblad (bijvoorbeeld wanneer u kolommen sorteert of instellingen wijzigt op de tabbladen **Kolommen** en **Analysefilters**), wordt het nieuwe analysetabblad automatisch opgeslagen en wordt Copilot gesloten.

1. Als u de gegenereerde analyse wilt wijzigen, kunt u een van deze stappen uitvoeren:

   - Als u wilt voortbouwen op de voorgaande instructies, voert u de informatie in het vak **Meer details over de analyse toevoegen** in en selecteert u vervolgens ![De aanpassingspijl weergeven](media/analysis-assist-adjust-button.png) de pijl **Aanpassen**. Copilot onthoudt uw eerdere instructies en gebruikt deze om aanpassingen door te voeren.

   - Als u helemaal opnieuw wilt beginnen door nieuwe instructies toe te voegen, selecteert u ![Toont het potloodpictogram voor het bewerken van de prompt](media/edit-pencil.png) **Prompt bewerken:**, voegt u de details toe aan de prompt en selecteert u vervolgens **Genereren**.

1. Als u het analysetabblad wilt opslaan, selecteert u **Behouden**. Als u het niet wilt opslaan, selecteert u **Verwijderen**.

## <a name="prompt-tips-and-examples"></a>Tips en voorbeelden voor prompts

Het maken van effectieve prompts voor Copilot is essentieel om nauwkeurige en relevante analysesuggesties te krijgen. Er zijn ook manieren om de tekst die u in prompts toevoegt, te minimaliseren om sneller te kunnen typen. Hier volgen enkele tips en richtlijnen, gevolgd door enkele voorbeelden:

- Wees beknopt en vermijd lange zinnen of meerdere zinnen.
- Zorg ervoor dat de veldnamen die in prompts worden gebruikt, enigszins overeenkomen met werkelijke veldnamen op de pagina.
- Gebruik natuurlijke taal waarbij u de gewenste gegevensstructuur op een vriendelijke en gemoedelijke manier uitdrukt.
- Gebruik veelgebruikte trefwoorden, woordgroepen en termen die worden gebruikt in gegevensanalyse, zoals `group by`, `sum`, `sort by`, enzovoort.
- Als de initiële respons niet is wat u wilt, voeg dan vervolginstructies toe of herformuleer de laatste instructie.
- Algemene afkortingen zijn acceptabel.
- Het gebruik van hoofdletters/kleine letters is niet belangrijk.

### <a name="examples"></a>Voorbeelden

In de volgende promptvoorbeelden wordt gebruik gemaakt van hulp bij analyse in de lijst **Artikelen** . De pagina voor artikelen bevat drie optelbare velden voor analyse: **Beschikbare hoeveelheid**, **Kostprijs**, **Eenheidsprijs**.

Prompt: `Show items by brand and unit of measure`

Deze prompt probeert totalen weer te geven voor alle optelbare velden, gegroepeerd op merk en het veld **Basiseenheid**. Maar in dit geval komt 'merk' met geen enkele veldnaam overeen, dus Copilot kan waarschijnlijk geen overeenkomend veld vinden. Vervolgens wordt u gevraagd de prompt opnieuw te formuleren en het opnieuw te proberen.

Prompt: `Show items by type and uom`

Deze prompt toont totalen voor alle optelbare velden, gegroepeerd op het veld **Type** en het veld **Basiseenheid**. Maar in plaats van 'maateenheid' te schrijven, wordt de afkorting `uom` gebruikt.

Prompt: `Show total quantity per type per UoM`

Deze prompt maakt een draaitabel in het veld **Beschikbare hoeveelheid** per **Basiseenheid** per **Type**.

## <a name="see-also"></a>Zie ook

[Veelgestelde vragen over verantwoordelijke AI voor Hulp bij analyse](faqs-analysis-assist.md)  
[Ad-hocgegevensanalyse](reports-adhoc-analysis.md)  
