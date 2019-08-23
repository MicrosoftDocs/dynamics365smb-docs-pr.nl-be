---
title: Business Central en Dynamics 365 for Sales synchroniseren | Microsoft Docs
description: Leer over het synchroniseren van gegevens tussen Business Central en Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/16/2019
ms.author: bholtorf
ms.openlocfilehash: 9290730bb559d4ac03a437a49ed81b09f3c01853
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755230"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a>Een synchronisatie plannen tussen Business Central en Dynamics 365 for Sales
U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren met geplande intervallen door taken in te stellen in de taakwachtrij. De synchronisatietaken synchroniseren gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en [!INCLUDE[crm_md](includes/crm_md.md)]-records die eerder zijn gekoppeld. Of voor records die niet al zijn gekoppeld kunnen de synchronisatietaken, afhankelijk van de synchronisatierichting en -regels, nieuwe records maken en koppelen in het doelsysteem. Er zijn verschillende synchronisatietaken die kant-en-klaar beschikbaar zijn. U kunt ze op de pagina **Taakwachtrijposten** weergeven. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Synchronisatieproces  
Elke synchronisatietaakwachtrijpost gebruikt een bepaalde integratietabeltoewijzing die aangeeft welke [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit moet worden gesynchroniseerd. De tabeltoewijzingen bevatten ook instellingen die bepalen welke records in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en de [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit moeten worden gesynchroniseerd.  

Om gegevens te synchroniseren moeten [!INCLUDE[crm_md](includes/crm_md.md)]-entiteitrecords worden gekoppeld aan [!INCLUDE[d365fin](includes/d365fin_md.md)]-records. Een [!INCLUDE[d365fin](includes/d365fin_md.md)]-klant moet bijvoorbeeld zijn gekoppeld aan een [!INCLUDE[crm_md](includes/crm_md.md)]-account. U kunt koppelingen handmatig instellen, voordat u de synchronisatietaken uitvoert, of u kunt de synchronisatietaken de koppelingen automatisch laten instellen. De volgende lijst beschrijft hoe gegevens tussen [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)] worden gesynchroniseerd wanneer u de synchronisatietaakwachtrijposten gebruikt. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Standaard worden alleen records in [!INCLUDE[d365fin](includes/d365fin_md.md)] die zijn gekoppeld aan records in [!INCLUDE[crm_md](includes/crm_md.md)] gesynchroniseerd. U kunt de tabeltoewijzing tussen een [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit en een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel wijzigen, zodat de integratiesynchronisatietaken nieuwe records in de doeldatabase maken voor elke record in de brondatabase die niet is gekoppeld. De nieuwe records worden ook gekoppeld aan de bijbehorende records in de bron. Wanneer u bijvoorbeeld klanten synchroniseert met [!INCLUDE[crm_md](includes/crm_md.md)]-rekeningen, wordt een nieuwe accountrecord gemaakt voor elke klant in [!INCLUDE[d365fin](includes/d365fin_md.md)]. De nieuwe accounts worden automatisch gekoppeld aan klanten in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Omdat de synchronisatie in dit geval tweerichting is, wordt een nieuwe klant gemaakt en gekoppeld voor elke [!INCLUDE[crm_md](includes/crm_md.md)]-account die niet al is gekoppeld.  

    > [!NOTE]  
    > Er zijn extra regels en filters waarmee wordt bepaald welke gegevens worden gesynchroniseerd. Zie voor meer informatie [Synchronisatieregels](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Als nieuwe records worden gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)], gebruiken de records de sjabloon die is gedefinieerd voor de integratietabeltoewijzing of de standaardsjabloon die beschikbaar is voor het recordtype. Velden worden gevuld met gegevens uit [!INCLUDE[d365fin](includes/d365fin_md.md)] of [!INCLUDE[crm_md](includes/crm_md.md)], afhankelijk van de synchronisatierichting. Zie voor meer informatie [Procedure: Tabeltoewijzingen wijzigen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Bij volgende synchronisaties worden alleen records die zijn gewijzigd of toegevoegd na de laatste succesvolle synchronisatietaak voor de entiteit, bijgewerkt.  

     Nieuwe records in [!INCLUDE[crm_md](includes/crm_md.md)] worden toegevoegd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als gegevens in velden in [!INCLUDE[crm_md](includes/crm_md.md)]-records zijn gewijzigd, worden de gegevens gekopieerd naar het overeenkomende veld in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Met tweerichtingssynchronisatie synchroniseert de taak van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)] en vervolgens van [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Standaardsynchronisatieposten in de taakwachtrij  
De volgende tabel beschrijft de standaardsynchronisatietaken.  

|Taakwachtrij-item|Omschrijving|Richting|Toewijzing van integratietabel|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|CONTACT - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-contacten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-contacten.|Bidirectioneel|CONTACT|  
|VALUTA - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-transactievaluta's met [!INCLUDE[d365fin](includes/d365fin_md.md)]-valuta's.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|VALUTA|  
|KLANT - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-accounts met [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten.|Bidirectioneel|KLANT|  
|KLANTENPRIJSGROEPPRIJS - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-verkoopprijslijsten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-klantenprijsgroepen| |KLANTENPRIJSGROEPEN-VERKOOPPRIJSLIJSTEN|
|ARTIKEL - PRODUCT - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-artikelen.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUCT|
|GEBOEKTEVERKOOPFACTUUR-FACT - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-facturen met [!INCLUDE[d365fin](includes/d365fin_md.md)] geboekte verkoopfacturen.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|FACTUREN-GEBOEKTE VERKOOPFACTUREN|
|RESOURCE - PRODUCT - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-resources.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|RESOURCE-PRODUCT|  
|VERKOPERS - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[d365fin](includes/d365fin_md.md)]-verkopers met [!INCLUDE[crm_md](includes/crm_md.md)]-gebruikers.|Van [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)]|VERKOPERS|
|VERKOOPPRIJS-PRODUCTPRIJS - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-productprijzen met [!INCLUDE[d365fin](includes/d365fin_md.md)]-verkoopprijzen.||PRODUCTPRIJS-VERKOOPPRIJS|
|MAATEENHEID - Dynamics 365 for Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-eenhedengroepen met [!INCLUDE[d365fin](includes/d365fin_md.md)]-maateenheden.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|MAATEENHEID|  
|Klantstatistiek - Dynamics 365 for Sales-synchronisatie|Werkt [!INCLUDE[crm_md](includes/crm_md.md)]-rekeningen bij met de recentste [!INCLUDE[d365fin](includes/d365fin_md.md)]-klantgegevens In [!INCLUDE[crm_md](includes/crm_md.md)] wordt deze informatie in het snelle weergaveformulier **Statistiek van Business Central-account** weergegeven van accounts die zijn gekoppeld aan [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten.<br /><br /> Deze gegevens kunnen ook handmatig worden bijgewerkt vanuit van elke klantrecord. Zie voor meer informatie [Procedure: Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Opmerking:** Dit taakwachtrij-item is alleen van belang als de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Over de Business Central-integratieoplossing](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Niet van toepassing.|Niet van toepassing.|   

## <a name="to-view-the-synchronization-job-log"></a>Logboek met synchronisatietaken weergeven  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Logboek van integratiesynchronisatie** in en kies vervolgens de gerelateerde koppeling.
2.  Als een of meer fouten zijn opgetreden voor een synchronisatietaak, wordt het aantal fouten weergegeven in de kolom **Mislukt**. Als u de fouten voor de taak wilt weergeven, kiest u het nummer.  

    > [!TIP]  
    > U kunt alle fouten van de synchronisatietaak weergeven door het logboek van de synchronisatietaak direct te openen.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Het logboek van de synchronisatietaak weergeven vanuit tabeltoewijzingen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.
2.  Selecteer op de pagina **Toewijzingen van integratietabellen** een post en kies **Logbestand integratiesynchronisatietaak**.  

## <a name="to-view-the-synchronization-error-log"></a>Logboek met synchronisatiefouten weergeven  
* Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten bij integratie** in en kies vervolgens de gerelateerde koppeling.

## <a name="see-also"></a>Zie ook  
[Gegevens synchroniseren in Business Central en Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Handmatig tabeltoewijzingen synchroniseren](admin-manual-synchronization-of-table-mappings.md)  
[Een synchronisatie plannen tussen Business Central en Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Over integratie van Dynamics 365 Business Central met Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



