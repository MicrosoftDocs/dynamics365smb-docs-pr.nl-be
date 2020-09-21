---
title: Aangepaste Power BI-rapporten voor Business Central-gegevens weergeven | Microsoft Docs
description: U kunt Power BI-rapporten gebruiken om extra inzicht te krijgen in gegevens in lijsten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 5d3acaf05952a61845eb8bb72b2556f2e54f8208
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697710"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a>Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prodshort](includes/prodshort.md)]

In [!INCLUDE[prodlong](includes/prodlong.md)] is in een aantal belangrijke lijstpagina's het besturingselement Feitenblok opgenomen, waarmee lezers van het rapport extra inzicht kunnen krijgen in de gegevens in de lijst. Wanneer u tussen rijen in de lijst verplaatst, wordt het rapport bijgewerkt en voor de geselecteerde post gefilterd. U kunt aangepaste rapporten maken om in dit besturingselement weer te geven. Er zijn echter een paar regels die u moet volgen om ervoor te zorgen dat rapporten werken zoals verwacht.  

## <a name="prerequisites"></a>Vereisten

- Een Power BI-account.
- Power BI Desktop.

Zie [[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md) voor meer informatie om aan de slag te gaan.

## <a name="defining-the-report-data-set"></a>De rapportgegevensset definiëren

Geef de gegevensbron op die de gegevens bevat die gerelateerd zijn aan de lijst. Als u bijvoorbeeld een rapport wilt maken voor de lijst Verkoop, moet u ervoor zorgen dat de gegevensset informatie bevat die verband houdt met de verkoop.  

## <a name="defining-the-report-filter"></a>Het rapportfilter definiëren

Als u wilt dat de gegevens worden bijgewerkt op basis van de geselecteerde record in de lijst, voegt u een filter toe aan het rapport. Het filter moet een veld bevatten van de gegevensbron die wordt gebruikt als *primaire sleutel*. In de meeste gevallen is de primaire sleutel voor een lijst **Nr.** toevoegen.

Als u een filter voor het rapport wilt definiëren, selecteert u de primaire sleutel in de lijst met beschikbare velden en sleept u dat veld vervolgens en zet u het neer in de sectie **Rapportfilter**. Het filter moet een basisrapportfilter zijn. Het kan geen pagina, visueel element of geavanceerd filter zijn. 

![Het rapportfilter instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="setting-the-report-size-and-color"></a>De rapportgrootte en kleur instellen

De grootte van het rapport moet worden ingesteld op 325 bij 310 pixels. Deze grootte is vereist voor een juiste schaling van het rapport in de beschikbare ruimte van het Power BI-besturingselement Feitenblok in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als u de grootte van het rapport wilt definiëren, plaatst u de focus buiten het rapportlay-outgebied en kiest u vervolgens het pictogram met de verfroller.

![De breedte en hoogte van het rapport instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

U kunt de breedte en hoogte van het rapport wijzigen door **Aangepast** in het veld **Soort** te kiezen.

Als u wilt dat de achtergrond van het rapport wordt vermengd met de achtergrondkleur van het Power BI-besturingselement Feitenblok, stelt u de achtergrondkleur van het rapport in op *#FFFFFF*. 

## <a name="using-reports-with-multiple-pages"></a>Rapporten met meerdere pagina's gebruiken

Met Power BI kunt u één rapport met meerdere pagina's maken. Voor rapporten die worden weergegeven met lijstpagina's, raden we echter af om meer dan één pagina te gebruiken. In het Power BI-besturingselement Feitenblok wordt alleen de eerste pagina van uw rapport weergegeven.

## <a name="naming-the-report"></a>Het rapport een naam geven

Geef het rapport een naam die de naam bevat van de lijstpagina die aan het rapport is gekoppeld. Is het rapport bijvoorbeeld gemaakt voor de lijstpagina **Verkoper**, neem dan het woord *verkoper* op in de naam.  

Deze naamgevingsconventie is geen vereiste. Deze zorgt er echter wel voor dat gebruikers de gewenste rapporten sneller kunnen selecteren in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Wanneer de rapportselectiepagina wordt geopend vanuit een lijstpagina, wordt de lijst met rapporten automatisch gefilterd op basis van de paginanaam. De rapporten worden gefilterd om het aantal weergegeven rapporten te beperken. Gebruikers kunnen het filter ook verwijderen als ze de volledige lijst met rapporten die beschikbaar zijn in Power BI, willen bekijken.  

## <a name="fixing-problems"></a>Problemen oplossen

Dit gedeelte bevat een tijdelijke oplossing voor de meest voorkomende problemen die zich kunnen voordoen wanneer u het Power BI-rapport maakt.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>U ziet geen rapport op de pagina Rapport selecteren

Dit komt waarschijnlijk omdat de naam van het rapport niet de naam van de lijstpagina bevat. Wis het filter om de volledige lijst met rapporten die beschikbaar zijn in Power BI, weer te geven.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Het rapport is geladen, maar is leeg, niet gefilterd of onjuist gefilterd

Controleer of het rapportfilter de juiste primaire sleutel bevat. In de meeste gevallen is dit het veld **Nr.** maar in de tabel **Grootboekpost** moet u bijvoorbeeld het veld **Postnr.** gebruiken.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Het rapport is geladen, maar er wordt een pagina weergegeven die u niet had verwacht

Controleer of de pagina die u wilt weergeven, de eerste pagina in uw rapport is.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Rapporten worden met ongewenste grijze randen weergegeven, zijn te klein of te groot

Controleer of de grootte van het rapport is ingesteld op 325 x 310 pixels. Sla het rapport op en vernieuw vervolgens de lijstpagina.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Uw bedrijfsgegevens inschakelen voor Power BI](admin-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[Aan de slag](product-get-started.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
