---
title: 'Wijzigingen in codeunit 12: Wijzigingen in procedures voor grootboekboeking'
description: In eerdere versies is codeunit 12 gewijzigd om de prestaties bij het boeken vanuit het dagboek te verbeteren. Lees meer over de wijzigingen in de boekingsprocedures in dit artikel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: c1ec373b6c7226d6b2548f2b29f326dcd9c6a459
ms.sourcegitcommit: a95681db16e81af109b34f8e5d88028c1552c6a2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367921"
---
# <a name="historical-changes-to-codeunit-12-changes-in-general-journal-post-procedures"></a>Historische wijzigingen in codeunit 12: Wijzigingen in procedures voor grootboekboekingen

De volgende wijzigingen zijn geïmplementeerd in versies van [!INCLUDE [navnow_md](includes/navnow_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Opmerking**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GetGLReg|GetGLReg|Bijgewerkt|  
|RunWithCheck|RunWithCheck|Bijgewerkt|  
|RunWithoutCheck|RunWithoutCheck|Bijgewerkt|  
|Code|Code|Bijgewerkt|  
||PostGenJnlLine|Toegevoegd|  
||InitAmounts|Toegevoegd|  
||InitLastDocDate|Toegevoegd|  
|InitVAT|InitVAT|Bijgewerkt|  
|PostVAT|PostVAT|Bijgewerkt|  
|InsertVAT|InsertVAT|Bijgewerkt|  
|SummarizeVAT|SummarizeVAT|Bijgewerkt|  
|InsertSummarizedVAT|InsertSummarizedVAT|Bijgewerkt|  
|PostGLAcc|PostGLAcc|Bijgewerkt|  
|PostCust|PostCust|Bijgewerkt|  
|PostVend|PostVend|Bijgewerkt|  
|PostBankAcc|PostBankAcc|Bijgewerkt|  
|PostFixedAsset|PostFixedAsset|Bijgewerkt|  
|PostICPartner|PostICPartner|Bijgewerkt|  
|InitCodeUnit|StartPosting|Bijgewerkt|  
||ContinuePosting|Toegevoegd|  
|FinishCodeunit|FinishPosting|Bijgewerkt|  
||PostUnrealizedVAT|Toegevoegd|  
||CheckPostUnrealizedVAT|Toegevoegd|  
||ExchangeAccounts|Toegevoegd|  
|InitGLEntry|InitGLEntry|Bijgewerkt|  
||InitGLEntryVAT|Toegevoegd|  
||InitGLEntryVATCopy|Toegevoegd|  
|InsertGLEntry|InsertGLEntry|Bijgewerkt|  
||CreateGLEntry|Toegevoegd|  
||CreateGLEntryBalAcc|Toegevoegd|  
||CreateGLEntryVAT|Toegevoegd|  
||CreateGLEntryVATCollectAdj|Toegevoegd|  
||CreateGLEntryFromVATEntry|Toegevoegd|  
||UpdateCheckAmounts|Toegevoegd|  
|ApplyCustLedgEntry|ApplyCustLedgEntry|Bijgewerkt|  
||CalcPmtDiscPossible|Toegevoegd|  
||CalcPmtTolerancePossible|Toegevoegd|  
|CalcPmtTolerance|CalcPmtTolerance|Bijgewerkt|  
|CalcPmtDisc|CalcPmtDisc|Bijgewerkt|  
|CalcPmtDiscIfAdjVAT|CalcPmtDiscIfAdjVAT|Bijgewerkt|  
|CalcPmtDiscTolerance|CalcPmtDiscTolerance|Bijgewerkt|  
||CalcPmtDiscVATBases|Toegevoegd|  
||CalcPmtDiscVATAmounts|Toegevoegd|  
||InsertPmtDiscVATForVATEntry|Toegevoegd|  
||InsertPmtDiscVATForGLEntry|Toegevoegd|  
|CalcCurrencyApplnRounding|CalcCurrencyApplnRounding|Bijgewerkt|  
|FindAmtForAppln|FindAmtForAppln|Bijgewerkt|  
|CalcCurrencyUnrealizedGainLoss|CalcCurrencyUnrealizedGainLoss|Bijgewerkt|  
|CalcCurrencyRealizedGainLoss|CalcCurrencyRealizedGainLoss|Bijgewerkt|  
|CalcApplication|CalcApplication|Bijgewerkt|  
|CalcRemainingPmtDisc|CalcRemainingPmtDisc|Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|CalcAmtLCYAdjustment|CalcAmtLCYAdjustment|Toegevoegd|  
|InitNewCVLedgEntry|InitFromGenJnlLine|Verplaatst naar tabel 383 Gedetailleerde K/L-postbuffer|  
|InitOldCVLedgEntry|CopyFromCVLedgEntryBuf|Verplaatst naar tabel 383 Gedetailleerde K/L-postbuffer|  
|InsertDtldCVLedgEntry|InsertDtldCVLedgEntry|Verplaatst naar tabel 383 Gedetailleerde K/L-postbuffer|  
||InitBankAccLedgEntry|Toegevoegd|  
||InitCheckLedgEntry|Toegevoegd|  
||InitCustLedgEntry|Toegevoegd|  
||InitVendLedgEntry|Toegevoegd|  
||InsertDtldCustLedgEntry|Toegevoegd|  
||InsertDtldVendLedgEntry|Toegevoegd|  
|CustUnrealizedVAT|CustUnrealizedVAT|Bijgewerkt|  
|CustPostApplyCustLedgEntry|CustPostApplyCustLedgEntry|Bijgewerkt|  
||PrepareTempCustLedgEntry|Toegevoegd|  
|UnapplyCustLedgEntry|UnapplyCustLedgEntry|Bijgewerkt|  
|TransferCustLedgEntry|CopyFromGenJnlLine|Verplaatst naar tabel 21 Klantenpost|  
|PostDtldCustLedgEntries|PostDtldCustLedgEntries|Bijgewerkt|  
||PostDtldCustLedgEntry|Toegevoegd|  
||PostDtldCustLedgEntryUnapply|Toegevoegd|  
||GetDtldCustLedgEntryAccNo|Toegevoegd|  
|ZeroTransNoDtldCustLedgEntries|SetZeroTransNo|Verplaatst naar tabel 379 Gedetailleerde klantenpost|  
|AutoEntrForDtldCustLedgEntries||Opnieuw gestructureerd naar PostDtldCustLedgEntryUnapply|  
|CustUpdateDebitCredit|UpdateDebitCredit|Verplaatst naar tabel 379 Gedetailleerde klantenpost|  
|ApplyVendLedgEntry|ApplyVendLedgEntry|Bijgewerkt|  
||PrepareTempVendLedgEntry|Toegevoegd|  
|VendPostApplyVendLedgEntry|VendPostApplyVendLedgEntry|Bijgewerkt|  
|UnapplyVendLedgEntry|UnapplyVendLedgEntry|Bijgewerkt|  
|TransferVendLedgEntry|CopyFromGenJnlLine|Verplaatst naar tabel 25 Leverancierspost|  
|PostDtldVendLedgEntries|PostDtldVendLedgEntries|Bijgewerkt|  
||PostDtldVendLedgEntry|Toegevoegd|  
||PostDtldVendLedgEntryUnapply|Toegevoegd|  
||GetDtldVendLedgEntryAccNo|Toegevoegd|  
||PostDtldCVLedgEntry|Toegevoegd|  
||PostDtldCustVATAdjustment|Toegevoegd|  
||PostDtldVendVATAdjustment|Toegevoegd|  
|ZeroTransNoDtldVendLedgEntries|SetZeroTransNo|Verplaatst naar tabel 380 Gedetail. leverancierspost|  
|AutoEntrForDtldVendLedgEntries||Opnieuw gestructureerd naar PostDtldVendLedgEntryUnapply|  
|VendUpdateDebitCredit|UpdateDebitCredit|Verplaatst naar tabel 380 Gedetail. leverancierspost|  
|VendUnrealizedVAT|VendUnrealizedVAT|Bijgewerkt|  
||PostUnrealVATEntry|Toegevoegd|  
||PostApply|Toegevoegd|  
|PostUnrealVATByUnapply|PostUnrealVATByUnapply|Bijgewerkt|  
||PostUnapply|Toegevoegd|  
||InsertDtldCustLedgEntryUnapply|Toegevoegd|  
||InsertDtldVendLedgEntryUnapply|Toegevoegd|  
||InsertTempVATEntry|Toegevoegd|  
||ProcessTempVATEntry|Toegevoegd|  
||UpdateCustLedgEntry|Toegevoegd|  
||UpdateVendLedgEntry|Toegevoegd|  
|UpdateCalcInterest|UpdateCalcInterest|Bijgewerkt|  
|UpdateCalcInterest2|UpdateCalcInterest2|Bijgewerkt|  
|GLCalcAddCurrency|GLCalcAddCurrency|Bijgewerkt|  
|HandleAddCurrResidualGLEntry|HandleAddCurrResidualGLEntry|Bijgewerkt|  
|CalcLCYToAddCurr|CalcLCYToAddCurr|Bijgewerkt|  
|CalcAddCurrFactor||Verwijderd|  
|GetCurrencyExchRate|GetCurrencyExchRate|Bijgewerkt|  
|ExchAmount|ExchangeAmount|Verplaatst naar tabel 330 Valutawisselkoers|  
|ExchangeAmtLCYToFCY2|ExchangeAmtLCYToFCY2|Bijgewerkt|  
|CalcAddCurrForUnapplication|CalcAddCurrForUnapplication|Bijgewerkt|  
|CheckNonAddCurrCodeOccurred|CheckNonAddCurrCodeOccurred|Bijgewerkt|  
|CheckCalcPmtDisc||Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|CheckCalcPmtDiscCVCust||Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|CheckCalcPmtDiscCust||Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|CheckCalcPmtDiscGenJnlCust||Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|CheckCalcPmtDiscCVVend||Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|CheckCalcPmtDiscVend||Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|CheckCalcPmtDiscGenJnlVend||Verplaatst naar codeunit 426 Betalingstolerantiebeheer|  
|Reverse|Reverse|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|ReverseVendLedgEntry|ReverseVendLedgEntry|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|ReverseVAT|ReverseVAT|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|SetReversalDescription|SetReversalDescription|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Verplaatst naar codeunit 17 Dagboek - Tegenboeken|  
||CheckDimComb|Toegevoegd in Codeunit 17 Gen. Dagboek - Tegenboeken|  
||CopyCustLedgEntry|Toegevoegd in Codeunit 17 Gen. Dagboek - Tegenboeken|  
||CopyVendLedgEntry|Toegevoegd in Codeunit 17 Gen. Dagboek - Tegenboeken|  
||CopyBankAccLedgEntry|Toegevoegd in Codeunit 17 Gen. Dagboek - Tegenboeken|  
|HandlDtlAddjustment|HandleDtldAdjustment|Bijgewerkt|  
|CollectAddjustment|CollectAdjustment|Bijgewerkt|  
|SetOverDimErr|SetOverDimErr|Bijgewerkt|  
|PostJob|PostJob|Bijgewerkt|  
|InsertVATEntriesFromTemp|InsertVATEntriesFromTemp|Bijgewerkt|  
|CaptureOrRefundCreditCardPmnt|CaptureOrRefundCreditCardPmnt|Bijgewerkt|  
|UpdateDOPaymentTransactEntry|UpdateDOPaymentTransactEntry|Bijgewerkt|  
|ABSMin|ABSMin|Bijgewerkt|  
|GetApplnRoundPrecision|GetApplnRoundPrecision|Bijgewerkt|  
|CheckDimValueForDisposal|CheckDimValueForDisposal|Bijgewerkt|  
|CalculateCurrentBalance|CalculateCurrentBalance|Bijgewerkt|  
|IncludeVATAmount||Verplaatst naar tabel 81 regel|  
|CalcVATAmountFromVATEntry|CalcVATAmountFromVATEntry|Bijgewerkt|  
||TotalVATAmountOnJnlLines|Toegevoegd|  
||SetGLRegReverse|Toegevoegd|  
||GetGLSetup|Toegevoegd|  
||ReadGLSetup|Toegevoegd|  
||CheckSalesExtDocNo|Toegevoegd|  
||CheckPurchExtDocNo|Toegevoegd|  
||CheckGLAccDimError|Toegevoegd|  
||GetCurrency|Toegevoegd|  
||PostDtldAdjustment|Toegevoegd|  
||GetNextEntryNo|Toegevoegd|  
||GetNextTransactionNo|Toegevoegd|  
||GetNextVATEntryNo|Toegevoegd|  
||IncrNextVATEntryNo|Toegevoegd|  
||IsNotPayment|Toegevoegd|  
||IsTempGLEntryBufEmpty|Toegevoegd|  
||IsVATAdjustment|Toegevoegd|  
||IsVATExcluded|Toegevoegd|  
||UpdateDimensions|Toegevoegd|  
||UpdateDimensionsFromCustLedgEntry|Toegevoegd|  
||UpdateDimensionsFromVendLedgEntry|Toegevoegd|  
||UpdateTotalAmounts|Toegevoegd|  
||CreateGLEntriesForTotalAmounts|Toegevoegd|  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Wijzigingen in codeunit 12: Algemene variabelen toewijzen voor dagboekboekingsregel](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)
