---
title: Urenstaten gebruiken voor projecten| Microsoft Docs
description: Beschrijft hoe u een urenstaat voor een project maakt, er planningsregels naar kopieert, werksoorten definieert, de urenstaat invult en deze verzendt voor goedkeuring.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5b53768d7a7757f3f3e186e5d241b318a71c770b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758629"
---
# <a name="use-time-sheets-for-jobs"></a>Urenstaten gebruiken voor projecten

U gebruikt de batchverwerking **Urenstaten maken** om urenstaten in te stellen voor een opgegeven aantal perioden of weken. U moet machtigingen hebben om urenstaten te maken.

U kunt uw projectplanningsregels kopiëren en gebruiken in een urenstaat. Op die manier hoeft u de gegevens slechts op één plaats in te voeren en zijn de regelgegevens altijd correct.

Nadat u urenstaatposten voor een project hebt goedgekeurd, kunt u deze boeken naar het relevante projectdagboek of resourcedagboek.

Voordat u urenstaten kunt gebruiken, moet u algemene informatie instellen en een beheerder en een of meer fiatteurs van urenstaten opgeven. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

## <a name="to-create-a-time-sheet"></a>Een urenstaat maken

U kunt de batchverwerking **Urenstaten maken** gebruiken om urenstaten in te stellen voor een opgegeven aantal perioden of weken. Vervolgens kan de eigenaar van de urenstaat deze openen en tijd vastleggen die aan een taak is besteed.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten** in en kies de gerelateerde koppeling.
2. Kies de actie **Urenstaten maken** op de pagina **Overzicht urenstaat**.
3. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > De velden **Urenstaat gebruiken** en **Gebruikers-id eigenaar urenstaat** moeten worden ingevuld op de kaart voor de resource van de urenstaat.
4. Kies de knop **OK**.  

U kunt de urenstaten die u hebt gemaakt, bekijken op de pagina **Overzicht urenstaat**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Projectplanningsregels kopiëren naar een urenstaat
De volgende procedure beschrijft hoe u snel projectplanningsregels toevoegt aan een urenstaat.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **Overzicht urenstaat** een urenstaat voor de betreffende periode en kies vervolgens de actie **Urenstaat bewerken**.  
3. Kies de actie **Regels maken van projectplanning**. Alle projectplanningsregels in de urenstaatperiode worden gekopieerd naar het veld **Resourcenr.** op de urenstaat voor de machine of persoon.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Werksoorten definiëren en er een toevoegen aan een urenstaat
U kunt de werksoort voor alle urenstaatregels voor projecten definiëren. Op deze manier kunt u gegevens toevoegen die u nodig hebt om de klant te factureren voor verschillende soorten werk.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten** in en kies de gerelateerde koppeling.   
2. Open de relevante urenstaat.
3. Kies het veld **Omschrijving**.  
4. Kies op de pagina **Projectdetail urenstaatregel** het veld **Werksoort** en selecteer een werksoort in de lijst, bijvoorbeeld **Km**.  
5. Als er geen werksoorten bestaan, kiest u de actie **Nieuw**.
6. Vul indien nodig op de pagina **Werksoorten** de velden in.
7. Herhaal stap 4 om de nieuwe werksoort aan de urenstaat toe te wijzen.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Urenstaatregels in andere urenstaten opnieuw gebruiken
Als uw urenstaatinformatie van periode tot periode gelijk blijft, kunt u tijd besparen door de regels te kopiëren uit de vorige periode. Vervolgens voert u alleen het tijdsgebruik voor de nieuwe periode in.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten** in en kies de gerelateerde koppeling.  
2. Open de urenstaat voor een periode na de periode voor een bestaande urenstaat met regels.  
3. Kies de actie **Regels kopiëren van vorige urenstaat**.

De regels worden gekopieerd, inclusief details zoals het type en beschrijving. Als de regel bijvoorbeeld is gekoppeld aan een project, wordt het **Projectnr.** gekopieerd. Alle gekopieerde regels hebben de status **Open**. U kunt nu indien nodig de regels wijzigen.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Urenstaatregels invullen en ter goedkeuring verzenden
Urenstaatregistratie wordt bijgehouden in uren, de standaard basiseenheid voor resources. Een urenstaat bevat standaard de algemene werkdagen van maandag tot en met vrijdag.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten** in en kies de gerelateerde koppeling.  
2. Selecteer een urenstaat voor de betreffende periode en kies vervolgens de actie **Urenstaat bewerken**.  
3. Vul de velden indien nodig op een regel in. Voer het aantal uren in dat door de resource op elke dag van de week wordt gebruikt.

    > [!TIP]  
    >   U kunt de som controleren van de urenstaaturen die u hebt ingevoerd in het feitenblok **Overzicht van werkelijk/gebudgetteerd**.  
4. Herhaal stap 3 voor andere werksoorten die de resource uitvoert.
5. Kies de **Verzenden**-actie en kies vervolgens de actie **Alle geopende regels** om alle regels te verzenden of kies de actie **Alleen geselecteerde regel(s)** om alleen de regels te verzenden die zijn geselecteerd op de pagina **Urenstaat**.  

    > [!NOTE]  
    >   U kunt alleen urenstaatregels verzenden waarvoor u tijd hebt ingevoerd.  
6. Als u gegevens wilt wijzigen op een regel die is ingesteld op **Ingediend**, selecteert u de regel en kiest u de actie **Opnieuw openen**.

    > [!NOTE]  
    >   Een beheerder kan een urenstaatregel weigeren die ter goedkeuring is verzonden. Als u een regel de status **Geweigerd** heeft, kunt u wijzigingen aanbrengen in de regel en opnieuw **Indienen** kiezen.  
7. Kies de knop **Ok**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Een urenstaat goedkeuren of weigeren
Een urenstaat moet ter goedkeuring worden ingediend om te worden gebruikt. U kunt afzonderlijke regels goedkeuren en weigeren op een urenstaat of deze terugsturen naar de indiener voor aanvullende actie. Een urenstaat kan worden goedgekeurd op twee manieren:

* Een beheerder van urenstaten kan een urenstaat goedkeuren.
* De persoon die is opgegeven in het veld **Gebruikers-id van fiatteur van urenstaat** op een resourcekaart kan urenstaten van die resource goedkeuren. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstatenmanager** in en kies de gerelateerde koppeling.
2. Selecteer een urenstaat in de lijst.  
3. Kies op de pagina **Urenstaat** de actie **Goedkeuren** en kies vervolgens de actie **Alle verzonden regels** om alle regels goed te keuren of kies de actie **Alleen geselecteerde regels** om alleen de regels toe te keuren die zijn geselecteerd op de pagina **Urenstaat**.
4. Kies de knop **OK**.  
5. U kunt ook de actie **Weigeren** kiezen en stap 4 tot en met 5 volgen.  

> [!TIP]  
>   Gebruik de feitenblokken **Status urenstaat** en **Overzicht van werkelijk/gebudgetteerd** om een overzicht te krijgen van urenstaatgegevens.

Nadat u een urenstaat hebt goedgekeurd of geweigerd, kan deze niet meer worden gewijzigd tenzij deze eerst opnieuw wordt geopend. In de volgende procedure wordt uitgelegd hoe u een goedgekeurde of geweigerde urenstaat opnieuw opent.

## <a name="to-reopen-a-time-sheet"></a>Een urenstaat opnieuw openen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstatenmanager** of **Urenstaten** in en kies de gerelateerde koppeling.
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

1. Voer in het tekstvak **Zoeken** **Urenstaat manager op taak** in en kies vervolgens de gerelateerde koppeling. Microsoft Dynamics NAV geeft een lijst met urenregistratieregels weer die zijn gekoppeld aan de projecten waarvoor u verantwoordelijk bent.
2. Kies op het tabblad **Start** de optie **Goedkeuren**. Kies **Alle** om alle regels goed te keuren. Kies **Geselecteerd** om alleen geselecteerde regels goed te keuren.

    > [!NOTE]
    > U kunt alleen urenstaten goedkeuren die de status **Ingediend** hebben.

3. Voor meer informatie over de goedkeuring of weigering selecteert u een urenstaatregel en kiest u op het tabblad **Navigeren** de optie **Opmerkingen**. Voer in het veld **Datum** een datum in en voer vervolgens een opmerking in het veld **Opmerking** in.
4. Kies de knop **OK**.

> [!NOTE]
> Nadat u een urenstaatregel per project hebt goedgekeurd of geweigerd, kan deze niet meer worden geopend of gewijzigd in het venster **Urenstaat**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Urenstaatregels naar een resourcedagboek boeken
Nadat u de urenstaatposten voor een resource hebt goedgekeurd, kunt u deze boeken naar het relevante resourcedagboek.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resourcedagboek** in en kies de desbetreffende koppeling.  
2. Kies de actie **Regels voorstellen uit urenstaten**.  
3. Vul indien nodig de velden in.  
4. Kies de knop **Ok**. Posten voor gebruik worden gemaakt in het resourcedagboek, waarin u informatie desgewenst kunt wijzigen.  
5. Kies de actie **Boeken**.  
6. Als u de boeking wilt controleren, kiest u de actie **Posten**. De pagina **Resourceposten** wordt geopend met de resultaten van het boeken van het resourcedagboek.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Urenstaatregels in een projectdagboek boeken
Nadat u de urenstaatposten voor een project hebt goedgekeurd, kunt u deze boeken naar het relevante projectdagboek.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectdagboek** in en kies de gerelateerde koppeling.  
2. Kies de actie **Regels voorstellen uit urenstaten**.  
3. Vul indien nodig de velden in.  
4. Kies de knop **Ok**. Posten voor gebruik worden gemaakt in het projectdagboek, waarin u de informatie desgewenst kunt wijzigen.  

    > [!NOTE]  
    >   Gegevens over het werksoort en of het werk factureerbaar is , wordt uit de urenstaatregel gekopieerd. U kunt indien nodig het aantal uren verminderen en een gedeeltelijke boeking doen. Als u het aantal vermindert, bevat de gemaakte regel de volgende keer dat u de actie **Regels voorstellen uit urenstaten** kiest, het resterende aantal uren.  
5. Kies de actie **Boeken**.  
6. Als u de boeking wilt controleren, kiest u de actie **Posten**. De pagina **Projectposten** wordt geopend met de resultaten van het boeken van het resourcedagboek.

## <a name="to-archive-time-sheets"></a>Urenstaten verplaatsen naar archief
Nadat u urenstaten hebt geboekt, kunt u ze archiveren voor latere naslag. Alle urenstatenregels moeten worden geboekt voordat een urenstaat kan worden gearchiveerd.

> [!NOTE]  
>   Bij het archiveren van een urenstaat wordt de urenstaat verwijderd uit de lijst op de pagina **Urenstaten** en de pagina **Urenstaatmanager**.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Urenstaten verplaatsen naar archief** in en kies de gerelateerde koppeling.  
2. Vul de overige velden desgewenst in en kies de knop **OK**.  
3. Als u gearchiveerde urenstaten wilt bekijken, kiest u het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Urenstaatarchieven** of **Urenstatenmanager** in en kiest u vervolgens de gerelateerde koppeling.

## <a name="see-also"></a>Zie ook
[Projectbeheer](projects-manage-projects.md)  
[Projectbeheer instellen](projects-setup-projects.md)    
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)     
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]