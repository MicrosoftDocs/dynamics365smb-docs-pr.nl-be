---
title: Een geboekte verkoopfactuur corrigeren of annuleren
description: 'Dit artikel beschrijft hoe u een geboekte verkoopfactuur corrigeert, ongedaan maakt of annuleert en een verkoopcreditnota vereffent.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'undo, credit memo, return'
ms.date: 03/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Niet-betaalde verkoopfacturen corrigeren of annuleren

U kunt een onbetaalde geboekte verkoopfactuur corrigeren of annuleren, op voorwaarde dat deze niet volledig is verzonden. Dit is handig als u een fout maakt of als de klant om een wijziging verzoekt voordat de verzending is voltooid. In alle andere scenario's raden we u aan om rechtstreeks een corrigerende verkoopcreditnota te maken. Zie voor meer informatie [Een verkoopcreditnota maken op basis van een geboekte verkoopfactuur](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Nadat een geboekte verkoopfactuur gedeeltelijk of volledig is betaald, kunt u deze niet corrigeren of annuleren vanaf de geboekte verkoopfactuur zelf. In plaats hiervan moet u handmatig een verkoopcreditnota maken om de verkoop nietig te verklaren en de klant terug te betalen, optioneel aangestuurd met een inkoopretourorder. Zie [Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.

Het verschil tussen het annuleren of corrigeren van een geboekte verkoopfactuur die niet is betaald of verzonden, wordt beschreven in de volgende tabel.

| Actie | Omschrijving |
| --- | --- |
| **Annuleren** |De geboekte verkoopfactuur is geannuleerd. Een correctieverkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Op de eerste geboekte verkoopfactuur worden de selectievakjes **Geannuleerd** en **Betaald** ingeschakeld. |
| **Corrigeren** |De geboekte verkoopfactuur is geannuleerd. Er wordt een nieuwe verkoopfactuur met dezelfde informatie gemaakt, tenzij de geboekte verkooporder is geboekt vanuit een verkooporder. In dat geval raden we u aan om de geboekte verkoopfactuur te annuleren en vervolgens de correctie uit te voeren en het verkoopproces voort te zetten vanuit de oorspronkelijke verkooporder. <br/><br/>De nieuwe verkoopfactuur heeft een ander nummer dan de aanvankelijke verkoopfactuur. Een correctieverkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Op de eerste geboekte verkoopfactuur worden de selectievakjes **Geannuleerd** en **Betaald** ingeschakeld. |
|**Corrigerende creditnota maken**|Een nieuwe verkoopcreditnota met dezelfde gegevens wordt gemaakt. U kunt de nieuwe verkoopcreditnota aanpassen voordat u deze boekt, zodat deze wordt toegepast op de oorspronkelijke factuur wanneer u deze boekt. |

Wanneer u een geboekte verkoopfactuur wijzigt of annuleert, wordt de corrigerende verkoopcreditnota toegepast op alle algemene grootboekposten en inventarisatieposten die werden gemaakt toen de aanvankelijke verkoopfactuur werd geboekt. Hiermee voert u een tegenboeking uit van de geboekte verkoopfactuur in uw financiële records en laat de gecorrigeerde verkoopcreditnota staan voor uw auditcontrole.  

> [!TIP]
> Als u een vooruitbetalingsfactuur hebt geboekt voor een verkoopfactuur die u vervolgens corrigeert of annuleert, moet u de vooruitbetaling ook corrigeren of annuleren. Zie voor meer informatie [Vooruitbetalingen storneren](finance-how-to-correct-prepayments.md).

## Om een geboekte verkoopfactuur te annuleren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de geboekte verkoopfactuur die u wilt annuleren.

    > [!NOTE]  
    > Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte verkoopfactuur niet annuleren omdat deze al is gecorrigeerd of geannuleerd.
3. Kies op de pagina **Geboekte verkoopfactuur** de actie **Annuleren**.

    Een verkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren. Het veld **Geannuleerd** op de eerste geboekte verkoopfactuur is gewijzigd in **Ja**.
4. Kies **Corrigerende creditnota tonen** om de geboekte verkoopcreditnota weer te geven die de in eerste instantie geboekte verkoopfactuur nietig verklaart.

### Gedeeltelijke factuurboeking wordt ook ondersteund

Als de annulering betrekking heeft op een gedeeltelijke factuurboeking, wordt de oorspronkelijke verkooporderregel bijgewerkt om de geannuleerde gefactureerde hoeveelheid weer te geven. De velden **Te factureren aantal** en **Aantal gefactureerd** op de gerelateerde verkooporderregel worden opnieuw ingesteld op de waarden vóór de gedeeltelijke boeking.

## Om een geboekte verkoopfactuur te corrigeren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de geboekte verkoopfactuur die u wilt corrigeren.

    > [!NOTE]  
    >   Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte verkoopfactuur niet corrigeren omdat deze al is gecorrigeerd of geannuleerd.
3. Kies op de pagina **Geboekte verkoopfactuur** de actie **Corrigeren**.  

    > [!NOTE]
    > Als de verkoopfactuur is geboekt vanuit een verkooporder, raden we u aan deze verkoopfactuur te *annuleren* en vervolgens de correctie vanuit de originele verkooporder te verwerken. Als de originele verkooporder is verwijderd, bijvoorbeeld als deze volledig is verzonden, kunt u een nieuwe verkooporder maken met de actie **Document kopiëren**. Zie voor meer informatie [Een verkoopcreditnota maken door een geboekte verkoopfactuur te kopiëren](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Een nieuwe verkoopfactuur met dezelfde gegevens wordt gemaakt waar u de correctie kunt maken. Het veld **Geannuleerd** op de eerste geboekte verkoopfactuur is gewijzigd in **Ja**.

    Een verkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte verkoopfactuur nietig te verklaren.
5. Kies de actie **Corrigerende creditnota tonen** om de geboekte verkoopcreditnota weer te geven die de in eerste instantie geboekte verkoopfactuur nietig verklaart.

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Documenten verzenden via e-mail](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
