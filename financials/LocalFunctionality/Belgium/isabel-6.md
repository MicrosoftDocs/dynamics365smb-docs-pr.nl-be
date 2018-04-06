---
title: Isabel 6
description: "De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee [!INCLUDE[d365fin](../../includes/d365fin_md.md)] veilig met Isabel kan worden geïntegreerd. CIS verwerkt de uitwisseling van documenten met en van de Isabel-server."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: f06394c4a2aa1dc7f1df1d6e1a1339e81a1a8d1f
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="isabel-6"></a>Isabel 6
De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee [!INCLUDE[d365fin](../../includes/d365fin_md.md)] veilig met Isabel kan worden geïntegreerd. CIS verwerkt de uitwisseling van documenten met en van de Isabel-server.  

Als u de bankbestanden wilt uploaden of downloaden, moet u uw omgeving instellen om met Isabel te werken. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] communiceert met de CIS.dll via een COM-wrapper.  

Ga als volgt te werk om uw systeem geschikt te maken voor samenwerking met Isabel:  

- Installeer de Isabel-beveiligingsonderdelen. Raadpleeg voor meer informatie het downloadgedeelte op de [Isabel-website](http://go.microsoft.com/fwlink/?LinkId=210323).  

- Installeer de COM-wrapper van de Isabel-organisatie. Deze wrapper is opgenomen in het Isabel GO 6.20-pakket.  

- Registreer de COM-wrapper op uw computer. Zoek de CIS.dll bij de opdrachtprompt en voer vervolgens de opdracht **regsvr32 CISComWrapper.dll** uit.  

## <a name="see-also"></a>Zie ook  
 [Isabel-website](http://go.microsoft.com/fwlink/?LinkId=210323)   
 [Elektronisch bankieren voor België](belgian-electronic-banking.md)   
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)

