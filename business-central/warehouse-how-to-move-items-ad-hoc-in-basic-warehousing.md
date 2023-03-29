---
title: Artikelen ongepland verplaatsen in standaard magazijnconfiguraties
description: In dit artikel worden ongeplande interne verplaatsingen tussen opslaglocaties zonder vraag vanuit een brondocument uitgelegd.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# Artikelen intern verplaatsen in standaardmagazijnconfiguraties

U kunt desgewenst artikelen tussen opslaglocaties verplaatsen zonder een vraag van een brondocument. Bijvoorbeeld als onderdeel van de volgende activiteiten:

* Uw magazijn reorganiseren.
* Artikelen naar een inspectiegebied brengen.
* Extra artikelen van en naar een productiegebied verplaatsen. 

Hoe u artikelen verplaatst, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

In magazijnconfiguraties waar de schakelaar **Opslaglocatie verplicht** is ingeschakeld, maar niet de schakelaar **Gestuurde opslag en pick**, kunt u ongeplande verplaatsingen registreren op de volgende pagina's:  

* Op de pagina **Interne verplaatsing**.
* Op de pagina **Artikelherindelingsdagboek**.  

## Interne verplaatsingen

Op de pagina **Interne verplaatsingen** kunt u regels voor Nemen en Plaatsen opgeven wanneer er geen vraag is vanuit een brondocument. De pagina Interne verplaatsing is als een werkblad om dingen te organiseren. U kunt de daadwerkelijke beweging er niet direct uit verwerken. Wanneer een regel is ingevuld, gebruikt u de actie **Voorraadverplaatsing maken** om de regel naar de pagina **Voorraadverplaatsing** pagina te sturen, waar u de beweging verwerkt en registreert.

### Items verplaatsen als een interne verplaatsing

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Interne verplaatsingen** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Zorg ervoor dat het veld **Nee.** op het sneltabblad **Algemeen** is ingevuld.
3. Voer in het veld **Locatiecode** de locatie in waar de verplaatsing plaatsvindt.  

    Indien de vestiging uw standaardvestiging is, wordt de vestigingscode automatisch toegevoegd.  
4. Voer in het veld **Naar opslaglocatie** de code in voor de opslaglocatie waar u de artikelen naar wilt verplaatsen.

    Voor productiedoeleinden kan dit bijvoorbeeld de opslaglocatie voor de grijpvoorraadlocatie kunnen zijn, zoals gedefinieerd op de vestigingskaart of afdeling.  
5. Voer in het veld **Vervaldatum** de datum in waarop de verplaatsing moet worden voltooid.  
6. Vul de velden indien nodig op elke regel in. Interne verplaatsingsdocumenten hebben één regel per verplaatsing. De regel bevat zowel de actie Nemen als de actie Plaatsen.
7. Kies het veld **Artikelnr.** om de pagina **Opslaglocatie-inhoudsoverzicht** te openen. Selecteer het artikel dat u wilt verplaatsen op basis van de beschikbaarheid in opslaglocaties. U kunt ook de actie **Opslaglocatie-inhoud ophalen** kiezen om de interne verplaatsingsregels in te vullen op basis van uw filters.  

    Nadat u het artikel hebt geselecteerd, wordt het veld **Van opslaglocatie** automatisch ingevuld op basis van de geselecteerde opslaglocatie-inhoud. U kunt elke opslaglocatie kiezen waar het artikel beschikbaar is. De velden **Artikelnr.** en **Van opslaglocatie** zijn gerelateerd. Het wijzigen van de waarde in het ene veld kan de waarde in het andere wijzigen.  

    Het veld **Van opslaglocatie** wordt ingevuld met de waarde die u in de kop hebt ingevoerd. U kunt deze online wijzigen in elke andere opslaglocatie die niet is geblokkeerd of bestemd is voor speciale doeleinden. Zie voor meer informatie [Het veld Speciaal](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Nadat u hebt bepaald van en naar welke opslaglocatie u de artikelen wilt verplaatsen, voert u het te verplaatsen aantal in het veld **Aantal** in.  

    > [!NOTE]  
    > Het aantal moet beschikbaar zijn in de opslaglocatie die is opgegeven in het veld **Van opslaglocatie**.  

9. Als u klaar bent om de verplaatsing te verwerken, kiest u de actie **Voorraadverplaatsing maken**.  

    > [!NOTE]  
    >  Nadat u de verplaatsing hebt gemaakt, worden de regels van de interne verplaatsing verwijderd.  

U voert de rest van de ongeplande verplaatsing op de pagina **Voorraadverplaatsing** op dezelfde manier uit als bij een verplaatsing op basis van brondocumenten.

### De voorraadverplaatsing registreren

1. Open op de pagina **Voorraadverplaatsing** het document waarvoor u de verplaatsing wilt vastleggen.  
2. In het veld **Opslaglocatie** op de verplaatsingsregels, is de opslaglocatie waar artikelen moeten worden gepickt de opslaglocatie waar het artikel beschikbaar is. U kunt de opslaglocatie indien nodig wijzigen.
3. Voer de verplaatsing uit en voer het verplaatste aantal in het veld **Te verwerken aantal** in. De waarde op de nemen- en plaatsen-regels moet hetzelfde zijn. Anders kunt u de verplaatsing niet registreren.

    Als het nodig is de artikelen voor een regel uit meerdere opslaglocaties te nemen, bijvoorbeeld omdat een opslaglocatie niet de volledige hoeveelheid bevat, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.  
4. Kies de actie **Voorraadverplaatsing registreren**.  

Het volgende gebeurt tijdens het boekingsproces:

* Magazijnboekingen geven aan dat het aantal is overgebracht van de 'Nemen'-opslaglocaties naar de 'Plaatsen'-opslaglocaties.

## Artikelen verplaatsen met het artikelherindelingsdagboek

In plaats van verplaatsingdocumenten te gebruiken, kunt u verplaatsingen registreren door hun opslaglocaties op artikelen opnieuw in te delen. Zie voor meer informatie [Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Verplaatsingen die zijn geboekt met herindelingsdagboeken, maken de verplaatsingsdocumenten niet gereed voor verplaatsing.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mag.-herindelingsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Definieer op elke dagboekregel de opslaglocaties waaruit en waarnaar u items wilt verplaatsen door de velden **Opslaglocatie** en **Nieuwe opslaglocatie** in te vullen.  

    1. Als u de gehele inhoud van een opslaglocatie wilt verplaatsen naar een andere opslaglocatie, kiest u de actie **Opslaglocatie-inhoud ophalen**.  
    2. Gebruik de filters voor het zoeken naar de opslaglocatie met de artikelen die u wilt verplaatsen en kies **OK**. De dagboekregels worden gevuld met de inhoud van de opslaglocatie.  
3. Vul de overige velden op elke dagboekregel in.
4. Boek het herindelingsdagboek.  

## Zie gerelateerde [Microsoft-training](/training/modules/manage-internal-warehouse-processes/)

## Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
