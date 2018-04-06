---
title: Uw gegevens verbinden met Flow| Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een geautomatiseerde werkstroom te maken.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23e9ebbb75d23595d568d022526e551bf590a979
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in een geautomatiseerde werkstroom
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.  

> [!NOTE]  
>   U moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Flow toevoegen
1. Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com/en-us/) en meld u aan.
2. Kies **Mijn Flows** vanuit het lint boven aan de pagina.
3. Kies in het venster **Mijn Flows** de optie **Geheel nieuw maken**.
4. Selecteer in de lijst met beschikbare triggers een van de beschikbare [!INCLUDE[d365fin](includes/d365fin_md.md)]-triggers:  
    *Wanneer een klantgoedkeuring wordt aangevraagd*,  
    *Wanneer goedkeuring van een dagboekbatch wordt aangevraagd*,  
    *Wanneer goedkeuring van een dagboekregel wordt aangevraagd*,  
    *Wanneer goedkeuring van een artikel wordt aangevraagd*,  
    *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*,  
    *Wanneer goedkeuring van een verkoopdocument wordt aangevraagd*, of  
    *Wanneer goedkeuring van een leverancier wordt aangevraagd*.
5. Flow vraagt u een bedrijf in uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-tenant te selecteren. Aangezien elke stap in Flow onafhankelijk is van de volgende, moet u het bedrijf mogelijk meerdere malen definiëren wanneer u een [!INCLUDE[d365fin](includes/d365fin_md.md)]-sjabloon gebruikt.

Nu hebt u met succes een verbinding gemaakt met uw Business Central-gegevens en kunt u uw stroom gaan maken. Zie de [Flow-documentatie](https://flow.microsoft.com/documentation/getting-started/) voor meer informatie.

Zie voor het oplossen van problemen met Microsoft Flow [Problemen oplossen met integratie met Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Zie ook
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  

