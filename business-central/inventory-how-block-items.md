---
title: Artikelen of artikelvarianten blokkeren voor verkoop en inkoop
description: U kunt voorkomen dat artikelen en artikelvarianten worden ingevoerd op regels in verkoop- of inkoopdocumenten en u kunt voorkomen dat ze worden geboekt in een transactie.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
ms.service: dynamics-365-business-central
---
# <a name="block-items-or-item-variants-from-sales-or-purchasing"></a>Artikelen of artikelvarianten blokkeren voor verkoop en inkoop

U kunt voorkomen dat artikelen en artikelvarianten worden ingevoerd op regels in verkoop- of inkoopdocumenten en u kunt voorkomen dat ze worden geboekt in transacties. Dit is bijvoorbeeld handig wanneer een artikel een bekend defect heeft. Als iemand een geblokkeerd artikel of een geblokkeerde artikelvariant kiest voor een verkoop- of aankoopdocument, zal een bericht hen laten weten dat het artikel is geblokkeerd.

De volgende tabel laat zien wat er gebeurt wanneer artikelen of varianten worden geblokkeerd.  

|Optie|Omschrijving|  
|--------------------|------------|  
|**Verkoop geblokkeerd**|U kunt het artikel of de variant niet kiezen in een verkoopdocument of een verkoopartikeldagboek.|  
|**Inkoop geblokkeerd**|U kunt het artikel of de variant niet kiezen in een inkoopdocument, in een inkoopartikeldagboek of in planningsprocessen voor inkoop.|  
|**Geblokkeerd**|U kunt het artikel of de variant niet opnemen wanneer u transacties boekt.|  

> [!NOTE]
> Geblokkeerde artikelen kunnen worden geretourneerd. Dit betekent dat geen van de bovenstaande instellingen van toepassing zijn op retourorders en creditnota's.

Wanneer u de actie **Kopiëren uit document** gebruikt om nieuwe documenten te maken op basis van bestaande documenten, ontvangt u een bericht als er artikelen of varianten op de brondocumentregels zijn geblokkeerd. De geblokkeerde documentregels worden uitgesloten van het nieuwe document en een bericht toont een overzicht van alle documentregels die in het brondocument zijn geblokkeerd.

## <a name="to-block-an-item"></a>Een artikel blokkeren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Afhankelijk van wat u wilt doen, selecteert u het artikel en kiest u vervolgens een of meer van de volgende selectievakjes:
    * **Geblokkeerd**
    * **Verkoop geblokkeerd**
    * **Inkoop geblokkeerd**  

## <a name="to-block-an-item-variant"></a>Een artikelvariant blokkeren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het artikel met een variant die u wilt blokkeren, kies **Varianten** en kies vervolgens een of meer van de volgende selectievakjes:  
    * **Geblokkeerd**
    * **Verkoop geblokkeerd**
    * **Inkoop geblokkeerd**

## <a name="see-also"></a>Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
