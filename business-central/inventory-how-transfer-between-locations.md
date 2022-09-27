---
title: Artikelen overbrengen tussen magazijnvestigingen
description: Beschrijft hoe u voorraad verplaatst van de ene plaats of magazijn naar een andere, met het herindelingsdagboek of met transferorders.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.search.forms: 5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b3fb127931f433ab7f433fca4ab8ba4a9ef306e1
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534871"
---
# <a name="transfer-inventory-between-locations"></a>Voorraad overbrengen tussen vestigingen

U kunt voorraadartikelen tussen vestigingen overbrengen door transferorders te maken. U kunt ook het artikelherindelingsdagboek gebruiken.

Met transferorders verzendt u de uitgaande transfer vanuit de ene vestiging en ontvangt u de inkomende transfer op de andere vestiging. U kunt zo de desbetreffende magazijnactiviteiten beheren en u krijgt meer zekerheid dat voorraadaantallen correct worden bijgewerkt.

Met het herindelingsdagboek hoeft u alleen de velden **Vestigingscode** en **Nieuwe vestigingscode** in te vullen. Als u het dagboek boekt, worden de artikelposten aangepast op de betreffende vestigingen. Met deze methode worden magazijnactiviteiten niet beheerd.

> [!NOTE]  
>   Als u artikelen in uw voorraad hebt geregistreerd zonder vestigingscode, bijvoorbeeld van een tijdstip waarop u slechts één magazijn had, kunt u deze artikelen niet overbrengen met transferorders. In plaats hiervan moet u het herindelingsdagboek gebruiken om de artikelen van een lege vestigingscode opnieuw in te delen voor een werkelijke vestigingscode.  Zie stap 3 in [Artikelen overbrengen met het artikelherindelingsdagboek](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal) voor meer informatie.

Als u artikelen wilt overbrengen, moeten locaties en transferroutes zijn ingesteld. Zie [Vestigingen instellen](inventory-how-setup-locations.md) voor meer informatie.

## <a name="to-transfer-items-with-a-transfer-order"></a>Artikelen overbrengen met een transferorder

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Transferorders** in en kies vervolgens de gerelateerde koppeling
2. Vul op de pagina **Transferorder** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Als u tijdens het instellen van de transferroute tussen deze vestigingen de velden **Transitcode**, **Expediteur** en **Expediteurservice** op de pagina **Transferroutegegevens** hebt ingevuld, worden de bijbehorende velden op de transferorder automatisch ingevuld.

    Wanneer u het veld **Servicecode expediteur** invult, wordt de ontvangstdatum in de ontvangstvestiging berekend door de verzendtijd van de expediteurservice op te tellen bij de verzenddatum.

3. Om de regels in te vullen, voert u ze handmatig in of kiest u een van de volgende opties onder de actie **Functies**:
    - Kies de actie **Opslaglocatie-inhoud ophalen** om bestaande artikelen uit een specifieke opslaglocatie te selecteren.
    - Kies de actie **Ontvangstregels ophalen** om artikelen te selecteren die net zijn aangekomen op de aflevervestiging.   

    Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te verzenden.
4. Kies de actie **Boeken**, kies de optie **Verzenden** en kies vervolgens de knop **OK**.

    De artikelen zijn nu in transit tussen de opgegeven vestigingen volgens de opgegeven transferroute.

    Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te ontvangen. De tranferorderregels zijn dezelfde als bij verzending en kunnen niet worden bewerkt.
5. Kies de actie **Boeken**, kies de optie **Ontvangen** en kies vervolgens de knop **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Artikelen overbrengen met het artikelherindelingsdagboek

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelherindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul op de pagina **Artikelherindelingsdagboeken** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voer in het veld **Vestiging** de vestiging in waar de artikelen momenteel zijn opgeslagen.

    > [!NOTE]  
    >   Als u artikelen wilt overbrengen die geen vestigingscode hebben, laat u het veld **Vestiging** leeg.
4. Voer in het veld **Nieuwe vestiging** de vestiging in waarnaar u de artikelen wilt overbrengen.
5. Kies de actie **Boeken**.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/transfer-items/)

## <a name="see-also"></a>Zie ook

[Voorraad beheren](inventory-manage-inventory.md)  
[Vestigingen instellen](inventory-how-setup-locations.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
