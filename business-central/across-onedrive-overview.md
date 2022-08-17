---
title: Integratie van Business Central en OneDrive voor Bedrijven
description: U kunt OneDrive voor Bedrijven gebruiken om bestanden, zoals rapporten of bestandsbijlagen, op te slaan, te beheren en te delen. Ook als u het spelt als One Drive.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 06adf2a30a7487fa3bc66e1aebec42e6c55184e2
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227431"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Integratie van Business Central en OneDrive voor Bedrijven

OneDrive voor Bedrijven is een cloudopslagservice die is opgenomen in Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] maakt het gemakkelijk om bestanden op te slaan, te beheren en te delen met andere mensen via OneDrive. Wanneer een bestand in uw OneDrive staat, kunt u profiteren van de rijke samenwerkingservaringen van de online versies van Microsoft-producten, zoals Word, Excel en PowerPoint. U kunt bijvoorbeeld een Word-document delen, waarna u en uw collega's het samen in realtime kunnen bewerken. Met OneDrive kunt u ook andere soorten bestanden openen, zoals pdf's. 

## <a name="get-started"></a>Aan de slag

We hebben de verbinding tot stand gebracht tussen [!INCLUDE[prod_short](includes/prod_short.md)] online en OneDrive, dus het is gemakkelijk om te beginnen. De enige vereiste is dat gebruikers OneDrive minstens één keer hebben geopend. 

Op de meeste pagina's waar bestanden beschikbaar zijn, zoals de Rapportinbox of bestanden die aan records zijn toegevoegd, vindt u de acties **Openen in OneDrive** en **Delen**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="De acties Openen in OneDrive en Delen voor rapporten":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="De acties Openen in OneDrive en Delen voor bijlagen":::

|Selectie|Actie|Zie voor meer informatie...|
|---------|-----|----------------|
|Openen in OneDrive|Kopieer het bestand naar een Business Central-map in uw OneDrive en open het bestand.|[Openen in OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Aandeel|Kopieer het bestand naar uw OneDrive en deel het met anderen.|[Delen in OneDrive](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> U kunt ook uw [!INCLUDE[prod_short](includes/prod_short.md)] in-premises verbinden met OneDrive. Er zijn echter een paar dingen om te doen om het te laten werken. Zie voor meer informatie [Business Central On-Premises configureren](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Zie ook

[OneDrive-integratie met Business Central beheren](admin-onedrive-integration.md)  
[Business Central-bestanden openen in OneDrive](across-share-onedrive.md)  
[Veelgestelde vragen over OneDrive](admin-onedrive-faq.md)