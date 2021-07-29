---
title: Weergeven en bewerken in Excel vanuit Business Central
description: Leer hoe u de pagina's in Microsoft Excel opent vanuit Business Central voor betere gegevensanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443494"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Weergeven en bewerken in Excel vanuit Business Central

Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de records weergeven met Microsoft Excel. Afhankelijk van de pagina hebt u twee opties voor weergave in Excel. U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren. In dit artikel worden de verschillen tussen de twee acties uitgelegd.

## <a name="open-in-excel"></a>Openen in Excel

Met de actie **Openen in Excel** kunt u wijzigingen aanbrengen in de records in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt de wijzigingen alleen opslaan in het Excel-bestand op uw computer.

- Met deze actie houdt Excel rekening met alle filters op de pagina waarmee de weergegeven records worden beperkt. De Excel-werkmap zal dezelfde rijen en kolommen bevatten die worden weergegeven op de pagina in [!INCLUDE[prod_short](includes/prod_short.md)].

- Deze actie werkt zowel onder Windows als MacOS.

- Vanaf update 18.3 kunt u ook lijsten bekijken die in paginaonderdelen worden getoond, zoals de regels in een verkooporder. Voorlopig is deze mogelijkheid een optionele functie, waarvoor u **Een lijstonderdeel exporteren naar Excel** moet inschakelen in **Functiebeheer**. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Openen in Excel** standaard beschikbaar. Als u echter [!INCLUDE[prod_short](includes/prod_short.md)] on-premises instelt om gegevens in Excel te bewerken, wordt de actie **Openen in Excel** vervangen door de actie **Bewerken in Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Bewerken in Excel

Met de actie **Bewerken in Excel** kunt u wijzigingen aanbrengen in de records in Excel en de wijzigingen dan terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)].

- Met deze actie respecteert Excel de meeste filters op de pagina die het aantal weergegeven records beperken, dus de Excel-werkmap bevat bijna dezelfde records en kolommen.

- Dit werkt alleen onder Windows, niet onder MacOS.

- U kunt het bedrijf waarmee u werkt wijzigen. Om van bedrijf te veranderen selecteert u het pictogram **Opties** ![Opties van Excel-invoegtoepassing.](media/cogwheel.png "Opties van Excel-invoegtoepassing") In het Excel-invoegtoepassingsvenster en selecteert u vervolgens het bedrijf in het veld **Bedrijf**.  

    > [!IMPORTANT]
    > Zorg er bij het veranderen van bedrijf voor dat het veld **Omgeving** niet leeg is. Als dat zo is, stel het dan in op een van de beschikbare opties; anders werkt de invoegtoepassing niet correct.  

Als u wijzigingen aanbrengt in de invoegtoepassing, moet u deze opnieuw laden om de verbinding bij te werken. Gebruik om opnieuw te laden het menu ![menu van Excel-invoegtoepassing](media/excel-addin-menu.png "Menu van Excel-invoegtoepassing") in de rechterbovenhoek van de invoegtoepassing. Neem contact op met uw beheerder als u de invoegtoepassing niet kunt laden. Zie als u de beheerder bent [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw systeembeheerder is geconfigureerd, en alleen beschikbaar voor de webclient. Zie voor systeembeheerders [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) voor meer informatie over de installatie van de Excel-invoegtoepassing.

### <a name="see-the-differences-between-the-options"></a>Zie de verschillen tussen de opties
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Werken met Business Central](ui-work-product.md)  
[Verbeteringen aan Excel-integratie in releasewave 2 van 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]