---
title: Betalingsvoorwaarden instellen
description: Gebruik betalingscondities voor het beheer van vervaldatums en contantkortingen.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 09/05/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-payment-terms"></a>Betalingsvoorwaarden instellen

Betalingscondities bepalen hoe u omgaat met vervaldata en betalingskortingen. U kunt elk gewenst aantal betalingsconditiecodes instellen en datumformules gebruiken om de betalingscondities te bepalen. Wanneer u zich voor het eerst aanmeldt voor [!INCLUDE [prod_short](includes/prod_short.md)] biedt het demonstratiebedrijf een aantal betaalmethoden aan die bedrijven vaak gebruiken. U kunt er echter zo veel toevoegen als u wilt.  

Als u betalingscondities aan klanten en leveranciers toewijst, worden altijd dezelfde condities gebruikt op de verkoop- en inkoopdocumenten die u voor hen maakt. De documentdatums op verkoop- en inkoopdocumenten, en niet de boekingsdatums ervan, worden gebruikt om vervaldatums voor betalingen te berekenen. Indien nodig kunt u de condities op het verkoop- of inkoopdocument wijzigen, bijvoorbeeld als u wilt dat een bepaalde klant u binnen 7 dagen betaalt in plaats van de standaard 14 dagen. Als u de voorwaarden op het document wijzigt, verandert de standaardbetalingstermijn die aan de klant is toegewezen niet. Voor verkoop- en inkoopdocumenten zijn dezelfde betalingscondities beschikbaar.

Wanneer u vervolgens een factuur boekt, berekent [!INCLUDE [prod_short](includes/prod_short.md)] de contantkortingen op basis van de betalingscondities. De contantkortingsdatum is de laatste datum waarop de klant een korting kan krijgen. De datum wordt ook berekend wanneer u een factuur boekt.  

Evenzo, wanneer u een creditnota plaatst, berekent [!INCLUDE [prod_short](includes/prod_short.md)] mogelijke contantkortingen op basis van de betalingscondities. Het berekent de korting op creditnota's op dezelfde manier als kortingen op facturen. Wanneer u een creditnota met een factuur vereffent, [!INCLUDE [prod_short](includes/prod_short.md)] wordt het kortingsbedrag voor de factuur verlaagd met het kortingsbedrag van de creditnota.  

Als u uw klanten herinneringen wilt sturen over achterstallige betalingen, moet u herinneringsniveaus en -voorwaarden instellen. Ga voor meer informatie over aanmaningen naar [De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Betalingscondities instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsvoorwaarden** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Nadat u de betalingscondities hebt ingesteld, wijst u deze toe aan klanten en leveranciers. Wijs eventueel betalingsvoorwaarden toe aan uw betalingsmethoden.  

> [!TIP]
> In de basisversie van [!INCLUDE [prod_short](includes/prod_short.md)] worden betalingsvoorwaarden met gedeeltelijke betalingen niet ondersteund. In plaats daarvan moet u de functie voor vooruitbetalingen gebruiken. Ga voor meer informatie over vooruitbetalingen naar [Vooruitbetalingen instellen](finance-set-up-prepayments.md).
>
> In bepaalde landen/regio's *kunt* u betalingsvoorwaarden instellen met gedeeltelijke betalingen. Om te zien of deze mogelijkheid in uw land/regio wordt ondersteund, raadpleegt u de sectie **Lokale functionaliteit** in de inhoudsopgave aan de linkerkant van een [Microsoft Learn](about-localization.md)-artikel.

## <a name="see-also"></a>Zie ook

[Betalingsmethoden instellen](finance-payment-methods.md)  
[Vooruitbetalingen instellen](finance-set-up-prepayments.md)  
[Financiën instellen](finance-setup-finance.md)  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
