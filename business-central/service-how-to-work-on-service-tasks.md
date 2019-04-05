---
title: Werken aan servicetaken | Microsoft Docs
description: Wanneer u een serviceorder of -offerte hebt gemaakt, serviceartikelregels hebt geregistreerd en resources aan de serviceartikelen in de order of offerte hebt toegewezen, kunt u beginnen met het herstel en onderhoud van de serviceartikelen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 973bc19e9d6e2efd28c56b0db70e4f53148f636e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816286"
---
# <a name="work-on-service-tasks"></a>Werken aan servicetaken
Wanneer u een serviceorder of -offerte hebt gemaakt, serviceartikelregels hebt geregistreerd en resources aan de serviceartikelen in de order of offerte hebt toegewezen, kunt u beginnen met het herstel en onderhoud van de serviceartikelen.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een pagina **Servicetaken** die u een overzicht biedt van alle serviceartikelen die aandacht vereisen. Beschouw dit venster als uw servicedashboard, waar u kunt zien welke orders in behandeling zijn, waar u reserveonderdelen kunt zoeken en registreren, en waar u de voorraad up-to-date kunt houden.  

Als u wijzigingen wilt bijhouden en een grafische weergave van uw serviceactiviteiten wilt generen, kunt u met de [!INCLUDE[d365fin](includes/d365fin_md.md)]-functies voor statistieken snel en automatisch diagrammen en analyses genereren.  

## <a name="to-work-on-a-service-task"></a>Werken aan servicetaken  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
2. Als u een lijst met servicetaken wilt krijgen waaraan een bepaalde resource of resourcegroep is toegewezen, vult u het veld **Resourcefilter** of **Resourcegroepfilter** in en drukt u op Enter.  
3. Als u een lijst wilt krijgen met servicetaken met een bepaalde responsdatum of responsdatums binnen een bepaalde periode, vult u het veld **Responsdatumfilter** in en drukt u op Enter.  
4. Als u een lijst wilt krijgen met servicetaken met een bepaalde toewijzingsstatus of herstelstatus, vult u het veld **Toewijzingsstatusfilter** of **Herstelstatuscodefilter** in en drukt u op Enter.  
5. Selecteer de servicetaak waaraan u wilt werken. Kies op het tabblad **Navigeren** in de groep **Servicetaken** voor **Artikelwerkbon**. De pagina **Serviceartikelwerkbon** wordt geopend.  
6. Registreer standaardteksten, reserveonderdelen, resource-uren en kosten met de betreffende opties in het veld **Soort**: <Blank>, **Artikel**, **Resource** en **Kosten**.  
7. Selecteer de gewenste status in het veld **Herstelstatus**.  

   > [!NOTE]  
   >  Vul het veld **Herstelstatus** in met de status **Gereedgemeld** of **Deels service verleend** als de service voor het serviceartikel is voltooid of een andere resource verdergaat met de service. De status **Gereedgemeld** of **Hertoewijzing vereist** wordt automatisch opgegeven voor de toewijzingspost voor het serviceartikel.  

## <a name="to-register-service-operations"></a>Servicewerkzaamheden registreren  
Wanneer u een service van een serviceorder uitvoert, kunt u de details registreren over de gebruikte artikelen, de opgelopen kosten en de tijd die is besteed. De gegevens die u opgeeft worden opgeslagen op de pagina **Serviceartikelwerkbon**. U kunt deze gegevens desgewenst bijwerken.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling.  
2. Open de serviceorder waarvoor u de service wilt registreren en kies de artikelregel.  
3. Kies **Acties**, kies **Regel** en kies **Serviceartikelwerkbon**.  
4. Geef op de regels de gebruikte artikelen, de opgelopen kosten en de tijd die is besteed aan de service op.  

   > [!NOTE]  
   >  U kunt services ook rechtstreeks registreren op de serviceregels die zijn gekoppeld aan de serviceorder.  

## <a name="to-register-spare-parts"></a>Reserveonderdelen registreren  
Wanneer u aan serviceartikelen in serviceorders werkt, moet u wellicht reserveonderdelen gebruiken voor de service. Met de volgende procedure wordt aangegeven hoe u de gebruikte reserveonderdelen op de pagina **Serviceartikelwerkbon** kunt registreren.  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de regel met het betreffende serviceartikel en kies de actie **Artikelwerkbon**.  
3. Voer een nieuwe serviceregel in.  
4. Kies in het veld **Soort** de optie **Artikel**.  
5. Selecteer in het veld **Nr.** het relevante reserveonderdeel.  
6. Geef in het veld **Aantal** het aantal artikelen op dat u wilt gebruiken.  

 U kunt een soortgelijke procedure gebruiken om reserveonderdelen te registreren op de pagina **Serviceregels**, die u opent via de pagina **Serviceorder**.  

## <a name="to-register-spare-parts-from-a-service-order"></a>Reserveonderdelen registreren vanuit een serviceorder  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling.  
2. Open de serviceorder waarvoor u reserveonderdelen wilt registreren.  
3. Kies de regel waarin het betreffende serviceartikel is opgenomen. Kies **Acties**, kies **Order** en kies **Serviceregels**.  
4. en voer een nieuwe serviceregel in.  

## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Een serviceartikel of serviceartikelonderdeel vervangen  
Wanneer u service uitvoert voor een serviceartikel dat bestaat uit onderdelen, moet u wellicht een defect onderdeel vervangen door een nieuw onderdeel. Elke keer dat u een reserveonderdeel voor een serviceartikel met componenten invoert, kunt u een component vervangen of een nieuw component maken. Het nieuwe artikel wordt pas als component van het serviceartikel geregistreerd als u deze serviceregel of de serviceorder boekt.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
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

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceorders** of **Serviceoffertes** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de serviceorder of offerte waarvoor u de kaart wilt openen.  
3. Voer op de serviceartikelregel waarvoor u de responstijd wilt wijzigen in het veld **Responstijd (Uren)** of in de velden **Responsdatum** en **Responstijd** de nieuwe responsuren of responsdatum en -tijd in.  

## <a name="to-register-faultresolution-codes"></a>Probleem-/oplossingscodes registreren  
Nadat u een serviceartikel hebt hersteld, kunt u de probleemcode en de oplossingscode voor het artikel registreren. Hiervoor selecteert u een combinatie van de bestaande relaties tussen probleem- en oplossingscodes. De probleem- en oplossingscodes worden weergegeven in de bijbehorende velden op de pagina **Serviceartikelwerkbon**. U kunt de codes ook rechtstreeks op deze pagina registreren.  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de regel met het betreffende serviceartikel en kies de actie **Artikelwerkbon**.  
3. Op de pagina **Serviceartikelwerkbon** kiest u **Rel. probleem-/oplossingscodes**. De pagina **Relaties probleem-/oplossingscodes** wordt geopend.  

  >  [!Note]
  >  De serviceartikelgroep en de probleemcodes worden automatisch uit de pagina **Serviceartikelwerkbon** gekopieerd om filters in te stellen voor de weergegeven relaties op de pagina.  

4. Vul de regel in. Kies de combinatie van probleem- en oplossingscodes, en kies **OK** om deze naar het serviceartikel te kopiëren. Als de juiste combinatie niet wordt gevonden, kunt u een nieuwe combinatie op de pagina instellen.  

## <a name="see-also"></a>Zie ook  
[Probleemrapportage instellen](service-how-setup-fault-reporting.md)
[Toewijzingsstatus en herstelstatus](service-allocation-status-and-repair-status.md)  
[Serviceboekingen](service-service-posting.md)  
