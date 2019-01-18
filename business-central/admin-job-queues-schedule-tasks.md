---
title: Taken plannen voor automatische uitvoering | Microsoft Docs
description: "Geplande taken worden beheerd door de taakwachtrij. Met deze taken worden rapporten en codeunits uitgevoerd. U kunt taken éénmalig of herhaaldelijk uitvoeren."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ad0f99509ff1a191c62dd1c3a6d569c9884ea851
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Gebruik van taakwachtrijen om taken te plannen
Met taakwachtrijen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen gebruikers specifieke rapporten en codeunits plannen en uitvoeren. U kunt taken éénmalig of herhaaldelijk uitvoeren. U kunt bijvoorbeeld het statistiekrapport **Verkoper - Statistiek** wekelijks uitvoeren om de verkopen per verkoper wekelijks bij te houden of u kunt de codeunit **E-mailwachtrij service verwerken** dagelijks uitvoeren om ervoor te zorgen dat niet-verzonden e-mailberichten aan klanten met betrekking tot hun serviceorders tijdig worden verzonden.  

## <a name="add-jobs-to-the-job-queue"></a>Taken toevoegen aan de taakwachtrij
Op de pagina **Taakwachtrijposten** worden alle bestaande posten weergegeven. Als u een nieuwe taakwachtrijpost toevoegt die u wilt plannen, moet u informatie opgeven over het objecttype dat u wilt uitvoeren, zoals een rapport of codeunit, en de naam en id van het object opgeven dat u wilt uitvoeren. U kunt ook parameters toevoegen om het gedrag van de taakwachtrijpost te specificeren. Zo kunt u een parameter toevoegen om alleen geboekte verkooporders te verzenden. U moet zijn gemachtigd om het betreffende rapport of de betreffende code-unit uit te voeren, want anders wordt een fout geretourneerd wanneer de verwerkingswachtrij wordt uitgevoerd.  

Stel desgewenst in het veld **Categoriefilter taakwachtrij** een filter in. U kunt taakwachtrijcategorieën gebruiken om taken in de lijst te groeperen.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden de taken automatisch uitgevoerd op basis van de opgegeven schema's voor elke taakwachtrijpost. U kunt een taakwachtrijpost ook starten, stoppen en handmatig in de wacht zetten.

### <a name="log-files"></a>Logbestanden
Fouten worden weergegeven op de pagina **Logposten taakwachtrij**, dat u kunt openen via het lint. U kunt ook problemen met verwerkingswachtrijen oplossen. Gegevens die worden gegenereerd wanneer een verwerkingswachtrij wordt uitgevoerd, worden opgeslagen in de database.  

### <a name="background-posting-with-job-queues"></a>Boeken op achtergrond met taakwachtrijen
Taakwachtrijen zijn een effectief hulpmiddel voor het plannen van de uitvoering van zakelijke processen op de achtergrond. Zo kan het voorkomen dat meerdere gebruikers tegelijkertijd proberen verkooporders te boeken, maar dat er slechts één order per keer kan worden verwerkt. Door het instellen van een routine voor het boeken op de achtergrond , kunt u de boekingen in een wachtrij voor verwerking op de achtergrond plaatsen.  

 U wilt mogelijk ook boekingen plannen voor tijden die geschikt zijn voor uw organisatie. Het kan bijvoorbeeld zinvol zijn in uw bedrijf bepaalde routines uit te voeren wanneer de meeste van de gegevensinvoer voor de dag is afgesloten. U kunt dat bereiken door de taakwachtrij in te stellen om diverse batchverwerkingsrapporten uit te voeren, zoals **Batchboeken verkooporders**, **Batchboeken verkoopfacturen** en **Batchboeken verk.-creditnota**.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt boeken op de achtergrond voor de volgende documentsoorten:  

-   Verkoop: verkooporder, retourorder, creditnota, factuur  

-   Inkoop: inkooporder, retourorder, creditnota, factuur  

 Als de taakwachtrij de verkooporder niet kan boeken, wordt de status gewijzigd in **Fout** en wordt de verkooporder toegevoegd aan de lijst met verkooporders die de gebruiker moet afhandelen.  

> [!NOTE]  
>  Wanneer u een document voor het boeken plant en het boekingsproces begint, is er automatisch binnen twee uur een time-out in de boekingsroutine geconfigureerd als het boekingsproces niet meer reageert.  

U stelt dit gebruik van de taakwachtrij op de pagina **Instellingen van verkoop en tegoeden** of **Inkopen en Leveranciers** in. Op het sneltabblad **Boeken in achtergrond** schakelt u het selectievakje **Documenten boeken via taakwachtrij** in en vult u de relevante gegevens in. Hier kunt u ook het veld **Taakwachtrijcategoriecode** gebruiken om alle taakwachtrijposten met die code uit te voeren. U kunt bijvoorbeeld een categorie **Vrkboeking** gebruiken om te filteren op alle verkooporders die overeenkomen met een taakwachtrij die dezelfde categoriecode heeft.  

> [!IMPORTANT]  
>  Wanneer u een taak voor het boeken en afdrukken van documenten instelt en er op de printer een dialoogvenster wordt weergegeven, zoals een verzoek om aanmeldingsgegevens of een waarschuwing over een laag printerinktniveau, dan wordt het document geboekt, maar niet afgedrukt. De overeenkomstige invoer van de taakwachtrij krijgt uiteindelijk een time-out en het veld **Status** wordt ingesteld op **Fout**. Dienovereenkomstig is het raadzaam dat u geen printerinstellingen gebruikt waarvoor interactie met de weergave van printerdialoogvensters nodig is in combinatie met boeken op de achtergrond.  

## <a name="use-the-my-job-queue-part"></a>Het onderdeel Mijn taakwachtrij gebruiken
In het onderdeel **Mijn taakwachtrij** deel worden de taakwachtrijen weergegeven die een gebruiker heeft gestart, maar die nog niet zijn voltooid. Standaard is het onderdeel niet zichtbaar, zodat u het moet toevoegen aan uw rolcentrum. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).  

In dit onderdeel ziet u de documenten die worden verwerkt of die in de wachtrij zijn gezet en waarvoor uw id is opgegeven in het veld **Toegewezen gebruikers-id**. Het onderdeel helpt u bij het bijhouden van alle taakwachtrijposten, inclusief de posten die betrekking hebben op boeken op de achtergrond. Het onderdeel kan u in één oogopslag laten zien of er een fout is opgetreden bij het boeken van een document en of er fouten zijn opgetreden in een taakwachtrijpost. Met het onderdeel kunt u een documentboeking annuleren als deze niet wordt uitgevoerd.  

## <a name="security"></a>Beveiliging  
Taakwachtrijposten worden uitgevoerd op basis van machtigingen. Die machtigingen moeten de uitvoering van de lijst of codeunit toestaan.  

Wanneer een taakwachtrij handmatig is geactiveerd, wordt deze uitgevoerd met de referenties van de gebruiker. Wanneer een taakwachtrij is geactiveerd als een geplande taak, wordt deze uitgevoerd met de referenties van de serverinstantie. Wanneer een taak wordt uitgevoerd, wordt deze uitgevoerd met de referenties van de taakwachtrij die deze activeert. De gebruiker die de taakwachtrijpost maakte, moet echter ook machtigingen hebben. Wanneer een taak wordt uitgevoerd in de gebruikerssessie (bijvoorbeeld bij het boeken op de achtergrond), wordt deze uitgevoerd met de referenties van de gebruiker die deze taak heeft gemaakt.  

> [!IMPORTANT]  
>  Als u de machtigingenset SUPER gebruikt die wordt geleverd met [!INCLUDE[d365fin](includes/d365fin_md.md)], hebben u en uw gebruikers de machtiging om alle objecten uit te voeren. In dit geval wordt de toegang voor elke gebruiker alleen beperkt door machtigingen voor gegevens.  

## <a name="using-job-queues-effectively"></a>Taakwachtrijen efficiënt gebruiken  
De record van de taakwachtrijpost heeft veel velden om de parameters in een codeunit te plaatsen die u hebt opgegeven voor het uitvoeren met een taakwachtrij. Dit betekent ook dat codeunits die moeten worden uitgevoerd via de taakwachtrij, moeten worden gespecificeerd met de taakwachtrijrecord als een parameter in de **OnRun** trigger. Dit biedt een extra beveiligingsniveau aangezien het voorkomt dat gebruikers willekeurige codeunits uitvoeren via de taakwachtrij. Als de gebruiker parameters aan een rapport moet doorgeven, kan dit enkel door de lijstuitvoering in een codeunit te plaatsen die vervolgens de invoerparameters parseert en deze in de lijst plaatst voordat deze wordt uitgevoerd.  

## <a name="see-also"></a>Zie ook  
[Beheer](admin-setup-and-administration.md)  
[Business Central instellen](setup.md)  

