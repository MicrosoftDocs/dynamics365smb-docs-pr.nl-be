---
title: Inkomende documenten verwerken| Microsoft Docs
description: Als u een extern document, zoals een PDF, wilt registreren in Business Central, moet u eerst een inkomende documentrecord maken of voltooien.
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
ms.openlocfilehash: bbec76297e32ec033d8f5c0fb0f24f54804ca532
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753087"
---
# <a name="processing-incoming-documents"></a>Inkomende documenten verwerken
Als u een extern document wilt registreren in [!INCLUDE[prod_short](includes/prod_short.md)], moet u eerst een inkomende documentrecord maken of voltooien. U kunt dit handmatig doen of u kunt een foto van het externe document maken en vervolgens de inkomende documentrecord maken met het afbeeldingsbestand bijgevoegd.

Vanuit PDF- of afbeeldingsbestanden die u ontvangt van uw handelspartners, kunt u elektronische documenten laten genereren door een externe OCR-service (Optical Character Recognition - optische tekenherkenning), die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)]. Bijvoorbeeld, wanneer u facturen in PDF-indeling van uw leverancier ontvangt, kunt u deze naar de OCR-service verzenden vanaf de pagina **Inkomende documenten**. U kunt ook het bestand naar de OCR-service via e-mail verzenden. Wanneer u het elektronische document terug ontvangt, wordt automatisch een gerelateerde inkomende documentrecord gemaakt. Na enkele seconden krijgt u het bestand weer terug van de OCR-service als een elektronische factuur die kan worden geconverteerd naar een inkoopfactuur voor de leverancier.

| Als u dit wilt doen | Zie |
| --- | --- |
| Maak inkomende documentrecords handmatig of automatisch door een foto te maken van een papieren ontvangstbewijs, bijvoorbeeld. |[Inkomende documentrecords maken](across-how-create-income-document-records.md) |
| Gebruik een OCR-service om PDF- en afbeeldingsbestanden naar elektronische documenten om te zetten die bijvoorbeeld kunnen worden geconverteerd naar inkoopfacturen in [!INCLUDE[prod_short](includes/prod_short.md)]. Train de OCR-service om fouten te voorkomen als de volgende keer vergelijkbare gegevens worden verwerkt. |[OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) |
| Verbind of verwijder inkomende documentrecords voor elk niet-geboekte verkoop- of inkoopdocument en voor elke klant- of grootboekpost uit het document of de post. |[Inkomende documentrecords maken direct van documenten en posten](across-how-connect-disconnect-income-document-records.md) |
| Vanuit de pagina's **Rekeningschema** en **Grootboekposten** zoekt u naar grootboekposten voor geboekte documenten die geen inkomende documentrecords hebben, en koppelt u deze centraal aan bestaande records of maakt u nieuwe records met gekoppelde documentbestanden. |[Geboekte documenten zonder inkomende documentrecords zoeken](across-how-find-posted-documents-without-income-document-records.md) |
| Beter overzicht krijgen door inkomende documentrecords in te stellen op Verwerkt om ze te verwijderen uit de standaardweergave. |[Vele inkomende documentrecords beheren](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Zie ook
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]