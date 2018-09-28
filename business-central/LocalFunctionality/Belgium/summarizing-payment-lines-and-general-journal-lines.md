---
title: Betalingsregels en dagboekregels samenvatten
description: In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] worden verschillende soorten transacties op dezelfde manier afgehandeld.
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
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0e94b66ce548e2ba2ad5217b0ca04a0da6d08948
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="summarizing-payment-lines-and-general-journal-lines"></a>Betalingsregels en dagboekregels samenvatten
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] worden de volgende soorten transacties op dezelfde manier afgehandeld:  

- Binnenlandse betalingen  
- Internationale betalingen  
- SEPA-betalingen  
- Niet-euro SEPA-betalingen  

## <a name="how-payment-journal-lines-are-transferred-to-the-general-journal"></a>Hoe betalingsdagboekregels naar het grootboek worden overgebracht  
Wanneer u de betalingsdagboekregels naar een bestand exporteert, brengt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] de betalingsdagboekregels naar het opgegeven dagboek over. Standaard wordt een dagboekregel gemaakt voor elke betalingsdagboekregel.  

De volgende twee velden in het venster **Elektronisch bankieren instellen** bepalen hoe de betalingsregels worden samengevat:  

- **Alg. dagb.regels samenvatten**  
- **Tekst van betaalberichten afbreken**  

Als u het selectievakje **Alg. dagb.regels samenvatten** in het venster **Elektronisch bankieren instellen** hebt geselecteerd, vat [!INCLUDE[d365fin](../../includes/d365fin_md.md)] alle betalingsdagboekregels voor een bepaalde leverancier in één dagboekregel samen. De algemene omschrijving 'Betaling %1', waarbij %1 het leveranciersnummer is, wordt gebruikt voor de samengevatte dagboekregelomschrijving. Er worden een afzonderlijke betalingsregel en een aparte dagboekregel gemaakt om het volgende af te handelen:  

- Betalingsdagboekregels die gedeeltelijke betalingen bevatten, met zowel het veld **Gedeeltelijke betaling** als het veld **Afzonderlijke regel** ingeschakeld.  

- Betalingsdagboekregels die een bericht met een standaardindeling bevatten (dus slagen voor de MOD97-test), waarmee **Bericht met standaardindeling** op Waar wordt ingesteld in het dagboek voor elektronisch bankieren.  

## <a name="example-1"></a>Voorbeeld 1  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] maakt:  

- Een gecombineerde betalingsregel in een XML-bestand met een samengevoegd betalingsbericht. Spaties zijn het scheidingsteken.  
- Eén betaling in het grootboek met een algemene beschrijving die ../../de leveranciersnaam bevat.  

## <a name="example-2"></a>Voorbeeld 2  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. Het selectievakje **Tekst van betaalberichten afbreken** wordt gewist en gecombineerde SEPA- en niet-auto SEPA-betalingsregels overschrijden 140 tekens in het betalingsbericht. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] maakt:  

- Twee gecombineerde betalingsregels in een XML-bestand. De eerste betalingsregel bevat de eerste samengevoegde betalingsberichten. De tweede betalingsregel bevat het betalingsbericht vanaf de derde regel.  

- Eén betaling in het grootboek met een algemene beschrijving die ../../de leveranciersnaam bevat.  

## <a name="example-3"></a>Voorbeeld 3  
In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld. Het selectievakje **Tekst van betaalberichten afbreken** wordt ook ingeschakeld en gecombineerde SEPA- en niet-SEPA betalingsregels overschrijden 140 tekens in het betalingsbericht. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] maakt:  

- Eén gecombineerde betalingsregel in een XML-bestand met twee samengevoegde betalingsberichten. Een beletselteken (…) wordt gebruikt om aan te geven dat het bericht afgekapt is.  

- Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.  

Op basis van de XML-structuur worden betalingen samengevat per rekeningnummer en bankrekeningnummer van de begunstigde en bankrekening. Het bankrekeningfilter mag leeg zijn.  

De EndToEndId in het SEPA-bericht wordt gehaald uit het betalingsbericht en kan worden afgekapt tot de maximumlengte van 45 tekens.  

## <a name="see-also"></a>Zie ook  
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)   
 [Financiën instellen](../../finance-setup-finance.md)  
 [Inkopen vastleggen](../../purchasing-how-record-purchases.md) 

