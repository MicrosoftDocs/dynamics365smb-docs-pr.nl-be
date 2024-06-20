---
title: De rapportlay-out instellen
description: Meer informatie over hoe u de lay-out instelt die op een rapport wordt gebruikt bij het bekijken en afdrukken van een rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 08/12/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# De lay-out instellen die door een rapport wordt gebruikt

> **GELDT VOOR:** Business Central Online, Business Central on-premises releasewave 1 van 2022 en hoger. Ga voor eerdere versies naar [hier](ui-how-change-layout-currently-used-report.md).

Een rapportlay-out bepaalt het uiterlijk van een rapport. Het bepaalt welke gegevensvelden van een rapportgegevensset worden weergegeven, hoe ze zijn gerangschikt, opgemaakt en meer. Een rapport kan meerdere lay-outs hebben, waartussen u indien nodig kunt schakelen.

Wanneer er meerdere bedrijven in de toepassing zijn, worden de lay-outs per bedrijf ingesteld. Dus hetzelfde rapport in het ene bedrijf kan een andere lay-out hebben in een ander bedrijf.

## Aan de slag

Er zijn enkele manieren om in te stellen welke lay-out een rapport gebruikt. Elke manier heeft voordelen, afhankelijk van wat u wilt doen: 

- Vanaf de rapportaanvraagpagina

  Wanneer u een rapport instelt om uit te voeren, bevat de rapportaanvraagpagina het veld **Rapportlay-out** dat de huidige standaardlay-out toont die door het rapport wordt gebruikt. U kunt dit veld gebruiken om tijdelijk over te schakelen naar een andere beschikbare lay-out van het rapport dat u uitvoert. Nadat u het rapport hebt uitgevoerd, keert de lay-out terug naar de standaardlay-out. Zie voor meer informatie [Rapporten uitvoeren en afdrukken](ui-work-report.md#switching-the-report-layout).

- Vanaf de pagina **Selectie rapportlay-out**

  De pagina **Selectie rapportlay-out** toont een lijst met alle rapporten. Deze pagina geeft aan wat de huidige standaardlay-out van een rapport is. U kunt lay-outs instellen in verschillende bedrijven, zonder dat u hoeft weg te gaan van het bedrijf waarmee u werkt.

- Vanaf de pagina **Rapportlay-outs** De pagina **Rapportlay-outs** toont alle beschikbare lay-outs voor elk rapport in het huidige bedrijf. De pagina wordt ook gebruikt om de standaardlay-out voor rapporten op te geven. Het is gemakkelijk om een specifieke lay-out te vinden door de lijst te sorteren of te filteren. Zodra u de lay-out hebt gevonden, kunt u deze instellen voor een rapport met een enkele selectie.

  > [!NOTE]
  > U kunt de pagina **Rapportlay-outs** niet gebruiken voor Word- en RDLC-lay-outs die zijn gemaakt met de verouderde **Aangepaste lay-outs**-functie. U ziet u deze aangepaste lay-outs niet eens vermeld op de pagina **Rapportlay-outs**. Voor deze lay-outs kunt u ze alleen instellen met de pagina **Selectie rapportlay-out**.

## De lay-out vanaf de pagina Rapportlay-outs instellen

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Zoek de lay-out in de lijst, selecteer de lay-out en selecteer vervolgens de actie **Standaard instellen** boven aan de pagina.

## De lay-out vanaf de pagina Selectie rapportlay-out instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Selectie rapportlay-out** in en kies vervolgens de gerelateerde koppeling.
  
   De pagina bevat een overzicht van alle rapporten die beschikbaar zijn voor het bedrijf dat in het veld **Bedrijf** boven aan de pagina is aangegeven. Met het veld **Lay-outbeschrijving** wordt de lay-out aangegeven die momenteel door het rapport wordt gebruikt.
2. Stel het veld **Bedrijf** bovenaan in op het bedrijf dat het rapport bevat.
3. Zoek en selecteer het rapport in de lijst en voer een van de volgende stappen uit:

   - Als de lay-out waarnaar u wilt overschakelen van een ander type is dan de huidige lay-out, selecteert u het veld **Lay-outtype** en kiest u vervolgens het type lay-out dat u op het rapport wilt instellen. 
   - Als de lay-out waarnaar u wilt overschakelen van hetzelfde type is als de huidige lay-out, selecteert u de actie **Lay-out selecteren** bovenaan.

4. In de pagina **Rapportlay-outs** selecteert u de lay-out en selecteer vervolgens **OK**.

## Terugkeren naar de oorspronkelijke standaardlay-out

Rapporten zijn ontworpen om standaard een lay-out te gebruiken. U kunt terugschakelen naar de oorspronkelijke standaardlay-out vanaf de pagina **Selectie rapportlay-out**. Selecteer gewoon het rapport en selecteer vervolgens de actie **Standaardselectie herstellen** boven aan de pagina.

## Zie ook

[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
