---
title: Taken plannen voor automatische uitvoering | Microsoft Docs
description: Geplande taken worden beheerd door de taakwachtrij. Met deze taken worden rapporten en codeunits uitgevoerd. U kunt taken éénmalig of herhaaldelijk uitvoeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 1cf5b75bc63acfa07a90cda1d03f45579a0aa51d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935387"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Gebruik van taakwachtrijen om taken te plannen
Met taakwachtrijen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen gebruikers specifieke rapporten en codeunits plannen en uitvoeren. U kunt taken éénmalig of herhaaldelijk uitvoeren. U kunt bijvoorbeeld het statistiekrapport **Verkoper - Statistiek** wekelijks uitvoeren om de verkopen per verkoper wekelijks bij te houden of u kunt de codeunit **E-mailwachtrij service verwerken** dagelijks uitvoeren om ervoor te zorgen dat niet-verzonden e-mailberichten aan klanten met betrekking tot hun serviceorders tijdig worden verzonden.

Op de pagina **Taakwachtrijposten** worden alle bestaande posten weergegeven. Als u een nieuwe taakwachtrijpost toevoegt die u wilt plannen, moet u informatie opgeven over het objecttype dat u wilt uitvoeren, zoals een rapport of codeunit, en de naam en id van het object opgeven dat u wilt uitvoeren. U kunt ook parameters toevoegen om het gedrag van de taakwachtrijpost te specificeren. Zo kunt u een parameter toevoegen om alleen geboekte verkooporders te verzenden. U moet zijn gemachtigd om het betreffende rapport of de betreffende code-unit uit te voeren, want anders wordt een fout geretourneerd wanneer de verwerkingswachtrij wordt uitgevoerd.  

Een taakwachtrij kan veel posten bevatten, die de taken vormen die door de wachtrij worden beheerd en uitgevoerd. Informatie in de post geeft aan welke code-unit of welk rapport wordt uitgevoerd, wanneer en hoe vaak de post wordt uitgevoerd, in welke categorie de taak wordt uitgevoerd en hoe deze wordt uitgevoerd.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Boeking op de achtergrond instellen met taakwachtrijen
Taakwachtrijen zijn een effectief hulpmiddel om de uitvoering van bedrijfsprocessen op de achtergrond te plannen, zoals wanneer meerdere gebruikers proberen verkooporders te boeken, maar er slechts één order tegelijk kan worden verwerkt. U wilt mogelijk ook boekingen plannen voor tijden die geschikt zijn voor uw organisatie. Het kan bijvoorbeeld zinvol zijn in uw bedrijf bepaalde routines uit te voeren wanneer de meeste van de gegevensinvoer voor de dag is afgesloten.

U kunt dat bereiken door de taakwachtrij in te stellen om diverse batchboekingsrapporten uit te voeren, zoals **Batchboeken verkooporders**, **Batchboeken verkoopfacturen**, **Batchboeken verk.-retourorders** en **Batchboeken verk.-creditnota**. Zie voor meer informatie [Een taakwachtrijpost maken voor boeking van verkooporders op de achtergrond](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt boeken op de achtergrond voor alle verkoop-, inkoop- en servicedocumenten.

In de volgende procedure wordt uitgelegd hoe u achtergrondboeking van verkooporders instelt. De stappen zijn vergelijkbaar voor inkoop en service.  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen van verkoop en tegoeden** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Verkoopinstellingen** het selectievakje **Boeken via taakwachtrij**.
3. Als u wilt filteren op taakwachtrijposten voor boeking van verkooporders, kiest u het veld **Taakwachtrijcategoriecode** en selecteert u vervolgens de categorie **Vrkboeking**.

    Er wordt een taakwachtrijobject, codeunit 88 **Verkoopboeking via taakwachtrij** gemaakt. Schakel het in op de pagina **Taakwachtrijposten**.
4. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Taakwachtrijposten** in en kies vervolgens de gerelateerde koppeling.
5. Kies op de pagina **Taakwachtrijposten** de actie **Nieuw**.
6. Selecteer in het veld **Uit te voeren objecttype** **Codeunit**.  
7. Selecteer in het veld **Uit te voeren object-id** 88, **Verkoopboeking via taakwachtrij**.

    Er zijn geen andere velden van toepassing op dit scenario.
8. Kies de actie **Status instellen op Gereed**.
9. Om te controleren dat de taakwachtrij werkt zoals verwacht, boekt u een verkooporder. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
10. Kijk op de pagina **Logposten taakwachtrij** of de verkooporder met succes is geboekt. Zie voor meer informatie [Status of fouten in de projectwachtrij weergeven](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Als u ook wilt dat verkoopdocumenten worden afgedrukt wanneer deze worden geboekt, schakelt u het selectievakje **Boeken en afdrukken via taakwachtrij** in op de pagina **Verkoopinstellingen**.  

> [!IMPORTANT]  
> Wanneer u een taak voor het boeken en afdrukken van documenten instelt en er op de printer een dialoogvenster wordt weergegeven, zoals een verzoek om aanmeldingsgegevens of een waarschuwing over een laag printerinktniveau, dan wordt het document geboekt, maar niet afgedrukt. De overeenkomstige invoer van de taakwachtrij krijgt uiteindelijk een time-out en het veld **Status** wordt ingesteld op **Fout**. Dienovereenkomstig is het raadzaam dat u geen printerinstellingen gebruikt waarvoor interactie met de weergave van printerdialoogvensters nodig is in combinatie met boeken op de achtergrond.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Een taakwachtrijpost maken voort batchboeking van verkooporders
In de volgende procedure wordt aangegeven hoe u het rapport **Batchboeken verkooporders** instelt om automatisch vrijgegeven verkooporders te boeken om 16:00 uur op werkdagen.  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Taakwachtrijposten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer in het veld **Uit te voeren objecttype** **Rapport**.  
4. Selecteer in het veld **Uit te voeren object-id** 296, **Batchboeken verkooporders**.
5. Selecteer het selectievakje **Rapportaanvraagpagina**.
6. Definieer op de aanvraagpagina **Batchboeken verkooporders** wat er wordt opgenomen tijdens automatische boeking van verkooporders en kies vervolgens de knop **OK**.
7. Selecteer alle selectievakjes van **Uitvoeren op maandagen** tot en met **Uitvoeren op vrijdagen**.
8. Voer in het veld **Begintijd** 4 PM in.
9. Kies de actie **Status instellen op Gereed**.

Verkooporders die gereed zijn om te boeken worden nu elke werkdag om 16:00 uur geboekt.

> [!NOTE]
> Als de taakwachtrij de verkooporder niet kan boeken, wordt de status gewijzigd in **Fout** en wordt de verkooporder toegevoegd aan de lijst met verkooporders die de gebruiker handmatig moet afhandelen. Zie voor meer informatie [Status of fouten in de projectwachtrij weergeven](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Nadat taakwachtrijen zijn ingesteld en werken, kan de status als volgt veranderen in elke doorlopende periode:

* **Afwachten**  
* **Gereed**  
* **In verwerking**  
* **Fout**  
* **Gereedgemeld**  

Nadat een taak is voltooid, wordt deze verwijderd uit de lijst met taakwachtrijposten, tenzij het een terugkerende taak is. Als het een terugkerende taak is, wordt het veld **Vroegste begintijd** aangepast, zodat het de volgende keer weergeeft dat de taak naar verwachting wordt uitgevoerd.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Status of fouten in de taakwachtrij weergeven
Gegevens die worden gegenereerd wanneer een taakwachtrij wordt uitgevoerd, worden opgeslagen in de database, zodat u taakwachtrijfouten kunt oplossen.

### <a name="to-view-status-for-any-job"></a>De status voor een taak weergeven
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Taakwachtrijposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Taakwachtrijposten** een taakwachtrijpost en kies vervolgens de actie **Logboekvermeldingen**.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Een status vanuit een verkoop- of inkoopdocument weergeven
1. Kies vanuit het document dat u hebt geprobeerd te boeken met de taakwachtrij, het veld **Status taakwachtrij**, dat **Fout** bevat.
2. Bekijk de foutmelding en los het probleem op.

## <a name="the-my-job-queue-part"></a>Het onderdeel Mijn taakwachtrij
In het onderdeel **Mijn taakwachtrij** in uw rolcentrum worden de taakwachtrijposten weergegeven die u hebt gestart, maar die nog niet zijn voltooid. Standaard is het onderdeel niet zichtbaar, zodat u het moet toevoegen aan uw rolcentrum. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).  

Dit onderdeel toont welke documenten met uw id in het veld **Toegewezen gebruikers-id** worden verwerkt of in de wachtrij staan, inclusief posten die verband houden met boeking op de achtergrond. Het onderdeel kan u in één oogopslag laten zien of er een fout is opgetreden bij het boeken van een document en of er fouten zijn opgetreden in een taakwachtrijpost. Met het onderdeel kunt u een documentboeking annuleren als deze niet wordt uitgevoerd.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Een fout in het gedeelte Mijn taakwachtrij weergeven
1. Kies in een post met de status **Fout** de actie **Fout weergeven**.
2. Bekijk de foutmelding en los het probleem op.

## <a name="security"></a>Beveiliging  
Taakwachtrijposten worden uitgevoerd op basis van machtigingen. Die machtigingen moeten de uitvoering van de lijst of codeunit toestaan.  

Wanneer een taakwachtrij handmatig is geactiveerd, wordt deze uitgevoerd met de referenties van de gebruiker. Wanneer een taakwachtrij is geactiveerd als een geplande taak, wordt deze uitgevoerd met de referenties van de serverinstantie. Wanneer een taak wordt uitgevoerd, wordt deze uitgevoerd met de referenties van de taakwachtrij die deze activeert. De gebruiker die de taakwachtrijpost maakte, moet echter ook machtigingen hebben. Wanneer een taak wordt uitgevoerd in de gebruikerssessie (bijvoorbeeld bij het boeken op de achtergrond), wordt deze uitgevoerd met de referenties van de gebruiker die deze taak heeft gemaakt.  

> [!IMPORTANT]  
>  Als u de machtigingenset SUPER gebruikt die wordt geleverd met [!INCLUDE[d365fin](includes/d365fin_md.md)], hebben u en uw gebruikers de machtiging om alle objecten uit te voeren. In dit geval wordt de toegang voor elke gebruiker alleen beperkt door machtigingen voor gegevens.  

## <a name="using-job-queues-effectively"></a>Taakwachtrijen efficiënt gebruiken  
De record van de taakwachtrijpost heeft veel velden om de parameters in een codeunit te plaatsen die u hebt opgegeven voor het uitvoeren met een taakwachtrij. Dit betekent ook dat codeunits die moeten worden uitgevoerd via de taakwachtrij, moeten worden gespecificeerd met de taakwachtrijrecord als een parameter in de **OnRun** trigger. Dit biedt een extra beveiligingsniveau aangezien het voorkomt dat gebruikers willekeurige codeunits uitvoeren via de taakwachtrij. Als de gebruiker parameters aan een rapport moet doorgeven, kan dit enkel door de lijstuitvoering in een codeunit te plaatsen die vervolgens de invoerparameters parseert en deze in de lijst plaatst voordat deze wordt uitgevoerd.  

## <a name="see-also"></a>Zie ook  
[Beheer](admin-setup-and-administration.md)  
[Business Central instellen](setup.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
