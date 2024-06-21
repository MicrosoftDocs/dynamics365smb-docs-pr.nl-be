---
title: Veel artikelafbeeldingen uit een ZIP-bestand importeren
description: 'Als u meerdere artikelafbeeldingen wilt importeren, geeft u uw afbeeldingsbestanden namen die corresponderen met uw artikelnummers, comprimeert u ze in een zip-bestand en gebruikt u vervolgens de pagina Artikelafbeeldingen importeren om te bepalen welke artikelafbeeldingen worden geïmporteerd.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Meerdere artikelafbeeldingen importeren
U kunt meerdere artikelafbeeldingen in één keer importeren. Geef uw afbeeldingsbestanden namen die corresponderen met uw artikelnummers, comprimeer ze in een zip-bestand en gebruik vervolgens de pagina Artikelafbeeldingen importeren om te bepalen welke artikelafbeeldingen worden geïmporteerd.

Alle algemene bestandsindelingen worden ondersteund.

## Afbeeldingsbestanden noemen naar de artikelnamen en het ZIP-bestand voorbereiden
1. Benoem elk bestand op de locatie waar uw artikelafbeeldingen zijn opgeslagen volgens het nummer van het gerelateerde artikel. Voorbeeld:

    |Artikelnr.|Bestandsnaam|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Verzamel alle bestanden in een ZIP-bestand. Selecteer bijvoorbeeld in Windows Verkenner de bestanden, en kies **Verzenden naar**, **Gecomprimeerde (gezipte) map**.     

## Artikelafbeeldingen importeren
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Artikelafbeeldingen importeren**.
3. Selecteer in het veld **Een ZIP-bestand selecteren** de relevante ZIP-map en kies de knop **Openen**.

    Er wordt een regel voor elk artikel en afbeelding gemaakt op de pagina **Artikelafbeeldingen importeren**.

    > [!NOTE]
    > Voor artikelkaarten die al een afbeelding hebben, wordt het selectievakje **Afbeelding bestaat al** geselecteerd. Als u geen bestaande afbeeldingen wilt vervangen, schakelt u het selectievakje **Afbeeldingen vervangen** uit. Als u geen afzonderlijke bestaande afbeeldingen wilt vervangen, verwijdert u de desbetreffende regels.

3. Kies de actie **Afbeeldingen importeren**.

Het veld **Status importeren** wordt bijgewerkt om aan te geven of de afbeeldingsimport is voltooid of overgeslagen.       

## Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Nummerreeksen maken](ui-create-number-series.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]