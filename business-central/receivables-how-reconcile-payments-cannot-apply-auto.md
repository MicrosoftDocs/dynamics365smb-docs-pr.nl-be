---
title: Gebruik de functie Verschil overboeken naar rekening om betalingen te verzoenen
description: 'Beschrijft hoe u betalingen verwerkt die niet aan een document kunnen worden toegewezen, bijvoorbeeld wanneer een wisselkoers ervoor zorgt dat bedragen afwijken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="reconcile-payments-that-cant-be-applied-automatically"></a>Betalingen die niet automatisch kunnen worden toegepast, afstemmen
Soms moet u betalingen naar uw bankrekening verwerken die niet kunnen worden toegepast op een gerelateerde openstaande klant-, leverancier- of bankrekeningpost. Redenen hiervoor kunnen zijn dat er geen document bestaat [!INCLUDE[prod_short](includes/prod_short.md)] waarop de betaling kan worden toegepast, of dat het gerelateerde document [!INCLUDE[prod_short](includes/prod_short.md)] een ander bedrag heeft dan het transactiebedrag, bijvoorbeeld vanwege een wisselkoers. Op de pagina  **Betalingsverzoeningsdagboek** worden alle transactiebedragen voor betalingen die nog niet zijn toegepast, weergegeven in het veld  **Verschil**, inclusief bedragen die om bovenstaande redenen niet kunnen worden toegepast.

De methoden om dit soort niet-vereffende betalingen op te lossen:
* Handmatig vereffenen
* Toewijzing van tekst aan rekening gebruiken
* Een te hoog bedrag overmaken naar een journaalregel om de vereiste boeking te creëren en te boeken, zoals een terugbetaling van een te veel betaald bedrag.

Betalingen die niet kunnen worden toegepast, kunnen op de volgende verschillende manieren op de regels van het betalingsreconciliatiejournaal worden weergegeven:

* De waarde in het veld **Verschil** is gelijk aan de waarde in het veld **Transactiebedrag**, waarmee wordt aangegeven dat er geen gedeelte van de betaling kan worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost.
* De waarde in het veld **Verschil** is lager dan de waarde in het veld **Transactiebedrag**, waarmee wordt aangegeven dat een gedeelte van de betaling kan worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost. Het resterende deel van de betaling kan niet worden toegepast en moet handmatig worden afgestemd of rechtstreeks op een rekening worden geboekt.

Als u dergelijke betalingen wilt reconciliëren, kunt u de actie **Verschil overboeken naar rekening** kiezen en vervolgens opgeven naar welke rekening het bedrag in het veld **Verschil** wordt geboekt wanneer u het dagboek van de betalingsreconciliatie boekt. U kunt dit doen via de pagina **Betalingsreconciliatiedagboek** of vanaf de pagina **Controle van betalingsvereffening**, die u opent door de waarde in het veld **Zekerheid afstemming** te kiezen of door het veld **Verschil** te kiezen.

> [!TIP]  
>   Er bestaat een vergelijkbare functionaliteit om automatische reconciliatie van terugkerende betalingen in te stellen die niet kunnen worden vereffend met gerelateerde openstaande klant-, leveranciers- of bankrekeningposten. Zie [Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.

## <a name="to-reconcile-payments-that-cant-be-applied-automatically"></a>Om betalingen te verzoenen die niet automatisch kunnen worden toegepast
1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsreconciliatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open een betalingreconciliatiedagboek. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).
3. Kies **Verschil overboeken naar rekening**. De pagina **Verschil overboeken naar rekening** wordt geopend.
4. Geef in het veld **Rekeningsoort** het soort rekening op waarnaar het betalingsbedrag wordt geboekt.
5. Geef in het veld **Rekeningnr.** de rekening op waarnaar het betalingsbedrag wordt geboekt.
6. Geef in het veld **Omschrijving** de tekst op waarmee deze directe betalingsboeking wordt omschreven. Standaard wordt de tekst in het veld **Transactietekst** op de dagboekregel van de betalingsreconciliatie ingevoegd.
7. Kies de knop **Ok**.

Als de waarde in het veld **Verschil** gelijk is aan de waarde in het veld **Transactiebedrag** als u het dagboek van de betalingsreconciliatie boekt, wordt de volledige betaling op de dagboekregel rechtstreeks naar de opgegeven tegenrekening geboekt.

Als de waarde in het veld **Verschil** lager is dan de waarde in het **Transactiebedrag**, wordt een extra dagboekregel gemaakt met dezelfde tekst en datum en met het verschil ingevoegd in het veld **Transactiebedrag**. Op de oorspronkelijke dagboekregel wordt het verschil afgetrokken van de waarde van het veld **Transactiebedrag** en blijft de betaling vereffend met de gerelateerde klant-, leveranciers- of bankrekeningpost. Wanneer u het dagboek van de betalingsreconciliatie boekt, wordt één deel van de betaling als een vereffende betaling geboekt. Het andere gedeelte van de betaling wordt direct naar de opgegeven rekening geboekt.

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
