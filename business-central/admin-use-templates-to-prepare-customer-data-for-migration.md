---
title: Migratie van klantgegevens met sjablonen voorbereiden
description: Leer hoe u configuratiesjablonen gebruikt om bestaande klantgegevens te structureren voordat u de hoofdgegevens migreert naar het nieuwe bedrijf in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 9dd985237f0e214c404d7f254c023b67af660e48
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443166"
---
# <a name="prepare-to-migrate-customer-data-with-templates"></a>Migratie van klantgegevens met sjablonen voorbereiden

Nadat u de instellingsgegevens hebt geïmporteerd en toegepast in de nieuwe database, kunt u beginnen met het migreren van de bestaande hoofdgegevens van de klant, zoals klantnummers en namen. Om ervoor te zorgen dat deze gegevens snel en nauwkeurig worden gemaakt in het nieuwe bedrijf kunt u het beste sjablonen gebruiken om de gegevens te structureren.  

Meestal maakt u gegevenssjablonen voor de volgende hoofdgegevens:  

- **Contact**  
- **Klant**  
- **Artikel**  
- **Leverancier**  

U kunt echter een sjabloonstructuur maken en toepassen op elke willekeurige tabel in [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!TIP]  
> U kunt ook gegevenssjablonen gebruiken voor dagelijkse bewerkingen om nieuwe records te maken die zijn gebaseerd op sjablonen. Deze gegevenssjablonen werken alleen voor de ondersteunde hoofdgegevenstabellen. Zie voor meer informatie bijvoorbeeld [Nieuwe artikelen registreren](inventory-how-register-new-items.md).  

Wanneer u klantgegevens, bijvoorbeeld voor artikelen, uit een bestand importeert, worden de verplichte veldgegevens die u hebt opgegeven verzameld uit de gekoppelde gegevenssjabloon. Wanneer u een nieuw artikel maakt, voert u alleen algemene informatie in zoals artikelnaam, -omschrijving en -prijs, en verzamelt u vervolgens de rest van de verplichte veldgegevens van een geselecteerde gegevenssjabloon.

Wanneer u een nieuwe hoofdgegevensrecord maakt, zoals een klantenkaart, zijn sommige velden verplicht en moeten deze altijd worden ingevuld. U kunt de meeste verplichte velden, zoals boekingsgroepen en betalingsvoorwaarden, groeperen om het maken van hoofdgegevens eenvoudiger en stabieler te maken. Zo kunt u bijvoorbeeld verplichte velden voor tabel 18, **Klant**, groeperen als de typen **Binnenlands**, **Buitenlands** of **Exporteren**.

> [!NOTE]
> Velden van het type Blob kunnen niet worden geëxporteerd/geïmporteerd met Excel.

## <a name="to-select-a-data-template"></a>Een gegevenssjabloon selecteren

Wanneer u een bestaande gegevenssjabloon selecteert, moet u beoordelen of de sjablonen die u hebt gemaakt voor het nieuwe bedrijf volstaan. Controleer de opgegeven velden en waarden om te bepalen welke sjablonen geschikt zijn voor een nieuw bedrijf.  

> [!TIP]  
> U kunt gegevenssjablonen ook gebruiken om snel nieuwe lijsten te maken. Gebruik deze om sneller en nauwkeuriger gegevens te maken. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Configuratiesjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Configuratiesjablonen** een gegevenssjabloon in de lijst, en kies de actie **Bewerken**.  

Als de standaardsjablonen niet aan uw behoeften voldoen, kunt u nieuwe sjablonen maken of velden toevoegen aan een bestaande sjabloon. Als de standaardsjablonen voldoende zijn, kunt u deze gebruiken om records te maken op basis van hoofdgegevenssjablonen.

## <a name="to-create-a-new-data-template"></a>Een nieuwe gegevenssjabloon maken

Als de standaardsjablonen niet aan de behoeften van uw nieuwe bedrijf voldoen, kunt u een nieuwe gegevenssjabloon maken.  

> [!TIP]
> Als u er meer dan één maakt, is het misschien handiger om een naamgevingsconventie te hanteren voor het veld **Code**.

Elke sjabloon bestaat uit een koptekst en een regel voor elk veld dat in de sjabloon moet worden opgenomen. Wanneer u een sjabloon maakt, kunt u opgeven welke velden altijd worden toegepast op gegevens van een bepaald type. Zo kunt u bijvoorbeeld verschillende klantsjablonen toepassen op verschillende soorten klanten. Wanneer u de klant maakt met behulp van een sjabloon kunt u de sjabloongegevens gebruiken om bepaalde velden vooraf in te vullen.

### <a name="to-copy-an-existing-data-template"></a>Een bestaande gegevenssjabloon kopiëren.

U kunt snel een nieuwe gegevenssjabloon maken door informatie te kopiëren uit een bestaande gegevenssjabloon, die u vervolgens bewerkt.

1. Open de pagina **Configuratiesjablonen**.
2. Kies de actie **Nieuw**.
3. Vul het veld **Code** in.
4. Kies de actie **Configuratiesjabloon kopiëren**.
5. Selecteer op de pagina **Configuratiesjablonen** een bestaande sjabloon om te kopiëren en kies vervolgens de knop **OK**.

De tabel-id, tabelnaam en regels van de bestaande gegevenssjabloon worden ingevoegd in de nieuwe sjabloon.

### <a name="to-create-a-data-template-header-manually"></a>Handmatig een gegevenssjabloonkop maken

1. Open de pagina **Configuratiesjablonen**.
2. Kies de actie **Nieuw**.
3. Vul het veld **Code** in.
4. Voer in het veld **Tabel-id** de tabel in waarop deze sjabloon van toepassing is. Het veld **Tabelnaam** wordt automatisch ingevuld als het veld **Tabel-id** is ingesteld.

### <a name="to-create-a-data-template-line-manually"></a>Handmatig een gegevenssjabloonregel maken

1. Selecteer op de eerste regel het veld **Veldnaam**. De pagina **Veldoverzicht** bevat de lijst met velden in de tabel.
2. Selecteer een veld en kies de knop **OK**. Het veld **Veldbijschrift** is gevuld met de veldnaam.
3. Voer in het veld **Standaardwaarde** een geschikte waarde in. In sommige gevallen wilt u wellicht een waarde gebruiken die niet als waarde beschikbaar is in de database. In dat geval kunt u het selectievakje **Relatiecontrole overslaan** selecteren om gegevens zonder fout te kunnen toepassen.

    > [!TIP]  
    > Aangezien het veld **Standaardwaarde** niet de overeenkomstige [!INCLUDE[prod_short](includes/prod_short.md)]-veldopties hoeft op te zoeken, kopieert en plakt u de gewenste waarde van de gerelateerde pagina in de sjabloon.

4. Selecteer het selectievakje **Verplicht** als gebruikers het veld moeten invullen.

    > [!NOTE]
    > Het selectievakje dient uitsluitend ter informatie. Er wordt geen bedrijfslogica afgedwongen. Gebruikers kunnen bijvoorbeeld geen factuur boeken als geen boekingsgroepen zijn ingesteld. U kunt het selectievakje **Verplicht** voor die velden selecteren om de gebruiker ze te laten invullen en zo later een boekingsfout te voorkomen.
5. Geef in het veld **Referentie** indien nodig gegevens over het veld op.
6. Kies de knop **Ok**.

## <a name="to-export-to-a-template-in-excel"></a>Exporteren naar een sjabloon in Excel

U kunt snel een Excel-werkmap maken als sjabloon die is gebaseerd op de structuur van een bestaande databasetabel. U kunt vervolgens de sjabloon gebruiken om klantgegevens te verzamelen in een consistente indeling die u later kunt importeren in [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.
2. Voeg een tabel toe aan de lijst of selecteer een bestaande tabel. Zie voor meer informatie [De bedrijfsconfiguratie beheren in een werkblad](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Kies de actie **Geeft velden weer** om de velden uit de tabel te definiëren die u in de sjabloon wilt opnemen.
4. Kies de actie **Exporteren naar sjabloon**.
5. Geef het Excel-bestand een naam en sla het op. De Excel-werkmap wordt automatisch geopend.

U kunt nu klantgegevens invoeren in het Excel-werkblad. Als u meerdere tabellen hebt geëxporteerd, wordt elke tabel op een afzonderlijk werkblad weergegeven. Sla de werkmap op voordat u verdergaat met de volgende procedure.

> [!NOTE]  
> De volgende fout kan optreden als een Engelstalige versie van Excel wordt uitgevoerd terwijl u uw landinstellingen hebt geconfigureerd voor een niet-Engelse taal: "Oude bestandsindeling of ongeldige typebibliotheek". U kunt deze fout verhelpen door ervoor te zorgen dat het taalpakket voor de niet-Engelse taal is geïnstalleerd.

## <a name="to-import-from-a-template-in-excel"></a>Importeren vanuit een sjabloon in Excel

1. Kies op de pagina **Configuratiewerkblad** de actie **Importeren vanuit sjabloon**.
2. Navigeer naar het sjabloonwerkblad dat u hebt gemaakt, en kies vervolgens de actie **Openen**.
3. Als u de verzamelde klantgegevens wilt toevoegen aan de database, kiest u de actie **Gegevens toepassen**.

Wanneer u gegevens uit een sjabloon in Excel toepast op een tabel waaraan eveneens een configuratiesjabloon is gekoppeld in het configuratiepakket, worden de standaardveldwaarden van de configuratiesjabloon eveneens toegepast.

Een record waarvan de gegevens op deze manier worden toegepast is voltooid, omdat deze bestaat uit gegevens die zijn ingevoerd door een gebruiker in Excel, plus de standaardwaarden die zijn opgegeven door de configuratiesjabloon.

> [!NOTE]
> Als de gegevens in de tabellen in het configuratiepakket datums bevatten, bijvoorbeeld boekingsdatums in facturen, worden de datums in aanmerking genomen in de tijdzone die is gespecificeerd in [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="to-create-a-record-from-a-configuration-template"></a>Een record maken vanuit een configuratiesjabloon

U kunt de structuur van de gegevens in de gegevenssjablonen gebruiken om uw informatie een voor een te converteren naar records in de database. Hiervoor gebruikt u de functie **Instance maken**. Dit is een miniatuurversie van de gegevensmigratie en kan nuttig zijn voor het maken van prototypen of het behandelen van kleinere taken voor het maken van gegevens.  

De volgende stappen illustreren hoe u een artikelkaart maakt van een artikelgegevenssjabloon. U kunt met dezelfde procedure een record maken van elke gegevenssjabloon.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiesjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de **artikel** sjabloon en kies vervolgens de actie **Bewerken**. Zie voor meer informatie [Een gegevenssjabloon maken](admin-use-templates-to-prepare-customer-data-for-migration.md#to-create-a-new-data-template).
3. Kies de actie **Instantie maken**. Er wordt een artikelkaart gemaakt.  
4. Kies de knop **OK**.  
5. Om de nieuwe artikelkaart te bekijken kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
6. Open de nieuwe artikelkaart.  
7. Vouw verschillende sneltabbladen uit en controleer of de gegevens erop kloppen.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Een configuratiesjabloon gebruiken voor een record

U kunt een gegevenssjabloon toepassen op elke record in [!INCLUDE[prod_short](includes/prod_short.md)] en deze techniek gebruiken om een record te wijzigen. Echter wanneer u dit doet, overschrijft u bestaande waarden in de record met die van de sjabloon. Wees dus voorzichtig wanneer u een sjabloon op bestaande records toepast.

> [!WARNING]  
> De functie **Sjabloon toepassen** overschrijft bestaande gegevens in een record. Als deze functie wordt gebruikt in de migratie van de hoofdgegevens, worden de geïmporteerde gegevens overschreven wanneer u records maakt.

De volgende procedure is gebaseerd op een nieuwe klantenkaart.  

1. Maak een klant. Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).
2. Kies op de pagina **Klantenkaart** de actie **Sjabloon toepassen**.  
3. Selecteer op de pagina **Klantensjablonen** een van de sjablonen en kies vervolgens de knop **OK**.  

De standaardwaarden van de gekozen klantensjabloon worden ingevoegd in de klantenkaart.

## <a name="see-also"></a>Zie ook

[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]