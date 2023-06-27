---
title: Snel aan de slag met inkoop (bevat video)
description: 'Leer hoe u de eerste kritieke velden over leveranciers in Business Central invult, zodat u producten en services kunt gaan kopen.'
author: jill-kotel-andersson
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: '26, 27, 50, 56'
ms.date: 09/29/2021
ms.author: edupont
---

# <a name="procurement-quick-start"></a>Snel aan de slag met inkoop

Om producten en services te kunnen kopen moet u eerst leveranciers instellen. Zodra dat is gebeurd, kunt u beginnen met het registreren van inkooporders en het ontvangen van facturen.  

## <a name="set-up-vendors"></a>Leveranciers instellen

De volgende video laat zien hoe u een leverancier instelt in [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### <a name="set-up-a-new-vendor"></a>Een nieuwe leverancier instellen

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Voor meer informatie en aanvullende dingen die u kunt doen wanneer u leveranciers registreert zie [Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md).  

## <a name="create-new-purchase-orders"></a>Nieuwe inkooporders maken

Wanneer u iets van een verkoper koopt, hebt u twee opties. De eerste en eenvoudigste is om gewoon een inkoopfactuur te maken. U moet echter inkooporders gebruiken als uw inkoopproces vereist dat u gedeeltelijke ontvangsten van een orderhoeveelheid registreert, bijvoorbeeld omdat de volledige hoeveelheid niet beschikbaar was bij de leverancier.

De volgende video laat zien hoe u een inkooporder maakt in [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-order"></a>Een inkooporder maken

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  

2. Selecteer op de pagina **Inkooporders** de actie **Nieuw** om een nieuwe inkooporder te maken.

3. Voer in het veld **Leveranciersnaam** de naam in van een bestaande leverancier.

    Overige velden op de pagina **Inkoopkop** worden nu ingevuld met de standaardinformatie over de geselecteerde leverancier.  

4. Vul desgewenst de overige velden op de pagina **Inkooporder** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    U kunt nu de inkooporderregels invullen met artikelen of resources die u hebt gekocht van de leverancier.

5. Voer op het sneltabblad **Regels** in het veld **Artikelnr.** het nummer van een voorraadartikel of een service in.

6. Voer in het veld **Aantal** het in te kopen aantal van een artikel in.

    Het veld **Regelbedrag** wordt bijgewerkt met de waarde in het veld **Directe kostprijs**, vermenigvuldigd met de waarde in het veld **Aantal**.

7. Voer in het veld **Kortingbedrag order** een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw** onder in de order.

8. Als u de ingekochte artikelen of diensten ontvangt, kiest u **Boeken**.

Voor meer informatie en aanvullende dingen die u kunt doen bij het maken van een inkooporder zie [Inkoop](purchasing-manage-purchasing.md).  

## <a name="create-a-purchase-invoice"></a>Een inkoopfactuur maken

U maakt een inkoopfactuur om de kosten van inkopen vast te leggen en betalingsverplichtingen te volgen. Een inkoopfactuur maken is vergelijkbaar met het maken van een inkooporder.

### <a name="how-to-create-and-post-a-purchase-invoice"></a>Een inkoopfactuur maken en boeken

1. Kies het pictogram ![Lampje dat de functie Vertel me 3 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Inkoopfactuur** de actie **Nieuw** om een nieuwe inkoopfactuur te maken.
3. Voer in het veld **Leverancier** de naam in van een bestaande leverancier.

    Overige velden op de pagina **Inkoopfactuur** worden nu ingevuld met de standaardinformatie over de geselecteerde leverancier.

4. Vul desgewenst de overige velden op de pagina **Inkoopfactuur** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    U kunt nu de inkoopfactuurregels invullen met voorraadartikelen of resources die u hebt gekocht van de leverancier.

5. Voer op het sneltabblad **Regels** in het veld **Artikelnr.** het nummer van een voorraadartikel of een service in.
6. Voer in het veld **Aantal** het in te kopen aantal van een artikel in.

    Het veld **Regelbedrag** wordt bijgewerkt met de waarde in het veld **Directe kostprijs**, vermenigvuldigd met de waarde in het veld **Aantal**.

7. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw** onder in de factuur.

8. Als u de ingekochte artikelen of diensten ontvangt, kiest u **Boeken**.

De inkoop wordt nu weerspiegeld in de voorraad, resourcejournalen en financiële records, en de leveranciersbetaling wordt geactiveerd. De inkoopfactuur wordt verwijderd uit het overzicht met inkoopfacturen en wordt vervangen door een nieuw document in het overzicht van geboekte inkoopfacturen.  

Voor meer informatie en aanvullende dingen die u kunt doen bij het maken van een factuur zie [Aankopen registreren met inkoopfacturen](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Zie ook

[Snelstartgidsen voor Business Central](quick-start-business-central.md)  
[Inkoopoverzicht](Purchasing-manage-purchasing.md)  
[Aankopen registreren met inkoopfacturen](purchasing-how-record-purchases.md)  
