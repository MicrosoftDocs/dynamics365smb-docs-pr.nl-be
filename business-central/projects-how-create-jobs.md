---
title: Een projectkaart voor een project maken en taken opgeven
description: Voor een nieuw project maakt u een projectkaart met projecttaken en planningsregels om u te helpen voortgang en budgetten te beheren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Projecten maken

Wanneer u een nieuw project start, moet u een projectkaart maken met geïntegreerde projecttaken en projectplanningsregels, die uit twee lagen wordt gestructureerd.  

De eerste laag bestaat uit projecttaken. U moet ten minste één projecttaak per project maken omdat alle boekingen naar een projecttaak verwijzen. Als uw project ten minste één projecttaak bevat, kunt u projectplanningregels instellen en verbruik voor het project boeken.

De tweede laag bestaat uit projectplanningregels, waarin gedetailleerd het verbruik wordt aangegeven van resources, artikelen en diverse grootboekkosten.

Dankzij de laagstructuur kunt u het project in kleinere taken onderverdelen en dus specifieke details gebruiken voor budgettering, offertes en registratie. Daarnaast krijgt u inzicht in hoe een project verloopt. Zo kunt u bijvoorbeeld bijhouden of u aan aangewezen mijlpalen voldoet of op koers zit wat de budgetverwachtingen betreft.

> [!TIP]
> Kies de actie **Nieuw project** in het rolcentrum **Projectmanager** om een begeleide instelling te starten die u begeleidt bij de stappen voor het maken van een project met geïntegreerde taken en planningsregels. In de volgende procedure wordt beschreven hoe u handmatig de stappen uitvoert. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## Meerdere klanten factureren voor projecttaken

Soms wijkt de partij die een service ontvangt, af van de partij die de rekening betaalt. Soms moet u ook meerdere klanten factureren voor taken in het project. Gebruik op de pagina **Projectkaart** het veld **Factureringsmethode voor taken** om op te geven of u één klant factureert, of meerdere klanten.

Als de klant die de service ontvangt ook de factuur betaalt, kiest u in de velden **Factureren aan** en **Verzenden aan** **Standaard (klant)** en **Standaard (orderadres)**.

Als u meerdere klanten factureert, kunt u voor elke taak in het project de klant opgeven die de service ontvangt en de klant die u moet factureren. U kunt ook de volgende informatie verschaffen.

* Waar het werk zal gebeuren door te selecteren uit een lijst met verzendadressen voor de klant.
* Voeg informatie over externe referenties toe om de communicatie over het project te vereenvoudigen.
* Overschrijf de standaard financiële voorwaarden van het project.

## Eén klant factureren voor meerdere projecttaken

U kunt uw facturatieproces vereenvoudigen door voor meerdere projecten één factuur naar een klant te sturen. Voeg projectplanningsregels uit meerdere projecten in één keer toe aan een verkoopfactuur. Dit proces is vergelijkbaar met het maken van een verkoopfactuur op basis van een projectplanningsregel en het invoeren van een waarde in het veld **Toevoegen aan verkoopfactuurnr.** .

Dit is een overzicht van het proces.

1. Maak een nieuwe verkoopfactuur en vul het veld **Orderklantnr.** in. . Vul indien nodig ook de velden **Factuurklantnr.** en **Valutacode** in.
2. Selecteer op het sneltabblad **Regels** de actie **Projectplanningsregels ophalen**. De pagina **Projectplanningsregels ophalen** toont factureerbare projectplanningsregels van projecten voor de orderklant, de factuurklant en de factureringsvaluta waarbij het te factureren aantal groter is dan nul. 
3. Kies de regels waaraan u de factuur wilt toevoegen en kies **OK**.

Herhaal deze stappen als u nog een set projectplanningsregels wilt toevoegen. U kunt ook de factuur of de regels ervan verwijderen en opnieuw beginnen.

> [!NOTE]
> Er zijn een aantal beperkingen:
>
> * De actie **Projectplanningsregels ophalen** is niet beschikbaar voor verkooporders of verkoopoffertes.
> * U kunt niet filteren op de velden **Verzendcode** of **Contactnr.** .

## Een projectkaart maken

U maakt een projectkaart en maakt vervolgens projecttaakregels en projectplanningsregels hiervoor.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u het project wilt basis op informatie uit een ander project, kiest u de actie **Project kopiëren**, vult u de benodigde velden in en kiest u de knop **OK**.

> [!NOTE]  
> Als u urenstaten in uw project gebruikt, moet u ook een verantwoordelijke aanwijzen. Deze persoon kan urenstaten goedkeuren voor de werknemertaken die aan het project zijn gekoppeld. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

Markeer optioneel acties op het project als geblokkeerd met behulp van het veld **Geblokkeerd**. In de volgende tabel wordt het effect van opties op dit veld beschreven.

|Optie  |Omschrijving  |
|---------|---------|
|Leeg |Alle acties zijn toegestaan.|
|Boeking    |U kunt wel met planningsregels werken, maar het project kan niet worden geboekt. Het boeken van projectgebruik of -omzet is niet mogelijk.|
|Alle  |Alle acties zijn geblokkeerd.|

## Taken maken voor een project

Een essentieel onderdeel bij het maken van een nieuw project is dat de verschillende taken worden opgegeven die bij het project horen. U geeft taken op door één regel per taak op te geven op het sneltabblad **Taken** op de pagina **Projectkaart**. Elk project moet minimaal één taak hebben.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open de projectkaart voor een relevant project.
3. Vul op het sneltabblad **Taken** indien nodig de velden in op een nieuwe regel.
4. Als u taken wilt laten inspringen en een hiërarchie wilt maken, kiest u de actie **Taken** en vervolgens de actie **Projecttaken inspringen**.
5. Herhaal stap 3 en 4 voor alle taken die u voor het project nodig hebt.
6. Als u de projecttaken wilt opgeven met informatie over andere projecttaken, kiest u de actie **Projecttaken kopiëren vanuit**, vult u de benodigde velden in en kiest u de knop **OK**.

## Planningsregels voor een project maken

U kunt de nieuwe projecttaken op projectplanningsregels verfijnen. Een planningsregel kan worden gebruikt voor het vastleggen van de gegevens die u voor een project wilt bijhouden. U kunt bijvoorbeeld de resources bijhouden die voor het project nodig zijn, of de items die nodig zijn. U heeft bijvoorbeeld een taak om een klant een project te laten goedkeuren. Die taak kan vervolgens worden gekoppeld aan planningsregels voor artikelen, zoals bijeenkomst met de klant en het toewijzen van een resource.  

Een projectplanningsregel kan van de volgende soorten zijn.  

| Type | Omschrijving |
| --- | --- |
| **Budget** |Zorgt voor het geschatte gebruik en de geschatte kosten voor het project. Doorgaans wordt hier een tijd- en materialenproject voor gebruikt. Planningsregels van dit type kunnen niet worden gefactureerd. |
| **Factureerbaar** |Levert de geschatte facturen aan de klant, doorgaans in een project met een vaste prijs. |
| **Budget en factureerbaar** |Levert gebudgetteerd gebruik dat gelijk is aan wat u wilt factureren. |

> [!NOTE]
> Tijdens het invoeren van gegevens op projectplanningsregels worden de kostprijsgegevens automatisch ingevuld. De kosten, prijs en korting voor resources en artikelen worden gebaseerd op informatie uit de resource en het artikel.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open de betreffende projectkaart.
3. Selecteer een projecttaak waarvoor **Boeking** de **Projecttaaksoort** is, en kies vervolgens de actie **Projectplanningsregels**.  
4. Vul op de pagina **Projectplanningsregels** op een nieuwe regel de benodigde velden in.
5. Herhaal stap 3 en 4 voor alle planningsregels die u voor de projecttaak nodig hebt.

## Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Video: Hoe u een project maakt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
