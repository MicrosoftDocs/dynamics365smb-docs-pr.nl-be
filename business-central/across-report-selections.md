---
title: Rapportselectie in Business Central
description: Leer hoe u de rapporten instelt die u gebruikt om verschillende soorten documenten af te drukken in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: d30baa44894658c03c3deffdf24a7923293b88fd
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024649"
---
# <a name="report-selection-in-business-central"></a>Rapportselectie in Business Central

U kunt standaardrapporten instellen die worden gebruikt om de verschillende documenten af te drukken voor inkopen en verkopen, zoals orders, offertes, facturen en creditnota's. Als u bijvoorbeeld een specifieke lay-out voor verkoopfacturen heeft, kunt u dat rapport specificeren op de pagina **Rapportselecties - Verkoop**, zodat het wordt gebruikt om verkoopfacturen te verzenden of af te drukken.  

De **Rapportselecties**-pagina's specificeren welk rapport in verschillende situaties zal worden afgedrukt. [!INCLUDE [prod_short](includes/prod_short.md)] bevat standaardconfiguraties, maar u kunt deze standaardinstellingen natuurlijk wijzigen. U kunt bijvoorbeeld ook lijsten aan de **Rapportselecties**-pagina's toevoegen als u meer dan één rapport per documentsoort wilt afdrukken.  

## <a name="available-report-selections"></a>Beschikbare rapportselecties

[!INCLUDE [prod_short](includes/prod_short.md)] bevat verschillende **Rapportselectie**-pagina's voor verschillende gebieden. In de volgende tabellen wordt beschreven waar u informatie over de verschillende pagina's kunt vinden.  

|Gebied of taak  |Meer informatie|
|--------------|----------|
|Voorbeeld van hoe rapportselectie werkt (verkoop)|[Rapportselectie voor verkoopdocumenten](#example-report-selection-for-sales-documents)|
|Standaardlay-out voor e-mails met verkoop- en inkoopdocumenten  |[Herbruikbare e-mailteksten en lay-outs instellen voor verkoop- en inkoopdocumenten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Cheque-indelingen definiëren     |[Een cheque-indeling selecteren](finance-how-define-check-layouts.md) |
|Rapporten definiëren voor btw-rapportage (Duitsland)|[Rapporten voor btw en Intrastat instellen](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Uw [!INCLUDE [prod_short](includes/prod_short.md)] kan extra **Rapportselectie**-pagina's bevatten, bijvoorbeeld afhankelijk van uw locatie en branche. U kunt uw instellingen altijd controleren door het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") te kiezen, **Rapportselecties** in te voeren en vervolgens de relevante koppeling te kiezen.

De standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)] omvat het volgende **Rapportselectie**-pagina's:

* **Rapportselectie - Verkoop**  
* **Rapportselectie - Inkoop**  
* **Rapportselectie - Voorraad**  
* **Rapportselectie - Cashflow**  
* **Rapportselectie - Magazijn**  
* **Rapportselectie - Bankrekening**  
* **Rapportselecties - Aanmaning/rentefactuur**  

## <a name="example-report-selection-for-sales-documents"></a>Voorbeeld: Rapportselectie voor verkoopdocumenten

De pagina **Rapportselectie - Verkoop** definieert de standaardrapporten die in verschillende scenario's voor elk gerelateerd documenttype moeten worden gebruikt. Kies een documenttype in het veld **Gebruik** en voeg vervolgens de rapportselectie toe of controleer deze. U kunt meer dan één rapport instellen en de volgorde bepalen waarin de rapporten moeten worden verzonden of afgedrukt.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Sommige typen documenten kunnen als e-mailbijlagen worden verzonden en andere niet. Elke **Rapportselectie**-pagina toont extra velden als het type e-mail standaard ondersteunt.  

Op de pagina's **Rapportselectie - Verkoop** en **Rapportselectie - Aankoop** helpen de volgende velden u bijvoorbeeld bij het instellen van e-mail:

|Veldnaam |Omschrijving  |
|-----------|-------------|
|**Gebruiken voor hoofdtekst van e-mailbericht**| Hiermee wordt opgegeven dat overzichtsgegevens, zoals het factuurnummer, de vervaldatum en de koppeling naar de betalingsservice, worden ingevoegd in de hoofdtekst van de e-mail die u verzendt.        |
|**Gebruiken voor e-mailbijlage**| Hiermee wordt opgegeven dat het gerelateerde document aan de e-mail wordt gekoppeld.|
|**Indelingsomschrijving van hoofdtekst van e-mailbericht**|Specificeert de lay-out van de hoofdtekst van de e-mail die wordt gebruikt, meestal een aangepaste rapportlay-out. |

## <a name="see-also"></a>Zie ook

[Herbruikbare e-mailteksten en lay-outs instellen voor verkoop- en inkoopdocumenten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Een cheque-indeling selecteren](finance-how-define-check-layouts.md)  
[Rapporten voor btw en Intrastat instellen (Duitsland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Indelingen van rapporten en documenten beheren](ui-manage-report-layouts.md)  
[Documentlay-outs definiëren voor klanten en leveranciers](ui-define-customer-vendor-document-layouts.md)  
[Printers instellen](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]