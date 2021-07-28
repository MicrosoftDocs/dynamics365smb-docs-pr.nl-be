---
title: Taken plannen voor automatische uitvoering
description: Geplande taken worden beheerd door de taakwachtrij. Met deze taken worden rapporten en codeunits uitgevoerd. U kunt taken éénmalig of herhaaldelijk uitvoeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b1d9893364d7472759a478877ebec49ace5e9647
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441305"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Gebruik van taakwachtrijen om taken te plannen

Met taakwachtrijen in [!INCLUDE[prod_short](includes/prod_short.md)] kunnen gebruikers specifieke rapporten en codeunits plannen en uitvoeren. U kunt taken éénmalig of herhaaldelijk uitvoeren. U kunt bijvoorbeeld het rapport **Verkoper * Verkoopstatistieken** wekelijks uitvoeren om de verkopen per verkoper elke week bij te houden of u kunt de codeunit **Goedkeuringsaanvragen delegeren** dagelijks uitvoeren om te voorkomen dat documenten zich opstapelen of anderszins de werkstroom blokkeren.

Op de pagina **Taakwachtrijposten** worden alle bestaande posten weergegeven. Als u een nieuwe taakwachtrijpost toevoegt die u wilt plannen, moet u informatie opgeven over het objecttype dat u wilt uitvoeren, zoals een rapport of codeunit, en de naam en id van het object opgeven dat u wilt uitvoeren. U kunt ook parameters toevoegen om het gedrag van de taakwachtrijpost te specificeren. Zo kunt u een parameter toevoegen om alleen geboekte verkooporders te verzenden. U moet zijn gemachtigd om het betreffende rapport of de betreffende code-unit uit te voeren, want anders wordt een fout geretourneerd wanneer de verwerkingswachtrij wordt uitgevoerd.  
> [!IMPORTANT]  
> Als u de machtigingenset SUPER gebruikt die wordt geleverd met [!INCLUDE[prod_short](includes/prod_short.md)], hebben u en uw gebruikers de machtiging om alle objecten uit te voeren binnen de licentie. Dat is nog steeds niet genoeg voor gedelegeerde beheerders of gebruikers met een apparaatlicentie, die geen taakwachtrij-items kunnen maken.

Een taakwachtrij kan veel posten bevatten, die de taken vormen die door de wachtrij worden beheerd en uitgevoerd. Informatie in de post geeft aan welke code-unit of welk rapport wordt uitgevoerd, wanneer en hoe vaak de post wordt uitgevoerd, in welke categorie de taak wordt uitgevoerd en hoe deze wordt uitgevoerd.  

Nadat taakwachtrijen zijn ingesteld en werken, kan de status als volgt veranderen in elke doorlopende periode:

* **Afwachten**  
* **Gereed**  
* **In verwerking**  
* **Fout**  
* **Gereedgemeld**  

Nadat een taak is voltooid, wordt deze verwijderd uit de lijst met taakwachtrijposten, tenzij het een terugkerende taak is. Als het een terugkerende taak is, wordt het veld **Vroegste begintijd** aangepast, zodat het de volgende keer weergeeft dat de taak naar verwachting wordt uitgevoerd.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Status of fouten in de taakwachtrij weergeven

Gegevens die worden gegenereerd wanneer een taakwachtrij wordt uitgevoerd, worden opgeslagen in de database, zodat u taakwachtrijfouten kunt oplossen.  
Voor elk item in de wachtrij kunt u de status bekijken en wijzigen. Wanneer u een taakwachtrij-item maakt, wordt de status ingesteld op **Afwachten**. U kunt de status bijvoorbeeld instellen op **Klaar** en weer op **Afwachten**. Als u dat niet doet, wordt statusinformatie automatisch bijgewerkt.

De volgende tabel beschrijft de waarden van het veld **Status**.

| Status | Omschrijving |
|--|--|
| Gereed | Geeft aan dat de taakwachtrijpost klaar is om te worden uitgevoerd. |
| In verwerking | Geeft aan dat de taakwachtrijpost wordt verwerkt. Dit veld wordt bijgewerkt terwijl de taakwachtrij wordt uitgevoerd. |
| Wachten | Standaard. Geeft de status van de taakwachtrijpost aan wanneer deze wordt gemaakt. Kies de actie **Status instellen op Gereed** om de status te wijzigen in **Gereed**. Kies de actie **Instellen op afwachten** of **Onderbreken** om de status te wijzigen in **Afwachten**. |
| Fout | Geeft aan dat er een fout is. Kies **Fout weergeven** om het foutbericht weer te geven. |
| Gereedgemeld | Geeft aan dat de taakwachtrijpost is voltooid. |

### <a name="to-view-status-for-any-job"></a>De status voor een taak weergeven
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Taakwachtrijposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Taakwachtrijposten** een taakwachtrijpost en kies vervolgens de actie **Logboekvermeldingen**.  

> [!TIP]
> Met [!INCLUDE [prod_short](includes/prod_short.md)] online kunt u ook de status van taakwachtrijposten bekijken met Application Insights in Microsoft Azure. Zie voor meer informatie [Traceringstelemetrie van levenscyclus van taakwachtrij analyseren](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) in de [!INCLUDE [prod_short](includes/prod_short.md)] Help voor ontwikkelaars en beheerders.

## <a name="the-my-job-queue-part"></a>Het onderdeel Mijn taakwachtrij
In het onderdeel **Mijn taakwachtrij** in uw rolcentrum worden de taakwachtrijposten weergegeven die u hebt gestart, maar die nog niet zijn voltooid. Standaard is het onderdeel niet zichtbaar, zodat u het moet toevoegen aan uw rolcentrum. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.  

Dit onderdeel toont welke documenten met uw id in het veld **Toegewezen gebruikers-id** worden verwerkt of in de wachtrij staan, inclusief posten die verband houden met boeking op de achtergrond. Het onderdeel kan u in één oogopslag laten zien of er een fout is opgetreden bij het boeken van een document en of er fouten zijn opgetreden in een taakwachtrijpost. Met het onderdeel kunt u een documentboeking annuleren als deze niet wordt uitgevoerd.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Een fout in het gedeelte Mijn taakwachtrij weergeven
1. Kies in een post met de status **Fout** de actie **Fout weergeven**.
2. Bekijk de foutmelding en los het probleem op.


## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Voorbeelden van wat kan worden gepland met behulp van een taakwachtrij

### <a name="schedule-reports"></a>Rapporten plannen

U kunt een rapport plannen voor uitvoering op een bepaalde datum en tijd. Geplande rapporten en batchtaken worden in de verwerkingswachtrij ingevoerd en verwerkt op het geplande tijdstip, net zoals andere taken. U kiest de optie **Schema** nadat u de actie **Verzenden naar** hebt gekozen en voert vervolgens informatie in zoals de printer, de tijd en datum en de herhaling.  

Zie voor meer informatie [Een rapport plannen voor uitvoering](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Synchronisatie plannen tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)]

Als u [!INCLUDE[prod_short](includes/prod_short.md)] hebt geïntegreerd met [!INCLUDE[prod_short](includes/cds_long_md.md)], kunt u de taakwachtrij gebruiken om te plannen wanneer u gegevens wilt synchroniseren voor de records die u in de twee zakelijke apps hebt gekoppeld. Afhankelijk van de richting en regels die u hebt gedefinieerd voor de integratie, kunnen de synchronisatietaken ook nieuwe records maken in de doel-app die overeenkomen met die in de bron. Als een verkoper bijvoorbeeld een nieuw contact maakt in [!INCLUDE[crm_md](includes/crm_md.md)], kan de synchronisatietaak dat contact maken voor de gekoppelde verkoper in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Een synchronisatie plannen tussen Business Central en Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md) voor meer informatie.

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Het boeken van verkoop- en inkooporders plannen

Taakwachtrijen zijn een effectief hulpmiddel om de uitvoering van bedrijfsprocessen op de achtergrond te plannen, zoals wanneer meerdere gebruikers proberen verkooporders te boeken, maar er slechts één order tegelijk kan worden verwerkt.  

Zie voor meer informatie [Boeking op de achtergrond instellen met taakwachtrijen](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## <a name="see-also"></a>Zie ook

[Beheer](admin-setup-and-administration.md)  
[Business Central instellen](setup.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Traceringstelemetrie van levenscyclus van taakwachtrij analyseren](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]