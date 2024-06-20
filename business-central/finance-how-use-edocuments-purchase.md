---
title: E-documenten gebruiken in het aankoopproces
description: Leer hoe u de e-documentfunctionaliteit kunt gebruiken die gerelateerd is aan inkoopfacturen en orders.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# E-documenten gebruiken in het aankoopproces

U kunt geconfigureerde elektronische documenten (e-documenten) gebruiken met de inkoopdocumenten.

De volgende inkoopdocumenten kunnen worden gebruikt met e-documenten:  

- Inkoopfacturen
- Inkooporders (uit versie 24.0)
- Inkoopcreditnota's
- Dagboeken

> [!NOTE]
> Vanaf [!INCLUDE[prod_short](includes/prod_short.md)] versie 24.0 is het mogelijk om **Inkooporders** te koppelen aan de ontvangen **E-documenten**.  

## E-documenten bij inkopen

De ontvangst van inkoop-e-documenten in Dynamics 365 Business Central kan als batchverwerking of handmatig worden uitgevoerd.  

### Leveranciers instellen om met verschillende inkoopdocumenten te werken  

Volg deze stappen om leveranciers te configureren zodat ze goed kunnen werken met inkomende elektronische facturen: 

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en selecteer vervolgens de gerelateerde koppeling. 
2. Kies de leverancier die u wilt configureren.   
3. Zoek op het sneltabblad **Ontvangen** het veld **E-document ontvangen om** om het standaardinkoopdocument op te geven dat moet worden gegenereerd van het ontvangen e-document. 

   > [!NOTE]
   > In het veld **E-document ontvangen om** kunnen gebruikers een **Inkoopfactuur** of **Inkooporder** selecteren op basis van wat ze graag zouden willen maken op basis van de ontvangen e-factuur. Deze selectie heeft geen invloed op het maken van corrigerende documenten; in beide scenario's genereert het systeem een **Creditnota**.  

   > [!NOTE]
   > Als de gebruiker de optie **Inkooporder** in het veld **E-document ontvangen om** kiest, probeert het systeem update een van de bestaande inkooporders uit te voeren, maar als de inkooporder voor een leverancier in het ontvangen **e-document** niet bestaat, zal [!INCLUDE[prod_short](includes/prod_short.md)] een nieuwe **Inkooporder** maken, waarbij dezelfde aanpak wordt gebruikt als voor het maken van de nieuwe **Inkoopfacturen** die later op deze pagina worden uitgelegd.  

4. Kies een van de opties die u voor de geselecteerde leverancier wilt gebruiken. 
5. De pagina sluiten.   

### Werken met inkoopfacturen  

#### De batchverwerking uitvoeren  

> [!NOTE]
> Deze batchverwerking is bedoeld voor het geautomatiseerd verzamelen van uw inkomende facturen. Het kan alleen werken in een land/regio waar de functionaliteit bestaat.  

Telkens wanneer een **taakwachtrij** wordt geselecteerd om te worden uitgevoerd en de externe service binnenkomende facturen heeft die door uw leverancier zijn verzonden, verzamelt en importeert het systeem deze facturen. Volg deze stappen om het proces te voltooien: 

1. Nadat de batchverwerking is uitgevoerd, worden de nieuw geïmporteerde facturen weergegeven op de pagina **E-documenten**, samen met hun basisdetailinformatie. 
2. Om meer details te bekijken opent u een specifiek e-document.   
3. Als er geen fouten of problemen in het e-document voorkomen, wijst het veld **Record** het documentnummer van de inkoopfactuur toe als het is geconfigureerd op de pagina **Leverancierskaart** (die het systeem automatisch heeft gemaakt). Selecteer de koppeling om het document te openen.
 
   > [!NOTE]
   > Dit door het systeem gemaakte document is niet het geboekte document. 

4. Om rechtstreeks naar het inkoopdocument te gaan selecteert u het veld **Record**. Nadat u de pagina **Inkoopfactuur** heeft geopend, controleert u het document. Als alles correct is, boekt u het document.  
5. Wanneer u het inkoopdocument boekt, wordt het veld **Record** van het **E-document** bijgewerkt van **Factuur** naar **Inkoopfactuur** en is het nummer van het geboekte inkoopdocument beschikbaar. U kunt het nummer selecteren om de geboekte inkoopfactuur te openen die u wilt annuleren. 

Details over logboeken zijn hetzelfde als in het verkoopproces voor e-documenten.  

Omdat fouten in het verkoopproces meestal verband houden met de beschikbaarheid van de dienst, kan het binnenkomende document meerdere redenen bevatten. De meest voorkomende reden voor een fout is dat het systeem de regels op het e-document dat u van uw leverancier heeft ontvangen, niet kan herkennen. Daarom kunnen er geen regels in uw inkoopfactuur worden ingevoerd. 

Er zijn twee veelvoorkomende fouten:  

- Als u deze specifieke regel van uw leveranciersfactuur wilt gebruiken die rechtstreeks naar de grootboekrekening is geboekt, moet u de waarde **Toewijzing tekst** correct hebben geconfigureerd. Als u deze fout wilt omzeilen als u grootboekrekeningen wilt gebruiken, selecteert u **Tekst afstemmen op rekening** om een specifieke toewijzing van de waarde **Toewijzing tekst** te maken met de waarde **Debetrekeningnr.** die u wilt gebruiken. 
- Als u de voorraad wilt traceren en regels van uw leveranciersfactuur wilt gebruiken om de artikelen op uw documentregels in te vullen, moet u de waarde **Nr. van artikelreferentie** correct hebben geconfigureerd. Om deze fout te omzeilen wijst u het externe artikel toe aan uw artikelnummers met behulp van de artikelreferentielijst. Zie voor meer informatie [Artikelverwijzingen gebruiken](inventory-how-use-item-cross-refs.md). 

Nadat u de fouten en waarschuwingen heeft verholpen, kunt u handmatig opgeven wanneer het systeem een inkoopfactuur moet maken op basis van uw instellingen door **Document maken** te selecteren.   

#### Handmatig facturen importeren  

Om externe e-documenten handmatig te importeren volgt u deze stappen:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-documentservice** in en selecteer vervolgens de gerelateerde koppeling 
2. Selecteer op de pagina **E-documentservice** de actieve service.   
3. Selecteer **Ontvangen** en upload het e-documentbestand dat u van de leverancier heeft ontvangen. 
4. Als er een foutmelding optreedt, opent u het e-document om de problemen op te lossen. 
5. Wanneer u klaar bent met het oplossen van de problemen, selecteert u in de groep **Handmatig importeren** de optie **Document maken**.  
6. Nadat het document is gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)], verandert het gebruik van een batchtaak niets aan de manier waarop u het bekijkt. 

### E-documenten met aan inkooporders  

#### Inkooporders koppelen aan de ontvangen e-documenten

Als uw **leverancier** het veld **E-document ontvangen om** heeft geconfigureerd om te werken met **Inkooporders**, doet [!INCLUDE[prod_short](includes/prod_short.md)] het volgende zodra het e-document wordt gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] (handmatig of vanaf een extern eindpunt):  

1. Als de **Inkooporder** voor deze specifieke leverancier bestaat en er een inkoopordernummer in het bestand van het ontvangen **E-document** staat, koppelt [!INCLUDE[prod_short](includes/prod_short.md)] dit **E-document** automatisch aan de genoemde **Inkooporder**, de **documentstatus** van dit **E-document** wordt **In uitvoering** en de **E-documentstatus** op de subpagina **Servicestatus** wordt **Order gekoppeld**. Deze koppeling zal zichtbaar zijn in het veld **Document** veld van dit specifieke **e-document**. Als u de automatisch gekoppelde **Inkooporder** moet wijzigen, kunt u dit doen met behulp van de actie **Koppeling van inkooporder bijwerken** en kiest u handmatig een van de bestaande inkooporders voor deze leverancier. U kunt dit alleen doen voordat u de regels tussen **E-document** en **Inkooporder** afstemt.  

2. Als de **inkooporder** voor deze specifieke leverancier bestaat, maar er geen inkoopordernummer in het ontvangen **E-document**bestand staat, biedt [!INCLUDE[prod_short](includes/prod_short.md)] de mogelijkheid om een van de bestaande inkooporders te kiezen als u dit document handmatig heeft geüpload. Dit opent de lijst **Inkooporders** met orders alleen voor de leverancier van wie u het **E-document** hebt ontvangen. U moet de gewenste **inkooporder** selecteren en vervolgens **OK** selecteren. Als u er niet in bent geslaagd de juiste **inkooporder** te selecteren of het **e-document** automatisch van een extern eindpunt hebt verkregen met behulp van de **taakwachtrij**, wordt een nieuw **e-document** niet aan enig inkoopdocument gekoppeld. De **documentstatus** toont **Fout** en de **Status van e-document** op de subpagina **Servicestatus** toont ook **Verwerkingsfout met geïmporteerd document**. Als u de koppeling met de **Inkooporder** wilt voltooien, kiest u de actie **Koppeling van inkooporder bijwerken** en kiest u vervolgens een van de bestaande inkooporders voor deze leverancier. 

3. Als de **inkooporder** voor deze specifieke leverancier niet bestaat wanneer een nieuw **e-document** wordt gemaakt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] een nieuwe **inkooporder**, waarbij hetzelfde maakmodel wordt gebruikt dat al bestaat voor nieuwe **Inkoopfacturen**. De **documentstatus** van dit **E-document** zal **Verwerkt** zijn en de **E-documentstatus** op de subpagina **Servicestatus** wordt **Geïmporteerd document gemaakt**. Deze koppeling zal zichtbaar zijn in het veld **Document** veld van dit specifieke **e-document**.   

#### Regels uit ontvangen e-document afstemmen met inkooporder  

U kunt uw ontvangen elektronische documenten afstemmen met regels van inkooporders van twee verschillende plaatsen: vanaf de pagina **E-document** of vanaf de pagina **Inkooporder**. De eenvoudigste manier om de reeds gekoppelde **Inkooporders** te vinden is het gebruik van de tegel **Gekoppelde inkooporders** als onderdeel van **E-documentactiviteiten**. Alle niet-gekoppelde documenten zijn te vinden via de tegel **Wachtende e-inkoopfacturen**, waar u een lijst hebt met **E-documenten** die u moet beoordelen.  

> [!NOTE]
> De **E-documentactiviteiten** met deze twee tegels vindt u in de volgende **Rolcentra**: Evaluatie van bedrijfsmanager, Bedrijfsmanager, Accountant, Voorraadbeheerder en Verzending en ontvangst.  

> [!NOTE]
> Als het btw-percentage verschilt tussen het binnenkomende document en het btw-percentage van het bedrijf, kunnen overeenkomende documenten niet worden gebruikt in een omgeving met meerdere landen/regio's.  

##### Overeenkomende regels uit inkooporder  

U kunt de regels uit de lijst **Inkooporders** of uit een van de geopende **Inkooporders** afstemmen. Voer de volgende stappen uit om hiermee te beginnen:  

1. Selecteer de tegel **Gekoppelde inkooporders** in uw rolcentrum als die er zijn. 
2. Kies een van de twee opties voor afstemming: 

   - Als u de regels uit de lijst **Inkooporders** wilt afstemmen, selecteert u de **Inkooporder**-regel die u wilt afstemmen en kiest u de actie **E-documentregels toewijzen**.  
   - Als u eerst de **Inkooporder** wilt openen, opent u het document en kiest u vervolgens de actie **E-documentregels toewijzen**. 

3. Omdat beide opties hetzelfde proces hebben, opent u de pagina **Afstemming inkooporders** met de volgende inhoud: 

    1. In de koptekst vindt u de volgende informatie, die u kan helpen de regels gemakkelijker af te stemmen: 

       |Veldnaam |Beschrijving |
       |--------|-----------------|
       |Leveranciersnaam |Hiermee wordt de naam van de leverancier van het elektronische document opgegeven. |
       |E-documentnr. |Hiermee wordt het gekoppelde elektronische documentnummer opgegeven. |
       |Datum e-document |Hiermee wordt de gekoppelde boekingsdatum van het elektronische document opgegeven.  |
       |Bedrag van e-document |Hiermee wordt gekoppelde het totaalbedrag van het e-document inclusief btw opgegeven. |

    2. Op de regels vindt u de regels die zijn geïmporteerd uit het bestand van het **E-document** aan de linkerkant en de regels uit de bestaande **Inkooporder** aan de rechterkant.  
    3. Alle regels aan beide zijden hebben artikelnummers en beschrijvingen, samen met de **Directe kostprijs** en het **Regelkorting %**.  
    4. Aan de kant **Geïmporteerde regels** kunt u het veld **Hoeveelheid** ook vinden als een totale hoeveelheid uit de e-factuur en het veld **Afgestemde hoeveelheid** geeft de hoeveelheid aan die al is afgestemd met de inkooporderregels. 
    5. Aan de kant **Inkooporderregels** vindt u ook de **Beschikbare hoeveelheid** als de hoeveelheid die met deze regel kan worden afgestemd (ontvangen, maar niet gefactureerde hoeveelheid) en **Te factureren aantal**, met vermelding van het aantal dat al aan deze regel is gekoppeld. 
    6. Als u regels wilt afstemmen, selecteert u de regels aan beide zijden die u wilt afstemmen en kiest u de actie **Handmatig afstemmen**. De afgestemde regels worden gemarkeerd met de groene kleur. 
    7. Het is mogelijk om een op een af te stemmen, maar het is ook mogelijk om veel met één of één met veel af te stemmen, door meer regels aan de ene of de andere kant te selecteren voordat u de actie **Handmatig afstemmen** kiest. 
    8. U kunt ook de actie **Automatisch afstemmen** kiezen om automatisch alle regels met hetzelfde **Type**, **Nr.**, **Eenheidsprijs**, **Korting** en **Maateenheid** af te stemmen. 
    9. Als u een fout maakt, kunt u de actie **Afstemming verwijderen** kiezen om de afgestemde regels aan de inkooporderzijde te verwijderen, of de actie **Afstemmen opnieuw instellen** kiezen om alles wat is afgestemd opnieuw in te stellen. 
    10. Als uw **E-document** veel regels bevat, kunt u tijdens het afstemmingsproces de actie **Regels in behandeling weergeven** kiezen om alle e-documentregels te verwijderen als ze al volledig op elkaar zijn afgestemd. Als u alle regels wilt zien, kunt u altijd de actie **Alle regels weergeven** kiezen. 

4. Zodra u klaar bent met het afstemmen, moet u de actie **Toepassen op inkooporder** kiezen.   
5. Nadat u de afstemming hebt toegepast op de **inkooporder**, werkt [!INCLUDE[prod_short](includes/prod_short.md)] de volgende velden bij:

    1. **Leveranciersfactuurnr.** en **Documentdatum** in de documentkop worden bijgewerkt met waarden uit het elektronische document dat u hebt ontvangen en gekoppeld. 
    2. **Te factureren aantal** op regels wordt bijgewerkt met de waarden uit de kolom **Te factureren aantal** van de pagina **Afstemming inkooporders** op basis van de afstemming die u hebt uitgevoerd. 
    3. Nu kunt u het document boeken door de actie **Boeken** te kiezen.  
    4. Zodra u het document hebt geboekt, verandert het veld **Document** op de pagina **E-document** de waarde en wordt het gerelateerd aan de **Geboekte inkoopfactuur**. 
    5. De pagina sluiten.  

> [!IMPORTANT]
> Standaard kunt u alleen de regels afstemmen die in beide documenten hetzelfde totaalbedrag hebben. Dat betekent dat **Directe kostprijs** samen met het toegepaste **Korting %** van de regel hetzelfde moeten zijn, omdat u in één document een bedrag zonder korting kunt hebben en in een ander document een bedrag met korting.  

Als u enige tolerantie wilt toevoegen en rekening wilt houden met het verschil tussen regels in **E-factuur** en **Inkooporder**, volgt u deze stappen:   

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopinstellingen** in en selecteer vervolgens de gerelateerde koppeling.  
2. U wilt tolerantie toestaan in het veld **Percentage overeenkomstverschil van e-document**, waarbij u het maximaal toegestane percentage van kostenverschil opgeeft bij het afstemmen van een inkomende **E-document**-regel met de **Inkooporder**-regel. 
3. Deze instelling is van toepassing op alle overeenkomende regels, maar houdt opnieuw rekening met de tolerantie voor het totale bedrag, zoals voor **Directe kostprijs** samen met het toegepaste **Regelkorting %**.  
4. De pagina sluiten.   

##### Regels uit een e-document afstemmen  

U kunt de regels op de pagina **E-document** afstemmen. Voer de volgende stappen uit om hiermee te beginnen:  

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-documenten** in en selecteer vervolgens de gerelateerde koppeling 
2. Selecteer het **E-document** dat u wilt afstemmen.   
3. Kies de actie **Inkooporder afstemmen** om de pagina **Afstemming inkooporders** te openen.  
4. Herhaal dezelfde stappen die u gebruikte toen u begon met het afstemmen vanuit inkooporders.

### Copilot Hulp bij afstemming van e-document  

> [!NOTE]
> Momenteel bevindt de copilot **Hulp bij afstemming van e-document** zich in de previewfase Klaar voor productie en is deze wereldwijd beschikbaar, behalve in Canada. Het werkt alleen in het Engels. 

> [!NOTE]
> Copilot is de door AI aangedreven assistent die mensen in uw organisatie helpt hun creativiteit aan te wenden en vervelende taken te automatiseren. De copilot **Hulp bij afstemming van e-document** helpt gebruikers hun ontvangen elektronische facturen eenvoudig af te stemmen met bestaande inkooporderorderregels, waarbij het LLM-model wordt gebruikt voor het afstemmen van regels tussen twee verschillende documenten. 

#### De copilot activeren  

Als u de copilot **Hulp bij afstemming van e-document** niet hebt geactiveerd, moet u dit handmatig doen. Als u de copilot **Hulp bij afstemming van e-document** wilt inschakelen, volgt u deze stappen: 

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Copilot en AI-mogelijkheden** in en selecteer vervolgens de gerelateerde koppeling. 
2. Kies in de lijst met mogelijkheden **Hulp bij afstemming van e-document** en wijzig de status in **Actief**.  

Zodra de copilot is geactiveerd, kunt u deze gaan gebruiken.

#### De copilot Hulp bij afstemming van e-document gebruiken 

Als de copilot is geactiveerd, krijgen bestaande acties **E-documentregels toewijzen** in ingekochte orders en **Inkooporder afstemmen** op de pagina **E-document** verschillende pictogrammen, die de AI-mogelijkheid symboliseren. U kunt deze acties (hetzelfde als in de vorige voorbeelden uit de lijst met inkooporders) uitvoeren vanuit een van de **Inkooporders** of vanuit **E-document**. Alle stappen voor uitvoering zijn hetzelfde, maar wanneer u deze actie uitvoert, zal het resultaat anders zijn en moet u deze stappen volgen:  

1. Kies de actie **E-documentregels toewijzen** of **Inkooporder afstemmen** voor reeds gekoppelde documenten.  
2. De prompt **Afstemmingsorderregels van e-document met Copilot** werkt en de pagina **Afstemming inkooporders** bevindt zich op de achtergrond. Dat betekent dat hetzelfde proces plaatsvindt, maar dan met de automatische ondersteuning van **Copilot**, die het afstemmingsproces uitvoert in plaats van u. 
3. Na een paar seconden stelt **Afstemmingsorderregels van e-document met Copilot** regels voor afstemming voor met enkele aanvullende details: 

    1. In de promptkop vindt u de volgende informatie: 

       |Veldnaam |Beschrijving |
       |--------|-----------------|
       |Automatisch afgestemd | Hiermee wordt het aantal automatisch voorgestelde overeenkomsten opgegeven. Dit is gebaseerd op een tekenreeksvergelijking en als de beschrijvingen 80% of meer overlappen, zal het systeem deze beschrijvingen automatisch afstemmen zonder GPT-mogelijkheden te gebruiken. |
       |Copilot afgestemd | Specificeert het aantal door de copilot voorgestelde overeenkomsten met behulp van zowel tekenreeks- als semantische vergelijking. |
       |E-documentnr. | Hiermee wordt het gekoppelde e-documentnummer opgegeven. |
       |Totaalbedrag van factuur exclusief btw | Hiermee wordt het totale factuurbedrag exclusief btw opgegeven. |
       |Afgestemd totaalbedrag inclusief btw | Hiermee wordt het afgestemde bedrag inclusief btw opgegeven. |
    
    2. Als alle regels overeenkomen, ziet u de groene tekst in de rechterbovenhoek: **Alle regels (100%) zijn afgestemd. Controleer afstemmingsvoorstellen.**.  
    3. Op de **Afgestemd voorstel**-regels vindt u de volgende informatie:  

       |Veldnaam |Beschrijving |
       |--------|-----------------|
       |E-documentregelnr. | Specificeert het regelnummer van het e-document (afkomstig uit het originele e-documentbestand). |
       |Omschrijving van e-documentregel | Specificeert de regelbeschrijving van het e-document (afkomstig uit het originele e-documentbestand). |
       |Afgestemde hoeveelheid | Hiermee wordt de hoeveelheid opgegeven die wordt vereffend met de inkooporderregel. |
       |Voorstel | Specificeert de door AI voorgestelde actie, en deze voorgestelde acties hebben betrekking op het afstemmen van de inkooporderregels. |

    4. Alle volledig voorgestelde en afgestemde lijnen zijn gemarkeerd met een groene kleur. Als er een probleem is, bijvoorbeeld een andere prijs, maar binnen de toegestane prijsklasse, wordt deze regel geel gemarkeerd. Als er enige gelijkenis is tussen de beschrijvingsvelden, maar het prijsverschil groter is dan toegestaan, wordt deze regel rood gemarkeerd. 
    5. Als u niet tevreden bent met sommige suggesties, kunt u deze verwijderen met behulp van de actie **Regel verwijderen**.  
    6. Als u voorstelafstemmingen wilt zien, kunt u de koppeling in de kolom **Voorstel** selecteren om de pagina **Afstemmingsdetails e-document** te openen. 
    7. Op de pagina **Afstemmingsdetails e-document** kunt u details van het **E-document** en de **Inkooporder** vergelijken om zeker te zijn van de voorgestelde afstemming voordat u deze bevestigt. 
    8. Sluit na het controleren de pagina.   

4. Als u niet tevreden bent met de meeste suggesties, of als u de functie **Afstemmingsorderregels van e-document met Copilot** niet wilt gebruiken, selecteert u **Verwijderen** en u kunt doorgaan met het handmatig afstemmen, zoals eerder uitgelegd.  
5. Als u suggesties wilt bewaren, kiest u de knop **Behouden**. Het systeem slaat alle suggesties van **Copilot** op.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] sluit de Copilot-prompt en regels op de pagina **Afstemming inkooporders** worden groen gemarkeerd, omdat ze al zijn afgestemd. 
7. Nu kunt u doorgaan met handmatig afstemmen; dat betekent dat u afstemmingen kunt verwijderen, handmatig kunt afstemmen of de afstemming opnieuw kunt instellen. Als u geen wijzigingen wilt aanbrengen, kiest u gewoon de actie **Toepassen op inkooporder** en werkt u verder met de **Inkooporder**. 

> [!NOTE]
> U kunt opnieuw de actie **Afstemmen met Copilot** op de pagina **Afstemming inkooporders** kiezen, maar in dit geval wordt u gevraagd of u de bestaande afstemmingen wilt overschrijven, omdat alle regels al zijn afgestemd.  

> [!NOTE]
> Prijs-/kostenanalyse en de controle van de beschikbare hoeveelheid maken deel uit van de voorverwerkingsactiviteit.   

## Overzicht van e-documentstatussen

Om een beter overzicht te krijgen van alle e-documenten in het bedrijf, kunt u het rolcentrum **Accountant** selecteren waar de statussen van e-documenten voorkomen. Daar vindt u e-documentactiviteiten met de volgende statussen:

- **Inkomende e-documenten:**

    - Verwerkt
    - Wordt uitgevoerd
    - Fout


## Zie ook

[E-documenten instellen](finance-how-setup-edocuments.md)    
[E-document gebruiken in het verkoopproces](finance-how-use-edocuments.md)   
[Functionaliteit van e-documenten uitbreiden](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Financieel beheer](finance.md)    
[Verkopen factureren](sales-how-invoice-sales.md)    
[Aankopen registreren met inkoopfacturen en orders](purchasing-how-record-purchases.md)    
[Werken met Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

