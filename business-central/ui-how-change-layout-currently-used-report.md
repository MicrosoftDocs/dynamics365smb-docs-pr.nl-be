---
title: De weergave van een rapport wijzigen door een andere lay-out te kiezen | Microsoft Docs
description: U kunt verschillende lay-outs voor een lijst gebruiken en schakelen tussen lay-outs om te bepalen hoe een rapport eruitziet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: af33d0679242e9915bc3e0de5825bf293e22c585
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809093"
---
# <a name="change-the-current-report-layout"></a>De huidige rapportindeling wijzigen
Een rapport kan worden ingesteld met meerdere rapportlay-outs, waartussen u indien nodig kunt schakelen.

Afhankelijk van de lay-outs die voor een rapport beschikbaar zijn, kunt u ervoor kiezen een ingebouwde RDLC-rapportlay-out, een ingebouwde Word-rapportlay-out of een aangepaste lay-out te maken. Zie [Rapportlay-outs beheren](ui-manage-report-layouts.md) voor meer informatie over RDLC- en Word-rapportlay-outs, ingebouwde en aangepaste lay-outs.

Wanneer aangepaste rapportlay-outs zijn gedefinieerd, kunt u deze selecteren uit klant- en leverancierskaarten om op te geven dat de geselecteerde lay-outs worden gebruikt voor verschillende soorten documenten die u voor de betreffende klant of leverancier maakt. Zie voor meer informatie [Documentlay-outs definiëren voor klanten en leveranciers](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Documentrapporten (niet -lijsten) die een Word-rapportindeling gebruiken zijn meestal sneller dan rapporten die een RDLC-rapportindeling gebruiken. Als u dus kunt kiezen tussen een Word- of een RDLC-rapportindeling voor een documentrapport, gebruik dan de Word-rapportindeling voor de beste prestaties.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Wijzigen welke rapportlay-out moet worden gebruikt voor een rapport of document
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Selectie van rapportlay-out** in en kies de gerelateerde koppeling.  
   De pagina **Selectie van rapportlay-out** bevat een overzicht van alle rapporten die beschikbaar zijn voor het bedrijf dat in het veld **Bedrijf** boven aan de pagina wordt opgegeven. Met het veld **Geselecteerde lay-out** wordt de lay-out opgegeven die momenteel in het rapport wordt gebruikt.
2. Stel het veld **Bedrijf** boven aan de pagina in op het bedrijf dat het rapport bevat.
3. Als u de lay-out wilt wijzigen die door een rapport wordt gebruikt, stelt u in de rij voor het rapport het veld **Geselecteerde lay-out** in op een van de volgende opties:
   * **RDLC (ingebouwd)**, gebruikt de ingebouwde RDLC-rapportlay-out in het rapport.
   * **Word (ingebouwd)**, gebruikt de ingebouwde Word-rapportlay-out in het rapport.
   * **Aangepast**, gebruikt een aangepaste lay-out in het rapport.  

> [!NOTE]
> Als u een rapportlay-out van het type **RDLC (ingebouwd)** of **Word (ingebouwd)** kiest en een foutbericht krijgt dat het rapport geen lay-out van de opgegeven soort heeft, moet u een andere lay-outoptie kiezen of een aangepaste rapportlay-out maken van het soort dat u wilt gebruiken. Zie de volgende procedure.

Als u een ingebouwde RDLC- of Word-rapportlay-out hebt geselecteerd, is er verder geen actie vereist en wordt de lay-out gebruikt als het rapport de volgende keer wordt uitgevoerd.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>De aangepaste lay-out wijzigen die voor een rapportlay-out wordt gebruikt
Misschien wilt u ook de huidige gebruikte aangepaste lay-out wijzigen. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

Alle aangepaste rapportlay-outs die bestaan voor rapportlay-outs in een bedrijf, worden vermeld op de pagina **Aangepaste rapportlay-outs**. Op de pagina **Selectie van rapportlay-out** ziet u welke aangepaste lay-outs voor elk rapport beschikbaar zijn in het feitenblok **Aangepaste lay-outs**.

1. Kies op de pagina **Selectie van rapportlay-out**, op de regel voor de rapportlay-out die u wilt wijzigen, de opzoekknop in het veld **Aangepaste lay-outbeschrijving**.
2. Selecteer op de pagina **Aangepaste rapportlay-outs** de rij voor de aangepaste lay-out die u wilt gebruiken, en kies vervolgens de knop **OK**.

De naam van de geselecteerde aangepaste lay-out wordt nu weergegeven in het veld **Aangepaste lay-outbeschrijving** en deze wordt de volgende keer dat het rapport of document wordt bekeken, afgedrukt of verzonden, gebruikt.

U kunt nu naar uw klanten- en leverancierskaarten gaan om op te geven welke lay-outs u wilt gebruiken voor verschillende documenten die u voor de betreffende klant of leverancier maakt, zoals orderbevestigingen of betalingsherinneringen. Zie voor meer informatie [Documentlay-outs definiëren voor klanten en leveranciers](ui-define-customer-vendor-document-layouts.md).

## <a name="see-also"></a>Zie ook
[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
