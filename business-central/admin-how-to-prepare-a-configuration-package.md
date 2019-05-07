---
title: Een configuratiepakket voorbereiden | Microsoft Docs
description: Wanneer u een nieuw bedrijf configureert, worden de tabelrelaties herkend en verwerkt. Gegevens worden in de juiste volgorde geïmporteerd en toegepast. Dimensietabellen worden eveneens geïmporteerd als ze zijn opgenomen in het configuratiepakket.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fde77f873897d801e6bf06d55d57e9406f352eed
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "941646"
---
# <a name="prepare-a-configuration-package"></a>Een configuratiepakket voorbereiden
Wanneer u een nieuw bedrijf configureert, worden de tabelrelaties herkend en verwerkt. Gegevens worden in de juiste volgorde geïmporteerd en toegepast. Dimensietabellen worden eveneens geïmporteerd als ze zijn opgenomen in het configuratiepakket. Zie [Klantgegevens importeren](admin-migrate-customer-data.md#to-import-customer-data) voor meer informatie. 

Als u uw klant wilt helpen bij het gebruiken van het configuratiepakket, wilt u wellicht een vragenlijst of een reeks vragenlijsten aan het pakket toevoegen. De vragenlijst kan de klant helpen inzicht te krijgen in de verschillende instellingsopties. Meestal worden vragenlijsten gemaakt voor de belangrijkste instellingentabellen, wanneer een klant mogelijk aanvullende richtlijnen over het selecteren van een juiste instelling nodig heeft. Zie voor meer informatie [Waarden van klantinstellingen verzamelen](admin-gather-customer-setup-values.md).

Zorg ervoor dat u zich in het rolcentrum RapidStart Services-implementatie bevindt. Zie voor meer informatie [Rolcentrum RapidStart Services-implementatie gebruiken](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md).

> [!IMPORTANT]  
>  Bij het exporteren en importeren van configuratiepakketten tussen de twee bedrijfdatabases, moeten de databases hetzelfde schema hebben om ervoor te zorgen dat alle gegevens kunnen worden overgedragen. Dit betekent dat de database dezelfde tabel- en veldstructuur moeten hebben, waarin de tabellen dezelfde primaire sleutel hebben en de velden dezelfde id's en gegevenssoorten hebben.  
>   
>  U kunt een configuratiepakket importeren dat is geëxporteerd uit een database met een ander schema dan de doeldatabase. Tabellen of velden in het configuratiepakket die niet voorkomen de doeldatabase, worden echter niet geïmporteerd. Tabellen met verschillende primaire sleutels en velden met verschillende gegevenssoorten worden niet succesvol geïmporteerd. Als in het configuratiepakket bijvoorbeeld tabel **50000, Klant** staat met de primaire sleutel **Code20** en in het configuratiepakket van de database die u wilt importeren, tabel **50000, Bankrekening klant** staat met de primaire sleutel **Code20 + Code 20**, worden de gegevens niet geïmporteerd.  

## <a name="to-create-a-configuration-package"></a>Een configuratiepakket maken  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul op het sneltabblad **Algemeen** de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Als u de tabellen voor configuratievragenlijsten, -sjablonen en -werkblad niet in het pakket wilt opnemen, schakelt u het selectievakje **Configuratietabellen uitsluiten** in. Anders worden deze tabellen automatisch toegevoegd aan de lijst met pakkettabellen bij het exporteren van het pakket.  
5. Kies de actie **Tabellen ophalen**. De batchverwerkingspagina **Pakkettabellen ophalen** wordt geopend.  
6. Kies het veld **Tabellen selecteren**. De pagina **Selectie voor configuratie** wordt geopend.  
7. Kies de actie **Alles selecteren** om alle tabellen aan het pakket toe te voegen of schakel het selectievakje **Geselecteerd** in voor elke tabel in de lijst die u wilt toevoegen.
8. Kies de knop **Ok**. Het aantal tabellen dat u hebt geselecteerd wordt vermeld in het veld **Tabellen selecteren**. Geef extra opties op en kies de knop **OK**. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen worden toegevoegd aan de regels van de pagina **Pakket voor configuratie**.  

    > [!NOTE]  
    >  U kunt dit ook doen in het configuratiewerkblad. Selecteer de tabellen die u wilt opnemen in het pakket en kies vervolgens de actie **Pakket toewijzen**.

9. Als u de velden wilt selecteren die u wilt opnemen uit een tabel, selecteert u de tabel en de kiest u op het tabblad **Regels** de actie **Velden**.
Geef op welke velden worden opgenomen in het pakket. Standaard zijn alle velden opgenomen.

    - Als u alleen de velden wilt selecteren die u wilt opnemen, kiest u de actie **Opgenomen items wissen**. U kunt alle velden toevoegen door de actie **Opgenomen items instellen** te kiezen.  
    - Als u wilt opgeven dat de veldgegevens niet moeten worden gevalideerd, schakelt u het selectievakje **Veld valideren** voor het veld uit.  

10. Bepaal of u mogelijke fouten hebt geïntroduceerd door de actie **Pakket valideren** te kiezen. Dit kan gebeuren wanneer u tabellen waarvan uw configuratie afhankelijk is niet opneemt.  
11. Kies de knop **OK**.  

Nadat u de lijst met velden die u wilt opnemen uit een tabel hebt verfijnd, kunt u uw resultaten in Excel controleren.  

### <a name="to-filter-and-review-your-dataset"></a>Uw gegevensset filteren en bekijken  
1. Als u wilt filteren op een bepaalde set records die u wilt opnemen in het pakket, kiest u op het tabblad **Regels** de actie **Filters** en geeft u vervolgens de juiste filterwaarden op.  
2. Kies op de pakketkaart op het tabblad **Regels** de actie **Exporteren naar Excel**.  
3. Bevestig de berichten die de export van gegevens naar Excel mogelijk maken. Het benoemde XLSX-bestand wordt geopend. Bekijk de records die zijn geëxporteerd.  
4. Sluit Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Een sjabloon opnemen voor toepassing op een tabel  
Voor bepaalde tabellen, zoals een tabel met hoofdgegevens, kunt u een sjabloon opgeven die kan worden toegepast op de gegevens. De sjabloon kan de vereiste velden bevatten die u wilt toepassen op alle hoofdgegevens en die nooit mogen variëren. Zo kunt u bijvoorbeeld een sjabloon maken die kan worden gebruikt met klantgegevens. De sjabloon kan alle vereiste velden bevatten waarmee vervolgens op consistente wijze gestandaardiseerde gegevens kunnen worden geïmporteerd. Informatie die niet kan worden gestandaardiseerd, zoals de naam van de klant, wordt vervolgens behandeld als u klantgegevens importeert.

1. Selecteer een tabel op de pagina **Pakketkaart voor configuratie** en kies vervolgens het veld **Gegevenssjabloon**. Er wordt een lijst met sjablonen weergegeven die zijn gebaseerd op de tabel.
2. Selecteer een sjabloon en kies vervolgens de knop **OK**.  

Nadat het pakket is voltooid, gebruikt u de volgende procedure om het pakket op te slaan in een bestand. Vervolgens kunt u het pakket aan een klant of partner geven om te gebruiken.

### <a name="to-save-and-export-a-configuration-package"></a>Een configuratiepakket opslaan en exporteren  
- Kies op de pagina **Pakketkaart voor configuratie** de actie **Pakket exporteren**.  

Het pakket wordt gemaakt vanuit een .rapidstart-bestand, dat de pakketinhoud in een gecomprimeerde indeling aanlevert. Configuratievragenlijsten, -sjablonen en het configuratiewerkblad worden automatisch toegevoegd aan het pakket tenzij u deze uitdrukkelijk uitsluit.  

U kunt het bestand opslaan met een naam die voor u zinvol is, maar u kunt de extensie van het bestand niet wijzigen. Het moet .rapidstart zijn.  

### <a name="to-copy-a-configuration-package"></a>Een configuratiepakket kopiëren  
Nadat u een pakket hebt gemaakt dat voldoet aan de meeste van uw behoeften, kunt u dit als basis gebruiken voor het maken van vergelijkbare pakketten. Hiermee kan de implementatie worden versneld en de herhaalbaarheid van RapidStart Services worden verbeterd.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een pakket in de lijst en kies vervolgens de actie **Pakket kopiëren**.  
3. Voer in het veld **Nieuwe pakketcode** een code in voor het nieuwe pakket.  
4. Schakel het selectievakje **Gegevens kopiëren** in als u ook databasegegevens wilt kopiëren vanuit het bestaande pakket.  
5. Kies de knop **OK**.

## <a name="to-customize-a-configuration-package"></a>Een configuratiepakket aanpassen
Gebruik het configuratiewerkblad voor het verzamelen en categoriseren van de gegevens die u wilt gebruiken voor het configureren van een nieuw bedrijf en voor het op een logische manier rangschikken van tabellen. De opmaak van het werkblad is gebaseerd op een eenvoudige hiërarchie: gebieden bevatten groepen, die weer tabellen bevatten. Gebieden en groepen zijn optioneel, maar zijn nodig als u een overzicht van het configuratieproces wilt inschakelen in het Rolcentrum RapidStart Services.

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies in het veld **Regelsoort** de optie **Gebied**. Voer in het veld **Naam** een beschrijvende naam in.  
3.  Kies in het veld **Regelsoort** de optie **Groep**. Voer in het veld **Naam** een beschrijvende naam in.  
4.  Kies in het veld **Regelsoort** de optie **Tabel**. Selecteer in het veld **Tabel-id** de tabel die u wilt opnemen in het werkblad.  

U kunt nu de tabellen toewijzen aan specifieke configuratiepakketten die u hebt gemaakt of die u wilt gaan maken. Zie [Een tabel aan een configuratiepakket toewijzen](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package) voor meer informatie.

## <a name="to-work-with-promoted-tables"></a>Werken met gepromoveerde tabellen  
1. Selecteer het selectievakje **Gepromoveerde tabel** om een tabel aan te duiden die vaak worden gebruikt tijdens de installatie door een gemiddelde klant, bijvoorbeeld de tabel **Grootboekrekening**. Wanneer een tabel deze aanduiding bevat, kan een klant op eenvoudige wijze zijn werkblad zodanig filteren dat alleen de lijst met gepromoveerde tabellen wordt weergegeven die aandacht vereisen.  
2. Als u de gefilterde weergave wilt zien, kiest u de actie **Alleen gepromoveerd**. De lijst met tabellen bevat alleen de tabellen waarvoor het selectievakje is ingeschakeld.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Een tabel toewijzen aan een configuratiepakket  
Nadat u de tabellen hebt gedefinieerd die u wilt behandelen als onderdeel van de configuratie, kunt u de tabellen gemakkelijk toewijzen aan configuratiepakketten. U kunt een tabel aan slechts één pakket toewijzen. In de volgende procedure wijst u het pakket toe vanuit het configuratiewerkblad.  

> [!NOTE]  
>  U kunt ook rechtstreeks een pakket maken en hier tabellen aan toevoegen. Zie [Een configuratiepakket maken](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package) voor meer informatie.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer in het configuratiewerkblad een regel of groep regels die u wilt toewijzen aan een configuratiepakket en kies vervolgens **Pakket toewijzen**.  
3.  Selecteer een pakket in de lijst of kies de actie **Nieuw** om een nieuw pakket te maken en kies vervolgens de knop **OK**.  

    Als een tabel niet al in het pakket is opgenomen, wordt deze nu toegevoegd. Het veld voor de pakketcode op de voorstelregel wordt ingevuld met de code van het pakket waaraan de tabel is toegewezen.  
4. Als u een bestaand pakket kiest, kunt u zien hoeveel tabellen het pakket al bevat aan de hand van de informatie in het veld **Aantal tabellen**.

## <a name="to-review-or-customize-existing-database-data"></a>Bestaande databasegegevens controleren en aanpassen
Als u een configuratiepakket voor een oplossing maakt, kunt u de beschikbare databasegegevens weergeven en aanpassen aan de behoeften van uw klant. De databasetabel moet over een bijbehorende pagina beschikken.  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.
2. Bepaal in het configuratiewerkblad van welke tabellen u de gegevens wilt bekijken of aanpassen.  

    > [!NOTE]  
    >  Zorg ervoor dat aan elke tabel een pagina-id is toegewezen. Voor standaard [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen wordt de waarde automatisch ingevuld. Voor aangepaste tabellen moet u de id opgeven.

3. Kies de actie **Databasegegevens**. De pagina voor de gerelateerde pagina wordt geopend.
4. Bekijk de beschikbare informatie. Wijzig deze zo nodig door records te verwijderen die niet relevant zijn of door nieuwe records toe te voegen.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Gegevens kopiëren van een testomgeving naar een productieomgeving  
Nadat u alle instellingsgegevens hebt ingevoerd en getest, kunt u doorgaan met het kopiëren van gegevens naar uw productieomgeving. U maakt een nieuw bedrijf in dezelfde database.

1. Open en initialiseer het nieuwe bedrijf.  
2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.  
3. Kies de actie **Gegevens kopiëren van bedrijf**.  
4. Kies op de pagina **Bedrijfsgegevens kopiëren** het veld **Kopiëren van**. De pagina **Bedrijven** wordt geopend.  
5. Selecteer het bedrijf waaruit u gegevens wilt kopiëren en kies vervolgens de knop **OK**. Er wordt een lijst geopend met tabellen die zijn geselecteerd op het configuratiewerkblad. In deze lijst worden alleen tabellen opgenomen die records bevatten.
6. Selecteer de tabellen waaruit u gegevens wilt kopiëren en kies vervolgens de actie **Gegevens kopiëren**. Kies op de pagina **Bedrijfsgegevens kopiëren** de knop **OK**.  

## <a name="see-also"></a>Zie ook  
[Waarden van klantinstellingen verzamelen](admin-gather-customer-setup-values.md)  
[Een bedrijfsconfiguratie instellen](admin-set-up-company-configuration.md)  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
