---
title: Documenten zonder bijlagen zoeken| Microsoft Docs
Description: U kunt grootboekposten zoeken voor geboekte inkoop- en verkoopdocumenten die geen elektronische inkomende documenten hebben, zoals geïmporteerde facturen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e15284452bb80acc329e46df7361ee9dea556996
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754979"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Geboekte documenten zonder inkomende documentrecords zoeken
Vanuit de pagina's **Rekeningschema** en **Grootboekposten** kunt u zoeken naar grootboekposten voor geboekte inkoop- en verkoopdocumenten die geen inkomende documentrecords hebben, en deze centraal koppelen aan bestaande records of nieuwe records maken met gekoppelde documentbestanden.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Geboekte documenten zonder inkomende documentrecords zoeken
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de desbetreffende koppeling.
2. Selecteer een regel voor een grootboekrekening waarvan de grootboekposten die u wilt zien, geboekte inkoop- en verkoopdocumenten zijn zonder inkomende documentrecords en kies vervolgens de actie **Geboekte documenten zonder inkomend document**.
3. U kunt ook de actie **Posten** kiezen.
4. Kies op de pagina **Grootboekposten** de actie **Geboekte documenten zonder inkomend document**.

De pagina **Geboekte documenten zonder inkomend document** wordt geopend en toont geboekte inkoop- en verkoopdocumenten zonder inkomende documentrecords die worden gerepresenteerd door grootboekposten in de Grootboekrekening waarvoor u de pagina hebt geopend. De pagina kan maximaal 1000 regels weergeven. Standaard bevat het veld **Datumfilter** daarom een filter dat de regels beperkt tot posten met een boekingsdatum vanaf het begin van de boekhoudperiode tot de werkdatum.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Gevonden documenten koppelen aan bestaande inkomende documentrecords
1. Selecteer op de pagina **Geboekte documenten zonder inkomend document** de regel voor een geboekt document dat u wilt koppelen aan een bestaande inkomende documentrecord en kies vervolgens de actie **Inkomend document selecteren** .
2. Selecteer op de pagina **Inkomende documenten** de inkomende documentrecord die u wilt koppelen aan het gevonden geboekte document en kies vervolgens de knop **OK**.
3. Selecteer op de pagina **Geboekte documenten zonder inkomend document** de inkomende documentrecord die nu is gekoppeld aan het geboekte document, zoals u kunt zien in het feitenblok **Inkomende documentbestanden**.

Als er geen relevante inkomende documentrecord op de pagina **Inkomende documenten** staat, kunt u er een maken. Zie [Inkomende documentrecords maken](across-how-create-income-document-records.md) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Inkomende documenten verwerken](across-process-income-documents.md)  
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]