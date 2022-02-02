---
title: Een leverancierskaart maken om nieuwe leveranciers te registreren (bevat video)
description: In dit onderwerp leert u hoe u een leverancierskaart maakt om een nieuwe leverancier te registreren en leverancierskaarten als sjabloon op te slaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: 26, 27, 34, 786, 1379, 1385, 1386, 1628
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: cad131feb9232bbf476b7444ebeb2dd1b9170647
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953371"
---
# <a name="register-new-vendors"></a>Nieuwe leveranciers registreren

Leveranciers leveren de producten die u verkoopt. Elke leverancier van wie u inkoopt, moet als een leverancierkaart zijn geregistreerd.

Voordat u nieuwe leveranciers kunt vastleggen, moet u verschillende inkoopcodes instellen waaruit u kunt selecteren wanneer u leverancierskaarten invult. Wanneer alle vereiste stamgegevens zijn gemaakt, kunt u aanvullende gegevens voor de leverancier configureren, zoals het toekennen van een prioriteit aan de leverancier voor betalingsdoeleinden en u kunt artikelen vermelden die deze leverancier en andere leveranciers kunnen leveren. Een andere reeks instellingen die u kunt opgeven, zijn de overeenkomsten met betrekking tot kortingen, prijzen en betalingswijzen. Zie voor meer informatie [Inkoop instellen](purchasing-setup-purchasing.md).

Leverancierskaarten bevatten de informatie die is vereist om producten van de leverancier te kunnen kopen. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md) en [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

> [!NOTE]  
> Als leveranciersjablonen voor verschillende leveranciersoorten bestaan, wordt een pagina automatisch weergegeven wanneer u een nieuwe leverancierskaart maakt, van waaruit u een geschikte leveranciersjabloon kunt selecteren. Als er slechts één leveranciersjabloon bestaat, gebruiken nieuwe leverancierkaarten altijd deze sjabloon.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Nieuwe leveranciers toevoegen
U kunt nieuwe leveranciers handmatig toevoegen door de velden op de pagina **Leverancierskaart** in te vullen of u kunt sjablonen gebruiken die vooraf gedefinieerde informatie bevatten. U kunt bijvoorbeeld een sjabloon maken voor verschillende typen leveranciersprofielen. Het gebruik van sjablonen bespaart tijd bij het toevoegen van nieuwe leveranciers en helpt ervoor te zorgen dat de informatie elke keer correct is. Als u sjablonen voor meer dan één type leverancier maakt, kunt u de sjabloon kiezen die u wilt gebruiken wanneer u een leverancier toevoegt. Als u slechts één sjabloon maakt, wordt deze voor alle nieuwe leveranciers gebruikt. Nadat u een sjabloon heeft gemaakt, kunt u de actie **Sjabloon toepassen** gebruiken om deze toe te passen op een of meer geselecteerde leveranciers. Om een sjabloon te maken vult u de informatie in die u opnieuw wilt gebruiken op de pagina Leverancierskaart en slaat u deze vervolgens op als sjabloon. Zie voor meer informatie [De pagina Leverancierskaart als sjabloon opslaan](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Het kan handig zijn om de pagina **Leverancierssjabloon** te personaliseren wanneer u een sjabloon maakt. U wilt bijvoorbeeld een veld toevoegen dat nog niet op de pagina wordt weergegeven. Zie [Uw werkruimte personaliseren](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner) voor meer informatie.

U kunt ook een leverancier maken op basis van een contact. Zie voor meer informatie [Een klant, leverancier, werknemer of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Een nieuwe leverancier maken

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Als het factuuradres dat voor elke factuur van een leverancier wordt gebruikt, niet bij u bekend is, vult u het veld **Leveranciersnr.** niet in. Kies in dat geval het nummer van de factuurleverancier nadat u een inkoopofferte, inkooporder of inkoopkop hebt ingesteld.

De leverancier is nu geregistreerd en de leverancierskaart is klaar om voor inkoopdocumenten te worden gebruikt.

Als u deze leverancierskaart als sjabloon wilt gebruiken wanneer u nieuwe leverancierskaarten maakt, kunt u deze opslaan als leveranciersjabloon. Zie voor meer informatie de sectie [De leverancierskaart als sjabloon opslaan](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Leveranciersinformatie verwijderen en bewerken

U kunt de informatie op leverancierskaarten op elk gewenst moment bewerken. Als u echter een transactie voor een leverancier hebt geboekt, kunt u de kaart niet verwijderen omdat de grootboekposten mogelijk nodig zijn voor controle. Als u leverancierskaarten met grootboekposten wilt verwijderen, neemt u contact op met uw Microsoft-partner om dat via code te doen.

> [!TIP]
> U kunt het IBAN op een bankrekening van een leverancier wijzigen zonder dat de wijziging van invloed is op uw historische journaalposten van krediettransfers. Journaalposten van krediettransfers slaan het IBAN van de ontvanger en het bankrekeningnummer van de ontvanger op die zijn opgegeven in de velden Bankrekening leverancier en Naam ontvanger op de pagina Leverancierskaart toen de boekingen werden gemaakt.


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
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]