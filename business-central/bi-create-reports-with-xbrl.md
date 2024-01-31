---
title: 'Procedure: Rapporten maken met XBRL'
description: XBRL is een op XML gebaseerde taal voor het taggen van financiële gegevens en het activeren van bedrijven om efficiënt en accuraat hun gegevens te verwerken en te delen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Lijsten met XBRL maken

> [!NOTE]
> We zijn bezig met het verwijderen van de functies voor XBRL-rapportage vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Meer informatie vindt u in [Wijzigingen in releasewave 1 van 2022](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e**X**tensible **B**usiness **R**eporting **L**anguage) is een op XML (eXtensible Markup Language) gebaseerde taal voor het coderen van financiële gegevens waardoor bedrijven efficiënt en nauwkeurig hun gegevens kunnen verwerken en delen. Door het XBRL-initiatief zijn talloze ERP-softwarebedrijven (enterprise resource planning) en internationale financiële organisaties in staat hun globale financiële rapportageactiviteiten uit te voeren. Het doel van het initiatief is een standaard vormen voor de uniforme rapportage van financiële gegevens voor banken, investeerders en overheidsinstanties. Dergelijke zakelijke rapportage kan omvatten:  

* Financiële overzichten  
* Financiële informatie  
* Niet-financiële informatie  
* Wettelijke archivering, zoals jaarlijkse en driemaandelijkse financiële overzichten  

> [!NOTE]
> U kunt grootboekgerelateerde schema's importeren en XBRL-instantiedocumenten maken door grootboekgegevens (G/L) uit het rekeningschema toe te wijzen aan elementen in taxonomieën die zijn ontworpen voor financiële rapporten, zoals balansen, resultatenrekeningen, enzovoort.
>
> De XBRL-mogelijkheden in Business Central ondersteunen taxonomieën voor specificatie 2.1. Taxonomieën kunnen echter niet-ondersteunde elementen bevatten, zoals formule-linkbases of iXBRL (inline XBRL), of andere structurele verschillen hebben. We raden u aan de XBRL-mogelijkheid te valideren voordat u deze voor rapportage gebruikt.
>
> Volledige ondersteuning voor taxonomieën vereist mogelijk XBRL-tagging en tools van derden. De organisatie XBRL International heeft een lijst met tools en diensten; afhankelijk van de XBRL-rapportagevereisten voor een bepaalde taxonomie. Het is mogelijk een goed idee om deze bronnen te verkennen. Meer informatie vindt u in [Aan de slag voor bedrijven](https://go.microsoft.com/fwlink/?linkid=2153466) en [Tools en services](https://go.microsoft.com/fwlink/?linkid=2153356).

## eXtensible Business Reporting Language

De XBRL-taxonomieën worden beheerd door www.xbrl.org. Op de website van XBRL kunt u taxonomieën downloaden en meer informatie over XBRL lezen.  

Stel dat iemand financiële informatie van u wil. Deze persoon voorziet u van een taxonomie (een XML-document) met een of meer schema's, elk met een of meer regels die moeten worden ingevuld. De regels komen overeen met de specifieke financiële gegevens die de afzender opvraagt. U importeert deze taxonomie en vult vervolgens het schema of de schema's in door op te geven welke rekening of rekeningen met elke regel overeenkomt/overeenkomen en welk berekening nodig is, bijvoorbeeld mutatie of saldobedragen. In sommige gevallen kunt u in plaats daarvan een constante invoeren, bijvoorbeeld het aantal werknemers. U bent nu gereed om het instantiedocument (een XML-document) te verzenden naar iemand die de gegevens opvraagt. Het idee is dat dit een terugkerende gebeurtenis kan zijn, dus tenzij er wijzigingen zijn aangebracht aan de taxonomie, moet u op aanvraag nieuwe instantiedocumenten voor nieuwe periodes exporteren.

## XBRL omvat de volgende onderdelen

De XBRL-**specificatie** legt uit wat XBRL is en hoe XBRL-instantiedocumenten en taxonomieën worden gemaakt. De XBRL-specificatie geeft een technische uitleg van XBRL en is bestemd voor mensen met een technische achtergrond.  

Het XBRL- **schema** bevat de belangrijkste low-level XBRL-onderdelen. Het schema is het fysieke XSD-bestand (ook wel een XML-schemadefinitie genoemd) dat aangeeft hoe XBRL-instantiedocumenten en taxonomieën worden samengesteld.

De XBRL-**linkbases** zijn de fysieke XML-bestanden waarin informatie staat over de onderdelen die worden gedefinieerd in het XBRL-schema, zoals labels in een of meer talen, de onderlinge relatie tussen onderdelen, hoe onderdelen worden berekend, enzovoort.  

Een XBRL- **taxonomie** is het 'vocabulaire' of 'woordenboek' dat in overeenstemming met de XBRL-specificatie is samengesteld door een groep en uitwisseling van zakelijke gegevens mogelijk maakt.  

Een XBRL- **instantiedocument** is een zakelijk rapport, zoals een financieel overzicht, dat is samengesteld volgens de XBRL-specificatie. De betekenis van de waarden in het instantiedocument wordt uitgelegd in de taxonomie. Een instantiedocument krijgt pas betekenis als u de taxonomie kent waarvoor het document is gemaakt.  

## Laagsgewijze taxonomieën

Een taxonomie kan bestaan uit een basistaxonomie, bijvoorbeeld US GAAP (United States generally accepted accounting principles) of IAS (International Accounting Standards), en vervolgens een of meer extensies hebben. De taxonomie verwijst dan naar een of meer schema's die elk zelf weer een afzonderlijke taxonomie vormen. Als u deze extra taxonomieën in de database laadt, worden de nieuwe onderdelen eenvoudig aan de bestaande onderdelen toegevoegd.  

## Linkbases

In de XBRL-specificatie 2 wordt de taxonomie beschreven in verschillende XML-bestanden. Het primaire XML-bestand is het taxonomieschemabestand zelf (.xsd-bestand) dat alleen een ongeordende lijst van elementen of feiten bevat die moeten worden gerapporteerd. Naast deze zijn er meestal enkele linkbasebestanden (.xml). De linkbasebestanden bevatten gegevens die een aanvulling op de ruwe taxonomie (.xsd-bestand) vormen. Er zijn zes soorten linkbasebestanden, waarvan er vier relevant zijn voor [!INCLUDE[prod_short](includes/prod_short.md)]. Dit zijn:

* Label linkbase: deze linkbase bevat labels of namen voor de elementen. Het bevat mogelijk labels in verschillende talen en deze worden aangeduid met een XML-eigenschap die 'lang' wordt genoemd. De XML-taal-id bevat meestal een afkorting van twee letters en hoewel gemakkelijk te raden moeten zijn wat de afkorting betekent, is er geen verbinding met de Microsoft Windows-taalcode of de taalcodes in de demonstratiegegevens. Dus wanneer u zoekt naar de talen voor een bepaalde taxonomie, ziet u de labels voor het eerste element in de taxonomie, wat betekent dat u dan een voorbeeld van elke taal kunt zien. Aan een taxonomie kunnen meerdere label-linkbases gekoppeld zijn zolang die linkbases verschillende talen bevatten.  
* Presentatielinkbase: deze linkbase bevat informatie over de onderdelenstructuur. U kunt dit beschouwen als het voorstel van de taxonomie-uitgever voor de wijze waarop de taxonomie door de toepassing aan u wordt gepresenteerd. De linkbase bevat een reeks koppelingen die elk twee elementen verbinden in bovenliggende-onderliggende relatie. Als alle koppelingen worden toegepast, kunnen de onderdelen hiërarchisch worden weergegeven. De presentatielinkbase heeft één functie: elementen aan u presenteren.
* Linkbaseberekening: deze linkbase bevat informatie over welke elementen bij welk niveau horen. De structuur is vergelijkbaar met de presentatielinkbase, behalve dat elke koppeling, of 'arc' zoals ze worden genoemd, een gewichtseigenschap heeft. Het gewicht kan 1 of –1 zijn, wat aangeeft of het element aan het bovenliggende element moet worden toegevoegd of ervan moet worden afgetrokken. De samentellingen hoeven niet per se in overeenstemming te zijn met de visuele presentatie.  
* Referentielinkbase: Deze linkbase bestaat uit een XML-bestand met aanvullende informatie over de gegevens die de taxonomie-uitgever nodig heeft.

## XBRL-regels instellen

Als u de taxonomie hebt geïmporteerd of bijgewerkt, moeten de schemaregels van alle vereiste gegevens worden voorzien om aan de specifieke vereisten voor financiële rapportage te voldoen. Deze informatie omvat basisbedrijfsgegevens, financiële overzichten, notities bij de financiële overzichten, aanvullende schema’s enzovoort.  

U kunt de XBRL-regels instellen door de gegevens in de taxonomie te koppelen aan de gegevens in uw grootboek.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XBRL-taxonomieën** in en kies vervolgens de gerelateerde koppeling  
2. Selecteer op de pagina **XBRL-taxonomieën** een taxonomie uit de lijst.  
3. Kies de actie **Regels**.  
4. Selecteer een regel en vul de velden in.  
5. Kies de actie **Informatie** voor meer informatie over wat u moet invullen.  
6. Om de koppeling tussen de grootboekrekeningen in het rekeningschema en de XBRL-regels in te stellen, kiest u de actie **Grootboekkoppelingsregels**.  
7. Als u notities aan het financieel overzicht wilt toevoegen, kiest u de actie **Notities**.  

   > [!TIP]
   > Kies om regels uit te sluiten van de geëxporteerde gegevens **NIET TOEPASBAAR** als de bronsoort.

   > [!NOTE]  
   > U kunt alleen gegevens exporteren die overeenkomen met de selectie in het veld **Brontype**. Dit omvat beschrijvingen en opmerkingen.  

   > [!NOTE]  
   > Taxonomieën kunnen elementen bevatten die [!INCLUDE[prod_short](includes/prod_short.md)] niet ondersteunt. Als een element niet wordt ondersteund, bevat het veld **Bronsoort** **Niet toepasbaar** en bevat het veld **Omschrijving** een foutmelding, zoals **Onverwacht type: "specifiek type niet herkend"**. Als u het element moet exporteren, kiest u een overeenkomend brontype. Meestal is dit een constante of een beschrijving. Hierdoor kunt u gegevens invoeren en exporteren, maar dergelijke elementen kunnen validatieregels hebben die niet kunnen worden gecontroleerd voordat ze worden geëxporteerd.

## Een XBRL-taxonomie importeren

De eerste stap bij het werken met de XBRL-functie is het importeren van een taxonomie in de database van uw bedrijf. Een taxonomie bestaat uit een of meer schema's en een aantal linkbases. Nadat u de schema's en linkbases hebt geïmporteerd en de linkbases op het schema hebt toegepast, kunt u de regels instellen en de grootboekrekeningen in het rekeningstelsel koppelen aan de juiste taxonomieregels.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XBRL-taxonomieën** in en kies vervolgens de gerelateerde koppeling  
2. Maak op de pagina **XBRL-taxonomieën** een nieuwe regel en voer de naam en de omschrijving van de taxonomie in.  
3. Kies de actie **Schema's** en voeg vervolgens de omschrijving van het schema in.  
4. Om het schema te importeren, kiest u op de pgaina **XBRL-schema´s** de actie **Importeren** en voert u een van de volgende handelingen uit stappen om het bestand te uploaden:

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Om de linkbase te importeren, kiest u op de pagina **XBRL-schema´s** de actie **Linkbases** en voert u een van de volgende handelingen uit stappen om het bestand te uploaden:

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. U kunt de linkbase nu op het stelsel toepassen. Doe hetzelfde om de overige linkbases te importeren.  
7. Kies de actie **Op taxonomie toepassen** om de linkbase op het schema toe te passen.  

> [!IMPORTANT]  
> In plaats van het afzonderlijk toepassen van de linkbases na het importeren, kunt u wachten tot u alle linkbases hebt geïmporteerd en deze vervolgens op hetzelfde moment toepassen. Kies hiervoor **NEE** wanneer u wordt gevraagd om de zojuist geïmporteerde linkbase op het schema toe te passen. Selecteer vervolgens de regels met de linkbases die u wilt toepassen.  

## Een XBRL-taxonomie bijwerken

Als een taxonomie verandert, moet u de huidige taxonomie overeenkomstig bijwerken. De reden voor de update kan een gewijzigd schema, een gewijzigde linkbase of een nieuwe linkbase zijn. Nadat u de taxonomie hebt bijgewerkt, moet u alleen nog de regels koppelen voor de gewijzigde of nieuwe regels.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XBRL-taxonomieën** in en kies vervolgens de gerelateerde koppeling  
2. Kies op de pagina **XBRL-taxonomieën** de actie **Schema's**.  
3. Werk een schema bij door het schema te selecteren dat u wilt bijwerken en kies de actie **Importeren**.  
4. Kies de actie **Linkbases** voor het bijwerken of toevoegen van een nieuwe linkbase.  
5. Selecteer de betreffende linkbase of selecteer <kbd>Ctrl</kbd>+<kbd>N</kbd> voor een nieuwe regel, selecteer het soort linkbase en voer vervolgens een omschrijving in.  
6. U importeert de linkbase door de actie **Importeren** te kiezen.  
7. Kies **Ja** om de linkbase op het schema toe te passen.  

## Zie ook

[Financiële Business Intelligence](bi.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
