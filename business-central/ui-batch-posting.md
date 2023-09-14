---
title: Meerdere documenten tegelijkertijd boeken
description: Leer hoe u meerdere niet-geboekte documenten in een lijst selecteert voor onmiddellijke of geplande batchboeking in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.reviewer: bholtorf
ms.date: 06/25/2021
ms.author: bholtorf
---
# <a name="post-multiple-documents-at-the-same-time"></a>Meerdere documenten tegelijkertijd boeken

In plaats van afzonderlijke documenten een voor een te boeken kunt u meerdere niet-geboekte documenten in een lijst selecteren voor directe batchboeking of voor batchboeking volgens een planning, bijvoorbeeld aan het einde van de dag. Dit kan handig zijn als alleen een supervisor documenten kan boeken die door andere gebruikers zijn gemaakt of om problemen met de systeemprestaties te voorkomen door boeking tijdens werkuren.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Meerdere inkooporders onmiddellijk boeken

In de volgende procedure wordt uitgelegd hoe u meerdere inkooporders onmiddellijk kunt boeken. De stappen zijn vergelijkbaar voor alle inkoop- en verkoopdocumenten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling
2. Ga op de pagina **Inkooporders** door met het selecteren van alle te boeken orders:
3. Voer in het veld **Nr.** de drie verticale stippen om het contextmenu te openen en kies vervolgens de actie **Meer selecteren**.
4. Schakel het selectievakje in voor alle regels die orders vertegenwoordigen die u tegelijkertijd wilt boeken.
5. Kies de actie **Boeken** en kies vervolgens weer de actie **Boeken**.
6. Kies de knop **Ja** in het bevestigingsbericht.

## <a name="to-batch-post-multiple-purchase-orders"></a>Meerdere inkooporders in een batch boeken

In de volgende procedure wordt uitgelegd hoe u inkooporders in een batch boekt. De stappen zijn vergelijkbaar voor alle inkoop- en verkoopdocumenten waarbij de actie **Batchboeken** beschikbaar is.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
2. Ga op de pagina **Inkooporders** door met het selecteren van alle te boeken orders:
3. Voer in het veld **Nr.** de drie verticale stippen om het contextmenu te openen en kies vervolgens de actie **Meer selecteren**.
4. Schakel het selectievakje in voor alle regels die orders vertegenwoordigen die u tegelijkertijd wilt boeken.
5. Kies de actie **Boeken** en kies vervolgens de actie **Batchboeken**.
6. Vul desgewenst de velden op de pagina **Batchboeken inkooporders** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Kies de knop **Ok**.
8. Als u mogelijke problemen wilt zien die zijn opgetreden tijdens het batchboeken van documenten, opent u de pagina **Foutberichtregister**.

> [!NOTE]
> Het boeken van meerdere documenten kan enige tijd duren en andere gebruikers blokkeren. Overweeg om boeken op de achtergrond in te schakelen. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a>Boeking op de achtergrond instellen met taakwachtrijen
Taakwachtrijen zijn een effectief hulpmiddel om de uitvoering van bedrijfsprocessen op de achtergrond te plannen, zoals wanneer meerdere gebruikers proberen verkooporders te boeken, maar er slechts één order tegelijk kan worden verwerkt.  

In de volgende procedure wordt uitgelegd hoe u achtergrondboeking van verkooporders instelt. De stappen zijn vergelijkbaar voor de inkoop.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Verkoopinstellingen** het selectievakje **Boeken via taakwachtrij**.
3. Kies het veld **Taakwachtrijcategoriecode** en selecteer vervolgens de code **VRKBOEKING**.

    > [!NOTE]
    > Sommige taken wijzigen dezelfde gegevens en moeten niet tegelijkertijd worden uitgevoerd omdat dat conflicten kan veroorzaken. Met achtergrondtaken voor verkoopdocumenten wordt bijvoorbeeld geprobeerd dezelfde gegevens tegelijkertijd te wijzigen. Taakwachtrijcategorieën helpen dit soort conflicten voorkomen door ervoor te zorgen dat wanneer een taak wordt uitgevoerd, een andere taak die tot dezelfde taakwachtrijcategorie behoort, pas wordt uitgevoerd als de eerste is voltooid. Een taak die bijvoorbeeld behoort tot een taakwachtrijcategorie Verkooptaak wacht tot alle andere verkoopgerelateerde taken zijn voltooid. U geeft een taakwachtrijcategorie op met het sneltabblad **Boeken op achtergrond** op de pagina **Verkoopinstellingen**.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] biedt taakwachtrijcategorieën voor verkoop-, inkoop- en grootboekboeking. We raden aan dat een van deze, of een die u maakt, altijd wordt opgegeven. Als u problemen ondervindt als gevolg van conflicten, kunt u overwegen een categorie in te stellen voor alle verkoop-, inkoop- en grootboekboeking.

    Als u ook wilt dat verkoopdocumenten worden afgedrukt wanneer deze worden geboekt, schakelt u het selectievakje **Boeken en afdrukken via taakwachtrij** in op de pagina **Verkoopinstellingen**.  
    Als u **PDF** selecteert in het veld **Soort rapportuitvoer**, zijn succesvol geboekte inkooporders beschikbaar in het onderdeel **Rapportinbox** in uw rolcentrum.

    > [!IMPORTANT]  
    > Wanneer u een taak voor het boeken en afdrukken van documenten instelt en er op de printer een dialoogvenster wordt weergegeven, zoals een verzoek om aanmeldingsgegevens of een waarschuwing over een laag printerinktniveau, dan wordt het document geboekt, maar niet afgedrukt. De overeenkomstige invoer van de taakwachtrij krijgt uiteindelijk een time-out en het veld **Status** wordt ingesteld op **Fout**. Dienovereenkomstig is het raadzaam dat u geen printerinstellingen gebruikt waarvoor interactie met de weergave van printerdialoogvensters nodig is in combinatie met boeken op de achtergrond.

    De volgende keer dat u verkoopdocumenten boekt, maakt [!INCLUDE [prod_short](includes/prod_short.md)] automatisch een taakwachtrij-item voor elk document en voert het de taken één voor één op de achtergrond uit.

4. Om te controleren dat de taakwachtrij werkt zoals verwacht, boekt u een verkooporder. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
    De verkooporder wordt nu toegevoegd aan een speciale taakwachtrijpost, die bepaalt wanneer de documenten worden geboekt. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Een status vanuit een verkoop- of inkoopdocument weergeven
Als de taakwachtrij de verkooporder niet kan boeken, wordt de status gewijzigd in **Fout** en wordt de verkooporder toegevoegd aan de lijst met verkooporders die de gebruiker handmatig moet afhandelen.
1. Kies vanuit het document dat u hebt geprobeerd te boeken via boeken op de achtergrond, het veld **Status taakwachtrij** dat de waarde **Fout** bevat.
2. Bekijk de foutmelding en los het probleem op.

U kunt ook op de pagina **Logposten taakwachtrij** kijken of de verkooporder met succes is geboekt. Voor meer informatie zie het gedeelte [De taakwachtrij bewaken](#monitor-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Een taakwachtrijpost maken voort batchboeking van verkooporders

U kunt eventueel ook boekingen uitstellen naar tijdstippen die handiger zijn voor uw organisatie. Het kan bijvoorbeeld zinvol zijn om in uw bedrijf bepaalde routines uit te voeren wanneer de meeste gegevens voor die dag zijn ingevoerd. U kunt dat bereiken door de taakwachtrij zo in te stellen dat er diverse batchboekingsrapporten worden uitgevoerd, zoals **Batchboeken verkooporders**, **Batchboeken verkoopfacturen** en vergelijkbare rapporten. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt boeken op de achtergrond voor alle verkoop-, inkoop- en servicedocumenten.

In de volgende procedure wordt getoond hoe u het rapport **Batchboeken verkooporders** instelt om automatisch verkooporders te boeken om 16:00 uur op werkdagen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Taakwachtrijposten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer in het veld **Uit te voeren objecttype** **Rapport**.  
4. Selecteer in het veld **Uit te voeren object-id** 296, **Batchboeken verkooporders**.

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

5. Selecteer het selectievakje **Rapportaanvraagpagina**.
6. Definieer op de aanvraagpagina **Batchboeken verkooporders** wat er wordt opgenomen tijdens automatische boeking van verkooporders en kies vervolgens de knop **OK**.

    > [!IMPORTANT]
    > Vergeet niet om strikte filters in te stellen. Als u dat verzuimt, boekt [!INCLUDE [prod_short](includes/prod_short.md)] alle documenten, zelfs als ze nog niet gereed zijn. U kunt overwegen een filter in te stellen voor het veld **Status** met de waarde *Vrijgegeven* en een filter in te stellen voor het veld **Boekingsdatum** met de waarde *..vandaag*. Zie [Sorteren, zoeken en filteren](ui-enter-criteria-filters.md) voor meer informatie.
7. Selecteer alle selectievakjes van **Uitvoeren op maandagen** tot en met **Uitvoeren op vrijdagen**.
8. Voer in het veld **Begintijd** 4 PM in.
9. Kies de actie **Status instellen op Gereed**.

Verkooporders die binnen de gedefinieerde filters vallen, worden nu elke werkdag om 16:00 uur geboekt.

## <a name="monitor-the-job-queue"></a>De taakwachtrij bewaken

Als u boeken op de achtergrond instelt met taakwachtrijen, maak er dan een regelmatige taak van om de taakwachtrij te controleren om eventuele problemen op te vangen. U kunt de status volgen op de pagina **Taakwachtrijposten**. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).  

Als beheerder kunt u [Application Insights](/azure/azure-monitor/app/app-insights-overview) gebruiken om telemetrie te verzamelen en te analyseren die u kunt gebruiken om problemen te identificeren. Zie voor meer informatie [Telemetrie bewaken en analyseren](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) in de ontwikkelaar- en beheerinhoud.  

## <a name="see-also"></a>Zie ook

[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
