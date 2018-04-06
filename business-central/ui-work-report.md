---
title: Een rapport plannen voor uitvoering op een bepaalde datum en tijd | Microsoft Docs
description: Leren over het invoeren van een lijst in een verwerkingswachtrij en het plannen om te worden verwerkt op een specifieke datum en tijd.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 01a7a1d254916a8b93744183d3678c2082aec42c
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="working-with-reports"></a>Werken met rapporten
In een rapport wordt informatie verzameld op basis van een bepaalde reeks criteria. De informatie wordt hierin weergegeven in een makkelijk leesbare en afdrukbare indeling. In de toepassing zijn er vele diverse rapporten die u kunt openen en gebruiken. De rapporten bieden veelal informatie in de context van de pagina waarop u werkt. De pagina **Klant** biedt bijvoorbeeld rapporten voor de top 10 van klanten, voor de verkoopstatistieken en nog veel meer.

U treft de rapporten aan op het tabblad **Rapporten** op geselecteerde pagina's, of u kunt door middel van zoeken rapporten op hun naam vinden. Wanneer u een rapport opent, ziet u een pagina waarop u informatie kunt opgeven door middel van opties en filters, waarmee u bepaalt u wat u in het rapport wilt opnemen. Afhankelijk van het rapport kunt u bijvoorbeeld een datumbereik opgeven, of een specifieke record zoals een klant, of een sorteervolgorde. Hier volgt een voorbeeld:

![Rapportopties](media/report_options.png "Rapportopties")

## <a name="previewing-a-report"></a>Een voorbeeldweergave van een rapport openen
Klik op **Voorbeeld** om het rapport te openen in uw internetbrowser. Wijs met de muisaanwijzer een gebied in het rapport aan om de menubalk op te roepen.  

![Werkbalk Afdrukvoorbeeld van rapport](media/report_viewer.png "Werkbalk Afdrukvoorbeeld van rapport")

Met de menubalk kunt u de volgende handelingen uitvoeren:

-   Door pagina's bladeren
-   In- en uitzoomen
-   Het formaat aanpassen aan de afmetingen van het venster
-   Tekst selecteren

    U kunt tekst van rapport kopiëren en dit vervolgens ergens anders plakken, zoals als op een pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)] of in Microsoft Word.  Met een muis kunt u bijvoorbeeld klikken op het punt van waaraf u wilt kopiëren, de muisknop ingedrukt houden en de muis verplaatsen om een of meer woorden, zinnen of alinea's te selecteren. Vervolgens klikt u met de rechtermuisknop en selecteert u **Kopiëren**. U kunt de geselecteerde tekst op elke gewenste plek plakken.
-   Document pannen

    U kunt het zichtbare deel van het rapport in iedere richting verplaatsen, zodat u andere delen kunt bekijken. Dit is handig als u hebt ingezooomd om details te zien.  U kunt bijvoorbeeld op een willekeurige plek in het rapportvoorbeeld klikken, de muisknop vasthouden en dan de muis verplaatsen.

-   Downloaden naar een PDF-bestand op uw computer of netwerk.
-   Afdrukken


## <a name="saving-a-report"></a>Een rapport opslaan
U kunt een rapport opslaan als een PDF-document, een Microsoft Word-document of een Microsoft Excel-document. Kies hiervoor **Verzenden naar** en selecteer de gewenste bestandsindeling.

## <a name="ScheduleReport"></a>Een rapport plannen voor uitvoering
U kunt een rapport plannen voor uitvoering op een bepaalde datum en tijd. Geplande rapporten worden in de verwerkingswachtrij ingevoerd en verwerkt op het geplande tijdstip, net zoals andere taken. U kunt ervoor kiezen het verwerkte rapport op te slaan in een bestand, zoals een Excel-, Word- of PDF-bestand, het afdrukken op een geselecteerde printer of het rapport alleen verwerken. Als u ervoor kiest het rapport in een bestand op te slaan, wordt het verwerkte rapport naar het gebied **Rapportinbox** in uw rolcentrum verzonden, waar u het kunt bekijken.

U kunt een rapport plannen wanneer u een rapport opent. U kiest de actie **Plannen** en voert vervolgens gegevens in, zoals printer en datum en tijd. Het rapport wordt vervolgens toegevoegd aan de taakwachtrij en wordt op de opgegeven tijd uitgevoerd. Als het rapport is verwerkt, wordt het artikel verwijderd uit de verwerkingswachtrij. Als u het verwerkte rapport in een bestand hebt opgeslagen, is het beschikbaar in het gebied **Rapportinbox**.

## <a name="PrintReport"></a>Een rapport afdrukken
U kunt een rapport afdrukken via de knop **Afdrukken** op de optiepagina die wordt weergegeven als u het rapport opent of via de menubalk in Voorbeeld.

## <a name="using-saved-settings"></a>Opgeslagen instellingen gebruiken
Een rapport kan een of meer vermeldingen bevatten in het vak **Opgeslagen instellingen**. *Opgeslagen instellingen* is een groep vooraf gedefinieerde opties en filters, die u op het rapport kunt toepassen voordat u de voorbeeldweergave maakt of het rapport als een bestand opslaat. Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten.

De opgeslagen instelling met de naam **Laatst gebruikte opties en filters** is altijd beschikbaar. Deze vermelding stelt het rapport in op de opties en filters die waren ingesteld toen het rapport voor de laatste keer werd bekeken.

>[!NOTE]
>Als beheerder kunt u de opgeslagen instellingen van rapporten configureren en beheren voor alle gebruikers. Zie voor meer informatie [Opgeslagen instellingen in rapporten beheren](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>De lay-out en weergave van een rapport weergeven
Een rapportlay-out bepaalt wat in een rapport wordt weergegeven, hoe het is ingedeeld en hoe het is opgemaakt. Zie [Wijzigen welke lay-out momenteel in een rapport wordt gebruikt](ui-how-change-layout-currently-used-report.md) als u naar een andere lay-out wilt schakelen. Of zie [Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md) als u uw eigen rapportlay-out wilt aanpassen.

## <a name="see-also"></a>Zie ook
[Printerselectie opgeven voor rapporten](ui-specify-printer-selection-reports.md)  
[Lay-outs van rapporten en documenten beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

