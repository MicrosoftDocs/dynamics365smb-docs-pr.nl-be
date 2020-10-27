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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5e8c611ed5d542436f470781c92d17095ecd1f5d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924590"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Gebruik van taakwachtrijen om taken te plannen

Met taakwachtrijen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen gebruikers specifieke rapporten en codeunits plannen en uitvoeren. U kunt taken éénmalig of herhaaldelijk uitvoeren. U kunt bijvoorbeeld het rapport **Verkoper * Verkoopstatistieken** wekelijks uitvoeren om de verkopen per verkoper elke week bij te houden of u kunt de codeunit **Goedkeuringsaanvragen delegeren** dagelijks uitvoeren om te voorkomen dat documenten zich opstapelen of anderszins de werkstroom blokkeren.

Op de pagina **Taakwachtrijposten** worden alle bestaande posten weergegeven. Als u een nieuwe taakwachtrijpost toevoegt die u wilt plannen, moet u informatie opgeven over het objecttype dat u wilt uitvoeren, zoals een rapport of codeunit, en de naam en id van het object opgeven dat u wilt uitvoeren. U kunt ook parameters toevoegen om het gedrag van de taakwachtrijpost te specificeren. Zo kunt u een parameter toevoegen om alleen geboekte verkooporders te verzenden. U moet zijn gemachtigd om het betreffende rapport of de betreffende code-unit uit te voeren, want anders wordt een fout geretourneerd wanneer de verwerkingswachtrij wordt uitgevoerd.  

Een taakwachtrij kan veel posten bevatten, die de taken vormen die door de wachtrij worden beheerd en uitgevoerd. Informatie in de post geeft aan welke code-unit of welk rapport wordt uitgevoerd, wanneer en hoe vaak de post wordt uitgevoerd, in welke categorie de taak wordt uitgevoerd en hoe deze wordt uitgevoerd.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Boeking op de achtergrond instellen met taakwachtrijen

Taakwachtrijen zijn een effectief hulpmiddel om de uitvoering van bedrijfsprocessen op de achtergrond te plannen, zoals wanneer meerdere gebruikers proberen verkooporders te boeken, maar er slechts één order tegelijk kan worden verwerkt.  

In de volgende procedure wordt uitgelegd hoe u achtergrondboeking van verkooporders instelt. De stappen zijn vergelijkbaar voor de inkoop.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopinstellingen** in en kies de desbetreffende koppeling.
2. Kies op de pagina **Verkoopinstellingen** het selectievakje **Boeken via taakwachtrij** .
3. Kies het veld **Taakwachtrijcategoriecode** en selecteer vervolgens de code **VRKBOEKING** .

    > [!NOTE]
    > Sommige taken wijzigen dezelfde gegevens en moeten niet tegelijkertijd worden uitgevoerd omdat dat conflicten kan veroorzaken. Met achtergrondtaken voor verkoopdocumenten wordt bijvoorbeeld geprobeerd dezelfde gegevens tegelijkertijd te wijzigen. Taakwachtrijcategorieën helpen dit soort conflicten voorkomen door ervoor te zorgen dat wanneer een taak wordt uitgevoerd, een andere taak die tot dezelfde taakwachtrijcategorie behoort, pas wordt uitgevoerd als de eerste is voltooid. Een taak die bijvoorbeeld behoort tot een taakwachtrijcategorie Verkooptaak wacht tot alle andere verkoopgerelateerde taken zijn voltooid. U geeft een taakwachtrijcategorie op met het sneltabblad **Boeken op achtergrond** op de pagina **Verkoopinstellingen** .
    >
    > [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt taakwachtrijcategorieën voor verkoop-, inkoop- en grootboekboeking. We raden aan dat een van deze, of een die u maakt, altijd wordt opgegeven. Als u problemen ondervindt als gevolg van conflicten, kunt u overwegen een categorie in te stellen voor alle verkoop-, inkoop- en grootboekboeking.

    Als u ook wilt dat verkoopdocumenten worden afgedrukt wanneer deze worden geboekt, schakelt u het selectievakje **Boeken en afdrukken via taakwachtrij** in op de pagina **Verkoopinstellingen** .  

    > [!IMPORTANT]  
    > Wanneer u een taak voor het boeken en afdrukken van documenten instelt en er op de printer een dialoogvenster wordt weergegeven, zoals een verzoek om aanmeldingsgegevens of een waarschuwing over een laag printerinktniveau, dan wordt het document geboekt, maar niet afgedrukt. De overeenkomstige invoer van de taakwachtrij krijgt uiteindelijk een time-out en het veld **Status** wordt ingesteld op **Fout** . Dienovereenkomstig is het raadzaam dat u geen printerinstellingen gebruikt waarvoor interactie met de weergave van printerdialoogvensters nodig is in combinatie met boeken op de achtergrond.

    De volgende keer dat u verkoopdocumenten boekt, maakt [!INCLUDE [prodshort](includes/prodshort.md)] automatisch een taakwachtrij-item voor elk document en voert het de taken één voor één op de achtergrond uit.

4. Om te controleren dat de taakwachtrij werkt zoals verwacht, boekt u een verkooporder. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.

5. Kijk op de pagina **Logposten taakwachtrij** of de verkooporder met succes is geboekt. Zie voor meer informatie [Status of fouten in de projectwachtrij weergeven](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Een taakwachtrijpost maken voort batchboeking van verkooporders

U kunt eventueel ook boekingen uitstellen naar tijdstippen die handiger zijn voor uw organisatie. Het kan bijvoorbeeld zinvol zijn om in uw bedrijf bepaalde routines uit te voeren wanneer de meeste gegevens voor die dag zijn ingevoerd. U kunt dat bereiken door de taakwachtrij zo in te stellen dat er diverse batchboekingsrapporten worden uitgevoerd, zoals **Batchboeken verkooporders** , **Batchboeken verkoopfacturen** en vergelijkbare rapporten. [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt boeken op de achtergrond voor alle verkoop-, inkoop- en servicedocumenten.

In de volgende procedure wordt getoond hoe u het rapport **Batchboeken verkooporders** instelt om automatisch verkooporders te boeken om 16:00 uur op werkdagen.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Taakwachtrijposten** in en kies de desbetreffende koppeling.  
2. Kies de actie **Nieuw** .  
3. Selecteer in het veld **Uit te voeren objecttype** **Rapport** .  
4. Selecteer in het veld **Uit te voeren object-id** 296, **Batchboeken verkooporders** .

   U kunt ook de volgende rapporten gebruiken:
  
   * 900 **Batchboeken assemblageorders**
   * 497 **Batchboeken inkoopfacturen**
   * 496 **Batchboeken inkooporders**
   * 498 **Batchboeken ink.-creditnota's**
   * 6665 **Batchboeken ink.-retourorders**
   * 298 **Batchboeken verk.-creditnota**
   * 297 **Batchboeken verkoopfacturen**
   * 296 **Batchboeken verkooporders**
   * 6655 **Batchboeken verk.-retourorder**
   * 6005 **Batchboeken servicecreditnota's**
   * 6004 **Batchverwerking servicefacturen**
   * 6001 **Batchboeken serviceorders**

5. Selecteer het selectievakje **Rapportaanvraagpagina** .
6. Definieer op de aanvraagpagina **Batchboeken verkooporders** wat er wordt opgenomen tijdens automatische boeking van verkooporders en kies vervolgens de knop **OK** .

    > [!IMPORTANT]
    > Vergeet niet om strikte filters in te stellen. Als u dat verzuimt, boekt [!INCLUDE [prodshort](includes/prodshort.md)] alle documenten, zelfs als ze nog niet gereed zijn. U kunt overwegen een filter in te stellen voor het veld **Status** met de waarde *Vrijgegeven* en een filter in te stellen voor het veld **Boekingsdatum** met de waarde *..vandaag* . Zie [Sorteren, zoeken en filteren](ui-enter-criteria-filters.md) voor meer informatie.
7. Selecteer alle selectievakjes van **Uitvoeren op maandagen** tot en met **Uitvoeren op vrijdagen** .
8. Voer in het veld **Begintijd** 4 PM in.
9. Kies de actie **Status instellen op Gereed** .

Verkooporders die binnen de gedefinieerde filters vallen, worden nu elke week om 16:00 uur geboekt.

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
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Taakwachtrijposten** in en kies de desbetreffende koppeling.
2. Selecteer op de pagina **Taakwachtrijposten** een taakwachtrijpost en kies vervolgens de actie **Logboekvermeldingen** .  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Een status vanuit een verkoop- of inkoopdocument weergeven
1. Kies vanuit het document dat u hebt geprobeerd te boeken via boeken op de achtergrond, het veld **Status taakwachtrij** dat de waarde **Fout** bevat.
2. Bekijk de foutmelding en los het probleem op.

## <a name="the-my-job-queue-part"></a>Het onderdeel Mijn taakwachtrij
In het onderdeel **Mijn taakwachtrij** in uw rolcentrum worden de taakwachtrijposten weergegeven die u hebt gestart, maar die nog niet zijn voltooid. Standaard is het onderdeel niet zichtbaar, zodat u het moet toevoegen aan uw rolcentrum. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.  

Dit onderdeel toont welke documenten met uw id in het veld **Toegewezen gebruikers-id** worden verwerkt of in de wachtrij staan, inclusief posten die verband houden met boeking op de achtergrond. Het onderdeel kan u in één oogopslag laten zien of er een fout is opgetreden bij het boeken van een document en of er fouten zijn opgetreden in een taakwachtrijpost. Met het onderdeel kunt u een documentboeking annuleren als deze niet wordt uitgevoerd.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Een fout in het gedeelte Mijn taakwachtrij weergeven
1. Kies in een post met de status **Fout** de actie **Fout weergeven** .
2. Bekijk de foutmelding en los het probleem op.

## <a name="security"></a>Beveiliging  
Taakwachtrijposten worden uitgevoerd op basis van machtigingen. Die machtigingen moeten de uitvoering van de lijst of codeunit toestaan.  

Wanneer een taakwachtrij handmatig is geactiveerd, wordt deze uitgevoerd met de referenties van de gebruiker. Wanneer een taakwachtrij is geactiveerd als een geplande taak, wordt deze uitgevoerd met de referenties van de serverinstantie. Wanneer een taak wordt uitgevoerd, wordt deze uitgevoerd met de referenties van de taakwachtrij die deze activeert. De gebruiker die de taakwachtrijpost maakte, moet echter ook machtigingen hebben. Wanneer een taak wordt uitgevoerd in een gebruikerssessie (bijvoorbeeld bij het boeken op de achtergrond), wordt deze taak uitgevoerd met de aanmeldingsgegevens van de gebruiker die deze taak heeft gemaakt.  

> [!IMPORTANT]  
> Als u de machtigingenset SUPER gebruikt die wordt geleverd met [!INCLUDE[d365fin](includes/d365fin_md.md)], hebben u en uw gebruikers de machtiging om alle objecten uit te voeren. In dit geval wordt de toegang voor elke gebruiker alleen beperkt door machtigingen voor gegevens.  

## <a name="using-job-queues-effectively"></a>Taakwachtrijen efficiënt gebruiken  
De record van de taakwachtrijpost heeft veel velden om de parameters in een codeunit te plaatsen die u hebt opgegeven voor het uitvoeren met een taakwachtrij. Dit betekent ook dat codeunits die moeten worden uitgevoerd via de taakwachtrij, moeten worden gespecificeerd met de taakwachtrijrecord als een parameter in de **OnRun** trigger. Dit biedt een extra beveiligingsniveau aangezien het voorkomt dat gebruikers willekeurige codeunits uitvoeren via de taakwachtrij. Als de gebruiker parameters aan een rapport moet doorgeven, kan dit enkel door de lijstuitvoering in een codeunit te plaatsen die vervolgens de invoerparameters parseert en deze in de lijst plaatst voordat deze wordt uitgevoerd.  

## <a name="scheduling-synchronization-between-d365fin-and-d365fin"></a>Synchronisatie plannen tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)]

Als u [!INCLUDE[d365fin](includes/d365fin_md.md)] hebt geïntegreerd met [!INCLUDE[d365fin](includes/cds_long_md.md)], kunt u de taakwachtrij gebruiken om te plannen wanneer u gegevens wilt synchroniseren voor de records die u in de twee zakelijke apps hebt gekoppeld. Afhankelijk van de richting en regels die u hebt gedefinieerd voor de integratie, kunnen de synchronisatietaken ook nieuwe records maken in de doel-app die overeenkomen met die in de bron. Als een verkoper bijvoorbeeld een nieuw contact maakt in [!INCLUDE[crm_md](includes/crm_md.md)], kan de synchronisatietaak dat contact maken voor de gekoppelde verkoper in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Een synchronisatie plannen tussen Business Central en Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md) voor meer informatie.

## <a name="see-also"></a>Zie ook

[Beheer](admin-setup-and-administration.md)  
[Business Central instellen](setup.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
