---
title: Maak een project kaart voor een project en specificeer taken
description: Voor een nieuw project maakt u een projectkaart met projecttaken en planningsregels om u te helpen voortgang en budgetten te beheren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Projecten maken

Wanneer u een nieuw project start, moet u een projectkaart maken met geïntegreerde projecttaken en projectplanningsregels, die uit twee lagen wordt gestructureerd.  

De eerste laag bestaat uit projecttaken. U moet ten minste één projecttaak per project maken omdat alle boekingen naar een projecttaak verwijzen. Als uw project ten minste één projecttaak bevat, kunt u projectplanningregels instellen en verbruik voor het project boeken.

De tweede laag bestaat uit projectplanningregels, waarin gedetailleerd het verbruik wordt aangegeven van resources, artikelen en diverse grootboekkosten.

Dankzij de laagstructuur kunt u het project in kleinere taken onderverdelen en dus specifieke details gebruiken voor budgettering, offertes en registratie. Daarnaast krijgt u inzicht in hoe een project verloopt. Zo kunt u bijvoorbeeld bijhouden of u aan aangewezen mijlpalen voldoet of op koers zit wat de budgetverwachtingen betreft.

> [!TIP]
> Kies de actie **Nieuw project** in het rolcentrum **Projectmanager** om een begeleide instelling te starten die u begeleidt bij de stappen voor het maken van een project met geïntegreerde taken en planningsregels. In de volgende procedure wordt beschreven hoe u handmatig de stappen uitvoert. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="to-create-a-project-card"></a>Een projectkaart maken

U maakt een projectkaart en maakt vervolgens projecttaakregels en projectplanningsregels hiervoor.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u het project wilt basis op informatie uit een ander project, kiest u de actie **Project kopiëren**, vult u de benodigde velden in en kiest u de knop **OK**.

> [!NOTE]  
> Als u bij uw project gebruikmaakt van urenstaten, moet u ook een verantwoordelijke persoon aanwijzen. Deze persoon kan urenstaten goedkeuren voor de werknemertaken die aan het project zijn gekoppeld. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

> [!NOTE]  
> Met de schakelaar  **gebruikscode koppelen toepassen** wordt aangegeven of projectboekposten aan projectplanningsregels zijn gekoppeld. Met de schakelaar  **gebruiksgebruik koppelen toepassen** wordt ook de mogelijkheden voor magazijnafhandeling, planning, assemblage op bestelling, artikeltracering en reservering voor een project geactiveerd.

Markeer optioneel acties op het project als geblokkeerd met behulp van het veld **Geblokkeerd**. De volgende tabel beschrijft het effect van de opties voor dit veld.

|Optie  |Beschrijving  |
|---------|---------|
|Leeg |Alle acties zijn toegestaan.|
|Boeking    |U kunt wel met planningsregels werken, maar het project kan niet worden geboekt. U kunt geen gebruik of verkoop voor het project boeken.|
|Alle  |Alle acties zijn geblokkeerd.|

## <a name="to-create-tasks-for-a-project"></a>Taken maken voor een project

Een essentieel onderdeel bij het maken van een nieuw project is dat de verschillende taken worden opgegeven die bij het project horen. U geeft taken op door één regel per taak op te geven op het sneltabblad **Taken** op de pagina **Projectkaart**. Elk project moet minimaal één taak hebben.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open de projectkaart voor een relevant project.
3. Vul op het sneltabblad **Taken** indien nodig de velden in op een nieuwe regel.
4. Als u taken wilt laten inspringen en een hiërarchie wilt maken, kiest u de actie **Taken** en vervolgens de actie **Projecttaken inspringen**.
5. Herhaal stap 3 en 4 voor alle taken die u voor het project nodig hebt.
6. Als u de projecttaken wilt opgeven met informatie over andere projecttaken, kiest u de actie **Projecttaken kopiëren vanuit**, vult u de benodigde velden in en kiest u de knop **OK**.

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Meerdere klanten factureren voor projecttaken

Soms wijkt de partij die een service ontvangt, af van de partij die de rekening betaalt. Soms moet u ook meerdere klanten factureren voor taken in het project. Gebruik op de pagina **Projectkaart** het veld **Factureringsmethode voor taken** om op te geven of u één klant factureert, of meerdere klanten.

Als de klant die de service ontvangt ook de factuur betaalt, kiest u in de velden **Factureren aan** en **Verzenden aan** **Standaard (klant)** en **Standaard (orderadres)**.

Als u meerdere klanten factureert, kunt u voor elke taak in het project de klant opgeven die de service ontvangt en de klant die u moet factureren. U kunt ook de volgende informatie verschaffen.

* Selecteer het verzendadres voor de klant waar de werkzaamheden zullen plaatsvinden.
* Voeg informatie over externe referenties toe om de communicatie over het project te vereenvoudigen.
* Overschrijf de standaard financiële voorwaarden van het project.

## <a name="specify-a-default-location-for-project-items"></a>Geef een standaardlocatie op voor projectartikelen

U kunt tijd besparen bij het invoeren van gegevens door een standaardlocatie en opslaglocatie voor projecten op te geven op de  pagina **Projectkaart**. Wanneer u projecttaken, projectplanningsregels en projectdagboekregels voor het project aanmaakt, worden de standaardlocatie en de opslaglocatie automatisch toegewezen. U kunt echter indien nodig de locatiecode en de opslaglocatie voor taken en regels wijzigen.

Als u een **Bin Code naar project** op de locatie definieert, wordt de opslaglocatie ingevuld wanneer u de locatiecode selecteert. Als uw magazijnstroom magazijnpicks vereist, kunt u ook andere opslaglocaties definiëren waaruit u artikelen wilt verbruiken.

Deze velden zijn de standaardwaarden wanneer u projecttaken maakt. Bestaande projecttaken veranderen niet.

Er zijn een paar dingen die u moet weten over het gebruik van standaardlocaties:

* Als u voor projecttaken een **Bin Code naar project** op de locatie definieert, wordt de opslaglocatie toegewezen wanneer u de locatiecode selecteert. Als uw magazijnstroom magazijnpicks vereist, kunt u ook andere opslaglocaties definiëren waaruit u artikelen wilt verbruiken.
* Voor projectplanningsregels is de **Locatiecode** gebaseerd op de waarde die is geselecteerd op de projectplanningsregel wanneer u een artikel selecteert. Als er geen bin code is gedefinieerd voor de projecttaak, wordt de opslaglocatie uit de standaard inhoud geselecteerd. U kunt de beide waarden handmatig wijzigen.
* Voor projectjournaalregels is de **Locatiecode** gebaseerd op de waarde die is geselecteerd op de projectjournaalregel wanneer u een artikel selecteert. Als er geen bin code is gedefinieerd voor de projecttaak, wordt de opslaglocatie uit de standaard inhoud geselecteerd. U kunt de beide waarden handmatig wijzigen.

## <a name="to-create-planning-lines-for-a-project"></a>Planningsregels voor een project maken

U kunt de nieuwe projecttaken op projectplanningsregels verfijnen. Een planningsregel kan worden gebruikt voor het vastleggen van de gegevens die u voor een project wilt bijhouden. U kunt bijvoorbeeld de resources bijhouden die voor het project nodig zijn, of de items die nodig zijn. U heeft bijvoorbeeld een taak om een klant een project te laten goedkeuren. Die taak kan vervolgens worden gekoppeld aan planningsregels voor artikelen, zoals bijeenkomst met de klant en het toewijzen van een resource.  

Een projectplanningsregel kan van de volgende soorten zijn.  

| Type | Beschrijving |
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

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Video: Hoe u een project maakt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
