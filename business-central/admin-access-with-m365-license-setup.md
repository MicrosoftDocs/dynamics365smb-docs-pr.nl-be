---
title: Toegang met Microsoft 365-licenties instellen
description: Een guide voor hoe beheerders de toegang tot Business Central kunnen configureren met Microsoft 365-licenties.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: 9061
---
# Business Central-toegang in Teams met Microsoft 365-licenties instellen

Beheerders moeten meerdere activiteiten voltooien voordat gebruikers Business Central kunnen gebruiken met hun Microsoft 365-licentie. De onderstaande stappen geven de minimale instellingen weer die nodig zijn om aan de slag te gaan. Ga voor meer informatie over toegang met Microsoft 365-licenties naar [Business Central-toegang met Microsoft 365-licenties](admin-access-with-m365-license.md).

## De Business Central-app voor Teams implementeren

Om als Business Central-licentiehouders gegevens te kunnen delen in Teams, en als Microsoft 365-licentiehouders toegang te krijgen tot die gegevens, moeten ze de Business Central-app voor Teams hebben geïnstalleerd. Hoewel gebruikers de app zelf kunnen installeren, wordt aanbevolen dat beheerders gecentraliseerde implementatie gebruiken. Met gecentraliseerde implementatie kunt u de app uitrollen naar een breder publiek in de hele organisatie en de inzet van individuele gebruikers tot een minimum beperken. 

Zie voor meer informatie over gecentraliseerde implementatie van de Business Central-app voor Teams, zie [De Business Central-app installeren met behulp van gecentraliseerde implementatie](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Als u eerder gecentraliseerde implementatie hebt uitgevoerd en de app alleen hebt geïmplementeerd voor de beveiligingsgroep van gelicentieerde Business Central-gebruikers, moet u deze opnieuw uitvoeren om implementatie in extra groepen of de hele organisatie mogelijk te maken, afhankelijk van hoe u de toegang configureert.

> [!TIP]
> Bent u op zoek naar een snellere manier om aan de slag te gaan bij het uitproberen van deze functie? Testgebruikers kunnen de app installeren op [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## Machtigingen configureren

Business Central is inherent veilig en minimaliseert risico's door niet standaard machtigingen te verlenen aan Microsoft 365-gebruikers. Beheerders moeten objectmachtigingen configureren die bepalen welke tabellen, pagina's en rapporten toegankelijk zijn in Teams met slechts een Microsoft 365-licentie. Deze machtigingen zijn de startmachtigingen die worden toegewezen wanneer een gebruiker zich voor de eerste keer aanmeldt met zijn Microsoft 365-licentie. 

Startmachtigingen configureren:

1. Zoek in Business Central naar **Licentieconfiguratie**.
2. Selecteer de Microsoft 365-licentie.
3. Selecteer bovenaan de **Microsoft 365**-licentiepagina het bewerkingspictogram ![Bewerkingspictogram](media/edit-pencil.png) en schakel vervolgens **Machtigingen aanpassen** in. 
4. Voeg in de sectie **Aangepaste machtigingensets** de juiste machtigingensets toe en kies of ze van toepassing zijn op een enkel bedrijf of alle bedrijven in de omgeving.

Met deze configuratie worden gebruikers met alleen een Microsoft 365-licentie toegevoegd aan de lijst **Gebruikers** wanneer ze Business Central voor de eerste keer openen. Zie [Gebruikers maken volgens licenties](ui-how-users-permissions.md) voor meer informatie over gebruikers.

> [!NOTE]
> Bij het synchroniseren van de gebruikerslijst in Business Central met gebruikers in Microsoft 365, worden alleen gebruikers met een Business Central-licentie toegevoegd aan de gebruikerslijst van Business Central. Voor meer administratieve controle over machtigingen, gebruikersgroepen en profielen kunt u een beveiligingsgroep toewijzen aan de omgeving. Wanneer omgevingen zijn beveiligd met een beveiligingsgroep en toegang inschakelen met Microsoft 365-licenties, omvat de actie **Gebruikers bijwerken vanuit Microsoft 365** op de pagina **Gebruikers** ook gebruikers die alleen een Microsoft 365-licentie hebben. Zie [Toegang beheren met Azure Active Directory-groepen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) in de Help voor ontwikkelaars en IT-professionals voor meer informatie over het beveiligen van omgevingen.

> [!TIP]
> Bent u op zoek naar een snellere manier om aan de slag te gaan bij het uitproberen van deze functie-sandbox of dit evaluatiebedrijf? Wijs de machtigingenset **D365 Lezen** toe, waarmee machtigingen worden verleend voor de meeste objecten.  

Wanneer u met meerdere omgevingen werkt, moet de licentieconfiguratie worden toegepast op elke omgeving en kan deze per omgeving verschillen. 

Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) en [Machtigingensets opstellen](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing) voor meer informatie.

## Toegang met Microsoft 365-licenties inschakelen

Toegang met Microsoft 365-licenties is standaard uitgeschakeld. De toegang moet voor elke omgeving afzonderlijk worden ingeschakeld, zodat beheerders controle hebben en een gefaseerde uitrol in de hele organisatie mogelijk is. U schakelt toegang in via het Business Central-beheercentrum: 

1. Selecteer in de rechterbovenhoek **Instellingen** ![Instellingen.](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") > **Beheercentrum**.  
2. Selecteer in het beheercentrum  **Omgevingen** en selecteer vervolgens de omgeving waarvoor u de licentietoegang wilt wijzigen. 
3. Selecteer op de **Omgevingsdetails** de optie **Wijzigen** voor de instelling **Toegang met Microsoft 365-licenties**.
4. Schakel in het deelvenster **Microsoft 365-licenties** de schakelaar in. 
5. Selecteer **Opslaan** wanneer u klaar bent en accepteer de bevestiging. De wijziging gaat per direct in.

## Uw installatie testen

Om te controleren of uw installatie klaar is voor productie, zullen de volgende stappen u helpen om te controleren of alles naar behoren werkt. 

1. Maak of wijs twee testgebruikers (A en B) aan.

   - Testgebruiker A moet een Business Central-licentie en Microsoft 365-licentie hebben met toegang tot Teams.
   - Testgebruiker B mag alleen een Microsoft 365-licentie hebben met toegang tot Teams.

2. Meld u bij de Business Central-webclient aan als testgebruiker A.

   1. Open een record waartoe testgebruiker B toegang zou moeten hebben, zoals een **Item**-kaart in het juiste bedrijf en in de juiste omgeving.
   2. Selecteer **Delen** ![!Delen met andere apps-actie op pagina's.](media/share-icon.png) > **Delen met Teams** om het venster Delen met teams te openen.
   3. Voeg in het veld **Delen naar** testgebruiker B toe als de ontvanger. 
   4. Wacht tot de koppeling is uitgevouwen naar een kaart en selecteer Delen. 

3. Meld u aan bij Microsoft Teams als testgebruiker B.

   1. Selecteer Chat en open het gesprek met testgebruiker A. 
   2. Selecteer in het bericht van testgebruiker A de knop Details op de kaart. Als de Business Central-client wordt weergegeven en alleen-lezen is, is uw configuratie geslaagd. 

> [!TIP]
> Is er iets fout gegaan? Bekijk dan [Problemen met toegang met Microsoft 365-licenties oplossen](admin-access-with-m365-license-troubleshooting.md).

## Zie ook

[Overzicht van toegang tot Business Central met Microsoft 365-licenties](admin-access-with-m365-license.md#minimum-requirements)  
[Problemen met toegang met Microsoft 365-licenties oplossen](admin-access-with-m365-license-troubleshooting.md)  
[Integratie van Business Central en Microsoft Teams](across-teams-overview.md)  
