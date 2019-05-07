---
title: Rapporten maken met XBRL | Microsoft Docs
description: XBRL staat voor eXtensible Business Reporting Language, is een op XML gebaseerde taal voor het coderen van financiële gegevens waardoor bedrijven efficiënt en nauwkeurig hun gegevens kunnen verwerken en delen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0576f2e7b93040118d2ef31458939d9b9822a6aa
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922027"
---
# <a name="create-reports-with-xbrl"></a>Lijsten met XBRL maken
XBRL staat voor eXtensible Business Reporting Language, is een op XML gebaseerde taal voor het coderen van financiële gegevens waardoor bedrijven efficiënt en nauwkeurig hun gegevens kunnen verwerken en delen. Door het XBRL-initiatief zijn talloze ERP-softwarebedrijven en internationale financiële organisaties in staat hun globale financiële rapportageactiviteiten uit te voeren. Het doel van het initiatief is een standaard vormen voor de uniforme rapportage van financiële gegevens voor banken, investeerders en overheidsinstanties. Dergelijke zakelijke rapportage kan omvatten:  

 • Financiële overzichten  
 • Financiële informatie  
 • Niet-financiële informatie  
 • Wettelijke archivering, zoals jaarlijkse en driemaandelijkse financiële overzichten  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] maakt het bedrijven mogelijk gegevens in XBRL te implementeren en te profiteren van de hierdoor mogelijk gemaakte flexibiliteit en automatisering voor het verzamelen en delen van gegevens.  

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language
XBRL (e **X**tensible **B**usiness **R**eporting **L**anguage) is een op XML gebaseerde taal voor financiële verslaglegging. XBRL biedt een standaardindeling waarmee een uniforme rapportage mogelijk wordt voor alle gebruikers die betrokken zijn bij de financiële gegevensstroom, zoals overheidsbedrijven en particuliere bedrijven, accountants, regelgevende instanties, analisten, investeringsmaatschappijen, de kapitaalmarkt en financiers, alsmede belangrijke derden zoals softwareontwikkelaars en gegevensbanken.  

De taxonomieën worden beheerd door www.xbrl.org. Op deze website kunt u taxonomieën downloaden en meer informatie over XBRL lezen.  

Iemand die financiële gegevens van u wil, voorziet u van een taxonomie (een XML-document) met een of meer schema's, elk met een of meer regels die moeten worden ingevuld. De regels komen overeen met de specifieke financiële gegevens die de afzender opvraagt. U importeert deze taxonomie in het programma en vult vervolgens het schema of de schema's in door op te geven welke rekening of rekeningen met elke regel overeenkomt/overeenkomen, welk tijdvenster moet worden gebruikt, bijvoorbeeld mutatie of saldobedragen. In sommige gevallen kunt u in plaats daarvan een constante invoeren, bijvoorbeeld het aantal werknemers. U bent nu gereed om het instantiedocument (een XML-document) verzenden naar iemand die de gegevens opvraagt. Het idee is dat dit een terugkerende gebeurtenis kan zijn, dus tenzij er wijzigingen zijn aangebracht aan de taxonomie, moet u op aanvraag nieuwe instantiedocumenten voor nieuwe periodes exporteren.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL bestaat uit de volgende onderdelen:  
De XBRL- **specificatie** legt uit wat XBRL is en hoe XBRL-instantiedocumenten en XBRL-taxonomieën worden gemaakt. De XBRL-specificatie geeft een technische uitleg van XBRL en is bestemd voor mensen met een technische achtergrond.  

Het XBRL- **schema** bevat de belangrijkste low-level XBRL-onderdelen. Het schema is het fysieke XSD-bestand dat aangeeft hoe instantiedocumenten en taxonomieën worden samengesteld.  

De XBRL- **linkbases** zijn de fysieke XML-bestanden waarin uiteenlopende informatie staat over de onderdelen die worden gedefinieerd in het XBRL-schema, zoals labels in een of meer talen, de onderlinge relatie tussen onderdelen, hoe onderdelen worden berekend, enz.  

Een XBRL- **taxonomie** is het 'vocabulaire' of 'woordenboek' dat in overeenstemming met de XBRL-specificatie is samengesteld door een groep, ten behoeve van de uitwisseling van zakelijke gegevens.  

Een XBRL- **instantiedocument** is een zakelijk rapport, zoals een financieel overzicht, dat is samengesteld volgens de XBRL-specificatie. De betekenis van de waarden in het instantiedocument wordt uitgelegd in de taxonomie. Een instantiedocument krijgt pas betekenis als u de taxonomie kent waarmee het document is gemaakt.  

## <a name="layered-taxonomies"></a>Laagsgewijze taxonomieën  
Een taxonomie kan bestaan uit een basistaxonomie, zoals us-gaap of IAS, waaraan een of meer uitbreidingen zijn toegevoegd. De taxonomie verwijst dan naar een of meer schema's die elk weer een afzonderlijke taxonomie vormen. Als u deze extra taxonomieën in de database laadt, worden de nieuwe onderdelen eenvoudig aan de bestaande onderdelen toegevoegd.  

## <a name="linkbases"></a>Linkbases  
 In de XBRL-specificatie. 2 wordt de taxonomie beschreven in verschillende XML-bestanden. Het primaire XML-bestand is het taxonomieschemabestand zelf (.xsd-bestand) dat alleen een ongeordende lijst van elementen of feiten bevat die moeten worden gerapporteerd. Naast deze zijn er meestal enkele linkbasebestanden (.xml) aan gekoppeld. De linkbasebestanden bevatten gegevens die een aanvulling op de ruwe taxonomie (.xsd-bestand) vormen. Er zijn zes soorten linkbase bestanden, waarvan er vier relevant zijn voor Productnaam XBRL. Dit zijn:  

-   Label linkbase: deze linkbase bevat labels of namen voor de elementen. Het bevat mogelijk labels in verschillende talen en deze worden aangeduid met een XML-eigenschap die 'lang' wordt genoemd. De XML-taalidentifier bevat meestal een afkorting van twee letters en hoewel gemakkelijk te raden moeten zijn wat de afkorting betekent, is er geen verbinding met de Windows- taalcode of de taalcodes in de demonstratiegegevens. Dus wanneer de gebruiker zoekt naar de talen voor een bepaalde taxonomie, ziet hij de labels voor het eerste element in de taxonomie, wat betekent dat hij dan een voorbeeld van elke taal kan zien. Aan een taxonomie kunnen meerdere label-linkbases gekoppeld zijn zolang deze linkbases verschillende talen bevatten.  

-   Presentatielinkbase: deze linkbase bevat informatie over de onderdelenstructuur. U kunt dit beschouwen als het voorstel van de taxonomie-uitgever voor de wijze waarop de taxonomie door het programma aan de gebruiker wordt gepresenteerd. De linkbase bevat een reeks koppelingen die elk twee elementen verbinden als bovenliggende en onderliggende. Als alle koppelingen worden toegepast, kunnen de onderdelen hiërarchisch worden weergegeven. De presentatielinkbase heeft één functie: elementen aan de gebruiker presenteren.  

-   Linkbaseberekening: deze linkbase bevat informatie over welke elementen bij welk niveau horen. De structuur is vergelijkbaar met de presentatielinkbase, behalve dat elke koppeling of 'arc', zoals ze worden genoemd, een gewichtseigenschap heeft. Het gewicht kan 1 of –1 zijn, wat aangeeft of het element aan het bovenliggende element moet worden toegevoegd of ervan moet worden afgetrokken. De samentellingen hoeven niet per se in overeenstemming te zijn met de visuele presentatie.  

-   Referentielinkbase: Deze linkbase bestaat uit een XML-bestand met aanvullende informatie over de gegevens die de taxonomie-uitgever nodig heeft.

## <a name="to-set-up-xbrl-lines"></a>XBRL-regels instellen  
Als u de taxonomie hebt geïmporteerd of bijgewerkt, moeten de schemaregels van alle vereiste gegevens worden voorzien. Het gaat om informatie zoals de standaard bedrijfsgegevens, actuele financiële overzichten, notities bij de financiële overzichten, aanvullende schema's en andere gegevens die nodig zijn om te voldoen aan de specifieke vereisten voor financiële verslaglegging.  

U kunt de XBRL-regels instellen door de gegevens in de taxonomie te koppelen aan de gegevens in uw grootboek.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XBRL-taxonomieën** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer op de pagina **XBRL-taxonomieën** een taxonomie uit de lijst.  
3.  Kies de actie **Regels**.  
4.  Selecteer een regel en vul de velden in.   
5.  Kies de actie **Informatie** voor meer informatie over wat u moet invullen.  
6.  Om de koppeling tussen de grootboekrekeningen in het rekeningschema en de XBRL-regels in te stellen, kiest u de actie **Grootboekkoppelingsregels**.  
7.  Als u notities aan het financieel overzicht wilt toevoegen, kiest u de actie **Notities**.  

> [!NOTE]  
>  U kunt alleen gegevens (inclusief omschrijving en notities) exporteren die overeenkomen met het bronsoort dat u hebt geselecteerd in het veld **Bronsoort**.  

> [!NOTE]  
>  U kunt niet-relevante regels markeren met het regelsoort **NOT APPLICABLE** (niet van toepassing) zodat ze niet worden geëxporteerd.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Een XBRL-taxonomie importeren  
De eerste stap bij het werken met de XBRL-functie is het importeren van een taxonomie in de database van uw bedrijf. Een taxonomie bestaat uit een of meer schema's en een aantal linkbases. Nadat u de schema's en linkbases hebt geïmporteerd en de linkbases op het schema hebt toegepast, kunt u de regels instellen en de grootboekrekeningen in het rekeningstelsel koppelen aan de juiste taxonomieregels.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XBRL-taxonomieën** in en kies vervolgens de gerelateerde koppeling.  
2.  Maak op de pagina **XBRL-taxonomieën** een nieuwe regel en voer de naam en de omschrijving van de taxonomie in.  
3.  Kies de actie **Schema's** en voeg de omschrijving van het schema in.  
4.  Om het schema te importeren, kiest u op de pagina **XBRL-schema's** de actie **Importeren** en selecteert u een map en een XSD-bestand. Kies de knop **Openen**.  
5.  Om de linkbase te importeren, kiest u op de pagina **XBRL-schema's** de actie **Linkbases** en selecteert u een map en een XML-bestand. Kies de knop **Openen**.  
6.  U kunt de linkbase nu op het stelsel toepassen. Doe hetzelfde om de overige linkbases te importeren.  
7. Kies de actie **Op taxonomie toepassen** om de linkbase op het schema toe te passen.  

> [!IMPORTANT]  
>  In plaats van het afzonderlijk toepassen van de linkbases na het importeren, kunt u wachten tot u alle linkbases hebt geïmporteerd en deze vervolgens op hetzelfde moment toepassen. Kies hiervoor de knop **NEE** wanneer u wordt gevraagd om de zojuist geïmporteerde linkbase op het schema toe te passen. Selecteer vervolgens de regels met de linkbases die u wilt toepassen.  

## <a name="to-update-an-xbrl-taxonomy"></a>Een XBRL-taxonomie bijwerken  
Als een taxonomie verandert, moet u de huidige taxonomie overeenkomstig bijwerken. De reden voor de update kan een gewijzigd schema, een gewijzigde linkbase of een nieuwe linkbase zijn. Nadat u de taxonomie hebt bijgewerkt, moet u alleen nog de regels koppelen voor de gewijzigde of nieuwe regels.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XBRL-taxonomieën** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies op de pagina **XBRL-taxonomieën** de actie **Schema's**.  
3.  Werk een schema bij door het schema te selecteren dat u wilt bijwerken en kies de actie **Importeren**.  
4.  Kies de actie **Linkbases** voor het bijwerken of toevoegen van een nieuwe linkbase.  
5.  Selecteer de betreffende linkbase of druk op Ctrl+N voor een nieuwe regel, selecteer het soort linkbase en voer een omschrijving in.  
6.  U importeert de linkbase door de actie **Importeren** te kiezen.  
7.  Kies de knop **Ja** om de linkbase op het schema toe te passen.  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)    
[Bedrijfsinformatie](bi.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
