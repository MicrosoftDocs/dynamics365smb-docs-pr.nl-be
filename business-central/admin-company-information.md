---
title: Overzicht van bedrijfsgegevens
description: 'De pagina Bedrijfsgegevens bevat basisinformatie voor een zakelijke entiteit, zoals naam, adressen en verzendgegevens.'
author: jswymer
ms.topic: conceptual
ms.search.form: 1
ms.date: 09/24/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---

# <a name="company-information-overview"></a>Overzicht van bedrijfsgegevens

[!INCLUDE[prod_short](includes/prod_short.md)] organiseert zakelijke entiteiten in *bedrijven*. Voor elk bedrijf moet u enkele basisgegevens van het bedrijf en relevante informatie invullen op de pagina **Bedrijfsgegevens**. De informatie op de pagina [**Bedrijfsgegevens**](https://businesscentral.dynamics.com/?page=1) wordt gebruikt in documenten, zoals factuurkoppen. U kunt meer dan één bedrijf instellen, bijvoorbeeld een moederbedrijf en een dochteronderneming.  

Als het voorraadmagazijn van het bedrijf zich op een ander adres bevindt dan het hoofdkantoor, kunt u de verschillende verzendvelden en het veld **Vestiging** op het sneltabblad **Verzending** invullen. De gegevens in deze velden worden vervolgens bijvoorbeeld afgedrukt op inkooporders, zodat leveranciers de artikelen naar de juiste vestiging verzenden.  

Voor elk bedrijf dat u instelt, moet u de pagina **Bedrijfsgegevens** invullen, samen met de pagina en **Grootboekinstellingen**. U moet ook elk gebied instellen in [!INCLUDE [prod_short](includes/prod_short.md)], zoals de pagina **Verkoopinstellingen**, voor elk bedrijf. Meer informatie vindt u in [Overzicht van taken om [!INCLUDE[prod_short](includes/prod_short.md)] in te stellen](setup.md).  

De pagina **Bedrijfsgegevens** bevat verschillende velden en sneltabbladen, afhankelijk van uw land/regio. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] De volgende tabel beschrijft de meest gebruikte sneltabbladen.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Als u klaar bent met het invullen van de gegevens, kunt u de pagina sluiten.  

## <a name="working-with-multiple-companies"></a>Werken met meerdere bedrijven

Als uw [!INCLUDE [prod_short](includes/prod_short.md)] meerdere bedrijven omvat, willen uw gebruikers wellicht met *bedrijfsbadges* werken zodat ze snel kunnen bepalen en bijhouden in welk bedrijf ze momenteel werken. Zie voor meer informatie [Een bedrijfsbadge selecteren](#badge).

Er zijn een paar functies die u kunt gebruiken om tussen bedrijven te schakelen terwijl u werkt, zoals de bedrijfswisselaar (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Meer informatie vindt u in [Overschakelen naar een ander bedrijf of een andere omgeving](ui-organization-switch.md).

## <a name="display-a-company-badge"></a><a name="badge"></a>Een bedrijfsbadge weergeven

Als er meer dan één bedrijf of omgeving is, ziet u de bedrijfsschakelaar rechtsboven in de app-balk, naast het zoekpictogram in de app-balk. Standaard gebruikt de bedrijfswisselaar een standaard bedrijfspictogram, zoals ![bedrijfspictogram Launcher.](media/ui-experience/company-icon.png "Geeft het bedrijfsschakelaarpictogram weer dat wordt gebruikt wanneer er één omgeving is") en ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Geeft het bedrijfsschakelaarpictogram weer dat wordt gebruikt wanneer er meerdere omgevingen zijn").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Toont het bedrijfsschakelaarpictogram in de kop van de Business Central-client.":::  

Vanaf releasewave 2, versie 23 van 2023, verschijnt de bedrijfsbadge op het browsertabblad bij gebruik van de webclient. Het wordt ook opgenomen in paginakoppelingen die u [kopieert en plakt](across-share-data-features.md#copying-a-link) in rich-text-editors, zoals Word, Outlook en Teams.
 
### <a name="set-the-company-badge"></a>De bedrijfsbadge instellen

Met de pagina **Bedrijfsgegevens** kunt u het standaardbedrijfspictogram per bedrijf vervangen door een aangepaste badge per bedrijf als de bedrijfsbadge het voor gebruikers gemakkelijker maakt om het bedrijf waarin ze werken te identificeren.

1. Vul op het sneltabblad **Bedrijfsbadge** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Als u klaar bent, vernieuwt u de browser (selecteer <kbd>Ctrl</kbd>+<kbd>F5</kbd>) om de badge in de client bij te werken.  

> [!NOTE]
> De bedrijfsschakelaar is geïntroduceerd in releasewave 2 van 2022, versie 21. In eerdere releases wordt de bedrijfsbadge niet gebruikt om te schakelen tussen bedrijven. De schakelaar wordt weergegeven in de rechterbovenhoek van de meeste pagina's, zelfs als er maar één bedrijf is. Als u de schakelaar selecteert, worden de volledige bedrijfsnaam en omgevingsnaam weergegeven.

## <a name="change-company-display-name"></a>Bedrijfsweergavenaam wijzigen

De bedrijfsnaam wordt altijd in de linkerbovenhoek weergegeven en werkt als een actie die u kunt kiezen om terug te gaan naar het rolcentrum. U kunt deze naam wijzigen op de pagina **Bedrijfsgegevens**.

1. Kies het ![pictogram Tand om het menu Instellingen te openen.](media/ui-experience/settings_icon_small.png) en kies vervolgens de actie **Bedrijfsgegevens**.
2. Voer in het veld **Naam** de nieuwe bedrijfsnaam in.
3. Verlaat de pagina. Het systeem start opnieuw op en geeft het nieuwe bedrijf in de linkerbovenhoek weer.

## <a name="experience"></a>Ervaring

De standaardgebruikerservaring in een [!INCLUDE [prod_short](includes/prod_short.md)]-proefversie omvat niet alle mogelijkheden. U kunt de volledige ervaring inschakelen op de pagina **Bedrijfsgegevens**. Zie voor meer informatie [Wijzigen welke functies worden weergegeven](ui-experiences.md).  

## <a name="see-also"></a>Zie ook

[Overzicht van taken voor het instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Snelstartgids Bedrijfsgegevens](quick-start-company-information.md)  
[Bedrijfsgegevens instellen in Italië](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Nieuwe bedrijven maken](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
