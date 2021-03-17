---
title: Problemen met synchronisatiefouten oplossen | Microsoft Docs
description: Geeft een leidraad voor het identificeren en oplossen van synchronisatiefouten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: ba7ec915dabd40a1f2287eb3310d1fad23f6090e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377860"
---
# <a name="troubleshooting-synchronization-errors"></a>Problemen met synchronisatiefouten oplossen
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Er zijn veel factoren betrokken bij de integratie van [!INCLUDE[prod_short](includes/prod_short.md)] met [!INCLUDE[prod_short](includes/cds_long_md.md)]en soms gaat het mis. In dit onderwerp worden enkele van de veel voorkomende fouten beschreven en worden enkele tips gegeven voor het oplossen van deze fouten.

Fouten komen vaak voor als gevolg van iets wat een gebruiker heeft gedaan met gekoppelde records of er is iets mis met de manier waarop de integratie is ingesteld. Fouten met betrekking tot gekoppelde records kunnen gebruikers zelf oplossen. Deze fouten worden veroorzaakt door acties zoals het verwijderen van gegevens in één, maar niet beide, zakelijke apps en vervolgens synchroniseren. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),

## <a name="example"></a>Voorbeeld
Deze video toont een voorbeeld van het oplossen van fouten die zijn opgetreden tijdens het synchroniseren met Sales. Het proces is voor alle integraties hetzelfde. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fouten die gerelateerd zijn aan hoe de integratie is ingesteld, vereisen doorgaans de aandacht van een beheerder. U kunt deze fouten bekijken op de pagina **Synchronisatiefouten bij integratie**. Voorbeelden van enkele typische problemen zijn:  
  
* De machtigingen en rollen die aan gebruikers zijn toegewezen, zijn niet correct.  
* Het beheerdersaccount is opgegeven als de integratiegebruiker.  
* Het wachtwoord van de integratiegebruiker is ingesteld om een wijziging te vereisen wanneer de gebruiker zich aanmeldt.  
* De wisselkoersen voor valuta's zijn niet opgegeven in de ene of de andere app.  
  
U moet de fouten handmatig oplossen, maar er zijn een paar manieren waarop de pagina u helpt. Voorbeeld:  

* De velden **Bron** en **Bestemming** kunnen koppelingen bevatten naar de rij waar de fout is gevonden. Klik op de link om de fout te onderzoeken.  
* De acties **Posten ouder dan 7 dagen verwijderen** en **Alle items verwijderen** schonen de lijst op. Meestal gebruikt u deze acties nadat u de oorzaak van een fout hebt opgelost die van invloed is op veel records. Wees echter voorzichtig. Met deze acties kunnen fouten worden verwijderd die nog steeds relevant zijn.

Soms kunnen de tijdstempels in records conflicten veroorzaken. De tabel 'CDS-integratierecord' bevat de tijdstempels 'Laatste synchronisatie gewijzigd op' en 'Laatste synchr. CDS gewijzigd op' voor de laatste integratie in beide richtingen voor een rij. Deze tijdstempels worden vergeleken met tijdstempels in Business Central- en Sales-records. In Business Central staat de tijdstempel in de tabel Integratierecord.

U kunt filteren op records die moeten worden gesynchroniseerd door de tijdstempels van rijen te vergelijken in de tabel 'Toewijzing van integratietabel', namelijk de velden 'Filter synchr. gewijzigd op' en 'Filter synchr. int.-tbl gewijz. op fltr.'.

Het conflictfoutbericht 'Kan de klantrecord niet bijwerken omdat deze een latere wijzigingsdatum heeft dan de accountrecord' of "Kan de accountrecord niet bijwerken omdat deze een latere wijzigingsdatum heeft dan de klantrecord' kan optreden als een rij een tijdstempel heeft dat groter is dan Toewijzing van integratietabel.'Filter synchr. gewijzigd op' maar niet recenter is dan het tijdstempel in Verkoopintegratierecord. Dit betekent dat de bronrij handmatig is gesynchroniseerd, niet door de taakwachtrijpost. 

Het conflict treedt op omdat de doelrij ook is gewijzigd: het tijdstempel van de rij is recenter dan het tijdstempel van Verkoopintegratierecord. De bestemmingscontrole vindt alleen plaats voor bidirectionele tabellen. 

Deze records worden nu verplaatst naar de pagina 'Overgeslagen synchronisatierecords', die u opent vanaf de pagina Microsoft Dynamics-verbinding instellen in Business Central. Daar kunt u opgeven welke wijzigingen moeten worden bewaard en vervolgens de records opnieuw synchroniseren.

## <a name="remove-couplings-between-records"></a>Koppelingen tussen records verwijderen
Als er iets misgaat in uw integratie en u records moet ontkoppelen om ze niet meer te laten synchroniseren, kunt u dit voor één of meer records tegelijk doen. U kunt een of meer records loskoppelen van lijstpagina's of de pagina **Fouten met gekoppelde gegevenssynchronisatie** door een of meer regels te kiezen en **Koppeling verwijderen** te kiezen. U kunt ook alle koppelingen verwijderen voor een of meer tabeltoewijzingen op de pagina **Integratietabeltoewijzingen**. 

## <a name="see-also"></a>Zie ook
[Integreren met Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gebruikersaccounts instellen voor integratie met Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)  
[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]