---
title: "Btw-nummers verifiëren | Microsoft Docs"
description: U kunt een EU-webservice gebruiken om te controleren of btw-nummers die u op klanten-, leveranciers- of contactkaarten invoert, geldig zijn.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a>Procedure: btw-nummers verifiëren
U kunt een EU-webservice gebruiken om te controleren of btw-nummers die u op klanten-, leveranciers- of contactkaarten invoert, geldig zijn.  

 Wanneer u het veld **VAT Registration No.** wijzigt op een kaart waar de waarde in het veld **Land-/regiocode** een EU-land/regio is, worden het nieuwe btw-nummer en uw gebruikers-ID vastgelegd in het venster **Btw-log**. U controleert een btw-nummer door te klikken op de knop **Btw-nummer controleren** controleren in het venster **Btw-log**. Er wordt een nieuwe regel gemaakt wanneer u de verificatiefunctie gebruikt. Als het nummer geverifieerd kan worden, bevat het veld **Status** de waarde **Geldig**. Als het nummer niet geverifieerd kan worden, bevat het veld **Status** de waarde **Ongeldig** en moet u het nummer in het veld **Btw-nummer** op de kaart wijzigen en de verificatiefunctie opnieuw starten.  

 De URL van de standaardwebservice is ingesteld in het veld **Validatie-URL btw-nummer** in het venster **Grootboekinstellingen**.  

 In de tabel **Btw-nummerformaat** kunt u voor elk land/regio de verschillende indelingen van het btw-registratienummer kiezen die gebruikers mogen invoeren in het veld **Btw-nummer**.  

> [!WARNING]  
>  Deze webservice gebruikt het http-protocol, wat betekent dat gegevens die door de server worden overgebracht, niet zijn versleuteld.  

> [!NOTE]  
>  Er kunnen onderbrekingen optreden voor deze service waarvoor Microsoft niet verantwoordelijk is, aangezien de service onderdeel is van een breed EU-netwerk van nationale btw-journalen.  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a>Btw-nummer van een klantenkaart verifiëren  
Hierna wordt beschreven hoe u een btw-nummer voor een klant kunt verifiëren. De stappen zijn voor contactpersonen en leveranciers vergelijkbaar.   
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.  

2.  Open de kaart van een klant waarvan u het btw-nummer wilt verifiëren.  

    > [!NOTE]  
    >  Het veld **Land-/regiocode** op de klantenkaart moet een EU-land/regio bevatten.  
3.  Klik op het sneltabblad **Facturering** op de detailknop naast het veld **Btw-nummer**.  

    Het venster **Btw-log** wordt geopend met één regel waar het veld **Status** de tekst **Niet gecontroleerd** bevat.  
4.  Kies de actie **Btw-nummer controleren**.  

     Er wordt een nieuwe regel gemaakt waarbij het veld **Status** de waarde **Geldig** of **Ongeldig** bevat.  
5.  Als het veld **Status** de tekst **Ongeldig** bevat, wijzigt u het nummer in het veld **Btw-nummer** op de kaart en herhaalt u stap 3 en 4.  

## <a name="see-also"></a>Zie ook  
[Financiën](finance.md)  
[Procedure: Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Procedure: Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

