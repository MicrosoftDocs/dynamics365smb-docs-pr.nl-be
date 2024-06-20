---
title: Een Shopify-account maken en instellen
description: 'Leer hoe u een Shopify-account kunt krijgen, zodat u de werkstroom voor integratie van Shopify en Business Central kunt demonstreren.'
ms.date: 03/04/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# <a name="create-and-set-up-a-shopify-account"></a>Een Shopify-account maken en instellen



Als u overweegt om Shopify als uw e-commerce-oplossing te gebruiken en een Shopify account nodig hebt om de geïntegreerde workflow te valideren, hebt u de volgende opties:

- Een proefversie nemen. Dit is het typische startpunt voor eindgebruikers.  
- Ontwikkelingswinkels maken. Deze aanpak is voor partners die terugkerende demo's, trainingen en ondersteuning bieden.

## <a name="trial-end-user"></a>Proefversie (eindgebruiker)

Ga naar de [Shopify-website](https://www.shopify.com) en gebruik uw e-mailaccount voor het beheerdersaccount om u aan te melden voor een gratis proefperiode. Voor meer informatie over het maken en personaliseren van uw online winkel zie [Shopify Helpcentrum](https://help.shopify.com/).

Pas in **Shopify-beheer** van de gemaakte winkel de volgende **instellingen** toe:

- Selecteer een abonnement bij de [**Abonnement**](https://www.shopify.com/admin/settings/plan)-instellingen om het afrekenproces te kunnen testen.

- Overweeg om *Aanmeldkoppeling tonen in de koptekst van de online winkel en afrekenen* in te schakelen in de sectie **Accounts in online winkel en bij afrekenen** van de [**Klantaccounts**](https://www.shopify.com/admin/settings/customer_accounts)-instellingen in uw **Shopify beheer**.
- Overweeg om *Nieuwe klantaccount* te selecteren in het gedeelte **Accounts in online winkel en bij afrekenen** van de instellingen voor klantaccounts.
- Overweeg om *Selfserviceretouren* in te schakelen in het gedeelte **Nieuwe klantaccounts** van de instellingen voor klantaccounts.

- Activeer testbetalingen. U hebt twee opties. Ga eerst naar [**Betalingen**](https://www.shopify.com/admin/settings/payments) instellingen:  
  1. *(voor testen) Bogus Gateway*. Zie voor meer informatie [Bogus Gateway activeren voor testen](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* in testmodus. Zie voor meer informatie [Shopify Payments testen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Deactiveer **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de [**Afrekening**-instellingen](https://www.shopify.com/admin/settings/checkout) in uw **Shopify-beheer**.
- Overweeg de optie *Bedrijfsnaam - optioneel* te selecteren in het gedeelte **Klantgegevens** van de afrekeninstellingen.
- Schakel de optie **Opties voor fooien tonen bij afrekenen** in het gedeelte **Fooien** van de afrekeninstellingen in als u van plan bent om fooien te demonstreren.

> [!Important]  
> Vergeet niet uw Shopify proefperiode te annuleren om betalingen te voorkomen.

## <a name="development-store"></a>Ontwikkelingswinkel

Begin met deelname aan het [Shopify-partnerprogramma](https://help.shopify.com/partners/about). Gebruik daarna het **Partnerdashboard** om de ontwikkelingswinkel te maken. Ga voor meer informatie naar [Ontwikkelingswinkels maken](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Pas nadat u de winkel hebt gemaakt in **Shopify-beheer** van de gemaakte winkel de volgende **instellingen** toe:

- Overweeg om *Aanmeldkoppeling tonen in de koptekst van de online winkel en afrekenen* in te schakelen in de sectie **Accounts in online winkel en bij afrekenen** van de [**Klantaccounts**](https://www.shopify.com/admin/settings/customer_accounts)-instellingen in uw **Shopify beheer**.
- Overweeg om *Nieuwe klantaccount* te selecteren in het gedeelte **Accounts in online winkel en bij afrekenen** van de instellingen voor klantaccounts.
- Overweeg om *Selfserviceretouren* in te schakelen in het gedeelte **Nieuwe klantaccounts** van de instellingen voor klantaccounts.
  
- Activeer testbetalingen. U hebt twee opties. Navigeer eerst naar [**Betalingen**](https://www.shopify.com/admin/settings/payments) instellingen:  
  1. *(voor testen) Bogus Gateway*. Zie voor meer informatie [Bogus Gateway activeren voor testen](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* in testmodus. Ga voor meer informatie naar [Shopify Payments testen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).
     
- Deactiveer **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de [**Afrekening**-instellingen](https://www.shopify.com/admin/settings/checkout) in uw **Shopify-beheer**.
- Overweeg de optie *Bedrijfsnaam - optioneel* te selecteren in het gedeelte **Klantgegevens** van de afrekeninstellingen.
- Als u van plan bent fooien te demonstreren, schakelt u de optie **Opties voor fooien tonen bij afrekenen** in het gedeelte **Fooien** van de afrekeninstellingen in.


> [!Note]  
> Ontwikkelingswinkels zijn meestal met een wachtwoord beveiligd. Wanneer u een specifieke pagina in uw online winkel probeert te openen vanuit [!INCLUDE [prod_short](../includes/prod_short.md)], bijvoorbeeld om naar een specifiek product of bestelling te gaan, moet u uw wachtwoord invoeren. Om te voorkomen dat u uw wachtwoord moet invoeren, logt u tijdens het testen in bij uw Shopify-beheer en opent u uw winkel vanaf daar. U hoeft het winkelwachtwoord pas in te voeren als u uw browser sluit of uw sessie verloopt.  

## <a name="see-also"></a>Zie ook

[Aan de slag met de Shopify-connector](get-started.md)  
[Procedure: Shopify-connector instellen en gebruiken](walkthrough-setting-up-and-using-shopify.md)
