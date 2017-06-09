---
title: Inkomende documenten| Microsoft Docs
description: Inkomende documenten beheren
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 01/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8fe06d78320970c667f638341da4abc28fa1e4ac
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="incoming-documents"></a>Inkomende documenten
Bepaalde bedrijfstransacties worden niet vanaf het begin geregistreerd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In plaats daarvan wordt een extern bedrijfsdocument bezorgd bij uw bedrijf als e-mailbijlage of als papieren exemplaar dat u kunt scannen. Dit is meestal bij aankopen, waarbij dergelijke inkomende documentbestanden betalingontvangsten voor kosten of kleine inkopen vertegenwoordigen.

In PDF- of afbeeldingsbestanden die inkomende documenten vertegenwoordigen, kunt u een externe OCR-service (Optical Character Recognition - optische tekenherkenning) elektronische documenten laten genereren die naar documentrecords kunnen worden geconverteerd binnen [!INCLUDE[d365fin](includes/d365fin_md.md)].

In het venster **Inkomende documenten** kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.

Het proces voor inkomende documenten kan bestaan uit de volgende voornaamste activiteiten:

* Registreer op een van de volgende manieren de externe documenten in [!INCLUDE[d365fin](includes/d365fin_md.md)] door regels te maken in het venster **Inkomende documenten**:
  * Handmatig door eenvoudige functies te gebruiken, vanaf een pc of een mobiel apparaat, op een van de volgende manieren:
    * Met de knop **Maken van bestand** en vul vervolgens de relevante velden in het venster **Inkomend document** in. Het bestand wordt automatisch gekoppeld.  
    * Met de knop **Nieuw** en vul vervolgens de relevante velden in het venster **Inkomend document** in en koppel het gerelateerde bestand handmatig.
    * Vanaf een tablet of een telefoon, gebruik de knop **Maken van camera** om een nieuwe inkomende documentrecord te maken en vervolgens de afbeelding te verzenden naar de OCR-service, bijvoorbeeld.
  * Automatisch, door het document van de OCR-service te ontvangen als een elektronisch document nadat u het gerelateerde PDF- of afbeeldingsbestand per e-mail naar de OCR-service hebt verzonden per e-mail. Het sneltabblad **Financiële informatie** wordt automatisch ingevuld in het venster **Inkomend document**.
* Gebruik de OCR-service om PDF- of afbeeldingsbestanden te laten omzetten naar elektronische documenten die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Maak nieuwe documenten of dagboekregels voor inkomende documentrecords door de informatie in te voeren die u leest uit inkomende documentbestanden.
* Koppel inkomende documentbestanden aan inkoop- en verkoopdocumenten van elke status, inclusief de leveranciers-, klant- en grootboekposten die het resultaat zijn van boeking.
* Bekijk inkomende documentrecords en de bijlagen ervan vanuit elk inkoop- en verkoopdocument of elke post, of zoek alle grootboekposten zonder inkomende documentrecords in het venster **Rekeningschema**.

| Als u dit wilt doen | Zie |
| --- | --- |
| De functie Inkomende documenten instellen en de OCR-service instellen. |[Procedure: Inkomende documenten instellen](across-how-setup-income-documents.md) |
| Maak inkomende documentrecords, koppel bestanden, gebruik OCR om PDF-bestanden om te zetten in elektronische documenten, converteer elektronische documenten naar documentrecords, controleer inkomende documentrecords uit geboekte verkoop- en inkoopdocumenten. |[Inkomende documenten verwerken](across-process-income-documents.md) |

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

