---
title: Standaard terugkerende inkoopregels
description: Stel veelgebruikte inkoopregels in om in te voegen in inkoopdocumenten en snel de regels in te vullen met standaardgegevens.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 07/06/2022
ms.author: a-reishima
---
# <a name="create-recurring-purchase-lines" />Periodieke inkoopregels maken

Als u vaak inkoopregels met dezelfde informatie moet maken, kunt u standaardregels instellen die u dan kunt invoegen op periodieke inkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders.

## <a name="set-up-recurring-purchase-lines" />Periodieke inkoopregels instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodieke inkoopregels** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Periodieke inkoopregels** de actie **Nieuw**.
3. Vul de benodigde velden in op het sneltabblad **Algemeen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Voer op het sneltabblad **Regels** de gegevens in de velden in die de standaardregels reflecteren die u verwacht te gebruiken als periodieke regels in inkoopdocumenten.

> [!NOTE]
> U kunt geen prijzen definiëren op periodieke inkoopregels, omdat de prijzen, kortingen, enzovoort, op de werkelijke inkoopdocumenten worden berekend nadat u de periodieke inkoopregels hebt ingevoegd.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-purchase-lines-to-a-vendor" />Periodieke inkoopregels toewijzen aan een leverancier

Wijs een of meer periodieke inkoopregels aan een leverancier toe zodat deze beschikbaar zijn om te worden ingevoegd op inkoopdocumenten van die leverancier.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een relevante leverancier.
3. Kies de actie **Periodieke inkoopregels**.
4. Selecteer op de pagina **Periodieke inkoopregels** codes voor de periodieke inkoopregels die u wilt kunnen invoegen op inkoopdocumenten voor de leverancier.
5. Vul de overige velden in om te definiëren wanneer, hoe en waar de periodieke inkoopregels moeten worden gebruikt.
6. Selecteer in de vier velden waarin u selecteert hoe de regels worden ingevoegd in elk documenttype, een van de volgende opties:

|Optie|Omschrijving|
|------|-----------|
|**Handmatig**|U moet handmatig een periodieke inkoopregel zoeken en invoegen die bestaat voor de leverancier.|
|**Automatisch**|Als er meerdere periodieke inkoopregels voor de leverancier zijn, ontvangt u een bericht van waaruit u er een kunt kiezen om in te voegen. Als er slechts één periodieke inkoopregel bestaat, wordt deze automatisch ingevuld.<br /><br />Dit werkt alleen als het nieuwe document is gemaakt op basis van een documentenlijst, bijvoorbeeld door kiezen van de actie **Nieuw** op de pagina **Inkooporders**. Het werkt niet als het document bijvoorbeeld is gemaakt op basis van een leverancierskaart.|
|**Altijd vragen**|Er wordt een bericht weergegeven en alle bestaande periodieke inkoopregels worden weergegeven zodat u er een kunt selecteren.

## <a name="insert-recurring-purchase-lines-on-a-purchase-invoice" />Periodieke inkoopregels invoegen op een inkoopfactuur

Als er periodieke inkoopregels voor de leverancier zijn, kunt u deze invoegen of automatisch laten invoegen op alle typen inkoopdocumenten, zoals een inkoopfactuur. Als u de **Altijd vragen**-opties hebt geactiveerd terwijl u periodieke inkoopregels toewijst aan leveranciers, wordt u geïnformeerd als er periodieke inkoopregels bestaan.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Open de inkoopfactuur waarin u een of meer standaardinkoopregels wilt invoegen.
3. Kies de actie **Periodieke inkoopregels ophalen**.
4. Kies op de pagina **Periodieke inkoopregels** de opzoekknop in het veld **Code** en selecteer een set standaardinkoopregels.
5. Kies de knop **OK** om de standaardinkoopregels op de factuur in te voegen, waar u deze opnieuw kunt gebruiken of de gegevens kunt bewerken.

## <a name="see-also" />Zie ook

[Inkoop](purchasing-manage-purchasing.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Periodieke verkopen maken](sales-how-work-standard-lines.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
