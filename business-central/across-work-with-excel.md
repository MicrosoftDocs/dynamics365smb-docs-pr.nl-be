---
title: Weergeven en bewerken in Excel vanuit Business Central | Microsoft Docs
description: Leer hoe u de pagina's in Microsoft Excel opent vanuit Business Central voor betere gegevensanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.contentlocale: nl-be
ms.lasthandoff: 01/22/2019

---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Weergeven en bewerken in Excel vanuit Business Central 

Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de records weergeven met Microsoft Excel. U hebt hiervoor twee opties. U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren. Dit zijn de verschillen tussen de twee methoden:  

## <a name="open-in-excel"></a>Openen in Excel

-    Met deze actie respecteert Excel eventuele filters op de pagina die beperken welke records worden weergegeven. Dit betekent dat de Excel-werkmap dezelfde rijen en kolommen bevat die op de pagina worden weergegeven in [!INCLUDE[prodshort](includes/prodshort.md)].

-    U kunt wijzigingen in de records aanbrengen in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prodshort](includes/prodshort.md)]. U kunt de wijzigingen alleen opslaan in het Excel-bestand op uw computer. 

-    Deze actie werkt zowel onder Windows als MacOS. 

>[!NOTE]
>Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Openen in Excel** niet beschikbaar als de actie **Bewerken in Excel** beschikbaar is.

## <a name="edit-in-excel"></a>Bewerken in Excel

-    Met deze actie respecteert de Excel-werkmap eventuele filters op de pagina niet die beperken welke records worden weergegeven. Dit betekent dat de Excel-werkmap alle beschikbare records en kolommen bevat, ongeacht wat op de pagina wordt weergegeven. 

-    Het voordeel van de actie **Bewerken in Excel** is dat u er wijzigingen in records in Excel mee kunt aanbrengen en de wijzigingen weer naar [!INCLUDE[prodshort](includes/prodshort.md)] kunt publiceren.

-    Dit werkt alleen onder Windows, niet onder MacOS.

>[!NOTE]
>Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw beheerder is geïnstalleerd. Voor beheerders: als u wilt weten hoe u de Excel-invoegtoepassing installeert, raadpleegt u [De Excel-invoegtoepassing instellen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

## <a name="see-also"></a>Zie ook

[Werken met Business Central](ui-work-product.md)  

