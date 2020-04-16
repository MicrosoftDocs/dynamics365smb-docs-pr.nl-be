---
title: De bedrijfsconfiguratie beheren in een werkblad | Microsoft Docs
description: Het configuratiewerkblad is de centrale locatie waar u configuratieactiviteiten kunt plannen, bijhouden en uitvoeren. U kunt een werkblad maken voor elk bedrijf waarmee u werkt of een standaardconfiguratiewerkblad maken dat kan worden gebruikt voor het configureren van meerdere identieke bedrijven.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ab8b53ec5f913e07b80cc04a44805d77b10ffe86
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187136"
---
# <a name="manage-company-configuration-in-a-worksheet"></a>De bedrijfsconfiguratie beheren in een werkblad
Het configuratiewerkblad is de centrale locatie waar u configuratieactiviteiten kunt plannen, bijhouden en uitvoeren. U kunt een werkblad maken voor elk bedrijf waarmee u werkt of een standaardconfiguratiewerkblad maken dat kan worden gebruikt voor het configureren van meerdere identieke bedrijven.  

De eerste stap bij het voorbereiden van een configuratiepakket is het selecteren van een bedrijf dat u al hebt ingesteld en aangepast aan de behoeften van uw oplossing. Dit bedrijf fungeert als de basislijn voor uw configuratieactiviteiten voor nieuwe bedrijven. In het werkblad wijst u de tabellen toe die u door uw configuratie wilt laten besturen en verwerken. Aangezien de meeste tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] relaties en afhankelijkheden met andere tabellen hebben, moet u zo nodig ook deze gerelateerde tabellen opnemen. Samen fungeren deze tabellen dan als de structuur waaromheen u een nieuw bedrijf opbouwt. De volgende stappen helpen u bij het inpakken en vervolgens implementeren van uw configuratie.  

Als planningsmiddel bij het bijhouden en controleren van uw werk gebruikt u het feitenblok **Pakkettabel voor configuratie** om informatie over records te zien. Gebruik het feitenblok **Aan configuratie gerelateerde tabellen** om het feitenblok tabelrelaties bekijken.  

De volgende procedures laten zien hoe u tabelgegevens voor uw configuratie kunt toevoegen en aanpassen.  

## <a name="to-open-the-configuration-worksheet"></a>Het configuratiewerkblad openen  
1.  Open in [!INCLUDE[d365fin](includes/d365fin_md.md)] het bedrijf dat de basislijn voor configuratie vormt en open vervolgens het rolcentrum RapidStart Services-implementatie.  
2.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en kies de desbetreffende koppeling.  

## <a name="to-add-a-table-to-the-worksheet"></a>Een tabel toevoegen aan het werkblad  
1.  Kies op de pagina **Werkblad voor configuratie** de actie **Lijst bewerken**.  
2.  Selecteer op de eerste regel in het veld **Regelsoort** **Tabel**.  
4.  Selecteer in het veld **Tabel-id** de tabel die u aan uw configuratie wilt toevoegen.  
5.  Voer in het veld **Pagina-id** de id in van de pagina die is gekoppeld aan de tabel. Voor standaardtabellen wordt de waarde automatisch ingevuld. Voor aangepaste tabellen moet u de id opgeven.
6.  Voer in het veld **Referentie** de url in van een documentatiepagina, bijvoorbeeld in de Help, met beste praktijken of instructies voor het instellen van de tabel.  
7.  Als u gerelateerde tabellen wilt toevoegen, kiest u de actie **Gerelateerde tabellen ophalen**.  

    > [!NOTE]  
    > Gerelateerde tabellen worden niet toegevoegd met de actie **Gerelateerde tabellen ophalen** als een van de volgende situaties bestaat:
    > - De relatie is voorwaardelijk.  
    > Voorbeeld: als u gerelateerde tabellen voor de tabel **Klant** ophaalt, wordt de tabel **Vestiging** niet toegevoegd, omdat deze slechts voorwaardelijk is gerelateerd aan de tabel **Klant**, namelijk als het veld **Vestiging** in de tabel **Klant** is gevuld.  
    > - De gerelateerde tabel wordt gefilterd.  
    > Voorbeeld: Een veld in de gekoppelde tabel heeft een WHERE-clausule. De reden hiervoor is dat de informatie van de betreffende relaties is opgeslagen in de systeemtabel **Veld**, die niet volledig toegankelijk is voor de toepassing.  
    > U moet dergelijke soorten tabellen handmatig toevoegen door stap 4 in deze procedure te volgen.  

8.  U kunt de resulterende lijst van tabellen wijzigen door een tabel te selecteren die u wilt verwijderen en vervolgens de actie **Verwijderen** te kiezen.  
9. Herhaal deze stappen voor elke code die u aan de configuratie wilt toevoegen.  
10. Als u dubbele tabelinformatie wilt verwijderen (wat het gevolg kan zijn van de actie **Gerelateerde tabellen ophalen**), kiest u de actie **Dubbele regels verwijderen**. Hierdoor worden dubbele tabellen met dezelfde pakketcode verwijderd.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Meerdere tabellen toevoegen aan het configuratiewerkblad  
1. Kies de actie **Tabellen ophalen**. De batchverwerkingspagina **Configuratie voor tabellen ophalen** wordt geopend.  
2. Geef op het sneltabblad **Opties** de soorten tabellen op die u aan de configuratie wilt toevoegen, zoals wordt beschreven in de volgende tabel.

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**Alleen met gegevens opnemen**|Schakel dit selectievakje in om alleen die tabellen op te nemen die gegevens bevatten. U wilt bijvoorbeeld een tabel opnemen waarin de typische betalingscondities die uw oplossing ondersteunt al zijn gedefinieerd.|  
    |**Gerelateerde tabellen opnemen**|Schakel dit selectievakje in om alle gerelateerde tabellen op te nemen. Zie stap 3 van deze procedure om een subset van gerelateerde tabellen toe te voegen.|  
    |**Dimensietabellen opnemen**|Schakel het selectievakje in als u dimensietabellen wilt opnemen.|  
    |**Alleen gelicentieerd tabellen opnemen**|Schakel dit selectievakje in als u alleen de tabellen wilt opnemen waartoe de licentie waaronder u het werkblad maakt u toegang biedt.|

3. Stel zo nodig op het sneltabblad **Object** filters in om de soorten tabellen op te geven die u wilt opnemen of uitsluiten.  
4. Kies de knop **Ok**. [!INCLUDE[d365fin](includes/d365fin_md.md)] tabellen worden toegevoegd aan het voorstel. Elke vermelding in de lijst heeft een regel van het soort **Tabel**.  
5. Als u dubbele tabelinformatie wilt verwijderen (wat het gevolg kan zijn van de actie **Tabellen ophalen**), kiest u de actie **Dubbele regels verwijderen**. Hierdoor worden dubbele tabellen met dezelfde pakketcode verwijderd.  
6. U kunt aan het werkblad tabellen toevoegen die zijn gerelateerd aan een tabel die u hebt geselecteerd. Raadpleeg de informatie in het feitenblok **Gerelateerde tabellen** om te zien of er tabellen ontbreken. U kunt gerelateerde tabellen voor een bepaalde tabel toevoegen door de tabel te selecteren in de lijst en de actie **Gerelateerde tabellen ophalen** te kiezen.  

    > [!NOTE]  
    > Gerelateerde tabellen worden niet toegevoegd met de actie **Gerelateerde tabellen ophalen** als een van de volgende situaties bestaat:
    > - De relatie is voorwaardelijk.  
    > Voorbeeld: als u gerelateerde tabellen voor de tabel **Klant** ophaalt, wordt de tabel **Vestiging** niet toegevoegd, omdat deze slechts voorwaardelijk is gerelateerd aan de tabel **Klant**, namelijk als het veld **Vestiging** in de tabel **Klant** is gevuld.  
    > - De gerelateerde tabel wordt gefilterd.  
    > Voorbeeld: Een veld in de gekoppelde tabel heeft een WHERE-clausule. De reden hiervoor is dat dit de desbetreffende relatiegegevens worden opgeslagen in de virtuele tabel **Veld** en om redenen van prestaties niet beschikbaar zijn op de pagina's zoals het configuratievoorstel.  
    > U moet gerelateerde tabellen met dergelijke complexe relaties handmatig toevoegen door stap 4 te volgen in [Een tabel toevoegen aan het werkblad](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet).

7. Als u tabellen wilt verwijderen uit de resulterende lijst met tabellen, selecteert u de tabel die u wilt verwijderen, en kiest u vervolgens de actie **Verwijderen**.  

Gebruik de volgende procedure om op te geven van welke tabel u velden wilt opnemen. Nadat u deze specificatie hebt uitgevoerd, kunt u de tabel naar Excel exporteren en de structuur van de tabel gebruiken als sjabloon voor het verzamelen van klantgegevens. Zie voor meer informatie [Klantgegevens migreren voorbereiden](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Een set velden en records opgeven voor een configuratietabel  
1. Selecteer een tabel in de lijst met configuratietabellen en kies vervolgens de actie **Lijst bewerken**.  
2. Selecteer een tabel waarvoor u veldgegevens wilt opgeven en kies vervolgens de actie **Velden**.  
3. Als u alleen de velden wilt selecteren die u wilt opnemen, kiest u de actie **Opgenomen items wissen**. U kunt alle velden toevoegen door de actie **Opgenomen items instellen** te kiezen.  
4. Als u wilt opgeven dat de veldgegevens niet moeten worden gevalideerd, schakelt u het selectievakje **Veld valideren** voor het veld uit.  
5. Kies de knop **Ok**.  
6. Als u wilt filteren op een bepaalde set records die u wilt opnemen in het configuratiewerkblad, kiest u de actie **Filters** en geeft u vervolgens de juiste filterwaarden op.

U kunt functionaliteitsgebieden en groepen tabellen maken in het werkblad om vergelijkbare functionaliteit bij elkaar te zetten. Zo kunt u bijvoorbeeld bij het instellen van het rekeningschema voor uw configuratie besluiten om een groep boekingstabellen te maken. Gebieden worden meestal gebruikt om een set tabellen die overeenkomen met een functioneel gebied te groeperen. Elk gebied kan groepen bevatten. Een groep kan worden gebruikt voor het bij elkaar zetten van tabellen met een algemene betekenis.  

In de volgende procedure wordt beschreven hoe u benamingen van gebieden en groepen kunt toevoegen nadat u de eerste lijst met tabellen hebt gemaakt. Nadat u deze categorieën hebt toegevoegd, kunt u doorgaan met het toevoegen en wijzigen van uw lijst met tabellen.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Functionaliteit categoriseren en groeperen in het werkblad  
1. Voeg aan het begin van een gebied een nieuwe regel in het werkblad in.  
2. Kies in het veld **Regelsoort** de optie **Gebied**. Voer in het veld **Naam** een naam voor het gebied in.  
3. Voeg aan het begin van een groep tabellen een nieuwe regel in het werkblad in.  
4. Kies in het veld **Regelsoort** de optie **Groep**. Voer in het veld **Naam** een naam voor het gebied in. De naam van de groep wordt automatisch ingesprongen weergegeven.  
5. Als u tabellen naar de juiste categorie wilt verplaatsen, selecteert u de tabel die u wilt verplaatsen en kiest u de actie **Omhoog** of **Omlaag**. U kunt ook een werkbladregel verwijderen en de tabel opnieuw invoegen op de vereiste locatie.  

Sommige [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen zijn standaard en de gegevens hierin veranderen waarschijnlijk niet van implementatie tot implementatie. Derhalve kunt u, om uw klant te helpen focussen, deze tabellen uit het werkblad verwijderen nadat u ze hebt opgenomen in het configuratiepakket. Wanneer de tabellen eenmaal zijn toegevoegd, blijven zij onderdeel van het configuratiepakket.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Een standaardtabel in het werkblad verwijderen  
Nadat u alle benodigde tabellen hebt toegevoegd aan een configuratiepakket, bepaalt u welke tabellen geen aandacht van de klant vereisen.  
1.  Selecteer de tabellen en verwijder deze vervolgens door de actie **Verwijderen** te kiezen.  

    > [!NOTE]  
    >  De tabellen blijven in het pakket, hoewel ze van het werkblad zijn verwijderd.  

## <a name="to-review-and-customize-existing-database-data"></a>Bestaande databasegegevens controleren en aanpassen
Als u een configuratiepakket voor een oplossing maakt, kunt u de beschikbare databasegegevens weergeven en aanpassen aan de behoeften van uw klant. De databasetabel moet over een bijbehorende pagina beschikken.  

## <a name="to-customize-data-in-the-database"></a>Gegevens in de database aanpassen  

1.  Bepaal op de pagina **Configuratiewerkblad** van welke tabellen u de gegevens wilt bekijken of aanpassen.  

    > [!NOTE]  
    >  Zorg ervoor dat aan elke tabel een pagina-id is toegewezen. Voor standaard [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen wordt de waarde automatisch ingevuld. Voor aangepaste tabellen moet u de id opgeven.  

2.  Kies de actie **Databasegegevens**.  

     De [!INCLUDE[d365fin](includes/d365fin_md.md)]-pagina voor de pagina wordt geopend.  

3.  Bekijk de beschikbare informatie. Wijzig deze zo nodig door records te verwijderen die niet relevant zijn of door nieuwe records toe te voegen.

## <a name="see-also"></a>Zie ook  
[Een bedrijfsconfiguratie instellen](admin-set-up-company-configuration.md)  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
