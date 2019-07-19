---
title: Isabel 6
description: De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee Business Central veilig met Isabel kan worden geïntegreerd. CIS verwerkt de uitwisseling van documenten met en van de Isabel-server.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: belgium-local-functionality
ms.openlocfilehash: a0501d6ad8410d3666ac7e7f3fa8597e48990518
ms.sourcegitcommit: e8abfb78e13f3c29035087b09d7930f2950ab7a3
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/01/2019
ms.locfileid: "1717631"
---
# <a name="isabel-6"></a>Isabel 6
De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee [!INCLUDE[d365fin](../../includes/d365fin_md.md)] veilig met Isabel kan worden geïntegreerd. CIS verwerkt de uitwisseling van documenten met en van de Isabel-server.  

Als u de bankbestanden wilt uploaden of downloaden, moet u uw omgeving instellen om met Isabel te werken. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] communiceert met het bestand CIS.dll via een COM-wrapper.  

Ga als volgt te werk om uw systeem geschikt te maken voor samenwerking met Isabel:  

- Installeer de Isabel-beveiligingsonderdelen. Raadpleeg voor meer informatie het downloadgedeelte op de [Isabel-website](https://go.microsoft.com/fwlink/?LinkId=210323).  

- Installeer de COM-wrapper van de Isabel-organisatie. Deze wrapper is opgenomen in het Isabel GO 6.20-pakket.  

- Registreer de COM-wrapper op uw computer. Zoek het bestand CIS.dll bij de opdrachtprompt en voer vervolgens de opdracht **regsvr32 CISComWrapper.dll** uit.  

## <a name="see-also"></a>Zie ook  
 [Isabel-website](https://go.microsoft.com/fwlink/?LinkId=210323)   
 [Elektronisch bankieren voor België](belgian-electronic-banking.md)   
 [Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)
