---
title: Gebruik van opslaglocaties voor locaties instellen | Microsoft Docs
description: Opslaglocaties vertegenwoordigen de standaard magazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen. Wanneer u uw opslaglocaties hebt gemaakt, kunt u de inhoud die u in de afzonderlijke opslaglocaties wilt plaatsen bijzonder gedetailleerde definiëren. De opslaglocatie kan echter ook functioneren als een vrije opslaglocatie zonder opgegeven inhoud.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 214de72b86e3d32e5161814a7f65079cbb4136b7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816304"
---
# <a name="set-up-locations-to-use-bins"></a>Locaties instellen om opslaglocaties te gebruiken
Opslaglocaties vertegenwoordigen de standaardmagazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen. Wanneer u uw opslaglocaties hebt gemaakt, kunt u de inhoud die u in de afzonderlijke opslaglocaties wilt plaatsen bijzonder gedetailleerde definiëren. De opslaglocatie kan echter ook functioneren als een vrije opslaglocatie zonder opgegeven inhoud.  

Als u de opslaglocatiefunctionaliteit op een locatie wilt gebruiken, moet u deze eerst activeren op de **Vestigingskaart**. U ontwerpt vervolgens de artikelstroom op de locatie door de opslaglocatiecodes op te geven in de instellingsvelden voor de verschillende stromen.  

> [!NOTE]  
>  Voordat u opslaglocatiecodes op de vestigingskaart kunt opgeven, moeten de opslaglocatiecodes worden gemaakt. Zie voor meer informatie [Opslaglocaties maken](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Een vestiging instellen voor het gebruik van opslaglocaties  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de vestiging waarin u opslaglocaties wilt gebruiken.  
3.  Kies de actie **Bewerken**.  
4.  Schakel op het sneltabblad **Magazijn** het selectievakje **Opslaglocatie verplicht** in.  
5.  Als u in de vestiging niet met gestuurde opslag en pick werkt, vult u in het veld **Std. opslaglocatieselectie** de methode in waarmee standaardopslaglocaties aan artikelen worden toegewezen.  
6.  Open de kaart voor de vestiging waarvoor u opslaglocaties wilt instellen.
7.  Selecteer op het sneltabblad **Opslaglocaties** de opslaglocaties die u wilt gebruiken als standaardopslaglocaties voor ontvangsten, verzendingen, inkomende en uitgaande opslaglocaties en open-shopflooropslaglocaties.  
8.  De opslaglocaties die u hier invult worden automatisch weergegeven op de koppen en daarna op de regels van verschillende magazijndocumenten. De standaardopslaglocaties bepalen alle begin- en eindplaatsingen van artikelen in het magazijn.  
9.  Selecteer een opslaglocatie voor magazijncorrecties als u met gestuurde opslag en pick werkt. De opslaglocatiecode in het veld **Herwaarderingsopslaglocatie** definieert de virtuele opslaglocatie waarin verschillen in de voorraad worden geregistreerd wanneer u waargenomen verschillen registreert in het magazijnartikeldagboek of wanneer u verschillen berekent bij het registreren van een magazijninventarisatie.  
10. Vul de velden op het sneltabblad **Opslaglocatiebeleid** in als deze van toepassing zijn op uw magazijn. De belangrijkste velden zijn **Opslaglocatiecapaciteitsbeleid**, **Breakbulk toestaan** en **Opslagsjabloon**.  
11. Vul op het sneltabblad **Magazijn** de velden **Uitslagtijd**, **Inslagtijd** en **Basisagendacode** in. Zie [Basisagenda's instellen](across-how-to-assign-base-calendars.md) voor meer informatie.

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
