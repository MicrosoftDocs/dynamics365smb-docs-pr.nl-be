---
title: Weergeven en bewerken in Excel vanuit Business Central | Microsoft Docs
description: Leer hoe u de pagina's in Microsoft Excel opent vanuit Business Central voor betere gegevensanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: b25413c8f0479aaccfc67ae96f2870690f993dfa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927284"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Weergeven en bewerken in Excel vanuit Business Central

Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de records weergeven met Microsoft Excel. U hebt hiervoor twee opties. U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren. Dit zijn de verschillen tussen de twee methoden:  

## <a name="open-in-excel"></a>Openen in Excel

- Met deze actie houdt Excel rekening met alle filters op de pagina waarmee de weergegeven records worden beperkt. Dit betekent dat de Excel-werkmap dezelfde rijen en kolommen bevat die worden weergegeven op de pagina in [!INCLUDE[prodshort](includes/prodshort.md)].

- U kunt wijzigingen in de records aanbrengen in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prodshort](includes/prodshort.md)]. U kunt de wijzigingen alleen opslaan in het Excel-bestand op uw computer.

- Deze actie werkt zowel onder Windows als MacOS.

> [!NOTE]
> Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Openen in Excel** standaard beschikbaar. Als u echter [!INCLUDE[prodshort](includes/prodshort.md)] on-premises instelt om gegevens in Excel te bewerken, wordt de actie **Openen in Excel** vervangen door de actie **Bewerken in Excel** .

## <a name="edit-in-excel"></a>Bewerken in Excel

- Met deze actie houdt Excel rekening met de meeste filters op de pagina waarmee de weergegeven records worden beperkt. Dit betekent dat de Excel-werkmap nagenoeg dezelfde records en kolommen bevat.

- Het voordeel van de actie **Bewerken in Excel** is dat u er wijzigingen in records in Excel mee kunt aanbrengen en de wijzigingen weer naar [!INCLUDE[prodshort](includes/prodshort.md)] kunt publiceren.

- Dit werkt alleen onder Windows, niet onder MacOS.

- U kunt het bedrijf waarmee u werkt wijzigen. Selecteer hiervoor het pictogram **Opties** ![Opties voor Excel-invoegtoepassingen](media/cogwheel.png "Opties van Excel-invoegtoepassing") in het Excel-invoegtoepassingsvenster en selecteer vervolgens het bedrijf in het veld **Bedrijf** .  

    > [!IMPORTANT]
    > Zorg er bij het veranderen van bedrijf voor dat het veld **Omgeving** niet leeg is. Als dat zo is, stel het dan in op een van de beschikbare opties; anders werkt de invoegtoepassing niet correct.  

Als u wijzigingen aanbrengt in de invoegtoepassing, moet u deze opnieuw laden om de verbinding bij te werken. Gebruik om opnieuw te laden het menu ![menu van Excel-invoegtoepassing](media/excel-addin-menu.png "Menu van Excel-invoegtoepassing") in de rechterbovenhoek van de invoegtoepassing.

> [!NOTE]
> Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw systeembeheerder is geconfigureerd, en alleen beschikbaar voor de webclient. Voor systeembeheerders: Zie [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) voor meer informatie over de installatie van de Excel-invoegtoepassing.

### <a name="see-the-differences-between-the-options"></a>Zie de verschillen tussen de opties
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Werken met Business Central](ui-work-product.md)  
[Verbeteringen aan Excel-integratie in releasewave 2 van 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
