---
title: Leveranciersbetalingen voorstellen
description: Gebruik de batchverwerking Leveranciersbetalingen voorstellen om betalingsregels voor uw leveranciers te maken op basis van vervaldatums en betalingskortingen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 07/17/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="suggest-vendor-payments"></a>Leveranciersbetalingen voorstellen

Op de pagina **Betalingsdagboek** kunt u door middel van de batchverwerking **Leveranciersbetalingen voorstellen** betalingsregels laten voorstellen. Op basis van uw instellingen stelt [!INCLUDE [prod_short](includes/prod_short.md)] regels voor het volgende voor:

- Betalingen die binnenkort verschuldigd zijn
- Betalingen waarbij een betalingskorting beschikbaar is.

Om optimaal van voorgestelde betalingen te profiteren, moet u uw leveranciers naar prioriteit indelen. Ga voor meer informatie over het prioriteren van leveranciers naar [De prioriteit van leveranciers bepalen](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> De batchverwerking sluit leveranciersposten uit die **Afwachten** of die al zijn toegepast en een waarde hebben in het veld **Vereffenings-id**.  

> [!IMPORTANT]  
> Als u wilt profiteren van contantkortingen en een beschikbaar bedrag hebt ingevoerd, wordt dit bedrag gebruikt voor de volgende posten:  
>
> * Prioritaire openstaande leveranciersposten eerst, in volgorde van prioriteit.
> * Achterstallige posten zonder prioriteitsnummer.  
> * Openstaande leveranciersposten die in aanmerking komen voor betalingskortingen. De posten zijn gerangschikt op leveranciersnummer.  

## <a name="use-the-suggest-vendor-payments-action"></a>De actie Leveranciersbetalingen voorstellen gebruiken

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en selecteer vervolgens de gerelateerde koppeling.  
2. Open het dagboek en selecteer vervolgens de actie **Leveranciersbetalingen voorstellen**.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Selecteer de knop **OK**.  

## <a name="insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>De vervaldatum als boekingsdatum invoegen op betalingsdagboekregels

Wanneer u de batchverwerking **Leveranciersbetalingen voorstellen** gebruikt om betalingsregels voor uw leveranciers te maken, kunt u twee speciale velden invullen om te zorgen dat de gegenereerde regels de vervaldatum gebruiken om de boekingsdatum te berekenen. Deze velden zijn **Bereken boekingsdatum van Toepasbaar-op-document. Vervaldatum** en **Toepasbaar-op-document. Vervaldatumoffset**.  

> [!IMPORTANT]  
> U kunt het veld  **Boekingsdatum berekenen op basis van Vervaldatum van toepassing op document** niet samen met het veld  **Betalingskortingen zoeken**  of het veld  **Samenvatten per leverancier**  gebruiken. Als de boekingsdatum is gebaseerd op de vervaldatum, worden enkele contantkortingen mogelijk niet correct berekend, omdat de boekingsdatum na de vervaldatum voor contantkorting ligt.  

En als de berekende boekingsdatum in het verleden ligt, wordt de boekingsdatum voorwaarts verplaatst naar de volgende werkdatum en wordt een waarschuwing weergegeven.  

U kunt ook handmatig betalingsregels maken, waarbij de vervaldatum wordt gebruikt om de boekingsdatum te berekenen. Nadat u posten hebt vereffend, kunt u met de actie **Boekingssdatum berekenen** de boekingsdatum op de dagboekregel bijwerken met de vervaldatum van de gerelateerde inkoopfactuur. Ga voor meer informatie over dit handmatige proces naar [Inkooptransacties handmatig vereffenen](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Als de inkoopfactuur achterstallig is, wordt de boekingsdatum ingesteld op de werkdatum en wordt het lettertype op de regel rood.  

## <a name="see-also"></a>Zie ook

- [Betalingsverplichtingen beheren](payables-manage-payables.md)  
- [Betalingen uitvoeren](payables-make-payments.md)  
- [Werken met dagboeken](ui-work-general-journals.md)  
- [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
