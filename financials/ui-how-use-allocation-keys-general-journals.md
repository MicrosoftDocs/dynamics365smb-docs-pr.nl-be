---
title: 'Procedure: Verdeelsleutels in dagboeken gebruiken | Microsoft Docs'
description: Leren hoe u verdeelsleutels in dagboeken gebruikt.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bbacf9b5634d51478dd4d54ac4b587ea9bfaaf99
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-allocation-keys-in-general-journals"></a>Procedure: verdeelsleutels in dagboeken gebruiken
U kunt een post in een dagboek verdelen over verschillende rekeningen wanneer u het dagboek boekt. De verdeling kan plaatsvinden op basis van aantal, percentage of bedrag.

## <a name="to-set-up-allocation-keys"></a>Verdeelsleutels instellen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Periodiek dagboek** in en kies vervolgens de gerelateerde koppeling.
2. Kies het veld **Batchnaam** om het venster **Fin. dagboekbatches** te openen.
3. U kunt verdeelsleutels in een bestaande batch in de lijst wijzigen of u kunt een nieuwe batch met verdeelsleutels maken.
   * Als u een nieuwe batch wilt maken, kiest u de actie **Nieuw** en gaat u naar de volgende stap.
   * Als u de verdeelsleutels van een bestaand dagboek wilt wijzigen, selecteert u het dagboek en gaat u naar stap 7.    
4. Voer in het veld **Naam** een naam voor de batch in, bijvoorbeeld Schoonmaak. Voer in het veld **Omschrijving** een omschrijving in, bijvoorbeeld Dagboek schoonmaakkosten.
5. Wanneer u klaar bent, sluit u het venster. Er wordt een nieuw, leeg periodiek dagboek geopend.
6. Vul de velden op de regel in.
7. Kies de actie **Verdeelsleutels**.
8. Voeg voor elke verdeelsleutel een regel toe. U moet ofwel het veld **Verdeelsleutel %**, of **Verdeelsleutelaantal**, of **Bedrag** invullen. U moet ook het veld **Rekeningnr.** invullen en, als u de transactie verdeelt over globale dimensies, ook de globale dimensievelden.
9. Als u een percentage op de regel invoert, wordt het bedrag in het veld **Bedrag** automatisch berekend. Deze bedragen hebben het tegengestelde teken van het totale bedrag in het veld **Bedrag** in het periodieke dagboek.
10. Kies **OK** na het invoeren van de verdeelsleutelregels om terug te keren naar het venster **Periodiek dagboek**. Het veld **Verdeeld bedrag (LV)** wordt ingevuld en de inhoud komt overeen met het veld **Bedrag**.
11. Boek het dagboek.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Een reeds ingestelde verdeelsleutel wijzigen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Periodiek dagboek** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer in het venster **Periodiek dagboek** het dagboek met de verdeling.
3. Kies de regel met de verdeelsleutel en kies vervolgens **Verdeelsleutels**.
4. Pas de relevante velden aan en kies vervolgens de knop **OK**.

## <a name="see-also"></a>Zie ook
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
