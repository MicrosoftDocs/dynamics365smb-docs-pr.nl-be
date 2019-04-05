---
title: Standaardregels instellen voor periodieke verkoop en inkopen | Microsoft Docs
description: U kunt verkoopregels en inkoopregels instellen die u vaak maakt en deze vervolgens invoeren op verkoop- en inkoopdocumenten om de regels snel te vullen met standaardgegevens.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4285603b736cbd585c839a533d325384ba27cd15
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "817147"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Periodieke verkoop- en inkoopregels maken
Als u vaak verkoop- en inkoopregels met dezelfde informatie moet maken, kunt u standaardregels instellen die u dan kunt invoegen op periodieke verkoop- en inkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders.  

In de volgende procedures wordt beschreven hoe u werkt met standaardverkoopregels op een verkoopfactuur. Dit werkt op een soortgelijke manier voor alle andere verkoopdocumenten en voor alle inkoopdocumenten.  

## <a name="to-set-up-standard-sales-lines"></a>Standaardverkoopregels instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Standaardverkoopregels** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Standaardverkoopregels** de actie **Nieuw**.  
3. Vul de benodigde velden in op het sneltabblad **Algemeen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Voer op het sneltabblad **Regels** gegevens in de velden in om verkoopregels voor te bereiden die de standaardregels reflecteren die u verwacht te gebruiken als terugkerende regels in verkoopdocumenten.  

> [!NOTE]
> U kunt geen prijzen definiëren op standaardverkoopregels, omdat de prijzen, kortingen, enzovoort, op de werkelijke verkoopdocumenten worden berekend nadat u de standaardverkoopregels hebt ingevoegd.

## <a name="to-assign-standard-sales-lines-to-a-customers"></a>Standaardverkoopregels aan klanten toewijzen
Wijs een of meer standaardverkoopregels aan een klant toe zodat deze beschikbaar zijn om te worden ingevoegd op verkoopdocumenten voor die klant.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de projectkaart voor een relevante klant.
3. Kies de actie **Periodieke verkoopregels**.
4. Selecteer op de pagina **Periodieke verkoopregels** codes voor de periodieke verkoopregels die u wilt kunnen invoegen op verkoopdocumenten voor de klant.
5. Vul de overige velden in om te definiëren wanneer, hoe en waar de periodieke verkoopregels moeten worden gebruikt. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Periodieke verkoopregels invoegen op een verkoopfactuur
Als er terugkerende verkoopregels voor de klant zijn, kunt u deze invoegen op alle typen verkoopdocumenten, zoals een verkoopfactuur. Als u het betreffende bericht hebt geactiveerd, wordt u geïnformeerd als er periodieke verkoopregels zijn.
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Facturen** in en kies vervolgens de gerelateerde koppeling.
2. Open de verkoopfactuur waarin u een of meer standaardverkoopregels wilt invoegen.
3. Kies de actie **Periodieke verkoopregels ophalen**.
4. Kies op de pagina **Periodieke verkoopregels** de opzoekknop in het veld **Code** en selecteer een set standaardverkoopregels.

    > [!NOTE]
    > Als u de set doorlopende verkoopregels samen met de batchverwerking **Periodieke verkoopfacturen maken** wilt gebruiken, moet u ook de velden **Geldig vanaf datum** en **Geldig tot datum** op de pagina **Periodieke verkoopregels** invullen. Zie voor meer informatie [Meerdere verkoopfacturen maken op basis van standaardverkoopregels](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Kies de knop **OK** om de standaardverkoopregels op de factuur in te voegen, waar u deze zo kunt gebruiken of de gegevens kunt bewerken.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Meerdere verkoopfacturen maken op basis van standaardverkoopregels
U kunt de batchverwerking **Periodieke verkoopfacturen maken** gebruiken om verkoopfacturen te maken volgens de standaardverkoopregels die zijn toegewezen aan de klanten, en met boekingsdatums binnen de datums voor geldig vanaf en geldig tot die u op de standaardverkoopregels opgeeft.

> [!NOTE]
> Op de pagina **Periodieke verkoopregels** kunt u ook een betalingsmethode voor automatische incasso en machtiging voor automatische incasso opgeven. De verkoopfacturen die zijn gemaakt met de batchverwerking **Periodieke verkoopfacturen maken** bevatten dan informatie die nodig is om de betaling voor de verkoopfacturen met automatische incasso van SEPA te innen. Zie voor meer informatie [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodieke verkoopfacturen maken** in en kies vervolgens de gerelateerde koppeling.
2. Vul de velden op de pagina **Periodieke verkoopfacturen maken** in met de benodigde gegevens.
3. In het filterveld **Code** voert u de code in voor standaardverkoopregels die aan een klant worden toegewezen voor wie u verkoopfacturen wilt maken.
4. Kies de knop **OK**.

Verkoopfacturen worden gemaakt voor klanten met de opgegeven standaard klantverkoopcode en een waarde opgegeven voor automatische incasso-informatie voor het boeken op de opgegeven datum.

## <a name="see-also"></a>Zie ook  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
