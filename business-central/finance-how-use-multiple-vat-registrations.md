---
title: Meerdere btw-registratienummers
description: Lees meer over de functionaliteit voor meerdere (alternatieve) btw-registratienummers.
author: altotovi
ms.topic: conceptual
ms.reviewer: null
ms.search.keywords: 'VAT, multiple, alternative, customer, tax, value-added tax'
ms.search.form: '212, 301,'
ms.date: 08/21/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Meerdere btw-registratienummers 

Voor bedrijven met magazijnen in meerdere EU-landen kan het beheren van de btw (belasting over de toegevoegde waarde) een uitdaging zijn, omdat elke magazijnlocatie een ander btw-nummer vereist om te voldoen aan de specifieke regelgeving van elk land. In dit artikel vindt u informatie over deze vereiste en wordt de functionaliteit voor meerdere btw-registratienummers uitgelegd. Met deze functionaliteit kunnen gebruikers belastingregistratienummers instellen voor klanten in verschillende landen/regio's.  

> [!NOTE]
> De functionaliteit *Meerdere btw-nummers voor klanten* is alleen beschikbaar vanaf Business Central 2024 releasewave 2 (versie 25).

## Hoe u de alternatieve btw-registratienummers instelt  

Om de alternatieve btw-registratienummers voor verschillende landen/regio's in te stellen, voert u de volgende stappen uit: volgen 

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, voer  **Alternatieve btw-registratie voor klanten** in en selecteer vervolgens de gerelateerde koppelen. 
2. Voeg de klant toe in het veld  **Klantnummer**  en het land/de regio die gerelateerd is aan deze btw-registratie in het veld  **btw-land-/regiocode**.  
3. U moet het btw-nummer toevoegen in het veld  **btw-registratienummer** . U moet zich aan de opmaak houden wanneer u  **Land-/regiocode** gebruikt. 
4. Als u verschillende btw- of algemene boekingsgroepen wilt gebruiken, kunt u deze ook toevoegen aan de instellingen in de velden  **btw-bus. Boekingsgroep** en  **Algemene bus. Boekingsgroep** . 
5. De pagina sluiten.   

Om een alternatief adres voor uw klant aan te maken, volgt u de volgende stappen: volgen  

1. Open de **Klant** kaart voor de klant waaraan u een nieuw **verzendadres** wilt toevoegen. 
2. Selecteer  **Klant** en kies de actie  **Verzendadressen** .   
3. De pagina  **Lijst met verzendadressen** wordt geopend en u selecteert  **Nieuw**. 
4. Vul de informatie in over de bestemming van uw klant.  
5. Kies de juiste **land-/regiocode**.   
6. Als u al een nieuw **btw-registratienummer** hebt geconfigureerd op de **Alternatieve btw-registratie voor klanten** voor dit land of deze regio, gebeurt er niets. 
7. Maar als u het **btw-registratienummer** niet eerder hebt geconfigureerd in de **Alternatieve btw-registratie van de klant** voor dit land of deze regio, verschijnt de volgende melding: **Klik op Toevoegen als u de alternatieve btw-registratie voor deze verzendlandcode wilt invoegen.** 
8. Er verschijnt een waarschuwing dat u een nieuw btw-nummer moet toevoegen. Om dit te doen, moet u de actie  **Toevoegen** in de melding selecteren. De pagina  **Alternatieve btw-registratie voor klanten** wordt geopend. 
9. Op deze pagina wordt uw **Klantnummer ingevuld.** En de  **btw-land-/regiocode**. U hoeft dus alleen de instellingen toe te voegen die u wilt gebruiken. 

## Werken met de verkoopdocumenten   

U kunt een nieuwe [verkoopfactuur](sales-how-invoice-sales.md) of [verkooporder](sales-how-sell-products.md) aanmaken in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u een verzendadres moet gebruiken dat verschilt van het adres van de klant en dat zich in een ander land bevindt, volgt u de volgende stappen: volgen  

### Alternatief verzendadres  

1. Vouw het sneltabblad **Verzending en facturering** uit.   
2. Selecteer in het veld Verzendadres de optie  **Alternatief verzendadres** . 
3. De pagina  **Lijst met verzendadressen** met beschikbare alternatieve adressen wordt weergegeven. 
4. Kies een van de adressen met een andere **land-/regiocode**. 
5. De dialoogpagina  **Alternatieve btw-registratie van klant bevestigen** wordt weergegeven met een lijst met velden die u hebt gewijzigd vanwege de instellingswijziging van de  **Alternatieve btw-registratie van klant** . 
6. Selecteer **OK** om te bevestigen.   

> [!NOTE]
> Als u een dergelijke keuze niet meer wilt bevestigen, kunt u het veld  **Niet meer weergeven**  selecteren. In de toekomst ziet u dit type melding over wijzigingen niet meer. Maar als u het opnieuw wilt inschakelen, kunt u dat doen door het veld  **Alternatieve btw-registratie bevestigen** in te schakelen in de  **btw-instellingen**.  
   
7. Zodra u bevestigt, worden de waarden overschreven met de waarden uit de instellingen van de  **Alternatieve btw-registratie voor klanten** . U kunt alle btw-gerelateerde velden controleren die zich onder het sneltabblad  **Factuurgegevens** bevinden.  
8. U boekt het document.  

### Aangepast adres  

Als u het verzendadres niet hebt geconfigureerd, maar toch een ander verzendadres wilt gebruiken, kunt u deze optie gebruiken.  

1. Vouw het sneltabblad **Verzending en facturering** uit.   
2. Kies in het veld Verzendadres de optie  **Aangepast adres** .  
3. Wijzig het land in het veld  **Land/Regio** .  
4. Zodra u de land-/regiocode wijzigt zodat deze overeenkomt met de **btw-land-/regiocode** van de **Alternatieve btw-registratie van klanten**, verschijnt de dialoogvensterpagina **Alternatieve btw-registratie van klanten bevestigen**  met een lijst met velden die zijn gewijzigd. 
5. [!INCLUDE[prod_short](includes/prod_short.md)] wijzigt ook alle btw-gerelateerde velden die zich onder het sneltabblad  **factuurdetails**  bevinden.  

### Werk zonder verzending 

Als er geen verzending als proces is, kunt u nog steeds gebruikmaken van de instellingen van de  **Alternatieve btw-registratie voor klanten** .

In de verkooporder of factuur vindt u de  **btw-land-/regiocode** onder het sneltabblad  **Factuurgegevens** en geeft u de waarde op die overeenkomt met de instellingen van de  **Alternatieve btw-registratie voor klanten** . U zou dezelfde bevestigingsdialoogpagina moeten zien als hierboven. 

In deze situatie kunt u een verkoopfactuur boeken met het juiste **btw-registratienummer** voor uw klant, zelfs als u geen artikelen met dit document verzendt. 

### Werken met de verkoopcreditnota  

Zodra u de factuur boekt met een **verzendadres** of **btw-land-/regiocode** met andere boekingsgegevens, haalt de corrigerende **Verkoopcreditnota** de waarden uit de **geboekte verkoopfactuur** koptekst, terwijl deze waarden worden overgenomen uit de **Alternatieve btw-registratie van de klant**. Er zijn dus geen andere acties vereist. 

## Zie ook

[Overzicht btw-beheer](finance-manage-vat.md)    
[Omzetbelasting instellen](finance-setup-vat.md)    
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)    
[btw melden bij de Belastingdienst](finance-how-report-vat.md)    
[Lokale functionaliteit in Business Central](about-localization.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
