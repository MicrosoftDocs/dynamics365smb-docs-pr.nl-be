---
title: Een sandboxomgeving maken | Microsoft Docs
description: Maak een omgeving waarin u kunt ontdekken, leren, demonstreren, ontwikkelen en testen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/26/2019
ms.author: solsen
ms.openlocfilehash: 10ccbc7546aa5d03c3837997a721c63c3ce465da
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796677"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Een sandboxomgeving maken
Een sandboxomgeving (voorbeeld) is een niet-productie-exemplaar van [!INCLUDE[d365fin](includes/d365fin_md.md)]. Geïsoleerd van de productieomgeving is een sandboxomgeving de plaats om de service te ontdekken, te leren kennen, te demonstreren, te ontwikkelen en te testen, zonder het risico te lopen dat de gegevens en instellingen van uw productieomgeving worden beïnvloed.

## <a name="to-create-a-sandbox-environment"></a>Een sandboxomgeving maken
U moet een abonnement op [!INCLUDE[d365fin](includes/d365fin_md.md)] hebben om een sandboxomgeving te maken. Per abonnement kan er slechts één sandboxomgeving bestaan.

1. Meld aan bij uw productie-exemplaar van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-service.

2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Sandboxomgeving** in en kies vervolgens de gerelateerde koppeling.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Kies de knop **Maken**.  

    Er wordt een ander tabblad met [!INCLUDE[d365fin](includes/d365fin_md.md)] geopend, waar u de installatie van uw sandbox-omgeving kunt voltooien.

    > [!NOTE]  
    >  Als u pop-upblokkering hebt ingeschakeld in uw browser, wijzigt u deze om URL's van het adres *.businesscentral.dynamics.com toe te staan.

4. Wanneer de sandboxomgeving gereed is, wordt u omgeleid naar de welkomstwizard van de sandboxomgeving.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Kies de knop **Meer informatie** om te lezen over scenario's die u in een sandbox-omgeving kunt proberen of kies de knop **Sluiten** om door te gaan naar het rolcentrum van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandboxexemplaar.

    Boven in het rolcentrum verschijnt een bericht om u te laten weten dat dit een sandboxomgeving is. Ook in de titelbalk van de client wordt de soort omgeving weergegeven.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > Een sandbox-omgeving die op deze manier is gemaakt, bevat alleen de standaarddemonstratiegegevens voor het CRONUS-bedrijf. Er worden geen gegevens gekopieerd of anderszins overgedragen vanuit de productieomgeving.<br /><br />
    > U kunt ook een sandbox-omgeving maken met de productiegegevens. U moet dit doen via het beheercentrum. Zie voor meer informatie [Omgevingen beheren](/business-central/dev-itpro/administration/tenant-admin-center-environments) in de Ontwikkelaar en IT Pro Help.

6. U kunt op elk moment terugkeren naar de pagina **Sandboxomgeving** en de sandboxomgeving herstellen.
    > [!NOTE]  
    >  Wanneer u de sandboxomgeving herstelt, wordt deze volledig verwijderd en vervolgens opnieuw gemaakt met de standaarddemonstratiegegevens.  

7. Als u wilt schakelen tussen uw productie- en sandboxomgeving, kunt u het startprogramma voor apps van Business Central gebruiken.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. Een beheerder of een andere gebruiker kan de toegang tot de sandboxomgeving voor sommige gebruikers beperken of zelfs blokkeren. Dit kunt u doen met de standaardbeveiligingsfuncties van het product, zoals de gebruikerskaart, gebruikersgroepen en machtigingensets.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Geavanceerde functionaliteit in de sandboxomgeving
### <a name="designer"></a>Ontwerper
In een sandboxomgeving is de functie **Ontwerper** ingeschakeld. U kunt deze functie activeren door het pictogram ![Ontwerper](./media/across-sandbox/sandbox-inclient-design-icon.png) te selecteren op een pagina.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>De geavanceerde gebruikerservaring inschakelen
Het is mogelijk om de geavanceerde (volledige) functionaliteit van [!INCLUDE[d365fin](includes/d365fin_md.md)] in een sandboxtenant in te schakelen door het veld **Ervaring** op de pagina **Bedrijfsgegevens** in te stellen.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Als u de geavanceerde functionaliteit in een sandboxtenant hebt ingeschakeld, krijgt u toegang tot alle standaardprofielen (rollen) en rolcentra. U kunt ook een evaluatiebedrijf maken dat volledig is ingesteld, inclusief demonstratiegegevens en toegang tot de geavanceerde gebieden van het product.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
