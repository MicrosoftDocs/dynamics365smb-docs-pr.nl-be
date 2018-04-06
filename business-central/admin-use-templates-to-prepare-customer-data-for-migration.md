---
title: Migratie van klantgegevens voorbereiden | Microsoft Docs
description: "Nadat u de instellingsgegevens hebt geïmporteerd en toegepast in de nieuwe database, kunt u beginnen met het migreren van de bestaande hoofdgegevens van de klant, zoals klantnummers en namen. Om ervoor te zorgen dat deze gegevens snel en nauwkeurig worden gemaakt in het nieuwe bedrijf kunt u het beste sjablonen gebruiken om de gegevens te structureren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3cfc53c1ea3c8d30f65b2d475a8dab052519e81e
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="prepare-to-migrate-customer-data"></a>Migratie van klantgegevens voorbereiden
Nadat u de instellingsgegevens hebt geïmporteerd en toegepast in de nieuwe database, kunt u beginnen met het migreren van de bestaande hoofdgegevens van de klant, zoals klantnummers en namen. Om ervoor te zorgen dat deze gegevens snel en nauwkeurig worden gemaakt in het nieuwe bedrijf kunt u het beste sjablonen gebruiken om de gegevens te structureren.  

Meestal maakt u gegevenssjablonen voor de volgende hoofdgegevens:  

-   **Contact**  
-   **Klant**  
-   **Artikel**  
-   **Leverancier**  

U kunt echter een sjabloonstructuur maken en toepassen op elke willekeurige tabel in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  U kunt ook gegevenssjablonen gebruiken voor dagelijkse bewerkingen om nieuwe records te maken die zijn gebaseerd op sjablonen. Deze gegevenssjablonen werken alleen voor de ondersteunde hoofdgegevenstabellen. Zie voor meer informatie bijvoorbeeld [Nieuwe artikelen registreren](inventory-how-register-new-items.md).  

Wanneer u klantgegevens, bijvoorbeeld voor artikelen, uit een bestand importeert, worden de verplichte veldgegevens die u hebt opgegeven verzameld uit de gekoppelde gegevenssjabloon. Wanneer u een nieuw artikel maakt, voert u alleen algemene informatie in zoals artikelnaam, -omschrijving en -prijs, en verzamelt u vervolgens de rest van de verplichte veldgegevens van een geselecteerde gegevenssjabloon.  

Wanneer u een nieuwe hoofdgegevensrecord maakt, zoals een klantenkaart, zijn sommige velden verplicht en moeten deze altijd worden ingevuld. U kunt de meeste verplichte velden, zoals boekingsgroepen en betalingsvoorwaarden, groeperen om het maken van hoofdgegevens eenvoudiger en stabieler te maken. Zo kunt u bijvoorbeeld verplichte velden voor tabel 18, **Klant**, groeperen als de typen **Binnenlands**, **Buitenlands** of **Exporteren**.

## <a name="to-select-a-data-template"></a>Een gegevenssjabloon selecteren
Wanneer u een bestaande gegevenssjabloon selecteert, moet u beoordelen of de sjablonen die u hebt gemaakt voor het nieuwe bedrijf volstaan. Controleer de opgegeven velden en waarden om te bepalen welke sjablonen geschikt zijn voor een nieuw bedrijf.  

> [!TIP]  
>  U kunt gegevenssjablonen ook gebruiken om snel nieuwe lijsten te maken. Gebruik deze om sneller en nauwkeuriger gegevens te maken. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiesjablonen** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer in het venster **Sjabloonoverzicht voor configuratie** een gegevenssjabloon in de lijst, en kies de actie **Bewerken**.  

Als de standaardsjablonen niet aan uw behoeften voldoen, kunt u nieuwe sjablonen maken of velden toevoegen aan een bestaande sjabloon. Als de standaardsjablonen voldoende zijn, kunt u deze gebruiken om records te maken op basis van hoofdgegevenssjablonen.

## <a name="to-create-a-data-template"></a>Een gegevenssjabloon maken
Als de standaardsjablonen niet aan de behoeften van uw nieuwe bedrijf voldoen, kunt u een nieuwe gegevenssjabloon maken. Als u er meer dan één maakt, is het misschien handiger om een naamgevingsconventie te hanteren voor het veld **Code**.

Elke sjabloon bestaat uit een kop en regels. Wanneer u een sjabloon maakt, kunt u opgeven welke velden altijd worden toegepast op gegevens van een bepaald type. Zo kunt u bijvoorbeeld verschillende klantsjablonen toepassen op verschillende soorten klanten. Wanneer u de klant maakt met behulp van een sjabloon kunt u de sjabloongegevens gebruiken om bepaalde velden vooraf in te vullen.

### <a name="to-create-a-data-template-header"></a>Een gegevenssjabloonkop maken
1. Open het venster **Sjabloonoverzicht voor configuratie**.
2. Kies de actie **Nieuw**.
3. Voer in het veld **Tabel-id** de tabel in waarop deze sjabloon van toepassing is. Het veld **Tabelnaam** wordt automatisch ingevuld als het veld **Tabel-id** is ingesteld.

### <a name="to-create-a-data-template-line"></a>Een gegevenssjabloonregel maken
1. Selecteer op de eerste regel het veld **Veldnaam**. Het venster **Veldoverzicht** bevat de lijst met velden in de tabel.
2. Selecteer een veld en kies de knop **OK**. Het veld **Veldbijschrift** is gevuld met de veldnaam.
3. Voer in het veld **Standaardwaarde** een geschikte waarde in. In sommige gevallen wilt u wellicht een waarde gebruiken die niet als waarde beschikbaar is in de database. In dat geval kunt u het selectievakje **Relatiecontrole overslaan** selecteren om gegevens zonder fout te kunnen toepassen.

    > [!TIP]  
    > Aangezien het veld **Standaardwaarde** niet de overeenkomstige [!INCLUDE[d365fin](includes/d365fin_md.md)]-veldopties hoeft op te zoeken, kopieert en plakt u de gewenste waarde van de gerelateerde pagina in de sjabloon.

    > Selecteer het selectievakje **Verplicht**. Het selectievakje dient uitsluitend ter informatie. Het geeft aan dat informatie moet worden ingevoerd in het veld door de gebruiker, maar dat er geen bedrijfslogica wordt afgedwongen. U kunt bijvoorbeeld geen factuur maken en geen order boeken als er geen boekingsgroepen zijn ingesteld. Aangezien boekingsgroepen zijn vereist kunt u het selectievakje **Verplicht** gebruiken voor die velden.

3. Geef in het veld **Referentie** indien nodig gegevens over het veld op.
4. Kies de knop **Ok**.

## <a name="to-export-to-a-template-in-excel"></a>Exporteren naar een sjabloon in Excel
U kunt snel een Excel-werkmap maken als sjabloon die is gebaseerd op de structuur van een bestaande databasetabel. U kunt vervolgens de sjabloon gebruiken om klantgegevens te verzamelen in een consistente indeling die u later kunt importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.
2. Voeg een tabel toe aan de lijst of selecteer een bestaande tabel. Zie voor meer informatie [De bedrijfsconfiguratie beheren in een werkblad](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Definieer de velden uit de tabel die u wilt opnemen in de sjabloon.
4. Kies de actie **Exporteren naar sjabloon**.
5. Geef het Excel-bestand een naam en sla het op. De Excel-werkmap wordt automatisch geopend.

U kunt nu klantgegevens invoeren in het Excel-werkblad. Als u meerdere tabellen hebt geëxporteerd, wordt elke tabel op een afzonderlijk werkblad weergegeven. Sla de werkmap op voordat u verdergaat met de volgende procedure.

> [!NOTE]  
> De volgende fout kan optreden als een Engelstalige versie van Excel wordt uitgevoerd terwijl u uw landinstellingen hebt geconfigureerd voor een niet-Engelse taal: "Oude bestandsindeling of ongeldige typebibliotheek". U kunt deze fout verhelpen door ervoor te zorgen dat het taalpakket voor de niet-Engelse taal is geïnstalleerd.

## <a name="to-import-from-a-template-in-excel"></a>Importeren vanuit een sjabloon in Excel
1. Kies in het venster **Werkblad voor configuratie** de actie **Importeren vanuit sjabloon**.
3. Navigeer naar het sjabloonwerkblad dat u hebt gemaakt, en kies vervolgens de actie **Openen**.
4. Als u de verzamelde klantgegevens wilt toevoegen aan de database, kiest u de actie **Gegevens toepassen**.

Wanneer u gegevens uit een sjabloon in Excel toepast op een tabel waaraan eveneens een configuratiesjabloon is gekoppeld in het configuratiepakket, worden de standaardveldwaarden van de configuratiesjabloon eveneens toegepast.

Een record waarvan de gegevens op deze manier worden toegepast is voltooid, omdat deze bestaat uit gegevens die zijn ingevoerd door een gebruiker in Excel, plus de standaardwaarden die zijn opgegeven door de configuratiesjabloon.

## <a name="to-create-a-record-from-a-configuration-template"></a>Een record maken vanuit een configuratiesjabloon
U kunt de structuur van de gegevens in de gegevenssjablonen gebruiken om uw informatie een voor een te converteren naar records in de database. Hiervoor gebruikt u de functie **Instance maken**. Dit is een miniatuurversie van de gegevensmigratie en kan nuttig zijn voor het maken van prototypen of het behandelen van kleinere taken voor het maken van gegevens.  

De volgende stappen illustreren hoe u een artikelkaart maakt van een artikelgegevenssjabloon. U kunt met dezelfde procedure een record maken van elke gegevenssjabloon.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiesjablonen** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de **artikel**sjabloon en kies vervolgens de actie **Bewerken**. Zie voor meer informatie het gedeelte "Een gegevenssjabloon maken".
3. Kies de actie **Instantie maken**. Er wordt een artikelkaart gemaakt.  
4. Kies de knop **OK**.  
5. Als u de nieuwe artikelkaart wilt controleren, kiest u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Artikelen** in en klikt u vervolgens op de gerelateerde koppeling.  
6. Open de nieuwe artikelkaart.  
7. Vouw verschillende sneltabbladen uit en controleer of de gegevens erop kloppen.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Een configuratiesjabloon gebruiken voor een record
U kunt een gegevenssjabloon toepassen op elke record in [!INCLUDE[d365fin](includes/d365fin_md.md)] en deze techniek gebruiken om een record te wijzigen. Echter wanneer u dit doet, overschrijft u bestaande waarden in de record met die van de sjabloon. Wees dus voorzichtig wanneer u een sjabloon op bestaande records toepast.

> [!WARNING]  
>  De functie **Sjabloon toepassen** overschrijft bestaande gegevens in een record. Als deze functie wordt gebruikt in de migratie van de hoofdgegevens, worden de geïmporteerde gegevens overschreven wanneer u records maakt.

De volgende procedure is gebaseerd op een nieuwe klantenkaart.  

1. Maak een klant. Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).
2. Kies in het venster **Klantenkaart** de actie **Sjabloon toepassen**.  
3. Selecteer in het venster **Klantensjablonen** een van de sjablonen en kies de knop **OK**.  

De standaardwaarden van de gekozen klantensjabloon worden ingevoegd in de klantenkaart.

## <a name="see-also"></a>Zie ook  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)

