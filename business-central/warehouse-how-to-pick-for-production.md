---
title: 'Artikelen picken of verplaatsen voor productie, assemblage of projecten in standaardmagazijnconfiguraties'
description: 'Als voor de magazijnvestiging vereist is dat u picks verwerkt, maar geen verzendingen, gebruikt u de pagina Voorraadpick om het picken van de onderdelen vast te leggen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Picken voor productie, assemblage of taken in standaardmagazijnconfiguraties

Hoe u materialen voor productie, projecten of assemblageorders verzamelt, is afhankelijk van de vestigingsinstellingen van uw magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

Zet in een standaardmagazijnconfiguratie voor de uitgaande stroom (pick) de schakelaar **Pick vereisen** aan, maar de schakelaar **Verzenden vereisen** uit op de pagina **Locatiekaart** voor de locatie.

Gebruik de volgende documenten voor interne doeleinden:

* Voorraadpick
* Voorraadverplaatsing

## <a name="inventory-picks"></a>Voorraadpicks

* Wanneer u een voorraadpick registreert voor een interne bewerking, zoals productie of een project, wordt het verbruik van de gepickte materialen tegelijkertijd geboekt.
* De schakelaar **Opslaglocatie verplicht** op de pagina **Locatiekaart** is optioneel.
* Bij gebruik van voorraadpicks definieert het veld **Opslaglocatie** op de materiaalregel of projectplanningsregels op een productieorder de opslaglocatie *nemen*. Materialen worden in mindering gebracht in de opslaglocatie 'nemen' wanneer u het verbruik boekt.

## <a name="inventory-movements"></a>Voorraadverplaatsingen

* Voor voorraadverplaatsingen moet u de schakelaar **Opslaglocatie verplicht** inschakelen op de pagina **Locatiekaart** voor de locatie.
* Voorraadverplaatsingen werken alleen met productieordermateriaalregels en assemblageorderregels.
* Wanneer u een voorraadpick registreert voor een interne bewerking, legt u enkel de fysieke verplaatsing vast van de materialen naar een opslaglocatie in het bewerkingsgebied. U boekt geen verbruik.
* Bij gebruik van voorraadverplaatsingen definieert het veld **Opslaglocatie** op materiaalregels op de productieorder de opslaglocatie *plaatsen* in het bewerkingsgebied. Magazijnmedewerker moeten de materialen in de opslaglocatie 'plaatsen' zetten.
* Registreer het verbruik van de gepickte materialen afzonderlijk door een verbruiksdagboek of assemblageorder te boeken.

>[!NOTE]
> Zelfs als de schakelaar **Pick vereist** is uitgeschakeld, kunt u een **Magazijnpick**-document gebruiken. Magazijnpick-documenten zijn vergelijkbaar met **Voorraadpick**-documenten. Dit is handig als u picks wilt gebruiken in bewerkingen en verzending in uitgaande magazijnstromen.

### <a name="production"></a>Productie

Gebruik **Voorraadpick**-documenten om productiematerialen in de stroom naar productie te picken.

Voor een locatie die opslaglocaties gebruikt, kunt u de stroom uitbreiden naar productie door **Voorraadverplaatsing**-documenten te gebruiken. Voorraadverplaatsingen zijn vooral handig voor het afboeken van materialen. Zie voor meer informatie over hoe materiaalverbruik wordt afgeboekt vanuit de opslaglocaties Naar productie of Grijpvoorraad [Productiematerialen afboeken in een standaard magazijnconfiguratie](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly"></a>Assemblage

Gebruik **Voorraadverplaatsing**-documenten om assemblagemateriaal naar het assemblagegebied te verplaatsen.

> [!NOTE]
> Voor **Voorraadverplaatsing**-documenten zijn opslaglocaties vereist.

[!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt assemblagestromen van het type op voorraad assembleren en op order assembleren. Zie voor meer informatie over op order assembleren in de uitgaande magazijnstroom [Op-order-assembleren-artikelen met voorraadpicks afhandelen](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management"></a>Projectbeheer

Gebruik **Voorraadpick**-documenten om projectmateriaal in de stroom naar productiebeheer te picken.

Voor locaties die opslaglocaties gebruiken, kunt u de stroom uitbreiden naar projecten met **Voorraadverplaatsing**-documenten.

> [!NOTE]
> De mogelijkheid om componenten voor taakplanningsregels te picken is toegevoegd aan [!INCLUDE[d365fin](includes/d365fin_md.md)] in 2022 releasewave 2. Om de mogelijkheid te gebruiken, moet een beheerder **Functie-update: Voorraad- en magazijnpicks vanuit projecten inschakelen** inschakelen op de pagina **Functiebeheer**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de waarde in het veld **Resterend aantal** op de taakplanningsregel wanneer deze voorraadpicks maakt. Als u voorraadkeuzes voor taken wilt gebruiken, moet u de schakelaar **Gebruikslink toepassen** inschakelen op de pagina **Projectkaart** voor het project. Hiermee kunt u het gebruik volgen ten opzichte van uw plan. Als u de schakelaar niet aanzet, blijft het resterende aantal op **0** en wordt de voorraadkeuze niet gemaakt. Zie voor meer informatie [Bijhouden van projectgebruik instellen](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

## <a name="pick-or-move-for-production-assembly-and-projects-in-a-basic-warehouse-configuration"></a>Picken of verplaatsen voor productie, assemblage en projecten in een standaard magazijnconfiguratie

U kunt een voorraadpick of voorraadverplaatsing op drie manieren maken:  

* Uit het brondocument zelf.  
* Voor verschillende brondocumenten tegelijk door een batchproject te gebruiken.  
* In twee stappen. Geef het brondocument vrij om het brondocument gereed te maken voor picken. Maak de voorraadpick of verplaatsing vanuit de **Voorraadpick**- of **Voorraadverplaatsing**-documenten. De voorraadpick of -verplaatsing zijn gebaseerd op het brondocument.  

### <a name="to-create-an-inventory-pick-from-the-source-document"></a>Een voorraadpick maken vanuit het brondocument

1. Kies in het brondocument, dat een productieorder of project kan zijn, de actie **Voorraadopslag/-pick maken**.  
2. Schakel het selectievakje **Voorraadpick maken** in.
3. Kies de knop **Ok**.

### <a name="to-create-an-inventory-movement-from-the-source-document"></a>Een voorraadverplaatsing maken op basis van het brondocument

1. Kies in het brondocument, dat een productieorder, assemblageorder of project kan zijn, de actie **Voorraadopslag/-pick maken**.  
2. Schakel het selectievakje **Voorraadverplaatsing maken** in.
3. Kies de knop **Ok**.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job"></a>Meerdere voorraadpicks of -verplaatsingen maken met een batchproject

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadopslag/-pick-verplaatsing maken** in en kies de gerelateerde koppeling.  
2. Gebruik op het sneltabblad **Magazijnverzoek** de velden **Brondocument** en **Bronnr.** om te filteren op soorten documenten of reeksen documentnummers. U kunt bijvoorbeeld picks voor alleen de productieorders maken.
3. Schakel op het sneltabblad **Opties** de schakelaar **Voorraadpick maken** of **Voorraadverplaatsing maken** in.
4. Kies de knop **Ok**.

### <a name="to-create-inventory-picks-or-movements-in-two-steps"></a>Voorraadpicks of -verplaatsingen in twee stappen maken

Om materialen voor brondocumenten in twee stappen te verzamelen of te verplaatsen, moet u het brondocument vrijgeven om het klaar te maken voor picking. Voor interne doeleinden kunnen brondocumenten op de volgende manieren vrijgegeven worden.  

|Brondocument|Vrijgavemethode|  
|---------------------|--------------------|  
|Productieorder|Wijzig op de pagina **Geplande productieorder** de status van een order in **Vrijgegeven** of gebruik de pagina **Vrijgegeven productieorder** om een vrijgegeven productieorder te maken.|  
|Assemblageorder|Wijzig de status van een assemblageorder in **Vrijgegeven**.|
|Projecten | Wijzig de status van een project in **Open** of maak direct een project met de status Open.|  

Een magazijnmedewerker die is toegewezen aan het picken van artikelen, kan een voorraadopslagdocument maken voor het brondocument.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadpicks** of **Voorraadverplaatsing** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer in het veld **Brondocument** het soort brondocument waarvoor de opslag is.

    > [!NOTE]
    > U kunt **Voorraadpick**-documenten niet gebruiken voor het picken van assemblagematerialen.
4. Selecteer het brondocument in het veld **Bronnr.**  
5. U kunt ook de actie **Brondocument ophalen** kiezen om het document te selecteren in een lijst met inkomende brondocumenten die gereed zijn voor picken op de locatie.  
6. Klik op de knop **OK** om de pick- of verplaatsingsregels in te vullen op basis van het geselecteerde brondocument.  

## <a name="to-record-the-inventory-pick"></a>De voorraadpick registreren

1. Open op de pagina **Voorraadpick** het document waarvoor u een pick wilt vastleggen.  
2. In het veld **Opslaglocatie** op de pickregels, de opslaglocatie waar artikelen moeten worden gepickt uit de opslaglocatie waar het artikel beschikbaar is. U kunt de opslaglocatie indien nodig wijzigen.
3. Voer de pick uit en voer het gepickte aantal in het veld **Te verwerken aantal** in.

    Als het nodig is de artikelen voor een regel uit meerdere opslaglocaties te picken, bijvoorbeeld omdat een opslaglocatie niet de volledige hoeveelheid bevat, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.  
4. Kies de actie **Boeken**.  

Het volgende gebeurt tijdens het boekingsproces:

* Boek het verbruik van de brondocumentregels die zijn gepickt.
* Als de vestiging opslaglocaties gebruikt, leidt de boeking ertoe dat er magazijnposten worden gemaakt om de gewijzigde aantallen in de opslaglocatie te boeken.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement"></a>De voorraadverplaatsing registreren

1. Open op de pagina **Voorraadverplaatsing** het document waarvoor u een verplaatsing wilt vastleggen.  
2. In het veld **Opslaglocatie** op de verplaatsingsregels wordt op basis van de standaardopslaglocatie en beschikbaarheid per artikel de opslaglocatie voorgesteld waaruit de artikelen moeten worden gepickt. U kunt de opslaglocatie indien nodig wijzigen.  
3. Voer de verplaatsing uit en voer het verplaatste aantal in het veld **Te verwerken aantal** in. De waarde op de nemen- en plaatsen-regels moet hetzelfde zijn. Anders kunt u de verplaatsing niet registreren.

    Als het nodig is de artikelen voor een regel uit meerdere opslaglocaties te nemen, bijvoorbeeld omdat een opslaglocatie niet de volledige hoeveelheid bevat, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.  
4. Kies de actie **Voorraadverplaatsing registreren**.  

Het volgende gebeurt tijdens het boekingsproces:

* Magazijnposten geven nu aan dat de materialen in de opslaglocaties zijn die op de orderregels van het brondocument zijn opgegeven. Bijvoorbeeld de assemblageorder, het productiemateriaal of de projectplanningsregel.

>[!NOTE]
> In tegenstelling tot wanneer u materialen met voorraadpicks verplaatst, wordt het verbruik niet geboekt wanneer u een voorraadverplaatsing registreert. U registreert het verbruik als een aparte stap door het brondocument te boeken.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration"></a>Materialen voor productie afboeken in een standaard magazijnconfiguratie

Afboekingsmethoden hebben invloed op de stroom van materialen in productie. Zie voor meer informatie [Materialen afboeken op basis van de output van een bewerking](production-how-to-flush-components-according-to-operation-output.md). Afhankelijk van de geselecteerde afboekingsmethode kunt u op de volgende manieren materialen picken voor productie:

* Gebruik een **Voorraadpick**-document om de pick vast te leggen voor artikelen die de afboekingsmethode **Handmatig** gebruiken. Wanneer u een voorraadpick registreert, wordt het verbruik van de gepickte componenten geboekt. 
* Gebruik een **Voorraadverplaatsing **-document met een verwijzing naar een brondocument om picks vast te leggen voor materialen die de afboekingsmethode **Handmatig** gebruiken. U dient het verbruik apart te registreren. Zie voor meer informatie [Productieverbruik in batches boeken](production-how-to-post-consumption.md). 
* Gebruik een **Voorraadverplaatsing**-document met een verwijzing naar een brondocument om picks vast te leggen voor materialen die de afboekingsmethode **Picken + Voorwaarts**, **Picken + Achterwaarts** gebruiken. Het verbruik van de materialen gebeurt automatisch wanneer u de status van de productieorder wijzigt of door een bewerking te starten of te beëindigen. Alle vereiste materialen moeten beschikbaar zijn. Anders wordt afgeboekte verbruiksboeking voor dat materiaal gestopt.
* Gebruik een **Voorraadverplaatsing**-document zonder een verwijzing naar een brondocument of andere manieren om de verplaatsing vast te leggen van materialen die gebruikmaken van de afboekingsmethode **Voorwaarts** of **Achterwaarts**. Het verbruik van de materialen gebeurt automatisch wanneer u de status van de productieorder wijzigt of door een bewerking te starten of te beëindigen. Alle vereiste materialen moeten beschikbaar zijn. Anders wordt het boeken van afgeboekte verbruiksboeking voor dat materiaal gestopt. Zie voor meer informatie [Artikelen intern verplaatsen in basismagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example"></a>Voorbeeld

U hebt een productieorder voor 15 STUKS van artikel SP-SCM1004. Enkele artikelen op de onderdelenlijst moeten handmatig in een verbruiksdagboek worden afgeboekt, en andere artikelen kunnen automatisch worden gepickt en worden afgeboekt met behulp van de afboekingsmethode **Pick + Achterwaarts**.  

In de volgende stappen wordt een voorbeeld gegeven van de acties die verschillende gebruikers uitvoeren en de gerelateerde reacties:  

1. De winkelsupervisor geeft de productieorder vrij. Artikelen met de afboekingsmethode **Voorwaarts** zonder routeringskoppeling worden afgetrokken van de grijpvoorraadlocatie.  
2. De winkelsupervisor kiest de actie **Voorraadopslag/-pick maken** op de productieorder en schakelt de schakelaars **Voorraadpick maken** en **Voorraadverplaatsing maken** in. Er wordt een voorraadpickdocument gemaakt voor artikelen met de afboekingsmethoden **Handmatig**, en er wordt een voorraadverplaatsing gemaakt voor artikelen met de afboekingsmethode **Pick + Achterwaarts** en **Pick + Voorwaarts**.
3. De magazijnmanager wijst de picks en verplaatsingen toe aan een magazijnmedewerker.
4. De magazijnmedewerker pickt de artikelen uit de desbetreffende opslaglocaties en plaatst ze in de verbruikslocatie of in de opslaglocatie die is opgegeven in de voorraadverplaatsing. De opslaglocatie kan de opslaglocatie van een afdeling of bewerkingsplaats zijn.  
5. De magazijnmedewerker boekt de pick. De hoeveelheid wordt in mindering gebracht op de opslaglocaties.
6. De magazijnmedewerker boekt de verplaatsing. Het aantal wordt in mindering gebracht op de opslaglocaties en toegevoegd aan de verbruikopslaglocatie. Het veld **Gepickt aantal** op de onderdelenlijst voor alle gepickte artikelen wordt bijgewerkt.  
7. De machineoperator informeert de productieplanner dat de eindproducten gereed zijn.  
8. De winkelsupervisor gebruikt het outputdagboek of productiedagboek om de output te boeken. Het aantal materialen dat de afboekingsmethode **Picken + Voorwaarts** of **Picken + Achterwaarts** met routeringskoppelingen gebruikt, wordt afgetrokken van de Verbruikslocatie.
9. De productieplanner wijzigt de status van de productieorder in **Gereedgemeld**. Het aantal materialen dat gebruikmaakt van de afboekingsmethode **Achterwaarts**, wordt afgetrokken van de grijpvoorraadlocatie en het aantal materialen dat gebruikmaakt van de afboekingsmethode **Picken + Achterwaarts** zonder routeringskoppeling wordt afgetrokken van de verbruikslocatie.  

 De volgende illustratie geeft aan wanneer het veld **Opslaglocatie** in de materialenlijst wordt gevuld volgens de instelling van uw vestiging of bewerkingsplaats/afdeling.  

:::image type="content" source="media/binflow.png" alt-text="Overzicht van wanneer en hoe het veld Opslaglocatie wordt ingevuld.":::

## <a name="see-also"></a>Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblage](assembly-assemble-items.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
