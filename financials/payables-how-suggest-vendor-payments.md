---
title: 'Procedure: Leveranciersbetalingen voorstellen | Microsoft Docs'
description: 'Procedure: Leveranciersbetalingen voorstellen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4b85fc783cdebb7c1d2e048315e48aee02a189fa
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-suggest-vendor-payments"></a>Procedure: Leveranciersbetalingen voorstellen
In het venster **Betalingsdagboek** kunt u door middel van de batchverwerking **Leveranciersbetalingen voorstellen** betalingsregels laten voorstellen. Regels voor zaken als betalingen die binnenkort moeten worden betaald, of betalingen waarbij een contantkorting beschikbaar is, worden weergegeven op basis van de instellingen.

Om optimaal van voorgestelde regels te profiteren, moet u uw leveranciers eerst naar prioriteit indelen. Zie voor meer informatie [Procedure: leveranciers in een prioriteitsvolgorde plaatsen](purchasing-how-prioritize-vendors.md).  

De leveranciersposten die **Afwachten** zijn, worden niet opgenomen.  

**Belangrijk:** Als u wilt profiteren van contantkortingen en een beschikbaar bedrag hebt ingevoerd, wordt dit bedrag gebruikt voor de volgende posten:  

* Prioritaire openstaande leveranciersposten eerst, in volgorde van prioriteit.  
* Achterstallige posten zonder prioriteitsnummer.  
* Openstaande leveranciersposten die voor contantkortingen in aanmerking komen, geordend op leveranciersnummer.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>De functie Leveranciersbetalingen voorstellen gebruiken
1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik op de gerelateerde koppeling.  
2. Open het desbetreffende dagboek en kies vervolgens de actie **Leveranciersbetalingen voorstellen**.  
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Kies de knop **Ok**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>De vervaldatum als boekingsdatum invoegen op betalingsdagboekregels
Wanneer u de batchverwerking **Leveranciersbetalingen voorstellen** gebruikt om betalingsregels voor uw leveranciers te maken, kunt u twee speciale velden invullen om te zorgen dat de gegenereerde regels de vervaldatum gebruiken om de boekingsdatum te berekenen. Deze velden zijn **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** en **Vervaldatumafwijking vereffeningsdoc.**.  

**Belangrijk:** U kunt het veld **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** niet gebruiken in combinatie met het veld **Contantkorting nemen** of het veld **Een regel per leverancier** . Als de boekingsdatum is gebaseerd op de vervaldatum, worden enkele contantkortingen mogelijk niet correct berekend, omdat de boekingsdatum na de vervaldatum voor contantkorting ligt.  

En als de berekende boekingsdatum in het verleden ligt, wordt de boekingsdatum voorwaarts verplaatst naar de volgende werkdatum en wordt een waarschuwing weergegeven.  

U kunt eventueel handmatig betalingsregels maken, waarbij de vervaldatum wordt gebruikt om de boekingsdatum te berekenen. Nadat u posten hebt vereffend, kunt u met de actie **Boekingssdatum berekenen** de boekingsdatum op de dagboekregel bijwerken met de vervaldatum van de gerelateerde inkoopfactuur. Zie voor meer informatie [Procedure: Inkooptransacties handmatig vereffenen](payables-how-apply-purchase-transactions-manually.md).  

**Opmerking:** Als de inkoopfactuur achterstallig is, wordt de boekingsdatum ingesteld op de werkdatum en wordt het lettertype op de regel rood.  

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Betalingen doen](payables-make-payments.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

