---
title: Nieuwe bedrijven configureren met een cmdlet | Microsoft Docs
description: In een aantal scenario's kunt u een configuratiepakket laden en importeren zonder uw gebruikers hierbij te betrekken of de gebruikersinterface van RapidStart Services te gebruiken. Hiervoor kunt u een Windows PowerShell-cmdlet gebruiken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ce8bfdb40d8d428f4b02abcbba4498d58d6481be
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Nieuwe bedrijven configureren met een cmdlet
In een aantal scenario's kunt u een configuratiepakket laden en importeren zonder uw gebruikers hierbij te betrekken of de gebruikersinterface van RapidStart Services te gebruiken. Hiervoor kunt u een Windows PowerShell-cmdlet gebruiken. Scenario's waarbij dit handig kan zijn:  

- Import van gegevens implementeren in meerdere [!INCLUDE[d365fin](includes/d365fin_md.md)]-installaties.
- Aanvullende toepassingsgebieden configureren voor meerdere klanten.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Een configuratiepakket implementeren met een cmdlet  

1. Een RapidStart Services-pakket voorbereiden. U kunt bijvoorbeeld een pakket maken om bepaalde waarden, de namen van de tabel en de velden waar deze waarden in moeten worden geplaatst, te importeren.  
2. Plaats het pakket op een computer waarop u de cmdlet zult uitvoeren.  
3. Open de [!INCLUDE[d365fin](includes/d365fin_md.md)]-beheershell.  
4. Voer **Aanroepen-NAVCodeUnit** in en geef informatie op zoals in het volgende voorbeeld.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
De cmdlet importeert het pakket in elk bedrijf. Gebruikers kunnen de nieuwe functies direct gebruiken.  

## <a name="see-also"></a>Zie ook  
[Nieuwe bedrijven configureren](admin-how-to-configure-new-companies.md)  
[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Windows PowerShell-cmdlets](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

