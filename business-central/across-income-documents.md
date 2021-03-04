---
title: Werken met inkomende documenten| Microsoft Docs
description: U kunt inkomende externe bedrijfsdocumenten, zoals betalingsontvangsten of PDF's beheren, OCR-taken beheren en elektronische bestanden naar documenten en records omzetten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f6250dd8921f50c4bb8ac2beba52a3aaf54df1c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754429"
---
# <a name="incoming-documents"></a>Inkomende documenten

Bepaalde bedrijfstransacties worden niet vanaf het begin geregistreerd in [!INCLUDE[prod_short](includes/prod_short.md)]. In plaats daarvan wordt een extern bedrijfsdocument bezorgd bij uw bedrijf als e-mailbijlage of als papieren exemplaar dat u kunt scannen. Dit is meestal bij aankopen, waarbij dergelijke inkomende documentbestanden betalingontvangsten voor kosten of kleine inkopen vertegenwoordigen.

In PDF- of afbeeldingsbestanden die inkomende documenten vertegenwoordigen, kunt u een externe OCR-service (Optical Character Recognition - optische tekenherkenning) elektronische documenten laten genereren die naar documentrecords kunnen worden geconverteerd binnen [!INCLUDE[prod_short](includes/prod_short.md)]. Kies een servicepakket dat past bij uw organisatie en/of land/regio. U kunt ook handmatig items maken die de externe documenten vertegenwoordigen.  

Op de pagina **Inkomende documenten** kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.

Het proces voor inkomende documenten kan bestaan uit de volgende voornaamste activiteiten:

* Registreer op een van de volgende manieren de externe documenten in [!INCLUDE[prod_short](includes/prod_short.md)] door regels te maken op de pagina **Inkomende documenten**:
  * Handmatig door eenvoudige functies te gebruiken, vanaf een pc of een mobiel apparaat, op een van de volgende manieren:
    * Gebruik de knop **Maken van bestand** en vul vervolgens de relevante velden op de pagina **Inkomend document** in. Het bestand wordt automatisch gekoppeld.  
    * Gebruik de knop **Nieuw** en vul vervolgens de relevante velden op de pagina **Inkomend document** in en koppel het gerelateerde bestand handmatig.
    * Vanaf een tablet of een telefoon, gebruik de knop **Maken van camera** om een nieuwe inkomende documentrecord te maken en vervolgens de afbeelding te verzenden naar de OCR-service, bijvoorbeeld.
  * Automatisch, door het document van de OCR-service te ontvangen als een elektronisch document nadat u het gerelateerde PDF- of afbeeldingsbestand per e-mail naar de OCR-service hebt verzonden per e-mail. Het sneltabblad **Financiële informatie** wordt automatisch ingevuld op de pagina **Inkomend document**.
* Gebruik de OCR-service om PDF- of afbeeldingsbestanden te laten omzetten naar elektronische documenten die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)].
* Maak nieuwe documenten of dagboekregels voor inkomende documentrecords door de informatie in te voeren die u leest uit inkomende documentbestanden.
* Koppel inkomende documentbestanden aan inkoop- en verkoopdocumenten van elke status, inclusief de leveranciers-, klant- en grootboekposten die het resultaat zijn van boeking.
* Bekijk inkomende documentrecords en de bijlagen ervan vanuit elk inkoop- en verkoopdocument of elke post, of zoek alle grootboekposten zonder inkomende documentrecords op de pagina **Rekeningschema**.

| Aan | Zie |
| --- | --- |
| De functie Inkomende documenten instellen en de OCR-service instellen. |[Inkomende documenten instellen](across-how-setup-income-documents.md) |
| Maak inkomende documentrecords, koppel bestanden, gebruik OCR om PDF-bestanden om te zetten in elektronische documenten, converteer elektronische documenten naar documentrecords, controleer inkomende documentrecords uit geboekte verkoop- en inkoopdocumenten. |[Inkomende documenten verwerken](across-process-income-documents.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]