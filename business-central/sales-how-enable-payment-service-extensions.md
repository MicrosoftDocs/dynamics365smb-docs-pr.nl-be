---
title: Klantbetalingen via betalingsservices inschakelen
description: 'Maak het makkelijker voor klanten om facturen te betalen, door klantbetalingen via betalingsservices in te schakelen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.search.forms: '1060, 1061, 1062'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="enable-customer-payments-through-payment-services"></a>Klantbetalingen via betalingsservices inschakelen

Als alternatief voor het innen van betalingen door middel van bankoverschrijving of creditcards kunt u klanten laten betalen via hun account door middel van betalingsservices zoals PayPal of WorldPay.  

Nadat u een betalingsservice hebt ingeschakeld in [!INCLUDE[prod_short](includes/prod_short.md)], wordt een koppeling naar de service beschikbaar op verkoopdocumenten die u per e-mail naar uw klanten verzendt. De klanten kunnen met de koppeling naar de betalingsservice gaan en de factuur betalen, rechtstreeks vanuit het verkoopdocument. Als u de koppeling niet wilt opnemen, bijvoorbeeld wanneer een klant met contant geld betaalt, kunt u de betalingsservice uit de factuur verwijderen voordat u hem boekt.  

De extensies , PayPal Payments Standard en WorldPay Payments Standard zijn geïnstalleerd in [!INCLUDE[prod_short](includes/prod_short.md)] en u hoeft ze alleen maar in te schakelen.  

## <a name="to-enable-a-payment-service-in-"></a>Een betalingsservice inschakelen in [!INCLUDE[prod_short](includes/prod_short.md)]

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsservices** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Betalingsservices** de actie **Nieuw**.  
3. Selecteer de betalingsservice en sluit vervolgens de pagina.  
4. Kies op de pagina **Betalingsservices** de actie **Instellingen**.  
5. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Sluit de pagina.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Een betalingsservice selecteren op een verkoopfactuur

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de verkoopfactuur die u wilt betalen door middel van de betalingsservice.  
3. Kies in het veld **Betalingsservice** de gewenste betalingsservice.  

    > [!NOTE]  
    > Het veld **Betalingsservice** is alleen beschikbaar als u betalingsservices hebt ingeschakeld.  

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
