---
title: Betalingsdagboeksjablonen en -batches maken
description: In de Belgische versie van Business Central worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1cbfb5a74c54a39ab3ed2bc11b7f4c3eca5964bd
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775007"
---
# <a name="create-payment-journal-templates-and-batches"></a>Betalingsdagboeksjablonen en -batches maken
In [!INCLUDE[prod_short](../../includes/prod_short.md)] worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten. Het betalingsdagboek bevat echter enkele velden die specifiek betrekking hebben op het verwerken van betalingen. Voordat u betalingsvoorstellen kunt genereren, moet u een betalingsdagboeksjabloon en een betalingsdagboekbatch instellen.  

Als u een bankrekening toewijst aan de betalingsdagboeksjabloon, wordt de bankrekening ingevoegd in alle betalingsdagboekbatches en betalingsdagboekregels die met deze sjabloon worden gemaakt. Door een bankrekening voor de dagboeksjabloon op te geven, kunt u de benodigde tijd voor het controleren van de betalingsvoorstellen beperken.  

## <a name="to-create-a-payment-journal-template"></a>Een betalingsdagboeksjabloon maken  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de velden op de pagina **EB-betalingsdagboeksjablonen** in.  

    [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Als de velden **Pagina-id** en **Testrapport-id** niet worden weergegeven, moet u deze velden toevoegen via personalisatie. U kunt pas doorgaan als de velden zijn ingevuld. Zie [Uw werkruimte personaliseren](../../ui-personalization-user.md) voor meer informatie.
4. Herhaal stap 2 voor aanvullende sjablonen.

5. Kies de knop **Ok**.  

## <a name="to-add-payment-journal-batches-to-the-journal-template"></a>Betalingsdagboekbatches toevoegen aan de dagboeksjabloon  

1.  Kies op de pagina **Betalingsdagboeksjablonen** de actie **Batches**.  
2.  Vul op de pagina **Betalingsdagboekbatch** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Naam**|Voer een unieke naam voor de dagboekbatch in.<br /><br /> **OPMERKING:** als de dagboeknaam numeriek moet wordt bijgewerkt, neemt u een nummer op in de dagboekbatchnaam. Zo wordt de waarde in de batchnaam KBC1 bij elke nieuwe boeking verhoogd (KBC2, KBC3, enzovoort).|  
    |**Beschrijving**|Voer een omschrijving voor de dagboekbatch in.|  
    |**Redencode**|Optioneel kunt u de redencode opgeven die is gekoppeld aan de dagboekbatch.|  
    |**Status**|Hiermee wordt de status van de batch opgegeven.|

Vervolgens kunt u de configuratie testen. Zie [Elektronische documenten testen](how-to-test-electronic-payments.md) voor meer informatie.  

3.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)   
 [IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]