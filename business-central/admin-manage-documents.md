---
title: Opslag beheren door documenten te verwijderen of gegevens te comprimeren
description: Leer hoe u omgaat met het verzamelen van historische documenten (en verminder de hoeveelheid gegevens die in een database wordt opgeslagen) door ze te verwijderen of te comprimeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 5263d4ba06cc7b2dc497efb6842a927704c31f35
ms.sourcegitcommit: 428ba6385cb27475e8803c2a8967daa22cfe8879
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/29/2021
ms.locfileid: "7724724"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Opslag beheren door documenten te verwijderen of gegevens te comprimeren

Een centrale rol, bijvoorbeeld de toepassingsbeheerder, moet regelmatig de verzamelde historische documenten verwijderen of comprimeren.  

> [!TIP]
> Zie voor informatie over andere manieren om de hoeveelheid gegevens die in een database is opgeslagen, te verminderen [Gegevens in Business Central-databases verminderen](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) in de documentatie voor ontwikkelaars en IT-professionals.

## <a name="delete-documents"></a>Documenten verwijderen

Het kan voorkomen dat u gefactureerde inkooporders moet verwijderen die niet automatisch zijn verwijderd. [!INCLUDE[prod_short](includes/prod_short.md)] controleert of de verwijderde inkooporders volledig zijn gefactureerd. U kunt geen orders verwijderen die u niet volledig hebt ontvangen en gefactureerd.  

Nadat retourorders zijn gefactureerd, worden deze doorgaans verwijderd. Wanneer u een factuur boekt, wordt deze overgebracht naar de pagina **Geboekte inkoopcreditnota**. Als u het selectievakje **Retourzending op creditnota** hebt ingeschakeld op de pagina **Inkoopinstellingen**, wordt de factuur overgebracht naar de pagina **Geboekte retourverzending**. U kunt de documenten verwijderen met behulp van de batchverwerking **Gef. ink.-retourorders verw.**. Voordat de verwijdering wordt uitgevoerd, controleert de batchverwerking of inkoopretourorders volledig zijn verzonden en gefactureerd.  

Inkoopraamcontracten worden niet verwijderd nadat u alle bijbehorende inkooporders hebt verwerkt en gefactureerd. U kunt raamcontracten verwijderen met de batchverwerking **Gefact. inkoopraamcontracten verwijderen**.  

Gefactureerde servicefacturen worden doorgaans automatisch verwijderd als ze volledig zijn gefactureerd. Wanneer een factuur wordt geboekt, wordt een bijbehorende post gemaakt op de pagina **Geboekte servicefacturen**. U kunt het geboekte document bekijken op de pagina **Geboekte servicefactuur**.  

Serviceorders worden echter niet automatisch verwijderd als het totale aantal op de order niet vanuit de serviceorder zelf is geboekt, maar vanuit de pagina **Servicefactuur**. In dit geval zult u wellicht gefactureerde orders die niet zijn verwijderd, zelf moeten verwijderen. Hiervoor kunt u de batchverwerking **Gefactureerde serviceorders verwijderen** uitvoeren.  

## <a name="compress-data-with-date-compression"></a>Gegevens comprimeren met datumcompressie

U kunt gegevens comprimeren in [!INCLUDE [prod_short](includes/prod_short.md)] zodat u ruimte bespaart in de database, wat u in [!INCLUDE [prod_short](includes/prod_short.md)] online zelfs geld kan besparen. De compressie wordt gebaseerd op datums en werkt door meerdere oude vermeldingen te combineren tot één nieuwe vermelding. 

U kunt posten comprimeren onder de volgende voorwaarden:

* Ze komen uit afgesloten boekjaren
* Het veld **Geopend** is ingesteld op **Nee**. 
* Ze zijn minstens vijf jaar oud. Neem contact op met uw Microsoft-partner als u gegevens wilt comprimeren die minder dan vijf jaar oud zijn.

U kunt bijvoorbeeld leveranciersposten van vorige boekjaren comprimeren zodat er voor elke rekening per maand slechts één creditpost en één debetpost is. De waarde van de nieuwe post is gelijk aan de som van alle gecomprimeerde posten. De toegewezen datum is de eerste dag van de gecomprimeerde periode, bijvoorbeeld de eerste dag van de maand (als u de posten per maand comprimeert). Na de compressie kunt u nog steeds van alle rekeningen de mutatie in het vorige boekjaar bekijken.

Het aantal posten dat resulteert van een batchverwerking voor datumcompressie is afhankelijk van hoeveel filters u instelt, welke velden worden gecombineerd en welke periodelengte u kiest. Er zal steeds minstens één post worden gevormd. Het resultaat van de compressie kunt u wanneer de batchverwerking is voltooid, bekijken op de pagina **Datumcompressiejournalen**.

U kunt de volgende soorten gegevens comprimeren met behulp van batchtaken. Er is een batchtaak voor elk type gegevens.

* Financiële boekingen - grootboekposten, btw-posten, bankrekeningposten, grootboekbudgetposten, klantenposten, leveranciersposten.
* Magazijnposten 
* Bronposten
* Artikelbudgetposten
* Vast activum - Vaste-activaposten, VA-onderhoudsposten, VA-verzekeringsposten.

Wanneer u criteria voor de compressie definieert, kunt u de opties onder **Te bewaren velden** gebruiken om de inhoud van bepaalde velden te behouden. Welke velden beschikbaar zijn, hangt af van de gegevens die u comprimeert.

> [!NOTE]
> Voordat u datumcompressie kunt uitvoeren, moeten uw analyseweergaven up-to-date zijn. Zie voor meer informatie [Een analyseweergave bijwerken](bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Na de compressie blijft de inhoud van de volgende velden altijd behouden: **Boekingsdatum**, **Leveranciersnr.**, **Documentsoort**, **Valutacode**, **Boekingsgroep**, **Bedrag**, **Restbedrag**, **Oorspronkelijk bedrag (LV)**, **Restbedrag (LV)**, **Bedrag (LV)**, **Inkoop (LV)**, **Factuurkorting (LV)**, **Contantkorting verleend (LV)** en **Contantkorting**.

## <a name="posting-compressed-entries"></a>Gecomprimeerde posten boeken
Gecomprimeerde posten worden iets anders geboekt dan standaardboekingen. Dit is bedoeld om het aantal nieuwe grootboekposten dat wordt gecreëerd door datumcompressie te verminderen, en is vooral belangrijk wanneer u informatie bewaart, zoals dimensies en documentnummers. Met datacompressie worden als volgt nieuwe posten gemaakt:
* Op de pagina **Grootboekposten** worden nieuwe posten gemaakt met nieuwe postnummers voor de gecomprimeerde posten. Het veld **Omschrijving** bevat **Datum gecomprimeerd** zodat de gecomprimeerde posten gemakkelijk te identificeren zijn. 
* Op grootboekpagina's, zoals de pagina **Klantenposten** worden een of meer posten gemaakt met nieuwe postnummers. 

Het boekingsproces creëert hiaten in de nummerreeks voor posten op de pagina **Grootboekposten**. Die nummers worden alleen toegewezen aan de posten op de grootboekpagina's. Het nummerbereik dat aan de posten is toegewezen, is beschikbaar op de **pagina Grootboekjournaal** in de velden **Van volgnr.** en **Tot volgnr.**. 

> [!NOTE]
> Nadat u datacompressie heeft uitgevoerd, worden alle rekeningen in het grootboek vergrendeld. U kunt bijvoorbeeld leveranciers- of bankboekingen niet ongedaan maken voor rekeningen gedurende de periode waarvoor datums zijn gecomprimeerd.

Het aantal posten dat resulteert van een batchverwerking voor datumcompressie is afhankelijk van hoeveel filters u instelt, welke velden worden gecombineerd en welke periodelengte u kiest. Er zal steeds minstens één post worden gevormd. 

> [!WARNING]
> Tijdens datumcompressie worden posten verwijderd. Het is daarom verstandig altijd eerst een reservekopie van de database te maken, voordat u de batchverwerking start.

### <a name="to-run-a-date-compression"></a>Een datumcompressie uitvoeren
1. Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Gegevensbeheer** in en kies de desbetreffende koppeling.
2. Ga op een van de volgende manieren te werk:
    * Als u een begeleide instelling wilt gebruiken om datumcompressie in te stellen voor een of meer soorten gegevens, kiest u **Guide voor gegevensbeheer**.
    * Om compressie in te stellen voor een individueel type gegevens, kiest u **Datumcompressie**, **Posten comprimeren** en kiest u vervolgens de gegevens die u wilt comprimeren.

   > [!NOTE]
   > U kunt alleen gegevens comprimeren die ouder zijn dan vijf jaar. Neem contact op met uw Microsoft-partner als u gegevens wilt comprimeren die minder dan vijf jaar oud zijn.

## <a name="see-also"></a>Zie ook

[Beheer](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]