---
title: 'Ontwerpdetails: Beschikbaarheid artikeltracering'
description: 'De pagina''s Artikeltraceringsregels en Artikeltraceringssamenvatting bevatten dynamische beschikbaarheidsinformatie voor serie- of lotnummers, wat de transparantie voor gebruikers vergroot.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-item-tracking-availability"></a>Ontwerpdetails: Beschikbaarheid artikeltracering
De pagina's **Artikeltraceringsregels** en **Artikeltraceringssamenvatting** bevatten dynamische beschikbaarheidsinformatie voor serie- of lotnummers. Het doel hiervan is transparantie voor gebruikers te verhogen in uitgaande documenten, zoals verkooporders, door ze te laten zien welke serienummers of hoeveel eenheden van een lotnummer momenteel zijn toegewezen in andere geopende documenten. Dit vermindert onzekerheid die door dubbele toewijzingen wordt veroorzaakt en geeft orderverwerkers vertrouwen dat de artikeltraceringsnummers en datums die op ongeboekte verkooporders worden toegezegd, kunnen worden gerealiseerd. Zie voor meer informatie [Ontwerpdetails: Pagina Artikeltraceringsregels](design-details-item-tracking-lines-window.md).  

 Wanneer u de pagina **Artikeltraceringsregels** opent, worden beschikbaarheidsgegevens opgehaald uit de tabel **Artikelpost** en **Reserveringspost** zonder datumfilter. Wanneer u het veld **Serienummer** of het veld **Lotnr.** kiest, wordt de pagina **Artikeltraceringssamenvatting** geopend met een overzicht van de artikeltraceringsgegevens in de tabel **Reserveringspost**. De lijst bevat de volgende informatie over elk serie- of lotnummer op de artikeltraceringsregel:  

|Veld|Omschrijving|  
|---------------------------------|---------------------------------------|  
|**Totaal aantal**|Het totale aantal van het lot- of serienummer dat zich momenteel in voorraad bevindt.|  
|**Totaal verzocht aantal**|Het totale aantal van het lot- of serienummer waarom momenteel in alle documenten wordt verzocht.|  
|**Huidig wachtend aantal**|Het aantal dat is ingevoerd in de huidige instantie van de pagina **Artikeltraceringsregels**, maar nog niet definitief is opgeslagen in de database.|  
|**Totaal beschikbaar aantal**|Het aantal van het serie- of lotnummer dat beschikbaar is voor aanvraag van de gebruiker.<br /><br /> Dit aantal wordt als volgt berekend op basis van andere velden op de pagina:<br /><br /> totaal aantal – (totaal aangevraagd aantal + huidig wachtend aantal).|  

> [!NOTE]  
>  U kunt de informatie in de voorgaande tabel ook weergeven door de functie **Posten selecteren** op de pagina **Artikeltraceringsregels** te gebruiken.  

 Om databaseprestaties te handhaven, worden beschikbaarheidsgegevens slechts eenmaal uit de database opgehaald wanneer u de pagina **Artikeltraceringsregels** opent en de functie **Beschikbaarheid vernieuwen** op de pagina gebruikt.  

## <a name="calculation-formula"></a>Berekeningsformule
 Zoals beschreven in de vorige tabel, wordt de beschikbaarheid van een bepaald serie- of lotnummer als volgt berekend.  

 totaal beschikbaar aantal = aantal op voorraad - (alle vraag + aantal nog niet vastgelegd in de database)  

> [!IMPORTANT]  
>  Deze formule geeft aan dat de beschikbaarheidsberekening van serie- of lotnummers alleen rekening houdt met voorraad en verwachte ontvangsten negeert. Levering die nog niet naar voorraad is geboekt, is niet van invloed op beschikbaarheid van artikeltracering, in tegenstelling tot normale artikelbeschikbaarheid waarbij verwachte ontvangsten worden opgenomen.  

## <a name="see-also"></a>Zie ook
 [Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
