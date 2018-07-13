---
title: Een service voor documentuitwisseling instellen | Microsoft Docs
description: U gebruikt een externe serviceprovider om elektronische documenten uit te wisselen met uw handelspartners.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 0e57f02f1689de12e75595a26c489eeda68a4b89
ms.contentlocale: nl-be
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-a-document-exchange-service"></a>Een service voor documentuitwisseling instellen
U gebruikt een externe serviceprovider om elektronische documenten uit te wisselen met uw handelspartners. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.  

## <a name="to-set-up-a-document-exchange-service"></a>Een service voor documentuitwisseling instellen  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen service doc.uitw.** in en klik op de gerelateerde koppeling.  
2. Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Gebruikersagent**|Voer elke willekeurige tekst in die kan worden gebruikt om uw bedrijf te identificeren in processen voor documentuitwisseling.|  
    |**Tenant-id doc.uitw.**|Voer de tenant in de service voor documentuitwisseling in die uw bedrijf vertegenwoordigt. Deze wordt geleverd door de aanbieder van de service voor documentuitwisseling.|  
    |**Ingeschakeld**|Geef op of de service is ingeschakeld. **Opmerking:** zodra u de service inschakelt, worden ten minste twee taakwachtrijposten gemaakt om het verkeer van elektronische documenten naar en vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] te verwerken. Wanneer u de service uitschakelt, worden de taakwachtrijposten verwijderd.|  
    |**Registratie-URL**|Geef de webpagina op waarop u zich aanmeldt voor de service voor documentuitwisseling.|  
    |**Service-URL**|Geef het adres op van de service voor documentuitwisseling die wordt aangeroepen wanneer u elektronische documenten verzendt en ontvangt.|  
    |**Aanmelden**|Geef de aanmeldpagina op voor de service voor documentuitwisseling. Dit is de pagina waarop u de gebruikersnaam en het wachtwoord van uw bedrijf invoert om aan te melden bij de service.|  
    |**Consumentsleutel**|Voer de 3 legged sleutel voor OAuth voor de consumentsleutel in. Deze wordt geleverd door de aanbieder van de service voor documentuitwisseling.|  
    |**Consumentgeheimsleutel**|Voer het geheim in dat de consumentsleutel beveiligt. Deze wordt geleverd door de aanbieder van de service voor documentuitwisseling.|  
    |**Token**|Voer de 3 legged sleutel voor OAuth voor het token in. Deze wordt geleverd door de aanbieder van de service voor documentuitwisseling.|  
    |**Tokengeheim**|Voer het geheim in dat het token beveiligt. Deze wordt geleverd door de aanbieder van de service voor documentuitwisseling.|  

    > [!NOTE]  
    > Uw aanmeldgegevens worden automatisch versleuteld.

## <a name="see-also"></a>Zie ook  
[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)

