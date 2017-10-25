---
title: Werken aan servicetaken | Microsoft Docs
description: Wanneer u een serviceorder of -offerte hebt gemaakt, serviceartikelregels hebt geregistreerd en resources aan de serviceartikelen in de order of offerte hebt toegewezen, kunt u beginnen met het herstel en onderhoud van de serviceartikelen.
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 32cbc23b24a8a04a62a246dd50eac8d8a721e2e7
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-on-service-tasks"></a>Procedure: Werken aan servicetaken
Wanneer u een serviceorder of -offerte hebt gemaakt, serviceartikelregels hebt geregistreerd en resources aan de serviceartikelen in de order of offerte hebt toegewezen, kunt u beginnen met het herstel en onderhoud van de serviceartikelen.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een venster **Servicetaken** dat u een overzicht biedt van alle serviceartikelen die aandacht vereisen. Beschouw dit venster als uw servicedashboard, waar u kunt zien welke orders in behandeling zijn, waar u reserveonderdelen kunt zoeken en registreren, en waar u de voorraad up-to-date kunt houden.  
  
Als u wijzigingen wilt bijhouden en een grafische weergave van uw serviceactiviteiten wilt generen, kunt u met de [!INCLUDE[d365fin](includes/d365fin_md.md)]-functies voor statistieken snel en automatisch diagrammen en analyses genereren.  
  
## <a name="to-work-on-a-service-task"></a>Werken aan servicetaken  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling. 
2. Als u een lijst met servicetaken wilt krijgen waaraan een bepaalde resource of resourcegroep is toegewezen, vult u het veld **Resourcefilter** of **Resourcegroepfilter** in en drukt u op Enter.  
3. Als u een lijst wilt krijgen met servicetaken met een bepaalde responsdatum of responsdatums binnen een bepaalde periode, vult u het veld **Responsdatumfilter** in en drukt u op Enter.  
4. Als u een lijst wilt krijgen met servicetaken met een bepaalde toewijzingsstatus of herstelstatus, vult u het veld **Toewijzingsstatusfilter** of **Herstelstatuscodefilter** in en drukt u op Enter.  
5. Selecteer de servicetaak waaraan u wilt werken. Kies op het tabblad **Navigeren** in de groep **Servicetaken** voor **Artikelwerkbon**. Het venster **Serviceartikelwerkbon** wordt geopend.  
6. Registreer standaardteksten, reserveonderdelen, resource-uren en kosten met de betreffende opties in het veld **Soort**: <Blank>, **Artikel**, **Resource** en **Kosten**.  
7. Selecteer de gewenste status in het veld **Herstelstatus**.  
  
   > [!NOTE]  
   >  Vul het veld **Herstelstatus** in met de status **Gereedgemeld** of **Deels service verleend** als de service voor het serviceartikel is voltooid of een andere resource verdergaat met de service. De status **Gereedgemeld** of **Hertoewijzing vereist** wordt automatisch opgegeven voor de toewijzingspost voor het serviceartikel.  

## <a name="to-register-service-operations"></a>Servicewerkzaamheden registreren  
Wanneer u een service van een serviceorder uitvoert, kunt u de details registreren over de gebruikte artikelen, de opgelopen kosten en de tijd die is besteed. De gegevens die u opgeeft worden opgeslagen in het venster **Serviceartikelwerkbon**. U kunt deze gegevens desgewenst bijwerken. 
   
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorders** in en klik op de gerelateerde koppeling.  
2. Open de serviceorder waarvoor u de service wilt registreren en kies de artikelregel.  
3. Kies **Acties**, kies **Regel** en kies **Serviceartikelwerkbon**.  
4. Geef op de regels de gebruikte artikelen, de opgelopen kosten en de tijd die is besteed aan de service op.  
  
   > [!NOTE]  
   >  U kunt services ook rechtstreeks registreren op de serviceregels die zijn gekoppeld aan de serviceorder.  
  
## <a name="to-register-spare-parts"></a>Reserveonderdelen registreren  
Wanneer u aan serviceartikelen in serviceorders werkt, moet u wellicht reserveonderdelen gebruiken voor de service. Met de volgende procedure wordt aangegeven hoe u de gebruikte reserveonderdelen in het venster **Serviceartikelwerkbon** kunt registreren.  
  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling. 
2. Kies de regel met het betreffende serviceartikel en kies de actie **Artikelwerkbon**.  
3. Voer een nieuwe serviceregel in.  
4. Kies in het veld **Soort** de optie **Artikel**.  
5. Selecteer in het veld **Nr.** het relevante reserveonderdeel.  
6. Geef in het veld **Aantal** het aantal artikelen op dat u wilt gebruiken.  
  
 U kunt een soortgelijke procedure gebruiken om reserveonderdelen te registreren op de pagina **Serviceregels**, die u opent via de pagina **Serviceorder**.  
  
## <a name="to-register-spare-parts-from-a-service-order"></a>Reserveonderdelen registreren vanuit een serviceorder  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorders** in en klik op de gerelateerde koppeling.  
2. Open de serviceorder waarvoor u reserveonderdelen wilt registreren.  
3. Kies de regel waarin het betreffende serviceartikel is opgenomen. Kies **Acties**, kies **Order** en kies **Serviceregels**.  
4. en voer een nieuwe serviceregel in.  
  
## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Een serviceartikel of serviceartikelonderdeel vervangen  
Wanneer u service uitvoert voor een serviceartikel dat bestaat uit onderdelen, moet u wellicht een defect onderdeel vervangen door een nieuw onderdeel. Elke keer dat u een reserveonderdeel voor een serviceartikel met componenten invoert, kunt u een component vervangen of een nieuw component maken. Het nieuwe artikel wordt pas als component van het serviceartikel geregistreerd als u deze serviceregel of de serviceorder boekt. 
    
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling. 
2. Kies de regel met het serviceartikel en kies de actie **Artikelwerkbon**.  
3. Voer een nieuwe serviceregel in.  
4. Kies in het veld **Soort** de optie **Artikel**.  
5. Selecteer in het veld **Nr.** het te vervangen onderdeel.  
6. Druk op **Enter**. Er verschijnt een dialoogvenster met drie opties: **Component vervangen**, **Nieuw Component** en **Negeren**. De volgende tabel beschrijft de opties.  
  
    |Optie | Description|  
    |----------------------------------|---------------------------------------|  
    |**Component vervangen**|De status van het component dat u wilt vervangen, wordt gewijzigd in niet-actief. Het artikel wordt weergegeven in het overzicht van vervangen componenten voor het serviceartikel.|  
    |**Nieuw onderdeel**|Het nieuwe component wordt in het overzicht van componenten voor het serviceartikel opgenomen.|  
    |**Negeren**|Er wordt niets gewijzigd in het overzicht van componenten voor het serviceartikel.|  
  
7. Kies **Onderdeel vervangen**.  
8. Kies het te vervangen onderdeel en kies **OK**.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>Responstijd wijzigen voor een serviceartikelregel  
Wanneer u een serviceartikelregel registreert in een serviceorder of -offerte, wordt automatisch een responstijd in uren ingevoerd en worden de responsdatum en -tijd op basis hiervan berekend, afhankelijk van of het serviceartikel in een servicecontract is opgenomen. U kunt de responstijd in uren en de responsdatum en -tijd desgewenst wijzigen.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorders** of **Serviceoffertes** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de serviceorder of offerte waarvoor u de kaart wilt openen.  
3. Voer op de serviceartikelregel waarvoor u de responstijd wilt wijzigen in het veld **Responstijd (Uren)** of in de velden **Responsdatum** en **Responstijd** de nieuwe responsuren of responsdatum en -tijd in.  

## <a name="to-register-faultresolution-codes"></a>Probleem-/oplossingscodes registreren  
Nadat u een serviceartikel hebt hersteld, kunt u de probleemcode en de oplossingscode voor het artikel registreren. Hiervoor selecteert u een combinatie van de bestaande relaties tussen probleem- en oplossingscodes. De probleem- en oplossingscodes worden weergegeven in de bijbehorende velden in het venster **Serviceartikelwerkbon**. U kunt de codes ook rechtstreeks in dit venster registreren.  
    
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling. 
2. Kies de regel met het betreffende serviceartikel en kies de actie **Artikelwerkbon**.  
3. Op de pagina **Serviceartikelwerkbon** kiest u **Rel. probleem-/oplossingscodes**. Het venster **Relaties probleem-/oplossingscodes** wordt geopend.  
  
  >  [!Note]
  >  De serviceartikelgroep en de probleemcodes worden automatisch uit het venster **Serviceartikelwerkbon** gekopieerd om filters in te stellen voor de weergegeven relaties in het venster.  
  
4. Vul de regel in. Kies de combinatie van probleem- en oplossingscodes, en kies **OK** om deze naar het serviceartikel te kopiëren. Als de juiste combinatie niet wordt gevonden, kunt u een nieuwe combinatie in het venster instellen.  

## <a name="see-also"></a>Zie ook  
[Procedure: Probleemrapportage instellen](service-how-setup-fault-reporting.md)
[Toewijzingsstatus en herstelstatus](service-allocation-status-and-repair-status.md)  
[Serviceboekingen](service-service-posting.md)  


