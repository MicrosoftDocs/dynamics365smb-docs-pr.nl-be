---
title: Geboekte verkoopfacturen corrigeren of annuleren | Microsoft Docs
description: Beschrijft hoe u een geboekte verkoopfactuur corrigeert, ongedaan maakt of annuleert en een verkoopcreditnota vereffent.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a74dcd8e2d0409ca7385ea8a47a78dd9a74561b6
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Niet-betaalde verkoopfacturen corrigeren of annuleren
U kunt een geboekte verkoopfactuur corrigeren of annuleren. Dit is handig als u een fout maakt of als de klant om een wijziging vraagt.

> [!NOTE]  
>   Nadat een geboekte verkoopfactuur gedeeltelijk of volledig is betaald, kunt u deze niet corrigeren of annuleren vanaf de geboekte verkoopfactuur zelf. In plaats hiervan moet u handmatig een verkoopcreditnota maken om de verkoop nietig te verklaren en de klant terug te betalen, optioneel aangestuurd met een inkoopretourorder. Zie [Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.

Op de pagina **Geboekte verkoopfactuur** kunt u de actie **Corrigeren** of de actie **Annuleren** kiezen om de acties uit te voeren die worden beschreven in de volgende tabel.

| Actie | Omschrijving |
| --- | --- |
| **Corrigeren** |De geboekte verkoopfactuur is geannuleerd. Een nieuwe verkoopfactuur met dezelfde gegevens wordt gemaakt. U kunt de correctie aanbrengen en dan doorgaan met het verkoopproces. De nieuwe verkoopfactuur heeft een ander nummer dan de aanvankelijke verkoopfactuur. Een correctieverkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Op de eerste geboekte verkoopfactuur worden de selectievakjes Geannuleerd en Betaald ingeschakeld. |
| **Annuleren** |De geboekte verkoopfactuur is geannuleerd. Een correctieverkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Op de eerste geboekte verkoopfactuur worden de selectievakjes Geannuleerd en Betaald ingeschakeld. |

Wanneer u een geboekte verkoopfactuur wijzigt of annuleert, wordt de corrigerende verkoopcreditnota toegepast op alle algemene grootboekposten en inventarisatieposten die werden gemaakt toen de aanvankelijke verkoopfactuur werd geboekt. Hiermee voert u een tegenboeking uit van de geboekte verkoopfactuur in uw financiële records en laat de gecorrigeerde verkoopcreditnota staan voor uw auditcontrole.

## <a name="to-correct-a-posted-sales-invoice"></a>Om een geboekte verkoopfactuur te corrigeren
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de geboekte verkoopfactuur die u wilt corrigeren.

    > [!NOTE]  
    >   Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte verkoopfactuur niet corrigeren omdat deze al is gecorrigeerd of geannuleerd.
3. Kies op de pagina **Geboekte verkoopfactuur** de actie **Corrigeren**.  
4. Een nieuwe verkoopfactuur met dezelfde gegevens wordt gemaakt waar u de correctie kunt maken. Het veld **Geannuleerd** op de eerste geboekte verkoopfactuur is gewijzigd in **Ja**.

    Een verkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren.
5. Kies de actie **Corrigerende creditnota tonen** om de geboekte verkoopcreditnota weer te geven die de in eerste instantie geboekte verkoopfactuur nietig verklaart.

## <a name="to-cancel-a-posted-sales-invoice"></a>Om een geboekte verkoopfactuur te annuleren
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de geboekte verkoopfactuur die u wilt annuleren.

    > [!NOTE]  
    >   Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte verkoopfactuur niet annuleren omdat deze al is gecorrigeerd of geannuleerd.
3. Kies op de pagina **Geboekte verkoopfactuur** de actie **Annuleren**.

    Een verkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Het veld **Geannuleerd** op de eerste geboekte verkoopfactuur is gewijzigd in **Ja**.
4. Kies **Corrigerende creditnota tonen** om de geboekte verkoopcreditnota weer te geven die de in eerste instantie geboekte verkoopfactuur nietig verklaart.

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

