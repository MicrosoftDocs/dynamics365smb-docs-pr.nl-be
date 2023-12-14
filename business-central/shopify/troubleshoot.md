---
title: Problemen oplossen met de synchronisatie tussen Shopify en Business Central
description: Leer wat u moet doen als er iets mis gaat tijdens de synchronisatie van gegevens tussen Shopify en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# Problemen oplossen met de synchronisatie tussen Shopify en Business Central

Mogelijk komt u situaties tegen waarin u problemen moet oplossen bij het synchroniseren van gegevens tussen Shopify en [!INCLUDE[prod_short](../includes/prod_short.md)]. Deze pagina definieert stappen voor het oplossen van enkele typische scenario's.

## Taken op de voorgrond uitvoeren

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u problemen wilt oplossen om de pagina **Shopify-winkelkaart** te openen.
3. Zet de schakelaar **Synchronisatie op achtergrond toestaan** uit.

Wanneer de synchronisatieactie wordt geactiveerd, wordt de taak nu op de voorgrond uitgevoerd. Als er een fout optreedt, krijgt u een foutdialoogvenster met een **Details kopiëren**-koppeling. Gebruik de koppeling om aanvullende informatie naar een teksteditor te kopiëren voor verdere analyse.

## Logboeken

Met de logboekfuncties kunt u gemakkelijker vaststellen waarom er een fout is opgetreden. Op de pagina **Shopify-winkelkaart** kunt u in het veld **Logmodus** het detailniveau opgeven dat u over fouten wilt vastleggen. Het veld biedt de volgende opties:

- **Uitgeschakeld**: geen informatie over fouten registreren.
- **Alleen fout**: alleen de foutmelding registreren, zonder de verzoek/antwoord-paren. Dit is de standaardinstelling voor nieuwe winkels.
- **Alle**: registreer de verzoek/antwoord-paren voor alle transacties, inclusief de succesvolle transacties. Alle fouten registreren fouten kan [!INCLUDE [prod_short](../includes/prod_short.md)] vertragen. Gebruik deze modus wanneer de gegevensuitwisseling niet tot fouten leidt, maar u meer inzicht wilt krijgen in de gegevens die daadwerkelijk zijn verzonden en ontvangen. Sommige gegevens worden altijd vastgelegd, ongeacht of registratie is ingeschakeld. Zie [Gegevensvastlegging](#data-capture) voor meer informatie.

### Logboeken controleren

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-logposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gerelateerde logboekpost en open vervolgens de pagina **Shopify-logpost**.
3. Bekijk het verzoek, de statuscode, de beschrijving en de reactiewaarden.

> [!TIP]
> Als u contact moet opnemen met Shopify-ondersteuning voor hulp bij het oplossen van problemen, let dan op de informatie in het veld **Aanvraag-id**. Met die informatie kan de ondersteuning het probleem sneller oplossen.

U kunt de verzoek- en antwoordwaarden als bestanden in tekstindeling downloaden.

### Logpostgegevens beheren

Om de omvang van uw database onder controle te houden zijn logposten opgenomen in een beleid voor het bewaren van gegevens, genaamd **Shopify-logpost**. Met het bewaarbeleid kunt u opgeven hoe lang u verschillende soorten gegevens wilt bewaren. Standaard worden Shopify-logposten een maand bewaard. Zie voor meer informatie over het bewaarbeleid in [Bewaarbeleid definiëren](../admin-data-retention-policies.md).

Op de pagina **Shopify-logposten** kunt u alle logposten verwijderen of alleen de posten die ouder zijn dan zeven dagen.

## Gegevensvastlegging

Ongeacht of registratie geactiveerd is ingeschakeld worden sommige Shopify-reacties altijd gelogd. U kunt de logboeken inzien of downloaden vanaf de pagina **Lijst voor gegevensvastlegging**.

Kies de actie **Opgehaalde Shopify-gegevens** op een van de volgende pagina's:

- **Shopify-order**
- **Shopify-orderregel**
- **Shopify-afhandelingen**
- **Verzendkosten voor Shopify-orders**
- **Shopify-ordertransacties**
- **Shopify-retournering**
- **Shopify-retourregel**
- **Shopify-terugbetaling**
- **Shopify-terugbetalingsregel**
- **Shopify-uitbetalingen**
- **Shopify-betalingstransacties**
- **Shopify-transacties**

## Synchronisatie opnieuw instellen

Voor optimale prestaties importeert de connector alleen klanten, producten en orders die zijn gemaakt of gewijzigd na de laatste synchronisatie. Op de pagina **Shopify-winkelkaart** zijn er functies beschikbaar die de datum/tijd van de laatste synchronisatie wijzigen of volledig resetten. Deze functie zorgt ervoor dat alle gegevens worden gesynchroniseerd en niet alleen de wijzigingen sinds de laatste synchronisatie.

Deze functie is alleen van toepassing op synchronisaties van Shopify naar [!INCLUDE[prod_short](../includes/prod_short.md)]. Het kan handig zijn als u verwijderde gegevens zoals producten, klanten of verwijderde bestellingen moet herstellen.

## Om het toegangstoken verzoeken

Als [!INCLUDE[prod_short](../includes/prod_short.md)] geen verbinding kan maken met uw Shopify-account, probeer dan het toegangstoken opnieuw in te stellen vanuit Shopify. U moet mogelijk een nieuw token aanvragen als er wijzigingen zijn in de beveiligingssleutels of vereiste machtigingen (toepassingsbereiken).

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u het toegangstoken wilt ophalen om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toegang aanvragen**.
4. Als daarom wordt gevraagd, logt u in bij uw Shopify-account.

De schakelaar **Heeft toegangssleutel** is geactiveerd.

## Verifieer en activeer machtigingen om http-verzoeken te doen bij gebruik in een niet-productieomgeving

Om correct te kunnen werken vereist de extensie Shopify-connector toestemming om HTTP-verzoeken te doen. HTTP-verzoeken zijn voor alle extensies verboden wanneer u tests uitvoert in sandboxomgevingen.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Extensiebeheer** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de extensie **Shopify-connector**.
3. Kies de actie **Configureren** om de pagina **Extensie-instellingen** te openen.
4. Zorg ervoor dat de schakelaar **HttpClient-aanvragen toestaan** is ingeschakeld.

## Het Shopify-toegangstoken roteren

De volgende procedures beschrijven hoe u het toegangstoken kunt roteren dat wordt gebruikt door de Shopify-connector om toegang te krijgen tot uw online Shopify-winkel.

### In Shopify

1. Ga vanuit uw **Shopify-beheer** naar [Apps](https://www.shopify.com/admin/apps).
2. Selecteer **Verwijderen** in de rij met de app **Dynamics 365 Business Central**.
3. Selecteer **Verwijderen** in het bericht dat wordt weergegeven.

### In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u het toegangstoken wilt roteren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toegang aanvragen**.
4. Meld u desgevraagd aan bij uw Shopify-account, controleer de privacy en machtigingen en kies vervolgens de knop **App installeren**.

## Bekende problemen

### Fout: de verkoopkoptekst bestaat niet. Identificatievelden en waarden: Document Type='Quote',No.='YOUR SHOPIFY STORE'

Om prijzen te berekenen, creëert de Shopify Connector een tijdelijk verkoopdocument (offerte) voor een tijdelijke klant (winkelcode) en gebruikt de standaardlogica voor prijsberekening. Als een externe extensie zich abonneert op gebeurtenissen in een tijdelijk verkoopdocument, is de kop mogelijk niet beschikbaar. We raden u aan contact op te nemen met de extensieprovider. Vraag hen om hun code aan te passen om te controleren op tijdelijke records. In sommige gevallen hoeft u alleen de methode `IsTemporary` op de juiste plek toe te voegen. Ga voor meer informatie over `IsTemporary`IsTemporary naar [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Om te verifiëren dat het probleem wordt veroorzaakt door een extensie van derden, gebruikt u de koppeling **Informatie naar klembord kopiëren** in het foutbericht en kopieert u vervolgens de inhoud naar de teksteditor. De informatie bevat een **AL-aanroepstack**, waarbij de bovenste regel de regel is waar de fout is opgetreden. Het volgende is een voorbeeld van een AL-aanroepstack.

AL-aanroepstack:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Vergeet niet om AL-aanroepstack-informatie te delen met de leverancier van de extensie.

### Fout: Bedrijfsboekingsgroep moet een waarde hebben in Klant: 'YOUR SHOPIFY STORE'. Het kan niet nul of leeg zijn

Kies op de pagina **Shopify-winkelkaart** in het veld **Klantensjablooncode** de sjabloon waarin **Bedrijfsboekingsgroep** is ingevuld. De klantsjabloon wordt gebruikt om klanten te maken en verkoopprijzen op verkoopdocumenten te berekenen.

### Fout: gegevens importeren naar uw Shopify-winkel is niet ingeschakeld. Ga naar de winkelkaart om deze in te schakelen

Zet op de pagina **Shopify-winkelkaart** de schakelaar **Gegevenssynchronisatie naar Shopify toestaan** aan. Deze instelling is bedoeld om de online winkel te beschermen tegen het verkrijgen van demogegevens van [!INCLUDE[prod_short](../includes/prod_short.md)].

### Fout: Oauth-fout invalid_request: kan Shopify API-toepassing niet vinden met api_key

Het lijkt erop dat u [App insluiten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) gebruikt, waarbij de client-URL deze indeling heeft: `https://[application name].bc.dynamics.com`. De Shopify-connector werkt niet voor Insluiten-apps. Als u meer wilt weten, gaat u naar [Voor welke Microsoft-producten is de Shopify-connector beschikbaar?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### Fout: interne fout. Het lijkt erop dat er bij ons iets is misgegaan. Aanvraag-id: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Neem contact op met Shopify-ondersteuning binnen zeven dagen na het optreden van deze fout en verstrek de aanvraag-id. Ga voor meer informatie naar [Ondersteuningsopties voor Shopify](shopify-faq.md#shopify).

### Fout: Oauth-fout invalid_request: Uw account heeft geen machtiging om de gevraagde toegang voor deze app te verlenen. 

Het lijkt erop dat de gebruiker die toegang vraagt, geen rechten heeft om apps te beheren (mogelijkheid om apps en kanalen te beheren en te installeren, en mogelijk app-kosten goed te keuren). U kunt dit probleem mogelijk oplossen door de app als accounteigenaar te installeren. Als alternatief kunt u de **App-machtiging** voor de gebruiker controleren in de [**Gebruikers en machtigingen**](https://www.shopify.com/admin/settings/account)-instellingen in uw **Shopify-beheer**.  

### [{"bericht":"Toegang geweigerd voor veld FIELD.","locatids":[{"regel":0,"kolom":0}],"pad":["pad"],"extensies":{"code":"ACCESS_DENIED","documentatie":https://shopify.dev/api/usage/access-scopes}}]

Vraag een nieuw token aan omdat de bijgewerkte versie van de connector meer machtigingen vereist (toepassingsbereiken). Ga voor meer informatie naar [Om toegangstoken vragen](#request-the-access-token).

## Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)
