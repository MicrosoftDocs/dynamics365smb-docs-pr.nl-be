---
title: Een projectkaart voor een project maken en taken opgeven| Microsoft Docs'
description: Voor een nieuw project maakt u een projectkaart met projecttaken en planningsregels om u te helpen voortgang en budgetten te beheren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 12fdf2f9080112b65a2723d17cecd12653be0c3c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780519"
---
# <a name="create-jobs"></a>Projecten maken
Wanneer u een nieuw project start, moet u een projectkaart maken met geïntegreerde projecttaken en projectplanningsregels, die uit twee lagen wordt gestructureerd.  

De eerste laag bestaat uit projecttaken. U moet ten minste één projecttaak per project maken omdat alle boekingen naar een projecttaak verwijzen. Als uw project ten minste één projecttaak bevat, kunt u projectplanningregels instellen en verbruik voor het project boeken.

De tweede laag bestaat uit projectplanningregels, waarin gedetailleerd het verbruik wordt aangegeven van resources, artikelen en diverse grootboekkosten.

Dankzij de laagstructuur kunt u het project in kleinere taken onderverdelen en dus specifieke details gebruiken voor budgettering, offertes en registratie. Daarnaast krijgt u inzicht in hoe een project verloopt. Zo kunt u bijvoorbeeld bijhouden of u aan aangewezen mijlpalen voldoet of op koers zit wat de budgetverwachtingen betreft.

> [!TIP]
> Kies de actie **Nieuw project** in het rolcentrum **Projectmanager** om een begeleide instelling te starten die u begeleidt bij de stappen voor het maken van een project met geïntegreerde taken en planningsregels. In de volgende procedure wordt beschreven hoe u handmatig de stappen uitvoert. Voor een voorbeeld van hoe u een project handmatig kunt maken kijkt u naar [Video: Hoe u een project maakt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

## <a name="to-create-a-job-card"></a>Een projectkaart maken
U maakt een projectkaart en maakt vervolgens projecttaakregels en projectplanningsregels hiervoor.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies de desbetreffende koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u het project wilt opgeven met informatie over andere projecten, kiest u de actie **Project kopiëren**, vult u de benodigde velden in en kiest u de knop **OK**.

> [!NOTE]  
>   Als u urenstaten in uw project gebruikt, moet u ook een verantwoordelijke aanwijzen. Deze persoon kan urenstaten goedkeuren voor de werknemertaken die aan het project zijn gekoppeld. Zie [Urenstaten instellen](projects-how-setup-time-sheets.md) voor meer informatie.

## <a name="to-create-tasks-for-a-job"></a>Taken maken voor een project
Een essentieel onderdeel bij het maken van een nieuw project is dat de verschillende taken worden opgegeven die bij het project horen. Dit doet u door nieuwe regels toe te voegen op het sneltabblad **Taken** op de pagina **Projectkaart**, met één taak per regel. Elk project moet minimaal één taak hebben.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies de desbetreffende koppeling.
2. Open de projectkaart voor een relevant project.
3. Vul op het sneltabblad **Taken** indien nodig de velden in op een nieuwe regel.
4. Als u taken wilt laten inspringen en een hiërarchie wilt maken, kiest u de actie **Taken** en vervolgens de actie **Projecttaken inspringen**.
5. Herhaal stap 3 en 4 voor alle taken die u voor de taak nodig hebt.
6. Als u de projecttaken wilt opgeven met informatie over andere projecttaken, kiest u de actie **Projecttaken kopiëren vanuit**, vult u de benodigde velden in en kiest u de knop **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Planningsregels voor een project maken
U kunt de nieuwe projecttaken op projectplanningsregels verfijnen. Een planningsregel kan worden gebruikt voor het vastleggen van de gegevens die u voor een project wilt bijhouden. U kunt met planningsregels gegevens toevoegen, zoals welke resources er nodig zijn of welke artikelen er moeten worden vastgelegd om het project uit te voeren. Als u bijvoorbeeld een taak hebt om goedkeuring van klanten te krijgen, kunt u die taak koppelen aan planningsregels voor artikelen, zoals bijeenkomst met de klant en het toewijzen van een resource.  

Een projectplanningsregel kan van de volgende soorten zijn.  

| Type | Omschrijving |
| --- | --- |
| **Budget** |Zorgt voor het geschatte gebruik en de geschatte kosten voor het project. Doorgaans wordt hier een tijd- en materialenproject voor gebruikt. Planningsregels van deze soort kunnen niet worden gefactureerd. |
| **Factureerbaar** |Levert de geschatte facturen aan de klant, doorgaans in een project met een vaste prijs. |
| **Budget en factureerbaar** |Levert gebudgetteerd gebruik dat gelijk is aan wat u wilt factureren. |

**Opmerking**. Tijdens het invoeren van gegevens op projectplanningsregels worden de kostprijsgegevens automatisch ingevuld. De kosten, de prijs en de korting voor resources en artikelen zijn bijvoorbeeld in eerste instantie gebaseerd op de gegevens die op de resource- en artikelkaarten staan.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies de desbetreffende koppeling.
2. Open de betreffende projectkaart.
3. Selecteer een projecttaak waarvoor **Boeking** de **projecttaaksoort** is, en kies vervolgens de actie **Projectplanningsregels**.  
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