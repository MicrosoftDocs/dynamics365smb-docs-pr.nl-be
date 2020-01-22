---
title: Elektronische documenten verzenden | Microsoft Docs
description: Leer hoe u facturen elektronisch verzendt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 10547ee8f8a9e760721e12746fc25031001e7330
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2954123"
---
# <a name="send-electronic-documents"></a>Elektronische documenten verzenden
De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt het verzenden van elektronische facturen en creditnota's in de PEPPOL-indeling, die wordt ondersteund door de grootste aanbieders van documentuitwisselingsservices. Een aanbieder van documentuitwisselingsservices verzendt elektronische documenten tussen handelspartners. Om ondersteuning te bieden voor elektronische documentindelingen, gebruikt u het kader voor gegevensuitwisseling.  

 In de algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] is een service voor documentuitwisseling vooraf geconfigureerd zodat u deze kunt instellen voor uw bedrijf. Zie [Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md) voor meer informatie.  

 Als u een verkoopfactuur als elektronisch PEPPOL-document wilt versturen, selecteert u de optie **Elektronisch document** in het dialoogvenster **Boeken en verzenden**. Hierin kunt u dit ook instellen als standaardprofiel voor documentverzending van de klant. Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, klanten, artikelen en eenheden. Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer gegevens worden geconverteerd in velden in [Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Een elektronische verkoopfactuur verzenden  

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies de gerelateerde koppeling  

2.  Maak een nieuwe verkoopfactuur.  

3.  Wanneer de verkoopfactuur klaar is voor facturering, kiest u de actie **Boeken en verzenden**.  

     Als het standaardverzendprofiel van de klant **Elektronisch document** is, wordt dit aangegeven in het dialoogvenster **Boeken en bevestiging verzenden** en hoeft u alleen maar de knop **Ja** te kiezen om de factuur te boeken en elektronisch te verzenden in de geselecteerde indeling.  

4.  In het dialoogvenster **Boeken en bevestiging verzenden** kiest u de Knop AssistEdit rechts van het veld **Document verzenden naar**.  

5.  Kies in het dialoogvenster **Document verzenden naar** in het veld **Elektronisch document** de optie **Via service voor documentuitwisseling**.  

6.  Kies in het veld **Indeling** de optie **PEPPOL**.  

7.  Kies de knop **Ok**. Het dialoogvenster **Boeken en bevestiging verzenden** verschijnt. **Elektronisch document (PEPPOL)** is toegevoegd aan het veld **Document verzenden naar**.  

8.  Kies de knop **Ja**.  

     De verkoopfactuur wordt geboekt en aan de klant gezonden als elektronisch document in de indeling PEPPOL.  

    > [!NOTE]  
    >  U kunt ook een geboekte verkoopfactuur als een elektronisch document verzenden. De procedure is hetzelfde als beschreven in dit onderwerp voor niet-geboekte verkoopdocumenten. Kies op de pagina **Geboekte verkoopfactuur** de actie **Activiteitenlogboek** om de status van en elektronische document weer te geven. Zie voor meer informatie **Activiteitenlogbestand**.  

## <a name="see-related-training-at-microsoft-learnlearnmoduleselectronic-documents-dynamics-365-business-centralindex"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Verzendprofielen van documenten instellen](sales-how-setup-document-send-profiles.md)  
[Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md)  
[Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
