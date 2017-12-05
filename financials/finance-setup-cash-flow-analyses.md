---
title: Cashflowanalyse instellen| Microsoft Docs
description: De grafieken in het rolcentrum Rekeningen instellen om de geldstroom in uw bedrijf te helpen analyseren, inclusief kosten en inkomsten, liquiditeit en kasontvangsten minus contante betalingen.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 7d78333c5a7151ad60f07433ba32cfea142a2445
ms.contentlocale: nl-be
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-cash-flow-analysis"></a>Cashflowanalyse instellen
Als u wat hulp wilt bij het bepalen wat u met uw contant geld moet doen, kunt de diagrammen bekijken in het rolcentrum Accountant:  

* **Cashcyclus**  
* **Inkomsten en uitgaven**  
* **Cashflow**  
* **Cashflowprognoses**  

In dit onderwerp wordt beschreven waar de gegevens in de diagrammen van afkomstig zijn en, indien nodig, wat u moet doen als u de diagrammen wilt gaan gebruiken.  

## <a name="the-cash-cycle-and-income--expense-charts"></a>De diagrammen Cashcyclus en Inkomsten en uitgaven
De diagrammen **Cashcyclus** en **Inkomsten en uitgaven** zijn gereed voor gebruik, gebaseerd op de rekeningschema's en rapportageschema´s. De rekeningen bevinden zich waar de gegevens uit afkomstig zijn en met rapportageschema´s wordt de relatie tussen verkopen en tegoeden berekend. Er worden enkele rekeningen en rapportageschema´s verschaft. U kunt deze ongewijzigd gebruiken, ze aanpassen en nieuwe toevoegen. Als u grootboekrekeningen toevoegt aan uw rekeningschema, bijvoorbeeld door deze te importeren uit QuickBooks, moet u een koppeling maken naar de rekeningen op de pagina **Rapportageschema´s** voor de volgende rapportageschemanamen:  

| Naam rapportschema | Waar het wordt gebruikt |
| --- | --- |
| **I_CACYCLE** |Cashcyclus |
| **I_CASHFLOW** |Cashflow |
| **I_INCEXP** |Inkomsten en uitgaven |
| **I_MINTRIAL** |Als resultatenrekening als u het rekeningschema niet gebruikt |

**Opmerking:** het is raadzaam de berekeningen te behouden die voor het rapportageschema worden verschaft.  

Voer rekeningen in het veld **Samentelling** voor **Totale opbrengsten**, **Totale tegoeden**, **Totaal schulden** en **Totale voorraad** in. Als u een koppeling wilt maken naar een bereik rekeningen of meer dan één specifieke rekening, voert u de rekeningnummers in die worden gescheiden door respectievelijk ".." of een verticale streep. Bijvoorbeeld **1111..4444** of **2222|3333|5555**.  

**Tip** controleer uw koppeling door de actie **Overzicht** te kiezen.  

## <a name="set-up-the-cash-flow-chart"></a>Het cashflowdiagram instellen
Het cashflowdiagram is gebaseerd op het volgende:  

* Een diagram van cashflowrekeningen.
* Een of meer cashflowinstellingen. Hiermee worden de rekeningen opgegeven die moeten worden gebruikt voor grootboek, inkoop, verkoop, services en vaste activa.  

Om u te helpen aan de slag te gaan zijn er enkele rekeningen en cashflowinstellingen verschaft. U kunt deze toevoegen, veranderen of verwijderen.  

Als u deze wilt instellen, kunt u zoeken naar **cashflowrekeningen**, de koppeling kiezen en vervolgens de velden invullen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Herhaal deze stappen voor **cashflowinstellingen**.  

## <a name="set-up-cash-flow-forecasts"></a>Cashflowprognoses instellen
In het diagram **Cashflowprognose** worden cashflowrekeningen, cashflowinstellingen en cashflowprognoses gebruikt. Sommige worden verschaft, maar u kunt die van uzelf instellen met behulp van een begeleide instelling. Met de begeleide instelling kunt u zaken opgeven zoals het aantal keren dat de prognose moet worden bijgewerkt, op welke rekeningen de prognose moet worden gebaseerd, wanneer u belastingen betaalt en of [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) moet worden ingeschakeld.  

Cashflowprognoses kunnen Cortana Intelligence gebruiken om documenten met een vervaldatum in de toekomst op te nemen. Het resultaat is een uitvoerigere voorspelling. De verbinding met Cortana Intelligence is al voor u ingesteld. U hoeft het alleen in te schakelen. Wanneer u zich bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] aanmeldt, verschijnt er een melding in een blauwe balk en wordt er een koppeling verschaft naar de standaardcashflowinstellingen. De melding wordt slechts eenmaal weergegeven. Als u de melding sluit, maar besluit Cortana Intelligence in te schakelen, kunt u de begeleide instelling gebruiken of een handmatig proces.  

> [!NOTE]  
>   U kunt ook uw eigen voorspellende webservice gebruiken. Zie [Uw eigen voorspellende webservice voor cashflowprognoses maken en gebruiken](#AnchorText).  

De begeleide instelling gebruiken:  

1. Kies in het rolcentrum Accountant onder het diagram **Cashflowprognose** de actie **Begeleide instelling openen**.  
2. Vul de velden in elke stap van de begeleiding in.  
3. Kies op de startpagina **Cashflowprognose** boven het diagram en kies vervolgens **Prognose herberekenen**.  

Een handmatig proces gebruiken:  

1. Zoek in het rolcentrum Accountant naar **Cashflowinstellingen** en klik vervolgens op de gerelateerde koppeling.  
2. Vouw het sneltabblad **Cortana Intelligence** uit en kies vervolgens het selectievakje **Cortana Intelligence ingeschakeld**.  
3. Kies op de startpagina **Cashflowprognose** boven het diagram en kies vervolgens **Prognose herberekenen**.  

> [!TIP]  
>   Overweeg de lengte van de perioden die de service in de berekeningen gebruikt. Hoe meer gegevens u biedt, hoe nauwkeuriger de voorspellingen zullen zijn. Let ook op grote variaties in perioden. Deze zijn ook van invloed op voorspellingen. Als Cortana Intelligence niet voldoende gegevens vindt of de gegevens sterk variëren, doet de service geen voorspelling.  

## <a name="AnchorText"> </a>Uw eigen voorspellende webservice voor cashflowprognoses maken en gebruiken
U kunt uw eigen voorspellende webservice maken op basis van een openbaar model met de naam **Prognosemodel voor Microsoft Dynamics 365 Business edition**. Dit voorspellende model is online beschikbaar in de Cortana Intelligence-galerie. Ga als volgt te werk om het model te gebruiken:  

1. Open een browser en ga naar de [Cortana Intelligence-galerie](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Zoek naar **Prognosemodel voor Microsoft Dynamics 365 Business edition** en open het model in Azure Machine Learning Studio.  
3. Gebruik het Microsoft-account om u aan te melden voor een werkruimte en kopieer vervolgens het model.  
4. Voer het model uit en publiceer het als een webservice.  
5. Noteer de API-URL en de API-sleutel. U kunt deze aanmeldingsgegevens voor een cashflowinstelling gebruiken.  
6. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Cashflowinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
7. Vouw het sneltabblad **Cortana Intelligence** uit en vul de velden in.  

## <a name="see-also"></a>Zie ook
[Cashflow in uw bedrijf analyseren](finance-analyze-cash-flow.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

