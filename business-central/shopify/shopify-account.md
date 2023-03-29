---
title: Een Shopify-account maken en instellen
description: 'Leer hoe u een Shopify-account kunt krijgen, zodat u de werkstroom voor integratie van Shopify en Business Central kunt demonstreren.'
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# Een Shopify-account maken en instellen

Als u overweegt om Shopify als uw e-commerce-oplossing te gebruiken en een Shopify account nodig hebt om de geïntegreerde workflow te valideren, hebt u de volgende opties:

- Een proefversie nemen. Dit is het typische startpunt voor eindgebruikers.  
- Ontwikkelingswinkels maken. Deze aanpak is voor partners die terugkerende demo's, trainingen en ondersteuning bieden.

## Proefversie (eindgebruiker)

Ga naar de [Shopify-website](https://www.shopify.com) en gebruik uw e-mailaccount voor het beheerdersaccount om u aan te melden voor een gratis proefperiode. Voor meer informatie over het maken en personaliseren van uw online winkel zie [Shopify Helpcentrum](https://help.shopify.com/).

Pas in **Shopify-beheer** van de gemaakte winkel de volgende **instellingen** toe:

- Deactiveer **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de [**Afrekening**-instellingen](https://www.shopify.com/admin/settings/checkout) in uw **Shopify-beheer**.
- Overweeg om *Aanmeldkoppeling tonen in winkel en bij afrekenen* in te schakelen in het gedeelte **Klantaccountinstellingen** van de afrekeninstellingen.
- Overweeg de optie *Bedrijfsnaam - optioneel* te selecteren in het gedeelte **Klantgegevens** van de afrekeninstellingen.
- Schakel de optie **Opties voor fooien tonen bij afrekenen** in het gedeelte **Fooien** van de afrekeninstellingen in als u van plan bent om fooien te demonstreren.
- Activeer testbetalingen. U hebt twee opties. Ga eerst naar [**Betalingen**](https://www.shopify.com/admin/settings/payments) instellingen:  
  1. *(voor testen) Bogus Gateway*. Zie voor meer informatie [Bogus Gateway activeren voor testen](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* in testmodus. Zie voor meer informatie [Shopify Payments testen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Selecteer een abonnement bij de [**Abonnement**](https://www.shopify.com/admin/settings/plan)-instellingen om het afrekenproces te kunnen testen.

> [!Important]  
> Vergeet niet uw Shopify proefperiode te annuleren om betalingen te voorkomen.

## Ontwikkelingswinkel

Begin met deelname aan het [Shopify-partnerprogramma](https://help.shopify.com/partners/about). Gebruik daarna het **Partnerdashboard** om de ontwikkelingswinkel te maken. Ga voor meer informatie naar [Ontwikkelingswinkels maken](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Pas nadat u de winkel hebt gemaakt in **Shopify-beheer** van de gemaakte winkel de volgende **instellingen** toe:

- Deactiveer **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de [**Afrekening**-instellingen](https://www.shopify.com/admin/settings/checkout) in uw **Shopify-beheer**.
- Overweeg om *Aanmeldkoppeling tonen in winkel en bij afrekenen* in te schakelen in het gedeelte **Klantaccountinstellingen** van de afrekeninstellingen.
- Overweeg de optie *Bedrijfsnaam - optioneel* te selecteren in het gedeelte **Klantgegevens** van de afrekeninstellingen.
- Als u van plan bent fooien te demonstreren, schakelt u de optie **Opties voor fooien tonen bij afrekenen** in het gedeelte **Fooien** van de afrekeninstellingen in.
- Activeer testbetalingen. U hebt twee opties. Navigeer eerst naar [**Betalingen**](https://www.shopify.com/admin/settings/payments) instellingen:  
  1. *(voor testen) Bogus Gateway*. Zie voor meer informatie [Bogus Gateway activeren voor testen](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* in testmodus. Ga voor meer informatie naar [Shopify Payments testen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

## Zie ook

[Aan de slag met de Shopify-connector](get-started.md)  
[Procedure: Shopify-connector instellen en gebruiken](walkthrough-setting-up-and-using-shopify.md)
