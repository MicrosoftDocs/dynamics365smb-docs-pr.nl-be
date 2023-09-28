---
title: Nummerreeksen maken
description: Leren hoe u nummerreeksen instelt die unieke id-codes toewijzen aan rekeningen en documenten in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 03/24/2022
ms.author: bholtorf
---
# <a name="create-number-series"></a>Nummerreeksen maken

Voor elk bedrijf dat u instelt, moet u unieke id-codes toewijzen aan zaken als grootboekrekeningen, klanten- en leveranciersrekeningen, facturen en overige documenten. De nummering is niet alleen belangrijk voor identificatie. Met een goed opgezet nummeringssysteem kan het bedrijf ook beter worden beheerd en geanalyseerd en kan het aantal fouten tijdens gegevensinvoer worden beperkt.

> [!Important]
> Standaard zijn hiaten niet toegestaan in nummerreeksen, omdat de exacte geschiedenis van financiële transacties wettelijk beschikbaar moet zijn en daarom een ononderbroken reeks zonder verwijderde nummers moet volgen.
> 
> Als u hiaten in bepaalde nummerreeksen wilt toestaan, raadpleegt u eerst uw auditor of boekhoudkundige manager om ervoor te zorgen dat u zich houdt aan de wettelijke vereisten in uw land/regio. Zie voor meer informatie de sectie [Hiaten in nummerreeksen](#gaps-in-number-series).

> [!NOTE]  
> Het wordt aanbevolen om dezelfde nummerreekscodes te gebruiken die worden vermeld op de pagina **Nr.-reeksoverzicht** in het voorbeeldbedrijf CRONUS. Codes zoals *I-FACT+* lijken in het begin mogelijk betekenisloos, maar [!INCLUDE[prod_short](includes/prod_short.md)] kent een aantal standaardinstellingen die afhankelijk zijn van deze codes.

U maakt een nummeringssysteem door een of meer codes in te stellen voor elk soort hoofdgegevens of document. U kunt bijvoorbeeld een code instellen voor het nummeren van klanten, een andere code voor het nummeren van verkoopfacturen en weer een andere code voor het nummeren van documenten in algemene dagboeken. Nadat u een code hebt ingesteld, moet u minimaal één nummerreeksregel instellen. De nummerreeksregel bevat gegevens, zoals het eerste en laatste nummer in de reeks en de begindatum. U kunt meer dan één nummerreeksregel per nummerreekscode invoeren, met een andere begindatum voor elke regel. De reeks wordt opeenvolgend gebruikt, waarbij elke reeks wordt gestart op de betreffende begindatum.

> [!NOTE]
> De maximale lengte van een nummer in een cijferreeks is 20 tekens. Er zijn enkele situaties waarin [!INCLUDE[prod_short](includes/prod_short.md)] een nummer toevoegt met een door het systeem gegenereerde id. Bijvoorbeeld wanneer documenten zoals facturen worden gebruikt om transacties toe te passen, zoals betalingen, genereert [!INCLUDE[prod_short](includes/prod_short.md)] identifiers voor de toegepaste transacties. De id bestaat uit een nummer uit een nummerreeks en een door het systeem toegewezen id van zes tekens, zoals -12345. Als u verwacht meer dan 9999 documenten in bank- of girojournalen of ontvangstendagboeken te verwerken, stelt u nummerreeksen in voor die typen documenten om minder dan 14 tekens te bevatten.

U configureert normaal gesproken de nummerreeks zodanig dat automatisch het eerstvolgende nummer wordt ingevoegd op nieuwe kaarten of documenten die u maakt. U kunt echter ook een nummerreeks instellen die toestaat dat u handmatig het nieuwe nummer invoert. U geeft dit aan met het selectievakje **Handm. nummering**.

Als u meer dan één nummerreekscode wilt gebruiken voor één soort hoofdgegevens (als u bijvoorbeeld verschillende nummerreeksen voor verschillende artikelcategorieën wilt gebruiken), kunt u relaties tussen nummerreeksen gebruiken.

## <a name="gaps-in-number-series"></a>Hiaten in nummerreeksen
Niet alle records die u maakt in [!INCLUDE[prod_short](includes/prod_short.md)], zijn financiële transacties die opeenvolgende nummering moeten gebruiken. Klantenkaarten, verkoopoffertes en magazijnactiviteiten zijn voorbeelden van records waaraan een nummer uit een nummerreeks wordt toegewezen, maar die niet worden onderworpen aan financiële controle en/of kunnen worden verwijderd. Voor dergelijke nummerreeksen kunt u het selectievakje **Lacunes in nummers toestaan** inschakelen op de pagina **Nr.-reeksregels**. Deze instelling kan ook worden gewijzigd nadat de nummerreeks is gemaakt. Zie [Een nieuwe nummerreeks maken](ui-create-number-series.md#to-create-a-new-number-series) voor meer informatie.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Werking van het veld Nr. in documenten en kaarten

In verkoop-, inkoop-, en transferdocumenten en op alle kaarten kan het veld **Nr.** automatisch vanuit een vooraf gedefinieerde nummerreeks worden ingevuld en u kunt het handmatig toevoegen. Onder bepaalde omstandigheden is het veld **Nr.** onzichtbaar om te voorkomen dat u het bewerkt.  

Het veld **Nr.** kan op drie manieren worden gevuld:

1. Als er slechts één nummerreeks voor het soort document of kaart bestaat waarbij het veld **Autom. nummering** is ingeschakeld en het veld **Handm. nummering** niet is ingeschakeld, wordt het veld automatisch gevuld met het volgende nummer in de reeks. Het veld **Nr.** is niet zichtbaar op de kaart of het document.  

    Zelfs als u sjablonen met verschillende nummerreeksen voor klanten definieert, als de nummerreeksen die zijn gedefinieerd op de pagina **Verkoopinstellingen** op deze manier zijn opgezet, is het veld **Nr.** onzichtbaar zijn op de klantenkaart, ongeacht welke sjabloon u gebruikt. Hetzelfde geldt voor andere soorten kaarten en documenten.  

    > [!NOTE]  
    > Als de nummerreeks niet werkt, bijvoorbeeld omdat de nummers op zijn, is het veld **Nr.** zichtbaar en kunt u handmatig een nummer invoeren of de problemen oplossen op de pagina **Nr.-reeks**.

2. Als er meer dan één nummerreeks voor het soort document of kaart bestaat en het selectievakje **Autom. nummering** niet is ingeschakeld voor de nummerreeks die momenteel is toegewezen, is het veld **Nr.** zichtbaar en kunt u opzoeken naar de pagina **Nr.-reeks** en de nummerreeks selecteren die u wilt gebruiken. Het volgende nummer in de reeks wordt dan ingevoegd in het **Nr.** veld.

3. Als u geen nummerreeks voor het type document of kaart hebt ingesteld of als het veld **Handm. nummering** is ingeschakeld voor de nummerreeks, is het veld **Nr.** zichtbaar en moet u het nummer handmatig invoeren. U kunt maximaal 20 tekens invoeren (cijfers en/of letters).

Wanneer u een nieuwe kaart of document opent waarvoor een nummerreeks bestaat, wordt de relevante pagina **Instelling nummerreeks** geopend, zodat u een nummerreeks kunt instellen voor dat type document of kaart voordat u doorgaat met verdere gegevensinvoer.

> [!NOTE]  
> Als u handmatige nummering moet inschakelen op, bijvoorbeeld, nieuwe artikelkaarten die zijn gemaakt met een gegevensmigratieproces, waarop het **Nr.** standaard is verborgen, gaat u naar de pagina **Voorraadinstellingen** en kiest u het veld **Artikelnrs.** om de gerelateerde nummerreeks te openen en in te stellen op **Handm. nummering**.

## <a name="to-create-a-new-number-series"></a>Een nieuwe nummerreeks maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Nr.-reeks** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.  
3. Vul op de nieuwe regel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Kies de actie **Regels**.  
5. Vul op de pagina **Nr.-reeksregels** de velden in om het daadwerkelijke gebruik en de inhoud van de nummerreeks die u in stap 2 hebt gemaakt, te definiëren.  
6. Herhaal stap 5 voor zo veel verschillende toepassingen van de nummerreeks die u nodig hebt. Het veld **Begindatum** definieert welke nummerreeksregel actief is.  

> [!TIP]
> Om gebruikers in staat te stellen handmatig nummers op te geven wanneer ze bijvoorbeeld een nieuwe klant of leverancier registreren, kiest u het veld **Handm. nummering** voor de nummerreeks zelf. Wis het veld om handmatige nummering niet toe te staan.

U kunt nummerreeksen toewijzen aan de sjablonen die u instelt voor de verschillende soorten klanten en leveranciers die uw verkopers en inkopers het vaakst toevoegen aan uw [!INCLUDE [prod_short](includes/prod_short.md)]. Stel in dat geval de relevante nummerreeksen in, koppel ze via relaties en voeg vervolgens de eerste nummerreeks in de relevante relatie toe aan de relevante instellingenpagina. Wanneer een gebruiker vervolgens een klant aanmaakt, kiest hij de relevante sjabloon en krijgt de nieuwe klant een nummer toegewezen uit de nummerreeks die voor die sjabloon is gedefinieerd.  

## <a name="to-create-relationships-between-number-series"></a>Relaties maken tussen nummerreeksen

Als u meerdere nummerreekscodes hebt ingesteld voor hetzelfde soort basisgegevens of transacties, kunt u relaties tussen de codes instellen. Met deze functie kunt u een code kiezen wanneer u een nummer gebruikt. Als u een relatie instelt tussen een verzameling nummerreeksen, koppelt u alle gekoppelde reeksen aan één nummerreekscode. Vervolgens kunt u die code invoeren in een veld op het sneltabblad **Nummering** op een van de relevante instellingenpagina's, zoals **Verkoopinstellingen**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Nr.-reeks** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel met de nummerreeks waarvoor u relaties wilt instellen en kies vervolgens **Relaties**.
3. Geef in het veld **Reeks** de code op voor de nummerreeks die u wilt koppelen aan de reeks die u in stap 2 hebt geselecteerd.
4. Voeg een regel toe voor elke code die u wilt koppelen aan de geselecteerde nummerreeksen.
5. Sluit de pagina.

Wanneer u nu iets instelt waarvoor u een nummer nodig hebt, kunt u de relaties gebruiken die u hebt ingesteld om te kiezen tussen de gekoppelde nummerreeksen.

## <a name="to-set-up-where-a-number-series-is-used"></a>Instellen waar een nummerreeks wordt gebruikt

In de volgende procedure wordt beschreven hoe u nummerreeksen instelt voor de module Verkoop. De stappen zijn vergelijkbaar voor andere modules.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Verkopen en klanten** op het sneltabblad **Nummerreeksen** de gewenste nummerreeksen voor iedere verkoopkaart of -document.

Het geselecteerde nummer wordt nu ingevuld op het veld **Nr.** op de kaart of het document, afhankelijk van de instellingen die u hebt ingevoerd op de nummerreeksregel.  

## <a name="see-also"></a>Zie ook

[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
