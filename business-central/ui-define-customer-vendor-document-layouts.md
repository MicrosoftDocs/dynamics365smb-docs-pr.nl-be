---
title: Speciale documentlay-outs toewijzen aan klanten of leveranciers | Microsoft Docs
description: Wanneer aangepaste rapportlay-outs zijn gedefinieerd, kunt u deze selecteren uit klant- en leverancierskaarten om op te geven dat de geselecteerde lay-outs worden gebruikt voor verschillende soorten documenten die u voor de betreffende klant of leverancier maakt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 086491f30ef0a223e5bf8a559af26b848e54d344
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773567"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Documentlay-outs definiëren voor klanten en leveranciers
Wanneer aangepaste rapportlay-outs zijn gedefinieerd, kunt u deze selecteren uit klant- en leverancierskaarten om op te geven welke lay-outs worden gebruikt voor verschillende soorten documenten die u voor de betreffende klant of leverancier maakt. De waarde in het veld **Gebruik** definieert voor welk proces de documentlay-out wordt gebruikt, zoals **Aanmaning**, **Verzending** en **Bevestiging**.

Naast het instellen van de lay-outs die voor welk document moeten worden gebruikt, kunt u tijd besparen bij het verzenden van documenten naar verschillende klant- of leverancierscontacten door de e-mailadressen van specifieke contacten in te stellen voor gebruik met specifieke documenten. Klantafschriften worden bijvoorbeeld verzonden naar accountantcontacten, verkooporders naar de kopers van uw klanten en inkooporders naar verkopers of accountmanagers van leveranciers.

Wanneer u een documentlay-out definieert voor een klant of leverancier, kunt u ook het e-mailadres opgeven van de contactpersoon die het document moet ontvangen. U kunt dit snel doen met de functie **E-mail selecteren vanuit contacten**, die automatisch filtert op contact-e-mailadressen die zijn geregistreerd voor de betreffende klant of leverancier.

Voordat u kunt definiëren welke documentlay-out wordt gebruikt voor welke processen en naar welke contactpersoon het document moet worden verzonden, moet u alle beschikbare rapporten (documenten) laden vanaf de pagina **Selecties rapporteren**. U kunt dit snel doen met de functie **Kopiëren uit rapportselectie**.

Hieronder wordt beschreven hoe u lay-outs van verkoopdocumenten vanaf een klantenkaart kunt definiëren. De stappen zijn hetzelfde voor lay-outs voor inkoopdocumenten van een leverancierskaart.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Alle beschikbare verkoopdocumenten voor een klant inschakelen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de kaart van de klant voor wie u documentlay-outs per bedrijfsproces wilt definiëren.
3. Kies op de pagina **Klantenkaart** de pagina **Documentlay-outs**.
4. Kies op de pagina **Documentlay-outs** de actie **Kopiëren uit rapportselectie**.

De pagina **Documentlay-outs** voor de klant in kwestie is gevuld met alle rapportlay-outs voor verkoop die in het systeem bestaan. Zie voor meer informatie over hoe ze zijn gemaakt [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

U kunt nu doorgaan met het aanpassen van de lijst met aangepaste rapportlay-outs of e-mailadressen voor de contactpersonen waarnaar de documenten moeten worden verzonden.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Een aangepaste rapportlay-out selecteren om te gebruiken voor de lay-out van het verkoopdocument
Als voor een of meer van de rapportlay-outs die zijn gedefinieerd op de pagina **Documentlay-outs** voor de klant, geen aangepaste rapportlay-out is gedefinieerd, kunt u dat snel doen.

1. Kies op de pagina **Documentlay-outs** op de regel voor een rapportlay-out waarvoor u een aangepaste lay-out wilt gebruiken, het veld **Aangepaste lay-outbeschrijving**. Het veld wordt ingevuld als de klantlay-out al is geselecteerd of leeg is.
2. Selecteer op de pagina **Aangepaste rapportlay-outs** de speciale documentlay-out die u wilt gebruiken voor het betreffende verkoopdocumenttype. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Instellen welk contact welke documentlay-out voor een klant ontvangt
U kunt tijd besparen bij het verzenden van documenten naar verschillende klanten of contactpersonen van leveranciers door contact-e-mailadressen op te geven op de verschillende regels op de pagina **Documentlay-outs**. Klantafschriften kunnen bijvoorbeeld worden verzonden naar accountantcontacten, verkooporders naar de kopers van uw klanten en inkooporders naar verkopers of accountmanagers van leveranciers.

1. Kies op de pagina **Documentlay-outs** op de regel voor een rapportlay-out die u naar een specifiek contact voor de klant wilt verzenden, de actie **E-mail selecteren vanuit contacten**.
2. Selecteer op de pagina **Contacten** de regel voor het relevante contact en kies vervolgens de knop **OK**.

Het e-mailadres van de contactpersoon wordt nu ingevoegd op de documentlay-outregel, zodat het verkoopdocument in kwestie, bijvoorbeeld aanmaningen, altijd naar die contactpersoon in het bedrijf van de klant wordt verzonden.

## <a name="see-also"></a>Zie ook  
[Aangepaste rapportlay-outs bijwerken](ui-update-report-layouts.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Een aangepaste indeling voor een rapport of document importeren of exporteren](ui-how-import-and-export-report-layout.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]