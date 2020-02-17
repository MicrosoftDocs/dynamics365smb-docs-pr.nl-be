---
title: De Wijzigingstool btw-tarief gebruiken | Microsoft Docs
description: De Wijzigingstool btw-tarief gebruiken
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992262"
---
# <a name="use-the-vat-rate-change-tool"></a>De Wijzigingstool btw-tarief gebruiken

## <a name="understanding-the-vat-rate-conversion-process"></a>Het proces voor het converteren van btw-tariefswijzigingen begrijpen.  
De tool voor het wijzigen van het btw-tarief voert op verschillende manieren conversies uit voor hoofdgegevens, dagboeken en orders. De geselecteerde stamgegevens en dagboeken worden bijgewerkt door de nieuwe algemene productboekingsgroep of de btw-productboekingsgroep. Als u een order volledig of gedeeltelijk hebt verzonden, blijven de verzonden artikelen onderdeel van de huidige algemene productboekingsgroep of btw-productboekingsgroep. Een nieuwe orderregel wordt gemaakt voor de niet verzonden items en bijgewerkt om overeen te komen met de huidige en de nieuwe BTW- of productboekingsgroepen. Bovendien worden gegevens over artikeltoeslagtoewijzigingen, reserveringen en artikeltracering dienovereenkomstig bijgewerkt.  

Er is een aantal dingen die niet worden geconverteerd door de tool:

* Verkoop- of inkooporders en facturen waar verzendingen zijn geboekt. Deze documenten zijn geboekt met het huidige btw-tarief.  
* Documenten met geboekte vooruitbetalingsfacturen. U hebt bijvoorbeeld vooruitbetalingen gedaan of ontvangen op facturen die nog niet zijn voltooid voordat u het wijzigingstool btw-tarief gaat gebruiken. In dit geval is er een verschil tussen de verschuldigde btw en de betaalde btw in de vooruitbetalingen wanneer de factuur is voltooid. Het wijzigingstool btw-tarief slaat deze documenten over en u moet deze handmatig bijwerken.  
* Doorverzendingen of speciale orders.  
* Verkoop- of inkooporders met magazijnintegratie als deze gedeeltelijk zijn verzonden of ontvangen.  
* Servicecontracten.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Conversies van btw-tariefswijziging voorbereiden  
Voordat u het wijzigingstool btw-tarief instelt, moet u de volgende voorbereidingen treffen.

* Als u transacties met verschillende tarieven hebt, moeten deze vervolgens worden gescheiden in verschillende groepen door voor elke tarief nieuwe grootboekrekeningen te maken of door met gegevensfilters transacties per tarief te groeperen.  
* Als u nieuwe grootboekrekeningen maakt, moet u nieuwe algemene boekingsgroepen maken.  
* Om het aantal documenten dat wordt geconverteerd zo klein mogelijk te maken, moet u zoveel mogelijk documenten boeken en niet-geboekte documenten tot een minimum beperken.  
* Back-up van gegevens maken.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Het wijzigingstool btw-tarief instellen  
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Wijziging btw-tarief instellen** in en kies de desbetreffende koppeling.  
2. Op de sneltabbladen **Hoofdgegevens**, **Dagboeken** en **Documenten** kiest u een boekingsgroepwaarde in de lijst met opties voor verplichte velden. Voor elke groep kunt u kiezen of u btw-productboekingsgroepen of algemene productboekingsgroepen wilt converteren of beide waarden wilt converteren als deze beschikbaar zijn in het stamgegevensitem. Voor sommige gebieden kunt u ook een filter instellen om alleen een subset van waarden te converteren, bijvoorbeeld grootboekrekeningen. 

### <a name="to-set-up-product-posting-group-conversion"></a>Conversie voor productboekingsgroepen instellen  
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Wijziging btw-tarief instellen** in en kies de desbetreffende koppeling.  
2. Kies op de pagina **Wijziging btw-tarief instellen** en kies de actie **Conversie boekingsgroep btw-producten** of **Conversie boekingsgroep algemene producten**.  
3. Voer in het veld **Van code** de huidige boekingsgroep in.  
4. Voer in het veld **Tot code** de nieuwe boekingsgroep in.  

### <a name="to-perform-vat-rate-change-conversion"></a>Een conversie voor een btw-tariefswijziging uitvoeren  
U gebruikt de Wijzigingstool btw-tarief om wijzigingen in het standaardtarief van btw te beheren. U kunt btw en algemene boekingsgroepconversies uitvoeren om btw-tarieven te wijzigen en nauwkeurige btw-rapportage te onderhouden. Afhankelijk van uw instellingen worden de volgende wijzigingen aangebracht:  

* Btw- en algemene boekingsgroepen worden geconverteerd.  
* Wijzigingen worden doorgevoerd in grootboekrekeningen, klanten, leveranciers, geopende documenten, dagboekregels, enzovoort.  

> [!IMPORTANT]  
>  Voordat u de conversie van de btw-tariefswijziging uitvoert, kunt u de conversie testen. Hiervoor volgt u de onderstaande stappen, maar zorg ervoor dat u de selectievakjes **Conversie uitvoeren** en **Wijzigingstool BTW-tarief voltooid** uitschakelt. Tijdens testconversie wordt het veld **Geconverteerd** in de tabel **Dagboekpost wijziging BTW-tarief** gewist en is het veld **Conversiedatum** in de tabel **Dagboekpost wijziging BTW-tarief** leeg. Kies nadat de conversie is voltooid de optie **Wijzigingslogposten btw-tarief** om de resultaten van de testconversie weer te geven. Controleer elke post voordat u de conversie uitvoert. Controleer met name transacties met een oud btw-tarief.     

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Wijziging btw-tarief** in en kies de koppeling **Wijziging btw-tarief instellen**.  
2. Controleer of u de conversie van de btw-productboekingsgroep of de conversie van de algemene productboekingsgroep al hebt ingesteld.  
3. Schakel het selectievakje **Conversie uitvoeren** in.  

    > [!IMPORTANT]  
    >  Schakel het selectievakje **Wijzigingstool BTW-tarief voltooid** uit. Het selectievakje wordt automatisch ingeschakeld wanneer de conversie btw-tariefswijziging is voltooid.  

4. Kies de actie **Converteren**.  
5. Wanneer de conversie voltooid is, kiest u de actie **Logbestandvermeldingen btw-tariefwijziging** om de resultaten van de conversie te zien.  

> [!IMPORTANT]  
>  Nadat de conversie is voltooid, wordt het veld **Geconverteerd** in de tabel **Dagboekpost wijziging BTW-tarief** ingeschakeld en bevat het veld **Conversiedatum** in de tabel **Dagboekpost wijziging BTW-tarief** de conversiedatum.  
## <a name="see-also"></a>Zie ook  
[Btw instellen](finance-setup-vat.md)  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)      
[Btw-aangifte doen bij een belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Lokale functionaliteit in Business Central](about-localization.md)
