---
title: Aangepaste rapportlay-outs bijwerken
description: 'Leer hoe u een aangepaste rapportlay-out kunt bijwerken die in een rapport wordt gebruikt, bijvoorbeeld wanneer er ontwerpwijzigingen zijn in de gegevensset van het rapport.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9652, 9650'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="legacy-update-custom-report-layouts"></a>(verouderd) Aangepaste rapportlay-outs bijwerken

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Soms moet u een aangepaste rapportlay-out die voor een rapport is gebruikt, bijwerken. Dit is vereist als er een ontwerpverandering in de gegevensset van het rapport is geweest, bijvoorbeeld een veld dat in de lay-out wordt gebruikt maar uit de gegevensset van het rapport is verwijderd. Als voor een rapportlay-out bijwerken vereist is, krijgt u een foutbericht wanneer u probeert een voorbeeld van het rapport te bekijken of het rapport af te drukken of op te slaan.  

U kunt een rapportlay-out automatisch bijwerken vanuit het foutbericht dat wordt weergegeven wanneer u het rapport uitvoert. In dat geval kiest u de knop **Ja** in het foutbericht. In geavanceerde of actieve rapporten kunt u bepaalde rapportlay-outs of alle aangepaste rapportlay-outs bijwerken die mogelijk zijn beïnvloed door wijzigingen in gegevenssets.  

U kunt ook updates testen zonder de vereiste wijzigingen toe te passen op de aangepaste rapportlay-outs. Zo kunt u bekijken welke wijzigingen worden toegepast op de rapportlay-out, en mogelijke problemen in het proces opsporen. Vanuit de testresultaten kunt u de aangepaste rapportlay-outs direct openen om mogelijke problemen te verhelpen. Het wordt aangeraden om de update van de rapportlay-out te testen voordat u de wijzigingen toepast.  

Niet alle wijzigingen in de gegevensset van rapporten kunnen automatisch worden bijgewerkt in de rapportlay-outs. Voor sommige wijzigingen moet u handmatig de rapportlay-out bewerken. Voor meer informatie. zie [Beperking voor update van aangepaste rapportlay-out](ui-update-report-layouts.md#UpdateLimitations),  

## <a name="to-update-one-or-more-custom-report-layouts"></a>Een of meer aangepaste rapportlay-outs bijwerken

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Selectie rapportlay-out** in en kies vervolgens de gerelateerde koppeling.  

2.  Als u een bepaald rapport wilt bijwerken, selecteert u deze lay-out in de lijst op de pagina **Selectie rapportlay-out** en kiest u de actie **Lay-out bijwerken**. Als u alle aangepaste rapportlay-outs voor het bedrijf wilt bijwerken, kiest u de actie **Alle lay-outs bijwerken**.  

Als zich geen fouten voordoen, worden de updates toegepast op de rapportlay-outs. Als zich fouten voordoen, verschijnt er een bericht waarin de fouten worden aangegeven. U moet de aangepaste rapportlay-out dan handmatig bewerken om de fout te verhelpen. Zie [Fouten corrigeren](ui-update-report-layouts.md#FixErrors) voor meer informatie.  

## <a name="to-test-custom-report-layout-updates"></a>Updates van aangepaste rapportlay-outs testen

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Selectie rapportlay-out** in en kies vervolgens de gerelateerde koppeling.  

2.  Kies op de pagina **Selectie van rapportlay-out** de actie **Testlay-outupdates**.  

 Wijzigingen in de rapportlay-outs worden getest, maar niet toegepast op de werkelijke rapportlay-outs. De pagina **Bijwerklogboek rapportlay-out** verschijnt waarin de status van potentiële updates voor elke rapportlay-out wordt aangegeven. Als er fouten voor een rapportlay-out zijn, kunt u de rapportlay-out van het bericht direct benaderen en bewerken om eventuele problemen te verhelpen. Zie [Fouten corrigeren](ui-update-report-layouts.md#FixErrors) voor meer informatie.  

## <a name="limitations-of-the-custom-report-layout-update"></a><a name="UpdateLimitations"></a>Beperking voor update van aangepaste rapportlay-out
 Er zijn verschillende soorten wijzigingen die de automatische update kan toepassen op aangepaste rapportlay-outs, bijvoorbeeld als een veld dat in de lay-out wordt gebruikt, in verwijderd uit de gegevensset van het rapport. De automatische update kan de volgende wijzigingen in de gegevensset van een rapport echter bijwerken.  

1.  Verwijderde velden, labels of gegevensitems.  

2.  Dubbele veldnamen in de rapportlay-out nadat de naam van een veld in de gegevensset is gewijzigd. Dit moet worden behandeld als een ontwerpfout.  

3.  Upgradescenario's met meerdere iteraties van een rapportlay-out die tot gevolg hebben dat namen van dezelfde velden, labels of gegevensitems meerdere keren worden gewijzigd.  

 Als tijdens het updateproces een van deze problemen wordt gedetecteerd, kan de update niet worden toegepast. U moet de problemen handmatig verhelpen, bijvoorbeeld door de rapportlay-out te bewerken in Word, of programmatisch met behulp van upgrade-codeunits.  

## <a name="fixing-errors"></a><a name="FixErrors"></a>Fouten corrigeren
 Als er een foutbericht verschijnt tijdens het bijwerken of testen van updates van de rapportlay-out, moet u waarschijnlijk de rapportlay-out wijzigen om het probleem op te lossen. Zie de foutmelding om de oorzaak van het probleem te achterhalen.  

 Het meest voorkomende probleem is dat een veld dat in de lay-out wordt gebruikt, uit de rapportgegevensset is verwijderd. In dit geval ziet u een regel in het foutbericht die zegt dat er een artikel is verwijderd. Als u dit probleem wilt oplossen, moet u de lay-out wijzigen en het desbetreffende veld verwijderen.  

 Zie voor meer informatie [Een aangepaste lay-out voor een rapport maken](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  

Nadat u de lay-out hebt gewijzigd, probeert u de lay-out opnieuw bij te werken.  

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
 [Rapportlay-outs beheren](ui-manage-report-layouts.md)  
 [Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
