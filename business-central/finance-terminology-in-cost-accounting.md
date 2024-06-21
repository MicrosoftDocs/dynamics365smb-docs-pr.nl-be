---
title: Terminologie in kostprijsboekhouding
description: 'Dit onderwerp definieert de belangrijkste termen die worden gebruikt in kostenberekening, zoals verdeelsleutel en verdeelbron.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 1123
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="terminology-in-cost-accounting"></a>Terminologie in kostprijsboekhouding

Dit onderwerp beschrijft de belangrijkste termen die worden gebruikt in kostprijsboekhouding.  

## <a name="key-terms"></a>Belangrijke termen

 De volgende tabel bevat definities van belangrijke termen in kostprijsboekhouding.  

|**Term**|**Definitie**|  
|--------------|--------------------|  
|Toewijzingssleutel|De toewijzingssleutel is de basis die wordt gebruikt voor het toewijzen van kosten. Meestal is het aantal vierkante meters bezet, het aantal werknemers of manuren gebruikt. Bijvoorbeeld, twee afdelingen met respectievelijk 20 en 10 werknemers delen kantinekosten. De kosten worden verdeeld tussen de afdelingen via een verdeelsleutel die het aantal werknemers vertegenwoordigt. Tweederde van de kosten worden toegewezen aan de eerste afdeling en eenderde van de kosten worden toegewezen aan de tweede afdeling.|  
|Toewijzingsbron|De verdelingsbron bepaalt welke kosten worden toegerekend. Toewijzingen zijn gedefinieerd in verdelingsbron- en verdeeldoeltabellen. Elke toewijzing bestaat uit een verdelingsbron en een of meer verdeeldoelen. Bijvoorbeeld kunnen alle kosten voor de kostensoort verwarming, die een verdelingsbron is, worden toegewezen aan de kostenplaatsen workshop, productie en verkoop, die drie verdeeldoelen zijn.|  
|Toewijzingsdoel|De verdeeldoelen bepalen waaraan de kosten worden toegerekend. Toewijzingen zijn gedefinieerd in verdelingsbron- en verdeeldoeltabellen. Elke toewijzing bestaat uit een verdelingsbron en een of meer verdeeldoelen. Bijvoorbeeld kunnen alle kosten voor de kostensoort verwarming, die een verdelingsbron is, worden toegewezen aan de kostenplaatsen workshop, productie en verkoop, die drie verdeeldoelen zijn.|  
|Kostprijsboekhouding|In de kostprijsboekhouding worden werkelijke kosten voor bewerkingen, proceskosten, afdelingskosten of productkosten vastgelegd. Deze kosten worden toegewezen aan kostenplaatsen en kostenobjecten met behulp van verschillende methoden voor kostenverdeling. Managers gebruiken statistieken en rapporten zoals kostenverdelingsbladen en winst- en verliesanalyses om beslissingen te kunnen nemen en kosten te verlagen. De kostprijsboekhouding haalt gegevens op uit het grootboek, maar werkt onafhankelijk daarvan. Daarom zijn transacties die in de kostprijsboekhouding zijn geboekt niet van invloed op de gegevens in het grootboek.|  
|Kostensoort|Het schema met kostensoorten heeft dezelfde functie als het rekeningschema in het grootboek. Ze zijn vaak op dezelfde manier gestructureerd. Daarom is het mogelijk om het grootboekrekeningschema over te brengen naar het schema met kostensoorten en dit vervolgens te wijzigen. Het schema van kostensoorten kan ook helemaal vanaf de basis worden gemaakt.|  
|Kostenplaats|Kostenplaatsen zijn meestal afdelingen en resultatencentra die grotendeels verantwoordelijk zijn voor de kosten en baten van een bedrijf. Kostenplaatsen kunnen worden gesynchroniseerd met dimensies in het grootboek. Het is ook mogelijk om nieuwe kostenplaatsen toe te voegen en hun eigen sorteerfunctie met subtotalen te definiëren.|  
|Kostenobject|Kostenobjecten zijn producten, productgroepen of diensten van een bedrijf of de gereedgemelde goederen van een bedrijf die iuiteindelijk verantwoordelijk zijn voor de kosten. Kostenobjecten kunnen worden gesynchroniseerd met dimensies in het grootboek. Het is ook mogelijk om nieuwe kostenobjecten toe te voegen en hun eigen sorteerfunctie met subtotalen te definiëren.|  
|Kostenverdeling|Kostenverdeling is een proces waarbij kosten worden toegerekend aan kostenplaatsen of kostenobjecten. Het salaris van de vrachtwagenchauffeur van de verkoopafdeling wordt bijvoorbeeld toegewezen aan de kostenplaats verkoopafdeling. Het is niet nodig om het salaris aan andere kostenplaatsen toe te wijzen. Een ander voorbeeld is een geval waarbij de kosten van een kostbaar computersysteem worden toegerekend aan de producten van het bedrijf waarvoor het systeem wordt gebruikt.|  
|Dynamische toewijzing|Dynamische toewijzingen zijn afhankelijk van de wijzigbare toewijzingsbases, bijvoorbeeld het aantal werknemers van de afdeling of de omzet van het project binnen een bepaalde periode. Er zijn negen vooraf gedefinieerde dynamische toewijzingbases die gebruikers met behulp van vijf filters kunnen definiëren.|  
|Directe kosten|Directe kosten zijn de kosten die rechtstreeks toegerekend kunnen worden aan een kostenobject, bijvoorbeeld materiaal dat voor een specifiek product is ingekocht.|  
|vaste kosten|Vaste kosten zijn de kosten die niet afhankelijk zijn van het goederen- of dienstenniveau dat door het bedrijf wordt geproduceerd. Ze zijn vaak tijdgerelateerd, zoals salarissen of huren die per maand worden betaald. In tegenstelling tot de variabele kosten die volumegerelateerd zijn en per geproduceerde hoeveelheid worden betaald.|  
|Indirecte kosten|Indirecte kosten zijn niet rechtstreeks toe te schrijven aan een kostenobject, zoals een bepaalde functie of product. Indirecte kosten kunnen vast of variabel zijn. Indirecte kosten kunnen belastingen zijn, of administratiekosten, kosten voor personeel en beveiligingskosten zijn, en staan ook bekend als overheadkosten.|  
|Niveau|Niveau wordt gebruikt om de volgorde van toewijzing definiëren. Hiermee geeft u een niveau op als een getal tussen 1 en 99. De verdelingsboeking volgt de volgorde van de niveaus. Niveau garandeert bijvoorbeeld dat eerste de administratie wordt toegewezen aan workshop voordat workshop wordt toegewezen aan voertuigen en productie.|  
|Statische toewijzing|Statische toewijzingen zijn gebaseerd op een vaste reeks waarden voor bijvoorbeeld vierkante meters gebruikt of een vastgestelde verdeelsleutel, zoals 5:2:4.|  
|Operationele kosten|Operationele kosten zijn de terugkerende uitgaven die verband houden met de activiteiten van een bedrijf, een apparaat en een onderdeel.|  
|Overheadkosten|Overheadkosten verwijzen naar lopende exploitatiekosten van een bedrijf. Dit zijn allemaal kosten die voorkomen in de resultatenrekening, met uitzondering van directe arbeid, directe materialen en directe kosten. Overheadkosten zijn administratieve kosten, reclame, afschrijving, verzekering, rente, juridische kosten, huur, reparaties, leveringen, belastingen, telefoonrekeningen, reizen en kosten voor energie, water, etc.|  
|Trapsgewijze variabele kosten|Trapsgewijze variabele kosten zijn kosten die op bepaalde momenten aanzienlijk variëren omdat er grote aankopen mee gemoeid zijn die niet over een periode kunnen worden uitgesmeerd. Een werknemer kan bijvoorbeeld 100 tafels produceren in een maand. Het salaris van de werknemer is constant voor een serie van 1 tot 100 geproduceerde tafels Als het bedrijf 110 tafels wil produceren, heeft het bedrijf twee werknemers nodig. Zo worden de kosten verdubbeld.|  
|Aandeel|Het deel of onderdeel dat is verdeeld over kostenplaatsen of kostenobjecten.|  
|Statische weging|Kosten worden toegewezen volgens verdeelsleutels die kunnen worden gewijzigd met een vermenigvuldigingsfactor. <br />Bijvoorbeeld, twee afdelingen met respectievelijk 20 en 10 werknemers delen kantinekosten. De kosten worden verdeeld tussen de afdelingen via een verdeelsleutel die het aantal werknemers vertegenwoordigt dat in de kantine eet. Van de eerste afdeling eten slechts 5 medewerkers in de kantine, zodat deze afdeling een vermenigvuldigingsfactor van 0,25 heeft. De basis waarop de toewijzing plaatsvindt is 0,25 = 20 x 5. Het totale aantal werknemers dat in de kantine eet is 15. Eenderde van de kosten wordt toegewezen aan de eerste afdeling en tweederde van de kosten worden toegewezen aan de tweede afdeling.|  
|Variabele kosten|Variabele kosten zijn kosten die wijzigen in relatie met de activiteiten van een bedrijf. Variabele kosten zijn de som van de marginale kosten over alle geproduceerde eenheden. Vaste en variabele kosten vormen de twee onderdelen van de totale kosten.|  
|Variant|Een variant wordt gebruikt als een optioneel door de gebruiker gedefinieerd label voor toewijzingen. Het doel van het label is toegewezen groepen filteren.|  

## <a name="see-also"></a>Zie ook

 [Over kostprijsboekhouding](finance-about-cost-accounting.md)  
 [Kosten verantwoorden](finance-manage-cost-accounting.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
