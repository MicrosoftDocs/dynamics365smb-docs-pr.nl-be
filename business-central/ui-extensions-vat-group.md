---
title: De extensie Btw-groepsbeheer voor het Verenigd Koninkrijk
description: U kunt samen met andere bedrijven een btw-groep vormen waarbij alle leden btw in één aangifte aangeven.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841932"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>De extensie Btw-groepsbeheer voor het Verenigd Koninkrijk

U kunt zich bij een of meer bedrijven in uw land/regio aansluiten om de btw-aangifte onder één btw-nummer te combineren. Dit type arrangement staat bekend als een *btw-groep*. U kunt zich met de groep bezighouden als lid of als groepsvertegenwoordiger.

## <a name="forming-a-vat-group"></a>Een btw-groep vormen
Btw-groepsleden en de groepsvertegenwoordiger kunnen de begeleide instelling **Btw-groepsbeheer instellen** gebruiken om hun betrokkenheid bij de groep te definiëren en een verbinding tot stand te brengen tussen hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenants. De groepsleden gebruiken de verbinding om hun btw-aangifte in te dienen bij de groepsvertegenwoordiger. De vertegenwoordiger gebruikt één btw-aangifte om btw bij de belastingdienst aan te geven voor de groep. 

## <a name="license-requirements"></a>Licentievereisten
Deelnemers aan de groep moeten een licentie hebben om [!INCLUDE[prod_short](includes/prod_short.md)] te gebruiken. U kunt geen gastaccounts gebruiken in btw-groepen. 

* Om btw-aangiften te berekenen en in te dienen, moet een gebruiker een volledige Business Central-gebruiker zijn.
* Om in te loggen en basistaken uit te voeren, zoals het maken van accounts, kunt u de licentie Dynamics 365 Business Central Teamlid hebben.

## <a name="vat-group-constellations"></a>Opstellingen van de btw-groep
De communicatie vindt plaats van groepsleden naar de vertegenwoordiger. De groepsvertegenwoordiger stelt een API URL ter beschikking waarmee de leden hun btw-aangifte kunnen indienen bij de btw-groepsvertegenwoordiger. 
[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt het indienen van btw-aangiften tussen groepen voor bedrijven met behulp van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises of online, en in elke combinatie. De instelling van de communicatie is afhankelijk van de opstelling. Dit artikel beschrijft verschillende groepsopstellingen.

De volgende lijst toont de aanbevolen volgorde van de stappen om een btw-groep in te stellen:

1. Maak de nieuwe instelling in Azure Active Directory. Zie [Vereisten voor verificatie](ui-extensions-vat-group.md#requirements-for-authentication) voor meer informatie.
2. Deel de technische informatie die leden van de btw-groep en de vertegenwoordiger nodig hebben om hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenants te verbinden. Gewoonlijk beschikt de btw-groepsvertegenwoordiger over deze informatie, zoals de naam van de omgeving van de btw-groepsvertegenwoordiger waarbij de btw-groepsleden btw zullen indienen.
3. Maak gebruikers die leden van de btw-groep kunnen gebruiken wanneer ze verbinding maken met de [!INCLUDE[prod_short](includes/prod_short.md)] van de groepsvertegenwoordiger. De gebruikers moeten volledige gebruikerslicenties hebben voor [!INCLUDE[prod_short](includes/prod_short.md)].
4. Voer de begeleide instelling **Btw-groepsbeheer instellen** uit om de leden van de btw-groep te verbinden.

  De begeleide instelling vereist enige informatie van de vertegenwoordiger van de btw-groep. Zie voor meer informatie [Btw-groepsleden instellen](#set-up-vat-group-members). Noteer de **Groepslid-id** voor elk lid van de btw-groep. De vertegenwoordiger heeft deze id's nodig om de bedrijven aan de btw-groep toe te voegen.
5. Stel de extensie Btw-groepsbeheer in [!INCLUDE[prod_short](includes/prod_short.md)] van de vertegenwoordiger van de btw-groep in met de begeleide instelling **Btw-groepsbeheer instellen**. 

> [!NOTE]
> Om verbinding te maken met de btw-groepsvertegenwoordiger, hebben groepsleden een gebruikersaccount nodig met toegang tot de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. De btw-groepsvertegenwoordiger moet hiervoor ten minste één gebruiker maken, maar om veiligheidsredenen wordt aanbevolen voor elk btw-groepslid een gebruiker te maken. Zorg ervoor dat u de inloggegevens voor deze gebruikers op een veilige manier onder de leden van de btw-groep verspreidt. Dit moet een systeemgebruikersaccount zijn dat niet is gerelateerd aan een echte persoon.

## <a name="about-the-vat-group-management-setup"></a>Over de instelling van btw-groepsbeheer

De btw-groepsvertegenwoordiger stelt een API beschikbaar aan groepsleden. De leden gebruiken de API om verbinding te maken met de [!INCLUDE[prod_short](includes/prod_short.md)]-tenant en btw-aangiften in te dienen. Leden van de btw-groep zullen vaak gebruik maken van [!INCLUDE[prod_short](includes/prod_short.md)] in aparte Azure Active Directory-tenants. Daarom is er instelling nodig om verbinding te maken tussen het lid van de btw-groep en de [!INCLUDE[prod_short](includes/prod_short.md)] van de vertegenwoordiger. 
  
Leden van de btw-groep maken verbinding met de vertegenwoordiger door een webservice aan te roepen in de tenant van de vertegenwoordiger van de btw-groep. De aanroeper moet worden geverifieerd met behulp van OAuth2. Wanneer de extensie Btw-groepsbeheer is ingesteld, wordt u gevraagd om u te verifiëren bij de vertegenwoordiger van de btw-groep om een toegangstoken op te halen en op te slaan. Dit toegangstoken wordt gebruikt bij het indienen van btw-aangiften bij de btw-groepsvertegenwoordiger. 

## <a name="construct-the-api-url"></a>Construeer de API-URL
1. Kies in het Business Central-beheercentrum voor de tenant van de vertegenwoordiger het tabblad **Omgevingen**.
2. Kopieer in de sectie **Details** de **URL**.
3. Open Kladblok en plak de URL. Vervang **https://businesscentral.dynamics.com** door **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Vereisten voor verificatie 
> [!NOTE]
> Hiervoor moet u referenties opgeven voor een beheerdersaccount dat een volledige licentie heeft voor [!INCLUDE[prod_short](includes/prod_short.md)].

Wanneer de btw-groepsvertegenwoordiger gebruikmaakt van [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises, gebruiken leden van de btw-groep Azure Active Directory om gebruikers te verifiëren wanneer ze btw-aangiften indienen bij de btw-groepsvertegenwoordiger. Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises moeten leden eenmalige aanmelding configureren. Voor meer informatie zie [Azure Active Directory-verificatie met WS-Federation configureren](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Als de leden van de btw-groep ook gebruikmaken van [!INCLUDE[prod_short](includes/prod_short.md)] online, kan het btw-groepslid zich verifiëren met behulp van de aangewezen gebruikersreferenties en de eindpuntinformatie. Zie voor meer informatie [Btw-groepsleden instellen](ui-extensions-vat-group.md#set-up-vat-group-members).

Leden van de btw-groep die [!INCLUDE[prod_short](includes/prod_short.md)] on-premises hebben, moeten een app-registratie instellen in Azure Active Directory voor de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. Dankzij de appregistratie kan de [!INCLUDE[prod_short](includes/prod_short.md)] online van de btw-groepsvertegenwoordiger het groepslid verifiëren. Zie voor meer informatie [Snelle start: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app).

Wanneer u de app-registratie maakt in Azure Active Directory, moet u de volgende informatie specificeren.

* Voeg in de sectie **Verificatie** **Web** toe als platform en gebruik de volgende **omleidings-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Selecteer in de sectie **Verificatie** in de optie om **Ondersteunde accounttypen** te selecteren **Accounts in elke organisatorische directory (elke Azure AD-directory - Multitenant)**.
* Maak in de sectie **Certificaten en geheimen** een nieuw cliëntgeheim en noteer de waarde. De Btw-groepsleden hebben het geheim nodig om de verbinding met de groepsvertegenwoordiger in te stellen.
* Voeg in de sectie **API-machtigingen** machtigingen toe aan [!INCLUDE[prod_short](includes/prod_short.md)]. Schakel gedelegeerde toegang tot **Financials.ReadWrite.All** en **user_impersonation** in.
* Let in de sectie **Overzicht** op de **Toepassing (client)-id**. De Btw-groepsleden hebben de id nodig om de verbinding met de groepsvertegenwoordiger in te stellen. 

## <a name="set-up-vat-group-members"></a>Btw-groepsleden instellen
> [!IMPORTANT]
> De aangesloten bedrijven in de btw-groep hoeven geen verbinding te maken met HMRC omdat ze rapporteren via de vertegenwoordiger van de groep.

Neem voordat u begint contact op met de btw-groepsvertegenwoordiger voor de volgende informatie over hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenant:

* De API-URL
* De naam van hun bedrijf 
* Client-id
* Clientgeheim
* Inloggegevens voor de toegewezen gebruiker 

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-groepsbeheer instellen** in en kies vervolgens de gerelateerde koppeling.
2. Geef in het veld **Btw-groepsrol** op of u lid van de groep of de vertegenwoordiger van de groep bent. Kies **Lid** om als groepslid te fungeren en uw btw-aangiften bij de groepsvertegenwoordiger in te dienen in plaats van bij de belastingdienst. Kies daarna **Volgende**.
3. Kopieer de waarde van het veld **Groepslid-id** en deel deze vervolgens met de btw-groepsvertegenwoordiger zodat deze uw bedrijf kan toevoegen als een goedgekeurd lid van de groep.
4. Geef in het veld **Productversie van groepsvertegenwoordiger** de versie van [!INCLUDE[prod_short](includes/prod_short.md)] op die de vertegenwoordiger gebruikt.
5. Voer in het veld **Bedrijf van groepsvertegenwoordiger** de bedrijfsnaam in van de btw-groepsvertegenwoordiger. Bijvoorbeeld **CRONUS UK Ltd**.
6. Kies in het veld **Verificatietype** de optie **OAuth2**. Als de btw-groepsvertegenwoordiger gebruikmaakt van [!INCLUDE[prod_short](includes/prod_short.md)] online, specificeert u **Groepsvertegenwoordiger gebruikt Business Central Online** en kies dan **Volgende**. Afhankelijk van of de vertegenwoordiger [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises gebruikt, volgt u de stappen in de sectie [Btw-groepsvertegenwoordiger gebruikt Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) of [Btw-groepsvertegenwoordiger gebruikt Business Central On-Premises](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>Btw-groepsvertegenwoordiger gebruikt Business Central Online
1. Voer de gebruikersgegevens in die zijn verstrekt door de btw-groepsvertegenwoordiger en voeg de vereiste machtigingen toe.
2. Kies de btw-aangifteconfiguratie die momenteel wordt gebruikt om btw-aangiften in te dienen bij de belastingdienst. Nadat u de installatie hebt voltooid, maakt [!INCLUDE[prod_short](includes/prod_short.md)] op basis van deze keuze een nieuwe configuratie en gebruikt de configuratie om btw-aangiften in te dienen bij de btw-groepsvertegenwoordiger.  
3. Voeg de **API-URL** van de btw-groepsvertegenwoordiger toe. De URL is doorgaans als volgt opgemaakt: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Bijvoorbeeld: `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>Btw-groepsvertegenwoordiger gebruikt Business Central On-Premises
1. Voer in het veld **Client-id** de client-id van de appregistratie in Azure Active Directory in.
2. Voer in het veld **Clientgeheim** het clientgeheim van de appregistratie in Azure Active Directory in.
3. Voer in het veld **OAuth 2.0-autoriteitseindpunt** `https://login.microsoftonline.com/common/oauth2` in.
4. Voer in het veld **OAuth 2.0-resource-URL** `https://api.businesscentral.dynamics.com/` in.
5. Voer in het veld **OAuth 2.0-omleidings-URL** `https://businesscentral.dynamics.com/OAuthLanding.htm` in.
6. Kies als u de verschillende velden hebt gespecificeerd **Volgende** en voer vervolgens de gebruikersreferenties in die zijn verstrekt door de btw-groepsvertegenwoordiger.
7. Kies de btw-rapportconfiguratie die u gebruikt om btw te rapporteren aan de autoriteiten in uw land/regio.

## <a name="set-up-the-vat-group-representative"></a>De btw-groepsvertegenwoordiger instellen
> [!NOTE]
> Voor on-premises ondersteunen we slechts één tenantinstantie van de groepsvertegenwoordiger.

> [!IMPORTANT]
> Het vertegenwoordigende bedrijf moet de serviceverbinding **HMRC btw-instelling** inschakelen op de pagina **Serviceverbindingen**. Vertegenwoordigers moeten ook btw-aangifteperiodes downloaden van HMRC.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-groepsbeheer instellen** in en kies vervolgens de gerelateerde koppeling.
2. Geef in het veld **Btw-groepsrol** op of u lid van de groep of de vertegenwoordiger van de groep bent. Kies **Vertegenwoordiger** om als btw-groepsvertegenwoordiger te fungeren en uw btw-aangiften bij de belastingdienst in te dienen voor de groep. Kies daarna **Volgende**.
3. Geef in het veld **Btw-vereffeningsrekening** de rekening op die u gebruikt voor btw-verrekeningen.
4. Geef in het veld **Vaknr. te betalen btw** het vak op dat het totale verschuldigde btw-bedrag vertegenwoordigt van een groepsindiening van btw.
5. Geef in het veld **Fin. dagboeksjabloon voor groepsvereffening** de dagboeksjabloon op die voor het document wordt gebruikt om de groeps-btw op de vereffeningsrekening te boeken.
6. Het veld **Goedgekeurde leden** toont het aantal groepsleden dat is ingesteld om btw-aangiften in te dienen bij de vertegenwoordiger. Als u nieuwe leden wilt toevoegen, kiest u het nummer om de pagina **Goedgekeurde leden** te openen.
7. Om nieuwe leden toe te voegen voegt u de volgende informatie toe aan de pagina **Goedgekeurde leden van btw-groep**:
    1. Voer in het veld **Groepslid-id** een id in voor het groepslid.
    2. Geef in het veld **Groepslidnaam** de naam van het groepslid op. 
    3. Geef in het veld **Bedrijf** het bedrijf op van waaruit het groepslid btw-aangiften zal doen in [!INCLUDE[prod_short](includes/prod_short.md)]. Bijvoorbeeld **CRONUS UK Ltd**.
    4. Contactdetails voor het bedrijf opgeven.

## <a name="use-the-vat-group-management-features"></a>De beheerfuncties van btw-groepsbeheer gebruiken
Leden van de btw-groep gebruiken de standaardprocessen om btw-aangiften voor te bereiden. Het enige verschil is de rapportversie **BTWGROEP** te kiezen, die de btw-aangifte indient bij de btw-groepsvertegenwoordiger, in plaats van bij de autoriteiten. Zie [Informatie over het rapport Btw-aangifte](finance-how-report-vat.md#vatreturn) voor meer informatie.

In de volgende secties worden de taken beschreven die vertegenwoordigers van btw-groepen moeten uitvoeren.

### <a name="vat-group-submissions"></a>Btw-groepsindieningen

De pagina **Btw-groepsindieningen** geeft een overzicht van de btw-aangiften die leden hebben ingediend. De pagina dient als conceptlocatie voor de indieningen totdat de btw-groepsvertegenwoordiger ze opneemt in een btw-aangifte voor de groep. U kunt de indieningen openen om de btw te bekijken voor de individuele vakken die door het lid van de btw-groep is opgegeven. 

> [!TIP]
> Op de pagina **Btw-aangifteperioden** bevat het veld **Indieningen van groepsleden** hoeveel aangiften leden hebben ingediend. Om ervoor te zorgen dat dit getal up-to-date is, kiest u de actie **Btw-aangifteperioden ophalen**.

### <a name="creating-a-group-vat-return"></a>Een groeps-btw-aangifte maken

Om voor de groep btw te rapporteren maakt u op de pagina **Btw-aangiften** een btw-aangifte alleen voor uw bedrijf. Voeg daarna de meest recente btw-aangiften van leden van de btw-groep toe door de actie **Groeps-btw opnemen** te kiezen.  

Wanneer de btw-aangifte van de btw-groepsvertegenwoordiger namens de hele groep bij de autoriteiten is ingediend, voert u normaal gesproken de actie **Btw-vereffening berekenen en boeken** uit. Met deze actie worden openstaande btw-posten en -overdrachtsbedragen naar de btw-vereffeningsrekening gesloten. Deze actie houdt momenteel geen rekening met de groepsindieningen. <!--Has this changed?--> Alleen de btw-posten van het bedrijf van de btw-groepsvertegenwoordiger worden geboekt. De bedragen voor de indiening van btw-groepsleden moeten handmatig naar het btw-vereffeningsbedrag worden geboekt, zodat de btw-vereffeningsrekening van de btw-groepsvertegenwoordiger de aansprakelijkheid weergeeft van wat aan de autoriteiten is gerapporteerd. Dit gedrag zal veranderen in een aanstaande update van [!INCLUDE[prod_short](includes/prod_short.md)], zodat de volledige groeps-btw (het totale bedrag op rapportregels in de btw-aangifte) zal worden vereffend. <!--Has this behavior changed?-->

> [!NOTE]
> Leden van de btw-groep kunnen ingediende btw-aangiften corrigeren zolang de groepsvertegenwoordiger de btw-aangifte voor de groep niet heeft vrijgegeven. Om een correctie door te voeren moet het btw-groepslid een nieuwe btw-aangifte voor de btw-aangifteperiode maken en deze indienen bij de btw-groepsvertegenwoordiger. Aan de kant van de btw-groepsvertegenwoordiger wordt de laatste btw-aangifte opgenomen op de pagina **Btw-aangiften**. 

> [!IMPORTANT]
> De btw-groepsfunctionaliteit wordt alleen ondersteund in markten waar [!INCLUDE[prod_short](includes/prod_short.md)] een btw-raamwerk gebruikt dat bestaat uit btw-aangiften en btw-aangifteperioden. U kunt geen btw-groepen gebruiken in andere markten die andere implementaties van lokale btw-rapportage hebben, zoals Oostenrijk, Duitsland, Italië, Spanje en Zwitserland. 

## <a name="see-also"></a>Zie ook
[Lokale functionaliteit van het Verenigd Koninkrijk in de Britse versie](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Belasting digitaal maken in het Verenigd Koninkrijk](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Btw instellen](finance-setup-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
