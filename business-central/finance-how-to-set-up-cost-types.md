---
title: Een kostensoortschema instellen | Microsoft Docs
description: Kostensoortschema's lijken op rekeningschema's in het grootboek.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 2846967648f5c0e0b6015c7990a941642fc27323
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "817037"
---
# <a name="set-up-cost-types"></a>Kostensoorten instellen
Een kostensoortschema lijkt op het rekeningschema in het grootboek. U kunt het kostensoortschema op de volgende manieren instellen:  

-   Geef het kostensoortschema een structuur die vergelijkbaar is met de resultatenrekeningen in het grootboekrekeningschema. Vervolgens kunt u het grootboekrekeningschema overbrengen naar het kostensoortschema. U kunt elke gewenste aanpassing na de overdracht aanbrengen.  
-   Maak nieuwe kostensoortschema's of voeg nieuwe kostensoorten toe aan bestaande kostensoortschema's. U moet elke nieuwe kostensoort afzonderlijk maken.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Het grootboekrekeningschema overbrengen naar het kostensoortschema  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostensoortschema** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Kostensoorten ophalen uit rekeningschema**. Kies in dialoogvenster de knop **Ja** om de overdracht te bevestigen. De functie maakt gebruik van het rekeningschema om een kostensoortschema te maken.  

    Het kostensoortschema bevat nu alle resultatenrekeningen in het grootboek inclusief koppen en subtotalen. U kunt het kostensoortschema zo nodig wijzigen. U kunt bijvoorbeeld dubbele kostensoorten verwijderen.  

    > [!IMPORTANT]  
    >  De functie **Kostensoorten registreren in rekeningschema** werkt de relatie tussen het rekeningschema en het kostensoortschema bij. Het veld **Nr.** wordt ingevuld en gecontroleerd om ervoor te zorgen dat iedere grootboekrekening slechts aan één kostensoort is gerelateerd. De functie wordt automatisch uitgevoerd voordat deze van grootboekposten naar kostprijsboekhouding wordt overgebracht.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Nieuwe kostensoorten instellen op de pagina Kostensoortschema  
1.  Open de pagina **Kostensoortschema** in de bewerkmodus.  
2.  Vul de velden indien nodig in zoals beschreven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  U kunt kostensoorten instellen en onderhouden op de pagina **Kostensoortkaart** of op de pagina **Kostensoortschema**. In deze procedure stelt u kostensoorten op de pagina **Kostensoortschema** in.

3.  Nadat u alle kostensoorten hebt gemaakt, kiest u de actie **Kostensoorten inspringen**. Kies in het dialoogvenster de knop **Ja**.  
4.  Koppel het nieuwe kostensoort aan de corresponderende grootboekrekening.  

    > [!IMPORTANT]  
    >  Als u definities hebt ingevoerd in de **Samentelling**-velden voor het regelsoort **Eindtotaal** voordat u de functie **Kostensoorten inspringen** uitvoert, moet u de definities opnieuw invoeren omdat de functie de waarden in alle velden **Eindtotaal** overschrijft.  

## <a name="to-update-cost-types"></a>Kostensoorten bijwerken  
1.  Op de pagina **Instelling kostprijsboekhouding** selecteert u of het kostensoortschema automatisch wilt laten bijwerken als het rekeningschema wordt gewijzigd.  
2.  In het veld **Grootboekrekening afstemmen** kunt u kiezen uit de volgende opties.  

- in **Geen uitlijning** - er wordt geen overeenkomstige wijziging in het kostensoortschema doorgevoerd als u het rekeningschema wijzigt.  
- **Geen uitlijning** - er wordt een overeenkomstige wijziging doorgevoerd in het kostensoortschema als u het rekeningschema wijzigt.  
- **Vragen** - wanneer u een wijziging aanbrengt in het rekeningschema krijgt u een bericht waarin u wordt gevraagd of u de overeenkomstige wijziging in het kostensoortschema wilt maken.  

## <a name="see-also"></a>Zie ook  
[Kosten verantwoorden](finance-manage-cost-accounting.md)  
[Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldi tussen kostensoort, kostenplaats en kostenobject](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Kostenboekhouding instellen](finance-set-up-cost-accounting.md)   
[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)   
[Kostprijsboekhouding](finance-about-cost-accounting.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
