---
title: Grootboekposten vereffenen en de vereffening ervan ongedaan maken
description: Door tijdelijke grootboekposten te vereffenen kunnen bedrijven werken met tijdelijke rekeningen en transferrekeningen in het grootboek. Tijdelijke en transferrekeningen worden gebruikt om tijdelijke posten op te slaan die op verdere verwerking in het grootboek wachten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9d3d5a39a5c1fa77ce34ee0029c4189f4c4d836b
ms.sourcegitcommit: 5b6dd8d881c0eb65ece6936a94dfda3185574335
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/28/2019
ms.locfileid: "1710944"
---
# <a name="apply-and-unapply-general-ledger-entries"></a>Grootboekposten vereffenen en de vereffening ervan ongedaan maken
Door tijdelijke grootboekposten te vereffenen kunnen bedrijven werken met tijdelijke rekeningen en transferrekeningen in het grootboek. Tijdelijke en transferrekeningen worden gebruikt om tijdelijke posten op te slaan die op verdere verwerking in het grootboek wachten.  

 U kunt tijdelijke rekeningen gebruiken voor:  

- Geldtransfers van de ene naar de andere bankrekening.  
- Financiële transactietransfers van het ene systeem naar het andere, waarbij een deel van de gegevens tijdelijk op het oorspronkelijke systeem staat.  
- Transacties waarvoor u een verkoopfactuur hebt verzonden naar een klant maar nog niet de bijbehorende inkoopfactuur van de leverancier hebt ontvangen.  

 Nadat de posten zijn verwerkt, kunt u de functie **Posten vereffenen** gebruiken om de geboekte posten en het boekingsrekeningsoort bij te werken.  

 U kunt de vereffening van de vereffende grootboekposten ongedaan maken en vervolgens de gesloten posten openen om wijzigingen aan te brengen.  

## <a name="to-apply-general-ledger-entries"></a>Grootboekposten vereffenen  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekjournalen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.  
3.  Kies op de pagina **Grootboekposten** de actie **Posten vereffenen**.  

    Alle openstaande posten voor de grootboekrekening worden weergegeven op de pagina **Grootboekposten vereffenen**.  

    > [!NOTE]  
    >  Standaard wordt het veld **Posten opnemen** ingesteld op **Open**. U kunt de waarde van het veld **Posten opnemen** wijzigen in **Alle** of **Afgesloten**. U kunt alleen de grootboekposten vereffenen die **open** zijn.  

4.  Selecteer de betreffende grootboekpost en kies **Vereffenings-id instellen**.  

    Het veld **Vereffenings-id** wordt bijgewerkt met de gebruikers-id. Het restbedrag wordt weergegeven op de pagina **Saldo** in het venster **Grootboekposten vereffenen**.  

5.  Kies de actie **Vereffening boeken**.  

    U kunt de vereffening boeken zelfs wanneer het saldobedrag gelijk is aan 0. Wanneer wordt geboekt, wordt het veld **Restbedrag** als volgt beïnvloed:  

    - Als het veld **Saldo** gelijk is aan 0, wordt het veld **Restbedrag** bij alle grootboekposten op 0 gezet.  

    - Als het veld **Saldo** niet gelijk is aan 0, wordt het bedrag in het veld **Saldo** overgebracht naar het veld **Restbedrag** van de grootboekpost die was geselecteerd toen u de vereffening boekte.  

    - Voor alle overige grootboekposten wordt het veld **Restbedrag** op 0 gezet en worden de velden **Open**, **Afgesloten door volgnr.**, **Afgesloten met bedrag** en **Afgesloten op** bijgewerkt.  

    > [!NOTE]  
    >  Wanneer wordt geboekt, worden de grootboekposten die het veld **Vereffenings-id** bijwerken, verwijderd.  

6.  Kies de knop **Ok**.  

## <a name="to-view-the-applied-general-ledger-entries"></a>De vereffende grootboekposten weergeven  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekjournalen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.  
3.  Selecteer de betreffende grootboekpost en kies de actie **Vereffende posten**.  

    U kunt alle vereffende grootboekposten weergeven.  

4.  Kies de knop **OK**.  

## <a name="to-unapply-general-ledger-entries"></a>De vereffening van grootboekposten ongedaan maken  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekjournalen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.  
3.  Selecteer de grootboekpost waarvan u de vereffening ongedaan wilt maken en kies vervolgens de actie **Vereffening ongedaan maken**.  

    De vereffening van de vereffende grootboekposten wordt ongedaan gemaakt.  

    > [!NOTE]  
    >  Als een post is vereffend met meer dan één vereffeningspost, moet u de vereffening van de laatste vereffeningspost het eerst ongedaan maken. Standaard wordt de laatste post weergegeven.  

4.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
[Belgische lokale functionaliteit](belgium-local-functionality.md)
