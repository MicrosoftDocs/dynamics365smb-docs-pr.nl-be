---
title: Productieagenda's instellen
description: 'Het maken en inschakelen van een afdelingskalender omvat verschillende taken, waaronder het opzetten van productieagenda''s en het maken van ploegendiensten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9291, 9293, 9295, 99000750, 99000751, 99000752, 99000753, 99000759, 99000769, 99000770, 99000771, 99000772, 99000920'
ms.date: 06/22/2021
ms.author: edupont
---
# Productieagenda's instellen

Een afdelings- of bewerkingsplaatsagenda bevat de werkdagen en -tijden, de diensten, vakanties en afwezigheid die bepalend zijn voor de brutocapaciteit, gemeten in tijd, van de afdeling op basis van de gedefinieerde efficiëntie- en capaciteitswaarden.

Voordat een bepaalde afdelings- of bewerkingsplaatsagenda kan worden berekend, moeten er eerst een of meer algemene productieagenda's worden ingesteld. In een productieagenda wordt een standaardwerkweek gedefinieerd in termen van begin- en eindtijden van een werkdag en de ploegen die er werkzaam zijn. Bovendien zijn in een productieagenda de vastgestelde vakantiedagen gedurende het jaar opgenomen.  

Hier wordt beschreven hoe u afdelingsagenda's instelt. Voor het instellen van bewerkingsplaatsagenda's zijn de stappen vergelijkbaar.  

## Ploegen maken  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Ploegen** in en kies vervolgens de gerelateerde koppeling.  
2.  Geef op een lege regel in het veld **Code** een nummer op om de ploeg aan te duiden, bijvoorbeeld **1**.  
3.  Geef een omschrijving voor de ploeg in het veld **Omschrijving**, bijvoorbeeld **Vroege ploeg**.  
4.  Vul eventueel regels voor een tweede of derde ploeg in.  

Ook als de afdeling niet met ploegen werkt, moet er toch minstens één ploegcode worden opgegeven.  

## Een productieagenda instellen  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Productieagenda's** in en kies vervolgens de gerelateerde koppeling.  
2.  Geef op een lege regel in het veld **Code** een nummer op ter aanduiding van de productieagenda.  
3.  Beschrijf de productieagenda in het veld **Omschrijving**.  
4.  Kies de actie **Werkdagen**.
5.  Geef op de pagina **Productieagendawerkdagen** een volledige werkweek, met de begin- en eindtijden voor elke dag, op.  

    Selecteer in het veld **Ploeg** een van de ploegen die u eerder hebt gedefinieerd. Voeg een regel toe voor elke werkdag en elke ploeg. Voorbeeld:  

    maandag 07:00 15:00 1   
    dinsdag 07:00 15:00 1  

    Als u een productieagenda met twee ploegen nodig hebt, gaat u op de volgende manier te werk:  

    maandag 07:00 15:00 1   
    maandag 15:00 23:00 2  
    dinsdag 07:00 15:00 1  
    dinsdag 15:00 23:00 2  

    Weekdagen die u niet in de productieagenda definieert, zoals zaterdag en zondag, worden beschouwd als niet-werkdagen en hebben in een afdelingsagenda een beschikbare capaciteit van nul.  

    Wanneer alle werkdagen van een week zijn gedefinieerd, kunt u de pagina **Productieagendawerkdagen** sluiten en doorgaan met het invoeren van vakanties en vrije dagen.  

6.  Selecteer op de pagina **Productieagenda's** de productieagenda en kies de actie **Vakantiedagen**.
7. Definieer op de pagina **Productieagendavakantiedagen** de vakantiedagen van het jaar door voor elke vakantiedag op afzonderlijke regels de begindatum en -tijd, de eindtijd en een omschrijving op te geven. Voorbeeld:  

    04 juli 2014 0:00:00 23:59:00 Zomervakantie  
    05 juli 2014 0:00:00 23:59:00 Zomervakantie  
    06 juli 2014 0:00:00 23:59:00 Zomervakantie  

De gedefinieerde vakantiedagen hebben in een afdelingsagenda een beschikbare capaciteit van nul.  

Nu kan de productieagenda worden toegewezen aan een afdeling om de afdelingsagenda te berekenen waarop de volledige tijdsplanning van alle bewerkingen op die afdeling wordt gebaseerd.  

## Een afdelingsagenda berekenen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afdelingen** in en kies vervolgens de gerelateerde koppeling.
2. Open de afdeling die u wilt bijwerken.  
3. Geef in het veld **Productieagendacode** op welke productieagenda moet worden gebruikt als basis voor de agenda van de afdeling.  
4. Kies de actie **Agenda**.  
5. Kies op de pagina **Afdelingsagenda** de actie **Matrix weergeven**.  

    In het linkerdeel van de matrixpagina worden alle afdelingen weergegeven die zijn ingesteld. In het rechterdeel ziet u een agenda met daarop de beschikbare capaciteitswaarden voor elke werkdag in de gedefinieerde eenheid, bijvoorbeeld **480** minuten. Elke regel geeft de agenda van één afdeling weer.  

    > [!NOTE]  
    >  U kunt de capaciteitswaarden voor elke week of maand ook bekijken door te schakelen tussen opties in het veld **Weergeven per** op de pagina **Afdelingsagenda**.  

    Als u de nieuwe productieagenda wilt weergeven als een lijn op de geselecteerde afdeling, moet deze productieagenda eerst worden berekend.  

6.  Kies de actie **Berekenen**.  
7.  Op het sneltabblad **Afdeling** kunt u een filter instellen, zodat er maar voor één afdeling een berekening wordt gemaakt. Stelt u geen filter in, dan worden alle bestaande afdelingsagenda's berekend.  
8.  Definieer de begin- en einddatum van de agendaperiode die moet worden berekend, bijvoorbeeld één jaar, van 1 jan. 2004 tot 31 dec. 2004.
9. Kies de knop **OK** om de capaciteit te berekenen.  

Er zijn nu agendaposten gemaakt (of bijgewerkt) waarin de beschikbare capaciteit per dag (of per andere periode) wordt weergegeven op basis van de volgende drie sets stamgegevens:  

- de in de productieagenda gedefinieerde werkdagen en ploeg  
- de waarde in het veld **Capaciteit** op de afdelingskaart  
- de waarde in het veld **Efficiëntie** op de afdelingskaart.  

De berekende afdelingsagenda bepaalt nu wanneer en hoe veel capaciteit beschikbaar is op deze afdeling. Hiermee bepaalt u de gedetailleerde planning van bewerkingen die worden uitgevoerd op de afdeling.  

## Afwezigheid op de afdeling registreren  
1.  Kies op de pagina **Afdelingsagenda** de actie **Matrix weergeven**.
2. Selecteer op de pagina **Afdelingsagendamatrix** de afdeling en de agendadag waarop de afwezigheid moet worden geregistreerd en kies vervolgens de actie **Afwezigheid**.  
3.  Definieer op de pagina **Afwezigheid** de begintijd, de eindtijd en de omschrijving van de afwezigheid van die dag, bijvoorbeeld: Voorbeeld:  

    25 jan. 2001 08:00 10:00 Onderhoud  

4.  Kies de actie **Bijwerken** en sluit vervolgens de pagina **Afwezigheid**.  

De geregistreerde afwezigheid is nu in mindering gebracht op de capaciteit van de geselecteerde dag.  

## Zie ook  
[Basisagenda's instellen](across-how-to-assign-base-calendars.md)  
[Afdelingen en bewerkingsplaatsen instellen](production-how-to-set-up-work-and-machine-centers.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]