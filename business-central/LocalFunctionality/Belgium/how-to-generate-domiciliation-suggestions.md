---
title: Domiciliëringsvoorstellen genereren
description: Als u domiciliëringen hebt ingesteld, kunt u beginnen met het genereren van domiciliëringsvoorstellen. U kunt domiciliëringsvoorstellen alleen voor binnenlandse klanten maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8087c4634c7e203f90a5fe95734f4091c632b8d1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778467"
---
# <a name="generate-domiciliation-suggestions"></a>Domiciliëringsvoorstellen genereren
Als u domiciliëringen hebt ingesteld, kunt u beginnen met het genereren van domiciliëringsvoorstellen. In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u domiciliëringsvoorstellen alleen voor binnenlandse klanten maken.  

## <a name="to-generate-domiciliation-suggestions"></a>Domiciliëringsvoorstellen genereren  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Domiciliëringsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Domiciliëringen voorstellen**.  
3.  Vul de velden in zoals weergegeven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Vervaldatum**|Geef hier de vervaldatum voor de batchverwerking op. Alleen posten met een vervaldatum vóór of op deze datum worden opgenomen.|  
    |**Contantkorting nemen**|Selecteer deze optie als u in de batchverwerking klantposten wilt opnemen waarvoor u een contantkorting kunt krijgen.|  
    |**Kortingsvervaldatum betaling**|Typ de datum die wordt gebruikt om de contantkorting te berekenen.|  
    |**Mogelijke terugbetalingen selecteren**|Selecteer deze optie als in de batchverwerking terugbetalingen moeten worden opgenomen.|  
    |**Boekingsdatum**|Typ de datum die als boekingsdatum verschijnt op de regels die tijdens de batchverwerking in het domiciliëringsdagboek worden ingevoegd.|  

4.  Voer aanvullende filtercriteria in.  
5.  Kies de knop **Ok**.  

Wanneer de batchverwerking is uitgevoerd, bevat het domiciliëringsdagboek alle openstaande klantenposten die overeenkomen met de filters.  

> [!NOTE]  
>  De domiciliëringsvoorstellen bevatten alleen klanten waarvoor een domiciliëringsnummer is ingesteld. Zie [Domiciliëringen instellen](how-to-set-up-domiciliations.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook  
 [Elektronisch bankieren voor België](belgian-electronic-banking.md)   
 [Incasso via domiciliëring](direct-debit-using-domiciliation.md)   
 [Domiciliëringen instellen](how-to-set-up-domiciliations.md)   
 [Domiciliëringen testen](how-to-test-domiciliations.md)   
 [Domiciliëringsregels bewerken en verwijderen](how-to-edit-and-delete-domiciliation-lines.md)   
 [Domiciliëringen exporteren en boeken](how-to-export-and-post-domiciliations.md)
