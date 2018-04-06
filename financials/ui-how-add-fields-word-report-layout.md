---
title: Velden toevoegen aan een Word-rapportlay-out | Microsoft Docs
description: Hier wordt beschreven hoe u velden uit een rapportgegevensset toevoegt aan een bestaande Word-rapportlay-out voor een rapport.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 77f377d6858294aeb54e30fcb178fc9757ac3938
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="add-fields-to-a-word-report-layout"></a>Velden toevoegen aan een Word-rapportlay-out
Een rapportgegevensset kan bestaan uit velden die labels, gegevens en afbeeldingen bevatten. In dit onderwerp wordt de procedure beschreven om velden uit een rapportgegevensset toe te voegen aan een bestaande Word-rapportlay-out voor een rapport. U voegt velden toe door het aangepaste Word XML-onderdeel voor het rapport te gebruiken en u voegt inhoudsbesturingselementen toe waarmee de velden worden toegewezen aan de rapportgegevensset. Het toevoegen van velden vereist dat u enige kennis van de gegevensset van het rapport hebt, zodat u kunt bepalen welke velden u aan de lay-out wilt toevoegen.  
  
> [!NOTE]  
>  U kunt geen ingebouwde rapportlay-outs wijzigen<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="OpenXMLPart"></a>Het aangepaste XML-onderdeel voor het rapport openen in Word  
  
1.  Open, als het nog niet open is, het Word-document met de rapportlay-out in Word.  
  
     Zie voor meer informatie [Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md).  
  
2.  Geef het tabblad **Ontwikkelaar** weer in het lint van Microsoft Word.  
  
     Het tabblad **Ontwikkelaar** wordt standaard niet weergegeven in het lint. Zie voor meer informatie [Het tabblad Ontwikkelaar op het lint weergeven](http://go.microsoft.com/fwlink/?LinkID=389631).  
  
3.  Kies op het tabblad **Ontwikkelaar** de optie **deelvenster XML-toewijzing**.  
  
4.  In het venster **XML-toewijzing** kiest u in de vervolgkeuzelijst **Aangepast XML-onderdeel** het aangepaste XML-onderdeel voor het ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->-rapport, dat meestal het laatste in de lijst is. De naam van het aangepaste XML-gedeelte heeft de volgende indeling:  
  
     urn:microsoft-dynamics-nav/reports/*report_name*/*ID*  
  
     *report_name* is de naam die is toegewezen aan het rapport<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *Id* is het identificatienummer van het rapport.  
  
     Nadat u het aangepaste XML-onderdeel hebt geselecteerd, worden in het deelvenster XML-toewijzing de labels en veldbesturingselementen weergegeven die beschikbaar zijn voor het rapport.  
  
### <a name="to-add-a-label-or-data-field"></a>Een label- of gegevensveld toevoegen  
  
1.  Plaats de cursor in het document waar u het besturingselement wilt toevoegen.  
  
2.  Klik in het venster **XML-toewijzing** met de rechtermuisknop op het besturingselement dat u wilt toevoegen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Onbewerkte tekst**.  
  
    > [!NOTE]  
    >  U kunt een veld toevoegen door handmatig de gegevenssetveldnaam in het inhoudsbesturingselement te typen. U moet het deelvenster **XML-toewijzing** gebruiken om de velden toe te wijzen.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Als u herhalende rijen met gegevensvelden wilt toevoegen, maakt u een lijst  
  
1.  Voeg in een tabel een tabelrij toe die een kolom bevat voor elk veld dat u wilt herhalen.  
  
     Deze rij wordt als tijdelijke aanduiding voor de herhalende velden gebruikt.  
  
2.  Selecteer de hele rij.  
  
3.  Klik in het venster **XML-koppeling** met de rechtermuisknop op het besturingselement dat correspondeert met het rapportgegevensitem dat de velden bevat die u wilt herhalen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Herhalend**.  
  
4.  Voeg de herhalende velden als volgt aan de rij toe:  
  
    1.  Plaats de aanwijzer in een kolom.  
  
    2.  Klik in het venster **XML-toewijzing** met de rechtermuisknop op het besturingselement dat u wilt toevoegen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Onbewerkte tekst**.  
  
    3.  Herhaal stap a en b voor elk veld.  
  
## <a name="adding-image-fields"></a>Afbeeldingsvelden toevoegen  
 Een rapportgegevensset kan een veld bevatten dat een afbeelding bevat, zoals een bedrijfslogo of een foto van een artikel. Als u een afbeelding uit de rapportgegevensset wilt toevoegen, voegt u een inhoudsbesturingselement van het type **Afbeelding** in.  
  
 Afbeeldingen worden in de linkerbovenhoek van het inhoudsbesturingselement uitgelijnd en de grootte ervan wordt automatisch aangepast aan het kader van het inhoudsbesturingselement.  
  
> [!IMPORTANT]  
>  U kunt alleen afbeeldingen toevoegen die een indeling hebben die door Word wordt ondersteund (zoals .bmp, .jpeg en .png). Als u een afbeelding toevoegt met een indeling die niet door Word wordt ondersteund, kan een fout optreden wanneer u het rapport uitvoert vanuit de ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->-client.  
  
#### <a name="to-add-an-image"></a>Een afbeelding toevoegen  
  
1.  Plaats de aanwijzer in het document waar u het besturingselement wilt toevoegen.  
  
2.  Klik in het venster **XML-toewijzing** met de rechtermuisknop op het besturingselement dat u wilt toevoegen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Afbeelding**.  
  
3.  Als u de afbeelding groter of kleiner wilt maken, versleept u een formaatgreep van of naar het midden van het inhoudsbesturingselement.  

## <a name="custom-xml-part-overview"></a>Overzicht van het aangepaste XML-onderdeel
Word-rapportlay-outs worden gemaakt met *aangepaste XML-onderdelen*. Een aangepast XML-onderdeel van een rapport bestaat uit elementen die corresponderen met de gegevensitems, kolommen en labels die de gegevensset van het rapport vormen. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Het aangepaste XML-onderdeel wordt gebruikt om de gegevens in een rapport toe te wijzen wanneer het rapport wordt uitgevoerd.

  
### <a name="xml-structure-of-custom-xml-part"></a>XML-structuur van aangepast XML-onderdeel  
De volgende tabel bevat een vereenvoudigd overzicht van de XML van een aangepast XML-onderdeel.  
  
|XML-elementen|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Koptekst|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|XML-naamruimtespecificatie. `<reportname>` is de naam die aan het rapport is toegewezen. `<id>` is de id die aan het rapport is toegewezen.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Bevat alle labels voor het rapport.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--><br />-   Labelelementen die gerelateerd zijn aan kolommen, hebben de indeling `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />-  Labelelementen hebben de indeling `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Labels worden in alfabetische volgorde weergegeven.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Gegevensitem en kolommen. van het hoogste niveau Kolommen worden in alfabetische volgorde weergegeven.<!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Gegevensitems en kolommen die zijn genest in het gegevensitem van het hoogste niveau. Kolommen worden in alfabetische volgorde weergegeven onder het desbetreffende gegevensitem.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Afsluitend element.|  
  
### <a name="custom-xml-part-in-word"></a>Aangepast XML-onderdeel in Word  
 In Word opent u het aangepaste XML gedeelte in het deelvenster **XML-toewijzing** en gebruikt u het deelvenster om elementen toe te wijzen aan inhoudsbesturingselementen in het Word-document. Het deelvenster **XML-toewijzing** is toegankelijk vanaf het tabblad **Ontwikkelaar** (zie [Het tabblad Ontwikkelaar op het lint weergeven](http://go.microsoft.com/fwlink/?LinkID=389631) voor meer informatie).  
  
 De elementen in het deelvenster **XML-toewijzing** staan in een structuur die lijkt op de XML-bron. Labelvelden worden gegroepeerd onder een gemeenschappelijk **Labels**-element en gegevensitems en kolommen worden gerangschikt in een hiërarchische structuur die met de XML-bron overeenkomt, met de kolommen weergegeven in alfabetische volgorde. Elementen worden geïdentificeerd op basis van hun naam, zoals gedefinieerd door de eigenschap Naam in Report Dataset Designer in ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.  
  
 De volgende afbeelding illustreert het eenvoudige aangepaste XML-onderdeel uit de vorige sectie in het deelvenster **XML-toewijzing** van een Word-document.  
  
 ![Clip van het deelvenster XML-toewijzing in Word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Als u een label of veld aan de lay-out wilt toevoegen, voegt u een inhoudsbesturingselement in dat is gekoppeld aan het element in het deelvenster **XML-toewijzing**.  
  
-   Als u herhalende rijen met kolommen wilt maken, voegt u een **Herhalend** inhoudsbesturingselement voor het bovenliggende gegevensitemelement in en voegt u vervolgens een inhoudsbesturingselement voor de kolommen toe.  
  
-   Voor labels is de werkelijke tekst die in het gegenereerde rapport wordt weergegeven, de waarde van de eigenschap **Bijschrift** voor het veld in de gegevensitemtabel (als het label gerelateerd is aan de kolom in de rapportgegevensset), of een label in Report Label Designer (als het label niet gerelateerd is aan een kolom in de gegevensset).  
  
-   De taal van het label dat wordt weergegeven wanneer u het rapport uitvoert, hangt af van de taalinstelling van het rapportobject. <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a>Zie ook  
 [Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md)   
