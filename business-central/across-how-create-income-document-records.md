---
title: Inkomende documentrecords maken
description: 'Gebruik verschillende functies op de pagina Inkomende documenten om onkostenbewijzen te bekijken, OCR-taken te beheren, inkomende documentbestanden te converteren en externe bestanden bij te voegen.'
author: jswymer
ms.topic: how-to
ms-service: dynamics365-business-central
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 03/2/2023
ms.author: jswymer
ms.custom: bap-template
ms.reviewer: jswymer
---
# Inkomende documentrecords maken

Op de pagina **Inkomende documenten** kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.

Als u een extern document wilt registreren in [!INCLUDE[prod_short](includes/prod_short.md)], moet u eerst een inkomende documentrecord maken of voltooien. U kunt deze taken handmatig uitvoeren of u kunt een foto van het externe document maken om de inkomende documentrecord te maken met het afbeeldingsbestand bijgevoegd.

Voordat u de functie **Inkomende documenten** gebruikt, moet u de benodigde instellingen uitvoeren. Zie voor meer informatie [Inkomende documenten instellen](across-how-setup-income-documents.md).

## Een inkomend document goedkeuren of weigeren

Als u de functie **Inkomende documenten** hebt ingesteld om goedkeuring te vereisen om documenten te maken, moeten gebruikers met de juiste rechten de records goedkeuren voordat ze worden verwerkt. Zie voor meer informatie [Fiatteurs van inkomende documentrecords instellen](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel met het document dat u wilt goedkeuren of weigeren en kies vervolgens de actie **Goedkeuren** of **Weigeren**.

Als u de inkomende documentrecord goedkeurt, wordt het selectievakje **Vrijgegeven** op de regel van het inkomende document geselecteerd. De gebruiker die verantwoordelijk is voor het aanmaken van, bijvoorbeeld, inkoopfacturen kan doorgaan om de record te verwerken.

## Een inkomende documentrecord maken door een foto te maken

> [!NOTE]  
> De volgende procedure geldt alleen voor de tablet en telefoonclient van [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies in het rolcentrum de tegel **Inkomend document maken van camera** en ga vervolgens naar stap 4.
2. Of kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
3. Kies op de pagina **Inkomende documenten** **Nieuw** en kies vervolgens **Maken van camera**. De camera op de tablet of de telefoon wordt ingeschakeld.
4. Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **Gebruiken**.

    Er wordt een nieuwe documentrecord gemaakt met de afbeelding gekoppeld.

## Een afbeelding aan een inkomende documentrecord koppelen door een foto te maken

> [!NOTE]  
> De volgende procedure geldt alleen voor de tablet en telefoonclient van [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een bestaande inkomende documentrecord.
3. Kies op de documentrecordpagina **Verwerken** en kies vervolgens **Afbeelding van camera bijvoegen**. De camera op de tablet of de telefoon wordt ingeschakeld.
4. Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **Gebruiken**.

    De afbeelding wordt gekoppeld aan de inkomende documentrecord.

## Een inkomend documentrecord handmatig maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en kies vervolgens de actie **Maken van bestand**.  
3. Voer op de pagina **Bestand invoegen** een van de volgende stappen uit om een bestand toe te voegen dat het inkomende document vertegenwoordigt:

   [!INCLUDE[file-upload](includes/file-upload.md)]

4. U kunt ook de actie **Nieuw** kiezen en vervolgens de volgende stappen uitvoeren:

    1. Als u een bestand wilt bijvoegen, kiest u **Verwerken** > **Bestand koppelen**.
    2. Sleep op de pagina **Bestand invoegen** een geselecteerd bestand dat het betreffende inkomende document vertegenwoordigt, of selecteer **klik hier om te bladeren** om het bestand te vinden en te openen.
    3. Vul op de pagina **Inkomende documenten** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Zie gerelateerde [Microsoft-training](/training/modules/incoming-documents-dynamics-365-business-central/)

## Zie ook

[OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md)
[Inkomende documentrecords maken direct van documenten en posten](across-how-connect-disconnect-income-document-records.md)
[Geboekte documenten zonder inkomende documentrecords zoeken](across-how-find-posted-documents-without-income-document-records.md)
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
