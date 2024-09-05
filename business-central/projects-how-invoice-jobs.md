---
title: Maak een projectverkoopfactuur om een project te factureren
description: Beschrijft hoe u klanten factureert voor projectonkosten terwijl een project loopt en kosten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
---
# <a name="invoice-projects"></a>Factuurprojecten

Tijdens het project kunnen projectkosten van resourceverbruik, materialen en aan het project gerelateerde inkopen, zich ophopen. Naarmate het project vordert, worden deze transacties geboekt in het projectdagboek. Het is van belang dat alle kosten worden vastgelegd in het projectdagboek voordat u het project aan de klant factureert.
Facturering kan plaatsvinden nadat het project is voltooid of op bepaalde intervallen tijdens de voortgang van het project op basis van een factureringsschema.

U kunt factureren:

* Meerdere projecten met behulp van een **project Maak verkoopfactuur** taak.
* Hele projecten, enkele projecten binnen een project of individuele projectplanningslijnen met behulp van de relevante actie op de projectpagina's.
* Combineer meerdere projectplanningsregels uit verschillende projecten tot één verkoopfactuur met behulp van de actie  **projectplanningsregels ophalen**  op de pagina  **Verkoopfactuur** .

## <a name="to-create-multiple-project-sales-invoices"></a>Meerdere projectverkoopfacturen maken

U kunt een factuur voor een project of voor een of meer projecttaken voor een klant maken wanneer het werk dat moet worden gefactureerd, voltooid is of de datum voor facturering op basis van een factureringsschema is bereikt.

In de volgende procedure wordt beschreven hoe u een batchverwerking gebruikt om meerdere projecten te factureren.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfactuur project maken** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Stel filters in als u de projecten wilt beperken die door de batchverwerking worden verwerkt.
4. Kies de knop **OK** om de facturen te maken.  

U kunt de gemaakte facturen bekijken en boeken op de pagina  **Verkoopfacturen** .

> [!NOTE]
> U kunt een klant ook factureren door het project te selecteren en vervolgens de actie  **projectverkoopfactuur maken**  te kiezen. U kunt ook de actie  **Verkoopfactuur maken**  gebruiken in de projecttaken.

## <a name="to-create-and-post-project-sales-invoice-from-project-planning-lines"></a>Projectverkoopfacturen maken en boeken vanuit projectplanningsregels

U kunt een factuur maken vanuit een projectplanningsregel en op dat moment de hoeveelheid van het artikel, resource of grootboekrekening die u wilt factureren, aangeven.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open een relevant project.
3. Selecteer een projecttaak waarvoor **Boeking** de **Projecttaaksoort** is, en kies vervolgens de actie **Projectplanningsregels**.  
4. Voer op een projectplanningsregel in het veld **Aantal te verplaatsen naar factuur** de hoeveelheid van het artikel, de resource en het soort grootboekrekening dat u wilt factureren in.  
5. Kies de actie **Verkoopfactuur maken**.
6. Voer op de pagina **Projecttransfer naar verkoopfactuur** de boekingsdatum in en of u een nieuwe factuur wilt maken of toevoegen aan deze factuur of aan een bestaande factuur.
7. Kies de knop **Ok**.  
8. Kies op de pagina **Projectplanningsregels** de actie **Verkoopfacturen/-creditnota's**.

    De pagina **Verkoopfactuur** wordt geopend met het aantal dat u naar de factuur hebt verzonden.
9. Breng eventuele aanvullende wijzigingen aan en kies vervolgens de actie **Boeken**.

> [!NOTE]  
> De bovengenoemde procedure is soortgelijk voor het maken, controleren en boeken van een aan een project gerelateerde verkoopcreditnota.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Eén klant factureren voor meerdere projecttaken

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
> * U kunt niet filteren op de velden **Verzendcode** of **Contactnr.** in.


## <a name="see-also"></a>Zie ook

[Projecten beheren](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
