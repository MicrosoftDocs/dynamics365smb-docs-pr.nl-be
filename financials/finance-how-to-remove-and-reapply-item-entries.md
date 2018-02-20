---
title: 'Procedure: artikelposten verwijderen en opnieuw toepassen | Microsoft Docs'
description: U kunt bepaalde artikelvereffeningsposten die automatisch worden gemaakt tijdens voorraadtransacties inzien en handmatig wijzigen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 12bde7fc508bb29e56ad63d76b526a80b5073f03
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="remove-and-reapply-item-ledger-entries"></a>Artikelposten verwijderen en opnieuw toepassen
U kunt in het venster **Vereffeningsvoorstel** bepaalde artikelvereffeningsposten die automatisch worden gemaakt tijdens voorraadtransacties inzien en handmatig wijzigen.  

Wanneer u een transactie boekt waarbij artikelen naar of uit voorraad worden verplaatst, wordt een artikelvereffening gemaakt tussen elke voorraadtoename en voorraadafname. Deze vereffeningen bepalen de kostenstroom van de goederen die in de voorraad zijn opgenomen naar de kosten die uit de voorraad worden gehaald. Vanwege de manier waarop de kostprijs wordt berekend, kan een onjuiste artikelvereffening leiden tot onjuiste gemiddelde kosten en tot een onjuiste kostprijs. Zie Ontwerpdetails: artikelvereffening voor meer informatie.

In de volgende scenario's moet u mogelijk een vereffening ongedaan maken of artikelposten opnieuw toepassen:

- U bent vergeten een vaste vereffening te maken.
- U hebt een onjuiste vaste vereffening uitgevoerd.
- U moet een artikel retourneren waarmee al een verkoop is vereffend.

Gebruik indien mogelijk een document om een artikelpost opnieuw toe te passen. Als u bijvoorbeeld een inkoopretour moet maken van een artikel dat al is vereffend met een verkoop, voert u de vereffening opnieuw uit door het inkoopretourdocument te maken en te boeken met de juiste vereffening in het veld **Vereffeningsnr. artikelpost** op de inkoopretourregel. Dit gaat vooral gemakkelijk met de functie **Geboekte documentregels ophalen voor tegenboeking** of **Document kopiëren** in het inkoopretourdocument. Wanneer u het document boekt, wordt de artikelpost automatisch opnieuw toegepast. Zie voor meer informatie [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md).

Als het niet mogelijk is om een document te gebruiken voor het opnieuw uitvoeren van een vereffening, als u bijvoorbeeld een vaste vereffening moet corrigeren, gebruikt u het venster **Vereffeningsvoorstel** om een vereffening te corrigeren.

> [!Warning]  
> Houd het volgende in gedachten wanneer u met het toepassingsvoorstel werkt:
    - U moet het opnieuw uitvoeren van een vereffening voor vereffeningsposten niet langere tijd uitstellen, omdat andere gebruikers de artikelen niet kunnen verwerken totdat u de vereffeningsposten opnieuw vereffent of het venster **Vereffeningsvoorstel** sluit. Gebruikers die acties willen uitvoeren voor een vereffeningspost waarvan de vereffening handmatig ongedaan is gemaakt, ontvangen het volgende foutmelding: "U kunt deze handeling niet uitvoeren omdat de posten voor artikel XXX niet vereffend zijn in het vereffeningsvoorstel door gebruiker XXX."
    - U moet artikelposten alleen buiten de gebruikelijke werktijden opnieuw vereffenen. Zo voorkomt u eventuele conflicten met andere gebruikers die transacties voor dezelfde artikelen boeken.
    - Wanneer u het vereffeningsvoorstel sluit, voert [!INCLUDE[d365fin](includes/d365fin_md.md)] een controle uit om ervoor te zorgen dat alle posten zijn toegepast. Als u bijvoorbeeld een aantalvereffening verwijdert en geen nieuwe vereffening maakt, zal bij het sluiten van het vereffeningsvoorstel alsnog een nieuwe vereffening worden aangemaakt. Zo blijven de kosten intact. Als u echter een vaste vereffening verwijdert, wordt niet automatisch een nieuwe vaste vereffening gemaakt bij het sluiten van het voorstel. U moet dan zelf een nieuwe vereffening aanmaken in het voorstel.
    - U kunt in het toepassingsvoorstel vereffeningen uit meerdere posten tegelijk verwijderen. Aangezien het vereffenen van posten echter invloed heeft op de posten die beschikbaar zijn voor vereffening, kunt u geen vereffening maken voor meerdere posten tegelijk.
    - Het toepassingsvoorstel kan onder de volgende omstandigheden geen vereffening maken: als er onvoldoende aantallen in voorraad zijn om te vereffenen, kan het toepassingsvoorstel geen vereffening maken wanneer u een negatieve voorraadmutatiepost zonder artikeltraceringsinformatie probeert te vereffenen met een positieve voorraadmutatiepost met artikeltraceringsinformatie.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Een artikelvereffening verwijderen met het Vereffeningsvoorstel  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vereffeningsvoorstel** in en klik vervolgens op de gerelateerde koppeling.  
2.  Het venster **Vereffeningsvoorstel** wordt geopend en toont bestaande artikelposten voor alle items.  
3.  Voer filters in op het sneltabblad **Algemeen** om de artikelpost waarvoor u de vereffening wilt wijzigen makkelijker te kunnen vinden.  
4.  Selecteer de artikelpost en kies de actie **Vereffende posten**. Het venster **Vereffende posten weergeven - Vereffende posten** wordt geopend, met daarin de artikelpost of de artikelposten die met de geselecteerde post zijn vereffend.  
5.  Selecteer de artikelpost waarvoor u de vereffening wilt verwijderen.  
6.  Kies de actie **Vereffening verwijderen**. De artikelvereffeningspost die de twee artikelposten koppelt, wordt dan verwijderd en naar het venster **Vereffende posten weergeven - Niet-vereffende posten** verplaatst.  
7.  Sluit het venster **Vereffende posten weergeven - Vereffende posten**.  

 Het veld **Resterend aantal** van de twee artikelposten worden verhoogd met het niet-vereffende aantal. De verwijderde artikelpost kan nu opnieuw worden vereffend in het venster **Vereffende posten weergeven - Niet-vereffende posten**.  

> [!IMPORTANT]  
>  U moet het opnieuw uitvoeren van een vereffening voor vereffeningsposten niet langere tijd uitstellen, omdat andere gebruikers de betrokken artikelen niet kunnen verwerken totdat u de vereffeningsposten opnieuw vereffent of het venster **Vereffeningsvoorstel** sluit. De volgende foutmelding wordt weergegeven als u probeert bewerkingen uit te voeren waar een handmatig niet-vereffende vereffeningspost in is opgenomen:  
>   
>  **U kunt deze handeling niet uitvoeren omdat posten voor artikel <item> niet vereffend zijn in het Vereffeningsvoorstel door gebruiker <user>.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Een artikelvereffening opnieuw vereffenen met het Vereffeningsvoorstel  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vereffeningsvoorstel** in en klik vervolgens op de gerelateerde koppeling.  
2.  Het venster **Vereffeningsvoorstel** wordt geopend en toont bestaande artikelposten voor alle items.  
3.  Als u posten opnieuw wilt vereffenen die zijn verwijderd na het openen van het voorstel, selecteert u de artikelpost die u opnieuw wilt vereffenen. Kies op het tabblad **Acties** in de groep **Functies** de optie **Opnieuw vereffenen**.  

    > [!NOTE]  
    >  Deze vereffening van het oorspronkelijke aantal gebeurt ook automatisch wanneer u het venster **Vereffeningsvoorstel** sluit.  
4.  Selecteer om een beschikbare open artikelpost op een andere post te vereffenen de artikelpost die u wilt vereffenen. Kies de actie **Niet-toegepaste posten**. Het venster **Vereffende posten weergeven - Niet-vereffende posten** opent.  
5.  Selecteer een of meer artikelposten die u wilt vereffenen met de post die is geselecteerd in het venster **Vereffeningsvoorstel** en klik op **OK**.  

     Er wordt een artikelvereffeningspost gemaakt tussen de twee artikelposten. De velden **Resterend aantal** van de twee posten worden gereduceerd met het vereffende aantal.  

    > [!NOTE]  
    >  Als u ervoor hebt gekozen een vereffening uit te voeren die tijdens het herwaarderen van de kosten tot een oneindige herhaling zou leiden, wordt de door u voorgestelde vereffening niet uitgevoerd. Dit kan voorkomen wanneer de originele posten negatieve voorraad hebben veroorzaakt. De vereffening wordt niet uitgevoerd. Daarom moet u een andere post selecteren voor de vereffening.  
6.  Als het veld **Automatische kostenwaardering** in de **Voorraadinstelling** is ingesteld op **Altijd**, voert het programma de batchverwerking voor het herwaarderen van de kosten automatisch uit nadat u een vereffening opnieuw hebt uitgevoerd. Anders voert u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uit om er zeker van zijn dat alle kosten up-to-date zijn.  

## <a name="see-also"></a>Zie ook  
[Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md)  
 [Voorraadkosten beheren](finance-manage-inventory-costs.md)   
 [Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

