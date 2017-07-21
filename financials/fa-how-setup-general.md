---
title: Grootboek VA instellen| Microsoft Docs
description: Voordat u werkt met vaste activa, moet u standaardgrootboekrekeningen instellen, boekingsgroepen, verdeelsleutels, dagboeksjablonen en batches, en klassecodes.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 4a41abe08412b357207cbbc08e8dc5041b12d942
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-general-fixed-assets-information"></a>Procedure: Algemene gegevens voor vaste activa instellen
Voordat u vaste activa kunt beheren, moet u de standaardgrootboekrekeningen, verdeelsleutels, dagboeksjablonen en - batches instellen voor de boeking en herindeling van vaste activa en kunt u vaste activa in categorieën indelen, zoals materiële en immateriële activa.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Algemene standaardwaarden instellen voor vaste activa
U definieert het algemene gedrag of de functionaliteit voor vaste activa en stelt de documentnummerreeks in het venster **VA-instellingen** in.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-instellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Boekingsgroepen voor vaste activa instellen
Met behulp van boekingsgroepen kunt u groepen van vaste activa definiëren. Posten voor deze boekingsgroepen worden naar dezelfde grootboekrekeningen geboekt.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-productboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden in het venster **VA-boekingsgroep** in.

    > [!NOTE]  
>   Om ervoor te zorgen dat tegenrekeningen voor verschillende boekingen van vaste activa automatisch worden ingevoegd als u de actie **VA-tegenrekening invoegen** op dagboekregels kiest, voert u op basis van boeking van waardevermeerdering de volgende stap uit.
4. Selecteer op het sneltabblad **Tegenrekening** in het veld **Tegenrekening waardevermeerdering** de grootboekrekening waarnaar u tegenrekeningsposten wilt boeken voor afschrijving.

Zie voor meer informatie over het gebruik van de actie **VA-tegenrekening invoegen** voor regels van het financieel dagboek voor vaste activa bijvoorbeeld [Procedure: Vaste activa herwaarderen](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Verdeelsleutels voor vaste activa instellen
Transacties kunnen over diverse afdelingen of projecten worden verdeeld, volgens een zelfgedefinieerde verdeelsleutel. U kunt bijvoorbeeld een verdeelsleutel instellen waarbij de afschrijvingskosten op bedrijfswagens voor 35 procent worden toegewezen aan de administratie en voor 65 procent aan de verkoopafdeling. Zie voor meer informatie [Procedure: Kosten en inkomsten toewijzen](year-allocate-costs-income.md).

Verdeelsleutels zijn van toepassing op klassen voor vaste activa en niet op afzonderlijke activa.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-productboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in het venster **VA-boekingsgroepen** de actie **Verdeelsleutels** en kies vervolgens een boekingssoort.
3. Vul indien nodig in het venster **VA-verdeelsleutels** de velden in.
4. Herhaal stap 2 en 3 voor elk boekingssoort waarvoor u verdeelsleutels wilt definiëren.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Dagboeksjablonen voor vaste activa instellen
Een sjabloon is een vooraf gedefinieerd model voor een dagboek. De sjabloon bevat informatie over traceringscodes, lijsten en nummerreeksen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt automatisch een dagboeksjabloon voor vaste activa gemaakt als u het venster **Dagboek voor vaste activa** voor het eerst opent, maar het is ook mogelijk om extra dagboeksjablonen in te stellen.  

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-dagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Dagboekbatches voor vaste activa instellen
U kunt meerdere dagboekbatches instellen, die individuele dagboeken voor elke dagboeksjabloon zijn. Werknemers kunnen bijvoorbeeld hun eigen dagboekbatch hebben, waarbij de initialen van de werknemer als batchnaam worden gebruikt. Zie voor meer informatie [Werken met diversendagboeken](ui-work-general-journals.md).  

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-dagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de betreffende dagboeksjabloon en kies vervolgens de actie **Batches**.
3. Vul in het venster **VA-dagboekbatches** indien nodig de velden in.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Herindelingsdagboeksjablonen voor vaste activa instellen
U kunt specifieke herindelingsdagboeken gebruiken wanneer u vaste activa moet verplaatsen, combineren of splitsen. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt automatisch een herindelingsdagboeksjabloon voor vaste activa gemaakt wanneer u het venster **VA-herindelingsdagboek** voor het eerst opent, maar u kunt extra VA-herindelingsdagboeksjablonen instellen. Zie voor meer informatie [Werken met diversendagboeken](ui-work-general-journals.md).  

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-herindelingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Herindelingsdagboekbatches voor vaste activa instellen
U kunt meerdere dagboekbatches instellen, die individuele dagboeken voor elke herindelingsdagboeksjabloon zijn. Werknemers kunnen bijvoorbeeld hun eigen herindelingsdagboekbatch hebben, waarbij de initialen van de werknemer als herindelingsbatchnaam worden gebruikt. Zie voor meer informatie [Werken met diversendagboeken](ui-work-general-journals.md).

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-herindelingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de betreffende dagboeksjabloon en kies vervolgens de actie **Batches**.
3. Vul in het venster **VA-herindelingsdagboekbatches** indien nodig de velden in.

## <a name="to-set-up-fixed-asset-class-codes"></a>Categorieën voor vaste activa instellen
U kunt categorieën voor vaste activa gebruiken om vaste activa te groeperen, bijvoorbeeld in materiële en immateriële activa.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-klassen** in en kies vervolgens de gerelateerde koppeling.
2. Voer codes en namen in voor de categorieën die u wilt maken.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Subcategorieën voor vaste activa instellen
U kunt subcategorieën voor vaste activa gebruiken om uw vaste activa in categorieën te groeperen, bijvoorbeeld gebouwen, voertuigen, meubels of machines.  

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-subklassen** in en kies vervolgens de gerelateerde koppeling.
2. Voer codes en namen in voor de categorieën die u wilt maken.

## <a name="to-set-up-fixed-asset-location-codes"></a>Vestigingscodes voor vaste activa instellen
U gebruikt vestigingen voor vaste activa om de locatie van het vaste activum te registreren, bijvoorbeeld afdeling verkoop, receptie, administratie, productie of magazijn. Dit is nuttige informatie voor de verzekering en voorraadbepaling.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-locaties** in en kies vervolgens de gerelateerde koppeling.
2. Voer codes en namen in voor de vestigingen van vaste activa die u wilt maken.

## <a name="to-register-opening-entries"></a>Beginsaldi registreren
Als u de module Vaste activa in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor het eerst gebruikt, moet u eerst het toepassingsgebied Financieel instellen voordat u vaste activa gaat instellen. Bepalend voor de manier waarop deze informatie wordt ingevuld, is de vraag of vaste activa is geïntegreerd met het grootboek.  

 Als VA-transacties naar het grootboek moeten worden geboekt, wordt de onderstaande procedure gebruikt.  

1. Controleer of u de procedures voor de basisinstellingen van vaste activa hebt voltooid.  
2. Maak een kaart voor ieder bestaand activum.  
3. Stel VA-afschrijvingsboeken in.  
4. Schakel grootboekintegratie in door de volgende stappen uit te voeren.
5. Voer in het tekstvak **Zoeken** de tekst **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
6. De relevante afschrijvingsboekkaart selecteren. Kies op het tabblad **Start** in de groep **Beheren** de optie **Bewerken**, als u het venster **Afschrijvingsboek** wilt openen.
7. Schakel alle velden op het sneltabblad **Integratie** uit door de vinkjes te verwijderen. Als u meer dan één afschrijvingsboek hebt, schakelt u de grootboekintegratie voor elk afschrijvingsboek in.  
8. In het dagboek voor vaste activa voert u voor elk activum de volgende regels in:
   * Een regel met de aanschafkosten.
   * Een regel met de gecumuleerde afschrijving tot het einde van het vorige boekjaar.
   * Een regel met de gecumuleerde afschrijving vanaf het begin van het lopende boekjaar tot de datum waarop [!INCLUDE[d365fin](includes/d365fin_md.md)] is ingesteld om te beginnen met het berekenen van de afschrijving.

Als er nog andere beginsaldi zijn, kunt u deze nu ook invoeren, zoals waardevermindering\- en waardevermeerdering.  

Als de vaste activa niet zijn geïntegreerd met het grootboek, kunt u stap 4 tot en met 7 overslaan.

## <a name="see-also"></a>Zie ook
[Vaste activa instellen](fa-setup.md)  
[Vaste activa](fa-manage.md)  
[Financiën](finance.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

