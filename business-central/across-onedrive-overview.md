---
title: Integratie van Business Central en OneDrive voor Bedrijven
description: 'U kunt OneDrive voor Bedrijven gebruiken om bestanden, zoals rapporten of bestandsbijlagen, op te slaan, te beheren en te delen. Ook als u het spelt als One Drive.'
author: jswymer
ms.topic: overview
ms.search.keywords: null
ms.date: 02/28/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="business-central-and-onedrive-for-business-integration"></a>Integratie van Business Central en OneDrive voor Bedrijven

OneDrive voor Bedrijven is een cloudopslagservice die is opgenomen in Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] maakt het gemakkelijk om bestanden op te slaan, te beheren en te delen met andere mensen via OneDrive. Wanneer een bestand in uw OneDrive staat, kunt u profiteren van de uitgebreide samenwerkingservaringen van de online versies van Microsoft-producten, zoals Word, Excel en PowerPoint. U kunt bijvoorbeeld een Word-document delen, waarna u en uw collega's het samen in realtime kunnen bewerken. Met OneDrive kunt u ook andere soorten bestanden openen, zoals pdf's. 

## <a name="get-started-with-onedrive-features"></a>Aan de slag met OneDrive-functies

Als u [!INCLUDE[prod_short](includes/prod_short.md)] online gebruikt, hebben we de verbinding tussen [!INCLUDE[prod_short](includes/prod_short.md)] online en OneDrive al tot stand gebracht. Het is dus gemakkelijk om te beginnen. De enige vereiste is dat gebruikers OneDrive minstens één keer hebben geopend. Met [!INCLUDE[prod_short](includes/prod_short.md)] on-premises moet een beheerder de verbinding configureren voordat u aan de slag kunt. Meer informatie vindt u in [OneDrive-integratie met Business Central beheren](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### <a name="open-and-share-in-onedrive"></a>Openen en delen in OneDrive

Op de meeste pagina's waar bestanden beschikbaar zijn, zoals de Rapportinbox of bestanden die aan records zijn toegevoegd, vindt u de acties **Openen in OneDrive** en **Delen**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="De acties Openen in OneDrive en Delen voor rapporten":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="De acties Openen in OneDrive en Delen voor bijlagen":::

|Selectie|Actie|Zie voor meer informatie...|
|---------|-----|----------------|
|Openen in OneDrive|Kopieer het bestand naar een Business Central-map in uw OneDrive en open het bestand.|[Openen in OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Aandeel|Kopieer het bestand naar uw OneDrive en deel het met anderen.|[Delen in OneDrive](across-share-onedrive.md#share) |

### <a name="save-excel-workbooks-and-report-files-in-onedrive"></a>Excel-werkmappen en -rapportbestanden in OneDrive opslaan

Als OneDrive-integratie is ingesteld, gebruiken enkele andere bekende functies automatisch OneDrive voor het opslaan van bestanden in plaats van bestanden op uw apparaat op te slaan:

- Met de acties **Openen in Excel** en **Bewerken in Excel** op lijstpagina´s wordt het Excel-bestand naar OneDrive gekopieerd en vervolgens in Excel Online geopend. Zie [Weergeven en bewerken in Excel](across-work-with-excel.md) voor meer informatie.
- Als u een rapport naar een Excel- of Word-bestand exporteert, wordt het bestand automatisch gekopieerd naar OneDrive en vervolgens geopend in Excel Online of Word Online. Zie [Een rapport in een bestand opslaan](ui-work-report.md#saving-a-report-to-a-file) voor meer informatie.

Deze functies zijn standaard niet ingeschakeld. Maar als beheerder kunt u ze eenvoudig inschakelen met de begeleide instelling **OneDrive instellen**.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> U kunt ook uw [!INCLUDE[prod_short](includes/prod_short.md)] in-premises verbinden met OneDrive. Er zijn echter een paar dingen om te doen om het te laten werken. Zie voor meer informatie [Business Central On-Premises configureren](admin-onedrive-integration-onpremises.md).

## <a name="see-also"></a>Zie ook

[OneDrive-integratie met Business Central beheren](admin-onedrive-integration.md)  
[Business Central-bestanden openen in OneDrive](across-share-onedrive.md)  
[Veelgestelde vragen over OneDrive](admin-onedrive-faq.md)  
