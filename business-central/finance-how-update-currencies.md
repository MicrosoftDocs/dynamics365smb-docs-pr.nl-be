---
title: Valutawisselkoersen bijwerken | Microsoft Docs
description: Als u meerdere valuta's in uw bedrijf wilt gebruiken, kunt u een code voor elke gebruikte valuta instellen en een externe wisselkoersservice gebruiken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a9fa636fb68a428da3c587e59be1bf76cf976207
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926950"
---
# <a name="update-currency-exchange-rates"></a>Valutawisselkoersen bijwerken
Aangezien bedrijven steeds vaker in andere landen/regio's opereren, is het belangrijk dat zij kunnen handelen en financiën in meer dan één valuta kunnen controleren of rapporteren. U moet een code instellen voor elke gebruikte valuta als u in andere valuta's dan uw lokale valuta inkoopt of verkoopt, in een andere valuta tegoeden of schulden hebt of grootboektransacties in verschillende valuta's vastlegt.

Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken, maar u kunt het ook instellen om een andere valuta te gebruiken, waaraan een huidige wisselkoers is toegewezen. Door een tweede valuta in te stellen als een zogenaamde aanvullende rapportagevaluta, legt [!INCLUDE[d365fin](includes/d365fin_md.md)] bedragen automatisch vast in zowel de LV als deze aanvullende rapportagevaluta voor elke grootboekpost en andere posten, zoals btw-posten. Zie voor meer informatie [Een extra rapportagevaluta instellen](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Wisselkoersen corrigeren
Aangezien valutakoersen constant wisselen, moeten de extra valuta-equivalenten in uw systeem periodiek worden gecorrigeerd. Als deze correcties niet worden uitgevoerd, kunnen de bedragen die omgerekend zijn van vreemde (of extra) valuta's en geboekt zijn in het grootboek in LV misleidend zijn. Bovendien moeten dagelijkse posten die geboekt zijn doordat een dagwisselkoers is ingevoerd in het programma worden bijgewerkt nadat de dagwisselkoersgegevens zijn ingevoerd.

De batchverwerking **Wisselkoers herwaarderen** wordt gebruikt om de wisselkoersen van de geboekte klant, leverancier en bankrekeningposten handmatig te corrigeren. U kunt er tevens extra rapportagevalutabedragen in grootboekposten mee bijwerken. U kunt de wisselkoersen ook automatisch laten corrigeren door een service te gebruiken. Zie [Een wisselkoersservice instellen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service) voor meer informatie.

### <a name="effect-on-customers-and-vendors"></a>Effect op klanten en leveranciers
Voor klanten- en leveranciersrekeningen wordt de valuta tijdens de batchverwerking met de wisselkoers die geldig is op de opgegeven boekingsdatum. Met de batchverwerking worden de verschillen voor de afzonderlijke valutasaldo's berekend en worden de bedragen geboekt naar de opgegeven grootboekrekening in het veld **Ongereal. koerswinstrekening** of **Ongereal. koersverliesrekening** in de tabel **Valuta's**. Tegenposten worden automatisch geboekt naar de liquiditeitsrekening in het grootboek.

In de batchverwerking worden alle open klantenposten en leveranciersposten verwerkt. Als er sprake is van een wisselkoersverschil voor een post, wordt in de batchverwerking een nieuwe gedetailleerde klanten- of leverancierspost gemaakt. Deze post staat voor het aangepaste bedrag op de klanten- of leverancierspost.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensies in klanten- en leveranciersposten
De herwaarderingsposten krijgen de dimensies van de klanten-/leveranciersposten toegewezen en de herwaarderingen worden geboekt per combinatie van dimensiewaarden.

### <a name="effect-on-bank-accounts"></a>Effect op bankrekeningen
Voor bankrekeningen wordt de valuta tijdens de batchverwerking geherwaardeerd met de wisselkoers die geldig is op de opgegeven boekingsdatum. Tijdens de batchverwerking worden de verschillen voor elke bankrekening met een valutacode berekend en worden de bedragen geboekt naar de opgegeven grootboekrekening in het veld **Gereal. koerswinstrekening** of **Gereal. koersverliesrekening** in de tabel **Valuta's**. Tegenposten worden automatisch geboekt naar de grootboekrekeningen die in de bankboekingsgroepen zijn opgegeven. Tijdens de batchverwerking wordt één post per valuta per boekingsgroep berekend.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensies op bankrekeningposten
De herwaarderingsposten voor de grootboekrekening van de bankrekening en voor de winst-/verliesrekening krijgen de standaarddimensies van de bankrekening toegewezen.

### <a name="effect-on-gl-accounts"></a>Effect op grootboekbankrekeningen
Als u in een rapportagevaluta boekt, kunt u met de batchverwerking nieuwe posten boeken voor valutaherwaarderingen tussen de lokale valuta en de rapportagevaluta. Met de batchverwerking worden de verschillen voor elke grootboekpost berekend en wordt de grootboekpost voor elke grootboekrekening geherwaardeerd op basis van de inhoud van het veld **Wisselkoersherwaardering**.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensies op grootboekrekeningposten
De herwaarderingsposten krijgen de standaarddimensies toegewezen van de rekeningen waarop ze worden geboekt.

> [!Important]
> Voordat u de batchverwerking kunt gebruiken, moet u de herwaarderingswisselkoersen invoeren waarmee de saldo's in vreemde valuta worden geherwaardeerd. U doet dit op de pagina **Valutawisselkoersen**.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Een wisselkoersservice instellen
U kunt een externe service gebruiken om valutawisselkoersen actueel te houden, zoals FloatRates.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Valutawisselkoersservices** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul op de pagina **Valutawisselkoersservice** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies het selectievakje **Ingeschakeld** om de service in te schakelen.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valutawisselkoersen bijwerken met een service
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Valuta's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Wisselkoersen bijwerken**.

De waarde in het veld **Wisselkoers** op de pagina **Valuta's** wordt bijgewerkt met de laatste wisselkoers.

## <a name="see-also"></a>Zie ook
[Een extra rapportagevaluta instellen.](finance-how-setup-additional-currencies.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
