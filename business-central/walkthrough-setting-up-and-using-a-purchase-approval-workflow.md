---
title: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken | Microsoft Docs
description: U kunt het proces van het goedkeuren van nieuwe of gewijzigde records, zoals documenten, dagboekregels en klantenkaarten automatiseren door werkstromen te maken met stappen voor de goedkeuringen in kwestie. Voordat u goedkeuringswerkstromen maakt, moet u eerst een fiatteur en een vervangende fiatteur instellen voor elke goedkeuringsgebruiker. U kunt ook limietbedragen instellen voor fiatteurs om te definiëren welke verkoop- en inkooporders zij mogen goedkeuren. U kunt goedkeuringsverzoeken en andere berichten als e-mail of interne notitie verzenden. Voor elke instelling van een goedkeuringsgebruiker kunt u ook instellen wanneer zij berichten ontvangen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: dfd2a97c6c41ac43bbe4d33792774f929a68d7f6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "913096"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken
U kunt het proces van het goedkeuren van nieuwe of gewijzigde records, zoals documenten, dagboekregels en klantenkaarten automatiseren door werkstromen te maken met stappen voor de goedkeuringen in kwestie. Voordat u goedkeuringswerkstromen maakt, moet u eerst een fiatteur en een vervangende fiatteur instellen voor elke goedkeuringsgebruiker. U kunt ook limietbedragen instellen voor fiatteurs om te definiëren welke verkoop- en inkooporders zij mogen goedkeuren. U kunt goedkeuringsverzoeken en andere berichten als e-mail of interne notitie verzenden. Voor elke instelling van een goedkeuringsgebruiker kunt u ook instellen wanneer zij berichten ontvangen.

> [!NOTE]
> Naast de werkstroomfunctionaliteit in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u met Microsoft Flow integreren om werkstromen te definiëren voor gebeurtenissen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Het zijn twee aparte werkstroomsystemen, maar elke Flow-sjabloon die u maakt met Microsoft Flow, wordt toegevoegd aan de lijst met werkstroomsjablonen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie voor meer informatie [Business Central gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md).   

 U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure  
In deze procedure worden de volgende taken beschreven:  

-   Goedkeuringsgebruikers instellen.  
-   Berichten instellen voor goedkeuringsgebruikers.  
-   Een goedkeuringswerkstroom wijzigen en inschakelen.  
-   Goedkeuring aanvragen voor een inkooporder, als Alicia.  
-   Een bericht ontvangen en vervolgens de aanvraag goedkeuren, als Sean.  

## <a name="prerequisites"></a>Vereisten  
Voor deze procedure hebt u het demobedrijf CRONUS International Ltd. nodig.

## <a name="story"></a>Scenario  
Sean een supergebruiker bij CRONUS. Hij maakt twee goedkeuringsgebruikers. De ene is Alicia, die een inkoopagent vertegenwoordigt. De andere is hijzelf, die de fiatteur van Alicia vertegenwoordigt. Sean kent vervolgens zichzelf onbeperkte rechten voor inkoopgoedkeuring toe en geeft op dat hij berichten ontvangt via interne notities zodra een relevante gebeurtenis plaatsvindt. Tot slot maakt Sean de vereiste goedkeuringswerkstroom als kopie van de bestaande werkstroomsjabloon Goedkeuringswerkstroom inkooporder, laat alle bestaande gebeurtenisvoorwaarden en antwoordopties ongewijzigd en schakelt vervolgens de werkstroom in.  

Om de goedkeuringswerkstroom te testen, meldt Sean zich eerst bij [!INCLUDE[d365fin](includes/d365fin_md.md)] aan als Alicia en vraagt vervolgens om goedkeuring van een inkooporder. Dan meldt Sean zich aan als zichzelf, ziet de notitie in zijn Rolcentrum, volgt de koppeling naar de goedkeuringsaanvraag voor de inkooporder en keurt de aanvraag goed.  

## <a name="setting-up-sample-data"></a>Voorbeeldgegevens instellen
Voordat u goedkeuringsgebruikers en hun berichtmethode kunt instellen, moet u ervoor zorgen dat er twee gebruikers zijn in [!INCLUDE[d365fin](includes/d365fin_md.md)]: één gebruiker kan Alicia vertegenwoordigen. De andere gebruiker, uzelf, vertegenwoordigt Sean. Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.

### <a name="setting-up-approval-users"></a>Goedkeuringsgebruikers instellen  
Wanneer u bent aangemeld als uzelf, stelt u Alicia in als een goedkeuringsgebruiker van wie u zelf de goedkeurder bent. Stel uw goedkeuringsrechten in en geef op hoe en wanneer u bericht over goedkeuringsaanvragen wilt ontvangen.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Uzelf en Alicia instellen als goedkeuringsgebruikers  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies op de pagina **Gebruikersinstellingen voor goedkeuring** die wordt geopend, de actie **Nieuw**.  

    > [!NOTE]  
    >  U moet een fiatteur instellen voordat u gebruikers kunt instellen die goedkeuring van de fiatteur vereisen. Daarom moet u uzelf instellen voordat u Alicia instelt.  

3.  Stel de twee goedkeuringsgebruikers op door de velden te vullen te vullen zoals beschreven in de volgende tabel.  

    |Gebruikers-ID|Fiatteur-id|Onbeperkte goedkeuring van inkopen|  
    |-------------|-----------------|---------------------------------|  
    |U||Geselecteerd|  
    |ALICIA|U||  

### <a name="setting-up-notifications"></a>Meldingen instellen  
In deze procedure wordt de gebruiker door een interne notitie geïnformeerd over goed te keuren aanvragen. Een goedkeuringsbericht kan ook via e-mail worden verzonden. Zie voor meer informatie [Vastleggen wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md). 

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Instellen hoe en wanneer u bericht ontvangt  
1.  Selecteer op de pagina **Gebruikersinstellingen voor goedkeuring** de regel voor uzelf en kies vervolgens de actie **Berichtinstellingen**.  
2.  Kies op de pagina **Berichtinstellingen** in het veld **Berichttype** de waarde **Goedkeuring**.  
3.  Kies in het veld **Berichtmethode** de optie **Opmerking**.  
6.  Kies op de pagina **Berichtinstellingen** de actie **Berichtplanning**.  
7.  Selecteer op de pagina **Berichtplanning** in het veld **Gebeurtenis** de optie **Meteen**.  
8. Kies de knop **OK**.  

## <a name="creating-the-approval-workflow"></a>De goedkeuringswerkstroom maken  
 Maak de werkstroom voor inkoopordergoedkeuring door de stappen van de werkstroomsjabloon Goedkeuringswerkstroom inkooporder te kopiëren. Laat de bestaande werkstroomstappen ongewijzigd en schakel vervolgens de werkstroom in.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Een werkstoorm voor goedkeuring van inkooporders maken en inschakelen  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies op de pagina **Werkstromen** de actie **Werkstroom maken van sjabloon**.  
3.  Selecteer op de pagina **Werkstroomsjablonen** de werkstroomsjabloon genaamd Goedkeuringswerkstroom inkooporder en kies vervolgens de knop **OK**.  

    De pagina **Werkstroom** wordt geopend voor een nieuwe werkstroom die alle gegevens van de geselecteerde sjabloon bevat. Aan de waarde in het veld **Code** wordt "- 01" toegevoegd, om aan te geven dat dit de eerste werkstroom is die is gemaakt vanuit de werkstroomsjabloon Goedkeuringswerkstroom inkooporder.  
5.  Schakel in de koptekst van de pagina **Werkstroom** het selectievakje **Ingeschakeld** in.  

## <a name="using-the-approval-workflow"></a>De goedkeuringswerkstroom gebruiken  
Gebruik de nieuwe werkstroom voor goedkeuring van inkooporders door u eerst aan te melden bij [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia om goedkeuring van een inkooporder aan te vragen. Meld u vervolgens aan als uzelf, bekijk de notitie in het Rolcentrum, volg de koppeling naar de goedkeuringsaanvraag en keur vervolgens de aanvraag goed.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Goedkeuring aanvragen voor een inkooporder als Alicia  
1. Meld u aan als Alicia.
2.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling.  
3.  Selecteer de regel voor open inkooporder 104001 en kies de actie **Bewerken**.  
4.  Kies op de pagina **Inkooporder** de actie **Goedkeuringsaanvraag verzenden**.  

Zoals u ziet is de waarde in het veld **Status** veranderd in **Wacht op goedkeuring**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>De inkooporder goedkeuren, als Sean  
1. Meld u aan als Sean.
2.  Zoek in het Rolcentrum, op de pagina **Mijn berichten** naar een nieuwe notitie van Alicia.  
3.  Als de notitie wordt weergegeven, kiest u op de pagina **Mijn berichten** de waarde **Goedkeuringspost: XX, XX** in het veld **Pagina**. De pagina **Aanvragen ter goedkeuring** wordt geopend met de aanvraag van Alicia voor de inkooporder gemarkeerd.  
4.  Kies op de pagina **Aanvragen ter goedkeuring** de actie **Goedkeuren**.  

    De waarde in het veld **Status** op de inkooporder van Alicia verandert in **Vrijgegeven**.  

U hebt nu een eenvoudige goedkeuringswerkstroom ingesteld en getest op basis van de eerste twee stappen van de werkstroom Goedkeuringswerkstroom inkooporder. U kunt op eenvoudige wijze deze werkstroom uitbreiden zodat de inkooporder van Alicia automatisch wordt geboekt wanneer Sean deze heeft goedgekeurd. Als u dit wilt doen, moet u de werkstroom Goedkeuringswerkstroom inkooporder inschakelen, waarin het antwoord op een vrijgegeven inkoopfactuur het boeken van deze inkoopfactuur is. Als eerste moet u de gebeurtenisvoorwaarde in de eerste werkstroomstap wijzigen van (inkoop) **Factuur** in **Order**.  

De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal werkstroomsjablonen voor scenario's die worden ondersteund door de toepassingscode. De meeste hiervan zijn voor goedkeuringswerkstromen.  

U definieert variaties van werkstromen door velden op werkstroomregels in te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).  

Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, moet een Microsoft-partner ze implementeren door de toepassingscode aan te passen. Raadpleeg [Procedure: Nieuwe werkstroomgebeurtenissen en -reacties implementeren](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.  

## <a name="see-also"></a>Zie ook  
[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)   
[Werkstromen maken](across-how-to-create-workflows.md)   
[Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md)   
[Werkstroom](across-workflow.md)  
[Business Central gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md)
