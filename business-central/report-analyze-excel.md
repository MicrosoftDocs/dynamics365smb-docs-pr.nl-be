---
title: Rapportgegevens analyseren met Excel en XML
description: Leer hoe u Excel en XML gebruikt om een rapportgegevensset te analyseren.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.date: 03/16/2022
ms.author: jswymer
---
# <a name="analyzing-report-data-with-excel-and-xml"></a><a name="analyzing-report-data-with-excel-and-xml"></a>Rapportgegevens analyseren met Excel en XML

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Als ontwikkelaar of gevorderde gebruiker helpt het om de gegevens te inspecteren die voor een bepaalde rapportgegevensset worden gegenereerd terwijl u nieuwe rapporten maakt of bestaande wijzigt. Om deze mogelijkheid te ondersteunen kunt u een rapportgegevensset rechtstreeks als onbewerkte gegevens exporteren naar een Excel-werkblad of XML-bestand. In Excel kunt u bijvoorbeeld vervolgens ad-hoc analyses van de gegevens uitvoeren en problemen diagnosticeren.

## <a name="get-started"></a><a name="get-started"></a>Aan de slag

Om een rapport naar een Excel-werkmap of XML-bestand te exporteren opent u het rapport in de client en selecteert u op de aanvraagpagina **Verzenden naar** > **Microsoft Excel-document (alleen gegevens)** of **XML-document**. Het bestand wordt naar uw apparaat gedownload.

## <a name="more-about-excel-data-only"></a><a name="more-about-excel-data-only"></a>Meer over Excel (alleen gegevens)

De optie **Microsoft Excel-document (alleen gegevens)** exporteert de rapportresultaten en de criteria die werden gebruikt om ze te genereren&mdash;maar het omvat niet de rapportlay-out. Het Excel-bestand bevat de volledige dataset, als onbewerkte gegevens, gerangschikt in rijen en kolommen. Alle gegevenskolommen van de gegevensset van het rapport worden opgenomen, ongeacht of ze in de rapportlay-out worden gebruikt.

Zodra u het Excel-bestand heeft, kunt u beginnen met het analyseren van de gegevens. U kunt bijvoorbeeld de gegevens filteren en Power Pivot gebruiken om ze weer te geven.

Elke keer dat u resultaten exporteert, wordt er een nieuw werkblad gemaakt. Met de optie **Microsoft Excel document (alleen gegevens)** kunt u hetzelfde rapport uitvoeren en opmaakwijzigingen opnieuw gebruiken. Bijvoorbeeld voor Power Pivot kunt u het rapport opnieuw uitvoeren voor een andere periode, de resultaten naar het werkblad kopiëren en het werkblad vervolgens vernieuwen. U vindt ook een rapportage-app op [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> U kunt geen rapport exporteren met meer dan 1,048,576 rijen of 16.384 kolommen. Met Business Central on-premises is het maximum aantal geëxporteerde rijen mogelijk nog lager. Business Central Server bevat een configuratie-instelling, genaamd **Max. gegevensrijen die naar Excel kunnen worden verzonden**, voor het verlagen van de limiet vanaf de maximale waarde. Voor meer informatie zie [Business Central Server configureren](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) of neem contact op met uw beheerder.

## <a name="for-administrators"></a><a name="for-administrators"></a>Voor beheerders

- **Microsoft Excel-document (alleen gegevens)** werd geïntroduceerd als een optionele functie in de releasewave 1 van 2021, update 18.3. Om gebruikers toegang te geven tot deze functie wanneer u 2021 releasewave 1 gebruikt, schakelt u de functie-update **Rapportgegevensset opslaan in Microsoft Excel-document** in **Functiebeheer** in. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management). In releasewave 2 van 2021 wordt deze functie permanent, dus hoeft u deze niet in te schakelen.

- Om **Microsoft Excel-document (alleen gegevens)** te gebruiken hebben gebruikersaccounts de machtiging **Actie Rapportgegevensset exporteren naar Excel toestaan** nodig. U kunt gebruikers deze machtiging geven door de machtiging **Hulpprogramma's voor probleemoplossing** of **Rapport naar Excel exporteren** te verlenen. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie  

## <a name="for-developers-and-advanced-users"></a><a name="for-developers-and-advanced-users"></a>Voor ontwikkelaars en gevorderde gebruikers

De optie **Microsoft Excel-document (alleen gegevens)** exporteert alle kolommen, inclusief kolommen die filters en opmaakinstructies voor andere waarden bevatten. Hier zijn een paar aandachtspunten:

- Binaire gegevens in een veld, zoals een afbeelding, worden niet geëxporteerd.

  In kolommen die binaire gegevens bevatten, bevatten velden de tekst **Binaire gegevens ({0} bytes)**, waar **{0}** het aantal bytes aangeeft.
- Vanaf Business Central 2021 releasewave 2 bevat het Excel-bestand ook het werkblad **Metagegevens rapporteren**.

  Dit werkblad toont de filters die zijn toegepast op het rapport en algemene rapporteigenschappen, zoals de naam, id en extensiedetails. De filters worden weergegeven in de kolom **Filter (DataItem::Table::FilterGroupNo::FieldName)**. De filters in deze kolom bevatten filters die zijn ingesteld op de aanvraagpagina van het rapport. Het bevat ook filters die zijn gedefinieerd in AL-code, bijvoorbeeld door de [eigenschap DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) en de [eigenschap DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Voor meer informatie over rapportontwerp zie [Rapportoverzicht](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Werken met -rapporten](ui-work-report.md)  
[Indelingen van rapporten en documenten beheren](ui-manage-report-layouts.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
