---
title: Betalingsbestanden uploaden naar een Isabel-server
description: Betalingsbestanden kunnen worden geüpload via de pagina IBS-logboeken. U kunt alleen betalingsbestanden uploaden als de velden Uploadintegratiemodus en Downloadintegratiemodus op de pagina Elektronisch bankieren instellen zijn ingesteld op Met toezicht.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 34ca4afa9714336652ed654194f02e5493a750ee
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "826345"
---
# <a name="upload-payment-files-to-an-isabel-server"></a>Betalingsbestanden uploaden naar een Isabel-server
> [!Note]
> [!INCLUDE[onprem_only](../../includes/onprem_only_md.md)]

Betalingsbestanden kunnen worden geüpload via de pagina **IBS-logboeken**. U kunt alleen betalingsbestanden uploaden als de velden **Uploadintegratiemodus** en **Downloadintegratiemodus** op de pagina **Elektronisch bankieren instellen** zijn ingesteld op **Met toezicht**.  

> [!NOTE]  
>  Voordat u betalingbestanden kunt uploaden, moet u zijn aangemeld bij de Isabel-server.  

## <a name="to-upload-payment-files-in-attended-mode"></a>Betalingsbestanden uploaden in de modus Met toezicht  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IBS-logboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Contract en gebruiker ophalen**.  
3.  Na het verifiëren van de betalingbestanden worden een gebruikers- en contract- id weergegeven in de velden **IBS-gebruikers-id** en **IBS-contract-id**.  

    Het veld **Uploadstatus** wordt ingesteld op **Gereed voor uploaden**. Als op de Isabel-server meerdere contracten voor de bankrekening bestaan, wordt **Uploadstatus** ingesteld op **Conflict bestaat**. Selecteer het juiste contract.  

4.  Kies de actie **Downloaden**. De betalingsbestanden worden geüpload naar de Isabel-server en het veld **Verwerkingsstatus** wordt ingesteld op **Verwerkt**.  
5.  Vervolg het verwerken van de betalingsbestanden door de bestanden op de Isabel-server te ondertekenen en te verzenden.  

## <a name="see-also"></a>Zie ook  
 [IBS-logposten archiveren](how-to-archive-ibs-log-entries.md)
