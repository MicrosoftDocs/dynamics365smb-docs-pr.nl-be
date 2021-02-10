---
title: Zakelijke contacten maken
description: Geeft een overzicht van de taken om contacten te maken en uw zakelijke relaties te definiëren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 01/05/2021
ms.author: edupont
ms.openlocfilehash: 42645a038c3937644fe90ce895ee454e1d1b5d5c
ms.sourcegitcommit: fe6943d410f5dca4e8b2986f95501009ae982d98
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/05/2021
ms.locfileid: "4827055"
---
# <a name="create-contacts"></a>Contacten maken
Wanneer u een zakelijke relatie ontwikkelt met iemand in een ander bedrijf, voegt u deze persoon toe als contact in [!INCLUDE[prod_short](includes/prod_short.md)]. Voeg vervolgens alle informatie over hen of hun bedrijf toe die nuttig kan zijn voor toekomstige communicatie. Op de pagina **Contactkaart** kunt u de volgende soorten contacten maken:

* **Persoon** - Dit is meestal wanneer u direct contact met iemand hebt gehad en hun contactgegevens heeft.
* **Bedrijf** - Bijvoorbeeld als het contact niet een individuele persoon is, maar een entiteit, zoals een aannemer of een bank. 

De informatie die relevant is voor elk type contact verschilt, dus de velden en acties die beschikbaar zijn, zijn verschillend. U kunt bijvoorbeeld alleen functiegroepen toewijzen aan een persoon en een sector alleen aan een bedrijf. 

U kunt de waarde van het veld **Type** later wijzigen. U kunt ook de velden op het tabblad **Overerving** op de pagina **Marketinginstellingen** gebruiken om de gegevens op te geven die moeten worden gedeeld tussen een persoon en zijn of haar bedrijf. Zie voor meer informatie [Contacten instellen](marketing-setup-contacts.md).

Wanneer een contact bijvoorbeeld wordt omgezet in een klant, wordt de contactpersoon of het contactbedrijf de naam van de klant. De record voor het contact wordt bewaard en u kunt het contact en de klant koppelen zodat hun gegevens in de toekomst worden gesynchroniseerd.

## <a name="to-create-a-contact-manually"></a>Handmatig een contact maken
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling.
2. Kies de actie **Nieuw**.
3. Voer in het veld **Nr.** een nummer voor het contact in.

    Als u echter een nummerreeks voor contacten hebt ingesteld op de pagina **Marketinginstellingen**, kunt u op **Enter** drukken om het volgende beschikbare contactnummer in te voegen.  
5. Vul indien nodig de resterende velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Een contact maken van een klant, leverancier of bankrekening
Als u klanten, leveranciers en bankrekeningen hebt waarvoor u contactkaarten wilt maken, kunt u de batchverwerkingen **Contacten maken van** gebruiken om contacten op basis van de bestaande gegevens te maken. Wanneer u op deze manier een contact maakt, worden de contactgegevens achteraf gesynchroniseerd met de gerelateerde klant-, leveranciers- of bankrekeninginformatie. Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Voordat u contacten kunt maken op basis van bestaande gegevens, moet u een zakenrelatiecode opgeven voor klanten, leveranciers of bankrekeningen op het sneltabblad **Interacties** van de pagina **Marketinginstellingen**. Zie [Contacten instellen](marketing-setup-contacts.md) voor meer informatie.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer een van de volgende opties in, afhankelijk van de bron van uw contactpersonen en kies de desbetreffende koppeling.
   * **Contacten maken van klanten**
   * **Contacten maken van leveranciers**
   * **Contacten maken van bankrekeningen**
2. Stel op de aanvraagpagina die wordt geopend in het gedeelte **Klant**, **Leverancier** of **Bankrekening** filters in als u contacten van bepaalde klanten, leveranciers of bankrekeningen wilt maken.
3. Kies **OK** om het maken van contacten te starten.

De volgende contactnummers in de nummerreeks worden aan de nieuwe contacten toegewezen. De zakenrelaties die op de pagina **Marketinginstellingen** worden opgegeven, worden toegewezen aan de nieuwe contacten.

> [!TIP]  
> U kunt dit ook andersom doen, namelijk door een klant, leverancier of bankrekening te maken vanuit een contact. Zie voor meer informatie [Een contact maken als een klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Een klant, leverancier, werknemer of bankrekening maken van een contact
Als u een klant, leverancier, werknemer of bankrekening hebt voor het bedrijf waarvoor u een contact wilt maken, kunt u de actie **Maken als** gebruiken. Wanneer u op deze manier een contact maakt, worden de contactgegevens achteraf gesynchroniseerd met de gerelateerde klant-, leveranciers-, werknemers- of bankrekeninginformatie. Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Voordat u klanten, leveranciers, werknemers of bankrekeningen kunt maken, moet u een zakenrelatiecode opgeven op het sneltabblad **Interacties** van de pagina **Marketinginstellingen**. Zie voor meer informatie [Contacten instellen](marketing-setup-contacts.md).

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling.
2. Selecteer het contact dat u als klant, leverancier, werknemer of bankrekening wilt maken.
3. Kies de actie **Maken als** en kies vervolgens **Klant**, **Leverancier**, **Bank** of **Werknemer**.
4. Kies de knop **OK**.

De contactgegevens worden nu overgebracht van de contactkaart naar een nieuwe klant-, leveranciers-, werknemers- of bankrekeningkaart. Mogelijk wilt u specifieke informatie toevoegen aan elk van de kaarten, bijvoorbeeld gegevens over facturering en betaling. Zie voor meer informatie bijvoorbeeld [Nieuwe klanten registreren](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Een contact koppelen aan een bestaande klant, leverancier, werknemer of bankrekening
Als u een contact en een klant, leverancier, werknemer of bankrekening hebt voor hetzelfde bedrijf, kunt u de twee entiteiten koppelen om gegevens te synchroniseren.

1. Open het contact dat u wilt koppelen.
2. Kies de actie **Koppelen aan bestaande** en kies vervolgens de actie **Klant**, **Leverancier**, **Bank** of **Werknemer**.
3. Selecteer op de pagina die wordt geopend, de klant, leverancier, werknemer of bankrekening om mee te koppelen.
4. Geef in het veld **Velden overnemen van** aan welke velden prioriteit moeten krijgen bij conflicterende informatie in overeenkomende velden van het contact en van de klant, leverancier, werknemer of rekening. Als bijvoorbeeld de verkoperscode verschilt voor het contact en de klant, kunt u ervoor kiezen de verkoper op de contactkaart te behouden door **Contact** te selecteren.
5. Kies de knop **OK**.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>Een koppeling verwijderen tussen een contact en een bestaande klant, leverancier, werknemer of bankrekening

Als u een contact en een klant, leverancier, werknemer of bankrekening ten onrechte hebt gekoppeld, verwijdert u de koppeling tussen de entiteiten zodat de gegevens niet langer synchroniseren.

1. Open het contact met de verkeerde koppeling.  
2. Kies de actie **Zakenrelaties**.  
3. Selecteer op de pagina die wordt geopend, de klant, leverancier, werknemer of bankrekening om de koppeling uit te verwijderen.  
4. Kies de actie **Verwijderen**.  

> [!NOTE]  
> Gebruik het venster **Zakenrelaties** niet om bestaande relaties te wijzigen. Verwijder in plaats daarvan de relatie en gebruik de actie **Koppelen aan bestaande**. Zie voor meer informatie de sectie [Een contactpersoon koppelen aan een bestaande klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Contacten synchroniseren met klanten, leveranciers, werknemers en bankrekeningen
Als sommige van uw contacten ook klanten, leveranciers, werknemers of bankrekeningen zijn, kunt u ze synchroniseren met gegevens vanuit de contactpersoon en de volgende voordelen krijgen:

* Hoeft u de gegevens slechts op één locatie bij te werken. Als u bijvoorbeeld het telefoonnummer op de contactkaart wijzigt, wordt het telefoonnummer automatisch bijgewerkt voor de klant, leverancier, werknemer of bankrekening.
* Als u een klanten-, leveranciers-, werknemers- of bankrekeningkaart maakt en een nummerreeks voor contacten hebt opgegeven, wordt er automatisch een contactkaart gemaakt.
* U kunt verkoopoffertes en -orders en inkoopoffertes en -orders maken vanuit het contact.
* U kunt uw interacties vastleggen wanneer u bepaalde acties uitvoert zoals orders afdrukken, raamcontracten, verkoopserviceorders maken, e-mailberichten verzenden, enzovoort.
* Als u een contact verwijdert dat aan een klant, leverancier, werknemer of bankrekening is gekoppeld, wordt alleen het contact verwijderd. De klant, leverancier, werknemer of bankrekening blijft bestaan.
* Als u een klant, leverancier, werknemer of bankrekening verwijdert die aan een contact is gekoppeld, blijft het contact bestaan.

> [!NOTE]  
> Sommige details, zoals facturerings- en boekingsgegevens, zijn niet beschikbaar voor contacten. Wanneer u contacten maakt als klanten, leveranciers, werknemers of bankrekeningen, wilt u deze wellicht handmatig toevoegen.

Er zijn drie manieren om gegevenssynchronisatie in te schakelen tussen contacten en klanten, leveranciers, werknemers of bankrekeningen:

* Wanneer u contacten maakt van klanten, leveranciers, werknemers of bankrekeningen. Zie [Een contact maken van een klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Wanneer u klanten, leveranciers, werknemers of bankrekeningen maakt van contacten. Zie [Een klant, leverancier of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Wanneer u contacten koppelt aan bestaande klanten, leveranciers, werknemers of bankrekeningen vanuit de contactkaart. Zie [Een contact koppelen aan een bestaande klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Zien aan welke klant, leverancier, werknemer of bankrekening een contact is gerelateerd
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling.
2. Selecteer de regel voor een contact, kies de actie **Gerelateerde informatie** en kies vervolgens de actie **Klant/Leverancier/Bankrek./Werknemer**.

## <a name="see-also"></a>Zie ook
[Contactpersonen beheren](marketing-contacts.md)  
[Contactpersonen instellen](marketing-setup-contacts.md)  
[Werken met Business Central](ui-work-product.md)
