---
title: Bewerkingsplannen maken
description: 'Dit onderwerp geeft een overzicht van de verschillende manieren om bewerkingsplannen te maken, inclusief vereisten en hoe u bewerkingsplankoppelingen kunt maken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000764, 99000765, 99000766, 99000767, 99000794, 99000796, 99000798, 99000806, 99000808, 99000810, 99000817, 99000834, 99000835, 99000836, 99000837, 99000840, 99000841, 99000844, 99000845'
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Bewerkingsplannen maken

Productiebedrijven maken gebruik van bewerkingsplannen om het productieproces te visualiseren en aan te sturen.

Een bewerkingsplan vormt de basis voor procesplanning, capaciteitsplanning, de geplande toewijzing van materiaalbehoeften en productiedocumenten.  

Voor productiestuklijsten worden de bewerkingsplannen toegewezen aan het productie-eindartikel. Een bewerkingsplan bevat de belangrijkste gegevens met betrekking tot wat er nodig is voor het productieproces voor een bepaald geproduceerd artikel. Zodra er voor een artikel een productieorder is gemaakt, worden op basis van het bewerkingsplan ervan de bewerkingen gepland zoals weergegeven op de pagina **Prod.-orderbewerkingsplan** onder de productieorder.  

Voordat u een bewerkingsplan kunt instellen, moet het volgende zijn gedaan:  

- Er zijn artikelkaarten gemaakt voor hoofdartikelen die onderdeel zijn van de productie. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).
- Er zijn productieresources ingesteld. Zie voor meer informatie [Afdelingen en bewerkingsplaatsen instellen](production-how-to-set-up-work-and-machine-centers.md).

## Een bewerkingsplan maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bewerkingsplannen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Selecteer in het veld **Soort** de optie **Serieel** om bewerkingen in het productiebewerkingsplan te berekenen op basis van de waarde in het veld **Bewerkingsnr.**. te kiezen.  
    Selecteer **Parallel** om de bewerkingen te berekenen op basis van de waarde in het **Volgend bewerkingsnr.** te kiezen.  
5. Als u het bewerkingsplan wilt bewerken, stelt u het veld **Status** in op **Nieuw** of **In ontwikkeling**. Als u het wilt inschakelen, stelt u het veld **Status** in op **Gecertificeerd**.  

    Vul de bewerkingsplanregels in.
6. Voer in het veld **Bewerkingsnr.** het nummer in van de eerste bewerking in, bijvoorbeeld **10**.  
7. In het veld **Soort** geeft u op wat voor soort resource wordt gebruikt (bijvoorbeeld **Afdeling**).  
8. Selecteer in het veld **Nr.** de resource of typ deze resource in het veld.  
9. In het veld **Bewerkingsplankoppeling** voert u een code in om het onderdeel aan een bepaalde bewerking te koppelen. Zie [Bewerkingsplankoppelingen maken](production-how-to-create-routings.md#to-create-routing-links) voor meer informatie.
10. Geef in de velden **Bewerkingstijd** en **Insteltijd** de verwerkingstijden op die nodig zijn voor de uitvoering van de bewerking.

     > [!NOTE]
     > De insteltijd wordt per productieorder berekend en de bewerkingstijd per geproduceerd artikel.  

11. Geef in het veld **Gelijktijdige capaciteit** op hoeveel eenheden van de geselecteerde resource worden gebruikt om de bewerking uit te voeren. Bij toewijzing van twee personen aan één verpakkingsbewerking wordt de bewerkingstijd bijvoorbeeld gehalveerd  
12. Ga door met het invullen van de regels voor alle bewerkingen die betrokken zijn bij de productie van het desbetreffende artikel.  
13. Als u regels wilt kopiëren uit een bestaand bewerkingsplan, kiest u de actie **Bewerkingsplan kopiëren** om bestaande regels te selecteren.  
14. Certificeer het bewerkingsplan.  
15. U kunt nu het nieuwe bewerkingsplan aan de kaart van het desbetreffende productieartikel koppelen door het veld **Bew.-plannr.** in te vullen. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).  

> [!NOTE]  
> Zorg ervoor dat u de vaste verrekenprijs van het artikel opnieuw berekent vanuit de kaart **Artikel**: kies hiervoor achtereenvolgens de acties **Productie**, **Vaste verrekenprijs berekenen** en **Alle niveaus**.  

## Bewerkingsplankoppelingen maken

Met bewerkingsplankoppelingen kunt u materialen zodanig aan bepaalde bewerkingen koppelen dat hun relatie behouden blijft ook al wordt de productiestuklijst of het bewerkingsplan gewijzigd. Ook kunnen hierdoor gemakkelijker materialen nog op het laatste moment worden afgeboekt, namelijk op het moment dat de specifieke gekoppelde bewerking wordt opgestart in plaats van wanneer de gehele productieorder wordt vrijgegeven. Zie voor meer informatie [Materialen afboeken op basis van de uitvoer van een bewerking](production-how-to-flush-components-according-to-operation-output.md).  

Een ander belangrijk voordeel van het koppelen van materialen en bewerkingen is dat beide elementen in een logische processtructuur worden weergegeven wanneer u de pagina **Productiedagboek** gebruikt voor het boeken van output en verbruik.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bewerkingsplannen** in en kies vervolgens de gerelateerde koppeling.  
2. Open het bewerkingsplan dat de bewerkingen bevat die moeten worden gekoppeld.  

    Controleer of de status van het bewerkingsplan **In ontwikkeling** is.  

3. Op de desbetreffende bewerkingsplanregel in de **Bewerkingsplankoppeling** selecteert u een code.  
4. Voeg in het bewerkingsplan desgewenst nog andere koppelingen toe aan andere bewerkingen.  

    > [!NOTE]  
    > U kunt het beste niet meer dan één bewerking in een bewerkingsplan koppelen om te voorkomen dat u per ongeluk hetzelfde materiaal aan twee verschillende bewerkingen koppelt, zodat het tweemaal wordt verbruikt.  
    >
    > Het is aan te raden om de bewerkingsplankoppeling dezelfde naam te geven als de bewerking zelf om er zeker van te zijn dat materialen maar aan één bewerking worden gekoppeld.

5. Stel de status van het bewerkingsplan in op **Gecertificeerd**.  

    Nu worden bewerkingsplankoppelingen aan bewerkingen toegewezen. Vervolgens moet u de feitelijke koppeling maken door dezelfde codes toe te wijzen aan bepaalde materialen in de desbetreffende productiestuklijst.  

6. Open de **productiestuklijst** met de onderdelen die aan de bovenstaande bewerkingen moeten worden gekoppeld. Zie voor meer informatie [Productiestuklijsten maken](production-how-to-create-production-boms.md).
7. Controleer of de status van de stuklijst **In ontwikkeling** is.  
8. Op de regel van de desbetreffende productiestuklijst in het veld **Bewerkingsplankoppeling** selecteert u de code die u zojuist hebt toegewezen aan de desbetreffende bewerking.  
9. Ga door met het toevoegen van materialen aan unieke bewerkingen waar dat nodig is.  
10. Stel de status van de productiestuklijst in op **Gecertificeerd**.  

    > [!NOTE]  
    > In een bestaande productieorder kunnen de bewerkingsplankoppelingen pas worden gebruikt nadat u die productieorder hebt vernieuwd. Zie voor meer informatie [Productieorders maken](production-how-to-create-production-orders.md).  

De geselecteerde materialen worden gekoppeld aan de geselecteerde bewerkingen zodra u een productieorder maakt of vernieuwt met behulp van de desbetreffende productiestuklijst en het desbetreffende bewerkingsplan. Dit is op de pagina **Prod.-ordermaterialen** te zien onder de productieorder. Op deze pagina kunt u ook op elk moment bewerkingsplankoppelingen verwijderen en toevoegen.

## Medewerkers, tools en kwaliteitsmetingen toewijzen aan bewerkingsplannen

Als u voor een bewerking medewerkers met speciale kwalificaties, speciale kennis of speciale autorisaties nodig hebt, kunt u deze medewerkers toewijzen aan de bewerking. Daarnaast kunt u tools en kwaliteitsvereisten toewijzen aan de bewerking. In deze procedure wordt beschreven hoe u personeel toewijst. De stappen zijn vergelijkbaar voor andere soorten bewerkinginformatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bewerkingsplannen** in en kies vervolgens de gerelateerde koppeling.  
2. Open het betreffende bewerkingsplan.  
3. Op het sneltabblad **Regels** selecteert u de regel die u wilt verwerken, kiest u de actie **Bewerkingen** en vervolgens kiest u de actie **Medewerkers**.  
4. Vul de velden op de pagina **Medewerkers bewerkingsplan** in.  
5. Kies de knop **OK** om de pagina af te sluiten. De ingevoerde waarden worden gekopieerd en toegewezen aan de bewerking.  

## Nieuwe versies maken van bewerkingsplannen

Het versieprincipe stelt u in staat verschillende versies van een bewerkingsplan te beheren. De structuur van de bewerkingsplanversie komt overeen met de structuur van het bewerkingsplan: een bewerkingsplanversiekop en -regels. Het belangrijkste verschil wordt bepaald door de begindatum.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bewerkingsplannen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het bewerkingsplan dat u wilt kopiëren en kies de actie **Versies**.  
3. Kies op de pagina **Bewerkingsplanversies** de actie **Nieuw**.
4. Vul de benodigde velden in.
5. Voer in het veld **Versiecode** de unieke identificatie van de versie in. Alle combinaties van cijfers en letters zijn toegestaan.  

    De nieuwe versie krijgt automatisch de status **Nieuw**.  
6. Als u bewerkingsregels wilt maken, selecteert u de eerste lege regel en vult u bij **Bewerkingsnr.** de waarde in die overeenkomt met de volgorde van de bewerkingen.

    De bewerkingsregels worden in oplopende volgorde gesorteerd op bewerkingsnummers. Als u later nog wijzigingen of toevoegingen wilt maken, is het raadzaam dat u tussen iedere stap voldoende ruimte voor tussenstappen laat. Het veld **Volgend bewerkingsnr.** verwijst naar de volgende bewerking. Het nummer van de bewerking kan rechtstreeks worden ingevoerd.

7. Wanneer de bewerkingsplanversie is voltooid, wordt het veld **Status** ingesteld op **Gecertificeerd**.

De geldigheid van de versie wordt aangegeven in het veld **Begindatum**.  

## Zie ook

[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]