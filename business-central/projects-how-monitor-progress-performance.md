---
title: Projectvoortgang en prestaties bewaken
description: Beschrijft hoe u een WIP-methode (Work in Progress) kunt creëren en WIP kunt berekenen om de financiële waarde van lopende projecten te schatten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/19/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# Projectvoortgang en prestaties bewaken

Met de functie Onderhanden werk (OHW) kunt u de financiële waarde van lopende projecten in het grootboek schatten.

Naarmate een project vordert, worden materialen en resources verbruikt en treden kosten op die naar het project moeten worden geboekt. In veel gevallen kunt u kosten voor een project boeken voordat u factureert. Maar als u alleen de kosten boekt, is uw financiële overzicht onjuist. Om de werkelijke waarde van het project bij te houden, berekent u OHW en boekt u deze in het grootboek. De volgende WIP-methoden zijn direct beschikbaar:

* Kostenwaarde
* Verkoopwaarde
* Herkenbare kosten
* Percentage van voltooiing
* Voltooid contract

U kunt ook een WIP-methode maken die voldoet aan de behoeften van uw organisatie en deze instellen als standaard.  

Zie voor meer informatie [OHW-methoden](projects-understanding-wip.md).

Als u het resultaat met een andere methode wilt bekijken, wijzigt u de methode en berekent u de WIP opnieuw. Er is geen limiet aan het aantal keren dat u WIP kunt berekenen. De waarde wordt niet automatisch naar grootboek gepost. Nadat u de WIP hebt berekend met de methode van uw voorkeur, kunt u een bericht plaatsen in de grootboek.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, voer  **project WIP Methods** in en kies vervolgens de gerelateerde koppelen.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sluit de pagina.   
4. Om van deze nieuwe methode de standaard te maken, kiest u het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, ga naar  **projectinstellingen** en kies de gerelateerde koppelen.  
5. Kies in het veld **Standaard OHW-methode** de methode uit de lijst.

## Een OHW-methode voor een project definiëren

Wanneer u een nieuw project maakt, moet u opgeven welke OHW-methode voor het project van toepassing is. In sommige gevallen is de OHW-methode voor een project al als standaard ingesteld.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voert u **Projecten** in en kiest u vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**. Zie voor meer informatie [Projecten maken](projects-how-create-jobs.md).  
3. Selecteer op de pagina  **project kaart**  in het veld  **WIP-methode** op het sneltabblad  **Boeking** een WIP-methode uit de lijst. Als er een standaardmethode is gedefinieerd, kunt u indien nodig een andere optie selecteren.  

### Een OHW-methode voor een project definiëren

U kunt een WIP-methode voor een project taak definiëren, projecttaken uitsluiten van de WIP-berekening of taken groeperen die samen moeten worden berekend.

Als u OHW voor elke projecttaak afzonderlijk wilt berekenen, biedt OHW-boeking gedefinieerde dimensies voor de specifieke taken.

Met het **OHW-totaal** worden projecttaken opgegeven die u wilt groeperen wanneer onderhanden werk (OHW) en verantwoording worden berekend. In elke groep taken moet er een taak zijn die aan twee voorwaarden voldoet:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* **WIP-Totaal** is ingesteld op **Totaal**. Als er geen projecttaken zijn waarvoor  **WIP-Totaal** is ingesteld op Totaal, wordt Totaal automatisch ingesteld op de laatste projectregel taak wanneer WIP voor de eerste keer wordt berekend.
* Het nummer in het veld  **project taak No.** is het laatste nummer in de groep of het bereik van projecttaken.

De volgende tabel beschrijft de opties:

| Veld | Beschrijving |
|--|--|
| **\<blank\>** | Leeg laten als de projecttaak deel uitmaakt van een groep taken. |
| **Totaal** | Definieert de reeks of groep taken die zijn opgenomen in de berekening van OHW en verantwoording. Binnen de groep wordt elke projecttaak waarvoor **Soort projecttaak** is ingesteld op **Boeken**, opgenomen in het OHW-totaal tenzij het veld **OHW-totaal** van de taak is ingesteld op **Uitgesloten**. |
| **Uitgesloten** | Geldt alleen voor een taak met **Soort projecttaak** **Boeken**, in welk geval de taak niet wordt opgenomen wanneer OHW en verantwoording worden berekend. |

In het volgende voorbeeld zijn projecttaken verdeeld in twee OHW-totaalgroepen, waarmee wordt gedemonstreerd hoe het veld **OHW-totaal** werkt:

|Projecttaaknr.|Beschrijving|Soort projecttaak|Veld **OHW-totaal**|  
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

Je merkt het volgende:

* Voor *1000* tot en met *1299* wordt WIP apart berekend voor deze groep projecttaken. Houd er echter rekening mee dat twee van de taken, 1010 en 1110, zijn uitgesloten van de WIP-berekening omdat hun projecttype taak  **Posting** is.
* Voor *1300* t/m *1399* wordt WIP apart berekend voor deze groep projecttaken.

## OHW berekenen

U kunt het WIP-bedrag dat u naar de balansrekeningen voor de rapportage aan het einde van de periode wilt boeken, bepalen met behulp van de batchtaak  **project Calculate WIP** .  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") Pictogram, voer  **project Calculate WIP** in en kies vervolgens de gerelateerde koppelen.  
2. Kies de actie **OHW berekenen**.
3. Vul op de pagina **OHW voor project berekenen** indien nodig de velden in.
4. Kies de knop **Ok**.  

> [!NOTE]  
> De batchtaak berekent alleen de WIP en plaatst deze niet in grootboek. Om WIP te boeken, voert u de batchtaak  **WIP naar G/L boeken** uit nadat u de WIP hebt berekend. Zie voor meer informatie de volgende procedure.

### Waarschuwingen bekijken

Als uw WIP-berekening resulteert in het bericht  *WIP is berekend met waarschuwingen*, wilt u de waarschuwingen mogelijk nog eens bekijken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Cockpit OHW project** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het project waarvoor u de waarschuwingen wilt bekijken. De schakelaar  **WIP-waarschuwingen** is ingeschakeld voor projecten met WIP-waarschuwingen.
3. Kies de actie **Waarschuwing weergeven** .

### WIP-items verwijderen

Als u verschillende WIP-methoden wilt proberen, krijgt u mogelijk de foutmelding  *Het project taak kan niet worden gewijzigd omdat het project gekoppelde WIP-projectvermeldingen heeft* . Om de WIP-methode te kunnen controleren, verwijdert u bestaande WIP-vermeldingen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Cockpit OHW project** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het project waarvan u de WIP-vermeldingen wilt verwijderen.
3. Kies de actie **WIP-items verwijderen** .

## OHW boeken

Wanneer u WIP berekent, kunt u deze boeken op de balansrekeningen voor de rapportage aan het einde van de periode. Gebruik de batchtaak  **projectboeking WIP naar G/L** .

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") Pictogram, voer  **project Post WIP to G/L** in en kies vervolgens de gerelateerde koppelen.  
2. Vul op de pagina **Project-OHW naar GB boeken** indien nodig de velden in.  
3. Kies de knop **Ok**.

## Projectvoltooiingsposten berekenen en boeken

Nadat u alle activiteiten voor een project hebt voltooid, inclusief het boeken van gebruik en facturering, moet u de status van het project bijwerken naar  **Voltooid**. Vervolgens moet u alle WIP die naar grootboek is gepost, ongedaan maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Projecten** in en kiest u vervolgens de gerelateerde koppeling.  
2. Selecteer een open project en kies vervolgens de actie **Bewerken**.
3. Selecteer op het sneltabblad  **Berichten** in het veld  **Status** de optie  **Voltooid**.
4. Volg de hulpstappen om de OHW te berekenen en te boeken, of volg stap 5 en 6 om dit handmatig te doen.  
5. Kies de actie **OHW berekenen**.
6. Vul op de pagina **OHW voor project berekenen** indien nodig de velden in.  

     Voor de project-WIP-vermeldingen die zijn gemaakt door het uitvoeren van de batchtaak, is het selectievakje  **project voltooid** aangevinkt om aan te geven dat het voltooiingsvermeldingen zijn.  
7. Kies de actie **Project-OHW naar GB boeken**.
8. Vul op de pagina **Project-OHW naar GB boeken** indien nodig de velden in.  

     Voor de project WIP grootboek-vermeldingen die zijn gemaakt door het uitvoeren van het batchproject, is het selectievakje  **project voltooid** aangevinkt om aan te geven dat het voltooiingsvermeldingen zijn.

## Projectposten weergeven

Alle posten met betrekking tot een project worden in projectjournalen opgeslagen en sequentieel genummerd, te beginnen met 1. Vanuit het projectjournaal hebt u een overzicht van alle projectposten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectjournalen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een relevant journaal en kies vervolgens de actie **Projectposten**.

Op de pagina  **projectboekposten**  kunt u de posten bekijken die aan een project zijn gekoppeld.  

## Zie ook

[Walkthrough - Berekenen van het werk in uitvoering voor een project](walkthrough-calculating-work-in-process-for-a-job.md)    
[Projecten beheren](projects-manage-projects.md)    
[Voorraadkosten beheren](finance-manage-inventory-costs.md)    
[Financiën](finance.md)    
[Inkoop](purchasing-manage-purchasing.md)    
[Verkoop](sales-manage-sales.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
