---
title: Een projectkaart voor een project maken en taken opgeven
description: Voor een nieuw project maakt u een projectkaart met projecttaken en planningsregels om u te helpen voortgang en budgetten te beheren.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6996c82ee184db980879ea98a6f2cbdca1b10852
ms.sourcegitcommit: 55f42d2407e109b4924218cb22129467b53deb08
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557205"
---
# <a name="create-jobs"></a>Projecten maken
Wanneer u een nieuw project start, moet u een projectkaart maken met geïntegreerde projecttaken en projectplanningsregels, die uit twee lagen wordt gestructureerd.  

De eerste laag bestaat uit projecttaken. U moet ten minste één projecttaak per project maken omdat alle boekingen naar een projecttaak verwijzen. Als uw project ten minste één projecttaak bevat, kunt u projectplanningregels instellen en verbruik voor het project boeken.

De tweede laag bestaat uit projectplanningregels, waarin gedetailleerd het verbruik wordt aangegeven van resources, artikelen en diverse grootboekkosten.

Dankzij de laagstructuur kunt u het project in kleinere taken onderverdelen en dus specifieke details gebruiken voor budgettering, offertes en registratie. Daarnaast krijgt u inzicht in hoe een project verloopt. Zo kunt u bijvoorbeeld bijhouden of u aan aangewezen mijlpalen voldoet of op koers zit wat de budgetverwachtingen betreft.

> [!TIP]
> Kies de actie **Nieuw project** in het rolcentrum **Projectmanager** om een begeleide instelling te starten die u begeleidt bij de stappen voor het maken van een project met geïntegreerde taken en planningsregels. In de volgende procedure wordt beschreven hoe u handmatig de stappen uitvoert. Voor een voorbeeld van hoe u een project handmatig kunt maken kijkt u naar [Video: Hoe u een project maakt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

Soms wijkt de partij die een service ontvangt, af van de partij die de rekening betaalt. Op de pagina **Taken** geeft u de klant die van het project profiteert op in de velden **Verkopen aan** en de te factureren partij in de velden **Factureren aan**. U kunt ook de volgende informatie verschaffen. 

* Waar het werk zal gebeuren door te selecteren uit een lijst met verzendadressen voor de klant.
* Voeg informatie over externe referenties toe om de communicatie over het project te vereenvoudigen.
* Overschrijf de standaard financiële voorwaarden van het project.

## <a name="to-create-a-job-card"></a>Een projectkaart maken
U maakt een projectkaart en maakt vervolgens projecttaakregels en projectplanningsregels hiervoor.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u het project wilt opgeven met informatie over andere projecten, kiest u de actie **Project kopiëren**, vult u de benodigde velden in en kiest u de knop **OK**.

> [!NOTE]  
>   Als u urenstaten in uw project gebruikt, moet u ook een verantwoordelijke aanwijzen. Deze persoon kan urenstaten goedkeuren voor de werknemertaken die aan het project zijn gekoppeld. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

## <a name="to-create-tasks-for-a-job"></a>Taken maken voor een project
Een essentieel onderdeel bij het maken van een nieuw project is dat de verschillende taken worden opgegeven die bij het project horen. U geeft taken op door één regel per taak op te geven op het sneltabblad **Taken** op de pagina **Projectkaart**. Elk project moet minimaal één taak hebben.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open de projectkaart voor een relevant project.
3. Vul op het sneltabblad **Taken** indien nodig de velden in op een nieuwe regel.
4. Als u taken wilt laten inspringen en een hiërarchie wilt maken, kiest u de actie **Taken** en vervolgens de actie **Projecttaken inspringen**.
5. Herhaal stap 3 en 4 voor alle taken die u voor de taak nodig hebt.
6. Als u de projecttaken wilt opgeven met informatie over andere projecttaken, kiest u de actie **Projecttaken kopiëren vanuit**, vult u de benodigde velden in en kiest u de knop **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Planningsregels voor een project maken
U kunt de nieuwe projecttaken op projectplanningsregels verfijnen. Een planningsregel kan worden gebruikt voor het vastleggen van de gegevens die u voor een project wilt bijhouden. U kunt bijvoorbeeld de resources bijhouden die voor het project nodig zijn, of de items die nodig zijn. U heeft bijvoorbeeld een taak om een klant een project te laten goedkeuren. Die taak kan vervolgens worden gekoppeld aan planningsregels voor artikelen, zoals bijeenkomst met de klant en het toewijzen van een resource.  

Een projectplanningsregel kan van de volgende soorten zijn.  

| Type | Omschrijving |
| --- | --- |
| **Budget** |Zorgt voor het geschatte gebruik en de geschatte kosten voor het project. Doorgaans wordt hier een tijd- en materialenproject voor gebruikt. Planningsregels van dit type kunnen niet worden gefactureerd. |
| **Factureerbaar** |Levert de geschatte facturen aan de klant, doorgaans in een project met een vaste prijs. |
| **Budget en factureerbaar** |Levert gebudgetteerd gebruik dat gelijk is aan wat u wilt factureren. |

> [!NOTE]
> Tijdens het invoeren van gegevens op projectplanningsregels worden de kostprijsgegevens automatisch ingevuld. De kosten, prijs en korting voor resources en artikelen worden gebaseerd op informatie uit de resource en het artikel. 

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open de betreffende projectkaart.
3. Selecteer een projecttaak waarvoor **Boeking** de **projecttaaksoort** is, en kies vervolgens de actie **Projectplanningsregels**.  
4. Vul op de pagina **Projectplanningsregels** op een nieuwe regel de benodigde velden in.
5. Herhaal stap 3 en 4 voor alle planningsregels die u voor de projecttaak nodig hebt.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Voorraad- en magazijnpickdocumenten maken voor een project
Om voorraad- en magazijnpickdocumenten voor projecten te maken moet uw beheerder de **Functie-update: Voorraad- en magazijnpicks vanuit projecten inschakelen** op de pagina **Functiebeheer** inschakelen.

De functie voegt de acties **Voorraadpick maken** en **Magazijnpick maken** toe aan de **Projectkaart**. Om een pickdocument te maken of te registreren gebruikt u de acties **Opslag-/pick-/verplaatsingsregels** of **Geregistreerde pickregels**.

U kunt de acties onder de volgende voorwaarden gebruiken:
* De **Status** van het project is **Open**.
* De **Regelsoort** van de taakplanningsregel is **Budget** of **Zowel Budget als Factureerbaar**.
* Het **Type** van de projectplanningsregel is **Artikel**.
* **Pick vereist** is ingeschakeld voor de gerelateerde locatie.
* **Gestuurde opslag en pick** is uitgeschakeld.

> [!NOTE] 
> Hoewel de instelling **Pick vereist** heet, kunt u het verbruik nog steeds rechtstreeks vanuit de projectdagboekregel voor de locatie boeken. Als voor uw vestiging wel pickverwerking maar geen verzendingsverwerking is ingesteld, gebruikt u de pagina **Voorraadpick** om de pickgegevens te beheren en af te drukken. U gebruikt de pagina ook om het resultaat van de pick in te voeren en te boeken, wat op zijn beurt het verbruik van de artikelen publiceert. 
> 
> Wanneer voor uw vestiging zowel pick- als verzendingsverwerking vereist is, wat wil zeggen dat u zowel het veld **Pick vereist** als het veld **Verzending vereist** hebt gekozen op de pagina **Vestiging**, gebruikt u de pagina **Magazijnpick** om de pick te verwerken. Magazijnpicks zijn vergelijkbaar met voorraadpicks. Het verschil is dat in plaats van de pickinformatie te boeken, u de pick registreert. Deze registratie boekt geen verbruik, maar maakt de artikelen alleen beschikbaar voor boeking. Als magazijnmanager kunt u met behulp van een pickvoorstel pickgegevens ordenen voordat de afzonderlijke magazijnpickinstructies worden gemaakt

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Video: Hoe u een project maakt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]