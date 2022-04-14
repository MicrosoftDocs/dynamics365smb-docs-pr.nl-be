---
title: Een nieuw bedrijf maken met configuratiepakketten
description: Gebruik RapidStart Services-tabellen en -pagina's om een nieuw bedrijf te maken waarvoor u een klantimplementatie wilt uitvoeren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 2d75c136fdd0dcf2891468d722008ab0bf183cbb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512424"
---
# <a name="create-a-new-company-based-on-configuration-packages"></a>Een nieuw bedrijf maken op basis van configuratiepakketten

Als u RapidStart Services voor [!INCLUDE[prod_short](includes/prod_short.md)] wilt gebruiken, maakt u eerst een nieuw bedrijf waarvoor u een klantimplementatie wilt uitvoeren. Bij het maken van een nieuw bedrijf worden de standaard [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen en pagina's gemaakt, maar deze zijn leeg.

Bovendien kunt u specifieke instellingsgegevens op uw bedrijf toepassen nadat u het hebt geïnitialiseerd. Deze gegevens worden in een configuratiepakket (een .rapidstart-bestand) verstrekt welke de inhoud in een gecomprimeerde indeling levert.  

Voorbeeldconfiguratiepakketten, inclusief land-/regiospecifieke bestanden, zijn opgenomen bij het demonstratiebedrijf CRONUS. Gebruik de volgende procedures om het voorbeeldconfiguratiepakket met een nieuw bedrijf te gebruiken.  

## <a name="to-use-the-sample-configuration-packages"></a>De voorbeeldconfiguratiepakketten gebruiken

1. Open het demonstratiebedrijf CRONUS. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).  
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
3. Kies het relevante pakket in de lijst en kies vervolgens de actie **Pakket exporteren**.  

Gebruik de onderstaande procedure om een nieuw bedrijf te maken en gebruik het configuratiepakket als deel van het proces.  

## <a name="to-create-a-new-company"></a>Een nieuw bedrijf maken

1. Maak een nieuw bedrijf. Zie [Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md) voor meer informatie.
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
3. Kies de optie **Pakket importeren** en geef vervolgens het bestand .rapidstart op dat u wilt importeren.  

Nadat u een nieuw bedrijf maakt, worden sommige tabellen automatisch ingevuld, zelfs als er geen bedrijfssjabloon is toegepast. U kunt bijvoorbeeld de standaardcodes bekijken voor het boeken en voor batchtransacties op de pagina **Broncode**. Als u een lokale versie van [!INCLUDE[prod_short](includes/prod_short.md)] hebt, moet u deze tabel bekijken en rekening houden met de lokale taal.

## <a name="about-data-tables"></a>Gegevenstabellen

[!INCLUDE[prod_short](includes/prod_short.md)]-gegevenstabellen worden geleverd in twee basistypen: Hoofd en Instellingen. Wanneer u een bedrijfsconfiguratie opzet, kunt u deze typen gebruiken om een gerichte configuratiestrategie te hanteren.  

### <a name="master-data-tables"></a>Hoofdgegevenstabellen

In de volgende tabel worden enkele voorbeelden van de hoofdgegevenstabellen weergegeven. Wanneer u een nieuw bedrijf initialiseert, zijn deze tabellen leeg.  

|Tabelnr.|Tabelnaam|  
|-------------------|--------------------|  
|15|Grootboekrekening|  
|18|Klant|  
|23|Leverancier|  
|27|Artikel|  
|5050|Contactpersoon|  

### <a name="setup-data-tables"></a>Instellingsgegevenstabellen

De volgende tabel bevat enkele van de instellingsgegevenstabellen, waarin u instelinformatie vastlegt in de configuratievragenlijst. Deze tabellen bevatten basislijngegevens wanneer het bedrijf wordt gemaakt.  

|Tabelnr.|Tabelnaam|  
|-------------------|--------------------|  
|98|Grootboekinstellingen|  
|311|Verkoopinstellingen|  
|312|Inkoopinstellingen|  
|313|Voorraadinstelling|  

Behalve instellingsgegevenstabellen bevat [!INCLUDE[prod_short](includes/prod_short.md)] ook instellingstabellen waarin kerngegevens over het bedrijf en de bedrijfsprocessen worden opgegeven. In de volgende tabel wordt een aantal ervan weergegeven.  

|Tabelnr.|Tabelnaam|  
|-------------------|--------------------|  
|3|Betalingsvoorwaarden|  
|4|Valuta|  
|6|Klantenprijsgroepen|  
|5700|SKU|

## <a name="see-also"></a>Zie ook

[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]