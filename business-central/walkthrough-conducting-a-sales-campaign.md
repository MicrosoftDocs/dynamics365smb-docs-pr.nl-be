---
title: Procedure voor een verkoopcampagne uitvoeren
description: Dit overzicht geeft een gedetailleerd overzicht van alle taken die betrokken zijn bij het uitvoeren van een verkoopcampagne in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 01/31/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Procedure voor een verkoopcampagne uitvoeren

Een campagne heeft betrekking op alle activiteiten waarbij meerdere contacten zijn betrokken. Een belangrijk deel van het opzetten van een campagne bestaat uit het selecteren van de doelgroep voor de campagne. In [!INCLUDE[prod_short](includes/prod_short.md)] maakt u hiervoor met behulp van filters een segment, oftewel een groep contacten.  

 U kunt de voorzieningen van Verkoop &amp; Marketing gebruiken om de marketingactiviteiten zorgvuldig te plannen en uw interacties met contacten en klanten te beheren. U kunt campagnes maken en segmenten met contacten instellen voor mailings en andere soorten interacties voor contacten en toekomstige klanten.  

 Met de campagne- en segmentfuncties en de bijbehorende geautomatiseerde processen kunt u uw marketingactiviteiten plannen, organiseren en bijhouden. Op deze manier maakt u meer kans op het binnenhalen van nieuwe klanten en het vasthouden van bestaande klanten.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure

 In deze procedure wordt het proces beschreven voor de follow-up na een beurs en het benaderen van mogelijke klanten (contacten) in een follow-upcampagne.  

 Het overzicht introduceert de functie voor het beheren van campagnes en segmenten in de afdeling Verkoop &amp; Marketing. In deze procedure worden de volgende taken beschreven:  

- De gegevens voorbereiden.
- Een campagne instellen.  
- De doelgroep kiezen.  
- Gegevens toepassen.  
- Brieven naar contacten verzenden.  
- Reacties op de campagne registreren.  

## <a name="roles"></a>Rollen

 In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

- Marketingmanager of verkoopmanager  
- Marketingmedewerker  

## <a name="prerequisites"></a>Vereisten

 Voordat u de stappen in dit overzicht kunt uitvoeren, moet u [!INCLUDE[prod_short](includes/prod_short.md)] installeren.  

## <a name="story"></a>Scenario

 De marketingmanager van de verkoopafdeling van CRONUS is verantwoordelijk voor het plannen en uitvoeren van campagnes. De marketingmanager neemt ook beslissingen over aan welke beurzen het bedrijf deelneemt en hij evalueert de voortgang van de campagne.  

 De marketingmedewerker van de marketingafdeling verzorgt het produceren, distribueren en plaatsen van het marketingmateriaal.  

 Het bedrijf heeft een nieuw product geïntroduceerd met de naam Rome Guest Chair. Het product is onlangs gepromoot op de Office Futurus-beurs. Veel klanten waren zeer geïnteresseerd in het product en als onderdeel van de promotiecampagne krijgen klanten die tijdens de campagneperiode een Rome Guest Chair aanschaffen, een speciale campagneprijs aangeboden.  

 Een van de taken van de marketingmedewerker na de beurs is het invoeren van alle mogelijke klanten als contacten in het systeem.  

 De marketingmanager stelt een campagne in, maakt een segment met alle nieuwe contacten en gebruikt vervolgens de contactgegevens om de doelgroep voor de campagne te selecteren.  

 De medewerker helpt bij het verzenden van de bedankbrieven naar de contacten die een visitekaartje hebben achtergelaten bij de beursstand en ten slotte registreert de manager alle reacties die ze ontvangen van de mogelijke klanten.  

## <a name="setting-up-a-campaign"></a>Een campagne instellen

 Nadat de medewerker de visitekaartjes heeft ingevoerd die op de beurs zijn afgegeven, stelt de marketingmanager een campagnekaart in om de activiteiten voor de campagne te beheren.  

### <a name="to-set-up-a-campaign"></a>Een campagne instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Campagnes** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** om een nieuwe campagne te maken. Ga naar de campagnekaart en druk op <kbd>Enter</kbd> om automatisch een campagnenummer in te voegen.  
3. Geef in het veld **Omschrijving** een omschrijving op voor de campagne, bijvoorbeeld **Office Futurus-beurs**.  
4. Kies het veld **Statuscode** en selecteer de statuscode "1-PLAN". 
5. Vul de velden **Begindatum** en **Einddatum** van de campagne in.  

## <a name="selecting-the-target-audience"></a>De doelgroep kiezen

 De marketingmanager maakt een segment om de contacten te selecteren waarmee hij of zij wil werken.  
 
 Wanneer u een segment maakt, kunt u verschillende criteria gebruiken om de contacten te selecteren die doelen voor het segment moeten zijn. U kunt bijvoorbeeld contactpersonen selecteren die met de site van een klant of prospect werken en verantwoordelijk zijn voor de inkopen van hun bedrijf. Met filters kunt u contactpersonen toevoegen die voldoen een de criteria die het meest geschikt voor de doelen waarvoor u ze wilt gebruiken. Gebruik filters om contacten toe te voegen, bijvoorbeeld op basis van hun functie, de zakelijke relatie of de branche van het contactbedrijf. Kies in deze procedure het filter **Functiegroep** om contacten te selecteren.

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Een segment maken met de relevante contacten

1. Kies de actie **Navigeren** en kies vervolgens **Segmenten**.  
2. Kies de actie **Nieuw** om een nieuw segment te maken. Ga naar de segmentkaart en selecteer **Enter** om automatisch een segmentnummer in te voegen.  
3. Geef op het sneltabblad **Algemeen** in het veld **Omschrijving** bijvoorbeeld *Bezoekers van Office Futurus-beurs* op.
4. Kies de actie **Contacten toevoegen** om het filter **Contacten toevoegen** te openen.  
5. Schuif omlaag naar het sneltabblad **Contact functiegroep**, selecteer het filter **Inkoop** als de **Functiegroepcode** en kies de knop **OK**.  

De pagina **Segment** bevat nu een lijst met contacten op basis van het ingevoerde filter. Op het sneltabblad **Algemeen** in het veld **Aantal regels** ziet u in een oogopslag het aantal contactpersonen dat aan deze criteria voldoet.  

> [!NOTE]  
> U kunt uw segmentatiecriteria opslaan, zodat u ze later weer kunt gebruiken.

### <a name="to-save-your-segmentation-criteria"></a>Uw segmentatiecriteria opslaan

1. Kies op de pagina **Segment** de optie **Acties**.
2. Kies **Functies**, vervolgens **Segment** en kies dan de actie **Criteria opslaan**.  
3. Typ op de pagina **Segmentcriteria opslaan** een code voor het segment. Voer in het veld **Beschrijving** een beschrijving van de segmentcriteria in.
4. Kies de knop **Ok**.  

## <a name="mining-the-data"></a>Gegevens toepassen

 De marketingmanager bekijkt de gesegmenteerde lijst met contacten en ziet dat de lijst veel te lang is. De manager besluit de lijst te verkleinen op basis van daadwerkelijke, potentiële klanten om zich op de juiste doelgroep te richten. Het proces van het verfijnen en/of beperken van de gegevens wordt ook 'data mining' genoemd.  

### <a name="to-remove-contacts-from-the-segment"></a>Contacten uit het segment verwijderen

1. Kies op de pagina **Segment** de optie **Acties**.
2. Kies op de menubalk hieronder **Functies**, kies **Contacten** en kies dan **Contacten reduceren**.  

  Het dialoogvenster **Contacten verwijderen - verminderen** wordt geopend.  
4. Selecteer op het sneltabblad **Zakenrelatie contact** het filter **KLT** als de **zakenrelatiecode** en kies de knop **OK**.

 De pagina **Segment** bevat nu een ingekorte lijst met contacten en in het veld **Aantal regels** ziet u het aantal contacten dat nu aan deze nieuwe criteria voldoet.  

 > [!NOTE]  
 > Als u om welke reden dan ook het verwijderen van een groep contacten ongedaan wilt maken, doet u dit met de functie **Ga terug**. Met andere woorden,u kunt uw laatste segmentatie ongedaan maken.  

### <a name="to-bring-back-the-removed-contacts"></a>De verwijderde contacten terughalen

1. Kies op de pagina **Segment** de actie **Segment**.
2. Kies de actie **Ga terug**.

De contactpersonen die u hebt verwijderd worden weer toegevoegd aan de lijst met contactpersonen.

## <a name="linking-a-segment-to-a-campaign"></a>Een segment aan een campagne koppelen

De marketingmanager besluit dat de gereduceerde lijst de definitieve lijst met contacten is die hij of zij in de campagne wil opnemen. Daarom koppelt hij of zij dit segment aan de campagne FUTURUS-beurs.  

### <a name="to-link-a-segment-to-the-campaign"></a>Een segment aan de campagne koppelen

1. Kies op de pagina **Segment** op het sneltabblad **Campagne** het veld **Campagnenr.** om de campagne te selecteren waaraan u het segment wilt koppelen, bijvoorbeeld, **CP0001**.
2. Selecteer **Ja**.  
3. Aangezien dit segment de doelgroep van de campagne is, schakelt u het selectievakje **Campagnedoel** in en kiest u **Ja**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Brieven en e-mailberichten verzenden naar contactpersonen

 De marketingmedewerker helpt de marketingmanager om correspondentie naar de prospects te verzenden waarin ze bedankt worden voor hun bezoek aan de beurs.

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Een segment gebruiken om een brief naar een contactpersoon te verzenden

> [!NOTE]  
> In deze procedure moet u een Word-document bijvoegen. U kunt bijlagen in elke taal toevoegen.

> [!NOTE]  
> Klik indien nodig op het pictogram **Potlood** om de pagina in de bewerkingsmodus te openen.

1. Open de **Segment**kaart voor de **Bezoekers aan de FUTURUS-beurs**.  
2. Selecteer op het sneltabblad **Interactie** in het veld **Interactiesjablooncode** de sjablooncode **BUS** voor zakenbrieven en selecteer **Ja**.
3. Open de pagina **Segmentinteractietalen** door het veld **Taal (Standaard)** te kiezen. Selecteer een **taalcode** en kies de knop **OK**.
4. Zorg ervoor dat **Correspondentietype (standaard)** is ingesteld op **Afdruk**.
5. Selecteer in het veld **Bijlage** het vak met het **beletselteken**. Dit opent het dialoogvenster Bijlage importeren.
    1. Selecteer de knop **Kiezen** om uw bestand te kiezen.
    1. Zoek het bestand en selecteer de knop **Openen** knop om het bij te voegen.
6. Typ in het veld **Onderwerp (Standaard)** bijvoorbeeld de volgende tekst: **Bedankt voor uw bezoek aan de beurs**. Druk op de <kbd>Tab</kbd>-toets om het veld te verlaten en selecteer de knop **Ja**.
7. Schuif **Word-doc. als bijlage verzenden** naar aan en selecteer de knop **Ja**.
8. Kies de actie **Registreren**. Schakel in het pop-upvenster Segment registreren het volgende in: **Opvolgingssegment maken**
9. Kies de knop **OK** om de **batchverwerking Segment registreren** te starten.  

De bijlagen worden verzonden. Wanneer het proces is voltooid, kiest u de knop **OK** voor het bericht dat aangeeft dat het segment is geregistreerd.  

 De brieven worden automatisch afgedrukt en het segment wordt geregistreerd. Omdat het segment is geregistreerd, staat het niet langer in de lijst met segmenten maar is het verplaatst naar de lijst met geregistreerde segmenten. Als u die lijst wilt zien, kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geregistreerde segmenten** in en kies vervolgens de gerelateerde koppeling.  

Nadat het segment is geregistreerd, wordt elke brief die wordt verzonden geregistreerd als een interactie, die u in het logboek kunt bekijken.  

Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Interactielogposten** in en kies vervolgens de gerelateerde koppeling. Er is een vermelding voor elke verzonden brief.  

### <a name="to-send-an-email-message-to-a-contact"></a>Een e-mailbericht verzenden naar een contactpersoon

1. Selecteer op het sneltabblad **Interactie** in het veld **Interactiesjablooncode** de sjabloon **BUS** (zakenbrief, business letter).  
2. Typ in het veld **Onderwerp (Standaard)** bijvoorbeeld de volgende tekst: **Bedankt voor uw bezoek aan de beurs**.  
3. Kies in het veld **Correspondentietype** de optie **E-mail**.  
4. Geef de taalinstellingen op en voeg een Word-document toe, zoals in de vorige procedure.  
5. Kies de actie **Registreren**. De pagina **Segment registreren** wordt geopend.  
6. Schakel het selectievakje **Bijlagen verzenden** in om de bijlagen te laten verzenden per e-mail.  
7. Schakel het selectievakje **Opvolgingssegm. maken** in.  
8. Kies de knop **OK**.  

 De brieven worden automatisch per e-mail verzonden en het segment wordt geregistreerd. Omdat het segment is geregistreerd, staat het niet langer in de lijst met segmenten maar is het opgeslagen in de lijst met geregistreerde segmenten. Als u die lijst wilt zien, kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geregistreerde segmenten** in en kies vervolgens de gerelateerde koppeling.  

## <a name="register-campaign-responses"></a>Campagnerespons vastleggen

 De prospects reageren in de volgende weken op de brief. De marketingmanager wil de reacties bijhouden en registreert deze in het programma.  

 Stel hiervoor een segment in voor de contacten die op de brief hebben gereageerd.  

### <a name="to-register-campaign-responses"></a>Campagnerespons vastleggen

1. Kies op de pagina **Segment** op het sneltabblad **Interactie** het veld **Interactiesjablooncode**.  

 Er is geen interactiesjabloon voor het vastleggen van de respons op campagnes. Maak dus een nieuwe sjabloon.  

2. Kies in de vervolgkeuzelijst **Interactiesjablonen** de actie **Nieuw** .  
3. Typ **RESP** in het veld **code** en **Campagnerespons** in het veld **Omschrijving**.  
4. Kies de knop **Ok**.
5. Kies **Ja** om te bevestigen dat u deze interactiesjablooncode op alle segmentlijnen wilt toepassen.
6. Ga naar het sneltabblad **Campagne** en schakel het veld **Campagnerespons** in. Kies **Ja** om het bericht *U hebt campagnerespons gewijzigd* te bevestigen.  
7. Kies op de pagina **Segment** de optie **Registreren**.  
8. Wis op de pagina **Segment registreren** het selectievakje **Bijlagen verzenden**. Kies vervolgens de knop **OK** om het bericht te bevestigen dat het segment is geregistreerd.  
  
## <a name="see-also"></a>Zie ook
[Relatiebeheer](marketing-relationship-management.md)  
 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
