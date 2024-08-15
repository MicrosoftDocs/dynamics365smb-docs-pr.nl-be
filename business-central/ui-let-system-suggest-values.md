---
title: Business Central waarden laten voorstellen
description: 'Als u handmatige berekeningen wilt voorkomen en taken snel en accuraat wilt voltooien, kunt u automatische gegevensinvoer instellen, zodat Business Central geselecteerde velden invult.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '39, 251, 981'
ms.date: 07/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Laat [!INCLUDE[prod_short](includes/prod_short.md)] waarden suggereren
[!INCLUDE[prod_short](includes/prod_short.md)] kan u helpen taken sneller en correcter te voltooien door velden vooraf te vullen of regels te vullen met gegevens die u anders zelf moet berekenen en invoeren. Hoewel dergelijke automatische gegevensinvoer altijd correct is, kunt u deze later wijzigen als u wilt.

De functionaliteit waarmee veldwaarden voor u worden ingevoerd, wordt meestal aangeboden voor taken waarin u grote volumes transactiegegevens invoert en fouten wilt voorkomen en tijd wilt besparen. Dit artikel bevat een selectie van dergelijke functionaliteiten. In toekomstige updates van [!INCLUDE[prod_short](includes/prod_short.md)] worden meer secties toegevoegd.

## Het selectievakje **Salderingsbedrag voorstellen** op de pagina **Fin. dagboekbatches**
Wanneer u bijvoorbeeld algemene dagboekregels invoert voor meerdere uitgaven die allemaal op dezelfde bankrekening moeten worden geboekt, kunt u elke keer dat u een nieuwe dagboekregel voor een uitgave invoert, het veld  **bedrag** op de bankrekeningregel automatisch laten bijwerken met het bedrag waarmee de uitgaven in evenwicht zijn. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie over het werken met diversendagboeken.

### Het veld **Bedrag** op salderingsdagboekregels automatisch laten invullen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Op de regel voor de dagboekbatch van uw voorkeur kiest u het selectievakje **Salderingsbedrag voorstellen**.
3. Open het dagboek en ga door met het registreren en boeken van transacties met de beschreven functie voor automatische invoer van een veldwaarde.       

Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie over het instellen van een persoonlijke dagboekbatch, bijvoorbeeld voor de verwerking van uitgaven.

## Het veld **Ontvangstdatum automatisch invullen** op de pagina **Betalingsregistratie**
Op de pagina  **Klantbetalingen registreren**  worden openstaande inkomende betalingen weergegeven als regels die verkoopdocumenten vertegenwoordigen waarop een bedrag betaald moet worden. Zie [Klantbetalingen vanuit een lijst met onbetaalde verkoopdocumenten handmatig reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) voor meer informatie over het vereffenen van klantbetalingen.

De belangrijkste acties die u op deze pagina uitvoert, zijn het invullen van het selectievakje  **Betaling verricht**  en het veld  **Ontvangstdatum** . U kunt [!INCLUDE[prod_short](includes/prod_short.md)] zo instellen dat automatisch een werkdatum in het veld **Ontvangen op** wordt ingevoerd wanneer u het selectievakje **Is betaald** inschakelt.

### Het veld **Ontvangen op** op de pagina **Betalingsregistratie** automatisch laten invullen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instelling van betalingsregistratie** in en kies vervolgens de gerelateerde koppeling.
2. Schakel het selectievakje **Ontvangstdatum automatisch invullen** in.
3. Open de pagina  **Klantbetalingen registreren**  en ga verder met het verwerken van binnenkomende klantbetalingen met behulp van de beschreven functionaliteit voor automatische invoer van een veldwaarde.

## Zie ook
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Financiën](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]