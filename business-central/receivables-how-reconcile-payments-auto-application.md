---
title: Betalingen reconciliëren met automatische vereffening
description: Beschrijft hoe u betalingen kunt reconciliëren via automatische vereffening om betalingen of kasontvangsten te vereffenen met de gerelateerde open posten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '389, 1290, 1294, 1287'
ms.date: 06/22/2022
ms.author: bholtorf
---
# <a name="reconcile-payments-using-automatic-application" />Betalingen reconciliëren met automatische vereffening

De pagina **Betalingsreconciliatiedagboek** specificeert betalingen, zowel inkomend als uitgaand, die zijn geregistreerd als transacties op uw online bankrekening of op een betalingsservice. U kunt de betalingen vereffenen met gerelateerde openstaande klant-, leveranciers- en bankrekeningposten. Vul de regels in het dagboek in door een bankafschrift te importeren als een bankfeed of bestand of door handmatig transacties in te voeren die u via uw betalingsservice doet.

> [!NOTE]
> De pagina biedt automatische afstemmingsfunctionaliteit waarmee betalingen worden vereffend met de gerelateerde open posten op basis van een afstemming van gegevens op een bankafschriftregel (dagboekregel) met gegevens in een of meer open posten. U kunt de voorgestelde automatische vereffeningen overschrijven en u kunt ervoor kiezen helemaal geen automatische vereffening te gebruiken. Zie stap 7 voor meer informatie.

Een betalingsreconciliatiedagboek is gerelateerd aan één bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)]. De bankrekening vertegenwoordigt de online bankrekening waarop de betalingstransacties worden geregistreerd. Eventuele open bankrekeningposten die gerelateerd zijn aan de vereffende klant- of leveranciersposten, worden gesloten wanneer u de actie **Betalingen boeken en bankrekening reconciliëren** kiest. De bankrekening wordt automatisch gereconcilieerd voor betalingen die u met het dagboek boekt.

Als u de pagina **Betalingsreconciliatiedagboek** gebruikt om klantbetalingen te registreren en te vereffenen, kunt u het dagboek instellen om een specifieke nummerreeks te gebruiken. Daarna kunt u de nummerreeks opgeven in het veld **Nummerreeks van betalingsreconciliatie** op een bankrekening. Het gebruik van een speciale nummerreeks kan het gemakkelijker maken om posten te identificeren die via het dagboek zijn geboekt.

Net als bij andere dagboeken kunt u bij het corrigeren van geboekte posten op de pagina **Grootboekregister** posten tegenboeken die zijn geboekt via het betalingsreconciliatiedagboek. Zo wilt bijvoorbeeld wellicht posten tegenboeken voor betalingen die u met de verkeerde klant hebt vereffend. U moet eerst het vereffenen van de geboekte klantposten ongedaan maken. Vervolgens kunt u de actie **Journaal tegenboeken** op de pagina **Grootboekregister** gebruiken om het dagboek tegen te boeken dat de betalingen heeft geboekt. Als alternatief kunt u op de pagina **Geboekte dagboeken** de actie **Geselecteerde regels naar dagboek kopiëren** gebruiken om specifieke regels van het geboekte betalingreconciliatiedagboek tegen te boeken. 

Wanneer u automatische vereffening gebruikt, herkent [!INCLUDE[prod_short](includes/prod_short.md)] bankposten die al zijn geboekt, wat dubbele boekingen helpt voorkomen.

U kunt banktransacties importeren als .csv-bankbestanden of in een andere indeling die uw bank biedt. Als u bankafschriften als bankfeeds wilt importeren, moet u eerst een speciale bankintegratieservice instellen en vervolgens de bankrekening aan de gerelateerde online bankrekening koppelen. Het dagboek van de betalingreconciliatie detecteert vervolgens automatisch bankfeeds wanneer u de actie **Banktransacties importeren** kiest. Bovendien kunt u een bankrekening zo instellen dat automatisch elk uur nieuwe bankafschriftfeeds worden geïmporteerd. Transacties voor betalingen die reeds zijn geboekt als vereffend en/of gereconcilieerd worden niet geïmporteerd. U kunt die transacties ophalen met de Envestnet Yodlee Bank Feeds-service, die in sommige landversies van [!INCLUDE[d365fin](includes/d365fin_md.md)] vooraf is geïnstalleerd. Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md). Ook kan een Microsoft-partner u helpen voldoen aan uw zakelijke of landvereisten.

Met de actie **Tekst afstemmen op rekening** kunt u toewijzingen instellen tussen tekst op betalingen en specifieke debet-, credit- en tegenrekeningen zodat dergelijke betalingen worden geboekt naar de opgegeven rekeningen wanneer u het betalingsreconciliatiedagboek boekt. Toewijzing is bijvoorbeeld nuttig voor periodieke ontvangsten of kosten, zoals regelmatige aankopen van autobrandstof of bankkosten en -rente, die regelmatig voorkomen op het bankafschrift en geen gerelateerd bedrijfsdocument nodig hebben. (Zie stap 10) Zie [Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.

Dagboekregels hebben mogelijk geen voorgestelde vereffening, wat om verschillende redenen kan gebeuren. Zo kan bijvoorbeeld een document ontbreken of heeft een klant te veel betaald, waardoor er een te hoog bedrag ontstaat nadat de betaling met een andere dagboekregel is vereffend. Voor dergelijke gevallen kunt u de actie **Verschil overboeken naar rekening** gebruiken om de ontbrekende grootboekpost te creëren en te boeken, bijvoorbeeld voor een terugbetaling, die nodig is om de betaling mee te vereffenen. (Zie stap 11) Zie [Betalingen reconciliëren die niet kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) voor meer informatie.

U gebruikt de functie **Automatisch vereffenen** automatisch wanneer u een bankbestand of -feed met betalingstransacties importeert of wanneer u de functie activeert, om betalingen te vereffenen met de gerelateerde openstaande posten op basis van een afstemming van tekst op een bankafschriftregel (dagboekregel) met tekst in een of meer openstaande posten. Deze automatisering is gebaseerd op regels die u definieert op de pagina **Regels betalingsvereffening**, waar u ook definieert of een toepassingssuggestie moet worden beoordeeld. Zie [Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md) voor meer informatie.

Op dagboekregels waar een betaling automatisch is vereffend met een of meer openstaande posten, heeft het veld **Zekerheid afstemming** de waarde **Laag**, **Gemiddeld** of **Hoog** om de kwaliteit aan te geven van de gegevensafstemming waarop de voorgestelde betalingsvereffening is gebaseerd.

Sommige betalingsvereffeningen vereisen uw beoordeling zoals gedefinieerd door de gebruikte afstemmingsregel, zoals regels met afstemmingszekerheid **Laag**. Andere regels vereisen uw beoordeling en handmatige wijziging omdat er een waarde in het veld **Verschil** staat. Om een of meer betalingsvereffeningen te bekijken kiest u het veld **Te controleren regels** of **Regels met verschil**, onderaan. De pagina **Controle van betalingsvereffening** wordt geopend met alle relevante informatie over de klant of leverancier waarmee de betaling wordt vereffend, de overeenkomstdetails en acties om de regel te verwerken, zoals de actie **Vereffening accepteren**. (Zie stappen 7 en 8)

Voor elke dagboekregel op de pagina **Dagboek betalingsreconciliatie** kunt u de pagina **Betalingsvereffening** openen om alle openstaande kandidaatposten voor de betaling te zien en gedetailleerde informatie voor elke post weer te geven over de gegevensafstemming waarop een betalingsvereffening wordt gebaseerd. Hier kunt u handmatig betalingen vereffenen of betalingen die automatisch met een verkeerde post zijn vereffend, opnieuw vereffenen. (Zie stap 10) Zie [Betalingen controleren of vereffenen na automatische vereffening](receivables-how-review-apply-payments-auto-application.md) voor meer informatie.

> [!NOTE]  
> U kunt het importeren van banktransacties starten op het moment dat u de pagina **Betalingsreconciliatiedagboek** opent voor een bestaand dagboek. In de volgende procedure wordt beschreven hoe u banktransacties importeert op de pagina **Dagboek betalingsreconciliatie** nadat u een nieuw dagboek hebt gemaakt.

## <a name="to-reconcile-payments-using-automatic-application" />Betalingen reconciliëren met automatische vereffening
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsreconciliatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Als u in een nieuw betalingsreconciliatiedagboek wilt werken, kiest u de actie **Nieuw dagboek**.
3. Selecteer op de pagina **Bankrekeninglijst betaling** de bankrekening waarvoor u betalingen wilt vereffenen en kies vervolgens de knop **OK**.
   De pagina **Dagboek betalingsreconciliatie** wordt geopend en is voorbereid op de geselecteerde bankrekening.
4. Kies de actie **Banktransacties importeren**.
   Als de bankrekening voor het geselecteerde dagboek niet is ingesteld voor het importeren van banktransacties, zal [!INCLUDE[d365fin](includes/d365fin_md.md)] u daarbij helpen.
5. Selecteer op de pagina **Te importeren bestand selecteren** het bestand dat banktransacties voor betalingen bevat die u wilt reconciliëren, en kies vervolgens de knop **Openen**.  
6. Als de Envestnet Yodlee Bank Feeds-service is ingeschakeld, wordt op de pagina **Bankafschriftfilter** die automatisch wordt geopend, het datuminterval opgegeven voor de bankafschriften die moeten worden geïmporteerd.

    De pagina **Dagboek betalingsreconciliatie** wordt gevuld met regels voor betalingen die banktransacties in het bankafschrift vertegenwoordigen.

     Op regels voor betalingen die automatisch zijn vereffend met gerelateerde openstaande posten, geeft het veld **Zekerheid afstemming** de kwaliteit aan van de gegevensafstemming waarop de voorgestelde betalingsvereffening is gebaseerd. Bovendien bevatten de velden **Rekeningnaam**, **Rekeningtype** en **Rekeningnr.** informatie over de klant of leverancier waarmee de betaling wordt vereffend.

    De automatische vereffeningen, de overeenkomstkwaliteiten en of regels moeten worden beoordeeld, worden bepaald door regels. U kunt de regels bewerken om de resultaten aan te passen. Zie [Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md) voor meer informatie.

7. Als u meerdere betalingsvereffeningen wilt accepteren/verwijderen of handmatig wilt wijzigen die een waarde in het veld **Verschil** hebben, kiest u de actie **Regels met verschil**, onderaan.

    De pagina **Controle van betalingsvereffening** wordt geopend met de eerste vereffening die moet worden gecontroleerd. De volgende te beoordelen vereffening wordt op de pagina weergegeven terwijl u de vorige verwerkt. De controle omvat informatie over de klant of leverancier waarmee de betaling wordt vereffend, de overeenkomstdetails en de acties om de regel te verwerken, zoals de actie **Vereffening accepteren** en de actie **Handmatig vereffenen**.

8. Als u meerdere betalingsvereffeningen die door de regel zijn ingesteld om te worden beoordeeld, wilt bekijken, kiest u de actie **Te controleren regels**. 

9. Als u een automatische vereffening wilt wijzigen, selecteert u een dagboekregel en kiest u vervolgens op de pagina **Betalingsvereffening** de actie **Handmatig vereffenen** om de betaling handmatig te vereffenen of opnieuw te vereffenen. Zie [Betalingen controleren of vereffenen na automatische vereffening](receivables-how-review-apply-payments-auto-application.md) voor meer informatie.

10. Selecteer een niet-vereffende dagboekregel voor een periodieke ontvangst of periodieke kosten, zoals een aankoop van autobenzine, en kies vervolgens de actie **Tekst afstemmen op rekening**. Zie [Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.

    Wanneer u de toewijzing van betalingstekst aan rekeningen hebt voltooid, kiest u de actie **Handmatig vereffenen**.

    Wanneer een tekst-naar-rekening toewijzing is ingesteld, bevat de resulterende automatische betalingsvereffening **Hoog - Toewijzing tekst aan rekening** in het veld **Zekerheid afstemming**.

11. Als een dagboekregel geen voorgestelde vereffening heeft omdat er geen post bestaat waarmee deze kan worden vereffend, kiest u de actie **Verschil overboeken naar rekening** om de ontbrekende grootboekpost te maken en te boeken die nodig is om de betaling mee te vereffenen. Zie [Betalingen reconciliëren die niet kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) voor meer informatie.

12. Als er geen regels meer hoeven te worden beoordeeld en het veld **Verschil** leeg is op alle regels, kiest u de actie **Boeken** en kiest u vervolgens een van de volgende opties:

    - **Betalingen boeken en bankrekening reconciliëren** - Om de betalingen te boeken als vereffend en ook de gerelateerde bankposten te sluiten als gereconcilieerd.
    - **Alleen betalingen boeken** - Om alleen de betalingen te boeken als vereffend, maar de gerelateerde bankrekeningposten open te laten. Vereist dat u de bankrekening afzonderlijk reconcilieert, bijvoorbeeld: zie [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie.
    - **Testrapport** - Als u het resultaat van de boeking wilt controleren voordat u boekt. Het rapport **Bankrekeningafschrift** wordt geopend en bevat dezelfde velden als de onderzijde van de pagina **Betalingsreconciliatiedagboek**.

Wanneer u het betalingreconciliatiedagboek boekt, worden de vereffende open posten gesloten. De klant-, leveranciers- of grootboekrekeningen worden bijgewerkt. Voor betalingen op dagboekregels die zijn gebaseerd op tekst-aan-rekening toewijzing, worden de opgegeven klant-, leveranciers- en grootboekrekeningen bijgewerkt. Voor alle dagboekregels worden bankposten gemaakt. Als u de actie **Betalingen boeken en bankrekening reconciliëren** kiest, worden eventuele open bankrekeningposten gesloten die zijn gerelateerd aan de vereffende klant- of leveranciersposten. Dit betekent dat de bankrekening automatisch wordt gereconcilieerd voor betalingen die u met het dagboek boekt.

U kunt de waarde in het veld **Saldo op bankrekening na boeking** met de waarde in het veld **Eindsaldo afschrift** vergelijken om te traceren wanneer de bankrekening wordt gereconcilieerd op basis van betalingen die u boekt.

> [!NOTE]  
>   Als u de bankrekening vanuit de pagina **Betalingsreconciliatiedagboek** niet wilt reconciliëren, moet u de pagina **Bankreconciliatie** gebruiken. Zie [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie.

## <a name="see-related-microsoft-trainingtrainingmodulesuse-journals-dynamics--business-central" />Zie gerelateerde [Microsoft-training](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
