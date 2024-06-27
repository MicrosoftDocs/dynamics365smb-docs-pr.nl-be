---
title: Marketingtekst aan artikelen toevoegen
description: Marketingtekst schrijven voor artikelen in Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="add-marketing-text-to-items"></a>Marketingtekst aan artikelen toevoegen

Voor elk artikel dat is geregistreerd in Business Central, kunt u *marketingtekst* over het artikel schrijven. Hoewel marketingtekst een soort beschrijving is, is het anders dan het veld **Beschrijving** van een artikel. Het veld **Beschrijving** wordt meestal gebruikt als een beknopte weergavenaam om het product snel te identificeren. De marketingtekst daarentegen is een rijkere en beschrijvende tekst. Het doel is het toevoegen van marketing- en promotionele inhoud, ook wel bekend als *kopij*. Deze tekst kan vervolgens bij het artikel worden gepubliceerd als het op een webshop is gepubliceerd, zoals Shopify, of in e-mails of andere communicatie met uw klanten worden geplakt.

Er zijn twee manieren om de marketingtekst te maken. De eenvoudigste manier om aan de slag te gaan, is door Copilot te gebruiken, dat door AI gegenereerde tekst voor u voorstelt. De andere manier is om bij nul te beginnen. 

## <a name="get-marketing-text-suggestions-with-copilot"></a><a name=copilot></a>Marketingtekstsuggesties krijgen met Copilot

Met Copilot krijgt u snel een tekstsuggestie die automatisch voor u wordt gegenereerd. De door AI gegenereerde tekst is toegesneden op het item en biedt een goed startpunt. De tekst wordt deels gebaseerd op de volgende informatie:

- Kenmerken die voor het artikel zijn gedefinieerd&mdash;zoals de beschrijving, kleur, afmetingen, materiaal, enzovoort. [Meer informatie over artikelkenmerken](inventory-how-work-item-attributes.md).
- Het veld **Beschrijving** van het artikel.
- De artikelcategorie. [Meer informatie over artikelen categoriseren](inventory-how-categorize-items.md).
- Selecteerbare stijlvoorkeuren zoals toon, formaat en lengte.

Copilot is ontworpen om u tijd te besparen en u te helpen creatieve en boeiende tekst te schrijven die uw merk weerspiegelt en consistent is in uw hele productlijn. Begin met het genereren van een suggestie en wijzig vervolgens de voorgestelde tekst indien nodig.

### <a name="available-languages"></a>Beschikbare talen

[!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

### <a name="prerequisites"></a>Vereisten

De functie voor marketingtekstsuggesties is geactiveerd in uw omgeving. Deze taak wordt meestal gedaan door een beheerder. Ga voor meer informatie naar [Copilot- en AI-mogelijkheden configureren](enable-ai.md).

### <a name="create-first-draft-with-copilot"></a>Een eerste concept maken met Copilot

Voer de volgende stappen uit om marketingtekst aan een bestaand artikel toe te voegen. Als u wilt weten hoe u een nieuw artikel toevoegt, gaat u naar [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

1. Open in Business Central het artikel dat u wilt wijzigen door de volgende stappen uit te voeren:

   - Selecteer in de rechterbovenhoek het pictogram ![Lampje dat de functie Vertel me opent 22](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling om een lijst met beschikbare artikelen weer te geven.

   - Dubbelklik op het artikel of selecteer in de kolom **Nr.** de waarde ervan .

1. Vanaf de artikelkaart zijn er twee manieren om aan de slag te gaan met het schrijven van marketingteksten met Copilot: vanuit het feitenblok **Marketingtekst** of via de actie **Marketingtekst**. Deze methoden worden aangegeven in de volgende afbeelding van een artikelkaart.  

   [![Toont een artikelkaart met het deelvenster Marketingtekst](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

   Voer een van de volgende stappen uit om het eerste concept voor een artikel te maken:

   - Selecteer in het deelvenster **Marketingtekst** in het feitenblok aan de rechterkant van de pagina **Opstellen met Copilot**. 

     Copilot begint met het opstellen van de marketingtekst.

   - Selecteer boven aan de pagina de actie **Marketingtekst** en selecteer vervolgens **Opstellen met Copilot** in het venster **Marketingtekst bewerken**.  De **Marketingtekst opstellen met Copilot**-vensters worden weergegeven en bevatten alle beschikbare kenmerken voor het artikel.
1. Selecteer de kenmerken waarvoor u Copilot-basissuggesties wilt ontvangen en selecteer vervolgens **Genereren**. U kunt de geselecteerde kenmerken en andere opties later wijzigen. Copilot begint met het opstellen van de marketingtekst. 

   ![Toont het venster voor het bewerken van de marketingtekst](media/marketing-text-copilot-attributes.svg)

1. Wanneer Copilot het concept voltooit, verschijnt de tekst in het Copilot-editorvenster zodat u deze kunt bekijken en bewerken.

   [![Toont de Maken met Copilot-vensters](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   U kunt nu meer suggesties krijgen, proberen de suggesties die u krijgt te verbeteren, tekst bewerken en meer. Ga naar [Controleren, bewerken en opslaan](#review-edit-and-save-text) voor details.

### <a name="review-edit-and-save-text"></a>Tekst controleren, bewerken en opslaan

Zodra u de eerste versie hebt, moet u deze controleren en wijzigingen aanbrengen in de tekst om deze gereed te maken voor publicatie. Dit werk wordt gedaan in de Copilot-editor, waarmee u meer suggesties kunt krijgen, voorkeuren kunt wijzigen om de suggesties te beïnvloeden en handmatig wijzigingen kunt aanbrengen en de tekst opmaken.

> [!IMPORTANT]
> De door AI gegenereerde tekst van Copilot is slechts een suggestie en kan fouten bevatten. Het vereist menselijk toezicht en controle om ervoor te zorgen dat de tekst klopt en gepast is. Bekijk alle voorgestelde tekst en bewerk deze indien nodig voordat u deze opslaat en publiceert voor openbaar gebruik.

Gebruik de volgende richtlijnen om de marketingtekst af te ronden en op te slaan.

1. Wijzig de tekst rechtstreeks in het vak tekst. Gebruik de werkbalk onderaan het vak om tekst op te maken, koppelingen toe te voegen en meer.
2. Selecteer **Opnieuw genereren** om een nieuwe suggestie te krijgen.
3. Als u niet tevreden bent met de suggesties, kunt u de tekstsuggesties verbeteren met behulp van de voorkeursopties **Toon**, **Formaat** en **Nadruk**.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Ga voor richtlijnen voor het verbeteren van suggesties naar [Tekstsuggesties verbeteren en aanpassen](#improve-and-tailor-text-suggestions).

4. Als u heen en weer wilt bladeren door de suggesties, gebruikt u de koppelingen vorige en volgende boven aan de pagina (*x* **of** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Controleer de tekst zorgvuldig op juistheid en geschiktheid:

   - Als u de tekst wilt opslaan, selecteert u **Behouden**. 
   - Als u niet wilt opslaan, selecteert u de knop weggooien (prullenbak) ![Toont het prullenbakpictogram voor het verwijderen van alle Copilot-voorstellen voor bankrekeningreconciliatie](media/copilot-delete-trash-can.png).

### <a name="improve-and-tailor-text-suggestions"></a>Tekstsuggesties verbeteren en aanpassen

Er zijn een paar stappen die u kunt nemen om de tekstsuggesties te verbeteren en aan te passen aan uw persoonlijke of zakelijke voorkeuren.

1. De artikelkenmerken wijzigen die door Copilot worden gebruikt.

   Copilot-suggesties zijn deels gebaseerd op de kenmerken die aan het artikel zijn toegewezen. Als u de beschikbare kenmerken en de huidige instellingen wilt bekijken, selecteert u het pictogram ![Toont het bewerkingspictogram in het Copilot-venster voor het wijzigen van kenmerken](media/edit-pencil.png) in de linkerbovenhoek. Kies po de pagina **Artikelkenmerken** de kenmerken die het beste aansluiten bij de kenmerken die u wilt promoten. Hoe meer relevante kenmerken u opneemt, hoe rijker de uitkomst wordt. Als u het gevoel hebt dat u enkele belangrijke kenmerken mist, voeg er dan meer toe. Zie [Werken met artikelkenmerken](inventory-how-work-item-attributes.md) voor meer informatie over kenmerken
1. Wijzig uw voorkeursinstellingen voor de opties **Toon**, **Formaat** en **Nadruk**.

   |Optie|Omschrijving|
   |-|-|
   |Toon |Gebruik deze optie om te beïnvloeden wat voor soort woorden, zinsdelen en interpunctie worden gebruikt om de doelgroep aan te spreken. U kunt kiezen uit verschillende vooraf gedefinieerde tonen, variërend van **Formeel** (wat resulteert in een zakelijke toon) tot **Creatief** (wat resulteert in een informele toon). |
   |Indeling en lengte|Gebruik deze optie om de algemene structuur van de tekst te bepalen, die uit drie delen bestaat, gedekt door vier verschillende opties: <ul><li>**Tagline** - Een pakkende zin of korte zin die het artikel of merk identificeert.</li><li>**Alinea** - Een enkele alinea met vloeiende en uitgebreide tekst, bestaande uit meerdere volledige zinnen.</li><li>**Tagline + alinea**- Een tagline gevolgd door een alinea</li><li>**Kort** - Een inleidende zin, vergelijkbaar met een tagline, gevolgd door een lijst met opsommingstekens met de belangrijkste aandachtspunten.</li></ul> |
   |Nadruk|Gebruik deze optie om uit een lijst met vooraf gedefinieerde eigenschappen te kiezen die u in de tekst wilt benadrukken. Kies een kwaliteit die het beste aansluit bij het type artikel waarover u schrijft. De kwaliteiten komen niet direct overeen met de kenmerken, beschrijving of categorie van het artikel. Bijvoorbeeld, **Kwaliteit** zou een goede keuze kunnen zijn voor zowel een fiets als bureau, terwijl **Snelheid** geschikt zou zijn voor een fiets, maar niet voor een bureau.|

1. Verbeter het veld **Beschrijving** op de artikelkaart.

   De tekst in het veld **Beschrijving** wordt ongewijzigd gebruikt op veel plaatsen in de voorgestelde tekst, dus het is belangrijk dat de beschrijving het beste weergeeft hoe u wilt verwijzen naar het artikel in de marketingtekst. 

1. Zorg ervoor dat het veld **Artikelcategoriecode** op de artikelkaart is ingesteld op de juiste categorie.

   Copilot zoekt naar woorden en zinsdelen die verband houden met de categorie en verwerkt deze in de voorgestelde tekst.

### <a name="working-with-multiple-languages"></a>Werken met meerdere talen

Tekst wordt altijd gegenereerd in de taal die is gedefinieerd in uw [gebruikersinstellingen](ui-change-basic-settings.md#language). Als uw organisatie in een andere taal werkt en gegevens in Business Central invoert, of als Business Central is verbonden met uw online winkel, zoals met Shopify, kan dit resulteren in het publiceren van inhoud die niet overeenkomt met vergelijkbare marketinginhoud.

## <a name="create-text-from-scratch"></a>Een geheel nieuwe tekst maken

1. Open in Business Central het artikel dat u wilt wijzigen als volgt:

    1. Selecteer in de rechterbovenhoek het pictogram ![Lampje dat de functie Vertel me opent 22](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling om een lijst met beschikbare artikelen weer te geven.
    2. Om het artikel te openen dubbelklikt u erop of selecteert u in het veld **Nr.** ervan .

2. Ga op een van de volgende manieren te werk:

   - Selecteer in het deelvenster **Marketingtekst** in het feitenblok aan de rechterkant van de pagina **Bewerken**.
   - Selecteer de actie **Marketingtekst**.
3. Wijzig de tekst rechtstreeks in het vak **Marketingtekst** . Gebruik de werkbalk onder aan het vak om tekst op te maken, koppelingen toe te voegen en meer.
4. Als u klaar bent, selecteert u **Opslaan** om de tekst op te slaan.

## <a name="see-also"></a>Zie ook

[Overzicht van suggesties voor marketing](ai-overview.md)  
[Problemen oplossen met Copilot- en AI-mogelijkheden](ai-copilot-troubleshooting.md)  
[Veelgestelde vragen over suggesties voor marketing](faqs-marketing-text.md)  
[Copilot- en AI-mogelijkheden configureren](enable-ai.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
