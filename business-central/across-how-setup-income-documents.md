---
title: Inkomende documenten instellen
description: 'De functie Inkomende documenten instellen om elektronische documenten te maken, OCR-taken te beheren, facturen te importeren en afbeeldingsbestanden te converteren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="set-up-incoming-documents" />Inkomende documenten instellen

Als u dagboekregels van inkomende documentrecords maakt, moet u op de pagina **Instellingen van inkomende documenten** vastleggen welke dagboeksjabloon en batch moeten worden gebruikt.

Wanneer de functie **Inkomende documenten** is ingesteld, kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten. Zie [Inkomende documentrecords maken](across-how-create-income-document-records.md) voor meer informatie.

## <a name="to-set-up-the-incoming-documents-feature" />De functie Inkomende documenten instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Als onderdeel van de instelling moet u beslissen of u goedkeuring van inkomende documenten wilt hebben. Om goedkeuring te vereisen moet u [goedkeurders en goedkeuringswerkstromen instellen](#to-set-up-approvers-of-incoming-document-records). Als uw organisatie niet van plan is goedkeuring te vereisen, kunt u de volgende sectie overslaan.

Ten slotte, als u een OCR-service gebruikt om PDF- of afbeeldingsbestanden te converteren die inkomende documenten vertegenwoordigen, moet u [deze instellen](#to-set-up-an-ocr-service). Anders kunt u die sectie ook overslaan.

## <a name="to-set-up-approvers-of-incoming-document-records" />Fiatteurs van inkomende documentrecords instellen

Als u niet wilt dat gebruikers facturen of dagboekregels maken van inkomende documentrecords, tenzij de documenten eerst zijn goedgekeurd, stelt u een goedkeuringsproces in voor inkomende documenten. Fiatteurs van inkomende documenten moeten worden ingesteld als gebruikers van goedkeuringswerkstromen.

Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. Op de pagina **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is. Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service" />Een OCR-service instellen

Als u PDF- en afbeeldingsbestanden wilt omzetten in elektronische documenten die u kunt converteren naar facturen, creditnota's of dagboekregels, stelt u de OCR-functie in. U kunt ook handmatig items maken die de externe documenten vertegenwoordigen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **OCR-service instellen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Uw aanmeldgegevens worden automatisch versleuteld.

Zie [OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.  

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
