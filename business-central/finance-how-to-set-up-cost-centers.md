---
title: Kostenplaatsen instellen | Microsoft Docs
description: Kostenplaatsen zijn afdelingen die verantwoordelijk zijn voor kosten en opbrengsten. Het schema van kostenplaatsen is vergelijkbaar met de dimensiegegevens voor het grootboek.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 92d3e28fc9d7dc5aa9b2c5e25df6a0c965ab725d
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cost-centers"></a>Kostenplaatsen instellen
Kostenplaatsen zijn afdelingen die verantwoordelijk zijn voor kosten en opbrengsten. Het schema van kostenplaatsen is vergelijkbaar met de dimensiegegevens voor het grootboek. U kunt het schema van kostenplaatsen op de volgende manieren instellen:  

-   Door de dimensiewaarden in het grootboek over te brengen naar het schema van kostenplaatsen. U kunt elke gewenste aanpassing na de overdracht aanbrengen.  
-   Door een nieuw schema van kostenplaatsen te maken dat onafhankelijk is van het grootboek of door een nieuwe kostenplaats toe te voegen aan een bestaand schema van kostenplaatsen. U moet elke kostenplaats afzonderlijk maken.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Dimensiewaarden in het grootboek overbrengen naar het schema van kostenplaatsen  
1.  Stel een dimensie als kostenplaats in met het venster **Dimensies kostprijsboekhouding bijwerken**. Alleen de waarden uit deze dimensie worden overgebracht.  
2.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Kostenplaatsschema** in en klik vervolgens op de gerelateerde koppeling.  
3.  Op het tabblad **Acties** in de groep **Functies** kiest u **Kostenplaatsen ophalen uit dimensie** om dimensiewaarden over te brengen naar het schema van kostenplaatsen. Met deze functie worden de dimensiewaarden die u in stap 1 hebt gedefinieerd overgebracht.  

    > [!NOTE]  
    >  U kunt het veld **Kostenplaatsdimensie afstemmen** zo instellen dat hiermee een eenrichtingssynchronisatie van dimensiewaarden uit het grootboek op het kostenplaatsschema wordt gedefinieerd. U kunt geen synchronisatie van het schema van kostenplaatsen met dimensiewaarden uit het grootboek definiëren.  

Het schema van kostenplaatsen bevat nu alle opgegeven dimensiewaarden van het grootboek waaronder titels en subtotalen.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a>Nieuwe kostenplaatsen maken in het venster Kostenplaatsschema  
U kunt kostenplaatsen instellen en onderhouden op de kaart **Kostenplaatskaart** of in het venster **Kostenplaatsschema**. In deze procedure stelt u kostenplaatsen in het venster **Kostenplaatsschema** in.  

1. Open het venster **Kostenplaatsschema** in de bewerkmodus.  
2. Voer in het veld **Code** de kostenplaatscode in. Alle kostenplaatsen moeten een code hebben.  
3. Voer in het veld **Naam** de naam van de kostenplaats in.  
4. Kies de vervolgkeuzepijl in het veld **Regelsoort** om het doel van de kostenplaats aan te geven.  

    - Voor kostenplaatsen van het soort **Totaal** moet u het veld **Samentelling** invullen. Gebruik de operator **of**, die uit een verticale lijn (**&#124;**) bestaat om bereiken voor kostenplaatsen in te stellen.  
    - Voor kostenplaatsen van het regelsoort **Eindtotaal** wordt dit veld automatisch ingevuld wanneer u de inspringfunctie gebruikt.  
5.  Vul de velden **Sorteervolgorde** en **Kostensubtype** in.  
6.  Kies de volgende lege regel om een nieuwe kostenplaats te maken en herhaal vervolgens stap 2 tot en met 5.  
7.  Nadat u alle kostenplaatsen hebt ingesteld, kiest u de actie **Kostenplaatsen inspringen**. Kies de knop **Ja**.  

> [!IMPORTANT]  
>  Als u definities in de velden **Samentelling** voor de kostenplaatsen **Eindtotaal** hebt ingevoerd voordat u de inspringfunctie uitvoerde, moet u deze opnieuw invoeren. De functie overschrijft de waarden in alle velden **Eindtotaal**.  

## <a name="see-also"></a>Zie ook  
[Kosten verantwoorden](finance-manage-cost-accounting.md)  
[Kostenboekhouding instellen](finance-set-up-cost-accounting.md)   
[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)   
[Kostprijsboekhouding](finance-about-cost-accounting.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

