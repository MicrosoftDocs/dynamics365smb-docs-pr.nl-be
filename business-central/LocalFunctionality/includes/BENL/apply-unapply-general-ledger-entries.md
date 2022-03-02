---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 525fefb060fa001004645ac5376ec3f5838450c4
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133499"
---
Door tijdelijke grootboekposten toe te passen, kunnen bedrijven werken met tijdelijke en transferaccounts in het grootboek. Tijdelijke en transferrekeningen worden gebruikt om tijdelijke posten op te slaan die op verdere verwerking in het grootboek wachten.  

U kunt tijdelijke rekeningen gebruiken voor:  

- Geldtransfers van de ene naar de andere bankrekening.  
- Financiële transactietransfers van het ene systeem naar het andere, waarbij een deel van de gegevens tijdelijk op het oorspronkelijke systeem staat.  
- Transacties waarvoor u een verkoopfactuur hebt verzonden naar een klant maar nog niet de bijbehorende inkoopfactuur van de leverancier hebt ontvangen.  

Nadat de posten zijn verwerkt, kunt u de functie **Posten vereffenen** gebruiken om de geboekte posten en het boekingsrekeningsoort bij te werken.  

U kunt de vereffening van de vereffende grootboekposten ongedaan maken en vervolgens de gesloten posten openen om wijzigingen aan te brengen.  

## <a name="to-apply-general-ledger-entries"></a>Grootboekposten vereffenen  

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekjournalen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.  
3. Kies op de pagina **Grootboekposten** de actie **Posten vereffenen**.  

    Alle openstaande posten voor de grootboekrekening worden weergegeven op de pagina **Grootboekposten vereffenen**.  

    > [!NOTE]  
    > Standaard wordt het veld **Posten opnemen** ingesteld op **Open**. U kunt de waarde van het veld **Posten opnemen** wijzigen in **Alle** of **Afgesloten**. U kunt alleen grootboekposten vereffenen die **open** zijn.  

4. Selecteer de relevante grootboekpost en kies de actie **Set van toepassing op id**.  

    Het veld **Vereffenings-id** wordt bijgewerkt met de gebruikers-id. Het restbedrag wordt weergegeven op de pagina **Saldo** in het venster **Grootboekposten vereffenen**.  
5. Kies de actie **Vereffening boeken**.  

    U kunt de vereffening boeken zelfs wanneer het saldobedrag gelijk is aan 0. Wanneer wordt geboekt, wordt het veld **Restbedrag** als volgt beïnvloed:  

    - Als het veld **Saldo** gelijk is aan 0, wordt het veld **Restbedrag** bij alle grootboekposten op 0 gezet.  

    - Als het veld **Saldo** niet gelijk is aan 0, wordt het bedrag in het veld **Saldo** overgebracht naar het veld **Restbedrag** van de grootboekpost die was geselecteerd toen u de vereffening boekte.  

    - Voor alle overige grootboekposten wordt het veld **Restbedrag** op 0 gezet en worden de velden **Open**, **Afgesloten door volgnr.**, **Afgesloten met bedrag** en **Afgesloten op** bijgewerkt.  

    > [!NOTE]  
    > Wanneer wordt geboekt, worden de grootboekposten die het veld **Vereffenings-id** bijwerken, verwijderd.  

6. Kies de knop **Ok**.  

## <a name="to-view-the-applied-general-ledger-entries"></a>De vereffende grootboekposten weergeven  

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekjournalen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.  
3. Selecteer de betreffende grootboekpost en kies de actie **Vereffende posten**.  

    U kunt alle vereffende grootboekposten weergeven.  

4. Kies de knop **Ok**.  

## <a name="to-unapply-general-ledger-entries"></a>De vereffening van grootboekposten ongedaan maken  

1. Kies het pictogram :::image type="icon" source="../../../media/ui-search/search_small.png" border="false":::, voer **Grootboekjournalen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.  
3. Selecteer de grootboekpost waarvan u de vereffening ongedaan wilt maken en kies vervolgens de actie **Vereffening ongedaan maken**.  

    De vereffening van de vereffende grootboekposten wordt ongedaan gemaakt.  

    > [!NOTE]  
    > Als een post is vereffend met meer dan één vereffeningspost, moet u de vereffening van de laatste vereffeningspost het eerst ongedaan maken. Standaard wordt de laatste post weergegeven.  

4. Kies de knop **Ok**.  
