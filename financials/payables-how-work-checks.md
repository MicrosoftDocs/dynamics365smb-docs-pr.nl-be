---
title: Cheques afgeven, afdrukken, annuleren, en nietig verklaren| Microsoft Docs
description: Beschrijft hoe u cheques afgeeft met het betalingsdagboek, cheques afdrukt, en chequeposten nietig verklaart of weergeeft in Financials.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0875164a3afee7a835346a8d4b9323dda9ebf080
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-checks"></a>Procedure: Werken met cheques
In [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u elektronische en handmatige cheques verzenden. Bij beide methoden wordt het betalingsdagboek gebruikt om cheques te verzenden naar leveranciers. Daarnaast kunt u cheques nietig verklaren en chequeposten weergeven.

Bij het proces voor het uitgeven van cheques worden betalingen voorgesteld, worden posten gemaakt en worden de computercheques afgedrukt.

> [!NOTE]  
>   Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat. Zie voor meer informatie [Procedure: Een Positive Pay-bestand exporteren](finance-how-positive-pay.md).

De printer moet correct zijn ingesteld op het afdrukken van chequeformulieren en u moet bepalen welke indeling wordt gebruikt. Zie voor meer informatie [Procedure: Cheque-indelingen definiëren](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Cheques uitgeven
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul het dagboek met relevante betalingen, bijvoorbeeld met behulp van de functie Leveranciersbetalingen voorstellen. Zie voor meer informatie [Procedure: Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).
3. Selecteer een van de volgende opties in het veld **Betalingssoort** op dagboekregels voor betalingen die u wilt doen met cheques:

   * **Automatische cheque**: selecteer deze optie als u een cheque wilt afdrukken voor het bedrag op de betalingsdagboekregel. U moet de cheques afdrukken voordat u de dagboekregels kunt boeken. U kunt **Automatische cheque** alleen selecteren als het **Tegenrekeningsoort** of het **Rekeningsoort** **Bankrekening** is.
   * **Handmatige cheque**: selecteer deze optie als u handmatig een cheque hebt gemaakt en er een bijbehorende chequepost moet worden gemaakt voor dit bedrag. Met deze optie kunt u geen cheques afdrukken vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]. U kunt **Handmatige cheque** alleen selecteren als het **Tegenrekeningsoort** of het **Rekeningsoort** **Bankrekening** is.

     > [!NOTE]  
>   U moet computercheques afdrukken voordat u de gerelateerde dagboekregels boekt.
4. In het geval van automatische cheques kiest u **Cheque afdrukken**.
5. Vul indien nodig de velden in het venster **Cheque** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Klik op **Afdrukken**.

> [!NOTE]  
>   Als u cheques in meerdere valuta's van verschillende bankrekeningen wilt afdrukken, moet u de batchverwerking **Cheque afdrukken** voor elke valuta afzonderlijk uitvoeren en de juiste bankrekening opgeven.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Afgedrukte cheques annuleren die niet zijn geboekt
U kunt niet-geboekte cheques annuleren nadat ze zijn afgedrukt door de actie **Ongeldige cheque** in het venster **Betalingsdagboek** te gebruiken.

1. Kies in het venster **Betalingsdagboek** de actie **Ongeldige cheque** en kies vervolgens welke cheques u wilt annuleren.

## <a name="to-void-checks"></a>Cheques nietig verklaren
Wanneer chequebetaling is geboekt, kunt u cheques alleen annuleren (nietig verklaren) vanuit de resulterende bankposten.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de betreffende bankrekening, kies de actie **Bewerken** en kies vervolgens de actie **Chequeposten**.
3. Kies in het venster **Chequeposten** de actie **Ongeldige cheque**.
4. Schakel het selectievakje **Cheque alleen nietig verklaren** in.
5. Kies de knop **Ok**.

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Procedure: Een Positive Pay-bestand exporteren](finance-how-positive-pay.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

