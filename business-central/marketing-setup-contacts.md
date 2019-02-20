---
title: Informatie instellen voor contactpersonen| Microsoft Docs
description: Schetst de taken voor het opgeven van informatie en codes, bijvoorbeeld over sectorgroepen en zakenrelaties, voordat u contactpersonen instelt.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: nl-be
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Contactpersonen instellen
Wanneer u contacten maakt, kunt u specifieke gegevens invoeren, zoals de sector waartoe de contactbedrijven behoren en uw zakenrelatie met de contacten.

Voordat u contacten maakt en details over uw zakenrelaties registreert, moet u de verschillende codes instellen waarmee u deze informatie kunt toewijzen aan uw contactbedrijven en medewerkers. Codes kunnen worden ingesteld voor mailinggroepen, sectoren, zakenrelaties, webbronnen, niveaus binnen de organisatie en functiegroepen.

Als u deze informatie hebt ingesteld, kunt u veel beter op een georganiseerde manier contacten maken en efficiënter zoeken naar alle contacten op basis van een bepaalde groep. Elke groep in uw bedrijf kan naar de informatie zoeken, waardoor de communicatie met de contacten succesvoller verloopt.

Naast uw contactpersonen moet u de zakenrelatie met uw contacten instellen, bijvoorbeeld prospect, bank, consultant en serviceleverancier. Zie voor meer informatie [Bedrijfsrelaties instellen voor contactbedrijven](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Sectoren instellen voor contactbedrijven
U gebruikt sectoren om het soort industrie aan te geven waartoe uw contacten behoren, bijvoorbeeld de detailhandel of de automobielindustrie.

Sectoren gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de sectorcode. U hoeft deze stap slechts eenmaal uit te voeren voor elke sector. Als u een sectorcode hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.

> [!NOTE]  
>   Als u de contacten wilt synchroniseren met leveranciers, klanten of bankrekeningen in een ander onderdeel van de toepassing, kunt u een zakenrelatie instellen.

### <a name="to-define-an-industry-group-code"></a>Een sectorcode definiëren
De sectorcode bepaalt het type of de categorie van de groep, zoals ADVERTENTIE voor reclame of PERS voor tv en radio. U kunt meerdere sectorcodes hebben. Als u de sectoren wilt definiëren, gebruikt u de pagina **Sectoren**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Sectoren** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

### <a name="AssignIndustryGroupContact">Sectoren toewijzen aan een contact</a>
U kunt geen sectoren toewijzen aan een contactpersoon, alleen aan contactbedrijven.

1. Open het contact.
2. Kies de actie **Bedrijf** en kies vervolgens de actie **Sectoren**. De pagina **Contact sectoren** wordt geopend.
3. Selecteer in het veld **Sectorcode** de sectorgroepen die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal sectoren toe te wijzen. U kunt sectoren ook toewijzen vanuit het contactoverzicht door dezelfde procedure te volgen.

Het aantal sectoren dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal sectoren** in het gedeelte **Segmentatie** op de pagina **Contact**.

Nadat u sectoren hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren. Zie voor meer informatie [Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Mailinggroepen voor contacten instellen
U kunt mailinggroepen gebruiken om groepen contacten aan te geven die dezelfde informatie moeten ontvangen. U kunt bijvoorbeeld een mailinggroep instellen voor de contacten aan wie u een verhuisbericht voor uw kantoor wilt sturen, of een andere groep om relatiegeschenken aan te zenden.

Mailinggroepen gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de mailinggroepcode. U hoeft deze stap slechts eenmaal uit te voeren voor elke mailinggroep. Als u een mailinggroepcode hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.

### <a name="to-define-mailing-group-codes"></a>Mailinggroepcodes definiëren
De mailinggroepscode bepaalt het type of de categorie van de groep, zoals VERHUIZING voor een kantoorverhuizing of GESCHENK voor relatiegeschenken. U kunt meerdere sectorcodes hebben. Als u de sectoren wilt definiëren, gebruikt u de pagina **Mailinggroepen**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mailinggroepen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

### <a name="AssignMailGroupContact"></a> Mailinggroepen toewijzen aan een contact
1. Open het contact.
2. Kies de actie **Mailinggroepen**. De pagina **Contact mailinggroepen** wordt geopend.
3. Selecteer in het veld **Mailinggroepcode** de mailinggroep die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal mailinggroepen toe te wijzen. U kunt mailinggroepen ook toewijzen vanuit het contactoverzicht door dezelfde procedure te volgen.

Het aantal mailinggroepen dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal mailinggroepen** van het gedeelte **Segmentatie** op de pagina **Contact**.

Nadat u mailinggroepen hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren. Zie voor meer informatie [Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Alternatieve adressen voor contacten instellen
U kunt een alternatief adres toewijzen voor het adres waarop de contacten soms e-mail en informatie ontvangen, bijvoorbeeld het adres van een vakantiehuis. U kunt ook een of meer perioden toewijzen aan elk alternatief adres dat u voor de contacten hebt ingevoerd, om aan te geven wanneer het adres geldig is.

### <a name="to-assign-an-alternate-address"></a>Een alternatief adres toewijzen
1. Open het contact.
2. Kies de actie **Alternatief adres** en kies vervolgens **Kaart**. De pagina **Contact alt. adresoverzicht** wordt geopend.
3. Voer een nieuw alternatief adres in en vul de velden in op de pagina **Alternatief adres van contact**.

Herhaal deze stappen om het gewenste aantal alternatieve adressen toe te wijzen. Voor elk alternatief adres kunt u een of meer perioden opgeven.

U kunt alternatieve adressen ook toewijzen vanaf de contactoverzichtpagina door dezelfde procedure te volgen.

### <a name="to-assign-an-alternate-address-date-range"></a>Perioden voor alternatieve adressen toewijzen
1. Open het contact.
2. Kies de actie **Alternatief adres** en kies vervolgens **Datumreeks**. De pagina **Contact alt. adres-/datumreeks** wordt geopend.
3. Kies de actie **Nieuw**.
4. Selecteer in het veld **Contact alt. adrescode** een alternatief adres voor dit contact en vul de velden **Begindatum** en **Einddatum** in.

Herhaal deze stappen om het gewenste aantal perioden toe te wijzen.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Functiegroepen instellen voor contactpersonen
U kunt informatie over de functiegroepen van contactpersonen toevoegen om aan te geven waar de contactpersoon verantwoordelijk voor is binnen het bedrijf, bijvoorbeeld IT, beheer of productie. U kunt deze gegevens gebruiken wanneer u gegevens over uw contacten invoert.

Functiegroepen gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de functiegroepcode. U hoeft deze stap slechts eenmaal uit te voeren voor elke functiegroep. Als u een functiegroep hebt, kunt u beginnen de code toe te wijzen aan contactpersonen.

### <a name="to-define-a-job-responsibility-code"></a>Een functiegroepcode definiëren
De functiegroepcode bepaalt het type of de categorie van het project, MARKETING of INKOOP. U kunt meerdere functiegroepcodes hebben. Als u de functiegroep wilt definiëren, gebruikt u de pagina **Functiegroepen**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Functiegroepen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Functiegroepen toewijzen aan een contactpersoon
U kunt functiegroepen toewijzen aan contactbedrijven.

1. Open de contactpersoon.
2. Kies de actie **Persoon** en kies vervolgens de actie **Functiegroepen**. De pagina **Contact functiegroepen** wordt geopend.
3. Selecteer in het veld **Functiegroepcode** de functiegroep die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal functiegroepen toe te wijzen. U kunt functiegroepen ook toewijzen vanuit het contactoverzicht door dezelfde procedure te volgen.

Het aantal functiegroepen dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal functiegroepen** in het gedeelte **Segmentatie** op de pagina **Contact**.

Nadat u functiegroepen hebt toegewezen aan uw contacten, kunt u deze gegevens gebruiken om contacten voor uw segmenten te selecteren. Zie voor meer informatie [Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Organisatieniveaus instellen voor contactpersonen
U kunt organisatieniveaus voor uw contacten gebruiken om op te geven welke functie ze hebben in het bedrijf, bijvoorbeeld directie. U kunt deze gegevens gebruiken wanneer u gegevens over uw contacten invoert.

Organisatieniveaus gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de organisatieniveaucode. U hoeft deze stap slechts eenmaal uit te voeren voor elk organisatieniveau. Als u een organisatieniveaucode hebt, kunt u beginnen de code toe te wijzen aan contactpersonen.

### <a name="to-define-an-organizational-level-code"></a>Een organisatieniveaucode definiëren
Het organisatieniveau bepaalt het type of de categorie van het organisatieniveau, bijvoorbeeld CEO of CFO. U kunt meerdere organisatieniveaucodes hebben. Als u het organisatieniveau wilt definiëren, gebruikt u de pagina **Organisatieniveaus**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Niveaus binnen de organisatie** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Organisatieniveaus toewijzen aan een contactpersoon
U kunt organisatieniveaus alleen toewijzen aan contactpersonen, niet aan contactbedrijven. U kunt slechts één niveau binnen de organisatie aan elk contact toewijzen.

1. Open het contact.
2. Selecteer in het veld **Organisatieniveaus** de code die u wilt toewijzen.

Nadat u niveaus binnen de organisatie aan de contacten hebt toegewezen, kunt u deze gegevens gebruiken om segmenten te maken.

Nadat u functiegroepen hebt toegewezen aan uw contacten, kunt u deze gegevens gebruiken om contacten voor uw segmenten te selecteren. Zie voor meer informatie [Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Webbronnen voor contactbedrijven instellen
U kunt webbronnen gebruiken met uw contactbedrijven om bijvoorbeeld zoekengines en websites op internet aan te geven die u wilt gebruiken om informatie over de contacten te zoeken. Als u webbronnen wilt toewijzen, moet u aangeven welk zoekprogramma en welk zoekwoord wordt gebruikt bij het zoeken naar de vereiste informatie.

Webbronnen gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de webbroncode. U hoeft deze stap slechts eenmaal uit te voeren voor elke webbron. Als u een webbroncode hebt, kunt u beginnen de code toe te wijzen aan contactpersonen.

### <a name="to-define-a-web-source-code"></a>Een webbroncode definiëren
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Webbronnen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de **Nieuw**-acties.
3. Vul de velden **Code**, **Omschrijving** en **URL** in.

    Typ %1 in het veld **URL** om een tijdelijke aanduiding in te voegen voor een zoekwoord in de URL. Wanneer u de webbron start vanaf een contact, wordt %1 automatisch vervangen door de zoekterm die u op de pagina **Contact webbronnen** hebt ingevoerd, bijvoorbeeld de naam van het bedrijf.

Herhaal deze stappen om het gewenste aantal webbronnen in te stellen.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Webbronnen toewijzen aan een contactbedrijf
Als u webbronnen wilt toewijzen, moet u aangeven welk zoekprogramma en welk zoekwoord wordt gebruikt bij het zoeken naar de vereiste informatie.

1. Open het contact.
2. Kies de actie **Bedrijf** en kies vervolgens de actie **Webbronnen**. De pagina **Contact webbronnen** wordt geopend.
3. Kies in het veld **Webbroncode** de webbron die u wilt toewijzen.
4. Voer in het veld **Zoekterm** de zoekterm in die moet worden gebruikt bij het zoeken naar de informatie.

Herhaal deze stappen om het gewenste aantal webbronnen toe te wijzen.

U kunt webbronnen ook toewijzen op de pagina **Contactoverzicht** door dezelfde procedure te volgen.

## <a name="see-also"></a>Zie ook
[Contactpersonen beheren](marketing-contacts.md)  
[Verkoopopportunities beheren](marketing-manage-sales-opportunities.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

