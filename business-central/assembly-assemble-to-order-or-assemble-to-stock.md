---
title: Op voorraad assembleren of Op order assembleren begrijpen
description: Meer informatie over het assembleren van artikelen voor verkooporders of om op voorraad te houden voor toekomstige verkopen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock" />Op voorraad assembleren of Op order assembleren begrijpen

Met [!INCLUDE [prod_short](includes/prod_short.md)] kunt u op de volgende manieren componenten aanleveren:

* Assembleren voor order  
* Assembleren voor voorraad  

## <a name="assemble-to-order" />Assembleren voor order

Gebruik het assembleren-op-order proces voor artikelen die u niet op voorraad wilt hebben. Bijvoorbeeld om de volgende redenen:

* U past de artikelen aan de eisen van de klant aan.
* U wilt de kosten van voorhanden voorraad minimaliseren.

De volgende lijst beschrijft enkele voordelen van het assembleren-op-order proces:  

* Componenten aanpassen wanneer u een verkooporder maakt.  
* Een overzicht met betrekking tot de beschikbaarheid van de component en de onderdelen ervan.  
* Assemblycomponenten direct reserveren om een onmiddellijk orderafhandeling te garanderen.  
* De winstgevendheid vaststellen van de aangepaste order door het berekenen van prijzen en kosten.  
* Integratie met het magazijn om de assemblage en verzending te vereenvoudigen.  
* Assembleren op order wanneer u een verkoopofferte of een verkoopraamcontract maakt.  
* Voorraadaantallen combineren met assembleren-op-order aantallen.  

In het op-order-assembleren proces assembleert u artikelen voor een verkooporder. Er is een één-op-één koppeling tussen de assemblageorder en de verkooporder.  

Wanneer u een assembleren-op-order artikel invoert op een verkooporderregel, wordt automatisch een assemblageorder gemaakt. De assemblageorder is gebaseerd op de verkoopregel en de regels ervan zijn gebaseerd op de assemblagestuklijst van het artikel. Het aantal materialen op de assemblagestuklijst wordt vermenigvuldigd met de orderhoeveelheid. De pagina **Op orderregels assembleren** toont details over de gekoppelde assemblageorderregels. De details kunnen u helpen bij het aanpassen van het assemblageartikel. De leveringsdatum is gebaseerd op de beschikbaarheid van materiaal. Ga voor meer informatie over het assembleren van artikelen voor verkooporders naar [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Hoewel dit geen onderdeel van het standaardproces is, kunt u voorraadaantallen en assembleren-op-order aantallen verkopen op dezelfde verkooporder. Zie voor meer informatie over het combineren van voorraad- en assembleren-op-order artikelen [Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Om aan te geven dat een artikel op order wordt geassembleerd kiest u in het veld **Assemblagebeleid** op de pagina **Artikel** voor het artikel **Op order assembleren**.  

## <a name="assemble-to-stock" />Assembleren voor voorraad

Gebruik het proces assembleren-op-voorraad voor artikelen die u assembleert en opslaat voor toekomstige verkoop. Op-voorraad-assembleren artikelen zijn standaardartikelen, zoals verpakte kits, die u niet aanpast. U kunt deze artikelen ook gebruiken als subassemblycomponenten. De artikelen worden gepickt en verwerkt als afzonderlijke artikelen en worden behandeld als voltooide productieartikelen. Ga voor meer informatie over componenten naar [Artikelen samenstellen](assembly-how-to-assemble-items.md).  

Wanneer u een assembleren-voor-voorraad artikel op een verkoopregel opgeeft, wordt het artikel hetzelfde behandeld als elk ander artikel dat uit de voorraad wordt verkocht. [!INCLUDE [prod_short](includes/prod_short.md)] controleert bijvoorbeeld alleen de beschikbaarheid van het geassembleerde artikel, en niet het materiaal ervan.  

> [!NOTE]  
> Hoewel het geen onderdeel is van het standaardproces, kunt u een artikel op order assembleren, zelfs als het artikel is ingesteld om op voorraad te worden geassembleerd. Zie voor meer informatie [Op-order-assembleren-artikelen en voorraadartikelen samen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  

Om aan te geven dat een artikel op voorraad wordt geassembleerd kiest u in het veld **Assemblagebeleid** op de pagina **Artikel** voor het artikel **Op voorraad assembleren**.  

## <a name="combination-scenarios" />Combinatiescenario's

Wanneer op order assembleren en voorraadaantallen worden gecombineerd op een verkooporder, moeten eerst de op order assembleren hoeveelheden worden verzonden.  

Als een assemblageorder is gekoppeld aan een verkooporderregel, wordt de waarde in het veld **Op order te assembleren aantal** op de verkooporderregel gekopieerd naar het veld **Te assembleren aantal**, via het veld **Aantal** in de assemblageorderkoptekst. Zie voor meer informatie [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)  

De waarde in het veld **Te assembleren aantal** is hetzelfde als de waarde in het veld **Te verzenden aantal**. Deze relatie beheert hoe u gedeeltelijke en volledige op-order-assembleren-hoeveelheden verzendt:

* Wanneer het volledige aantal op de verkooporderregel op order wordt geassembleerd
* In combinatiescenario's waarbij een deel van het aantal op order wordt geassembleerd en een deel vanuit voorraad wordt verzonden.

Het combinatiescenario biedt flexibiliteit voor deelzendingen. U kunt het veld **Te assembleren aantal** gebruiken om de hoeveelheid op te geven die gedeeltelijk uit voorraad moet worden verzonden en door op order te assembleren.  

Als het volledige aantal op de verkoopregel op order moet worden geassembleerd en verzonden, wordt de waarde in het veld **Te verzenden aantal** gekopieerd naar het veld **Te assembleren aantal** in de gekoppelde assemblageorder wanneer u het te verzenden aantal wijzigt. Deze update zorgt ervoor dat het te verzenden aantal volledig wordt geleverd door het assembleren-voor-order aantal.  

Echter, in combinatiescenario's wordt de hele waarde in **Te verzenden aantal** niet gekopieerd naar het veld **Te assembleren aantal** in de assemblageorderkop. In plaats daarvan wordt een standaardwaarde ingevoegd in het veld **Te assembleren aantal**. De waarde wordt berekend vanuit het veld **Te verzenden aantal** om ervoor te zorgen dat de assembleren-op-order hoeveelheden als eerste worden verzonden.

Als u wilt afwijken van deze standaardprocedure omdat u bijvoorbeeld alleen een groter of een kleiner aantal dan het aantal in het veld **Te verzenden aantal** wilt assembleren, kunt u het veld **Te assembleren aantal** wijzigen, maar alleen binnen vooraf gedefinieerde regels, zoals hieronder beschreven.  

Een voorbeeld van waarom u het assemblage-aantal mogelijk wilt wijzigen, is dat u een gedeeltelijke verzending van voorraadaantallen wilt boeken voordat u de assemblyuitvoer verzendt.  

In de volgende tabellen worden de regels uitgelegd voor het definiëren van de minimum- en maximumwaarden die u handmatig in het veld **Te assembleren aantal** kunt invoeren wanneer u in een combinatiescenario wilt afwijken van de standaardwaarde. In de tabel wordt een combinatiescenario weergegeven waarbij het veld **Te verzenden aantal** op de gekoppelde verkooporderregel wordt gewijzigd van 7 in 4, waardoor **Te assembleren aantal** wordt ingesteld op de standaardwaarde 4.  

**Verkooporderregel**

|                | **Aantal** | **Te verzenden aantal** | **Aant. op order assembleren** | **Verzonden aantal** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Initiële waarde**| 10          | 7                | 7                             | 0                    |
|**Wijziging**      |              | 4                |                               |                      |

**Assemblageorderkop**

|                | **Aantal** | **Te verzenden aantal** | **Op order te assembleren aantal** | **Verzonden aantal** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Initiële waarde**| 7           | 7                | 0                             | 7                    |
|**Wijziging**      |              | 4 (standaard ingevoegd)|                         |                      |

Gebaseerd op dit voorbeeld kunt u het veld **Te assembleren aantal** als volgt wijzigen:  

* Het minimumaantal dat u kunt invoeren is 1. U moet ten minste één eenheid assembleren om de vier eenheden te kunnen verkopen, aangenomen dat de overige drie eenheden in voorraad beschikbaar zijn.  
* Het maximumaantal dat u kunt invoeren is 4. Deze limiet zorgt ervoor dat u niet meer van het artikel assembleert dan u nodig hebt voor de verkoop.  

## <a name="see-related-microsoft-trainingtrainingpathsassemble-items-dynamics--business-central" />Zie gerelateerde [Microsoft-training](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
