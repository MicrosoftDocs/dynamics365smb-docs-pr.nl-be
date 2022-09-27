---
title: Artikeltracering instellen met serie-, lot- en pakketnummers
description: Artikeltracering instellen met serie-, lot- en pakketnummers
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/31/2021
ms.author: edupont
ms.openlocfilehash: c298903d62da4cfd346a46ff1978ab91644fb13f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533280"
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Artikeltracering instellen met serie-, lot- en pakketnummers

Houd voorraadartikelen bij, zelfs in complexe magazijnconfiguraties met nummers die specifiek zijn voor elk artikel, hetzij als afzonderlijk object, als lot of als pakket. Met artikeltracering kunt u artikelen traceren via interne magazijnverplaatsingen en uitgaande en inkomende documenten.

Artikelen met serie- en lotnummers kunnen voorwaarts en achterwaarts worden getraceerd in de toeleveringsketen. Dit is handig voor algemene kwaliteitsmeting en voor terugroepacties. Zie voor meer informatie [Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> Schakel in releasewave 1 en later de functie-update *Tracering per pakketnummer gebruiken in reserverings- en traceringssysteem* in als u zowel met pakketnummers als serie- en lotnummers wilt werken. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](admin-feature-management.md). Zodra de functie is ingeschakeld, kunt u pakketnummers toewijzen aan uitgaande en inkomende documenten, net zoals u met lotnummers kunt werken.  

## <a name="numbers-and-item-tracking"></a>Aantallen en artikeltracering

Als onderdeel van uw magazijnprocessen kunt u uw voorraad bundelen in pakketten, dozen, containers, enzovoort. Maar om de items bij te houden, kent u unieke nummers toe als identificatie. U vervaardigt en verkoopt bijvoorbeeld een stoel met artikelnummer *1900-S*. Elke individuele stoel heeft een serienummer, *1001*, maar u bundelt ook vier stoelen tot een lot, *LOT0001*, en u verzendt de stoelen in een container met het pakketnummer *CONTAINER010* dat ook andere artikelen omvat, zoals *LOT0100* met bijzettafels, en *LOT200* met lampen.  

Afhankelijk van uw configuratie gebruikt u deze verschillende nummers om de voorraad bij te houden in [!INCLUDE [prod_short](includes/prod_short.md)] in de verschillende stadia van inkoop, verkoop, magazijnactiviteiten, enzovoort.

## <a name="to-set-up-item-tracking-codes"></a>Artikeltraceringscodes instellen

Een artikeltraceringscode weerspiegelt de verschillende overwegingen die een bedrijf moet maken met betrekking tot het gebruik van serie- en lotnummers voor artikelen die in de voorraad worden verplaatst.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeltraceringscodes** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Definieer op de tabbladen **Serienr.**, **Lotnr.** en **Pakketnr.** beleid voor artikeltracering via respectievelijk serie-, lot- en pakketnummers.  

> [!NOTE]  
> Als u bepaalde artikelen of bepaalde lots tijdens hun levensduur wilt bijhouden, moet u respectievelijk de velden **Specifieke serienr.-tracering** en **Specifieke lottracering** kiezen. Wanneer u een uitgaande eenheid van een artikel met deze artikeltraceringscode verwerkt, moet u daarom altijd opgeven welk bestaand serienummer of lotnummer moet worden verwerkt. Dit betekent dat elke verkochte eenheid van het artikel moet worden vereffend met een bepaalde reeks serienummers of een specifiek lotnummer in de voorraad. Met andere woorden: het serienummer of lotnummer dat bij de invoer in de voorraad aan het artikel is toegewezen, moet samen met dat artikelsoort uit de voorraad worden geboekt.

Omdat dit bepaalde configuratieveld alle mogelijke artikeltransacties omvat, worden de afzonderlijke inkomende/uitgaande velden ook geselecteerd. De afzonderlijke inkomende/uitgaande velden hebben echter geen invloed op voorraadvereffening. Ze geven uitsluitend aan wanneer artikeltraceringsnummers worden toegewezen in de werkstroom van uw bedrijf.  

> [!NOTE]  
>  Om tijdens magazijnactiviteiten artikeltraceringsnummers toe te wijzen moeten de velden **Magazijnserienr.-tracering** en **Magazijnlottracering** zijn ingeschakeld op de bij het artikel horende artikeltraceringscodekaart.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Vervalregels instellen voor serie- of lotnummers

Voor sommige artikelen wilt u mogelijk bepaalde vervaldatums en regels instellen in de artikeltraceringscode. Met deze functie kunt u bijhouden wanneer bepaalde serie- of lotnummers vervallen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeltraceringscodes** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een bestaande artikeltraceringscode en kies de actie **Bewerken**.  
3. Schakel op het sneltabblad **Diversen** de volgende velden in:  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Strikte verloopdatumboeking**|Hiermee wordt opgegeven dat de vervaldatum van het artikeltraceringsnummer dat bij binnenkomst in de voorraad is toegewezen, strikt moet worden nagekomen bij het verlaten van de voorraad.|  
    |**Invoer van vervaldatum vereisen**|Hiermee wordt opgegeven dat u een vervaldatum op de artikeltraceringsregel moet invoeren.|  
    |**Vervaldatums gebruiken**|Hiermee wordt opgegeven dat u vervaldatums wilt berekenen. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Garanties instellen voor serie- of lotnummers

Mogelijk wilt u voor bepaalde artikelen bepaalde garanties instellen in de artikeltraceringscode. Met deze functie kunt u bijhouden wanneer de garanties op bepaalde serie- en lotnummers in de voorraad verlopen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeltraceringscodes** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een bestaande artikeltraceringscode en kies de actie **Bewerken**.  
3. Vul het veld **Garantiedatumformule** op het sneltabblad **Overig** in en schakel de volgende velden in:  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Garantiedatumformule**|Bevat de laatste dag van de garantie voor het artikel.|  
    |**Invoer van garantiedatum vereisen**|Geeft aan dat u een garantiedatum op de artikeltraceringsregel handmatig moet invoeren.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>Artikelen voor tracering instellen met de juiste artikeltraceringscodes

Om artikeltracering in te schakelen moet u eerst de artikeltraceringscodes aan een artikel toewijzen. Er zijn twee manieren om artikeltraceringscodes toe te voegen: door de code uit een vooraf gedefinieerde lijst te selecteren of door een nieuwe unieke code toe te wijzen. Wijs de velden aan om een korte omschrijving te lezen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een bestaand item uit de lijst en open de pagina **Artikelkaart**.  
3. Wijs op het sneltabblad **Artikeltracering** de juiste artikeltraceringscodes toe en kies de **Artikeltraceringscode**, de **Serienrs.** en de **Lotnrs.**.
    1. Als alternatief kunt u ook een nieuwe artikeltraceringscode maken door de actie **Nieuw** te selecteren.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/prepare-item-tracking/)

## <a name="see-also"></a>Zie ook

[Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)  
[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)  
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Artikelen reserveren](inventory-how-to-reserve-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
