---
title: Aangepaste configuratiepakketten voor bedrijven maken | Microsoft Docs
description: Naarmate uw bedrijf groeit, zult u waarschijnlijk gaan vertrouwen op een set bedrijfstypen die u met de meeste van uw klanten gebruikt. U kunt uw implementatieproces stroomlijnen door van deze typen configuratiepakketten voor bedrijven te maken die beschikbaar zijn voor hergebruik.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e1cf9d530c8af95373cfbdef8a3f6822cbba938
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915796"
---
# <a name="create-custom-company-configuration-packages"></a>Aangepaste configuratiepakketten voor bedrijven maken
Naarmate uw bedrijf groeit, zult u waarschijnlijk gaan vertrouwen op een set bedrijfstypen die u met de meeste van uw klanten gebruikt. U kunt uw implementatieproces stroomlijnen door van deze typen configuratiepakketten voor bedrijven te maken die beschikbaar zijn voor hergebruik.  

In het algemeen maakt u een configuratiepakket per functiegebied. Zo kunt u bijvoorbeeld een pakket maken voor uw productiefunctionaliteit. Dat kunt u vervolgens toepassen en nieuwe gebieden in een bedrijf instellen als u ze nodig hebt  

Een andere benadering zou zijn om een pakket te maken dat de tabellen bevat waarin de instellingen worden gedefinieerd, zoals de volgende:  

-   VA-instellingen  
-   Grootboekinstellingen  
-   Voorraadinstellingen  
-   Productie-instellingen  
-   Inkoopinstellingen  
-   Marketinginstellingen  
-   Service-instellingen  
-   Verkoopinstellingen  
-   Magazijninstellingen  
-   Boekingsgroepinstellingen  
-   Btw-boekingsgroepinstellingen  
-   Voorraadboekingsinstellingen  

Als u een complete lijst met instellingstabellen wilt zien, kiest u het pictogram Lampje dat de functie ![Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Handmatige instelling** in en kiest u vervolgens de gerelateerde koppeling.  

> [!IMPORTANT]
> Wees voorzichtig als u tabellen of velden kiest die dezelfde tijdelijke naam hebben, maar die worden onderscheiden door speciale tekens, zoals %, &, <, >, (, en ). De tabel 'XYZ' kan bijvoorbeeld de velden "Veld 1" en "Veld 1%" bevatten.
>
> De XML-processor accepteert slechts enkele speciale tekens en zal andere verwijderen. Als het verwijderen van een speciaal teken, zoals het %-teken in 'Veld 1%', resulteert in twee of meer tabellen of velden met dezelfde naam, zal er een fout optreden wanneer u een configuratiepakket exporteert of importeert.

## <a name="to-create-a-custom-company-configuration-package"></a>Een aangepast configuratiepakket voor een bedrijf maken  
1.  Maak een nieuw bedrijf. Zie voor meer informatie [Nieuwe bedrijven maken in Business Central](about-new-company.md).  
3.  Stel het nieuwe bedrijf in op de door u benodigde wijze. Vul alle vereiste instellingentabellen in.  
4.  Open het nieuwe bedrijf.
5. Open de pagina **Configuratiewerkblad** .  
6.  Voeg de tabellen die u wilt overbrengen naar een ander bedrijf toe aan het werkblad. Wijs de werkbladregels toe aan het pakket.  
7.  Maak een vragenlijst voor de meest gebruikte instellingentabel.  
8.  Stel configuratiesjablonen op om het gemakkelijker te maken om hoofdgegevens, zoals klanten of artikelen, te definiëren.  
9.  Exporteer uw pakket als een .rapidstart-bestand.  

## <a name="see-also"></a>Zie ook  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]