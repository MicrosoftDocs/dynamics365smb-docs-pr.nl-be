---
title: E-documenten gebruiken bij verkoop
description: Leer hoe u de e-documentfunctionaliteit kunt gebruiken die gerelateerd is aan verkoop.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 03/29/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# E-documenten gebruiken in het verkoopproces

U kunt geconfigureerde elektronische documenten (e-documenten) gebruiken bij verkoopdocumenten.

U kunt de volgende verkoopdocumenten gebruiken met e-documenten:  

- Verkoopfacturen
- Verkooporders
- Verkoopcreditnota's
- Servicefacturen
- Servicecreditnota's
- Rentefacturen
- Aanmaningen

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

## Overzicht van e-documentstatussen

Om een beter overzicht te krijgen van alle e-documenten in het bedrijf, kunt u het rolcentrum **Accountant** selecteren waar de statussen van e-documenten voorkomen. Daar vindt u e-documentactiviteiten met de volgende statussen:

- **Uitgaande e-documenten:**

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
