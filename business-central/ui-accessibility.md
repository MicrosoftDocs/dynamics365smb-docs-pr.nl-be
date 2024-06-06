---
title: Ondersteunende functies
description: Dit artikel bevat informatie over sneltoetsen en andere ondersteunende functies in Business Central voor mensen met een handicap.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accessibility, shortcuts, charts, tooltips, screen reader'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="accessibility-and-keyboard-shortcuts"></a>Toegankelijkheid en sneltoetsen

Dit artikel bevat informatie over de functies die [!INCLUDE[prod_short](includes/prod_short.md)] toegankelijk maken voor mensen met een handicap. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt de volgende toegankelijkheidsfuncties:  

- Toetsenbordsneltoetsen. Zie [Toetsenbordsneltoetsen](keyboard-shortcuts.md).
- Aanraak- en penbewegingen op tablets en telefoons. Zie [Aanraak- en penbewegingen](touch-gestures.md).
- Navigatie  
- Koppen  
- Alternatieve tekst voor afbeeldingen en koppelingen  
- Ondersteuning voor algemene ondersteunende technologieën 
- In- en uitzoomen op een pagina
- Knopinfo over elementen in de gebruikersinterface

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="navigation"></a><a name="Navigation"></a>Navigatie
  
U kunt verschillende combinaties van Tab, Shift en pijltoetsen van uw toetsenbord gebruiken om tussen elementen op een pagina te schakelen. Elementen zijn onder meer acties, velden en kolommen, onderdelen en andere besturingselementen. Over het algemeen kunt u <kbd>Tab</kbd> of <kbd>Shift</kbd>+<kbd>Tab</kbd> selecteren om naar het volgende of vorige element te gaan.

Wanneer u zich concentreert op een gebied dat acties bevat, zoals de navigatiebalk boven aan het rolcentrum of de actiebalk op andere pagina's, gebruikt u de pijltjestoetsen om door de verschillende acties en groepen te bladeren. Selecteer <kbd>Enter</kbd> voor een groep om de onderliggende acties te openen en ga verder met het gebruik van de pijltjestoetsen. Druk op <kbd>Tab</kbd> of <kbd>Shift</kbd>+<kbd>Tab</kbd> om het actiegebied te verlaten.

Met Tab kunt u ook schakelen tussen de hoofdbrowserpagina en dialoogvensters waarin bijvoorbeeld om bevestiging wordt gevraagd of de aanmeldingspagina.  

## <a name="headings-in-content"></a><a name="Headings"></a>Koppen in inhoud

In de HTML-bron voor [!INCLUDE[prod_short](includes/prod_short.md)]-inhoud worden tags gebruikt om gebruikers van ondersteunende technologie te helpen de structuur en inhoud van de pagina te begrijpen. Op pagina's met lijsten worden de kolommen bijvoorbeeld gedefinieerd in TH-tags en de kolomkoppen worden ingesteld met het kenmerk TITLE in de tag. Bijschriften voor elementen, zoals sneltabbladen, feitenblokken en velden, zijn opgenomen in koptags (H1, H2, H3 en H4).  

## <a name="image-and-links"></a><a name="Images"></a>Afbeelding en koppelingen

Een omschrijvende tekst voor afbeeldingen wordt ingesteld met het kenmerk ALT in de IMG-tag. Een omschrijvende tekst voor hyperlinks wordt ingesteld met het titelkenmerk in de A-tag.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a>Ondersteunende technologieën

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt meerdere ondersteunende technologieën, zoals hoog contrast, schermlezers en spraakherkenningssoftware. Sommige ondersteunende technologieën werken mogelijk niet goed met bepaalde elementen op [!INCLUDE[prod_short](includes/prod_short.md)]-pagina's.  

## <a name="zoom"></a><a name="zoom"></a>In-/uitzoomen

De meeste browsers gebruiken standaardsneltoetsen om in en uit te zoomen op de huidige pagina. Deze sneltoetsen zijn niet specifiek voor [!INCLUDE [prod_short](includes/prod_short.md)], maar ze werken als u [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt in een browser. Zie voor een lijst met ondersteunde sneltoetsen [Sneltoetsen voor het in- en uitzoomen](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>Knopinfo

Knopinfo is beschikbaar voor de meeste elementen in de gebruikersinterface, zoals paginavelden en kolommen, acties, tegels met indicatiestapels en grafieken. Knopinfo biedt extra tekst waarin een element wordt uitgelegd, zodat u het doel ervan beter kunt begrijpen. 

Knopinfo is op verschillende manieren toegankelijk, afhankelijk van de client (web of mobiel) en het apparaat waarmee u werkt. Gebruik de volgende tabel als richtlijn. Sommige knopinfo kan worden gelezen door schermlezers. In dit geval opent u de knopinfo zoals beschreven in de tabel en gebruikt u vervolgens de schermlezer om naar de tooltip te navigeren, zoals u met elk ander element zou doen.

#### <a name="accessing-tooltips"></a>Toegang tot knopinfo

|Element|Muisactie voor webclient|Sneltoets voor webclient|Aanraakgebaar op tablet/telefoon voor mobiele app|Ondersteuning voor schermlezer|
|-------|-----------------|------------|--------------------------|---------------------|
|Paginavelden en kolomkoppen|De muisaanwijzer op het veldbijschrift of de kolomkop plaatsen of hierop klikken|Focus naar de veld- of kolomkop verplaatsen en <kbd>Alt</kbd>+<kbd>Pijl-omhoog</kbd> selecteren|Tikken op het veldbijschrift |ja|
|Grafiekelementen, zoals een staaf, lijn, taartpunt|De muisaanwijzer op het element plaatsen|De focus naar het element verplaatsen, bijvoorbeeld met pijltoetsen|Op het element tikken en vasthouden|ja|
|Acties|De muisaanwijzer op de actie plaatsen|geen|geen |nee|
|Tegels met indicatiestapels|De muisaanwijzer op de tegel plaatsen |geen|geen|nee|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information"></a>Meer informatie over toegankelijkheid

Meer informatie over toegankelijkheid voor Microsoft-producten en ondersteunende technologieën vindt u op de site [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).

## <a name="see-also"></a>Zie ook

[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Veelgestelde vragen](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
