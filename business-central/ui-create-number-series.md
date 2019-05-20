---
title: Nummerreeksen maken | Microsoft Docs
description: Leren hoe u nummerreeksen instelt die unieke ID-codes toewijzen aan rekeningen en documenten in Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a650bb8dec324e94801da828d7e967b514ae3ca1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251389"
---
# <a name="create-number-series"></a>Nummerreeksen maken
Voor elk bedrijf dat u instelt, moet u unieke id-codes toewijzen aan zaken als grootboekrekeningen, klanten- en leveranciersrekeningen, facturen en overige documenten. De nummering is niet alleen belangrijk voor identificatie. Met een goed opgezet nummeringssysteem kan het bedrijf ook beter worden beheerd en geanalyseerd en kan het aantal fouten tijdens gegevensinvoer worden beperkt.

> [!NOTE]  
>   Het wordt aanbevolen om dezelfde nummerreekscodes te gebruiken die worden vermeld op de pagina **Nr.-reeksoverzicht** in het voorbeeldbedrijf CRONUS. Codes zoals *I-FACT+* lijken in het begin mogelijk betekenisloos, maar [!INCLUDE[d365fin](includes/d365fin_md.md)] kent een aantal standaardinstellingen die afhankelijk zijn van deze codes.

U maakt een nummeringssysteem door een of meer codes in te stellen voor elk soort hoofdgegevens of document. U kunt bijvoorbeeld een code instellen voor het nummeren van klanten, een andere code voor het nummeren van verkoopfacturen en weer een andere code voor het nummeren van documenten in algemene dagboeken. Nadat u een code hebt ingesteld, moet u minimaal één nummerreeksregel instellen. De nummerreeksregel bevat gegevens, zoals het eerste en laatste nummer in de reeks en de begindatum. U kunt meer dan één nummerreeksregel per nummerreekscode invoeren, met een andere begindatum voor elke regel. De reeks wordt opeenvolgend gebruikt, waarbij elke reeks wordt gestart op de betreffende begindatum.

U configureert normaal gesproken de nummerreeks zodanig dat automatisch het eerstvolgende nummer wordt ingevoegd op nieuwe kaarten of documenten die u maakt. U kunt echter ook een nummerreeks instellen die toestaat dat u handmatig het nieuwe nummer invoert. U geeft dit aan met het selectievakje **Handm. nummering**.

Als u meer dan één nummerreekscode wilt gebruiken voor één soort hoofdgegevens (als u bijvoorbeeld verschillende nummerreeksen voor verschillende artikelcategorieën wilt gebruiken), kunt u relaties tussen nummerreeksen gebruiken.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Werking van het veld Nr. in documenten en kaarten
In verkoop-, inkoop-, en transferdocumenten en op alle kaarten kan het veld **Nr.** automatisch vanuit een nummerreeks of handmatig worden ingevuld en kan het onzichtbaar worden gemaakt.

Het veld **Nr.** kan op drie manieren worden gevuld:

1. Als er slechts één nummerreeks voor het soort document of kaart bestaat waarbij het veld **Autom. nummering** is ingeschakeld en het veld **Handm. nummering** niet is ingeschakeld, wordt het veld automatisch gevuld met het volgende nummer in de reeks en is het veld **Nr.** niet zichtbaar.

    > [!NOTE]  
    > Als de nummerreeks niet werkt, bijvoorbeeld omdat de nummers op zijn, is het veld **Nr.** zichtbaar en kunt u handmatig een nummer invoeren of de problemen oplossen op de pagina **Nr.-reeksoverzicht**.

2. Als er meer dan één nummerreeks voor het soort document of kaart bestaat en het selectievakje **Autom. nummering** niet is ingeschakeld voor de nummerreeks die momenteel is toegewezen, is het veld **Nr.** zichtbaar en kunt u opzoeken naar de pagina **Nr.-reeksoverzicht** en de nummerreeks selecteren die u wilt gebruiken. Het volgende nummer in de reeks wordt dan ingevoegd in het **Nr.** veld.

3. Als u geen nummerreeks voor het type document of kaart hebt ingesteld of als het veld **Handm. nummering** is ingeschakeld voor de nummerreeks, is het veld **Nr.** zichtbaar en moet u het nummer handmatig invoeren. U kunt maximaal 20 tekens invoeren (cijfers en/of letters).

Wanneer u een nieuwe kaart of document opent waarvoor een nummerreeks bestaat, wordt de relevante pagina **Instelling nummerreeks** geopend, zodat u een nummerreeks kunt instellen voor dat type document of kaart voordat u doorgaat met verdere gegevensinvoer.

> [!NOTE]  
> Als u handmatige nummering moet inschakelen op, bijvoorbeeld, nieuwe artikelkaarten die zijn gemaakt met een gegevensmigratieproces, waarop het **Nr.** standaard is verborgen, gaat u naar de pagina **Voorraadinstellingen** en kiest u het veld **Artikelnrs.** om de gerelateerde nummerreeks te openen en in te stellen op **Handm. nummering**.

## <a name="to-create-a-new-number-series"></a>Een nieuwe nummerreeks maken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Nr.-reeksen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul op de nieuwe regel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Instellen waar een nummerreeks wordt gebruikt
In de volgende procedure wordt beschreven hoe u nummerreeksen instelt voor de module Verkoop. De stappen zijn vergelijkbaar voor andere modules.
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkopen en Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Verkopen en klanten** op het sneltabblad **Nummerreeksen** de gewenste nummerreeksen voor iedere verkoopkaart of -document.

Het geselecteerde nummer wordt nu ingevuld op het veld **Nr.** op de kaart of het document, afhankelijk van de instellingen die u hebt ingevoerd op de nummerreeksregel.

## <a name="to-create-relationships-between-number-series"></a>Relaties maken tussen nummerreeksen
Als u meerdere nummerreekscodes hebt ingesteld voor hetzelfde soort basisgegevens of transacties, kunt u relaties tussen de codes instellen. Met deze functie kunt u een code kiezen wanneer u een nummer gebruikt.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Nr.-reeksen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel met de nummerreeks waarvoor u relaties wilt instellen en kies vervolgens **Relaties**.
3. Geef in het veld **Reeks** de code op voor de nummerreeks die u wilt koppelen aan de reeks die u in stap 2 hebt geselecteerd.
4. Voeg een regel toe voor elke code die u wilt koppelen aan de geselecteerde nummerreeksen.
5. Sluit de pagina.

Wanneer u nu iets instelt waarvoor u een nummer nodig hebt, kunt u de relaties gebruiken die u hebt ingesteld om te kiezen tussen de gekoppelde nummerreeksen.

## <a name="see-also"></a>Zie ook
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
