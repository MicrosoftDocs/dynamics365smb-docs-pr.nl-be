---
title: De termijnen en niveaus van aanmaningen instellen
description: 'Leer hoe u Business Central zo instelt dat u een aanmaning aan een klant kunt verzenden over een betaling die achterstallig is, en kosten aan de betaling kunt toevoegen vanwege de vertraging.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-reminder-terms-and-levels"></a>De termijnen en niveaus van aanmaningen instellen

U kunt aanmaningen gebruiken om klanten te herinneren aan openstaande bedragen en om betaling te verzoeken. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Nadat u de aanmaningstermijnen en -niveaus hebt ingesteld, kunt u deze opnemen in geautomatiseerde processen voor het maken, afgeven en verzenden van aanmaningen. Ga voor meer informatie over het geautomatiseerde proces naar [Aanmaningen in incasso's automatiseren](finance-automate-reminders.md).

## <a name="reminder-terms"></a>Aanmaningscondities

Als klanten betalingen hebben openstaan, moet u bepalen wanneer en hoe u hen wilt aanmanen. Daarnaast kunt u hun rekening eventueel debiteren met rente of kosten. U kunt zoveel aanmaningscondities instellen als u wilt.  

> [!NOTE]
> Als u rente wilt berekenen op te late betalingen, kunt u dit doen wanneer u aanmaningen maakt. Als u echter alleen rente wilt berekenen en u uw klanten hiervan op de hoogte wilt stellen zonder een aanmaning te verzenden, gebruikt u een [rentefactuur](finance-setup-finance-charges.md). Zie voor meer informatie [Aanmaningen](receivables-collect-outstanding-balances.md#reminders) of [Financiële kosten](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="set-up-attachment-and-email-body-texts-for-communications"></a>Bijlagen en e-mailteksten voor communicatie instellen

Op de pagina **Instellen van aanmaningstermijnen** kunt u bijlageteksten en standaard e-mailberichten instellen die u voor alle aanmaningsniveaus kunt gebruiken, of kunt u voor elk niveau specifieke berichten maken. Het bericht dat u voor het eerste aanmaningsniveau verzendt, kan bijvoorbeeld een andere toon of inhoud hebben dan het tweede of derde niveau. Als u bijlagen en e-mailberichtteksten voor alle niveaus wilt maken, kiest u **Klantcommunicatie** boven aan de pagina. Als u berichten voor specifieke regels wilt maken, kiest u op het sneltabblad **Aanmaningsniveau** een regel en kiest u vervolgens de actie **Klantcommunicatie** op het sneltabblad.

Standaard wordt voor bijlagen en e-mailteksten uw taalinstelling gebruikt. Als u echter aanmaningen naar klanten in andere landen verzendt, wilt u wellicht in andere talen communiceren. U kunt teksten maken voor elke taal die door [!INCLUDE [prod_short](includes/prod_short.md)] wordt ondersteund door de actie **Tekst toevoegen voor taal** te gebruiken. Zorg er dan voor dat de talen voor bijlageteksten en e-mailteksten hetzelfde zijn. Als deze niet overeenkomen en de aanmaningstermijn meer dan één niveau heeft, kan de automatisering het bericht mogelijk niet aanpassen voor een of meer niveaus. Om te controleren of de talen overeenkomen, gebruikt u de actie **Overzicht van communicatie** en vergelijkt u de communicatie voor de teksten.

Wanneer u een e-mail verzendt, bestaat de aanmaning uit een rapport dat u bij de e-mail voegt. U definieert het rapport waarmee de aanmaning wordt gegenereerd op de pagina **Rapportselecties - Aanmaning/rentefactuur**, waar u ook het rapport selecteert dat de hoofdtekst van de e-mail bevat in het veld **Naam van lay-out van hoofdtekst van e-mailbericht**. Wanneer u e-mails naar uw klanten verzendt, worden de teksten op het sneltabblad **E-mailtekst** ingevoegd in het rapport dat is geselecteerd in het veld **Naam van lay-out van hoofdtekst van e-mailbericht**. Het standaardrapport heeft een tekstveld voor deze tekst. Als u wilt, kunt u dit rapport bewerken, bijvoorbeeld om inhoud toe te voegen of te verwijderen. Bewerk de lay-out van deze rapporten op de pagina **Rapportlay-outs**. Ga voor meer informatie over rapportlay-outs naar [Aan de slag met het maken van rapportlay-outs](ui-get-started-layouts.md).

> [!NOTE]
> Als u rechtstreeks vanuit [!INCLUDE [prod_short](includes/prod_short.md)] per e-mail wilt communiceren, moet u dat hebben ingesteld. Ga voor meer informatie over het verbinden van e-mailaccounts met [!INCLUDE [prod_short](includes/prod_short.md)] naar [E-mail instellen](admin-how-setup-email.md).

### <a name="set-up-reminder-terms"></a>Aanmaningstermijnen instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningscondities** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Als u meer dan één combinatie van aanmaningscondities wilt gebruiken, stelt u een code in voor elke.

## <a name="reminder-levels"></a>Aanmaningsniveaus

Voor elke aanmaningstermijn kunt u een onbeperkt aantal aanmaningsniveaus definiëren, hoewel de meeste bedrijven slechts twee of drie niveaus gebruiken. De instelling van niveau 1 wordt gebruikt als er voor het eerst een aanmaning wordt gemaakt voor een klant. Wanneer de aanmaning wordt verstuurd, wordt het niveau geregistreerd in de aanmaningsposten die worden gemaakt en gekoppeld aan de individuele klantposten. Als het nodig is om de klant nog eens aan te manen, worden alle aanmaningposten die zijn gekoppeld aan open klantposten gecontroleerd op wat het hoogst gebruikte niveau is. De voorwaarden van het volgende niveau worden dan gebruikt voor de nieuwe aanmaning.

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
7. Als u automatisch gerelateerde waarden in de resulterende tekst wilt invoegen, kunt u de volgende tijdelijke aanduidingen in het veld **Tekst** invoeren.  

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

    Als u bijvoorbeeld **U bent %9 %7 verschuldigd op %2.** schrijft, bevat de aanmaning de volgende tekst: **U bent USD 1,200.50 verschuldigd op 02-02-2024.**.

    > [!NOTE]
    > In [!INCLUDE [prod_short](includes/prod_short.md)] wordt de vervaldatum berekend op basis van de datumformule die u invoert. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#use-date-formulas).

8. Als u de taal voor een e-mailbericht wilt opgeven, kiest u de actie **Tekst voor taal toevoegen**. Het veld **Taalcode** wordt bijgewerkt om uw selectie weer te geven. Voer op het sneltabblad **E-mailtekst** de inhoud van het bericht in de geselecteerde taal in.

Nadat u de aanmaningstermijnen hebt ingesteld, kunt u deze op de klantkaartpagina's aan klanten toewijzen. Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Zie ook

[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Aanmaningen voor uitstaande saldi verzenden](receivables-send-reminders.md)  
[Rentefactuurcondities instellen](finance-setup-finance-charges.md)  
[Financiën instellen](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
