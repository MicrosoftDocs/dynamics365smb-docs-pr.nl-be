---
title: Artikeltoeslagen toewijzen aan verkoop en inkopen (bevat video)
description: Wijs artikeltoeslagen toe wanneer u bij voorraadartikelen toegevoegde kosten wilt berekenen, zoals vracht en fysieke verwerking, die u maakt wanneer u artikelen inkoopt of verkoopt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost, landed cost
ms.search.form: 5709, 5800, 5805, 5814
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 6cfebffb12eb2cd7ffa84e12a07c01968c429069
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145614"
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden
Als u wilt zorgen voor goede waardering, moeten voor uw voorraadartikelen toegevoegde kosten worden berekend, zoals vracht, fysieke verwerking, verzekering en transport, die u maakt wanneer u de artikelen inkoopt of verkoopt. Voor inkopen bestaan de werkelijke kosten van een ingekocht artikel uit de inkoopprijs van de leverancier en alle bijkomende directe artikeltoeslagen die kunnen worden toegewezen voor afzonderlijke ontvangsten of retourzendingen. Voor verkopen is het belang van de verzendkosten van verkochte artikelen te weten net zo groot zijn als de leveringskosten van aangekochte artikelen te weten.

Naast het registreren van de toegevoegde kosten in uw voorraadwaarde kunt u de functie Artikeltoeslagen voor het volgende gebruiken:

- Bepaal de leveringskosten van een artikel, zodat u beter een besluit kunt nemen over de optimalisering van het distributienetwerk.
- Splits de kosten of prijs per eenheid van een artikel op voor analysedoeleinden.
- Neem inkooptegoeden op in de kostprijs en de verkoopprijskorting in de eenheidsprijs.

Voordat u artikeltoeslagen kunt toewijzen, moet u artikeltoeslagnummers instellen voor de verschillende soorten artikeltoeslagen, inclusief naar welke grootboekrekeningen kosten met betrekking tot verkoop, inkoop en voorraadherwaarderingen worden geboekt. Een artikeltoeslagnummer bevat een combinatie van een algemene productboekingsgroep, belastinggroepcode, btw-productboekingsgroep en artikeltoeslag. Wanneer u het artikeltoeslagnummer opgeeft in een inkoop- of verkoopdocument, wordt de relevante grootboekrekening opgehaald op basis van het artikeltoeslagnummer en de gegevens in het document.

Voor zowel inkoop- als verkoopdocumenten kunt u een artikeltoeslag op twee manieren toewijzen:
- In het verkoopdocument dat de artikelen bevat waaraan de artikelkosten gerelateerd zijn. Dit doet u normaal voor documenten die nog niet volledig zijn geboekt.
- Op een aparte factuur door de artikeltoeslag te koppelen aan een geboekte ontvangst of verzendingen, waarin de artikelen waaraan de artikelkosten gerelateerd zijn, worden vermeld.

> [!NOTE]  
>   U kunt artikeltoeslagen toewijzen aan orders, facturen en creditnota's, voor zowel verkoop- als inkopen. In de volgende procedures wordt beschreven hoe u met artikeltoeslagen werkt voor een inkoopfactuur. De stappen lijken op alle andere inkoop- en verkoopdocumenten.

## <a name="example"></a>Voorbeeld
Deze video laat zien hoe om te gaan met extra verzendkosten als onderdeel van voorraadkosten.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Artikeltoeslagnummers instellen
De verschillende soorten artikeltoeslagen die in uw bedrijf worden gebruikt, onderscheidt u van elkaar met artikeltoeslagnummers.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeltoeslagen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Artikeltoeslagen** de actie **Nieuw** om een nieuwe regel te maken.
3. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Een artikeltoeslag rechtstreeks toewijzen aan de inkoopfactuur voor het artikel
Als u de artikeltoeslag kent wanneer u de inkoopfactuur van het artikel boekt, volgt u deze procedure.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Een nieuwe inkoopfactuur maken. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).
3. Zorg ervoor dat de inkoopfactuur een of meer regels van de soort Artikel bevat.
4. Selecteer op een nieuwe regel in het veld **Type** **Toeslag (Artikel)**.
5. Typ in het veld **Aantal** het gewenste aantal eenheden van de artikeltoeslag waarvoor u een factuur hebt ontvangen.
6. Typ in het veld **Directe kostprijs** het bedrag van de artikeltoeslag.
7. Vul indien nodig de resterende velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    In de volgende stappen volgt voert u de feitelijke toewijzing uit. Tot de artikeltoeslag volledig is toegewezen, wordt de waarde in het veld **Toe te wijzen aantal** in rood weergegeven.
8. Kies op het tabblad **Regels** de actie **Artikeltoeslagtoewijzing**.

    De pagina **Artikeltoeslagtoewijzing** wordt geopend met één regel voor elke regel van de soort Artikel op de inkoopfactuur. Als u de artikeltoeslag aan een of meer factuurregels wilt toewijzen, kunt u een functie gebruiken die de kosten voor u toewijst en distribueert, of kunt u het veld **Toe te wijzen aantal** handmatig invullen. In de volgende stappen wordt beschreven hoe de functie Artikeltoeslag voorstellen gebruikt.

9. Kies op de pagina **Artikeltoeslagtoewijzing** de actie **Artikeltoeslag voorstellen**.
10. Als er meerdere factuurregels van de soort Artikel zijn, kiest u een van de vier verdelingopties.  

Als de artikeltoeslag volledig is toegewezen, wordt de waarde in het veld **Toe te wijzen aantal** op de inkoopfactuur nul.

De artikeltoeslag wordt nu toegewezen aan de inkoopfactuur. Als u de ontvangst van de inkoopfactuur boekt, worden de voorraadkosten van het artikel bijgewerkt met de kosten van de artikeltoeslag.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Een artikeltoeslag vanuit een aparte factuur rechtstreeks toewijzen aan de inkoopfactuur voor het artikel
Als u een factuur hebt ontvangen voor de artikeltoeslag nadat u de oorspronkelijke inkoopontvangst hebt geboekt, volgt u deze procedure.
1. Herhaal stap 1 tot en met 8 in [Een artikeltoeslag rechtstreeks toewijzen aan de inkoopfactuur voor het artikel](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Kies op de pagina **Artikeltoeslagtoewijzing** de actie **Ontvangstregels ophalen**.
3. Selecteer op de pagina **Inkoopontvangstregels** de geboekte inkoopontvangst voor het artikel waaraan u de artikeltoeslag wilt toewijzen, en kies vervolgens de knop **OK**.
4. Kies de actie **Artikeltoeslag voorstellen**.

De artikeltoeslag op de afzonderlijke inkoopfactuur wordt nu toegewezen aan het artikel op de geboekte inkoopontvangst, waardoor de voorraadwaarde van het artikel wordt bijgewerkt met de kosten van de artikeltoeslag.

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]