---
title: Een klantenkaart maken om nieuwe klanten registreren | Microsoft Docs
description: "Beschrijft hoe u een klantenkaart maakt om informatie te registreren over elke nieuwe klant of cliënt aan wie u verkoopt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ca4f1880e7a95eaf945d48ca2cdd7b3d5f80a621
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-register-new-customers"></a>Procedure: Nieuwe klanten registreren
Klanten zijn de bron van uw inkomsten. U moet elke klant aan wie u verkoopt registreren als een klantenkaart. Klantenkaarten bevatten de informatie die is vereist om producten aan de klant te verkopen. Zie [Procedure: Verkopen factureren](sales-how-invoice-sales.md) en [Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md) voor meer informatie.  

Voordat u nieuwe klanten kunt vastleggen, moet u verschillende verkoopcodes instellen waaruit u kunt selecteren bij het invullen van klantenkaarten. Zie [Verkopen instellen](sales-setup-sales.md) voor meer informatie.

> [!NOTE]  
>   Als er klantsjablonen voor verschillende klantsoorten bestaan, wordt een venster weergegeven wanneer u een nieuwe klantenkaart maakt waar u een geschikte sjabloon kunt selecteren. Als er slechts één klantensjabloon bestaat, gebruiken nieuwe klantenkaarten altijd deze sjabloon.

## <a name="to-create-a-new-customer-card"></a>Een nieuwe klantenkaart maken
1. Kies op de startpagina de actie **Klanten** om de lijst met bestaande klanten te openen.  
2. Kies in het venster **Klanten** de actie **Nieuw**.

    Als er slechts één klantensjabloon bestaat, wordt vervolgens een nieuwe klantenkaart geopend waarin sommige velden zijn ingevuld met informatie van de sjabloon.

    Als er meer dan één klantensjabloon bestaat, wordt er een venster geopend waarin u een klantensjabloon kunt selecteren. In dat geval volgt u de volgende twee stappen.
3. Kies in het venster **Selecteer een sjabloon voor een nieuwe klant** de sjabloon die u wilt gebruiken voor de nieuwe klantenkaart.
4. Kies de knop **Ok**. Een nieuwe klantenkaart wordt geopend waarin in sommige velden informatie uit de sjabloon is ingevuld.  
5. Ga indien nodig door met het invullen of wijzigen van velden op de klantenkaart. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Op het sneltabblad **Verkoopprijzen** kunt u speciale prijzen of kortingen weergeven die u voor de klant verleent als aan bepaalde criteria, zoals artikel, minimaal orderaantal of einddatum, wordt voldaan. Elke rij vertegenwoordigt een speciale prijs of regelkorting. Elke kolom vertegenwoordigt een criterium dat moet worden toegepast om de speciale prijs te garanderen die u invoert in het veld **Eenheidsprijs** of de regelkorting die u invoert in het veld **Regelkorting %**. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).

De klant is nu geregistreerd en de klantenkaart is klaar om voor verkoopdocumenten te worden gebruikt.

Als u deze klantenkaart als sjabloon wilt gebruiken wanneer u nieuwe klantenkaarten maakt, kunt u deze opslaan als een sjabloon. Zie de volgende onderwerpen voor meer informatie.

## <a name="to-save-the-customer-card-as-a-template"></a>De klantenkaart als sjabloon opslaan
1. Kies in het venster **Klantenkaart** de actie **Opslaan als sjabloon**. Het venster **Klantensjabloon** opent de weergave van de klantenkaart als sjabloon.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**. Het venster **Dimensiesjablonen** wordt geopend en toont alle dimensiecodes die voor de klant zijn ingesteld.
4. Bewerk of typ dimensiecodes die van toepassing zijn op nieuwe klantenkaarten die worden gemaakt met de sjabloon.  
5. Wanneer u de nieuwe klantensjabloon hebt voltooid, kiest u de knop **OK**.

De klantensjabloon wordt toegevoegd aan de lijst met klantensjabloon, zodat u deze kunt gebruiken om nieuwe klantenkaarten te maken.

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)    
[Verkopen instellen](sales-setup-sales.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

