---
title: Door de gebruiker gedefinieerde VA-afschrijvingsmethoden instellen
description: In Business Central kunt u een door de gebruiker gedefinieerde afschrijvingsmethode toepassen om de afschrijvingsmethode van uw activum te definiëren op de pagina Vast activum.
author: jill-kotel-andersson
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a>Vaste activa instellen met door de gebruiker gedefinieerde afschrijvingsmethoden

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] gebruiken om de door de gebruiker gedefinieerde afschrijvingsmethoden in te stellen zoals hier beschreven.

Voor elke door de gebruiker gedefinieerde methode gebruikt u de pagina **Afschrijvingstabellen**, waarin u voor iedere periode (maand, kwartaal, jaar of boekhoudperiode) een afschrijvingspercentage moet opgeven. Wanneer u vervolgens een afschrijvingsboek met een door de gebruiker gedefinieerde methode toewijst aan een vast activum, moet u de velden **Datum 1e afschr. eigen def.** en **Begindatum afschr.** op de pagina **FA-afschrijvingsboeken** voor het specifieke vaste activum instellen.  

De formule voor het berekenen van de afschrijvingsbedragen luidt als volgt:  

*Afschrijvingsbedrag = (Afschrijvingen % x Aantal afschrijvingsdagen x Afschrijvingsbasis) / (100 x 360)*


> [!NOTE]  
> Terwijl de datum in het veld **Datum 1e afschr. eigen def.** wordt gebruikt om de tijdsintervallen te bepalen, is het de **Begindatum afschr.** die wordt gebruikt om het aantal afschrijvingsdagen te bepalen. Als de **Datum 1e afschr. eigen def.** vroeger is dan de **Begindatum afschr.**, wordt het percentage voor de eerste periode in de afschrijvingstabel slechts gedeeltelijk gebruikt bij het berekenen van de eerste afschrijving. Dit betekent dat het activum niet volledig afgeschreven is aan het einde van de laatste periode.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a>Een afschrijvingsboek toewijzen aan een vast activum met een door de gebruiker gedefinieerde afschrijvingsmethode

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum waarvoor u een afschrijvingsboek voor vaste activa wilt instellen.
3. Kies de actie **Gerelateerd** en kies dan **Vast activum** en dan **Afschrijvingsboeken**. Dit opent de pagina **VA-afschrijvingsboeken**.

   Standaard zijn enkele van de velden die moeten worden ingevuld volgens de onderstaande instructies verborgen, dus u moet ze weergeven. Hiervoor moet u de pagina personaliseren. Zie voor meer informatie [Een pagina personaliseren via de banner Personaliseren](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).
4. Selecteer in het veld **Afschrijvingsmethode** **Door gebruiker gedefinieerd**.
5. Selecteer in het veld **Code van afschrijvingstabel** de **afschrijvingstabel** die u wilt gebruiken.
6. Selecteer in het veld **Begindatum afschr.** de startdatum voor de afschrijvingsberekening.
7. Wanneer u een door de gebruiker gedefinieerde methode gebruikt, moet het veld **Datum 1e afschr. eigen def.** worden ingesteld op een datum die gelijk is aan of eerder is dan het veld **Begindatum afschr.**. Als u een waarde hebt geselecteerd in het veld **Periodelengte** in de afschrijvingstabel, moet de datum in het veld **Datum 1e afschr. eigen def.** de begindatum van een boekhoudperiode zijn.
8. Vul het veld **Aantal afschrijvingsjaren** in of het veld **Einddatum afschr.**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods"></a>Eigen afschrijvingsmethoden instellen

Op de pagina **Afschrijvingstabel** kunt u door de gebruiker gedefinieerde afschrijvingsmethoden instellen. U kunt bijvoorbeeld afschrijving instellen op basis van het aantal eenheden.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afschrijvingstabellen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Afschrijvingstabeloverzicht** de actie **Nieuw**.  
3. Vul op de pagina **Afschrijvingstabel** de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Gebruik de functie **Cijfersomtabel maken** om een afschrijvingstabel te definiëren op basis van de methode *Cijfersom*.

Met de methode *Cijfersom*, als een vast activum wordt afgeschreven over 4 jaar, dan wordt de afschrijving voor elk jaar als volgt berekend:

Cijfersom = 1 + 2 + 3 + 4 = 10 Afschrijving:

* Jaar 1 = 4/10  
* Jaar 2 = 3/10  
* Jaar 3 = 2/10  
* Jaar 4 = 1/10  

### <a name="depreciation-based-on-number-of-units"></a>Afschrijving op basis van aantal eenheden

Deze eigen methode kan ook worden gebruikt om af te schrijven op basis van het aantal eenheden, bijvoorbeeld in het geval van productiemachines met een vastgestelde capaciteit gedurende hun levensduur. Op de pagina **Afschrijvingstabellen** kunt u het aantal eenheden invullen dat per periode (maand, kwartaal, jaar of boekhoudperiode) kan worden geproduceerd.  

### <a name="example---user-defined-depreciation"></a>Voorbeeld - door gebruiker ingestelde afschrijving

U gebruikt een afschrijvingsmethode waarmee u activa versneld kunt afschrijven (omdat u hierdoor minder inkomstenbelasting hoeft te betalen).  

Voor een vast activum dat u van de belastingdienst in drie jaar mag afschrijven, kunt u de volgende afschrijvingspercentages gebruiken:  

* Jaar 1: 25%  
* Jaar 2: 38%  
* Jaar 3: 37%  

De aanschafkosten bedragen LV 100.000 en de afschrijfbare levensduur is vijf jaar. De afschrijving wordt jaarlijks berekend.  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 01/01/20 |Aanschafkosten |(Begindatum afschrijving) |100,000.00 |100,000.00 |
| 12/31/20 |Afschrijvingen |360 |-25.000,00 |75,000.00 |
| 12/31/21 |Afschrijvingen |360 |-38.000,00 |37,000.00 |
| 12/31/22 |Afschrijvingen |360 |-37.000,00 |0 |
| 12/31/23 |Afschrijvingen |Geen |Geen |0 |
| 12/31/24 |Afschrijvingen |Geen |Geen |0 |

In het vorige voorbeeld worden de velden **Datum 1e afschr. eigen def.** en **Begindatum afschr.** ingesteld op 01/01/20 op de pagina **FA-afschrijvingsboeken** voor het specifieke vaste activum. Als het veld **Datum 1e afschr. eigen def.** echter de datum 01-01-20 bevat en het veld **Begindatum afschr.** de datum 01-04-20, dan zou het resultaat als volgt zijn:  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 01/01/20 |Aanschafkosten |(Begindatum afschrijving) |100,000.00 |100,000.00 |
| 12/31/20 |Afschrijvingen |270 |-18.750,00 |81,250.00 |
| 12/31/21 |Afschrijvingen |360 |-38.000,00 |42,250.00 |
| 12/31/22 |Afschrijvingen |360 |-37.000,00 |6,250.00 |
| 12/31/23 |Afschrijvingen |90 |-6.250,00 |0 |
| 12/31/24 |Afschrijvingen |Geen |Geen |0 |


## <a name="see-also"></a>Zie ook
[Vaste activa instellen](fa-setup.md)  
[Vaste activa](fa-manage.md)  
[Afschrijving van vaste activa instellen](fa-how-setup-depreciation.md)  
[Afschrijvingsmethoden voor vaste activa](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
