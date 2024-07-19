---
title: De extensie PayPal Payments Standard gebruiken
description: Dit artikel beschrijft hoe u de standaardextensie gebruikt om klanten de mogelijkheid te bieden betalingen te doen met PayPal.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# De extensie PayPal Payments Standard

Met de PayPal Payments Standard-extensie kunt u uw klantenserviceniveau verbeteren door het voor uw klanten gemakkelijker te maken hun rekeningen te betalen.

Als alternatief voor het innen van betalingen via bankoverschrijving of creditering Kaarten kunnen klanten betalen via hun PayPal-rekening. Wanneer u een verkoopfactuur verzendt per e-mail, is er een PayPal-koppeling in de e-mailhoofdtekst en in het gekoppelde PDF-document aanwezig. Als de klant koppelen kiest, wordt de servicepagina voor zijn PayPal-rekening geopend en worden de betalingsgegevens weergegeven. De klant kan de factuur vervolgens als elke andere PayPal-betaling betalen.

De service PayPal Payments Standard biedt de volgende voordelen:

* Klantbetalingen komen sneller op uw bankrekening binnen.
* Klanten kunnen op meer manieren facturen betalen.
* PayPal biedt een betrouwbare betalingsservice, die klanten liever gebruiken dan dat ze creditcardinformatie op websites invoeren.
* PayPal biedt meerdere manieren om betalingen te verwerken, inclusief creditcardverwerking, PayPal-rekeningen en andere bronnen.
* De PayPal-koppeling kan automatisch aan verkoopdocumenten worden toegevoegd of handmatig door de gebruiker.
* Met de service PayPal Payments Standard bent u geen maandelijkse kosten of installatiekosten kwijt.
* Omdat het een extensie is, kunt u de service PayPal Payment Standard gemakkelijk inschakelen wanneer en als uw bedrijf het nodig heeft.  

Voor meer informatie over het instellen van de extensie gaat u naar [Klantbetaling via PayPal inschakelen](sales-how-enable-payment-service-extensions.md).

## Registreer betalingen automatisch voor zakelijke accounts

[!INCLUDE [prod_short](includes/prod_short.md)] kan betalingen automatisch registreren als u een Business Merchant-account heeft voor het PayPal Commerce Platform. Wanneer uw klanten PayPal koppelen gebruiken om een ​​factuur te betalen, [!INCLUDE [prod_short](includes/prod_short.md)] wordt de invoer gepost en Sluiten het document.

Als u deze mogelijkheid wilt gebruiken, schakelt u op de pagina  **Betalingsregistratie instellen** in [!INCLUDE [prod_short](includes/prod_short.md)] de optie **Betalingen automatisch registrerenin** schakel en verifieer de accounts die u voor de betalingen gaat gebruiken. Als u besluit dat u betalingen niet automatisch wilt registreren, kunt u dit weer uitschakelen.

> [!TIP]
> Ontwikkelaars kunnen sandbox-accounts gebruiken om de installatie te testen. Wijzig hiervoor de PayPal-URL in **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] maakt gebruik van de PayPal's Instant Payment Notification (IPN) via kennisgeving_url.

## Zie ook

[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
