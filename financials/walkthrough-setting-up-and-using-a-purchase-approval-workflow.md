---
title: 'Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken | Microsoft Docs'
description: "U kunt het proces van het goedkeuren van nieuwe of gewijzigde records, zoals documenten, dagboekregels en klantenkaarten automatiseren door werkstromen te maken met stappen voor de goedkeuringen in kwestie. Voordat u goedkeuringswerkstromen maakt, moet u eerst een fiatteur en een vervangende fiatteur instellen voor elke goedkeuringsgebruiker. U kunt ook limietbedragen instellen voor fiatteurs om te definiëren welke verkoop- en inkooporders zij mogen goedkeuren. U kunt goedkeuringsverzoeken en andere berichten als e-mail of interne notitie verzenden. Voor elke instelling van een goedkeuringsgebruiker kunt u ook instellen wanneer zij berichten ontvangen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 58c243000bea5b70666b2a08cdd5696444e22f0f
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken
U kunt het proces van het goedkeuren van nieuwe of gewijzigde records, zoals documenten, dagboekregels en klantenkaarten automatiseren door werkstromen te maken met stappen voor de goedkeuringen in kwestie. Voordat u goedkeuringswerkstromen maakt, moet u eerst een fiatteur en een vervangende fiatteur instellen voor elke goedkeuringsgebruiker. U kunt ook limietbedragen instellen voor fiatteurs om te definiëren welke verkoop- en inkooporders zij mogen goedkeuren. U kunt goedkeuringsverzoeken en andere berichten als e-mail of interne notitie verzenden. Voor elke instelling van een goedkeuringsgebruiker kunt u ook instellen wanneer zij berichten ontvangen.  

 U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure  
In deze procedure worden de volgende taken beschreven:  

-   Goedkeuringsgebruikers instellen (met inbegrip van het instellen van een gebruiker in Windows en in [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Berichten instellen voor goedkeuringsgebruikers.  
-   Een goedkeuringswerkstroom wijzigen en inschakelen.  
-   De taakwachtrij starten waarmee berichten worden verzonden.  
-   Goedkeuring aanvragen voor een inkooporder, als Alicia.  
-   Een bericht ontvangen en vervolgens de aanvraag goedkeuren, als Sean.  

## <a name="prerequisites"></a>Vereisten  
Voor deze procedure hebt u het demobedrijf CRONUS International Ltd. nodig.

## <a name="story"></a>Scenario  
Sean is een supergebruiker bij CRONUS op zijn eigen computer.  

Hij maakt twee goedkeuringsgebruikers. De ene is Alicia, die een inkoopagent vertegenwoordigt. De andere is hijzelf, die de fiatteur van Alicia vertegenwoordigt. Sean kent vervolgens zichzelf onbeperkte rechten voor inkoopgoedkeuring toe en geeft op dat hij berichten ontvangt via interne notities zodra een relevante gebeurtenis plaatsvindt. Tot slot maakt Sean de vereiste goedkeuringswerkstroom als kopie van de bestaande werkstroomsjabloon Goedkeuringswerkstroom inkooporder, laat alle bestaande gebeurtenisvoorwaarden en antwoordopties ongewijzigd en schakelt vervolgens de werkstroom in.  

Om de goedkeuringswerkstroom te testen, meldt Sean zich eerst bij [!INCLUDE[d365fin](includes/d365fin_md.md)] aan als Alicia en vraagt vervolgens om goedkeuring van een inkooporder. Dan meldt Sean zich aan als zichzelf, ziet de notitie in zijn Rolcentrum, volgt de koppeling naar de goedkeuringsaanvraag voor de inkooporder en keurt de aanvraag goed.  

## <a name="setting-up-the-sample-data"></a>Voorbeeldgegevens instellen  
U moet op de lokale computer en in [!INCLUDE[d365fin](includes/d365fin_md.md)] een nieuwe gebruiker maken die Alicia vertegenwoordigt en die u later zult selecteren als goedkeuringsgebruiker. Uw eigen gebruikersaccount vertegenwoordigt Sean.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Alicia als gebruiker toevoegen op de lokale computer  

1.  Kies **Start**, voer in het vak **Programma's en bestanden zoeken** **Lokale gebruikers en groepen bewerken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open de map **Gebruikers**.  
3.  Kies op het tabblad **Acties** de optie **Nieuwe gebruiker**.  
4.  Voer in het veld **Gebruikersnaam** Alicia in.  
5.  Voer in de velden **Wachtwoord** en **Wachtwoord bevestigen** een geldig wachtwoord in.  
6.  Schakel het selectievakje **Gebruiker moet wachtwoord bij volgende aanmelding wijzigen** uit.  
7.  Sluit het venster **Lokale gebruikers en groepen**.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Alicia toevoegen als gebruiker in [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikers** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies in het venster **Windows-gebruikers** op het tabblad **Start** in de groep **Nieuw** de optie **Nieuw**.  
3.  Voer in het venster **Gebruikerskaart** in het veld **Gebruikersnaam** de waarde Alicia in.  
4.  Klik in het veld **Windows-gebruikersnaam** op de knop AssistEdit.  
5.  Voer in het venster **Gebruiker of groep selecteren**, in het veld **Voer de te selecteren objectnaam in**, Alicia in en klik vervolgens op de knop **Namen controleren**.  
6.  Wanneer [COMPUTERNAAM]ALICIA wordt weergegeven in het veld, klikt u op de knop **OK**.  
7.  Selecteer op het sneltabblad **Gebruikersmachtigingensets**, in het veld **Machtigingensets** de optie **SUPER**.  
8.  Selecteer in het veld **Bedrijf** de optie **CRONUS Nederland BV**  
9. Kies de knop **Ok**.  

## <a name="setting-up-approval-users"></a>Goedkeuringsgebruikers instellen  
Stel met de Windows-gebruiker die u zojuist hebt gemaakt Alicia in als goedkeuringsgebruiker met uzelf als fiatteur. Stel uw goedkeuringsrechten in en geef op hoe en wanneer u bericht over goedkeuringsaanvragen wilt ontvangen.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Uzelf en Alicia instellen als goedkeuringsgebruikers  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikersinstellingen voor goedkeuring** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies in het venster **Gebruikersinstellingen goedkeuring** op het tabblad **Start** in de groep **Nieuw** de optie **Nieuw**.  

    > [!NOTE]  
    >  U moet een fiatteur instellen voordat u gebruikers kunt instellen die goedkeuring van de fiatteur vereisen. Daarom moet u uzelf instellen voordat u Alicia instelt.  

3.  Stel de twee goedkeuringsgebruikers op door de velden te vullen te vullen zoals beschreven in de volgende tabel.  

    |Gebruikers-ID|Fiatteur-id|Onbeperkte goedkeuring van inkopen|  
    |-------------|-----------------|---------------------------------|  
    |[COMPUTERNAAM][U]||Geselecteerd|  
    |[COMPUTERNAAM]ALICIA|[COMPUTERNAAM][U]||  

## <a name="setting-up-notifications"></a>Meldingen instellen  
Geef op hoe en wanneer u bericht van goedkeuringsaanvragen wilt ontvangen.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Instellen hoe en wanneer u bericht ontvangt  
1.  Selecteer in het venster **Gebruikersinstellingen voor goedkeuring**, de regel voor uzelf en kies vervolgens op het tabblad **Start**, in de groep **Proces** de optie **Bericht instellen**.  
2.  Voer in het venster **Berichtinstellingen** in het veld **Berichttype** de waarde **Goedkeuring** in.  
3.  Selecteer het veld **Berichtsjablooncode** en klik op de knop **Geavanceerd**.  
4.  Kies in het venster **Berichtsjablonen** op het tabblad **Start** in de groep **Beheren** de optie **Lijst bewerken**.  
5.  Voer op de regel voor de sjabloon GOEDKEURING in het veld **Berichtmethode** de waarde **Notitie** in.  
6.  Kies de knop **OK**.  
7.  Kies in het venster **Berichtinstellingen** op het tabblad **Start** in de groep **Verwerken** de optie **Berichtplanning**.  
8.  Kies in het venster **Berichtplanning** in het veld **Gebeurtenis** de optie **Meteen**.  
9. Kies de knop **OK**.  

## <a name="creating-the-approval-workflow"></a>De goedkeuringswerkstroom maken  
 Maak de werkstroom voor inkoopordergoedkeuring door de stappen van de werkstroomsjabloon Goedkeuringswerkstroom inkooporder te kopiëren. Laat de bestaande werkstroomstappen ongewijzigd en schakel vervolgens de werkstroom in.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Een werkstoorm voor goedkeuring van inkooporders maken en inschakelen  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Werkstromen** in en klik op de gerelateerde koppeling.  
2.  Kies in het venster **Werkstromen** op het tabblad **Acties** in de groep **Algemeen** de optie **Werkstroom maken van sjabloon**.  
3.  Kies op het tabblad **Acties** in de groep **Algemeen** de optie **Werkstroom maken van sjabloon**. Het venster **Werkstroomsjablonen** verschijnt.  
4.  Selecteer de werkstroomsjabloon genaamd Goedkeuringswerkstroom inkooporder en klik vervolgens op de knop **OK**.  

    Het venster **Werkstroom** wordt geopend voor een nieuwe werkstroom die alle gegevens van de geselecteerde sjabloon bevat. Aan de waarde in het veld **Code** wordt "- 01" toegevoegd, om aan te geven dat dit de eerste werkstroom is die is gemaakt vanuit de werkstroomsjabloon Goedkeuringswerkstroom inkooporder.  
5.  Schakel in de koptekst van het venster **Werkstroom** het selectievakje **Ingeschakeld** in.  

## <a name="starting-a-notification-job-queue"></a>Taakwachtrij voor berichten starten  
Zorg dat een taakwachtrij in uw installatie is ingesteld om werkstroomberichten te verwerken.  

### <a name="to-start-the-notify-job-queue"></a>De taakwachtrij MELDEN starten  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Taakwachtrijen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer in het venster **Taakwachtrijen** de regel voor de taakwachtrij MELDEN en kies vervolgens op het tabblad **Start** in de groep **Verwerken** de optie **Taakwachtrij starten**.  

## <a name="using-the-approval-workflow"></a>De goedkeuringswerkstroom gebruiken  
Gebruik de nieuwe werkstroom voor goedkeuring van inkooporders door u eerst aan te melden bij [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia om goedkeuring van een inkooporder aan te vragen. Meld u vervolgens aan als uzelf, bekijk de notitie in het Rolcentrum, volg de koppeling naar de goedkeuringsaanvraag en keur vervolgens de aanvraag goed.  

Als u zich bij [!INCLUDE[d365fin](includes/d365fin_md.md)] wilt aanmelden als een andere gebruiker, gebruikt u de functie **Uitvoeren als andere gebruiker**.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>U aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)] als Alicia  

1.  Druk voor de webclient [!INCLUDE[d365fin](includes/d365fin_md.md)] op de knop voor de browserstart voor de webpagina op Shift + rechtermuisknop en kies vervolgens **Uitvoeren als andere gebruiker**.  

    Druk voor de Windows-client [!INCLUDE[d365fin](includes/d365fin_md.md)] op de startknop voor het programma op Shift + rechtermuisknop en kies vervolgens **Uitvoeren als andere gebruiker**.  

2.  Voer in het venster **Windows-beveiliging** [COMPUTERNAAM]ALICIA in en het vereiste wachtwoord.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Goedkeuring aanvragen voor een inkooporder als Alicia  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkooporders** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de regel voor openstaande inkooporder 104001 en kies vervolgens op het tabblad **Start** in de groep **Beheren** de optie **Bewerken**.  
3.  Kies in het venster **Inkooporder** op het tabblad **Acties** in de groep **Goedkeuring** de optie **Goedkeuringsaanvraag verzenden**.  

    Zoals u ziet is de waarde in het veld **Status** veranderd in **Wacht op goedkeuring**.  

4.  Sluit [!INCLUDE[d365fin](includes/d365fin_md.md)] af.  

### <a name="to-approve-the-purchase-order-as-sean"></a>De inkooporder goedkeuren, als Sean  

1.  Start [!INCLUDE[d365fin](includes/d365fin_md.md)] zoals u dat gewoonlijk doet. Het programma wordt met u als gebruiker geopend.  
2.  Zoek in het Rolcentrum, in het venster **Mijn berichten** naar een nieuwe notitie van Alicia.  

    > [!NOTE]  
    >  Hoewel de berichtherhaling is ingesteld op **Meteen**, arriveert het bericht ongeveer een minuut nadat Alicia de goedkeuringsaanvraag heeft verzonden. Dit komt door de standaard herhalingsfrequentie van de functie Taakwachtrij.  

3.  Als de notitie wordt weergegeven in het venster **Mijn berichten**, kiest u de waarde **Goedkeuringspost: XX, XX** in het veld **Pagina**. Het venster **Aanvragen ter goedkeuring** wordt geopend met de aanvraag van Alicia voor de inkooporder gemarkeerd.  
4.  Kies in het venster **Aanvragen ter goedkeuring** op het tabblad **Start** in de groep **Verwerken** de optie **Goedkeuren**.  

    De waarde in het veld **Status** op de inkooporder van Alicia verandert in **Vrijgegeven**.  

U hebt nu een eenvoudige goedkeuringswerkstroom ingesteld en getest op basis van de eerste twee stappen van de werkstroom Goedkeuringswerkstroom inkooporder. U kunt op eenvoudige wijze deze werkstroom uitbreiden zodat de inkooporder van Alicia automatisch wordt geboekt wanneer Sean deze heeft goedgekeurd. Als u dit wilt doen, moet u de werkstroom Goedkeuringswerkstroom inkooporder inschakelen, waarin het antwoord op een vrijgegeven inkoopfactuur het boeken van deze inkoopfactuur is. Als eerste moet u de gebeurtenisvoorwaarde in de eerste werkstroomstap wijzigen van (inkoop) **Factuur** in **Order**.  

De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal werkstroomsjablonen voor scenario's die worden ondersteund door de toepassingscode. De meeste hiervan zijn voor goedkeuringswerkstromen. Zie Werkstroomsjablonen voor meer informatie.  

U definieert variaties van werkstromen door velden op werkstroomregels in te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).  

Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, moet een Microsoft-partner ze implementeren door de toepassingscode aan te passen. Raadpleeg [Procedure: Nieuwe werkstroomgebeurtenissen en -reacties implementeren](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.  

## <a name="see-also"></a>Zie ook  
[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)   
[Werkstromen maken](across-how-to-create-workflows.md)   
[Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md)   
[Werkstroom](across-workflow.md)

