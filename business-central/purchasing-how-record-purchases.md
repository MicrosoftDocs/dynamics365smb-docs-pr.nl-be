---
title: Een inkoopfactuur maken en inkopen vastleggen | Microsoft Docs
description: Hierin wordt beschreven hoe u voorraad, niet-voorraadartikelen of resources inkoopt door inkoopfacturen of inkooporders te maken en te boeken.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4073ccccd36f6ec62804a5c1bd1881fb4d7a167d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926809"
---
# <a name="record-purchases"></a>Inkopen vastleggen
U maakt een inkoopfactuur of inkooporder om de kosten van inkopen vast te leggen en leveranciers te volgen. Als u voorraad moet controleren, worden inkoopfacturen en inkooporders ook gebruikt om voorraadniveaus dynamisch aan te passen zodat u uw voorraadkosten kunt beperken en betere klantenservice kunt bieden. De inkoopkosten, inclusief servicekosten en voorraadwaarden die resulteren uit boekingsinkoopfacturen of orders, dragen bij aan winstcijfers en andere financiële KPI's in het rolcentrum.

Naast het kopen van fysieke artikelen (artikelsoort **Voorraad** ), die van invloed zijn op de voorraadwaardering, kunt u services aanschaffen die worden weergegeven door tijdseenheden. U kunt dit doen met de artikelsoort **Service** of met de regelsoort **Resource** .

> [!NOTE]  
> U moet inkooporders gebruiken als uw inkoopproces vereist dat u gedeeltelijke ontvangsten van een orderhoeveelheid registreert, bijvoorbeeld omdat de volledige hoeveelheid niet beschikbaar was bij de leverancier. Als u artikelen verkoopt door rechtstreeks van uw leverancier bij de klant te leveren, als een doorverzending, moet u ook inkooporders gebruiken. Zie [Doorverzendingen maken](sales-how-drop-shipment.md) voor meer informatie. Wat betreft alle andere aspecten werken inkooporders op dezelfde manier als inkoopfacturen. De volgende procedure is gebaseerd op een inkoopfactuur. De stappen zijn vergelijkbaar met de stappen voor een inkooporder.

Wanneer u de voorraadartikelen ontvangt of wanneer de ingekochte service wordt voltooid, boekt u de inkoopfactuur of -order om de voorraad en financiële records bij te werken en betaling aan de leverancier te activeren volgens de betalingscondities. Zie voor meer informatie [Inkopen boeken](ui-post-purchases.md) en [Betalingen doen](payables-make-payments.md).

> [!CAUTION]  
> Boek geen inkoopfactuur totdat u de fysieke artikelen ontvangt en de uiteindelijke kosten van de inkoop kent, inclusief eventuele toeslagen. Anders kloppen uw voorraadwaarde en winstcijfers mogelijk niet.

U kunt een geboekte inkoopfactuur gemakkelijk corrigeren of annuleren voordat u de leverancier betaalt. Dit is handig als u een typefout wilt corrigeren of als u de aankoop in het begin van het orderproces wilt wijzigen. Zie voor meer informatie [Onbetaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Als u al hebt betaald voor artikelen of services op de geboekte inkoopfactuur, moet u een inkoopcreditnota maken om de inkoop tegen te boeken. Zie voor meer informatie [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md).

De artikelkaart kan van het type **Voorraad** , **Service** en **Niet-voorraad** zijn om op te geven of het artikel een fysieke voorraadeenheid, een eenheid voor arbeidskosten of een fysieke eenheid die niet in voorraad wordt gehouden, is. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md). Het inkoopfactureringsproces is hetzelfde voor alle drie de artikeltypen.

> [!NOTE]
> Met de inkoopregelsoort **Resource** kunt u ook externe resources aanschaffen, bijvoorbeeld om een leverancier te factureren voor geleverd werk. Zie [Resources instellen](projects-how-setup-resources.md) voor meer informatie.<br /><br />
> Om een gekochte resource te gebruiken moet u mogelijk de capaciteit van de resource instellen en deze handmatig aan een taak toewijzen. Als u een resource koopt, wordt er een resourcepost gemaakt, maar resourceposten worden niet bijgehouden voor hoeveelheid en waarde, zoals bijvoorbeeld artikelen. Als het bijhouden van hoeveelheden en waarden vereist is, overweeg dan om andere typen regelartikelen te gebruiken.

U kunt leveranciersvelden op de inkoopfactuur op twee manieren invullen afhankelijk van of de leverancier reeds is geregistreerd.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="to-create-a-purchase-invoice"></a>Een inkoopfactuur maken
Hieronder wordt beschreven hoe u een inkoopfactuur maakt. De stappen zijn vergelijkbaar met de stappen voor een inkooporder. Het belangrijkste verschil is dat inkooporders extra velden en acties hebben voor de fysieke afhandeling van artikelen.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.  
2. Voer in het veld **Leverancier** de naam in van een bestaande leverancier.

    Overige velden op de pagina **Inkoopfactuur** worden nu ingevuld met de standaardinformatie over de geselecteerde leverancier. Als de leverancier niet is geregistreerd, volgt u deze stappen:
3. Voer in het veld **Leverancier** de naam van de nieuwe leverancier in.
4. Kies in dialoogvenster voor het registreren van de nieuwe leverancier de knop **Ja** .
5. Kies op de pagina **Selecteer een sjabloon voor een nieuwe leverancier** een sjabloon om de leverancierskaart op te baseren en kies vervolgens de knop **OK** .
6. Een nieuwe leverancierskaart wordt geopend, die vooraf is ingevuld met de informatie over de geselecteerde leveranciersjabloon. Het veld **Naam** is vooraf ingevuld met de naam van de nieuwe leverancier die u op de inkoopfactuur hebt ingevoerd.
7. Ga verder met het invullen van de overige velden op de leverancierskaart. Zie voor meer informatie [Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md).  
8. Wanneer u de leverancierskaart hebt voltooid, kiest u de knop **OK** om terug te keren naar de pagina **Inkoopfactuur** .

    Verschillende velden op de pagina **Inkoopfactuur** worden gevuld met gegevens die u op de nieuwe leverancierskaart hebt opgegeven.
9. Vul desgewenst de overige velden op de pagina **Inkoopfactuur** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    U kunt nu de inkoopfactuurregels invullen met voorraadartikelen of resources die u hebt gekocht van de leverancier.

    > [!NOTE]  
    >   Als u terugkerende inkoopregels voor de leverancier hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de factuur door de actie **Terugkerende inkoopregels ophalen** te kiezen.
10. Voer op het sneltabblad **Regels** in het veld **Artikelnr.** het nummer van een voorraadartikel of een service in.
11. Voer in het veld **Aantal** het in te kopen aantal van een artikel in.

    > [!NOTE]  
    >   Voor artikelen van de soort **Service** en voor regels van de soort **Resource** is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel.

    Het veld **Regelbedrag** wordt bijgewerkt met de waarde in het veld **Directe kostprijs** , vermenigvuldigd met de waarde in het veld **Aantal** .

    De prijs en het regelbedrag worden weergegeven met of zonder btw afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de leverancierskaart.

    De totalenvelden onder de regels worden automatisch bijgewerkt wanneer u regels maakt of wijzigt om de bedragen weer te geven die naar de grootboeken worden geboekt.

    > [!NOTE]
    > In zeldzame gevallen kunnen de geboekte bedragen afwijken van wat wordt weergegeven in de totalenvelden. Dit is meestal het gevolg van afrondingsberekeningen met betrekking tot btw of omzetbelasting.<br /><br />Om de bedragen te controleren die daadwerkelijk worden geboekt, kunt u de pagina **Statistieken** gebruiken, die rekening houdt met de afrondingsberekeningen. Als u de actie **Vrijgeven** kiest, worden de totalenvelden ook bijgewerkt met afrondingsberekeningen.

12. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw** onder in de factuur.

    > [!NOTE]  
    >   Als u factuurkortingen voor de leverancier hebt opgegeven, wordt het percentage automatisch ingevoegd in het veld **Kortingspercentage op leveranciersfactuur** als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Kortingsbedrag op factuur** .
13. Als u de ingekochte artikelen of diensten ontvangt, kiest u **Boeken** .

De inkoop wordt nu weerspiegeld in de voorraad, resourcejournalen en financiële records, en de leveranciersbetaling wordt geactiveerd. De inkoopfactuur wordt verwijderd uit het overzicht met inkoopfacturen en wordt vervangen door een nieuw document in het overzicht van geboekte inkoopfacturen.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Resources instellen](projects-how-setup-resources.md)  
[Inkopen boeken](ui-post-purchases.md)  
[Offertes aanvragen](purchasing-how-request-quotes.md)  
[Artikelen kopen voor een verkoop](purchasing-how-purchase-products-sale.md)  
[Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Doorverzendingen voorbereiden](sales-how-drop-shipment.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
