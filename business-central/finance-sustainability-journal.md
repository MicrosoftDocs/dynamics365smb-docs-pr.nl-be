---
title: Duurzaamheidsposten vastleggen
description: Leer hoe u uitstoot van broeikasgassen vastlegt.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Duurzaamheidsposten vastleggen  

Op dit moment is de enige manier om de uitstoot van broeikasgassen in het **Duurzaamheidsgrootboek** te registreren, het gebruik van de **Duurzaamheidsdagboeken**.   

## Duurzaamheidsdagboek  

**Duurzaamheidsdagboeken** zijn ontworpen om duurzaamheidsgerelateerde activiteiten bij te houden en vast te leggen met behulp van dezelfde gebruikerservaring als andere dagboeken in Business Central. Binnen het dagboek hebben gebruikers de mogelijkheid om uitstoot handmatig in te voeren als zij over de benodigde informatie beschikken. Als ze deze gegevens niet hebben, kunnen ze ook ingebouwde formules gebruiken om de uitstoot nauwkeurig te berekenen op basis van specifieke bekende parameters die overeenkomen met verschillende soorten bronnen en rekeningen. 

De informatie die u invoert in een dagboek is tijdelijk en kan in het dagboek worden gewijzigd. Wanneer u het dagboek boekt, wordt de informatie overgebracht naar **Duurzaamheidsposten** op afzonderlijke **Duurzaamheidsrekeningen**, waar deze niet kan worden gewijzigd. U kunt echter wel tegenboekingen of correcties boeken.  

### Dagboeksjablonen en -batches gebruiken 

Er zijn standaard twee **Duurzaamheidsdagboeksjablonen**: de standaard en de terugkerende. Voor elke dagboeksjabloon kunt u uw eigen persoonlijke dagboek instellen als een dagboekbatch. Om dit te doen moet u de actie **Batches** op de pagina **Sjablonen van duurzaamheidsdagboek** kiezen en de nieuwe **Duurzaamheidsdagboekbatch** op de nieuwe pagina maken. U kunt bijvoorbeeld voor elk uitstootbereik uw eigen dagboekbatch definiëren met behulp van de optie **Uitstootbereik**, waarbij u kunt kiezen uit drie bestaande bereiken. U kunt ook de **Broncode** en **Redencode** voor elk van de batches toevoegen of wijzigen. 

>[!TIP]
>U kunt voor elk uitstoottype één dagboekbatch hebben als u veel regels heeft, omdat dit de kans op fouten verkleint, maar u kunt ook de gemeenschappelijke batch voor alle soorten uitstoot gebruiken.   

### Duurzaamheidsdagboeken valideren 

U kunt op de pagina **Duurzaamheidsinstelling** een achtergrondcontrole inschakelen om vertragingen bij het boeken te voorkomen. De controle geeft een melding wanneer er tijdens het werken een fout optreedt in het **Duurzaamheidsdagboek** en dat zorgt ervoor dat u het dagboek niet kunt boeken.  

Wanneer u de validatie inschakelt, toont het feitenblok **Dagboekcontrole** problemen op de huidige regel en in de hele batch. Validatie vindt plaats wanneer u een dagboekbatch laadt en wanneer u een andere dagboekregel kiest. De tegel **Totaal aantal problemen** in het feitenblok toont het totale aantal problemen dat [!INCLUDE [prod_short](includes/prod_short.md)] heeft gevonden en u kunt ervoor kiezen om een overzicht van de problemen te openen. 

### Werken met duurzaamheidsdagboeken 

Volg de stappen om aan de slag te gaan met de **Duurzaamheidsdagboeken**:   

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsdagboek** in en selecteer vervolgens de gerelateerde koppeling. 
2. Op de pagina **Duurzaamheidsdagboek** kunt u zoveel regels invoeren als u van plan bent met dezelfde batch te boeken.  
3. Als **documenttype** kunt u de optie leeg laten of ervoor kiezen **Factuur** of **Creditnota** te gebruiken.  
4. In het veld **Rekeningnr.** kunt u alleen **Duurzaamheidsrekeningen** met geselecteerd veld **Directe boeking**, **Boeking** als het **Rekeningtype** en niet-geblokkeerde rekening kiezen. Rekeningen moeten ook zijn geconfigureerd met categorie en subcategorie.  

>[!NOTE]
>Als u de batch gebruikt waar het uitstootbereik is geconfigureerd, moet het **Uitstootbereik** in de **Duurzaamheidsrekening** gelijk zijn aan het **Uitstootbereik** in de gebruikte batch.  

5. U heeft twee opties: de bedragen handmatig boeken of formules gebruiken.   

    1. Als u over nauwkeurige informatie over de uitstoot beschikt en deze wilt boeken (dat wil zeggen dat deze op de ontvangen factuur staat), moet u het veld **Handmatige invoer** selecteren om op te geven dat de bedragen handmatig worden ingevoerd. In dit geval kunt u uw gegevens niet invullen in de velden **Brandstof/elektriciteit**, **Afstand**, **Aangepast bedrag**, **Installatievermenigvuldiger** en **Tijdfactor**, omdat ze bij deze keuze niet kunnen worden bewerkt. Maar de velden **Uitstoot CO2**, **Uitstoot CH4** en **Uitstoot N2O** zijn bewerkbaar en u kunt uw gegevens daar direct invullen. 
    2. Als u uw uitstoot niet nauwkeurig kent, moet u deze berekenen en hoeft u het **Handmatige invoer** veld niet te hebben geselecteerd, en in dit geval kunnen de velden **Uitstoot CO2**, **Uitstoot CH4** en **Uitstoot N2O** niet worden bewerkt, maar u kunt uw berekeningsgegevens invoeren op basis van de formule die u gebruikt. Meer informatie over de gebruikte formules en gedefinieerd in de **Categorie van duurzaamheidsrekening** vindt u hier in [Duurzaamheidsrekeningschema en -grootboek](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Kies de actie **Boeken** om het dagboek te boeken. Wanneer u posten boekt in een **Duurzaamheidsdagboek**, worden posten gegenereerd in het **Duurzaamheidsgrootboek**. 

In het geval dat uw formule is gebaseerd op de optie **Berekenen op basis van grootboek** in de **Categorie van duurzaamheidsrekening**, moet u de actie **Bedrag van grootboekposten innen** gebruiken voordat u het dagboek boekt om de uitstoot te berekenen op basis van deze gegevensbron. Als u na het invullen van de dagboekregels enkele wijzigingen in de uitstootfactoren heeft aangebracht, moet u ook de actie **Herberekenen** kiezen om het juiste bedrag in het dagboek te krijgen.  

### Periodieke dagboeken 

Een periodiek dagboek is een **Duurzaamheidsdagboek** met specifieke velden voor het beheer van transacties die u vaak boekt met weinig of geen wijzigingen. Bijvoorbeeld duurzaamheidstransacties zoals elektriciteit, warmte of andere soortgelijke transacties. Met terugkerende dagboeken kunt u vaste en variabele bedragen boeken. Met een periodiek dagboek maakt u posten die regelmatig worden geboekt, slechts eenmaal. De rekeningen, dimensies, dimensiewaarden enzovoort worden bijvoorbeeld na het boeken in het dagboek bewaard. Als er wijzigingen nodig zijn, kunt u deze elke keer dat u een bericht plaatst, aanbrengen. 

Het veld **Periodieke methode** is belangrijk. Het bepaalt hoe het bedrag op de dagboekregel na het boeken wordt behandeld. Als u bijvoorbeeld elke keer dat u de regel boekt hetzelfde bedrag gebruikt, kunt u het bedrag laten staan. In dit geval moet u **V Vast** gebruiken als optie. Als u dezelfde rekeningen en dezelfde tekst op de regel wilt gebruiken, maar het bedrag elke keer dat u boekt varieert, kunt u ervoor kiezen het bedrag na het boeken te verwijderen en in dat geval kiest u de optie **V Variabel**. 

U moet ook de **Periodieke frequentie** configureren, omdat dit datumformuleveld bepaalt hoe vaak de boeking op de journaalregel moet worden geboekt, en moet worden ingevuld. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#use-date-formulas).  

De **Vervaldatum** bepaalt de datum waarop de regel voor het laatst mag worden geboekt. De regel wordt niet geboekt na deze datum. Het voordeel van het gebruik van het veld **Vervaldatum** is dat de regel niet onmiddellijk uit het dagboek wordt verwijderd. U kunt een latere datum invoeren, zodat u de regel in de toekomst kunt gebruiken. Als het veld leeg is, wordt de regel steeds geboekt totdat deze uit het dagboek wordt verwijderd.  

## Zie ook  
[Financiën](finance.md)    
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)   
[Duurzaamheidsinstelling](finance-sustainability-setup.md)   
[Duurzaamheidsrekeningschema en -grootboek](finance-sustainability-accounts-ledger.md)   
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
