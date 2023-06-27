---
title: Betalingsvoorwaarden instellen
description: Gebruik in de basisversie van Business Central betalingscondities om vervaldatums en betalingskortingen te beheren.
author: edupont04
ms.topic: conceptual
ms.search.form: 4
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-payment-terms"></a>Betalingscondities instellen

Betalingscondities bepalen hoe u omgaat met vervaldata en betalingskortingen. U kunt elk gewenst aantal betalingsconditiecodes instellen en datumformules gebruiken om de betalingscondities te bepalen. Wanneer u zich voor het eerst aanmeldt voor [!INCLUDE [prod_short](includes/prod_short.md)] biedt het demonstratiebedrijf een aantal betaalmethoden aan die bedrijven vaak gebruiken. U kunt er echter zo veel toevoegen als u wilt.  

U kunt betalingscondities aan klanten en leveranciers toewijzen zodat altijd dezelfde condities worden gebruikt op de verkoop- en inkoopdocumenten die u voor hen maakt. Indien nodig kunt u de condities op het verkoop- of inkoopdocument wijzigen, bijvoorbeeld als u wilt dat een bepaalde klant u binnen 7 dagen betaalt in plaats van de standaard 14 dagen. Dit verandert niet de standaardbetalingsconditie die aan de klant is toegewezen. Voor verkoop- en inkoopdocumenten zijn dezelfde betalingscondities beschikbaar.

Als u vervolgens een factuur boekt, berekent [!INCLUDE [prod_short](includes/prod_short.md)] de betalingskortingen op basis van de betalingscondities. De contantkortingsdatum, dat wil zeggen de laatste datum waarop een klant kan betalen en een korting op de betaling kan ontvangen, wordt op dat moment ook berekend.  

Evenzo, wanneer u een creditnota plaatst, berekent [!INCLUDE [prod_short](includes/prod_short.md)] mogelijke betalingskortingen op basis van de betalingscondities. De berekening van contantkortingen op creditnota's gebeurt op dezelfde manier als bij contantkortingen op facturen. Als u een creditnota met een factuur vereffent, wordt het bedrag van de eventuele contantkorting op de factuur verminderd met het bedrag van de contantkorting op de creditnota.  

Als u uw klanten herinneringen wilt sturen over achterstallige betalingen, moet u herinneringsniveaus en -voorwaarden instellen. Zie voor meer informatie [De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Betalingscondities instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsvoorwaarden** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Nadat u de betalingscondities hebt ingesteld, wijst u deze toe aan klanten en leveranciers. Wijs eventueel betalingsvoorwaarden toe aan uw betalingsmethoden.  

> [!TIP]
> In de basisversie van [!INCLUDE [prod_short](includes/prod_short.md)] worden betalingsvoorwaarden met gedeeltelijke betalingen niet ondersteund. In plaats daarvan moet u de functie voor vooruitbetalingen gebruiken. Zie voor meer informatie [Vooruitbetalingen instellen](finance-set-up-prepayments.md) voor meer informatie.
>
> In bepaalde landen/regio's, *kunt* u betalingsvoorwaarden instellen met gedeeltelijke betalingen. Om te zien of deze mogelijkheid in uw land/regio wordt ondersteund, raadpleegt u de sectie **Lokale functionaliteit** in het navigatievenster aan de linkerkant van een [Microsoft Learn](about-localization.md)-artikel.

## <a name="see-also"></a>Zie ook

[Betalingsmethoden instellen](finance-payment-methods.md)  
[Vooruitbetalingen instellen](finance-set-up-prepayments.md)  
[Financiën instellen](finance-setup-finance.md)  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
