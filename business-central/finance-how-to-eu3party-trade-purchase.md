---
title: EU-inkooptransacties van derde partijen
description: In dit artikel wordt uitgelegd hoe u inkooptransacties van derden in de Europese Unie (EU) instelt en gebruikt.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/07/2023
ms.author: altotovi
---

# <a name="eu-third-party-purchase-transactions"></a>EU-inkooptransacties van derde partijen

Handel met derden in de Europese Unie (EU) vindt plaats wanneer u een inkoopfactuur ontvangt van een klant in een EU-land/-regio en de producten naar een ander EU-land/-regio worden verzonden zonder het land/regio van verblijf binnen te gaan. Het transactiebedrag kan afzonderlijk worden geïdentificeerd en gerapporteerd om te voldoen aan de vereisten voor btw van sommige EU-landen/regio's en vereisten voor het btw-informatie-uitwisselingssysteem (VIES). Microsoft Dynamics 365 Business Central maakt het mogelijk om aankooptransacties in te stellen als EU-handel van derden. Geboekte EU-transacties van derden kunnen worden gefilterd in btw-overzichten en worden uitgesloten van het bedrag in de kolom **Verkoop aan klant** van het rapport **Btw - Intracommunautaire opgave**.

Zelfs als de functie vooraf is geïnstalleerd als een extensie, is deze niet standaard geactiveerd. Volg deze stappen om de functie in te schakelen.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), ga naar de werkruimte **Functiebeheer** en selecteer vervolgens de gerelateerde koppeling.
2. Zoek en selecteer in de lijst **Functie-update: de bestaande functionaliteit voor inkoop met externe EU-partij vervangen door de nieuwe extensie Inkoop handel met externe EU-partij**.
3. Selecteer in de kolom **Geactiveerd voor** **Alle gebruikers**.

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>EU-handelsfunctionaliteit voor derden voor een aankoop inschakelen

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-instelling** in en selecteer vervolgens de gerelateerde koppeling.
2. Markeer op de pagina **Btw-instelling** het veld **Inkoop handel met externe EU-partij inschakelen** .

## <a name="use-eu-third-party-trade-functionality"></a>EU-handelsfunctionaliteit van derden gebruiken

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfactuur** (of een ander inkoopdocument) in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer een bestaande inkoopfactuur of selecteer **Nieuw** om een ​​nieuwe te maken.
3. Schakel op het sneltabblad **Factuurdetails** het selectievakje **ABC-/Driehoekstransacties** in.
4. Selecteer **OK**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>EU-handelsrecords van derden opnemen of uitsluiten op de btw-aangifte

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-aangifte** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Btw-aangifte** een van de volgende opties om EU-handelsrecords van derden weer te geven met behulp van het veld **Filter op handel met externe EU-partij**.

    | Optie | Omschrijving |
    |--------|-------------|
    | Alle | Toon alle records, ongeacht of het veld **ABC-/Driehoekstransacties** in documenten was gemarkeerd. |
    | EU extern | Toon alleen records, ongeacht of het veld **ABC-/Driehoekstransacties** in documenten was gemarkeerd. |
    | Niet EU extern | Toon alleen records waarbij het veld **ABC-/Driehoekstransacties** in documenten niet was gemarkeerd. |


## <a name="see-also"></a>Zie ook
[Financieel beheer](finance.md)  
[Werken met Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
