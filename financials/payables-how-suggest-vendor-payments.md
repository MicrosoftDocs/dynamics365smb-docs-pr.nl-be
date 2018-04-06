---
title: De batchverwerking Betalingsvoorstellen maken gebruiken| Microsoft Docs
description: U kunt leveranciersbetalingsinstellingen opgeven om voorstellen of voorstellen voor betalingen te krijgen die binnenkort moeten worden betaald of waar een korting beschikbaar is.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 384bc05b8f775859c9ca6d6ea4241efb63a9e69d
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="suggest-vendor-payments"></a>Leveranciersbetalingen voorstellen
In het venster **Betalingsdagboek** kunt u door middel van de batchverwerking **Leveranciersbetalingen voorstellen** betalingsregels laten voorstellen. Regels voor zaken als betalingen die binnenkort moeten worden betaald, of betalingen waarbij een contantkorting beschikbaar is, worden weergegeven op basis van de instellingen.

Om optimaal van voorgestelde regels te profiteren, moet u uw leveranciers eerst naar prioriteit indelen. Zie voor meer informatie [Leveranciers in een prioriteitsvolgorde plaatsen](purchasing-how-prioritize-vendors.md).  

De leveranciersposten die **Afwachten** zijn, worden niet opgenomen.  

> [!IMPORTANT]  
>   Als u wilt profiteren van contantkortingen en een beschikbaar bedrag hebt ingevoerd, wordt dit bedrag gebruikt voor de volgende posten:  

* Prioritaire openstaande leveranciersposten eerst, in volgorde van prioriteit.  
* Achterstallige posten zonder prioriteitsnummer.  
* Openstaande leveranciersposten die voor contantkortingen in aanmerking komen, geordend op leveranciersnummer.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>De functie Leveranciersbetalingen voorstellen gebruiken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2. Open het desbetreffende dagboek en kies vervolgens de actie **Leveranciersbetalingen voorstellen**.  
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Kies de knop **Ok**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>De vervaldatum als boekingsdatum invoegen op betalingsdagboekregels
Wanneer u de batchverwerking **Leveranciersbetalingen voorstellen** gebruikt om betalingsregels voor uw leveranciers te maken, kunt u twee speciale velden invullen om te zorgen dat de gegenereerde regels de vervaldatum gebruiken om de boekingsdatum te berekenen. Deze velden zijn **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** en **Vervaldatumafwijking vereffeningsdoc.**.  

> [!IMPORTANT]  
>   U kunt het veld **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** niet samen gebruiken met het veld **Contantkorting nemen** of het veld **Een regel per leverancier**. Als de boekingsdatum is gebaseerd op de vervaldatum, worden enkele contantkortingen mogelijk niet correct berekend, omdat de boekingsdatum na de vervaldatum voor contantkorting ligt.  

En als de berekende boekingsdatum in het verleden ligt, wordt de boekingsdatum voorwaarts verplaatst naar de volgende werkdatum en wordt een waarschuwing weergegeven.  

U kunt eventueel handmatig betalingsregels maken, waarbij de vervaldatum wordt gebruikt om de boekingsdatum te berekenen. Nadat u posten hebt vereffend, kunt u met de actie **Boekingssdatum berekenen** de boekingsdatum op de dagboekregel bijwerken met de vervaldatum van de gerelateerde inkoopfactuur. Zie voor meer informatie [Inkooptransacties handmatig vereffenen](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Als de inkoopfactuur achterstallig is, wordt de boekingsdatum ingesteld op de werkdatum en wordt het lettertype op de regel rood.  

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Betalingen uitvoeren](payables-make-payments.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

