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
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 82b5f3ec52be27c4fbe60a6a63a0cfc5f6f1bd7c
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196555"
---
# <a name="troubleshooting-synchronization-errors"></a>Problemen met synchronisatiefouten oplossen
Er zijn veel factoren betrokken bij de integratie van [!INCLUDE[d365fin](includes/d365fin_md.md)] met Common Data Serviceen soms gaat het mis. In dit onderwerp worden enkele van de veel voorkomende fouten beschreven en worden enkele tips gegeven voor het oplossen van deze fouten.

Fouten komen vaak voor als gevolg van iets wat een gebruiker heeft gedaan met gekoppelde records of er is iets mis met de manier waarop de integratie is ingesteld. Fouten met betrekking tot gekoppelde records kunnen gebruikers zelf oplossen. Deze fouten worden veroorzaakt door acties zoals het verwijderen van een record in één, maar niet beide, zakelijke apps en vervolgens synchroniseren. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),

## <a name="example"></a>Voorbeeld
Deze video toont een voorbeeld van het oplossen van fouten die zijn opgetreden tijdens het synchroniseren met Sales. Het proces is voor alle integraties hetzelfde. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fouten die gerelateerd zijn aan hoe de integratie is ingesteld, vereisen doorgaans de aandacht van een beheerder. U kunt deze fouten bekijken op de pagina **Synchronisatiefouten bij integratie**. Voorbeelden van enkele typische problemen zijn:  
  
* De machtigingen en rollen die aan gebruikers zijn toegewezen, zijn niet correct.  
* Het beheerdersaccount is opgegeven als de integratiegebruiker.  
* Het wachtwoord van de integratiegebruiker is ingesteld om een wijziging te vereisen wanneer de gebruiker zich aanmeldt.  
* De wisselkoersen voor valuta's zijn niet opgegeven in de ene of de andere app.  
  
U moet de fouten handmatig oplossen, maar er zijn een paar manieren waarop de pagina u helpt. Voorbeeld:  

* De velden **Bron** en **Bestemming** kunnen koppelingen bevatten naar de record waar de fout is gevonden. Klik op de koppeling om de record te openen en de fout te onderzoeken.  
* De acties **Posten ouder dan 7 dagen verwijderen** en **Alle items verwijderen** schonen de lijst op. Meestal gebruikt u deze acties nadat u de oorzaak van een fout hebt opgelost die van invloed is op veel records. Wees echter voorzichtig. Met deze acties kunnen fouten worden verwijderd die nog steeds relevant zijn.

Soms kunnen de tijdstempels in records conflicten veroorzaken. De tabel 'CDS-integratierecord' bevat de tijdstempels 'Laatste synchronisatie gewijzigd op' en 'Laatste synchr. CDS gewijzigd op' voor de laatste integratie in beide richtingen voor een record. Deze tijdstempels worden vergeleken met tijdstempels in Business Central- en Sales-records. In Business Central staat de tijdstempel in de tabel Integratierecord.

U kunt filteren op records die moeten worden gesynchroniseerd door de tijdstempels van records te vergelijken in de tabel 'Toewijzing van integratietabel', namelijk de velden 'Filter synchr. gewijzigd op' en 'Filter synchr. int.-tbl gewijz. op fltr.'.

Het conflictfoutbericht 'Kan de klantrecord niet bijwerken omdat deze een latere wijzigingsdatum heeft dan de accountrecord' of "Kan de accountrecord niet bijwerken omdat deze een latere wijzigingsdatum heeft dan de klantrecord' kan optreden als een record een tijdstempel heeft dat is groter dan Toewijzing van integratietabel.'Filter synchr. gewijzigd op' maar niet recenter is dan het tijdstempel op Verkoopintegratierecord. Dit betekent dat de bronrecord handmatig is gesynchroniseerd, niet door de taakwachtrijpost. 

Het conflict treedt op omdat de doelrecord ook is gewijzigd: het tijdstempel van de record is recenter dan het tijdstempel van Verkoopintegratierecord. De bestemmingscontrole vindt alleen plaats voor bidirectionele tabellen. 

Deze records worden nu verplaatst naar de pagina 'Overgeslagen synchronisatierecords', die u opent vanaf de pagina Microsoft Dynamics-verbinding instellen in Business Central. Daar kunt u opgeven welke wijzigingen moeten worden bewaard en vervolgens de records opnieuw synchroniseren.

## <a name="see-also"></a>Zie ook
[Integreren met Common Data Service](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gebruikersaccounts instellen voor integratie met Common Data Service](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)  
[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  
