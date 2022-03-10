---
title: Converteren van bestaande locaties naar magazijnlocaties | Microsoft Docs
description: U kunt een bestaande voorraadvestiging zones en opslaglocaties laten gebruiken en laten functioneren als een magazijnvestiging.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d8c87884b359c02815187ab6b5c994ebccce119f
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140123"
---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Bestaande locaties converteren naar magazijnlocaties
U kunt een bestaande voorraadvestiging zones en opslaglocaties laten gebruiken en laten functioneren als een magazijnvestiging.  

Met de batchverwerking om een vestiging als magazijn te laten functioneren maakt u de eerste magazijnposten voor de correctieopslaglocatie voor het magazijn voor alle artikelen die voorraad in de vestiging hebben. Deze eerste posten worden in evenwicht gebracht als magazijninventarisatieposten worden geboekt nadat de batchverwerking is uitgevoerd.  

U kunt voor of na de omzetting zones en opslaglocaties maken. De enige opslaglocatie die u voor de omzetting moet maken is de opslaglocatie die als correctieopslaglocatie zal worden gebruikt.  

> [!IMPORTANT]  
>  Voordat u de locatie omzet voor magazijnactiviteiten, kunt u alle negatieve voorraad en open magazijndocumenten leegmaken door een rapport te draaien dat voor de locatie de artikelen met negatieve voorraad en open magazijndocumenten aangeeft. Zie voor meer informatie Op negatieve voorraad controleren.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Een bestaande vestiging als een magazijnvestiging laten functioneren  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnvestiging maken** in en kies vervolgens de gerelateerde koppeling.  
2.  Geef in het veld **Locatiecode** de locatie op die geschikt moet zijn voor magazijnverwerking.  
3.  Geef in het veld **Wijzig opslaglocatiecode** de opslaglocatie op van de locatie waar de niet-gesynchroniseerde magazijnposten worden opgeslagen. Zie voor meer informatie [De aangepaste magazijnposten synchroniseren met de gerelateerde artikelposten](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).  

    Aan de hand van de openstaande artikelposten voor de opgegeven vestiging worden magazijndagboekregels gemaakt die elke combinatie van artikelnr., variant, eenheidscode en, indien nodig, lotnr. en serienummer samenvatten in de artikelposten. Vervolgens wordt het magazijndagboek geboekt. Hierdoor ontstaan magazijnposten die de voorraad in de correctieopslaglocatie van het magazijn plaatsen. De **correctieopslaglocatie** wordt ook op de vestigingskaart ingesteld.  

4.  Als u wilt zien welke artikelen gedurende de batchverwerking aan de correctieopslaglocatie zijn toegevoegd, kunt u de lijst **Mag.-herwaarderingsopslaglocatie** laten opstellen.  
5.  Nadat de batchverwerking **Magazijnvestiging maken** is voltooid, moet u een magazijninventarisatie uitvoeren en boeken. Zie voor meer informatie [Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md)  

> [!NOTE]  
>  U kunt de batchverwerking **Magazijnvestiging maken** het beste uitvoeren op een tijdstip waarop de batchverwerking niet van invloed is op de dagelijkse werkzaamheden in het systeem. Tijdens deze batchverwerking wordt elke post in de tabel **artikelposten** verwerkt en als er veel artikelposten zijn, kan de verwerking uren duren.  

 Voor vestigingen waar voor de omzetting geen magazijnbeheerdocumenten werden gebruikt, moet u alle brondocumenten die voor de omzetting gedeeltelijk ontvangen of gedeeltelijk verzonden waren opnieuw openen.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]