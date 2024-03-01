---
author: brentholtorf
ms.topic: include
ms.date: 02/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
U kunt aanmaningen gebruiken om klanten te herinneren aan openstaande bedragen. U kunt aanmaningen ook gebruiken om aanmaningskosten zoals rente en boetes te berekenen en deze op te nemen op de aanmaning.

Voor u aanmaningen kunt maken, moet u aanmaningscondities instellen en deze toewijzen aan uw klanten. Zie voor meer informatie [De termijnen en niveaus van aanmaningen instellen](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] De inhoud van de pagina **Rentefactuurcondities** bepaalt of er rente in rekening wordt gebracht op de aanmaning.  

U kunt de batchverwerking **Aanmaningen maken** periodiek uitvoeren om aanmaningen te maken voor alle klanten met achterstallige saldo's, of u kunt handmatig een aanmaning maken voor een specifieke klant en de regels automatisch laten uitrekenen en invullen.  

Nadat u de aanmaningen hebt gemaakt, kunt u ze aanpassen. De tekst die wordt afgedrukt aan het begin of eind van een aanmaning wordt bepaald door de aanmaningscondities en kan worden bekeken in de kolom **Omschrijving**. Als een berekend bedrag automatisch is ingevoegd in de begin-, of eindtekst, wordt de tekst niet aangepast wanneer u regels verwijdert. In dat geval moet u de functie **Aanmaningstekst bijwerken** gebruiken.  

Voor een klantpost waarbij het veld **Afwachten** is ingevuld wordt geen aanmaning gemaakt. Als er echter een aanmaning wordt gemaakt op basis van een andere post, wordt een wachtende post ook opgenomen op de aanmaning. Er wordt geen rente berekend op regels met deze posten.

Nadat u aanmaningen hebt gemaakt en eventuele aanpassingen hebt gedaan, kunt u testrapporten afdrukken of de aanmaningen versturen, meestal als e-mail.

### <a name="to-create-a-reminder-automatically"></a>Automatisch een aanmaningen maken

Een herinnering is te vergelijken met een factuur. Wanneer u een aanmaning maakt, moeten een aanmaningskop, evenals een of meer aanmaningsregels, worden ingevuld. U kunt een functie gebruiken om automatisch aanmaningen te maken voor alle klanten.

1. Kies het pictogram ![Lampje dat de functie Vertel me 0 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Aanmaning** de actie **Aanmaningen maken**.
3. Vul op de pagina **Aanmaningen maken** de velden in om te definiëren hoe en naar wie de aanmaningen worden gemaakt.
4. Kies de knop **OK**.

### <a name="to-create-a-reminder-manually"></a>Handmatig aanmaningen maken

Op de pagina **Aanmaning** kunt u het sneltabblad **Algemeen** handmatig invullen en de regels vervolgens automatisch laten invullen.

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 weer opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op het sneltabblad **Algemeen** in.
4. Kies de actie **Aanmaningsregels voorstellen**.
5. Vul in de batchverwerking **Aanmaningsregels voorstellen** de velden in om te definiëren hoe en naar wie de aanmaningen worden gemaakt.
6. Schakel het selectievakje **Wachtende posten opnemen** in als ook u wachtende, openstaande posten wilt opnemen in de aanmaningen.
7. Schakel het selectievakje **Alleen vervallen posten** in als u alleen vervallen, open posten wilt opnemen in de aanmaningen. Alleen facturen en betalingen worden weergegeven, aangezien dit de posten zijn waarvoor betalingen van uw klanten mogelijk te laat zijn.

    > [!Important]
    > Open posten die in de wacht staan, worden ingevoegd, ongeacht de instelling van het selectievakje **Alleen vervallen posten**.

8. Kies de knop **OK**.

### <a name="to-replace-reminder-texts"></a>Aanmaningsteksten vervangen

U kunt op verschillende manieren bepalen hoe u tekst wilt weergegeven op de afgedrukte aanmaning. In sommige gevallen kunt u de begin- en eindtekst die u hebt gedefinieerd voor het huidige niveau vervangen door de tekst van een ander niveau.

1. Kies het pictogram ![Lampje dat de functie Vertel me 3 weer opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies vervolgens de gerelateerde koppeling.
2. Open de relevante aanmaning en kies de actie **Aanmaningstekst bijwerken**.
3. Voer op de pagina **Aanmaningstekst bijwerken** het vereiste niveau in het veld **Aanmaningsniveau** in.
4. Klik op **OK** om de begin- en eindtekst bij te werken.

### <a name="to-issue-a-reminder"></a>Een aanmaning verzenden

Nadat u aanmaningen hebt gemaakt en eventuele aanpassingen hebt gedaan, kunt u testrapporten afdrukken of de aanmaningen versturen.

Wanneer u een aanmaning verstuurt, worden de gegevens overgebracht naar een afzonderlijke pagina voor verstuurde aanmaningen. Tegelijkertijd worden aanmaningsposten geboekt. Als er rente of aanmaningskosten in rekening zijn gebracht worden posten zowel geboekt als klantpost als in het grootboek.

Wanneer een aanmaning is verzonden, worden de posten geboekt volgens uw specificaties op de pagina **Aanmaningscondities**. Op basis van deze specificatie wordt bepaald welke rente en/of toeslagen worden geboekt naar de klantenrekening en het grootboek. De instelling op de pagina **Klantboekingsgroepen** bepaalt naar welke rekening de boekingen worden uitgevoerd.

Voor elke klantenpost op de rentefactuur wordt een post gemaakt op de pagina **Aanmanings-/rentefactuurposten**.

Als de selectievakjes **Rente boeken** of **Toeslag boeken** op de pagina **Aanmaningscondities** zijn ingeschakeld, worden ook de volgende posten gemaakt:

- Eén post op de pagina **Klantenposten**
- Eén debiteurenpost in de desbetreffende grootboekrekening
- Eén rentepost en/of één toeslagpost in de desbetreffende grootboekrekening

Daarnaast kunnen btw-posten worden gemaakt als u de aanmaning verzendt.

1. Kies het pictogram ![Lampje dat de functie Vertel me 4 ook hier opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de desbetreffende aanmaning en kies vervolgens de actie **Verzenden**.
3. Vul op de pagina **Aanmaningen verzenden** de benodigde velden in.
4. Kies de knop **Ok**.

Een aanmaning wordt afgedrukt of verzonden naar een opgegeven e-mailadres als PDF-bijlage.

### <a name="to-cancel-an-issued-reminder"></a>Een verzonden aanmaning annuleren

Als aanmaningen ten onrechte zijn uitgegeven, kunt u ze annuleren voordat ze worden verzonden. U kunt dit één voor één of als een batch doen.

1. Selecteer op de pagina **Verzonden aanmaningen** een of meer regels voor verzonden aanmaningen die u wilt annuleren en kies vervolgens de actie **Annuleren**.
2. Vul op de pagina **Verzonden aanmaningen annuleren** desgewenst de velden in en kies vervolgens de knop **OK**.


