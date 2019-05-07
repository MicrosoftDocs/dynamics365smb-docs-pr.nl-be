---
title: Klantbetalingen via betalingsservices inschakelen | Microsoft Docs
description: Maak het makkelijker voor klanten om facturen te betalen, door betalingsservices in te schakelen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e5d4d9fd0c6857c22f2b4c929a6e6ed528cadf26
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931688"
---
# <a name="enable-customer-payments-through-payment-services"></a>Klantbetalingen via betalingsservices inschakelen
Als alternatief voor het innen van betalingen door middel van bankoverschrijving of creditcards kunt u klanten laten betalen via hun account door middel van betalingsservices zoals Microsoft Pay, PayPal of WorldPay.  

Nadat u een betalingsservice hebt ingeschakeld in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt een koppeling naar de service beschikbaar op verkoopdocumenten die u per e-mail naar uw klanten verzendt. De klanten kunnen met de koppeling naar de betalingsservice gaan en de factuur betalen, rechtstreeks vanuit het verkoopdocument. Als u de koppeling niet wilt opnemen, bijvoorbeeld wanneer een klant met contant geld betaalt, kunt u de betalingsservice uit de factuur verwijderen voordat u hem boekt.  

De extensies Microsoft Pay, PayPal Payments Standard en WorldPay Payments Standard zijn geïnstalleerd in [!INCLUDE[d365fin](includes/d365fin_md.md)] en u hoeft ze alleen maar in te schakelen.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Een betalingsservice inschakelen in [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsservices** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Betalingsservices** de actie **Nieuw**.  
3. Selecteer de betalingsservice en sluit vervolgens de pagina.  
4. Kies op de pagina **Betalingsservices** de actie **Instellingen**.  
5. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Sluit de pagina.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Een betalingsservice selecteren op een verkoopfactuur
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de verkoopfactuur die u wilt betalen door middel van de betalingsservice.  
3. Kies in het veld **Betalingsservice** de gewenste betalingsservice.  

    > [!NOTE]  
    > Het veld **Betalingsservice** is alleen beschikbaar als u betalingsservices hebt ingeschakeld.  

## <a name="see-also"></a>Zie ook  
[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
