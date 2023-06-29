---
title: Business Central waarden laten voorstellen
description: 'Als u handmatige berekeningen wilt voorkomen en taken snel en accuraat wilt voltooien, kunt u automatische gegevensinvoer instellen, zodat Business Central geselecteerde velden invult.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '39, 251, 981'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="letting--suggest-values"></a><a name="letting--suggest-values"></a>[!INCLUDE[prod_short](includes/prod_short.md)] waarden laten voorstellen
[!INCLUDE[prod_short](includes/prod_short.md)] kan u helpen taken sneller en correcter te voltooien door velden vooraf te vullen of regels te vullen met gegevens die u anders zelf moet berekenen en invoeren. Hoewel dergelijke automatische gegevensinvoer altijd correct is, kunt u deze later wijzigen als u wilt.

De functionaliteit waarmee veldwaarden voor u worden ingevoerd, wordt meestal aangeboden voor taken waarin u grote volumes transactiegegevens invoert en fouten wilt voorkomen en tijd wilt besparen. Dit onderwerp bevat een selectie van deze functionaliteit. In toekomstige updates van [!INCLUDE[prod_short](includes/prod_short.md)] worden meer secties toegevoegd.

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a><a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>Het selectievakje **Salderingsbedrag voorstellen** op de pagina **Fin. dagboekbatches**
Wanneer u bijvoorbeeld dagboekregels invoert voor meerdere uitgaven die allemaal naar dezelfde bankrekening moeten worden geboekt, kunt u telkens als u een nieuwe dagboekregel voor een uitgave invoert, het veld **Bedrag** op de bankrekeningregel automatisch laten bijwerken in het bedrag waarmee de uitgaven sluitend worden gemaakt. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie over het werken met diversendagboeken.

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a><a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Het veld **Bedrag** op salderingsdagboekregels automatisch laten invullen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Op de regel voor de dagboekbatch van uw voorkeur kiest u het selectievakje **Salderingsbedrag voorstellen**.
3. Open het dagboek en ga door met het registreren en boeken van transacties met de beschreven functie voor automatische invoer van een veldwaarde.       

Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie over het instellen van een persoonlijke dagboekbatch, bijvoorbeeld voor de verwerking van uitgaven.

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a><a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>Het veld **Ontvangstdatum automatisch invullen** op de pagina **Betalingsregistratie**
De pagina **Betalingsregistratie** bevat openstaande inkomende betalingen als regels die geboekte verkoopdocumenten vertegenwoordigen waar een betalingstermijn voor een bedrag is verstreken. Zie [Klantbetalingen vanuit een lijst met onbetaalde verkoopdocumenten handmatig reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) voor meer informatie over het vereffenen van klantbetalingen.

Uw hoofdacties op de pagina bestaan eruit het selectievakje **Is betaald** en het veld **Ontvangen op** in te vullen. U kunt [!INCLUDE[prod_short](includes/prod_short.md)] zo instellen dat automatisch een werkdatum in het veld **Ontvangen op** wordt ingevoerd wanneer u het selectievakje **Is betaald** inschakelt.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a><a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>Het veld **Ontvangen op** op de pagina **Betalingsregistratie** automatisch laten invullen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instelling van betalingsregistratie** in en kies vervolgens de gerelateerde koppeling.
2. Schakel het selectievakje **Ontvangstdatum automatisch invullen** in.
3. Open de pagina **Betalingregistratie** en ga door met het verwerken van inkomende klantbetalingen met de beschreven functie voor automatische invoer van een veldwaarde.

## <a name="see-also"></a><a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Financiën](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
