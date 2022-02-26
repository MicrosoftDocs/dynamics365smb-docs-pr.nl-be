---
title: Bankrekeningen instellen (bevat video)
description: Ontdek hoe bankrekeningen worden gebruikt in Business Central en hoe u bedragen kunt reconciliëren met uw bank.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: 816b46e859fb4125c93346243f57f88b5f941a70
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029286"
---
# <a name="set-up-bank-accounts"></a>Bankrekeningen instellen

U gebruikt bankrekeningen in [!INCLUDE[prod_short](includes/prod_short.md)] om uw banktransacties bij te houden. Bedragen op rekeningen kunnen worden uitgedrukt in de lokale valuta of in een vreemde valuta. Nadat u bankrekeningen hebt ingesteld, kunt u ook de optie voor het afdrukken van cheques gebruiken. De bankrekeningen bevatten extra functionaliteit voor [betalingsreconciliatie](receivables-apply-payments-auto-reconcile-bank-accounts.md), [bankreconciliatie](bank-how-reconcile-bank-accounts-separately.md) en het importeren en exporteren van bankbestanden. De bankrekeningen kunnen ook worden opgenomen in transacties in de dagboeken. Elke bankrekening is gekoppeld aan een rekening in het rekeningschema via de toegewezen boekingsgroep voor bankrekeningen. Als u een bankrekening gebruikt bij een betalingstransactie, wordt er automatisch een boeking gemaakt op zowel de bankrekening als de gekoppelde grootboekrekening.  

Bankrekeningen werken anders, afhankelijk van of er een valutacode is opgegeven:

- Valutacode is leeg

  Alle transacties op de bankrekening zijn in de lokale valuta (LV) van het huidige bedrijf. Als er een transactie naar de rekening wordt gedaan in een andere valuta, worden de bedragen in LV op de rekening geboekt op basis van de relevante valutakoers. Alle cheques die vanaf deze rekening worden uitgegeven, moeten in LV worden uitgegeven. Als de bankrekening in een dagboek wordt gebruikt, neemt de dagboekregel automatisch de lege valutacode over.  
- Valutacode is opgegeven

  Alle transacties die naar deze rekening worden gedaan, moeten in dezelfde valuta zijn als op de rekening is aangegeven. Alle cheques die vanaf deze rekening worden uitgegeven, moeten ook deze valuta hebben.  

Een bankrekening is een geïntegreerd onderdeel van [!INCLUDE[prod_short](includes/prod_short.md)] en speelt een rol in vele andere mogelijkheden. De volgende afbeelding toont de belangrijkste relaties:

![Illustratie van bankrekeningrelaties.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Dit betekent dat het maken van een bankrekening deze beschikbaar maakt op alle hierboven getoonde plaatsen en wordt gespiegeld voor de relevante grootboekrekening en op de pagina **Bedrijfsgegevens**.

Een bankrekening wordt meestal dagelijks gecontroleerd om ervoor te zorgen dat eventuele nieuwe betalingen van klanten zo snel mogelijk worden geregistreerd. Dit helpt ervoor te zorgen dat de werkelijke status van de klanten wordt weerspiegeld in [!INCLUDE[prod_short](includes/prod_short.md)] zodat verkopers, accountants en andere medewerkers toegang hebben tot relevante en actuele informatie. Zo vermijden ze onnodige telefoontjes naar de klant over achterstallige facturen of vertragingen in verzendingen.  

![Illustratie van bankbetaling.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Een andere taak is het importeren van de leveranciersvalutabetalingen met de gerealiseerde valutakoersen om ervoor te zorgen dat de actuele status van de leveranciers up-to-date is. De eenvoudigste manier om ervoor te zorgen dat de bankrekening wordt bijgewerkt, is door middel van [betalingsreconciliatie](receivables-apply-payments-auto-reconcile-bank-accounts.md). In het **betalingsreconciliatiedagboek** kunt u rechtstreeks vanuit een online bankapplicatie banktransacties importeren en min of meer automatisch laten boeken. Het dagboek identificeert en publiceert automatisch het volgende:  

- Automatische incasso-betalingen van klanten  
- Klantbetalingen van enkele facturen  
- Lump-sumbetalingen van klanten.  
- Klantbetalingen in vreemde valuta's  
- Leveranciersbetalingen  
- Leveranciersbetalingen in vreemde valuta  
- Periodieke leveranciersbetalingen en abonnementen  
- Bankkosten en rente  

Betalingsreconciliatie levert een enorme tijdsbesparing op bij het boeken van inkomende en uitgaande betalingen. Echter, de transacties op de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] worden pas als 100% correct beschouwd als u een bankreconciliatie uitvoert.  

Bankreconciliatie is hoe u ervoor zorgt dat de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] overeenkomt met de externe rekening bij de bank.  

 ![Illustratie van bankrekeningreconciliatie.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

In de bovenstaande afbeelding vertegenwoordigt de linkerkant de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] en de rechterkant vertegenwoordigt de transacties die van de bank zijn geïmporteerd via de online banktoepassing. Het diagram in het midden toont de transacties van beide kanten, wat de bankreconciliatie is.

Van de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] moeten de meeste transacties bekend zijn bij de fysieke bank. De enige uitzonderingen zijn de volgende gevallen:  

- Correcties geboekt in [!INCLUDE[prod_short](includes/prod_short.md)]  
- Uitgegeven cheques die nog niet zijn geïnd  
- Leveranciersbetalingen die niet zijn goedgekeurd door de bank  

Van de fysieke rekening in de bank komen voortdurend onbekende transacties binnen die niet zijn geïdentificeerd in het betalingsreconciliatiedagboek, zoals:  

- Nieuwe leveranciersabonnementen  
- Klantbetalingen zonder beschrijving
- Bankrente
- Bankkosten
- Creditcardkosten die nog niet zijn gemeld

Hoe beter uw toewijzingsgegevens in het betalingsreconciliatiedagboek hoe meer transacties automatisch worden geboekt en hoe eenvoudiger de periodieke bankreconciliatie wordt.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Sommige velden kunnen gevoelige gegevens bevatten, zoals de velden **Bankfiliaalnr.**, **Bankrekeningnr.**, **SWIFT-code** en **IBAN-code**. Zie voor meer informatie [Vertrouwelijke velden bewaken](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Bankrekeningen instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Bankrekeningen** de actie **Nieuw**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Het veld **Boekingsgroep van bankrekening** verbindt de bankrekening bijvoorbeeld met de onderliggende grootboekrekening in de balans. Zie [Boekingsgroepen instellen](finance-posting-groups.md) voor meer informatie.

> [!TIP]
> Sommige velden zijn verborgen totdat u de actie **Meer tonen** kiest, meestal omdat ze zelden worden gebruikt. Andere moeten worden toegevoegd via personalisatie. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

U kunt zoveel bankrekeningen maken als u nodig hebt voor uw bedrijf. Voor elke bankrekening moet u informatie opgeven die de bankrekening uniek identificeerbaar maakt. Deze informatie omvat het geografische adres van de bank, nummerreeksen voor verschillende soorten transacties, zoals automatische afschrijvingen en overboekingen, de valuta waarin bedragen zijn gespecificeerd en informatie die wordt gebruikt voor het importeren van bankafschriften. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->
> [!NOTE]
> Als u wilt dat in het veld **Saldo** een beginsaldo wordt ingevuld, moet u een bankrekeningpost boeken met het bedrag in kwestie. U kunt dit doen door een bankrekeningreconciliatie uit te voeren. Zie [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie.  
>
> U kunt echter ook het beginsaldo toepassen als onderdeel van het proces voor het maken van algemene gegevens in nieuwe bedrijven. U kunt dit doen met behulp van de begeleide-instelling **Bedrijfsgegevens migreren**. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md).  

> [!IMPORTANT]
> Het is belangrijk dat u het beginsaldo niet rechtstreeks in het grootboek boekt. Als boekingen in de grootboekrekening rechtstreeks op de grootboekrekening worden geboekt, zal dit er doorgaans toe leiden dat u de bankrekening niet kunt afstemmen, of, in het geval van bankrekeningen in vreemde valuta, resulteren in verschillen die zich opstapelen terwijl u meer bankafstemmingen boekt. Vaak boekt u het beginsaldo direct op de bankrekening en komt het bedrag dan op de grootboekrekening terecht. U kunt het ook later terugboeken naar een aangewezen grootboekrekening die u hebt gebruikt om het openingsgrootboeksaldo te compenseren. In beide gevallen moet u eventuele directe boekingen op de grootboekrekening uitbetalen voordat u uw eerste bankafstemming start, en vooral als de bankrekening in een vreemde valuta is.  

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Uw bankrekening instellen om bankbestanden te importeren of te exporteren

Velden op het sneltabblad **Transfer** op de pagina **Bankrekeningkaart** zijn gerelateerd om bankfeeds en -bestanden te importeren en te exporteren. Zie voor meer informatie [De AMC Banking 365 Fundamentals-extensie](ui-extensions-amc-banking.md) gebruiken en [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een bankrekening waarvoor u bankbestanden exporteert of importeert.
3. Vul indien nodig de velden op het sneltabblad **Transfer** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andere services voor bestandsexport en de verschillende indelingen vereisen andere instellingswaarden op de pagina **Bankrekeningkaart**. U wordt over verkeerde of ontbrekende instellingswaarden geïnformeerd als u het bestand probeert te exporteren. Lees daarom de korte omschrijvingen van de velden zorgvuldig of raadpleeg de relateerde onderwerpen met procedures. Als u bijvoorbeeld een betalingsbestand voor een Noord-Amerikaanse elektronische betaling (EFT) exporteert, moeten daarvoor zowel het veld **Laatste afdrachtsadviesnr.** als **Transitnr.** zijn ingevuld. Zie voor meer informatie [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

De velden op het sneltabblad **Transit** in de bankrekening hebben verschillende doelen, afhankelijk van of de betaling inkomend of uitgaand is.

De afbeelding toont de route van inkomende betalingen:

:::row:::
    :::column:::
        1. De transacties worden geëxporteerd vanuit de bankrekening in een voor mensen leesbaar .csv-formaat of in het eigen formaat van de bank.
        <br><br>
2. De *definitie van gegevensuitwisseling* wijst de informatie in het bestand toe aan de velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Gegevensuitwisseling instellen](across-set-up-data-exchange.md)
<br><br>
3. De *instellingen voor gegevensexport/import* definiëren de export of import en koppelen naar de definitie van gegevensuitwisseling.
<br><br>
4. Het *importformaat bankafschriften* koppelt de importinstellingen aan de bankrekening.
<br><br>
5. De betalingen worden geïmporteerd via het **betalingsreconciliatiedagboek** of de pagina **Bankreconciliatie**.
    :::column-end:::
    :::column:::
        ![Illustratie van betalingen die van de bank zijn ontvangen op bankrekeningen.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Inkomende betalingen worden altijd geïmporteerd via het **betalingsreconciliatiedagboek** of rechtstreeks in de pagina **Bankreconciliatie**. Uitgaande betalingen kunnen daarentegen afkomstig zijn uit elk betalingsdagboek. De enige voorwaarde is dat het veld **Exporteren betaling toestaan** in de relevante betalingsdagboekbatch moet zijn geselecteerd.

De afbeelding toont de route van uitgaande betalingen:

:::row:::
    :::column:::
        6. De transacties die zijn ingevuld in een betalingsjournaal dat is voorbereid voor het exporteren van betalingen naar een bestand.
        <br><br>
        7. Het *importformaat bankafschriften* koppelt de importinstellingen aan de bankrekening
        <br><br>
        8. De *instellingen voor gegevensexport/import* definiëren de export of import en koppelen naar de definitie van gegevensuitwisseling.
        <br><br>
        9. De *definitie van gegevensuitwisseling* wijst de informatie in het bestand toe aan de velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Gegevensuitwisseling instellen](across-set-up-data-exchange.md)
        <br><br>
        10. De betalingen worden geëxporteerd vanuit het betalingsdagboek en geïmporteerd in de bankrekening
    :::column-end:::
    :::column:::
        ![Illustratie van betalingen vanuit bankrekeningen, die naar de bank zijn verzonden.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Bankrekeningen van leveranciers instellen voor de export van bankbestanden

Velden op het sneltabblad **Transfer** op de pagina **Bankrekeningkaart leverancier** zijn gerelateerd om bankfeeds en -bestanden te exporteren. Zie voor meer informatie [De AMC Banking 365 Fundamentals-extensie](ui-extensions-amc-banking.md) gebruiken en [Betalingen exporteren naar een bankbestand](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een leverancier naar wiens bankrekening u betalingsbankbestanden exporteert.
3. Kies de actie **Bankrekeningen**.
4. Kies vanuit de **lijst Bankrekeningen van leverancier** de relevante bankrekening of voeg een nieuwe bankrekening toe.  
5. Vul indien nodig de velden op de pagina **Bankrekeningkaart leverancier** op het sneltabblad **Transfer** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Sommige velden in de bankrekening van de leverancier kunnen gevoelige gegevens bevatten, zoals de velden **Bankfiliaalnr.**, **Bankrekeningnr.**, **SWIFT-code** en **IBAN-code**. Zie voor meer informatie [Vertrouwelijke velden bewaken](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Uw bankrekening wijzigen

Als u een andere bankrekening voor uw bedrijf wilt gebruiken, moet u de nieuwe bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] maken. We raden u aan om niet zomaar de informatie over de rekening die u momenteel gebruikt te vervangen, omdat dit kan leiden tot onjuiste gegevens. Uw beginsaldo kan bijvoorbeeld onjuist zijn of uw bankfeed werkt mogelijk niet meer correct. Het is belangrijk dat u de huidige en nieuwe rekeningen gescheiden houdt.

Nadat u de nieuwe bankrekening hebt gemaakt, moet u ook een nieuwe bankboekingsgroep maken en deze toewijzen aan een nieuwe grootboekrekening. U kunt een bestaande bankboekingsgroep opnieuw gebruiken en banktransacties worden geboekt naar dezelfde grootboekrekeningen als de andere bankrekeningen die de bankboekingsgroep delen. We raden u echter aan een nieuwe bankboekingsgroep en grootboekrekening te maken, zodat afstemmingen eenvoudiger kunnen worden uitgevoerd.

> [!NOTE]
> Houd er rekening mee dat de bankrekeninggegevens op openstaande verkoopfacturen nog steeds de originele bankrekening tonen. Dienovereenkomstig zullen betalingen waarschijnlijk nog steeds op die rekening worden geboekt. We raden u aan beide accounts na de wijziging gedurende een bepaalde periode actief te houden.

Om een beknopter beeld te krijgen van uw cashrekeningen in financiële rapportage, gebruikt u de rekeningen **Begintotaal** en **Eindtotaal** in uw rekeningschema, de rijen **Samentelling** in rekeningschema's of grootboekrekeningcategorieën. Voor meer informatie zie het gedeelte [Business Intelligence en Financial Reporting](bi.md).

## <a name="see-also"></a>Zie ook

[Bankieren instellen](bank-setup-banking.md)  
[Boekingsgroepen instellen](finance-posting-groups.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)  
[Automatische incasso via SEPA instellen in Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Uw bankrekening voor automatische incasso van SEPA instellen](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Een bankrekening instellen voor SEPA-kredietoverboekingen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-kredietoverdracht](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Betalingsreconciliatie](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Het grootboek en COA begrijpen](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
