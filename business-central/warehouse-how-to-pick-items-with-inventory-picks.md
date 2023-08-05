---
title: Artikelen picken met een voorraadpick
description: Ontdek hoe u voorraadpicks kunt gebruiken om pick- en verzendinformatie voor brondocumenten vast te leggen en te boeken.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# Artikelen picken met een voorraadpick

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Uitgaand proces|Pick vereist|Verzending vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Picken en verzending vanaf de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Picken en verzending vanuit een voorraadpickdocument boeken|Ingeschakeld||Basis: Order voor order|  
|H|Picken en verzending vanuit een magazijnverzendingdocument boeken||Ingeschakeld|Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Picken vanuit een magazijnpickdocument boeken en verzending vanuit een magazijnverzendingdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Zie voor meer informatie [Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md).

Dit artikel verwijst naar methode B in de tabel.

Als voor uw vestiging wel een pickverwerking vereist is maar geen verzendingsverwerking, gebruikt u de pagina **Voorraadpick** om pick- en verzendingsinformatie voor de brondocumenten te verzamelen en boeken. Uitgaande brondocumenten kunnen verkooporders, inkoopretourorders en uitgaande transferorders zijn.

> [!NOTE]
> Productie- en assemblageorders met materiaalbehoeften vertegenwoordigen ook uitgaande brondocumenten. Lees meer over het afhandelen van productie- en assemblageorders voor interne processen op [Ontwerpdetails: Interne magazijnstromen](design-details-internal-warehouse-flows.md).
>
> Hoewel serviceorders ook uitgaande brondocumenten zijn, ondersteunen ze niet het basisniveau van complexiteit per order.
>
> Als u verkoopregelaantallen pickt en verzendt die worden geassembleerd voor de order, moet u bepaalde regels volgen wanneer u de voorraadpickregels maakt. Zie voor meer informatie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](#handling-assemble-to-order-items-with-inventory-picks).  

U kunt een voorraadpick op drie manieren maken:

* Maak de voorraadpick rechtstreeks vanuit het brondocument.  
* Maak voorraadpicks voor meerdere brondocumenten tegelijk met behulp van een batchproject.
* Vraag de pick in twee stappen aan door eerst het brondocument vrij te geven, dat als signaal voor het magazijn fungeert dat het brondocument gereed is voor picking.

De voorraadpick kan vervolgens worden gemaakt vanaf de pagina **Voorraadpick** op basis van het brondocument.  

## Een voorraadpick maken vanuit het brondocument

1. Klik in het brondocument, dat een verkooporder, inkoopretourorder of uitgaande transferorder kan zijn, op de actie **Voorraadopslag/-pick maken**.
2. Schakel het selectievakje **Voorraadpick maken** in.  
3. Kies de knop **OK**. Er wordt een nieuwe voorraadpick gemaakt.

## Meerdere voorraadpicks maken met een batchverwerking

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadopslag/-pick-verplaatsing maken** in en kies de gerelateerde koppeling.  
2. Gebruik op het sneltabblad **Magazijnverzoek** de velden **Brondocument** en **Bronnr.** om te filteren op bepaalde soorten documenten of reeksen documentnummers. U kunt bijvoorbeeld picks voor alleen de verkooporders maken.  
3. Schakel op het sneltabblad **Opties** het selectievakje **Voorraadpick maken** in.
4. Kies de knop **Ok**.

## De pick in twee stappen maken

### Een voorraadpick aanvragen door het brondocument vrij te geven

Voor verkooporders, inkoopretourorders en uitgaande transferorders maakt u het magazijnverzoek door de order vrij te geven. Door de order vrij te geven, zijn de artikelen beschikbaar voor picken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de verkooporder die u wilt vrijgeven en kies de actie **Vrijgeven**.

### Een voorraadpick maken op basis van het brondocument

Nadat u een order hebt vrijgegeven, kan de magazijnmedewerker een voorraadpick maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadpicks** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer in het veld **Brondocument** het soort document waarvoor u pickt.  
4. Selecteer het brondocument in het veld **Bronnr.**  
5. U kunt ook de actie **Brondocument ophalen** kiezen om alle uitgaande brondocumenten te selecteren die gereed zijn voor picken op de vestiging.  
6. Kies de knop **OK** om de pickregels in te vullen op basis van de geselecteerde brondocumenten.  

## Voorraadpicks registreren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadpick** in en kies vervolgens de gerelateerde koppeling.  
2. In het veld **Opslaglocatie** op de pickregels wordt op basis van de standaardopslaglocatie per artikel de opslaglocatie voorgesteld waaruit de artikelen moeten worden gepickt. De opslaglocatie op deze pagina kunt u desgewenst wijzigen.  
3. Voer de pick uit en voer het aantal in het veld **Te verwerken aantal** in.

    Als het nodig is de artikelen voor een regel uit meerdere opslaglocaties te picken, bijvoorbeeld omdat een opslaglocatie niet de volledige hoeveelheid bevat, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.

4. Kies de actie **Boeken**.  

    * Boek de verzending van de brondocumentregels die zijn gepickt.
    * Als de vestiging opslaglocaties gebruikt, leidt de boeking er ook toe dat er magazijnposten worden gemaakt om de wijziging in de aantallen in de opslaglocatie te boeken.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Op-order-assembleren-artikelen met voorraadpicks afhandelen

U kunt ook de pagina **Voorraadpick** gebruiken voor het picken en verzenden voor verkoop waarbij artikelen moeten worden geassembleerd voordat ze verzonden kunnen worden. Zie voor meer informatie [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)

Op order assembleren-artikelen zijn pas fysiek op een opslaglocatie aanwezig wanneer ze zijn geassembleerd en geboekt als output naar een opslaglocatie. Picken van op-order-assembleren-artikelen uit een opslaglocatie voor verzending volgt een bijzondere stroom.

1. Vanuit een opslaglocatie brengen magazijnmedewerkers de assemblageartikelen naar de verzenddock waar de voorraadpick wordt geboekt.
2. De geboekte voorraadpick boekt de assemblyuitvoer, het materiaalverbruik en de verkoopverzending.

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] zo instellen dat automatisch een voorraadverplaatsing wordt gemaakt wanneer de voorraadpick voor het assemblageartikel wordt gemaakt. Selecteer het veld **Verplaatsingen automatisch aanmaken** op de pagina **Assemblage-instelling**. Zie voor meer informatie [Standaardmagazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Voorraadpickregels voor verkoopartikelen worden op verschillende manieren gemaakt, al naar gelang geen, enkele of alle verkoopregelaantallen op order zijn geassembleerd. In scenario's waarbij een deel van de hoeveelheid wordt geassembleerd en een ander deel uit de voorraad wordt gepickt, moeten minimaal twee pickregels worden gemaakt.

Bij een verkoop waarbij het volledige aantal op de verkooporderregel op order wordt geassembleerd, wordt één voorraadpickregel voor het aantal gemaakt. De waarde in het veld **Te assembleren aantal** is hetzelfde als de waarde in het veld **Te verzenden aantal**. Het veld **Op order assembleren** wordt geselecteerd op de regel.

Als een assemblyuitvoerstroom voor de vestiging is ingesteld, bevat het veld **Opslaglocatie** op de voorraadpickregel de waarde uit de volgende velden, in onderstaande volgorde.

* ***Opslagloc. verz. asm.-op-order** <!-- not applicable for inv pick-->
* **Opslagloc.code Vanuit-assembl.**

Als geen opslaglocatie op de verkooporderregel is opgegeven en assemblyuitvoerstroom voor de vestiging is ingesteld, is het veld **Opslaglocatie** op de voorraadpickregel leeg. De magazijnmedewerker moet de pagina **Opslaglocatie-inhoud** openen en de opslaglocatie selecteren waar de assemblageartikelen worden geassembleerd.

In scenario's waarbij een deel van de hoeveelheid wordt geassembleerd en een ander deel wordt gepickt, moeten minimaal twee pickregels worden gemaakt.

* Eén pickregel dient voor het op-order-assembleren-aantal. [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt de volgende velden, in deze volgorde, om de opslaglocatie te bepalen: **Opslaglocatie**, **Opslagloc. verz. asm.-op-order** en tot slot **Opslagloc.code Vanuit-assembl.**. Als deze velden leeg azijn, moet de magazijnmedewerker de pagina **Opslaglocatie-inhoud** openen en de opslaglocatie kiezen waar de artikelen worden geassembleerd.  
* De andere pickregel is afhankelijk van welke opslaglocaties aan het resterend aantal kunnen voldoen. Als het artikel in meerdere opslaglocaties wordt bewaard, worden er meerdere regels gemaakt. De 'Nemen'-regel is gebaseerd op het aantal in het veld **Te verzenden aantal**.

> [!NOTE]  
> Als artikelen op bestelling worden geassembleerd, maakt de voorraadpick voor de gekoppelde verkooporder een voorraadverplaatsing voor alle assemblagematerialen.  

## Zie gerelateerde [Microsoft-training](/training/paths/pick-ship-items-business-central/)

## Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Procedure: picken en verzenden in standaardmagazijnconfiguraties](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
