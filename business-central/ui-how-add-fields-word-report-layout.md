---
title: Velden toevoegen aan een Word-rapportlay-out
description: In dit onderwerp wordt beschreven hoe u velden uit een rapportgegevensset toevoegt aan een bestaande Word-rapportlay-out voor een rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 01/25/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Werken met Word-lay-outs

Een Word-rapportlay-out bepaalt de inhoud en opmaak van een rapport wanneer er een voorbeeld van wordt bekeken en het wordt afgedrukt vanuit Business Central. U maakt en wijzigt deze lay-outs met behulp van Microsoft Word.

[![Voorbeeld van een Word-rapportlay-outdocument voor Business Central.](media/word-layout.png)](media/word-layout.png#lightbox) 

Wanneer u een Word-rapportlay-out wijzigt, geeft u op welke velden van de rapportgegevensset in het rapport moeten worden opgenomen en hoe de velden zijn gerangschikt. U definieert ook de algemene opmaak van het rapport, zoals lettertype en -grootte van de tekst, marges en achtergrondafbeeldingen. Meestal rangschikt u de inhoud van het rapport door tabellen aan de lay-out toe te voegen.

U kunt algemene opmaak- en lay-outwijzigingen aanbrengen, zoals het lettertype wijzigen, een tabel toevoegen en aanpassen of een gegevensveld verwijderen, door de basisfuncties voor bewerking van Word te gebruiken, net als in elk ander Word-document.

Als u een nieuwe Word-rapportlay-out ontwerpt of nieuwe gegevensvelden toevoegt, begint u door een tabel te maken die rijen en kolommen bevat die uiteindelijk de gegevensvelden zullen bevatten.

> [!TIP]  
> Geef de tabelrasterlijnen weer zodat u de grenzen van tabelcellen ziet. Verberg de rasterlijnen als u klaar bent met bewerken. Als u tabelrasterlijnen wilt weergeven of verbergen, selecteert u de tabel en kiest u onder **Lay-out** op het tabblad **Tabel** de optie **Rasterlijnen weergeven**.

## Lettertypen insluiten in Word-lay-outs voor consistentie

Als u ervoor wilt zorgen dat rapporten altijd met de beoogde lettertypen worden weergegeven en afgedrukt, ongeacht waar gebruikers de rapporten openen of afdrukken, kunt u de lettertypen insluiten in het Word-document. Houd er echter rekening mee dat insluiten van lettertypen Word-bestanden aanzienlijk groter maakt. Zie voor meer informatie over het insluiten van lettertypen in Word, [Lettertypen insluiten in Word, PowerPoint of Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

## Gegevensvelden toevoegen

Een rapportgegevensset kan bestaan uit velden die labels, gegevens en afbeeldingen bevatten. In dit onderwerp wordt de procedure beschreven om velden uit een rapportgegevensset toe te voegen aan een bestaande Word-rapportlay-out voor een rapport. U voegt velden toe door het aangepaste Word XML-onderdeel voor het rapport te gebruiken en u voegt inhoudsbesturingselementen toe waarmee de velden worden toegewezen aan de rapportgegevensset. Het toevoegen van velden vereist dat u enige kennis van de gegevensset van het rapport hebt, zodat u kunt bepalen welke velden u aan de lay-out wilt toevoegen.  
  
> [!NOTE]  
>  U kunt geen ingebouwde rapportlay-outs wijzigen.<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

###  <a name="OpenXMLPart"></a> Het aangepaste XML-onderdeel voor het rapport openen in Word  
  
1. Open, als het nog niet open is, het Word-document met de rapportlay-out in Word.  
  
     Zie voor meer informatie [Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md).  
  
2. Geef het tabblad **Ontwikkelaar** weer in het lint van Microsoft Word.  
  
     Het tabblad **Ontwikkelaar** wordt standaard niet weergegeven in het lint. Zie voor meer informatie [Het tabblad Ontwikkelaar op het lint weergeven](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3. Kies op het tabblad **Ontwikkelaar** de optie **deelvenster XML-toewijzing**.  
  
4. Kies in het venster **XML-toewijzing** in de vervolgkeuzelijst **Aangepast XML-onderdeel** het aangepaste XML-onderdeel voor het [!INCLUDE[prod_short](includes/prod_short.md)]-rapport, dat meestal het laatste in de lijst is. De naam van het aangepaste XML-gedeelte heeft de volgende indeling:  
  
     `urn:microsoft-dynamics-nav/reports/<report_name>/<ID>`  

     `<report_name>` is de naam die aan het rapport is toegewezen 

     `<ID>` is het identificatienummer van het rapport.  
  
     Nadat u het aangepaste XML-onderdeel hebt geselecteerd, worden in het deelvenster XML-toewijzing de labels en veldbesturingselementen weergegeven die beschikbaar zijn voor het rapport.  
  
### Een label- of gegevensveld toevoegen  
  
1. Plaats de cursor in het document waar u het besturingselement wilt toevoegen.  
  
2. Klik in het venster **XML-toewijzing** met de rechtermuisknop op het besturingselement dat u wilt toevoegen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Onbewerkte tekst**.  
  
    > [!NOTE]  
    >  U kunt een veld toevoegen door handmatig de gegevenssetveldnaam in het inhoudsbesturingselement te typen. U moet het deelvenster **XML-toewijzing** gebruiken om de velden toe te wijzen.  
  
### Als u herhalende rijen met gegevensvelden wilt toevoegen, maakt u een lijst  
  
1. Voeg in een tabel een tabelrij toe die een kolom bevat voor elk veld dat u wilt herhalen.  
  
   Deze rij wordt als tijdelijke aanduiding voor de herhalende velden gebruikt.  
  
2. Selecteer de hele rij.  
  
3. Klik in het venster **XML-koppeling** met de rechtermuisknop op het besturingselement dat correspondeert met het rapportgegevensitem dat de velden bevat die u wilt herhalen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Herhalend**.  
  
4. Voeg de herhalende velden als volgt aan de rij toe:  
  
    1. Plaats de aanwijzer in een kolom.  
  
    2. Klik in het venster **XML-toewijzing** met de rechtermuisknop op het besturingselement dat u wilt toevoegen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Onbewerkte tekst**.  
  
    3. Herhaal stap a en b voor elk veld.  
  
## Afbeeldingsvelden toevoegen

Een rapportgegevensset kan een veld bevatten dat een afbeelding bevat, zoals een bedrijfslogo of een foto van een artikel. Als u een afbeelding uit de rapportgegevensset wilt toevoegen, voegt u een inhoudsbesturingselement van het type **Afbeelding** in.  
  
Afbeeldingen worden in de linkerbovenhoek van het inhoudsbesturingselement uitgelijnd en de grootte ervan wordt automatisch aangepast aan het kader van het inhoudsbesturingselement.  
  
> [!IMPORTANT]  
> U kunt alleen afbeeldingen toevoegen die een indeling hebben die door Word wordt ondersteund (zoals .bmp, .jpeg en .png). Als u een afbeelding toevoegt met een indeling die niet door Word wordt ondersteund, kan een fout optreden wanneer u het rapport uitvoert vanuit de [!INCLUDE[prod_short](includes/prod_short.md)]-client.  
  
### Een afbeelding toevoegen  
  
1. Plaats de aanwijzer in het document waar u het besturingselement wilt toevoegen.  
  
2. Klik in het venster **XML-toewijzing** met de rechtermuisknop op het besturingselement dat u wilt toevoegen, kies **Inhoudsbesturingselement invoegen** en kies vervolgens **Afbeelding**.  
  
3. Als u de afbeelding groter of kleiner wilt maken, versleept u een formaatgreep van of naar het midden van het inhoudsbesturingselement.  

##  <a name="RemoveField"></a> Label- en gegevensvelden verwijderen

Label- en gegevensvelden van een rapport bevinden zich in inhoudsbesturingselementen in Word. De volgende afbeelding is een voorbeeld van een inhoudsbesturingselement wanneer het in een Word-document is geselecteerd.  

![Inhoudsbesturingselement voor veld in Word-rapportlay-out](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

De naam van het label- of gegevensveld wordt weergegeven in het inhoudsbesturingselement. In het voorbeeld is de veldnaam CompanyAddr1.  

### Een label- of gegevensveld verwijderen  

1. Klik met de rechtermuisknop op het veld dat u wilt verwijderen, en kies vervolgens **Inhoudsbesturingselement verwijderen**.  

     Het inhoudsbesturingselement wordt verwijderd, maar de veldnaam blijft als tekst.  

2. Verwijder de resterende tekst indien nodig.

## Overzicht van het aangepaste XML-onderdeel

Word-rapportlay-outs worden gemaakt met *aangepaste XML-onderdelen*. Een aangepast XML-onderdeel van een rapport bestaat uit elementen die corresponderen met de gegevensitems, kolommen en labels die de gegevensset van het rapport vormen. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Het aangepaste XML-onderdeel wordt gebruikt om de gegevens in een rapport toe te wijzen wanneer het rapport wordt uitgevoerd.

### XML-structuur van aangepast XML-onderdeel

De volgende tabel bevat een vereenvoudigd overzicht van de XML van een aangepast XML-onderdeel.  
  
|XML-elementen|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Koptekst|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|XML-naamruimtespecificatie. `<reportname>` is de naam die aan het rapport is toegewezen. `<id>` is de id die aan het rapport is toegewezen.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Bevat alle labels voor het rapport.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Labelelementen die gerelateerd zijn aan kolommen, hebben de indeling `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Labelelementen hebben de indeling `<LabelName>LabelName</LabelName`.<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Labels worden in alfabetische volgorde weergegeven.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Gegevensitem en kolommen. van het hoogste niveau Kolommen worden in alfabetische volgorde weergegeven.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Gegevensitems en kolommen die zijn genest in het gegevensitem van het hoogste niveau. Kolommen worden in alfabetische volgorde weergegeven onder het desbetreffende gegevensitem.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Afsluitend element.|  
  
### Aangepast XML-onderdeel in Word

 In Word opent u het aangepaste XML gedeelte in het deelvenster **XML-toewijzing** en gebruikt u het deelvenster om elementen toe te wijzen aan inhoudsbesturingselementen in het Word-document. Het deelvenster **XML-toewijzing** is toegankelijk vanaf het tabblad **Ontwikkelaar** (zie [Het tabblad Ontwikkelaar op het lint weergeven](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon) voor meer informatie).  
  
 De elementen in het deelvenster **XML-toewijzing** staan in een structuur die lijkt op de XML-bron. Labelvelden worden gegroepeerd onder een gemeenschappelijk **Labels**-element en gegevensitems en kolommen worden gerangschikt in een hiërarchische structuur die met de XML-bron overeenkomt, met de kolommen weergegeven in alfabetische volgorde. Elementen worden geïdentificeerd op basis van hun kolomnaam, zoals gedefinieerd in de gegevensset van het rapport, in AL-code. Zie voor meer informatie [Een rapportgegevensset definiëren](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 De volgende afbeelding illustreert het eenvoudige aangepaste XML-onderdeel uit de vorige sectie in het deelvenster **XML-toewijzing** van een Word-document.  
  
 ![Clip van het venster XML-toewijzing in Word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
* Als u een label of veld aan de lay-out wilt toevoegen, voegt u een inhoudsbesturingselement in dat is gekoppeld aan het element in het deelvenster **XML-toewijzing**.  
  
* Als u herhalende rijen met kolommen wilt maken, voegt u een **Herhalend** inhoudsbesturingselement voor het bovenliggende gegevensitemelement in en voegt u vervolgens een inhoudsbesturingselement voor de kolommen toe.  
  
* Voor labels is de werkelijke tekst die in het gegenereerde rapport wordt weergegeven, de waarde van de eigenschap **Bijschrift** voor het veld in de gegevensitemtabel (als het label gerelateerd is aan de kolom in de rapportgegevensset), of een label in Report Label Designer (als het label niet gerelateerd is aan een kolom in de gegevensset).  
  
* De taal van het label dat wordt weergegeven wanneer u het rapport uitvoert, hangt af van de taalinstelling van het rapportobject.  
  
## Zie ook

[Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
