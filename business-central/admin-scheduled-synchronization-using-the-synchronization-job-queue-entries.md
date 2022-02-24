---
title: Business Central en Dynamics 365 Sales synchroniseren | Microsoft Docs
description: Leer over het synchroniseren van gegevens tussen Business Central en Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 4b6137f6d5fa057d801a1afe30480017ceadd1c8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879094"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Een synchronisatie plannen tussen Business Central en Dynamics 365 Sales
U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren met geplande intervallen door taken in te stellen in de taakwachtrij. De synchronisatietaken synchroniseren gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en [!INCLUDE[crm_md](includes/crm_md.md)]-records die eerder zijn gekoppeld. Of voor records die niet al zijn gekoppeld kunnen de synchronisatietaken, afhankelijk van de synchronisatierichting en -regels, nieuwe records maken en koppelen in het doelsysteem. Er zijn verschillende synchronisatietaken die kant-en-klaar beschikbaar zijn. U kunt ze op de pagina **Taakwachtrijposten** weergeven. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.-->

## <a name="synchronization-process"></a>Synchronisatieproces  
Elke synchronisatietaakwachtrijpost gebruikt een bepaalde integratietabeltoewijzing die aangeeft welke [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit moet worden gesynchroniseerd. De tabeltoewijzingen bevatten ook instellingen die bepalen welke records in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en de [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit moeten worden gesynchroniseerd.  

Om gegevens te synchroniseren moeten [!INCLUDE[crm_md](includes/crm_md.md)]-entiteitrecords worden gekoppeld aan [!INCLUDE[d365fin](includes/d365fin_md.md)]-records. Een [!INCLUDE[d365fin](includes/d365fin_md.md)]-klant moet bijvoorbeeld zijn gekoppeld aan een [!INCLUDE[crm_md](includes/crm_md.md)]-account. U kunt koppelingen handmatig instellen, voordat u de synchronisatietaken uitvoert, of u kunt de synchronisatietaken de koppelingen automatisch laten instellen. De volgende lijst beschrijft hoe gegevens tussen [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)] worden gesynchroniseerd wanneer u de synchronisatietaakwachtrijposten gebruikt. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md).

-   Het selectievakje **Alleen gekoppelde records synchr.** bepaalt of nieuwe records worden gemaakt wanneer u synchroniseert. Standaard is het selectievakje ingeschakeld, wat betekent dat alleen gekoppelde records worden gesynchroniseerd. In de toewijzing van de integratietabel kunt u de tabeltoewijzing tussen een [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit en een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel wijzigen, zodat de integratiesynchronisatietaken nieuwe records in de doeldatabase maken voor elke record in de brondatabase die niet is gekoppeld. Zie voor meer informatie [Nieuwe records maken](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Voorbeeld** Als u het selectievakje **Alleen gekoppelde records synchr.** uitschakelt wanneer u klanten synchroniseert in [!INCLUDE[d365fin](includes/d365fin_md.md)] met accounts in [!INCLUDE[crm_md](includes/crm_md.md)], wordt voor elke klant een nieuw account aangemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)] en automatisch gekoppeld. Omdat de synchronisatie in dit geval tweerichting is, wordt bovendien een nieuwe klant gemaakt en gekoppeld voor elk [!INCLUDE[crm_md](includes/crm_md.md)]-account dat niet al is gekoppeld.  

    > [!NOTE]  
    > Er zijn extra regels en filters waarmee wordt bepaald welke gegevens worden gesynchroniseerd. Zie voor meer informatie [Synchronisatieregels](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Als nieuwe records worden gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)], gebruiken de records de sjabloon die is gedefinieerd voor de integratietabeltoewijzing of de standaardsjabloon die beschikbaar is voor het recordtype. Velden worden gevuld met gegevens uit [!INCLUDE[d365fin](includes/d365fin_md.md)] of [!INCLUDE[crm_md](includes/crm_md.md)], afhankelijk van de synchronisatierichting. Zie voor meer informatie [Tabeltoewijzingen wijzigen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Bij volgende synchronisaties worden alleen records die zijn gewijzigd of toegevoegd na de laatste succesvolle synchronisatietaak voor de entiteit, bijgewerkt.  

     Nieuwe records in [!INCLUDE[crm_md](includes/crm_md.md)] worden toegevoegd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als gegevens in velden in [!INCLUDE[crm_md](includes/crm_md.md)]-records zijn gewijzigd, worden de gegevens gekopieerd naar het overeenkomende veld in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Met tweerichtingssynchronisatie synchroniseert de taak van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)] en vervolgens van [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Standaardsynchronisatieposten in de taakwachtrij  
De volgende tabel beschrijft de standaardsynchronisatietaken.  

|Taakwachtrij-item|Omschrijving|Richting|Toewijzing van integratietabel|Standaardsynchronisatiefrequentie (minuten)|Standaardinactiviteitslaaptijd (minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|CONTACT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-contacten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-contacten.|Bidirectioneel|CONTACT|30|720 <br>(12 uur)| 
|VALUTA - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-transactievaluta's met [!INCLUDE[d365fin](includes/d365fin_md.md)]-valuta's.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|VALUTA|30|720 <br> (12 uur)| 
|KLANT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-accounts met [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten.|Bidirectioneel|KLANT|30|720<br> (12 uur)|
|KLANTENPRIJSGROEPPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-verkoopprijslijsten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-klantenprijsgroepen| |KLANTENPRIJSGROEPEN-VERKOOPPRIJSLIJSTEN|30|1440<br> (24 uur)|
|ARTIKEL - PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-artikelen.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUCT|30|1440<br> (24 uur)|
|GEBOEKTEVERKOOPFACTUUR-FACT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-facturen met [!INCLUDE[d365fin](includes/d365fin_md.md)] geboekte verkoopfacturen.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|FACTUREN-GEBOEKTE VERKOOPFACTUREN|30|1440<br> (24 uur)|
|RESOURCE-PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-resources.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|RESOURCE-PRODUCT|30|720<br> (12 uur)|  
|VERKOPERS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[d365fin](includes/d365fin_md.md)]-verkopers met [!INCLUDE[crm_md](includes/crm_md.md)]-gebruikers.|Van [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)]|VERKOPERS|30|1440<br> (24 uur)|
|VERKOOPPRIJS-PRODUCTPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-productprijzen met [!INCLUDE[d365fin](includes/d365fin_md.md)]-verkoopprijzen.||PRODUCTPRIJS-VERKOOPPRIJS|30|1440<br> (24 uur)|
|MAATEENHEID - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-eenhedengroepen met [!INCLUDE[d365fin](includes/d365fin_md.md)]-maateenheden.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|MAATEENHEID|30|720<br> (12 uur)|  
|Klantstatistieken - Dynamics 365 Sales-synchronisatie|Werkt [!INCLUDE[crm_md](includes/crm_md.md)]-rekeningen bij met de recentste [!INCLUDE[d365fin](includes/d365fin_md.md)]-klantgegevens In [!INCLUDE[crm_md](includes/crm_md.md)] wordt deze informatie in het snelle weergaveformulier **Statistiek van Business Central-account** weergegeven van accounts die zijn gekoppeld aan [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten.<br /><br /> Deze gegevens kunnen ook handmatig worden bijgewerkt vanuit van elke klantrecord. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Opmerking:** Dit taakwachtrij-item is alleen van belang als de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Over de Business Central-integratieoplossing](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Niet van toepassing|Niet van toepassing|30|Niet van toepassing|   

## <a name="about-inactivity-timeouts"></a>Over inactiviteittime-outs
Sommige taakwachtrij-items, zoals die waarbij synchronisatie tussen wordt gepland tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)], gebruiken het veld **Time-out inactiviteit** op de taakwachtrij-itemkaart om te voorkomen dat het taakwachtrij-item onnodig wordt uitgevoerd.  
<br><br>

> ![Stroomdiagram voor wanneer taakwachtrij-items in de wacht worden gezet vanwege inactiviteit.](media/on-hold-with-inactivity-timeout.png)

Wanneer de waarde in dit veld niet nul is en de taakwachtrij geen wijzigingen heeft gevonden tijdens de laatste run, zet [!INCLUDE[d365fin](includes/d365fin_md.md)] het taakwachtrij-item in de wacht. Wanneer dat gebeurt, bevat het veld **Status van taakwachtrij** **Afwachten vanwege inactiviteit** en wacht [!INCLUDE[d365fin](includes/d365fin_md.md)] gedurende de periode die is gespecificeerd in het veld **Time-out inactiviteit** voordat het taakwachtrij-item opnieuw wordt uitgevoerd. 

Standaard zoekt het taakwachtrij-item VALUTA, dat valuta's in [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseert met wisselkoersen in [!INCLUDE[d365fin](includes/d365fin_md.md)], elke 30 minuten naar wijzigingen in wisselkoersen. Als er geen wijzigingen worden gevonden, zet [!INCLUDE[d365fin](includes/d365fin_md.md)] het taakwachtrij-item VALUTA gedurende 720 minuten (zes uur) in de wacht. Als een wisselkoers wordt gewijzigd in [!INCLUDE[d365fin](includes/d365fin_md.md)] terwijl het taakwachtrij-item in de wacht staat, activeert [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch het taakwachtrij-item en wordt de taakwachtrij opnieuw gestart. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] activeert automatisch taakwachtrij-items die in de wacht staan, alleen als er wijzigingen plaatsvinden in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Veranderingen in [!INCLUDE[crm_md](includes/crm_md.md)] activeren geen taakwachtrij-items.

## <a name="to-view-the-synchronization-job-log"></a>Logboek met synchronisatietaken weergeven  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Logboek van integratiesynchronisatie** in en kies de desbetreffende koppeling.
2.  Als een of meer fouten zijn opgetreden voor een synchronisatietaak, wordt het aantal fouten weergegeven in de kolom **Mislukt**. Als u de fouten voor de taak wilt weergeven, kiest u het nummer.  

    > [!TIP]  
    > U kunt alle fouten van de synchronisatietaak weergeven door het logboek van de synchronisatietaak direct te openen.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Het logboek van de synchronisatietaak weergeven vanuit tabeltoewijzingen  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies de desbetreffende koppeling.
2.  Selecteer op de pagina **Toewijzingen van integratietabellen** een post en kies **Logbestand integratiesynchronisatietaak**.  

## <a name="to-view-the-synchronization-error-log"></a>Logboek met synchronisatiefouten weergeven  
* Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten bij integratie** in en kies de desbetreffende koppeling.

## <a name="see-also"></a>Zie ook  
[Gegevens synchroniseren in Business Central en Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Handmatig tabeltoewijzingen synchroniseren](admin-manual-synchronization-of-table-mappings.md)  
[Een synchronisatie plannen tussen Business Central en Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Over integratie van Dynamics 365 Business Central met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
