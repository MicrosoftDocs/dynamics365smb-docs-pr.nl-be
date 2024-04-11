---
title: Periodieke standaardverkoopregels
description: Stel veelgebruikte verkoopregels in om in te voegen in verkoopdocumenten en snel de regels in te vullen met standaardgegevens.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, sell, replenishment'
ms.search.form: 172
ms.date: 02/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Periodieke verkopen maken

Als u vaak verkoopregels met dezelfde informatie moet maken, kunt u standaardregels instellen die u dan kunt invoegen op periodieke verkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders.  

## Periodieke verkoopregels instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodieke verkoopregels** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Periodieke verkoopregels** de actie **Nieuw**.  
3. Vul de benodigde velden in op het sneltabblad **Algemeen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Voer op het sneltabblad **Regels** gegevens in de velden in om verkoopregels voor te bereiden die de standaardregels reflecteren die u verwacht te gebruiken als terugkerende regels in verkoopdocumenten.  

> [!NOTE]
> U kunt geen prijzen definiëren op periodieke verkoopregels, omdat de prijzen, kortingen, enzovoort, op de werkelijke verkoopdocumenten worden berekend nadat u de periodieke verkoopregels hebt ingevoegd.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Periodieke verkoopregels aan een klant toewijzen

Wijs een of meer periodieke verkoopregels aan een klant toe zodat deze beschikbaar zijn om te worden ingevoegd op verkoopdocumenten voor die klant.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de projectkaart voor een relevante klant.
3. Kies de actie **Periodieke verkoopregels**.
4. Selecteer op de pagina **Periodieke verkoopregels** codes voor de periodieke verkoopregels die u wilt kunnen invoegen op verkoopdocumenten voor de klant.
5. Vul de overige velden in om te definiëren wanneer, hoe en waar de periodieke verkoopregels moeten worden gebruikt.  

    Als u van plan bent de set periodieke verkoopregels samen met de batchverwerking **Periodieke verkoopfacturen maken** te gebruiken, gebruikt u de velden **Geldig vanaf datum** en **Geldig tot datum** wanneer de periodieke verkoopregels worden gebruikt voor het maken van facturen. Zie voor meer informatie [Meerdere verkoopfacturen maken op basis van standaardverkoopregels](sales-how-work-standard-lines.md#create-multiple-sales-invoices-based-on-recurring-sales-lines).

    U kunt ook een betalingsmethode voor automatische incasso en machtiging voor automatische incasso opgeven. De verkoopfacturen die zijn gemaakt met de batchverwerking **Periodieke verkoopfacturen maken** bevatten dan de informatie die nodig is om de betaling voor de verkoopfacturen met automatische incasso van SEPA te innen. Zie voor meer informatie [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md).

6. Selecteer in de vier velden, waarin u selecteert hoe de regels worden ingevoegd in vier documenttypen, een van de volgende opties:

|Optie|Omschrijving|
|------|-----------|
|**Handmatig**|U moet handmatig een terugkerende verkoopregel zoeken en invoegen die bestaat voor de klant.|
|**Automatisch**|Als er meerdere terugkerende verkoopregels voor de klant zijn, ontvangt u een bericht van waaruit u er een kunt kiezen om in te voegen. Als er slechts één terugkerende verkoopregel bestaat, wordt deze automatisch ingevuld.<br /><br />Dit werkt alleen als het nieuwe document is gemaakt op basis van een documentenlijst, bijvoorbeeld door kiezen van de actie **Nieuw** op de pagina **Verkooporders**. Het werkt niet als het document bijvoorbeeld is gemaakt op basis van een klantenkaart.|
|**Altijd vragen**|Er wordt een bericht weergegeven en alle bestaande terugkerende verkoopregels worden weergegeven zodat u er een kunt selecteren.

## Periodieke verkoopregels invoegen op een verkoopfactuur

Als er periodieke verkoopregels voor de klant zijn, kunt u deze invoegen of laten invoegen op alle typen verkoopdocumenten, zoals een verkoopfactuur. Als u de **Altijd vragen**-opties hebt geactiveerd terwijl u periodieke verkoopregels toewijst aan klanten, wordt u geïnformeerd als er periodieke verkoopregels bestaan.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Open de verkoopfactuur waarin u een of meer standaardverkoopregels wilt invoegen.
3. Kies de actie **Periodieke verkoopregels ophalen**.
4. Kies op de pagina **Periodieke verkoopregels** de opzoekknop in het veld **Code** en selecteer een set standaardverkoopregels.
5. Kies de knop **OK** om de standaardverkoopregels op de factuur in te voegen, waar u deze zo kunt gebruiken of de gegevens kunt bewerken.

## Meerdere verkoopfacturen maken op basis van periodieke verkoopregels

U kunt de batchverwerking **Periodieke verkoopfacturen maken** gebruiken om verkoopfacturen te maken volgens de standaardverkoopregels die zijn toegewezen aan de klanten, en met boekingsdatums binnen de datums voor geldig vanaf en geldig tot die u op de standaardverkoopregels opgeeft.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Periodieke verkoopfacturen maken** in en kies vervolgens de gerelateerde koppeling.
2. Vul de velden op de pagina **Periodieke verkoopfacturen maken** in met de benodigde gegevens.
3. In het filterveld **Code** voert u de code in voor standaardverkoopregels die aan een klant worden toegewezen voor wie u verkoopfacturen wilt maken.
4. Kies de knop **OK**.

Verkoopfacturen worden gemaakt voor klanten met de opgegeven standaard klantverkoopcode en een waarde opgegeven voor automatische incasso-informatie voor het boeken op de opgegeven datum.

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Periodieke inkoopregels maken](purchasing-how-work-recurring-purchase-lines.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
