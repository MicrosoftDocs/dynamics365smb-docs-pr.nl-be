---
title: Betalingsregels en dagboekregels samenvatten
description: Business Central geeft een overzicht van betalingsregels en dagboekregels.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d272ae25eb43533ce7285c29473ffcaac6e8464c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749714"
---
# <a name="summarizing-payment-lines-and-general-journal-lines"></a>Betalingsregels en dagboekregels samenvatten
Business Central geeft een overzicht van betalingsregels en dagboekregels van de volgende typen betalingen:  

- Binnenlandse betalingen  
- Internationale betalingen  
- SEPA-betalingen  
- Niet-euro SEPA-betalingen  

## <a name="how-payment-journal-lines-are-transferred-to-the-general-journal"></a>Hoe betalingsdagboekregels naar het grootboek worden overgebracht  
Wanneer u de betalingsdagboekregels naar een bestand exporteert, brengt [!INCLUDE[prod_short](../../includes/prod_short.md)] de betalingsdagboekregels naar het opgegeven dagboek over. Standaard wordt een dagboekregel gemaakt voor elke betalingsdagboekregel.  

De volgende twee velden op de pagina **Elektronisch bankieren instellen** bepalen hoe de betalingsregels worden samengevat:  

- **Alg. dagb.regels samenvatten**  
- **Tekst van betaalberichten afbreken**  

Als u het selectievakje **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** hebt geselecteerd, vat [!INCLUDE[prod_short](../../includes/prod_short.md)] alle betalingsdagboekregels voor een bepaalde leverancier in één dagboekregel samen. De algemene beschrijving "Betaling %1", waarbij %1 het nummer van de leverancier is, wordt gebruikt voor de beknopte journaalregelbeschrijving. Er worden een afzonderlijke betalingsregel en een aparte dagboekregel gemaakt om het volgende af te handelen:  

- Betalingsdagboekregels die gedeeltelijke betalingen bevatten, met zowel het veld **Gedeeltelijke betaling** als het veld **Afzonderlijke regel** ingeschakeld.  

- Betalingsdagboekregels die een bericht met een standaardindeling bevatten (slagen voor de MOD97-test), waarmee **Bericht met standaardindeling** op Waar wordt ingesteld in het dagboek voor elektronisch bankieren.

## <a name="example-1"></a>Voorbeeld 1  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. [!INCLUDE[prod_short](../../includes/prod_short.md)] maakt:  

- Een gecombineerde betalingsregel in een XML-bestand met een samengevoegd betalingsbericht. Spaties zijn het scheidingsteken.  
- Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.  

## <a name="example-2"></a>Voorbeeld 2  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. Het selectievakje **Tekst van betaalberichten afbreken** wordt gewist en de gecombineerde SEPA- en niet-auto SEPA-betalingsregels overschrijden 140 tekens in het betalingsbericht. [!INCLUDE[prod_short](../../includes/prod_short.md)] maakt:  

- Twee gecombineerde betalingsregels in een XML-bestand. De eerste betalingsregel bevat de eerste samengevoegde betalingsberichten. De tweede betalingsregel bevat het betalingsbericht vanaf de derde regel.  

- Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.  

## <a name="example-3"></a>Voorbeeld 3  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. Het selectievakje **Tekst van betaalberichten afbreken** wordt ook ingeschakeld en de gecombineerde SEPA- en niet-SEPA betalingsregels overschrijden 140 tekens in het betalingsbericht. [!INCLUDE[prod_short](../../includes/prod_short.md)] maakt:  

- Eén gecombineerde betalingsregel in een XML-bestand met twee samengevoegde betalingsberichten. Een beletselteken (…) wordt gebruikt om aan te geven dat het bericht afgekapt is.  

- Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.  

Op basis van de XML-structuur worden betalingen samengevat per rekeningnummer, bankrekeningnummer van de begunstigde en bankrekeningnummer. Het filter voor de bankrekening kan leeg zijn.  

De EndToEndId in het SEPA-bericht wordt gehaald uit het betalingsbericht en kan worden afgekapt tot de maximumlengte van 45 tekens.  

## <a name="see-also"></a>Zie ook  
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)   
 [Financiën instellen](../../finance-setup-finance.md)  
 [Inkopen vastleggen](../../purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]