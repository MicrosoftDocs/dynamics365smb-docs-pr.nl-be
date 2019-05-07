---
title: Een leverancierskaart maken om nieuwe leveranciers te registreren | Microsoft Docs
description: Meer informatie over hoe u een leverancierskaart maakt om een nieuwe leverancier te registreren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9f388b788e8788049ee30567972090984063cad1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "930367"
---
# <a name="register-new-vendors"></a>Nieuwe leveranciers registreren
Leveranciers leveren de producten die u verkoopt. Elke leverancier van wie u inkoopt, moet als een leverancierkaart zijn geregistreerd.

Voordat u nieuwe leveranciers kunt vastleggen, moet u verschillende inkoopcodes instellen waaruit u kunt selecteren wanneer u leverancierskaarten invult. Wanneer alle vereiste stamgegevens zijn gemaakt, kunt u aanvullende gegevens voor de leverancier configureren, zoals het toekennen van een prioriteit aan de leverancier voor betalingsdoeleinden en u kunt artikelen vermelden die deze leverancier en andere leveranciers kunnen leveren. Een andere reeks instellingen die u kunt opgeven, zijn de overeenkomsten met betrekking tot kortingen, prijzen en betalingswijzen. Zie voor meer informatie [Inkoop instellen](purchasing-setup-purchasing.md).

Leverancierskaarten bevatten de informatie die is vereist om producten van de leverancier te kunnen kopen. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md) en [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

> [!NOTE]  
>   Als leveranciersjablonen voor verschillende leveranciersoorten bestaan, wordt een pagina automatisch weergegeven wanneer u een nieuwe leverancierskaart maakt, van waaruit u een geschikte leveranciersjabloon kunt selecteren. Als er slechts één leveranciersjabloon bestaat, gebruiken nieuwe leverancierkaarten altijd deze sjabloon.

## <a name="to-create-a-new-vendor-card"></a>Een nieuwe leverancierskaart maken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Leveranciers** de optie **Nieuw**.

    Wanneer er meer dan één leveranciersjabloon bestaat, opent er een pagina waarin u een leveranciersjabloon kunt selecteren. In dat geval volgt u de volgende twee stappen.
3. Kies op de pagina **Selecteer een sjabloon voor een nieuwe leverancier** de sjabloon die u wilt gebruiken voor de nieuwe leverancierskaart.
4. Kies de knop **Ok**. Een nieuwe leverancierskaart wordt geopend met enkele velden ingevuld met informatie uit de sjabloon.
5. Ga door met velden op de leverancierskaart in te vullen of te wijzigen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Als u het factuuradres dat voor elke factuur van een leverancier wordt gebruikt niet kent, vult u het veld **Betaaladres** niet in. Kies in dat geval het nummer van de factuurleverancier nadat u een inkoopofferte, inkooporder of inkoopkop hebt ingesteld.

De leverancier is nu geregistreerd en de leverancierskaart is klaar om voor inkoopdocumenten te worden gebruikt.

Als u deze leverancierskaart als sjabloon wilt gebruiken wanneer u nieuwe leverancierskaarten maakt, kunt u deze opslaan als leveranciersjabloon. Zie de volgende onderwerpen voor meer informatie.

## <a name="to-save-the-vendor-card-as-a-template"></a>De leverancierskaart als sjabloon opslaan
1. Kies op de pagina **Leverancierskaart** de actie **Opslaan als sjabloon**. De pagina **Leveranciersjabloon** opent de weergave van de leverancierkaart als sjabloon.
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**. De pagina **Dimensiesjablonen** geeft alle dimensiecodes weer die voor de leverancier zijn ingesteld.
4. Bewerk of typ dimensiecodes die van toepassing zijn op nieuwe leverancierkaarten die worden gemaakt met de sjabloon.
5. Wanneer u de nieuwe leveranciersjabloon hebt voltooid, kiest u de knop **OK**.  
   De leveranciersjabloon wordt toegevoegd aan de lijst met leveranciersjablonen, zodat u deze kunt gebruiken om nieuwe leverancierskaarten te maken.

## <a name="see-also"></a>Zie ook
[Dubbele records samenvoegen](sales-how-merge-duplicate-records.md)  
[Nummerreeksen maken](ui-create-number-series.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)   
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
