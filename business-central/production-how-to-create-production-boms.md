---
title: Productiestuklijsten maken
description: 'Leer hoe u een productiestuklijst (BOM), nieuwe versies van een productiestuklijst maakt en hoe u de formule voor het berekenen van hoeveelheden gebruikt.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'production bom, bills of material,'
ms.search.form: '911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818'
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-production-boms"></a>Productiestuklijsten maken

Een productiestuklijst bevat hoofdgegevens waarmee de onderdelen en subverzamelingen worden beschreven die worden gebruikt bij de productie van een hoofdartikel. Nadat een productieorder voor dat hoofdartikel is gemaakt, bepaalt de productiestuklijst de berekening van materiaalbehoeften zoals weergegeven op de pagina **Prod.-ordermaterialen**.

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt tevens assemblagestuklijsten. U gebruikt assemblageorders voor het maken van eindartikelen van onderdelen in een eenvoudig proces dat kan worden uitgevoerd door een of meer standaardbronnen die geen bewerkingsplaatsen of -afdelingen betreffen of waarbij geen bronnen gebruikt worden. Een assemblageproces kan bijvoorbeeld zijn het picken van twee flessen wijn en één pak koffie en deze als een cadeau-item verpakken. Zie voor meer informatie [Assemblagestuklijsten of productiestuklijsten](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> De app **Demogegevens van Contoso Coffee** bevat demonstratieproducten voor verschillende productiestuklijstscenario's die kunnen worden gebruikt in een testomgeving, ook tijdens een proef. Leer hoe u de gegevens voor Contoso Coffee instelt en vind handleidingen voor verschillende scenario's op [Inleiding tot de demogegevens voor Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).

Voordat u een bewerkingsplan kunt instellen, moet het volgende zijn gedaan:  

- Er zijn artikelkaarten gemaakt voor hoofdartikelen die onderdeel zijn van de productie. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).
- Er zijn productieresources ingesteld. Zie voor meer informatie [Afdelingen en bewerkingsplaatsen instellen](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a>Een productiestuklijst maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **productiestuklijsten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u de stuklijst wilt bewerken, stelt u het veld **Status** in op **Nieuw** of **In ontwikkeling**. Als u het wilt inschakelen, stelt u het veld **Status** in op **Gecertificeerd**.  

    Ga door om de regels van de productiestuklijst in te vullen.
5. Geef in het veld **Soort** aan of het artikel op deze stuklijstregel een gewoon artikel is of een productiestuklijst. Als het een productiestuklijst is, moet deze al bestaan als gecertificeerde productiestuklijst.  
6. Selecteer in het veld **Nr.** het artikel of de productiestuklijst in kwestie of typ deze in het veld.  
7. Geef in het veld **Aantal per** op hoeveel eenheden van het artikel er in een hoofdartikel gaan, bijvoorbeeld 4 wielen voor 1 auto.  
8. In het veld **Uitvalpercentage** kunt u een vast percentage opgeven voor uitval van materialen tijdens de productie. Wanneer materialen gereed zijn om te worden gebruikt in een vrijgegeven productieorder, wordt dit percentage opgeteld bij het verwachte aantal in het veld **Verbruiksaantal** in een productiedagboek. Zie voor meer informatie [Verbruik en output registreren](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Dit uitvalpercentage heeft betrekking op uitval van materialen tijdens de productie (bij het ophalen uit voorraad), terwijl het uitvalpercentage bij bewerkingsplanregels betrekking heeft op uitval van output (voordat deze bij de voorraad wordt geteld).  

9. In het veld **Bewerkingsplankoppeling** voert u een code in om het onderdeel aan een bepaalde bewerking te koppelen. Zie [Bewerkingsplankoppelingen maken](production-how-to-create-routings.md#to-create-routing-links) voor meer informatie.
10. Als u regels wilt kopiëren uit een bestaande productiestuklijst, kiest u **Stuklijst kopiëren** om bestaande regels te selecteren.  
11. Certificeer de productiestuklijst.  
12. U kunt nu het nieuwe bewerkingsplan aan de kaart van het desbetreffende productieartikel koppelen. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Als u de vaste verrekenprijs van het artikel opnieuw wilt berekenen, kiest u de actie **Productie** en vervolgens **Vaste verrekenprijs berekenen**.  

## <a name="to-create-a-new-version-of-a-production-bom"></a>Een nieuwe versie van een productiestuklijst maken

Nieuwe versies van productiestuklijsten worden bijvoorbeeld gebruikt wanneer een artikel wordt vervangen door een ander artikel of wanneer een klant een speciale versie van een product nodig heeft. Met behulp van het versieprincipe kunt u verschillende versies van een productiestuklijst beheren. De structuur van de productiestuklijstversie komt overeen met de structuur van de productiestuklijsten. Het belangrijkste verschil is de geldigheidsduur van de versies. De geldigheid wordt bepaald door de begindatum.  

De begindatum geeft het begin aan van de periode waarin deze versie geldig is. De begindatum wordt gebruikt als filtercriterium voor berekeningen en evaluaties. De stuklijstversie is geldig tot aan de begindatum van de volgende versie.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **productiestuklijsten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de productiestuklijst die u wilt kopiëren en kies vervolgens de actie **Versies**.  
3. Kies de actie **Nieuw**.  
4. Vul de vereiste velden in.
5. Voer in het veld **Versiecode** de unieke identificatie van de versie in. Alle combinaties van cijfers en letters zijn toegestaan.  

    De nieuwe versie krijgt automatisch de status **Nieuw**.
6. Wanneer de stuklijstversie is voltooid, wordt het veld **Status** ingesteld op **Gecertificeerd**.  

De geldigheid van de versie wordt aangegeven in het veld **Begindatum**.  

> [!NOTE]  
> Selecteer de optie **Artikel** in het veld **Soort** als u een artikel wilt gebruiken uit uw overzicht met artikelgegevens in de productiestuklijst. Als het artikel ook een productiestuklijst bevat (waarbij het veld **Prod.-stuklijstnr.** is ingevuld op de artikelkaart), wordt de productiestuklijst meegenomen in de berekening.  
>
> Selecteer de optie **Productiestuklijst** als u een phantom-productiestuklijst wilt gebruiken op de regel.  
>
> Met behulp van phantom-productiestuklijsten kunt u producten structureren. Dit type productiestuklijst levert nooit een gereedgemeld product op, maar wordt alleen gebruikt om de afhankelijke vraag te bepalen. Voor phantom-productiestuklijsten bestaan geen artikelgegevens in de module Voorraad.

## <a name="quantity-calculation-formula-on-production-boms"></a>Formule voor berekening van het aantal in productiestuklijsten

Bij de berekening van het aantal wordt rekening gehouden met de verschillende dimensies die ook op de productiestuklijstregels zijn ingevoerd. De dimensies verwijzen naar een ordereenheid van het desbetreffende artikel. Lengte, breedte, hoogte en gewicht kunnen als dimensies worden ingevoerd.  

De kolommen Berekeningsformule, Lengte, Breedte, Hoogte en Gewicht worden niet weergegeven, omdat ze slechts door een aantal gebruikers worden gebruikt. U moet deze kolommen eerst weergeven als u de berekening wilt instellen en uitvoeren.  

De relatie tussen de afzonderlijke materialen wordt bepaald in de berekeningsformule. De volgende opties zijn beschikbaar als berekeningsformule:  

- **Leeg**: dimensies worden niet meegenomen in de berekening. (Aantal per = Aantal.)  
- **Lengte** - Aantal = Aantal per * Lengte  
- **Lengte x Breedte** - Aantal = Aantal per * Lengte x Breedte  
- **Lengte x Breedte x Diepte** - Aantal = Aantal per x Lengte x Breedte x Diepte  
- **Gewicht** - Aantal = Aantal per x Gewicht  
- **Vast aantal** - Aantal = Aantal per

> [!NOTE]
> De berekeningsformule **Vast aantal** zorgt ervoor dat het verbruik van een onderdeel hetzelfde is, ongeacht de uitval- of uitvoerhoeveelheden. Voor productieordermaterialen, wanneer het veld **Berekeningsformule** is ingesteld op **Vast aantal**, is de veldwaarde voor **Verwachte hoeveelheid** altijd gelijk aan het veld **Aantal per**. Het uitvalpercentage dat op dezelfde regel is gedefinieerd, wordt genegeerd. Het rapport **Beschikbaarheid per stuklijst** houd rekening met Vast aantal. Het rapport toont het artikel als het knelpunt als de beschikbare hoeveelheid kleiner is dan de hoeveelheid in het veld **Aantal per bovenliggend artikel**. De velden **Bovenliggende kan worden gemaakt** en **Topartikel kan worden gemaakt** zijn altijd leeg, ongeacht de beschikbare hoeveelheid. Vast aantal wordt ook meegenomen in berekeningen voor standaardkosten. De partijgrootte voor het geproduceerde artikel is van invloed op de kosten die voor één artikel worden toegewezen.

### <a name="example"></a>Opmerking

Een productiestuklijst vereist 70 metalen onderdelen met de volgende dimensies: lengte = 0,20 m en breedte = 0,15 m. De waarden worden als volgt ingevoerd: Berekeningsformule = Lengte x Breedte, Lengte = 20, Breedte = 15, Aantal per = 70. Het aantal wordt als volgt berekend: Aantal per x Lengte * Breedte, dat wil zeggen Aantal = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a>Zie ook

[Bewerkingsplannen maken](production-how-to-create-routings.md)  
[Productvarianten beheren](inventory-item-variants.md)  
[Procedure: varianten](contoso-coffee/manufacturing/variants.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Gepland](production-planning.md)  
[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
