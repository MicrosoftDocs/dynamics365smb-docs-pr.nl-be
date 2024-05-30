---
title: Opslag beheren door documenten te verwijderen of gegevens te comprimeren
description: Leer hoe u omgaat met het verzamelen van historische documenten (en verminder de hoeveelheid gegevens die in een database wordt opgeslagen) door ze te verwijderen of te comprimeren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 04/16/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Opslag beheren door documenten te verwijderen of gegevens te comprimeren

Een centrale rol, bijvoorbeeld de toepassingsbeheerder, moet regelmatig de verzamelde historische documenten verwijderen of comprimeren.  

> [!TIP]
> Lees voor meer informatie over andere manieren om de hoeveelheid gegevens die in een database is opgeslagen, te verminderen [Gegevens opgeslagen in Business Central-databases verminderen](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) in onze documentatie voor ontwikkelaars en IT-professionals.

## <a name="delete-documents"></a>Documenten verwijderen

Het kan voorkomen dat u gefactureerde inkooporders moet verwijderen. U kunt ze echter pas verwijderen als u de artikelen in de inkooporders volledig hebt gefactureerd en ontvangen. [!INCLUDE[prod_short](includes/prod_short.md)] helpt u door dat te controleren.

Bedrijven verwijderen retourorders meestal nadat ze zijn gefactureerd. Wanneer u een factuur boekt, brengt [!INCLUDE [prod_short](includes/prod_short.md)] deze over naar de pagina **Geboekte inkoopcreditnota**. Als u het selectievakje **Retourzending op creditnota** hebt ingeschakeld op de pagina **Inkoopinstellingen**, wordt de factuur overgebracht naar de pagina **Geboekte retourverzending**. U kunt de documenten verwijderen met behulp van de batchverwerking **Gef. ink.-retourorders verw.**. Voordat documenten worden verwijderd, controleert de batchverwerking of inkoopretourorders volledig zijn verzonden en gefactureerd.  

Inkoopraamcontracten worden niet automatisch verwijderd nadat u alle bijbehorende inkooporders hebt verwerkt en gefactureerd. In plaats daarvan kunt u ze verwijderen met de batchverwerking **Gefactureerde inkoopraamcontracten verwijderen**.  

Bedrijven verwijderen gefactureerde serviceorders meestal nadat ze volledig zijn gefactureerd. Wanneer een factuur wordt geboekt, wordt een bijbehorende post gemaakt en kan deze vervolgens worden weergegeven op de pagina **Geboekte servicefacturen**.  

Serviceorders worden echter niet automatisch verwijderd als het totale aantal op de order niet via de pagina **Servicefactuur** is geboekt, maar via de serviceorder zelf. Mogelijk moet u dergelijke gefactureerde orders handmatig verwijderen door de batchverwerking **Gefactureerde serviceorders verwijderen** uit te voeren.  

## <a name="compress-data-with-date-compression"></a>Gegevens comprimeren met datumcompressie

U kunt gegevens comprimeren in [!INCLUDE [prod_short](includes/prod_short.md)] zodat u ruimte bespaart in de database&mdash;wat u in [!INCLUDE [prod_short](includes/prod_short.md)] online zelfs geld kan besparen. De compressie, gebaseerd op datums en functies, combineert meerdere oude posten in één nieuwe post.

U kunt posten comprimeren die voldoen aan alle volgende voorwaarden:

* Ze komen uit afgesloten boekjaren.
* Het veld **Geopend** is ingesteld op **Nee**.
* Ze zijn minstens vijf jaar oud. Neem contact op met uw Microsoft-partner als u gegevens wilt comprimeren die minder dan vijf jaar oud zijn.

Zo kunt u bijvoorbeeld leveranciersposten van vorige boekjaren comprimeren zodat er voor elke rekening per maand slechts één creditpost en één debetpost is. De waarde van de nieuwe post is gelijk aan de som van alle gecomprimeerde posten. De toegewezen datum is de eerste dag van de gecomprimeerde periode, zoals de eerste dag van de maand (als u de posten per maand comprimeert). Na de compressie kunt u nog steeds van alle rekeningen de mutatie in het vorige boekjaar bekijken.

Het aantal posten dat resulteert van een batchverwerking voor datumcompressie is afhankelijk van hoeveel filters u instelt, welke velden worden gecombineerd en welke periodelengte u kiest. Er is altijd minstens één post. Het resultaat van de compressie kunt u wanneer de batchverwerking is voltooid, bekijken op de pagina **Datumcompressiejournalen**.

U kunt de volgende soorten gegevens comprimeren met behulp van batchverwerkingen.

* Financiële boekingen - grootboekposten, btw-posten, bankrekeningposten, grootboekbudgetposten, klantenposten en leveranciersposten.
* Magazijnposten
* Bronposten
* Artikelbudgetposten
* Vaste-activaposten (VA), VA-onderhoudsposten en VA-verzekeringsposten.

Wanneer u criteria voor de compressie definieert, kunt u de inhoud van bepaalde velden behouden met de opties onder **Te bewaren velden**. Welke velden beschikbaar zijn, hangt af van de gegevens die u comprimeert.

> [!NOTE]
> Voordat u datumcompressie kunt uitvoeren, moeten uw analyseweergaven actueel zijn. Zie voor meer informatie het gedeelte [Een analyseweergave bijwerken](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Na de compressie blijft de inhoud van de volgende velden altijd behouden: **Boekingsdatum**, **Leveranciersnr.**, **Documentsoort**, **Valutacode**, **Boekingsgroep**, **Bedrag**, **Restbedrag**, **Oorspronkelijk bedrag (LV)**, **Restbedrag (LV)**, **Bedrag (LV)**, **Inkoop (LV)**, **Factuurkorting (LV)**, **Contantkorting verleend (LV)** en **Contantkorting**.

## <a name="posting-compressed-entries"></a>Gecomprimeerde posten boeken

Gecomprimeerde posten worden iets anders geboekt dan standaardboekingen. Dit verschil is bedoeld om het aantal nieuwe grootboekposten dat wordt gecreëerd door datumcompressie te verminderen, en is vooral belangrijk wanneer u informatie bewaart, zoals dimensies en documentnummers. Met datacompressie worden als volgt nieuwe posten gemaakt:

* Op de pagina **Grootboekposten** worden nieuwe posten gemaakt voor de gecomprimeerde posten. Het veld **Omschrijving** bevat **Datum gecomprimeerd** zodat de gecomprimeerde posten gemakkelijk te identificeren zijn. 
* Op grootboekpagina's, zoals de pagina **Klantenposten** worden een of meer nieuwe posten gemaakt. 

Het boekingsproces creëert hiaten in de nummerreeks voor posten op de pagina **Grootboekposten**. Die nummers worden alleen toegewezen aan de posten op de grootboekpagina's. Het nummerbereik dat aan de posten is toegewezen, is beschikbaar op de pagina **Grootboekjournaal** in de velden **Van volgnr.** en **Tot volgnr.**. 

> [!NOTE]
> Nadat u datumcompressie hebt uitgevoerd, kunt u leveranciers- of bankposten niet meer tegenboeken voor transacties die door de compressie worden beïnvloed.

Het aantal posten dat resulteert van een datumcompressie is afhankelijk van hoeveel filters u instelt, welke velden worden gecombineerd en welke periodelengte u kiest. Er is altijd minstens één post.

> [!WARNING]
> Tijdens datumcompressie worden posten verwijderd. Het is daarom verstandig altijd eerst een reservekopie van de database te maken, voordat u de batchverwerking start.

### <a name="to-run-a-date-compression"></a>Een datumcompressie uitvoeren

1. Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Het pictogram Zoeken naar pagina of rapport"), voer **Gegevensbeheer** in en kies de gerelateerde koppeling.
2. Doe een van de volgende dingen, afhankelijk van uw wensen:
    * Als u een begeleide instelling wilt gebruiken om datumcompressie in te stellen voor een of meer soorten gegevens, kiest u **Guide voor gegevensbeheer**.
    * Om compressie in te stellen voor een individueel type gegevens, kiest u **Gegevenscompressie**, **Posten comprimeren** en kiest u vervolgens de gegevens die u wilt comprimeren.

   > [!NOTE]
   > U kunt alleen gegevens comprimeren die ouder zijn dan vijf jaar. Neem contact op met uw Microsoft-partner als u gegevens wilt comprimeren die minder dan vijf jaar oud zijn. Ze moeten de gebeurtenis `OnSetMinimumNumberOfYearsToKeep` in de codeunit Datumcompressie gebruiken om de drempelwaarde in te stellen.


## <a name="see-also"></a>Zie ook

[Beheer](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
