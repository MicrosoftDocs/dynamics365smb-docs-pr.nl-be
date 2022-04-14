---
title: Werkstromen gebruiken
description: U kunt werkstromen instellen en gebruiken die bedrijfsprocessen verbinden, zoals automatisch boeken of het aanvragen en verlenen van goedkeuring voor nieuwe records.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 8fc4dc464e6562684db6b4ae67422f59cb641927
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511219"
---
# <a name="use-workflows"></a>Werkstromen gebruiken

Een werkstroom is een reeks taken die worden geactiveerd door een actie, een voorwaarde of een regel. Werkstromen worden meestal geïmplementeerd om bedrijfslogica in een organisatie te integreren, zoals het scheiden van taken, het verenigen van processen of om vertrouwen en verantwoordelijkheden te vergroten.  

De werkstromen zijn ontworpen om aanvragen voor goedkeuring van een nieuwe waarde te creëren, terwijl de oude waarde behouden blijft voor het geval het verzoek niet wordt goedgekeurd. De nieuwe waarde wordt pas geïmplementeerd nadat de laatste aanvraag is goedgekeurd.  

De bedrijfslogica kan goedkeuring zijn van:

- Nieuwe hoofdgegevens zoals grootboekrekeningen, klanten, leveranciers of artikelen
- Wijzigingen in velden in bestaande records die zinvolle informatie bevatten, zoals: **Bankrekeningnr. leverancier** of **Kredietlimiet van klant**
- Wijzigingen in velden in bestaande records die bedrijfskritische informatie bevatten, zoals **Verkoopprijzen van artikelen**
- Nieuwe gebruikers of wijzigingen in gebruikersmachtigingen
- Inkoopdocumenten
- Verkoopdocumenten
- Inkomende documenten
- Financiële dagboeken voorafgaand aan boeking

De volgende afbeelding toont een voorbeeld van een werkstroom met sequentiële goedkeuring die wordt geactiveerd door een gebruiker. Door de workflow te activeren, wordt een goedkeuringsverzoek gemaakt voor de eerste fiatteur.  

![Illustratie van een werkstroom met sequentiële goedkeuring.](media/Workflows/approval-flow.png)

In dit voorbeeld moet de aanvraag worden goedgekeurd door de eerste fiatteurgoed voordat de aanvraag wordt doorgestuurd naar de volgende fiatteur. Als het verzoek niet wordt goedgekeurd door de eerste fiatteur, gaat het verzoek nooit naar de volgende fiatteur.  

De route die wordt gevolgd vanaf de eerste activering van de werkstroom kan variëren, afhankelijk van de aard van de goedkeuring.  

De volgende afbeelding toont een parallelle goedkeuring die door de gebruiker wordt geactiveerd. Door de werkstroom te activeren wordt er tegelijkertijd een goedkeuringsverzoek naar alle fiatteurs gestuurd.  

![Illustratie van een werkstroom met parallelle goedkeuring.](media/Workflows/approval-flow-2.png)

De werkstroom wordt echter pas goedgekeurd als alle aanvragen zijn goedgekeurd door de fiatteurs, zoals weergegeven in de volgende afbeelding:  

![Illustratie van een afgewezen werkstroom met parallelle goedkeuring.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Het is niet mogelijk om een werkstroom te maken met meerdere fiatteurs en te verwachten dat de hele werkstroom wordt goedgekeurd nadat de eerste aanvraag is goedgekeurd. Alle aanvragen moeten worden goedgekeurd voordat de werkstroom kan worden goedgekeurd.

U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Het is ook mogelijk om dezelfde werkstroom meerdere keren aan te maken. Elke werkstroom geactiveerd door een gebeurtenis met verschillende filters. Dit is handig als een goedkeuringsverzoek in de ene afdeling moet worden goedgekeurd door één fiatteur, terwijl goedkeuringsverzoeken in andere afdelingen door een andere fiatteur moeten worden goedgekeurd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.  

 Voordat u kunt beginnen met werkstromen gebruiken, moet u de werkstroomgebruikers instellen, werkstromen maken, mogelijk de code aanpassen en opgeven hoe gebruikers berichten ontvangen. Zie voor meer informatie [Werkstromen instellen](across-set-up-workflows.md).  

> [!NOTE]  
> Veelvoorkomende werkstroomstappen gaan over gebruikers die goedkeuring aanvragen voor taken, en fiatteurs die goedkeuringsaanvragen accepteren of afwijzen. Daarom verwijzen veel onderwerpen over het gebruik van werkstromen naar goedkeuringen.  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Stel in dat een werkstroom start wanneer de eerste invoerpuntgebeurtenis plaatsvindt.|[Werkstromen inschakelen](across-how-to-enable-workflows.md)|  
|Vraag goedkeuring van een taak aan, als fiatteur, accepteer, weiger of delegeer goedkeuringen en verzend of bekijk goedkeuringsberichten.|[Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md)|  
|Maak werkstroomstappen die voorkomen dat een bepaald recordtype wordt gebruikt voordat een bepaalde gebeurtenis plaatsvindt, bijvoorbeeld de goedkeuring van de record.|[Gebruik van een record beperken en toestaan](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Geef instanties van werkstroomstappen met de status Voltooid weer.|[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md)|  
|Verwijder een werkstroom als u zeker weet dat u die niet meer gebruikt.|[Werkstromen verwijderen](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a>Zie ook  
[Werkstromen instellen](across-set-up-workflows.md)   
[Werkstroom](across-workflow.md)   
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]