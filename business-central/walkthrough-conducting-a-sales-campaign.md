---
title: 'Procedure: Een verkoopcampagne uitvoeren | Microsoft Docs'
description: Een campagne heeft betrekking op alle activiteiten waarbij meerdere contacten zijn betrokken. Een belangrijk deel van het opzetten van een campagne bestaat uit het selecteren van de doelgroep voor de campagne. In Business Central maakt u hiervoor met behulp van filters een segment, oftewel een groep contacten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7b9bfeea6a4a3f93559d49319257053aef2f7bec
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "934176"
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Procedure: Een verkoopcampagne uitvoeren
Een campagne heeft betrekking op alle activiteiten waarbij meerdere contacten zijn betrokken. Een belangrijk deel van het opzetten van een campagne bestaat uit het selecteren van de doelgroep voor de campagne. In [!INCLUDE[d365fin](includes/d365fin_md.md)] maakt u hiervoor met behulp van filters een segment, oftewel een groep contacten.  

 U kunt de voorzieningen van Verkoop &amp; Marketing gebruiken om de marketingactiviteiten zorgvuldig te plannen en uw interacties met contacten en klanten te beheren. U kunt campagnes maken en segmenten met contacten instellen voor mailings en andere soorten interacties voor contacten en toekomstige klanten.  

 Met de campagne- en segmentfuncties en de bijbehorende geautomatiseerde processen kunt u uw marketingactiviteiten plannen, organiseren en bijhouden. Op deze manier maakt u meer kans op het binnenhalen van nieuwe klanten en het vasthouden van bestaande klanten.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure  
 In deze procedure wordt het proces beschreven voor de follow-up na een beurs en het benaderen van mogelijke klanten (contacten) in een follow-upcampagne.  

 Het overzicht introduceert de functie voor het beheren van campagnes en segmenten in de afdeling Verkoop &amp; Marketing. In deze procedure worden de volgende taken beschreven:  

-   Een campagne instellen.  
-   De doelgroep kiezen.  
-   Gegevens toepassen.  
-   Brieven naar contacten verzenden.  
-   Reacties op de campagne registreren.  

## <a name="roles"></a>Rollen  
 In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

-   Marketingmanager of verkoopmanager  
-   Marketingmedewerker  

## <a name="prerequisites"></a>Vereisten  
 Voordat u de stappen in dit overzicht kunt uitvoeren, moet u [!INCLUDE[d365fin](includes/d365fin_md.md)] installeren.  

## <a name="story"></a>Scenario  
 De marketingmanager van de verkoopafdeling van CRONUS is verantwoordelijk voor het plannen en uitvoeren van campagnes. Hij neemt ook beslissingen over de beurzen waaraan het bedrijf deelneemt en hij evalueert de voortgang van de campagne.  

 De marketingmedewerker van de marketingafdeling verzorgt het produceren, distribueren en plaatsen van het marketingmateriaal.  

 Het bedrijf heeft net een nieuw product geïntroduceerd met de naam Millennium Server. Het product is onlangs gepromoot op de Computer Futurus-beurs. Veel klanten waren zeer geïnteresseerd in het product en als onderdeel van de promotiecampagne krijgen klanten die tijdens de campagneperiode een Millennium Server aanschaffen, een speciale campagneprijs aangeboden.  

 Een van de taken van de marketingmedewerker na de beurs is het invoeren van alle mogelijke klanten als contacten in het systeem.  

 De marketingmanager stelt een campagne in, maakt een segment met alle nieuwe contacten en gebruikt vervolgens de contactgegevens om de doelgroep voor de campagne te selecteren.  

 De medewerker helpt bij het verzenden van de bedankbrieven naar de contacten die een visitekaartje hebben achtergelaten bij de beursstand en ten slotte registreert de manager alle reacties die ze ontvangen van de mogelijke klanten.  

## <a name="setting-up-a-campaign"></a>Een campagne instellen  
 Nadat de medewerker de visitekaartjes heeft ingevoerd die op de beurs zijn afgegeven, stelt de marketingmanager een campagnekaart in om de activiteiten voor de campagne te beheren.  

### <a name="to-set-up-a-campaign"></a>Een campagne instellen  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Campagnes** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw** om een nieuwe campagne te maken. Ga naar de campagnekaart en druk op Enter om automatisch een campagnenummer in te voegen.  
3.  Geef in het veld **Omschrijving** een omschrijving op voor de campagne, bijvoorbeeld **FUTURUS-beurs**.  
4.  Kies het veld **Statuscode** en selecteer een statuscode in de lijst die wordt geopend op de pagina **Campagnestatus**.  
5.  Vul de velden **Begindatum** en **Einddatum** van de campagne in.  

## <a name="selecting-the-target-audience"></a>De doelgroep selecteren  
 De marketingmanager maakt een segment om de contacten te selecteren waarmee hij wil werken.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Een segment maken met de relevante contacten  

1.  Kies de actie **Segmenten**.  
2.  Kies de actie **Nieuw** om een nieuw segment te maken. Ga naar de segmentkaart en druk op Enter om automatisch een segmentnummer in te voegen.  
3.  Geef in het sneltabblad **Algemeen** in het veld **Omschrijving** bijvoorbeeld **Bezoekers van FUTURUS-beurs** op.  

     Nadat u algemene informatie over het segment hebt ingevoerd, selecteert u de contacten die u in het segment wilt opnemen.  

     U kunt de contacten op basis van allerlei criteria selecteren, bijvoorbeeld contactpersonen die bij een bestaande klant of een prospect werken en verantwoordelijk zijn voor de inkopen van hun bedrijf.  

     Met filters kunt u contactpersonen toevoegen die voldoen een de criteria die het meest geschikt voor de doelen waarvoor u ze wilt gebruiken. Gebruik filters om contacten toe te voegen, bijvoorbeeld op basis van hun functie, de zakelijke relatie of de branche van het contactbedrijf. Kies in dit overzicht het filter **Functiegroep** om de contacten te selecteren.  

4.  Kies op de pagina **Segment** de actie **Contacten toevoegen** om het filter **Contacten toevoegen** te openen.  
5.  Selecteer in het sneltabblad **Functiegroep** het filter **Inkoop** als de **Functiegroepcode** en klik op **OK**.  

     De pagina **Segment** bevat nu een lijst met contacten op basis van het ingevoerde filter. Op het sneltabblad **Algemeen** in het veld **Aantal regels** ziet u in een oogopslag het aantal contactpersonen dat aan deze criteria voldoet.  

    > [!NOTE]  
    >  U kunt uw segmentatiecriteria opslaan, zodat u ze later weer kunt gebruiken.

    1.  Kies op de pagina **Segment** de actie **Segment** en kies vervolgens de actie **Criteria opslaan**.  
    2.  Typ op de pagina **Segmentcriteria opslaan** een code voor het segment. Voer in het veld **Beschrijving** een beschrijving van de segmentcriteria in.
    3.  Kies de knop **Ok**.  

## <a name="mining-the-data"></a>Gegevens toepassen  
 De marketingmanager bekijkt de gesegmenteerde lijst met contacten en ziet dat de lijst veel te lang is. Hij besluit de lijst in te korten op basis van echte prospects zodat hij zeker weet hij zich op de juiste doelgroep richt. Het proces van het verfijnen en/of beperken van de gegevens wordt ook 'data mining' genoemd.  

### <a name="to-remove-contacts-from-the-segment"></a>Contacten uit het segment verwijderen  

1.  Klik op de pagina **Segment** op de actie **Contacten** en vervolgens op **Contacten verminderen** om het filter **Contacten verwijderen -verminderen** te openen.  
2.  Selecteer in het sneltabblad **Functiegroep** het filter **PROS** als de **Zakenrelatiecode** en klik op **OK**.  

     De pagina **Segment** bevat nu een ingekorte lijst met contacten en in het veld **Aantal regels** ziet u het aantal contacten dat nu aan deze nieuwe criteria voldoet.  

    > [!NOTE]  
    >  Als u om welke reden dan ook het verwijderen van een groep contacten ongedaan wilt maken, doet u dit met de functie **Ga terug**. Met andere woorden,u kunt uw laatste segmentatie ongedaan maken.  
    >   
    >  Kies op de pagina **Segment** de actie **Segment** en kies vervolgens de actie **Ga terug**.  
    >   
    >  De contactpersonen die u zojuist hebt verwijderd worden weer toegevoegd aan de lijst met contactpersonen.  

## <a name="linking-a-segment-to-a-campaign"></a>Een segment aan een campagne koppelen  
 De marketingmanager besluit dat de beperkte lijst de definitieve lijst met contacten is die hij in de campagne wil opnemen. Daarom koppelt hij dit segment aan de campagne FUTURUS-beurs.  

### <a name="to-link-a-segment-to-the-campaign"></a>Een segment aan de campagne koppelen  

1.  Kies op de pagina **Segment** op het sneltabblad **Campagne** het veld **Campagnenr.** om de campagne te selecteren waaraan u het segment wilt koppelen, bijvoorbeeld, **CP0001**.  
2.  Aangezien dit segment de doelgroep van de campagne is, schakelt u het selectievakje **Campagnedoel** in.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Brieven en e-mailberichten verzenden naar contactpersonen  
 De marketingmedewerker helpt de marketingmanager om correspondentie naar de prospects te verzenden waarin ze bedankt worden voor hun bezoek aan de beurs.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Een segment gebruiken om een brief naar een contactpersoon te verzenden  

1.  Open de **Segment**kaart voor de **Bezoekers aan de FUTURUS-beurs**.  
2.  Selecteer op het sneltabblad **Interactie** in het veld **Interactiesjablooncode** de sjabloon **BUS** (zakenbrief, business letter).  
3.  Typ in het veld **Onderwerp (Standaard)** bijvoorbeeld de volgende tekst: **Bedankt voor uw bezoek aan de beurs**.  

    > [!NOTE]  
    >  Aan deze sjabloon zijn meerdere documenten gekoppeld, die elk in een andere taal zijn geschreven. Bijvoorbeeld in het Engels en het Deens.  

4.  Open de pagina **Segmentinteractietalen** door het veld **Taal (Standaard)** te kiezen. Selecteer een taalcode en kies de knop **OK**.  
5.  U kunt het document in de geselecteerde taal weergeven. Kies de actie **Bijlage** en kies vervolgens de actie **Openen**.  

     Reageer op het bericht waarin om toestemming wordt gevraagd om Word te starten door de optie **Toestaan voor deze clientsessie** te kiezen.  

     Hiermee opent u het bijgevoegde Word-document zodat u het kunt inspecteren. U kunt van deze gelegenheid gebruikmaken om de brief te bewerken en wijzigen. Sluit Word wanneer u gereed bent.  

6.  Typ het onderwerp van de brief in het veld **Onderwerp** in de taal die voor de sjabloon is geselecteerd.  
7.  Kies de actie **Registreren**.
8.  Kies het selectievakje **Bijlagen verzenden** om de bijlagen te laten afdrukken.  

    1. Schakel het selectievakje **Opvolgingssegm. maken** in.  
    2. Kies de knop **OK** om de batchverwerking **Segment registreren** te starten.  

9. De bijlagen worden verzonden. Wanneer het proces is voltooid, kiest u de knop **OK** voor het bericht dat aangeeft dat het segment is geregistreerd.  

     De brieven worden automatisch afgedrukt en het segment wordt geregistreerd. Omdat het segment is geregistreerd, staat het niet langer in de lijst met segmenten maar is het verplaatst naar de lijst met geregistreerde segmenten. Als u die lijst wilt zien, kiest u het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Geregistreerde segmenten** in en kiest u vervolgens de gerelateerde koppeling.  

10. Nadat het segment is geregistreerd, wordt elke brief die wordt verzonden geregistreerd als een interactie, die u in het logboek kunt bekijken.  

     Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Interactielogposten** in en kies vervolgens de gerelateerde koppeling. Er is een vermelding voor elke verzonden brief.  

### <a name="to-send-an-email-message-to-a-contact"></a>Een e-mailbericht verzenden naar een contactpersoon  

1.  Selecteer op het sneltabblad **Interactie** in het veld **Interactiesjablooncode** de sjabloon **BUS** (zakenbrief, business letter).  
2.  Typ in het veld **Onderwerp (Standaard)** bijvoorbeeld de volgende tekst: **Bedankt voor uw bezoek aan de beurs**.  
3.  Kies in het veld **Correspondentietype** de optie **E-mail**.  
4.  Geef taalinstellingen op, zoals in de vorige procedure.  
5.  Kies de actie **Registreren**. De pagina **Segment registreren** wordt geopend.  
6.  Schakel het selectievakje **Bijlagen verzenden** in om de bijlagen te laten verzenden per e-mail.  
7.  Schakel het selectievakje **Opvolgingssegm. maken** in.  
8.  Kies de knop **OK**.  

     De brieven worden automatisch per e-mail verzonden en het segment wordt geregistreerd. Omdat het segment is geregistreerd, staat het niet langer in de lijst met segmenten maar is het opgeslagen in de lijst met geregistreerde segmenten. Als u die lijst wilt zien, kiest u het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Geregistreerde segmenten** in en kiest u vervolgens de gerelateerde koppeling.  

## <a name="registering-campaign-responses"></a>Campagnerespons vastleggen  
 De prospects reageren in de volgende weken op de brief. De marketingmanager wil de reacties bijhouden en registreert deze in het programma.  

 Stel hiervoor een segment in voor de contacten die op de brief hebben gereageerd.  

### <a name="to-register-campaign-responses"></a>Campagnerespons vastleggen  

1.  Klik op de pagina **Segment** op het sneltabblad **Interactie**.  
2.  Kies het veld **Interactiesjablooncode**.  

     Er is geen interactiesjabloon voor het vastleggen van de respons op campagnes. Maak dus een nieuwe sjabloon.  

3.  Kies op de pagina **Interactiesjablonen** de actie **Nieuw** .  
4.  Typ **RESP** in het veld **code** en **Campagnerespons** in het veld **Omschrijving**.  
5.  Kies de knop **Ok**.  
6.  Selecteer deze interactiesjabloon in het veld **Interactiesjablooncode** en bevestig de vraag of u de segmentregels met dezelfde interactiesjablooncode wilt bijwerken.  

     Geef nu op dat deze contacten hebben gereageerd op de campagne:  
7.  Selecteer op het sneltabblad **Campagne** in het veld **Campagnenr.** uw campagne.  
8.  Verlaat het veld **Campagnenr.** en bevestig de vraag of u de segmentregels met dezelfde interactiesjablooncode wilt bijwerken.  
9. Selecteer het veld **Campagnerespons** en bevestig het volgende bericht.  

     Registreer het segment zodat u zeker weet dat de interacties worden vastgelegd.  
10. Kies op de pagina **Segment** de optie **Registreren**.  
11. Schakel op de pagina **Segment registreren** het selectievakje **Bijlagen verzenden** uit. Klik vervolgens op **OK** en bevestig het bericht dat verschijnt.  

     Nadat het segment is geregistreerd, wordt automatisch een post voor de campagne gemaakt op de pagina **Campagneposten** om deze actie vast te leggen.  

## <a name="see-also"></a>Zie ook  
[Relatiebeheer](marketing-relationship-management.md)  
 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
