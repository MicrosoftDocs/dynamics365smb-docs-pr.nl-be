---
title: Problemen met synchronisatiefouten oplossen
description: Dit onderwerp biedt enige begeleiding voor het identificeren en oplossen van synchronisatieproblemen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="troubleshooting-synchronization-errors"></a>Problemen met synchronisatiefouten oplossen


Er zijn veel factoren betrokken bij de integratie van [!INCLUDE[prod_short](includes/prod_short.md)] met [!INCLUDE[prod_short](includes/cds_long_md.md)]en soms gaat het mis. In dit onderwerp worden enkele van de veel voorkomende fouten beschreven en worden enkele tips gegeven voor het oplossen van deze fouten.

Fouten komen vaak voor als gevolg van iets wat een gebruiker heeft gedaan met gekoppelde records of er is iets mis met de manier waarop de integratie is ingesteld. Fouten met betrekking tot gekoppelde records kunnen gebruikers zelf oplossen. Deze fouten worden veroorzaakt door acties zoals het verwijderen van gegevens in één, maar niet beide, zakelijke apps en vervolgens synchroniseren. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),

Fouten die gerelateerd zijn aan hoe de integratie is ingesteld, vereisen doorgaans de aandacht van een beheerder. U kunt deze fouten bekijken op de pagina **Synchronisatiefouten bij integratie**. 

De volgende tabel bevat voorbeelden van typische problemen:  

|Verzenden  |Oplossing  |
|---------|---------|
|De machtigingen en rollen die aan de integratiegebruiker zijn toegewezen, zijn niet correct. | Deze fout komt uit [!INCLUDE[prod_short](includes/cds_long_md.md)] en bevat vaak de volgende tekst "Hoofdgebruiker (Id=\<user id>, type=8) heeft geen machtiging \<privilegeName>". Deze fout treedt op omdat de integratiegebruiker een machtiging niet heeft die toegang geeft tot een entiteit. Meestal treedt deze fout op als u aangepaste entiteiten synchroniseert of als u een app hebt geïnstalleerd in [!INCLUDE[prod_short](includes/cds_long_md.md)] waarvoor toestemming is vereist om toegang te krijgen tot andere [!INCLUDE[prod_short](includes/cds_long_md.md)]-entiteiten. Om deze fout op te lossen wijst u de machtiging toe aan de integratiegebruiker in [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> U vindt de naam van de integratiegebruiker op de pagina **Dataverse-verbinding instellen**. Het foutbericht bevat de naam van de machtiging, waarmee u de entiteit kunt identificeren waarvoor u een machtiging nodig hebt. Om de ontbrekende machtiging toe te voegen logt u in op [!INCLUDE[prod_short](includes/cds_long_md.md)] met een beheerdersaccount en bewerkt u de beveiligingsrol die aan de integratiegebruiker is toegewezen. Zie voor meer informatie [Een beveiligingsrol maken of bewerken om toegang te beheren](/power-platform/admin/create-edit-security-role). |
|U koppelt een record die een andere record gebruikt die niet is gekoppeld. Bijvoorbeeld een klant van wie de valuta niet is gekoppeld of een artikel waarvoor de eenheid niet is gekoppeld. | U moet eerst de afhankelijke record koppelen, bijvoorbeeld een valuta of eenheid, en vervolgens de koppeling opnieuw proberen. |

Hieronder volgen enkele hulpprogramma's op de pagina Synchronisatiefouten bij integratie die u kunnen helpen deze problemen handmatig op te lossen.  

* De velden **Bron** en **Bestemming** kunnen koppelingen bevatten naar de rij waar de fout is gevonden. Klik op de link om de fout te onderzoeken.  
* De acties **Posten ouder dan 7 dagen verwijderen** en **Alle items verwijderen** schonen de lijst op. Meestal gebruikt u deze acties nadat u de oorzaak van een fout hebt opgelost die van invloed is op veel records. Wees echter voorzichtig. Met deze acties kunnen fouten worden verwijderd die nog steeds relevant zijn.
* De actie **Foutaanroepstack weergeven** toont informatie die kan helpen bij het identificeren van de oorzaak van de fout. Als u de fout niet zelf kunt oplossen en u besluit een ondersteuningsverzoek in te dienen, neem dan de informatie op in het ondersteuningsverzoek.

## <a name="see-also"></a>Zie ook
[Integreren met Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gebruikersaccounts instellen voor integratie met Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md)  
[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
