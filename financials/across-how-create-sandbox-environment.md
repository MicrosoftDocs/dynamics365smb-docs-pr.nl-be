---
title: Een sandboxomgeving maken | Microsoft Docs
description: Maak een omgeving waarin u kunt ontdekken, leren, demonstreren, ontwikkelen en testen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3ee160e2c38107aea1342b51d729aa172bbbc3e
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a>Een sandboxomgeving maken
Een sandboxomgeving (voorbeeld) is een niet-productie-exemplaar van [!INCLUDE[d365fin](includes/d365fin_md.md)]. Geïsoleerd van de productieomgeving is een sandboxomgeving de plaats om de service te ontdekken, te leren kennen, te demonstreren, te ontwikkelen en te testen, zonder het risico te lopen dat de gegevens en instellingen van uw productieomgeving worden beïnvloed.

## <a name="to-create-a-sandbox-environment"></a>Een sandboxomgeving maken
U moet een abonnement op [!INCLUDE[d365fin](includes/d365fin_md.md)] hebben om een sandboxomgeving te maken. Per abonnement kan er slechts één sandboxomgeving bestaan.

1. Meld aan bij uw productie-exemplaar van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-service.
2. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Sandboxomgeving** in en kies vervolgens de gerelateerde koppeling.
![Instellingen van sandboxomgeving](./media/across-sandbox/sandbox-environment-setup.png)
3. Selecteer **Maken**.  
  Er wordt een ander tabblad in uw browser geopend waarin u de instelling van uw sandboxomgeving kunt voltooien.
> [!NOTE]  
>  Als u pop-upblokkering hebt ingeschakeld in uw browser, wijzigt u deze om URL's van het adres *.financials.dynamics.com toe te staan.   

4. Wanneer de sandboxomgeving gereed is, wordt u omgeleid naar de welkomstwizard van de sandboxomgeving.
![Welkomstwizard van sandbox](./media/across-sandbox/sandbox-wizard.png)

5. Kies **Meer informatie** voor scenario's die u in een sandboxomgeving kunt uitproberen. U kunt ook **Sluiten** kiezen om door te gaan naar het rolcentrum van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandboxexemplaar.
6. Boven in het rolcentrum verschijnt een bericht om u te laten weten dat dit een sandboxomgeving is. Ook in de titelbalk van de client wordt de soort omgeving weergegeven.
![Bericht in rolcentrum van sandbox](./media/across-sandbox/sandbox-rolecenter-notification.png)  
In de sandboxomgeving wordt een gloednieuwe tenant gemaakt. Deze tenant wordt geladen met standaarddemonstratiegegevens voor het CRONUS-bedrijf. Tijdens het maken van de sandbox worden er geen gegevens gekopieerd of anderszins overgebracht vanuit de productieomgeving.
7.  U kunt op elk moment terugkeren naar de pagina **Sandboxomgeving** en de sandboxomgeving herstellen.
> [!NOTE]  
>  Wanneer u de sandboxomgeving herstelt, wordt deze volledig verwijderd en vervolgens opnieuw gemaakt met de standaarddemonstratiegegevens.  

8.  Als u wilt schakelen tussen uw productie- en sandboxomgeving, kunt u het startprogramma voor apps van Finance and Operations, Business edition gebruiken.
![Dynamics 365-menu in sandbox](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Een beheerder of een andere gebruiker kan de toegang tot de sandboxomgeving voor sommige gebruikers beperken of zelfs blokkeren. Dit kunt u doen met de standaardbeveiligingsfuncties van het product, zoals de kaart Gebruiker, gebruikersgroepen en machtigingensets.

![Machtigingensets sandbox](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Geavanceerde functionaliteit in de sandboxomgeving
### <a name="the-in-client-designer"></a>De in-clientontwerper
In een sandboxomgeving is de functie voor in-clientontwerper ingeschakeld. U kunt deze functie activeren door het ontwerppictogram ![Ontwerper](./media/across-sandbox/sandbox-inclient-design-icon.png) op een pagina te selecteren.

![In-clientontwerper](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>De geavanceerde gebruikerservaring inschakelen
Het is mogelijk om de geavanceerde (volledige) functionaliteit van [!INCLUDE[d365fin](includes/d365fin_md.md)] in een sandboxtenant in te schakelen door het veld **Ervaring** op de pagina **Bedrijfsgegevens** in te stellen.

![Geavanceerde sandboxomgeving](./media/across-sandbox/sandbox-advanced.png)

![Sandboxproductie](./media/across-sandbox/sandbox-production.png)

Als u de geavanceerde functionaliteit in een sandboxtenant hebt ingeschakeld, krijgt u toegang tot alle standaardprofielen en rolcentra. U kunt ook een evaluatiebedrijf maken dat volledig is ingesteld, inclusief demonstratiegegevens en toegang tot de geavanceerde gebieden van het product.

![Nieuw bedrijf in sandbox](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

