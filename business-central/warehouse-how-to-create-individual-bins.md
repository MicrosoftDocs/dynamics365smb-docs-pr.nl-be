---
title: Opslaglocaties maken
description: 'Genereer groepen van vergelijkbare opslaglocaties in het werkblad voor het maken van opslaglocaties, maak afzonderlijke opslaglocaties op de locatiekaart of automatisch op het Voorstel opslaglocatieaanmaak.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="create-bins" />Opslaglocaties maken

De meest effectieve manier om opslaglocaties te maken voor uw magazijn, is door groepen van gelijke opslaglocaties te genereren. U doet dit in het opslaglocatiemaakvoorstel, maar u kunt uw opslaglocaties ook stuksgewijs maken via de vestigingskaart. U kunt ook een functie op de pagina **Voorstel opslaglocatieaanmaak** gebruiken om automatisch opslaglocaties te maken.  

## <a name="to-create-a-bin-from-the-location-card" />Een opslaglocatie maken vanaf de vestigingskaart

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de vestiging waarvan u een opslaglocatie wilt maken en kies de actie **Opslaglocaties**.  
3. Kies de actie **Nieuw**.
4. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field" />Het veld Speciaal

Het veld **Speciaal** op de pagina **Opslaglocaties** geeft op dat aantallen op de opslaglocatie worden beschermd tegen picken voor andere vraag. Hoeveelheden op speciale opslaglocaties kunnen echter nog steeds worden gereserveerd. De hoeveelheden in specifieke opslaglocaties kunnen dus worden opgenomen in het veld **Totaal beschikbaar aantal** op de pagina **Reservering**.

Een opslaglocatie speciaal maken biedt vergelijkbare functionaliteit als typen opslaglocaties in standaardmagazijnbeheer, die alleen beschikbaar is in geavanceerd magazijnbeheer. Zie [Typen opslaglocaties instellen](warehouse-how-to-set-up-bin-types.md) voor meer informatie.

### <a name="example" />Voorbeeld

Een afdeling wordt ingesteld met een opslaglocatiecode in het veld **Code verbruikslocatie**. Productieordermateriaalregels met deze opslaglocatie eisen dat voorwaarts afgeboekte materialen daar worden geplaatst. Echter, totdat de materialen uit de opslaglocatie worden verbruikt, kunnen andere eisen materialen uit die opslaglocatie picken of verbruiken omdat ze nog steeds worden beschouwd als beschikbare opslaglocatie-inhoud. Om ervoor te zorgen dat de opslaglocatie-inhoud alleen beschikbaar is voor materiaalvragen die deze opslaglocatie voor productie gebruiken, moet u het veld **Speciaal** kiezen op de regel voor die opslaglocatie.

> [!Caution]
> Artikelen in specifieke opslaglocaties worden niet beveiligd wanneer deze worden gepickt en verbruikt als productie- of assemblycomponenten met de pagina **Voorraadpick**. Zie voor meer informatie [Picken voor productie of assemblage in standaardmagazijnconfiguraties](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet" />Individuele opslaglocaties maken op het maakvoorstel voor opslaglocaties

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorstel opslaglocatieaanmaak** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul op elke regel de velden in die nodig zijn om de opslaglocaties een naam te geven en er speciale kenmerken voor in te stellen.  
3.  Kies de actie **Opslaglocaties maken**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet" />Automatisch opslaglocaties maken in het voorstel voor opslaglocatieaanmaak

Voordat u begint met het automatisch maken van opslaglocaties, moet u bepalen welke soort opslaglocatie essentieel is voor uw bedrijf. Bovendien moet u weten welke artikelenstroom het meest praktisch is voor de fysieke structuur van uw magazijn.  

> [!NOTE]  
> Zodra een opslaglocatie in gebruik is, kunt u deze alleen nog verwijderen als de opslaglocatie leeg is. Als u de namen van de huidige opslaglocaties echter wilt wijzigen, kunt u de artikelen naar een nieuw opslaglocatiesysteem verplaatsen met behulp van het herindelingsdagboek. Dit is een handmatig proces dat veel tijd in beslag neemt. U kunt de opslaglocaties daarom het beste vanaf het begin af aan correct instellen.  

Voor gebruik van de pagina **Voorstel opslaglocatieaanmaak** moet u zijn ingesteld als magazijnmedewerker op de locatie waar de opslaglocaties bestaan. Zie voor meer informatie [Magazijnmedewerkers instellen](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorstel opslaglocatieaanmaak** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Opslaglocaties berekenen**.
3. Selecteer op de pagina **Opslaglocaties berekenen** in het veld **Opslaglocatiesjabloon** de sjabloon waarop u de overige opslaglocaties wilt baseren.
4.  Voer een omschrijving in voor de opslaglocaties die u wilt maken.  
5.  Als u de opslaglocaties te maken, vult u de velden **Van nr.** en **Tot nr.** in in de drie categorieën die op de pagina worden weergegeven: **Rek**, **Sectie** en **Niveau**. De naam van een opslaglocatie kan uit maximaal 20 tekens bestaan.  

    > [!NOTE]  
    >  het aantal tekens dat u in de drie categorieën voor een veld hebt ingevoerd (bijvoorbeeld het aantal tekens dat u hebt ingevoerd in de drie velden **Van nr.**) mag niet groter zijn dan 20 (inclusief eventuele scheidingstekens).  

     Als u letters in de code gebruikt, moet u dezelfde letters gebruiken in de velden **Van nr.** en **Tot nr.** in in. U kunt bijvoorbeeld het gedeelte Rek van de code als volgt instellen: **Van nr. A01** en **Tot nr. A10**. De toepassing is niet ingesteld voor het genereren van codes met letterreeksen, zoals van A01 tot F05.  

6.  In het veld **Veldscheidingsteken** kunt u een scheidingsteken invoeren, bijvoorbeeld een liggend streepje. Hiermee kunt u de categorievelden van elkaar scheiden die u hebt opgegeven als onderdeel van de opslaglocatie.  
7.  Als de toepassing al een regel bevat voor een opslaglocatie en u niet wilt dat er een extra regel wordt gemaakt, selecteert u het veld **Bestaande opslagloc. controleren**.  
8. Wanneer u alle velden hebt ingevuld, klikt u op **OK**.

    Voor elke opslaglocatie in het voorstel wordt een regel gemaakt. U kunt nu ook sommige opslaglocaties verwijderen, bijvoorbeeld als er sprake is van een rek met een passage door de eerste twee niveaus van een aantal secties.  

9. Wanneer u alle overbodige opslaglocaties hebt verwijderd, kiest u de actie **Opslaglocaties maken**. De toepassing maakt dan een opslaglocatie voor elke regel in het voorstel.  

Herhaal dit proces voor elke volgende set opslaglocaties, totdat u alle opslaglocaties van het magazijn hebt gemaakt.  

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/modules/create-new-bins/)

## <a name="see-also" />Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
