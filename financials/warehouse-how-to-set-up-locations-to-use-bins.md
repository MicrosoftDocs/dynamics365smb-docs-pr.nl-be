---
title: Gebruik van opslaglocaties voor locaties instellen | Microsoft Docs
description: "Opslaglocaties vertegenwoordigen de standaard magazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen. Wanneer u uw opslaglocaties hebt gemaakt, kunt u de inhoud die u in de afzonderlijke opslaglocaties wilt plaatsen bijzonder gedetailleerde definiëren. De opslaglocatie kan echter ook functioneren als een vrije opslaglocatie zonder opgegeven inhoud."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7fa813b2bbaffe72a0f697101f1c10883cf54f2d
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations-to-use-bins"></a>Procedure: gebruik van opslaglocaties voor locaties instellen
Opslaglocaties vertegenwoordigen de standaardmagazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen. Wanneer u uw opslaglocaties hebt gemaakt, kunt u de inhoud die u in de afzonderlijke opslaglocaties wilt plaatsen bijzonder gedetailleerde definiëren. De opslaglocatie kan echter ook functioneren als een vrije opslaglocatie zonder opgegeven inhoud.  

Als u de opslaglocatiefunctionaliteit op een locatie wilt gebruiken, moet u deze eerst activeren op de **Vestigingskaart**. U ontwerpt vervolgens de artikelstroom op de locatie door de opslaglocatiecodes op te geven in de instellingsvelden voor de verschillende stromen.  

> [!NOTE]  
>  Voordat u opslaglocatiecodes op de vestigingskaart kunt opgeven, moeten de opslaglocatiecodes worden gemaakt. Zie [Procedure: Opslaglocaties maken](warehouse-how-to-create-individual-bins.md) voor meer informatie.  

## <a name="to-set-up-a-location-to-use-bins"></a>Een vestiging instellen voor het gebruik van opslaglocaties  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vestigingen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de vestiging waarin u opslaglocaties wilt gebruiken.  
3.  Kies de actie **Bewerken**.  
4.  Schakel op het sneltabblad **Magazijn** het selectievakje **Opslaglocatie verplicht** in.  
5.  Als u in de vestiging niet met gestuurde opslag en pick werkt, vult u in het veld **Std. opslaglocatieselectie** de methode in waarmee standaardopslaglocaties aan artikelen worden toegewezen.  
6.  Open de kaart voor de vestiging waarvoor u opslaglocaties wilt instellen.
7.  Selecteer op het sneltabblad **Opslaglocaties** de opslaglocaties die u wilt gebruiken als standaardopslaglocaties voor ontvangsten, verzendingen, inkomende en uitgaande opslaglocaties en open-shopflooropslaglocaties.  
8.  De opslaglocaties die u hier invult worden automatisch weergegeven op de koppen en daarna op de regels van verschillende magazijndocumenten. De standaardopslaglocaties bepalen alle begin- en eindplaatsingen van artikelen in het magazijn.  
9.  Selecteer een opslaglocatie voor magazijncorrecties als u met gestuurde opslag en pick werkt. De opslaglocatiecode in het veld **Herwaarderingsopslaglocatie** definieert de virtuele opslaglocatie waarin verschillen in de voorraad worden geregistreerd wanneer u waargenomen verschillen registreert in het magazijnartikeldagboek of wanneer u verschillen berekent bij het registreren van een magazijninventarisatie.  
10. Vul de velden op het sneltabblad **Opslaglocatiebeleid** in als deze van toepassing zijn op uw magazijn. De belangrijkste velden zijn **Opslaglocatiecapaciteitsbeleid**, **Breakbulk toestaan** en **Opslagsjabloon**.  
11. Vul op het sneltabblad **Magazijn** de velden **Uitslagtijd**, **Inslagtijd** en **Basisagendacode** in. Zie [Procedure: basisagenda's instellen](across-how-to-assign-base-calendars.md) voor meer informatie.

## <a name="filling-the-consumption-bin"></a>De verbruiksopslaglocatie vullen
In dit stroomdiagram wordt weergegeven hoe het veld **Opslaglocatie** op de productieordercomponentregels wordt ingevuld op basis van uw locatie-instellingen.

![Diagram van opslaglocatiestroom](media/binflow.png "Opslaglocatiestroom")  

## <a name="see-also"></a>Zie ook
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

