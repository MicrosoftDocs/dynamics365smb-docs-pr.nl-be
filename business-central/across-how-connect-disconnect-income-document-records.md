---
title: Inkomende documentrecords maken van documenten
description: U kunt externe bedrijfsdocumenten opslaan door de documentbestanden aan de gerelateerde inkomende documentrecords te koppelen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a><a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Inkomende documentrecords maken direct van documenten en posten

U kunt externe bedrijfsdocumenten opslaan in [!INCLUDE[prod_short](includes/prod_short.md)] door de documentbestanden aan de gerelateerde inkomende documentrecords te koppelen. Als het document, zoals een inkoopfactuur, niet is ontstaan als inkomende documentrecord, kunt u het later nog maken en koppelen aan een inkomende documentrecord. U kunt inkomende documentbestanden ook koppelen aan geboekte inkoop- en verkoopdocumenten en aan leveranciers-, klant- en grootboekposten door het feitenblok **Inkomende documentbestanden** te gebruiken, bijvoorbeeld op de pagina **Geboekte inkoopfacturen** en de pagina **Leveranciersposten**.

Vanuit de pagina's **Rekeningschema** en **Grootboekposten** kunt u zoeken naar grootboekposten voor geboekte inkoop- en verkoopdocumenten die geen inkomende documentrecords hebben, en deze centraal koppelen aan bestaande records of nieuwe records maken met gekoppelde documentbestanden. Zie [Geboekte documenten zonder inkomende documentrecords zoeken](across-how-find-posted-documents-without-income-document-records.md) voor meer informatie.

In de volgende procedures wordt beschreven hoe u een bestand koppelt aan een leverancierspost of een bestaande inkoopfactuur die niet van een inkomende documentrecord is gemaakt. Het koppelen van een bestand aan geboekte inkoop- of verkoopdocumenten werkt op dezelfde wijze.

## <a name="create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a><a name="create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Een inkomende documentrecord maken van een inkoopfactuur en koppelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor een inkoopfactuur waaraan u een bestand wilt koppelen en kies vervolgens de actie **Inkomend document van bestand maken**.
3. U kunt ook de regel voor een inkoopfactuur selecteren waaraan u een bestand wilt koppelen en vervolgens de actie **Bestand koppelen** kiezen.
4. Op de pagina **Bestand invoegen**, selecteert u het bestand dat het betreffende inkomende document vertegenwoordigt. Kies vervolgens de knop **Openen**.

## <a name="create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a><a name="create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Een inkomende documentrecord maken van een leverancierspost en koppelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Leveranciersposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een regel voor een leverancierspost waaraan u een bestand wilt koppelen en kies vervolgens de actie **Inkomend document van bestand maken**.
3. U kunt ook een regel voor een leverancierspost selecteren waaraan u een bestand wilt koppelen en vervolgens de actie **Bestand koppelen** kiezen.
4. Op de pagina **Bestand invoegen**, selecteert u het bestand dat het betreffende inkomende document vertegenwoordigt. Kies vervolgens de knop **Openen**.

## <a name="remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a><a name="remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>De relatie van een inkomende documentrecord met een geboekt document verwijderen

U kunt bestandbijlagen van niet-geboekte documenten op elk moment verwijderen door de gerelateerde inkomende documentrecord te verwijderen. Als het document is geboekt, moet u eerst de relatie met de inkomende documentrecord verwijderen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor een inkomende documentrecord die is verbonden met een geboekt document dat u wilt verwijderen en kies vervolgens de actie **Referentie naar record verwijderen**.

De verbinding met het geboekte document wordt verwijderd. U kunt nu doorgaan met het verbinden van een andere inkomende documentrecord met het geboekte document, zoals wordt beschreven in dit artikel.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Inkomende documentrecords maken](across-how-create-income-document-records.md)
[OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md)
[Geboekte documenten zonder inkomende documentrecords zoeken](across-how-find-posted-documents-without-income-document-records.md)
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
