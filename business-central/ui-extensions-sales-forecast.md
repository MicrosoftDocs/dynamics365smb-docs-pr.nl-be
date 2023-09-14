---
title: De extensie Verkoop- en voorraadprognose gebruiken om voorraad te beheren | Microsoft Docs
description: Deze extensie helpt verkopen voorspellen om een duidelijk overzicht te krijgen van verwachte nulvoorraden en helpt u zelfs aanvullingsorders voor leveranciers te maken.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 12/20/2021
ms.author: bholtorf
---

# De extensie Verkoop- en voorraadprognose

Voorraadbeheer is een wisselwerking tussen klantenservice en het beheren van uw kosten. Enerzijds is voor weinig voorraad minder werkkapitaal nodig, maar anderzijds leiden nulvoorraden mogelijk tot gemiste verkopen. De extensie Verkoop- en voorraadprognose voorspelt potentiële verkopen aan de hand van historische gegevens en biedt een helder overzicht van verwachte nulvoorraden. Op basis van de prognose helpt de extensie aanvullingsaanvragen aan leveranciers te maken en bespaart u tijd.  

## Prognoses instellen

De verbinding met [Azure AI](https://azure.microsoft.com/overview/ai-platform/) is al voor u ingesteld in [!INCLUDE[prod_short](includes/prod_short.md)]. Maar u kunt de prognose configureren voor gebruik van een ander soort rapportageperiode. Zo kunt u overschakelen van prognose per maand naar prognose per kwartaal. U kunt ook het aantal perioden kiezen op basis waarvan de prognose moet worden berekend, afhankelijk van hoe specifiek u de prognose wilt. We stellen voor dat u een prognose maakt per maand en met een horizon van 12 maanden voor de prognose.

> [!TIP]  
> Overweeg de lengte van de perioden die de service in de berekeningen gebruikt. Hoe meer gegevens u biedt, hoe nauwkeuriger de voorspellingen zullen zijn. Let ook op grote variaties in perioden. Deze zijn ook van invloed op voorspellingen. Als Azure AI niet voldoende gegevens vindt of de gegevens sterk variëren, doet de service geen voorspelling.

## De prognoses gebruiken

De extensie gebruikt Azure AI om toekomstige verkoop op basis van uw verkoophistorie te voorspellen om u te helpen voorraadtekort te voorkomen. Wanneer u bijvoorbeeld een artikel op de pagina **Artikelen** kiest, wordt in het diagram in het deelvenster **Artikelprognose** de geschatte verkoop van dit artikel in de komende periode getoond. Op deze manier kunt u zien of uw voorraad van het artikel waarschijnlijk binnenkort op raakt.  

U kunt de extensie ook gebruiken om voorstellen te doen met betrekking tot bevoorrading. Als u bijvoorbeeld een inkooporder maakt voor Fabrikam omdat u de nieuwe bureaustoel wilt kopen, doet de extensie Verkoop- en voorraadprognose het voorstel om ook de LONDON-draaistoel te herbevoorraden die u gewoonlijk van deze leverancier koopt. Dit komt omdat de extensie voorspelt dat uw voorraad van de LONDON-draaistoel in de komende twee maanden op raakt. U kunt dus eventueel nu al meer stoelen bestellen.  

## Ontwerpdetails

Abonnementen voor [!INCLUDE[prod_short](includes/prod_short.md)] komen met toegang tot verschillende voorspellende webservices in alle regio's waar [!INCLUDE[prod_short](includes/prod_short.md)] beschikbaar is. Zie de Microsoft Dynamics 365 Business Central Licentiehandleiding voor meer informatie. De gids kan worden gedownload op de [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/)-website. 

Deze webservices zijn staatloos, wat betekent dat ze gegevens alleen gebruiken om voorspellingen op aanvraag te berekenen. Ze slaan geen gegevens op.

> [!NOTE]  
>   U kunt ook uw eigen voorspellende webservice gebruiken in plaats van de onze. Zie [Uw eigen voorspellende webservice voor verkoop- en voorraadprognoses maken en gebruiken](#AnchorText). 

### Vereiste gegevens voor prognoses

Om voorspellingen te doen over toekomstige verkopen, heeft de webservice kwantitatieve gegevens nodig over verkopen in het verleden. Die gegevens zijn afkomstig van de velden **Boekingsdatum**, **Artikelnr.** en **Hoeveelheid** op de pagina **Artikelposten**, waar:

- De boekingssoort is 'Verkoop'.
- De boekingsdatum ligt tussen de datum die wordt berekend op basis van de waarden in de velden **Historische perioden** en **Periodesoort** op de pagina **Instelling van verkoop- en voorraadprognose** en de werkdatum.

Voordat de webservice wordt gebruikt, comprimeert [!INCLUDE[prod_short](includes/prod_short.md)] transacties op **Artikelnr.** en **Boekingsdatum**, op basis van de waarde in het veld **Periodesoort** op de pagina **Instelling van verkoop- en voorraadprognose**.

## <a name="AnchorText"> </a>Uw eigen voorspellende webservice voor verkoop- en voorraadprognoses maken en gebruiken

U kunt uw eigen voorspellende webservice maken op basis van een openbaar model met de naam **Prognosemodel voor Business Central**. Dit voorspellend model is online beschikbaar in de Azure AI-galerie. Ga als volgt te werk om het model te gebruiken:  

1. Open een browser en ga naar de [Azure AI-galerie](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Zoek naar **Prognosemodel voor Microsoft Business Central** en open het model in Azure Machine Learning Studio.  
3. Gebruik het Microsoft-account om u aan te melden voor een werkruimte en kopieer vervolgens het model.  
4. Voer het model uit en publiceer het als een webservice.  
5. Noteer de API-URL en de API-sleutel. U kunt deze aanmeldingsgegevens voor een cashflowinstelling gebruiken.  
6. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instelling van verkoop- en voorraadprognose** in en kies vervolgens de gerelateerde koppeling.  
7. Vouw het sneltabblad **Algemeen** uit en vul de velden API-URL en API-sleutel in.  

## Zie gerelateerde [Microsoft-training](/training/modules/use-sales-inventory-forecast-extension/)

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Voorraad](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Artificial Intelligence in Microsoft Dynamics 365 Business Central gebruiken](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
