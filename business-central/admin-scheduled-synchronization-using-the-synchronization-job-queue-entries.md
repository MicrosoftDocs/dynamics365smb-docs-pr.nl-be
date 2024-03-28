---
title: Business Central en Dataverse synchroniseren
description: Leer over het synchroniseren van gegevens tussen Business Central en Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.service: dynamics-365-business-central
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Een synchronisatie plannen tussen Business Central en Dataverse

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] met [!INCLUDE[cds_long_md](includes/cds_long_md.md)] synchroniseren met geplande intervallen door taken in te stellen in de taakwachtrij. De synchronisatietaken synchroniseren gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]-records en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-records die zijn gekoppeld. Voor records die niet al zijn gekoppeld kunnen de synchronisatietaken, afhankelijk van de synchronisatierichting en -regels, nieuwe records maken en koppelen in het doelsysteem.

Er zijn verschillende synchronisatietaken die kant-en-klaar beschikbaar zijn. De taken worden uitgevoerd in de volgende volgorde om koppelingsafhankelijkheden tussen tabellen te voorkomen. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

1. VALUTA - Common Data Service-synchronisatietaak.
2. LEVERANCIER - Common Data Service-synchronisatietaak.
3. CONTACT - Common Data Service-synchronisatietaak.
4. KLANT - Common Data Service-synchronisatietaak.
5. VERKOPERS - Common Data Service-synchronisatietaak.

U kunt de taken op de pagina **Taakwachtrijposten** bekijken. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Standaardsynchronisatieposten in de taakwachtrij

De volgende tabel beschrijft de standaardsynchronisatietaken voor [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Taakwachtrij-item | Omschrijving | Richting | Toewijzing van integratietabel | Standaardsynchronisatiefrequentie (minuten) | Standaardinactiviteitslaaptijd (minuten) |
|--|--|--|--|--|--|--|
| CONTACT - Common Data Service-synchronisatietaak | Synchroniseert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-contacten met [!INCLUDE[prod_short](includes/prod_short.md)]-contacten. | Bidirectioneel | CONTACT | 30 | 720 <br>(12 uur) |
| VALUTA - Common Data Service-synchronisatietaak | Synchroniseert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-transactievaluta's met [!INCLUDE[prod_short](includes/prod_short.md)]-valuta's. | Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | VALUTA | 30 | 720 <br> (12 uur) |
| KLANT - Common Data Service-synchronisatietaak | Synchroniseert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-accounts met [!INCLUDE[prod_short](includes/prod_short.md)]-klanten. | Bidirectioneel | KLANT | 30 | 720<br> (12 uur) |
| LEVERANCIER - Common Data Service-synchronisatietaak | Synchroniseert [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-accounts met [!INCLUDE[prod_short](includes/prod_short.md)]-klanten. | Bidirectioneel | LEVERANCIER | 30 | 720<br> (12 uur) |
| VERKOPERS - Common Data Service-synchronisatietaak | Synchroniseert [!INCLUDE[prod_short](includes/prod_short.md)]-verkopers met [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-gebruikers. | Van [!INCLUDE[cds_long_md](includes/cds_long_md.md)] naar [!INCLUDE[prod_short](includes/prod_short.md)] | VERKOPERS | 30 | 1440<br> (24 uur) |

## <a name="synchronization-process"></a>Synchronisatieproces

Elke synchronisatietaakwachtrijpost gebruikt een bepaalde integratietabeltoewijzing die aangeeft welke [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel moet worden gesynchroniseerd. De tabeltoewijzingen bevatten ook instellingen die bepalen welke records in de [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel moeten worden gesynchroniseerd.  

Om gegevens te synchroniseren moeten [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabelrecords worden gekoppeld aan [!INCLUDE[prod_short](includes/prod_short.md)]-records. Een [!INCLUDE[prod_short](includes/prod_short.md)]-klant moet bijvoorbeeld zijn gekoppeld aan een [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-account. U kunt koppelingen handmatig instellen, voordat u de synchronisatietaken uitvoert, of u kunt de synchronisatietaken de koppelingen automatisch laten instellen. De volgende lijst beschrijft hoe gegevens tussen [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)] worden gesynchroniseerd wanneer u de synchronisatietaakwachtrijposten gebruikt. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md).

- Het selectievakje **Alleen gekoppelde records synchr.** bepaalt of nieuwe records worden gemaakt wanneer u synchroniseert. Standaard is het selectievakje ingeschakeld, wat betekent dat alleen gekoppelde records worden gesynchroniseerd. In de toewijzing van de integratietabel kunt u de tabeltoewijzing tussen een [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel en een [!INCLUDE[prod_short](includes/prod_short.md)]-tabel wijzigen, zodat de integratiesynchronisatietaken nieuwe records in de doeldatabase maken voor elke rij in de brondatabase die niet is gekoppeld. Zie voor meer informatie [Nieuwe records maken](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Voorbeeld** Als u het selectievakje **Alleen gekoppelde records synchr.** uitschakelt wanneer u klanten synchroniseert in [!INCLUDE[prod_short](includes/prod_short.md)] met accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)], wordt voor elke klant een nieuw account aangemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] en automatisch gekoppeld. Omdat de synchronisatie in dit geval tweerichting is, wordt bovendien een nieuwe klant gemaakt en gekoppeld voor elk [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-account dat niet al is gekoppeld.  

    > [!NOTE]  
    > Er zijn extra regels en filters waarmee wordt bepaald welke gegevens worden gesynchroniseerd. Ga voor meer informatie naar [Synchronisatieregels](admin-synchronizing-business-central-and-sales.md).

- Als nieuwe records worden gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)], gebruiken de records de sjabloon die is gedefinieerd voor de integratietabeltoewijzing of de standaardsjabloon die beschikbaar is voor het rijtype. Velden worden gevuld met gegevens uit [!INCLUDE[prod_short](includes/prod_short.md)] of [!INCLUDE[cds_long_md](includes/cds_long_md.md)], afhankelijk van de synchronisatierichting. Zie voor meer informatie [Tabeltoewijzingen wijzigen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Bij volgende synchronisaties worden alleen records die zijn gewijzigd of toegevoegd na de laatste succesvolle synchronisatietaak voor de tabel, bijgewerkt.  

     Nieuwe records in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] worden toegevoegd in [!INCLUDE[prod_short](includes/prod_short.md)]. Als gegevens in velden in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-records zijn gewijzigd, worden de gegevens gekopieerd naar het overeenkomende veld in [!INCLUDE[prod_short](includes/prod_short.md)].  

- Met tweerichtingssynchronisatie synchroniseert de taak van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en vervolgens van [!INCLUDE[cds_long_md](includes/cds_long_md.md)] naar [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>Over inactiviteittime-outs

Sommige taakwachtrij-items, zoals die waarbij synchronisatie wordt gepland tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[cds_long_md](includes/cds_long_md.md)], gebruiken het veld **Time-out inactiviteit** op de pagina **Taakwachtrij-item** om te voorkomen dat het taakwachtrij-item onnodig wordt uitgevoerd.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Stroomdiagram voor wanneer taakwachtrij-items in de wacht worden gezet vanwege inactiviteit.":::

Wanneer de waarde in dit veld niet nul is en de taakwachtrij geen wijzigingen heeft gevonden tijdens de laatste run, zet [!INCLUDE[prod_short](includes/prod_short.md)] het taakwachtrij-item in de wacht. Wanneer dat gebeurt, bevat het veld **Status van taakwachtrij** **Afwachten vanwege inactiviteit** en wacht [!INCLUDE[prod_short](includes/prod_short.md)] gedurende de periode die is gespecificeerd in het veld **Time-out inactiviteit** voordat het taakwachtrij-item opnieuw wordt uitgevoerd.  

Standaard zoekt het taakwachtrij-item VALUTA, dat valuta's in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] synchroniseert met wisselkoersen in [!INCLUDE[prod_short](includes/prod_short.md)], elke 30 minuten naar wijzigingen in wisselkoersen. Als er geen wijzigingen worden gevonden, zet [!INCLUDE[prod_short](includes/prod_short.md)] het taakwachtrij-item VALUTA gedurende 720 minuten (zes uur) in de wacht. Als een wisselkoers wordt gewijzigd in [!INCLUDE[prod_short](includes/prod_short.md)] terwijl het taakwachtrij-item in de wacht staat, activeert [!INCLUDE[prod_short](includes/prod_short.md)] automatisch het taakwachtrij-item en wordt de taakwachtrij opnieuw gestart. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] activeert automatisch taakwachtrij-items die in de wacht staan, alleen als er wijzigingen plaatsvinden in [!INCLUDE[prod_short](includes/prod_short.md)]. Veranderingen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] activeren geen taakwachtrij-items.

## <a name="to-view-the-synchronization-job-log"></a>Logboek met synchronisatietaken weergeven

1. Kies het pictogram :::image type="icon" source="media/ui-search/search_small.png" border="false":::, voer **Logboek van integratiesynchronisatie** in en kies vervolgens de gerelateerde koppeling.
2. Als een of meer fouten zijn opgetreden voor een synchronisatietaak, wordt het aantal fouten weergegeven in de kolom **Mislukt**. Als u de fouten voor de taak wilt weergeven, kiest u het nummer.  

    > [!TIP]  
    > U kunt alle fouten van de synchronisatietaak weergeven door het logboek van de synchronisatietaak direct te openen.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Het logboek van de synchronisatietaak weergeven vanuit tabeltoewijzingen

1. Kies het pictogram :::image type="icon" source="media/ui-search/search_small.png" border="false":::, voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Toewijzingen van integratietabellen** een post en kies **Logbestand integratiesynchronisatietaak**.  

## <a name="to-view-the-synchronization-error-log"></a>Logboek met synchronisatiefouten weergeven

- Kies het pictogram :::image type="icon" source="media/ui-search/search_small.png" border="false":::, voer **Synchronisatiefouten bij integratie** in en kies vervolgens de gerelateerde koppeling.

## <a name="see-also"></a>Zie ook

[Gegevens synchroniseren in Business Central en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Handmatig tabeltoewijzingen synchroniseren](admin-manual-synchronization-of-table-mappings.md)  
[Een synchronisatie plannen tussen Business Central en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Over integratie van Dynamics 365 Business Central met [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
