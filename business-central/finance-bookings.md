---
title: Uw boekingen factureren in Business Central
description: In dit onderwerp wordt uitgelegd hoe u bulkfacturering kunt uitvoeren vanuit Microsoft Bookings in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-"></a>Massaal factureren voor Microsoft Bookings in [!INCLUDE[prod_short](includes/prod_short.md)]

Als uw bedrijf de app Bookings gebruikt in Microsoft 365, kunt u massaal factureren voor afspraken. De pagina **Niet gefactureerde boekingen** in [!INCLUDE[prod_short](includes/prod_short.md)] biedt een overzicht van de voltooide boekingen van het bedrijf. Op deze pagina kunt u snel afspraken selecteren die u wilt factureren en conceptfacturen maken voor de geleverde services.  

## <a name="connect-to-bookings"></a>Verbinden met Bookings

Als u [!INCLUDE[prod_short](includes/prod_short.md)] wilt verbinden met Bookings, moet u uw Bookings-bedrijf opgeven, opgeven wat u wilt synchroniseren met Bookings, hoe vaak moet worden gesynchroniseerd en welke sjablonen moeten worden gebruikt. U stelt deze informatie in op de pagina **Instelling van Booking-synchronisatie**, die u kunt starten vanaf de pagina **Instelling van Exchange-synchronisatie**, die u kunt vinden met behulp van [Zoeken](ui-search.md).  

Als u bijvoorbeeld klanten wilt synchroniseren tussen Bookings en [!INCLUDE[prod_short](includes/prod_short.md)], moet u de standaardsjabloon opgeven die moet worden gebruikt om nieuwe klanten toe te voegen aan [!INCLUDE[prod_short](includes/prod_short.md)], op basis van de klanten in uw Bookings-bedrijf.  

> [!NOTE]
> De app Bookings is bedoeld om afspraken te boeken voor individuele klanten, in plaats van bedrijven. De synchronisatie met [!INCLUDE[prod_short](includes/prod_short.md)] synchroniseert dus slechts klantcontacten van het type *Persoon*. Er is ook een e-mailadres vereist om het contact te synchroniseren.  

Als u serviceartikelen wilt synchroniseren tussen Bookings en [!INCLUDE[prod_short](includes/prod_short.md)], moet u ook de standaardsjabloon opgeven die moet worden gebruikt om nieuwe serviceartikelen toe te voegen in [!INCLUDE[prod_short](includes/prod_short.md)], op basis van de services in ons Bookings-bedrijf.  

> [!NOTE]
> Alleen artikelen van het type *Service* worden gesynchroniseerd tussen Bookings en [!INCLUDE[prod_short](includes/prod_short.md)]. De sjabloon die u instelt op de pagina **Configuratiesjablonen**, zodat deze kan worden gebruikt voor de artikelsynchronisatie, moet het type definiëren als *Service*.

## <a name="invoice-appointments"></a>Afspraken factureren

Wanneer het tijd is om facturen te verzenden voor de voltooide boekingen, gaat u naar de pagina **Niet gefactureerde boekingen**. Afhankelijk van hoe vaak de gegevens worden gesynchroniseerd, is de lijst lang of kort. U kunt facturen maken voor alle boekingen in de lijst of voor één tegelijkertijd. U kunt een of meer posten in het overzicht selecteren en alleen die factureren.  

De ondersteuning voor het factureren van afspraken vanuit Bookings is eenvoudiger dan de volledigere werkstroom voor het werken met verkoopoffertes, verkooporders en verkoopfacturen. Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie. U kunt uw services verkopen met [!INCLUDE[prod_short](includes/prod_short.md)] of kiezen om Bookings te gebruiken, afhankelijk van uw zakelijke behoeften.  

> [!NOTE]
> In mei 2022 ontdekten we een probleem in de integratie met Bookings. Momenteel is voor de synchronisatie van Bookings naar [!INCLUDE [prod_short](includes/prod_short.md)] vereist dat u de facturen handmatig aan klanten in [!INCLUDE [prod_short](includes/prod_short.md)] koppelt.

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
