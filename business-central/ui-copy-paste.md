---
title: Gegevens kopiëren en plakken
description: Velden en rijen uit Business Central-pagina's kopiëren en ergens anders plakken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a77c5bcadb15cd1180fc102a1f15881d0cc5db5a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315672"
---
# <a name="copy-and-paste-faq"></a>Veelgestelde vragen over kopiëren en plakken
U kunt een of meer rijen (records) uit een lijst of een enkel veld op een pagina kopiëren en vervolgens wat u hebt gekopieerd, plakken op dezelfde pagina, een andere pagina of een extern document (zoals Microsoft Excel en Outlook-e-mail). Als u wilt kopiëren, drukt u op CTRL+C (cmd+C in MacOs) op het toetsenbord. Als u wilt plakken, drukt u op CTRL+V (cmd+V in MacOs).

Er zijn verschillende andere toetsenbordsneltoetsen voor het kopiëren en plakken die u helpen tijd te besparen wanneer u gegevens invoert. Zie voor meer informatie hierover [Toetsenbordsneltoetsen](keyboard-shortcuts.md#CopyRows).

In dit artikel worden veelgestelde vragen beantwoord over kopiëren en plakken.  

## <a name="what-can-i-copy-and-paste"></a>Wat kan ik kopiëren en plakken?
- Een of meer rijen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopiëren naar dezelfde lijst of naar een lijst met identieke kolommen.
- Een of meer rijen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopiëren en plakken in Excel of andere toepassingen.
- Een of meer rijen in Excel kopiëren en plakken in een [!INCLUDE[d365fin](includes/d365fin_md.md)]-lijst.
- De waarde van een afzonderlijk veld in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopiëren en deze ergens anders plakken.

## <a name="does-copy-and-paste-work-with-tiles"></a>Werkt kopiëren en plakken met tegels?
Ja, maar alleen voor een enkele geselecteerde tegel.

## <a name="how-do-i-copy-a-row"></a>Hoe kopieer ik een rij?
Als u één rij wilt kopiëren, selecteert u deze en drukt u op Ctrl+C.

Als u meerdere rijen wilt kopiëren, kunt u:
- Op Ctrl drukken en op een andere rij klikken of op Shift drukken en klikken om de rij en alle rijen ertussenin te selecteren. Zie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#CopyRows) voor meer muis- en toetsenbordcombinaties voor het selecteren van rijen.
- Selecteer ![Meer opties weergeven](media/show-more-options-icon.png "pictogram Meer opties weergeven") in de eerste kolom, kies **Meer selecteren**, schakel het selectievakje in naast elke rij die u wilt kopiëren, en druk op Ctrl+C.

## <a name="how-do-i-paste-rows"></a>Hoe plak ik rijen?
Selecteer een lege rij, met focus in een willekeurige cel, en druk vervolgens op Ctrl + V.

Als u bestaande rijen wilt vervangen, selecteert u de rijen en drukt u op Ctrl+V. In dit geval kunt u alleen hetzelfde aantal rijen plakken als u hebt geselecteerd.

> [!NOTE]
> De lijst waarin u plakt, moet bewerkbaar zijn.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email"></a>Kan ik rijen plakken in een Outlook-e-mailbericht?
Ja. Dit wordt geplakt als een keurig geformatteerde tabel die de inspringing, numerieke uitlijning en kleur behoudt, zoals u zou zien in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>In welke lijsten kan ik rijen kopiëren en plakken?
U kunt rijen in een willekeurige lijst plakken, inclusief werkbladen, feitenblokken of lijsten die zijn ingesloten in een pagina (zoals regels van een verkooporder). Als u rijen wilt plakken, moet de lijst echter bewerkbaar zijn.

Op sommige pagina's kan het toepassingsontwerp voorkomen dat u rijen plakt. Neem contact op met de beheerder of toepassingsontwikkelaar om de [eigenschap Bewerkbaar](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) op de pagina te wijzigen of de eigenschap [PasteIsValid](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) te wijzigen in de brontabel.

## <a name="on-which-clients-is-copy-and-paste-available"></a>In welke clients is kopiëren en plakken beschikbaar?
Kopiëren en plakken is beschikbaar in de browser of de [!INCLUDE[d365fin](includes/d365fin_md.md)]-app voor Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Wat is het maximale aantal rijen dat kan worden gekopieerd?
U kunt zoveel rijen kopiëren als u in beeld hebt geschoven. Als u bijvoorbeeld alle 1000 rijen op een pagina wilt kopiëren, moet u eerst naar de onderzijde van de pagina schuiven en wachten tot de rijen worden weergegeven voordat u kopieert. Het maximale aantal rijen dat u kunt kopiëren wordt alleen beperkt door het geheugen van uw apparaat.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Moet ik exact hetzelfde aantal kolommen hebben wanneer ik rijen plak?
Ja. Ongeacht of u rijen kopieert uit [!INCLUDE[d365fin](includes/d365fin_md.md)], uit Excel of uit een andere tabelbron, de rijen die u plakt in [!INCLUDE[d365fin](includes/d365fin_md.md)], moeten exact overeenkomende kolommen hebben; niet meer en niet minder.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Waarom krijg ik fouten wanneer ik rijen plak?
Wanneer u plakt in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt elke rij gecontroleerd om ervoor te zorgen dat waarden in elke kolom geldig zijn. Als een kolom een waarde bevat die niet geldig is, wordt het plakken gestopt en wordt een foutbericht weergegeven. Als u dit wilt vermijden, zorgt u dat de kolommen geldige waarden bevatten voordat u deze plakt.


## <a name="see-also"></a>Zie ook
[Assisterende functies](ui-accessibility.md)  
[Aan de slag](product-get-started.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Veelgestelde vragen](across-faq.md)  
