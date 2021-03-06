---
title: Betalingsdagboeksjablonen en -batches maken
description: In de Belgische versie van Business Central worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 38c7e750d6a1861ba57344bcf83086b5131017cd
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379567"
---
# <a name="create-payment-journal-templates-and-batches"></a>Betalingsdagboeksjablonen en -batches maken
In [!INCLUDE[prod_short](../../includes/prod_short.md)] worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten. Het betalingsdagboek bevat echter enkele velden die specifiek betrekking hebben op het verwerken van betalingen. Voordat u betalingsvoorstellen kunt genereren, moet u een betalingsdagboeksjabloon en een betalingsdagboekbatch instellen.  

Als u een bankrekening toewijst aan de betalingsdagboeksjabloon, wordt de bankrekening ingevoegd in alle betalingsdagboekbatches en betalingsdagboekregels die met deze sjabloon worden gemaakt. Door een bankrekening voor de dagboeksjabloon op te geven, kunt u de benodigde tijd voor het controleren van de betalingsvoorstellen beperken.  

## <a name="to-create-a-payment-journal-template"></a>Een betalingsdagboeksjabloon maken  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Vul op de pagina **Betalingsdagboeksjablonen** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Naam**|Voer de unieke naam in van de betalingsdagboeksjabloon die u maakt.|  
    |**Beschrijving**|Voer een omschrijving voor de betalingsdagboeksjabloon in.|  
    |**Bankrekening**|Selecteer de bankrekening die wordt gebruikt als u een betalingsvoorstel maakt.|  
    |**Redencode**|Selecteer de redencode die wordt gebruikt voor alle dagboekbatches en regels die worden gemaakt met de dagboeksjabloon. Als u een andere redencode op een dagboekregel wilt gebruiken, kunt u deze handmatig wijzigen.|  
    |**Broncode**|Selecteer de broncode die wordt gebruikt voor alle dagboekbatches en regels die worden gemaakt met de dagboeksjabloon.|  

4.  Kies de knop **OK**.  

## <a name="to-add-payment-journal-batches-to-the-journal-template"></a>Betalingsdagboekbatches toevoegen aan de dagboeksjabloon  

1.  Kies op de pagina **Betalingsdagboeksjablonen** de actie **Batches**.  
2.  Vul op de pagina **Betalingsdagboekbatch** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Dagboeksjabloon**|Geef een dagboeksjabloonnaam op voor de betalingsdagboekbatch.|  
    |**Naam**|Voer een unieke naam voor de dagboekbatch in.<br /><br /> **OPMERKING:** als de dagboeknaam numeriek moet wordt bijgewerkt, neemt u een nummer op in de dagboekbatchnaam. Zo wordt de waarde in de batchnaam KBC1 bij elke nieuwe boeking verhoogd (KBC2, KBC3, enzovoort).|  
    |**Beschrijving**|Voer een omschrijving voor de dagboekbatch in.|  
    |**Redencode**|Hiermee wordt de redencode opgegeven die is gekoppeld aan de dagboekbatch.|  
    |**Status**|Hiermee wordt de status van de batch opgegeven.|  

3.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)   
 [IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]