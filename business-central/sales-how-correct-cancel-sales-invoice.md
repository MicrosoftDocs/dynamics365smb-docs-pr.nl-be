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
ms.date: 07/03/2020
ms.author: sgroespe
ms.openlocfilehash: 248e8fd461abd42cfdac257d7e519723350fe174
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534708"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Niet-betaalde verkoopfacturen corrigeren of annuleren

U kunt een geboekte verkoopfactuur corrigeren of annuleren. Dit is handig als u een fout maakt of als de klant om een wijziging vraagt.

> [!NOTE]  
> Nadat een geboekte verkoopfactuur gedeeltelijk of volledig is betaald, kunt u deze niet corrigeren of annuleren vanaf de geboekte verkoopfactuur zelf. In plaats hiervan moet u handmatig een verkoopcreditnota maken om de verkoop nietig te verklaren en de klant terug te betalen, optioneel aangestuurd met een inkoopretourorder. Zie [Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.

Op de pagina **Geboekte verkoopfactuur** kunt u de actie **Corrigeren** of de actie **Annuleren** kiezen om de acties uit te voeren die worden beschreven in de volgende tabel.

| Actie | Omschrijving |
| --- | --- |
| **Corrigeren** |De geboekte verkoopfactuur is geannuleerd. Een nieuwe verkoopfactuur met dezelfde gegevens wordt gemaakt. U kunt de correctie aanbrengen en dan doorgaan met het verkoopproces. De nieuwe verkoopfactuur heeft een ander nummer dan de aanvankelijke verkoopfactuur. Een correctieverkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Op de eerste geboekte verkoopfactuur worden de selectievakjes Geannuleerd en Betaald ingeschakeld. |
| **Annuleren** |De geboekte verkoopfactuur is geannuleerd. Een correctieverkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Op de eerste geboekte verkoopfactuur worden de selectievakjes Geannuleerd en Betaald ingeschakeld. |

Wanneer u een geboekte verkoopfactuur wijzigt of annuleert, wordt de corrigerende verkoopcreditnota toegepast op alle algemene grootboekposten en inventarisatieposten die werden gemaakt toen de aanvankelijke verkoopfactuur werd geboekt. Hiermee voert u een tegenboeking uit van de geboekte verkoopfactuur in uw financiële records en laat de gecorrigeerde verkoopcreditnota staan voor uw auditcontrole.  

> [!TIP]
> Als u een vooruitbetalingsfactuur hebt geboekt voor een verkoopfactuur die u vervolgens corrigeert of annuleert, moet u de vooruitbetaling ook corrigeren of annuleren. Zie voor meer informatie [Vooruitbetalingen storneren](finance-how-to-correct-prepayments.md).

## <a name="to-correct-a-posted-sales-invoice"></a>Om een geboekte verkoopfactuur te corrigeren

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopfacturen** in en kies vervolgens de desbetreffende koppeling.  
2. Selecteer de geboekte verkoopfactuur die u wilt corrigeren.

    > [!NOTE]  
    >   Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte verkoopfactuur niet corrigeren omdat deze al is gecorrigeerd of geannuleerd.
3. Kies op de pagina **Geboekte verkoopfactuur** de actie **Corrigeren**.  
4. Een nieuwe verkoopfactuur met dezelfde gegevens wordt gemaakt waar u de correctie kunt maken. Het veld **Geannuleerd** op de eerste geboekte verkoopfactuur is gewijzigd in **Ja**.

    Een verkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren.
5. Kies de actie **Corrigerende creditnota tonen** om de geboekte verkoopcreditnota weer te geven die de in eerste instantie geboekte verkoopfactuur nietig verklaart.

## <a name="to-cancel-a-posted-sales-invoice"></a>Om een geboekte verkoopfactuur te annuleren

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopfacturen** in en kies vervolgens de desbetreffende koppeling.  
2. Selecteer de geboekte verkoopfactuur die u wilt annuleren.

    > [!NOTE]  
    >   Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte verkoopfactuur niet annuleren omdat deze al is gecorrigeerd of geannuleerd.
3. Kies op de pagina **Geboekte verkoopfactuur** de actie **Annuleren**.

    Een verkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Het veld **Geannuleerd** op de eerste geboekte verkoopfactuur is gewijzigd in **Ja**.
4. Kies **Corrigerende creditnota tonen** om de geboekte verkoopcreditnota weer te geven die de in eerste instantie geboekte verkoopfactuur nietig verklaart.

### <a name="partial-invoice-posting-also-supported"></a>Gedeeltelijke factuurboeking wordt ook ondersteund

Als de annulering betrekking heeft op een gedeeltelijke factuurboeking, wordt de oorspronkelijke verkooporderregel bijgewerkt om de geannuleerde gefactureerde hoeveelheid weer te geven. De velden **Te factureren aantal** en **Aantal gefactureerd** op de gerelateerde verkooporderregel worden opnieuw ingesteld op de waarden vóór de gedeeltelijke boeking.

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
