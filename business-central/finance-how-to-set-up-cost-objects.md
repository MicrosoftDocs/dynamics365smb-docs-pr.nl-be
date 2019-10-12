---
title: Kostenobjecten instellen | Microsoft Docs
description: Leer hoe u kostenobjecten instelt. Kostenobjecten lijken op dimensies voor het grootboek.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: ae2ca5b4c6f63a004d42c2ae1ef9f0efa95dd02c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306040"
---
# <a name="set-up-cost-objects"></a>Kostenobjecten instellen
Kostenobjecten zijn projecten, producten of diensten van een bedrijf. Het schema van kostenobjecten is vergelijkbaar met de dimensiegegevens voor het grootboek. U kunt het schema van kostenobjecten op de volgende manieren instellen:  

* Door de dimensiewaarden in het grootboek over te brengen naar het schema van kostenobjecten. U kunt elke gewenste aanpassing na de overdracht aanbrengen.  
* Door een nieuw schema van kostenobjecten te maken dat onafhankelijk is van het grootboek of door een nieuw kostenobject toe te voegen aan een bestaand schema van kostenobjecten. U moet elk kostenobject afzonderlijk maken.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Door de dimensiewaarden vanuit het grootboek over te brengen naar het schema van kostenobjecten.  
1.  Stel een dimensie als kostenobjectdimensie in op de pagina **CA-dimensies bijwerken**. Alleen de waarden uit deze dimensie worden overgebracht.  
2.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenobjectschema** in en kies vervolgens de gerelateerde koppeling.  
3.  Kies de actie **Kostenobjecten ophalen uit dimensie** om dimensiewaarden over te brengen naar het schema van kostenobjecten. Met deze functie worden de dimensiewaarden die u in stap 1 hebt gedefinieerd overgebracht.  

    > [!NOTE]  
    >  U kunt het veld **Kostenobjectdimensie afstemmen** zo instellen dat hiermee een eenrichtingssynchronisatie van dimensiewaarden uit het grootboek op het schema van kostenobjecten wordt gedefinieerd. U kunt geen synchronisatie van het schema van kostenobjecten met dimensiewaarden uit het grootboek definiëren.  

Het schema van kostenobjecten bevat nu alle opgegeven dimensiewaarden van het grootboek waaronder titels en subtotalen.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Nieuwe kostenobjecten maken op de pagina Kostenobjectschema  
U kunt kostenobjecten instellen en onderhouden op de kaart **Kostenobjectkaart** of op de pagina **Kostenobjectschema**. In deze procedure stelt u kostenobjecten op de pagina **Kostenobjectschema** in.  

1.  Open de pagina **Kostenobjectschema** in de bewerkmodus.  
2.  Voer in het veld **Code** de kostenobjectcode in. Alle kostenobjecten moeten een code hebben.  
3.  Voer in het veld **Naam** de naam van het kostenobject in.  
4.  Kies de vervolgkeuzepijl in het veld **Regelsoort** om het doel van het kostenobject aan te geven.  

    * Voor kostenobjecten van het regelsoort **Totaal** vult u het veld **Totaal van/tot** in. Gebruik de operator **of**, die uit een verticale lijn (**&#124;**) bestaat om bereiken voor kostenobjecten in te stellen.  
    * Voor kostenobjecten van het regelsoort **Eindtotaal** wordt dit veld automatisch ingevuld wanneer u de inspringfunctie gebruikt.  
5.  Vul het veld **Sorteervolgorde** in.  
6.  Kies de volgende lege regel om een nieuw kostenobject te maken en herhaal vervolgens stap 2 tot en met 5.  
7.  Nadat u alle kostenobjecten hebt ingesteld, kiest u de actie **Kostenobjecten inspringen**. Kies de knop **Ja**.  

> [!IMPORTANT]  
>  Als u definities in de velden **Totaal van/tot** voor de kostenobjecten **Eindtotaal** hebt ingevoerd voordat u de inspringfunctie uitvoert, moet u deze opnieuw invoeren. De functie overschrijft de waarden in alle velden **Eindtotaal**.  

## <a name="see-also"></a>Zie ook  
[Kosten verantwoorden](finance-manage-cost-accounting.md)  
[Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldi tussen kostensoort, kostenplaats en kostenobject](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Kostenboekhouding instellen](finance-set-up-cost-accounting.md)   
[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)   
[Kostprijsboekhouding](finance-about-cost-accounting.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
