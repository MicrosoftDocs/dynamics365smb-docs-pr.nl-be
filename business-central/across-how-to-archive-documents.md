---
title: Verkoop- en inkoopdocumenten archiveren
description: 'U kunt verkoop- en inkooporders, offertes, retourorders en raamcontracten archiveren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/26/2024
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# Documenten archiveren

U kunt verkoop- en inkooporders, offertes, retourorders en raamcontracten archiveren. Als u de functies voor projectbeheer gebruikt, kunt u uw projecten ook archiveren. U kunt documenten en projecten meerdere keren archiveren, waarbij u steeds een verschillende gearchiveerde versie opslaat.

Voor verkoopdocumenten waarvan het origineel nog bestaat en niet is geboekt, kunt u de actie **Herstellen** gebruiken om het te overschrijven met een gearchiveerde versie. 

> [!NOTE]
> U kunt alleen verkoopdocumenten en projecten herstellen. De actie is niet beschikbaar voor gearchiveerde inkoopdocumenten.

Voor gearchiveerde documenten waarvan het origineel is verwijderd, kunt u de inhoud opnieuw gebruiken door de gegevens te kopiëren, bijvoorbeeld met de actie **Kopiëren uit document**.  

## Automatische documentarchivering instellen

U kunt archiveren automatiseren om een nieuwe versie van het gearchiveerde document te maken wanneer iemand de volgende dingen doet:

* Wijzigt of verwijdert een document of project.
* Print, downloadt of verzendt een document per e-mail.
* Converteert een offerte naar een order of factuur.
* Plaatst een order.

In de volgende stappen wordt beschreven hoe u de automatische archivering van verkoopdocumenten via de pagina **Instellingen verkoop en tegoeden**. De stappen zijn vergelijkbaar voor inkoopdocumenten en projecten. Voor inkoopdocumenten gebruikt u de pagina **Instellingen inkoop en betalingen**. Gebruik voor projecten de pagina **Projectinstellingen**.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Geef op het sneltabblad **Archiveren** op of automatische archivering moet worden ingeschakeld voor de verschillende soorten verkoopdocumenten. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

In de volgende tabel worden de opties voor het veld **Offertes archiveren** beschreven.

|Optie|Omschrijving|
|------|-----------|
|**Nooit**| Archiveer nooit verkoopoffertes wanneer deze worden verwijderd.|
|**Vraag**|Vraag de gebruiker te kiezen of verkoopoffertes moeten worden gearchiveerd wanneer ze worden verwijderd.|
|**Altijd**|Verkoopoffertes automatisch archiveren wanneer deze worden verwijderd.|

## Een verkooporder handmatig archiveren

In de volgende procedure wordt beschreven hoe u een verkooporder handmatig archiveert. De stappen zijn vergelijkbaar voor alle documenten en projecten die u kunt archiveren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Open een verkooporder die u wilt archiveren.  
3. Kies de actie **Document archiveren**.

De verkooporder wordt gearchiveerd. U kunt deze bekijken op de pagina **Gearchiveerde verkooporders**.

## Een niet-geboekt verkoopdocument of een project vanuit het archief herstellen

In de volgende procedure wordt beschreven hoe een gearchiveerde verkooporder wordt hersteld tot de oorspronkelijke verkooporder. Een document herstellen kan alleen als het oorspronkelijke document niet is geboekt. De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes en ook voor projecten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporderarchieven** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gearchiveerde verkooporder of versie ervan die u wilt herstellen en kies vervolgens de actie **Herstellen**.  

De inhoud van de oorspronkelijke verkooporder of het oorspronkelijke project wordt vervangen door de gearchiveerde versie.

## Gearchiveerde versies verwijderen

Gebruik een bewaarbeleid om gearchiveerde versies op te ruimen die u niet langer nodig hebt. Met bewaarbeleid kunnen beheerders bepalen hoe lang ze gegevens willen bewaren. Ze kunnen bijvoorbeeld een beleid instellen dat gegevens na een vervaldatum verwijdert. Ga voor meer informatie naar [Bewaarbeleid definiëren](admin-data-retention-policies.md).

Er zijn een paar dingen waar u op moet letten bij het maken van bewaarbeleid voor gearchiveerde documenten en projecten:

* Als het oorspronkelijke document niet wordt verwijderd, verwijdert [!INCLUDE [prod_short](includes/prod_short.md)] de gearchiveerde versies niet. Gearchiveerde versies verlopen niet zolang het origineel bestaat.
* Wanneer u het bewaarbeleid instelt, kunt u opgeven dat u wilt dat het beleid alle gearchiveerde versies verwijdert, behalve de meest recente. U hebt bijvoorbeeld tien versies en wilt een kopie van de laatste versie bewaren. 
* [!INCLUDE [prod_short](includes/prod_short.md)] berekent de vervaldatum voor documenten op basis van de datum van de meest recente gearchiveerde versie.

## Zie ook

[Documentregels traceren](across-how-to-track-document-lines.md)  
[Verkoop](sales-manage-sales.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
