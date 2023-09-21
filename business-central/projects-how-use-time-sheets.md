---
title: Urenstaten gebruiken
description: 'Beschrijft hoe u een urenstaat maakt om werksoorten te definiëren, de urenstaat invult en de urenstaat indient voor goedkeuring.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 03/01/2022
ms.author: bholtorf
---
# <a name="use-time-sheets"></a>Urenstaten gebruiken

U kunt urenstaten gebruiken in [!INCLUDE [prod_short](includes/prod_short.md)] om afwezigheid bij te houden en om de tijd en resources die aan een project worden besteed bij te houden. U kunt met tijdbeheer vroeg problemen identificeren en vertragingen of budgetoverschrijdende kosten voorkomen. Met urenstaten kan een resource eenvoudig tijdsgebruik rapporteren voor een individu of een machine en een manager kan het gebruik en de toewijzing ervan eenvoudig bekijken. Dit artikel beschrijft hoe u een urenstaat maakt, werksoorten definieert, de urenstaat invult en de urenstaat indient voor goedkeuring.  

U kunt uw projectplanningsregels kopiëren en gebruiken in een urenstaat. Op die manier hoeft u de gegevens slechts op één plaats in te voeren en zijn de regelgegevens altijd correct.

Nadat u urenstaatposten voor een project hebt goedgekeurd, kunt u deze boeken naar het relevante projectdagboek of resourcedagboek.

Voordat u urenstaten kunt gebruiken, moet u algemene informatie instellen en een beheerder en een of meer fiatteurs van urenstaten opgeven. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.  

> [!TIP]
> Vanaf releasewave 2 van 2021 kunt u toegewezen urenstaten beheren op een mobiel apparaat. Uw beheerder moet mogelijk echter de **Functie-update: nieuwe ervaring met urenstaten** inschakelen op de pagina [Functiebeheer](https://businesscentral.dynamics.com/?page=2610) om deze mogelijkheid te gebruiken. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

## <a name="to-create-time-sheets"></a>Urenstaten maken

U kunt de batchverwerking **Urenstaten maken** gebruiken om urenstaten in te stellen voor een opgegeven aantal perioden of weken. Vervolgens kan de eigenaar van de urenstaat deze openen en tijd vastleggen die aan een taak is besteed. U kunt ook [de automatische uitvoering van de batchtaak plannen](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> U moet machtigingen hebben om urenstaten te maken. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Urenstaten maken** op de pagina **Urenstaten**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > De velden **Urenstaat gebruiken** en **Gebruikers-id eigenaar urenstaat** moeten worden ingevuld op de kaart voor de resource van de urenstaat.

    Kies optioneel de actie **Plannen** om op te geven hoe vaak u wilt dat de taak automatisch wordt uitgevoerd. Als u bijvoorbeeld de taak wilt configureren om gedurende vier weken wekelijks te worden uitgevoerd, stelt u op de pagina **Een rapport plannen - Urenstaten maken** het veld **Formule voor volgende uitvoeringsdatum** in op *4W*. Zie [Een rapport plannen voor uitvoering](ui-work-report.md#ScheduleReport) voor meer informatie.  
4. Kies de knop **Ok**.  

U kunt de urenstaten die u hebt gemaakt, bekijken op de pagina **Urenstaten**. Elke urenstaat bestaat uit een of meer regels die de tijd definiëren die u ter goedkeuring wilt indienen. In de volgende tabel worden de soorten regels beschreven die u aan de urenstaat kunt toevoegen.

| **Veld** | **Beschrijving** |
|---|---|
| | Gebruik dit om een opmerking of markering toe te voegen aan het veld **Omschrijving** van de urenstaatregel. U kunt dit veld bijvoorbeeld gebruiken om urenstaatposten te categoriseren. Als u het veld **Soort** leeg laat voor een urenstaatregel, kunt u geen tijdwaarden in de weekdagvelden voor die regel invoeren. |
| Afwezigheid | Gebruik dit om de tijd te registreren dat u afwezig bent tijdens een werkweek. Geef, om de informatie voor die regel te voltooien, de soort afwezigheid op in het veld **Afwezigheidsredencode**. |
| Assemblageorder | Wordt gebruikt om tijd te registreren voor assemblageorders. Een urenstaatregel van deze soort wordt gemaakt tijdens het boeken van assemblageorderregels waarvoor de resource is ingesteld op gebruik van urenstaten. U kunt een regel van deze soort niet handmatig selecteren. |
| Project | Wordt gebruikt om tijdverbruik te registeren voor een project. Geef om de informatie voor de regel te voltooien het projectnummer en het projecttaaknummer op waarvoor u tijd wilt registreren. U kunt tijd registreren voor regels die u niet hebt gepland.|
| Bron | Wordt gebruikt om tijdverbruik te registeren voor een resource. Geef, om de informatie voor de regel te voltooien, een omschrijving van het werk. |
| Service | Gebruik dit om tijdverbruik voor een serviceorder of servicecreditnota te registreren. |

Als u bijvoorbeeld een urenstaat wilt indienen voor een werkweek waarin u de meeste dagen aan schoonmaakwerkzaamheden hebt gewerkt, maar één vrije dag had vanwege medische afspraken, voegt u regels toe zoals geïllustreerd in de volgende tabel.

| Soort | Omschrijving | Werksoortcode | Afwezigheidstypecode |
|--|--|--|--|
| Bron | Werkuren | Schoonmaken |  |
| Afwezigheid | Verlof |  | Gezondheid |
|  | Ik moest dinsdag vrij nemen vanwege een medische afspraak. |  |  |

In dit hypothetische voorbeeld registreert u dan de relevante uren over de relevante dagen in de velden voor elke weekdag.  

> [!TIP]
> In de meeste gevallen heeft uw bedrijf voorgedefinieerde werksoorten voor de verschillende soorten regels. In die gevallen kiest u gewoon het relevante werktype uit de lijst en voegt u uw eigen beschrijving toe.  
>
> Kies het werktype door de knop :::image type="icon" source="media/assist-edit-icon.png" border="false"::: te kiezen in het veld **Omschrijving**, door de actie **Activiteitsdetails** te kiezen en deze vervolgens op te geven op de pagina die wordt geopend, of door deze te kiezen in respectievelijk het veld **Werktypecode** of het veld **Afwezigheidstypecode**. In dit geval kunt u het gedeelte [Werksoorten definiëren en er een toevoegen aan een urenstaat](#to-define-work-types-and-add-one-to-a-time-sheet) negeren.  

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Urenstaatregels in andere urenstaten opnieuw gebruiken

Als uw urenstaatinformatie van periode tot periode gelijk blijft, kunt u tijd besparen door de regels te kopiëren uit de vorige periode. Vervolgens voert u alleen het tijdsgebruik voor de nieuwe periode in.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Urenstaten** in en kies vervolgens de gerelateerde koppeling.  
2. Open de urenstaat voor een periode na de periode voor een bestaande urenstaat met regels.  
3. Kies de actie **Regels kopiëren van vorige urenstaat**.

De regels worden gekopieerd, inclusief details zoals het type en beschrijving. Als de regel bijvoorbeeld is gekoppeld aan een project, wordt het **Projectnr.** gekopieerd. Alle gekopieerde regels hebben de status **Open**. U kunt nu indien nodig de regels wijzigen.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Projectplanningsregels kopiëren naar een urenstaat
De volgende procedure beschrijft hoe u snel projectplanningsregels toevoegt aan een urenstaat.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Urenstaten** een urenstaat voor de betreffende periode.  
3. Kies de actie **Regels maken van projectplanning**. Alle projectplanningsregels in de urenstaatperiode worden gekopieerd naar het veld **Resourcenr.** op de urenstaat voor de machine of persoon.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Werksoorten definiëren en er een toevoegen aan een urenstaat

U kunt het werksoort voor alle urenstaatregels voor serviceorders, projectorders en resources definiëren. Op deze manier kunt u gegevens toevoegen die u nodig hebt om de klant te factureren voor verschillende soorten werk.  

1. Kies op de pagina **Urenstaten** de relevante urenstaat.
2. Kies op de eerste regel in het gedeelte **Regels** het veld **Soort** en kies vervolgens het relevante type, zoals: *Resource*.  
3. Kies het veld **Omschrijving** en vul dan op de pagina **Resourcedetail urenstaatregel** de velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Als er geen werksoorten bestaan, kiest u de actie **Nieuw**.
    2. Vul op de pagina **Werksoorten** de benodigde velden in en ga terug naar de urenstaat.
4. Vul de rest van de urenstaat in. Zie voor meer informatie het gedeelte [Urenstaatregels invullen en ter goedkeuring verzenden](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Soortgelijke stappen zijn van toepassing op het definiëren van afwezigheidscodes.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>Urenstaatregels invullen en ter goedkeuring verzenden

Urenstaatregistratie wordt bijgehouden in uren, de standaard basiseenheid voor resources. Een urenstaat bevat standaard de algemene werkdagen van maandag tot en met vrijdag.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Urenstaten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een urenstaat voor de betreffende periode.
3. Vul de velden indien nodig op een regel in. Voer het aantal uren in dat door de resource op elke dag van de week wordt gebruikt.  

    Om werk bij te houden voegt u in de meeste gevallen een regel van het type *Resource* toe en vervolgens registreert u elke dag bestede uren. Als u afwezigheid wilt registreren, voegt u een regel van het type *Afwezigheid* toe.  

    > [!TIP]  
    > U kunt de som controleren van de urenstaaturen die u hebt ingevoerd in het feitenblok **Overzicht van werkelijk/gebudgetteerd**.  
4. Herhaal stap 3 voor andere werksoorten die de resource uitvoert.  

    Vervolgens moet u beslissen of u alle regels op de urenstaat wilt indienen of dat u afzonderlijke regels wilt indienen.  

    * Om de urenstaat voor een of meer regels in te dienen kiest u de betreffende regel en kiest u vervolgens de actie **Indienen**.

        Kies op de inzendingspagina de optie **Alleen geselecteerde regels**. De regel verandert van status van *Open* naar *Ingediend*.
    * Om de urenstaat voor alle openstaande regels in te dienen kiest u de actie **Indienen** bovenaan de pagina **Urenstaat**.  

        U wordt gevraagd om te bevestigen dat u alle openstaande regels op de huidige urenstaat wilt indienen.  

    > [!NOTE]  
    > U kunt alleen urenstaatregels verzenden waarvoor u tijd hebt ingevoerd.  
5. Als u gegevens wilt wijzigen op een regel die is ingesteld op **Ingediend**, selecteert u de regel en kiest u de actie **Opnieuw openen**.

    > [!NOTE]  
    >   Een beheerder kan een urenstaatregel weigeren die ter goedkeuring is verzonden. Als een regel de status **Geweigerd** heeft, kunt u wijzigingen aanbrengen in de regel en opnieuw **Indienen** kiezen.  
6. Kies de knop **Ok**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Een urenstaat goedkeuren of weigeren
Een urenstaat moet ter goedkeuring worden ingediend om te worden gebruikt. U kunt afzonderlijke regels goedkeuren en weigeren op een urenstaat of deze terugsturen naar de indiener voor aanvullende actie. Een urenstaat kan worden goedgekeurd op twee manieren:

* Een beheerder van urenstaten kan een urenstaat goedkeuren.
* De persoon die is opgegeven in het veld **Gebruikers-id van fiatteur van urenstaat** op een resourcekaart kan urenstaten van die resource goedkeuren. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstatenmanager** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een urenstaat in de lijst.  
3. Kies op de pagina **Urenstaat** 
    1. de actie **Verwerken** en kies dan de actie **Goedkeuren**.
    2. Kies de actie **Alle verzonden regels** om alle regels goed te keuren of de actie **Alleen geselecteerde regel(s)** om alleen de regels goed te keuren die zijn geselecteerd op de pagina **Urenstaat**.
4. Kies de knop **OK**.  
5. U kunt ook de actie **Weigeren** kiezen en stap 4 tot en met 5 volgen.  

> [!TIP]  
>   Gebruik de feitenblokken **Status urenstaat** en **Overzicht van werkelijk/gebudgetteerd** om een overzicht te krijgen van urenstaatgegevens.

Nadat u een urenstaat hebt goedgekeurd of geweigerd, kan deze niet meer worden gewijzigd tenzij deze eerst opnieuw wordt geopend. In de volgende procedure wordt uitgelegd hoe u een goedgekeurde of geweigerde urenstaat opnieuw opent.

## <a name="to-reopen-a-time-sheet"></a>Een urenstaat opnieuw openen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Urenstatenmanager** of **Urenstaten** in en kies vervolgens de gerelateerde koppeling.
2. Open een urenstaat uit de lijst.  

    > [!NOTE]  
    >   U kunt alleen regels met de status **Goedgekeurd** opnieuw openen. U kunt geen regels met de status **Afgewezen** opnieuw openen. U kunt een urenstaat niet opnieuw openen als deze is geboekt.  
3. Kies op de pagina **Urenstaat** de actie **Opnieuw openen** en kies vervolgens de actie **Alle verzonden regels** om alle regels opnieuw te openen of kies de actie **Alleen geselecteerde regels** om alleen de regels opnieuw te openen die zijn geselecteerd op de pagina **Urenstaat**.
4. Kies de knop **OK**. De status van de urenstaatregel of -regels verandert in **Verzonden**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>Urenstaten per project bekijken en goedkeuren

U kunt voor een project een persoon opgeven die verantwoordelijk is voor het project. Die gegevens worden gekoppeld aan urenstaatregels en kunnen worden gebruikt om een lijst met urenstaten te maken, die door een projectmanager moet worden gecontroleerd en goedgekeurd. De teamprojectmanager kan bijvoorbeeld verantwoordelijk zijn voor bepaalde projecten in uw bedrijf. In dat geval moet de manager worden aangewezen als de **Verantwoordelijke** op de projectkaart. In deze weergave met urenstaatinformatie ziet u de projecttaken die zijn gekoppeld aan een project en het aantal uren dat is verbruikt.

> [!NOTE]
> Om urenstaten te kunnen goedkeuren in het venster **Urenstaat manager op taak** moet u eerst een optie bij **Urenstaat op taakgoedkeuring** in het venster **Resource-instellingen** selecteren. Zie [Resources instellen](projects-how-setup-resources.md) voor meer informatie.

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>Een urenstaat per project goedkeuren of weigeren

1. Voer in het tekstvak **Zoeken** **Urenstaat manager op taak** in en kies vervolgens de gerelateerde koppeling. [!INCLUDE[prod_short](includes/prod_short.md)] geeft een lijst met urenstaatregels weer die zijn gekoppeld aan de projecten waarvoor u verantwoordelijk bent.
2. Kies de actie **Goedkeuren** en kies vervolgens de actie **Alle verzonden regels** om alle regels goed te keuren of kies de actie **Alleen geselecteerde regel(s)** om alleen de regels goed te keuren die zijn geselecteerd op de pagina **Urenstaat**.

    > [!NOTE]
    > U kunt alleen urenstaten goedkeuren die de status **Ingediend** hebben.

3. Om aanvullende informatie over de goedkeuring of afwijzing te geven selecteert u de actie **Verwant** en selecteert u vervolgens **Opmerkingen** en dan **Regelopmerkingen** en voert u opmerkingen in.
4. Kies de knop **Ok**.

> [!NOTE]
> Nadat u een urenstaatregel per project hebt goedgekeurd of geweigerd, kan deze niet meer worden geopend of gewijzigd in het venster **Urenstaat**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Urenstaatregels naar een resourcedagboek boeken
Nadat u de urenstaatposten voor een resource hebt goedgekeurd, kunt u deze boeken naar het relevante resourcedagboek.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resourcedagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Regels voorstellen uit urenstaten**.  
3. Vul op de pagina **Resourcedagboekregels voorstellen** de benodigde velden in.  
4. Kies de knop **OK**. Posten voor gebruik worden gemaakt in het resourcedagboek, waarin u informatie desgewenst kunt wijzigen.  
5. Kies de actie **Boeken**.  
6. Als u de boeking wilt controleren, kiest u de actie **Posten**. De pagina **Resourceposten** wordt geopend met de resultaten van het boeken van het resourcedagboek.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Urenstaatregels in een projectdagboek boeken
Nadat u de urenstaatposten voor een project hebt goedgekeurd, kunt u deze boeken naar het relevante projectdagboek.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectjournalen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Regels voorstellen uit urenstaten**.  
3. Vul op de pagina **Projectdagboekregels voorstellen** de benodigde velden in.  
4. Kies de knop **OK**. Posten voor gebruik worden gemaakt in het projectdagboek, waarin u de informatie desgewenst kunt wijzigen.  

    > [!NOTE]  
    >   Gegevens over het werksoort en of het werk factureerbaar is , wordt uit de urenstaatregel gekopieerd. U kunt indien nodig het aantal uren verminderen en een gedeeltelijke boeking doen. Als u het aantal vermindert, bevat de gemaakte regel de volgende keer dat u de actie **Regels voorstellen uit urenstaten** kiest, het resterende aantal uren.  
5. Kies de actie **Boeken**.  
6. Als u de boeking wilt controleren, kiest u de actie **Posten**. De pagina **Projectposten** wordt geopend met de resultaten van het boeken van het resourcedagboek.

## <a name="to-archive-time-sheets"></a>Urenstaten verplaatsen naar archief
Nadat u urenstaten hebt geboekt, kunt u ze archiveren voor latere naslag. Alle urenstatenregels moeten worden geboekt voordat een urenstaat kan worden gearchiveerd.

> [!NOTE]  
>   Bij het archiveren van een urenstaat wordt de urenstaat verwijderd uit de lijst op de pagina **Urenstaten** en de pagina **Urenstaatmanager**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Urenstaten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de actie **Urenstaten verplaatsen naar archief**.  
3. Vul op de pagina **Urenstaten verplaatsen naar archief** de benodigde velden in en kies de knop **OK**.  
4. Om gearchiveerde urenstaten te bekijken kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Urenstaatarchieven** of **Urenstaatarchiefbeheer** in en kiest u vervolgens de gerelateerde koppeling.

## <a name="see-also"></a>Zie ook
[Projectbeheer](projects-manage-projects.md)  
[Projectbeheer instellen](projects-setup-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
