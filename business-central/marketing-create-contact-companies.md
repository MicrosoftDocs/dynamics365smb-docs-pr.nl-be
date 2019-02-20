---
title: Contactbedrijven maken| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: nl-be
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Contactbedrijven maken
Uw bedrijf ontmoet regelmatig potentiële bedrijven die in de toekomst meestal zakenrelaties worden. Wanneer een nieuw contact tot stand is gekomen, moet deze informatie worden geregistreerd zodat de communicatie kan worden voortgezet.

Door zoveel mogelijk gegevens over een specifiek bedrijf toe te wijzen garandeert u een efficiënte communicatie. Als u bijvoorbeeld de relevante sectoren toewijst, zorgt u ervoor dat specifieke bedrijven worden inbegrepen in iedere relevante communicatie.

U kunt ook de zakenrelatie met een contact definiëren. Een contact kan bijvoorbeeld een prospect, bank of contractant zijn.

## <a name="creatinge-contact-companies"></a>Contactbedrijven maken
U kunt een contactkaart maken voor elk nieuw bedrijf waarmee u een zakelijke relatie hebt, bijvoorbeeld een klant, leverancier, potentiële klant, bank, advocatenkantoor, consultant, enzovoort.

Er zijn twee manieren om een contact maken: volledig nieuw of van een bestaande klant, leverancier of bankrekening.,

Voordat u een contact maakt, kunt u de instellingen controleren op de pagina **Marketinginstellingen**. Zie voor meer informatie [CRM instellen](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Een geheel nieuw bedrijfscontact maken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contacten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Voer in het veld **Nr.** een nummer in voor het contact.

    Als u echter een nummerreeks voor contacten hebt ingesteld op de pagina **Marketinginstellingen** kunt u op Enter drukken om het volgende beschikbare contactnummer te selecteren.  
4. Stel **Soort** in op **Bedrijf**.
5. Vul de overige velden in.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Een bedrijfscontact maken van een klant, leverancier of bankrekening
Als u al een aantal klanten, leveranciers of bankrekeningen hebt ingesteld, kunt u contacten maken op basis van de bestaande gegevens. Wanneer u op deze manier een contact maakt, worden de contactgegevens gesynchroniseerd met de klant-, leveranciers- of bankrekeninginformatie.

> [!NOTE]  
>   Voordat u op deze manier contactbedrijven kunt maken, moet u een zakenrelatiecode opgeven voor klanten, leveranciers en bankrekeningen op de pagina **Marketinginstellingen**. Als u contacten van bankrekeningen maakt, moet u ook nummers opgeven voor bankrekeningen op de pagina **Grootboekinstellingen**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer een van de volgende in, afhankelijk van waaruit u contacten wilt maken en kies vervolgens de gerelateerde koppeling.
   * **Contacten maken van klanten**
   * **Contacten maken van leveranciers**
   * **Contacten maken van bankrekeningen**
2. Stel op de batchverwerkingspagina die wordt geopend, in het gedeelte **Klant**, **Leverancier** of **Bankrekening** filters in als u contacten van bepaalde klanten, leveranciers of bankrekeningen wilt maken.
3. Kies **OK** om het maken van contacten te starten.

    De volgende contactnummers in de nummerreeks worden aan de nieuwe contacten toegewezen. De zakenrelatie voor leveranciers die op de pagina **Marketinginstellingen** is opgegeven, wordt toegewezen aan de nieuwe contacten.

> [!TIP]  
>   U kunt ook een klant, leverancier of bankrekening maken van een contact. Zie voor meer informatie [Een klant, leverancier of bankrekening maken van een contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Contacten synchroniseren met klanten, leveranciers en bankrekeningen
Als sommige van uw contacten ook klanten, leveranciers of bankrekeningen zijn, kunt u de contactgegevens synchroniseren met de desbetreffende klant, leverancier of bankrekening. Synchronisatie maakt gegevens die gemeenschappelijk zijn voor contacten en klanten, leveranciers of bankrekeningen hetzelfde.  

Voordat u uw contacten kunt synchroniseren met klanten, leveranciers of bankrekeningen, moet u een zakenrelatiecode voor klanten, leveranciers en of bankrekeningen opgeven op de pagina **Marketinginstellingen**. Zie voor meer informatie [CRM instellen](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Andere manieren om contacten te synchroniseren met klanten, leveranciers en bankrekeningen
U kunt de contacten met drie methoden synchroniseren met klanten, leveranciers en/of bankrekeningen:

* Contacten koppelen aan bestaande klanten, leveranciers en/of bankrekeningen op de contactkaart. Zie voor meer informatie [Contacten koppelen aan klanten, leveranciers en bankrekeningen](marketing-how-link-contact.md).
* Maak klanten,, leveranciers of bankrekeningen vanuit het contact. Zie voor meer informatie [Een klant, leverancier of bankrekening maken van een contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Contacten maken van klanten, leveranciers of bankrekeningen. Zie voor meer informatie [Een bedrijfscontact maken van een klant, leverancier of bankrekening](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Gevolgen van synchronisatie
Wanneer het contact wordt gesynchroniseerd met de klant-, leveranciers- of bankrekening:

* Hoeft u de gegevens slechts op één locatie bij te werken. Als u bijvoorbeeld het telefoonnummer op de contactkaart wijzigt, wordt het telefoonnummer automatisch bijgewerkt met dezelfde wijziging als van de klant, leveranciers of bankrekening.
* Als u een klanten-, leveranciers- of bankrekeningkaart maakt en een nummerreeks voor contacten hebt opgegeven, wordt er automatisch een contactkaart gemaakt voor de klant, leverancier of bankrekening.
* U kunt verkoopoffertes, inkoopoffertes, verkoop- en inkooporders maken vanuit het contact.
* U kunt uw interacties laten vastleggen wanneer u bepaalde acties uitvoert zoals orders, raamcontracten afdrukken, verkoopserviceorders maken, e-mailberichten verzenden, enzovoort.
* Als u een contact verwijdert dat aan een klant, leverancier of bankrekening is gekoppeld, wordt alleen het contact verwijderd. De klant, leverancier of bankrekening blijft.
* Als u een klant, leverancier of bankrekening verwijdert die aan een contact is gekoppeld, blijft het contact.

> [!NOTE]  
>   Sommige details, zoals facturerings- en boekingsgegevens, worden niet weergegeven op de contactkaart. Mogelijk wilt u deze handmatig toevoegen op de klanten-, leveranciers- of bankrekeningkaart wanneer u klanten, leveranciers of bankrekeningen van contacten maakt.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Contacten koppelen aan klanten, leveranciers en bankrekeningen
Als u een contact en een klant, leverancier of bankrekening voor hetzelfde bedrijf hebt, kunt u de twee entiteiten koppelen. Als u de twee entiteiten koppelt, kunt u gegevens synchroniseren die gemeenschappelijk zijn, zodat deze zich beide op dezelfde plaats bevinden.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Een contact koppelen aan een bestaande klant, leverancier of bankrekening
1. Open het contact dat u wilt koppelen.
2. Kies de actie **Koppelen aan bestaande** en kies vervolgens **Klant**, **Leverancier** of **Bank**.
3. Selecteer de klant, leverancier of bankrekening om aan te koppelen.

   In **Velden overnemen van** geeft u aan welke velden prioriteit moeten krijgen bij conflicterende informatie in overeenkomende velden van het contact en van de klant, leverancier of rekening. Als de verkoperscode voor het contact bijvoorbeeld anders is dan voor de klant, kunt u er door **Contact** te selecteren voor kiezen de informatie in het contact te gebruiken.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Een klant, leverancier of bankrekening maken van een contact
   Mogelijk wilt u een aantal van uw bestaande contacten vastleggen als klanten, leveranciers of bankrekeningen. Als u een klant, leverancier of bankrekening maakt van een contact, kunt u bestaande gegevens gebruiken. Wanneer u op deze manier een klant, leverancier of bankrekening maakt, wordt deze gesynchroniseerd met het contact. Synchronisatie maakt gegevens die gemeenschappelijk zijn voor contacten en klanten, leveranciers of bankrekeningen hetzelfde.

   Voordat u op deze manier contacten kunt vastleggen, moet u een zakenrelatiecode opgeven voor klanten, leveranciers en bankrekeningen op de pagina **Marketinginstellingen**. Als u contacten vastlegt als bankrekeningen maakt, moet u ook nummers opgeven voor bankrekeningen op de pagina **Grootboekinstellingen**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Een contact maken als klant, leverancier of bankrekening
   1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contacten** in en kies vervolgens de gerelateerde koppeling.
   2. Selecteer het contact dat u als klant, leverancier of bankrekening wilt maken.
   3. Kies de actie **Maken als** en kies vervolgens **Klant**, **Leverancier** of **Bank**.
   4. Bevestig het bericht.

   De contactgegevens worden nu overgebracht van de kaart **Contact** naar de kaart **Bankrekening**, **Klant**, of **Leverancier**. Mogelijk wilt u specifieke informatie toevoegen aan elk van de kaarten, bijvoorbeeld gegevens over facturering en betaling.

## <a name="setting-up-business-relations-on-contact-companies"></a>Zakenrelaties instellen voor contactbedrijven
U kunt zakenrelaties gebruiken om de zakenrelatie aan te geven die u hebt met uw contacten bijvoorbeeld een prospect, bank, serviceleverancier, enzovoort.

Zakenrelaties gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de zakenrelatiecode. U hoeft deze stap slechts eenmaal uit te voeren voor elke zakenrelatie. Als u een zakenrelatie hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.

> [!NOTE]  
>   Als u de contacten wilt synchroniseren met leveranciers, klanten of bankrekeningen in een ander onderdeel van de toepassing, kunt u een zakenrelatie instellen.

### <a name="to-define-a-business-relation-code"></a>Een zakenrelatiecode definiëren
De zakenrelatiecode geeft een categorie of soort aan van de zakenrelatie, zoals BANK of JURIDISCH. U kunt meerdere zakenrelatiecodes hebben. Als u de zakenrelatie wilt definiëren, gebruikt u de pagina **Zakenrelaties**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Zakenrelaties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

### <a name="AssignBusRelContact"></a> Zakenrelaties toewijzen aan contacten
U kunt geen zakenrelaties toewijzen aan een contactpersoon, alleen aan contactbedrijven.

1. Open het contact.
2. Kies de actie **Bedrijf** en kies vervolgens de actie **Zakenrelaties**.

    De pagina **Zakenrelaties (Relatie)** wordt weergegeven.
3. Selecteer in het veld **Zakenrelatiecode** de zakenrelatie die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal zakenrelaties toe te wijzen. U kunt zakenrelaties ook toewijzen in het contactoverzicht door dezelfde procedure te volgen.

Het aantal zakenrelaties dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal zakenrelaties** in het gedeelte **Segmentatie** van de pagina **Contact**.

Nadat u zakenrelaties hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren. Zie voor meer informatie [Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Zie ook
[Contactpersonen maken](marketing-create-contact-persons.md)   
[Werken met Business Central](ui-work-product.md)

