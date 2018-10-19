---
title: Te late betaling voorspellen voor verkoopdocumenten | Microsoft Docs
description: Gebruik ons voorspellend model om te voorspellen of een factuur op tijd betaald zal worden.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 960c8bcd172602a8ab5ea8f3774740bd63fe8ff6
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="the-late-payment-prediction-extension"></a>De extensie Voorspelling van te late betaling  
Effectief beheer van tegoeden is belangrijk voor de algemene financiële status van een bedrijf. De extensie Voorspelling van te late betaling kan u helpen uitstaande tegoeden te reduceren en uw inningsstrategie af te stemmen door te voorspellen of verkoopfacturen op tijd worden betaald. Als bijvoorbeeld wordt voorspeld dat een betaling te laat zal zijn, kunt u besluiten de betalingsvoorwaarden of de betalingsmethode voor de klant aan te passen.

## <a name="what-are-predictions-based-on"></a>Waar worden voorspellingen op gebaseerd?  
De extensie Voorspelling van te late betaling gebruikt een voorspellend model dat wij in Azure Machine Learning Studio Azure hebben ontwikkeld en hebben getraind met gegevens die representatief zijn voor allerlei kleine tot middelgrote bedrijven. Hoewel we ons voorspellend model al hebben getraind en geëvalueerd, blijft ons voorspellend model leren van uw gegevens. Hoe meer u het model gebruikt en hoe meer gegevens u eraan voert, hoe accurater uw voorspellingen worden. Standaard evalueert de extensie het model en worden de voorspellingen bijgewerkt op wekelijkse basis. U kunt de voorspellingen echter wanneer u wilt bijwerken door de actie **Voorspelling bijwerken** te kiezen in het venster **Klantenposten**.  

> [!Note]
> Wij gebruiken elke week een beetje van uw computertijd wanneer we het model evalueren en uw voorspellingen bijwerken. Naast handmatig aanpassen van uw voorspellingen zijn er andere acties die computertijd gebruiken: wanneer u het model traint (bijvoorbeeld als u onlangs gegevens hebt toegevoegd) en wanneer u het model evalueert (waarbij naar de kwaliteit van het model wordt gekeken).

## <a name="getting-started"></a>Aan de slag
De extensie is gratis in [!INCLUDE[d365fin](includes/d365fin_md.md)] en we bieden een abonnement aan op Azure Machine Learning. Het abonnement biedt 30 minuten computertijd per maand. Als u meer dan dat nodig hebt, kunt u uw eigen voorspellend model maken en dit gebruiken. Zie voor meer informatie het gedeelte _Uw eigen voorspellend model maken_, verderop in dit onderwerp.  

Wanneer u een geboekt verkoopdocument opent, wordt boven in het venster een bericht weergegeven. Als u de Extensie Voorspelling van te late betaling wilt gebruiken, kunt u deze inschakelen door **Activeren** te kiezen in het bericht. U kunt ook handmatig de extensie instellen. Bijvoorbeeld als u betreurt dat u het bericht hebt gesloten.  

Als u de extensie handmatig wilt inschakelen, voert u de volgende stappen uit:

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceverbindingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de optie **Voorspelling van te late betalingen instellen** en vul de benodigde velden in.

## <a name="viewing-all-payment-predictions"></a>Alle betalingsvoorspellingen weergeven
Als u de extensie inschakelt, is de tegel **Voorspelling van te late betalingen instellen** beschikbaar in het rolcentrum **Bedrijfsmanager**. De tegel bevat het aantal betalingen dat voorspeld wordt te laat te zijn en u kunt het venster **Klantenposten** openen waarin u dieper op de geboekte facturen kunt inzoomen. Er zijn drie kolommen om aandacht aan te besteden:  

* **Te late betaling**: geeft aan of de betaling van de factuur voorspeld wordt om te laat te zijn.
* **Zekerheid van voorspelling**: geeft aan hoe betrouwbaar de voorspelling is. **Hoog** betekent dat de voorspelling minimaal 90% zeker is, **Gemiddeld** ligt tussen 80 en 90% en **Laag** ligt onder 80%.
* **Zekerheidspercentage van voorspelling**: toont het werkelijke percentage achter de betrouwbaarheidsscore. Standaard wordt deze kolom niet weergegeven, maar u kunt deze toevoegen als u wilt. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

> [!Tip]
> Het venster Klantenposten bevat ook een feitenblok aan de rechterkant. Terwijl u voorspellingen bekijkt, kunnen de gegevens in de sectie **Klantdetails** handig zijn. Wanneer u de factuur in de lijst hebt gekozen, bevat het gedeelte gegevens over de klant. U kunt ook direct actie ondernemen. Als een klant bijvoorbeeld slecht betaalt, kunt u de klantenkaart vanuit het feitenblok openen en de klant blokkeren voor toekomstige verkopen.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Een betalingsvoorspelling weergeven voor een specifiek verkoopdocument
U kunt vooraf te late betalingen voorspellen. In de vensters **Verkoopoffertes**, **Verkooporders** en **Verkoopfacturen** kunt u de actie **Betaling voorspellen** gebruiken om een voorspelling te genereren voor het verkoopdocument dat u bekijkt.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** window you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Uw eigen voorspellend model maken
Bent u geïnteresseerd in het maken van uw eigen voorspellend model? U kunt Azure Machine Learning Studio gebruiken om uw eigen voorspellend model te maken en het gebruiken in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als u uw eigen model wilt gebruiken, moet u zich abonneren op Azure Machine Learning. Zie voor meer informatie [Documentatie van Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765).  

We bieden echter een gemakkelijkere manier om uw eigen voorspellend model te maken en te gebruiken. U kunt gegevens vanuit uw facturen met ons voorspellend experiment delen in Azure Machine Learning en ons experiment een voorspellend model laten maken en trainen op basis van uw gegevens. Als u uw gegevens wilt delen, kiest u in het venster **Voorspelling van te late betalingen instellen** de actie **Mijn model maken**. Achteraf worden voorspellingen gebaseerd op uw model en uw gegevens, niet de onze.  

> [!Note]
>   De kwaliteit van het model is belangrijk. Wanneer ons voorspellend experiment uw gegevens gebruikt om een model te trainen, wordt een kwaliteitswaarde voor het model als percentage bepaald. De modelkwaliteit geeft aan hoe accuraat de voorspellingen van het model waarschijnlijk zijn. Verschillende factoren kunnen de kwaliteit van een model beïnvloeden. Bijvoorbeeld dat er onvoldoende gegevens waren of dat de gegevens niet voldoende variatie bevatten. U kunt de kwaliteit van het model dat u momenteel gebruikt, bekijken in het venster **Voorspelling van te late betalingen instellen**. U kunt ook een minimumdrempelwaarde voor de modelkwaliteit opgeven. Modellen met een kwaliteitswaarde onder de drempel produceren geen voorspellingen.  

### <a name="to-use-your-model-instead-of-ours"></a>Uw model in plaats van het onze gebruiken  
Als u uw eigen model maakt in Azure Machine Learning Studio, zonder de hulpmiddelen in [!INCLUDE[d365fin](includes/d365fin_md.md)] te gebruiken, moet u uw aanmeldingsgegevens opgeven, zodat [!INCLUDE[d365fin](includes/d365fin_md.md)] het model kan openen. Er is een aantal stappen om dat te doen:

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorspelling van te late betalingen instellen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het selectievakje **Mijn Azure-abonnement gebruiken**.  
3. Kies in het veld **Geselecteerd model** de optie **Mijn model**.  
4. Voer op het sneltabblad **Aanmeldingsgegevens van mijn model** de API-URL en API-sleutel voor uw model op.  

## <a name="see-also"></a>Zie ook  
[Documentatie van Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Business Central aanpassen met extensies](ui-extensions.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

