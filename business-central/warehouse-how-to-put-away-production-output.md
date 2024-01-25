---
title: Productieoutput opslaan
description: In dit artikel wordt beschreven hoe u uw productieoutput kunt opslaan.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# Productie- of assemblageoutput opslaan

Hoe u de productieoutput opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

In standaardmagazijnconfiguraties waar voor uw vestiging opslagverwerking vereist is, gebruikt u het document **Voorraadopslag** om productieoutput te boeken en de opslag ervoor vast te leggen.  

> [!NOTE]  
> Assemblageprocessen ondersteunen geen voorraadopslag. U boekt een assemblageorder om output te registreren. Als u opslaglocaties gebruikt, kunt u artikelen later tussen de opslaglocaties verplaatsen. Zie voor meer informatie [Artikelen ad hoc verplaatsen in basismagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

In geavanceerde magazijnconfiguraties waar voor een vestiging zowel opslag- als ontvangstverwerking vereist is, kunt u een interne-opslagdocument of een verplaatsingsdocument maken om de output op te slaan.  

## Productieoutput opslaan met een voorraadopslag

De eerste stap bij het opslaan van output is het maken van het inkomende magazijnverzoek. Deze aanvraag informeert het magazijn dat de output van de productie- of assemblageorder gereed is voor opslag.

### Ink.magazijnontvangst maken  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vrijgegeven productieorder** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in de productieorder die gereed is voor opslag en kies dan de actie **Ink. magazijnontvangst maken**.  

> [!NOTE]  
> U kunt de inkomende magazijnaanvraag ook maken door het veld **Inkomend verzoek maken** te kiezen bij het vernieuwen van de productieorder. Zie voor meer informatie [Productieorders vernieuwen of opnieuw plannen](production-how-to-replan-refresh-production-orders.md).  

### Output opslaan met een voorraadopslag  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadopslag** in en kies vervolgens de gerelateerde koppeling.  
2. Een nieuwe voorraadopslag maken. Zie voor meer informatie [Artikelen opslaan met voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Kies de actie **Brondocumenten ophalen** en selecteer de vrijgegeven productieorder om de productieorderoutput te openen.  
4. Vul waar nodig de opslagregels in.
5. Wanneer de regels gereed zijn voor boeken, kiest u de actie **Boeken**. Boeken leidt tot het maken van de magazijnposten en tot het boeken van de output van de artikelen.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Het is ook mogelijk om rechtstreeks vanuit een vrijgegeven productieorder een **Voorraadopslag** te maken. Zie voor meer informatie [Artikelen opslaan met voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Wanneer u een voorraadopslag boekt, wordt ervan uitgegaan dat alle bewerkingen worden geboekt overeenkomstig het standaardbewerkingsplan. Dat wil zeggen, het outputaantal wordt geboekt op basis van de laatste bewerking. U kunt het outputdagboek gebruiken om verschillen in het outputaantal en de instel- en bewerkingstijd te boeken. Als u een gedeeltelijke boeking moet uitvoeren nadat u de voorraadopslag hebt gemaakt, kunt u dit doen voor insteltijden en hoeveelheden voor alle bewerkingen, behalve de laatste. De laatste bewerking wordt bestuurd door de voorraadopslag.  

Als u alleen instel- of bewerkingstijd hoeft te boeken voor de laatste bewerking, stelt u de outputhoeveelheid voor de laatste bewerking in op 0. U kunt ervoor kiezen om de laatste regel helemaal niet te boeken door deze te verwijderen.

## Assemblage en productieoutput opslaan in geavanceerde magazijnconfiguraties

Wanneer u de output van een productie- of assemblageorder boekt in een magazijn dat gestuurde opslag en pick gebruikt, wordt de output in de opslaglocatie geplaatst die is gedefinieerd in de productie- of assemblageorder. Zie [Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet) voor meer informatie over de verschillende manieren om artikelen in het magazijn met geavanceerde configuraties te verplaatsen.

> [!NOTE]  
> In geen van beide procedures (assembly- of productieoutput) kunt u het brondocumentnummer, zoals het productieordernummer invoeren in de documenten voor interne opslag, opslag of verplaatsing.  

## Zie ook  

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
