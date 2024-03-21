---
title: Voorraad tellen en corrigeren
description: Beschrijft hoe u fysieke voorraad telt en voorraaddocumenten gebruikt om voorhanden voorraad aan te passen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="count-and-adjust-inventory-using-documents"></a>Voorraad tellen en aanpassen met documenten

U kunt een inventarisatie van uw artikelen maken met behulp van inventarisatieorder- en inventarisatieregistratiedocumenten. De pagina **Inventarisatieorder** wordt gebruikt om het hele inventarisatieproject te organiseren, bijvoorbeeld één per vestiging. De pagina **Inventarisatieregistratie** wordt gebruikt om de werkelijke telling van artikelen te communiceren en vast te leggen. U kunt meerdere registraties voor één order maken, bijvoorbeeld om groepen artikelen naar verschillende werknemers te distribueren.

Het rapport **Inventarisatieregistratie** kan worden afgedrukt vanuit elke registratie en bevat lege aantalvelden voor het invoeren van de getelde voorraad. Wanneer een gebruiker klaar is met tellen en de aantallen worden ingevoerd op de pagina **Inventarisatieregistratie**, kiest u de actie **Voltooien**. Hierdoor worden de aantallen overgebracht naar de gerelateerde regels op de pagina **Inventarisatieorder**. Functionaliteit zorgt dat een artikeltelling niet tweemaal kan worden geregistreerd.  

> [!NOTE]
> Documenten gebruiken om een inventarisatie uit te voeren biedt meer controle en ondersteunt distributie van de telling naar meerdere werknemers. U kunt de taak ook uitvoeren met dagboeken, zoals de pagina's **Inventarisatiedagboeken** en **Mag.-inventarisatiedagboeken**. Zie voor meer informatie [Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md) In dit artikel wordt beschreven hoe u een fysieke inventarisatie uitvoert met behulp van documenten.
>
> Als u zones gebruikt, kunt u geen fysieke voorraadorders gebruiken. Gebruik in plaats daarvan de pagina **Mag.-inventarisatiedagboek** om uw magazijnposten te tellen voordat u deze synchroniseert met artikelposten.

Inventariseren met behulp van documenten bestaat uit de volgende algemene stappen:

1. Een inventarisatieorder maken met verwachte artikelaantallen vooraf ingevuld.
2. Een of meer inventarisatieregistraties genereren vanuit de order.
3. De getelde artikelaantallen invoeren in de registraties, zoals bijvoorbeeld vastgelegd op afdrukken, en dit instellen op **Gereedgemeld**.
4. De inventarisatieorder voltooien en boeken.

## <a name="to-create-a-physical-inventory-order"></a>Een inventarisatieorder maken

Een inventarisatieorder is een volledig document dat bestaat uit een inventarisatieorderkop en enkele inventarisatieorderregels. De informatie in een inventarisatiekop beschrijft hoe de inventarisatie wordt uitgevoerd. De inventarisatieorderregels bevatten de informatie over de artikelen en de vestigingen ervan.

Als u de inventarisatieorderregels wilt maken, gebruikt u meestal de functie **Regels berekenen** om de huidige voorraad als regels in de order te krijgen. U kunt ook de functie **Kopiëren uit document** gebruiken om de regels te vullen met de inhoud van een andere open of geboekte inventarisatieorder. In de volgende procedure wordt beschreven hoe u de functie **Regels berekenen** gebruikt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inventarisatieorders boeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul de vereiste velden op het sneltabblad **Algemeen** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de actie **Regels berekenen**.
5. Selecteer de benodigde opties.
6. Stel filters in, bijvoorbeeld om slechts een subset van artikelen op te nemen die moeten worden geteld met de eerste registratie.

    > [!TIP]
    > Als u wilt plannen dat meerdere werknemers de voorraad tellen, wordt het aangeraden verschillende filters in te stellen, steeds wanneer u de actie **Regels berekenen** gebruikt om de order alleen te vullen met de subset voorraadartikelen die één gebruiker registreert. Als u vervolgens meerdere voorraadregistraties voor meerdere werknemers genereert, minimaliseert u het risico om artikelen tweemaal te tellen. Zie voor meer informatie de sectie [Een inventarisatieregistratie maken](#to-create-a-physical-inventory-recording).

7. Kies de knop **Ok**.

Er wordt een regel in de order ingevoegd voor elk artikel dat bestaat in de geselecteerde vestiging en volgens de ingestelde filters en opties. Voor artikelen die voor artikeltracering zijn ingesteld, wordt het selectievakje **Artikeltracering gebruiken** geselecteerd en is informatie over de verwachte hoeveelheid en serie- en lotnummers beschikbaar door de actie **Regels** te kiezen en vervolgens **Artikeltraceringsregels**. Zie voor meer informatie de sectie [Artikeltracering verwerken tijdens inventarisatie](#handling-item-tracking-when-counting-inventory).

U kunt nu doorgaan met een of meer registraties te maken. Dat zijn instructies voor de werknemers die de feitelijke inventarisatie uitvoeren.  

## <a name="to-create-a-physical-inventory-recording"></a>Een inventarisatieregistratie maken

Voor elke inventarisatieorder kunt u een of meer inventarisatieregistratiedocumenten maken waarin werknemers de getelde aantallen handmatig of via een geïntegreerd scanapparaat invoeren.

Standaard wordt een registratie gemaakt voor alle regels in de gerelateerde inventarisatieorder. Om te voorkomen dat twee werknemers hetzelfde artikel tellen in het geval van gedistribueerde inventarisatie, is het raadzaam de inventarisatieorder geleidelijk te vullen door filters in te stellen in de batchverwerking **Regels berekenen** (zie de sectie 'Een inventarisatieorder maken') en vervolgens de inventarisatieregistratie te maken en daarbij het selectievakje **Alleen regels die zich niet in registraties bevinden** in te schakelen. Deze instellingen zorgen dat elke nieuwe registratie die u maakt, alleen andere artikelen bevat dan de artikelen in andere registraties.

In het geval van handmatig tellen kunt u een lijst, het rapport **Inventarisatieregistratie**, afdrukken die een lege kolom bevat om de getelde aantallen in te noteren. Als het tellen is voltooid, voert u de vastgelegde aantallen op de pagina **Inventarisatieregistratie** in. Ten laatste brengt u de vastgelegde aantallen naar de gerelateerde inventarisatieorder over door de status in te stellen op **Gereedgemeld**.

1. Kies op een pagina **Inventarisatieorder** die regels bevat voor de artikelen die in één registratie moeten worden geteld, de actie **Nieuwe registratie maken**.
2. Benodigde opties selecteren en filters instellen.
3. Kies de knop **Ok**.

    Er wordt een inventarisatieregistratiedocument gemaakt.

4. Voor elke set te tellen artikelen laadt u deze in de gerelateerde inventarisatieorder en herhaalt u stap 1 tot en met 3 met het selectievakje **Alleen regels die zich niet in registraties bevinden** ingeschakeld.

5. Kies de actie **Registraties** om de pagina **Nieuwe inventarisatieregistratielijst** te openen.
6. Open de relevante registratie.
7. Vul indien nodig de velden op het sneltabblad **Algemeen** in.
8. Maak voor artikelen waarvoor artikeltracering wordt gebruikt, een extra regel voor elke lot- of serienummer door de actie **Functies** te kiezen en vervolgens de actie **Regel kopiëren**. Zie voor meer informatie de sectie [Artikeltracering verwerken tijdens inventarisatie](#handling-item-tracking-when-counting-inventory).  
9. Kies de actie **Afdrukken** om het fysieke document voor te bereiden dat werknemers gaan gebruiken om de getelde aantallen te noteren.

## <a name="to-finish-a-physical-inventory-recording"></a>Een inventarisatieregistratie voltooien

Als de medewerkers de voorraadaantallen hebben geteld, moet u voorbereidingen treffen om deze in het systeem te registreren.

1. Klik op de pagina **Nieuwe inventarisatieregistratielijst**, selecteer de inventarisatieregistratie die u wilt voltooien, en kies vervolgens de actie **Bewerken**.
2. Vul op het sneltabblad **Regels** het werkelijke aantal in het veld **Aantal** in voor elke regel.
3. Voor artikelen met serie- of lotnummers (het selectievakje **Artikeltracering gebruiken** is ingeschakeld), voert u de getelde aantallen op de specifieke regels voor de serie- en lotnummers van het artikel in. Zie voor meer informatie de sectie [Artikeltracering verwerken tijdens inventarisatie](#handling-item-tracking-when-counting-inventory).
4. Selecteer het selectievakje **Geregistreerd** op elke regel.
5. Als u alle gegevens van een inventarisatieregistratie hebt ingevoerd, kiest u de actie **Voltooien**. Voor alle regels moet het selectievakje **Geregistreerd** zijn ingeschakeld.

    > [!NOTE]
    > Als u een inventarisatieregistratie voltooit, wordt elke regel overgebracht naar de regel in de gerelateerde inventarisatieorder die er exact mee overeenkomst. Voor een overeenkomst moeten de waarden in de velden **Artikelnr.**, **Variant**, **Vestiging**, en **Opslaglocatie** hetzelfde zijn voor de registratie en de orderregels.<br /><br />
    > Als geen overeenkomende inventarisatieorderregel bestaat, en als het selectievakje **Registratie zonder order toestaan** is ingeschakeld, wordt automatisch een nieuwe regel ingevoegd en wordt het selectievakje **Geregistreerd zonder order** op de gerelateerde inventarisatieorderregel geselecteerd. Anders wordt een foutbericht weergegeven en wordt het proces geannuleerd.<br /><br />
    > Als meer dan één inventarisatieregistratieregel overeenkomt met een inventarisatieorderregel, wordt een bericht weergegeven en wordt het proces geannuleerd. Als om welke reden dan ook twee identieke inventarisatieregels in de inventarisatieorder komen, kunt u een functie gebruiken om dit op te lossen. Zie voor meer informatie de sectie [Dubbele inventarisatieorderregels zoeken](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>Een inventarisatieorder voltooien

Als u een inventarisatieregistratie hebt voltooid, wordt het veld **Geregistreerd aantal (basis)** in de gerelateerde inventarisatieorder bijgewerkt met de getelde (geregistreerde) waarden en wordt het selectievakje **Bij registratie** ingeschakeld. Als een getelde waarde verschilt van de verwachte waarde, wordt het verschil weergegeven in respectievelijk het veld **Positief aantal (basis)** en het veld **Negatief aantal (basis)**.

Als u verwachte aantallen en eventuele geregistreerde verschillen wilt zien voor artikelen met artikeltracering, kiest u de actie **Regels** en kiest u vervolgens de actie **Artikeltraceringsregels** om verschillende weergaven te selecteren voor serie- en lotnummers die betrokken zijn bij de inventarisatietelling.

U kunt ook de actie **Verschillen van inventarisatieorder** kiezen om eventuele verschillen tussen de verwachte hoeveelheid en de getelde hoeveelheid te bekijken.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Dubbele inventarisatieorderregels zoeken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inventarisatieorders boeken** in en kies vervolgens de gerelateerde koppeling.
2. Open de inventarisatieorder waarvoor u dubbele regels wilt weergeven.
3. Kies de actie **Dubbele regels weergeven**.

Dubbele inventarisatieorderregels worden weergegeven, zodat u deze kunt verwijderen en slechts één regel kunt behouden met een unieke set waarden in de velden **Artikelnr.**, **Variant**, **Vestiging** en **Opslaglocatie**.

### <a name="to-post-a-physical-inventory-order"></a>Een inventarisatieorder boeken

Na voltooiing van een inventarisatieorder en de wijziging van de status ervan in **Gereedgemeld**, kunt u deze boeken. U kunt de status van een inventarisatieorder alleen instellen op **Gereedgemeld** als aan het volgende is voldaan:

- Alle gerelateerde inventarisatieregistraties hebben de status **Gereedgemeld**.
- Elke inventarisatieorderregel is geteld door ten minste één inventarisatieorderregel
- De selectievakjes **Op registratieregels** en **Verwacht aantal (berekend)** zijn geselecteerd voor alle inventarisatieorderregels.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inventarisatieorders boeken** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de inventarisatieorder die u wilt voltooien en kies de actie **Bewerken**.

    Op de pagina **Inventarisatieorder** ziet u het aantal dat is geregistreerd in het veld **Geregistreerd aantal (basis)**.
3. Kies de actie **Voltooien**.

    De waarde in het veld **Status** is **Gereedgemeld**, en u kunt de order nu alleen wijzigen door eerst de actie **Opnieuw openen** te kiezen.
4. Als u de order wilt boeken, kiest u de actie **Boeken** en kiest u vervolgens de knop **OK**.

    De artikelposten worden bijgewerkt samen met eventuele gerelateerde artikeltraceringsposten.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### <a name="to-view-posted-physical-inventory-orders"></a>Geboekte inventarisatieorders weergeven

Na het boeken wordt de inventarisatieorder verwijderd en kunt u het document weergeven en evalueren als een geboekte inventarisatieorder, inclusief de inventarisatieregistraties ervan en eventuele gemaakte opmerkingen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte inventarisatieorders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Geboekte inventarisatieorders** de geboekte voorraadorder die u wilt weergeven en kies vervolgens de actie **Weergeven**.
3. Als u een lijst met gerelateerde inventarisatieregistraties wilt weergeven, kiest u de actie **Registraties**.

## <a name="handling-item-tracking-when-counting-inventory"></a>Artikeltracering verwerken tijdens inventarisatie

Artikeltracering heeft betrekking op de serie- en lotnummers die zijn toegewezen aan artikelen. Wanneer een artikel wordt geteld dat bijvoorbeeld in voorraad is opgeslagen als 10 verschillende lotnummers, moet de werknemer registreren welke en hoeveel eenheden van elk lotnummer zich in voorraad bevinden. Zie voor meer informatie over artikeltracering [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).

Het selectievakje **Artikeltracering gebruiken** op inventarisatieorderregels wordt automatisch ingeschakeld als een artikeltraceringscode is ingesteld voor het artikel, maar u kunt het ook handmatig inschakelen of uitschakelen.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Voorbeeld - een inventarisatieregistratie voorbereiden voor een artikel met artikeltracering

Neem een inventarisatie voor artikel A, dat in voorraad is opgeslagen als tien verschillende serienummers.
1. Schakel op de registratieregel voor het artikel het selectievakje **Artikeltracering gebruiken** in.
2. Kies het veld **Serienummer**, selecteer het eerste serienummer dat in voorraad voor het artikel bestaat, en kies vervolgens de knop **OK**.

    Kopieer de regel voor het eerste artikel met artikeltracering om extra regels in te voegen die corresponderen met het aantal serienummers dat in voorraad is opgeslagen.

3. Kies de actie **Functies** en vervolgens de actie **Regel kopiëren**.
4. Voer op de pagina **Regel van inventarisatierecord kopiëren** 9 in het veld **Aantal exemplaren** in en kies vervolgens de knop **OK**.
5. Selecteer op de eerste kopieregel het veld **Serienummer** en selecteer het volgende serienummer van het artikel.
6. Herhaal stap 5 voor de resterende acht serienummers, waarbij u erop let niet dezelfde tweemaal te selecteren.
7. Kies de actie **Afdrukken** om de afdruk voor te bereiden die werknemers gaan gebruiken om de getelde artikelen en serie-/lotnummers te noteren.

U ziet dat het rapport **Inventarisatieregistratie** tien regels bevat voor artikel A, één voor elk serienummer.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Voorbeeld - Getelde lotnummerverschillen registreren en boeken

Een artikel met lottracering wordt in voorraad opgeslagen met de nummerreeks 'LOT'.

**Verwachte voorraad**:

|Lotnr.|Aantal|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Totaal|120|

**Geregistreerde aantallen**:

|Lotnr.|Aantal|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Totaal|112|

**Te boeken aantallen**:

|Lotnr.|Verwacht aantal|Geregistreerd aantal|Te boeken aantal|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Totaal|120|112|-8|

Op de pagina **Inventarisatieorder** bevat het veld **Negatief aantal (basis)** *8*. Voor de desbetreffende orderregel bevat de pagina **Artikeltraceringslijst van inventarisatie** de positieve of negatieve aantallen voor de individuele lotnummers.

## <a name="inventory-documents"></a>Voorraaddocumenten

De volgende soorten documenten zijn handig voor het beheren van uw magazijn:

* Gebruik **Voorraadontvangsten** om positieve aanpassingen van artikelen te registreren op basis van kwaliteit, kwantiteit en kosten.
* Gebruik **Voorraadzendingen** om ontbrekende of beschadigde goederen af te schrijven.

U kunt deze documenten in elk stadium afdrukken, vrijgeven en opnieuw openen, en gemeenschappelijke waarden, inclusief dimensies, toewijzen in de koptekst. Als u de documenten opnieuw wilt afdrukken nadat ze zijn geboekt, kunt u dat doen op de pagina's **Geboekte voorraadontvangst** en **Geboekte voorraadverzending**.

> [!NOTE]
> Voordat u deze documenten kunt gebruiken, moet u een nummerreeks specificeren om hun id's te creëren. Zie de volgende sectie voor meer informatie.

### <a name="to-set-up-numbering-for-inventory-documents"></a>Nummering voor inventarisdocumenten instellen

In de volgende procedure wordt beschreven hoe u nummering instelt voor voorraaddocumenten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Geef op het sneltabblad **Nummering** in de volgende velden de reeks getallen voor documenten op:

   * **Voorraadontvangstnrs.**  
   * **Geboekte voorraadontvangstnrs.**  
   * **Voorraadverzendingsnrs.**  
   * **Geboekte voorraadverzendingsnrs.**  

### <a name="to-create-and-post-an-inventory-document"></a>Een voorraaddocument maken en boeken

De volgende procedure laat zien hoe u een voorraadontvangst maakt, afdrukt en boekt. De stappen zijn vergelijkbaar voor voorraadverzendingen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadontvangsten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in de kop van de pagina **Voorraadontvangst** de locatie in het veld **Locatie** en vul vervolgens de overige velden in, indien nodig.
3. Kies op het sneltabblad **Regels** in het **Artikel** het voorraadartikel. Geef in het veld **Aantal** op hoeveel artikelen moeten worden toegevoegd. 
4. Om een **Voorraadontvangst**-rapport af te drukken vanaf de pagina **Voorraadontvangst**, kiest u de actie **Afdrukken**.

De volgende functies zijn beschikbaar op de pagina **Voorraadontvangst**:

* Kies de actie **Vrijgeven** of **Opnieuw openen** om de status voor de volgende verwerkingsfase in te stellen  
* Kies de actie **Boeken** om de voorraadontvangst te boeken of kies **Boeken en afdrukken** om de ontvangst te boeken en het testrapport af te drukken  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="printing-inventory-documents"></a>Voorraaddocumenten afdrukken

U kunt de rapporten specificeren die in verschillende stadia moeten worden afgedrukt door een van de volgende opties te kiezen in het veld **Gebruik** van de pagina **Rapportselectie - Voorraad**:

* Voorraadontvangst
* Voorraadverzending
* Geboekte voorraadontvangst
* Geboekte voorraadverzending

> [!NOTE]
> De beschikbare rapporten kunnen variëren, afhankelijk van de lokalisatie voor uw land/regio. De basistoepassing bevat geen lay-outs.

## <a name="see-also"></a>Zie ook

[Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md)  
[Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
