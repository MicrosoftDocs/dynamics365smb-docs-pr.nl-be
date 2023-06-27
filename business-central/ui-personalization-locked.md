---
title: Waarom een pagina is vergrendeld voor personaliseren
description: 'Het kan zijn dat u een pagina niet kunt personaliseren. Lees hier wat u kunt doen om deze te ontgrendelen, zodat u deze kunt personaliseren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="why-a-page-is-locked-from-personalization"></a>Waarom een pagina is vergrendeld voor personaliseren

Er zijn twee voorwaarden die voorkomen dat u een pagina personaliseert. Of de pagina is vergrendeld (zoals aangegeven door het pictogram ![Personaliseringsvergrendeling.](media/personalization-lock-icon.png "Personalisatievergrendeling")) of de pagina is geblokkeerd (zoals aangegeven door het pictogram ![Personalisatie geblokkeerd.](media/personalization-blocked-icon.png "Personalisatie geblokkeerd")).  

## <a name="locked-from-personalizing"></a>Vergrendeld tegen personaliseren

Als er een pictogram ![Personaliseringsvergrendeling.](media/personalization-lock-icon.png "Personalisatievergrendeling") is, is te zien is op de banner **Personaliseren** wanneer u een pagina opent, kunt u op dit moment geen persoonlijke instellingen wijzigen op de pagina.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Hiervoor kunnen twee redenen bestaan:

1. U hebt de pagina eerder gepersonaliseerd, maar dit is met een eerdere versie van het product gebeurd. We hebben de manier waarop personalisatie achter de schermen werkt, gewijzigd sinds u de pagina voor het laatst hebt gepersonaliseerd. De oude en de nieuwe aanpak werken helaas niet goed samen.

2. Tot dusverre hebt u alleen de nu afgeschafte [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] gebruikt om de pagina te personaliseren.

### <a name="unlocking-the-page"></a>De pagina ontgrendelen

Als u een pagina wilt ontgrendelen en door wilt gaan met personaliseren, kiest u het pictogram ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personalisatievergrendeling") en kiest u vervolgens de actie **Ontgrendelen**.  

> [!CAUTION]
> De huidige personalisatie van de pagina wordt gewist. De pagina keert terug naar de oorspronkelijke indeling en u moet opnieuw beginnen.  

## <a name="blocked-from-personalizing"></a>Geblokkeerd tegen personaliseren

Als de banner **Personaliseren** het pictogram ![Personalisatie geblokkeerd](media/personalization-blocked-icon.png "Personalisatie geblokkeerd") bevat, betekent dit dat u geblokkeerd wordt om personalisatie op de pagina aan te brengen.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

De reden hiervoor is dat het rolcentrum of de rol die op dat moment aan uw gebruikersaccount is gekoppeld, deze pagina specifiek voor uw rol wijzigt. Neem contact op met uw beheerder voor hulp. U kunt ook overschakelen naar een rolcentrum met rolaanpassing voor deze pagina. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).

## <a name="see-also"></a>Zie ook

[Uw werkruimte personaliseren](ui-personalization-user.md)  
[Pagina's aanpassen voor profielen](ui-personalization-manage.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
