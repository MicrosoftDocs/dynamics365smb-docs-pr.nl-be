---
title: Een nieuw bedrijf maken | Microsoft Docs
description: Gebruik RapidStart Services-tabellen en -pagina's om een nieuw bedrijf te maken waarvoor u een klantimplementatie wilt uitvoeren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: bb2e3e8d431160c94f7944fe8986ea9cc115ffe7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439647"
---
# <a name="create-a-new-company"></a>Een nieuw bedrijf maken
Als u RapidStart Services voor [!INCLUDE[prod_short](includes/prod_short.md)] wilt gebruiken, maakt u eerst een nieuw bedrijf waarvoor u een klantimplementatie wilt uitvoeren. Bij het maken van een nieuw bedrijf worden de standaard [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen en pagina's gemaakt, maar deze zijn leeg.

Bovendien kunt u specifieke instellingsgegevens op uw bedrijf toepassen nadat u het hebt geïnitialiseerd. Deze gegevens worden in een configuratiepakket (een .rapidstart-bestand) verstrekt welke de inhoud in een gecomprimeerde indeling levert.  

Voorbeeldconfiguratiepakketten, inclusief land-/regiospecifieke bestanden, zijn opgenomen bij het demonstratiebedrijf CRONUS. Gebruik de volgende procedures om het voorbeeldconfiguratiepakket met een nieuw bedrijf te gebruiken.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Het voorbeeldconfiguratiepakket BASICCONFIG gebruiken  
1. Open het bedrijf CRONUS International Ltd. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
3. Kies het pakket BASICCONFIG in de lijst en kies vervolgens de actie **Pakket exporteren**.  

Gebruik de onderstaande procedure om een nieuw bedrijf aan te maken en gebruik het pakket BASICCONFIG als deel van het proces.  

## <a name="to-create-a-new-company"></a>Een nieuw bedrijf maken  
1. Maak een nieuw bedrijf. Zie [Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md) voor meer informatie.
2. Vanuit het rolcentrum RapidStart Services-implementatie kunt u het configuratiepakket nu importeren dat u vanuit het bedrijf CRONUS International Ltd. hebt geëxporteerd.

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