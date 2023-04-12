---
title: Marketingtekst aan artikelen toevoegen
description: Marketingtekst schrijven voor artikelen in Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Marketingtekst aan artikelen toevoegen

Voor elk artikel dat is geregistreerd in Business Central, kunt u *marketingtekst* over het artikel schrijven. Hoewel marketingtekst een soort beschrijving is, is het anders dan het veld **Beschrijving**. Het veld **Beschrijving** wordt meestal gebruikt als een beknopte weergavenaam om het product snel te identificeren. De marketingtekst daarentegen is een rijkere en beschrijvende tekst. Het doel is het toevoegen van marketing- en promotionele inhoud, ook wel bekend als *copy*. Deze tekst kan vervolgens met het artikel worden gepubliceerd als het op een webshop wordt gepubliceerd, bijvoorbeeld Shopify.

Er zijn twee manieren om de marketingtekst te maken. De eenvoudigste manier om aan de slag te gaan, is door Copilot te gebruiken, dat door AI gegenereerde tekst voor u voorstelt. De andere manier is om bij nul te beginnen. 

## <a name=copilot></a>Door AI gegenereerde marketingtekst schrijven (preview) met Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Met Copilot krijgt u snel een tekstsuggestie die automatisch voor u wordt gegenereerd. De door AI gegenereerde tekst is toegesneden op het item en biedt een goed startpunt. De tekst wordt deels gebaseerd op de volgende informatie:

- Kenmerken die voor het artikel zijn gedefinieerd, zoals de beschrijving, kleur, afmetingen, materiaal, enzovoort.
- Selecteerbare stijlvoorkeuren zoals toon, formaat en lengte.

Copilot is ontworpen om u tijd te besparen en u te helpen creatieve en boeiende tekst te schrijven die uw merk weerspiegelt en consistent is in uw hele productlijn. Begin met het genereren van een suggestie en wijzig vervolgens de voorgestelde tekst indien nodig.

> [!NOTE]
> In de preview-versie van Business Central is door AI gegenereerde tekst alleen in het Engels.

### Vereisten

- U gebruikt een [preview-versie](ai-preview-getstarted.md) van Business Central die is ingeschakeld voor Copilot. Het inschakelen van Copilot wordt gedaan door een beheerder. Ga voor meer informatie naar [Op AI gebaseerde artikelmarketingtekst met Copilot configureren](enable-ai.md).
- De taal die u gebruikt in Business Central moet Engels zijn. Alle beschikbare Engelse landinstellingen werken, zoals Engels (Verenigde Staten), Engels (Verenigd Koninkrijk) of Engels (Zuid-Afrika).

   Om de taal te wijzigen, selecteert u in de rechterbovenhoek het pictogram **Instellingen** ![Instellingen](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum"). > **Mijn instellingen** > **Taal**. Ga voor meer informatie naar [Basisinstellingen wijzigen](ui-change-basic-settings.md#language).
- Bekijk de [Veelgestelde vragen over copiloot](ai-faq.md) voor meer informatie over door AI gegenereerde tekstsuggesties van Copilot en hoe u deze kunt gebruiken.

### Een eerste concept maken met Copilot

1. Open in Business Central het artikel dat u wilt wijzigen. Voer de volgende stappen uit om een artikel te openen:

   1. Selecteer in de rechterbovenhoek het pictogram ![Lampje dat de functie Vertel me opent 22](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling om een lijst met beschikbare artikelen weer te geven.
   2. Om het artikel te openen dubbelklikt u erop of selecteert u in het veld **Nr.** de waarde ervan.

   Ga voor informatie over het maken van een artikel naar [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

   [![Toont een artikelkaart met het deelvenster Marketingtekst](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. Vanaf de artikelkaart zijn er twee manieren om aan de slag te gaan met het schrijven van marketingtekst met Copilot:

   - Eén manier is om het deelvenster **Marketingtekst** in het feitenblok aan de rechterkant van de pagina te gebruiken. Volg deze stappen:

      1. Selecteer **Maken met Copilot** in het deelvenster **Marketingtekst**.

         De voorgestelde tekst verschijnt in het deelvenster.
      2. Als u nog een suggestie wilt, selecteert u **Maken met Copilot**. Als u een suggestie niet leuk vindt, selecteert u **Sluiten** om het deelvenster te wissen.

         U kunt deze stap steeds opnieuw doen totdat u een suggestie krijgt waarvan u denkt dat het een goed genoeg startpunt is. Houd er echter rekening mee dat de huidige suggestie wordt overschreven en dat u deze niet noodzakelijkerwijs terug kunt krijgen. Dus als u de huidige suggestie leuk vindt, ga dan naar de volgende stap. U hebt nog steeds de mogelijkheid om meer suggesties te krijgen en zelfs om de suggesties te verbeteren, als u dat later wilt.
      3. Selecteer **Deze suggestie controleren en opslaan** of **Bewerken** om de tekst te bekijken, te bewerken en op te slaan.

         Deze stap brengt u naar de pagina **Maken met Copilot**. Ga naar de volgende sectie.

         > [!NOTE]
         > De tekst wordt pas opgeslagen als u deze stap uitvoert.

   - Een andere manier is om de actie **Marketingtekst** boven aan de artikelkaartpagina te selecteren om direct naar de pagina **Maken met Copilot** te gaan.

     Selecteer op de pagina **Maken met Copilot** **Maken met Copilot** om de eerste suggestie te krijgen. U kunt daarna meer suggesties krijgen, proberen de suggesties die u krijgt te verbeteren, tekst bewerken en meer. Ga naar [Controleren, bewerken en opslaan](#review-edit-and-save-text) voor details.

   > [!TIP]
   > [Waar komt de suggestie vandaan?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### Tekst controleren, bewerken en opslaan

Zodra u de eerste versie hebt, moet u deze controleren en wijzigingen aanbrengen in de tekst om deze gereed te maken voor publicatie. Dit werk wordt gedaan vanaf de pagina **Maken met Copilot**. De huidige tekst wordt weergegeven in het vak **Marketingtekst**. Op de pagina kunt u meer suggesties krijgen, voorkeuren wijzigen om de suggesties te beïnvloeden, en handmatig wijzigingen aanbrengen en de tekst opmaken.

[![Toont de Maken met Copilot-vensters](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> De door AI gegenereerde tekst van Copilot is slechts een suggestie en kan fouten bevatten. Het vereist menselijk toezicht en controle om ervoor te zorgen dat de tekst klopt en gepast is. Bekijk alle voorgestelde tekst en bewerk deze indien nodig voordat u deze opslaat en publiceert voor openbaar gebruik.

Gebruik de volgende richtlijnen om de marketingtekst af te ronden en op te slaan.

1. Wijzig de tekst rechtstreeks in het vak **Marketingtekst** . Gebruik de werkbalk onderaan het vak om tekst op te maken, koppelingen toe te voegen en meer.
2. Selecteer **Concept maken** om een nieuwe suggestie te krijgen.
3. Als u niet tevreden bent met suggesties, kunt u tekstsuggesties verbeteren op basis van uw voorkeuren.

   Selecteer **Meer instellingen**, wijzig de opties die worden weergegeven onder **Kiezen hoe Copilot suggesties doet** en selecteer vervolgens **Concept maken** om een nieuwe suggestie te krijgen.

   Ga voor richtlijnen voor het verbeteren van suggesties naar [Tekstsuggesties verbeteren en aanpassen](#improve-and-tailor-text-suggestions).

4. Als u terug wilt gaan naar de vorige suggestie, selecteert u **Ongedaan maken**.
5. Controleer de tekst zorgvuldig op juistheid en geschiktheid en selecteer vervolgens **OK** om deze op te slaan.

### Tekstsuggesties verbeteren en aanpassen

Er zijn een paar stappen die u kunt nemen om de tekstsuggesties te verbeteren en aan te passen aan uw persoonlijke of zakelijke voorkeuren.

1. Gebruik de opties boven aan de pagina **Maken met Copilot** om het resultaat van de door AI gegenereerde tekst te beïnvloeden: 

   |Optie|Omschrijving|
   |-|-|
   |Op te nemen kenmerken|Gebruik deze optie om de suggesties gedeeltelijk te baseren op de kenmerken die aan het artikel zijn toegewezen. Kies de kenmerken die het beste aansluiten bij de kenmerken die u wilt promoten. Hoe meer relevante kenmerken u opneemt, hoe rijker de uitkomst zal zijn. Als u het gevoel hebt dat u enkele belangrijke kenmerken mist, voeg er dan meer toe. Zie [Werken met artikelkenmerken](inventory-how-work-item-attributes.md) voor meer informatie over kenmerken |
   |Een kwaliteit benadrukken|Gebruik deze optie om uit een lijst met vooraf gedefinieerde eigenschappen te kiezen die u in de tekst wilt benadrukken. Kies een kwaliteit die het beste aansluit bij het type artikel waarover u schrijft. De kwaliteiten komen niet direct overeen met de kenmerken, beschrijving of categorie van het artikel. Bijvoorbeeld, **Kwaliteit** zou een goede keuze kunnen zijn voor zowel een fiets als bureau, terwijl **Snelheid** geschikt zou zijn voor een fiets, maar niet voor een bureau.|
   |Toon van stem|Gebruik deze optie om te beïnvloeden wat voor soort woorden, zinsdelen en interpunctie worden gebruikt om de doelgroep aan te spreken. U kunt kiezen uit verschillende vooraf gedefinieerde tonen, variërend van **Formeel** (wat resulteert in de meest zakelijke toon van de keuzes) tot **Creatief** (wat resulteert in een zeer informele toon). |
   |Indeling en lengte|Gebruik deze optie om de algemene structuur van de tekst te bepalen, die uit drie delen bestaat, gedekt door vier verschillende opties: <ul><li>**Tagline** - Een pakkende zin of korte zin die het artikel of merk identificeert.</li><li>**Alinea** - Een enkele alinea met vloeiende en uitgebreide tekst, bestaande uit meerdere volledige zinnen.</li><li>**Tagline + alinea**- Een tagline gevolgd door een alinea</li><li>**Kort** - Een inleidende zin, vergelijkbaar met een tagline, gevolgd door een lijst met opsommingstekens met de belangrijkste aandachtspunten.</li></ul> |

2. Verbeter het veld **Beschrijving** op de artikelkaart.

   De tekst in het veld **Beschrijving** wordt ongewijzigd gebruikt op veel plaatsen in de voorgestelde tekst, dus het is belangrijk dat de beschrijving het beste weergeeft hoe u wilt verwijzen naar het artikel in de marketingtekst. 

3. Zorg ervoor dat het veld **Artikelcategoriecode** op de artikelkaart is ingesteld op de juiste categorie.

   Copilot zoekt naar woorden en zinsdelen die verband houden met de categorie en verwerkt deze in de voorgestelde tekst.

## Een geheel nieuwe marketingtekst maken

1. Open in Business Central het artikel dat u wilt wijzigen als volgt:

    1. Selecteer in de rechterbovenhoek het pictogram ![Lampje dat de functie Vertel me opent 22](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling om een lijst met beschikbare artikelen weer te geven.
    2. Om het artikel te openen dubbelklikt u erop of selecteert u in het veld **Nr.** het nummer ervan.

2. Ga op een van de volgende manieren te werk:

   - Selecteer in het deelvenster **Marketingtekst** in het feitenblok aan de rechterkant van de pagina **Bewerken**.
   - Selecteer de actie **Marketingtekst**.
3. Wijzig de tekst rechtstreeks in het vak **Marketingtekst** . Gebruik de werkbalk onderaan het vak om tekst op te maken, koppelingen toe te voegen en meer.
4. Als u klaar bent, selecteert u **Opslaan** om de tekst op te slaan.

## Zie ook

[Overzicht van op AI gebaseerde artikelmarketingtekst met Copilot configureren](ai-overview.md)  
[Door AI aangestuurde artikelmarketingtekst met Copilot configureren](enable-ai.md)  
[Veelgestelde vragen over op AI gebaseerde artikelmarketingtekst met Copilot](ai-faq.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  