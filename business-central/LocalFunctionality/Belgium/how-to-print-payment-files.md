---
title: Betalingsbestanden afdrukken
description: Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 86ce737314b5e98c735e22a5b50a9700f4a5d668
ms.contentlocale: nl-be
ms.lasthandoff: 11/22/2018

---
# <a name="print-payment-files"></a>Betalingsbestanden afdrukken
Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.  

Een betalingsbestand bevat binnenlandse, internationale of SEPA-betalingen (in euro's of in een andere valuta). Het bestand kan per schijf of via een modem of Isabel (Interbanks Standards Association Belgium) worden verzonden. U kunt slechts één bestand per boekingsdatum en valutacode maken. Wanneer u de betalingen naar een bestand exporteert, wordt er een bijbehorende notitie afgedrukt die ook naar de bank kan worden verzonden.  

In het betalingsdagboek wordt het veld **Status** op de geëxporteerde regels ingesteld op **Geboekt**.  

## <a name="to-print-a-payment-file"></a>Een betalingsbestand afdrukken  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboek** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vul op het sneltabblad **Opties** de velden in zoals in de volgende tabel wordt beschreven.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Batchnaam**|Geef de batchnaam van het betalingsdagboek op.|  
    |**Bankrekening**|Geef de bankrekening van het betalingsdagboek op.|  
    |**Exportprotocol**|Geef de exportprotocolcode van de betalingsdagboekregel op. Exportprotocollen bepalen welk betalingsbestand in het betalingsdagboek wordt gegenereerd.<br /><br /> U kunt een combinatie van exportindelingen in één batch hebben, bijvoorbeeld binnenlandse, internationale en SEPA-betalingen. Wanneer u de betalingsregels naar een bestand exporteert, kunt u echter slechts één exportindeling, of exportprotocol, gebruiken. **Opmerking:** door het exportprotocol op te geven, geeft u ook het validatietype op dat wordt uitgevoerd in het betalingsdagboek.|  

3.  Kies de actie **Betalingsregels controleren**.

    De pagina **Logboeken voor controlefouten exporteren** bevat eventuele fouten die kunnen bestaan. Als er fouten zijn, moet u deze oplossen voordat u verder kunt gaan.

4. Als er geen fouten zijn, kiest u de actie **Betalingsregels exporteren**.  

    Vervolgens wordt het rapport geopend dat u in het veld **Testrapport-id** in **Betalingsdagboeksjablonen** hebt opgegeven.  

5.  Klik op **Afdrukken**.  

## <a name="see-also"></a>Zie ook  
 [Elektronisch bankieren voor België](belgian-electronic-banking.md)   
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)   
 [IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)   
 [Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)   
 [Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md)   
 [Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)   
 [Elektronische betalingen testen](how-to-test-electronic-payments.md)   
 [Regels voor elektronische betalingen beheren](how-to-manage-electronic-payment-lines.md)

