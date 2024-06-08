---
title: Goedkeuringswerkstromen gebruiken
description: 'U kunt werkstromen instellen en gebruiken die bedrijfsprocessen verbinden, zoals automatisch boeken of het aanvragen en verlenen van goedkeuring voor nieuwe records.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 02/20/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="use-approval-workflows"></a>Goedkeuringswerkstromen gebruiken

Een werkstroom is een reeks taken die worden geactiveerd door een actie, een voorwaarde of een regel. Werkstromen worden meestal geïmplementeerd om bedrijfslogica in een organisatie te integreren, zoals het scheiden van taken, het verenigen van processen of het toepassen van best practices.

De werkstromen kunnen zijn ontworpen om aanvragen voor goedkeuring van een wijziging van een recordveld te maken, terwijl de oude gegevens behouden blijven voor het geval het verzoek niet wordt goedgekeurd. De nieuwe waarde wordt pas geïmplementeerd nadat de laatste aanvraag is goedgekeurd.

De bedrijfslogica kan de goedkeuring zijn van:

- Nieuwe stamgegevens zoals grootboekrekeningen, klanten, leveranciers of artikelen.
- Wijzigingen in velden in bestaande records die vertrouwelijke informatie bevatten, zoals: **Bankrekeningnr. leverancier** of **Kredietlimiet van klant**.
- Wijzigingen in velden in bestaande records die bedrijfskritische informatie bevatten, zoals **Verkoopprijzen van artikelen**.
- Nieuwe gebruikers of wijzigingen in gebruikersmachtigingen.
- Inkoopdocumenten.
- Verkoopdocumenten.
- Inkomende documenten.
- Financiële dagboeken voorafgaand aan boeking.

De volgende afbeelding toont een voorbeeld van een werkstroom met sequentiële goedkeuring die wordt geactiveerd door een gebruiker. Door de workflow te activeren, wordt een goedkeuringsverzoek gemaakt voor de eerste fiatteur.  

![Illustratie van een werkstroom met sequentiële goedkeuring.](media/Workflows/approval-flow.png)

In de bovenstaande afbeelding ziet u hoe de aanvraag moet worden goedgekeurd door de eerste fiatteur voordat deze wordt doorgestuurd naar de volgende. Als het verzoek niet wordt goedgekeurd door de eerste fiatteur, gaat het verzoek nooit naar de volgende fiatteur.

De route die wordt gevolgd vanaf de eerste activering van de werkstroom kan variëren, afhankelijk van de aard van de goedkeuring.  

De volgende afbeelding toont een parallelle goedkeuring die door de gebruiker wordt geactiveerd. Een parallelle goedkeuring betekent dat een goedkeuringsverzoek tegelijk naar alle fiatteurs wordt gestuurd.  

![Illustratie van een werkstroom met parallelle goedkeuring.](media/Workflows/approval-flow-2.png)

De werkstroom wordt echter pas afgesloten als alle aanvragen zijn goedgekeurd, zoals weergegeven in de volgende afbeelding:  

![Illustratie van een afgewezen werkstroom met parallelle goedkeuring.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Voor een werkstroom met meerdere fiatteurs moeten alle fiatteurs elke stap goedkeuren voordat de werkstroom naar de volgende gebeurtenis kan gaan. Goedkeuring van slechts één fiatteur zal de werkstroom niet vooruit helpen.

U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Het is ook mogelijk om dezelfde werkstroom meerdere keren te maken. Elke werkstroom kan worden geactiveerd door een gebeurtenis met verschillende filters. Dit is handig als een goedkeuringsverzoek in de ene afdeling moet worden goedgekeurd door één fiatteur, terwijl goedkeuringsverzoeken in andere afdelingen door een andere fiatteur moeten worden goedgekeurd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.  

Voordat u kunt beginnen met werkstromen gebruiken, moet u de werkstroomgebruikers instellen, werkstromen maken, mogelijk de code aanpassen en opgeven hoe gebruikers berichten ontvangen. Zie voor meer informatie [Werkstromen instellen](across-set-up-workflows.md).

> [!NOTE]  
> Veelvoorkomende werkstroomstappen gaan over gebruikers die goedkeuring aanvragen voor taken, en fiatteurs die goedkeuringsaanvragen accepteren of afwijzen. Daarom verwijzen veel onderwerpen over het gebruik van werkstromen naar goedkeuringen.  

 De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.  

| **Als u dit wilt doen** | **Zie** |
|--|--|
| Stel een goedkeuringswerkstroom in wanneer de eerste invoerpuntgebeurtenis plaatsvindt. | [Goedkeuringswerkstromen inschakelen](across-how-to-enable-workflows.md) |
| Vraag goedkeuring van een taak aan; accepteer, weiger of delegeer goedkeuringen als fiatteur; en verzend of bekijk goedkeuringsberichten. | [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md) |
| Maak werkstroomstappen die voorkomen dat een bepaald recordtype wordt gebruikt voordat een bepaalde gebeurtenis plaatsvindt, bijvoorbeeld de goedkeuring van de record. | [Gebruik van een record beperken en toestaan](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Geef instanties van werkstroomstappen met de status **Voltooid** weer. | [Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md) |
| Verwijder een goedkeuringswerkstroom als u zeker weet dat u die niet meer gebruikt. | [Goedkeuringswerkstromen verwijderen](across-how-to-delete-workflows.md) |

## <a name="see-also"></a>Zie ook

[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Werkstroom](across-workflow.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
