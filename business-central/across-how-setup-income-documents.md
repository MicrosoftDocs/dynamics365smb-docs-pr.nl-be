---
title: Inkomende documenten instellen| Microsoft Docs
description: Gebruik de functie inkomende documenten om elektronische documenten te maken, OCR-taken te beheren, facturen te importeren en afbeeldingsbestanden te converteren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 313de95353fc42b222fa95cd36d320881a7fbdb8
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442597"
---
# <a name="set-up-incoming-documents"></a>Inkomende documenten instellen

Als u dagboekregels van inkomende documentrecords maakt, moet u op de pagina **Instellingen van inkomende documenten** vastleggen welke dagboeksjabloon en batch moeten worden gebruikt.

Als u niet wilt dat gebruikers facturen of dagboekregels maken van inkomende documentrecords, tenzij de documenten zijn goedgekeurd, moet u werkstroomfiatteurs instellen.

Als u PDF- en afbeeldingsbestanden naar elektronische documenten wilt omzetten waarnaar u kunt converteren, bijvoorbeeld inkoopfacturen in [!INCLUDE[prod_short](includes/prod_short.md)], moet u eerst de OCR-functie instellen en de service inschakelen. Kies een servicepakket dat past bij uw organisatie en/of land/regio. U kunt ook handmatig items maken die de externe documenten vertegenwoordigen.  

Wanneer de functie Inkomende documenten is ingesteld, kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten. Zie [Inkomende documenten verwerken](across-process-income-documents.md) voor meer informatie.

## <a name="to-set-up-the-incoming-documents-feature"></a>De functie Inkomende documenten instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instellingen inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Als onderdeel van de instelling moet u beslissen of u goedkeuring van inkomende documenten wilt hebben. Om goedkeuring te vereisen moet u goedkeurders en goedkeuringswerkstromen instellen. Als uw organisatie niet van plan is goedkeuring te vereisen, kunt u de volgende sectie overslaan.  

Ten slotte, als u een service gebruikt om PDF- of afbeeldingsbestanden te converteren die inkomende documenten vertegenwoordigen, moet u deze instellen. Anders kunt u die sectie ook overslaan.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Fiatteurs van inkomende documentrecords instellen

Stel eventueel een goedkeuringsproces in voor de inkomende documenten. Fiatteurs van inkomende documenten moeten worden ingesteld als gebruikers van goedkeuringswerkstromen.

Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. Op de pagina **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Een OCR-service instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **OCR-service instellen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Uw aanmeldgegevens worden automatisch versleuteld.

Zie [OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook

[Inkomende documenten verwerken](across-process-income-documents.md)  
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]