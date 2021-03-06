---
title: SEPA-betalingen in andere valuta's dan de euro indienen
description: In de Belgische versie van Business Central kunt u niet-euro SEPA-betalingen bij de bank archiveren. Dit is handig als u betalingen verzendt naar andere landen/regio's die SEPA niet gebruiken en voor andere valuta's dan de euro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 90c1e00584ae633b0feafd5a0420f7565db8d9c2
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379553"
---
# <a name="file-non-euro-sepa-payments"></a>SEPA-betalingen in andere valuta's dan de euro indienen
In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank. Dit is handig als u betalingen verzendt naar andere landen/regio's die SEPA niet gebruiken en voor andere valuta's dan de euro.  

Voordat u een dergelijke SEPA-betalingen kunt indienen, moet u de volgende beheertaken uitvoeren:  

- Stel een nieuw exportprotocol voor een niet-euro-SEPA in.  
- Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** uit voor elk land in de EEA-zone.  
- Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** niet in euro's is.  
- Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.  

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
 [SEPA-betalingen indienen](how-to-file-sepa-payments.md)   
 [SEPA-betalingen activeren](how-to-activate-sepa-payments.md)   
 [SEPA-betalingen](sepa-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]