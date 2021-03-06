---
title: CODA-afschriften vereffenen
description: Nadat een CODA-afschrift is geïmporteerd, kunnen de afschriftregels worden geopend vanuit de pagina Bankrekeningkaart. De vereffeningsstatus is op elke regel leeg omdat de afschriftbedragen niet zijn vereffend met openstaande posten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9df39e10efd1c5a040e1f5a7c162d32b41066971
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379577"
---
# <a name="apply-coda-statements"></a>CODA-afschriften vereffenen
Nadat een CODA-afschrift is geïmporteerd, kunnen de afschriftregels worden geopend vanuit de pagina **Bankrekeningkaart**. De vereffeningsstatus is op elke regel leeg omdat de afschriftbedragen niet zijn vereffend met openstaande posten.  

Afschriftbedragen kunnen als volgt worden vereffend met openstaande posten:  

-   Door CODA-afschriftregels handmatig te vereffenen.  
-   Door CODA-afschriftbedragen automatisch te vereffenen met de betreffende posten en rekeningen. De automatische verwerking van CODA-afschriftregels wordt aanbevolen.  

## <a name="to-manually-apply-the-coda-statement-lines"></a>De CODA-afschriftregels handmatig vereffenen  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de bankrekening en kies de actie **CODA-afschriften**.  
3.  Selecteer het CODA-afschrift en kies vervolgens de actie **Bewerken**.  
4.  Vul voor elke bankafschriftregel de velden in zoals in de volgende tabel is beschreven.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Rekeningnr.**|Voer het nummer van de grootboekrekening, de bank, de klant, de leverancier of een vast activum in waaraan de afschriftregel van de bankrekening is gekoppeld.|  
    |**Beschrijving**|In [!INCLUDE[prod_short](../../includes/prod_short.md)] wordt automatisch de omschrijving van het geïmporteerde CODA-bestand opgehaald, maar u kunt de inhoud van dit veld wijzigen.|  

5.  Kies de knop **OK**.  

## <a name="to-automatically-apply-the-coda-statement-lines"></a>De CODA-afschriftregels automatisch vereffenen  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de bankrekening en kies de actie **CODA-afschriften**.  
3.  Selecteer het CODA-afschrift en kies vervolgens de actie **Bewerken**.  
4.  Kies de actie **CODA-afschriftregels**.  
5.  Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Standaardboeking**|Selecteer deze optie als u wilt dat met de batchverwerking afschriftbedragen worden geboekt die niet aan bestaande posten kunnen worden gekoppeld.|  
    |**Lijst afdrukken**|Selecteer deze optie om een overzicht van afschriftbedragen af te drukken die niet automatisch kunnen worden gekoppeld.|  

6.  Kies de knop **OK**.  

    Wanneer u de batchverwerking start, worden de afschriftbedragen vereffend met bestaande posten op basis van de transactiecodes. Zie voor meer informatie [Bankrekeningen instellen voor CODA](how-to-set-up-bank-accounts-for-coda.md).

## <a name="see-also"></a>Zie ook  
 [CODA-bankafschriften](coda-bank-statements.md)   
 [Bankrekeningen instellen voor CODA](how-to-set-up-bank-accounts-for-coda.md)   
 [IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)   
 [CODA-afschriften importeren](how-to-import-coda-statements.md)   
 [Financiële dagboeken maken](how-to-create-financial-journals.md)   
 [CODA-afschriften automatisch overbrengen en boeken](how-to-automatically-transfer-and-post-coda-statements.md)   
 [CODA-afschriften handmatig overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]