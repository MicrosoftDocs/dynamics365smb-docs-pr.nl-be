---
title: Artikelen ontvangen | Microsoft Docs
description: Bij ontvangst van artikelen in een magazijn waarvoor magazijnontvangstverwerking is ingesteld, moet u de regels ophalen van het vrijgegeven brondocument waaruit de ontvangst voortkomt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 038ecb0122e58cfdca3ff62ac93554fab01dcdb6
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786608"
---
# <a name="receive-items"></a>Artikelen ontvangen

Bij ontvangst van artikelen in een magazijn waarvoor magazijnontvangstverwerking niet is ingesteld, registreert u de ontvangst in het gerelateerde bedrijfsdocument, zoals een inkooporder, verkoopretourorder of inkomende transferorder.

Bij ontvangst van artikelen in een magazijn waarvoor magazijnontvangstverwerking is ingesteld, moet u de regels ophalen van het vrijgegeven brondocument waaruit de ontvangst voortkomt. Als u met opslaglocaties werkt, kunt u de voorgestelde standaardopslaglocatie accepteren of, als het artikel nog niet in het magazijn is gebruikt, een andere opslaglocatie voor het artikel invullen. Vervolgens moet u de aantallen van de ontvangen artikelen invullen en de ontvangst boeken.  

## <a name="to-receive-items-with-a-purchase-order"></a>Artikelen ontvangen met een inkooporder

Hieronder wordt beschreven hoe u artikelen ontvangt met een inkooporder. De stappen zijn vergelijkbaar voor verkoopretourorders en transferorders.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.
2. Open een bestaande inkooporder of maak een nieuwe. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).
3. Voer in het veld **Te ontvangen aantal** het aantal in dat u hebt ontvangen.

  > [!NOTE]
  > Als het ontvangen aantal groter is dan het bestelde aantal, zoals aangegeven op de inkooporder in het veld **Aantal**, en als voor de leverancier is ingesteld dat meerontvangsten zijn toegestaan, gebruikt u het veld **Te veel ontvangen** bovenaan om het overtollige aantal te verwerken. Voor meer informatie zie [Meer artikelen ontvangen dan besteld](warehouse-how-receive-items.md#to-receive-more-items-than-ordered).

4. Kies de actie **Boeken**.

  De waarde in het veld **Ontvangen aantal** wordt dienovereenkomstig bijgewerkt. Als het een gedeeltelijke ontvangst is, is de waarde lager dan de waarde in het veld **Aantal**.

> [!NOTE]
> Als u een magazijndocument gebruikt om de ontvangst te boeken, kunt u de actie **Boeken** in de inkooporder gebruiken. In plaats daarvan heeft een magazijnmedewerker de inkooporderhoeveelheid al geboekt als ontvangen. Zie voor meer informatie [Artikelen ontvangen met een magazijnontvangst](warehouse-how-receive-items.md#to-receive-items-with-a-warehouse-receipt).

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Artikelen ontvangen met een magazijnontvangst

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnontvangsten** in en kies de desbetreffende koppeling.  
2. Kies de actie **Nieuw**.  

    Vul de velden op het sneltabblad **Algemeen** in. Bij het ophalen van brondocumentregels worden bepaalde gegevens automatisch naar elke regel gekopieerd.  

    Voor magazijnconfiguraties met gestuurde opslag en pick: als de vestiging een standaardzone en -opslaglocatie voor ontvangsten heeft, worden de velden **Zone** en **Opslaglocatie** automatisch ingevuld. U kunt deze waarden desgewenst wijzigen.  

    > [!NOTE]  
    > Als u artikelen wilt ontvangen met andere magazijnklassen dan de magazijnklasse van de opslaglocatie in het veld **Opslaglocatie** op de documentkop, moet u de inhoud van het veld **Opslaglocatie** op de kop verwijderen voordat u de brondocumentregels voor de artikelen ophaalt.  
3. Kies de actie **Brondocumenten ophalen**. De pagina **Brondocumenten** verschijnt.

    U kunt vanuit een nieuwe of geopende magazijnontvangst de pagina **Filters om brondoc. op te halen** gebruiken voor het ophalen van de vrijgegeven brondocumentregels die bepalen welke artikelen moeten worden ontvangen of verzonden.

    1. Kies de actie **Filters om brondoc. op te halen gebruiken**.  
    2. U stelt een nieuw filter in door een omschrijvende code in te voeren in het veld **Code** en vervolgens de actie **Wijzigen** te kiezen.  
    3. Definieer het soort brondocumentregels dat u wilt ophalen door de relevante filtervelden in te vullen.  
    4. Kies de actie **Uitvoeren**.  

    Alle vrijgegeven brondocumentregels die voldoen aan de filtercriteria worden nu ingevoegd op de pagina **Magazijnontvangst** van waaruit u de filterfunctie hebt geactiveerd.  

    De filtercombinaties die u definieert, worden opgeslagen op de pagina **Filters om brondoc. op te halen** tot de volgende keer dat u deze nodig hebt. U kunt een onbeperkt aantal filtercombinaties maken. U kunt de criteria op elk moment wijzigen door de actie **Wijzigen** te kiezen.

4. Selecteer de brondocumenten waarvoor u artikelen wilt ontvangen en klik op **OK**.  

    De regels van de brondocumenten verschijnen op de pagina **Magazijnontvangst**. Het veld **Te ontvangen aantal** is ingevuld met de openstaande hoeveelheid voor elke regel, maar u kunt het aantal wijzigen indien nodig. Als u de inhoud van het veld **Opslaglocatie** op het sneltabblad **Algemeen** verwijdert voordat u de regels ophaalt, moet u op elke ontvangstregel een opslaglocatie invullen.  

    > [!NOTE]  
    >  Kies de actie **Te ontvangen aantal verwijderen** als u op alle regels nul wilt invullen in het veld **Te ontvangen aantal**. Om het veld nogmaals in te vullen met het openstaande aantal, kiest u de actie **Te ontvangen aantal automatisch invullen**.  

    > [!NOTE]  
    >  U kunt niet meer artikelen ontvangen dan het aantal in het veld **Openstaand aantal** op de brondocumentregel. Om meer artikelen te ontvangen, haalt u een ander brondocument op dat een regel bevat voor het item met behulp van de filterfunctie om brondocumenten met het artikel op te halen.  

5. Boek de magazijnontvangst. De velden met aantallen in de brondocumenten worden bijgewerkt en de artikelen worden bij de bedrijfsvoorraad gevoegd.  

Als u met magazijnopslag werkt, worden de ontvangstregels naar de magazijnopslagfunctie verzonden. Artikelen die al zijn ontvangen, kunnen pas na opslag worden gepickt. De ontvangen artikelen worden geïdentificeerd als beschikbare voorraad nadat de opslag is geregistreerd.  

Als u niet met magazijnopslag, maar met opslaglocaties werkt, wordt de opslag van de artikelen geregistreerd in de opslaglocatie die is opgegeven op de brondocumentregel.  

> [!NOTE]  
> Met de functie **Boeken en afdrukken** kunt u zowel de ontvangst boeken als opslaginstructies afdrukken waarin wordt aangegeven waar de artikelen moeten worden opgeslagen.  
>
> Als uw locatie met gestuurde opslag en pick werkt, wordt de beste opslaglocatie voor de artikelen bepaald aan de hand van de opslagsjablonen. De opslaglocatie wordt vervolgens op de opslaginstructie afgedrukt.

## <a name="to-receive-more-items-than-ordered"></a>Meer artikelen ontvangen dan besteld

Wanneer u meer goederen ontvangt dan u hebt besteld, wilt u deze misschien ontvangen in plaats van de ontvangst te annuleren. Het kan bijvoorbeeld goedkoper zijn om het eigen risico op uw inventaris te houden dan ze terug te sturen of uw leverancier kan u korting geven om ze te bewaren.

### <a name="to-set-up-over-receipts"></a>Meerontvangsten instellen

U moet een percentage definiëren waarmee u toestaat dat de bestelde hoeveelheid bij ontvangst wordt overschreden. U definieert dit onder een meerontvangstcode, die het percentage in het veld **Tolerantiepercentage voor meerontvangst** bevat. Vervolgens wijst u de code toe aan de kaarten van relevante artikelen en/of leveranciers.  

Hieronder wordt beschreven hoe u een meerontvangstcode instelt en toewijst aan een artikel. De stappen zijn vergelijkbaar voor een leverancier.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.
2. Open de kaart voor een artikel waarvan u vermoedt dat het soms wordt geleverd met een grotere hoeveelheid dan besteld.
3. Kies de opzoekknop in het veld **Meerontvangstcode**.
4. Kies de actie **Nieuw**.
5. Maak op de pagina **Meerontvangstcodes** een of meer nieuwe regels die verschillend meerontvangstbeleid definiëren. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Selecteer een regel en kies de knop **OK**.

De meerontvangstcode wordt toegewezen aan het artikel. Met elke inkooporder of magazijnontvangst voor het artikel kan nu meer worden ontvangen dan de bestelde hoeveelheid volgens het opgegeven tolerantiepercentage voor meerontvangst.

> [!NOTE]
> U kunt een goedkeuringswerkstroom instellen om te vereisen dat meerontvangsten moeten worden goedgekeurd voordat ze kunnen worden afgehandeld. In dat geval moet u het selectievakje **Goedkeuring vereist** inschakelen op de pagina **Meerontvangstcodes**. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).

### <a name="to-perform-an-over-receipt"></a>Een meerontvangst uitvoeren

Op inkoopregels en magazijnontvangstregels wordt het veld **Meer ontvangen hoeveelheid** gebruikt om meer ontvangen hoeveelheden vast te leggen, dat wil zeggen hoeveelheden die de waarde in het veld **Aantal**, het bestelde aantal, overschrijden.

Wanneer u een meerontvangst afhandelt, kunt u de waarde in het veld **Te ontvangen aantal** verhogen tot het werkelijk ontvangen aantal. Het veld **Meer ontvangen hoeveelheid** wordt dan bijgewerkt om de overtollige hoeveelheid weer te geven. U kunt ook de overtollige hoeveelheid invoeren in het veld **Meer ontvangen hoeveelheid**. Het veld **Te ontvangen aantal** wordt dan bijgewerkt om het bestelde aantal plus de overtollige hoeveelheid aan te geven. In de volgende procedure wordt beschreven hoe u het veld **Te ontvangen aantal** invult.  

1. Op een inkooporder of een magazijnontvangstdocument waarbij de ontvangen hoeveelheid hoger is dan besteld, voert u de werkelijk ontvangen hoeveelheid in het veld **Te ontvangen aantal** in.

    Als de verhoging binnen de tolerantie valt die is gespecificeerd door de toegewezen meerontvangstcode, wordt het veld **Meer ontvangen hoeveelheid** bijgewerkt om de hoeveelheid weer te geven waarmee de waarde in het veld **Aantal** is overschreden.

    Als de verhoging hoger is dan de opgegeven tolerantie, is de meerontvangst niet toegestaan. In dat geval kunt u onderzoeken of er een andere meerontvangstcode bestaat die dit toelaat. Anders kan alleen de bestelde hoeveelheid worden ontvangen en moet de overtollige hoeveelheid anders worden afgehandeld, bijvoorbeeld door deze terug te sturen naar de leverancier.

2. Boek de ontvangst zoals u zou doen voor elke andere ontvangst.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat geen functionaliteit om automatisch de financiële administratie van meerontvangsten te initiëren. U moet dit handmatig afhandelen in overleg met de leverancier, bijvoorbeeld doordat de leverancier een nieuwe of bijgewerkte factuur stuurt.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
