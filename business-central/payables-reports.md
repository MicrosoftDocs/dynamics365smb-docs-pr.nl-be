---
title: Crediteurenrapporten en analyses
description: Bekijk welke rapporten en analyses beschikbaar zijn in de standaardversie van Business Central, zodat u uw betalingsverplichtingen kunt volgen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 347
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: edb3b32f88198d8e21aa2bfddafc1b7f319be9de
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953396"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Crediteurenrapporten en -analyses in Business Central

Om u te helpen bij het beheren van uw betalingsverplichtingen in [!INCLUDE [prod_short](includes/prod_short.md)] zijn standaardrapporten en -analyses ingebouwd. Het gaat verder dan traditionele rapportagebeperkingen om u te helpen efficiënt verschillende soorten rapporten te ontwerpen.  

## <a name="reports"></a>Rapporten

De volgende tabel beschrijft enkele van de belangrijkste rapporten in betalingsverplichtingenrapportage.

| Rapport | Object-id | Omschrijving |
|--|--|--|
| **Vervallen betalingen** | 322|Toont achterstallige saldi voor leveranciers in achterstallige tijdsintervallen. De achterstallige bedragen kunnen naar behoefte worden weergegeven op vervaldatum, boekingsdatum of op documentdatum. U kunt ervoor kiezen om de bedragen in lokale valuta (LV) weer te geven en details van de achterstallige documenten af te drukken. De tijdsintervallen kunnen koppen hebben met datums of met een aantal achterstallige datums, relatief aan de gespecificeerde veroudering per type.<br>Dit rapport is het hoofdrapport voor het reconciliëren van het leveranciersgrootboek met het grootboek. Ervan uitgaande dat u directe boekingen niet hebt toegestaan op de rekeningen die worden gebruikt in de crediteurenrekening van de leveranciersboekingsgroepen, is dit rapport een specificatie van de bedragen die u in het grootboek vindt.|
| **Leverancier - Saldo t/m datum** | 321 | Toont het leverancierssaldo op de einddatum van het opgegeven datumbereik. U kunt ervoor kiezen om het leverancierssaldo in uw lokale valuta (LV) weer te geven. Selecteer het veld **Niet-toegepaste vermeldingen opnemen** om posten weer te geven die op de einddatum zijn gesloten, maar waarvan op een later tijdstip de vereffening ongedaan is gemaakt (geopend). Selecteer **Posten met nulsaldo weergeven** om leveranciers met een saldo van nul weer te geven op de einddatum van het datumfilter. Het datumfilter is van toepassing op de gedetailleerde leveranciersposten voor de posten in het rapport. Als u betalingen hebt die later zijn dan de einddatum die zijn toegepast op facturen binnen het datumbereik, zullen de facturen in het rapport verschijnen omdat ze niet zijn afgesloten op de einddatum. |
| **Leverancier - Proefbalans** | 329 | Toont de mutaties voor leveranciers voor de periode die is opgegeven in het datumfilter, evenals de mutatie van jaar tot heden voor het fiscale jaar dat overeenkomt met de geselecteerde periode. Het rapport is gegroepeerd op leveranciersboekingsgroepen en geeft een ander beeld van het leveranciersboek dan het rapport **Vervallen betalingen**. **Opmerking**: als u geen boekhoudperiode hebt ingesteld, weet het systeem niet welk fiscaal jaar moet worden gebruikt en toont het ofwel het jaar tot nu toe vanaf het meest recente gedefinieerde fiscale jaar of selecteert u gewoon de periode, die al dan niet vanaf het begin van een jaar loopt.|
| **Leverancier - Historie** | 304 | Toont alle leveranciersposten binnen het gespecificeerde datumfilter. Het rapport toont de beginsaldi van de leverancier ten opzichte van het datumfilter. |
| **Inkoopstatistiek** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Dit rapport kan ook worden gebruikt in crediteuren, omdat het gemakkelijker is om geboekte betalingen, kortingen en andere transacties voor een bepaalde leverancier snel op te zoeken.|
|**Leverancier - Open posten**|305| Verouderd rapport voor vervallen betalingen. We raden u aan om in plaats hiervan het rapport **Vervallen betalingen** te gebruiken. U kunt een periodelengte en een datum kiezen om te gebruiken als ingestelde *overschreden per*-datum.|
|**Wachtende betalingen**|319|Toont leveranciersboekingen waarbij het veld **Wachten** niet leeg is.|
|**Voorbetalingsdagboek leverancier**|317|Toont het betalingsdagboek met betalingskorting en tolerantie-informatie. Het rapport kan worden gebruikt om betalingen te controleren voordat betalingsbestanden worden gemaakt en het journaal wordt geboekt. **Opmerking**: het rapport toont betalingskortingen onjuist wanneer meerdere creditnota's in een aanvraag zijn gebruikt. In dit geval wordt de betalingskorting voor de extra creditnota's weergegeven als een niet-vereffend bedrag.|
|**Leveranciersoverzicht**|301|Bevat diverse basisgegevens voor leveranciers, zoals de boekingsgroep, kortingen en betalingen, prioriteitsniveau, de standaardvaluta van de leverancier en het huidige saldo (in LV) van de leverancier. U kunt de lijst bijvoorbeeld gebruiken om de gegevens in de tabel Leverancier te onderhouden.|

## <a name="see-also"></a>Zie ook

[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Werken met dimensies](finance-dimensions.md)  
[Vaste activa beheren](fa-manage.md)  
[Overzicht van lokale functionaliteit](about-localization.md)  
[Accountantervaringen binnen [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
