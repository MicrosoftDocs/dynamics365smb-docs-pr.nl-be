---
title: Overzicht van instellingen voor serviceartikelen en serviceartikelonderdelen | Microsoft Docs
description: Leer wat u moet instellen voordat u serviceartikelen, inclusief standaardwaarden voor onder andere de responstijd, het contractkortingspercentage en de serviceprijsgroep, kunt gebruiken.
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
ms.openlocfilehash: 068d141ee8490cc34e8b2092b7dcfda36139660d
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-service-items-and-service-item-components"></a>Serviceartikelen en serviceartikelonderdelen instellen
Als u met serviceartikelen wilt werken, moet u het volgende instellen

* Serviceartikelgroepen. 
* Optioneel

## <a name="to-set-up-service-item-groups"></a>Serviceartikelgroepen instellen
U kunt groepen van artikelen instellen die aan elkaar gerelateerd zijn met betrekking tot herstel en onderhoud. U kunt standaardwaarden voor serviceartikelen in een serviceartikelgroep opgeven, zoals responstijd, contractkortingspercentage en serviceprijsgroep. Voor artikelen in een serviceartikelgroep kunt u aangeven of deze automatisch als serviceartikelen moeten worden geregistreerd wanneer ze worden verkocht.  
  
U wijst serviceartikelgroepen toe aan artikelen op de kaart **Artikel** en aan serviceartikelen op de kaart **Serviceartikel**.  
  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceartikelgroepen** in en klik vervolgens op de gerelateerde koppeling.  
2. Maak een nieuwe serviceartikelgroep.  
3. Vul de velden **Code** en **Omschrijving** in.  
4. Geef in het veld **Std. contractkorting %** het standaardpercentage voor de contractkorting op dat u wilt toewijzen aan de serviceartikelen in de groep.  
5. Geef in het veld **Std. serviceprijsgroepcode** de code voor de standaardserviceprijsgroep op die u wilt toewijzen aan de serviceartikelen in de groep.  
6. Voer in het veld **Std. responstijd (Uren)** de standaardresponstijd in uren in die u wilt toewijzen aan de serviceartikelen in de groep.  
7. Als u de artikelen in de groep bij verkoop als serviceartikelen wilt registreren, moet u het veld **Serviceartikel maken** selecteren.  

## <a name="to-set-up-service-item-components"></a>Serviceartikelcomponenten instellen
Een serviceartikel kan bestaan uit meerdere onderdelen die u door reserveonderdelen kunt vervangen wanneer voor het artikel service wordt uitgevoerd. Deze onderdelen zijn ingesteld op de pagina **Serviceartikelonderdeeloverzicht**. Als u onderdelen wilt instellen voor serviceartikelen die zijn ingesteld als stuklijst, kunt u de stuklijstartikelen kopiëren en instellen als serviceartikelcomponenten. 
  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceartikelen** in en klik vervolgens op de gerelateerde koppeling. 
2. Open het serviceartikel waarvoor u componenten wilt instellen.  
3. Kies de actie **Materialen**. Het venster **Serviceartikelonderdeeloverzicht** wordt geopend.  
4. Een nieuw component toevoegen.  
5. Kies in het veld **Soort** de optie **Serviceartikel** als de component zelf een geregistreerd serviceartikel is. Selecteer anders **Artikel**.  
6. Selecteer in het veld **Nr.** het artikel of serviceartikel dat een component is van het serviceartikel.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Serviceartikelcomponenten instellen uit stuklijsten
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceartikelen** in en klik vervolgens op de gerelateerde koppeling.  
2. Open het serviceartikel waarvoor u componenten wilt instellen vanuit een stuklijst.  
3. Kies de actie **Materialen**. Het venster **Serviceartikelonderdeeloverzicht** wordt geopend.  
4. Kies de actie **Van stuklijst kopiëren**.  
  
    Wanneer het artikel waaraan het serviceartikel is gekoppeld, een stuklijst is, worden automatisch componenten gemaakt voor alle artikelen in de stuklijst.  

## <a name="to-set-up-a-service-shelf"></a>Serviceschappen instellen
U kunt serviceschappen instellen om de opslaglocatie van uw serviceartikelen aan te duiden. U wijst serviceschappen toe aan serviceartikelen op de pagina's **Serviceorder** en **Serviceartikelwerkbon**.  
  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceschappen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de benodigde velden in.

## <a name="see-also"></a>Zie ook
[Codes voor standaardservices instellen](service-how-setup-service-coding.md)   
[Troubleshooting instellen](service-how-setup-troubleshooting.md)
