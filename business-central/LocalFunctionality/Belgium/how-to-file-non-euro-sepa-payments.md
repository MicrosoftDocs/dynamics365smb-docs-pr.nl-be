---
title: SEPA-betalingen in andere valuta's dan de euro indienen
description: In de Belgische versie van Business Central kunt u niet-euro SEPA-betalingen bij de bank archiveren. Dit is handig als u betalingen verzendt naar andere landen/regio's die SEPA niet gebruiken en voor andere valuta's dan de euro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b7b8724155fa56fe8194f55f742ee6a87f36c725
ms.sourcegitcommit: 951d3c9d541f0b1d26712d37e253c2958dae3321
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889172"
---
# <a name="file-non-euro-sepa-payments"></a>SEPA-betalingen in andere valuta's dan de euro indienen
In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank. Dit is handig als u betalingen verzendt naar andere landen/regio's die SEPA niet gebruiken en voor andere valuta's dan de euro.  

Voordat u een dergelijke SEPA-betalingen kunt indienen, moet u de volgende beheertaken uitvoeren:  

- Stel een nieuw exportprotocol voor een niet-euro-SEPA in.  
- Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** uit voor elk land in de EEA-zone.  
- Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** niet in euro's is.  
- Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN- en SWIFT-code bevat.  

## <a name="to-file-a-non-euro-sepa-payment"></a>Een SEPA-betaling in andere valuta's dan de euro indienen  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SEPA-betalingen in andere valuta's dan de euro indienen** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Dagboeksjabloon**|Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.|  
    |**Dagboekbatch**|Geef de dagboekbatch voor het SEPA-betalingsrapport op.|  
    |**Dagboekregels boeken**|Geef op of u de betalingsregels naar het grootboek wilt overbrengen.|  
    |**Dimensies opnemen**|Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen. De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** is geselecteerd.|  
    |**Uitvoeringsdatum**|Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.|  
    |**Bestandsnaam**|Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.|  

3.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook

[SEPA-betalingen activeren](how-to-activate-sepa-payments.md)  
[Betalingen verrichten met de extensie AMC Banking 365 Fundamentals of SEPA-krediettransfer](../../finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
