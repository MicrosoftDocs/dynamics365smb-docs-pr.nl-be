---
title: Kosten of inkomsten rechtstreeks in grootboek registreren
description: 'Voor bedrijfsactiviteiten waarbij geen document betrokken is, kunt u op de pagina Financieel dagboek transacties maken.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Transacties direct naar het grootboek boeken

Met diversendagboeken kunt u financiële transacties direct naar grootboekrekeningen en andere rekeningen boeken, zoals bank-, klant-, leveranciers- en werknemersrekeningen.  

Een veelvoorkomend gebruik van het dagboek is onkosten van werknemers tijdens zakelijke activiteiten te boeken, voor terugbetaling. Zie voor meer informatie [Onkosten van werknemers vastleggen en terugbetalen](finance-how-record-reimburse-employee-expenses.md).

Dagboeken boeken financiële transacties direct naar grootboekrekeningen en andere rekeningen zoals bank-, klant-, leveranciers- en werknemersrekeningen. Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen. Posten worden zelfs gemaakt als u bijvoorbeeld een dagboekregel naar een klantrekening boekt, omdat een post via een boekingsgroep is geboekt naar een rekening met vorderingen in het grootboek. U kunt uw versie van een dagboek aanpassen door een dagboekbatch of -sjabloon in te stellen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.

Voor posten die u samen met documenten boekt, is een creditnotaproces vereist. Boekingen die u bij het dagboek boekt, kunt u echter wel storneren. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

## Een transactie direct naar het grootboek boeken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open de relevante dagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul op een nieuwe dagboekregel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Herhaal stap 3 voor alle afzonderlijke transacties die u wilt boeken.

    > [!TIP]  
    > Als u meerdere transactieregels vóór één tegenrekeningsregel wilt invoeren, bijvoorbeeld, voor één bankrekening, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**. Het veld **Bedrag** op de tegenrekeningsregel wordt automatisch ingevuld met de waarde die nodig is om de transacties in balans te brengen.
5. Kies de actie **Boeken** om de transacties op de betreffende grootboekrekeningen te registreren.

## Zie ook

[Werken met dagboeken](ui-work-general-journals.md)  
[Kosten van werknemers registreren en terugbetalen](finance-how-record-reimburse-employee-expenses.md)  
[Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]