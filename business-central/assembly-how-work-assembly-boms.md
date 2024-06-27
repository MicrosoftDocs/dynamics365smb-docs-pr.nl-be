---
title: Werken met assemblagestuklijsten
description: U maakt een assemblagestuklijst om de onderdelen op te geven die vereist zijn om het artikel samen te stellen dat de assemblagestuklijst vertegenwoordigt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="work-with-assembly-boms"></a>Werken met assemblagestuklijsten

U gebruikt assemblagestuklijsten om hoofdartikelen te structureren die via onderdelen moeten worden geassembleerd met weinig tot geen resourcegebruik. Een assemblagestuklijst kan bijvoorbeeld worden gebruikt om een hoofdartikel als een pakket bestaande uit onderdeelartikelen te verkopen.

Gebruik assemblageorders voor het maken van voltooide artikelen van onderdelen in een eenvoudig proces dat kan worden uitgevoerd door een of meer standaardbronnen die geen bewerkingsplaatsen of -afdelingen betreffen of waarbij geen bronnen gebruikt worden. Een assemblageproces kan bijvoorbeeld zijn het picken van twee flessen wijn en één pak koffie en deze als een cadeau-item verpakken.  

Een assemblagestuklijst betreft de hoofdgegevens die bepalen welke onderdelen gebruikt worden in een samengesteld eindartikel en welke bronnen gebruikt worden voor het samenstellen van het assemblageartikel. Wanneer u een assemblageartikel en een hoeveelheid in een assemblageorder invoert, worden de assemblageorderregels ingevuld volgens de assemblagestuklijst. De order heeft één assemblageorderregel per component of resource. Zie voor meer informatie [Assemblagebeheer](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt ook productiestuklijsten. Productiestuklijsten verschillen van assemblagestuklijsten doordat er complexere procedures worden gehanteerd, waaronder het gebruik van resources, afdelingen of bewerkingsplaatsen. Zie voor meer informatie over de verschillen [Werken met stuklijsten](inventory-how-work-BOMs.md) en [Productiestuklijsten maken](production-how-to-create-production-boms.md).

## <a name="to-create-an-assembly-bom"></a>Een assemblagestuklijst maken

Als u een artikel wilt definiëren dat uit andere artikelen bestaat, en eventueel uit de resources waarmee het artikel wordt samengesteld, moet u een assemblagestuklijst maken.  

Assemblagestuklijsten kunnen meerdere niveaus bevatten, wat betekent dat een onderdeel op de assemblagestuklijst zelf ook een assemblageartikel kan zijn. In dat geval bevat het veld **Assemblagestuklijst** op de assemblagestuklijstregel **Ja**.

Er gelden speciale vereisten voor artikelen in assemblagestuklijsten met betrekking tot beschikbaarheid. Zie voor meer informatie [De beschikbaarheid van een artikel bekijken op basis van het gebruik ervan in assemblagestuklijsten](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Het maken van een assemblagestuklijst bestaat uit twee delen:

- Een nieuw artikel instellen.
- De stuklijststructuur van het assemblageartikel definiëren.

1. Stel een nieuw artikel in. Meer informatie op [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

   Ga verder om onderdelen of resources in de assemblagestuklijst in te voeren.  
2. Kies op de pagina **Artikel** voor een assemblageartikel de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.
3. Vul indien nodig de velden op de pagina **Assemblagestuklijst** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Assemblageartikelen kunnen varianten hebben, net als elk ander artikel, wat helpt uw lijst met producten korter te houden. Zie voor meer informatie over de functie [Productvarianten beheren](inventory-item-variants.md).

## <a name="to-edit-assembly-boms"></a>Assemblagestuklijsten bewerken

U kunt de regels op een assemblagestuklijst op elk gewenst moment bewerken. De stuklijst kan echter in gebruik zijn bij lopende verkopen of assemblages van de bovenliggende. Het wijzigen van de stuklijst kan van invloed zijn op deze activiteiten. Kies de actie **Waar gebruikt** om te zien in welke artikelen het wordt gebruikt en vervolgens of verkoop- of assemblageorders kunnen worden beïnvloed.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de waarde **Ja** in de kolom **Assemblagestuklijst**.
3. Kies op de pagina **Assemblagestuklijst** de actie **Lijst bewerken** en wijzig vervolgens desgewenst een veld.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Onderdelen en resources ingesprongen volgens de stuklijststructuur weergeven

Vanuit de pagina **Assemblagestuklijst** kunt u een afzonderlijke pagina openen die de onderdelen en resources bevat die zijn ingesprongen op basis van hun stuklijstpositie onder het assemblageartikel.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een assemblageartikel. (Het veld **Assemblagestuklijst** op de pagina **Artikelen** bevat **Ja**.)
3. Kies op de pagina **Artikel** de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.
4. Kies op de pagina **Assemblagestuklijst** de actie **Stuklijst weergeven**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Het assemblageartikel in documentregels vervangen door de samenstellende onderdelen

Vanuit ieder in- of verkoopdocument dat een assemblageartikel bevat, kunt u de regel voor dit artikel door middel van een speciale actie vervangen door nieuwe regels voor de samenstellende onderdelen ervan. Deze actie bijvoorbeeld nuttig als u de onderdelen wilt verkopen als een kit die samen het assemblageartikel vertegenwoordigen.

De actie **Stuklijst weergeven** is ook beschikbaar op de pagina **Assemblagestuklijst** als een methode om subassemblageartikelen in een assemblagestuklijst te bekijken.

> [!CAUTION]  
> Wanneer u de actie **Stuklijst weergeven** hebt gebruikt, kunt u dit niet gemakkelijk ongedaan maken. U moet de verkooporderregels voor de onderdelen verwijderen, en vervolgens opnieuw een verkooporderregel voor het assemblageartikel invoeren.

De volgende procedure is gebaseerd op een verkoopfactuur. Dezelfde stappen zijn van toepassing op andere verkoopdocumenten en op alle inkoopdocumenten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Open een verkoopfactuur die een regel voor een assemblageartikel bevat.
3. Kies de regel voor een assemblageartikel en selecteer vervolgens de regelactie **Stuklijst weergeven**.

Alle velden op de verkoopfactuurregel voor het assemblageartikel worden worden gewist, behalve de velden **Artikel** en **Beschrijving**. Volledige verkoopfactuurregels worden ingevoegd voor de onderdelen en mogelijke resources, waaruit het assemblageartikel is opgebouwd.

> [!NOTE]
> Het rapport **Picklijst per order** wordt ook gewijzigd om alleen de componenten weer te geven. Dit betekent dat een magazijnmedewerker die het bovenliggende artikel, het assemblageartikel, pickt, het niet zal zien in de picklijst. Zie voor meer informatie [De picklijst afdrukken](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>De vaste verrekenprijs van een assemblageartikel berekenen

U berekent de kostprijs van een assemblageartikel door de kostprijs van elk onderdeel en elke resource in de assemblagestuklijst bij elkaar op te tellen.

U kunt de vaste verrekenprijs voor een of meerdere artikelen ook berekenen en bijwerken op de pagina **Vaste-verrekenprijsvoorstel**. Zie voor meer informatie [Standaardkosten bijwerken](finance-how-to-update-standard-costs.md).  

De kostprijs van een assemblagestuklijst is altijd gelijk aan het totaal van de kostprijzen van de verschillende componenten, inclusief overige assemblagestuklijsten, en eventuele resources.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een assemblageartikel. (Het veld **Assemblagestuklijst** op de pagina **Artikelen** bevat **Ja**.)
3. Kies op de pagina **Artikelkaart** de actie **Assemblagestuklijst**.
4. Kies op de pagina **Assemblagestuklijst** de actie **Vaste verrekenprijs berekenen**.
5. Selecteer een van de volgende opties en kies de knop **OK**.

|Optie |Omschrijving |
|-------|------------|
|**Hoogste niveau**|Berekent de vaste verrekenprijs van het assemblageartikel als de totale kosten van alle gekochte of geassembleerde artikelen op die assemblagestuklijst, ongeacht eventuele onderliggende assemblagestuklijsten.|
|**Alle niveaus**|Berekent de vaste verrekenprijs van het assemblageartikel als de som van:</br></br>* De berekende kosten van alle onderliggende assemblagestuklijsten op de assemblagestuklijst.</br>* De kosten van alle ingekochte artikelen op de assemblagestuklijst.|

De kosten van de artikelen waaruit de assemblagestuklijst bestaat, worden gekopieerd van artikelkaarten van de componenten. De kosten van elk artikel worden vermenigvuldigd met het aantal, en de totale kostprijs wordt weergegeven in het venster **Kostprijs** op de artikelkaart.

## <a name="see-also"></a>Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Productvarianten beheren](inventory-item-variants.md)  
[De beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
