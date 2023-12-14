---
title: De termijnen en niveaus van aanmaningen instellen
description: 'Leer hoe u Business Central zo instelt dat u een aanmaning aan een klant kunt verzenden over een betaling die achterstallig is, en kosten aan de betaling kunt toevoegen vanwege de vertraging.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 02/09/2022
ms.author: bholtorf
---
# <a name="set-up-reminder-terms-and-levels"></a>De termijnen en niveaus van aanmaningen instellen

U kunt aanmaningen gebruiken om klanten te herinneren aan openstaande bedragen. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a>Aanmaningscondities

Als klanten betalingen hebben openstaan, moet u bepalen wanneer en hoe u hen wilt aanmanen. Daarnaast kunt u hun rekening eventueel debiteren met rente of kosten. U kunt zoveel aanmaningscondities instellen als u wilt.  

> [!NOTE]
> Als u rente wilt berekenen op te late betalingen, kunt u dit doen wanneer u aanmaningen maakt. Als u echter alleen rente wilt berekenen en u uw klanten hiervan op de hoogte wilt stellen zonder aanmaningen te versturen, moet u [rentefacturen](finance-setup-finance-charges.md) gebruiken. Zie voor meer informatie [Aanmaningen](receivables-collect-outstanding-balances.md#reminders) of [Financiële kosten](receivables-collect-outstanding-balances.md#finance-charges), respectievelijk.

### <a name="to-set-up-reminder-terms"></a>U kunt aanmaningscondities als volgt instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Aanmaningscondities** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Als u meer dan één combinatie van aanmaningscondities wilt gebruiken, stelt u een code in voor elke.

## <a name="reminder-levels"></a>Aanmaningsniveaus

Voor elke aanmaningsconditiecode kunt u een onbeperkt aantal aanmaningsniveaus definiëren. De instelling van niveau 1 wordt gebruikt als er voor het eerst een aanmaning wordt gemaakt voor een klant. Wanneer de aanmaning wordt verstuurd, wordt het niveau geregistreerd in de aanmaningsposten die worden gemaakt en gekoppeld aan de individuele klantposten. Als het nodig is om de klant nog eens aan te manen, worden alle aanmaningposten die zijn gekoppeld aan open klantposten gecontroleerd op wat het hoogst gebruikte niveau is. De voorwaarden van het volgende niveau worden dan gebruikt voor de nieuwe aanmaning.

Als u meer aanmaningen maakt dan waar u niveaus voor hebt gedefinieerd, worden de voorwaarden van het hoogste niveau gebruikt. U kunt zoveel aanmaning maken als ingesteld in het veld **Max. aantal aanmaningen** in de aanmaningscondities.

### <a name="to-set-up-reminder-levels"></a>Aanmaningsniveaus volgt instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Aanmaningscondities** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Aanmaningscondities** de regel met de condities waarvoor u niveaus wilt instellen en kies vervolgens de actie **Niveaus**.  
3. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > De instelling van het veld de **Rente berekenen** bepaalt of rente op de aanmaning zal verschijnen wanneer de aanmaning wordt verzonden. Het veld **Rente boeken** op de pagina **Aanmaningscondities** bepaalt echter of de berekende rente moet worden geboekt naar grootboek- en klantrekeningen.
    >
    > Om aan te geven dat rente moet worden berekend, kiest u het veld **Rente berekenen**.

    Geef desgewenst voor elk aanmaningsniveau extra kosten op in zowel LV als in vreemde valuta. U kunt allerlei toeslagen in vreemde valuta's definiëren voor elke code op de pagina **Aanmaningsniveaus**.  

    De extra kosten kunnen op drie verschillende manieren worden berekend, die worden bepaald door de waarde van het veld **Toeslag berekeningssoort**.  

    - **Vast**

        Kosten worden berekend op basis van de waarden van de **Toeslag-** velden op de regel voor het aanmaningsniveau zelf.  
    - **Dynamisch enkel**

        Kosten worden berekend op basis van de waarden van de velden op de relevante regel op de pagina **Instellingen voor toeslag** voor dat aanmaningsniveau.
    - **Dynamisch samengevoegd**

        Kosten worden berekend op basis van de waarden van de velden op de gecombineerde regels op de pagina **Instellingen voor toeslag** voor dat aanmaningsniveau.

4. Kies de actie **Valuta's**.
5. Definieer op de pagina **Valuta's voor aanmaningsniveau** voor elke aanmaningsniveaucode en corresponderend aanmaningsniveaunummer een valutacode en een toeslag.

    > [!NOTE]  
    > De valutacondities die u hier hebt ingesteld, worden gebruikt wanneer u aanmaningen maakt in een vreemde valuta. Als u geen condities voor aanmaningen in vreemde valuta's hebt ingesteld, worden de condities die op de pagina **Aanmaningsniveau** zijn ingesteld, gebruikt en vervolgens omgerekend naar de betreffende valuta.

    Voor elk aanmaningsniveau kunt u tekst specificeren die wordt afgedrukt vóór (**Begintekst**) of na (**Eindtekst**) in de posten op de aanmaning.

6. Kies respectievelijk de acties **Begintekst** of **Eindtekst** en vul de pagina **Aanmaningstekst** in.
7. Als u automatisch gerelateerde waarden in de resulterende aanmaningstekst wilt invoegen, voert u de volgende tijdelijke aanduidingen in het veld **Tekst** in.  

    |Tijdelijke aanduiding|Waarde|  
    |-----------------|-----------|  
    |%1|Inhoud van het veld **Documentdatum** in de aanmaningskop|  
    |%2|Inhoud van het veld **Vervaldatum** in de aanmaningskop|  
    |%3|Inhoud van het veld **Rente** in de relateerde rentefactuurcondities|  
    |%4|Inhoud van het veld **Restbedrag** in de aanmaningskop|  
    |%5|Inhoud van het veld **Rentebedrag** in de aanmaningskop|  
    |%6|Inhoud van het veld **Toeslag** in de aanmaningskop|  
    |%7|Het totaalbedrag van de aanmaning|  
    |%8|Inhoud van het veld **Aanmaningsniveau** in de aanmaningskop|  
    |%9|Inhoud van het veld **Valutacode** in de aanmaningskop|  
    |%10|Inhoud van het veld **Boekingsdatum** in de aanmaningskop|  
    |%11|De bedrijfsnaam|  
    |%12|Inhoud van het veld **Toeslag per regel** in de aanmaningskop|  

    Als u bijvoorbeeld schrijft **U bent %9 %7 verschuldigd op %2.**, bevat de resulterende aanmaning de volgende tekst: **U bent USD 1,200.50 verschuldigd op 02-02-2014**.

    > [!NOTE]
    > De vervaldatum wordt berekend op basis van de datumformule die u invoert. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#use-date-formulas).

Nadat u de aanmaningscondities hebt ingesteld (met aanvullende niveaus en tekst), voert u een van de codes in op elke klantenkaart. Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Zie ook

[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Aanmaningen voor uitstaande saldi verzenden](receivables-send-reminders.md)  
[Rentefactuurcondities instellen](finance-setup-finance-charges.md)  
[Financiën instellen](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
