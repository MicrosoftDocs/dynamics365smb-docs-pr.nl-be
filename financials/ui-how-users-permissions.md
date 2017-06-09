---
title: 'Procedure: Gebruikers en machtigingen beheren | Microsoft Docs'
description: Machtigingensets beheren voor gebruikers nadat u gebruikers in Office 365 hebt gemaakt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d1a973b864a654e2047c5a89271519da04f55c08
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Procedure: Gebruikers en machtigingen beheren
Als u gebruikers wilt toevoegen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet de Office 365-beheerder van uw bedrijf eerst de gebruikers in het Office 365-beheercentrum maken. Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Als gebruikers in Office 365 zijn aangemaakt, kunnen ze worden geïmporteerd in het venster **Gebruikers** door middel van de **Gebruikers ophalen uit Office 365**. Aan gebruikers worden machtigingensets toegewezen op basis van het plan dat aan de gebruiker is toegewezen in Office 365.

U kunt vervolgens machtigingensets aan gebruikers toewijzen om te bepalen tot welke databaseobjecten (en daardoor tot welke UI-elementen) zij toegang hebben en in welke bedrijven.

**Belangrijk:** Als de database meerdere bedrijven bevat, moet ten minste één gebruiker een lid van de gebruikersgroep SUPER zijn in alle bedrijven.

Een machtigingenset is een verzameling machtigingen voor bepaalde objecten in de database. Aan alle gebruikers moeten een of meer machtigingensets worden toegewezen voordat ze toegang hebben tot [!INCLUDE[d365fin](includes/d365fin_md.md)]. Er zijn standaard verschillende vooraf gedefinieerde machtigingensets beschikbaar. U kunt de machtigingensets gebruiken zoals deze zijn gedefinieerd, u kunt de sets aanpassen of u kunt uw eigen machtigingensets maken.

U kunt gebruikers toevoegen aan gebruikersgroepen. Hierdoor wordt het gemakkelijker om dezelfde machtigingensets aan meerdere gebruikers toe te wijzen.

**Opmerking:** Deze functionaliteit vereist dat uw ervaring is ingesteld op Pakket. Zie [Uw ervaring in [!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen](ui-experiences.md) voor meer informatie.

## <a name="to-assign-permissions-to-a-user"></a>Machtigingen toewijzen aan een gebruiker
1. Kies in de rechterbovenhoek het pictogram Zoeken naar pagina of rapport, voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gebruiker waaraan u machtigingen wilt toewijzen.
Alle machtigingensets die al zijn toegewezen aan de gebruiker worden weergegeven in het feitenblok **Machtigingensets**.
3. Kies de actie **Bewerken** om het venster **Gebruikerskaart** te openen.
4. Vul op het sneltabblad **Gebruikersmachtigingensets** waar nodig de velden in op een nieuwe regel. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Gebruikers in gebruikersgroepen samenvoegen
U kunt gebruikersgroepen instellen om u te helpen machtigingensets te beheren voor groepen gebruikers in uw bedrijf. U kunt een functie gebruiken om alle machtigingensets van een bestaande gebruikersgroep naar de nieuwe gebruikersgroep te kopiëren. De leden van de gebruikersgroep worden niet gekopieerd.

1. Kies in de rechterbovenhoek het pictogram Zoeken naar pagina of rapport, voer **Gebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.
2. U kunt ook in het venster **Gebruikers** de actie **Gebruikersgroepen** kiezen.
3. Selecteer in het venster **Gebruikersgroepen** een bestaande gebruikersgroep die u wilt kopiëren en kies de actie **Gebruikersgroep kopiëren**.
4. Geef in het veld **Nieuwe gebruikersgroepcode** de naam van de nieuwe gebruikersgroep en kies de knop **OK**.

    Als alternatief voor het kopiëren kunt u de actie Nieuw gebruiken om een nieuwe regel voor een lege gebruikersgroep te maken, die u vervolgens handmatig invult.
5. Als u nieuwe of extra gebruikers wilt toevoegen, kiest u in het venster **Gebruikersgroep** de actie **Gebruikersgroepsleden**.
6. Vul in het venster **Gebruikersgroepsleden** op een nieuwe regel de velden waar nodig in door bestaande gebruikers te selecteren.
7. Als u nieuwe of extra machtingensets wilt toevoegen, kiest u in het venster **Gebruikersgroep** de actie **Machtigingensets van gebruikersgroep**.
8. Vul in het venster **Machtigingensets van gebruikersgroep** op een nieuwe regel de velden waar nodig in door bestaande machtigingensets te selecteren.

## <a name="to-create-or-modify-permission-sets"></a>Machtigingensets maken of wijzigen
Als de standaard machtigingensets van [!INCLUDE[d365fin](includes/d365fin_md.md)] ontoereikend zijn of niet geschikt zijn voor uw organisatie, kunt u nieuwe machtigingensets maken. En als de afzonderlijke objectmachtigingen die een machtigingenset definiëren niet voldoende zijn, kunt een machtigingenset aanpassen. U kunt een machtigingenset handmatig maken, of u kunt een opnamefunctie gebruiken die uw acties vastlegt terwijl u door scenario navigeert en daarmee de vereiste machtigingenset genereert.

### <a name="to-create-or-modify-permission-sets-manually"></a>Machtigingensets handmatig maken of wijzigen
1. Kies in de rechterbovenhoek het pictogram Zoeken naar pagina of rapport, voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Kies in het venster **Gebruikers** de actie **Machtigingensets**.
3. Kies in het venster **Machtigingensets** de actie **Nieuw**.
4. Vul op een nieuwe regel de velden indien nodig in.
5. Kies de actie **Machtigingen**.
6. Vul in het venster **Machtigingen** waar nodig de velden in de koptekst in.
7. Vul op een nieuwe regel de vijf velden voor de verschillende machtigingstypen in zoals beschreven in de volgende tabel.

    |Optie|Omschrijving|
    |------|-----------|
    |Leeg|Geeft aan dat het machtigingstype niet voor het object is verleend.|
    |**Ja**|Geeft aan dat het machtigingstype is verleend met directe toegang tot het object.|
    |**Indirect**|Geeft aan dat het machtigingstype is verleend met indirecte toegang tot het object.|

    Indirechte machtiging voor een tabel in betekent dat u de tabel niet kunt openen en lezen, maar u kunt de gegevens in de tabel weergeven via een ander object, zoals een pagina, waarvoor u een directe toegangsmachtiging hebt. Zie het onderdeel “Voorbeeld: indirecte machtiging” in dit onderwerp voor meer informatie.

8. Voer in het veld **Beveiligingsfilter** een filter in dat u op de machtiging wilt toepassen, door het veld te selecteren waarvoor u de toegang van een gebruiker wilt beperken.

    Als u bijvoorbeeld een beveiligingsfilter wilt maken zodat een gebruiker alleen verkopen met een bepaalde verkopercode kan weergeven, kiest u het veldnummer voor het veld **Verkoperscode**. Voer vervolgens in het veld **Veldfilter** de waarde in waarmee u de toegang wilt beperken. Als u de toegang van een gebruiker wilt beperken tot de verkopen van Annette Hill, voert u AH in.
9. Herhaal stap 7 en 8 en voeg aan de machtigingenset machtigingen toe voor aanvullende objecten.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Machtigingensets maken of bewerken door uw acties op te nemen
1. Kies in de rechterbovenhoek het pictogram Zoeken naar pagina of rapport, voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Kies in het venster **Gebruikers** de actie **Machtigingensets**.
3. Kies in het venster **Machtigingensets** de actie **Nieuw**.
4. Vul op een nieuwe regel de velden indien nodig in.
5. Kies de actie **Machtigingen**.
6. Kies in het venster **Machtigingen** de actie **Starten**.

    Een opnameproces wordt gestart, dat al uw acties in de gebruikersinterface vastlegt.
7. Ga naar de verschillende vensters en activiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] waartoe u gebruikers met deze machtigingenset toegang wilt verlenen. U moet de taken uitvoeren waarvoor u machtigingen wilt opnemen.
8. Om de opname te stoppen, gaat u terug naar het venster **Machtigingen** en kiest u de actie **Stoppen**.
9. Kies de knop **Ja** om de opgenomen toegangsrechten aan de nieuwe machtigingenset toe te voegen.
10. Geef voor elk object in de opgenomen lijst aan of gebruikers records mogen invoegen, wijzigen of verwijderen in de opgenomen tabellen. Zie stap 7 in het gedeelte "Machtigingensets handmatig maken of wijzigen".

### <a name="example---indirect-permission"></a>Voorbeeld: indirecte machtiging
U kunt een indirecte machtiging toewijzen om een object enkel door middel van een ander object te laten gebruiken.
Een gebruiker kan bijvoorbeeld machtiging hebben om codeunit 80, **Verkoop-boeken**, uit te voeren. De codeunit **Verkoop-boeken** voert veel taken uit, waaronder het wijzigen van tabel 37, **Inkoopregel**. Wanneer de gebruiker een verkoopdocument boekt, de codeunit **Verkoop-boeken**, controleert [!INCLUDE[d365fin](includes/d365fin_md.md)] of de gebruiker de machtiging heeft om de tabel **Inkoopregel** te wijzigen. Als dat niet het geval is, kan de codeunit de taken niet uitvoeren en ontvangt de gebruiker een foutmelding. Indien dit wel zo is, wordt de codeunit uitgevoerd.

De gebruiker hoeft echter geen volledige toegang te hebben tot de tabel **Inkoopregel** om de codeunit uit te voeren. Als de gebruiker indirecte machtiging heeft voor de tabel **Inkoopregel**, kan de codeunit **Verkoop-boeken** worden uitgevoerd. Wanneer een gebruiker een indirecte machtiging heeft, kan die gebruiker enkel de tabel **Inkoopregel** wijzigen door de codeunit **Verkoop-boeken** of een ander object uit te voeren dat machtiging heeft om de tabel **Inkoopregel** te wijzigen. De gebruiker kan alleen de tabel **Inkoopregel** wijzigen vanuit de ondersteunde toepassingsgebieden. De gebruiker kan de functie niet per ongeluk of opzettelijk op andere manieren uitvoeren.

## <a name="see-also"></a>Zie ook
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Welkom bij [!INCLUDE[d365fin](includes/d365fin_md.md)](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

