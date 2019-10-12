---
title: Problemen met synchronisatiefouten oplossen | Microsoft Docs
description: Geeft een leidraad voor het identificeren en oplossen van synchronisatiefouten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304293"
---
# <a name="troubleshooting-synchronization-errors"></a>Problemen met synchronisatiefouten oplossen
Er zijn veel factoren betrokken bij de integratie van [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[crm_md](includes/crm_md.md)]en soms gaat het mis. In dit onderwerp worden enkele van de veel voorkomende fouten beschreven en worden enkele tips gegeven voor het oplossen van deze fouten.

Fouten komen vaak voor als gevolg van iets wat een gebruiker heeft gedaan met gekoppelde records of er is iets mis met de manier waarop de integratie is ingesteld. Fouten met betrekking tot gekoppelde records kunnen gebruikers zelf oplossen. Deze fouten worden veroorzaakt door acties zoals het verwijderen van een record in één, maar niet beide, zakelijke apps en vervolgens synchroniseren. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fouten die gerelateerd zijn aan hoe de integratie is ingesteld, vereisen doorgaans de aandacht van een beheerder. U kunt deze fouten bekijken op de pagina **Synchronisatiefouten bij integratie**. Voorbeelden van enkele typische problemen zijn:  
  
* De machtigingen en rollen die aan gebruikers zijn toegewezen, zijn niet correct.  
* Het beheerdersaccount is opgegeven als de integratiegebruiker.  
* Het wachtwoord van de integratiegebruiker is ingesteld om een wijziging te vereisen wanneer de gebruiker zich aanmeldt.  
* De wisselkoersen voor valuta's zijn niet opgegeven in de ene of de andere app.  
  
U moet de fouten handmatig oplossen, maar er zijn een paar manieren waarop de pagina u helpt. Voorbeeld:  

* De velden **Bron** en **Bestemming** kunnen koppelingen bevatten naar de record waar de fout is gevonden. Klik op de koppeling om de record te openen en de fout te onderzoeken.  
* De acties **Posten ouder dan 7 dagen verwijderen** en **Alle items verwijderen** schonen de lijst op. Meestal gebruikt u deze acties nadat u de oorzaak van een fout hebt opgelost die van invloed is op veel records. Wees echter voorzichtig. Met deze acties kunnen fouten worden verwijderd die nog steeds relevant zijn.

## <a name="see-also"></a>Zie ook
[Integreren met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gebruikersaccounts instellen voor integratie met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)  
[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  