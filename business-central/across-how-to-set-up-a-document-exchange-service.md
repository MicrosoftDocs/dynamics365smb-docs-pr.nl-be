---
title: Een service voor documentuitwisseling instellen | Microsoft Docs
description: U gebruikt een externe serviceprovider om elektronische documenten uit te wisselen met uw handelspartners.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a9bba4d097ca24de094f153c91d7888811cdfd4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241204"
---
# <a name="set-up-a-document-exchange-service"></a>Een service voor documentuitwisseling instellen
U gebruikt een externe serviceprovider om elektronische documenten uit te wisselen met uw handelspartners. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.  

## <a name="to-set-up-a-document-exchange-service"></a>Een service voor documentuitwisseling instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen service doc.uitw.** in en kies vervolgens de gerelateerde koppeling.  
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
