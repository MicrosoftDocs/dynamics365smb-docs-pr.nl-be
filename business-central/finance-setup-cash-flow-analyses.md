---
title: Cashflowanalyse instellen
description: 'Gebruik de grafieken in het rolcentrum Accountant om de geldstroom in uw bedrijf te helpen analyseren, inclusief kosten en inkomsten, liquiditeit en kasontvangsten minus contante betalingen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="setting-up-cash-flow-analysis"></a>Cashflowanalyse instellen

Als u wat hulp wilt bij het bepalen wat u met uw contant geld moet doen, kunt de diagrammen bekijken in het rolcentrum Accountant:

* **Cashcyclus**  
* **Inkomsten en uitgaven**  
* **Cashflow**  
* **Cashflowprognoses**  

In dit artikel wordt beschreven waar de gegevens in de diagrammen van afkomstig zijn en, indien nodig, wat u moet doen als u de diagrammen wilt gaan gebruiken.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>De diagrammen Cashcyclus en Inkomsten en uitgaven

De diagrammen **Cashcyclus** en **Inkomsten en uitgaven** zijn gereed voor gebruik, gebaseerd op de rekeningschema's en financiële rapporten. De rekeningen bevinden zich waar de gegevens uit afkomstig zijn en met financiële rapporten wordt de relatie tussen verkopen en tegoeden berekend. Er worden enkele rekeningen en financiële rapporten verschaft. U kunt deze ongewijzigd gebruiken, ze aanpassen en nieuwe toevoegen. Als u grootboekrekeningen toevoegt aan uw rekeningschema, bijvoorbeeld door deze te importeren uit QuickBooks, moet u een koppeling maken naar de rekeningen op de pagina **Financiële rapporten** voor de volgende rapporten:

| Naam van financieel rapport | Waar het wordt gebruikt |
| --- | --- |
| **I_CACYCLE** |Cashcyclus |
| **I_CASHFLOW** |Cashflow |
| **I_INCEXP** |Inkomsten en uitgaven |
| **I_MINTRIAL** |Als resultatenrekening als u het rekeningschema niet gebruikt |

> [!NOTE]
> Het is raadzaam de berekeningen te behouden die voor het financiële rapport worden verschaft.

Voer rekeningen in het veld **Samentelling** voor **Totale opbrengsten**, **Totale tegoeden**, **Totaal schulden** en **Totale voorraad** in. Als u aan een reeks rekeningen wilt toewijzen, voert u de rekeningnummers in, gescheiden door ".." zoals in **1111..4444**. U kunt ook toewijzen aan specifieke rekeningen door de rekeningnummers in te voeren, gescheiden door een verticaal streepje zoals in **2222|3333|5555**.  

> [!TIP] 
> Controleer uw koppeling door de actie **Overzicht** te kiezen.  

## <a name="set-up-the-cash-flow-chart"></a>Het cashflowdiagram instellen

Het cashflowdiagram is gebaseerd op:  

* Een diagram van cashflowrekeningen.
* Een of meer cashflowinstellingen. Met deze instellingen worden de rekeningen opgegeven die moeten worden gebruikt voor grootboek, inkoop, verkoop, services en vaste activa.  

Om u te helpen aan de slag te gaan zijn er enkele rekeningen en cashflowinstellingen verschaft. U kunt deze toevoegen, veranderen of verwijderen.  

Als u de rekeningen wilt instellen, zoekt u naar **Cashflowrekeningschema**, kiest u de koppeling en vult u vervolgens de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Herhaal deze stappen voor **Cashflowinstellingen**.

## <a name="set-up-cash-flow-forecasts"></a>Cashflowprognoses instellen

In het diagram **Cashflowprognose** worden cashflowrekeningen, cashflowinstellingen en cashflowprognoses gebruikt. Sommige worden verschaft, maar u kunt die van uzelf instellen met behulp van een begeleide instelling. Met de gids kunt u zaken opgeven zoals het aantal keren dat de prognose moet worden bijgewerkt, op welke rekeningen de prognose moet worden gebaseerd, wanneer u belastingen betaalt en of [Azure AI](https://azure.microsoft.com/overview/ai-platform/) moet worden ingeschakeld.  

Cashflowprognoses kunnen Azure AI gebruiken om een uitgebreidere prognose op te stellen. De verbinding met Azure AI is al voor u ingesteld. U hoeft het alleen in te schakelen. Wanneer u zich bij [!INCLUDE[prod_short](includes/prod_short.md)] aanmeldt, verschijnt er een melding in een blauwe balk en wordt er een koppeling verschaft naar de standaardcashflowinstellingen. De melding wordt slechts eenmaal weergegeven. Als u de melding sluit, maar vervolgens besluit Azure AI in te schakelen, kunt u de begeleide instelling gebruiken of een handmatig proces.  

> [!NOTE]
>
> U kunt ook uw eigen voorspellende webservice gebruiken. Zie [Uw eigen voorspellende webservice voor cashflowprognoses maken en gebruiken](#AnchorText).  

De begeleide instelling gebruiken:  

1. Kies in het rolcentrum Accountant onder het diagram **Cashflowprognose** de actie **Begeleide instelling openen**.
2. Vul de velden in elke stap van de begeleiding in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Ga terug naar het rolcentrum Accountant en kies de actie **Prognose herberekenen** onder het diagram **Cashflowprognose**.

Een handmatig proces gebruiken:  

1. Kies in het rolcentrum Accountant het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Cashflowinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vouw het sneltabblad **Azure AI** uit en kies vervolgens het veld **Azure AI ingeschakeld**.
3. Ga terug naar het rolcentrum Accountant en kies de actie **Prognose herberekenen** onder het diagram **Cashflowprognose**.

> [!TIP]  
> Overweeg de lengte van de perioden die de service in de berekeningen gebruikt. Hoe meer gegevens u biedt, hoe nauwkeuriger de voorspellingen zullen zijn. Let ook op grote variaties in perioden. Deze zijn ook van invloed op voorspellingen. Als Azure AI niet voldoende gegevens vindt of de gegevens sterk variëren, doet de service geen voorspelling.  

## <a name="design-details"></a>Ontwerpdetails

Abonnementen voor [!INCLUDE[prod_short](includes/prod_short.md)] komen met toegang tot verschillende voorspellende webservices in alle regio's waar [!INCLUDE[prod_short](includes/prod_short.md)] beschikbaar is. Lees meer in de licentiehandleiding voor Microsoft Dynamics 365 Business Central. De gids kan worden gedownload op de [Business Central](https://dynamics.microsoft.com/business-central/overview/)-website.

Deze webservices zijn staatloos, wat betekent dat ze gegevens alleen gebruiken om voorspellingen op aanvraag te berekenen. Ze slaan geen gegevens op.

> [!NOTE]
>
> U kunt ook uw eigen voorspellende webservice gebruiken in plaats van de onze. Zie [Uw eigen voorspellende webservice voor cashflowprognoses maken en gebruiken](#AnchorText).

### <a name="data-required-for-forecast"></a>Vereiste gegevens voor prognoses

Om voorspellingen te doen over toekomstige inkomsten en uitgaven hebben webservices historische gegevens nodig van vorderingen, schulden en belastingen.

#### <a name="receivables"></a>Tegoeden

Velden **Vervaldatum** en **Bedrag (LV)** van de pagina **Klantenposten**, waar:

* Het documenttype is *Factuur* of *Creditnota*.
* De vervaldatum ligt tussen de datum die wordt berekend op basis van de waarden in de velden **Historische perioden** en **Periodesoort** op de pagina **Cashflowinstellingen** en de werkdatum.

Voordat de voorspellende webservice wordt gebruikt, comprimeert [!INCLUDE[prod_short](includes/prod_short.md)] transacties op **Vervaldatum**, gebaseerd op de waarde in het veld **Periodesoort** op de pagina **Cashflowinstellingen**.

#### <a name="payables"></a>Schulden

Velden **Vervaldatum** en **Bedrag (LV)** op de pagina **Leveranciersposten**, waar:

* Het documenttype is *Factuur* of *Creditnota*.
* De vervaldatum ligt tussen de datum die wordt berekend op basis van waarden in de velden **Historische perioden** en **Periodesoort** op de pagina **Cashflowinstellingen** en de werkdatum.

Voordat de voorspellende webservice wordt gebruikt, comprimeert [!INCLUDE[prod_short](includes/prod_short.md)] transacties op **Vervaldatum**, gebaseerd op de waarde in het veld **Periodesoort** op de pagina **Cashflowinstellingen**.

#### <a name="tax"></a>Belasting

Velden **Documentdatum** en **Bedrag (LV)** op de pagina **Btw-posten**, waar:

* Het documenttype is *verkoop*.
* De documentdatum ligt tussen de datum die wordt berekend op basis van de waarden in de velden **Historische perioden** en **Periodesoort** op de pagina **Cashflowinstellingen** en de werkdatum.

Voordat de voorspellende webservice wordt gebruikt, comprimeert [!INCLUDE[prod_short](includes/prod_short.md)] transacties op **Documentdatum**, gebaseerd op de waarde in het veld **Periodesoort** op de pagina **Cashflowinstellingen**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a>Uw eigen voorspellende webservice voor cashflowprognoses maken en gebruiken

U kunt uw eigen voorspellende webservice maken op basis van een openbaar model met de naam **Prognosemodel voor Business Central**. Dit voorspellend model is online beschikbaar in de Azure AI-galerie. Ga als volgt te werk om het model te gebruiken:  

1. Open een browser en ga naar de [Azure AI-galerie](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Zoek naar **Prognosemodel voor Microsoft Business Central** en open het model in Microsoft Azure Machine Learning Studio.  
3. Gebruik het Microsoft-account om u aan te melden voor een werkruimte en kopieer vervolgens het model.  
4. Voer het model uit en publiceer het als een webservice.  
5. Noteer de API-URL en de API-sleutel. U kunt deze aanmeldingsgegevens voor een cashflowinstelling gebruiken.  
6. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Cashflowinstellingen** in en kies vervolgens de gerelateerde koppeling.  
7. Vouw het sneltabblad **Azure AI** uit en vul vervolgens de velden in, inclusief de API-URL en API-sleutel die zijn geleverd door Azure Machine Learning Studio. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. Kies in het rolcentrum Accountant de actie **Prognose herberekenen** onder het diagram **Cashflowprognose**.

## <a name="see-also"></a>Zie ook

[Cashflow in uw bedrijf analyseren](finance-analyze-cash-flow.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
