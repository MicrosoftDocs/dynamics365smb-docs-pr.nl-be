---
title: Veldtoewijzing bij het importeren van SEPA CAMT-bestanden | Microsoft Docs
description: In Europese markten kunt u bankafschriftbestanden in de regionale SEPA-norm (Single Euro Payments Area) importeren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/06/2023
ms.custom: bap-template
---
# <a name="field-mapping-when-importing-sepa-camt-files" />Veldtoewijzing bij het importeren van SEPA CAMT-bestanden

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt de regionale SEPA-norm (Single Euro Payments Area) voor het importeren van SEPA-bankafschriften (CAMT-indeling). Zie voor meer informatie [De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md).  

 De SEPA CAMT-standaard heeft zelf lokale variaties. U moet daarom mogelijk de algemene definitie voor gegevensuitwisseling, aangeduid door de code **SEPA CAMT** op de pagina **Definities van gegevensuitwisseling**, wijzigen om deze aan de lokale variant van de standaard aan te passen. De volgende tabellen tonen de element-aan-veld-toewijzing voor tabellen 81, 273 en 274 in de SEPA CAMT-implementatie in [!INCLUDE[prod_short](includes/prod_short.md)].  

 Voor informatie over het maken of het aanpassen van de definitie van gegevensuitwisseling raadpleegt u [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81" />CAMT-gegevenstoewijzing aan velden in de tabel Dagboek (81)

|Elementpad|Berichtelement|Gegevenssoort|Omschrijving|Identificatie voor een negatief teken|Veldnr.|Veldnaam|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Bedrag|Decimaal|Het geldbedrag in de kaspost||13|Bedrag|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Tekst|Geeft aan of de post een credit- of een debetpost is|DBIT|13|Bedrag|  
|Stmt/Ntry/BookgDt/Dt|Datum|Datum|De datum waarop een post wordt geboekt naar een rekening in de boeken van de rekeningservice||5|Boekingsdatum|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|De datum en tijd waarop een post wordt geboekt naar een rekening in de boeken van de rekeningservice||5|Boekingsdatum|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Naam|Tekst|De naam van de partij die een geldbedrag is verschuldigd aan de (uiteindelijke) incassant||1221|Informatie over betaler|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ongestructureerd|Tekst|Informatie die wordt verschaft om de afstemming/reconciliatie mogelijk te maken van een post met de artikelen die de betaling wordt geacht te vereffenen, zoals commerciële facturen in een vorderingsysteem, in een ongestructureerde vorm||8|Omschrijving|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Tekst|Extra informatie over de invoer||1222|Transactie-informatie|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273" />CAMT-gegevenstoewijzing aan velden in de tabel Bankreconciliatie (273)

|Elementpad|Berichtelement|Gegevenssoort|Omschrijving|Identificatie voor een negatief teken|Veldnr.|Veldnaam|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Datum|De datum en tijd waarop het bericht is gemaakt.||3|Afschriftdatum|  
|Stmt/Bal/Amt|Bedrag|Decimaal|Het bedrag dat resulteert uit de tot een nettowaarde teruggebrachte bedragen voor alle debet- en creditposten||4|Eindsaldo afschrift|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274" />CAMT-gegevenstoewijzing aan velden in de tabel Bankreconciliatieregel (274)

|Elementpad|Berichtelement|Gegevenssoort|Omschrijving|Identificatie voor een negatief teken|Veldnr.|Veldnaam|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Bedrag|Decimaal|Het geldbedrag in de kaspost||7|Afschrifttotaal|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Tekst|Geeft aan of de post een credit- of een debetpost is|DBIT|7|Afschrifttotaal|  
|Stmt/Ntry/BookgDt/Dt|Datum|Datum|De datum waarop een post wordt geboekt naar een rekening in de boeken van de rekeningservice||5|Transactiedatum|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|De datum en tijd waarop een post wordt geboekt naar een rekening in de boeken van de rekeningservice||5|Transactiedatum|  
|Stmt/Ntry/ValDt/Dt|Datum|Datum|De datum waarop activa beschikbaar worden voor de rekeninghouder in het geval van een creditpost, of niet meer beschikbaar zijn voor de rekeninghouder in het geval van een debetpost||12|Waardedatum|  
|Stmt/Ntry/ValDt/DtTm|DateTime|DateTime|De datum en tijd waarop activa beschikbaar worden voor de rekeninghouder in het geval van een creditpost, of niet meer beschikbaar zijn voor de rekeninghouder in het geval van een debetpost||12|Waardedatum|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Naam|Tekst|De naam van de partij die een geldbedrag is verschuldigd aan de (uiteindelijke) incassant||15|Informatie over betaler|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ongestructureerd|Tekst|Informatie die wordt verschaft om de afstemming/reconciliatie mogelijk te maken van een post met de artikelen die de betaling wordt geacht te vereffenen, zoals commerciële facturen in een vorderingsysteem, in een ongestructureerde vorm||6|Omschrijving|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Tekst|Extra informatie over de invoer||16|Transactie-informatie|  

 Elementen in het knooppunt **Ntry** die worden geïmporteerd in [!INCLUDE[prod_short](includes/prod_short.md)] maar niet aan velden worden toegewezen, worden opgeslagen in de tabel **Kolomdef. boekingsuitwisseling**. Gebruikers kunnen deze elementen vanuit de pagina's **Betalingsreconciliatiedagboek**, **Betalingsvereffening** en **Bankreconciliatie** weergeven door de actie **Details bankrekeningafschriftregel** te kiezen. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]
> Bij het importeren van CAMT-bankafschriften, verwacht [!INCLUDE[prod_short](includes/prod_short.md)] dat elke transactie uniek is, wat betekent dat het veld **Transactie-id** dat afkomstig is van de tag *Stmt/Ntry/NtryDtls/TxDtls/Refs/EndToEndId* in het CAMT-bestand, uniek moet zijn binnen de openstaande bankrekeningreconciliatie. Als de informatie niet aanwezig is, negeert [!INCLUDE[prod_short](includes/prod_short.md)] de betaling. Als een eerdere bankafstemming op dezelfde bankrekening is geboekt met dezelfde transactie-id als bij de huidige import, wordt de huidige transactie niet automatisch gereconcilieerd, maar kan deze nog steeds worden geïmporteerd.

## <a name="see-also" />Zie ook

[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[De AMC Banking 365 Fundamentals-extensie gebruiken](ui-extensions-amc-banking.md)  
[XML-schema's gebruiken om definities voor gegevensuitwisseling voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
