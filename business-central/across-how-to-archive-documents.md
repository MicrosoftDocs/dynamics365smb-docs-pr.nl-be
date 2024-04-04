---
title: Verkoop- en inkoopdocumenten archiveren
description: 'U kunt verkoop- en inkooporders, offertes, retourorders en raamcontracten archiveren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/18/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# <a name="archive-documents"></a>Documenten archiveren

U kunt verkoop- en inkooporders, offertes, retourorders en raamcontracten archiveren. U kunt een verkoop- of inkoopdocument meerdere keren archiveren, waarbij u steeds een verschillende gearchiveerde versie opslaat.

Voor gearchiveerde verkoopdocumenten waarvan het origineel nog bestaat en niet is geboekt, kunt u de actie **Herstellen** gebruiken om het huidige document te overschrijven met een gearchiveerde versie. De actie werkt alleen voor verkoopdocumenten.

Voor gearchiveerde documenten waarvan het origineel is verwijderd, kunt u de inhoud alleen opnieuw gebruiken door de gegevens te kopiëren, bijvoorbeeld met de actie **Kopiëren uit document**.  

## <a name="to-set-up-automatic-document-archiving"></a>Automatische documentarchivering instellen

U kunt automatische archivering van verkoop- en inkooporders, offertes, raamcontracten en retourorders instellen. Als automatisch archiveren is ingeschakeld, wordt er een nieuwe versie van het gearchiveerde document gemaakt wanneer iemand de volgende dingen doet:

* Wijzigt of verwijdert een document.
* Print, downloadt of verzendt een document per e-mail.
* Converteert een offerte naar een order of factuur.
* Plaatst een order.

In de volgende procedure wordt beschreven hoe u automatische archivering van verkoopdocumenten instelt. De stappen zijn vergelijkbaar voor inkoopdocumenten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Geef op het sneltabblad **Archiveren** op of automatische archivering moet worden ingeschakeld voor de verschillende soorten verkoopdocumenten. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

In de volgende tabel worden de opties voor het veld **Offertes archiveren** beschreven.

|Optie|Omschrijving|
|------|-----------|
|**Nooit**| Archiveer nooit verkoopoffertes wanneer deze worden verwijderd.|
|**Vraag**|Vraag de gebruiker te kiezen of verkoopoffertes moeten worden gearchiveerd wanneer ze worden verwijderd.|
|**Altijd**|Verkoopoffertes automatisch archiveren wanneer deze worden verwijderd.|

## <a name="to-manually-archive-a-sales-order"></a>Een verkooporder handmatig archiveren

In de volgende procedure wordt beschreven hoe u een verkooporder handmatig archiveert. De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Open een verkooporder die u wilt archiveren.  
3. Kies de actie **Document archiveren**.

De verkooporder wordt gearchiveerd. U kunt deze bekijken op de pagina **Gearchiveerde verkooporders**.

## <a name="to-restore-a-non-posted-sales-document-or-a-project-from-the-archive"></a>Een niet-geboekte verkooporder vanuit het archief herstellen

In de volgende procedure wordt beschreven hoe een gearchiveerde verkooporder wordt hersteld tot de oorspronkelijke verkooporder. Een document herstellen kan alleen als het oorspronkelijke document niet is geboekt. De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporderarchieven** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gearchiveerde verkooporder of versie ervan die u wilt herstellen en kies vervolgens de actie **Herstellen**.  

De inhoud van de oorspronkelijke verkooporder wordt vervangen door de gearchiveerde versie.

## <a name="to-delete-archived-versions"></a>Gearchiveerde verkooporders verwijderen

Gebruik een bewaarbeleid om gearchiveerde documenten op te ruimen die u niet langer nodig hebt. Met bewaarbeleid kunnen beheerders bepalen hoe lang ze gegevens willen bewaren. Ze kunnen bijvoorbeeld een beleid instellen dat gegevens na een vervaldatum verwijdert. Zie voor meer informatie [Bewaarbeleid definiëren](admin-data-retention-policies.md).

Er zijn een paar dingen waar u op moet letten bij het maken van bewaarbeleid voor gearchiveerde documenten:

* *Als het originele document niet is verwijderd, verwijdert Business Central de gearchiveerde versies niet. Gearchiveerde versies verlopen niet zolang het origineel bestaat.
* Wanneer u het bewaarbeleid instelt, kunt u opgeven dat u wilt dat het beleid alle gearchiveerde versies van een document verwijdert, behalve de meest recente. U hebt bijvoorbeeld tien versies van een document en wilt een kopie van de laatste versie bewaren. 
* Business Central berekent de vervaldatum voor documenten op basis van de datum van de meest recente gearchiveerde versie.

## <a name="see-also"></a>Zie ook

[Documentregels traceren](across-how-to-track-document-lines.md)  
[Verkoop](sales-manage-sales.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
