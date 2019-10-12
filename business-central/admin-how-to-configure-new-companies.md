---
title: Nieuwe bedrijven configureren | Microsoft Docs
description: U kunt een nieuw bedrijf dat u hebt gemaakt configureren en aanpassen. U kunt uw implementatie verder afstellen door de configuratie te voltooien in drie fasen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b3169663fd764bf4f7c9c6dc8895b152fdca19bd
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304576"
---
# <a name="configure-new-companies"></a>Nieuwe bedrijven configureren
Als u een nieuw bedrijf in uw oplossingimplementatie wilt configureren, volgt u doorgaans drie fasen. In de eerste fase importeert u het configuratiepakket. Dit is een .rapidstart-bestand met de configuratie-informatie. In de tweede fase wijzigt u de configuratiegegevens en past u deze vervolgens toe op uw nieuwe bedrijf. In de laatste fase controleert en corrigeert u fouten.  

Bij de volgende procedures wordt ervan uitgegaan dat u een configuratiepakket hebt gemaakt en opgeslagen. Zie [Een configuratiepakket voorbereiden](admin-how-to-prepare-a-configuration-package.md) voor meer informatie.  

In de volgende procedure wordt ervan uitgegaan dat u uw nieuwe bedrijf hebt geïnitialiseerd en geopend, en dat u zich in het rolcentrum RapidStart Services-implementatie bevindt.

## <a name="to-import-a-configuration-package"></a>Een configuratiepakket importeren  
1. Open het nieuwe bedrijf in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-database.  
2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiepakketten** in en selecteer vervolgens de gerelateerde koppeling.  
3. Kies de actie **Pakket importeren**.  
4. Navigeer naar de locatie waar u het .rapidstart-configuratiepakketbestand hebt opgeslagen, en kies vervolgens de knop **Openen**.  
5. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsgegevens** in en kies vervolgens de gerelateerde koppeling. Voer informatie over het bedrijf in op de bedrijfsgegevenskaart. Neem informatie op, zoals bankgegevens. U kunt ook een logo voor het bedrijf opgeven.  

Alle tabellen die u hebt aangewezen voor opname in het nieuwe bedrijf worden geïmporteerd. Op dit punt kunt u de gegevens van het pakket toepassen op de database of de tabelgegevens aanpassen en wijzigen om te voldoen aan de specificaties van de klant.  

## <a name="to-apply-package-data"></a>Pakketgegevens toepassen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en selecteer vervolgens de gerelateerde koppeling.  
2. Selecteer de tabel waarvoor u gegevens wilt wijzigen en kies vervolgens de actie **Gegevens toepassen**. Kies de knop **Ja** om de toepassing te bevestigen.
3. Ga terug naar de pagina **Configuratiewerkblad** om te bevestigen dat de gegevens zich nu in de database bevinden en dat de toepassing is geslaagd, en kies de actie **Databasegegevens**.  

> [!NOTE]  
>  Nadat u gegevens hebt toegepast, kunt u deze alleen bekijken in de database. Zij bevinden zich niet langer in het pakket.  

## <a name="to-modify-and-apply-package-data"></a>Pakketgegevens wijzigen en toepassen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en selecteer vervolgens de gerelateerde koppeling.  
2. Selecteer de tabel waarvoor u gegevens wilt wijzigen en kies vervolgens de actie **Pakketgegevens**.  
3. Breng uw wijzigingen aan op de pagina **Pakketrecords voor configuratie**. Zo kunt u bijvoorbeeld opties verwijderen die niet van toepassing zijn.  
4. Kies de actie **Gegevens toepassen** en kies vervolgens de knop **OK**.  
5. Ga terug naar de pagina **Configuratiewerkblad** om te bevestigen dat de gegevens zich nu in de database bevinden en dat de toepassing is geslaagd, en kies de actie **Databasegegevens**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Een configuratiefout zoeken en identificeren  
Er zijn bepaalde typen fouten die kunnen optreden wanneer u gegevens toepast op een database. De meest voorkomende fout is dat vereiste tabellen niet zijn opgenomen. U corrigeert dergelijke fouten in het configuratiewerkblad.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiepakketten** in en selecteer vervolgens de gerelateerde koppeling.  
2. Selecteer het pakket dat u wilt controleren en kies vervolgens de actie **Bewerken**.  

    Een tabel met fouten wordt gemarkeerd weergegeven. Het aantal pakketfouten wordt weergegeven in het veld **Aantal pakketfouten**.  

3. Kies het veld **Aantal pakketfouten** om de pagina **Pakketrecords voor configuratie** te openen, met de lijst met records met fouten.  

### <a name="to-fix-an-error"></a>Een fout corrigeren  
1. Open het bedrijf dat is gebaseerd op uw configuratiepakket.  
2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiewerkblad** in en selecteer vervolgens de gerelateerde koppeling.  
3. Corrigeer fouten, zoals ontbrekende gerelateerde tabellen, in het werkblad.  
4. Voeg de tabellen toe aan het bestaande configuratiepakket of maak een nieuw pakket dat alleen de nieuwe tabellen bevat. Zie [Een configuratiepakket voorbereiden](admin-how-to-prepare-a-configuration-package.md) voor meer informatie.  
5. Open het nieuwe bedrijf waarvoor u de configuratie implementeert.  
6. Importeer het configuratiepakket.  

    > [!NOTE]  
    >  Als u hetzelfde pakket opnieuw importeert, kunt u eventuele gegevenswijzigingen overschrijven die u al hebt aangebracht. Om die reden wilt u wellicht nieuwe tabellen toevoegen aan een nieuw pakket en in plaats daarvan dit importeren.  

7. Pas de gegevens op de database toe, zoals beschreven in [Pakketgegevens wijzigen en toepassen](admin-how-to-configure-new-companies.md#to-modify-and-apply-package-data).

## <a name="see-also"></a>Zie ook  
[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
