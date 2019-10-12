---
title: Kostenposten overbrengen en boeken | Microsoft Docs
description: Voordat u kostenverdelingen definieert, moet u begrijpen waar kostenposten vandaankomen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5391aa089e24dd4ed25e2df4979491433034697e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301618"
---
# <a name="transferring-and-posting-cost-entries"></a>Kostenposten overbrengen en boeken
Voordat u kostenverdelingen definieert, moet u begrijpen hoe kostenposten uit de volgende bronnen worden opgehaald:  

-   Automatische overdracht van grootboekposten.  
-   Handmatig kostenboeking voor zuivere kostenposten, interne heffingen en handmatige toewijzingen.  
-   Automatisch toegewezen boekingen voor werkelijke kosten.  
-   Overdracht van budgetposten naar werkelijke posten.

## <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Criteria voor het overbrengen van grootboekposten naar kostenposten
Het is belangrijk dat u een goed begrip heeft van de criteria voor het overbrengen van grootboekposten naar kostenposten. Tijdens de overdracht maakt de batchverwerking **Grootboekposten overbrengen naar kostprijsboekhouding** gebruik van de volgende criteria om te bepalen of en hoe de grootboekposten worden overgebracht.  

Grootboekposten worden overgebracht in de volgende gevallen:  

-   De posten hebben dimensiewaarden die een bijbehorende kostenplaats of kostenobject hebben.  
-   De posten hebben dimensiewaarden die een bijbehorende kostenplaats en kostenobject hebben. Voor deze posten heeft de kostenplaats voorrang. Dit voorkomt de situatie waarin een kostensoort zowel in een kostenobject als kostenplaats wordt weergegeven, en daarom twee keer in de statistieken wordt meegeteld.  
-   Het documentnummer in de posten is leeg, en wordt daarom weergegeven met documentnummer 0000 in de kostenposten.  
-   De posten worden overgebracht naar een kostensoort dat gecombineerde posten toestaat, en deze posten worden maandelijks of dagelijks overgebracht als een gecombineerde post.  

Grootboekposten worden niet overgebracht in de volgende gevallen:  

-   De posten hebben dimensiewaarden die geen bijbehorende kostenplaats of kostenobject hebben.  
-   De posten bevatten een bedrag met waarde nul.  
-   De posten zijn van een grootboekrekening die is verwijderd.  
-   De posten hebben een grootboekrekening die niet van het soort **Resultatenrekening** is.  
-   De posten hebben een grootboekrekening waaraan geen kostensoort is toegewezen.  
-   De posten hebben een boekingsdatum vóór de **Begindatum voor GB-overdracht**.  
-   De posten zijn geboekt met een ultimodatum. Dit zijn meestal de posten die een negatief effect hebben op het saldo van de resultatenrekening aan het einde van het jaar.

## <a name="transferring-general-ledger-entries-to-cost-entries"></a>Grootboekposten overbrengen naar kostenposten.
U kunt grootboekposten overbrengen naar kostenposten.  

Voordat u begint met de bewerking om grootboekposten over te brengen naar kostenposten, moet u de overdracht voorbereiden zodat wordt voorkomen dat u fouten handmatig moet corrigeren die tijdens de boeking worden gemaakt.  

### <a name="to-prepare-the-transfer"></a>De overdracht voorbereiden  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van kostprijsboekhouding** in en kies vervolgens de gerelateerde koppeling.  
2.  Controleer op de pagina **Instelling kostprijsboekhouding** of het veld **Begindatum voor GB-overdracht** op de juiste waarde is ingesteld.  
3.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostensoortschema** in en kies vervolgens de gerelateerde koppeling.  
4.  Controleer op de pagina **Kostensoortkaart** of het veld **Grootboekrekeningbereik** juist gekoppeld is voor elke kostensoort om posten uit het grootboek te halen.  
5.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
6.  Voor elke gewenste grootboekrekening controleert u op de pagina **Grootboekrekening** of het veld **Nr. kostensoort** juist is gekoppeld aan een kostensoort. Zie [Kostenboekhouding instellen](finance-set-up-cost-accounting.md) voor meer informatie.  
7.  Controleer of alle relevante grootboekposten over dimensiewaarden beschikken die overeenkomen met een kostenplaats en een kostenobject.  

### <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Grootboekposten overbrengen naar kostenposten.  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekposten overbrengen naar kostprijsboekhouding** in en kies vervolgens de gerelateerde koppeling.  
2.  Klik op **Ja** om de overdracht te starten. Tijdens de bewerking worden alle grootboekposten overgebracht die niet al zijn overgebracht.  

    Tijdens de overdracht worden door het proces verbindingen in de posten in de tabel **Kostenpost** en de tabel **Kostenregister** gemaakt. Hierdoor kunt de bron van de kostenposten traceren.

## <a name="automatic-transfer-and-combined-entries"></a>Automatische overdracht en gecombineerde posten
In kostprijsboekhouding kunt u grootboekposten overbrengen naar een kostensoort door middel van een gecombineerde boeking. U kunt opgeven of een kostensoort gecombineerde posten ontvangt in het veld **Posten combineren** in de definitie van het kostensoort. De volgende tabel beschrijft de verschillende opties.  

|Posten combineren|Description|  
|---------------------|-----------------|  
|Geen|Elke grootboekpost wordt afzonderlijk overgebracht naar het bijbehorende kostensoort.|  
|Dag|Grootboekposten met dezelfde boekingsdatum worden als één post overgeboekt naar de bijbehorende kostensoort.|  
|Maand|Alle grootboekposten in dezelfde kalendermaand worden als één post overgeboekt naar de bijbehorende kostensoort.|  

> [!IMPORTANT]  
>  Als u het selectievakje **Automatisch overdragen van GB** op de pagina **Instelling kostprijsboekhouding** hebt ingeschakeld, wordt de kostprijsboekhouding automatisch bijgewerkt in [!INCLUDE[d365fin](includes/d365fin_md.md)] na elke boeking in het grootboek. Gecombineerde posten zijn niet mogelijk.

## <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Resultaten van het overbrengen van grootboekposten naar kostenposten
Tijdens de overdracht van grootboekposten naar kostenposten, maakt [!INCLUDE[d365fin](includes/d365fin_md.md)] verbindingen aan in de posten in de tabel **Grootboekpost**, de tabel **Kostenpost** en de tabel **Kostenregister** om de verbindingen tussen kostenposten en grootboekposten te kunnen traceren.  

### <a name="general-ledger-entries"></a>Grootboekposten  
Voor elke grootboekpost die wordt overgebracht naar kostprijsboekhouding, vult [!INCLUDE[d365fin](includes/d365fin_md.md)] de kosten in het veld **Postnr.** in.  

### <a name="cost-entries"></a>Kostenposten  
Voor elke kostenpost slaat [!INCLUDE[d365fin](includes/d365fin_md.md)] het nummer van de bijbehorende grootboekpost op in het veld **Grootboekpostnr.** in de tabel **Kostenpost**.  

Voor gecombineerde kostenposten slaat [!INCLUDE[d365fin](includes/d365fin_md.md)] het nummer van de laatste grootboekpost op; dit is de post met het hoogste nummer.  

Het veld **Grootboekrekening** in de tabel **Kostenpost** bevat het nummer van de grootboekrekening waaruit de kostenpost afkomstig is.  

Voor enkele kostenposten wordt de boekingstekst door [!INCLUDE[d365fin](includes/d365fin_md.md)] uit de grootboekpost overgebracht naar het tekstveld **Beschrijving**. Voor gecombineerde posten laat dit tekstveld zien dat deze posten als gecombineerde posten zijn overgebracht. Voor een gecombineerde post voor de maand oktober 2013 luidt de tekst mogelijk bijvoorbeeld **Gecombineerde posten, oktober 2013**.  

### <a name="cost-register"></a>Kostenregister  
In de tabel **Kostenregister**, wordt door [!INCLUDE[d365fin](includes/d365fin_md.md)] een post gemaakt met de bronoverdracht van het grootboek. Door de post worden de eerste en laatste nummers van de overgebrachte grootboekposten vastgelegd, evenals de eerste en laatste nummers van de kostenposten die zijn gemaakt.

## <a name="see-also"></a>Zie ook  
 [Kostprijsboekhouding](finance-about-cost-accounting.md)   
 [Kostenboekhouding instellen](finance-set-up-cost-accounting.md)   
 [Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)   
 [Kosten verantwoorden](finance-manage-cost-accounting.md)
