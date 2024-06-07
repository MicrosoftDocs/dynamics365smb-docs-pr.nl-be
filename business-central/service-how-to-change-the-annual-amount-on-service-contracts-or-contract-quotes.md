---
title: Het jaarlijkse bedrag van servicecontracten of servicecontractoffertes wijzigen
description: U kunt het bedrag wijzigen dat jaarlijks wordt gefactureerd in servicecontracten of servicecontractoffertes.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a>Het jaarlijkse bedrag van servicecontracten of servicecontractoffertes wijzigen
U kunt het jaarlijkse bedrag van het servicecontract of de servicecontractofferte wijzigen om het bedrag te corrigeren dat jaarlijks wordt gefactureerd.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a>Het jaarlijkse bedrag van het servicecontract of de servicecontractofferte wijzigen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontracten** of **Servicecontractoffertes** in het tekstvak in en kies vervolgens de gerelateerde koppeling.  
2. Kies het contract of de contractofferte.  
3. Kies de actie **Contract openen** om het contract of de contractofferte te openen en bewerken.  
4. Schakel het selectievakje **Bedragen in onbalans toestaan** in als u het jaarlijkse bedrag wilt wijzigen en het verschil in het jaarlijkse bedrag handmatig wilt verdelen over de contractregels. Schakel anders het selectievakje uit om het verschil in het jaarlijkse bedrag automatisch te verdelen over de contractregels nadat u het jaarlijkse bedrag hebt gewijzigd.  
5. Wijzig de inhoud van het veld **Jaarlijks bedrag**. Als het jaarlijkse bedrag negatief is, kunt u het servicecontract niet ondertekenen (omzetten in een servicecontract als u aan een contractofferte werkt) of vergrendelen. Als u het jaarlijkse bedrag instelt op nul, moet de inhoud van het veld **Factuurperiode** **Geen** zijn als u het servicecontract ondertekent of vergrendelt.  
6. Afhankelijk van of het selectievakje **Bedragen in onbalans toestaan** is ingeschakeld, voert u de handmatige of automatische verdeling van het verschil in het jaarlijkse bedrag uit. De contractregels worden zodanig bijgewerkt dat de waarde in het veld **Berekend jaarlijks bedrag** gelijk is aan het nieuwe jaarlijkse bedrag.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts"></a>Verschillen tussen nieuwe en berekende jaarlijks bedragen verdelen
Als u het jaarlijkse bedrag van een servicecontract of contractofferte wijzigt, moet u mogelijk het verschil tussen het nieuwe en berekende jaarlijkse bedrag verdelen over de contractregels. Er zijn drie methoden om bedragen verdelen:

* Gelijke verdeling  
* Verdeling op basis van regelbedragen  
* Verdeling op basis van winst

### <a name="even-distribution"></a>Gelijke verdeling
Als u het jaarlijkse bedrag wijzigt van een servicecontract of contractofferte, moet u mogelijk het verschil tussen het nieuwe en het berekende jaarlijkse bedrag verdelen over de contractregels. Gelijke verdeling is een van de automatische verdeelmethodes waarmee u het verschil tussen het nieuwe en het berekende jaarlijkse bedrag gelijk kunt verdelen over de regelbedragen op de contractregels. Het idee achter deze verdeelmethode wordt beschreven in de volgende procedure:  

1. Het verschil tussen de nieuwe waarde in het veld **Jaarlijks bedrag** en de waarde in het veld **Berekend jaarlijks bedrag** wordt gedeeld door het aantal contractregels in het servicecontract of de servicecontractofferte.  
2. De waarde van het veld **Regelbedrag** wordt bijgewerkt door er het resultaat van de voorgaande bewerking bij op te tellen.  
3. De inhoud van de velden **Bedrag Regelkorting**, **Regelkorting %** en **Winst** worden bijgewerkt op basis van de nieuwe waarde in het veld **Bedrag Regel**. Dit gebeurt op de volgende manier:   
    * Totale regelkorting = Regelwaarde - Regelbedrag.  
    * Regelkorting % = Totale regelkorting / Regelwaarde * 100.  
    * Winst = Regelbedrag - Regelkostprijs.  

 De stappen worden herhaald voor elke contractregel.  

#### <a name="example"></a>Opmerking
Het selectievakje **Bedragen in onbalans toestaan** is niet ingeschakeld op het servicecontract, dat drie contractregels bevat met dergelijke informatie.  

|Artikel|Regelkostprijs|Regelwaarde|Regelkorting %|Totale regelkorting|Regelbedrag|Winst|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|30,00|40,00|  0.00|  0.00|40,00|10.00|  
|Artikel 2|40,00|50.00|10.00|5.00|45.00|5.00|  
|Artikel 3|50.00|70.00|10.00|7.00|63.00|13.00|  

De waarde in het veld **Jaarlijks bedrag** is gelijk aan de inhoud van het veld **Berekend jaarlijks bedrag**, dat altijd is ingesteld op het totaal van de regelbedragen. In dit geval is de waarde gelijk aan: 40 + 45 + 63 = 148.  

Als u het **Jaarlijkse bedrag** wijzigt in 139, wordt het bedrag berekend dat moet worden toegevoegd aan elke waarde in het veld **Regelbedrag**. Dit bedrag wordt berekend door het **Berekend jaarlijkse bedrag** af te trekken van de nieuwe waarde in het veld **Jaarlijks bedrag** en het resultaat te delen door het aantal contractregels in het servicecontract. In dit geval is de waarde gelijk aan: (139 + 148) / 3 = -3. Vervolgens wordt dit bedrag opgeteld bij de waarde in elke waarde in het veld **Regelbedrag** en worden de waarden in de velden **Regelkorting %**, **Totale regelkorting** en **Winst** bijgewerkt met behulp van de formules die hierboven zijn beschreven.  

Uiteindelijk bevatten de contractregels de volgende gegevens.  

|Artikel|Regelkostprijs|Regelwaarde|Regelkorting %|Totale regelkorting|Regelbedrag|Winst|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|30,00|40,00|7.50|3.00|37.00|7.00|  
|Artikel 2|40,00|50.00|16.00|8.00|42.00|2.00|  
|Artikel 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount"></a>Verdeling op basis van regelbedrag
Als u het jaarlijkse bedrag van een servicecontract of contractofferte wijzigt, moet u mogelijk het verschil tussen het nieuwe en berekende jaarlijkse bedrag verdelen over de contractregels. Verdeling op basis van regelbedrag is een automatische methode waarmee u het verschil tussen het nieuwe en het berekende jaarlijkse bedrag kunt verdelen tussen de regelbedragen op de contractregels. Het verschil wordt proportioneel verdeeld op basis van het aandeel van het regelbedrag in het berekende jaarlijkse bedrag. Hieronder volgt een uitleg van de verdeelprocedure per contractregel:  

1. De procentuele bijdrage van het regelbedrag wordt als volgt berekend: de inhoud van het veld **Regelbedrag** wordt gedeeld door de waarde in het veld **Berekend jaarlijks bedrag** op alle contractregels.  
2. De waarde van het veld **Regelbedrag** wordt berekend door het verschil tussen het nieuwe en het berekende jaarlijkse bedrag erbij op te tellen, nadat dat is vermenigvuldigd met de procentuele bijdrage in het regelbedrag.  
3. De inhoud van de velden **Totale regelkorting**, **Regelkorting %** en **Winst** wordt bijgewerkt op basis van de nieuwe waarde in het veld **Totale regelkorting**. Dit gebeurt op de volgende manier:  

    * Totale regelkorting = Regelwaarde - Regelbedrag.  
    * Regelkorting % = Totale regelkorting / Regelwaarde * 100  
    * Winst = Regelbedrag - Regelkostprijs  

De stappen worden herhaald voor elke contractregel.  

#### <a name="example-1"></a>Opmerking
Het selectievakje **Bedragen in onbalans toestaan** is niet ingeschakeld op het servicecontract, dat drie contractregels bevat met dergelijke informatie.  

|Artikel|Regelkostprijs|Regelwaarde|Regelkorting %|Totale regelkorting|Regelbedrag|Winst|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15.00|17.00|3.00|0.51|25.00|1.49|  
|Artikel 2|20.00|23.00|Geen|  0.00|55.10|3.00|  
|Artikel 3|24.00|27.00|3.00|0.81|112.70|2.19|  

De waarde in het veld **Jaarlijks bedrag** is gelijk aan de inhoud van het veld **Berekend jaarlijks bedrag**, dat altijd is ingesteld op het totaal van de regelbedragen. In dit geval is de waarde gelijk aan: 16,49 + 23,00 + 26,19 = 65,68.  

Als u het **Jaarlijks bedrag** verandert in 60, wordt de winstpercentagebijdrage voor elke contractregel berekend:  

* Artikel 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Artikel 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Artikel 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557  

De waarde van het veld **Regelbedrag** wordt op elke contractregel bijgewerkt met de formule: Regelbedrag = Regelbedrag + verschil tussen het nieuwe en het berekende jaarlijkse bedrag * Bijdrage in percentage. Vervolgens wordt de waarde in de velden **Totale regelkorting**, **Regelkorting %** en **Winst** bijgewerkt met de formules uit de hierboven beschreven procedure.  

Uiteindelijk bevatten de contractregels de volgende gegevens.  

|Artikel|Regelkostprijs|Regelwaarde|Regelkorting %|Totale regelkorting|Regelbedrag|Winst|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15.00|17.00|11.41|1.94|15.06|0.06|  
|Artikel 2|20.00|23.00|8.65|1.99|21.01|1.01|  
|Artikel 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### <a name="distribution-based-on-profit"></a>Verdeling op basis van winst
Als u het jaarlijkse bedrag van een servicecontract of contractofferte wijzigt, moet u mogelijk het verschil tussen het nieuwe en berekende jaarlijkse bedrag verdelen over de contractregels. Verdeling op basis van winst is een van de automatische methodes waarmee u het verschil tussen het nieuwe en het berekende jaarlijkse bedrag kunt verdelen over de regelbedragen op de contractregels. Het verschil wordt proportioneel verdeeld op basis van het winstaandeel in de totale winst op het contract of de contractofferte. Hieronder volgt een uitleg van de verdeelprocedure per contractregel:  

1. De procentuele bijdrage aan de winst wordt als volgt berekend: de inhoud van het veld **Winst** wordt gedeeld door de som van de waarden in het veld **Winst** op alle contractregels.  
2. De waarde van het veld **Regelbedrag** wordt berekend door het verschil tussen het nieuwe en het berekende jaarlijkse bedrag erbij op te tellen, nadat dat is vermenigvuldigd met de procentuele bijdrage aan de winst.  
3. De inhoud van de velden Bedrag Regelkorting, Regelkorting % en Winst worden bijgewerkt op basis van de nieuwe waarde in het veld **Bedrag Regel**. Dit gebeurt op de volgende manier:  

    * Totale regelkorting = Regelwaarde - Regelbedrag.  
    * Regelkorting % = Totale regelkorting / Regelwaarde * 100  
    * Winst = Regelbedrag - Regelkostprijs  

#### <a name="example-2"></a>Opmerking
Het selectievakje **Bedragen in onbalans toestaan** is niet ingeschakeld in het servicecontract, dat drie contractregels bevat met dergelijke informatie.  

|Artikel|Regelkostprijs|Regelwaarde|Regelkorting %|Totale regelkorting|Regelbedrag|Winst|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|20.00|25.00|  0.00|  0.00|25.00|5.00|  
|Artikel 2|50.00|58.00|5.00|2.90|55.10|5.10|  
|Artikel 3|100.00|115.00|2.00|2.30|112.70|12.70|  

De waarde in het veld **Jaarlijks bedrag** is gelijk aan de inhoud van het veld **Berekend jaarlijks bedrag**, dat altijd is ingesteld op het totaal van de regelbedragen. In dit geval is de waarde gelijk aan: 25,00 + 55,10 + 112,70 = 192,80.  

 Als u het **Jaarlijks bedrag** verandert in 180, wordt de winstpercentagebijdrage voor elke contractregel berekend:  

* Artikel 1 – 5 / (5 + 5,1 +1 2,7) = 0,2193 %  
* Artikel 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Artikel 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557  

De waarde van het veld **Regelbedrag** wordt op elke contractregel bijgewerkt met de formule: Regelbedrag = Regelbedrag + verschil tussen het nieuwe en het berekende jaarlijkse bedrag * Bijdrage in percentage. Vervolgens wordt de waarde in de velden **Totale regelkorting**, **Regelkorting %** en **Winst** bijgewerkt met de formules uit stap 3 van de hierboven beschreven procedure.  

Uiteindelijk bevatten de contractregels de volgende gegevens.  

|Artikel|Regelkostprijs|Regelwaarde|Regelkorting %|Totale regelkorting|Regelbedrag|Winst|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|20.00|25.00|11.24|2.81|22.19|2.19|  
|Artikel 2|50.00|58.00|9.93|5.76|52.24|2.24|  
|Artikel 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also"></a>Zie ook
[Servicecontractoffertes en servicecontracten maken](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[CRM - Service instellen](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
