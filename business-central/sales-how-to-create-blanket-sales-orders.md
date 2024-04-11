---
title: Werken met verkoopraamcontracten of inkooporders
description: Gebruik raamcontracten als een klant ermee heeft ingestemd grote hoeveelheden te kopen die in meerdere kleinere zendingen moeten worden geleverd gedurende een bepaalde periode. Hetzelfde geldt voor inkopen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '507, 509, 6620, 6622, 6623, 9303, 9310'
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="work-with-blanket-sales-orders-or-blanket-purchase-orders"></a>Werken met verkoopraamcontracten of inkoopraamcontracten

Een verkoopraamcontract biedt een kader voor een langdurige overeenkomst tussen u en uw klant. Evenzo gebruikt u inkoopraamcontracten om langetermijnovereenkomsten tussen u en uw leverancier te beheren.

Een raamcontract wordt meestal gemaakt als uw klant ermee heeft ingestemd grote hoeveelheden aan te kopen die in meerdere kleinere zendingen moeten worden geleverd gedurende een bepaalde periode. Inkoopraamcontracten hebben vaak betrekking op slechts één artikel met vooraf vastgestelde leverdatums. De belangrijkste reden voor het gebruik van een raamcontract in plaats van een verkooporder is dat de ingevoerde hoeveelheden op een raamcontract niet van invloed op de artikelbeschikbaarheid en dus gebruikt kunnen worden als een werkblad voor controle, prognose en planningsdoeleinden.

In het raamcontract kan elke afzonderlijke verzending worden ingesteld als een orderregel, die vervolgens op het moment van verzenden kan worden omgezet in een verkooporder.

Een verkoopraamcontract kan bijvoorbeeld worden gebruikt als een klant belt om een order te plaatsen van 1000 eenheden van een artikel, waarbij dit artikel gedurende de komende maand moeten worden geleverd met 250 eenheden per week.

> [!NOTE]
> Inkoopraamcontracten functioneren op een soortgelijke manier als verkoopraamcontracten. Deze documentatie beschrijft alleen verkoopraamcontracten.

## <a name="to-create-a-blanket-sales-order"></a>Een verkoopraamcontract maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopraamcontracten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Laat het veld **Besteldatum** leeg. Als de afzonderlijke verkooporders worden gemaakt uit het raamcontract, wordt de orderdatum van de verkoopdatum ingesteld op de werkelijke werkdatum.
5. Maak op het sneltabblad **Regels** afzonderlijke regels voor elke zending. Als uw klant bijvoorbeeld 1000 eenheden wil die gelijkmatig over vier weken moeten worden verdeeld, voert u vier afzonderlijke regels van elk 250 eenheden in.  

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Een verkooporder maken uit een verkoopraamcontract

1. Als u een order wilt maken voor een van de regels uit het verkoopraamcontract, verwijdert u het aantal uit het veld **Te verzenden aantal** op alle regels die u op dit moment niet wilt verzenden.  
2. Wanneer u klaar bent om orders te maken, kiest u de actie **Order maken** en klikt u vervolgens op **Ja**. Er wordt een bericht weergegeven waarin u wordt meegedeeld dat aan het raamcontract een ordernummer is toegewezen. Het raamcontract is echter niet verwijderd.  
3. Kies de knop **Ok**.  
4. Als u de resultaten wilt zien van de voorgaande stappen, kiest u eerst de actie **Regel**, vervolgens de actie **Ongeboekte regels** en daarna de actie **Orders**.  
5. Selecteer op de pagina **Verkoopregels** de gewenste verkooporder. Klik op de actie **Regel** en vervolgens op de actie **Document weergeven**.  

Het volgende geldt voor verkooporders nadat ze zijn gemaakt uit verkoopraamcontracten:  

- Als het raamcontract eenmaal is omgezet in een verkooporder, bevat de verkooporder alle regels uit het raamcontract. De regels waarop het aantal in het veld **Te verzenden aantal** is verwijderd, worden weergegeven, maar met lege **Aantal**-velden. U kunt de regels behouden, bewerken of verwijderen.  
- Onthoud dat het aantal op de verkooporderregel niet hoger mag zijn dan het aantal van de gerelateerde raamcontractregel. Als dit wel zo is, kan de verkooporder niet worden geboekt.  
- Als de verkooporder is geboekt als verzonden en/of gefactureerd, worden de velden **Verzonden aantal** en **Gefactureerd aantal** bijgewerkt op het gerelateerde raamcontract.  
- Het raamcontractnummer en het regelnummer worden vastgelegd als eigenschappen van de verkoopregels als deze worden gemaakt uit een raamcontract.  
- Als verkooporders niet rechtstreeks vanuit het raamcontract worden gemaakt maar er wel aan gerelateerd zijn, kan er een koppeling worden gemaakt tussen een verkooporder en een raamcontract door het gekoppelde raamcontractnummer in te voeren in het veld **Raamcontractnr.** op de verkooporderregel. op de verkooporderregel.  
- Nadat u de verkooporder hebt gemaakt voor het totale aantal van een raamcontractregel, kunt u geen andere verkooporder voor dezelfde regel maken. Voorkomt dat gebruikers een aantal in het veld **Te verzenden aantal** invoeren. Als er echter aanvullende aantallen moeten worden toegevoegd aan een raamcontract, kan de waarde in het veld **Aantal** worden verhoogd, waarna er extra orders kunnen worden gemaakt.  
- Het gefactureerde verkoopraamcontract blijft in het systeem aanwezig totdat het wordt verwijderd, hetzij door afzonderlijke raamcontracten te verwijderen, hetzij door de batchverwerking **Gefact. raamcontracten verwijderen** uit te voeren.  
- Wanneer een klant ook als contact is vastgelegd in de module Marketing en u een interactiesjablooncode voor een verkoopraamcontract hebt opgegeven op de pagina **Marketinginstellingen**, wordt zodra u op **Afdrukken** klikt om het verkoopraamcontract af te drukken, automatisch een interactie in de tabel Interactielogpost vastgelegd.

## <a name="to-view-the-status-of-a-blanket-sales-order"></a>De status van een verkoopraamcontract weergeven

U kunt de status van een verkoopraamcontract op de pagina **Raamverkooporderstatistiek** bekijken. Dit kan nodig zijn wanneer u de order die is gemaakt vanuit het verkoopraamcontract gaat factureren.  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopraamcontracten** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer een verkoopraamcontract en kies de actie **Statistieken**.  
3.  Op het sneltabblad **Algemeen** op de pagina **Raamverkooporderstatistiek** kunt u een samenvatting van de hele order bekijken, gebaseerd op het totaal van alle velden **Aantal** op de verkoopraamcontractregels.  

- Op het sneltabblad **Facturering** kunt u een samenvatting bekijken gebaseerd op het totaal van de velden **Te factureren aantal** op de verkoopraamcontractregels.  
- Op het sneltabblad **Verzending** kunt u een samenvatting bekijken gebaseerd op het totaal van de velden **Te ontvangen aantal** op de verkoopraamcontractregels.  
- Op het sneltabblad **Vooruitbetaling** vindt u algemene informatie bekijken over eventuele vooruitbetaalde bedragen.  
- Op het sneltabblad **Leverancier** kunt u bepaalde basisgegevens over de leverancier bekijken.

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Niet-geboekte en geboekte verkoopraamcontractregels weergeven

De koppeling tussen het verkoopraamcontract en de oorspronkelijke verkooporder en een eventueel ander verkoopdocument blijft na het boeken behouden als een lijst van geboekte en niet-geboekte verkooporderfactuurregels.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopraamcontracten** in en kies vervolgens de gerelateerde koppeling.
2. Open de verkoopraamorder die u wilt bekijken.
3. Als u ongeboekte posten wilt weergeven, selecteert u de bewuste regel, klikt u op de actie **Regel** en kiest u vervolgens de actie **Ongeboekte regels**. Kies een van de volgende opties.  

|Optie|Description|
|--|--|
|**Orders**|Toont openstaande orders die zijn gerelateerd aan de geselecteerde regel.|
|**Facturen**|Toont openstaande facturen die zijn gerelateerd aan de geselecteerde regel. Openstaande facturen worden handmatig gerelateerd aan een raamcontract door het raamcontractnummer in te voeren op de verkoopfactuurregel.|
|**Retourorders**|Toont openstaande retourorders die zijn gerelateerd aan de geselecteerde regel.|
|**Creditnota's**|Toont openstaande creditnota's die zijn gerelateerd aan de geselecteerde regel.|

4. Als u geboekte posten wilt weergeven, selecteert u de bewuste regel, klikt u op de actie **Regel** en kiest u vervolgens de actie **Geboekte regels**. Kies een van de volgende opties.  

|Optie|Description|
|---|----|
|**Verzendingen**|Geboekte verzendingen die zijn gerelateerd aan de geselecteerde regel.|
|**Facturen**|Geboekte facturen die zijn gerelateerd aan de geselecteerde regel.|
|**Retourontvangsten**|Geboekte retourontvangsten die zijn gerelateerd aan de geselecteerde regel.|
|**Creditnota's**|Geboekte creditnota's die zijn gerelateerd aan de geselecteerde regel.|

5. Kies op de pagina **Verkoopregels** de actie **Document weergeven** om de post te bekijken.

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Raamassemblageorders](assembly-how-to-create-blanket-assembly-orders.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
