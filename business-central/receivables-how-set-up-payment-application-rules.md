---
title: Regels voor automatische vereffening van betalingen
description: Lees over het instellen van regels voor de automatische vereffening van betalingen op de pagina Regels betalingsvereffening.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-rules-for-automatic-application-of-payments" />Regels instellen voor automatische vereffening van betalingen

Op de pagina **Regels betalingsvereffening** stelt u de regels in die bepalen hoe betalingstekst (op een banktransactie) automatisch moet worden afgestemd met de gerelateerde openstaande (onbetaalde) facturen, creditnota's of andere posten wanneer u de functie **Automatisch vereffenen** gebruikt in het venster **Betalingsreconciliatiedagboek**. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

U stelt nieuwe betalingsvereffeningsregels in door te bepalen welke soorten gegevens op een dagboekregel van een betalingsreconciliatie met gegevens op een of meer openstaande posten moeten overeenstemmen voordat de gerelateerde betaling automatisch wordt vereffend met de openstaande posten. De kwaliteit van elke automatische vereffening wordt weergegeven als een waarde van **Laag** tot **Hoog** in het veld **Zekerheid afstemming** op de pagina **Betalingsreconciliatiedagboek** op basis van de regel voor betalingsvereffening die is gebruikt.

Elke rij op de pagina **Regels betalingsvereffening** staat voor een betalingsvereffeningsregel. Regels worden toegepast in de volgorde die wordt opgegeven door het veld **Sorteervolgorde**. Als er meerdere regels tegelijk worden gebruikt, wordt de afstemmingszekerheid van de hoogste gesorteerde regel gebruikt.

De automatische vereffeningsfunctie is gebaseerd op afstemmingscriteria in een prioriteitsvolgorde. Eerst probeert de functie, in volgorde van prioriteit, tekst in de vijf **Gerelateerde partij**-velden op een dagboekregel af te stemmen met tekst in de bankrekening, de naam of het adres van klanten of leveranciers met onbetaalde documenten die openstaande posten vertegenwoordigen. Vervolgens probeert de functie tekst in de velden **Transactietekst** en **Aanvullende transactie-informatie** af te stemmen met een dagboekregel met tekst in de velden **Extern documentnummer** en **Documentnummer** bij openstaande posten. Ten slotte probeert de functie het bedrag in het veld **Afschrifttotaal** op een dagboekregel af te stemmen met het bedrag op openstaande posten.

> [!NOTE]
> Tekstafstemming is alleen mogelijk voor tekst die langer is dan vier tekens.

Behalve de afstemmingscriteria is het volgende van toepassing met betrekking tot het teken voor het betalingsbedrag:

- Voor negatieve bedragen wordt eerst afgestemd met openstaande posten die klantfacturen vertegenwoordigen, en vervolgens met creditnota's van leveranciers.
- Voor positieve bedragen wordt eerst een afstemming uitgevoerd met openstaande posten die leveranciersfacturen vertegenwoordigen en dan met creditnota's van klanten.

## <a name="to-set-up-a-payment-application-rule" />Een betalingsvereffeningsregel instellen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Regels betalingsvereffening** in en kies vervolgens de gerelateerde koppeling.
2. Definieer een nieuwe of bewerkte betalingsvereffeningsregel door de velden op een regel in te vullen, zoals beschreven in de volgende tabel.

|Veld|Omschrijving|
|-|-|
|**Zekerheid afstemming**|Geeft aan hoe zeker u bent over de vereffeningsregel die u op de regel definieert. <br /></br>Een waarde die u in dit veld opgeeft, wordt in het veld **Zekerheid afstemming** op de pagina **Betalingsreconciliatiedagboek** weergegeven, afhankelijk van de kwaliteit van de automatische betalingsvereffening op de dagboekregel.|
|**Prioriteit**|Geeft de prioriteit aan van de vereffeningsregel in verhouding tot andere vereffeningsregels die als regels zijn gedefinieerd op de pagina **Regels betalingsvereffening**. 1 is de hoogste prioriteit.|
|**Gerelateerde partij afgestemd**|Geeft op hoeveel gegevens over de klant of leverancier, zoals adres, plaats en bankrekeningnummer, op de dagboekregel van de betalingsreconciliatie met gegevens op de openstaande post moeten overeenkomen voordat de vereffeningsregel wordt gebruikt om de betaling automatisch te vereffenen met de openstaande post.|
|**Doc.nr./extern documentnr. afgestemd**|Hiermee wordt opgegeven of tekst op de regel van het betalingsreconciliatiedagboek moet overeenkomen met de waarde in het veld **Documentnummer** of het veld **Extern documentnummer** in de openstaande post voordat de vereffeningsregel wordt gebruikt om de betaling automatisch met de openstaande post te vereffenen.|
|**Bedrag incl. tolerantie afgestemd**|Geeft aan hoeveel posten voor een klant of leverancier moeten overeenkomen met het bedrag inclusief betalingstolerantie voordat de vereffeningsregel wordt gebruikt om automatisch een betaling toe te passen op de openstaande post.|
|**Controle vereist**|Geeft aan of de automatische betalingstoepassing wordt aanbevolen voor handmatige beoordeling door de gebruiker voordat wordt gepost. Het kiezen van het veld **Te controleren regels** veld op de pagina **Betalingsvereffeningsjournaal** start een begeleide ervaring waarin u gemakkelijk meerdere vereffeningen achter elkaar kunt beoordelen op de pagina **Controle van betalingsvereffening**.|

De volgende tabel beschrijft de standaardregels voor betalingsvereffening in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Important]
> De regels voor betalingsvereffening kunnen in uw implementatie van [!INCLUDE[prod_short](includes/prod_short.md)] verschillen.

| Zekerheid afstemming | Prioriteit | Gerelateerde partij afgestemd | Doc.nr./extern documentnr. Afgestemd | Bedrag incl. tolerantie afgestemd |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Hoog             | 1        | Volledig                 | Ja - Meerdere                 | Eén overeenkomst                      |
| Hoog             | 2        | Volledig                 | Ja - Meerdere                 | Meerdere overeenkomsten               |
| Hoog             | 3        | Volledig                 | Ja                            | Eén overeenkomst                      |
| Hoog             | 4        | Volledig                 | Ja                            | Meerdere overeenkomsten               |
| Hoog             | 5        | Gedeeltelijk             | Ja - Meerdere                 | Eén overeenkomst                      |
| Hoog             | 6        | Gedeeltelijk             | Ja - Meerdere                 | Meerdere overeenkomsten               |
| Hoog             | 7        | Gedeeltelijk             | Ja                            | Eén overeenkomst                      |
| Hoog             | 8        | Volledig                 | Nee                             | Eén overeenkomst                      |
| Hoog             | 9        | Nee                    | Ja - Meerdere                 | Eén overeenkomst                      |
| Hoog             | 10       | Nee                    | Ja - Meerdere                 | Meerdere overeenkomsten               |
| Gemiddeld           | 1        | Volledig                 | Ja - Meerdere                 | Niet in aanmerking genomen                 |
| Gemiddeld           | 2        | Volledig                 | Ja                            | Niet in aanmerking genomen                 |
| Gemiddeld           | 3        | Volledig                 | Nee                             | Meerdere overeenkomsten               |
| Gemiddeld           | 4        | Gedeeltelijk             | Ja - Meerdere                 | Niet in aanmerking genomen                 |
| Gemiddeld           | 5        | Gedeeltelijk             | Ja                            | Niet in aanmerking genomen                 |
| Gemiddeld           | 6        | Nee                    | Ja                            | Eén overeenkomst                      |
| Gemiddeld           | 7        | Nee                    | Ja - Meerdere                   | Niet in aanmerking genomen                 |
| Gemiddeld           | 8        | Gedeeltelijk             | Nee                             | Eén overeenkomst                      |
| Gemiddeld           | 9        | Nee                    | Ja                            | Niet in aanmerking genomen                 |
| Laag              | 1        | Volledig                 | Nee                             | Geen overeenkomsten                     |
| Laag              | 2        | Gedeeltelijk             | Nee                             | Meerdere overeenkomsten               |
| Laag              | 3        | Gedeeltelijk             | Nee                             | Geen overeenkomsten                     |
| Laag              | 4        | Nr.                    | Nr.                             | Eén overeenkomst                      |
| Laag              | 5        | Nr.                    | Nr.                             | Meerdere overeenkomsten               |

## <a name="see-related-microsoft-trainingtrainingmodulesreconciliation-journals-dynamics-365-business-centralindex" />Zie gerelateerde [Microsoft-training](/training/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also" />Zie ook
[Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
