---
title: 'Procedure: Projecten beheren | Microsoft Docs'
description: In deze procedure maakt u kennis met de functies voor projectbeheer in taken (projecten). Projecten zijn een manier waarop u het verbruik van de bedrijfsresources kunt plannen en de diverse kosten kunt bijhouden die samenhangen met de resources voor een bepaald project. Projecten brengen het verbruik met zich mee van arbeidsuren, machine-uren, voorraadartikelen en andere soorten verbruik die u mogelijk wilt bijhouden terwijl het project voortduurt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b6a61a9c5d2b8c7b3d197780c580c8bcf957560e
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-managing-projects-with-jobs"></a>Procedure: Projecten plannen
In deze procedure maakt u kennis met de functies voor projectbeheer in taken (projecten). Projecten zijn een manier waarop u het verbruik van de bedrijfsresources kunt plannen en de diverse kosten kunt bijhouden die samenhangen met de resources voor een bepaald project. Projecten brengen het verbruik met zich mee van arbeidsuren, machine-uren, voorraadartikelen en andere soorten verbruik die u mogelijk wilt bijhouden terwijl het project voortduurt.  

 In deze procedure wordt het instellen van een nieuw project behandeld en komt een aantal algemene taken aan de orde zoals het werken met vaste prijzen, in termijnen betalen, facturen boeken voor projecten en projecten kopiëren.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure  
 In deze procedure worden de volgende taken gedemonstreerd:  

### <a name="setting-up-a-job"></a>Een project instellen  
 Als de budgetstructuur voor projecten is ingesteld, is het eenvoudig om een project te maken. Dit scenario omvat de volgende procedures:  

-   Projecttaakregels en planningsregels instellen.  
-   Projectspecifieke prijzen voor artikelen, resources en grootboekrekeningen.  
-   Factureren vanuit een project.  

### <a name="handling-fixed-prices"></a>Werken met vaste prijzen  
 In projecten kunt u werken met vaste prijzen en prijzen voor services of goederen die van tevoren zijn overeengekomen met de klant. In dit scenario kunt u het volgende doen:  

-   Bekijken hoe contractuele en gefactureerde waarden worden vastgesteld.  
-   Extra (niet gefactureerd) werk dat niet is gefactureerd, in het schema opnemen.  

### <a name="copying-a-job"></a>Een project kopiëren  
 In dit deel van het overzicht wordt besproken hoe u een project geheel of gedeeltelijk kunt kopiëren om het handmatig invoeren van gegevens te beperken en de nauwkeurigheid te verhogen. Dit omvat het volgende:  

-   Een deel van een project kopiëren naar een nieuw project.  
-   Projectspecifieke prijzen kopiëren.  
-   Planningsregels kopiëren.  

### <a name="making-payment-by-installment"></a>Betalen in termijnen  
 Als een groot, duur project lang doorloopt, spreekt de klant vaak met het bedrijf af om in termijnen te betalen. In dit scenario ziet u hoe betaling in termijnen instelt aan de hand van de volgende onderwerpen:  

-   Betalingen in termijnen opzetten voor een project.  
-   Betalingen aan klanten factureren.  
-   Verbruik verantwoorden in een project met termijnbetalingen.  

## <a name="roles"></a>Rollen  
 Deze procedure bevat taken voor de volgende rollen:  

-   Projectmanager  
-   Lid van het projectteam  

## <a name="prerequisites"></a>Vereisten  
 Voordat u de stappen in deze procedure kunt uitvoeren, moet u het volgende doen:  

-   Installeer de demodatabase CRONUS International Ltd.
-   Maak voorbeeldgegevens met behulp van de stappen in het volgende gedeelte.  

## <a name="story"></a>Scenario  
In dit scenario gaat het om het bedrijf Cronus International Ltd., een design- en consultancyfirma die nieuwe infrastructuren ontwerpt (conferentiezalen en kantoren) en inricht met meubels, accessoires en opslagruimten. Het bedrijf werkt meestal met projecten. Prakash is projectleider bij CRONUS. Hij gebruikt projecten om een overzicht te bieden van alle lopende projecten die CRONUS heeft gestart, alsmede van de projecten die zijn afgerond. Hij is gewoonlijk degene die afspraken met klanten maakt en het grootste deel van het project, zoals taak- en planningsregels en prijzen, invoert in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hij constateert dat het maken, onderhouden en redigeren van informatie eenvoudig is. Prakash is tevens te spreken over de manier waarop projecten kunnen worden gekopieerd in [!INCLUDE[d365fin](includes/d365fin_md.md)] en de mogelijkheid om te betalen in termijnen.

 Tricia, een lid van het projectteam dat aan Prakash rapporteert, is verantwoordelijk voor de dagelijkse controle van het project. Behalve haar eigen werk, voert zij ook het werk in dat voor elke taak door technici wordt uitgevoerd. Zij legt de artikelen die zij hebben gebruikt en de kosten die zij hebben gemaakt vast.  

## <a name="preparing-sample-data"></a>Voorbeeldgegevens voorbereiden  
 Voordat u met dit scenario begint, moet u Tricia toevoegen als een nieuwe resource.  

### <a name="to-prepare-the-sample-data"></a>De voorbeeldgegevens voorbereiden  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Resources** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Nieuw** om een nieuwe resourcekaart te maken.  
3.  Voer op het sneltabblad **Algemeen** de volgende informatie in:  

    - **Nr.**: **Tricia**  
    - **Naam**: **Tricia**  
    - **Soort**: **Persoon**  

4.  Kies het veld **Basiseenheid** en kies de actie **Nieuw** om het venster **Resource-eenheid** te openen. Selecteer **Uur** in het veld **Code**. Kies de knop **Ok**.  
5.  Typ in het sneltabblad **Facturering** de volgende gegevens:  

    -   **Directe kostprijs**: **5**  
    -   **Indirecte kosten %**: **4**  
    -   **Kostprijs**: **10**  
    -   **Productboekingsgroep**: **Services**  
    -   **BTW-productboekingsgroep**: **VAT 25**  

6.  Kies de knop **OK** om de wijzigingen op te slaan.  

 In de volgende procedure kunt u een projectdagboekbatch voor Tricia maken om haar gebruik te boeken.  

### <a name="to-create-a-job-journal-batch"></a>Een projectdagboekbatch maken  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies in het venster **Projectdagboek** het veld **Batchnaam**. Het venster **Projectdagboekbatches** wordt geopend.  
3.  Kies de actie **Nieuw** om een nieuwe regel te maken met de volgende informatie:  

    -   **Naam**: **Tricia**  
    -   **Omschrijving**: **Tricia**  
    -   **Nr.-reeks**: **JJNL-GEN**  

4.  Klik op **OK** om alle open vensters te sluiten.  

## <a name="setting-up-a-job"></a>Een project instellen  
 In dit scenario heeft CRONUS een contract binnengehaald van de klant Progressive Home Furnishings voor het ontwerpen van een conferentie- en eetzaal. De klant is gevestigd in de Verenigde Staten en voor het project is speciale software nodig. De projectmanager komt tot overeenstemming met de klant en maakt een project dat deze afspraak dekt.  

### <a name="to-set-up-a-job"></a>Een project instellen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Nieuw** om een nieuwe kaart te maken.  
3.  Voer op het sneltabblad **Algemeen** de volgende informatie in:  

    -   **Omschrijving**: **Adviseren over de inrichting van een conferentiezaal**  
    -   **Factureren aan**: **01445544**  

4.  Typ op het sneltabblad **Boeking** de volgende gegevens:  

    -   **Status**: **Order**  
    -   **Projectboekingsgroep**: **Instellen**  
    -   **OHW-methode**: **Kostprijs**  

5.  Geef op het sneltabblad **Duur** de datum van vandaag op in de velden **Begindatum** en **Einddatum**. Deze datums zijn belangrijk voor het toepassen van de valutakoers wanneer het project wordt gefactureerd.  
6.  Controleer of in het sneltabblad **Buitenlandse handel** de valutacode **USD** is ingesteld. Als u USD selecteert in het veld **Factuurvalutacode**, wordt het project in Amerikaanse dollars gefactureerd en alleen gepland in de lokale valuta van CRONUS.  

 U kunt de prijzen voor klanten aanpassen per project, afhankelijk van de overeenkomsten die u hebt ingesteld. In de volgende procedure kent de projectmanager kosten toe aan de tijd van Tricia, stelt de prijs voor de vereiste software in en voegt de reiskosten toe die de klant is overeengekomen te betalen.  

### <a name="to-customize-pricing"></a>Prijzen aanpassen  

1.  Kies vanuit de projectkaart de actie **Resource**.  
2.  Geef de volgende gegevens op in het venster **Resourceprijzen project**:  

    -   **Code**: **Tricia**  
    -   **Eenheidsprijs**: **20**  

3.  Kies de knop **OK** om het venster te sluiten.  
4.  Kies de actie **Artikel**.  
5.  Geef de volgende gegevens en aangepaste prijs op in het venster **Artikelprijzen project**:  

    1.  **Artikelnr.**: **80201 (grafisch programma)**  
    2.  **Eenheidsprijs**: **200**  

6.  Kies de knop **OK** om het venster te sluiten.  
7.  Kies de actie **Grootboekrekening**.  
8.  Voer in het venster **GB-rekeningprijzen project** de volgende informatie en de kosten van reizen in, waarvoor de klant is overeengekomen te betalen, plus 25 procent:  

    1.  **Grootboekrekening**: **8430 (reizen)**  
    2.  **Kostprijsfactor**: **1,25**  

9. Kies de knop **OK** om het venster te sluiten.  

 De laatste stappen bij het instellen van een project is het toevoegen van de projecttaken en de planningsregels die deel van elke taak uitmaken. De planningregels bepalen wat aan de klant wordt gefactureerd.  

### <a name="to-add-job-tasks"></a>Projecttaken toevoegen aan  

1.  Kies op de kaart **Project** voor het nieuwe project de actie **Projecttaakregels**.  
2.  De volgende tabel beschrijft de informatie die u moet invoeren in de velden.  

    |Projecttaaknr.|Description|Soort projecttaak|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Adviezen voor zaalontwerp|Begintotaal|  
    |1010|Bespreking met klant|Rekening|  
    |1020|Ontwikkeling|Rekening|  
    |1090|Consultancy totaal|Eindtotaal|  

3.  Kies op het tabblad **Acties**, in de groep **Functies**, de optie **Projecttaken inspringen** om te laten zien dat sommige taken subcategorieën van andere taken zijn.  

 De volgende soorten planningsregel zijn beschikbaar:  

-   **Planning**: wordt toegevoegd aan de planning, maar niet gefactureerd.  
-   **Contract**: wordt gefactureerd, maar niet toegevoegd aan de planning.  
-   **Planning en contract**: gefactureerd en toegevoegd aan de planning.  

 In dit scenario maakt de projectmanager gebruik van **Planning en contract**. Hij maakt drie planningsregels voor taak 1010 en twee planningsregels voor taak 1020.  

### <a name="to-create-planning-lines"></a>Planningsregels maken  

1.  Selecteer regel 1010 en kies vervolgens de actie **Projectplanningsregels**. Geef de volgende informatie op:  

     **Regel 1**  

    -   **Regelsoort**: **Planning en contract**  
    -   **Planningsdatum**: **(datum van vandaag)**  
    -   **Soort**: **Bron**  
    -   **Nr.**: **Tricia**  
    -   **Aantal**: **40**  

     **Regel 2**  

    -   **Regelsoort**: **Planning en contract**  
    -   **Planningsdatum**: **(datum van vandaag)**  
    -   **Soort**: **Bron**  
    -   **Nr.**: **Timothy**  
    -   **Aantal**: **40**  

     **Regel 3**  

    -   **Regelsoort**: **Planning en contract**  
    -   **Planningsdatum**: **(datum van vandaag)**  
    -   **Soort**: **Grootboekrekening**  
    -   **Nr.**: **8430 (Reizen)**  
    -   **Aantal**: **2**  
    -   **Kostprijs**: **400**  

2.  Kies de knop **OK** om het venster te sluiten. De totalen worden bijgewerkt in het venster **Projecttaakregels**.  
3.  Selecteer regel 1020 en kies vervolgens de actie **Projectplanningsregels**. Geef de volgende informatie op:  

     **Regel 1**  

    -   **Regelsoort**: **Planning en contract**  
    -   **Planningsdatum**: **(datum van vandaag)**  
    -   **Soort**: **Bron**  
    -   **Nr.**: **Tricia**  
    -   **Aantal**: **80**  

     **Regel 2**  

    -   **Regelsoort**: **Planning en contract**  
    -   **Planningsdatum**: **(datum van vandaag)**  
    -   **Soort**: **Artikel**  
    -   **Nr.**: **80201 (grafisch programma)**  
    -   **Aantal**: **1**  

4.  Kies de knop **OK** om het venster te sluiten. Totalen worden bijgewerkt in het venster **Projecttaakregels**.  

## <a name="calculating-remaining-usage"></a>Resterend gebruik berekenen  
 Tricia, het projectteamlid, heeft een tijdje aan het project gewerkt en wil haar uren en gebruik tijdens het project registreren. Ze heeft niet meer uren gewerkt dan van tevoren met de klant is afgesproken. Ze gebruikt de batchverwerking **Resterend gebruik berekenen** om het resterende verbruik voor het project te berekenen in een projectdagboek. De batchverwerking berekent voor elke projecttaak het verschil tussen het geplande gebruik van artikelen, resources en grootboekkosten en het werkelijke gebruik dat in de projectposten is geboekt. Het resterende gebruik kan zij vervolgens boeken vanuit het projectdagboek waarin het wordt weergegeven.  

### <a name="to-calculate-remaining-usage"></a>Het resterende gebruik berekenen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open in het venster **Projectdagboek** in het veld **Batchnaam** de lijst **Projectdagboekbatches**. Selecteer de projectdagboekbatch **Tricia**.  
3.  Kies de actie **Resterend gebruik berekenen**.  
4.  Kies in het venster **Resterend gebruik berekenen**, op het sneltabblad **Projecttaak** het veld **Projectnr.** en selecteer het relevante projectnummer, meestal project J00010.  
5.  Typ **J00001** in het veld **Document nr.** op het sneltabblad **Opties**. Zo kunt u toekomstige boekingen gemakkelijker bijhouden.  
6.  Geef de datum van vandaag op als boekingsdatum.  
7.  Kies de knop **Ok**. Hiermee genereert u projectdagboekregels die zijn afgeleid van de planningsregels die Prakash voor het projectdagboek heeft gemaakt.  
8.  Kies de knop **OK** in het bevestigingsvenster. De gegenereerde regels worden toegevoegd aan het projectdagboek.  
9. Controleer of alle documentnummers J00001 zijn. Kies vervolgens de actie **Boeken**. Kies **Ja** om de boeking te bevestigen.  
10. De regels worden nu geboekt. Kies de knop **OK** om de vensters te sluiten.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Een projectverkoopfactuur maken en boeken  
 Tricia kan vervolgens een nieuwe factuur maken voor het hele project of voor een deel van een project. Ze kan de factuur ook aan een andere factuur voor dezelfde klant en voor hetzelfde project koppelen. In dit geval factureert zij voor het volledige project, aangezien het project nu is voltooid.  

### <a name="to-create-a-job-sales-invoice"></a>Een projectverkoopfactuur maken  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer het project dat u eerder hebt gemaakt en kies de actie **Projectverkoopfactuur maken**.  
3.  Schakel op het sneltabblad **Projecttaak** alle filters voor **Projecttaaknr.** uit om het project te factureren. Selecteer het relevante project in het veld **Projectnr.**.  
4.  Vul op het sneltabblad **Opties** de boekingsdatum in en of u één factuur per taak wilt maken of slechts één factuur voor alle taken.  
5.  Kies de knop **OK** om de factuur te maken en kies vervolgens de knop **OK** in het bevestigingsvenster.  

 Nadat Tricia de factuur heeft gemaakt, kan zij toegang hiertoe krijgen vanuit **Verkoop en marketing** onder **Orderverwerking** en extra verwerkingen uitvoeren.  

### <a name="to-post-a-new-sales-invoice"></a>Een nieuwe verkoopfactuur boeken  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open de factuur voor klantnr. 01445544. U ziet de gegevens die zijn ingevoerd op de planningsregels.  
3.  Kies de actie **Boeken**. Kies **Ja** om de boeking te bevestigen.  

### <a name="to-view-the-posted-invoice"></a>De geboekte factuur weergeven  

1.  Open het project en kies vervolgens de actie **Projectplanningsregels**.  
2.  Selecteer een van de planningsregels die zijn gefactureerd en kies de actie **Verkoopfactuur/creditnota**.
3. Kies in het venster **Projectfacturen** de actie **Verkoopfactuur/creditnota openen**.  

 Als ze een vraag heeft over de prijzen, de kosten en de winst die relevant zijn voor dit specifieke project, kan ze deze informatie opvragen in het venster **Statistiek**.  

### <a name="to-open-the-statistics-window"></a>Het venster Statistiek openen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Statistieken**. U kunt gedetailleerde informatie over de projectprijzen, -kosten en -winsten bekijken in zowel lokale als vreemde valuta's.  
3.  Kies de knop **Sluiten** om het venster **Projectstatistiek** te sluiten.  

## <a name="handling-fixed-prices"></a>Werken met vaste prijzen  
 CRONUS heeft een contract binnengehaald voor het inrichten van vergaderruimten. Als projectleider wil Prakash een goed overzicht hebben van de taken die nodig zijn voor het project met de bijbehorende gebudgetteerde en gemaakte kosten voor elke taak. Bovendien wil hij weten wat de totale contractprijs voor het project is en wat het bedrag is dat tot nu toe is gefactureerd. Hij heeft met de klant een vaste prijs voor een project afgesproken.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>Vaste prijzen beheren in projecten  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer het projectnummer **Guildford** en kies de actie **Projecttaakregels**.  
3.  Selecteer regel 1120 en klik in het veld **Planning (totale kostprijs)** met de rechtermuisknop op het bedrag en kies **DrillDown**.  

     Op basis van de projectplanningsregels besluit Prakash dat hij Tricia ook voor 30 uur wilt inzetten in deze fase van het project. Hij spreekt een vaste prijs af met de klant.  

4.  Selecteer in het venster **Projecttaakregels** regel 1120 en kies de actie **Projectplanningsregels**.  
5.  Kies de actie **Nieuw** om een nieuwe regel te maken met de volgende informatie:  

    -   **Regelsoort**: **Planning en contract**  
    -   **Soort**: **Bron**  
    -   **Nr.**: **Tricia**  
    -   **Aantal**: **30**  

7.  Kies de knop **OK** om het venster te sluiten.  
8.  Klik met de rechtermuisknop in het veld **Planning (totale kostprijs)** en kies opnieuw **Drilldown** in het venster **Projecttaakregels**. Geef de wijzigingen in de planning weer. U ziet dat de 30 uur aan de planning zijn toegevoegd.  
9. Kies de knop **OK** om de vensters te sluiten.  

 Nadat Tricia aan de planning voor deze taakregel is toegevoegd, werkt ze 25 uur aan het project. Ze voert deze uren in het projectdagboek in.  

### <a name="to-enter-hours-in-the-job-journal"></a>Uren invoeren in het projectdagboek  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Maak een nieuwe regel met de volgende informatie:  

    -   **Regelsoort**: **(blanco)**  
    -   **Boekingsdatum**: **(datum van vandaag)**  
    -   **Documentnr.**: **J00002**  
    -   **Projectnr.**: **Guildford**  
    -   **Projecttaaknr.**: **1120**  
    -   **Soort**: **Bron**  
    -   **Nr.**: **Tricia**  
    -   **Aantal**: **25**  

3.  Kies de actie **Boeken**.  

     Een paar dagen later werkt Tricia nog eens 10 uur aan het project. Ze heeft nu in totaal 35 uur gewerkt. Aangezien 30 uur zijn afgesproken met de klant, worden slechts vijf uur aan de klant in rekening gebracht. Tricia zal de extra vijf uur die ze aan de planning heeft gewerkt handmatig toevoegen.  

4.  Kies in het venster **Projectdagboek** de actie **Resterend gebruik berekenen**.  
5.  Voer in het venster **Resterend gebruik berekenen** de volgende informatie in op het sneltabblad **Opties**:  

    -   **Documentnr.**: **J00003**  
    -   **Boekingsdatum**: **(datum van vandaag)**  

6.  Voer het volgende in op het sneltabblad **Projecttaak**:  

    -   **Projectnr.**: **Guildford**  
    -   **Projecttaaknr.**: **1120**  

     Kies de knop **OK** om de berekening uit te voeren. Er zijn vijf uur werk die resteren voor Tricia. Het veld **Regelsoort** is leeg, wat betekent dat alleen het gebruik nog moet worden geboekt omdat het werk al is gepland.  

7.  Maak in het venster **Projectdagboek** een nieuwe regel met de volgende gegevens. Zorg ervoor dat beide projectnummers opeenvolgend zijn met de projectnummers die u al hebt gebruikt:  

    -   **Regelsoort**: **Planning**  
    -   **Projectnr.**: **Guildford**  
    -   **Projecttaaknr.**: **1120**  
    -   **Soort**: **Bron**  
    -   **Nr.**: **Tricia**  
    -   **Aantal**: **5**  

     Door **Planning** te kiezen als regelsoort werkt het programma de geplande kosten en prijzen bij zonder de contractkosten en prijzen aan te passen die aan de klant worden gefactureerd.  

8.  Kies de actie **Boeken**. Kies de knop **OK** om het venster te sluiten.  
9. Open het overzicht **Projecten**.  
10. Selecteer het project GUILDFORD en kies de actie **Projecttaakregels**.  
11. Selecteer regel 1120 en klik in het veld **Planning (totale kostprijs)** met de rechtermuisknop op het bedrag. Kies **Drilldown** om de gegevens weer te geven.  

     Wijzigingen worden automatisch ingevoerd op de regel voor Projecttaaknr. 1120. In de totale kosten voor gepland werk, zijn vijf extra uren werk door Tricia toegevoegd aan de planning.  

12. Kies de knop **Sluiten** om het venster te sluiten.  
13. Klik nu met de rechtermuisknop op het bedrag in het veld **Contract (totale kostprijs)** en kies **Drilldown** om de informatie weer te geven.  

     In de totale prijs van het contract, zijn alleen de oorspronkelijk afgesproken 30 uur opgenomen aangezien die met de klant zijn overeengekomen.  

## <a name="copying-jobs"></a>Projecten kopiëren  
 Prakash heeft een overeenkomst bereikt met de klant Selagorian Ltd om 10 conferentieruimten in te richten. De overeenkomst lijkt op een eerder project. Daarom kan tijd worden bespaard door dat eerdere project te kopiëren.  

 In het venster **Project kopiëren** kunt u het project en de taakregels selecteren die u wilt kopiëren. U kunt ook kiezen om de bronprojectboekingen te kopiëren, waardoor planningsregels worden gemaakt op basis van het daadwerkelijke gebruik, of u kunt de bronprojectplanningsregels kopiëren, waarmee de oorspronkelijke planningsregels worden gekopieerd naar het nieuwe project. Vervolgens kunt u kiezen welk type planningsregel of boeking u wilt opnemen en alleen datgene selecteren wat relevant is voor dit nieuwe project. Ten slotte kunt u het project selecteren waarnaar u wilt kopiëren, en definiëren of prijzen en aantallen eveneens moeten worden gekopieerd.  

### <a name="to-copy-a-job"></a>Een project kopiëren  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Nieuw** om een nieuw project te maken. Geef de volgende informatie op:  

    -   **Omschrijving**: **10 conferentieruimten inrichten**  
    -   **Factureren aan**: **20000**  

3.  Kies de actie **Projecttaken kopiëren vanuit**.  
4.  Voer in het venster **Projecttaken kopiëren** het volgende in:  

    -   **Projectnr.**: **Guildford**  
    -   **Projecttaaknr. van**: **1000**  
    -   **Bron**: **Projectplanningsregels**  
    -   **Incl. planningsregelsoort**: **Planning + Contract**  
    -   **Naar projectnr.**: **Guildford 10 conferentieruimten inrichten**  
    -   Selecteer de velden **Dimensies kopiëren** en **Aantal kopiëren**.  

5.  Kies de knop **OK** om het project te kopiëren en kies vervolgens de knop **OK** om het bevestigingsvenster te sluiten.  

     Door prijzen, projecttaakregels en projectplanningsregels voor twee taken te vergelijken, kunt u zien of de informatie met succes is gekopieerd.  

## <a name="making-payments-by-installments"></a>Betalen in termijnen  
 CRONUS heeft net een groot project binnengehaald dat een jaar gaat duren. Omdat hiervoor veel resources nodig zijn, stelt de projectmanager het contract zo in dat de klant een gedeelte van de prijs vooraf betaalt, een tweede deel wanneer het project half is voltooid en de laatste betaling na voltooiing.  

### <a name="to-set-up-a-new-account"></a>Een nieuwe rekening instellen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies in het venster **Rekeningschema** de actie **Nieuw** om een nieuwe kaart te maken.  
3.  Geef op de kaart **Nieuwe grootboekrekening** de volgende gegevens op:  

    -   **Nr.**: **6630**  
    -   **Naam**: **Projectbetaling**  

4.  Selecteer op het sneltabblad **Boeken** in het veld **Prod.-boekingsgroep** de optie **MISC**. Kies de knop **OK** om het venster te sluiten.  
5.  Selecteer in het venster **Rekeningschema** de optie **Nr. 6630 Projectbetaling** en kies de actie **Inspringen**. Kies **Ja** om te bevestigen.  

 De volgende procedures laten zien hoe u een nieuw project kunt maken, prijzen kunt instellen en vervolgens betaling in termijnen kunt instellen. U kunt in de projecttaakregels specifieke regels opnemen voor de betalingen in termijnen. Al het voltooide werk voor het project dat aan de planning wordt toegevoegd, wordt op de verbruiksregels ingevoerd. Voor elke betalingstaakregel in de planningsregels is de regelsoort Contract, wat betekent dat de klant wordt gefactureerd. Voer een nieuwe regel in voor de aanbetaling. Geef op de taakregel voor verbruik de gegevens op voor de artikelen en resources die in dit project zijn gebruikt. Hierdoor wordt de planning uitgebreid met de arbeidsuren en de artikelen die voor het project zijn gebruikt.  

### <a name="to-make-a-payment-by-installment"></a>Betalen in termijnen  

1.  Maak een nieuw project.  
2.  Vul op de nieuwe **projectkaart** de volgende gegevens in:  

    -   **Omschrijving**: **Opknappen receptie**  
    -   **Factureren aan**: **30000**  
    -   **Projectboekingsgroep**: **Instellen**  
    -   **OHW-methode**: **Kostprijs**  

3.  Kies op de projectkaart de actie **Resource**. Geef de volgende informatie op:  

    -   **Code**: **Tricia**  
    -   **Eenheidsprijs**: **10**  

     Kies de knop **OK** om het venster te sluiten.  

4.  Kies op de kaart **Project** de actie **Projecttaakregels**.  

     De volgende tabel beschrijft de regels die u gaat maken.  

    |Regel|Projecttaaknr.|Description|Soort projecttaak|  
    |----------|------------------|---------------------------------------|-------------------|  
    |0|1000|Betaling - Aanbetaling|Boeken|  
    |2|2000|Gebruik|Rekening|  
    |3|3000|Betaling - Halverwege|Rekening|  
    |4|4000|Betaling - Voltooiing|Boeken|  

5.  Selecteer in het venster **Projecttaakregels** taak 1000 en kies de actie **Projectplanningsregels**.  
6.  Maak een planningsregel met de volgende informatie:  

    -   **Regelsoort**: **Contract**  
    -   **Planningsdatum**: **(datum van vandaag)**  
    -   **Soort**: **Grootboekrekening**  
    -   **Nr.**: **6630**  
    -   **Aantal**: **1**  
    -   **Eenheidsprijs**: **5000**  

     Kies de knop **OK** om het venster te sluiten.  

7.  Selecteer in het venster **Projecttaakregels** de optie **Taak 2000** en open de bijbehorende optie **Projectplanningsregels**.  

     De volgende tabel beschrijft de planningsregels die u gaat maken.  

    |Lijn|Regelsoort|Planningsdatum|Soort|Nr.|Aantal|  
    |----------|---------------|-------------------|----------|---------|--------------|  
    |1|Schema|(datum van vandaag)|Resource|Tricia|120|  
    |2|Schema|(datum van vandaag)|Artikel|70104|10|  

     Kies de knop **OK** om het venster te sluiten. U ziet in het venster **Projecttaakregels** dat de planningsbedragen zijn bijgewerkt.  

8.  Selecteer **taak 3000** in het venster **Projecttaakregels**.  
9. Maak een planningsregel met de volgende informatie:  

    -   **Regelsoort**: **Contract**  
    -   **Planningsdatum**: **een toekomstige datum**  
    -   **Soort**: **Grootboekrekening**  
    -   **Nr.**: **6630**  
    -   **Aantal**: **1**  
    -   **Eenheidsprijs**: **5000**  

     Kies de knop **OK** om het venster te sluiten.  

10. Maak een soortgelijke planningsregel voor projecttaak 4000.  

 Nu de taak- en planningsregels zijn ingevoerd kan Prakash een factuur voor de eerste betaling maken. Hij doet dit op basis van de projecttaakregels om er zeker van te zijn dat de factuur alleen de regels voor de eerste betaling bevat. Open de verkooporder vanuit de planningsregels of de taakregels.  

### <a name="to-create-an-invoice"></a>Een factuur maken  

1.  Selecteer in het venster **Projecttaakregels** regel 1000 en kies de actie **Verkoopfactuur maken**.  
2.  Stel in het venster **Verkoopfactuur maken** de datum van vandaag in als de boekingsdatum, geef **Per taak** op en kies de knop **OK** om een factuur te maken met de standaardinformatie. Klik op **OK** om het bevestigingsvenster af te sluiten.  
3.  Kies de actie **Verkoopfactuur/creditnota**. U ziet op de verkoopfactuur dat alleen de aanbetaling in de factuur is opgenomen. Verstuur de factuur nu aan de klant zoals is overeengekomen.  

## <a name="next-steps"></a>Volgende stappen  
 In dit scenario heeft u enkele van de basisstappen voor het werken met projecten in [!INCLUDE[d365fin](includes/d365fin_md.md)] doorlopen. U hebt geleerd over hoe u een nieuw project kunt maken, een project kunt kopiëren en betalingen kunt verwerken. Ook hebt u een demonstratie gekregen van het bijhouden van uren en het opstellen van facturen.  

## <a name="see-also"></a>Zie ook  
 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)   
 [Projectbeheer instellen](projects-setup-projects.md)   
 [Procedure: Resources gebruiken](projects-how-use-resources.md)   
 [Procedure: Voortgang en prestaties bewaken](projects-how-monitor-progress-performance.md)   
 [Procedure: Projecten factureren](projects-how-invoice-jobs.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

