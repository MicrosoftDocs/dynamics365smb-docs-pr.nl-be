---
title: Artikelen verplaatsen in geavanceerde magazijnconfiguraties | Microsoft Docs
description: Bij geavanceerde magazijnconfiguraties, dat wil zeggen locaties met gestuurde opslag en pick, worden magazijnverplaatsingen tussen opslaglocaties door een senior medewerker uitgevoerd, die de magazijnverplaatsingen in het verplaatsingswerkblad voorbereidt en deze vervolgens toewijst aan magazijnmedewerkers.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/232017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 019d60da5611174b873d07e8adb25ed78b01467b
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-move-items-in-advanced-warehouse-configurations"></a>Procedure: Artikelen verplaatsen in geavanceerde magazijnconfiguraties
Bij geavanceerde magazijnconfiguraties, dat wil zeggen locaties met gestuurde opslag en pick, worden magazijnverplaatsingen tussen opslaglocaties uitgevoerd door een senior medewerker die de magazijnverplaatsingen in het verplaatsingswerkblad voorbereidt en deze vervolgens toewijst aan magazijnmedewerkers.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>artikelen met het magazijnverplaatsingswerkblad verplaatsen
Het venster **Verplaatsingsvoorstel** heeft twee functies waarmee de regels automatisch kunnen worden ingevuld. De eerste functie is **Opslaglocatieaanvulling berekenen**. Deze functie gebruikt de rangorde van de opslaglocatie om aanvulling voor te stellen voor hogere gerangschikte opslaglocaties van lage gerangschikte opslaglocaties. De tweede post is de functie **Opslaglocatie-inhoud ophalen**, waarmee de voorstelregels worden gevuld met de volledige opslaglocatie-inhoud van de opslaglocatie of de opslaglocaties die u opgeeft.

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verplaatsingsvoorstel** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vul de magazijnverplaatsingsgegevens in op de voorstelregels.  
3. Kies de actie **Verplaatsing maken** om een magazijnverplaatsingsdocument te maken dat vervolgens kan worden geregistreerd wanneer de magazijnverplaatsing is voltooid.  

### <a name="to-register-the-warehouse-movement"></a>De magazijnverplaatsing als registreren  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verplaatsingen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open de magazijnverplaatsing die u wilt verwerken.  
3.  Specificeer op de regels van de actiesoort **Plaats** waar, welk en wanneer het betrokken artikel verplaatst moet worden door het bewerken van het veld **Code Zone**, **Opslaglocatiecode**, **Te verwerken aantal** of **Vervaldatum**.  

    Als de opslaglocaties van het systeemmagazijn overeenkomen met de fysieke structuur van het werkelijke magazijn, kunt u een aantal verschillende artikelen uit opeenvolgende bulkopslaglocaties nemen en de artikelen vervolgens in pickopslaglocaties plaatsen die mogelijk ook naast elkaar zijn gelegen.  
4.  Specificeer op de regels van de actiesoort **Nemen** in het veld **Te verwerken aantal** een aantal voor de onderdelen van de opslaglocatie-inhoud die u wilt verplaatsen. Alle overige velden op de regels van de actiesoort **Nemen** zijn alleen-lezen.  
5.  Als u alle voorgestelde aantallen zoals opgegeven in het veld **Aantal** wilt verplaatsen, kiest u de actie **Te verwerken aantal autom. invullen**.  
6. Kies de actie **Registreren**.  

> [!NOTE]  
>  Wanneer in de vestiging gestuurde opslag en pick wordt gebruikt, kunt u artikelen niet handmatig plaatsen of ophalen uit een opslaglocatie met het type ONTVANGEN, aangezien artikelen in een dergelijke opslaglocatie moeten worden geregistreerd als opgeslagen artikelen voordat ze onderdeel vormen van de beschikbare voorraad.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>U kunt als volgt verplaatsingen van een artikel registreren die eerder zijn uitgevoerd  
Als in de vestiging gestuurde opslag en pick wordt gebruikt en u artikelen naar andere opslaglocaties moet verplaatsen zonder een bestaande opslag, pick of verplaatsing te gebruiken, kunt u de correcte plaatsing van de artikelen in het magazijn registreren in het **magazijnherindelingsdagboek.**

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Mag. herindelingsdagboek** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vul de velden **Artikelnr.**, **Van zone**, **Van opslaglocatie**, **Naar zone** en **Naar opslaglocatie** in.  
3.  Kies de actie **Registreren**.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

