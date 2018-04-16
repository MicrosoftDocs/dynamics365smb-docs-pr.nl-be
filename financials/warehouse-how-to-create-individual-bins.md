---
title: Opslaglocaties maken | Microsoft Docs
description: De meest effectieve manier om opslaglocaties te maken voor uw magazijn, is door groepen van gelijke opslaglocaties te genereren. U doet dit in het opslaglocatiemaakvoorstel, maar u kunt uw opslaglocaties ook stuksgewijs maken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f8cd19f97c530397dd6b499157e13340331aa3ba
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-bins"></a>Opslaglocaties maken
De meest effectieve manier om opslaglocaties te maken voor uw magazijn, is door groepen van gelijke opslaglocaties te genereren. U doet dit in het opslaglocatiemaakvoorstel, maar u kunt uw opslaglocaties ook stuksgewijs maken via de vestigingskaart. U kunt ook een functie in het venster **Voorstel opslaglocatieaanmaak** gebruiken om automatisch opslaglocaties te maken.  

## <a name="to-create-a-bin-from-the-location-card"></a>Een opslaglocatie maken vanaf de vestigingskaart  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vestigingen** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de vestiging waarvan u een opslaglocatie wilt maken en kies de actie **Opslaglocaties**.  
3. Kies de actie **Nieuw**.
4. Vul de velden in. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Individuele opslaglocaties maken op het maakvoorstel voor opslaglocaties  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Voorstel opslaglocatieaanmaak** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vul op elke regel de velden in die nodig zijn om de opslaglocaties een naam te geven en er speciale kenmerken voor in te stellen.  
3.  Kies de actie **Opslaglocaties maken**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Automatisch opslaglocaties maken in het voorstel voor opslaglocatieaanmaak  
Voordat u begint met het automatisch maken van opslaglocaties, moet u bepalen welke soort opslaglocatie essentieel is voor uw bedrijf. Bovendien moet u weten welke artikelenstroom het meest praktisch is voor de fysieke structuur van uw magazijn.  

> [!NOTE]  
>  Zodra een opslaglocatie in gebruik is, kunt u deze alleen nog verwijderen als de opslaglocatie leeg is. Als u de namen van de huidige opslaglocaties echter wilt wijzigen, kunt u de artikelen naar een nieuw opslaglocatiesysteem verplaatsen met behulp van het herindelingsdagboek. Dit is een handmatig proces dat veel tijd in beslag neemt. U kunt de opslaglocaties daarom het beste vanaf het begin af aan correct instellen.  

Voor gebruik van het venster **Voorstel opslaglocatieaanmaak** moet u zijn ingesteld als magazijnmedewerker op de locatie waar de opslaglocaties bestaan. Zie voor meer informatie [Magazijnmedewerkers instellen](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Voorstel opslaglocatieaanmaak** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Opslaglocaties berekenen**.
3. Selecteer in het venster **Opslaglocaties berekenen** in het veld **Opslaglocatiesjabloon** de sjabloon waarop u de overige opslaglocaties wilt baseren.
4.  Voer een omschrijving in voor de opslaglocaties die u wilt maken.  
5.  Als u de opslaglocaties te maken, vult u de velden **Van nr.** en **Tot nr.** in in de drie categorieën die in het venster worden weergegeven: **Rek**, **Sectie** en **Niveau**. De naam van een opslaglocatie kan uit maximaal 20 tekens bestaan.  

    > [!NOTE]  
    >  het aantal tekens dat u in de drie categorieën voor een veld hebt ingevoerd (bijvoorbeeld het aantal tekens dat u hebt ingevoerd in de drie velden **Van nr.**) mag niet groter zijn dan 20 (inclusief eventuele scheidingstekens).  

     Als u letters in de code gebruikt, moet u dezelfde letters gebruiken in de velden **Van nr.** en **Tot nr.** in in. U kunt bijvoorbeeld het gedeelte Rek van de code als volgt instellen: **Van nr. A01** en **Tot nr. A10**. Het programma is niet ingesteld voor het genereren van codes met letterreeksen, zoals van A01 tot F05.  

6.  In het veld **Veldscheidingsteken** kunt u een scheidingsteken invoeren, bijvoorbeeld een liggend streepje. Hiermee kunt u de categorievelden van elkaar scheiden die u hebt opgegeven als onderdeel van de opslaglocatie.  
7.  Als het programma al een regel bevat voor een opslaglocatie en u niet wilt dat er een extra regel wordt gemaakt, selecteert u het veld **Bestaande opslagloc. controleren**.  
8. Wanneer u alle velden hebt ingevuld, klikt u op **OK**.

    Voor elke opslaglocatie in het voorstel wordt nu een regel gemaakt. U kunt nu ook sommige opslaglocaties verwijderen, bijvoorbeeld als er sprake is van een rek met een passage door de eerste twee niveaus van een aantal secties.  

9. Wanneer u alle overbodige opslaglocaties hebt verwijderd, kiest u de actie **Opslaglocaties maken**. Het programma maakt nu een opslaglocatie voor elke regel in het voorstel.  

Herhaal dit proces voor elke volgende set opslaglocaties, totdat u alle opslaglocaties van het magazijn hebt gemaakt.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

