---
title: Artikelen opslaan met een voorraadopslag
description: Ontdek hoe u documenten voor voorraadopslag kunt gebruiken om opslag- en ontvangstinformatie vast te leggen en te boeken.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '7375,'
---
# <a name="put-items-away-with-inventory-put-aways"></a><a name="put-items-away-with-inventory-put-aways"></a>Artikelen opslaan met voorraadopslag

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Inkomend proces|Ontvangst vereist|Opslag vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Ontvangst en opslag van de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken||Ingeschakeld|Basis: Order voor order|  
|H|Ontvangst en opslag van een magazijnontvangstdocument boeken|Ingeschakeld||Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Lees meer op [Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).

Dit artikel verwijst naar methode B in de tabel.

Wanneer uw vestiging zodanig is ingesteld dat magazijnopslagverwerking een vereiste is, maar ontvangstverwerking niet, gebruikt u het document **Voorraadopslag** om opslag- en ontvangstinformatie voor uw brondocumenten vast te leggen en te boeken. Inkomende brondocumenten kunnen inkooporders, verkoopretourorders en inkomende transferorders zijn.

> [!NOTE]
> Productie- en assemblageoutput vertegenwoordigen ook inkomende brondocumenten. Lees meer over het afhandelen van productie- en assemblage-output voor interne processen op [Ontwerpdetails: Interne magazijnstromen](design-details-internal-warehouse-flows.md).

U kunt een voorraadopslag op drie manieren maken:  

* Maak de voorraadopslag rechtstreeks vanuit het brondocument.  
* Gebruik de batchverwerking om de voorraadopslag voor verschillende brondocumenten tegelijk te maken.  
* Maak de opslag in twee stappen door eerst het brondocument vrij te geven om de artikelen beschikbaar te maken voor opslag. U kunt de voorraadopslag maken op basis van het brondocument via de pagina **Voorraadopslag**.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a><a name="to-create-an-inventory-put-away-from-the-source-document"></a>Een voorraadopslag maken op basis van het brondocument

1. Klik in het brondocument, dat een inkooporder, verkoopretourorder of inkomende transferorder kan zijn, op de actie **Voorraadopslag/-pick maken**.  
2. Schakel het selectievakje **Voorraadopslag/-pick maken** in.
3. Kies de knop **OK**. Er wordt een nieuwe voorraadopslag gemaakt.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a><a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Meerdere voorraadopslagactiviteiten maken met een batchverwerking

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadopslag/-pick-verplaatsing maken** in en kies de gerelateerde koppeling. 
2. Gebruik op het sneltabblad **Magazijnverzoek** de velden **Brondocument** en **Bronnr.** om te filteren op bepaalde soorten documenten of reeksen documentnummers. U kunt bijvoorbeeld opslag voor alleen de verkooporders maken.
3. Schakel op het sneltabblad **Opties** het selectievakje **Voorraadopslag maken** in.
4. Kies de knop **Ok**. De opgegeven voorraadopslagactiviteiten worden gemaakt.

## <a name="to-create-the-put-away-in-two-steps"></a><a name="to-create-the-put-away-in-two-steps"></a>De opslag in twee stappen maken

### <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a><a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Een voorraadopslag aanvragen door het brondocument vrij te geven

Wanneer u inkooporders, verkoopretourorders en inkomende transferorders vrijgeeft, komen de artikelen op de orders beschikbaar om te worden opgeslagen. In de volgende stappen wordt beschreven hoe u de artikelen op een inkooporder klaarmaakt om te worden opgeslagen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling
2. Selecteer de inkooporder die u wilt vrijgeven en kies de actie **Vrijgeven**.  

### <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a><a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Een voorraadopslag maken op basis van het brondocument

Een magazijnmedewerker kan op basis van het vrijgegeven brondocument een nieuwe voorraadopslag maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadopslag** in en selecteer vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer in het veld **Brondocument** het soort brondocument waarvoor u opslaat.  
4. Selecteer het brondocument in het veld **Bronnr.**  
5. U kunt ook de actie **Brondocument ophalen** kiezen om het document te selecteren in een lijst met inkomende brondocumenten die gereed zijn voor opslag op de locatie.  
6. Klik op de knop **OK** om de opslagregels in te vullen op basis van het geselecteerde brondocument.  

## <a name="to-record-the-inventory-put-away"></a><a name="to-record-the-inventory-put-away"></a>De voorraadopslag registreren

1. Open een eerder gemaakt opslagdocument op de pagina **Voorraadopslag**.  
2. In het veld **Opslaglocatie** op de opslagregels worden op basis van de standaardopslaglocatie per artikel de opslaglocaties voorgesteld waarin de artikelen moeten worden opgeslagen. U kunt de opslaglocatie indien nodig wijzigen.  
3. Voer de opslag uit en voer het werkelijk opgeslagen aantal in het veld **Te verwerken aantal** in.

    Als het nodig is de artikelen voor een regel in meerdere opslaglocaties te plaatsen, bijvoorbeeld omdat de aangewezen opslaglocatie vol is, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.  
4. Nadat u de artikelen hebt opgeslagen, kiest u de actie **Boeken**.  

    * De ontvangst boeken van de brondocumentregels die zijn opgeslagen
    * Als de vestiging opslaglocaties gebruikt, leidt de boeking er ook toe dat er magazijnposten worden gemaakt om de aantallen in de opslaglocatie te boeken.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/receive-put-away-items/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
