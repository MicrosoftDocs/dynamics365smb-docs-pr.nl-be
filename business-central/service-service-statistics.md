---
title: Servicestatistieken
description: 'Krijg een snel overzicht van de inhoud en statistieken van servicedocumenten, zoals orders, offertes, facturen of creditnota''s, serviceregels en meer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---

# <a name="viewing-service-statistics"></a><a name="viewing-service-statistics"></a><a name="viewing-service-statistics"></a>Servicestatistieken weergeven
U kunt statistische gegevens gebruiken om servicedocumenten te analyseren en te bepalen hoe goed u uw serviceprocessen beheert. U kunt servicecontracten, artikelen, offertes, orders, facturen en creditnota's analyseren door de actie **Statistieken** te kiezen. Voor serviceartikelen en contracten kunt u ook **Serviceartikel Trendscape** of **Contract Trendscape** gebruiken om een overzicht van serviceposten voor een bepaald serviceartikel te bekijken.   

## <a name="viewing-statistics-for-service-orders"></a><a name="viewing-statistics-for-service-orders"></a><a name="viewing-statistics-for-service-orders"></a>Statistieken voor serviceorders weergeven
De functie serviceorderstatistiek biedt u een overzicht van de inhoud van de volledige serviceorder, de details op de serviceregels en gegevens met betrekking tot facturering, verzending en verbruik, evenals het saldo van de klant.  

De statistiekgegevens voor een serviceorder worden weergegeven op de pagina **Serviceorderstatistiek** voor de desbetreffende order. U kunt de desbetreffende pagina openen vanuit een serviceorder. Kies **Statistieken** op de pagina **Serviceorders**. Op de sneltabbladen op de pagina worden gegevens als aantal, bedrag, btw, kosten, winst en de kredietlimiet van de klant weergegeven. De bedragen op de pagina zijn gesteld in de valuta van de serviceorder, tenzij anders aangegeven.  

### <a name="view-totals-for-a-service-order"></a><a name="view-totals-for-a-service-order"></a><a name="view-totals-for-a-service-order"></a>Totalen voor een serviceorder weergeven
U kunt het totaalbedrag op de serviceregels (inclusief en exclusief btw), het btw-gedeelte, de kosten en de winst op de serviceregels weergeven. Daarnaast wordt er artikelspecifieke informatie weergegeven, zoals het gewicht, het volume en het aantal colli.  

### <a name="view-shipping-information"></a><a name="view-shipping-information"></a><a name="view-shipping-information"></a>Verzendgegevens weergeven
U kunt informatie weergeven over de te verzenden artikelen, resources of kosten. Voor deze informatie worden de waarden gebruikt die zijn opgegeven in het veld **Te verzenden aantal** van elke serviceregel in de order.  

### <a name="view-order-details"></a><a name="view-order-details"></a><a name="view-order-details"></a>Ordergegevens weergeven
U kunt informatie weergeven over de artikelen, resource-uren en kosten die moeten worden gefactureerd en verbruikt. In de volgende tabel worden deze gegevens beschreven.  

|Kolom | Omschrijving|  
|------------|---------------------------------------|  
|**Facturering**|Bevat bedragen die moeten worden geboekt als gefactureerd vanuit de serviceorder.|  
|**Verbruik**|Bevat de hoeveelheid en de kosten van artikelen, of de resources die worden geboekt als verbruikt.|  
|**Totaal**|Hier worden de totaalbedragen voor de serviceorder weergegeven, die worden berekend door de factureringsbedragen op te tellen bij de verbruiksbedragen.|  

### <a name="analyze-service-order-lines"></a><a name="analyze-service-order-lines"></a><a name="analyze-service-order-lines"></a>Serviceorderregels analyseren
U kunt de gegevens analyseren op basis van de soorten serviceregels die zijn opgenomen in de serviceorder. De bedragen worden afzonderlijk weergegeven voor:  

* Artikelen  
* Resources  
* Kosten en grootboekrekeningen  

### <a name="view-customer-information"></a><a name="view-customer-information"></a><a name="view-customer-information"></a>Klantgegevens weergeven
Bekijk het saldo van de klantenrekening en het maximale krediet dat kan worden verleend aan de klant voor wie u het servicedocument hebt opgesteld.

## <a name="viewing-service-item-statistics"></a><a name="viewing-service-item-statistics"></a><a name="viewing-service-item-statistics"></a>Serviceartikelstatistieken weergeven
Op de pagina **Serviceartikelstatistiek** kunt u bijgewerkte gegevens over een serviceartikel bekijken op basis van de volgende serviceboekingssoorten:  

* Resources  
* Artikelen  
* Servicekosten  
* Servicecontracten  
* Totaal  

Voor elk boekingssoort kunt u het gefactureerde bedrag, het verbruik (bedrag), de kosten, het aantal, het gefactureerde en het verbruikte aantal, het winstbedrag en -percentage bekijken. Het winstpercentage wordt berekend volgens de volgende formule:  

* (Gefactureerd bedrag - Gebruik (Kosten)) x 100 / Gefactureerd bedrag  

## <a name="use-trendscapes"></a><a name="use-trendscapes"></a><a name="use-trendscapes"></a>Trendscapes gebruiken
Voor serviceartikelen en servicecontracten biedt de pagina **Serviceartikel Trendscape** of **Contract Trendscape** een overzicht van serviceposten gedurende een periode voor een bepaald serviceartikel of contract. U kunt de trendscape weergeven door het serviceartikel of contract te openen, de actie **Statistieken** te kiezen en vervolgens **Trendscape** te kiezen.

Wanneer u de lijst doorloopt, worden de bedragen berekend op basis van het opgegeven tijdsinterval en weergegeven in de lokale valuta. De bedragen worden berekend op basis van serviceposten. Dit zijn de posten die worden gemaakt wanneer u serviceorders of servicefacturen boekt.

U kunt de lijst filteren door op te geven welke serviceartikelen moeten worden opgenomen.  

> [!Tip]  
>  Als u **Dag** hebt gekozen als tijdsinterval en een lange periode moet doorlopen, kunt u dat sneller doen door een groter interval te kiezen, bijvoorbeeld **Kwartaal**. Zodra u de gewenste periode hebt gevonden, kunt u teruggaan naar het originele interval om de gegevens gedetailleerder te bekijken.   

## <a name="viewing-gains-and-losses-on-contracts"></a><a name="viewing-gains-and-losses-on-contracts"></a><a name="viewing-gains-and-losses-on-contracts"></a>Winsten en verliezen op contracten weergeven
Een vermelding van contractwinst of -verlies wordt gegenereerd wanneer een contractofferte wordt omgezet in een servicecontract, als contractregels worden toegevoegd of verwijderd uit een servicecontract of wanneer een contract wordt geannuleerd. U kunt contractwinsten of -verliezen bekijken op de volgende pagina's.  

|Pagina | Omschrijving|  
|----------------|---------------------------------------|  
|**Winst/verlies contract (Contract)**|Het winst-/verliescontract per servicecontract weergeven.|  
|**Winst/verlies contract (Groep)**|Het winst-/verliescontract per servicecontractgroep weergeven.|  
|**Winst/verlies contract (Klant)**|Het winst-/verliescontract per klant weergeven.|  
|**Winst/verlies contract (Reden)**|Het winst-/verliescontract per redencode weergeven.|  
|**Winst/verlies contract (Divisie)**|Het winst-/verliescontract per divisie weergeven.|  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer de naam in van de pagina die u wilt weergeven en kies vervolgens de gerelateerde koppeling.  
2. Vul de filtercriteria in die u wilt toepassen. Kies bijvoorbeeld op de pagina **Winst/verlies contract (Reden)** een waarde voor **Redencodefilter**.  
3. Kies de actie **Matrix weergeven**.

## <a name="viewing-statistics-for-posted-service-documents"></a><a name="viewing-statistics-for-posted-service-documents"></a><a name="viewing-statistics-for-posted-service-documents"></a>Statistieken voor geboekte servicedocumenten weergeven
Met de functie voor servicestatistieken kunt u een statistisch overzicht opstellen van de inhoud van geboekte servicedocumenten, zoals geboekte verzendingen, facturen en creditnota's.  

De statistische informatie wordt weergegeven op de statistiekpagina voor het bijbehorende geboekte servicedocument. U kunt de desbetreffende statistiekpagina openen vanuit een geboekte serviceverzending, geboekte servicefactuur of geboekte servicecreditnota. Kies voor elk van deze documenttypen de actie **Statistieken**. Kies bijvoorbeeld op de pagina **Geboekte servicefacturen** de actie **Statistieken**.  

### <a name="posted-service-shipment-statistics"></a><a name="posted-service-shipment-statistics"></a><a name="posted-service-shipment-statistics"></a>Statistiek geboekte serviceverzendingen
Op de pagina **Statistiek serviceverzendingen** wordt een overzicht gegeven van een geboekte serviceverzending. Het venster bevat informatie over de fysieke inhoud van de verzending, zoals het aantal verzonden artikelen, resource-uren of -kosten, en gewicht en volume van de verzonden artikelen.  

### <a name="posted-service-invoice-statistics"></a><a name="posted-service-invoice-statistics"></a><a name="posted-service-invoice-statistics"></a>Statistiek geboekte servicefacturen
Op de pagina **Statistiek servicefacturen** wordt een statistisch overzicht gegeven van een geboekte servicefactuur. U kunt de totalen van de geboekte servicefactuur bekijken. U vindt hier onder andere het totaalbedrag op de serviceregels (inclusief en exclusief btw) dat als gefactureerd is geboekt, het btw-gedeelte, de kosten en de winst op de geboekte factuur. Daarnaast bevat de pagina informatie over het volgende:  

* De artikelen op de servicefactuurregels, zoals gewicht, volume en het aantal colli.  
* Het saldo op de rekening van de klant en het maximumkrediet dat u de klant kunt verlenen.  

### <a name="posted-service-credit-memo-statistics"></a><a name="posted-service-credit-memo-statistics"></a><a name="posted-service-credit-memo-statistics"></a>Statistiek Geboekte servicecreditnota
De pagina **Statistiek servicecreditnota's** biedt een statistisch overzicht van de regels in een geboekte servicecreditnota. Het overzicht kan het volgende bevatten:

* De totale bedragen op de geboekte creditnota, weergegeven als het aantal, het bedrag, de btw, de kosten en de winst. Daarnaast vindt u hier informatie over de artikelen op de serviceregels van de geboekte creditnota, zoals aantal, gewicht en volume.  
* Algemene informatie over de klant, zoals de kredietlimiet van de klant en het rekeningsaldo.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook
[Serviceorders maken](service-how-to-create-service-orders.md)   
[Serviceartikelen maken](service-how-to-create-service-items.md)   
[Service plannen](service-plan-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
