---
title: Uw boekingen factureren in Business Central | Microsoft Docs
description: Leren hoe u massaal factureert vanuit Microsoft Bookings in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 0048d0e78084c939c9e2a707975598a171108cdc
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183944"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-d365fin"></a>Massaal factureren voor Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Als uw bedrijf de app Bookings gebruikt in Office 365, kunt u massaal factureren voor afspraken. De pagina **Niet-gefactureerde Bookings** in [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt een overzicht van de voltooide boekingen van het bedrijf. Op deze pagina kunt u snel afspraken selecteren die u wilt factureren en conceptfacturen maken voor de geleverde services.  

## <a name="connect-to-bookings"></a>Verbinden met Bookings
Als u [!INCLUDE[d365fin](includes/d365fin_md.md)] wilt verbinden met Bookings, moet u uw Bookings-bedrijf opgeven, opgeven wat u wilt synchroniseren met Bookings, hoe vaak moet worden gesynchroniseerd en welke sjablonen moeten worden gebruikt. U stelt deze informatie in op de pagina **Instelling van Booking-synchronisatie**, die u kunt starten vanaf de pagina **Instelling van Exchange-synchronisatie**, die u kunt vinden met behulp van [Zoeken](ui-search.md).  

Als u bijvoorbeeld klanten wilt synchroniseren tussen Bookings en [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de standaardsjabloon opgeven die moet worden gebruikt om nieuwe klanten toe te voegen aan [!INCLUDE[d365fin](includes/d365fin_md.md)], op basis van de klanten in uw Bookings-bedrijf.  

> [!NOTE]
> De app Bookings is bedoeld om afspraken te boeken voor individuele klanten, in plaats van bedrijven. De synchronisatie met [!INCLUDE[d365fin](includes/d365fin_md.md)] synchroniseert dus slechts klantcontactpersonen van het type Persoon. Er is ook een e-mailadres vereist om het contact te synchroniseren.  

Als u serviceartikelen wilt synchroniseren tussen Bookings en [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u ook de standaardsjabloon opgeven die moet worden gebruikt om nieuwe serviceartikelen toe te voegen in [!INCLUDE[d365fin](includes/d365fin_md.md)], op basis van de services in ons Bookings-bedrijf.  

> [!NOTE]
> Alleen artikelen van het type *Service* worden gesynchroniseerd tussen Bookings en [!INCLUDE[d365fin](includes/d365fin_md.md)]. De sjabloon die u instelt op de pagina **Configuratiesjablonen**, zodat deze kan worden gebruikt voor de artikelsynchronisatie, moet het type definiëren als *Service*.

## <a name="invoice-appointments"></a>Afspraken factureren
Wanneer het tijd is om facturen te verzenden voor de voltooide boekingen, gaat u naar de pagina **Niet-gefactureerde Bookings**. Afhankelijk van hoe vaak de gegevens worden gesynchroniseerd, is de lijst lang of kort. U kunt facturen maken voor alle boekingen in de lijst of voor één tegelijkertijd. U kunt een of meer posten in het overzicht selecteren en alleen die factureren.  

De ondersteuning voor het factureren van afspraken vanuit Bookings is eenvoudiger dan de volledigere werkstroom voor het werken met verkoopoffertes, verkooporders en verkoopfacturen. Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie. U kunt uw services verkopen met [!INCLUDE[d365fin](includes/d365fin_md.md)] of kiezen om Bookings te gebruiken, afhankelijk van uw zakelijke behoeften.  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  
