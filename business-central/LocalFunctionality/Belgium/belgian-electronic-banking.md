---
title: Elektronisch bankieren voor België
description: Via elektronisch bankieren kunt u gegevens elektronisch uitwisselen met Belgische financiële instellingen. Hierdoor gaat de verwerking sneller en worden fouten voorkomen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 11308
ms.date: 01/10/2022
ms.author: edupont
ms.openlocfilehash: ec28c51ba356c279d89a3283fb94dd19e4357d97
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7970876"
---
# <a name="belgian-electronic-banking"></a>Elektronisch bankieren voor België

In de Belgisch versie van [!INCLUDE [prod_short](../../includes/prod_short.md)] kunt u gegevens elektronisch uitwisselen met Belgische financiële instellingen. Dit versnelt de verwerkingstijd en helpt fouten voorkomen als gevolg van handmatige gegevensinvoer of -verwerking.  

U kunt elektronisch bankieren gebruiken om de volgende functies uit te voeren:  

- Elektronische betalingen verzenden.  
- Bankafschriften met CODA verwerken.  
- Incassobetalingen verwerken met domiciliëringen.  

## <a name="setup"></a>Instelling

Voordat u elektronische betalingen en bankafschriften kunt verwerken, moet u elektronisch bankieren instellen op de pagina **Elektronisch bankieren instellen** zoals beschreven in de volgende tabel.

|Veld|Omschrijving |
|-----|------------|
|**Alg. dagb.regels samenvatten**| Selecteer deze optie om aan te geven of u de betalingsdagboekregels voor elke leverancier wilt groeperen. Betalingen met een gestructureerd bericht worden niet gegroepeerd. |
|**Tekst van betaalberichten afbreken** |Selecteer deze optie om lange betaalberichten af te kappen. Berichten worden afgekapt als ze uit meer dan 106 tekens bestaan voor binnenlandse betalingen. Voor internationale betalingen is dit 140 tekens. |

Zie [Betalingsregels en dagboekregels samenvatten](summarizing-payment-lines-and-general-journal-lines.md) voor meer informatie over de invloed van de twee velden op de wijze waarop betalingsdagboekregels worden overgedragen naar het dagboek.  

## <a name="see-also"></a>Zie ook

[Belgische lokale functionaliteit](belgium-local-functionality.md)  
[Belgische elektronische betalingen](belgian-electronic-payments.md)  
[CODA-bankafschriften](coda-bank-statements.md)  
[Incasso via domiciliëring](direct-debit-using-domiciliation.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]