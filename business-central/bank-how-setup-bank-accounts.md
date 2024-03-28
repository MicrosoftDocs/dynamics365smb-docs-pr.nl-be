---
title: Bankrekeningen instellen (bevat video)
description: Ontdek hoe bankrekeningen worden gebruikt in Business Central en hoe u bedragen kunt reconciliëren met uw bank.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 08/03/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Bankrekeningen instellen

U gebruikt bankrekeningen in [!INCLUDE[prod_short](includes/prod_short.md)] om uw banktransacties bij te houden. Bedragen op rekeningen kunnen worden uitgedrukt in de lokale valuta of in een vreemde valuta. Nadat u bankrekeningen hebt ingesteld, kunt u ook de optie voor het afdrukken van cheques gebruiken. De bankrekeningen bevatten extra functionaliteit voor [betalingsreconciliatie](receivables-apply-payments-auto-reconcile-bank-accounts.md), [bankreconciliatie](bank-how-reconcile-bank-accounts-separately.md) en het importeren en exporteren van bankbestanden. De bankrekeningen kunnen ook worden opgenomen in transacties in de dagboeken. Elke bankrekening is gekoppeld aan een rekening in het rekeningschema via de toegewezen boekingsgroep voor bankrekeningen. Als u een bankrekening gebruikt bij een betalingstransactie, wordt er automatisch een post gemaakt op zowel de bankrekening als de gekoppelde grootboekrekening.  

Bankrekeningen werken anders, afhankelijk van of er een valutacode is opgegeven:

- Als de valutacode leeg is

  Alle transacties op de bankrekening zijn in de lokale valuta (LV) van het huidige bedrijf. Als er een transactie naar de rekening wordt gedaan in een andere valuta, worden de bedragen in LV op de rekening geboekt op basis van de relevante valutakoers. Alle cheques die vanaf deze rekening worden uitgegeven, moeten in LV worden uitgegeven. Als de bankrekening in een dagboek wordt gebruikt, neemt de dagboekregel automatisch de lege valutacode over.  
  
- Valutacode is opgegeven

  Alle transacties die naar deze rekening worden gedaan en cheques die vanaf deze rekening worden uitgegeven, moeten in dezelfde valuta zijn als op de rekening is aangegeven.

U kunt tijd besparen bij het invoeren van gegevens door een bankrekening als standaardrekening te gebruiken voor de valuta die voor de rekening is opgegeven. Als u dat doet, wordt de rekening toegewezen aan verkoop- en servicedocumenten die de valuta gebruiken. Als u de rekening als standaard voor verkoop- en servicedocumenten wilt gebruiken, zet u op de pagina **Bankrekeningkaart** de schakelaar **Als standaard voor valuta gebruiken** aan. Indien nodig kunt u een andere rekening kiezen wanneer u aan een document werkt.

Een bankrekening is een integraal onderdeel van [!INCLUDE[prod_short](includes/prod_short.md)] en speelt een rol in vele andere mogelijkheden. De volgende afbeelding toont de belangrijkste relaties:

![Illustratie van bankrekeningrelaties.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

U ziet dat het maken van een bankrekening deze beschikbaar maakt op alle hierboven getoonde plaatsen en wordt gespiegeld voor de relevante grootboekrekening en op de pagina **Bedrijfsgegevens**.

Een bankrekening wordt meestal dagelijks gecontroleerd om ervoor te zorgen dat eventuele nieuwe betalingen van klanten zo snel mogelijk worden geregistreerd. Dit helpt ervoor te zorgen dat de werkelijke status van een klant wordt weerspiegeld in [!INCLUDE[prod_short](includes/prod_short.md)]. Dat geeft verkopers, accountants en andere medewerkers toegang tot de meest relevante en actuele informatie, zodat ze niet onnodig naar de klant hoeven te bellen over achterstallige facturen of vertragingen in zendingen.  

![Illustratie van bankbetaling.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Een andere taak is het importeren van de leveranciersvalutabetalingen met de gerealiseerde valutakoersen om ervoor te zorgen dat de actuele status van de leveranciers up-to-date is. Het gebruik van de mogelijkheid van [betalingsreconciliatie](receivables-apply-payments-auto-reconcile-bank-accounts.md) is de gemakkelijkste manier om dat te doen. In het **betalingsreconciliatiedagboek** kunt u rechtstreeks vanuit een online bankapplicatie banktransacties importeren en min of meer automatisch laten boeken. Het dagboek identificeert en publiceert automatisch het volgende:  

- Automatische incasso-betalingen van klanten  
- Klantbetalingen van enkele facturen  
- Lump-sumbetalingen van klanten.  
- Klantbetalingen in vreemde valuta's  
- Leveranciersbetalingen  
- Leveranciersbetalingen in vreemde valuta  
- Periodieke leveranciersbetalingen en abonnementen  
- Bankkosten en rente  

Betalingsreconciliatie levert aanzienlijke tijdsbesparingen op bij het boeken van inkomende en uitgaande betalingen. De transacties op de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] worden echter pas als 100% correct beschouwd als u een bankreconciliatie uitvoert.  

Bankreconciliatie is hoe u ervoor zorgt dat de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] overeenkomt met de externe rekening bij de bank.  

 ![Illustratie van bankrekeningreconciliatie.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

In de bovenstaande afbeelding vertegenwoordigt de uiterste linkse zijde de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] en de uiterst rechtse zijde de transacties die van de bank zijn geïmporteerd via de online banktoepassing. Het diagram in het midden toont de transacties van beide kanten, wat de bankreconciliatie is.

Van de bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] moeten de meeste transacties bekend zijn bij de fysieke bank. De enkele uitzonderingen zijn de volgende gevallen:  

- Correcties geboekt in [!INCLUDE[prod_short](includes/prod_short.md)]  
- Uitgegeven cheques die nog niet zijn geïnd 
- Leveranciersbetalingen die nog niet zijn goedgekeurd door de bank  

Van de fysieke rekening bij de bank komen voortdurend onbekende transacties binnen die niet zijn geïdentificeerd in het betalingsreconciliatiedagboek, zoals:  

- Nieuwe leveranciersabonnementen  
- Klantbetalingen zonder beschrijving
- Bankrente
- Bankkosten
- Creditcardkosten die nog niet zijn gerapporteerd

Hoe beter u gegevens toewijst in het betalingsreconciliatiedagboek, hoe meer transacties automatisch worden geboekt en hoe eenvoudiger de periodieke bankreconciliatie wordt.

Bekijk in de video hieronder de basisstappen om een bankrekening in te stellen in [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Sommige velden kunnen gevoelige gegevens bevatten, zoals de velden **Bankfiliaalnr.**, **Bankrekeningnr.**, **SWIFT-code** en **IBAN-code**. Zie voor meer informatie [Vertrouwelijke velden bewaken](across-log-changes.md#monitor-sensitive-fields).

## Bankrekeningen instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Bankrekeningen** de actie **Nieuw**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Een voorbeeld is het veld **Boekingsgroep van bankrekening** dat de bankrekening verbindt met de onderliggende grootboekrekening in de balans. Zie voor meer informatie [Boekingsgroepen instellen](finance-posting-groups.md).

> [!TIP]
> Sommige velden zijn verborgen totdat u de actie **Meer tonen** kiest, meestal omdat ze zelden worden gebruikt. Andere moeten worden toegevoegd via personalisatie. Zie voor meer informatie [Uw werkruimte personaliseren](ui-personalization-user.md).

U kunt zoveel bankrekeningen maken als u nodig hebt voor uw bedrijf. Voor elke bankrekening moet u informatie opgeven die de bankrekening uniek identificeerbaar maakt. Deze informatie omvat het geografische adres van de bank, nummerreeksen voor verschillende soorten transacties, zoals automatische afschrijvingen en overboekingen, de valuta waarin bedragen zijn opgegeven en informatie die wordt gebruikt voor het importeren van bankafschriften. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## Een beginsaldo invoeren

Als u wilt dat in het veld **Saldo** een beginsaldo wordt ingevuld, moet u een bankrekeningpost boeken met het bedrag in kwestie. U kunt dit doen door een bankrekeningreconciliatie uit te voeren. Zie voor meer informatie [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md).  
>
> U kunt echter ook het beginsaldo toepassen als onderdeel van het proces voor het maken van algemene gegevens in nieuwe bedrijven. U kunt dit doen met behulp van de begeleide instelling **Bedrijfsgegevens migreren**. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  

> [!IMPORTANT]
> U moet het beginsaldo niet rechtstreeks naar het grootboek boeken. Als u posten in de grootboekrekening hebt die er rechtstreeks naar zijn geboekt, leidt dit er doorgaans toe dat u de bankrekening niet kunt afstemmen. Bij bankrekeningen in vreemde valuta resulteert een dergelijke praktijk in toenemende verschillen naarmate u meer bankreconciliaties boekt. Gewoonlijk boekt u het beginsaldo direct op de bankrekening en komt het bedrag op de grootboekrekening terecht. U kunt het ook later terugboeken naar de grootboekrekening die u gebruikt om het beginsaldo van het grootboek te salderen. In beide gevallen moet u eventuele directe boekingen op de grootboekrekening salderen voordat u uw eerste bankreconciliatie start&mdash;vooral als de bankrekening in een vreemde valuta is.

## Uw bankrekening instellen om bankbestanden te importeren of te exporteren

De velden met betrekking tot de import en export van bankfeeds en -bestanden bevinden zich op het sneltabblad **Transfer** op de pagina **Bankrekeningkaart**. Zie voor meer informatie [De AMC Banking 365 Fundamentals-extensie gebruiken](ui-extensions-amc-banking.md) en [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor de bankrekening waarvoor u bankbestanden exporteert of importeert.
3. Vul indien nodig de velden op het sneltabblad **Transfer** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andere services voor bestandsexport en de verschillende indelingen vereisen andere instellingswaarden op de pagina **Bankrekeningkaart**. U wordt over verkeerde of ontbrekende instellingswaarden geïnformeerd als u het bestand exporteert. Lees de korte beschrijvingen van de velden zorgvuldig of raadpleeg de relateerde onderwerpen met procedures. Als u bijvoorbeeld een betalingsbestand voor een Noord-Amerikaanse elektronische betaling (EFT) exporteert, moeten daarvoor zowel het veld **Laatste afdrachtsadviesnr.** als het veld **Transitnr.** zijn ingevuld. Zie voor meer informatie [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

De velden op het sneltabblad **Transit** in de bankrekening hebben verschillende doelen, afhankelijk van of de betaling inkomend of uitgaand is.

De onderstaande afbeelding toont de route van inkomende betalingen (nummers in de omschrijving komen overeen met die in afbeelding):

:::row:::
    :::column:::

1. De transacties worden geëxporteerd vanuit de bankrekening in een voor mensen leesbaar .csv-formaat of in het eigen formaat van de bank.
2. De *definitie van gegevensuitwisseling* wijst de informatie in het bestand toe aan de velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Gegevensuitwisseling instellen](across-set-up-data-exchange.md)
3. Met de *instellingen voor gegevensexport/-import* worden de export of import gedefinieerd en wordt een koppeling gemaakt met de gegevensuitwisselingsdefinitie.
4. Het *importformaat bankafschriften* koppelt de importinstellingen aan de bankrekening.
5. De betalingen worden geïmporteerd via het **betalingsreconciliatiedagboek** of de pagina **Bankreconciliatie**.

  :::column-end:::
  :::column:::

        ![Illustratie van betalingen die van de bank zijn ontvangen op bankrekeningen.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Inkomende betalingen worden altijd geïmporteerd via het **Betalingsreconciliatiedagboek** of rechtstreeks naar de pagina **Bankreconciliatie**. Uitgaande betalingen kunnen daarentegen afkomstig zijn uit elk betalingsdagboek. De enige voorwaarde is dat het veld **Exporteren betaling toestaan** in de relevante betalingsdagboekbatch moet zijn geselecteerd.

De onderstaande afbeelding toont de route van uitgaande betalingen (nummers in de omschrijving komen overeen met die in afbeelding):

:::row:::
    :::column:::

6. De transacties die zijn ingevuld in een betalingsjournaal dat is voorbereid voor het exporteren van betalingen naar een bestand.
7. Met de *indeling voor import van bankafschriften* worden de importinstellingen aan de bankrekening gekoppeld.
8. Met de *instellingen voor gegevensexport/-import* worden de export of import gedefinieerd en wordt een koppeling gemaakt met de gegevensuitwisselingsdefinitie.
9. Met de *definitie van gegevensuitwisseling* wordt de informatie in het bestand toegewezen aan de velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Gegevensuitwisseling instellen](across-set-up-data-exchange.md)
10. De betalingen worden geëxporteerd vanuit het betalingsdagboek en geïmporteerd naar de bankrekening.

  :::column-end:::
  :::column:::

        ![Illustratie van betalingen vanuit bankrekeningen, die naar de bank zijn verzonden.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## Bankrekeningen van leveranciers instellen voor de export van bankbestanden

Velden op het sneltabblad **Transfer** op de pagina **Bankrekeningkaart leverancier** zijn gerelateerd aan de export van bankfeeds en -bestanden. Zie voor meer informatie [De AMC Banking 365 Fundamentals-extensie gebruiken](ui-extensions-amc-banking.md) en [Betalingen exporteren naar een bankbestand](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## Uw bankrekening wijzigen

Als u een andere bankrekening voor uw bedrijf wilt gebruiken, moet u de nieuwe bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] maken. We raden u aan om niet zomaar de informatie over de rekening die u momenteel gebruikt te vervangen, omdat dit kan leiden tot onjuiste gegevens. Uw beginsaldo kan bijvoorbeeld onjuist zijn of uw bankfeed werkt mogelijk niet meer correct. Het is belangrijk dat u de huidige en nieuwe rekeningen gescheiden houdt.

Nadat u de nieuwe bankrekening hebt gemaakt, moet u ook een nieuwe bankboekingsgroep maken en deze toewijzen aan een nieuwe grootboekrekening. U kunt een bestaande bankboekingsgroep opnieuw gebruiken en banktransacties worden geboekt naar dezelfde grootboekrekeningen als andere bankrekeningen die de bankboekingsgroep delen. We raden u echter aan een nieuwe bankboekingsgroep en grootboekrekening te maken, zodat afstemmingen eenvoudiger kunnen worden uitgevoerd.

> [!NOTE]
> Houd er rekening mee dat de bankrekeninggegevens op openstaande verkoopfacturen nog steeds de originele bankrekening tonen. Dienovereenkomstig zullen betalingen waarschijnlijk nog steeds op die rekening worden geboekt. We raden u aan beide accounts na de wijziging gedurende een bepaalde periode actief te houden.

Om een beknopter beeld te krijgen van uw kasrekeningen in financiële rapportage, gebruikt u de rekeningen **Begintotaal** en **Eindtotaal** in uw rekeningschema, de rijen **Samentelling** in financiële rapporten of grootboekrekeningcategorieën. Zie voor meer informatie het gedeelte [Business Intelligence en financiële rapportage](bi.md).

## Zie ook

[Bankieren instellen](bank-setup-banking.md)  
[Boekingsgroepen instellen](finance-posting-groups.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)  
[Automatische incasso via SEPA instellen in Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Uw bankrekening voor automatische incasso van SEPA instellen](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Een bankrekening instellen voor SEPA-kredietoverboekingen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-krediettransfer](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Betalingsreconciliatie](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Het grootboek en COA begrijpen](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
