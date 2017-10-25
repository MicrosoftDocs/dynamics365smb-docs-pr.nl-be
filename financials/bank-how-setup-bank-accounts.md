---
title: Bankrekeningen instellen| Microsoft Docs
description: "U kunt in Financials bankrekeningen reconciliëren met afschriften van de bank."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-bank-accounts"></a>Procedure: bankrekeningen instellen
U gebruikt bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)] om uw banktransacties bij te houden. Bedragen op rekeningen kunnen worden uitgedrukt in de lokale valuta of in een vreemde valuta. Nadat u bankrekeningen hebt ingesteld, kunt u ook de optie voor het afdrukken van cheques gebruiken.

## <a name="to-set-up-bank-accounts"></a>Bankrekeningen instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.
2. Kies in het venster **Bankrekeningen** de actie **Nieuw**.
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Uw bankrekening instellen om bankbestanden te importeren of te exporteren
Velden op het sneltabblad **Transfer** in het venster **Bankrekeningkaart** zijn gerelateerd om bankfeeds en -bestanden te importeren en te exporteren. Zie [Procedure: Conversieservice voor bankgegevens instellen](bank-how-setup-bank-data-conversion-service.md) en [Procedure: De service Envestnet Yodlee Bank Feeds instellen](bank-how-setup-bank-statement-service.md) voor meer informatie.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.
2. Open de kaart voor een bankrekening waarvoor u bankbestanden exporteert of importeert.
3. Vul indien nodig de velden op het sneltabblad **Transfer** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Andere services voor bestandsexport en de verschillende indelingen vereisen andere instellingswaarden in het venster **Bankrekeningkaart**. U wordt over verkeerde of ontbrekende instellingswaarden geïnformeerd als u het bestand probeert te exporteren. Lees daarom de korte omschrijvingen van de velden zorgvuldig of raadpleeg de relateerde onderwerpen met procedures. Als u bijvoorbeeld een betalingsbestand voor een Noord-Amerikaanse elektronische betaling (EFT) exporteert, moeten daarvoor zowel het veld **Laatste afdrachtsadviesnr.** als **Transitnr.** zijn ingevuld. Zie voor meer informatie [Procedure: Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Bankrekeningen van leveranciers instellen voor de export van bankbestanden
Velden op het sneltabblad **Transfer** in het venster **Bankrekeningkaart leverancier** zijn gerelateerd om bankfeeds en -bestanden te exporteren. Zie [Procedure: Conversieservice voor bankgegevens instellen](bank-how-setup-bank-data-conversion-service.md) en [Procedure: Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md) voor meer informatie.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en klik vervolgens op de gerelateerde koppeling.
2. Open de kaart voor een leverancier naar wiens bankrekening u betalingsbankbestanden exporteert.
3. Kies de actie **Bankrekeningen**.
3. Vul indien nodig de velden in het venster **Bankrekeningkaart leverancier** op het sneltabblad **Transfer** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Zie ook
[Bankieren instellen](bank-setup-banking.md)  
[Bankrekeningen beheren](bank-manage-bank-accounts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

