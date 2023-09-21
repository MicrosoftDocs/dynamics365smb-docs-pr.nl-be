---
title: Profielen gebruiken om contacten te classificeren
description: Lees over het instellen van profielvragenlijsten om de profielen van uw zakelijke contacten te classificeren.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, profiles'
ms.search.form: '5109, 5110'
ms.author: bholtorf
ms.date: 05/20/2022
---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Profielvragenlijsten gebruiken om bedrijfscontactpersonen te classificeren

U kunt een prospect classificeren, zodat u kunt vaststellen op welke prospect u uw verkoopcampagne het best kunt richten. U kunt profielvragenlijsten instellen die u wilt gebruiken wanneer u gegevens voor de profielen van de contacten invoert. Binnen elke vragenlijst kunt u de verschillende vragen instellen die u aan uw contacten wilt stellen. Op deze manier kunt u contacten groeperen zodat uw campagnes eerder de juiste mensen targeten op basis van de criteria die u definieert met de vragenlijsten.  

Met de juiste vragenlijsten kunt u uw prospects classificeren en in categorieën indelen. U kunt de basis voor uw classificatie leggen door bestaande vragen en antwoorden te gebruiken en combineren met nieuwe vragen en antwoorden. Elk antwoord in de classificatie krijgt een puntwaarde en, afhankelijk van het bereik dat u voor de categorieën instelt (*Van waarde* en *Tot waarde*), uw contacten worden met het classificatiesysteem ingedeeld in de gedefinieerde categorieën. Bijvoorbeeld *Klanten van ABC*, *Trouwe/ontrouwe leveranciers* of *Platinum/gouden/zilveren* prospects.  

U kunt ook de vragenlijst uitvoeren om automatisch een aantal vragen te beantwoorden op basis van de contact-, klant- of leveranciersgegevens.  

## <a name="to-add-a-profile-questionnaire"></a>Een profielvragenlijst toevoegen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Profielvragenlijstinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Vragen toevoegen aan een profielvragenlijst

1. Kies de desbetreffende profielvragenlijst en kies de actie **Instelling van vragenlijst bewerken**.  
2. Kies op de eerste lege regel in het veld **Soort** de optie **Vraag**, en typ vervolgens uw vraag in het veld **Omschrijving**. Vul de overige velden op de regel in.  

    Voeg eventueel details toe aan de vraag.

    1. Kies de regel met de vraag en kies vervolgens het menu **Regel** en kies vervolgens **Vraagdetails**.  

    2. Schakel het veld **Automatisch beantwoorden** op het sneltabblad **Classificatie** op de pagina **Profielvraagdetails** in.  

    3. Selecteer in het veld **Contactclass.-veld** de optie **Classificatie**.  

    4. Vul het veld **Min. beantwoordings-%** in. De standaardwaarde is **0**.  

        Hiermee wordt het aantal vragen opgegeven als percentage dat beantwoord moet worden alvorens de classificatie wordt berekend.

    5. Kies op het tabblad **Acties** in de groep **Pagina** de optie **Antwoordpunten**. Geef aan hoeveel punten u voor elk antwoord op de pagina **Antwoordpunten** wilt geven.

        Als u een overzicht wilt van de punten die u per antwoord hebt gegeven, kiest u de actie **Antwoordpunten**.

    6. Om een update uit te voeren gaat u terug naar de pagina **Profielvragenlijstinstellingen**. Kies in het menu **Acties** in de groep **Functies** de optie **Classificatie bijwerken**.

    Op de pagina **Profielvragenlijstinstellingen** wordt het aantal contacten dat voldoet aan deze criteria, weergegeven in het veld **Aantal contacten** en op de **contactkaart** van elk contact.

3. Klik op de volgende lege regel in het veld **Soort** en kies de optie **Antwoord**. Typ vervolgens uw antwoord in het veld **Omschrijving**.  
4. Selecteer de prioriteit in het veld **Prioriteit**. In de velden **Van waarde** en **Naar waarde** definieert u een puntenbereik. Contacten die punten krijgen binnen het gedefinieerde bereik ontvangen het antwoord.  

Herhaal deze stappen om alle vragen en antwoorden in de profielvragenlijst in te voeren.

Nadat u een vragenlijst hebt gemaakt, moet u beoordelingen maken om uw contacten te classificeren. Het is ook mogelijk om vragen zo in te stellen dat ze automatisch worden geclassificeerd op basis van de informatie op de contactkaart.  

> [!NOTE]
> Als u een automatisch te beantwoorden vraag invoert, klikt u op **Regel** en kiest u vervolgens **Vraagdetails** om de criteria in te voeren voor het beantwoorden van de vraag.

## <a name="apply-questionnaires-to-contacts"></a>Vragenlijsten toepassen op contacten

U kunt uw vragenlijsten handmatig toepassen op contacten. Open de desbetreffende contactkaart en kies de actie **Profiel**. Nadat u de vragenlijsten heeft toegepast die u wilt toepassen, kunt u de categorieën in uw campagnes gaan gebruiken.  

## <a name="the-automatic-classification-of-contacts"></a>De automatische classificatie van contactpersonen

U kunt de contacten automatisch indelen op basis van klant-, leveranciers- en contactgegevens, door automatisch beantwoorde profielvragen in te stellen op de pagina **Profielvragenlijstinstellingen**.  

> [!NOTE]
> Een classificatie op basis van klantgegevens kan alleen worden toegewezen aan contacten die als klant zijn geregistreerd. Een classificatie op basis van leveranciersgegevens kan alleen worden toegewezen aan contacten die als leverancier zijn geregistreerd. De automatische classificatie wordt niet automatisch bijgewerkt. Daarom wilt u de profielvragenlijsten mogelijk bijwerken, nadat u de klant-, leveranciers- of contactgegevens waarop de profielvragenlijsten zijn gebaseerd, hebt bijgewerkt.  

Nadat u de automatisch beantwoorde profielvragen hebt ingesteld en als u de profielvragenlijst met deze vragen aan een contact toewijst, worden de juiste antwoorden voor het contact automatisch door [!INCLUDE[prod_short](includes/prod_short.md)] toegewezen.  

## <a name="example"></a>Opmerking

U kunt de contacten indelen op basis van de aantallen die ze bij u hebben gekocht:

|Antwoord|Van toepassing op|
|--- |--- |
|A|contacten die voor 500.000 LV of meer hebben gekocht|
|B|contacten die voor tussen 100.000 en 499.999 LV hebben gekocht|
|U|contacten die voor 99.999 LV of minder hebben gekocht|

Hiervoor moet u de pagina **Profielvragenlijstinstellingen** als volgt invullen:

| Soort     | Omschrijving        | Automatische indeling     | Van waarde | Naar waarde |
|----------|--------------------|------------------------------|------------|----------|
| Vraag | ABC-classificatie | Klik op het selectievakje om het in te schakelen |            |          |
| Antwoord   | A                  |                              | 500.000    |          |
| Antwoord   | B                  |                              | 100,000    | 499,999  |
| Antwoord   | U                  |                              |            | 99,999   |

Vul vervolgens de pagina **Profielvraagdetails** als volgt in:

| Veld                         | Waarde         |
|-------------------------------|---------------|
| Veld Klantclassificatie | Verkoop (LV)   |
| Indelingsmethode         | Gedefinieerde waarde |

Wanneer u de profielvragenlijst met deze vraag aan een contact toewijst, wordt het relevante antwoord voor dit contact automatisch ingevoerd op de profielregels van de contactkaart.

## <a name="see-also"></a>Zie ook

[Contacten maken](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
