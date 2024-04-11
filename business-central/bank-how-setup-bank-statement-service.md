---
title: Yodlee Bank Feeds instellen
description: U kunt betalingsgegevens naar elke gegevensindeling converteren die uw bank vereist en het exporteren of importeren van bankbestanden inschakelen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Yodlee, feed, stream, payment process'
ms.search.form: '1280, 1290'
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>De service Envestnet Yodlee Bank Feeds instellen

U kunt elektronische bankafschriften van uw bank importeren om snel de pagina **Betalingsreconciliatiedagboek** te vullen, zodat u betalingen kunt vereffenen en de bankrekening kunt reconciliëren. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!IMPORTANT]
> Vanwege de nieuwe Payment Services Directive in Europa (PSD2) kunt u na 14 september 2019 niet langer automatisch bankafschriften van banken in het Verenigd Koninkrijk importeren in [!INCLUDE[prod_short](includes/prod_short.md)]. We onderzoeken de mogelijkheid om deze functie in de toekomst opnieuw aan te bieden.

> [!NOTE]
> De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de online versie van Business Central. Deze functionaliteit wordt niet ondersteund voor on-premises versies van [!INCLUDE [prod_short](includes/prod_short.md)], of voor [!INCLUDE [prod_short](includes/prod_short.md)]-omgevingen die worden gehost op ingesloten ISV-toepassingsservices. Als u deze functionaliteit on-premises wilt gebruiken, moet u een cobrand-account verkrijgen van Envestnet en moet u code toevoegen om te integreren met de Yodlee API.
>
> De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de VS en Canada.
> Alleen banken die in deze landen/regio's zijn gevestigd, worden ondersteund, ook al kunnen banken uit andere landen/regio's ook worden vermeld in het bankselectievenster van Envestnet Yodlee Bank Feeds in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> Neem voor technische assistentie met de Envestnet Yodlee-functionaliteit contact op met Microsoft Support. Neem geen contact op met Envestnet Yodlee. Zie voor meer informatie [Technische ondersteuning configureren voor Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/technical-support).

De Envestnet Yodlee Bank Feeds-service wordt geïnstalleerd als een extensie voor [!INCLUDE[prod_short](includes/prod_short.md)] online en kan worden ingeschakeld in de ondersteunde landen/regio's. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met extensies](ui-extensions.md).

Nadat u de bankfeedservice hebt ingeschakeld, moet u een bankrekening koppelen aan de online bankrekening waar de feed vandaan zal komen. U koppelt bankrekeningen aan online bankrekeningen in de volgende scenario's:

* Er bestaat geen bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] voor uw online bankrekening. Daarom kunt u de bankrekening maken door te koppelen vanuit de online bankrekening.
* Er bestaat een bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)], die u aan een online bankrekening wilt koppelen.
* Een gekoppelde bankrekening moet worden ontkoppeld omdat u de bankfeedservice niet meer voor de rekening wilt gebruiken.
* Online bankrekeningen zijn gewijzigd en u wilt de informatie over bankrekeningen bijwerken in [!INCLUDE[prod_short](includes/prod_short.md)] .

Als de bankfeedservice is ingeschakeld, kunt u een bankrekening instellen om elke twee uur automatisch nieuwe bankafschriften te importeren op de pagina **Betalingsreconciliatiedagboek**. Transacties voor betalingen die reeds zijn geboekt als vereffend en/of gereconcilieerd op de pagina **Betalingsreconciliatiedagboek**, worden niet geïmporteerd. Zie voor meer informatie het gedeelte “Automatische import van bankafschriften inschakelen”.

> [!NOTE]  
> Als u de begeleide instelling Bedrijf instellen gebruikt, worden sommige stappen in de volgende procedures automatisch uitgevoerd wanneer u de instelling van de bedrijfsbankrekening uitvoert. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md).

## <a name="to-enable-the-bank-feed-service"></a>De bankfeedservice inschakelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Open de bankrekening die u voor de bankfeedservice gebruikt.
3. Selecteer op de pagina **Bankrekeningkaart** in het veld **Importindeling van bankafschrift** YODLEEBANKFEED.  

De bankfeedservice wordt ingeschakeld als u een bankrekening koppelt aan de gerelateerde online bankrekening. Zie de volgende procedure.  

> [!NOTE]
> Als u de begeleide instelling **Bedrijfsinstelling** gebruikt, schakelt u de service in door het selectievakje **Een bankfeedservice gebruiken** te selecteren. Zie voor meer informatie [Nieuwe bedrijven maken in Business Central](about-new-company.md).

## <a name="to-create-a-new-linked-bank-account"></a>Een nieuwe gekoppelde bankrekening maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de betreffende bankrekening en kies vervolgens **Nieuwe gekoppelde bankrekening maken**. De pagina **Bankrekening koppelen** opent na een aantal ogenblikken.

    > [!NOTE]  
    > Deze pagina toont de daadwerkelijke webpagina van de Envestnet Yodlee Bank Feeds-service. De terminologie en functionaliteit op de pagina komen mogelijk niet overeen met de instructies in dit onderwerp.  
3. Gebruik op de pagina **Koppeling aan online bankrekening** in het deelvenster **Rekening koppelen** de zoekfunctie om de bank te zoeken waar u een of meer online bankrekeningen hebt.
4. Kies de banknaam. Het deelvenster **Aanmelden** wordt geopend.
5. Voer de gebruikersnaam en het wachtwoord in die u gebruikt om u aan te melden bij de online bank en kies vervolgens de knop **Volgende**.  
6. De bankfeedservice treft voorbereidingen om de eerste online bankrekening bij de opgegeven bank te koppelen aan een nieuwe bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)].

    > [!NOTE]  
    > Als u meer dan één online bankrekening bij de bank hebt, moet u er extra bankrekeningen voor maken in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie stap 8 t/m 10.  

    Nadat het proces is voltooid, wordt de naam van de bank in het deelvenster **Mijn rekeningen** op het tabblad **Gekoppeld** weergegeven. Het nummer tussen haakjes geeft aan hoeveel online bankrekeningen zijn gekoppeld.  
7. Kies de knop **Ok**.

    Als u slechts één online bankrekening koppelt, wordt de pagina **Bankrekeningkaart** geopend en wordt de naam van de online bankrekening weergegeven. In dit geval is de koppeling van de bankrekening voltooid. Alleen de bankrekening hoeft nog te worden ingesteld. Zie voor meer informatie [Bankrekeningen instellen](bank-how-setup-bank-accounts.md).

    Als u meerdere online bankrekeningen koppelt, wordt de pagina **Bankrekening koppelen** geopend met de aanvullende online bankrekeningen die nog niet zijn gekoppeld aan bankrekeningen in [!INCLUDE[prod_short](includes/prod_short.md)]. In dat geval volgt u de volgende stap.  
8. Selecteer op de pagina **Bankrekening koppelen** de regel voor een online bankrekening en kies vervolgens de actie **Koppelen aan nieuwe bankrekening**.  

    De pagina **Bankrekeningkaart** voor een nieuwe bankrekening wordt geopend en de naam van de online bankrekening wordt weergegeven.

    Als er al een bankrekening bestaat in [!INCLUDE[prod_short](includes/prod_short.md)] waaraan u de extra online de bankrekening wilt koppelen, voert u de volgende stap uit.  
9. Selecteer op de pagina **Bankrekening koppelen** de regel voor een online bankrekening en kies vervolgens de actie **Koppelen aan bestaande bankrekening**.
10. Selecteer op de pagina **Bankenoverzicht** de bankrekening waarmee u wilt koppelen, en kies vervolgens de knop **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Een bankrekening koppelen aan een online bankrekening

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor een bankrekening die niet is gekoppeld aan een online bankrekening, en kies vervolgens de actie **Koppelen aan online bankrekening**. De pagina **Koppeling aan online bankrekening** wordt geopend met de naam van de bank al ingevuld in het deelvenster **Rekening koppelen**.
3. Kies de banknaam. Het deelvenster **Aanmelden** wordt geopend.
4. Voer de gebruikersnaam en het wachtwoord in die u gebruikt om u aan te melden bij de online bank en kies vervolgens de knop **Volgende**.  

    De bankfeedservice treft voorbereidingen om uw bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] te koppelen aan de gerelateerde online bankrekening.  

    Wanneer het proces met succes is voltooid, wordt de naam van de bank in het deelvenster **Mijn rekeningen** op het tabblad **Gekoppeld** weergegeven. Als de bank meerdere bankrekening heeft, wordt alleen de bankrekening die u in stap 2 hebt geselecteerd, gekoppeld.  
5. Kies de knop **OK**.

Op de pagina **Bankenoverzicht** is het selectievakje **Gekoppeld** ingeschakeld.

## <a name="to-edit-the-credentials-for-an-online-bank-account"></a>De inloggegevens voor een online bankrekening bewerken

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies de desbetreffende koppeling.  
2. Kies de regel voor een bankrekening die is gekoppeld aan een online bankrekening, en kies vervolgens de actie **Online bankrekeninggegevens bewerken**.
3. Werk de inloggegevens bij.

## <a name="to-unlink-a-bank-account"></a>Een bankrekening ontkoppelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de regel voor een gekoppelde bankrekening die u wilt ontkoppelen van de gerelateerde online bankrekening, en kies de actie **Online bankrekening ontkoppelen**.

> [!NOTE]  
> Als u **Ja** kiest in het bevestigingsdialoogvenster, wordt de koppeling met de online bankrekening verwijderd en worden de logdetails gewist. Om de bankrekening weer te koppelen aan de online bankrekening, moet u zich weer aanmelden bij de bank. Zie voor meer informatie het gedeelte “Een bankrekening koppelen aan een online bankrekening“.

## <a name="to-update-bank-account-linking"></a>Koppeling aan bankrekening bijwerken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de betreffende bankrekening en kies vervolgens de actie **Koppeling aan bankrekening bijwerken**.

Als er problemen voor de gekoppelde bankrekeningen zijn op de pagina **Bankenoverzicht**, wordt de pagina **Bankrekening koppelen** geopend, waarin wordt aangegeven welke bankrekeningen problemen hebben. Problemen kunnen het beste worden opgelost door de online bankrekening te ontkoppelen en de koppeling vervolgens opnieuw te maken. Zie voor meer informatie het gedeelte “Een bankrekening koppelen aan een online bankrekening“.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Automatisch importeren van bankafschriften inschakelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor een gekoppelde bankrekening, en kies vervolgens de actie **Instelling van automatische import van bankafschriften**.
3. Geef op de pagina **Instelling van automatische import van bankafschriften** in het veld **Aantal opgenomen dagen** op hoe ver in het verleden u banktransacties wilt ophalen.

    > [!NOTE]  
    > U wordt aangeraden deze waarde in te stellen op 7 dagen of meer.  
4. Schakel het selectievakje **Ingeschakeld** in.  

Op de pagina **Betalingsreconciliatiedagboek** worden elk uur nieuwe betalingen weergegeven die worden gedaan op de online bankrekening.

> [!NOTE]  
> Transacties voor betalingen die reeds zijn geboekt als vereffend en/of gereconcilieerd op de pagina **Betalingsreconciliatiedagboek**, worden niet geïmporteerd.

## <a name="see-also"></a>Zie ook

[Bankieren instellen](bank-setup-banking.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
