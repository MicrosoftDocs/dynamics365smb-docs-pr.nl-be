---
title: Een nieuw bedrijf maken | Microsoft Docs
description: Om RapidStart Services te kunnen gebruiken worden tabellen en pagina's gemaakt, maar ze bevatten geen gegevens.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 49b2bb9a59c5bcd5d414b129acffaedfa0d0eaa1
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="create-a-new-company"></a>Een nieuw bedrijf maken
Als u RapidStart Services wilt gebruiken voor [!INCLUDE[d365fin](includes/d365fin_md.md)], maakt u eerst een nieuw bedrijf waarvoor u een klantimplementatie wilt uitvoeren. Bij het maken van een nieuw bedrijf worden de standaard [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen en pagina's gemaakt, maar deze zijn leeg.

Bovendien kunt u specifieke instellingsgegevens op uw bedrijf toepassen nadat u het hebt geïnitialiseerd. Deze gegevens worden in een configuratiepakket (een .rapidstart-bestand) verstrekt welke de inhoud in een gecomprimeerde indeling levert.  

Voorbeeldconfiguratiepakketten, inclusief land-/regiospecifieke bestanden, zijn opgenomen bij het demonstratiebedrijf CRONUS. Gebruik de volgende procedures om het voorbeeldconfiguratiepakket met een nieuw bedrijf te gebruiken.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Het voorbeeldconfiguratiepakket BASICCONFIG gebruiken  
1. Open het bedrijf CRONUS International Ltd. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).
2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
3. Kies het pakket BASICCONFIG in de lijst en kies vervolgens de actie **Pakket exporteren**.  

Gebruik de onderstaande procedure om een nieuw bedrijf aan te maken en gebruik het pakket BASICCONFIG als deel van het proces.  

## <a name="to-create-a-new-company"></a>Een nieuw bedrijf maken  
1. Maak een nieuw bedrijf. Zie [Nieuwe bedrijven maken in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md) voor meer informatie.
2. Vanuit het rolcentrum RapidStart Services-implementatie kunt u het configuratiepakket nu importeren dat u vanuit het bedrijf CRONUS International Ltd. hebt geëxporteerd.

Nadat u een nieuw bedrijf maakt, worden sommige tabellen automatisch ingevuld, zelfs als er geen bedrijfssjabloon is toegepast. U kunt bijvoorbeeld de standaardcodes bekijken voor het boeken en voor batchtransacties op de pagina **Broncode**. Als u een lokale versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] hebt, moet u deze tabel bekijken en rekening houden met de lokale taal.

## <a name="about-data-tables"></a>Gegevenstabellen
[!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevenstabellen worden geleverd in twee basistypen: Hoofd en Instellingen. Wanneer u een bedrijfsconfiguratie opzet, kunt u deze typen gebruiken om een gerichte configuratiestrategie te hanteren.  

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

Behalve instellingsgegevenstabellen bevat [!INCLUDE[d365fin](includes/d365fin_md.md)] ook instellingstabellen waarin kerngegevens over het bedrijf en de bedrijfsprocessen worden opgegeven. In de volgende tabel wordt een aantal ervan weergegeven.  

|Tabelnr.|Tabelnaam|  
|-------------------|--------------------|  
|3|Betalingsvoorwaarden|  
|4|Valuta|  
|6|Klantenprijsgroepen|  
|5700|SKU|

  

## <a name="see-also"></a>Zie ook  
[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)

