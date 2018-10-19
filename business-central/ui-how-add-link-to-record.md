---
title: Vanuit een record naar externe gegevens of programma's koppelen | Microsoft Docs
description: Koppel een hyperlink aan een document of een website aan een bepaalde record, zoals een klant of document.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c2e70ad534a28cf5062e9e54a2dfbd3af6afaa39
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Koppelingen naar websites, documenten of programma's voor records toevoegen
Voor een bepaalde record, zoals een klant, document of verkooporder, kunt u een koppeling naar een extern document, een website of een programma toevoegen. Of u wilt een koppeling die wordt geopend, e-mailen naar een bepaalde geadresseerde als u het selecteert. De kaartpagina voor sommige records, zoals klanten- en leverancierskaarten, bevatten een veld **Startpagina** waarin u een internetadres (URL) kunt opgeven. Als u andere koppelingen wilt opnemen, kunt u de methode gebruiken die in dit artikel wordt beschreven.

Stel dat u afgedrukte facturen van leveranciers ontvangt. U kunt deze scannen en als PDF-bestanden opslaan op een SharePoint-site. Vervolgens kunt u in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] een koppeling vanuit een inkoopfactuur naar de betreffende factuur in SharePoint maken. Ook kunt u een koppeling maken van een artikelkaart naar de overeenkomstige pagina in de onlinecatalogus van uw leverancier.

## <a name="to-add-a-link-on-a-record"></a>Een koppeling aan een record toevoegen   

1.  Open de record waaraan u de koppeling wilt koppelen, zoals een klantenkaart of een verkooporder. Als u de koppeling aan een bepaalde regel wilt koppelen, bijvoorbeeld aan een regel in een dagboek, selecteert u de regel.  

2.  Kies de actie **Koppelingen** om het venster **Koppelingen** te openen met alle koppelingen die aan die record zijn toegevoegd.

3. Als u een nieuwe koppeling wilt toevoegen, kiest u **+nieuw**.

4.  Voer in het veld **Koppelingsadres** het volgende in

    -   Als u een koppeling met een bestand op uw computer of netwerk wilt toevoegen, voert u het volledige pad en de bestandsnaam in, bijvoorbeeld **C:My Documentsinvoice1.doc**.
    -   Als u een koppeling met een website wilt toevoegen, voert u het internetadres (URL) in, bijvoorbeeld **www.microsoft.com**.
    -   Als u een koppeling met een website wilt toevoegen, voert u het internetadres (URL) in, bijvoorbeeld **www.microsoft.com**.
    -   Als u een koppeling met een programma wilt toevoegen, voert u een bepaalde tekenreeks in om het programma te openen. Als u OneNote op een bepaalde pagina wilt openen, voert u bijvoorbeeld **onenote:///C:My Documentstest.one** in. Als u Outlook wilt openen met een nieuwe lege e-mail naar een bepaalde alias, voert u **mailto:testalias** in.  

5.  Vul het veld **Beschrijving** in met informatie over de koppeling.  

6.  Kies de knop **Opslaan**.  

## <a name="to-delete-a-link-from-a-record"></a>Een koppeling uit een record verwijderen  

Als u een koppeling wilt verwijderen, kunt u in het venster **Koppelingen** eerst **…** en vervolgens **Verwijderen** selecteren.

Als u één record verwijdert, bijvoorbeeld een verkooporderregel, een verkooporder of een klant, worden alle koppelingen verwijderd die aan die record zijn gekoppeld. Als u records echter verwijdert met een batchtaak, zoals de batchtaak **Gefact. verk.-orders verw.**, worden de koppelingen nog wel opgeslagen in de database. U kunt ze uit de database verwijderen door de code-unit **Bestandskoppelingen zonder recordreferentie verwijderen** uit te voeren. Als u dit wilt doen, kiest u het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Koppelingen zonder recordreferentie verwijderen** in en kiest u vervolgens de gerelateerde koppeling.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  In the **Data Deletion** window, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Zie ook  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

