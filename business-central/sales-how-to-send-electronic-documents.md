---
title: Elektronische documenten verzenden
description: Leer hoe u facturen elektronisch verzendt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383012"
---
# <a name="send-electronic-documents"></a>Elektronische documenten verzenden

De algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt het verzenden van elektronische facturen en creditnota's in de PEPPOL-indeling, een indeling die wordt ondersteund door de grootste aanbieders van documentuitwisselingsservices. Een aanbieder van documentuitwisselingsservices verzendt elektronische documenten tussen handelspartners. Om ondersteuning te bieden voor elektronische documentindelingen, gebruikt u het kader voor gegevensuitwisseling.  

 In de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] is een service voor documentuitwisseling vooraf geconfigureerd zodat u deze kunt instellen voor uw bedrijf. Zie [Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md) voor meer informatie. In sommige gevallen moet u echter een app installeren. Zie voor meer informatie [Veelgestelde vragen over elektronische facturering](faq-electronic-invoicing.yml).  

 Als u een verkoopfactuur als elektronisch PEPPOL-document wilt verzenden, selecteert u de optie **Elektronisch document** in het dialoogvenster **Boeken en verzenden**. U kunt ook het standaardprofiel voor documentverzending van de klant instellen vanuit dat dialoogvenster. Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, klanten, artikelen en eenheden. Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer gegevens worden geconverteerd in velden in [Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Een elektronische verkoopfactuur verzenden

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies de gerelateerde koppeling  

2. Maak een nieuwe verkoopfactuur.  

3. Wanneer de verkoopfactuur klaar is voor facturering, kiest u de actie **Boeken en verzenden**.  

     Als het standaardverzendprofiel van de klant **Elektronisch document** is, wordt het weergegeven in het dialoogvenster **Boeken en bevestiging verzenden**. Op deze manier hoeft u alleen maar de knop **Ja** te kiezen om de factuur elektronisch in de geselecteerde indeling te boeken en te verzenden.  

4. In het dialoogvenster **Boeken en bevestiging verzenden** kiest u de Knop AssistEdit rechts van het veld **Document verzenden naar**.  

5. Kies in het dialoogvenster **Document verzenden naar** in het veld **Elektronisch document** de optie **Via service voor documentuitwisseling**.  

6. Kies in het veld **Indeling** de optie **PEPPOL**.  

7. Kies de knop **Ok**. Het dialoogvenster **Boeken en bevestiging verzenden** verschijnt. **Elektronisch document (PEPPOL)** is toegevoegd aan het veld **Document verzenden naar**.  

8. Kies de knop **Ja**.  

     De verkoopfactuur wordt geboekt en naar de klant verzonden in de PEPPOL-indeling.  

    > [!NOTE]  
    >  U kunt ook een geboekte verkoopfactuur als een elektronisch document verzenden. De procedure is hetzelfde als beschreven in dit onderwerp voor niet-geboekte verkoopdocumenten. Kies op de pagina **Geboekte verkoopfactuur** de actie **Activiteitenlogboek** om de status van en elektronische document weer te geven.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Verkopen factureren](sales-how-invoice-sales.md)  
[Verzendprofielen van documenten instellen](sales-how-setup-document-send-profiles.md)  
[Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md)  
[Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[Veelgestelde vragen over elektronische facturering](faq-electronic-invoicing.yml)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]