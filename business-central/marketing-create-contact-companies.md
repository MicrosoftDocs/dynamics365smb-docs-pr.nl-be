---
title: Contactbedrijven maken| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 67b11d9c763ef4688af35a3f9cd83ee8c364fcee
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528449"
---
# <a name="create-contacts"></a>Contacten maken
U ontmoet regelmatig personen van andere bedrijven, wat kan leiden tot zakenrelaties, zoals een klantrelatie. Als een dergelijk nieuw contact tot stand is gekomen, moet zoveel mogelijk informatie op een contactkaart worden geregistreerd zodat de communicatie kan worden voortgezet.

U kunt het contact maken als type **Bedrijf**, bijvoorbeeld als de relatie niet een individuele persoon is, maar een entiteit, zoals een aannemer of een bank. U kunt het contact ook maken als type **Persoon**. De functionaliteit is min of meer hetzelfde voor beide typen en beide kunnen worden gewijzigd naarmate de relatie evolueert.

Wanneer een contactkaart bijvoorbeeld wordt omgezet in een klantenkaart, wordt de contactpersoon of het contactbedrijf de naam van de klant. De contactkaart blijft en gegevens op de twee kaarten worden voortaan gesynchroniseerd als u deze aan elkaar koppelt.

## <a name="person-or-company"></a>Persoon of bedrijf
U kunt besluiten een contact in te stellen als een persoon of bedrijf, meestal afhankelijk van de vraag of u de naam van de contactpersoon op dat moment weet. U doet dit wanneer u het veld **Soort** op de pagina **Contactkaart** invult. U kunt ook contactkaarten onderhouden voor zowel een bedrijf als een of meer personen die in het bedrijf werken. Dit gebeurt automatisch wanneer u het veld **Bedrijfsnaam** op een contactkaart van het soort **Persoon** invult.

De functionaliteit is gelijk voor beide soorten, behalve dat de opties voor aanvullende informatie afhankelijk van het type verschillen. U kunt bijvoorbeeld alleen functiegroepen toewijzen aan een persoon en een sector alleen aan een bedrijf. Dit wordt aangegeven in de gebruikersinterface doordat velden en acties die niet van toepassing zijn, grijs worden gemaakt. U kunt de waarde van het veld **Type** later wijzigen of u kunt de velden op het sneltabblad **Overerving** op de pagina **Marketinginstellingen** gebruiken om te bepalen welke gegevens worden gedeeld tussen een persoon en het gerelateerde bedrijf van de persoon. Zie voor meer informatie [Contacten instellen](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>Handmatig een contact maken
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling.
2. Kies de actie **Nieuw**.
3. Voer in het veld **Nr.** een nummer voor het contact in.

    Als u echter een nummerreeks voor contacten hebt ingesteld op de pagina **Marketinginstellingen** kunt u op Enter drukken om het volgende beschikbare contactnummer in te voegen.  
5. Vul indien nodig de resterende velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Een contact maken van een klant, leverancier of bankrekening
Als u klanten, leveranciers en bankrekeningen hebt waarvoor u contactkaarten wilt maken, kunt u de batchverwerkingen **Contacten maken van** gebruiken om contacten op basis van de bestaande gegevens te maken. Wanneer u op deze manier een contact maakt, worden de contactgegevens achteraf gesynchroniseerd met de gerelateerde klant-, leveranciers- of bankrekeninginformatie. Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

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
> U kunt dit ook andersom doen, namelijk door een klant, leverancier of bankrekening te maken vanuit een contact. Zie voor meer informatie [Een contact maken als een klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Een klant, leverancier of bankrekening maken van een contact
Als u een klant, leverancier of bankrekening hebt voor het bedrijf waarvoor u een contact wilt maken, kunt u de functie **Maken als** gebruiken. Wanneer u op deze manier een contact maakt, worden de contactgegevens achteraf gesynchroniseerd met de gerelateerde klant-, leveranciers- of bankrekeninginformatie. Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Voordat u klanten, leveranciers of bankrekeningen kunt maken van contacten, moet u een zakenrelatiecode opgeven voor klanten, leveranciers of bankrekeningen op het sneltabblad **Interacties** van de pagina **Marketinginstellingen**. Zie voor meer informatie [Contacten instellen](marketing-setup-contacts.md).

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling.
2. Selecteer het contact dat u als klant, leverancier of bankrekening wilt maken.
3. Kies de actie **Maken als** en kies vervolgens **Klant**, **Leverancier** of **Bank**.
4. Kies de knop **OK**.

De contactgegevens worden nu overgebracht van de contactkaart naar een nieuwe klant-, leveranciers- of bankrekeningkaart. Mogelijk wilt u specifieke informatie toevoegen aan elk van de kaarten, bijvoorbeeld gegevens over facturering en betaling. Zie voor meer informatie bijvoorbeeld [Nieuwe klanten registreren](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Een contact koppelen aan een bestaande klant, leverancier of bankrekening
Als u een contact en een klant, leverancier of bankrekening hebt voor hetzelfde bedrijf, kunt u de twee entiteiten koppelen, zodat gemeenschappelijke gegevens worden gesynchroniseerd.

1. Open het contact dat u wilt koppelen.
2. Kies de actie **Koppelen aan bestaande** en kies vervolgens de actie **Klant**, **Leverancier** of **Bank**.
3. Selecteer op de pagina die wordt geopend, de klant, leverancier of bankrekening om mee te koppelen.
4. Geef in het veld **Velden overnemen van** aan welke velden prioriteit moeten krijgen bij conflicterende informatie in overeenkomende velden van het contact en van de klant, leverancier of rekening. Als op de contactkaart bijvoorbeeld een andere verkoper wordt vermeld dan op de klantkaart, kunt u ervoor kiezen de verkoper op de contactkaart te behouden door **Contact** te selecteren.
5. Kies de knop **Ok**.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Contacten synchroniseren met klanten, leveranciers en bankrekeningen
Als sommige van uw contacten ook klanten, leveranciers of bankrekeningen zijn, kunt u de contactgegevens synchroniseren met de desbetreffende klant, leverancier of bankrekening.

Het heeft de volgende voordelen wanneer een contact wordt gesynchroniseerd met een klant, leverancier of bankrekening.

* Hoeft u de gegevens slechts op één locatie bij te werken. Als u bijvoorbeeld het telefoonnummer op de contactkaart wijzigt, wordt het telefoonnummer automatisch bijgewerkt met dezelfde wijziging als van de klant, leveranciers of bankrekening.
* Als u een klanten-, leveranciers- of bankrekeningkaart maakt en een nummerreeks voor contacten hebt opgegeven, wordt er automatisch een contactkaart gemaakt voor de klant, leverancier of bankrekening.
* U kunt verkoopoffertes en orders en inkoopoffertes en orders maken vanuit het contact.
* U kunt uw interacties laten vastleggen wanneer u bepaalde acties uitvoert zoals orders, raamcontracten afdrukken, verkoopserviceorders maken, e-mailberichten verzenden, enzovoort.
* Als u een contact verwijdert dat aan een klant, leverancier of bankrekening is gekoppeld, wordt alleen het contact verwijderd. De klant, leverancier of bankrekening blijft.
* Als u een klant, leverancier of bankrekening verwijdert die aan een contact is gekoppeld, blijft het contact.

> [!NOTE]  
> Sommige details, zoals facturerings- en boekingsgegevens, worden niet weergegeven op de contactkaart. Mogelijk wilt u deze handmatig toevoegen op de klanten-, leveranciers- of bankrekeningkaart wanneer u klanten, leveranciers of bankrekeningen van contacten maakt.

De synchronisatie van gemeenschappelijke gegevens tussen contacten en de gerelateerde klanten, leveranciers of bankrekeningen wordt ingeschakeld op drie manieren:

* Wanneer u contacten maakt van klanten, leveranciers of bankrekeningen. Zie [Een contact maken van een klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Wanneer u klanten, leveranciers of bankrekeningen maakt vanuit contacten. Zie [Een klant, leverancier of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).
* Wanneer u contacten koppelt aan bestaande klanten, leveranciers of bankrekeningen vanuit de contactkaart. Zie [Een contact koppelen aan een bestaande klant, leverancier of bankrekening](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).

## <a name="to-view-which-customer-vendor-or-bank-account-a-contact-is-related-to"></a>Zien aan welke klant, leverancier of bankrekening een contact is gerelateerd
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contactpersonen** in en kies de desbetreffende koppeling.
2. Selecteer de regel voor een contact, kies de actie **Gerelateerde informatie** en kies vervolgens de actie **Klant/Leverancier/Bankrek.**.

De pagina voor de gerelateerde kaart wordt geopend.

## <a name="see-also"></a>Zie ook
[Contactpersonen beheren](marketing-contacts.md)  
[Contactpersonen instellen](marketing-setup-contacts.md)  
[Werken met Business Central](ui-work-product.md)
