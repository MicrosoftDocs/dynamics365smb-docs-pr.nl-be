---
title: Artikelen picken met een voorraadpick
description: Als voor een vestiging wel een pickverwerking vereist is maar geen verzending, gebruikt u de voorraadpickdocumenten om pick- en verzendingsinformatie voor de brondocumenten te verzamelen en boeken.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8764fa82ef8bf408e85655b5a97719d9f649e7be
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078374"
---
# <a name="pick-items-with-inventory-picks"></a>Artikelen picken met een voorraadpick

Als voor uw vestiging wel een pickverwerking vereist is maar geen verzendingsverwerking, gebruikt u de pagina **Voorraadpick** om pick- en verzendingsinformatie voor de brondocumenten te verzamelen en boeken. Het uitgaande brondocument kan een verkooporder zijn, maar ook een inkoopretourorder, een uitgaande transferorder of een productieorder waarvan de onderdelen kunnen worden gepickt.

> [!NOTE]  
> Materialen voor assemblageorders kunnen niet worden gepickt of geboekt met voorraadpicks. Gebruik in plaats daarvan de pagina **Voorraadverplaatsing**. Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied bij standaard magazijnbeheer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)
>
> Als u verkoopregelaantallen pickt en verzendt die worden geassembleerd voor de order, moet u bepaalde regels volgen wanneer u de voorraadpickregels maakt. Zie de sectie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](#handling-assemble-to-order-items-with-inventory-picks) voor meer informatie.  

U kunt een voorraadpick op drie manieren maken:  

- Maak de pick in twee stappen door eerst een voorraadpick aan te vragen door het brondocument vrij te geven. Dit zorgt ervoor dat er een waarschuwing wordt gestuurd naar het magazijn dat het brondocument kan worden gepickt. De voorraadpick kan vervolgens worden gemaakt vanaf de pagina **Voorraadpick** op basis van het brondocument.  
- Maak de voorraadpick rechtstreeks vanuit het brondocument.  
- Gebruik de batchverwerking om voorraadpicks voor verschillende brondocumenten tegelijk te maken.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Een voorraadpick aanvragen door het brondocument vrij te geven

Voor verkooporders, inkoopretourorders en uitgaande transferorders maakt u het magazijnverzoek door de order vrij te geven. Hieronder wordt beschreven hoe u dit doet vanuit een verkooporder.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de verkooporder die u wilt vrijgeven en kies de actie **Vrijgeven**.

Voor productieorders maakt u automatisch het magazijnverzoek voor het picken (*afboeken*) van onderdelen wanneer de productieorderstatus is gewijzigd in **Vrijgegeven** of wanneer de vrijgegeven productieorder is gemaakt. Zie [Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md) voor meer informatie.

Wanneer het magazijnverzoek is gemaakt, ziet een magazijnmedewerker die verantwoordelijk is voor het picken van artikelen dat het brondocument gereed is voor de pick en kan hij/zij een nieuw document maken op basis van het magazijnverzoek.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Een voorraadpick maken op basis van het brondocument

Nu het verzoek is gemaakt, kan de magazijnmedewerker een nieuwe voorraadpick maken op basis van het vrijgegeven brondocument.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadpicks** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
    Zorg ervoor dat het veld **Nee.** op het sneltabblad **Algemeen** is ingevuld.
3. Selecteer in het veld **Brondocument** het soort brondocument waarvoor u pickt.  
4. Selecteer het brondocument in het veld **Bronnr.**  
5. U kunt ook de actie **Brondocument ophalen** kiezen om het document te selecteren in een lijst met uitgaande brondocumenten die gereed zijn voor picken op de locatie.  
6. Klik op de knop **OK** om de pickregels in te vullen op basis van het geselecteerde brondocument.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Een voorraadpick maken vanuit het brondocument

1. Klik in het brondocument, dat een verkooporder, inkoopretourorder, uitgaande transferorder of productieorder kan zijn, op de actie **Voorraadopslag/-pick maken**.
2. Schakel het selectievakje **Voorraadpick maken** in.  
3. Kies de knop **OK**. Er wordt een nieuwe voorraadpick gemaakt.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Meerdere voorraadpicks maken met een batchverwerking

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadopslag/-pick maken** in en kies vervolgens de gerelateerde koppeling.  
2. Gebruik op het sneltabblad **Magazijnverzoek** de velden **Brondocument** en **Bronnr.** om te filteren op bepaalde soorten documenten of reeksen documentnummers. U kunt bijvoorbeeld picks voor alleen de verkooporders maken.  
3. Schakel op het sneltabblad **Opties** het selectievakje **Voorraadpick maken** in.
4. Kies de knop **OK**. De opgegeven voorraadpicks worden gemaakt.

> [!NOTE]  
> Als u verkoopregelaantallen pickt en verzendt die worden geassembleerd voor de order moet u bepaalde regels volgen wanneer u de voorraadpickregels maakt. Zie de sectie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](#handling-assemble-to-order-items-with-inventory-picks) voor meer informatie.  
>
> Artikelen die in standaardmagazijnconfiguraties worden geassembleerd voor verkooporders worden gepickt uit de bijbehorende verkooporder, zoals beschreven in dit onderwerp. Zie de sectie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](#handling-assemble-to-order-items-with-inventory-picks) voor meer informatie.  

## <a name="to-record-the-inventory-picks"></a>De voorraadpicks registreren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadpick** in en kies vervolgens de gerelateerde koppeling.  
2. In het veld **Opslaglocatie** op de pickregels wordt op basis van de standaardopslaglocatie per artikel de opslaglocatie voorgesteld waaruit de artikelen moeten worden gepickt. De opslaglocatie op deze pagina kunt u desgewenst wijzigen.  
3. Voer de pick uit en voer het werkelijk opgeslagen aantal in het veld **Te verwerken aantal** in.

    Als het nodig is de artikelen voor een regel vanuit meerdere opslaglocaties te picken, bijvoorbeeld omdat ze niet beschikbaar zijn in de aangewezen opslaglocatie, gebruikt u de functie **Regel splitsen** op het sneltabblad **Regels**. Zie voor meer informatie over het splitsen van regels [Magazijnactiviteitsregels splitsen](warehouse-how-to-split-warehouse-activity-lines.md)  
4. Als u de pick hebt uitgevoerd, kiest u de actie **Boeken**.  

Het boekingsproces boekt de verzending van de brondocumentregels die zijn gepickt of, in het geval van productieorders, het boekingsproces boekt het verbruik. Als de vestiging opslaglocaties gebruikt, leidt de boeking er ook toe dat er magazijnposten worden gemaakt om de aantallen in de opslaglocatie te boeken.  

## <a name="to-delete-inventory-pick-lines"></a>Voorraadpickregels verwijderen

Als er geen items op de voorraadpick beschikbaar zijn, kunt u deze voorraadpickregels verwijderen nadat u ze hebt geboekt. Daarna kunt u het voorraadpickdocument verwijderen. Het brondocument, bijvoorbeeld een verkooporder of een productieorder, bevat artikelen die nog moeten worden gepickt, die later kunnen worden verkregen via een nieuwe voorraadpick wanneer de artikelen beschikbaar komen.  

> [!WARNING]  
> Dit proces is niet mogelijk als in het brondocument serie-/ lotnummers zijn opgegeven. Als bijvoorbeeld een verkooporderregel een serie-/lotnummer bevat, wordt de traceringsspecificatie van dat artikel verwijderd als een voorraadpickregel voor het serie-/lotnummer is verwijderd.  
>
> Als voorraadpickregels serie-/ lotnummers hebben die niet beschikbaar zijn, mag u de betreffende regels niet verwijderen. In plaats daarvan moet u het veld **Te verwerken aantal** wijzigen in nul, de werkelijke picks boeken en vervolgens het voorraadpickdocument verwijderen. Zo zorgt u ervoor dat de voorraadpickregels voor die serie-/lotnummers later opnieuw vanuit de verkooporder kunnen worden aangemaakt.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Op-order-assembleren-artikelen met voorraadpicks afhandelen

De pagina **Voorraadpick** wordt ook gebruikt voor het picken en verzenden voor verkoop waarbij artikelen moeten worden geassembleerd voordat ze verzonden kunnen worden. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).

Artikelen die verzonden moeten worden, zijn pas fysiek op een opslaglocatie aanwezig wanneer ze in het assemblagegebied worden geassembleerd en worden geboekt als uitvoer naar opslaglocatie. Dit betekent dat het picken van op-order-assembleren-artikelen voor verzending een bijzondere werkstroom volgt. Vanuit een opslaglocatie brengen magazijnmedewerkers de assemblageartikelen naar de verzenddock waar de voorraadpick wordt geboekt. Tijdens de geboekte voorraadpick worden de assemblageuitvoer, het materiaalverbruik en de verkoopverzending geboekt.

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] zo instellen dat automatisch een voorraadverplaatsing wordt gemaakt wanneer de voorraadpick voor het assemblageartikel wordt gemaakt. Als u dit wilt inschakelen, selecteert u het veld **Verplaatsingen automatisch aanmaken** op de pagina **Assemblage-instelling**. Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied bij standaard magazijnbeheer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Voorraadpickregels voor verkoopartikelen worden op verschillende manieren gemaakt, al naar gelang geen, enkele of alle verkoopregelaantallen op order zijn geassembleerd.

Bij een normale verkoop waarbij u voorraadpicks gebruikt om verzending van voorraadaantallen te boeken, wordt er één voorraadpickregel, of meerdere wanneer het artikel in verschillende opslaglocaties is geplaatst, gemaakt voor iedere verkooporderregel. Deze pickregel is gebaseerd op het aantal in het veld **Te verzenden aantal**.

Bij een op-order-assembleren-verkoop, waarbij het volledige aantal op de verkooporderregel op order wordt geassembleerd, wordt één voorraadpickregel voor dat aantal gemaakt. Dit betekent dat de waarde in het veld Te assembleren aantal overeenkomt met de waarde in het veld **Te verzenden aantal**. Het veld **Op order assembleren** wordt geselecteerd op de regel.

Als een assemblage-uitvoerstroom voor de locatie is ingesteld, wordt de waarde in het veld **Opslagloc. verz. asm.-op-order** of de waarde in het veld **Opslagloc.code Vanuit-assembl.**, in die volgorde, ingevoegd in het veld **Opslaglocatie** op de voorraadpickregel.

Als geen opslaglocatie op de verkooporderregel is opgegeven en assemblage-uitvoerstroom voor de locatie is ingesteld, is het veld **Opslaglocatie** op de voorraadpickregel leeg. De magazijnmedewerker moet de pagina **Opslaglocatie-inhoud** openen en de opslaglocatie selecteren waar de assemblageartikelen worden geassembleerd.

In combinatiescenario's waarbij een deel van de hoeveelheid eerst moet worden geassembleerd en een ander deel uit de voorraad moet worden gepickt, moeten minimaal twee voorraadpickregels worden gemaakt. Eén pickregel dient voor het op-order-assembleren-aantal. De andere pickregel is afhankelijk van welke opslaglocaties aan het resterend aantal in voorraad kunnen voldoen. Opslaglocatiescodes op de twee regels worden op verschillende manieren ingevuld, zoals voor de twee verschillende typen verkoop respectievelijk wordt beschreven. Zie voor meer informatie het gedeelte Combinatiescenario's in [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Procedure: picken en verzenden in standaardmagazijnconfiguraties](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]