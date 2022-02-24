---
title: Een btw-nummer valideren | Microsoft Docs
description: Een btw-nummer valideren.
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu
ms.openlocfilehash: 4b282d8819851fd6529f901f44a39777a8b8e74c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183080"
---
# <a name="validate-a-vat-registration-number"></a>Een btw-nummer valideren.

## <a name="to-verify-vat-registration-numbers"></a>Btw-nummers controleren
Het is belangrijk dat de btw-registratienummers die u voor klanten, leveranciers en contactpersonen hebt, geldig zijn. Bedrijven wijzigen bijvoorbeeld soms hun belastingschuldstatus, en in sommige landen kan de belastingdienst u vragen om rapporten te verschaffen, zoals het rapport Verkoopoverzicht EU, waarin de btw-registratienummers worden weergegeven die u gebruikt wanneer u zaken doet.

De Europese commissie verschaft de VIES-service voor btw-nummervalidatie op de website. Deze service is openbaar en gratis. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan u moeite besparen. U kunt namelijk de VIES-service om btw-nummers voor klanten, leveranciers en contactpersonen te valideren en bij te houden, rechtstreeks van de klanten-, leveranciers en contactkaarten gebruiken. De service in [!INCLUDE[d365fin](includes/d365fin_md.md)] heet **Instelling van validatieservice van EU-btw-nummers**. De service is beschikbaar op de pagina **Serviceverbindingen** en u kunt deze service meteen gebruiken. De serviceverbinding is gratis en er is geen aanmelding vereist.

Als u de **Validatieservice van EU-btw-nummers** wilt inschakelen, opent u het item op de pagina **Serviceverbinding**. Het veld **Eindpunt van service** moet al zijn ingevuld. Als dit niet het geval is, kunt u de actie **Standaardeindpunt instellen** gebruiken. Stel vervolgens het veld **Geactiveerd** in en u bent klaar.

> [!Note]
> Als u de validatieservice van EU-btw-nummers wilt inschakelen, moet u over beheerdertoegangsrechten beschikken.

Wanneer u onze serviceverbinding gebruikt, registreren we een overzicht van btw-nummers en verificaties voor elke klant, leverancier of contactpersoon in het **Btw-log**, zodat u deze eenvoudig kunt bijhouden. Het logboek is specifiek voor elke klant. Het logboek is bijvoorbeeld handig om te bewijzen dat u hebt gecontroleerd dat het huidige btw-nummer juist is. Wanneer u een btw-nummer verifieert, wordt in de kolom **Aanvraag-id** in het logboek aangegeven dat u actie hebt ondernomen.

U kunt het btw-log weergeven op de klanten-, leveranciers- of contactkaarten, op het sneltabblad **Facturering**, door de zoekknop te kiezen in het veld **Btw-nummer**.  

Onze service kan u ook wat tijd besparen als u een klant of een leverancier maakt. Als u het btw-nummer van de klant weet, kunt u het in het veld **Btw-nummer** op de klanten- of leverancierskaart invoeren. De klantnaam wordt dan voor u ingevuld. Sommige landen verschaffen ook bedrijfsadressen in een gestructureerde indeling. In deze landen wordt het adres ook door ons ingevuld.  

Er zijn een paar dingen waarmee u rekening moet houden met betrekking tot de VIES-service voor btw-nummervalidatie:

* De service gebruikt het http-protocol, wat betekent dat gegevens die door de server worden overgebracht, niet zijn versleuteld.  
* Deze service wordt mogelijk onderbroken. Hiervoor is Microsoft niet verantwoordelijk. De service maakt deel uit van een breed EU-netwerk van nationale btw-journalen.

## <a name="see-also"></a>Zie ook  
[Btw instellen](finance-setup-vat.md)  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)      
[Btw-aangifte doen bij een belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Lokale functionaliteit in Business Central](about-localization.md)
