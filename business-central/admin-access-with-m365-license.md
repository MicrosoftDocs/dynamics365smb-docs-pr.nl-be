---
title: Business Central-toegang met Microsoft 365-licenties
description: 'Ontdek hoe gebruikers toegang kunnen krijgen tot Business Central-gegevens, bijvoorbeeld in Microsoft Teams-chats en kanalen, met enkel een Microsoft 365-licentie, zonder Business Central-licentie.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="business-central-access-with-microsoft--licenses" />Business Central-toegang met Microsoft 365-licenties

[!INCLUDE[prod_short](includes/prod_short.md)]-gebruikers krijgen een Dynamics 365 Business Central-licentie waarmee ze hun bedrijfsgegevens kunnen bekijken, wijzigen en gebruiken vanuit elke gebruikersinterface. Voor alle andere medewerkers in de organisatie die slechts af en toe gegevens hoeven te bekijken, biedt Business Central toegang via Microsoft 365.  

Wanneer een organisatie zowel een Dynamics 365 Business Central als een Microsoft 365-abonnement heeft, kunnen beheerders omgevingen configureren om toegang te verlenen met Microsoft 365-licenties, en precies kiezen tot welke tabellen en andere objecten deze categorie van gebruikers toegang krijgt. Indien geconfigureerd, kunnen medewerkers met een Microsoft 365 -licentie maar geen [!INCLUDE [prod_short](includes/prod_short.md)]-licentie [!INCLUDE [prod_short](includes/prod_short.md)]-records bekijken die met hen zijn gedeeld in Microsoft Teams-chats en kanalen.

## <a name="why-enable-access-with-microsoft--licenses" />Waarom toegang met Microsoft 365-licenties inschakelen

- Ontgrendel stamgegevens waartoe elke medewerker in de hele organisatie toegang zou moeten hebben.

- Geef afdelingen die niet op [!INCLUDE [prod_short](includes/prod_short.md)] draaien de mogelijkheid om zichzelf te bedienen door toegang te krijgen tot belangrijke gegevens die nodig zijn om hun taken succesvol te kunnen uitvoeren, waardoor het niet langer nodig is om voortdurend gegevens op te vragen bij anderen.

- Zorg voor efficiëntere samenwerking, zodat taken en projecten waarbij verschillende afdelingen betrokken zijn, op tijd worden voltooid, door de wrijving te elimineren die doorgaans gepaard gaat met fouten waarbij de toegang wordt geweigerd als gevolg van licenties.

- Verhoog de teamprestaties zodat mensen gegevensgestuurde beslissingen kunnen nemen waar iedereen bij betrokken is, zelfs als ze niet in [!INCLUDE [prod_short](includes/prod_short.md)] werken.

- Voldoe aan de doelstellingen van het licentiebudget door licenties toe te wijzen die geleidelijk aansluiten op de behoeften van werknemers, met Microsoft 365-licenties voor alleen-lezen toegang, Dynamics 365 Business Central Team Member-licenties voor beperkte schrijftoegang, en Dynamics 365 Business Central Essentials of Premium voor volledige schrijftoegang.

- Verbeter de gegevensbeveiliging door de noodzaak voor het plakken van schermfragmenten van bedrijfsgegevens buiten de grenzen van gegevensbeheer te verminderen.

## <a name="use-rights" />Gebruiksrechten

Wanneer iemand [!INCLUDE [prod_short](includes/prod_short.md)] opent met een Microsoft 365-licentie, geeft de licentie de gebruiker het recht om [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens te lezen (maar niet te schrijven) via een vereenvoudigde gebruikersinterface in Microsoft Teams. In dit gedeelte worden deze gebruiksrechten en -beperkingen uitgelegd die u helpen bij het plannen van de configuratie en het optimaal benutten van deze mogelijkheid. Raadpleeg voor meer informatie over dit licentietype in vergelijking met andere [!INCLUDE [prod_short](includes/prod_short.md)]-licenties de [Dynamics 365-licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### <a name="client-access" />Client-toegang

Gebruikers hebben recht op toegang tot [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens in Microsoft Teams. In de onderstaande tabel vindt u een overzicht van welke van de verschillende methoden voor toegang tot de [!INCLUDE [prod_short](includes/prod_short.md)]-service zijn toegestaan met deze licentie.

|Klant die de Business Central-service opent |Toegang|
|-|-|
|Business Central-app voor Microsoft Teams|![Ja](media/check.png)|
|Business Central-webclient |![Nee](media/x-icon.png ) |
|Mobiele Business Central-apps|![Nee](media/x-icon.png )|
|Business Central-API's|![Nee](media/x-icon.png )|
|Business Central-integraties met andere Office-toepassingen|![Nee](media/x-icon.png )|
|Business Central ingesloten in andere toepassingen |![Nee](media/x-icon.png )|

### <a name="data-access" />Toegang tot gegevens

Gebruikers mogen tabelgegevens lezen, maar kunnen geen records wijzigen, maken of verwijderen. Het [!INCLUDE [prod_short](includes/prod_short.md)]-platform voorkomt automatisch dat er naar gegevenstabellen wordt geschreven.  

### <a name="use-of-objects" />Gebruik van objecten

Toegang met Microsoft 365-licenties legt geen beperkingen op voor welke Business Central-objecten of objectbereiken toegang mogelijk is. Gebruikers hebben recht op toegang tot de Microsoft-basistoepassing en eventuele uitbreidingen zoals aanpassingen en add-on-apps.

## <a name="simplified-user-interface" />Vereenvoudigde gebruikersinterface

Gebruikers hebben recht op een beperkte set voorzieningen en functies die worden aangeboden door [!INCLUDE [prod_short](includes/prod_short.md)] in Microsoft Teams. In de onderstaande tabellen vindt u een aantal noemenswaardige functies. Deze lijst is niet volledig en kan worden gewijzigd.

Functies van de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams:

|Functie  |Beschikbaar|
|-|-|
|Bekijk [!INCLUDE [prod_short](includes/prod_short.md)]-kaarten|![Ja](media/check.png)|
|Kaartdetails weergeven |![Ja](media/check.png) |
|Kaartgegevens vastzetten als tabblad |![Ja](media/check.png)|
|[!INCLUDE [prod_short](includes/prod_short.md)]-tabbladen weergeven|![Ja](media/check.png)|
|Een [!INCLUDE [prod_short](includes/prod_short.md)]-tabblad toevoegen|![Nee_](media/x-icon.png )|
|Zakelijke contacten zoeken |![Nee](media/x-icon.png )|
|Een voorbeeld van een koppeling plakken en delen als een kaart|![Nee](media/x-icon.png )|

Functies van de [!INCLUDE [prod_short](includes/prod_short.md)]-client ingebed in Teams:

|Functie |Beschikbaar|Voorbeeldfuncties|
|-|-|-|
|Systeemacties voor gegevensmanipulatie |![Nee](media/x-icon.png )|Bewerken, maken, verwijderen|
|Basisfuncties in lijsten|![Ja](media/check.png)|Zoeken, sorteren, lay-out wijzigen|
|Geavanceerde functies in lijsten|![Nee](media/x-icon.png )|Filterdeelvenster, weergaven|
|Inzoomen van lijst naar kaart |![Ja](media/check.png)||
|Gegevens openen vanuit gerelateerde tabellen|![Nee](media/x-icon.png )|Feitenblokdeelvenster, veld-inzoomen, kijkje, opzoeken |
|Acties|![Nee](media/x-icon.png )|Actiebalk, actiemenu's, acties voor paginameldingen|
|Systeembrede sneltoetsen|![Nee](media/x-icon.png )|Mijn instellingen, Rolverkenner, Vertel me-zoeken  |
|Kopiëren|![Ja](media/check.png)|Rijen kopiëren, veldwaarde kopiëren, koppeling naar pagina kopiëren|
|UI-aanpassing|![Nee](media/x-icon.png )|Personaliseren| 
|Inline-aanpassing|![Ja](media/check.png)|Grootte van kolom wijzigen, Uitvouwen/samenvouwen, Meer tonen |
|Delen van gegevens |![Nee](media/x-icon.png )|Openen of bewerken in Excel, delen naar Teams|
|Inline gebruikersondersteuning|![Ja](media/check.png) |Knopinfo, koppelingen naar documentatie|
|Geavanceerde gebruikersondersteuning |![Nee](media/x-icon.png )|Leertips voor pagina en veld, Help-deelvenster|

## <a name="minimum-requirements" />Minimumvereisten

In dit gedeelte worden de minimale vereisten beschreven waaraan uw organisatie moet voldoen om toegang met Microsoft 365-licenties mogelijk te maken, en voor individuele Microsoft Teams-gebruikers om toegang te krijgen tot [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens zonder een [!INCLUDE [prod_short](includes/prod_short.md)]-licentie.

### <a name="requirements-to-enable-access" />Vereisten om toegang in te schakelen

- [!INCLUDE [prod_short](includes/prod_short.md)] online (SaaS).

- Omgevingen moeten platformversie 21.1 of hoger zijn.

### <a name="requirements-for-individual-users-to-access-data-in-teams" />Vereisten voor individuele gebruikers om toegang te krijgen tot gegevens in Teams

- Gegevens moeten toegankelijk zijn via de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams. Gebruikers moeten de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams hebben geïnstalleerd en moeten een van de ondersteunde Teams-clients gebruiken. Voor een lijst met Teams-clients die worden ondersteund door [!INCLUDE [prod_short](includes/prod_short.md)] raadpleegt u [Minimumvereisten om Business Central te gebruiken](product-requirements.md#teams).

- Gebruikers moeten intern zijn in de organisatie, wat betekent dat een gebruikersidentiteit afkomstig is van dezelfde thuistenant waar [!INCLUDE [prod_short](includes/prod_short.md)] is geïmplementeerd en waar toegang is ingeschakeld. Externe identiteiten worden niet ondersteund. [!INCLUDE [prod_short](includes/prod_short.md)] verhindert automatisch toegang voor gasten.

- Gebruikers moeten een Microsoft 365-licentie van een van de volgende abonnementen hebben.
  
  |Ondersteund abonnement|Product-id |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Azure AD-identiteit) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  De meeste aanbiedingen op basis van deze abonnementen worden ook ondersteund. Als u zich bijvoorbeeld abonneert op Microsoft 365 Business Premium (Non-profit Staff Pricing), is dit een specifieke aanbieding voor non-profitorganisaties op basis van het Microsoft 365 Business Premium-abonnement en wordt het daarom ondersteund.

  > [!NOTE]
  > Kunt u uw abonnement niet vinden in de lijst? Microsoft is voortdurend op zoek naar feedback over hoe we onze service kunnen verbeteren en ons aanbod kunnen uitbreiden, zodat meer klanten van deze mogelijkheid kunnen profiteren. Deel uw idee voor welke abonnementen we in de toekomst moeten gaan ondersteunen op [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Gebruikers moeten een Microsoft 365-licentie waarbij de Microsoft Teams-app ingeschakeld is in de lijst met apps voor die licentie.

  |Ondersteunde apps|Serviceplan-id|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- De organisatie moet ten minste één andere gebruiker hebben die is toegewezen aan een Dynamics 365 Business Central-licentie.

## <a name="next-steps" />Volgende stappen

- Krijg inzicht in de gebruikerstoegangsstroom om u te helpen bij het plannen van uw aanpak en configuratie van Business Central om aan de zakelijke behoeften te voldoen. Zie [Gebruikerstoegangsstroom](admin-access-with-m365-license-flow.md).
- Stel uw omgeving en gebruikers in voor toegang met Microsoft 365-licenties. Zie [Toegang instellen met Microsoft 365-licenties ](admin-access-with-m365-license-setup.md).

## <a name="see-also" />Zie ook

[Integratie van Business Central en Microsoft Teams](across-teams-overview.md)  
