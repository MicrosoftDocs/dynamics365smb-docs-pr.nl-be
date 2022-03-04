---
title: Verbinding maken met Microsoft Dataverse (bevat video)
description: Een verbinding instellen tussen Business Central en Dataverse. Bedrijven maken doorgaans de verbinding om gegevens te integreren met een andere Dynamics 365-bedrijfsapp.
author: bholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 7200, 7201
ms.date: 09/30/2021
ms.author: bholtorf
ms.openlocfilehash: 8b5a393356f4028de8278bad3177592c8d26fe40
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130760"
---
# <a name="connect-to-microsoft-dataverse"></a>Verbinding maken met Microsoft Dataverse



In dit onderwerp wordt beschreven hoe u een verbinding tot stand brengt tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Bedrijven maken doorgaans de verbinding om gegevens te integreren en te synchroniseren met een andere Dynamics 365-bedrijfsapp, zoals [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Voordat u begint

Voordat u de verbinding maakt, moet u een aantal gegevens gereed hebben:  

* De URL van de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-omgeving waarmee u verbinding wilt maken. Als u de begeleide instelling **Dataverse-verbinding instellen** gebruikt om de verbinding tot stand te brengen, ontdekken we uw omgevingen, maar u kunt ook de URL van een andere omgeving in uw tenant invoeren.  
* De gebruikersnaam en het wachtwoord van een account dat beheerdersmachtigingen heeft in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Als u een on-premises [!INCLUDE[prod_short](includes/prod_short.md)] 2020 releasewave 1, versie 16.5, hebt, leest u het artikel [Enkele bekende problemen](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). U moet de beschreven tijdelijke oplossing voltooien voordat u verbinding kunt maken met [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* De lokale valuta voor het bedrijf in [!INCLUDE[prod_short](includes/prod_short.md)] moet dezelfde zijn als de basistransactievaluta in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Nadat een basistransactie is ingesteld in [!INCLUDE[cds_long_md](includes/cds_long_md.md)], kan deze niet worden gewijzigd. Zie voor meer informatie [De entiteit Transactievaluta (valuta)](/powerapps/developer/data-platform/transaction-currency-currency-entity). Dit betekent dat alle [!INCLUDE[prod_short](includes/prod_short.md)] bedrijven waarmee u verbinding maakt met een [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-organisatie dezelfde valuta moeten gebruiken.

> [!IMPORTANT]
> Uw [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-omgeving mag niet in de beheermodus zijn. De beheermodus zorgt ervoor dat de verbinding mislukt omdat het integratiegebruikersaccount voor de verbinding geen beheerdersmachtigingen heeft. Zie [Beheermodus](/power-platform/admin/admin-mode) voor meer informatie.

> [!Note]
> Deze stappen beschrijven de procedure voor [!INCLUDE[prod_short](includes/prod_short.md)] online.
> Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt en geen Azure Active Directory-account gebruikt om verbinding te maken met [!INCLUDE [cds_long_md](includes/cds_long_md.md)], moet u ook een gebruikersnaam en wachtwoord van een gebruikersaccount opgeven voor de integratie. Dit account wordt de 'integratiegebruiker' genoemd. Als u een Azure Active Directory-account gebruikt, is het gebruikersaccount voor integratie niet vereist of weergegeven. De integratiegebruiker wordt automatisch ingesteld en heeft geen licentie nodig.

## <a name="set-up-a-connection-to-cds_long_md"></a>Een verbinding instellen met [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Voor alle verificatiesoorten anders dan Microsoft 365-verificatie stelt u de verbinding met [!INCLUDE[cds_long_md](includes/cds_long_md.md)] in op de pagina **Dataverse-verbinding instellen**. Het is raadzaam de begeleide instelling **Dataverse-verbinding instellen** te gebruiken voor Microsoft 365-verificatie. De begeleide instelling maakt het gemakkelijker om de verbinding in te stellen en geavanceerde functies op te geven, zoals het eigendomsmodel en initiële synchronisatie.  

> [!IMPORTANT]
> Tijdens het instellen van de verbinding met [!INCLUDE[cds_long_md](includes/cds_long_md.md)] wordt de beheerder gevraagd om de volgende machtigingen te geven aan een geregistreerde Azure-toepassing met de naam [!INCLUDE[prod_short](includes/prod_short.md)]-integratie met [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * De machtiging **Toegang tot [!INCLUDE[cds_long_md](includes/cds_long_md.md)] krijgen als uzelf** is nodig, zodat [!INCLUDE[prod_short](includes/prod_short.md)] namens de beheerder automatisch een niet-gelicentieerde, niet-interactieve gebruiker van de [!INCLUDE[prod_short](includes/prod_short.md)]-integratietoepassing kan maken, beveiligingsrollen kan toewijzen aan deze gebruiker en de [!INCLUDE[prod_short](includes/prod_short.md)]-integratieoplossing kan implementeren naar [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Deze toestemming wordt slechts één keer gebruikt tijdens het instellen van de verbinding met [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * De machtiging **Volledige toegang tot Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** hebben is nodig zodat de automatisch gemaakte gebruiker van de [!INCLUDE[prod_short](includes/prod_short.md)]-integratietoepassing toegang tot [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens kan krijgen die worden gesynchroniseerd.  
> * De machtiging **Aanmelden en uw profiel lezen** is nodig om te verifiëren dat de gebruiker die zich aanmeldt de beveiligingsrol Systeembeheerder toegewezen heeft gekregen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Door namens de organisatie toestemming te geven geeft de beheerder de geregistreerde Azure-toepassing genaamd [!INCLUDE[prod_short](includes/prod_short.md)]-integratie met [!INCLUDE[cds_long_md](includes/cds_long_md.md)] het recht gegevens te synchroniseren met de referenties van de automatisch gemaakte gebruiker van de [!INCLUDE[prod_short](includes/prod_short.md)]-integratietoepassing.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>De begeleide instelling Dataverse-verbinding instellen gebruiken
De begeleide instelling Dataverse-verbinding instellen kan het gemakkelijker maken om de toepassingen te verbinden en kan u zelfs helpen bij het uitvoeren van een eerste synchronisatie. Als u ervoor kiest om de eerste synchronisatie uit te voeren, zal [!INCLUDE[prod_short](includes/prod_short.md)] de gegevens in beide applicaties bekijken en aanbevelingen doen voor het benaderen van de initiële synchronisatie. De volgende tabel beschrijft de verschillende aanbevelingen.

|Aanbeveling  |Omschrijving  |
|---------|---------|
|**Volledige synchronisatie**|Gegevens bestaan alleen in [!INCLUDE[prod_short](includes/prod_short.md)] of alleen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. De aanbeveling is om alle gegevens van de service die ze heeft te synchroniseren met de andere service.|
|**Geen synchronisatie**|Er zijn gegevens in beide toepassingen en bij volledige synchronisatie worden de gegevens gedupliceerd. De aanbeveling is om records te koppelen.|
|**Niet voldaan aan afhankelijkheid**|Er zijn gegevens in beide toepassingen, maar de rij of tabel kan niet worden gesynchroniseerd omdat deze afhankelijk is van een rij of tabel waarvoor de aanbeveling Geen synchronisatie geldt. Als klanten bijvoorbeeld niet kunnen worden gesynchroniseerd, kunnen gegevens voor contacten die afhankelijk zijn van de klantgegevens ook niet worden gesynchroniseerd.|

> [!IMPORTANT]
> Normaal gesproken gebruikt u alleen volledige synchronisatie wanneer u de applicaties voor de eerste keer integreert en bevat slechts één applicatie gegevens. Volledige synchronisatie kan handig zijn in een demonstratieomgeving omdat het automatisch records maakt en koppelt in elke applicatie, waardoor het sneller wordt om met gesynchroniseerde gegevens te werken. U moet echter alleen volledige synchronisatie uitvoeren als u één rij wilt in [!INCLUDE[prod_short](includes/prod_short.md)] voor elke rij in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] voor de tabeltoewijzingen. Anders kan het resultaat dubbele records zijn.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Begeleide instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Een verbinding instellen met Microsoft Dataverse** om de begeleide instelling te starten.
3. Vul de vereiste velden in.

> [!NOTE]
> Als u niet wordt gevraagd om u aan te melden met uw beheerdersaccount, komt dit waarschijnlijk omdat pop-ups worden geblokkeerd. Sta pop-ups vanaf `https://login.microsoftonline.com` toe om u aan te melden.

### <a name="to-create-or-maintain-the-connection-manually"></a>De verbinding handmatig maken of onderhouden

In de volgende procedure wordt beschreven hoe u de verbinding op de pagina **Dataverse-verbinding instellen** handmatig instelt. Dit is ook de pagina waar u instellingen voor de integratie beheert.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Dataverse-verbinding instellen** in en kies vervolgens de gerelateerde koppeling.
2. Voer de volgende gegevens in voor de verbinding van [!INCLUDE[prod_short](includes/prod_short.md)] met [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Veld|Omschrijving|
    |-----|-----|
    |**Omgevings-URL**|Als u eigenaar bent van omgevingen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)], vinden we die voor u wanneer u de instelling uitvoert. Als u verbinding wilt maken met een andere omgeving in een andere tenant, kunt u de beheerdersreferenties voor de omgeving invoeren en zullen we die ontdekken. |
    |**Ingeschakeld**|Begin de integratie te gebruiken. Als u de verbinding niet nu inschakelt, worden de verbindingsinstellingen opgeslagen, maar hebben gebruikers geen toegang tot [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-gegevens uit [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt naar deze pagina terugkeren en de verbinding later inschakelen.  |

3. Kies in het veld **Eigendomsmodel** of u wilt dat een teamtabel in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] eigenaar is van nieuwe records of een of meer specifieke gebruikers. Als u **Persoon** kiest, moet u elke gebruiker opgeven. Als u **Team** kiest, wordt de standaardbedrijfsunit weergegeven in het veld **Gekoppelde bedrijfsunit**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Als u de verbindingsinstellingen wilt testen, kiest u **Verbinding** en vervolgens **Verbinding testen**.  

    > [!NOTE]  
    > Als gegevensversleuteling niet is ingeschakeld in [!INCLUDE[prod_short](includes/prod_short.md)], wordt u gevraagd of u het wilt inschakelen. Als u gegevensversleuteling wilt inschakelen, kiest u **Ja** en geeft u de vereiste informatie op. Anders kiest u **Nee**. U kunt gegevenscodering later inschakelen. Zie voor meer informatie [Gegevens versleutelen in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) in de Help voor ontwikkelaars en beheerders.  
5. Als [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synchronisatie niet al is ingesteld, wordt u gevraagd of u de standaardinstellingen voor synchronisatie wilt gebruiken. Afhankelijk van of u records uitgelijnd wilt houden in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)], kiest u **Ja** of **Nee**.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>De koppeling op basis van overeenkomsten aanpassen

Vanaf 2021 release wave 2 kunt u records koppelen in [!INCLUDE [prod_short](includes/prod_short.md)] en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] op basis van door de beheerder gedefinieerde criteria.  

Het algoritme voor het matchen van records kan worden gestart vanaf de volgende plaatsen in [!INCLUDE [prod_short](includes/prod_short.md)]:

* Lijstpagina's die records tonen die zijn gesynchroniseerd met [!INCLUDE [cds_long_md](includes/cds_long_md.md)], zoals de pagina's Klanten en Artikelen.  

    Selecteer meerdere records en kies vervolgens de actie **Gerelateerd**, kies **Dataverse**, kies **Koppeling** en kies vervolgens **Koppeling op basis van overeenkomsten**.

    Wanneer het op overeenkomsten gebaseerde koppelingsproces wordt gestart vanuit een hoofdgegevenslijst, wordt er direct een koppelingstaak gepland nadat u de koppelingscriteria hebt geselecteerd.  
* De pagina Controle van volledige **Dataverse-synchronisatie**.  

    Wanneer het volledige synchronisatieproces detecteert dat u ontkoppelde records in [!INCLUDE [prod_short](includes/prod_short.md)] en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] hebt, wordt een koppeling **Koppelingscriteria selecteren** weergegeven voor de relevante integratietabel.  

    U kunt het proces **Volledige synchronisatie uitvoeren** starten vanaf de pagina's **Dataverse-verbinding instellen** en **Dynamics 365-verbinding instellen** en het kan worden gestart als een stap in de begeleide instelling **Een verbinding instellen met Dataverse** wanneer u ervoor kiest om de installatie te voltooien en aan het einde volledige synchronisatie uit te voeren.  

    Wanneer het op overeenkomsten gebaseerde koppelingsproces wordt gestart vanaf de pagina **Controle van volledige Dataverse-synchronisatie**, wordt er direct een koppelingstaak gepland nadat u de instelling hebt voltooid.  
* De lijst **Toewijzingen van integratietabellen**.  

    Selecteer een toewijzing, kies de actie **Koppeling** en kies vervolgens **Op overeenkomsten gebaseerde koppeling**.

    Wanneer het op overeenkomsten gebaseerde koppelingsproces wordt gestart vanuit een integratietabeltoewijzing, wordt een koppelingstaak uitgevoerd voor alle ontkoppelde records in die toewijzing. Als het werd uitgevoerd voor een set geselecteerde records uit de lijst, wordt het alleen uitgevoerd voor de geselecteerde ontkoppelde records.

In alle drie de gevallen wordt de pagina **Koppelingscriteria selecteren** geopend, zodat u de relevante koppelingscriteria kunt definiëren. Pas op deze pagina de koppeling aan met de volgende taken:

* Kies op welke velden overeenkomsten met [!INCLUDE [prod_short](includes/prod_short.md)]-records en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-entiteiten worden bepaald, en kies ook of de overeenkomst op dat veld hoofdlettergevoelig is of niet.  

* Geef op of er een synchronisatie moet worden uitgevoerd na het koppelen van records en, als de record bidirectionele toewijzing gebruikt, kies ook wat er gebeurt als conflicten worden vermeld op de pagina **Updateconflicten oplossen**.  

* Geef prioriteit aan de volgorde waarin records worden doorzocht door een *overeenkomstprioriteit* op te geven voor de relevante toewijzingsvelden. De overeenkomstprioriteiten zorgen ervoor dat het algoritme naar een overeenkomst zoekt in een aantal iteraties, zoals gedefinieerd door de **Prioriteit overeenkomst**-veldwaarden in oplopende volgorde. Een blanco waarde in het veld **Prioriteit overeenkomst** wordt geïnterpreteerd als prioriteit 0, dus velden met deze waarde worden als eerste beschouwd.  

* Geef op of u een nieuw entiteitsexemplaar wilt maken in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] in het geval dat er geen unieke ontkoppelde overeenkomst kan worden gevonden met behulp van de matchcriteria. Om deze mogelijkheid te activeren kiest u de actie **Nieuw maken als geen overeenkomst is gevonden**.  

### <a name="view-the-results-of-the-coupling-job"></a>De resultaten van de koppelingstaak bekijken

Om de resultaten van de koppelingstaak te bekijken opent u de pagina **Integratietabeltoewijzingen**, selecteert u de relevante toewijzing, kiest u de actie **Koppeling** actie en kiest u vervolgens de actie **Taaklogbestand voor integratiekoppeling**.  

Als er records zijn die niet zijn gekoppeld, kunt u inzoomen op de waarde in de kolom Mislukt, waardoor een lijst met fouten wordt geopend die aangeeft waarom de records niet konden worden gekoppeld.  

Mislukte koppeling komt vaak voor in de volgende gevallen:

* Er zijn geen overeenkomstcriteria gedefinieerd

    Voer in dit geval de op overeenkomsten gebaseerde koppeling opnieuw uit, maar vergeet niet om koppelingscriteria te definiëren.

* Er is geen overeenkomst gevonden voor een aantal records, op basis van de gekozen overeenkomende velden

    Herhaal in dit geval de koppeling met enkele andere overeenkomende velden.

* Er zijn meerdere overeenkomsten gevonden voor een aantal records, op basis van de gekozen overeenkomende velden  

    Herhaal in dit geval de koppeling met enkele andere overeenkomende velden.

* Er is één overeenkomst gevonden, maar de overeenkomende record is al gekoppeld aan een andere record in [!INCLUDE [prod_short](includes/prod_short.md)]  

    Herhaal in dit geval de koppeling met enkele andere overeenkomende velden of onderzoek waarom die [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-entiteit is gekoppeld aan die andere record in [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> Om u te helpen een overzicht te krijgen van de voortgang van de koppeling, geeft het veld **Gekoppeld aan Dataverse** aan of een bepaalde record is gekoppeld aan een [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-entiteit of niet. U kunt de lijst met records die worden gesynchroniseerd met [!INCLUDE [cds_long_md](includes/cds_long_md.md)], filteren op dit veld.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Verbindingen vanuit Business Central Online upgraden om op certificaten gebaseerde verificatie te gebruiken
> [!NOTE]
> Deze sectie is alleen relevant voor [!INCLUDE[prod_short](includes/prod_short.md)] online-tenants die worden gehost door Microsoft. Online tenants die worden gehost door ISV's en installaties op locatie worden niet beïnvloed.

In april 2022 [!INCLUDE[cds_long_md](includes/cds_long_md.md)] is het verificatietype van Office365 (gebruikersnaam/wachtwoord) aan het aflopen. Voor meer informatie zie [Afschaffing van het Office365-verificatietype](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Bovendien beëindigt [!INCLUDE[prod_short](includes/prod_short.md)] in maart 2022 het gebruik van op clientgeheimen gebaseerde service-to-service-verificatie voor online tenants, en vereist het gebruik van op certificaten gebaseerde service-to-service-verificatie voor verbindingen met [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] online-tenants die worden gehost door ISV's en on-premises installaties, kunnen clientgeheimauthenticatie blijven gebruiken om verbinding te maken met [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

Om te voorkomen dat integraties worden verstoord _moet u upgraden_ om op certificaten gebaseerde verificatie te gebruiken. Hoewel de wijziging is gepland voor maart 2022, raden we u ten zeerste aan zo snel mogelijk te upgraden. In de volgende stappen wordt beschreven hoe u kunt upgraden naar verificatie op basis van certificaten. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Uw Business Central online-verbinding upgraden om op certificaten gebaseerde verificatie te gebruiken

> [!NOTE]
> Verificatie op basis van certificaten is beschikbaar in Business Central 2021 releasewave 1 en hoger. Als u een eerdere versie gebruikt, moet u vóór maart 2022 een update naar Business Central 2021-releasewave 1 plannen. Zie [Updates plannen](/dynamics365/business-central/dev-itpro/administration/update-rollout-timeline#scheduling-updates) voor meer informatie. Als u problemen ondervindt, neemt u contact op met uw partner of ondersteuning.

1. Controleer in het [Business Central-beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center) of u Business Central 2021 releasewave 1 of hoger (versie 18 of hoger) gebruikt.
2. Afhankelijk van of u integreert met Dynamics 365 Sales, voert u een van de volgende handelingen uit:
   * Als u dat doet, opent u de pagina **Microsoft Dynamics 365-verbinding instellen**.
   * Als u dat niet doet, opent u de pagina **Dataverse 365-verbinding instellen**.
3. Kiezen **Verbinding** en dan **Certificaatverificatie gebruiken** om de verbinding te upgraden om verificatie op basis van certificaten te gebruiken.
4. Meld u aan met beheerdersreferenties voor Dataverse. Aanmelden duurt minder dan een minuut.

> [!NOTE]
> U moet deze stappen herhalen in elke [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving, inclusief zowel productie- als sandbox-omgevingen, en in elk bedrijf waar u een verbinding mee hebt [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Verbinding maken met on-premises versies

Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises wilt verbinden met [!INCLUDE[cds_long_md](includes/cds_long_md.md)], moet u wat informatie opgeven op de pagina **Dataverse-verbinding instellen**.

Als u verbinding wilt maken met een Azure Active Directory (Azure AD)-account, moet u een toepassing registreren in Azure AD en de toepassings-id, het sleutelkluisgeheim en de omleidings-URL opgeven die moeten worden gebruikt. De omleidings-URL wordt vooraf ingevuld en zou voor de meeste installaties moeten werken. U moet uw installatie instellen om HTTPS te gebruiken. Zie voor meer informatie [SSL configureren om de Business Central Web Client-verbinding te beveiligen](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Als u uw server instelt om een andere startpagina te hebben, kunt u altijd de URL wijzigen. Het clientgeheim wordt opgeslagen als een versleutelde tekenreeks in uw database. 

### <a name="prerequisites"></a>Vereisten

Dataverse moet een van de volgende verificatietypen gebruiken:

* Office365 (oud)

  > [!IMPORTANT]
  > Met ingang van april 2022 wordt Office365 (oud) niet langer ondersteund. Zie voor meer informatie [Belangrijke veranderingen (afschrijvingen) die aanstaande zijn in Power Apps, Power Automate en apps voor klantbetrokkenheid](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).
* Office365 (modern, gebaseerd op OAuth2-clientgeheim)
* OAuth

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Een toepassing registreren in Azure AD voor verbinding van Business Central met Dataverse

Bij de volgende stappen wordt ervan uitgegaan dat u Azure AD gebruikt om identiteiten en toegang te beheren. Voor meer informatie over het registreren van een toepassing in Azure AD raadpleegt u [Quickstart: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app). 

1. Kies in de Azure Portal onder **Beheren** in het navigatiedeelvenster **Verificatie**.  
2. Voeg onder **URL's omleiden** de omleidings-URL toe die wordt voorgesteld op de pagina **Dataverse-verbinding instellen** in [!INCLUDE[prod_short](includes/prod_short.md)].
3. Kies **Beheren** **API-machtigingen**.
4. Kies onder **Geconfigureerde machtigingen** **Een machtiging toevoegen** en voeg daarna als volgt gedelegeerde machtigingen toe aan het tabblad **Microsoft-API's**:
    * Voeg voor Business Central de machtiging **Financials.ReadWrite.All** toe.
    * Voeg voor Dynamics CRM de **user-impersonation**-machtigingen toe.  

    > [!NOTE]
    > De naam van de Dynamics CRM-API kan veranderen.

5. Kies onder **Beheren** **Certificaten en geheimen** en maak vervolgens een nieuw geheim voor uw app. U gebruikt het geheim in [!INCLUDE[prod_short](includes/prod_short.md)], in het veld **Clientgeheim** op de pagina **Dataverse-verbinding instellen** of slaat het op een veilige locatie op en verschaft het in een gebeurtenisabonnee zoals eerder in dit onderwerp beschreven.
6. Kies **Overzicht** en zoek de waarde **Toepassing (client)-id**. Dit is de client-id van uw toepassing. U moet het invoeren op de pagina **Dataverse-verbinding instellen** in het veld **Client-id** of bewaren op een veilige locatie en verschaffen in een gebeurtenisabonnee.
7. Voer in [!INCLUDE[prod_short](includes/prod_short.md)] op de pagina **Dataverse-verbinding instellen** in het veld **Omgeving-URL** de URL voor uw [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-omgeving in.
8. Als u de verbinding met [!INCLUDE[cds_long_md](includes/cds_long_md.md)] wilt inschakelen, zet u de schakelaar **Ingeschakeld** aan.
9. Meld u aan met uw beheerdersaccount voor Azure Active Directory (dit account moet een geldige licentie hebben voor [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en een beheerder zijn in uw [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-omgeving). Nadat u zich hebt aangemeld, wordt u gevraagd toe te staan dat uw geregistreerde toepassing zich aanmeldt bij [!INCLUDE[cds_long_md](includes/cds_long_md.md)] namens de organisatie. U moet toestemming geven om de instelling te voltooien.

   > [!NOTE]
   > Als u niet wordt gevraagd om u aan te melden met uw beheerdersaccount, komt dit waarschijnlijk omdat pop-ups worden geblokkeerd. Sta pop-ups vanaf `https://login.microsoftonline.com` toe om u aan te melden.

### <a name="to-disconnect-from-cds_long_md"></a>Verbinding met [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verbreken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dataverse-verbinding instellen** in en kies vervolgens de gerelateerde koppeling.
2. Schakel op de pagina **Dataverse-verbinding instellen** de schakelaar **Geactiveerd** uit.  

## <a name="see-also"></a>Zie ook

[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
