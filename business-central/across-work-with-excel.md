---
title: Weergeven en bewerken in Excel vanuit Business Central (bevat video)
description: Leer hoe u de pagina's in Microsoft Excel opent vanuit Business Central voor betere gegevensanalyse.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: d27ad94c21325808d92b8f71e97a5bb8a484ded5
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142613"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Weergeven en bewerken in Excel vanuit Business Central

Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de lijst exporteren naar Microsoft Excel en deze daar weergeven. Afhankelijk van de pagina hebt u twee opties voor weergave in Excel. Beide opties zijn verkrijgbaar via het pictogram **Delen** ![Een pagina delen in een andere app.](media/share-icon.png) bovenaan een pagina. U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren. In dit artikel worden de verschillen tussen de twee acties uitgelegd.

## <a name="open-in-excel"></a>Openen in Excel

Met de actie **Openen in Excel** kunt u wijzigingen aanbrengen in de records in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt de wijzigingen alleen opslaan in een Excel-bestand, zonder dat dit invloed heeft op de gegevens in [!INCLUDE[prod_short](includes/prod_short.md)].

- Met deze actie houdt Excel rekening met alle filters op de pagina waarmee de weergegeven records worden beperkt. De Excel-werkmap zal dezelfde rijen en kolommen bevatten die worden weergegeven op de pagina in [!INCLUDE[prod_short](includes/prod_short.md)].

- Deze actie werkt zowel onder Windows als MacOS.

- Vanaf update 18.3 kunt u ook lijsten bekijken die in paginaonderdelen worden getoond, zoals de regels in een verkooporder. 

> [!NOTE]
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Openen in Excel** standaard beschikbaar. Als u echter [!INCLUDE[prod_short](includes/prod_short.md)] on-premises instelt om gegevens in Excel te bewerken, wordt de actie **Openen in Excel** vervangen door de actie **Bewerken in Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Bewerken in Excel

De actie **Bewerken in Excel** is beschikbaar bij de meeste lijsten, maar niet alle. Met de actie **Bewerken in Excel** kunt u wijzigingen aanbrengen in de records in Excel en de wijzigingen dan terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer Excel wordt geopend, ziet u het deelvenster **Excel-invoegtoepassing** aan de rechterkant.

- Met deze actie respecteert Excel de meeste filters op de pagina die het aantal weergegeven records beperken, dus de Excel-werkmap bevat bijna dezelfde records en kolommen.

- Om de laatste gegevens te krijgen van [!INCLUDE[prod_short](includes/prod_short.md)], kiest u **Vernieuwen** in het deelvenster Excel-invoegtoepassing.

- U kunt het bedrijf waarmee u werkt wijzigen. Om van bedrijf te veranderen selecteert u het pictogram **Opties** ![Opties van Excel-invoegtoepassing.](media/cogwheel.png "Opties van Excel-invoegtoepassing") In het Excel-invoegtoepassingsvenster en selecteert u vervolgens het bedrijf in het veld **Bedrijf**.  

    > [!IMPORTANT]
    > Zorg er bij het veranderen van bedrijf voor dat het veld **Omgeving** niet leeg is. Als dat zo is, stel het dan in op een van de beschikbare opties; anders werkt de invoegtoepassing niet correct.  

Als u wijzigingen aanbrengt in de invoegtoepassing, moet u deze opnieuw laden om de verbinding bij te werken. Gebruik om opnieuw te laden het menu ![menu van Excel-invoegtoepassing](media/excel-addin-menu.png "Menu van Excel-invoegtoepassing") in de rechterbovenhoek van de invoegtoepassing. Neem contact op met uw beheerder als u de invoegtoepassing niet kunt laden. Als u de beheerder bent, zie [De Business Central-invoegtoepassing voor Excel verkrijgen](admin-deploy-excel-addin.md).

> [!NOTE]
> De invoegtoepassing werkt met Excel voor het web (online) vanaf elk apparaat, zolang u maar een ondersteunde browser gebruikt. Het werkt ook met de Excel-app voor Windows (pc); maar niet voor macOS.
>
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw systeembeheerder is geconfigureerd, en alleen beschikbaar voor de webclient. Zie voor systeembeheerders [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) voor meer informatie over de installatie van de Excel-invoegtoepassing.


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Eerste aanmelding

De actie **Bewerken in Excel** vereist dat de Business Central-invoegtoepassing in Excel is geïnstalleerd. In sommige gevallen heeft uw beheerder de invoegtoepassing mogelijk zo ingesteld dat deze automatisch voor u wordt geïnstalleerd. In dit geval hoeft u zich alleen maar aan te melden bij Business Central in het deelvenster **Excel-invoegtoepassing** met uw gebruikersnaam en wachtwoord. Anders wordt het deelvenster **Nieuwe Office-invoegtoepassing** geopend. Om de invoegtoepassing te installeren kiest u **Deze invoegtoepassing vertrouwen**, waardoor de invoegtoepassing rechtstreeks vanuit de Office Store wordt geïnstalleerd.

Als de invoegtoepassing om de een of andere reden niet wordt geïnstalleerd, neemt u contact op met uw beheerder of probeert u deze handmatig te installeren. Zie voor meer informatie [De invoegtoepassing handmatig installeren voor eigen gebruik](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Zie de verschillen tussen de opties
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Werken met Business Central](ui-work-product.md)  
[Verbeteringen aan Excel-integratie in releasewave 2 van 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]