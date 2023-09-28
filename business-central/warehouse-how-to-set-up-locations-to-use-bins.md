---
title: Gebruik van opslaglocaties voor locaties instellen
description: Opslaglocaties vertegenwoordigen de standaard magazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# <a name="set-up-locations-to-use-bins"></a>Locaties instellen om opslaglocaties te gebruiken

Opslaglocaties vertegenwoordigen de basismagazijnstructuur, en u kunt ze gebruiken om te suggereren waar artikelen geplaatst moeten worden. Nadat u opslaglocaties hebt gemaakt, definieert u de inhoud van deze opslaglocaties of laat u ze dienen als vrije opslaglocaties zonder specifieke inhoud.

Als u de opslaglocatiefunctionaliteit op een locatie wilt gebruiken, schakelt u de schakelaar **Opslaglocatie verplicht** in op de kaart **Vestiging**. Nadat u de schakelaar hebt ingeschakeld, zijn de velden **Opslaglocatie** en **Zone** beschikbaar in de volgende documenten:

* Magazijnontvangstkop
* Magazijnontvangstregel
* Magazijnopslagregels
* Magazijnverzendkop
* Magazijnverzendregels
* Magazijnopslagregels

De volgende stap is het ontwerpen van de artikelstroom op de locatie door opslaglocatiecodes op te geven in instellingsvelden die de verschillende stromen vertegenwoordigen.  

> [!NOTE]  
> U moet opslaglocatiecodes maken voordat u deze voor de vestiging kunt opgeven. Zie voor meer informatie [Opslaglocaties maken](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Een vestiging instellen voor het gebruik van opslaglocaties

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de vestiging waarin u opslaglocaties wilt gebruiken.  
3. Kies de actie **Bewerken**.  
4. Schakel op het sneltabblad **Magazijn** het selectievakje **Opslaglocatie verplicht** in.  
5. Als u in de vestiging niet met gestuurde opslag en pick werkt, kiest u in het veld **Std. opslaglocatieselectie** de methode waarmee [!INCLUDE [prod_short](includes/prod_short.md)] een standaardopslaglocatie moet toewijzen aan een artikel.  
6. Open de kaart voor de vestiging waarvoor u opslaglocaties wilt instellen.
7. Selecteer op het sneltabblad **Opslaglocaties** de te gebruiken opslaglocaties als standaardopslaglocaties voor ontvangsten, verzendingen, inkomende en uitgaande opslaglocaties en open-shopflooropslaglocaties.  

    De opslagcodes die u hier specificeert, worden automatisch weergegeven op de koppen en daarna op de regels van verschillende magazijndocumenten. De standaardopslaglocaties bepalen alle begin- en eindplaatsingen van artikelen in het magazijn.  
8. Als u met gestuurde opslag en pick werkt, selecteer dan een opslaglocatie voor magazijncorrecties. De opslaglocatie in het veld **Correctieopslaglocatie** definieert een virtuele opslaglocatie om voorraadverschillen vast te leggen:

    * Wanneer u geregistreerde verschillen ziet in het magazijnartikeldagboek
    * verschillen die worden berekend wanneer u een inventarisatie registreert  
9. Optioneel: vul de velden op het sneltabblad **Opslaglocatiebeleid** in. De belangrijkste velden zijn **Opslaglocatiecapaciteitsbeleid**, **Breakbulk toestaan** en **Opslagsjabloon**.  
10. Vul op het sneltabblad **Magazijn** de velden **Uitslagtijd**, **Inslagtijd** en **Basisagendacode** in. Ga voor meer informatie naar [Basisagenda's instellen](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin"></a>De verbruiksopslaglocatie vullen

Het volgende stroomdiagram geeft weer hoe het veld **Opslaglocatie** op de productieordercomponentregels wordt ingevuld op basis van uw vestigingsinstellingen.

:::image type="content" source="media/binflow.png" alt-text="Bincodeveld op productieorder-materiaalregels.":::

## <a name="see-also"></a>Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
