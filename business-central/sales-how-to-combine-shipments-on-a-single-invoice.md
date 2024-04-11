---
title: Verzendingen combineren op één factuur | Microsoft Docs
description: 'Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Verzendingen combineren op één factuur

Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.  

Voordat u een verzamelfactuur kunt maken, moet u meerdere verkoopverzendingen voor dezelfde klant in dezelfde valuta boeken. U moet dus twee of meer verkooporders hebben gemaakt en deze als verzonden maar niet als gefactureerd boeken. 

## Verzendingen handmatig op één factuur combineren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.
3. Voer in het veld **Orderklantnr.** de klant in die de factuur voor de verzonden artikelen zal ontvangen.  
4. Selecteer op het sneltabblad **Regels** de actie **Verzendregels ophalen**.  
5. Selecteer de verzendregels die u wilt opnemen in de factuur:  

    - Als u alle regels wilt invoegen, selecteert u alle regels en klikt u op **OK**.  
    - Als u specifieke regels wilt invoegen, selecteert u deze regels en klikt u op **OK**. Gebruik de Ctrl-toets om meerdere niet-aaneengesloten regels te selecteren.  

    Als u de verkeerde verzendregel hebt geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de factuur verwijderen en de functie **Verzendregels ophalen** opnieuw uitvoeren.  
7. Kies de actie **Boeken** om de factuur te boeken.  

> [!TIP]  
> Als u orders hebt verzonden waarvoor de waarde voor **Orderklantnr.** anders is dan de waarde voor **Factuurklantnr.**, worden die regels niet weergegeven in het rapport **Verzendregels ophalen**. Gebruik personalisatie om het veld **Orderklant** toe te voegen aan de pagina en het filter te verwijderen. U kunt nu zendingsregels aan de factuur toevoegen, ongeacht de waarde in het veld **Orderklantnr.** zolang het veld **Factuurklantnr.** op de verzendregels overeenkomt met de waarde op de verkoopfactuur.  

## Verzendingen automatisch op één factuur combineren

[!INCLUDE[prod_short](includes/prod_short.md)] selecteert alleen verkooporders waar **Verzendingen combineren** is gekozen. 

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verzendingen combineren** in en kies vervolgens de gerelateerde koppeling. De opvraagpagina voor de batchverwerking wordt geopend.  
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies het selectievakje **Facturen boeken**.  
4. Kies de knop **OK**.  

> [!NOTE]  
>  U moet de facturen handmatig boeken als het selectievakje **Facturen boeken** niet was ingeschakeld bij de batchverwerking.  

## Openstaande verkooporders verwijderen na boeking van een verzamelfactuur

Als verzendingen worden gecombineerd op een factuur en worden geboekt, wordt er een geboekte verkoopfactuur gemaakt voor de gefactureerde regel. Het veld **Verzonden aantal** op het oorspronkelijke verkoopraamcontract of de oorspronkelijke verkooporder wordt bijgewerkt op basis van het gefactureerde aantal.  

Als u op deze manier verzendingen factureert, blijven de orders van waaruit de verzending zijn geboekt bestaan, ook als ze volledig zijn verzonden en gefactureerd.   

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gefactureerde verkooporders verwijderen** in en kies vervolgens de gerelateerde koppeling  
2. Geef in het filterveld **Nr.** op welke verkooporders moeten worden verwijderd.  
3. Kies de knop **Ok**.  

U kunt afzonderlijke verkooporders ook handmatig verwijderen.  

Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals verkoopraamcontracten.

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
