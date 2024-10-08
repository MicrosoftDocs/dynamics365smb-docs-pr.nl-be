---
title: Een inkoopofferte maken om een offerte op te vragen
description: Beschrijft hoe u een verkoopaanbieding of een offerteaanvraagdocument maakt om uw aanbod aan een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="request-quotes"></a>Offertes aanvragen

U kunt een inkoopofferte als conceptversie van de inkooporder gebruiken. De order kan vervolgens in een inkoopfactuur of een order worden omgezet.

## <a name="create-a-purchase-quote"></a>Een inkoopofferte maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopoffertes** in en kies vervolgens de gerelateerde koppeling
2. Maak een nieuw document op dezelfde manier als u een inkooporder maakt. Meer informatie op [Inkopen vastleggen](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order"></a>Een inkoopofferte omzetten in een inkooporder

Wanneer u de leveranciersofferte hebt geaccepteerd, kunt u deze omzetten naar een inkooporder of de inkoop verwerken.

1. Open de inkoopofferte die u wilt converteren, en kies de actie **Order maken**.

De inkoopofferte wordt verwijderd uit de database. Een inkooporder wordt gemaakt op basis van de informatie in de inkoopofferte, die u kunt gebruiken om de inkoop te verwerken, en vervolgens een inkoopfactuur te boeken. Op de inkooporder en de inkoopfactuur vermeldt het veld **Offertenr.** het nummer van de inkoopofferte van waaruit ze zijn gemaakt.

> [!NOTE]
> Het is niet mogelijk om een inkoopofferte direct om te zetten naar een inkoopfactuur, zoals bij verkoopoffertes wel mogelijk is. Voor meer informatie over het maken van een inkoopfactuur, leest u [Inkopen registreren met inkoopfacturen](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Zie ook

[Inkoop](purchasing-manage-purchasing.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Documenten verzenden via e-mail](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
