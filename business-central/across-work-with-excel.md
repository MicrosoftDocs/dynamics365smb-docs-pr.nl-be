---
title: Weergeven en bewerken in Excel vanuit Business Central (bevat video)
description: Leer hoe u de pagina's in Microsoft Excel opent vanuit Business Central voor betere gegevensanalyse.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Weergeven en bewerken in Excel vanuit Business Central

Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de lijst exporteren naar Microsoft Excel en deze daar weergeven. Afhankelijk van de pagina hebt u twee opties voor weergave in Excel. Beide opties zijn verkrijgbaar via het pictogram **Delen** ![Een pagina delen in een andere app.](media/share-icon.png) bovenaan een pagina. U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren. In dit artikel worden de twee acties uitgelegd.

## Openen in Excel

Met de actie **Openen in Excel** kunt u wijzigingen aanbrengen in de records in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt de wijzigingen alleen opslaan in een Excel-bestand, zonder dat dit invloed heeft op de gegevens in [!INCLUDE[prod_short](includes/prod_short.md)].

- Met deze actie houdt Excel rekening met alle filters op de pagina waarmee de weergegeven records worden beperkt. De Excel-werkmap zal dezelfde rijen en kolommen bevatten die worden weergegeven op de pagina in [!INCLUDE[prod_short](includes/prod_short.md)].

- Deze actie werkt zowel onder Windows als MacOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

> [!IMPORTANT]
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Openen in Excel** standaard beschikbaar. Als u echter [!INCLUDE[prod_short](includes/prod_short.md)] on-premises instelt om gegevens in Excel te bewerken, wordt de actie **Openen in Excel** vervangen door de actie **Bewerken in Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> In Excel hebben hele getallen in kolommen een decimaalteken aan het eind (zoals een punt `.` of komma `,`), ook al wordt het decimaalteken niet weergegeven in Business Central. Het decimaalteken is afhankelijk van de regio-instellingen van uw apparaat. Bijvoorbeeld, `10` in Business Central kan verschijnen als `10.` of `10,` in Excel. U kunt de indeling in Excel wijzigen door de waarden te selecteren en vervolgens <kbd>Ctrl</kbd>+<kbd>1 te selecteren</kbd>. Ga voor meer informatie over het wijzigen van de getalindeling in Excel naar [Getallen opmaken](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).


## Bewerken in Excel

De actie **Bewerken in Excel** is beschikbaar bij de meeste lijsten, maar niet alle. Met de actie **Bewerken in Excel** kunt u wijzigingen aanbrengen in de records in Excel en de wijzigingen dan terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer Excel wordt geopend, ziet u het deelvenster **Excel-invoegtoepassing** aan de rechterkant.

- Met deze actie respecteert Excel de meeste filters op de pagina die het aantal weergegeven records beperken, dus de Excel-werkmap bevat bijna dezelfde records en kolommen.

- Om de laatste gegevens van [!INCLUDE[prod_short](includes/prod_short.md)] te krijgen, kiest u **Vernieuwen** in het deelvenster Excel-invoegtoepassing.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### Eerste aanmelding

De actie **Bewerken in Excel** vereist dat de Business Central-invoegtoepassing in Excel is geïnstalleerd. In sommige gevallen heeft uw beheerder de invoegtoepassing mogelijk zo ingesteld dat deze automatisch voor u wordt geïnstalleerd. In dit geval hoeft u zich alleen maar aan te melden bij Business Central in het deelvenster **Excel-invoegtoepassing** met uw gebruikersnaam en wachtwoord. Anders wordt het deelvenster **Nieuwe Office-invoegtoepassing** geopend. Om de invoegtoepassing te installeren kiest u **Deze invoegtoepassing vertrouwen**, waardoor de invoegtoepassing rechtstreeks vanuit de Office Store wordt geïnstalleerd.

Als de invoegtoepassing niet wordt geïnstalleerd, neemt u contact op met uw beheerder of probeert u deze handmatig te installeren. Zie voor meer informatie [De invoegtoepassing handmatig installeren voor eigen gebruik](admin-deploy-excel-addin.md#install).

### Werken in omgevingen en bedrijven

U kunt het bedrijf waarmee u werkt wijzigen. Om van bedrijf te veranderen selecteert u het pictogram **Opties** ![Opties van Excel-invoegtoepassing.](media/cogwheel.png "Opties van Excel-invoegtoepassing") In het Excel-invoegtoepassingsvenster en selecteert u vervolgens het bedrijf in het veld **Bedrijf**.  

> [!IMPORTANT]
> Zorg er bij het veranderen van bedrijf voor dat het veld **Omgeving** niet leeg is. Als dat zo is, stel het dan in op een van de beschikbare opties; anders werkt de invoegtoepassing niet correct.  

Als u wijzigingen aanbrengt in de invoegtoepassing, moet u deze opnieuw laden om de verbinding bij te werken. Gebruik om opnieuw te laden het menu ![menu van Excel-invoegtoepassing](media/excel-addin-menu.png "Menu van Excel-invoegtoepassing") in de rechterbovenhoek van de invoegtoepassing. Neem contact op met uw beheerder als u de invoegtoepassing niet kunt laden. Als u de beheerder bent, zie [De Business Central-invoegtoepassing voor Excel verkrijgen](admin-deploy-excel-addin.md).

> [!NOTE]
> De invoegtoepassing werkt met Excel voor het web (online) vanaf elk apparaat, zolang u maar een ondersteunde browser gebruikt. Het werkt ook met de Excel-app voor Windows (pc); maar niet voor macOS.
>
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw systeembeheerder is geconfigureerd, en alleen beschikbaar voor de webclient. Zie voor systeembeheerders [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) voor meer informatie over de installatie van de Excel-invoegtoepassing.

### Limieten bij het gebruik van Excel voor het web 

Wanneer **Bewerken in Excel** wordt gebruikt op lijstpagina's voor tabellen met veel kolommen, heeft de resulterende werkmap mogelijk te veel kolommen om het bestand te kunnen bekijken in Excel voor het web. In [!INCLUDE[prod_short](includes/prod_short.md)] wordt de geëxporteerde werkmap automatisch beperkt tot 100 kolommen wanneer OneDrive is geconfigureerd voor systeemfuncties. 

<!--## See the differences between the options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]-->

## Zie ook

[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Werken met Business Central](ui-work-product.md)  
[Verbeteringen aan Excel-integratie in releasewave 2 van 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
