---
title: Standaardregels instellen voor periodieke verkoop en inkopen | Microsoft Docs
description: U kunt verkoopregels en inkoopregels instellen die u vaak maakt en deze vervolgens invoeren op verkoop- en inkoopdocumenten om de regels snel te vullen met standaardgegevens.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 40af4b0010b46938a9ce53a12dd95f1b2a687cc9
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748181"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Periodieke verkoop- en inkoopregels maken
Als u vaak verkoop- en inkoopregels met dezelfde informatie moet maken, kunt u standaardregels instellen die u dan kunt invoegen op periodieke verkoop- en inkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders.  

In de volgende procedures wordt beschreven hoe u werkt met standaardverkoopregels op een verkoopfactuur. Dit werkt op een soortgelijke manier voor alle andere verkoopdocumenten en voor alle inkoopdocumenten.  

## <a name="to-set-up-recurring-sales-lines"></a>Periodieke verkoopregels instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodieke verkoopregels** in en kies de gerelateerde koppeling.  
2. Kies op de pagina **Periodieke verkoopregels** de actie **Nieuw**.  
3. Vul de benodigde velden in op het sneltabblad **Algemeen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Voer op het sneltabblad **Regels** gegevens in de velden in om verkoopregels voor te bereiden die de standaardregels reflecteren die u verwacht te gebruiken als terugkerende regels in verkoopdocumenten.  

> [!NOTE]
> U kunt geen prijzen definiëren op periodieke verkoopregels, omdat de prijzen, kortingen, enzovoort, op de werkelijke verkoopdocumenten worden berekend nadat u de periodieke verkoopregels hebt ingevoegd.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>Periodieke verkoopregels aan een klant toewijzen

Wijs een of meer periodieke verkoopregels aan een klant toe zodat deze beschikbaar zijn om te worden ingevoegd op verkoopdocumenten voor die klant.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de projectkaart voor een relevante klant.
3. Kies de actie **Periodieke verkoopregels**.
4. Selecteer op de pagina **Periodieke verkoopregels** codes voor de periodieke verkoopregels die u wilt kunnen invoegen op verkoopdocumenten voor de klant.
5. Vul de overige velden in om te definiëren wanneer, hoe en waar de periodieke verkoopregels moeten worden gebruikt.  

    Als u van plan bent de set periodieke verkoopregels samen met de batchverwerking **Periodieke verkoopfacturen maken** te gebruiken, gebruikt u de velden **Geldig vanaf datum** en **Geldig tot datum** wanneer de periodieke verkoopregels worden gebruikt voor het maken van facturen. Zie voor meer informatie [Meerdere verkoopfacturen maken op basis van standaardverkoopregels](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-recurring-sales-lines).

    U kunt ook een betalingsmethode voor automatische incasso en machtiging voor automatische incasso opgeven. De verkoopfacturen die zijn gemaakt met de batchverwerking **Periodieke verkoopfacturen maken** bevatten dan de informatie die nodig is om de betaling voor de verkoopfacturen met automatische incasso van SEPA te innen. Zie voor meer informatie [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md).

6. Selecteer in de vier velden, waarin u selecteert hoe de regels worden ingevoegd in vier documenttypen, een van de volgende opties:

|Optie|Omschrijving|
|------|-----------|
|**Handmatig**|U moet handmatig een terugkerende verkoopregel zoeken en invoegen die bestaat voor de klant.|
|**Automatisch**|Als er meerdere terugkerende verkoopregels voor de klant zijn, ontvangt u een bericht van waaruit u er een kunt kiezen om in te voegen. Als er slechts één terugkerende verkoopregel bestaat, wordt deze automatisch ingevuld.<br /><br />Merk op dat dit alleen werkt als het nieuwe document is gemaakt op basis van een documentenlijst, bijvoorbeeld door kiezen van de actie **Nieuw** op de pagina **Verkooporders**. Het werkt niet als het document bijvoorbeeld is gemaakt op basis van een klantenkaart.|
|**Altijd vragen**|Er wordt een bericht weergegeven en alle bestaande terugkerende verkoopregels worden weergegeven zodat u er een kunt selecteren.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Periodieke verkoopregels invoegen op een verkoopfactuur

Als er periodieke verkoopregels voor de klant zijn, kunt u deze invoegen of laten invoegen op alle typen verkoopdocumenten, zoals een verkoopfactuur. Als u de **Altijd vragen**-opties hebt geactiveerd, wordt u geïnformeerd als er periodieke verkoopregels zijn.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Facturen** in en kies de gerelateerde koppeling.
2. Open de verkoopfactuur waarin u een of meer standaardverkoopregels wilt invoegen.
3. Kies de actie **Periodieke verkoopregels ophalen**.
4. Kies op de pagina **Periodieke verkoopregels** de opzoekknop in het veld **Code** en selecteer een set standaardverkoopregels.
5. Kies de knop **OK** om de standaardverkoopregels op de factuur in te voegen, waar u deze zo kunt gebruiken of de gegevens kunt bewerken.

## <a name="to-create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Meerdere verkoopfacturen maken op basis van periodieke verkoopregels
U kunt de batchverwerking **Periodieke verkoopfacturen maken** gebruiken om verkoopfacturen te maken volgens de standaardverkoopregels die zijn toegewezen aan de klanten, en met boekingsdatums binnen de datums voor geldig vanaf en geldig tot die u op de standaardverkoopregels opgeeft.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodieke verkoopfacturen maken** in en kies de gerelateerde koppeling.
2. Vul de velden op de pagina **Periodieke verkoopfacturen maken** in met de benodigde gegevens.
3. In het filterveld **Code** voert u de code in voor standaardverkoopregels die aan een klant worden toegewezen voor wie u verkoopfacturen wilt maken.
4. Kies de knop **OK**.

Verkoopfacturen worden gemaakt voor klanten met de opgegeven standaard klantverkoopcode en een waarde opgegeven voor automatische incasso-informatie voor het boeken op de opgegeven datum.

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]