---
title: Betalingsregels en dagboekregels samenvatten
description: Business Central geeft een overzicht van betalingsregels en dagboekregels.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ab3c62c9040638c9373cbc975570e566dfaf4926
ms.sourcegitcommit: 5b6dd8d881c0eb65ece6936a94dfda3185574335
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/28/2019
ms.locfileid: "1710989"
---
# <a name="summarizing-payment-lines-and-general-journal-lines"></a>Betalingsregels en dagboekregels samenvatten
Business Central geeft een overzicht van betalingsregels en dagboekregels van de volgende typen betalingen:  

- Binnenlandse betalingen  
- Internationale betalingen  
- SEPA-betalingen  
- Niet-euro SEPA-betalingen  

## <a name="how-payment-journal-lines-are-transferred-to-the-general-journal"></a>Hoe betalingsdagboekregels naar het grootboek worden overgebracht  
Wanneer u de betalingsdagboekregels naar een bestand exporteert, brengt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] de betalingsdagboekregels naar het opgegeven dagboek over. Standaard wordt een dagboekregel gemaakt voor elke betalingsdagboekregel.  

De volgende twee velden op de pagina **Elektronisch bankieren instellen** bepalen hoe de betalingsregels worden samengevat:  

- **Alg. dagb.regels samenvatten**  
- **Tekst van betaalberichten afbreken**  

Als u het selectievakje **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** hebt geselecteerd, vat [!INCLUDE[d365fin](../../includes/d365fin_md.md)] alle betalingsdagboekregels voor een bepaalde leverancier in één dagboekregel samen. De algemene beschrijving "Betaling %1", waarbij %1 het nummer van de leverancier is, wordt gebruikt voor de beknopte journaalregelbeschrijving. Er worden een afzonderlijke betalingsregel en een aparte dagboekregel gemaakt om het volgende af te handelen:  

- Betalingsdagboekregels die gedeeltelijke betalingen bevatten, met zowel het veld **Gedeeltelijke betaling** als het veld **Afzonderlijke regel** ingeschakeld.  

- Betalingsdagboekregels die een bericht met een standaardindeling bevatten (slagen voor de MOD97-test), waarmee **Bericht met standaardindeling** op Waar wordt ingesteld in het dagboek voor elektronisch bankieren.

## <a name="example-1"></a>Voorbeeld 1  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] maakt:  

- Een gecombineerde betalingsregel in een XML-bestand met een samengevoegd betalingsbericht. Spaties zijn het scheidingsteken.  
- Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.  

## <a name="example-2"></a>Voorbeeld 2  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. Het selectievakje **Tekst van betaalberichten afbreken** wordt gewist en de gecombineerde SEPA- en niet-auto SEPA-betalingsregels overschrijden 140 tekens in het betalingsbericht. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] maakt:  

- Twee gecombineerde betalingsregels in een XML-bestand. De eerste betalingsregel bevat de eerste samengevoegde betalingsberichten. De tweede betalingsregel bevat het betalingsbericht vanaf de derde regel.  

- Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.  

## <a name="example-3"></a>Voorbeeld 3  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. Het selectievakje **Tekst van betaalberichten afbreken** wordt ook ingeschakeld en de gecombineerde SEPA- en niet-SEPA betalingsregels overschrijden 140 tekens in het betalingsbericht. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] maakt:  

- Eén gecombineerde betalingsregel in een XML-bestand met twee samengevoegde betalingsberichten. Een beletselteken (…) wordt gebruikt om aan te geven dat het bericht afgekapt is.  

- Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.  

Op basis van de XML-structuur worden betalingen samengevat per rekeningnummer, bankrekeningnummer van de begunstigde en bankrekeningnummer. Het filter voor de bankrekening kan leeg zijn.  

De EndToEndId in het SEPA-bericht wordt gehaald uit het betalingsbericht en kan worden afgekapt tot de maximumlengte van 45 tekens.  

## <a name="see-also"></a>Zie ook  
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)   
 [Financiën instellen](../../finance-setup-finance.md)  
 [Inkopen vastleggen](../../purchasing-how-record-purchases.md)
