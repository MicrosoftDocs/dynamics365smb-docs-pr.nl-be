---
title: Een btw-aangifte instellen
description: In dit onderwerp wordt uitgelegd hoe u een sjabloon voor btw-aangiften en namen voor btw-aangiften instelt om te voldoen aan de veranderende vereisten van de belastingdienst.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="set-up-vat-statement-templates-and-vat-statement-names"></a><a name="set-up-vat-statement-templates-and-vat-statement-names"></a><a name="set-up-vat-statement-templates-and-vat-statement-names"></a>Sjablonen voor btw-overzichten en namen voor btw-aangiften instellen

De belastingdienst kan de vereisten om btw te boeken wijzigen en doet dat ook. Met sjablonen en namen voor btw-overzichten kunt u zich op de komende veranderingen voorbereiden en de overstap naar de nieuwe regels soepel maken. U kunt btw-aangiftesjablonen gebruiken om verschillende rapporten in te stellen wanneer u ervoor kiest de aangifte af te drukken. Elke btw-aangiftesjabloon kan meerdere btw-afschriftnamen hebben die op hun beurt de berekeningen definiëren, en u kunt een nieuwe btw-afschriftnaam maken wanneer de vereisten veranderen. Eén naam kan bijvoorbeeld btw voor dit jaar berekenen op basis van de huidige vereisten en een andere sjabloon kan btw berekenen op basis van vereisten voor volgend jaar. Namen zijn ook een manier om een historie te bewaren van btw-aangifte-indelingen, bijvoorbeeld, zodat u terug kunt kijken en kunt zien hoe u in vorige jaren btw hebt berekend.

## <a name="to-define-a-vat-statement"></a><a name="to-define-a-vat-statement"></a><a name="to-define-a-vat-statement"></a>Een btw-aangifte definiëren

Met btw-aangiften kunt u het btw-vereffeningsbedrag voor een bepaalde periode berekenen, bijvoorbeeld voor een kwartaal.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Btw-aangiften** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het veld **Naam** kies vervolgens **Nieuw** op de pagina **Btw-aangiftes**.
3. Vul de vereiste velden in. Gewoonlijk wilt u een instelling voor elke combinatie van btw-bedrijfsboekingsgroep en btw-productboekingsgroep hebben. Voor rijnummers is het logisch om equivalente nummers of codes te gebruiken zoals in uw officiële btw-overzicht [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> U kunt de gegevens filteren die het afschrift zal bevatten, afhankelijk van uw keuze in het veld **Soort**. **Rekeningsamentelling** is handig als u de btw van een bepaalde rekening wilt.
**Btw-postentotaal** haalt btw van de rekeningen die zijn toegewezen aan de selecties in de velden **Algemeen boekingssoort**, **Btw-bedr.-boekingsgroep** en/of **Btw-prod.-boekingsgroep**. Met **Vak-/Rubrieksamentelling** kunt u een waarde of snelfiltercriterium invoeren in het veld **Vak-/Rubrieksamentelling**. Zie voor meer informatie [Gegevens zoeken, filteren en sorteren](ui-enter-criteria-filters.md). **Omschrijving** wordt vaak gebruikt om een notitie aan de aangifte toe te voegen. U kunt het bijvoorbeeld gebruiken als een kop wanneer u vak/rubrieksamentelling gebruikt.

## <a name="to-preview-the-vat-statement"></a><a name="to-preview-the-vat-statement"></a><a name="to-preview-the-vat-statement"></a>Een voorbeeld van een btw-overzicht bekijken

Nadat u een btw-aangifte hebt gedefinieerd, kunt u er een voorbeeld van bekijken om te controleren of het aan uw wensen voldoet.
> [!Tip]
> Het is het best om één sectie in de btw-aangifte te hebben die **Type** **Btw-postentotaal** gebruikt en een andere sectie eronder die **Type** **Rekeningsamentelling** gebruikt, om de bedragen te reconciliëren op basis van de tabel **Btw-post** vergeleken met het bedrag in de **grootboekrekeningen**. U kunt ook het rapport **GB - Btw-reconciliatie** hiervoor gebruiken.

1. Kies **Voorbeeld**.
2. Voer een datumfilter in om de aangifte te beperken tot een specifieke periode. Zie voor meer informatie over het aanpassen van de pagina om het datumfilter weer te geven [Gegevens zoeken, filteren en sorteren](ui-enter-criteria-filters.md).
3. U kunt verschillende opties selecteren om het soort btw-posten aan te geven dat u in de aangifte wilt opnemen.
4. Op de regels waarop het veld **Soort** de waarde **Btw-postentotaal** bevat, kunt u een lijst zien met btw-posten door het bedrag in het veld **Bedrag** te kiezen.
5. U kunt personalisatie gebruiken om meer velden op de regels weer te geven. Bijvoorbeeld het ongerealiseerde basisbedrag en het ongerealiseerde btw-bedrag, als u ongerealiseerde btw gebruikt.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Btw instellen](finance-setup-vat.md)  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)  
[Btw-aangifte doen bij een belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Lokale functionaliteit in Business Central](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
