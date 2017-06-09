---
title: 'Procedure: Interacties maken voor contacten en segmenten | Microsoft Docs'
description: Beschrijft hoe u interacties maakt voor contacten en segmenten in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b50d332441bee01158559616fff5d5f5ca381a90
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-interactions-on-contacts-and-segments"></a>Procedure: Interacties maken voor contacten en segmenten
U kunt interacties maken om alle interacties en communicatie vast te leggen die u hebt met uw contacten en segmenten, bijvoorbeeld direct mail.

Voordat u interacties maakt, moet u interactiesjablonen instellen. Zie voor meer informatie [Interactiesjablonen instellen](marketing-interactions.md#set-up-interaction-templates).

## <a name="to-create-an-interaction"></a>Een interactie maken
1. Open het contact, de verkoper of de interactielogpost.
2. Kies de actie **Interactie maken**.
3. Vul de velden in en kies de knop **OK**.

**Opmerking**: als u nog een andere taak in wilt uitvoeren voordat u de interactie voltooit, kunt u **Annuleren** kiezen en ervoor kiezen de interactie op een later tijdstip te voltooien. Dit stelt de interactie uit.

## <a name="to-finish-and-delete-postponed-interactions"></a>Uitgestelde interacties voltooien en verwijderen
1. Open het contact, de verkoper of de interactielogpost.
2. Kies **Uitgestelde interacties**.
3. Selecteer de interactie die u wilt voltooien, en kies vervolgens de actie **Hervatten**.

## <a name="to-create-an-interaction-on-a-segment"></a>Een interactie voor een segment maken
1. Kies op de startpagina **Actieve segmenten** of klik in de rechterbovenhoek op het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Segmenten** in en klik op de gerelateerde koppeling.
2. Vul in het venster **Segment** in het gedeelte **Interactie** de velden in waarmee u wilt opgeven welke interactie u wilt toewijzen aan het segment.

    Nadat u een interactie aan het segment hebt toegewezen, kunt u de interactie persoonlijk aanpassen voor de verschillende contacten in het segment, bijvoorbeeld door een andere interactiesjabloon te selecteren of door de bijlage te wijzigen op de regels in het venster **Segment**.  
3. Om het segment en de interacties vast te leggen kiest u de actie **Logbestand**. Het venster **Segment registreren** wordt geopend.
4. Als u een nieuw segment wilt maken met dezelfde contacten, schakelt u het selectievakje **Opvolgingssegm. maken** in. Voordat het opvolgingssegment kan worden gemaakt, moet u nummerreeksen voor segmenten hebben ingesteld in het venster **Marketinginstellingen**.

Een interactie wordt geregistreerd voor elk contact binnen het segment in de tabel **Interactielogpost** en het segment wordt geregistreerd. Geregistreerde segmenten kunt u vinden in het venster **Geregistreerd segment**.

Als u het selectievakje **Opvolgingssegment maken** hebt ingeschakeld, wordt er automatisch een nieuw segment gemaakt met dezelfde contacten als in het segment dat u zojuist hebt geregistreerd.

## <a name="see-also"></a>Zie ook
[Interacties registreren](marketing-interactions.md)  
[Contactpersonen beheren](marketing-contacts.md)  
[Verkoopopportunities beheren](marketing-manage-sales-opportunities.md)  
[CRM instellen](marketing-setup-marketing.md)  
[Werken met Financials](ui-work-product.md)

