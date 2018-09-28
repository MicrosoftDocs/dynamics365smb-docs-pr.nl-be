---
title: 'Ontwerpdetails - Wijzigingen in codeunit 12: Toewijzing algemene variabelen voor dagboekboekingsregel | Microsoft Docs'
description: "De volgende wijzigingen zijn geïmplementeerd in deze versie van Business Central."
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
ms.openlocfilehash: aae8b02b95d3e385030610533f4b1b7f04602d5e
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Wijzigingen in codeunit 12: Toewijzing algemene variabelen voor dagboekboekingsregel
De volgende wijzigingen zijn geïmplementeerd in deze versie van [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Opmerking**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Ongewijzigd|  
|SalesSetup@1010 : Record 311;||Gewijzigd naar lokaal|  
|PurchSetup@1011 : Record 312;||Gewijzigd naar lokaal|  
|AccountingPeriod@1012 : Record 50;||Gewijzigd naar lokaal|  
|GLAcc@1013 : Record 15;||Gewijzigd naar lokaal|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Naam gewijzigd|  
|GLEntryTmp@1015 : TIJDELIJKE record 17;|TempGLEntryBuf@1010 : TIJDELIJKE record 17;|Naam gewijzigd|  
|TempGLEntryVAT@1016 : TIJDELIJKE record 17;|TempGLEntryVAT@1016 : TIJDELIJKE record 17;|Ongewijzigd|  
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
|FAGLPostBuf@1047 : TIJDELIJKE record 5637;||Gewijzigd naar lokaal|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Ongewijzigd|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Ongewijzigd|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Ongewijzigd|  
|TempVATEntry@1088 : TIJDELIJKE record 254;|TempVATEntry@1088 : TIJDELIJKE record 254;|Ongewijzigd|  
|ReversedGLEntryTemp@1089 : TIJDELIJKE Record 17;||Verplaatst naar Codeunit17|  
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
|FiscalYearStartDate@1054 : Datum;|FiscalYearStartDate@1011 : Datum;|Ongewijzigd|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Ongewijzigd|  
|BalanceCheckAmount@1056 : Decimaal;|BalanceCheckAmount@1056 : Decimaal;|Ongewijzigd|  
|BalanceCheckAmount2@1057 : Decimaal;|BalanceCheckAmount2@1057 : Decimaal;|Ongewijzigd|  
|BalanceCheckAddCurrAmount@1058 : Decimaal;|BalanceCheckAddCurrAmount@1058 : Decimaal;|Ongewijzigd|  
|BalanceCheckAddCurrAmount2@1059 : Decimaal;|BalanceCheckAddCurrAmount2@1059 : Decimaal;|Ongewijzigd|  
|CurrentBalance@1060 : Decimaal;|CurrentBalance@1060 : Decimaal;|Ongewijzigd|  
|SalesTaxBaseAmount@1061 : Decimaal;||Gewijzigd naar lokaal|  
|TotalAddCurrAmount@1062 : Decimaal;|TotalAddCurrAmount@1062 : Decimaal;|Ongewijzigd|  
|TotalAmount@1063 : Decimaal;|TotalAmount@1063 : Decimaal;|Ongewijzigd|  
|UnrealizedRemainingAmountCust@1086 : Decimaal;|UnrealizedRemainingAmountCust@1086 : Decimaal;|Ongewijzigd|  
|UnrealizedRemainingAmountVend@1074 : Decimaal;|UnrealizedRemainingAmountVend@1074 : Decimaal;|Ongewijzigd|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Ongewijzigd|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Ongewijzigd|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Ongewijzigd|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Ongewijzigd|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Ongewijzigd|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Ongewijzigd|  
|LastLineNo@1070 : Integer;||Verwijderd|  
|LastDate@1071 : Datum;|LastDate@1021 : Datum;|Ongewijzigd|  
|LastDocType@1072 : ' ,Betaling,Factuur,Creditnota,Rentefactuur,Aanmaning';|LastDocType@1025 : ' ,Betaling,Factuur,Creditnota,Rentefactuur,Aanmaning';|Ongewijzigd|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Ongewijzigd|  
|AddCurrGLEntryVATAmt@1075 : Decimaal;|AddCurrGLEntryVATAmt@1017 : Decimaal;|Ongewijzigd|  
|CurrencyDate@1076 : Datum;|CurrencyDate@1020 : Datum;|Ongewijzigd|  
|CurrencyFactor@1077 : Decimaal;|CurrencyFactor@1019 : Decimaal;|Ongewijzigd|  
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
||AmountRoundingPrecision@1012 : Decimaal;|Toegevoegd|  
||CrCardTransactionEntryNo@1013 : Integer;|Toegevoegd|  

## <a name="see-also"></a>Zie ook  
 [Designdetails: Wijzigingen in codeunit 12: Wijzigingen in procedures voor grootboekboekingen](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

