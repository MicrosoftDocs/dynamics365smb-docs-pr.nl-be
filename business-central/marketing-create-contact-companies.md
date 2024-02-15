---
title: Zakelijke contacten maken
description: Geeft een overzicht van de taken die nodig zijn bij het maken van contacten en het definiëren van uw zakelijke relaties op de contactkaart.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.date: 08/30/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Contacten maken

Wanneer u een zakelijke relatie ontwikkelt met iemand in een ander bedrijf, voegt u deze persoon toe als contact in [!INCLUDE[prod_short](includes/prod_short.md)]. Voeg vervolgens alle informatie over hen of hun bedrijf toe die nuttig kan zijn voor toekomstige communicatie. U kunt de volgende soorten contacten maken op de pagina **Contactkaart**:

* **Persoon**: gebruik dit wanneer u direct contact met iemand hebt gehad en hun contactgegevens heeft.
* **Bedrijf**: gebruik dit voor een contact dat niet een individuele persoon is, maar een entiteit, zoals een aannemer of een bank.

De informatie die relevant is voor elk type contact verschilt, dus de beschikbare velden en acties zijn verschillend. U kunt bijvoorbeeld alleen functiegroepen toewijzen aan een persoon en een sector alleen aan een bedrijf.

U kunt de waarde van het veld **Type** later wijzigen. U kunt ook de velden op het tabblad **Overerving** op de pagina **Marketinginstellingen** gebruiken om de gegevens op te geven die moeten worden gedeeld tussen een persoon en zijn of haar bedrijf. Zie voor meer informatie [Contacten instellen](marketing-setup-contacts.md).

Wanneer een contact bijvoorbeeld wordt omgezet in een klant, wordt de contactpersoon of het contactbedrijf de naam van de klant. De record voor het contact wordt bewaard en u kunt het contact en de klant koppelen zodat hun gegevens in de toekomst worden gesynchroniseerd.

> [!NOTE]
> Als u de [functie-update voor conversiesjablonen](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees) inschakelt, kunt u ook leveranciers of werknemers maken vanuit zakelijke contacten.
>
> Als u echter al gebruikmaakt van de ingebouwde functionaliteit voor het automatisch maken van klanten of artikelen, dan ondersteunt deze functie-update geen aangepaste velden en bevatten nieuwe klanten of artikelen dergelijke gegevens niet.

## Handmatig een contact maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contacten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Kies in het veld **Nr.** een nummer voor het contact in.

   Als u echter een nummerreeks voor contacten hebt ingesteld op de pagina **Marketinginstellingen**, kunt u <kbd>Enter</kbd> selecteren om het volgende beschikbare contactnummer in te voegen.
4. Vul indien nodig de resterende velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Een contact maken van een klant, leverancier of bankrekening

Als u bestaande klanten, leveranciers en bankrekeningen hebt waarvoor u contactkaarten wilt maken, kunt u de batchverwerkingen **Contacten maken van** gebruiken. Wanneer u op deze manier een contact maakt, worden de contactgegevens later gesynchroniseerd met de gerelateerde klant-, leveranciers- of bankrekeninginformatie. Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers, werknemers en bankrekeningen](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts)

> [!NOTE]  
> Voordat u contacten kunt maken op basis van bestaande gegevens, moet u een zakenrelatiecode opgeven voor klanten, leveranciers of bankrekeningen op het sneltabblad **Interacties** van de pagina **Marketinginstellingen**. Zie voor meer informatie [Contacten instellen](marketing-setup-contacts.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer een van de volgende in, die overeenkomt met de entiteit van waaruit u contacten wilt maken, en kies vervolgens de gerelateerde koppeling.
   * **Contacten maken van klanten**
   * **Contacten maken van leveranciers**
   * **Contacten maken van bankrekeningen**
2. Stel op de aanvraagpagina die wordt geopend in het gedeelte **Klant**, **Leverancier** of **Bankrekening** filters in als u contacten van bepaalde klanten, leveranciers of bankrekeningen wilt maken.
3. Kies **OK** om de contacten te maken.

De volgende contactnummers in de nummerreeks worden aan de nieuwe contacten toegewezen. De zakenrelatiecode die op de pagina **Marketinginstellingen** wordt opgegeven, wordt toegewezen aan de nieuwe contacten.

> [!TIP]  
> U kunt dit ook andersom doen, namelijk door een klant, leverancier, werknemer of bankrekening te maken vanuit een contact. Zie voor meer informatie de sectie [Een klant, leverancier, werknemer of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## Een klant, leverancier, werknemer of bankrekening maken van een contact

Als u een klant, leverancier, werknemer of bankrekening hebt voor het bedrijf waarvoor u een contact wilt maken, kunt u de actie **Maken als** gebruiken. Wanneer u op deze manier een contact maakt, worden de contactgegevens later gesynchroniseerd met de gerelateerde klant-, leveranciers-, werknemers- of bankrekeninginformatie. Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts)<!--Should this link include "Employees" as per the section title below?-->

> [!NOTE]  
> Voordat u klanten, leveranciers, werknemers of bankrekeningen kunt maken, moet u een zakenrelatiecode opgeven op het sneltabblad **Interacties** van de pagina **Marketinginstellingen**. Zie voor meer informatie [Contacten instellen](marketing-setup-contacts.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contacten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het contact dat u als klant, leverancier, werknemer of bankrekening wilt maken.
3. Kies de actie **Maken als** en kies vervolgens **Klant**, **Leverancier**, **Bank** of **Werknemer**.
4. Klik op **OK**.

De contactgegevens worden nu overgebracht van de contactkaart naar een nieuwe klant-, leveranciers-, werknemers- of bankrekeningkaart. Mogelijk wilt u specifieke informatie toevoegen aan elk van de kaarten, bijvoorbeeld gegevens over facturering en betaling. Zie voor een voorbeeld [Nieuwe klanten registreren](sales-how-register-new-customers.md).

## Een contact koppelen aan een bestaande klant, leverancier, werknemer of bankrekening

Als u een contact en een klant, leverancier, werknemer of bankrekening hebt voor hetzelfde bedrijf, kunt u de twee entiteiten koppelen om gegevens te synchroniseren.

1. Open het contact dat u wilt koppelen.
2. Kies de actie **Koppelen aan bestaande** en kies vervolgens de actie **Klant**, **Leverancier**, **Bank** of **Werknemer**.
3. Selecteer op de pagina die wordt geopend, de klant, leverancier, werknemer of bankrekening om mee te koppelen.
4. Geef in het veld **Velden overnemen van** de velden op die prioriteit moeten krijgen bij conflicterende informatie in gemeenschappelijke velden van het bestaande contact en de klant, leverancier, werknemer of rekening. Als de verkoperscode verschilt voor het contact en de klant, kunt u ervoor kiezen de verkoper op de contactkaart te behouden door **Contact** te selecteren.
5. Klik op **OK**.

## Een koppeling verwijderen tussen een contact en een bestaande klant, leverancier, werknemer of bankrekening

Als u een contact met een klant, leverancier, werknemer of bankrekening ten onrechte hebt gekoppeld, verwijdert u de koppeling tussen de entiteiten zodat de gegevens niet langer synchroniseren.

1. Open het contact met de verkeerde koppeling.  
2. Kies de actie **Zakenrelaties**.  
3. Selecteer op de pagina die wordt geopend, de klant, leverancier, werknemer of bankrekening om de koppeling uit te verwijderen.  
4. Kies de actie **Verwijderen**.  

> [!NOTE]  
> Gebruik het venster **Zakenrelaties** niet om bestaande relaties te wijzigen. Verwijder in plaats daarvan de relatie en gebruik de actie **Koppelen aan bestaande**. Zie voor meer informatie de sectie [Een contactpersoon koppelen aan een bestaande klant, leverancier, werknemer of bankrekening](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Contacten synchroniseren met klanten, leveranciers, werknemers en bankrekeningen

Als sommige van uw contacten ook klanten, leveranciers, werknemers of bankrekeningen zijn, kunt u ze synchroniseren met gegevens vanuit de contactpersoon en de volgende voordelen krijgen:

* Hoeft u de gegevens slechts op één locatie bij te werken. Als u het telefoonnummer op de contactkaart wijzigt, wordt het telefoonnummer dus automatisch bijgewerkt voor de klant, leverancier, werknemer of bankrekening.
* Als u een klanten-, leveranciers-, werknemers- of bankrekeningkaart maakt en een nummerreeks voor contacten hebt opgegeven, wordt er automatisch een contactkaart gemaakt.
* U kunt verkoopoffertes en -orders en inkoopoffertes en -orders maken vanuit het contact.
* U kunt uw interacties vastleggen wanneer u bepaalde acties uitvoert zoals orders afdrukken, raamcontracten, verkoopserviceorders maken, e-mailberichten verzenden, enzovoort.
* Als u een contact verwijdert dat aan een klant, leverancier, werknemer of bankrekening is gekoppeld, wordt alleen het contact verwijderd. De klant, leverancier, werknemer of bankrekening blijft bestaan.
* Als u een klant, leverancier, werknemer of bankrekening verwijdert die aan een contact is gekoppeld, blijft het contact ook bestaan.

> [!NOTE]  
> Sommige details, zoals facturerings- en boekingsgegevens, zijn niet beschikbaar voor contacten. Wanneer u contacten maakt als klanten, leveranciers, werknemers of bankrekeningen, wilt u die informatie wellicht handmatig toevoegen.

Er zijn drie manieren om gegevenssynchronisatie in te schakelen tussen contacten en klanten, leveranciers, werknemers of bankrekeningen:

* Wanneer u contacten maakt van klanten, leveranciers of bankrekeningen. Zie voor meer informatie de sectie [Een contact maken van een klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Wanneer u klanten, leveranciers, werknemers of bankrekeningen maakt van contacten. Zie voor meer informatie de sectie [Een klant, leverancier, werknemer of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Wanneer u contacten koppelt aan bestaande klanten, leveranciers, werknemers of bankrekeningen vanuit de contactkaart. Zie voor meer informatie de sectie [Een contactpersoon koppelen aan een bestaande klant, leverancier, werknemer of bankrekening](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Zien aan welke klant, leverancier, werknemer of bankrekening een contact is gerelateerd

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Contacten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor een contact, kies de actie **Gerelateerde informatie** en kies vervolgens de actie **Klant/Leverancier/Bankrekening/Werknemer**.

## Zie ook

[Contactpersonen beheren](marketing-contacts.md)  
[Contactpersonen instellen](marketing-setup-contacts.md)  
[Online kaarten gebruiken om locaties en routebeschrijvingen te vinden](across-online-maps.md)  
[Werken met Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
