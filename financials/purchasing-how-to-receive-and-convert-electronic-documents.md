---
title: Elektronische documenten ontvangen en converteren | Microsoft Docs
description: U kunt elektronische documenten rechtstreeks van handelspartners of via een OCR-service ontvangen.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1e2f5142eb21d346b17b7d541191df553086b30f
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="receive-and-convert-electronic-documents"></a>Elektronische documenten ontvangen en converteren
De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt het ontvangen van elektronische facturen en creditnota's in de PEPPOL-indeling, die wordt ondersteund door de grootste aanbieders van documentuitwisselingsservices. Als u bijvoorbeeld een factuur van een leverancier wilt ontvangen als elektronisch PEPPOL-document, verwerkt u het document in het venster Inkomende documenten om het te converteren naar een inkoopfactuur of dagboekregel in [!INCLUDE[d365fin](includes/d365fin_md.md)].

 Naast het rechtstreeks ontvangen van elektronische documenten van handelspartners, kunt u elektronische documenten ontvangen van een OCR-service die van uw PDF- of afbeeldingsbestanden elektronische documenten heeft gemaakt.  

 Voordat u elektronische documenten via de documentuitwisselingsservice kunt ontvangen, moet u eerst diverse mastergegevens, zoals bedrijfsgegevens, leveranciers, artikelen en maateenheden instellen. Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer gegevens en elementen in het inkomende documentbestand worden geconverteerd naar velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md) voor meer informatie.  

 Voordat u elektronische documenten via de OCR-service kunt ontvangen, moet u de vooraf geconfigureerde serviceverbinding instellen en inschakelen. Zie voor meer informatie [Inkomende documenten instellen](across-how-setup-income-documents.md).  

 Het verkeer van elektronische documenten in en uit [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt beheerd door de functie Taakwachtrij. Voordat u elektronische documenten kunt ontvangen, moet de relevante taakwachtrij worden gestart.  

 U kunt de conversie van elektronische documenten handmatig starten, zoals in deze procedure wordt beschreven, of u kunt een werkstroom inschakelen om elektronische documenten automatisch te converteren wanneer deze worden ontvangen. De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een werkstroomsjabloon, *Werkstroom van inkomend elektronisch via OCR naar open Inkoopfactuur*, die naar een werkstroom kan worden gekopieerd en kan worden ingeschakeld. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

> [!NOTE]  
>  Wanneer u elektronische documenten die van de OCR-service worden ontvangen, converteert naar documenten of journaalregels in [!INCLUDE[d365fin](includes/d365fin_md.md)], worden meerdere regels in het brondocument op één regel gecombineerd. De ene regel krijgt het type Grootboekrekening en de velden **Omschrijving** en **Nr.** (van grootboekrekening) zijn leeg. De waarde in het veld **Bedrag** is gelijk aan het totaalbedrag, exclusief btw van alle regels in het brondocument.  
>   
>  Om ervoor te zorgen dat de velden **Omschrijving** en **Nr.** worden ingevuld, kunt u de knop **Tekst afstemmen op rekening** kiezen in het venster **Inkomende documenten** om te definiëren dat een bepaalde factuurtekst altijd aan een bepaalde debet- of creditrekening in het grootboek wordt toegewezen. Het veld **Omschrijving** op document- of dagboekregels die zijn gemaakt van een elektronisch document voor die leverancier of klant wordt gevuld met de betreffende tekst en het veld **Nr.** (van grootboekrekening) wordt gevuld met de betreffende rekening.  
>   
>  In plaats van toe te wijzen aan een grootboekrekening kunt u ook toewijzen aan een bankrekening. Dit is bijvoorbeeld handig voor elektronische documenten voor kosten die al zijn betaald en waarvoor u een dagboekregel wilt maken die kan worden geboekt naar een bankrekening.  

 In de volgende procedure wordt beschreven hoe u een leveranciersfactuur ontvangt en converteert naar een inkooporder in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dezelfde procedure geldt wanneer u een leveranciersfactuur converteert naar een dagboekregel.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Een elektronische factuur ontvangen en converteren naar een inkoopfactuur  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkomende documenten** en klik op de gerelateerde koppeling.  

2.  Selecteer de regel voor de inkomende documentrecord die een nieuwe elektronische factuur representeert, en kies vervolgens op het tabblad **Start** in de groep **Beheren** de optie **Bewerken**.  

     In het venster **Kaart inkomend document** wordt het gerelateerde XML-bestand gekoppeld en worden de meeste velden vooraf ingevuld met informatie uit de elektronische factuur. Zie [Inkomende documentrecords maken](across-how-create-income-document-records.md) voor meer informatie.  

3.  Kies in het veld **Soort gegevensuitwisseling** de optie **PEPPOL-factuur** of **OCR-factuur**, afhankelijk van de bron van het elektronische document.  

4.  Als u tekst in de leveranciersfactuur wilt toewijzen aan een specifieke debetrekening, kiest u op het tabblad **Acties** in de groep **Algemeen** de optie **Tekst afstemmen op rekening**. Vervolgens vult u het venster **Toewijzing tekst aan rekening** in.  

5.  Kies op het tabblad **Acties** in de groep **Algemeen** de optie **Document maken**.  

     Er wordt in [!INCLUDE[d365fin](includes/d365fin_md.md)] een inkoopfactuur gemaakt op basis van de gegevens in het elektronische document.  

     Eventuele validatiefouten, die meestal worden veroorzaakt door onjuiste of ontbrekende hoofdgegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)], worden weergegeven op het sneltabblad **Foutmeldingen**.  

## <a name="see-also"></a>Zie ook  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Inkomende documenten](across-income-documents.md)  
[Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)   
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

