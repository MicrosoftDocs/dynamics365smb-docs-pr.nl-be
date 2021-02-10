---
title: Artikelkruisverwijzingen gebruiken
description: Stel verwijzingen in tussen de beschrijvingen die u en uw leverancier voor een artikel gebruiken, zodat u de artikelbeschrijving van de leverancier op inkoopdocumenten kunt invoegen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 7d670f6553a1bd70dcc3d97f90436f36c6627c56
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013804"
---
# <a name="use-item-cross-references"></a>Artikelkruisverwijzingen gebruiken
Als u een kruisverwijzing instelt tussen de artikelbeschrijving die u voor een artikel gebruikt, en de beschrijving die de leverancier van dat artikel gebruikt, wordt de artikelbeschrijving van de leverancier automatisch in inkoopdocumenten voor de leverancier ingevuld wanneer u het veld **Kruisverwijzingsnr..** invult. Dezelfde functionaliteit geldt voor klantartikelnummers in verkoopdocumenten.

In de volgende procedures wordt beschreven hoe u artikelkruisverwijzingen aan de inkoopkant gebruikt. De stappen zijn vergelijkbaar voor de verkoopkant.

> [!NOTE]
> Het komt steeds vaker voor dat artikel-id's zoals GTIN's of GUID's 30 of meer tekens bevatten, wat meer is dan de huidige functie voor artikelkruisverwijzingen aankan. Als u referenties moet gebruiken die meer dan 30 tekens bevatten, kan uw beheerder de functie **Langere itemreferenties schrijven** functie op de pagina [Functiebeheer](https://businesscentral.dynamics.com/?page=2610) gebruiken (koppeling vereist dat u een [!INCLUDE[prod_short](includes/prod_short.md)]-tenant hebt). Hoe u verwijzingen gebruikt, verandert niet, maar de namen van zaken als pagina's en knoppen wel. De pagina **Artikelkruisverwijzingposten** wordt bijvoorbeeld de pagina **Artikelverwijzingsposten**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Een artikelkruisverwijzing naar de artikelbeschrijving van een leverancier instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.
2. Open de kaart voor een artikel waarvoor u een kruisverwijzing wilt maken naar de artikelomschrijving die de leverancier gebruikt voor het artikel.
3. Kies de actie **Kruisverwijzingen**.

     Als u de actie **Kruisverwijzingen** niet kunt vinden, kiest u ervoor om meer opties weer te geven en zoekt u de actie vervolgens onder **Gerelateerd** > **Artikel**.
  
4. Vul op een nieuwe regel op de pagina **Artikelkruisverwijzingposten** de velden naar wens in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>De artikelomschrijving van een leverancier invoeren in een inkooporder

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.
2. Maak een inkooporder voor de leverancier voor wie u een artikelkruisverwijzing hebt ingesteld in de vorige procedure.
3. Maak een inkoopregel voor het artikel waarvoor u een artikelkruisverwijzing hebt ingesteld in de vorige procedure.
4. Selecteer in het veld **Kruisverwijzingssoortnr.** de artikelkruisverwijzing die u hebt gemaakt, en kies vervolgens de knop **OK**.

Het veld **Omschrijving** op de regel wordt overschreven met de artikelomschrijving van de leverancier, zoals ingesteld in de artikelkruisverwijzingspost.

## <a name="see-also"></a>Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
