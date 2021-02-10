---
title: Opslag beheren door documenten te verwijderen of gegevens te comprimeren
description: Ontdek hoe u uw historische gegevens kunt behouden door grootboekposten te comprimeren of door ze te verwijderen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f0d713f57345c312ddbfe6b5462f2623b1088dfc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753879"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Opslag beheren door documenten te verwijderen of gegevens te comprimeren

Een centrale rol, bijvoorbeeld de toepassingsbeheerder, moet regelmatig de verzamelde historische documenten verwijderen of comprimeren.  

> [!TIP]
> Zie voor informatie over andere manieren om de hoeveelheid gegevens die in een database is opgeslagen, te verminderen [Gegevens in Business Central-databases verminderen](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) in de Help voor ontwikkelaars en IT-professionals.

## <a name="delete-documents"></a>Documenten verwijderen

Het kan voorkomen dat u gefactureerde inkooporders moet verwijderen die niet automatisch zijn verwijderd. [!INCLUDE[prod_short](includes/prod_short.md)] controleert of de verwijderde inkooporders volledig zijn gefactureerd. U kunt geen orders verwijderen die u niet volledig hebt ontvangen en gefactureerd.  

Nadat retourorders zijn gefactureerd, worden deze doorgaans verwijderd. Wanneer u een factuur boekt, wordt deze overgebracht naar de pagina **Geboekte inkoopcreditnota**. Als u het selectievakje **Retourzending op creditnota** hebt ingeschakeld op de pagina **Inkoopinstellingen**, wordt de factuur overgebracht naar de pagina **Geboekte retourverzending**. U kunt de documenten verwijderen met behulp van de batchverwerking **Gef. ink.-retourorders verw.**. Voordat de verwijdering wordt uitgevoerd, controleert de batchverwerking of inkoopretourorders volledig zijn verzonden en gefactureerd.  

Inkoopraamcontracten worden niet verwijderd nadat u alle bijbehorende inkooporders hebt verwerkt en gefactureerd. U kunt raamcontracten verwijderen met de batchverwerking **Gefact. inkoopraamcontracten verwijderen**.  

Gefactureerde servicefacturen worden doorgaans automatisch verwijderd als ze volledig zijn gefactureerd. Wanneer een factuur wordt geboekt, wordt een bijbehorende post gemaakt op de pagina **Geboekte servicefacturen**. U kunt het geboekte document bekijken op de pagina **Geboekte servicefactuur**.  

Serviceorders worden echter niet automatisch verwijderd als het totale aantal op de order niet vanuit de serviceorder zelf is geboekt, maar vanuit de pagina **Servicefactuur**. In dit geval zult u wellicht gefactureerde orders die niet zijn verwijderd, zelf moeten verwijderen. Hiervoor kunt u de batchverwerking **Gefactureerde serviceorders verwijderen** uitvoeren.  

## <a name="compress-data-with-date-compression"></a>Gegevens comprimeren met datumcompressie

U kunt gegevens comprimeren in [!INCLUDE [prod_short](includes/prod_short.md)] zodat u ruimte bespaart in de database, wat u in [!INCLUDE [prod_short](includes/prod_short.md)] online zelfs geld kan besparen. De compressie wordt gebaseerd op datums en werkt door meerdere oude vermeldingen te combineren tot één nieuwe vermelding. U kunt alleen posten uit afgesloten boekjaren comprimeren en alleen leveranciersposten waarvan het veld **Open** is ingesteld op *Nee*.  

U kunt bijvoorbeeld leveranciersposten van vorige boekjaren comprimeren zodat er voor elke rekening per maand slechts één creditpost en één debetpost is. De waarde van de nieuwe post is gelijk aan de som van alle gecomprimeerde posten. De toegewezen datum is de eerste dag van de gecomprimeerde periode, bijvoorbeeld de eerste dag van de maand (als u de posten per maand comprimeert). Na de compressie kunt u nog steeds van alle rekeningen de mutatie in het vorige boekjaar bekijken.

Het aantal posten dat resulteert van een batchverwerking voor datumcompressie is afhankelijk van hoeveel filters u instelt, welke velden worden gecombineerd en welke periodelengte u kiest. Er zal steeds minstens één post worden gevormd. Het resultaat van de compressie kunt u wanneer de batchverwerking is voltooid, bekijken op de pagina **Datumcompressiejournalen**.

U kunt de volgende soorten gegevens comprimeren in [!INCLUDE [prod_short](includes/prod_short.md)] met behulp van batchtaken:

* Bankrekeningposten

  Na de compressie kunt u met de functie **Te bewaren velden** de inhoud van de velden **Documentnr., Ons contact**, **Globale dimensiecode 1** en **Globale dimensiecode 2** bewaren.
* Leveranciersposten

  Na de compressie blijft de inhoud van de volgende velden altijd behouden: **Boekingsdatum**, **Leveranciersnr.**, **Documentsoort**, **Valutacode**, **Boekingsgroep**, **Bedrag**, **Restbedrag**, **Oorspronkelijk bedrag (LV)**, **Restbedrag (LV)**, **Bedrag (LV)**, **Inkoop (LV)**, **Factuurkorting (LV)**, **Contantkorting verleend (LV)** en **Contantkorting**.

  Met de functie **Te bewaren velden** kunt u ook de inhoud van deze extra velden bewaren: **Documentnr.**, **Orderleveranciersnr.**, **Code van inkoper**, **Globale dimensiecode 1** en **Globale dimensiecode 2**.

> [!NOTE]
> Nadat u datacompressie heeft uitgevoerd, worden alle rekeningen in het grootboek vergrendeld. U kunt bijvoorbeeld leveranciers- of bankboekingen niet ongedaan maken voor rekeningen gedurende de periode waarvoor datums zijn gecomprimeerd.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Het aantal posten dat resulteert van een batchverwerking voor datumcompressie is afhankelijk van hoeveel filters u instelt, welke velden worden gecombineerd en welke periodelengte u kiest. Er zal steeds minstens één post worden gevormd. 

> [!WARNING]
> Tijdens de datumcompressie worden posten verwijderd. Het is daarom verstandig altijd eerst een reservekopie van de database te maken, voordat u de batchverwerking start.

De volgende tabel bevat de velden op het sneltabblad **Opties** die beschikbaar zijn voor alle batchtaken. De sectie **Te bewaren velden** bevat aanvullende velden die hierboven worden beschreven.

|Veld  |Omschrijving  |
|-------|-------------|
|Begindatum     |Voer de eerste datum in die in de datumcompressie moet worden opgenomen. De compressie betreft alle posten vanaf deze datum tot de einddatum.|
|Einddatum     |Voer de laatste datum in die in de datumcompressie moet worden opgenomen. De compressie betreft alle posten vanaf de begindatum tot deze datum.|
|Periodelengte |Selecteer de lengte van de periode waarvan posten worden gecombineerd. Kies het veld om de opties weer te geven. Als u de periodelengte *Kwartaal*, *Maand* of *Week* hebt geselecteerd, worden alleen posten met een gezamenlijke boekhoudperiode gecomprimeerd.|
|Te bewaren velden     |Plaats vinkjes in de vakjes als u de inhoud van bepaalde velden wilt bewaren, ook al worden de posten gecomprimeerd. Hoe meer velden u selecteert, des te nauwkeuriger zijn de gecomprimeerde posten. Als u geen van deze velden selecteert, wordt (afhankelijk van de periode die is geselecteerd in het veld **Periodelengte**) één post per dag, week enzovoort gemaakt. |

## <a name="see-also"></a>Zie ook

[Beheer](admin-setup-and-administration.md)  
