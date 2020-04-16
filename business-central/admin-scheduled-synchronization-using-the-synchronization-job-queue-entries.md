---
title: Business Central en Common Data Service synchroniseren | Microsoft Docs
description: Leer over het synchroniseren van gegevens tussen Business Central en Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cce95930cde316c5e233382effb0bb241b3b79fd
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196603"
---
# <a name="scheduling-a-synchronization-between-business-central-and-common-data-service"></a>Een synchronisatie plannen tussen Business Central en Common Data Service
U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[d365fin](includes/cds_long_md.md)] synchroniseren met geplande intervallen door taken in te stellen in de taakwachtrij. De synchronisatietaken synchroniseren gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en [!INCLUDE[d365fin](includes/cds_long_md.md)]-records die eerder zijn gekoppeld. Of voor records die niet al zijn gekoppeld kunnen de synchronisatietaken, afhankelijk van de synchronisatierichting en -regels, nieuwe records maken en koppelen in het doelsysteem. 

Er zijn verschillende synchronisatietaken die kant-en-klaar beschikbaar zijn. De taken worden uitgevoerd in de volgende volgorde om koppelingsafhankelijkheden tussen entiteiten te voorkomen. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

1. VALUTA - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak.
2. LEVERANCIER - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak. 
3. CONTACT - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak.
4. KLANT - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak.
5. VERKOPERS - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak.

U kunt de taken op de pagina **Taakwachtrijposten** bekijken. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

### <a name="default-synchronization-job-queue-entries"></a>Standaardsynchronisatieposten in de taakwachtrij  
De volgende tabel beschrijft de standaardsynchronisatietaken voor [!INCLUDE[d365fin](includes/cds_long_md.md)].  

|Taakwachtrij-item|Omschrijving|Richting|Toewijzing van integratietabel|Standaardsynchronisatiefrequentie (minuten)|Standaardinactiviteitslaaptijd (minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|CONTACT - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak|Synchroniseert [!INCLUDE[d365fin](includes/cds_long_md.md)]-contacten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-contacten.|Bidirectioneel|CONTACT|30|720 <br>(12 uur)| 
|VALUTA - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak|Synchroniseert [!INCLUDE[d365fin](includes/cds_long_md.md)]-transactievaluta's met [!INCLUDE[d365fin](includes/d365fin_md.md)]-valuta's.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[d365fin](includes/cds_long_md.md)]|VALUTA|30|720 <br> (12 uur)| 
|KLANT - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak|Synchroniseert [!INCLUDE[d365fin](includes/cds_long_md.md)]-accounts met [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten.|Bidirectioneel|KLANT|30|720<br> (12 uur)|
|LEVERANCIER - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak|Synchroniseert [!INCLUDE[d365fin](includes/cds_long_md.md)]-accounts met [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten.|Bidirectioneel|LEVERANCIER|30|720<br> (12 uur)|
|VERKOPERS - [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatietaak|Synchroniseert [!INCLUDE[d365fin](includes/d365fin_md.md)]-verkopers met [!INCLUDE[d365fin](includes/cds_long_md.md)]-gebruikers.|Van [!INCLUDE[d365fin](includes/cds_long_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)]|VERKOPERS|30|1440<br> (24 uur)|

## <a name="synchronization-process"></a>Synchronisatieproces  
Elke synchronisatietaakwachtrijpost gebruikt een bepaalde integratietabeltoewijzing die aangeeft welke [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en [!INCLUDE[d365fin](includes/cds_long_md.md)]-entiteit moet worden gesynchroniseerd. De tabeltoewijzingen bevatten ook instellingen die bepalen welke records in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en de [!INCLUDE[d365fin](includes/cds_long_md.md)]-entiteit moeten worden gesynchroniseerd.  

Om gegevens te synchroniseren moeten [!INCLUDE[d365fin](includes/cds_long_md.md)]-entiteitrecords worden gekoppeld aan [!INCLUDE[d365fin](includes/d365fin_md.md)]-records. Een [!INCLUDE[d365fin](includes/d365fin_md.md)]-klant moet bijvoorbeeld zijn gekoppeld aan een [!INCLUDE[d365fin](includes/cds_long_md.md)]-account. U kunt koppelingen handmatig instellen, voordat u de synchronisatietaken uitvoert, of u kunt de synchronisatietaken de koppelingen automatisch laten instellen. De volgende lijst beschrijft hoe gegevens tussen Common Data Service en [!INCLUDE[d365fin](includes/d365fin_md.md)] worden gesynchroniseerd wanneer u de synchronisatietaakwachtrijposten gebruikt. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md).

-   Het selectievakje **Alleen gekoppelde records synchr.** bepaalt of nieuwe records worden gemaakt wanneer u synchroniseert. Standaard is het selectievakje ingeschakeld, wat betekent dat alleen gekoppelde records worden gesynchroniseerd. In de toewijzing van de integratietabel kunt u de tabeltoewijzing tussen een [!INCLUDE[d365fin](includes/cds_long_md.md)]-entiteit en een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel wijzigen, zodat de integratiesynchronisatietaken nieuwe records in de doeldatabase maken voor elke record in de brondatabase die niet is gekoppeld. Zie voor meer informatie [Nieuwe records maken](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Voorbeeld** Als u het selectievakje **Alleen gekoppelde records synchr.** uitschakelt wanneer u klanten synchroniseert in [!INCLUDE[d365fin](includes/d365fin_md.md)] met accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)], wordt voor elke klant een nieuw account aangemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)] en automatisch gekoppeld. Omdat de synchronisatie in dit geval tweerichting is, wordt bovendien een nieuwe klant gemaakt en gekoppeld voor elk [!INCLUDE[d365fin](includes/cds_long_md.md)]-account dat niet al is gekoppeld.  

    > [!NOTE]  
    > Er zijn extra regels en filters waarmee wordt bepaald welke gegevens worden gesynchroniseerd. Zie voor meer informatie [Synchronisatieregels](admin-synchronizing-business-central-and-sales.md).

-   Als nieuwe records worden gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)], gebruiken de records de sjabloon die is gedefinieerd voor de integratietabeltoewijzing of de standaardsjabloon die beschikbaar is voor het recordtype. Velden worden gevuld met gegevens uit [!INCLUDE[d365fin](includes/d365fin_md.md)] of [!INCLUDE[d365fin](includes/cds_long_md.md)], afhankelijk van de synchronisatierichting. Zie voor meer informatie [Tabeltoewijzingen wijzigen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Bij volgende synchronisaties worden alleen records die zijn gewijzigd of toegevoegd na de laatste succesvolle synchronisatietaak voor de entiteit, bijgewerkt.  

     Nieuwe records in [!INCLUDE[d365fin](includes/cds_long_md.md)] worden toegevoegd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als gegevens in velden in [!INCLUDE[d365fin](includes/cds_long_md.md)]-records zijn gewijzigd, worden de gegevens gekopieerd naar het overeenkomende veld in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Met tweerichtingssynchronisatie synchroniseert de taak van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[d365fin](includes/cds_long_md.md)] en vervolgens van [!INCLUDE[d365fin](includes/cds_long_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="about-inactivity-timeouts"></a>Over inactiviteittime-outs
Sommige taakwachtrij-items, zoals die waarbij synchronisatie tussen wordt gepland tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)], gebruiken het veld **Time-out inactiviteit** op de taakwachtrij-itemkaart om te voorkomen dat het taakwachtrij-item onnodig wordt uitgevoerd.  
<br><br>

> ![Stroomdiagram voor wanneer taakwachtrij-items in de wacht worden gezet vanwege inactiviteit.](media/on-hold-with-inactivity-timeout.png)

Wanneer de waarde in dit veld niet nul is en de taakwachtrij geen wijzigingen heeft gevonden tijdens de laatste run, zet [!INCLUDE[d365fin](includes/d365fin_md.md)] het taakwachtrij-item in de wacht. Wanneer dat gebeurt, bevat het veld **Status van taakwachtrij** **Afwachten vanwege inactiviteit** en wacht [!INCLUDE[d365fin](includes/d365fin_md.md)] gedurende de periode die is gespecificeerd in het veld **Time-out inactiviteit** voordat het taakwachtrij-item opnieuw wordt uitgevoerd. 

Standaard zoekt het taakwachtrij-item VALUTA, dat valuta's in [!INCLUDE[d365fin](includes/cds_long_md.md)] synchroniseert met wisselkoersen in [!INCLUDE[d365fin](includes/d365fin_md.md)], elke 30 minuten naar wijzigingen in wisselkoersen. Als er geen wijzigingen worden gevonden, zet [!INCLUDE[d365fin](includes/d365fin_md.md)] het taakwachtrij-item VALUTA gedurende 720 minuten (zes uur) in de wacht. Als een wisselkoers wordt gewijzigd in [!INCLUDE[d365fin](includes/d365fin_md.md)] terwijl het taakwachtrij-item in de wacht staat, activeert [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch het taakwachtrij-item en wordt de taakwachtrij opnieuw gestart. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] activeert automatisch taakwachtrij-items die in de wacht staan, alleen als er wijzigingen plaatsvinden in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Veranderingen in [!INCLUDE[d365fin](includes/cds_long_md.md)] activeren geen taakwachtrij-items.

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
[Gegevens synchroniseren in Business Central en [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Handmatig tabeltoewijzingen synchroniseren](admin-manual-synchronization-of-table-mappings.md)  
[Een synchronisatie plannen tussen Business Central en [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Over integratie van Dynamics 365 Business Central met [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
