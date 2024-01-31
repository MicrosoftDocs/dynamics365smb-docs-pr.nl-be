---
title: E-documenten gebruiken in verkoop en inkoop
description: Leer hoe u de e-documentfunctionaliteit kunt gebruiken die gerelateerd is aan verkoop- en inkoopfacturen.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# E-documenten gebruiken in verkoop en inkoop

U kunt geconfigureerde elektronische documenten (e-documenten) gebruiken bij verkoop- en inkoopdocumenten.

U kunt de volgende documenten gebruiken met e-documenten:  

- Verkoop: 
    - Verkoopfacturen
    - Verkooporders
    - Verkoopcreditnota's
    - Servicefacturen
    - Servicecreditnota's
    - Rentefacturen
    - Aanmaningen
- Inkoop: 
    - Inkoopfacturen
    - Inkooporders (alleen nieuw document maken)
    - Inkoopcreditnota's
    - Dagboeken

> [!NOTE]
> Momenteel kan een inkooporder alleen worden gebruikt als u het document maakt op basis van het e-document van uw leverancier. U kunt het bestaande document echter niet bijwerken met regels die u van uw leverancier heeft gekregen.  

## E-documenten bij verkoop

Als u een e-factuur wilt maken en naar een klant wilt verzenden, moet u de verkoopfactuur maken en boeken. Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie over het standaardproces.

Nadat u het verkoopdocument heeft geboekt, opent u de pagina **Geboekte verkoopfactuur** om toegang te krijgen tot de gerelateerde pagina **E-document**.

### E-documenten weergeven

Volg deze stappen om bestaande e-documenten te bekijken.

1. Selecteer op de pagina **Geboekte verkoopfactuur** **E-document** \> **E-document openen**.
2. Op de pagina **E-document** kunt u in de koptekst basisinformatie over de geboekte factuur bekijken.
3. Het veld **Record** bevat het documentnummer van de geboekte verkoopfactuur. Selecteer de koppeling om het document te openen.
4. In het veld **Elektronische documentstatus** kunt u de realtime status van het document en de locatie ervan in de procespijplijn bekijken. Als het document is geboekt, is de status **Verwerkt**.

### E-documentstatussen en -logboeken

Voor meer informatie over het servicestatusniveau van uw e-document raadpleegt u het sneltabblad **Status van e-documentservice**. Op de regels toont het systeem een of meer services waarvan het document gebruik heeft gemaakt. In het meest voorkomende scenario gebruikt elk document slechts één service. Een document kan echter meerdere services gebruiken.

- Controleer het veld **Code van e-documentservice** om te bepalen welke service is gebruikt.
- Controleer het veld **Status van e-document** om de huidige servicestatus voor dit document te bepalen.
- Als u meer details wilt, selecteert u het veld **Logboeken** voor de service op de pagina **E-documentlogbestanden**. Er wordt een chronologisch overzicht getoond van de verschillende statussen van het document.
- Controleer de velden **Volgnummer** en **Gemaakt op** en andere informatie op de pagina **E-documentlogboeken**. In het veld **Status van e-document** is de eerste status **Geëxporteerd**, wat aangeeft dat het e-documentbestand is gemaakt. De volgende status is **Verzonden**, wat aangeeft dat het document naar de serviceprovider is verzonden, indien geconfigureerd.

Voor meer inzichten selecteert u de post met de status **Geëxporteerd** en voert u vervolgens een van de volgende acties uit:

- **Toewijzingslogboeken openen**: krijg een overzicht van alle geëxporteerde velden uit de brontabellen in het veld **Oorspronkelijke waarde**. Als u tijdens het exportproces transformatieregels hebt gebruikt, kunt u ook de uiteindelijke waarde ophalen in het veld **Nieuwe waarde**.
- **Bestand exporteren**: exporteer het XML-bestand voor handmatige beoordeling.

Als u de communicatie tussen uzelf en de service waarnaar u uw document verzendt, wilt bekijken, gebruikt u het veld **Communicatielogboeken**. Open de pagina **Communicatielogbestanden van e-document** om details over het verzoek en de redenen voor het bericht bij die service te bekijken.

Als er een probleem is met de serviceprovider en het document niet kan worden verzonden, zoekt u naar de volgende indicatoren op de pagina **E-document**:

- Het veld **Elektronische documentstatus** in de kop toont de status **Fout**.
- Het veld **E-documentstatus** op het sneltabblad **Status van e-documentservice** toont de status **Verzendfout**.
- Het sneltabblad **Fouten en waarschuwingen** bevat een of meer berichten die de oorzaak van het probleem aangeven.

Nadat het probleem is opgelost, voert u handmatig de **Document verzenden**-acties uit. Als u andere acties nodig heeft, zoals **Document opnieuw maken**, **Document annuleren** of **Goedkeuring ophalen**, kunt u deze uitvoeren.

## E-documenten bij inkopen

De ontvangst van elektronische inkoopfacturen in Dynamics 365 Business Central kan als batchverwerking of handmatig worden uitgevoerd.

### De batchverwerking uitvoeren

> [!NOTE]
> Deze batchverwerking is bedoeld voor het geautomatiseerd verzamelen van uw inkomende facturen. Het kan alleen werken in een land/regio waar de functionaliteit bestaat.

Telkens wanneer een taakwachtrij wordt uitgevoerd en de externe service binnenkomende facturen heeft die door uw leverancier zijn verzonden, verzamelt en importeert het systeem deze facturen. Volg deze stappen om het proces te voltooien.

1. Nadat de batchverwerking is uitgevoerd, worden de nieuw geïmporteerde facturen weergegeven op de pagina **E-documenten**, samen met hun basisdetailinformatie.
2. Om meer details te bekijken opent u een specifiek e-document.
3. Als er geen fouten of problemen in het e-document en de toewijzing ervan voorkomen, toont het veld **Record** het documentnummer van de inkoopfactuur die het systeem automatisch heeft gemaakt. Selecteer de koppeling om het document te openen. Dit door het systeem gemaakte document is niet het geboekte document.
4. Om rechtstreeks naar het inkoopdocument te gaan selecteert u het veld **Record**. Nadat u de pagina **Inkoopfactuur** heeft geopend, controleert u het document. Als alles correct is, boekt u het document.
5. Wanneer u het inkoopdocument boekt, wordt het veld **Record** van het **E-document** bijgewerkt van **Factuur** naar **Inkoopfactuur** en is het nummer van het geboekte inkoopdocument beschikbaar. U kunt het nummer selecteren om de geboekte inkoopfactuur te openen die u wilt annuleren.

Details over logboeken zijn hetzelfde als in het verkoopproces voor e-documenten.

Omdat fouten in het verkoopproces meestal verband houden met de beschikbaarheid van de dienst, kan het binnenkomende document meerdere redenen bevatten. De meest voorkomende reden voor een fout is dat het systeem de regels op het e-document dat u van uw leverancier heeft ontvangen, niet kan herkennen. Daarom kunnen er geen regels in uw inkoopfactuur worden ingevoerd.

Er zijn twee veelvoorkomende fouten:

- Als u deze specifieke regel van uw leveranciersfactuur wilt gebruiken die rechtstreeks naar de grootboekrekening is geboekt, moet u de waarde **Toewijzing tekst** correct hebben geconfigureerd. Als u deze fout wilt omzeilen als u grootboekrekeningen wilt gebruiken, selecteert u **Tekst afstemmen op rekening** om een specifieke toewijzing van de waarde **Toewijzing tekst** te maken met de waarde **Debetrekeningnr.** die u wilt gebruiken.
- Als u de voorraad wilt traceren en regels van uw leveranciersfactuur wilt gebruiken om artikelen op uw documentregels in te vullen, moet u de waarde **Nr. van artikelreferentie** correct hebben geconfigureerd. Om deze fout te omzeilen wijst u het externe artikel toe aan uw artikelnummers met behulp van de artikelreferentielijst. Zie voor meer informatie [Artikelverwijzingen gebruiken](inventory-how-use-item-cross-refs.md).

Nadat u de fouten en waarschuwingen heeft verholpen, kunt u handmatig opgeven wanneer het systeem een inkoopfactuur moet maken op basis van uw instellingen door **Document maken** te selecteren.

### Handmatig facturen importeren

Om externe e-documenten handmatig te importeren volgt u deze stappen.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-documentservice** in en selecteer vervolgens de gerelateerde koppeling
2. Selecteer op de pagina **E-documentservice** de actieve service. 
3. Selecteer **Ontvangen** en upload het e-documentbestand dat u van de leverancier heeft ontvangen.
4. Als er een foutmelding optreedt, opent u het e-document om de problemen op te lossen.
5. Wanneer u klaar bent met het oplossen van de problemen, selecteert u in de groep **Handmatig importeren** de optie **Document maken**.
6. Nadat het document in Business Central is gemaakt, kunt u het op dezelfde manier bekijken als wanneer u een batchverwerking gebruikt.

## Overzicht van e-documentstatussen

Om een beter overzicht te krijgen van alle e-documenten in het bedrijf, kunt u het rolcentrum **Accountant** selecteren waar de statussen van e-documenten voorkomen. Daar vindt u e-documentactiviteiten met de volgende statussen:

- **Uitgaande e-documenten:**

    - Verwerkt
    - Wordt uitgevoerd
    - Fout

- **Inkomende e-documenten:**

    - Verwerkt
    - Wordt uitgevoerd
    - Fout

## Zie ook

[Hoe u belastingen instelt in Business Central](finance-how-setup-edocuments.md)  
[Hoe u e-documenten uitbreidt in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Financieel beheer](finance.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Aankopen registreren met inkoopfacturen en orders](purchasing-how-record-purchases.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
