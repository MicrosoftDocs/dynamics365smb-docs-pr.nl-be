---
title: Gebruikers maken volgens licenties
description: Beschrijft hoe u gebruikers aan Business Central Online of on-premises kunt toevoegen op basis van licenties.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 03/24/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---
# Gebruikers maken volgens licenties

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Dit artikel beschrijft hoe beheerders gebruikers maken en bepalen wie zich kan aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)]. U leert ook hoe u machtigingen toewijst aan verschillende gebruikers op basis van uw productlicenties.

Wanneer u gebruikers maakt in [!INCLUDE[prod_short](includes/prod_short.md)], verleent u hen machtigingen via machtigingensets. U kunt gebruikers ook in gebruikersgroepen indelen. Gebruikersgroepen maken het gemakkelijker om machtigingen en andere instellingen voor meerdere gebruikers tegelijkertijd te beheren. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.  

Voor meer informatie over de verschillende soorten licenties en hoe licenties werken in [!INCLUDE[prod_short](includes/prod_short.md)] [downloadt u de Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Het proces van het beheren van gebruikers en licenties is afhankelijk van of [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises wordt geïmplementeerd. Voor [!INCLUDE [prod_short](includes/prod_short.md)] online moet u gebruikers toevoegen vanuit Microsoft 365. In on-premises implementaties kunt u rechtstreeks gebruikers maken, bewerken en verwijderen.  

## Gebruikers en licenties beheren in online-tenants

Gebruikersaccounts in [!INCLUDE[prod_short](includes/prod_short.md)] moeten eerst worden gemaakt in het Microsoft 365-beheercentrum. Deze gebruikersaccounts zijn niet exclusief voor [!INCLUDE [prod_short](includes/prod_short.md)]. Als u zich abonneert op andere abonnementen, kunnen deze worden gebruikt om u aan te melden bij andere applicaties, zoals Power BI. Ga voor informatie over het maken van gebruikers in het Microsoft 365-beheercentrum naar [Gebruikers toevoegen in het Microsoft-beheercentrum](/microsoft-365/admin/add-users/add-users).

Uw abonnement op [!INCLUDE[prod_short](includes/prod_short.md)] online bepaalt het aantal [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikerslicenties dat u is toegestaan. Gebruikers worden aan uw tenant toegevoegd in het Microsoft Partnercentrum, meestal door uw Microsoft-partner. Zie voor meer informatie [Beheer van Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

U wijst licenties toe aan gebruikers op basis van het werk dat elke gebruiker zal doen in [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt licenties op verschillende manieren toewijzen:

- De Microsoft 365-beheerder van uw bedrijf kan dit doen in het [Microsoft 365-beheercentrum](https://admin.microsoft.com). Zie voor meer informatie [Gebruikers afzonderlijk of in bulk toevoegen aan Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Een Microsoft-partner kan licenties toewijzen in het Microsoft 365-beheercentrum of in het Microsoft Partner Center. Zie voor meer informatie [Gebruikersbeheertaken voor klantaccounts](/partner-center/assign-licenses-to-users) in de Microsoft Partner Center Help.

Zie voor meer informatie [Beheer van Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in de Help voor beheerders.

Nadat gebruikersaccounts zijn gemaakt in het Microsoft 365-beheercentrum, zijn er twee manieren om ze te importeren in [!INCLUDE [prod_short](includes/prod_short.md)]:

- Een gebruikersaccount wordt automatisch geïmporteerd wanneer de gebruiker zich voor het eerst aanmeldt bij [!INCLUDE [prod_short](includes/prod_short.md)].

   > [!NOTE]
   > Nadat een gebruiker zich heeft aangemeld bij [!INCLUDE [prod_short](includes/prod_short.md)] online, kunt u de gebruiker niet meer verwijderen.

- De beheerder kan gebruikers importeren door de actie  **Gebruikers bijwerken vanuit Microsoft 365**  te kiezen op de pagina **Gebruikers* .

Beide benaderingen hebben hun eigen voordelen en u kunt ze tegelijkertijd gebruiken. Elke benadering stelt beheerders in staat om [!INCLUDE [prod_short](includes/prod_short.md)] proactief te configureren om de startmachtigingen, gebruikersgroepen en gebruikersprofielen toe te wijzen. Door de actie **Gebruikers bijwerken vanuit Microsoft 365** te gebruiken hebben beheerders meer controle over het aanpassen van machtigingen, gebruikersgroepen en profielen. Het is een ideale benadering wanneer u [!INCLUDE [prod_short](includes/prod_short.md)] voor het eerst instelt, voordat gebruikers inloggen of wanneer u een nieuw team gebruikers toevoegt.

> [!NOTE]
> Nadat u gebruikers hebt toegevoegd in het Microsoft 365-beheercentrum, raden we u aan de gebruikersinformatie zo spoedig mogelijk bij te werken in [!INCLUDE[prod_short](includes/prod_short.md)]. Het actueel houden van gebruikersinformatie is eenvoudig te doen en zorgt ervoor dat mensen zich altijd kunnen aanmelden. Zie voor meer informatie [Gebruikers toevoegen of gebruikersgegevens en licentietoewijzingen bijwerken in Business Central](#adduser).<br>
>
> Het bijwerken van gebruikersinformatie is vooral belangrijk als u machtigingensets voor de licentie hebt aangepast. Als een nieuwe gebruiker probeert zich aan te melden bij [!INCLUDE[prod_short](includes/prod_short.md)] voordat u deze hebt toegevoegd, lukt dat die gebruiker misschien niet. Zie [Machtigingen configureren op basis van licenties](#licensespermissions) voor meer informatie.
>
> Gebruikers die dit probleem ervaren, worden echter niet echt geblokkeerd. Ze kunnen de actie **Terug naar begin** gebruiken of zich gewoon opnieuw aanmelden om het probleem op te lossen.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Zie voor meer informatie [Gedelegeerde beheerderstoegang tot Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="licensespermissions"></a>Machtigingen configureren op basis van licenties

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Beheerders kunnen machtigingensets en gebruikersgroepen configureren voor elke licentie.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

De veelgebruikte licentie *Dynamics 365 Business Central Teamlid* heeft bijvoorbeeld standaard de volgende machtigingen:

- D365 LEZEN
- D365-TEAMLID
- BEWERKEN IN EXCEL - BEKIJKEN
- RAPPORT EXPORTEREN EXCEL
- LOKAAL

Andere machtigingensets worden automatisch toegevoegd op basis van de gebruikersgroepen die aan de licentie zijn toegewezen. Bij het maken van een nieuwe gebruiker op basis van deze licentie wijst [!INCLUDE[prod_short](includes/prod_short.md)] de machtigingensets toe die afkomstig zijn van de gebruikersgroepen en de machtigingensets van de licentie. Dezelfde startmachtigingen worden aan de gebruiker toegewezen als zijn of haar gebruikersaccount automatisch is gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] of als de beheerder de actie **Gebruikers bijwerken vanuit Microsoft 365** heeft gebruikt op de pagina **Gebruikers**.

Als deze standaardconfiguratie niet de juiste instelling is voor een bepaalde omgeving, kan de beheerder die configuratie wijzigen. Aangepaste machtigingen zijn echter alleen van invloed op nieuwe gebruikers aan wie die licentie is toegewezen. Machtigingen voor bestaande gebruikers aan wie de licentie is toegewezen, worden niet beïnvloed.  

1. Meld u met een beheerdersaccount aan bij [!INCLUDE[prod_short](includes/prod_short.md)].  
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Licentieconfiguratie** in en kies vervolgens de gerelateerde koppeling.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. Kies op de pagina **Licentieconfiguratie** de licentie die u wilt aanpassen en kies vervolgens de actie **Configureren**.  
4. Kies het veld **Machtigingen aanpassen** veld om aanpassing in te schakelen en breng vervolgens de relevante wijzigingen aan.  

    In ons voorbeeld wil de beheerder de machtiging om te bewerken in Excel verwijderen, dus verwijderen verwijdert de beheerder de gebruikersgroep *Excel-exportactie* uit de Teamlid-licentie. In de toekomst krijgen nieuwe gebruikers aan wie de Teamlid-licentie is toegewezen niet de optie om gegevens naar Excel te exporteren. Als de organisatie hierover van gedachten verandert, kunnen ze gewoon teruggaan naar de pagina **Licentieconfiguratie** en de aanpassing voor dat licentietype uitschakelen.  

> [!IMPORTANT]
> Deze aanpassing van machtigingen wordt alleen van kracht voor nieuwe gebruikers die u de betreffende licentie toewijst. Bestaande gebruikers worden niet bijgewerkt. We raden u aan de machtigingen aan te passen voordat u gebruikerslicenties gaat toewijzen in het Microsoft 365-beheercentrum.

### <a name="adduser"></a>Gebruikers toevoegen of gebruikersgegevens en licentietoewijzingen bijwerken in Business Central

Nadat u gebruikers heeft toegevoegd of gebruikersinformatie heeft gewijzigd in het Microsoft 365-beheercentrum, kunt u de gebruikersinformatie snel importeren naar [!INCLUDE[prod_short](includes/prod_short.md)]. De import omvat licentietoewijzingen.  

1. Meld u met een beheerdersaccount aan bij [!INCLUDE[prod_short](includes/prod_short.md)].
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.  
3. Kies **Gebruikers bijwerken vanuit Microsoft 365**.

> [!IMPORTANT]  
> Voor het uitvoeren van de synchronisatie van gebruikers van Microsoft 365 met behulp van de gids **Gebruikers bijwerken vanuit Microsoft 365** is de SUPER-machtigingenset vereist.

> [!NOTE]
> De gids **Gebruikers bijwerken vanuit Microsoft 365** werkt gebruikers niet bij aan wie geen licentie is toegewezen, zoals iemand die globale beheerder en Dynamics 365-beheerder is. Die gebruikers zullen de volgende keer dat ze inloggen op de omgeving updaten.

Voor nieuw gemaakte gebruikers is de volgende stap het toewijzen van gebruikersgroepen en machtigingen. Ga naar [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor informatie Als u een gebruiker bijwerkt en de update een licentiewijziging omvat, worden gebruikers toegewezen aan de juiste gebruikersgroep en worden hun machtigingensets bijgewerkt. Zie [Machtigingen beheren via gebruikersgroepen](ui-define-granular-permissions.md) voor meer informatie.  

> [!NOTE]
> Alle gebruikers in een omgeving moeten dezelfde licentie krijgen, Essentials of Premium. Ga voor meer informatie over licenties naar de website van [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Voor meer informatie over het synchroniseren van gebruikersinformatie met Microsoft 365 gaat u naar de sectie [Synchronisatie met Microsoft 365](#m365).

> [!NOTE]
> Als u een externe auditor gebruikt om uw boeken en financiële rapportage beheren, kunt u deze uitnodigen voor uw [!INCLUDE[prod_short](includes/prod_short.md)], zodat hij of zij met u kan werken aan uw fiscale gegevens. Zie voor meer informatie [Uw externe accountant uitnodigen voor uw Business Central](finance-accounting.md#inviteaccountant).

### De toegang van een gebruiker tot het systeem verwijderen

U kunt de toegang van een gebruiker tot [!INCLUDE[prod_short](includes/prod_short.md)] online verwijderen. Alle verwijzingen naar de gebruiker blijven behouden. De gebruiker kan zich echter niet aanmelden en actieve sessies voor de gebruiker worden gestopt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling
2. Open de pagina **Gebruikerskaart** voor de relevante gebruiker en selecteer in het veld **Status** de optie **Uitgeschakeld**.
3. Als u de gebruiker weer toegang wilt geven, stelt u het veld **Status** in op **Ingeschakeld**.

U kunt de licentie ook verwijderen van een gebruiker in het Microsoft 365-beheercentrum. De gebruiker kan zich dan niet meer aanmelden. Zie voor meer informatie [Licenties van gebruikers verwijderen](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="m365"></a>Synchronisatie met Microsoft 365

Wanneer u een licentie voor [!INCLUDE[prod_short](includes/prod_short.md)] toewijst aan een gebruiker in Microsoft 365, zijn er twee manieren om de gebruiker te maken in [!INCLUDE[prod_short](includes/prod_short.md)].  

- De beheerder kan de gebruiker toevoegen door de actie **Gebruikers bijwerken vanuit Microsoft 365** te kiezen op de pagina **Gebruikers** zoals beschreven in de sectie [Een gebruiker toevoegen of gebruikersgegevens bijwerken in Business Central](#adduser).
- De licentie-informatie wordt automatisch bijgewerkt wanneer de gebruiker zich voor de eerste keer aanmeldt.

In beide gevallen worden automatisch verschillende instellingen toegepast. Deze instellingen worden vermeld in de tweede en derde kolom in de onderstaande tabel.

Als u gebruikersgegevens wijzigt in Microsoft 365, kunt u [!INCLUDE[prod_short](includes/prod_short.md)] bijwerken om de verandering te weerspiegelen. Gebruik een van de acties op de pagina **Gebruikers**, afhankelijk van wat u wilt bijwerken. Deze acties worden beschreven in de laatste twee kolommen in de onderstaande tabel.

|Wat gebeurt er wanneer:|Eerste gebruiker, eerste aanmelding|Gebruikers bijwerken vanuit Microsoft 365|Standaardgebruikersgroepen van gebruiker herstellen|
|-|-|-|-|
|Bereik:|Huidige gebruiker|Meerdere geselecteerde gebruikers|Eén geselecteerde gebruiker (behalve huidige)|
|Maak de nieuwe gebruiker en wijs SUPER-machtigingenset toe.<br /><br /><!--Platform-->|**X**|**X** | | 
|Werk de gebruiker bij op basis van informatie in Microsoft 365: Status, Volledige naam, Contact-e-mail, E-mailadres voor verificatie.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Synchroniseer gebruikersplannen (licenties) met toegewezen licenties en rollen in Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Voeg de gebruiker toe aan gebruikersgroepen volgens de huidige gebruikersplannen. Verwijder de SUPER-machtigingenset voor alle gebruikers behalve de eerste gebruiker die zich aanmeldt en [beheerders](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Er is ten minste één SUPER nodig.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Verwijdert handmatig toegewezen gebruikersgroepen en machtigingen.|

Gebruikers hebben toegang tot Business Central-gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]-records in Teams met alleen hun Microsoft 365-licentie. Wanneer toegang is ingeschakeld voor een omgeving, worden bij synchronisatie met de actie **Gebruikers bijwerken vanuit Microsoft 365** geen gebruikers opgenomen die alleen een Microsoft 365-licentie hebben. Om deze gebruikers in de synchronisatie op te nemen moet u eerst de omgevingsinstellingen bijwerken door een beveiligingsgroep toe te wijzen die gebruikers bevat met een [!INCLUDE[prod_short](includes/prod_short.md)]-licentie en gebruikers met alleen een Microsoft 365-licentie.

Lees meer over het beveiligen van toegang tot omgevingen met behulp van beveiligingsgroepen op [Toegang beheren met Microsoft Entra-groepen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Krijg een overzicht van toegang tot [!INCLUDE[prod_short](includes/prod_short.md)] in Teams met Microsoft 365-licenties op [admin-access-with-m365-license](admin-access-with-m365-license.md).

## Gebruikers en licenties beheren in on-premises implementaties

Voor on-premises implementaties wordt het aantal gebruikerslicenties opgegeven in het licentiebestand (.bclicense of .flf). Wanneer een beheerder of Microsoft-partner het licentiebestand uploadt, kan deze opgeven welke gebruikers zich kunnen aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)].

Voor on-premises implementaties maakt de beheerder gebruikers rechtstreeks op de pagina **Gebruikers**.

### Een gebruiker in een on-premises implementatie bewerken of verwijderen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling
2. Selecteer de gebruiker die u wilt bewerken en kies vervolgens de actie **Bewerken**.
3. Wijzig indien nodig op de pagina **Gebruikerskaart** de informatie.  
4. Als u een gebruiker wilt verwijderen, selecteert u die gebruiker en kiest u de actie **Verwijderen**.

> [!NOTE]
> Voor on-premises implementaties kan een beheerder specificeren hoe gebruikersreferenties in het [!INCLUDE[server](includes/server.md)]-exemplaar worden geverifieerd. Wanneer u een gebruiker maakt, geeft u het type referentie op dat u gebruikt.
>
> Zie voor meer informatie [Verificatie en referentietypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in de beheer-Help voor [!INCLUDE[prod_short](includes/prod_short.md)].

## Zie ook

[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Profielen beheren](admin-users-profiles-roles.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Aanpassen [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Beheer](admin-setup-and-administration.md)  
[Licenties in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Gebruikers aan Microsoft 365 toevoegen voor bedrijven](/microsoft-365/admin/add-users/add-users)  
[Beveiliging en bescherming in Business Central (beheerinhoud)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Een telemetrie-id toewijzen aan gebruikers](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]