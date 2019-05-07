---
title: SEPA-betalingen via automatische incasso boeken | Microsoft Docs
description: Wanneer een incasso-opdracht wordt verwerkt door uw bank, kunt u doorgaan met het boeken van de ontvangst van de betaling voor de betrokken verkoopfacturen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "930767"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a>SEPA-betalingsontvangsten via automatische incasso boeken
Wanneer een incasso-opdracht wordt verwerkt door uw bank, kunt u doorgaan met het boeken van de ontvangst van de betaling voor de betrokken verkoopfacturen. Zie voor meer informatie [SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

U kunt de betalingsontvangst van de pagina **Incasso-opdrachten** of de pagina **Verzamelingsposten van incasso** direct boeken. U kunt ook het werk aan een andere gebruiker doorgeven door de dagboekregels voor te bereiden.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Een betalingsontvangst van een automatische incasso boeken vanuit de pagina Verzamelingen van automatische incasso  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Incasso-opdrachten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een regel voor een verzameling automatische incasso die is geëxporteerd naar een bankbestand en verwerkt door de bank. Zie voor meer informatie [SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Kies de actie **Betalingsontvangsten boeken**.  
4. Vul op de pagina **Incasso-opdracht boeken** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Incasso-opdrachtnr.**|Geef de verzameling automatische incasso op waar u een betalingsontvangst voor wilt boeken.|  
    |**Algemeen dagboeksjabloon**|Geef op welk dagboeksjabloon te gebruiken voor het boeken van de betalingsontvangst, zoals de sjabloon voor ontvangsten.|  
    |**Batchnaam financieel dagboek**|Geef op welke dagboekbatch moet worden gebruikt voor het boeken van de betalingsontvangst.|  
    |**Alleen dagboek aanmaken**|Schakel dit selectievakje in als u niet de betalingsontvangst boeken wilt wanneer u de **OK** knop kiest. De betalingsontvangst in het opgegeven dagboek wordt voorbereid en wordt niet geboekt totdat iemand de dagboekregels in kwestie boekt.|  

5. Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
 [Verkoop](sales-manage-sales.md)
