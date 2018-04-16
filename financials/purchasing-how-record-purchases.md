---
title: Een inkoopfactuur maken en inkopen vastleggen | Microsoft Docs
description: Hierin wordt beschreven hoe u voorraad en serviceartikelen inkoopt door inkoopfacturen of inkooporders te maken en te boeken.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3228d82190e81198817d0e1fa5c86f6c9d0f784f
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="record-purchases"></a>Inkopen vastleggen
U maakt een inkoopfactuur of inkooporder om de kosten van inkopen vast te leggen en leveranciers te volgen. Als u voorraad moet controleren, worden inkoopfacturen en inkooporders ook gebruikt om voorraadniveaus dynamisch aan te passen zodat u uw voorraadkosten kunt beperken en betere klantenservice kunt bieden. De inkoopkosten, inclusief servicekosten en voorraadwaarden die resulteren uit boekingsinkoopfacturen of orders, dragen bij aan winstcijfers en andere financiële KPI's in het rolcentrum.

> [!NOTE]  
>   U moet inkooporders gebruiken als uw inkoopproces vereist dat u gedeeltelijke ontvangsten van een orderhoeveelheid registreert, bijvoorbeeld omdat de volledige hoeveelheid niet beschikbaar was bij de leverancier. Als u artikelen verkoopt door rechtstreeks van uw leverancier bij de klant te leveren, als een doorverzending, moet u ook inkooporders gebruiken. Zie [Doorverzendingen maken](sales-how-drop-shipment.md) voor meer informatie. Wat betreft alle andere aspecten werken inkooporders op dezelfde manier als inkoopfacturen. De volgende procedure is gebaseerd op een inkoopfactuur. De stappen zijn vergelijkbaar met de stappen voor een inkooporder.

Wanneer u de voorraadartikelen ontvangt of wanneer de ingekochte service wordt voltooid, boekt u de inkoopfactuur of -order om de voorraad en financiële records bij te werken en betaling aan de leverancier te activeren volgens de betalingscondities. Zie voor meer informatie [Betalingen doen](payables-make-payments.md).

> [!CAUTION]  
>   Boek geen inkoopfactuur totdat u de artikelen ontvangt en de uiteindelijke kosten van de inkoop kent, inclusief eventuele toeslagen. Anders kloppen uw voorraadwaarde en winstcijfers mogelijk niet.

U kunt een geboekte inkoopfactuur gemakkelijk corrigeren of annuleren voordat u de leverancier betaalt. Dit is handig als u een typefout wilt corrigeren of als u de aankoop in het begin van het orderproces wilt wijzigen. Zie voor meer informatie [Onbetaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Als u al hebt betaald voor artikelen op de geboekte inkoopfactuur, moet u een inkoopcreditnota maken om de inkoop tegen te boeken. Zie voor meer informatie [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md).

Artikelen kunnen van het type **Voorraad** of **Service** zijn. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md). Het inkoopfactuurproces is gelijk voor beide artikelsoorten.

U kunt leveranciersvelden op de inkoopfactuur op twee manieren invullen afhankelijk van of de leverancier reeds is geregistreerd.

## <a name="to-create-a-purchase-invoice"></a>Een inkoopfactuur maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer in het veld **Leverancier** de naam in van een bestaande leverancier.

    Overige velden in het venster **Inkoopfactuur** worden nu ingevuld met de standaardinformatie over de geselecteerde leverancier. Als de leverancier niet is geregistreerd, volgt u deze stappen:
3. Voer in het veld **Leverancier** de naam van de nieuwe leverancier in.
4. Kies in dialoogvenster voor het registreren van de nieuwe leverancier de knop **Ja**.
5. Kies in het venster **Selecteer een sjabloon voor een nieuwe leverancier** een sjabloon om de leverancierskaart op te baseren en kies vervolgens de knop **OK**.
6. Een nieuwe leverancierskaart wordt geopend, die vooraf is ingevuld met de informatie over de geselecteerde leveranciersjabloon. Het veld **Naam** is vooraf ingevuld met de naam van de nieuwe leverancier die u op de inkoopfactuur hebt ingevoerd.
7. Ga verder met het invullen van de overige velden op de leverancierskaart. Zie voor meer informatie [Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md).  
8. Wanneer u de leverancierskaart hebt voltooid, kiest u de knop **OK** om terug te keren naar het venster **Inkoopfactuur**.

    Verschillende velden in het venster **Inkoopfactuur** worden gevuld met gegevens die u op de nieuwe leverancierskaart hebt opgegeven.
9. Vul indien nodig de overige velden in het venster **Inkoopfactuur** in. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    U kunt nu de inkoopfactuurregels invullen met voorraadartikelen of services die u hebt gekocht van de leverancier.

    > [!NOTE]  
   >   Als u terugkerende inkoopregels voor de leverancier hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de factuur door de actie **Terugkerende inkoopregels ophalen** te kiezen.
10. Voer op het sneltabblad **Regels** in het veld **Artikelnr.** het nummer van een voorraadartikel of een service in.
11. Voer in het veld **Aantal** het in te kopen aantal van een artikel in.

    > [!NOTE]  
    >   Voor artikelen van de soort **Service** is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel.

    Het veld **Regelbedrag** wordt bijgewerkt met de waarde in het veld **Directe kostprijs**, vermenigvuldigd met de waarde in het veld **Aantal**.

    De prijs en het regelbedrag worden weergegeven met of zonder btw afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de leverancierskaart.
12. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw** onder in de factuur.

    > [!NOTE]  
    >   Als u factuurkortingen voor de leverancier hebt opgegeven, wordt het percentage automatisch ingevoegd in het veld **Kortingspercentage op leveranciersfactuur** als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Kortingsbedrag op factuur**.
13. Als u de ingekochte artikelen of diensten ontvangt, kiest u **Boeken**.

De inkoop wordt nu weerspiegeld in de voorraad en financiële records, en de leveranciersbetaling is ingeschakeld. De inkoopfactuur wordt verwijderd uit het overzicht met inkoopfacturen en wordt vervangen door een nieuw document in het overzicht van geboekte inkoopfacturen.

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Offertes aanvragen](purchasing-how-request-quotes.md)  
[Artikelen kopen voor een verkoop](purchasing-how-purchase-products-sale.md)  
[Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Doorverzendingen voorbereiden](sales-how-drop-shipment.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

