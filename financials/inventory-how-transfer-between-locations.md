---
title: 'Procedure: Voorraad overbrengen tussen vestigingen| Microsoft Docs'
description: Beschrijft hoe de voorraad tussen ruimten of magazijnen wordt overgebracht met het herindelingsdagboek of met transferorders.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 03/28/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 43a60a6eb646de13ca9bf1458061f0bbefbeab12
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-inventory-between-locations"></a>Procedure: Voorraad overbrengen tussen vestigingen
U kunt voorraadartikelen tussen vestigingen overbrengen door transferorders te maken. U kunt ook het artikelherindelingsdagboek gebruiken.

Met transferorders verzendt u de uitgaande transfer vanuit de ene vestiging en ontvangt u de inkomende transfer op de andere vestiging. U kunt zo de desbetreffende magazijnactiviteiten beheren en u krijgt meer zekerheid dat voorraadaantallen correct worden bijgewerkt.

Met het herindelingsdagboek hoeft u alleen de velden **Vestigingscode** en **Nieuwe vestigingscode** in te vullen. Als u het dagboek boekt, worden de artikelposten aangepast op de betreffende vestigingen. Met deze methode worden magazijnactiviteiten niet beheerd.

**Opmerking**: als u artikelen in uw voorraad hebt geregistreerd zonder vestigingscode, bijvoorbeeld van een tijdstip waarop u slechts één magazijn had, kunt u deze artikelen niet overbrengen met transferorders. In plaats hiervan moet u het herindelingsdagboek gebruiken om de artikelen van een lege vestigingscode opnieuw in te delen voor een werkelijke vestigingscode.  Zie stap 3 in het gedeelte "Artikelen overbrengen met het artikelherindelingsdagboek" voor meer informatie.

Als u artikelen wilt overbrengen, moeten locaties en transferroutes zijn ingesteld. Zie voor meer informatie [Procedure: Vestigingen instellen](inventory-how-setup-locations.md).

**Opmerking**: voor deze functionaliteit is vereist dat uw ervaring is ingesteld op **Pakket**. Zie [Uw ervaring in [!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen](ui-experiences.md) voor meer informatie.

## <a name="to-transfer-items-with-a-transfer-order"></a>Artikelen overbrengen met een transferorder
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Transferorders** in en kies vervolgens de gerelateerde koppeling.
2. Vul in het venster **Transferorder** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    **Opmerking**: als u de velden **Transitcode**, **Expediteur** en **Service expediteur** hebt ingevuld in het venster **Transferroutegegevens** toen u de transferroute instelde, worden de corresponderende velden op de transferorder automatisch ingevuld.

    Wanneer u het veld **Servicecode expediteur** invult, wordt de ontvangstdatum in de ontvangstvestiging berekend door de verzendtijd van de expediteurservice op te tellen bij de verzenddatum.

    Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te verzenden.
3. Kies de actie **Boeken**, kies de optie **Verzenden** en kies vervolgens de knop **OK**.

    De artikelen zijn nu in transit tussen de opgegeven vestigingen volgens de opgegeven transferroute.

    Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te ontvangen.
4. Kies de actie **Boeken**, kies de optie **Ontvangen** en kies vervolgens de knop **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Artikelen overbrengen met het artikelherindelingsdagboek
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Artikelherindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul in het venster **Artikelherindelingsdagboeken** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voer in het veld **Vestiging** de vestiging in waar de artikelen momenteel zijn opgeslagen.

    **Opmerking**: als u artikelen wilt overbrengen die geen vestigingscode hebben, laat u het veld **Vestiging** leeg.
4. Voer in het veld **Nieuwe vestiging** de vestiging in waarnaar u de artikelen wilt overbrengen.
5. Kies de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Voorraad beheren](inventory-manage-inventory.md)  
[Procedure: Vestigingen instellen](inventory-how-setup-locations.md)  
[Toeleveringsketen](madeira-supply-chain.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
