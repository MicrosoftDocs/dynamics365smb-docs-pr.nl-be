---
title: Aan de slag met het maken van lay-outs
description: 'Leren hoe u lay-outs maakt om de weergave aan te passen van een rapport wanneer het wordt bekeken, afgedrukt of opgeslagen.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
---
# <a name="get-started-creating-report-layouts"></a>Aan de slag met het maken van rapportlay-outs

Business Central wordt geleverd met veel ingebouwde lay-outs die u in uw rapporten kunt gebruiken. Andere lay-outs zijn mogelijk toegevoegd als onderdeel van andere extensies. Maar het is ook mogelijk om vanuit het niets of op basis van een bestaande lay-out uw eigen rapporten te maken.

> [!IMPORTANT]
> U kunt ook rapportlay-outs gebruiken om inhoud aan e-mailberichten toe te voegen. Rapportlay-outs kunnen bijvoorbeeld tijd besparen en zorgen voor consistentie door dezelfde inhoud opnieuw te gebruiken wanneer u met uw klanten communiceert. Als u aangepaste rapportlay-outs met e-mail wilt gebruiken, moet het bestandstype voor de lay-out Word zijn. U kunt het RDLC-bestandstype niet gebruiken. Voor meer informatie zie [Herbruikbare e-mailteksten en lay-outs instellen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="overview"></a>Overzicht

Bij het werken met rapportlay-outs helpt het om de lay-out te zien als een bestand dat wordt geïmporteerd en toegewezen aan een rapport. Ongeacht het type lay-out is de manier waarop u lay-outs beheert in Business Central in principe hetzelfde. Meestal werkt u vanuit de pagina **Rapportlay-outs**. Het belangrijkste verschil is hoe u de lay-out ontwerpt, wat wordt gedaan met behulp van de toepassingssoftware waarop de lay-out is gebouwd, zoals Word, Excel of SQL Server Report Builder.

Met dit idee in gedachten, zijn er in principe drie of vier taken betrokken bij het instellen van een lay-out voor een rapport:

1. Bepaal het type lay-out.
2. Exporteer een kopie van een bestaande lay-out om als uitgangspunt te gebruiken.
3. Breng wijzigingen aan in het lay-outbestand in de juiste toepassing.
4. Voeg het nieuwe lay-outbestand toe aan het rapport.

> [!IMPORTANT]
> U kunt een lay-out van een extensie niet wijzigen of vervangen. Dit is een lay-out die afkomstig is van een extensie. Alleen door de gebruiker ingestelde lay-outs kunt u wijzigen of verwijderen. Op de pagina **Rapportlay-outs** kunt u zien of de lay-out een extensielay-out of een door de gebruiker ingestelde lay-out is door te kijken in de kolom **Extensie**. Een extensielay-out toont informatie over de bronextensie in de kolom. De kolom **Extensie** zal leeg zijn voor een door de gebruiker ingestelde lay-out.
>
> Voor meer informatie over het verschil tussen extensielay-outs en door de gebruiker ingestelde lay-outs, zie [Lay-outbron](ui-manage-report-layouts.md#layout-sources).

## <a name="get-started"></a>Aan de slag

Afhankelijk van wat uw situatie is, zullen de daadwerkelijke taken variëren. Gebruik de volgende tabel om u op weg te helpen.

|Wat u wilt doen?|Zie...|
|-----------------------|------|
|Uitzoeken wat het beste lay-outtype is om te gebruiken voor mijn situatie|[Bepalen welk type lay-out u wilt](#decide)|
|Maak een nieuwe lay-out voor een rapport, die is gebaseerd op een bestaande lay-out, waarbij de bestaande lay-out behouden blijft.|[Een nieuwe lay-out maken](#create)|
|Wijzigingen aanbrengen in een bestaande lay-out die in een rapport wordt gebruikt|[Een lay-out wijzigen](#modify)|
|Ik heb een nieuwe versie van een lay-outbestand voor een rapport. In wil het bestaande lay-outbestand vervangen.|[Een lay-out vervangen](#replace)|
|Van de huidige lay-out die door een rapport wordt gebruikt, overschakelen naar een andere lay-out|[De lay-out instellen die door een rapport wordt gebruikt](ui-set-report-layout.md)|
|De naam en beschrijving van een lay-out wijzigen|[De naam van een lay-out wijzigen](#rename)|

## <a name="decide-what-type-of-layout-you-want"></a><a name="decide"></a>Bepalen welk type lay-out u wilt

Het eerste dat u moet doen bij het maken van een lay-out, is beslissen welk [lay-outtype](ui-manage-report-layouts.md#layout-types) u wilt. U kunt kiezen uit Word, Excel of RDLC. Het lay-outtype is afhankelijk van hoe u wilt dat het gegenereerde rapport eruitziet. Bovendien hangt het af van uw kennis van toepassingssoftware voor het maken van de lay-outs, zoals Word, Excel en SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-lay-outs zijn over het algemeen het gemakkelijkst te maken en aan te passen, omdat de functies voor het samenvatten van gegevens, het toevoegen van afbeeldingen en het opmaken, veelgebruikte Excel-functies zijn.

* Niet alle rapporten en documenten hebben een gegevensset die geoptimaliseerd is voor gebruik met een Excel-lay-out. Samenvoegingen en complexe berekeningen werken bijvoorbeeld het beste met RDLC- of Word-lay-outs. Hetzelfde geldt voor documenten.

* Als u alleen stijlwijzigingen aanbrengt, zoals lettertype, grootte en kleuren, is een Word-lay-out ook een goede keuze.

* Het toevoegen van gegevensvelden of het herschikken van gegevensvelden in Word of RDLC is geavanceerder dan bij Excel.

* Word- en RDLC-lay-outs zijn goed te gebruiken voor rapporten die uiteindelijk worden afgedrukt.  

* De algemene grondslagen voor Word- en RDLC-lay-outs lijken op elkaar. Elk type heeft echter bepaalde ontwerpfuncties die bepalen hoe het gegenereerde rapport eruitziet in [!INCLUDE[prod_short](includes/prod_short.md)]. Hetzelfde rapport kan er anders uitzien wanneer u de Word-lay-out gebruikt dan wanneer u de RDLC-rapportlay-out gebruikt.

## <a name="create-a-new-layout"></a><a name="create"></a>Een nieuwe lay-out maken

Er zijn twee manieren om een nieuwe lay-out te maken van een bestaande lay-out. Eén manier is door de bestaande lay-out op te slaan als een kopie. De andere manier is om de bestaande lay-out te exporteren.

## [Kopiëren](#tab/copy)

Kopiëren is een snelle manier om een nieuwe lay-out te maken die hetzelfde is als een bestaande lay-out. Zodra u de kopie hebt, brengt u wijzigingen aan door de lay-out te exporteren. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer de lay-out waarvan u een kopie wilt hebben voor uw nieuwe lay-out en kies vervolgens de actie **Info bewerken**.

    Als u een extensielay-out hebt geselecteerd, wordt u gevraagd of u een kopie wilt bewerken. Als u wilt doorgaan, selecteert u **Ja**.

    > [!TIP]
    > Om u te helpen de lay-out te vinden, gebruikt u het vak **Zoeken**, het deelvenster **Filter** en kolommen sorteren.
3. Wijzig de **Lay-outnaam**.
4. Zet de schakelaar **Wijzigingen in kopie opslaan** op **Aan** en selecteer vervolgens **OK**.

   De nieuwe lay-out wordt weergegeven op de pagina **Rapportlay-outs**.
5. Zie [Een bestaande lay-out wijzigen](#modify) als u wijzigingen wilt aanbrengen in de nieuwe lay-out.

### [Exporteren/importeren](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer de lay-out waarvan u een kopie wilt hebben voor uw nieuwe lay-out en kies vervolgens de actie **Lay-out exporteren**.

   Het lay-outbestand wordt naar uw apparaat gedownload. 

    > [!TIP]
    > Om u te helpen de lay-out te vinden, gebruikt u het vak **Zoeken**, het deelvenster **Filter** en kolommen sorteren.

3. Open het lay-outbestand in de juiste toepassing, zoals Word (voor een .docx-bestand) of Excel (voor een .xlsx-bestand).

   Zie voor meer informatie:

   * [Werken met Word-indelingen](ui-how-add-fields-word-report-layout.md)
   * [Werken met Excel-indelingen](ui-excel-report-layouts.md)
   * [Werken met RDLC-indelingen](ui-rdlc-report-layouts.md)

   Breng wijzigingen aan in het bestand en sla het op.

4. Terug op de pagina **Rapportlay-outs**, selecteert u d actie **Nieuwe layout**.
5. Vul de volgende velden in:

   |Veld|Omschrijving|Verplicht|
   |-----|-----------|---------|
   |Rapport-id|Ingesteld op de id die aan het rapport is toegewezen|ja|
   |Lay-outnaam| Typ een korte beschrijvende naam voor de lay-out zodat u deze gemakkelijk kunt herkennen.|ja|
   |Omschrijving| Typ meer gedetailleerde informatie over de lay-out. |nee|
   |Opties voor opmaak|Stel dit veld in op het type lay-out, zoals Word, Excel of RDLC.|ja|

6. Selecteer **OK** en voer vervolgens een van de volgende stappen uit om het lay-outbestand voor het rapport te uploaden:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Het geselecteerde bestand wordt geüpload naar de lay-out en u keert terug naar de pagina **Rapportlay-outs**.

Als u wilt zien hoe het rapport eruitziet met de nieuwe lay-out, selecteert u de lay-out in de lijst en selecteert u vervolgens **Rapport uitvoeren**.

---

## <a name="modify-a-layout"></a><a name="modify"></a>Een lay-out wijzigen

Volg deze stappen om een bestaande, door de gebruiker ingestelde lay-out te wijzigen.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer de lay-out die u wilt bewerken en kies vervolgens de actie **Lay-out exporteren**.

   Het lay-outbestand wordt naar uw apparaat gedownload. 

   > [!TIP]
   > Om u te helpen de lay-out te vinden, gebruikt u het vak **Zoeken**, het deelvenster **Filter** en kolommen sorteren.

3. Open het lay-outbestand in de juiste toepassing, zoals Word (voor een .docx-bestand) of Excel (voor een .xlsx-bestand).

   Zie voor meer informatie:

   * [Werken met Word-indelingen](ui-how-add-fields-word-report-layout.md)
   * [Werken met Excel-indelingen](ui-excel-report-layouts.md)
   * [Werken met RDLC-indelingen](ui-rdlc-report-layouts.md)

   Breng wijzigingen aan in het bestand en sla het op.

4. Terug op de pagina **Rapportlay-outs** selecteert u de bestaande lay-out en vervolgens de actie **Lay-out vervangen**.
5. Selecteer **OK** > **Kiezen** om de bestandsverkenner op uw apparaat te openen.
6. Zoek en selecteer het Excel-bestand en kies vervolgens **Openen**.

   Het geselecteerde bestand wordt geüpload naar de lay-out en u keert terug naar de pagina **Rapportlay-outs**.
7. Als u wilt zien hoe het rapport eruitziet met de nieuwe lay-out, selecteert u de lay-out in de lijst en selecteert u vervolgens **Rapport uitvoeren**.

## <a name="replace-a-layout"></a><a name="replace"></a>Een lay-out vervangen

Volg deze stappen om het bestaande bestand met de door de gebruiker ingestelde lay-out te vervangen door een nieuw bestand.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer de bestaande lay-out en selecteer vervolgens de actie **Lay-out vervangen**.
3. Selecteer **OK** > **Kiezen** om de bestandsverkenner op uw apparaat te openen.
4. Zoek en selecteer het Excel-bestand en kies vervolgens **Openen**.

   Het geselecteerde bestand wordt geüpload naar de lay-out en u keert terug naar de pagina **Rapportlay-outs**.
5. Als u wilt zien hoe het rapport eruitziet met de nieuwe lay-out, selecteert u de lay-out in de lijst en selecteert u vervolgens **Rapport uitvoeren**.

## <a name="rename-a-layout"></a><a name="rename"></a>De naam van een lay-out wijzigen

Volg deze stappen als u de naam en beschrijving van een door de gebruiker ingestelde lay-out wilt wijzigen.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer de lay-out waarvan u de naam wilt wijzigen en kies vervolgens de actie **Info bewerken**.

    > [!TIP]
    > Om u te helpen de lay-out te vinden, gebruikt u het vak **Zoeken**, het deelvenster **Filter** en kolommen sorteren.
3. Verander de **Lay-outnaam** en selecteer vervolgens **OK**.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met Word-indelingen](ui-how-add-fields-word-report-layout.md)  
[Werken met Excel-lay-outs](ui-excel-report-layouts.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
