---
title: De lay-out opgeven van een cheque
description: 'U kunt uw cheques ontwerpen en afdrukken in verschillende indelingen, om te voldoen aan standaards van uw lokale autoriteiten.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'print check, customize'
ms.search.form: '374, 404'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="select-a-check-layout" />Een cheque-indeling selecteren

U kunt uw eigen cheques ontwerpen in overeenstemming met de standaards die zijn ingesteld door de plaatselijke autoriteiten. Chequeafbeeldingen kunnen worden afgedrukt in het Engels, Frans of Spaans.

Cheques worden ontworpen om te worden afgedrukt in zowel Amerikaanse als Canadese chequeafbeeldingsindelingen, in een cheque-strook-cheque indeling of een strook-strook-cheque indeling.

## <a name="to-select-a-check-layout" />Een cheque-indeling selecteren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekening van rapportselecties** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Rapportselectie - Bank** in het veld **Gebruik** de optie **Cheque**.
3. Selecteer een van de volgende rapport-id's.

| Rapport-id | Rapportnaam | Omschrijving |
| --- | --- | --- |
| 1401 |Cheque |Dit is het standaardrapport. |
| 10411 |Cheque (strook/strook/cheque) |Dit rapport is ontworpen om cheques af te drukken in de indeling strook/strook/cheque. |
| 10412 |Cheque (strook/cheque/strook) |Dit rapport is ontworpen om cheques af te drukken in de indeling strook/cheque/strook. |
| 10413 |Drie cheques per pagina |Dit rapport is ontworpen voor het afdrukken van drie cheques op elke pagina. |

Wanneer u de cheque-indelingen hebt ingesteld, kunt u cheques afdrukken vanuit de pagina **Betalingsdagboek**. Zie voor meer informatie [Werken met cheques](payables-how-work-checks.md).

Als u een van deze standaardcontrole-indelingen wilt wijzigen, gebruikt u de integratie van Word of RDLC om dit te doen. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

## <a name="use-micr-and-security-fonts" />MICR en beveiligingslettertypen gebruiken
De online versie van [!INCLUDE[prod_short](includes/prod_short.md)] bevat vooraf geïnstalleerde lettertypen op de servers die kunnen worden gebruikt bij het definiëren van cheque-indelingen. Het volgende geeft aan welke lettertypen beschikbaar zijn en bevat koppelingen naar gedetailleerde informatie van de externe leveranciers van de lettertypen.

> [!Important]
> MICR- en chequebeveiligingslettertypen in Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] zijn gelicentieerd in een lettertypepakket van IDAutomation.com, Inc. Deze producten mogen alleen worden gebruikt als onderdeel van en in verband met Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].

In update 15.3 en nieuwer zijn MICR-lettertypen (Magnetic Ink Character Recognition) geïnstalleerd en beschikbaar voor gebruik. Zowel E-13B als de CMC-7-standaarden worden ondersteund. Naast MICR-lettertypen zijn er speciale beveiligingslettertypen beschikbaar voor het genereren van tekst, namen, bedragen en de valutasymbolen dollar, euro, pond en yen, die moeilijk te manipuleren zijn nadat een cheque is afgedrukt.

> [!NOTE]
> Om veiligheids- en juridische redenen kunt u geen aangepaste lettertypen uploaden naar de [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving.

### <a name="micr-e-13b-specifications" />MICR E-13B-specificaties

Hieronder volgt een samenvatting van de specificaties voor de MICR E-13B-lettertypen die nuttig kunnen zijn bij het kalibreren van lettertypen voor cheque-indelingen met specifieke MICR-printers.

![MICR E-13B-specificaties.](media/font_MICR_E-13B_Specifications.png "MICR E-13B-specificaties")

### <a name="delimiter-characters" />Scheidingstekens

![Scheidingstekens.](media/font-micr-letters.png "Scheidingstekens")

De volledige specificatie van MICR E-13B-lettertypen vindt u in de documentatie van de leverancier: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications" />MICR CMC-7-specificaties

De volgende CMC-7-lettertypen zijn beschikbaar in [!INCLUDE[prod_short](includes/prod_short.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
- IDAutomationCMC7n40

Hieronder volgt een samenvatting van de specificaties voor de MICR CMC-7-lettertypen die nuttig kunnen zijn bij het kalibreren van lettertypen voor cheque-indelingen met specifieke MICR-printers.

![MICR CMC-7-specificaties.](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7-specificaties")

### <a name="delimiter-characters-1" />Scheidingstekens

![Scheidingstekens voor CMC-7.](media/font-cmc7-letters.png "Scheidingstekens voor CMC-7")

De volledige specificatie van MICR CMC-7-lettertypen vindt u in de documentatie van de leverancier: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications" />Specificaties voor veilige lettertypen

Hieronder volgt een samenvatting van de specificaties voor de chequebeveiligingslettertypen die nuttig kunnen zijn bij het kalibreren van lettertypen voor cheque-indelingen met specifieke MICR-printers.

![Specificaties van chequebeveiligingslettertypen.](media/font_check-security-font_Specifications.png "Specificaties van chequebeveiligingslettertypen")

De volledige specificatie van chequebeveiligingslettertypen vindt u hier in de documentatie van de leverancier: (https://www.idautomation.com/security-fonts/).

Lettertypen voor andere doeleinden zijn ook beschikbaar in [!INCLUDE[prod_short](includes/prod_short.md)]. Voor meer informatie zie [Beschikbare lettertypen](ui-fonts.md)

## <a name="see-also" />Zie ook

[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Lettertypen in Business Central](ui-fonts.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)   
[Periodeafsluitingsprocessen voltooien](year-how-complete-period-end-processes.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
