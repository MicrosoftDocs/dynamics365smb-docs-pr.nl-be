---
title: Conversie voor bankgegevens instellen
description: 'U kunt bankrekeningen instellen om transacties bij te houden en bankfeeds, zoals Yodlee, te importeren of exporteren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>De extensie AMC Banking 365 Fundamentals instellen
Een algemene provider van services om betalingsgegevens naar elke willekeurige gegevensindeling te converteren die uw bank vereist, is verbonden en gereed om te worden ingeschakeld in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit wordt in [!INCLUDE[prod_short](includes/prod_short.md)] de extensie AMC Banking 365 Fundamentals genoemd.

U kunt betalingsregels uit de pagina **Betalingsdagboek** exporteren naar een bestand of een gegevensstroom die u vervolgens uploadt naar uw bank voor automatische verwerking, zodat u geen afzonderlijke elektronische betalingen hoeft te doen. Zie voor meer informatie [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

U kunt bankafschriftbestanden op de pagina **Betalingsreconciliatiedagboek** importeren door de extensie AMC Banking 365 Fundamentals te gebruiken om een bestand dat u van de bank ontvangt, te converteren naar een gegevensstroom die [!INCLUDE[prod_short](includes/prod_short.md)] kan importeren. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Als alternatief voor het importeren van bankafschriften met de extensie AMC Banking 365 Fundamentals kunt u de service Envestnet Yodlee Bank Feeds gebruiken. Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).

Als u bankbestanden wilt importeren of exporteren, moet u uw eigen bankrekening en de bankrekeningen van uw leveranciers instellen. Zie voor meer informatie [Bankrekeningen instellen](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> De extensie AMC Banking 365 Fundamentals kan een limiet stellen aan het aantal regels dat in één bestand kan worden geëxporteerd. Er wordt een foutbericht gestuurd als de limiet wordt overschreden. U wordt aangeraden alleen te werken met bankafschriftbestanden die maximaal 1000 regels bevatten omdat anders de verwerkingstijd in de extensie AMC Banking 365 Fundamentals beduidend kan toenemen.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Uw bedrijf aanmelden bij de extensie AMC Banking 365 Fundamentals
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instelling gegevensconv.service bank** in en kies vervolgens de gerelateerde koppeling.  
2. De pagina **Instelling gegevensconv.service bank** wordt geopend met drie vooraf ingevulde velden met relevante URL's van de provider van de extensie AMC Banking 365 Fundamentals.

    > [!NOTE]  
    >   In de demonstratiedatabase CRONUS International Ltd. worden de velden Gebruikersnaam en Wachtwoord vooraf gevuld met demo-aanmeldingsgegevens, die u vervangt door de werkelijke gegevens van uw bedrijf wanneer u zich aanmeldt bij de extensie AMC Banking 365 Fundamentals.
3. Kies in het veld **Inschrijvings-URL** de browserknop om de aanmeldingspagina van de serviceprovider te openen.  
4. Voer op de inschrijvingspagina van de serviceprovider van bankgegevens de gebruikersnaam en het wachtwoord in van het abonnement van uw bedrijf op de service en voltooi vervolgens het aanmeldingsproces volgens de instructies van de serviceprovider.

    Uw bedrijf is nu aangemeld bij de extensie AMC Banking 365 Fundamentals. Ga door met het invoeren van de gebruikersnaam en het wachtwoord, die u voor de service hebt opgegeven in de gerelateerde instellingsvelden in [!INCLUDE[prod_short](includes/prod_short.md)].

5. Voer op de pagina **Instelling gegevensconv.service bank** in het veld **Naam** dezelfde waarde in die u in stap 4 als aanmeldnaam op de pagina van de serviceprovider hebt ingevoerd.
6. Voer in het veld **Wachtwoord** dezelfde waarde in die u in stap 4 in het veld **Wachtwoord** op de pagina van de serviceprovider hebt ingevoerd.

> [!NOTE]  
> Uw aanmeldgegevens worden automatisch versleuteld.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>De lijst met momenteel ondersteunde bankgegevensindelingen weergeven of bijwerken
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instelling gegevensconv.service bank** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Instelling gegevensconv.service bank** de actie **Banknaam - Gegevensconversielijst** om de lijst met banknamen te openen die bankgegevensindelingen vertegenwoordigen die door de conversieservice worden ondersteund.
3. Kies op de pagina **Banknaam - Gegevensconversielijst** de actie **Banknaamlijst bijwerken**.

De lijst met indelingen voor bankgegevens die worden ondersteund door de extensie AMC Banking 365 Fundamentals, wordt nu bijgewerkt. Dit is de lijst met banknamen, gefilterd op land/regio, die u kunt selecteren vanuit het veld **Banknaam - Gegevensconversie** op de pagina **Bankrekeningkaart**.

> [!NOTE]  
>   De bijwerking van ondersteunde bankgegevensindelingen treedt ook op wanneer u een waarde selecteert of invoert in het veld **Banknaam - Gegevensconversie** voor de bankrekening.

Uw hebt zich nu aangemeld bij de extensie AMC Banking 365 Fundamentals. Ga verder om de inschrijvingsinformatie door te voeren voor elke bankrekening die de service zal gebruiken.

## <a name="see-also"></a>Zie ook
[Bankieren instellen](bank-setup-banking.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
