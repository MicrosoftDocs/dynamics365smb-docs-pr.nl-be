---
title: Batchverwerking Leveranciersbetalingen voorstellen
description: U kunt leveranciersbetalingsinstellingen opgeven om voorstellen of voorstellen voor betalingen te krijgen die binnenkort moeten worden betaald of waar een korting beschikbaar is.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: 256
ms.date: 04/01/2021
ms.author: edupont
---
# Leveranciersbetalingen voorstellen

Op de pagina **Betalingsdagboek** kunt u door middel van de batchverwerking **Leveranciersbetalingen voorstellen** betalingsregels laten voorstellen. Regels voor betalingen die binnenkort moeten worden betaald, of betalingen waarbij een contantkorting beschikbaar is, worden weergegeven op basis van de instellingen.

Om optimaal van voorgestelde betalingen te profiteren, moet u uw leveranciers eerst naar prioriteit indelen. Zie voor meer informatie [Leveranciers in een prioriteitsvolgorde plaatsen](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Leveranciersposten die **Afwachten**, worden niet opgenomen in de batchverwerking.  

> [!IMPORTANT]  
>   Als u wilt profiteren van contantkortingen en een beschikbaar bedrag hebt ingevoerd, wordt dit bedrag gebruikt voor de volgende posten:  
    * Prioritaire openstaande leveranciersposten eerst, in volgorde van prioriteit.   
    * Achterstallige posten zonder prioriteitsnummer.  
    * Openstaande leveranciersposten die voor contantkortingen in aanmerking komen, geordend op leveranciersnummer.  

## De functie Leveranciersbetalingen voorstellen gebruiken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open het desbetreffende dagboek en kies vervolgens de actie **Leveranciersbetalingen voorstellen**.  
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Kies de knop **Ok**.  

## De vervaldatum als boekingsdatum invoegen op betalingsdagboekregels

Wanneer u de batchverwerking **Leveranciersbetalingen voorstellen** gebruikt om betalingsregels voor uw leveranciers te maken, kunt u twee speciale velden invullen om te zorgen dat de gegenereerde regels de vervaldatum gebruiken om de boekingsdatum te berekenen. Deze velden zijn **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** en **Vervaldatumafwijking vereffeningsdoc.**.  

> [!IMPORTANT]  
>   U kunt het veld **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** niet samen gebruiken met het veld **Contantkorting nemen** of het veld **Een regel per leverancier**. Als de boekingsdatum is gebaseerd op de vervaldatum, worden enkele contantkortingen mogelijk niet correct berekend, omdat de boekingsdatum na de vervaldatum voor contantkorting ligt.  

En als de berekende boekingsdatum in het verleden ligt, wordt de boekingsdatum voorwaarts verplaatst naar de volgende werkdatum en wordt een waarschuwing weergegeven.  

U kunt eventueel handmatig betalingsregels maken, waarbij de vervaldatum wordt gebruikt om de boekingsdatum te berekenen. Nadat u posten hebt vereffend, kunt u met de actie **Boekingssdatum berekenen** de boekingsdatum op de dagboekregel bijwerken met de vervaldatum van de gerelateerde inkoopfactuur. Zie voor meer informatie [Inkooptransacties handmatig vereffenen](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Als de inkoopfactuur achterstallig is, wordt de boekingsdatum ingesteld op de werkdatum en wordt het lettertype op de regel rood.  

## Zie gerelateerde [Microsoft-training](/training/modules/suggest-vendor-payments-dynamics-365-business-central/)

## Zie ook

[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Betalingen uitvoeren](payables-make-payments.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
