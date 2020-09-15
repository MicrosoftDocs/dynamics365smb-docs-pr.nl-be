---
title: Belgische elektronische betalingen
description: In de module voor elektronisch bankieren in de Belgische versie van Business Central kunt u elektronische betalingen naar binnen- en buitenland, en SEPA en niet-Euro SEPA verzenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 381a47409f991ec1733926026ae6f01cb9ffe242
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778693"
---
# <a name="belgian-electronic-payments"></a>Belgische elektronische betalingen
In de module voor elektronisch bankieren in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u elektronische betalingen naar binnen- en buitenland, en SEPA en niet-Euro SEPA verzenden.  

|Elektronische betaling|Description|  
|------------------------|---------------------------------------|  
|Binnenlands|Deze betalingen worden uitgevoerd in de lokale valuta (LV) en worden verwerkt door een lokale financiële instelling voor begunstigden die rekeningen hebben bij een lokale financiële instelling. De geldigheid van de bankrekeningnummers wordt door [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gecontroleerd.|  
|Internationaal|Deze betalingen worden uitgevoerd in een vreemde valuta of de lokale valuta (LV) en worden verwerkt door een lokale financiële instelling voor begunstigden die rekeningen hebben bij een buitenlandse financiële instelling. De geldigheid van de bankrekeningnummers wordt niet door [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gecontroleerd.|  
|SEPA|Deze betalingen worden uitgevoerd in euro's en verwerkt in landen/regio's waar SEPA-betalingen zijn toegestaan. De geldigheid van de bankrekeningnummers wordt door [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gecontroleerd.|  
|SEPA-betalingen in andere valuta's|Deze betalingen worden uitgevoerd in andere valuta's dan de euro en naar een land of regio buiten de EEA (European Economic Association). De geldigheid van de bankrekeningnummers wordt door [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gecontroleerd.|  

 Omdat de standaard voor elektronische betalingen per land/regio verschilt, kunnen elektronische betalingen gemaakt in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] alleen worden verwerkt door financiële instellingen in België. Voor internationale betalingen moeten de lokale financiële instellingen de betaling verwerken met de buitenlandse instellingen.  

> [!NOTE]  
>  Creditnota's kunnen niet afzonderlijk worden verwerkt omdat betalingen geen negatief saldo mogen hebben. Als u een creditnota wilt verwerken, moet u deze aan een of meer facturen toevoegen door betalingen te totaliseren.  

Voordat u een elektronische betaling kunt uitvoeren, moet u het gebruik van elektronisch bankieren instellen in [!INCLUDE[d365fin](../../includes/d365fin_md.md)].  

## <a name="correcting-payment-lines"></a>Betalingsregels corrigeren  
U moet alle fouten corrigeren voordat u de regels met elektronische betalingen kunt boeken. U kunt betalingsregels op de volgende manieren corrigeren.  

|Storno|Description|  
|----------------|---------------------------------------|  
|Een betalingsdagboekregel toevoegen|Als het betalingsdagboek al veel regels bevat en u nog een regel wilt toevoegen, kunt u de dagboekregel handmatig invoeren. U kunt dit bijvoorbeeld doen als u een creditnota wilt terugbetalen aan een klant. Dergelijke klantbetalingen worden niet automatisch voorgesteld door de batchverwerking **Leveranciersbetalingen voorstellen**.|  
|Een betalingsdagboekregel bewerken|Als u geen bankrekening aan het betalingsdagboek hebt toegewezen of als u geen bankrekening van voorkeur op de leverancierskaart hebt opgegeven, moet u deze gegevens handmatig op elke dagboekregel invoeren voordat u het dagboek boekt. Als u een bankrekening voor een leverancier opgeeft, wordt de bankrekening gekopieerd naar alle betalingsdagboekregels voor die leverancier. Zie voor meer informatie [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md).|  
|Een betalingsdagboekregel verwijderen|Met de batchverwerking **Leveranciersbetalingen voorstellen** maakt u betalingsvoorstellen voor alle leveranciers die overeenkomen met de opgegeven criteria. Als u de betaling voor een bepaalde leverancierspost of leverancier wilt voorkomen, kunt u de betreffende dagboekregels verwijderen.|  

Zie [Regels voor elektronische betalingen beheren](how-to-manage-electronic-payment-lines.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook  
[Belgische lokale functionaliteit](belgium-local-functionality.md)  
[Elektronisch bankieren voor België](belgian-electronic-banking.md)   
[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)   
[IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)   
[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)   
[Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md)   
[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)   
[Elektronische betalingen testen](how-to-test-electronic-payments.md)   
[Regels voor elektronische betalingen beheren](how-to-manage-electronic-payment-lines.md)   
[Betalingsbestanden afdrukken](how-to-print-payment-files.md)
