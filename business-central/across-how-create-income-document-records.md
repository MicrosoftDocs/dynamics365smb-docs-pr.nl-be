---
title: Records maken van inkomende documenten| Microsoft Docs
description: U kunt records maken van inkomende documenten, zoals e-facturen, en OCR-taken, eCommerce en documentuitwisseling beheren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 637bb7ae6a757681ab0ada1b61ba0ec303a9cb97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384761"
---
# <a name="create-incoming-document-records"></a>Inkomende documentrecords maken
Op de pagina **Inkomende documenten** kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.

Als u een extern document wilt registreren in [!INCLUDE[prod_short](includes/prod_short.md)], moet u eerst een inkomende documentrecord maken of voltooien. U kunt dit handmatig doen of u kunt een foto van het externe document maken en vervolgens de inkomende documentrecord maken met het afbeeldingsbestand bijgevoegd.

Voordat u de functie Inkomende documenten gebruikt, moet u de benodigde instellingen uitvoeren. Zie voor meer informatie [Inkomende documenten instellen](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Een inkomend document goedkeuren of weigeren
Als u gebruikers niet wilt toestaan om facturen of dagboekregels te maken van inkomende documentrecords, tenzij ze zijn goedgekeurd, kunt u goedkeurders instellen die de records moeten goedkeuren voordat ze kunnen worden verwerkt.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies de desbetreffende koppeling.
2. Selecteer de regel met het document dat u wilt goedkeuren of weigeren en kies vervolgens de actie **Goedkeuren** of **Weigeren**.

Als u de inkomende documentrecord goedkeurt, wordt het selectievakje **Vrijgegeven** op de regel van het inkomende document geselecteerd. De gebruiker die verantwoordelijk is voor het aanmaken van, bijvoorbeeld, inkoopfacturen kan doorgaan om de record te verwerken.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Een inkomende documentrecord maken door een foto te maken
> [!NOTE]  
>   De volgende procedure geldt alleen voor de [!INCLUDE[prod_short](includes/prod_short.md)] Tablet- en Telefoon-client.

1. Kies op de app-balk de tegel **Inkomend document maken van camera** en ga vervolgens naar stap 4.
2. U kunt ook op de app-bar de optieknop kiezen, **Inkomende documenten** kiezen en **Alle** kiezen.
3. Kies op de pagina **Inkomende documenten** de selectieknop en kies vervolgens **Maken van camera**. De camera op de tablet of de telefoon wordt ingeschakeld.
4. Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **OK**.

    Er wordt een nieuwe documentrecord gemaakt met de afbeelding gekoppeld.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Een afbeelding aan een inkomende documentrecord koppelen door een foto te maken
> [!NOTE]  
>   De volgende procedure geldt alleen voor de [!INCLUDE[prod_short](includes/prod_short.md)] Tablet- en Telefoon-client.

1. Kies op de app-bar de optieknop, kies **Inkomende documenten** en kies **Alle**.
2. Open de kaart voor een bestaande inkomende documentrecord.
3. Kies op de pagina **Inkomende documenten** de selectieknop en kies vervolgens **Afbeelding van camera bijvoegen**. De camera op de tablet of de telefoon wordt ingeschakeld.
4. Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **OK**.

    De afbeelding wordt gekoppeld aan de inkomende documentrecord.

## <a name="to-create-an-incoming-document-record-manually"></a>Een inkomend documentrecord handmatig maken
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies de desbetreffende koppeling.
2. Kies de actie **Maken van bestand**.  
3. Selecteer op de pagina **Bestand invoegen** een bestand en kies vervolgens **Openen**. Het bestand wordt automatisch gekoppeld.
4. U kunt ook de actie **Nieuw** kiezen.
5. Als u een bestand wilt bijvoegen, kiest u de actie **Bestand koppelen**.
6. Op de pagina **Bestand invoegen**, selecteert u het bestand dat het betreffende inkomende document vertegenwoordigt. Kies vervolgens de knop **Openen**.
7. Vul op de pagina **Inkomende documenten** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Zie ook
[Inkomende documenten verwerken](across-process-income-documents.md)  
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]