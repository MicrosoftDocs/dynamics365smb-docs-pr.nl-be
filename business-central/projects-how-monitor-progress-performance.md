---
title: Voortgang en prestaties van projecten bewaken
description: Beschrijft hoe u een OHW-methode (onderhanden werk) kunt maken en OHW kunt berekenen om de financiële waarde van projecten in te schatten terwijl ze bezig zijn.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.date: 08/04/2022
ms.author: edupont
---
# Voortgang en prestaties van projecten bewaken

Met de functie Onderhanden werk (OHW) kunt u de financiële waarde van lopende projecten in het grootboek schatten.

Naarmate een project vordert, worden materialen en resources verbruikt en treden kosten op die naar het project moeten worden geboekt. In veel gevallen kunt u kosten voor een project boeken voordat u factureert. Maar als alleen kosten zijn geboekt, klopt uw financiële afschrift niet. Om de werkelijke waarde van de taak bij te houden, berekent u OHW en boekt u deze in het grootboek. Zie voor meer informatie [OHW-methoden](projects-understanding-wip.md).

U kunt het OHW-bedrag berekenen op basis van de volgende zaken:

* Kostenwaarde
* Verkoopwaarde
* Kostprijs van omzet
* Percentage van voltooiing
* Voltooid contract

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## Een OHW-methode voor een project maken

Maak een OHW-methode voor een project taken die voldoet aan de behoeften van uw organisatie en stel deze in als standaard.  

> [!NOTE]
> Nadat u uw nieuwe methode hebt gebruikt om OHW-posten te maken, kunt u de methode niet meer verwijderen of wijzigen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **OHW-methoden taak** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sluit de pagina.   
4. Om van deze nieuwe methode de standaard te maken, kiest u het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **projectinstellingen** in en kies vervolgens de gerelateerde koppeling.  
5. Kies in het veld **Standaard OHW-methode** de methode uit de lijst.

## Een OHW-methode voor een project definiëren

Wanneer u een nieuw project maakt, moet u opgeven welke OHW-methode voor het project van toepassing is. In sommige gevallen is de OHW-methode voor een project al als standaard ingesteld.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **projecten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**. Zie voor meer informatie [Projecten maken](projects-how-create-jobs.md).  
3. Selecteer op de pagina **Projectkaart** in het veld **OHW-methode** een OHW-methode uit de lijst. Als een standaardmethode is gedefinieerd, kunt u indien nodig een andere optie selecteren.  

### Een OHW-methode voor een project definiëren

U kunt een OHW-methode definiëren voor een projecttaak, bepaalde projecttaken uitsluiten van de OHW-berekening of taken groeperen die samen moeten worden berekend. 

Als u OHW voor elke projecttaak afzonderlijk wilt berekenen, biedt OHW-boeking gedefinieerde dimensies voor de specifieke taken.

Met het **OHW-totaal** worden projecttaken opgegeven die u wilt groeperen wanneer onderhanden werk (OHW) en verantwoording worden berekend. In elke groep taken moet er een taak zijn die aan twee voorwaarden voldoet:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Heeft een **OHW-totaal** ingesteld op *Totaal*. (Als er geen projecttaken zijn waarvoor **OHW-totaal** is ingesteld op *Totaal*, wordt *Totaal* automatisch ingesteld op de laatste projecttaakregel wanneer OHW voor de eerste keer wordt berekend.)

* Heeft een **Projecttaaknr.** dat de laatste is in de groep of reeks projecttaken.

De volgende tabel beschrijft de volgende drie opties:

| Veld | Omschrijving |
|--|--|
| **\<blank\>** | Leeg laten als de projecttaak deel uitmaakt van een groep taken. |
| **Totaal** | Definieert de reeks of groep taken die zijn opgenomen in de berekening van OHW en verantwoording. Binnen de groep wordt elke projecttaak waarvoor **Taaksoort project** is ingesteld op **Boeken**, opgenomen in het OHW-totaal tenzij het veld **OHW-totaal** van de taak is ingesteld op **Uitgesloten**. |
| **Uitgesloten** | Geldt alleen voor een taak met **Soort projecttaak** **Boeken**, in welk geval de taak niet wordt opgenomen wanneer OHW en verantwoording worden berekend. |

In het volgende voorbeeld zijn projecttaken verdeeld in twee OHW-totaalgroepen, waarmee wordt gedemonstreerd hoe het veld **OHW-totaal** werkt:

|Projecttaaknr.|Omschrijving|Soort projecttaak|Veld **OHW-totaal**|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Voorbereiding|Begintotaal|\<blank\>|
|1010|.    Schoonmaakkosten|Boeking|**Uitgesloten**|
|1099|Totale voorbereiding|Eindtotaal|\<blank\>|
|1100|Bekleding|Begintotaal|\<blank\>|
|1110|.    Verlijmen|Boeking|**Uitgesloten**|
|1120|.    Tapijt leggen|Boeking|\<blank\>|
|1199|Totale bekleding|Eindtotaal|\<blank\>|
|1200|Voltooien|Begintotaal|\<blank\>|
|1210|.    Tapijt stofzuigen|Boeking|\<blank\>|
|1299|Totale afwerking|Eindtotaal|**Totaal**|
|1300|Foutcorrectie|Begintotaal|\<blank\>|
|1310|.    Foutcorrectie|Boeking|\<blank\>|
|1399|Totale foutcorrectie|Eindtotaal|**Totaal**|

U zult merken:

* *1000* t/m *1299*: OHW wordt afzonderlijk berekend voor deze reeks projecttaken. Houd er echter rekening mee dat twee van de taken, 1010 en 1110, zijn uitgesloten van de OHW-berekening omdat het soort projecttaak ervan **Boeken** is.

* *1300* t/m *1399*: OHW wordt afzonderlijk berekend voor deze reeks projecttaken.

## OHW berekenen

U kunt het OHW-bedrag bepalen dat moet worden geboekt naar balansrekeningen voor eindrapportage van een periode. U gebruikt hiervoor de batchverwerking **OHW voor project berekenen**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voert u **ohw voor project berekenen** in en kiest u vervolgens de gerelateerde koppeling.  
2. Kies de actie **OHW berekenen**.
3. Vul op de pagina **OHW voor project berekenen** indien nodig de velden in.
4. Kies de knop **OK**.  

> [!NOTE]  
>   Met de batchverwerking wordt het OHW alleen berekend en niet naar het grootboek geboekt. Om het te boeken moet u de batchverwerking **OHW naar GB boeken** uitvoeren nadat u het OHW hebt berekend. Zie voor meer informatie de volgende procedure.

## OHW boeken

Wanneer u OHW hebt berekend, kunt u het boeken naar balansrekeningen voor de einddatumrapportage. Hiervoor gebruikt u de batchverwerking **Project-OHW naar GB boeken**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **project-ohw naar gb boeken** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op de pagina **Project-OHW naar GB boeken** indien nodig de velden in.  
3. Kies de knop **OK**.

## Projectvoltooiingsposten berekenen en boeken

Wanneer u alle activiteiten voor een project hebt uitgevoerd, waaronder gebruiksboekingen en -facturering, moet u het project bijwerken om de **Status** in te stellen op **Voltooid**. Vervolgens moet u eventueel OHW tegenboeken dat naar het grootboek is geboekt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een open project en kies vervolgens de actie **Bewerken**.
3. Selecteer in het veld **Status** de optie **Voltooid**.
4. Volg de hulpstappen om OHW te berekenen en te boeken. Of volg stap 5 en 6 om dit handmatig te doen.  
5. Kies de actie **OHW berekenen**.
6. Vul op de pagina **OHW voor project berekenen** indien nodig de velden in.  

     De OHW-posten voor het project die worden gemaakt door het uitvoeren van de batchverwerking, hebben nu een vinkje in het selectievak **Project voltooid** om aan te geven dat het voltooiingsposten zijn.  
7. Kies de actie **Project-OHW naar GB boeken**.
8. Vul op de pagina **Project-OHW naar GB boeken** indien nodig de velden in.  

     De OHW-grootboekposten voor het project die worden gemaakt door het uitvoeren van de batchverwerking hebben nu een vinkje in het selectievak **Project voltooid** om aan te geven dat het voltooide posten zijn.

## Projectposten bekijken

Alle posten met betrekking tot een project worden in projectjournalen opgeslagen en sequentieel genummerd, te beginnen met 1. Vanuit het projectjournaal hebt u een overzicht van alle projectposten.    

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **projectjournalen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een relevant journaal en kies vervolgens de actie **Projectposten**.

De pagina **Projectposten** wordt geopend, waarin u de posten die zijn gekoppeld aan een project, kunt bekijken.  

## Gerelateerde [Microsoft-training](/training/paths/calculate-post-job-wip/) zoeken

## Zie ook

[Procedure - Onderhanden werk voor een project berekenen](walkthrough-calculating-work-in-process-for-a-job.md)
[Projecten beheren](projects-manage-projects.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
