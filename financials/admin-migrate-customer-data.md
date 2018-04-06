---
title: Klantgegevens migreren | Microsoft Docs
description: U kunt bestaande klantgegevens van een bestaand ERP-systeem migreren naar Business Central met RapidStart Services. U kunt Excel .xlsx-bestanden gebruiken als gegevensdrager. U kunt de gegevens ook handmatig verplaatsen door deze rechtstreeks in het bedrijf in te voeren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 96cc05cb450bd37da5699c0962bb7e9deb7d5248
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="migrate-customer-data"></a>Klantgegevens migreren
U kunt bestaande klantgegevens van een bestaand ERP-systeem migreren naar [!INCLUDE[d365fin](includes/d365fin_md.md)] met de hulpprogramma's voor gegevensmigratie van RapidStart Services. U kunt Excel-bestanden gebruiken als gegevensdrager. U kunt de gegevens ook handmatig verplaatsen door deze rechtstreeks in het bedrijf in te voeren.

De vensters **Migratieoverzicht** en **Werkblad voor configuratie** bieden ook toegang tot de functies en weergaven voor taken die betrekking hebben op gegevensmigratie. Het is raadzaam één tabel tegelijk te migreren om afhankelijkheden in uw gegevens te verwerken. De migratie betreft ook de mastergegevenstabellen met informatie over klanten, leveranciers, artikelen, contactpersonen en het grootboek.  

# <a name="to-import-configuration-packages"></a>Configuratiepakketten importeren
Wanneer u een nieuw bedrijf maakt, kunt u de bedrijfsinstellingen voor het nieuwe bedrijf importeren. U importeert de instellingen vanuit een .rapidstart-bestand, dat de pakketinhoud in een gecomprimeerde indeling aanlevert. Er wordt een overeenkomende set standaard gegevensmigratietabellen geïmporteerd. De gegevensreeks bevat hoofdgegevenstabellen en instellingsgegevenstabellen. Uw eerste taak in gegevensmigratie is evalueren of de standaardinstellingen van de migratie voldoen aan de behoeften van het nieuwe bedrijf.

> [!NOTE]  
>  U kunt niet een bestand dat niet reeds een RapidStart Services configuratiepakket is, hernoemen als een .rapidstart-configuratiepakketbestand en het vervolgens proberen te importeren. Als u dit probeert, verschijnt er een foutbericht.  

Zorg ervoor, voordat u begint, dat u zich in het rolcentrum RapidStart Services-implementatie bevindt.

> [!IMPORTANT]  
>  Bij het exporteren en importeren van configuratiepakketten tussen de twee bedrijfdatabases, moeten de databases hetzelfde schema hebben om ervoor te zorgen dat alle gegevens kunnen worden overgedragen. Dit betekent dat de database dezelfde tabel- en veldstructuur moeten hebben, waarin de tabellen dezelfde primaire sleutel hebben en de velden dezelfde id's en gegevenssoorten hebben.  
>   
>  U kunt een configuratiepakket importeren dat is geëxporteerd uit een database met een ander schema dan de doeldatabase. Tabellen of velden in het configuratiepakket die niet voorkomen de doeldatabase, worden echter niet geïmporteerd.
>   
> Tabellen die verschillende primaire sleutels en velden met verschillende gegevenssoorten hebben, kunnen niet succesvol geïmporteerd worden. Als in het configuratiepakket bijvoorbeeld tabel **50000 Klant** staat met de primaire sleutel **Code20** en in het configuratiepakket van de database die u wilt importeren, tabel **50000 Bankrekening klant** staat met de primaire sleutel **Code20 + Code 20**, worden de gegevens niet geïmporteerd.  

1. Open het nieuw bedrijf.  
2. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
3. Kies de actie **Pakket importeren**. Navigeer naar het .rapidstart-pakketbestand dat u wilt importeren en kies vervolgens de actie **Openen**. Tijdens het importeren wordt de inhoud van het pakket gedecomprimeerd en wordt de pakketrecord gemaakt.  

    Wanneer het importeren voltooid is, kunt u het aantal configuratietabellen dat is geïmporteerd bekijken in het veld **Aantal tabellen**.  
4. Als u de lijst met configuratietabellen wilt controleren, kiest u de actie **Weergeven**.  
5. Als u het pakket wilt toepassen, kiest u de actie **Pakket toepassen**.  

    > [!NOTE]  
    >  De gegevens over de gegevensmigratie zijn gebaseerd op configuratiesjablonen, als u deze opgeeft. U moet de sjabloon eerst bijwerken om de lijst met velden te kunnen wijzigen.  

6.  Als u de veldselecties wilt bekijken, selecteert u een tabel en kiest u op het tabblad **Regels** de actie **Velden**. Vergelijk en bekijk het aantal velden dat beschikbaar is met het aantal velden waarvan de gegevens zijn toegepast.  

Als de selectie van tabellen niet aan uw behoeften voldoet, kunt u een of meer nieuwe gegevensmigratiebestanden maken. Als de bestanden voldoende zijn, kunt u doorgaan met de gegevensmigratie met behulp van Excel- of XML-bestanden.

## <a name="to-create-a-data-migration-file"></a>Een gegevensmigratiebestand maken
U kunt nieuwe gegevensmigratiebestanden maken en aanpassen voor uw bedrijf. Een bestand kan echter alleen worden gebruikt voor het migreren van een veld waarvan de eigenschap **Veldklasse** is ingesteld op **Normaal**.  

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiepakket** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer en open het pakket dat u wilt gebruiken om gegevens te migreren en kies de actie **Tabellen ophalen**. Het venster **Pakkettabel ophalen** wordt geopend.  
3. Voer in het veld **Tabel-id** een tabelnummer in of selecteer een tabel in de lijst, bijvoorbeeld tabel 18, **Klant**. Het veld **Tabelnaam** wordt automatisch ingevuld.  
4. Selecteer de nieuwe migratietabel en kies op het tabblad **Tabellen** de actie **Velden**. Het venster **Migratievelden** wordt geopend.  
5. Wis het selectievakje **Veld opnemen** voor elk veld dat u niet wilt importeren en kies vervolgens de actie **Opgenomen items instellen** of **Opgenomen items wissen**.  

> [!IMPORTANT]  
>  Als het selectievakje **Veld opnemen** standaard is ingeschakeld, is dat veld onderdeel van de primaire sleutel. De selectie moet niet worden gewist, anders worden fouten geïntroduceerd en kan de record niet worden geïmporteerd.  
>
>  Als u een veld opneemt dat een relatie heeft met een andere tabel, is het selectievakje **Veld valideren** automatisch ingeschakeld. Validatie kan leiden tot het bijwerken van andere velden in deze en andere tabellen en wordt uitgevoerd in de volgorde van het veldnummer.  

Er wordt een nieuwe migratietabel gemaakt.  

## <a name="to-export-data-migration-files"></a>Gegevensmigratiebestanden exporteren
Nadat u hebt bepaald naar welke tabellen u klantgegevens wilt overbrengen, kunt u de bestanden exporteren.  

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer en open het pakket dat u wilt gebruiken voor het exporteren.
3. Selecteer de tabel of tabellen die u wilt exporteren en kies vervolgens de actie **Naar Excel exporteren**.
4. Sla het geëxporteerde Excel-bestand op.  
5. Herhaal deze procedure voor alle relevante gegevensmigratietabellen. Als u meerdere tabellen tegelijk selecteert, worden de gegevens ervan naar een gemeenschappelijke werkmap geëxporteerd.  

Als de tabel leeg is, bevat het resulterende gegevensmigratiebestand lege cellen voor de velden die u hebt geselecteerd toen u migratietabellen koos of maakte voor het nieuwe bedrijf. Als de geselecteerde gegevensmigratietabel gegevens bevat, worden deze geëxporteerd.  

## <a name="to-map-values-to-be-used-during-import"></a>Waarden toewijzen die moeten worden gebruikt tijdens import
Als u gegevens vereffent die u hebt geïmporteerd uit Excel of uit een RapidStart-pakket, behandelt en verwerkt [!INCLUDE[d365fin](includes/d365fin_md.md)] de toewijzing op basis van tabelrelaties:  

- Als u een toewijzing rechtstreeks voor een veld in een tabel definieert, wordt deze door [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt.  

- Als het veld een relatie met een andere tabel heeft, zoekt [!INCLUDE[d365fin](includes/d365fin_md.md)] naar de toewijzing die is gedefinieerd voor het veld met de primaire sleutel in de gerelateerde tabel. De gekoppelde tabel moet echter deel uitmaken van het configuratiepakket.  

- Als de toewijzingsinformatie op beide plaatsen is gedefinieerd (rechtstreeks voor het veld en in de gekoppelde tabel voor de primaire sleutel), zoekt [!INCLUDE[d365fin](includes/d365fin_md.md)] op beide plaatsen naar de toewijzing.  

- Als dezelfde toewijzingen rechtstreeks voor een veld en in de gerelateerde tabel zijn gedefinieerd maar verschillende waarden hebben, heeft de toewijzing die rechtstreeks voor het veld is gedefinieerd, prioriteit op de toewijzing die is gedefinieerd voor de tabel waarnaar het veld verwijst.  

In de volgende procedures moet u van tevoren kijken welke waarden u wilt behouden tijdens het migratieproces. Als u de volgende procedures wilt uitvoeren, hebt u gegevensmigratiebestanden (.xlsx) nodig die u hebt geëxporteerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie voor meer informatie het gedeelte "Gegevensmigratiebestanden exporteren".

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.
2. Open het pakket voor het betreffende bedrijf.  
3. Selecteer de tabel waarvoor u waarden wilt toewijzen, en kies op het sneltabblad **Tabellen** de actie **Velden**.  
4. Voor elk veld dat u wilt toewijzen, kiest u de actie **Toewijzing**.  
5. Voer in het veld **Oude waarde** de waarde in die u wilt wijzigen. Voer in het veld **Nieuwe waarde** de waarde in waarin u de oude waarde wilt wijzigen. Kies de knop **OK**.  
6. Importeer de klantgegevens. Zie voor meer informatie het gedeelte "Klantgegevens importeren".
7. Kijk in het veld **Aantal pakketfouten** of er fouten zijn gerapporteerd. Zoom in om fouten te bekijken als die er zijn. Het venster **Pakketrecords voor configuratie** wordt geopend.
8. Kies de actie **Fout weergeven**. U ziet het volgende foutbericht: **<option> is geen geldige optie. Geldige opties zijn <valid option list>**. Kies de knop **OK**.  
9. Als u de toewijzing wilt toepassen die u hebt ingesteld, kiest u de actie **Gegevens toepassen**.  

### <a name="mapping-example"></a>Voorbeeld van toewijzing  
In het volgende voorbeeld ziet u hoe [!INCLUDE[d365fin](includes/d365fin_md.md)] koppelingsdefinities implementeert.  

1. Een configuratietabel maken die een tabel **Verkoper/Inkoper** heeft. Een koppeling definiëren voor het veld **Code**.  
2. Voeg extra tabellen toe aan het pakket, bijvoorbeeld **Klant** en **Leverancier**. Deze tabellen verwijzen beide naar de tabel **Verkoper/Inkoper** via respectievelijk de **Verkoperscode** en de **Inkoperscode**.  
3. Wanneer u gegevens vereffent, wordt de toewijzing die u voor het veld **Code** in de tabel **Verkoper/Inkoper** hebt opgegeven, ook meegenomen tijdens het verwerken van de velden **Verkoperscode** en **Inkoperscode**.

## <a name="to-add-additional-values-to-included365finincludesd365finmdmd"></a>Aanvullende waarden toevoegen aan [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de tabel waarvoor u extra waarden wilt toevoegen, en kies op het tabblad **Tabellen** de actie **Velden**.  
3. Voor de velden waarvoor u wilt dat [!INCLUDE[d365fin](includes/d365fin_md.md)] aanvullende waarden toestaat tijdens migratie, schakelt u het selectievakje **Ontbrekende codes maken** in.  
4. Importeer de klantgegevens. Zie voor meer informatie het gedeelte "Klantgegevens importeren".

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Gegevens opschonen en verwerken voordat u ze toepast
In sommige gevallen wilt u wellicht klantgegevens opruimen en verwerken voordat u deze op de database toepast. Als u dat wilt doen, kunt u de batchverwerking **Configuratiepakket - verwerken** gebruiken om problemen op te lossen, zoals:  

- Zet datums en decimalen om in de notatie die vereist is voor de instellingen op de computer van een gebruiker.  
- Verwijder voorloopspaties/volgspaties of speciale tekens.  

Nadat u de batchverwerking hebt uitgevoerd, gebruikt u de volgende procedure om de gegevens te verwerken.  

1. Open het configuratiepakket voor het bedrijf.  
2. Kies de actie **Gegevens verwerken**.  
3. Als u de toewijzing wilt toepassen die u hebt ingesteld, kiest u de actie **Gegevens toepassen**.

## <a name="to-migrate-customer-data"></a>Klantgegevens migreren
Nadat u een migratietabel hebt geëxporteerd, is uw volgende stap het invoeren van de oude gegevens van de klant. Om uw taken te vereenvoudigen, kunt u de XML-manipulatiehulpprogramma's gebruiken die in Excel zijn ingebouwd. U kunt ook ingebouwde functies van Excel gebruiken om te helpen met het opmaken van gegevens en deze in de correcte cel te plaatsen.

Voor hulp met XML schakelt u het tabblad **Ontwikkelaar** van het Excel-lint in en kiest u de actie **Bron** om het XML-schema van uw migratietabel te zien zoals in het Excel wordt aangeduid.

De volgende procedure is gebaseerd op een Excel-werkblad dat u hebt gemaakt voor de migratie. Zie voor meer informatie Procedure: Migratietabellen exporteren.

> [!IMPORTANT]  
> Wijzig de kolommen in de Excel-werkbladen niet. Als ze worden verplaatst, gewijzigd of verwijderd, kan het werkblad niet worden geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Open in Excel het geëxporteerde gegevensbestand. Er is een werkblad met de naam van de tabel.
2. Hernoem Sheet1 om aan te geven dat het werkblad wordt gebruikt om de gegevens te transformeren. Kopieer de veldnamenrij zonder opmaak vanuit de geëxporteerde tabel naar het nieuwe werkblad.
3. Kopieer al uw klantgegevens op een derde werkblad. Hernoem het werkblad naar bijvoorbeeld Oude gegevens.
4. Maak een Excel-formule om gegevens in het transformatiewerkblad te koppelen met de velden in het geëxporteerde werkblad en de oude klantgegevens.
5. Nadat u alle gegevens hebt toegewezen, kopieert u het gegevensbereik naar het werkblad met de tabel.
6. Sla het bestand op en controleer of het bestandstype niet is gewijzigd.

U bent nu klaar om de gegevensmigratiebestanden met oude klantgegevens te importeren naar [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-import-customer-data"></a>Klantgegevens importeren
Nadat de klantgegevens zijn ingevoerd in de gegevensmigratiebestanden in Excel, importeert u de bestanden in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Open het venster **Pakketkaart voor configuratie**.
2. Selecteer de tabel waarvoor u waarden wilt importeren en kies op het sneltabblad **Tabellen** de actie **Vanuit Excel importeren**.
3. Zoek en open het gewenste bestand waaruit u gegevens wilt importeren naar [!INCLUDE[d365fin](includes/d365fin_md.md)].

Gegevens uit het bestand worden geïmporteerd in de configuratiepakkettabellen. U kunt het aantal records zien dat werd aangemaakt, in het veld **Aantal pakketrecords**. Bovendien ziet u het aantal migratiefouten.

## <a name="to-validate-customer-data"></a>Klantgegevens valideren
Klantgegevens moeten worden gevalideerd voordat u de records kunt toepassen op de [!INCLUDE[d365fin](includes/d365fin_md.md)]-database.  

> [!NOTE]  
>  In de meeste gevallen worden geen ongeldige gegevens in de database gemaakt. De toepassing kan echter soms worden geblokkeerd als een geïmporteerde migratietabel fouten bevat.  

1. Controleer in het venster **Migratieoverzicht** het veld **Aantal migratiefouten** om te zien of eventuele fouten tijdens het importeren zijn opgetreden.  
2. Als er fouten zijn, selecteert u de migratietabel en kiest u op het sneltabblad **Tabellen** de actie **Fouten**. Het selectievakje **Ongeldig** is ingeschakeld voor elke record die een fout bevat.  
3. Als u fouten wilt controleren, selecteert u een regel en kiest u **Fout weergeven**.  

    Het veld **Fouttekst** bevat de reden voor de fout. Het veld **Veldbijschrift** bevat het bijschrift van het veld dat de fout bevat.  
4.  Als u een fout wilt corrigeren of een andere update wilt aanbrengen, kiest u in het venster **Migratieoverzicht** de actie **Migratierecord** en corrigeert u vervolgens in het venster **Migratierecord** de record met de fout.  

Nadat u een correctie hebt aangebracht, wordt de record verwijderd uit de lijst met records in het venster **Migratiegegevensfouten**.  

U bent nu gereed om de gegevens van de klant toe te passen op de database.  

## <a name="to-apply-customer-data"></a>Klantgegevens toepassen
Als u alle geïmporteerde gegevensmigratierecords hebt die geldig zijn en geen fouten bevatten, kunt u de records toepassen op de [!INCLUDE[d365fin](includes/d365fin_md.md)]-database.  

1. Open het venster **Configuratiepakketten**.  
2. Selecteer de tabel voor het gegevensmigratiebestand dat u wilt toepassen, en kies de actie **Gegevens toepassen**.

U kunt het aantal databaserecords zien die werden aangemaakt in het veld **Aantal databaserecords**. U kunt controleren of de juiste gegevens zijn gemaakt door de koppeling te kiezen in het veld **Aantal databaserecords**.  

De bedrijfsdatabase van de klant is nu ingesteld en elementaire gegevens zijn geïmporteerd. De volgende stappen in het implementatieproces zijn gebruikers opleiden, processen definiëren, maken van aanvullende gegevens, aanpassen van lijsten, enzovoort.

## <a name="see-also"></a>Zie ook  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
