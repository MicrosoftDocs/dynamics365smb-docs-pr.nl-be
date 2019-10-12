---
title: Deel contacten tussen Business Central en Outlook| Microsoft Docs
description: Deze service heeft diepe integratie met Office 365, zodat u contacten kunt delen tussen Outlook en Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: c28118ad9aa894678e4630800c638cf252c4f524
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307786"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Contacten in Business Central synchroniseren met contacten in Microsoft Outlook
U kunt in [!INCLUDE[d365fin](includes/d365fin_md.md)] dezelfde contactpersonen zien als in Outlook als u synchronisatie van contactpersonen instelt. Als u bijvoorbeeld een verkoper bent, doet u mogelijk werk in Outlook en werk in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als de contactpersonen op beide plaatsen hetzelfde zijn, is uw werk eenvoudiger.  

Een speciale map in Outlook maakt het gemakkelijk contactpersonen te vinden en u kunt een filter instellen om alleen de contactpersonen uit [!INCLUDE[d365fin](includes/d365fin_md.md)] te synchroniseren die u in Outlook wilt zien. Als de synchronisatie van contactpersonen is ingesteld, kunt u de synchronisatie handmatig starten of een automatische synchronisatie instellen die de contacten op geplande basis gesynchroniseerd houdt.  

## <a name="set-up-synchronization"></a>Synchronisatie instellen
U stelt in hoe u contactpersonen wilt synchroniseren met Outlook op de pagina **Instelling van Exchange-synchronisatie** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als vereiste moet uw gebruikersprofiel in [!INCLUDE[d365fin](includes/d365fin_md.md)] uw Office 365 e-mailaccount opgeven. U kunt dit controleren in de sectie **Office 365-verificatie** van uw gebruikersprofiel in de lijst **Gebruikers**.  

Vervolgens kunt u op de pagina **Instelling van Exchange-synchronisatie** controleren of de verbinding met Exchange werkt en vervolgens synchronisatie van contactpersonen instellen. Open de pagina **Instelling van contactsynchronisatie** en start de synchronisatie. Stel desgewenst een filter in voor welke contactpersonen worden gesynchroniseerd tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Outlook. U kunt bijvoorbeeld een filter instellen op naam, type, bedrijf of iets soortgelijks. U kunt ook de standaardnaam wijzigen van de map waarmee de contactpersonen in Outlook worden gesynchroniseerd. De standaardnaam is *Business Central*.  

Wanneer deze synchronisatie is ingesteld, worden wijzigingen die u in de contactpersoon aanbrengt in Outlook of [!INCLUDE[d365fin](includes/d365fin_md.md)], met de andere gesynchroniseerd.  

Elk van uw collega's kan tevens hun eigen Exchange-synchronisatie instellen en hun eigen filter instellen op basis waarvan contactpersonen worden gesynchroniseerd.  

## <a name="synchronize-contacts"></a>Contactpersonen synchroniseren
Als u gewend bent met contactpersonen te werken in [!INCLUDE[d365fin](includes/d365fin_md.md)], is het gemakkelijk de synchronisatie handmatig wanneer het u uitkomt te starten vanuit de lijst **Contactpersonen**. Kies gewoon de actie **Synchroniseren met Office 365** en beslis of u het filter wilt wijzigen dat u hebt ingesteld. Wanneer u OK kiest, begint de synchronisatie direct en worden de nieuwste wijzigingen toegepast op uw contactpersonen in Outlook.  

In de lijst **Contactpersonen** kunt u contactpersonen op twee manieren synchroniseren:

* **Synchroniseren met Office 365**

  Deze actie synchroniseert alle wijzigingen sinds de vorige synchronisatie vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] naar Office 365, op basis van de datum van laatste wijziging. Nieuwe contactpersonen vanuit Office 365 worden ook terug gesynchroniseerd naar [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dit gaat meestal sneller dan een hele synchronisatie.  

* **Volledig synchroniseren met Office 365**

  Deze actie synchroniseert alle contacten in beide richtingen, ongeacht de datum van laatste synchronisatie en laatste wijziging.  

In beide gevallen worden contacten alleen gesynchroniseerd vanuit Outlook als ze de vereiste velden ingevuld hebben. De vereiste velden om te synchroniseren naar Office 365 zijn **Naam** en **E-mailadres**, en ze moeten van het type Persoon zijn. [!INCLUDE[d365fin](includes/d365fin_md.md)] is de hoofdtabel van de contactgegevens, dus de contactgegevens van [!INCLUDE[d365fin](includes/d365fin_md.md)] worden opgeslagen in het geval van duplicaten.  

In Outlook worden de contacten uit [!INCLUDE[d365fin](includes/d365fin_md.md)] weergegeven in een map onder **Overige contactpersonen** in de weergave **Mensen**. Als u niet vertrouwd bent met de weergave Mensen in Outlook, kunt u erheen gaan vanuit de navigatieopties in de linkerbenedenhoek van Outlook.  

## <a name="see-also"></a>Zie ook
[Aan de slag](product-get-started.md)  
[Financiën](finance.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Contactpersonen (personen) gebruiken in Outlook op het web](https://support.office.com/en-us/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
