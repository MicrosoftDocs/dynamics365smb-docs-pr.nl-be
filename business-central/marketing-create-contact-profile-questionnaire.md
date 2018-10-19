---
title: Profielen gebruiken om contacten te classificeren
description: Profielvragenlijsten instellen om te helpen uw bedrijfscontactpersonen te classificeren
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2018
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6a69a5de1ac0d6e2d238415204ec95fad9af7b9b
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Profielvragenlijsten gebruiken om bedrijfscontactpersonen te classificeren
U kunt profielvragenlijsten instellen die u wilt gebruiken wanneer u gegevens voor de profielen van de contacten invoert. Binnen elke vragenlijst kunt u de verschillende vragen instellen die u aan uw contacten wilt stellen.  

U kunt ook de vragenlijst uitvoeren om automatisch een aantal vragen te beantwoorden op basis van de contact-, klant- of leveranciersgegevens.  

## <a name="to-add-a-profile-questionnaire"></a>Een profielvragenlijst toevoegen
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vragenlijstinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies op het tabblad **Start** in de groep **Nieuw** de optie **Nieuw**.  
3.  Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Vragen toevoegen aan een profielvragenlijst
1.  Kies de betreffende vragenlijst en kies op het tabblad **Start** in de groep **Verwerken** de optie **Vragenlijstinstellingen bewerken**.  
2.  Kies op de eerste lege regel in het veld **Soort** de optie **Vraag**, en typ vervolgens uw vraag in het veld **Omschrijving**. Vul de overige velden op de regel in.  
3.  Klik op de volgende lege regel in het veld **Soort** en kies de optie **Antwoord**. Typ vervolgens uw antwoord in het veld **Omschrijving**.  
4.  Selecteer de prioriteit in het veld **Prioriteit**. In de velden **Van waarde** en **Naar waarde** definieert u een puntenbereik. Contacten die punten krijgen binnen het gedefinieerde bereik ontvangen het antwoord.  

Herhaal deze stappen om alle vragen en antwoorden in de profielvragenlijst in te voeren.

Nadat u een vragenlijst hebt gemaakt, moet u contactbeoordelingen maken om uw contacten te classificeren. Het is ook mogelijk om vragen zo in te stellen dat ze automatisch worden geclassificeerd op basis van de informatie op de contactkaart.  

> [!NOTE]
> Als u een automatisch te beantwoorden vraag invoert, klikt u op <STRONG>Regel</STRONG> en kiest u vervolgens <STRONG>Vraagdetails</STRONG> om de criteria in te voeren voor het beantwoorden van de vraag.

## <a name="the-automatic-classification-of-contacts"></a>De automatische classificatie van contactpersonen
U kunt de contacten automatisch indelen op basis van klant-, leveranciers- en contactgegevens, door automatisch beantwoorde profielvragen in te stellen in het venster **Profielvragenlijstinstellingen**.  

> [!NOTE]
> Een classificatie op basis van klantgegevens kan alleen worden toegewezen aan contacten die als klant zijn geregistreerd. Een classificatie op basis van leveranciersgegevens kan alleen worden toegewezen aan contacten die als leverancier zijn geregistreerd. De automatische classificatie wordt niet automatisch bijgewerkt. Daarom wilt u de profielvragenlijsten mogelijk bijwerken, nadat u de klant-, leveranciers- of contactgegevens waarop de profielvragenlijsten zijn gebaseerd, hebt bijgewerkt.  

Nadat u de automatisch beantwoorde profielvragen hebt ingesteld en als u de profielvragenlijst met deze vragen aan een contact toewijst, worden de juiste antwoorden voor het contact automatisch door [!INCLUDE[d365fin](includes/d365fin_md.md)] toegewezen.  

## <a name="example"></a>Opmerking
U kunt de contacten indelen op basis van de aantallen die ze bij u hebben gekocht:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Antwoord</strong></th>
<th><strong>Van toepassing op</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>contacten die voor 500.000 LV of meer hebben gekocht</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>contacten die voor tussen 100.000 en 499.999 LV hebben gekocht</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>contacten die voor 99.999 LV of minder hebben gekocht</p></td>
</tr>
</tbody>
</table>

Hiervoor moet u het venster **Profielvragenlijstinstellingen** als volgt invullen:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Soort</strong></th>
<th><strong>Omschrijving</strong></th>
<th><strong>Automatische indeling</strong></th>
<th><strong>Van waarde</strong></th>
<th><strong>Naar waarde</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Vraag</p></td>
<td><p>ABC-classificatie</p></td>
<td><p>Klik op het selectievakje om het in te schakelen</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Antwoord</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500.000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Antwoord</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100.000</p></td>
<td><p>499.999</p></td>
</tr>
<tr class="even">
<td><p>Antwoord</p></td>
<td><p>L</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99.999</p></td>
</tr>
</tbody>
</table>

Vul vervolgens het venster **Profielvraagdetails** als volgt in:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Veld</strong></th>
<th><strong>Waarde</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Veld Klantclassificatie</strong></td>
<td><emphasis>Verkoop (LV)</emphasis></td>
</tr>
<tr>
<td><strong>Indelingsmethode</strong></td>
<td><emphasis>Waarde</emphasis></td>
</tr>
</tbody>
</table>

Wanneer u de profielvragenlijst met deze vraag aan een contact toewijst, wordt het relevante antwoord voor dit contact automatisch ingevoerd op de profielregels van de contactkaart.

## <a name="see-also"></a>Zie ook
[Contactpersonen maken](marketing-create-contact-persons.md)  
[Contacten maken](marketing-how-create-contact-persons.md)  
[Contactbedrijven maken](marketing-create-contact-companies.md)  

