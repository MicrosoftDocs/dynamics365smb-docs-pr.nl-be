---
title: Artikelen overbrengen tussen magazijnvestigingen| Microsoft Docs
description: Beschrijft hoe u voorraad verplaatst van de ene plaats of magazijn naar een andere, met het herindelingsdagboek of met transferorders.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2020
ms.author: SorenGP
ms.openlocfilehash: c7d383fdaf75857013651944207616bdc7208e6d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181976"
---
# <a name="transfer-inventory-between-locations"></a>Voorraad overbrengen tussen vestigingen
U kunt voorraadartikelen tussen vestigingen overbrengen door transferorders te maken. U kunt ook het artikelherindelingsdagboek gebruiken.

Met transferorders verzendt u de uitgaande transfer vanuit de ene vestiging en ontvangt u de inkomende transfer op de andere vestiging. U kunt zo de desbetreffende magazijnactiviteiten beheren en u krijgt meer zekerheid dat voorraadaantallen correct worden bijgewerkt.

Met het herindelingsdagboek hoeft u alleen de velden **Vestigingscode** en **Nieuwe vestigingscode** in te vullen. Als u het dagboek boekt, worden de artikelposten aangepast op de betreffende vestigingen. Met deze methode worden magazijnactiviteiten niet beheerd.

> [!NOTE]  
>   Als u artikelen in uw voorraad hebt geregistreerd zonder vestigingscode, bijvoorbeeld van een tijdstip waarop u slechts één magazijn had, kunt u deze artikelen niet overbrengen met transferorders. In plaats hiervan moet u het herindelingsdagboek gebruiken om de artikelen van een lege vestigingscode opnieuw in te delen voor een werkelijke vestigingscode.  Zie stap 3 in [Artikelen overbrengen met het artikelherindelingsdagboek](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal) voor meer informatie.

Als u artikelen wilt overbrengen, moeten locaties en transferroutes zijn ingesteld. Zie [Vestigingen instellen](inventory-how-setup-locations.md) voor meer informatie.

## <a name="to-transfer-items-with-a-transfer-order"></a>Artikelen overbrengen met een transferorder
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferorders** in en kies de desbetreffende koppeling.
2. Vul in de koptekst van de pagina **Transferorder** de velden in zoals nodig. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

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
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelherindelingsdagboeken** in en kies de gerelateerde koppeling.
2. Vul op de pagina **Artikelherindelingsdagboeken** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voer in het veld **Vestiging** de vestiging in waar de artikelen momenteel zijn opgeslagen.

    > [!NOTE]  
    >   Als u artikelen wilt overbrengen die geen vestigingscode hebben, laat u het veld **Vestiging** leeg.
4. Voer in het veld **Nieuwe vestiging** de vestiging in waarnaar u de artikelen wilt overbrengen.
5. Kies de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Voorraad beheren](inventory-manage-inventory.md)  
[Vestigingen instellen](inventory-how-setup-locations.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)
