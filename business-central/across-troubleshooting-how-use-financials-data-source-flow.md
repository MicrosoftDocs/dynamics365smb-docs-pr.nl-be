---
title: Problemen oplossen met integratie met Microsoft Flow| Microsoft Docs
description: Problemen oplossen met hoe u uw Financials-gegevens als gegevensbron beschikbaar kunt maken en een OData-URL van uw webservices kunt opgeven om een geautomatiseerde werkstroom te maken.
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 68355bc0b4afe4fcdd92f9cdb190d4b5c0d845df
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Problemen oplossen met integratie met Microsoft Flow - Aanvraag-URL te lang
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.  

> [!NOTE]  
>   U moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.  

Als u een Microsoft Flow maakt met de [!INCLUDE[d365fin](includes/d365fin_md.md)]-connector, kan er een foutbericht worden weergegeven dat de gevraagde URL te lang is na het maken van de stroom, zoals de volgende: **RequestUriTooLong**.

## <a name="cause"></a>Oorzaak
Voor een te activeren stroom wordt gezocht naar wijzigingen in uw gegevens. Wanneer wordt bepaald of uw gegevens zijn gewijzigd, vergelijken de connectors de gegevens in de cache met de nieuwe gegevens die uit de bron zijn aangevraagd.  

Als de gegevensaanvraag een URL maakt die te lang is, mislukt het. Veel voorkomende oorzaken zijn:
- Over het algemeen een brontabel met meer dan 250 rijen
- Brontabellen die duizenden records bevatten

## <a name="workaround"></a>Oplossing
Volg deze stappen als oplossing.
1. Kies ervoor de stroom te bewerken die is mislukt.
2. Vouw **Geavanceerde opties weergegeven** uit op de stroomtrigger.
3. Voer in het veld **Aantal overslaan** het aantal records in dat moet worden overgeslagen.  
Als de tabel die u als gegevensbron gebruikt, bijvoorbeeld 4000 records bevat, voert u 4000 in als het aantal records dat moet worden overgeslagen.
4. Werk uw stroom bij.

> [!NOTE]  
> De connector is nu in bèta. Updates op hoe gegevenswijzigingen worden behandeld in een toekomstige versie.


## <a name="see-also"></a>Zie ook
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  

