---
title: Verkoopregels voorstellen met Copilot
description: Meer informatie over regels op verkooporders voorstellen met Copilot.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# Regels op verkoopdocumenten voorstellen met Copilot (preview)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u sneller verkoopdocumenten kunt maken door Copilot te laten voorstellen welke artikelen worden toegevoegd aan regels op verkoopdocumenten voor uw klanten.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Informatie over verkoopregels voorstellen met Copilot

Verkoopregelsuggesties met Copilot kunnen helpen bij het maken van regels in verkoopdocumenten zoals verkoopoffertes, orders en facturen op basis van gestructureerde invoer of natuurlijke taal. De functie is geen chat voor algemene doeleinden, maar een zeer specifieke en geïntegreerde ervaring die u kunt gebruiken voor verkoopdocumenten. De functie biedt twee verschillende vaardigheden waarmee u gegevens over afzonderlijke producten of volledige documenten kunt vinden.

* Producten vinden

  Informatie die producten beschrijft, wordt op meerdere plaatsen opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)]. Zo worden artikelnummers en omschrijvingen opgeslagen in de tabel **Artikel**, worden meerdere barcodes opgeslagen in de tabel **Artikelreferentie** en worden producteigenschappen opgeslagen in de tabel **Artikelkenmerken**. Terwijl u misschien vraagt naar een *Rode fiets*, kan het daadwerkelijke product een *karmozijnrode toerfiets*, waar *Fiets* is een productcategorie en *rood* een kenmerk.

* Documenten zoeken op verwijzing

  Vaak herhalen mensen een eerdere bestelling of gebruiken ze deze op zijn minst als uitgangspunt. Maar het kan lastig zijn om de juiste volgorde in een reeks bestellingen te vinden. Mogelijk herinnert u zich een deel van de id van de bestelling. Dit kan een door het bedrijf toegewezen nummer zijn of een referentienummer dat u van een klant hebt ontvangen. Als u prompts kunt gebruiken als *Laatste factuur van april nodig*, zou u een bestelling sneller moeten kunnen vinden.

## Vereisten

* Verkoopregelsuggestie met Copilot wordt ingeschakeld en geactiveerd door een beheerder. Voor meer informatie over het inschakelen van AI-mogelijkheden gaat u naar [Copilot- en AI-mogelijkheden configureren](enable-ai.md).
* U bent bekend met het maken van verkooporders.

## Geografische beschikbaarheid

De volgende tabel toont de geografische Microsoft Azure-gebieden waarin deze functie beschikbaar is.

|Omgeving Azure-regio  |Azure OpenAI Service-geografie   |Beheerdersactie vereist om Copilot te ontgrendelen  |
|---------|---------|---------|
|Duitsland (Noord, West-Centraal)     | Zweden of Zwitserland        |  Ja       |
|Noorwegen (Oost, West)     | Zweden of Zwitserland        | Ja     |
|Singapore     |         |         |
|Zuid-Afrika (Noord, West)     |   Verenigde Staten      |   Ja      |
|Zwitserland (Noord, West)     |  Zweden of Zwitserland       |    Ja     |
|Verenigde Arabische Emiraten (Noord, West)     |    Verenigde Staten     |   Ja     |
|Verenigde Staten (Centraal, Oost, Noord-Centraal, Zuid-Centraal, West)     |   Verenigde Staten      |   Nr.      |
|Europa (West, Noord)     |   Zweden of Zwitserland      |   Ja      |
|Azië/Pacific     |         |         |
|Australië (Zuidoost)     |   Verenigde Staten      |    Ja     |
|Zuid-Amerika     |         |         |
|India (Centraal, Zuid)     |    Verenigde Staten     |   Ja      |
|Japan (Oost, West)     |    Verenigde Staten     |    Ja     |
|Frankrijk (Centraal, Zuid)     |    Zweden of Zwitserland     |    Ja     |
|Korea (Centraal, Zuid)     |    Verenigde Staten     |    Ja     |

## Voorbeelden van prompts

Verkoopregels voorstellen met Copilot kan een breed scala aan prompts verwerken. In deze sectie vindt u enkele voorbeelden van prompts voor verschillende scenario's die we hebben getest.

### Voorbeeldaanvraag om het vorige document te herhalen

Prompt: *Ik heb alle producten van factuur 103031 nodig*

### Tijdens het telefoongesprek typt de gebruiker snel een lijst met vereiste producten en hoeveelheden, niet altijd nauwkeurig genoeg of met interne productnamen

Prompt: *2 rood kinderfitsen*

Merk op dat de prompt werkt, zelfs met meerdere typefouten.

### Een gebruiker kopieert een vraag uit een inkomende communicatie en plakt deze op de pagina Suggesties voor verkoopregels

Prompt: *Hallo, ik ben geïnteresseerd in accessoires voor mijn XXXX-laptop, zoals een draadloze muis, een toetsenbordhoes en een laptoptas. Ik vraag me af of u aanbevelingen of suggesties heeft voor deze items. Heeft u speciale aanbiedingen of kortingen voor trouwe klanten zoals ik? Met vriendelijke groet, M*

Merk op dat XXXX-laptop niet in de zoekresultaten is opgenomen.

## Regels op een verkoopdocument voorstellen

In dit proces wordt beschreven hoe u regels op een verkooporder kunt voorstellen. De stappen zijn hetzelfde voor verkoopoffertes en facturen.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporder** in en kies vervolgens de gerelateerde koppeling.
1. Open de verkooporder.
1. Op het sneltabblad **Regels** selecteert u **Voorstellen voor regels ophalen**.
1. Voer in het venster **Regels voorstellen met Copilot** uw prompt in of selecteer er een uit de prompthulp.

## Suggesties bekijken, opslaan, weggooien of opnieuw genereren

Nadat Copilot de artikelen heeft voorgesteld om aan regels toe te voegen, bekijkt u de suggesties en bepaalt u of dit is wat u zoekt:

* Als u één voorgestelde regel wilt verwijderen, selecteert u deze in de lijst en selecteert u vervolgens de actie **Regel verwijderen**.
* Om alle voorgestelde regels te verwijderen en het Copilot-venster te sluiten, kiest u de knop Verwijderen (prullenbak) naast de knop **Behouden**.
* Als u de regels die in het Copilot-venster worden weergegeven wilt overdragen, kiest u **Behouden**. 

Er is een veld **Betrouwbaarheid** met de scores **Hoog (80+)**, **Gemiddeld ( 60-80)** en **Laag (60-)** dat u wijst op regels die aandacht behoeven.

Met deze stap bevestigt u dat u de regels naar een verkoopdocument wilt overbrengen. U kunt daar ook de overgedragen regels verwijderen of bewerken, of het hele document verwijderen.

## Zie ook

[Veelgestelde vragen over verkoopregels voorstellen met Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Copilot- en AI-mogelijkheden configureren](enable-ai.md)
