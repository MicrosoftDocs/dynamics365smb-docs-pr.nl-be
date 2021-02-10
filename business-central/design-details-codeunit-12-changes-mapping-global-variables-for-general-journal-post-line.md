---
title: Wijzigingen in het toewijzen van globale variabelen voor boeking in Codeunit 12
description: In eerdere versies is codeunit 12 gewijzigd om de prestaties bij het boeken vanuit het dagboek te verbeteren. Lees meer over de wijzigingen in de globale variabelen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: 0fc79ba982e17b9295f0f611ca34b4eb615001f3
ms.sourcegitcommit: a95681db16e81af109b34f8e5d88028c1552c6a2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367771"
---
# <a name="historical-changes-to-codeunit-12-mapping-global-variables-for-general-journal-post-line"></a>Historische wijzigingen in codeunit 12: Globale variabelen toewijzen voor dagboekboekingsregel

De volgende wijzigingen zijn geïmplementeerd in versies van [!INCLUDE [navnow_md](includes/navnow_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Opmerking**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Ongewijzigd|  
|SalesSetup@1010 : Record 311;||Gewijzigd naar lokaal|  
|PurchSetup@1011 : Record 312;||Gewijzigd naar lokaal|  
|AccountingPeriod@1012 : Record 50;||Gewijzigd naar lokaal|  
|GLAcc@1013 : Record 15;||Gewijzigd naar lokaal|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Naam gewijzigd|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Naam gewijzigd|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Ongewijzigd|  
|OrigGLEntry@1017 : Record 17;||Verwijderd|  
|VATPostingSetup@1019 : Record 325;||Gewijzigd naar lokaal|  
|Cust@1020 : Record 18;||Gewijzigd naar lokaal|  
|Vend@1021 : Record 23;||Gewijzigd naar lokaal|  
|GenJnlLine@1022 : Record 81;||Gewijzigd naar lokaal|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Ongewijzigd|  
|CustPostingGr@1030 : Record 92;||Gewijzigd naar lokaal|  
|VendPostingGr@1031 : Record 93;||Gewijzigd naar lokaal|  
|Currency@1032 : Record 4;||Gewijzigd naar lokaal|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Ongewijzigd|  
|ApplnCurrency@1034 : Record 4;||Gewijzigd naar lokaal|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Ongewijzigd|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Ongewijzigd|  
|BankAcc@1039 : Record 270;||Gewijzigd naar lokaal|  
|BankAccLedgEntry@1040 : Record 271;||Gewijzigd naar lokaal|  
|CheckLedgEntry@1041 : Record 272;||Gewijzigd naar lokaal|  
|CheckLedgEntry2@1042 : Record 272;||Gewijzigd naar lokaal|  
|BankAccPostingGr@1043 : Record 277;||Gewijzigd naar lokaal|  
|GenJnlTemplate@1044 : Record 80;||Gewijzigd naar lokaal|  
|TaxJurisdiction@1045 : Record 320;||Gewijzigd naar lokaal|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Ongewijzigd|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Gewijzigd naar lokaal|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Ongewijzigd|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Ongewijzigd|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Ongewijzigd|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Ongewijzigd|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Verplaatst naar Codeunit17|  
|CostAccSetup@1092 : Record 1108;||Gewijzigd naar lokaal|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Ongewijzigd|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Gewijzigd naar lokaal|  
|FAJnlPostLine@1050 : Codeunit 5632;||Gewijzigd naar lokaal|  
|SalesTaxCalculate@1051 : Codeunit 398;||Gewijzigd naar lokaal|  
|GenJnlApply@1052 : Codeunit 225;||Gewijzigd naar lokaal|  
|DimMgt@1053 : Codeunit 408;||Gewijzigd naar lokaal|  
|JobPostLine@1028 : Codeunit 1001;||Gewijzigd naar lokaal|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Gewijzigd naar lokaal|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Toegevoegd|  
||AddCurrencyCode@1117 : Code[10];|Toegevoegd|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Ongewijzigd|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Ongewijzigd|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Ongewijzigd|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Ongewijzigd|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Ongewijzigd|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Ongewijzigd|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Ongewijzigd|  
|SalesTaxBaseAmount@1061 : Decimal;||Gewijzigd naar lokaal|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Ongewijzigd|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Ongewijzigd|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Ongewijzigd|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Ongewijzigd|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Ongewijzigd|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Ongewijzigd|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Ongewijzigd|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Ongewijzigd|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Ongewijzigd|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Ongewijzigd|  
|LastLineNo@1070 : Integer;||Verwijderd|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Ongewijzigd|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Ongewijzigd|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Ongewijzigd|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Ongewijzigd|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Ongewijzigd|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Ongewijzigd|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Ongewijzigd|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Ongewijzigd|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Ongewijzigd|  
|AllApplied@1081 : Boolean;||Gewijzigd naar lokaal|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Ongewijzigd|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Ongewijzigd|  
|Prepayment@1037 : Boolean;||Verwijderd|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Ongewijzigd|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Ongewijzigd|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Ongewijzigd|  
||GLSetupRead@1015 : Boolean;|Toegevoegd|  
||AmountRoundingPrecision@1012 : Decimal;|Toegevoegd|  
||CrCardTransactionEntryNo@1013 : Integer;|Toegevoegd|  

## <a name="see-also"></a>Zie ook  
 [Designdetails: Wijzigingen in codeunit 12: Wijzigingen in procedures voor grootboekboekingen](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)
