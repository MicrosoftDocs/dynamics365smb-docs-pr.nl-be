---
title: Goedkeuringswerkstromen maken om taken te verbinden
description: Leer hoe u werkstromen kunt maken om taken te verbinden die door verschillende mensen in bedrijfsprocessen worden uitgevoerd.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/29/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a>Werkstromen maken om taken in bedrijfsprocessen met elkaar te verbinden

U kunt werkstromen maken om taken in bedrijfsprocessen te verbinden die door verschillende gebruikers worden uitgevoerd. U kunt systeemtaken, zoals automatische boekingen, opnemen als stappen in werkstromen die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.  

Maak op de pagina **Werkstroom** een werkstroom door de stappen te vermelden op de regels. Elke stap bestaat uit een trigger en een respons:

* Een gebeurtenis die de voorwaarden specificeert die de werkstroom starten.
* Een werkstroomreactie die definieert wat de werkstroom doet.

[!INCLUDE[workflow](includes/workflow.md)]

Wanneer u werkstromen maakt, kunt u de stappen van bestaande werkstromen of van werkstroomsjablonen kopiëren. Werkstroomsjablonen zijn niet-bewerkbare werkstromen die [!INCLUDE[prod_short](includes/prod_short.md)] biedt. De identifiers voor werkstroomsjablonen krijgen het voorvoegsel 'MS-', zoals in 'MS-PIW'. Meer informatie op [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)  

> [!NOTE]  
> Alle berichten over werkstroomstappen worden verzonden via een taakwachtrij. Zorg ervoor dat de taakwachtrij uw zakelijke behoeften weerspiegelt. Zie voor meer informatie [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustratie van een werkstroomvoorbeeld.":::

Een werkstroom is onderverdeeld in drie secties:

1. **Als gebeurtenis**  
   Dit is waar de trigger wordt geselecteerd.  
   Voorbeelden van een trigger:
   * Een hoofdgegevensrecord is gewijzigd
   * Er wordt een dagboekregel gemaakt
   * Er wordt een inkomend document gemaakt of vrijgegeven
   * Er wordt goedkeuring van een document aangevraagd
2. **Op voorwaarde**  
   De **voorwaarden** zijn gerelateerd aan de gebeurtenis en maken het mogelijk filters te maken om te beslissen hoe de werkstroom doorgaat.
3. **Dan reactie**  
   De **reacties** specificeren de volgende stappen in de werkstroom.

De opties voor gebeurtenissen en responsen zijn door het systeem gedefinieerd. Om nieuwe opties toe te voegen, moet u een extensie ontwikkelen.

## <a name="to-create-a-workflow"></a>Een workflow maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. De pagina **Werkstroom** verschijnt.  
3. Voer in het veld **Code** maximaal 20 tekens in om de werkstroom te identificeren.  
4. Als u de werkstroom wilt maken vanuit een werkstroomsjabloon, kiest u op de pagina **Werkstromen** de actie **Nieuwe werkstroom uit sjabloon**. Meer informatie op [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)  
5. Beschrijf de werkstroom in het veld **Omschrijving**.  
6. Geef in het veld **Categorie** op tot welke categorie de werkstroom hoort.  
7. Geef in het veld **Als gebeurtenis** de gebeurtenis op die zich moet voordoen om de werkstroomstap te starten.  

   Als u het veld kiest, bevat de pagina **Werkstroomgebeurtenissen** alle beschikbare werkstroomgebeurtenissen.  
8. Geef in het veld **Op voorwaarde** een of meer voorwaarden op waaraan moet worden voldaan voordat de gebeurtenis in het veld **Als gebeurtenis** zich kan voordoen.  

   Wanneer u het veld kiest, bevat de pagina **Gebeurtenisvoorwaarden** filtervelden die voorwaarden voor de gebeurtenis kunnen zijn. U kunt desgewenst nieuwe filtervelden toevoegen.  

   Als de werkstroomgebeurtenis de wijziging van een specifiek veld in een record is, gebruikt u de pagina **Gebeurtenisvoorwaarden** om het veld en het type wijziging te selecteren.  

   1. Als u een veldwijziging voor de gebeurtenis wilt opgeven, selecteert u op de pagina **Gebeurtenisvoorwaarden** in het veld **Veld** die wijziging.  
   2. Selecteer in het veld **Operator** **Afgenomen**, **Toegenomen** of **Aangepast**.  
9. Geef in het veld **Dan reactie** het antwoord op dat volgt als de werkstroomgebeurtenis plaatsvindt.  

   Als u het veld kiest, bevat de pagina **Werkstroomreacties** alle beschikbare werkstroomreacties en responsopties.  
10. Op het sneltabblad **Opties voor de geselecteerde reactie** geeft u als volgt opties op voor de werkstroomreactie door waarden te selecteren in de verschillende velden die verschijnen:  

    1. Als u opties voor een werkstroomantwoord wilt opgeven waarbij het gaat om het verzenden van een melding, vult u de velden in de volgende tabel in.  

    > [!NOTE]
    > Deze velden variëren, afhankelijk van het door u gekozen antwoord.

       |Veld|Omschrijving|
       |-----|-----------|
       |**Afzender informeren**|Geef op of de aanvrager van de goedkeuring op de hoogte wordt gebracht in plaats van de ontvanger van de goedkeuringsaanvraag. Als u het selectievakje inschakelt, wordt het veld **Gebruikers-id ontvanger** uitgeschakeld omdat de aanvrager van de goedkeuring, de afzender, wordt geïnformeerd in plaats van de ontvanger. De naam van de werkstroomreactie verandert dienovereenkomstig in **Maak een bericht voor &lt;afzender&gt;**. Als het selectievakje niet is ingeschakeld, is de naam van de werkstroomreactie **Maak een bericht voor &lt;gebruiker&gt;**.|
       |**Gebruikers-id ontvanger**|Geef de gebruiker op die het bericht moet ontvangen. **Opmerking**: deze optie is alleen beschikbaar voor werkstroomreacties met een tijdelijke aanduiding voor een bepaalde gebruiker. Voor werkstroomreacties zonder tijdelijke aanduidingen voor gebruikers wordt de meldingsontvanger meestal bepaald door de **Gebruikersinstellingen voor goedkeuring**.|
       |**Type berichtitem**|Geef een trigger op voor het werkstroombericht. De trigger kan een recordwijziging, een goedkeuringsverzoek of een verstreken vervaldatum zijn.|
       |**Doelpagina van koppeling**|Geef de pagina op waarop de koppeling in het bericht wordt geopend. De pagina moet dezelfde brontabel moet hebben als de betrokken record.|
       |**Aangepaste koppeling**|Geef de URL op van een koppeling die wordt opgenomen in het bericht, naast de koppeling naar de pagina.|

    2. Als u opties voor een werkstroomantwoord wilt opgeven waarbij het gaat om het maken van een goedkeuringsaanvraag, vult u de velden in de volgende tabel in.  

       |Veld|Omschrijving|  
       |-----|-----------|  
       |**Formule van vervaldatum**|Geef het aantal dagen op dat de fiatteur heeft om het verzoek op te lossen. De termijn gaat in op het moment dat het verzoek is verzonden.|
       |**Delegeren na**|Geef op of en wanneer een goedkeuringsaanvraag automatisch aan de vervanger wordt gedelegeerd. U kunt selecteren dat één, twee of, vijf dagen na de datum automatisch wordt gedelegeerd als de goedkeuring is aangevraagd.|
       |**Soort fiatteur**|Geef op wie de fiatteur is, op basis van de instellingen voor goedkeuringsgebruikers en werkstroomgebruikers. Wanneer het veld is ingesteld op **Verkoper/Inkoper**, bepaalt de gebruiker die is opgegeven in het veld **Verkoper/inkoper** op de pagina **Gebruikersinstellingen voor goedkeuring**, de fiatteur. Goedkeuringsaanvragen worden vervolgens gemaakt op basis van de waarde in het veld **Limietsoort van fiatteur**. Meer informatie op [Goedkeuringsgebruikers instellen](across-how-to-set-up-workflow-users.md).|
       |**Bevestigingsbericht tonen**|Geef op of er een bevestigingsbericht wordt weergegeven nadat een gebruiker een goedkeuring heeft aangevraagd.|
       |**Limietsoort van fiatteur**|Specificeer het effect van limieten voor fiatteurs. De goedkeuringslimiet van een fiatteur moet hoger zijn dan de waarde in het verzoek. De volgende opties zijn mogelijk: <ol><li>**Fiatteursketen** geeft aan dat posten voor goedkeuringsaanvragen worden gemaakt voor alle fiatteurs van de aanvrager tot en met de eerste gekwalificeerde fiatteur.</li><li>**Directe fiatteur** geeft aan dat een goedkeuringsaanvraagpost alleen wordt gemaakt voor de directe fiatteur van de aanvrager, ongeacht de goedkeuringslimiet van de fiatteur.</li><li>**Eerste gekwalificeerde fiatteur** geeft aan dat een goedkeuringsaanvraagpost alleen wordt gemaakt voor de eerste fiatteur van de aanvrager.</li><li>**Specifieke fiatteur** geeft aan dat u de in het veld **Fiatteur-id** gekozen gebruiker op de hoogte stelt.</li></ol>|

    3. Als u opties voor een werkstroomantwoord wilt opgeven waarbij het gaat om het maken van dagboekregels vult u de velden in de volgende tabel in.  

       |Veld|Omschrijving|  
       |-----|-----------|  
       |**Sjabloonnaam van financieel dagboek**|Geef de naam op van de dagboeksjabloon die binnen de opgegeven dagboekregels worden gemaakt.|  
       |**Batchnaam van financieel dagboek**|Geef de naam op van de dagboekbatch die binnen de opgegeven dagboekregels worden gemaakt.|  

11. Kies de knop **Inspringing vergroten** en **Inspringing verkleinen** om de gebeurtenisnaam in het veld **Als** in te laten springen om de positie van de stap in de werkstroom bepalen.  

    1. Laat de gebeurtenis inspringen onder de naam van de vorige stap om aan te geven dat dit de volgende stap is.  
    2. Geef aan dat de stap een van meerdere alternatieve stappen is die afhankelijk van de voorwaarde ervan, kunnen beginnen, door de gebeurtenisnaam op dezelfde inspringing te plaatsen als de andere alternatieve stappen. Rangschik dergelijke optionele stappen overeenkomstig de prioriteit door de belangrijkste stap eerst te plaatsen.  

    > [!NOTE]  
    >  U kunt alleen de inspringing van een stap wijzigen als er geen verdere stap is.  

12. Herhaal stap 7 t/m 11 om meer werkstroomstappen toe te voegen, voor of na de stap die u hebt gemaakt.  
13. Schakel het selectievakje **Geactiveerd** in om aan te geven dat de werkstroom wordt gestart wanneer de gebeurtenis in de eerste stap van het type **Startpunt** plaatsvindt. Zie voor meer informatie [Werkstromen gebruiken](across-use-workflows.md).  

> [!NOTE]  
> Schakel een werkstroom pas in als u zeker weet dat deze gereed is.  

> [!TIP]  
> Als u relaties wilt verkennen tussen de tabellen die in werkstromen worden gebruikt, kiest u het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), en voert u vervolgens **Werkstroom – Tabelrelaties** in.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Voorbeeld van het maken van een nieuwe werkstroom met bestaande gebeurtenissen

In het volgende voorbeeld wordt een nieuwe werkstroom gemaakt om een wijziging in de naam van een leverancier goed te keuren:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. De pagina **Werkstroom** verschijnt.
3. Vul in het werkstroomgedeelte de velden in, zoals in de volgende tabel is beschreven.

    |Veld  |Waarde  |
    |---------|---------|
    |**Code**|**VENDAPN-01**|
    |**Beschrijving**|**Goedkeuring van naamswijziging van leverancier** |
    |**Categorie**|**INKOOP**|

4. Doe het volgende om de eerste werkstroomstap te maken.

    1. Geef in het veld **Als gebeurtenis** *Een leveranciersrecord is gewijzigd* op.  
    2. Kies in het veld **Op voorwaarde** de waarde **Altijd**. Kies dan op de pagina **Gebeurtenisvoorwaarden** de koppeling **Een voorwaarde toevoegen voor wanneer een veldwaarde verandert** en selecteer vervolgens het veld **Naam**. Het resultaat van deze stap is dat de voorwaarde luidt als *Naam is gewijzigd*.  
    3. Kies in het veld **Dan reactie** de koppeling **Reactie selecteren**. Kies dan op de pagina **Werkstroomreacties** in het veld **Reactie selecteren** de reactie **Draai de waarde van het veld \<Field\> op de record terug en sla de wijziging op**. Geef dan in de sectie **Opties voor de geselecteerde reactie** het veld **Naam** op.  
    4. Kies de koppeling **Meer reacties toevoegen** en voeg vervolgens een item toe voor de reactie **Maak een goedkeuringsaanvraag voor de record met fiatteurstype <%1> en reactie <%2>**.  
    5. Wijzig in het gedeelte **Opties voor de geselecteerde reactie** voor de nieuwe reactie het veld **Soort fiatteur** in **Werkstroomgebruikersgroep**. Geef vervolgens in het veld **Werkstroomgebruikersgroep** de gebruikersgroep op. Meer informatie op [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  
    6. Voeg een derde reactie toe **Verzend goedkeuringsaanvraag voor de record en maak een bericht.**  
    7. Voeg een vierde respons toe, **Toon bericht %1**. Geef vervolgens in het gedeelte **Opties voor de geselecteerde reactie** in het veld **Bericht** **Er is een goedkeuringsaanvraag verzonden** op.  
    8. Kies **OK** om terug te gaan naar de werkstroomstap.  

5. Voeg op de volgende regel een nieuwe werkstroomstap toe voor de gebeurtenis **Er is een goedkeuringsaanvraag goedgekeurd**.

    1. Geef in het veld **Als gebeurtenis** **Er is een goedkeuringsaanvraag goedgekeurd** op.  
    2. Kies het regelmenu en kies vervolgens **Inspringing vergroten**.  
    3. Kies in het veld **Op voorwaarde** de waarde **Altijd**. Geef vervolgens in het veld **Wacht op goedkeuringen** **0** op. De voorwaarde leest als **Wacht po goedkeuringen:0** om aan te geven dat het verzoek niet meer fiatteurs nodig heeft.  
    4. Kies in het veld **Dan reactie** de koppeling **Reactie selecteren**. Kies dan in het veld **Reactie selecteren** op de pagina **Werkstroomreacties** de reactie **Verzend goedkeuringsaanvraag voor de record en maak een bericht**.  
    5. Klik op **OK**.  
6. Voeg op de volgende regel een tweede werkstroomstap toe voor de gebeurtenis **Er is een goedkeuringsaanvraag goedgekeurd**.  

    1. Geef in het veld **Als gebeurtenis** **Er is een goedkeuringsaanvraag goedgekeurd** op.
    2. Kies in het veld **Op voorwaarde** de waarde **Altijd**. Geef vervolgens in het veld **Wacht op goedkeuringen** **>0** op. De voorwaarde leest als **Wacht op goedkeuringen:>0** om aan te geven dat dit niet de laatste fiatteur is.  
    3. Kies in het veld **Dan reactie** de koppeling **Reactie selecteren**. Kies dan in het veld **Reactie selecteren** op de pagina **Werkstroomreacties** de reactie **Verzend goedkeuringsaanvraag voor de record en maak een bericht**.  
    4. Klik op **OK**.  
7. Voeg op de volgende regel een werkstroomstap toe voor de gebeurtenis **Er is een goedkeuringsaanvraag gedelegeerd**.  

    1. Geef in het veld **Als gebeurtenis** **Er is een goedkeuringsaanvraag gedelegeerd** op.  
    2. Laat in het veld **Op voorwaarde** de waarde **Altijd** staan.  
    3. Kies in het veld **Dan reactie** de koppeling **Reactie selecteren**. Kies dan in het veld **Reactie selecteren** op de pagina **Werkstroomreacties** de reactie **Verzend goedkeuringsaanvraag voor de record en maak een bericht**.  
    4. Klik op **OK**.  
8. Voeg op de volgende regel een tweede werkstroomstap toe voor de gebeurtenis **Er is een goedkeuringsaanvraag geweigerd**.  

    1. Geef in het veld **Als gebeurtenis** **Er is een goedkeuringsaanvraag geweigerd** op.  
    2. Laat in het veld **Op voorwaarde** de waarde **Altijd** staan.  
    3. Kies in het veld **Dan reactie** de koppeling **Reactie selecteren**. Kies dan, op de pagina **Werkstroomreacties** in het veld **Reactie selecteren** de reactie **Negeer de nieuwe waarden**.  
    4. Kies de koppeling **Meer reacties toevoegen** en voeg vervolgens een item toe voor de reactie **Weiger de goedkeuringsaanvraag voor de record en maak een bericht**
    5. Klik op **OK**.  
9. Zet de schakelaar **Geactiveerd** aan om de werkstroom in te schakelen.  

De volgende illustratie geeft een overzicht van het resultaat van deze procedure.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustratie van de werkstroom voor goedkeuring van leveranciersnaam.":::

Test vervolgens de werkstroom door een bestaande leverancierskaart te openen en de naam te wijzigen. Controleer of er een goedkeuringsverzoek is verzonden na het wijzigen van de leveranciersnaam.

## <a name="see-also"></a>Zie ook

[Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)  
[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Goedkeuringswerkstroomberichten instellen](across-setting-up-workflow-notifications.md)  
[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md)  
[Goedkeuringswerkstromen verwijderen](across-how-to-delete-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
