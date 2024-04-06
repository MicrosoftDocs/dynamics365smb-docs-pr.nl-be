---
title: Serviceartikelen en serviceartikelonderdelen
description: 'Leer wat u moet instellen voordat u serviceartikelen, inclusief standaardwaarden voor onder andere de responstijd en de serviceprijsgroep, kunt gebruiken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-service-items-and-service-item-components"></a>Serviceartikelen en serviceartikelonderdelen instellen
Als u met serviceartikelen wilt werken, moet u het volgende instellen

* Serviceartikelgroepen.
* Optioneel

## <a name="to-set-up-service-item-groups"></a>Serviceartikelgroepen instellen
U kunt groepen van artikelen instellen die aan elkaar gerelateerd zijn met betrekking tot herstel en onderhoud. U kunt standaardwaarden voor serviceartikelen in een serviceartikelgroep opgeven, zoals responstijd, contractkortingspercentage en serviceprijsgroep. Voor artikelen in een serviceartikelgroep kunt u aangeven of deze automatisch als serviceartikelen moeten worden geregistreerd wanneer ze worden verkocht.  

U wijst serviceartikelgroepen toe aan artikelen op de kaart **Artikel** en aan serviceartikelen op de kaart **Serviceartikel**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceartikelgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe serviceartikelgroep.  
3. Vul de velden **Code** en **Omschrijving** in.  
4. Geef in het veld **Std. contractkorting %** het standaardpercentage voor de contractkorting op dat u wilt toewijzen aan de serviceartikelen in de groep.  
5. Geef in het veld **Std. serviceprijsgroepcode** de code voor de standaardserviceprijsgroep op die u wilt toewijzen aan de serviceartikelen in de groep.  
6. Voer in het veld **Std. responstijd (Uren)** de standaardresponstijd in uren in die u wilt toewijzen aan de serviceartikelen in de groep.  
7. Als u de artikelen in de groep bij verkoop als serviceartikelen wilt registreren, moet u het veld **Serviceartikel maken** selecteren.  

## <a name="to-set-up-service-item-components"></a>Serviceartikelcomponenten instellen
Een serviceartikel kan bestaan uit meerdere onderdelen die u door reserveonderdelen kunt vervangen wanneer voor het artikel service wordt uitgevoerd. Deze onderdelen zijn ingesteld op de pagina **Serviceartikelonderdeeloverzicht**. Als u onderdelen wilt instellen voor serviceartikelen die zijn ingesteld als stuklijst, kunt u de stuklijstartikelen kopiëren en instellen als serviceartikelcomponenten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceartikelen** in en kies vervolgens de gerelateerde koppeling
2. Open het serviceartikel waarvoor u componenten wilt instellen.  
3. Kies de actie **Materialen**. De pagina **Serviceartikelonderdeeloverzicht** wordt geopend.  
4. Een nieuw component toevoegen.  
5. Kies in het veld **Soort** de optie **Serviceartikel** als de component zelf een geregistreerd serviceartikel is. Selecteer anders **Artikel**.  
6. Selecteer in het veld **Nr.** het artikel of serviceartikel dat een component is van het serviceartikel.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Serviceartikelcomponenten instellen uit stuklijsten
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceartikelen** in en kies vervolgens de gerelateerde koppeling  
2. Open het serviceartikel waarvoor u componenten wilt instellen vanuit een stuklijst.  
3. Kies de actie **Materialen**. De pagina **Serviceartikelonderdeeloverzicht** wordt geopend.  
4. Kies de actie **Van stuklijst kopiëren**.  

    Wanneer het artikel waaraan het serviceartikel is gekoppeld, een stuklijst is, worden automatisch componenten gemaakt voor alle artikelen in de stuklijst.  

## <a name="to-set-up-a-service-shelf"></a>Serviceschappen instellen
U kunt serviceschappen instellen om de opslaglocatie van uw serviceartikelen aan te duiden. U wijst serviceschappen toe aan serviceartikelen op de pagina's **Serviceorder** en **Serviceartikelwerkbon**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceschappen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de benodigde velden in.

## <a name="see-also"></a>Zie ook
[Codes voor standaardservices instellen](service-how-setup-service-coding.md)   
[Troubleshooting instellen](service-how-setup-troubleshooting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
