---
title: Aangepaste indelingen voor rapporten en documenten maken en wijzigen
description: 'Leren hoe u aangepaste lay-outs maakt om de weergave aan te passen van een rapport wanneer het wordt bekeken, afgedrukt of opgeslagen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/06/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(verouderd) Aangepaste rapportlay-outs maken en wijzigen

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Standaard hebben rapporten een ingebouwde rapportlay-out. De rapportlay-out kan een RDLC-rapportlay-out (Report Definition Language Client-Side) zijn, of een Microsoft Word-rapportlay-out, of beide. U kunt ingebouwde lay-outs niet wijzigen, maar u kunt wel aangepaste lay-outs maken. Een rapport kan meerdere aangepaste rapportlay-outs hebben.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] omvat de term 'rapport' ook documenten die extern worden verspreid, zoals verkoopfacturen en orderbevestigingen die u aan klanten als pdf-bestanden verzendt.

Om een aangepaste lay-out te maken kopieert u een bestaande aangepaste lay-out of voegt u een nieuwe aangepaste lay-out toe. Aangepaste lay-outs zijn vaak gebaseerd op een ingebouwde lay-out. Wanneer u een nieuwe aangepaste lay-out toevoegt, kunt u een RDLC-rapportlay-out, een Word-rapportlay-out of beide kiezen. De nieuwe aangepaste lay-out wordt gebaseerd op de ingebouwde lay-out voor het rapport, als er een is. Als er geen ingebouwde lay-out voor het type is, wordt er een nieuwe lege lay-out gemaakt. U moet deze lege lay-out helemaal opnieuw aanpassen en ontwerpen. Zie [Rapportlay-outs beheren](ui-manage-report-layouts.md) voor meer informatie over RDLC- en Word-rapportlay-outs, ingebouwde en aangepaste lay-outs.  

> [!TIP]
> Gebruik financiële rapporten om inzicht te krijgen in de financiële gegevens die in uw rekeningschema zijn opgeslagen. Meer informatie op [Financiële rapportage voorbereiden met financiële gegevens en accountcategorieën](bi-how-work-account-schedule.md).

Nadat u uw aangepaste rapportlay-outs hebt gedefinieerd, kunt u deze selecteren op de pagina met de klantenkaart en de leverancierskaart. De lay-outs worden dan gebruikt wanneer u documenten voor de klant of leverancier maakt. Meer informatie op [Documentlay-outs definiëren voor klanten en leveranciers](ui-define-customer-vendor-document-layouts.md).

U kunt ook aangepaste rapportlay-outs gebruiken om inhoud aan e-mailberichten toe te voegen. Rapportlay-outs kunnen tijd besparen en zorgen voor consistentie door dezelfde inhoud opnieuw te gebruiken wanneer u met uw klanten communiceert. Als u aangepaste rapportlay-outs met e-mail wilt gebruiken, moet het bestandstype voor de lay-out Word zijn en kunt u RDLC niet gebruiken. Meer informatie op [Herbruikbare e-mailteksten en lay-outs instellen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a>Een aangepaste lay-out maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Selectie rapportlay-out** in en kies vervolgens de gerelateerde koppeling.

    De pagina **Selectie rapportlay-out** bevat een overzicht van alle rapporten die beschikbaar zijn in het bedrijf dat in het veld **Bedrijfsnaam** boven aan de pagina wordt opgegeven.
2. Kies in het veld **Bedrijfsnaam** het bedrijf waarvoor u de rapportlay-out wilt maken.
3. Selecteer de rij voor het rapport waarvoor u de lay-out wilt maken en kies vervolgens de actie **Aangepaste lay-outs**.  

   Op de pagina **Aangepaste rapportlay-outs** worden alle aangepaste lay-outs weergegeven die beschikbaar zijn voor het geselecteerde rapport.
4. Als u een kopie van een bestaande aangepaste lay-out wilt maken, selecteert u de bestaande aangepaste lay-out in de lijst en kiest u de actie **Kopiëren**.  

   De kopie van de aangepaste lay-out wordt op de pagina **Aangepaste rapportlay-outs** weergegeven en bevat de woorden *Kopie van* in het veld **Beschrijving**.
5. Als u een nieuwe aangepaste lay-out wilt toevoegen die op een ingebouwde lay-out is gebaseerd, volgt u deze stappen:  
   1. Kies de actie **Nieuw**. De pagina **Ingebouwde lay-out voor een rapport invoegen** verschijnt met de velden **Id** en **Naam** automatisch ingevuld.
   2. Zet de schakelaar **Word-lay-out invoegen** aan om een aangepast Word-rapportlay-outtype toe te voegen OF zet de schakelaar **RDLC-lay-out invoegen** aan om een aangepast RDLC-rapportlay-outtype toe te voegen.
   4. Kies de knop **Ok**.  

    De nieuwe aangepaste lay-out wordt nu weergegeven op de pagina **Aangepaste rapportlay-outs**. Als een nieuwe lay-out wordt gebaseerd op een ingebouwde lay-out, bevat deze de woorden **Kopie van een ingebouwde lay-out** in het veld **Beschrijving**. Als er geen ingebouwde lay-out voor het rapport was, bevat de nieuwe lay-out de woorden **Nieuwe lay-out** in het veld **Beschrijving**, wat aangeeft dat de aangepaste lay-out leeg is.
6. Standaard is het veld **Bedrijfsnaam** leeg, wat betekent dat de aangepaste lay-out beschikbaar voor rapporten is in alle bedrijven. Als u de aangepaste lay-out alleen beschikbaar wilt maken voor een specifiek bedrijf, kiest u **Bewerken** en stelt u het veld **Bedrijfsnaam** in op het gewenste bedrijf.

De aangepaste lay-out is gemaakt en u kunt deze naar wens aanpassen.

> [!TIP]
> U kunt de rapportresultaten exporteren naar een Microsoft Excel-bestand om de volledige gegevensset te bekijken, inclusief alle kolommen, maar zonder de lay-out. Het Excel-bestand kan u helpen te valideren dat het rapport de verwachte gegevens retourneert of om problemen vast te stellen. Zie voor meer informatie [Rapportgegevens analyseren met Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Een aangepaste lay-out wijzigen

Als u een aangepaste rapportlay-out wilt wijzigen, moet u de rapportlay-out eerst als bestand exporteren naar een locatie op uw computer of netwerk. Open vervolgens het geëxporteerde document en breng de wijzigingen aan. Wanneer u klaar bent met het aanbrengen van de wijzigingen, importeert u de rapportlay-out.

### <a name="modify-a-custom-layout"></a>Een aangepaste lay-out wijzigen

1. Exporteer een aangepaste lay-out vanuit de pagina **Aangepaste rapportlay-outs**. Als die pagina nog niet is geopend, zoekt en opent u de pagina **Selectie rapportlay-out**, selecteert u het rapport met de lay-out die u wilt wijzigen, en kiest u de actie **Aangepaste lay-outs**.  
2. Op de pagina **Aangepaste rapportlay-outs** selecteert u de lay-out die u wilt wijzigen. Vervolgens kiest u de actie **Lay-out exporteren** en **Opslaan** of **Opslaan als** om de rapportlay-out op te slaan op uw computer of netwerk.  
3. Open het rapportlay-outdocument dat u hebt opgeslagen en breng wijzigingen aan.

   Als u een Word-lay-out wijzigt, wordt het lay-outdocument in Word geopend. Lees meer over het bewerken van Word-rapporten op [Werken met Word-lay-outs](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC-rapportlay-outs zijn geavanceerder dan Word-RDLC-rapportlay-outs. Leer meer over het aanpassen van een RDLC-rapportlay-out op [RDLC-rapportlay-outs ontwerpen](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Sla uw wijzigingen op wanneer u klaar bent.

4. Keer terug naar de pagina **Aangepaste rapportlay-outs**, selecteer de geëxporteerde en gewijzigde rapportlay-out en kies vervolgens de actie **Lay-out importeren**.  

5. Selecteer in het dialoogvenster **Importeren** de optie **Kiezen**, selecteer het gewijzigde rapportlay-outdocument en kies vervolgens **Openen**.

> [!IMPORTANT]
> Vergeet niet om het rapportlay-outdocument dat u hebt gewijzigd te importeren. Anders is de nieuwe rapportlay-out niet beschikbaar.

<!--
## <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a>Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

### <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a>Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>To remove a label or data field

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### <a name="adding-data-fields"></a>Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-also"></a>Zie ook

[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[De huidige rapportindeling wijzigen](ui-how-change-layout-currently-used-report.md)  
[Een aangepaste indeling voor een rapport of document importeren of exporteren](ui-how-import-and-export-report-layout.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  
[Financiële rapportage voorbereiden met financiële gegevens en accountcategorieën](bi-how-work-account-schedule.md)  
[Bedrijfsinformatie](bi.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
