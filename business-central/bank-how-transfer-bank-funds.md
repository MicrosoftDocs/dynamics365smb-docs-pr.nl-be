---
title: Bankfondsen overboeken
description: 'U kunt bedragen overbrengen van de ene naar de andere bankrekening, inclusief andere valuta''s, door de transactie in het dagboek te boeken.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 04/29/2021
ms.author: edupont
---
# <a name="transfer-bank-funds" />Bankfondsen overboeken

Soms moet u een bedrag van de ene naar de andere bankrekening overboeken in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u dit wilt doen, moet u de transactie boeken op de pagina **Dagboek**. De taak verschilt afhankelijk van of de bankrekeningen dezelfde valuta gebruiken of niet.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code" />Een transfer boeken tussen bankrekeningen met dezelfde valutacode

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Dagboek** in en kies vervolgens de gerelateerde koppeling.
2. Vul op een dagboekregel de velden **Boekingsdatum** en **Documentnr.** in.
3. Selecteer in het veld **Rekeningsoort** de optie **Bankrekening**.
4. Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.
5. Voer in het veld **Bedrag** het bedrag in dat u wilt overbrengen.

    Vervolgens moet u de tegenrekening opgeven. Als u de relevante velden niet kunt zien, kiest u de actie **Meer kolommen weergeven** om alle beschikbare velden te bekijken.
6. Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.
7. Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.
8. Boek het dagboek.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes" />Transfers boeken tussen bankrekeningen met verschillende valutacodes

Als u gelden wilt overbrengen tussen bankrekeningen die verschillende valuta's gebruiken, moet u twee dagboekregels boeken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Dagboek** in en kies vervolgens de gerelateerde koppeling.
2. Maak twee dagboekregels en vul de velden **Boekingsdatum** en **Documentnr.** in.
3. Selecteer op de eerste dagboekregel **Bankrekening** in het veld **Soort**.
4. Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.
5. Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in, met of zonder minteken.

    > [!TIP]
    > Een bedrag zonder minteken is een debetbedrag, een bedrag met een minteken is een kredietbedrag.

    > [!NOTE]
    > Sommige bedrijven geven er de voorkeur aan om tussen rekeningen over te boeken op afzonderlijke dagboekregels. Andere bedrijven geven er de voorkeur aan om alles op één dagboekregel te boeken met behulp van een tegenrekening. Neem contact op met uw plaatselijke expert als u niet zeker weet wat u moet doen.
    >
    > Als uw bedrijf liever een tegenrekening gebruikt, stelt u het veld **Tegenrekeningsoort** in op **Bankrekening** en stelt u het veld **Tegenrekeningnr.** in op de bankrekening waarnaar u het geld wilt overboeken. Ga dan verder met stap 9 of 10.
    >
    > Als uw bedrijf liever een aparte dagboekregel gebruikt, gaat u verder met de volgende stap.
6. Selecteer op de tweede dagboekregel **Bankrekening** in het veld **Soort**.
7. Selecteer in het veld **Rekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.
8. Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in, met of zonder minteken.

    > [!TIP]
    > Een bedrag zonder minteken is een debetbedrag, een bedrag met een minteken is een kredietbedrag.
9. Als de gebruikte wisselkoersen in het dagboek verschillen van de wisselkoersen op de pagina **Valutawisselkoersen**, voert u een nieuwe dagboekregel in voor de wisselkoerswinsten of -verliezen.  

    1. Geef **Grootboekrekening** op in het veld **Rekeningsoort**.  

    2. Voer in het veld **Rekeningnr.** het grootboekrekeningnummer voor wisselkoerswinst of -verlies in.  

    3. Voer de wisselkoerswinsten of -verliezen in het veld **Bedrag** in, met of zonder minteken.

    > [!TIP]
    > Een bedrag zonder minteken is een debetbedrag, een bedrag met een minteken is een kredietbedrag.
10. Boek het dagboek.

## <a name="see-also" />Zie ook

[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
