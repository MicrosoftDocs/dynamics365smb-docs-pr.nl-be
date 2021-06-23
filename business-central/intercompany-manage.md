---
title: Intercompany-transacties beheren
description: Met de intercompany-functionaliteit kunt u zakelijke processen en transacties tussen bedrijven binnen dezelfde organisatie vereenvoudigen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/02/2021
ms.author: edupont
ms.openlocfilehash: 0a69507b32f8782fe876458adb590529bfd64b20
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184436"
---
# <a name="managing-intercompany-transactions"></a>Intercompany-transacties beheren

Uw organisatie bestaat wellicht uit meerdere bedrijven, maar heeft mogelijk niet hetzelfde aantal boekhoud- en administratieteams. Met de intercompany-functionaliteit kunt u zaken doen met uw dochteronderneming en uw interne partnerorganisaties op dezelfde wijze als met uw externe leveranciers en klanten. U geeft de intercompany-transactiegegevens slechts eenmaal op in de relevante documenten. U kunt de functies gebruiken waarmee u al vertrouwd bent, zoals Klanten en Leveranciers. De toewijzingsmogelijkheden voor het rekeningschema en de dimensies helpen ervoor te zorgen dat de informatie op de juiste plaatsen wordt weergegeven.  

De intercompany-functionaliteit heeft vier voordelen:  

- Verhoogde productiviteit dankzij tijdsbesparing en vereenvoudigde transacties.  
- Geminimaliseerd foutpotentieel door eenmalige invoer van informatie en geautomatiseerde wijzigingen in het hele systeem.  
- Complete audittrail en volledige zichtbaarheid van zakelijke activiteiten en transactiegeschiedenissen.  
- Efficiënte en kosteneffectieve transacties met filialen en dochterondernemingen.  

U hebt de volledige controle over alle transactiedocumenten. U kunt bijvoorbeeld een document dat aan u is verzonden weigeren en zo incorrecte journaalboekingen tegenboeken en incorrecte ontvangsten/zendingen ongedaan maken. U kunt ook, wanneer u inkoopt bij een partner of dochteronderneming, de inkooporder wijzigen zo lang de verkopende onderneming nog geen goederen heeft verzonden.  

Wanneer u een transactie uitvoert, hoeft u geen rekeningen op te geven voor een aparte reeks boeken, maar geeft u eenvoudigweg de identificatie van het partnerbedrijf op. De intercompany-functionaliteit maakt grootboekregels aan, die leiden tot het sluitend maken van de boeken van beide bedrijven die bij de transactie zijn betrokken. In Klanten en Leveranciers wijst u een intercompany-partnercode toe aan een klant of leverancier. Vanaf dat moment wordt voor alle orders en facturen die voor de transacties van deze bedrijven zijn gegenereerd, overeenkomstige documenten in het partnerbedrijf geproduceerd, wat sluitende rekeningen tot gevolg heeft.  

Nadat u zakenpartners in het systeem hebt ingesteld als klanten en leveranciers, en intercompany-partnercodes aan hen hebt toegewezen, kunt u intercompany-inkoop- en verkoopdocumenten uitwisselen, zoals artikelen en artikeltoeslagen. [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt intercompany-transacties tussen meerdere databases, bijvoorbeeld in verschillende landen/regio's, maar ook in meerdere valuta's, verschillende rekeningschema's, verschillende dimensies en verschillende artikelnummering.  

> [!NOTE]
> Niet alle soorten gegevens kunnen op deze manier tussen bedrijven worden uitgewisseld. Inkoopfacturen worden niet via intercompany-processen bij zakenpartners ingediend. Verkoopfacturen die via intercompany-processen worden ingediend, worden echter als inkoopfacturen in het ontvangende bedrijf gemaakt.

Consolideren van financiële gegevens kan vooral relevant zijn voor IC-processen. Zie voor meer informatie [Financiële gegevens uit meerdere bedrijven consolideren](finance-consolidated-company-reporting.md).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

|Als u dit wilt doen: |Zie|
|---|---|
|Maak uw IC-leveranciers en -klanten als zogenaamde IC-partners en stel een IC-rekeningschema in.|[Intercompany instellen](intercompany-how-setup.md)|
|Gebruik IC-documenten of -dagboeken om transacties met uw IC-partners te boeken.|[Werken met intercompany-documenten en -dagboeken](intercompany-how-work-documents-journals.md)|
|Organiseer en verwerk inkomend en uitgaande transacties die u uitwisselt met uw IC-partners.|[De intercompany-inbox en outbox beheren](intercompany-how-manage-intercompany-inbox.md)|
|Gebruik intercompany-boekingen om kosten tussen partnerbedrijven te verdelen.|[Kosten toewijzen aan intercompany-partners](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]