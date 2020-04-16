---
title: Verdeelsleutels in dagboeken gebruiken | Microsoft Docs
description: Leren hoe u verdeelsleutels in dagboeken gebruikt.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 408dfeaeb56f271a2b9b3d5cf515e41abeaf78e8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195567"
---
# <a name="use-allocation-keys-in-general-journals"></a>Verdeelsleutels in dagboeken gebruiken
U kunt een post in een dagboek verdelen over verschillende rekeningen wanneer u het dagboek boekt. De verdeling kan plaatsvinden op basis van aantal, percentage of bedrag.

## <a name="to-set-up-allocation-keys"></a>Verdeelsleutels instellen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodiek dagboek** in en kies de desbetreffende koppeling.
2. Kies het veld **Batchnaam** om de pagina **Fin. dagboekbatches** te openen.
3. U kunt verdeelsleutels in een bestaande batch in de lijst wijzigen of u kunt een nieuwe batch met verdeelsleutels maken.
   * Als u een nieuwe batch wilt maken, kiest u de actie **Nieuw** en gaat u naar de volgende stap.
   * Als u de verdeelsleutels van een bestaand dagboek wilt wijzigen, selecteert u het dagboek en gaat u naar stap 7.    
4. Voer in het veld **Naam** een naam voor de batch in, bijvoorbeeld Schoonmaak. Voer in het veld **Omschrijving** een omschrijving in, bijvoorbeeld Dagboek schoonmaakkosten.
5. Wanneer u klaar bent, sluit u de pagina. Er wordt een nieuw, leeg periodiek dagboek geopend.
6. Vul de velden op de regel in.
7. Kies de actie **Verdeelsleutels**.
8. Voeg voor elke verdeelsleutel een regel toe. U moet ofwel het veld **Verdeelsleutel %**, of **Verdeelsleutelaantal**, of **Bedrag** invullen. U moet ook het veld **Rekeningnr.** invullen. Als u de transactie wilt toewijzen aan verschillende globale dimensies, moet u ook de globale dimensievelden invullen.
9. Als u een percentage op de regel invoert, wordt het bedrag in het veld **Bedrag** automatisch berekend. Deze bedragen hebben het tegengestelde teken van het totale bedrag in het veld **Bedrag** in het periodieke dagboek.
10. Kies **OK** na het invoeren van de verdeelsleutelregels om terug te keren naar de pagina **Periodiek dagboek**. Het veld **Verdeeld bedrag (LV)** wordt ingevuld en de inhoud komt overeen met het veld **Bedrag**.
11. Boek het dagboek.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Een reeds ingestelde verdeelsleutel wijzigen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodiek dagboek** in en kies de desbetreffende koppeling.
2. Selecteer op de pagina **Periodiek dagboek** het dagboek met de verdeling.
3. Kies de regel met de verdeelsleutel en kies vervolgens **Verdeelsleutels**.
4. Pas de relevante velden aan en kies vervolgens de knop **OK**.

## <a name="see-also"></a>Zie ook
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
