---
title: Rapportselectie in Business Central
description: Leer hoe u de rapporten instelt die u gebruikt om verschillende soorten documenten af te drukken in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'setup, reporting'
ms.search.form: '306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917'
ms.date: 06/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Rapportselectie voor documenten in Business Central

U kunt standaardrapporten instellen om documenten af te drukken voor verkopen, aankopen en service, zoals orders, offertes en facturen. Als u bijvoorbeeld een specifieke lay-out voor verkoopfacturen heeft, kunt u dat rapport specificeren op de pagina **Rapportselecties - Verkoop**, zodat het wordt gebruikt om verkoopfacturen te verzenden of af te drukken.  

## Beschikbare rapportselecties

De **Rapportselecties**-pagina's specificeren welk rapport in verschillende situaties zal worden afgedrukt. [!INCLUDE [prod_short](includes/prod_short.md)] biedt standaardconfiguraties, maar u kunt deze indien nodig wijzigen. U kunt bijvoorbeeld ook lijsten aan de **Rapportselecties**-pagina's toevoegen als u meer dan één rapport per documentsoort wilt afdrukken. 

In de volgende tabel wordt beschreven waar u informatie over de verschillende pagina's kunt vinden.  

|Gebied of taak  |Meer informatie|
|--------------|----------|
|Voorbeeld van hoe rapportselectie werkt (verkoop)|[Rapportselectie voor verkoopdocumenten](#example-report-selection-for-sales-documents) vindt u hieronder|
|Standaardlay-out voor e-mails met verkoop- en inkoopdocumenten  |[Herbruikbare e-mailteksten en lay-outs instellen voor verkoop- en inkoopdocumenten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Cheque-indelingen definiëren     |[Een cheque-indeling selecteren](finance-how-define-check-layouts.md) |
|Rapporten definiëren voor btw-rapportage (Duitsland)|[Rapporten voor btw en Intrastat instellen](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Uw [!INCLUDE [prod_short](includes/prod_short.md)] kan extra **Rapportselectie**-pagina's bevatten, bijvoorbeeld afhankelijk van uw locatie en branche. Als u uw instellingen wilt controleren, kiest u het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Rapportselectie** in en kiest u vervolgens de relevante koppeling.

De standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)] omvat de volgende **Rapportselectie**-pagina's:

* **Rapportselectie - Verkoop**  
* **Rapportselectie - Inkoop**  
* **Rapportselectie - Voorraad**  
* **Rapportselectie - Cashflow**  
* **Rapportselectie - Magazijn**  
* **Rapportselectie - Bankrekening**  
* **Rapportselectie - Taak**  
* **Rapportselectie - service**

## Voorbeeld: Rapportselectie voor verkoopdocumenten

De pagina **Rapportselectie - verkoop** bevat standaardrapporten voor gebruik in verschillende scenario's voor elk gerelateerd documenttype. Kies een documenttype in het veld **Gebruik** en voeg vervolgens de rapportselectie toe of controleer deze. U kunt meer dan één rapport instellen en de volgorde opgeven waarin de rapporten moeten worden verzonden of afgedrukt.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

U kunt niet alle documenttypen als e-mailbijlagen verzenden. Voor de typen waarvoor het mogelijk is, bevat de pagina **Rapportselectie** extra velden.  

Op de pagina's **Rapportselectie - verkoop** en **Rapportselectie - aankoop** helpen de volgende velden u bijvoorbeeld bij het instellen van e-mail:

|Veldnaam |Omschrijving  |
|-----------|-------------|
|**Gebruiken voor hoofdtekst van e-mailbericht**| Voeg samengevatte informatie, zoals het factuurnummer, vervaldatum of een koppeling naar een betalingsservice in een e-mail in.        |
|**Gebruiken voor e-mailbijlage**| Voeg het gerelateerde document toe aan de e-mail.|
|**Indelingsomschrijving van hoofdtekst van e-mailbericht**|Geef de lay-out van de hoofdtekst van de e-mail op die u wilt gebruiken. Meestal is de lay-out een aangepaste rapportlay-out. |

## Zie ook

[Herbruikbare e-mailteksten en lay-outs instellen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Een cheque-indeling selecteren](finance-how-define-check-layouts.md)  
[Rapporten voor btw en Intrastat instellen (Duitsland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Indelingen van rapporten en documenten beheren](ui-manage-report-layouts.md)  
[Documentlay-outs definiëren voor klanten en leveranciers](ui-define-customer-vendor-document-layouts.md)  
[Printers instellen](ui-specify-printer-selection-reports.md)  
[Financiële rapporten en analyses in Business Central](finance-reports.md)  
[Debiteurenrapporten en -analyses in Business Central](receivables-reports.md)  
[Crediteurenrapporten en -analyses in Business Central](payables-reports.md)  
[VA-rapporten en analyses in Business Central](fa-reports.md)  
[Projectrapporten en analyses in Business Central](project-reports.md)  
[Verkooprapporten en analyses in Business Central](sales-reports.md)  
[Inkooprapporten en analyses in Business Central](purchase-reports.md)  
[Voorraad- en magazijnrapporten en analyses in Business Central](inventory-WMS-reports.md)  
[Assemblagerapporten en analyses in Business Central](assembly-reports.md)  
[Productierapporten en analyses in Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
