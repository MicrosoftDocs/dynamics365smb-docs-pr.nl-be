---
title: De extensie Btw-groepsbeheer
description: U kunt met andere bedrijven samenwerken om een btw-groep te vormen en optreden als lid of vertegenwoordiger van de groep bij het aangeven van btw.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 7148fa8e59a509af3206e7da898a371ffb5332a5
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029152"
---
# <a name="the-vat-group-management-extension"></a>De extensie Btw-groepsbeheer

U kunt zich bij een of meer bedrijven in uw land/regio aansluiten om de btw-aangifte onder één btw-nummer te consolideren. Dit type arrangement staat bekend als een *btw-groep*. U kunt zich met de groep bezighouden als lid of als groepsvertegenwoordiger.

## <a name="forming-a-vat-group"></a>Een btw-groep vormen
Btw-groepsleden en de groepsvertegenwoordiger kunnen de begeleide instelling **Btw-groepsbeheer instellen** gebruiken om hun betrokkenheid bij de groep te definiëren en een verbinding tot stand te brengen tussen hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenants. De groepsleden gebruiken de verbinding om hun btw-aangifte in te dienen bij de groepsvertegenwoordiger. De vertegenwoordiger dient namens de groep de btw in bij de belastingdienst door middel van één btw-aangifte. 

## <a name="vat-group-constellations"></a>Opstellingen van de btw-groep
De communicatie vindt plaats van groepsleden naar de vertegenwoordiger. De groepsvertegenwoordiger stelt een API ter beschikking waarmee de leden hun btw-aangifte kunnen indienen bij de btw-groepsvertegenwoordiger. 
[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt het indienen van btw-aangiften tussen groepen voor bedrijven met behulp van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises of online, en in elke combinatie. De instelling van de communicatie is afhankelijk van de opstelling. In de volgende secties wordt beschreven hoe u verschillende groepsopstellingen instelt.

De volgende lijst toont de aanbevolen volgorde van de stappen om een btw-groep in te stellen:

1. Maak de nieuwe instelling in Azure Active Directory. Zie [Vereisten voor verificatie](ui-extensions-vat-group.md#requirements-for-authentication) voor meer informatie.
2. Deel de technische informatie die leden van de btw-groep en de vertegenwoordiger nodig hebben om hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenants te verbinden. Gewoonlijk beschikt de btw-groepsvertegenwoordiger over deze informatie, zoals de naam van de omgeving van de btw-groepsvertegenwoordiger waarbij de btw-groepsleden btw zullen indienen.
3. Maak gebruikers in de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger die leden van de btw-groep kunnen gebruiken om te verifiëren en verbinding te maken.
4. Voer de begeleide instelling **Btw-groepsbeheer instellen** uit om de leden van de btw-groep te verbinden.

  De begeleide instelling vereist enige informatie van de vertegenwoordiger van de btw-groep. Zie voor meer informatie de sectie [Btw-groepslid instellen](#vat-group-member-setup). Noteer de **Groepslid-id** voor elk lid van de btw-groep. De vertegenwoordiger heeft deze id's nodig om de bedrijven aan de btw-groep toe te voegen.
5. Stel de extensie Btw-groepsbeheer in [!INCLUDE[prod_short](includes/prod_short.md)] van de vertegenwoordiger van de btw-groep in met de begeleide instelling **Btw-groepsbeheer instellen**. 

> [!NOTE]
> Om verbinding te maken met de btw-groepsvertegenwoordiger, hebben groepsleden een gebruiker nodig met toegang tot de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. De btw-groepsvertegenwoordiger moet hiervoor ten minste één gebruiker maken, maar om veiligheidsredenen wordt aanbevolen voor elk btw-groepslid een gebruiker te maken. Zorg ervoor dat u de inloggegevens voor deze gebruikers op een veilige manier onder de leden van de btw-groep verspreidt.

## <a name="understanding-the-vat-group-management-setup"></a>Inzicht in de instelling van Btw-groepsbeheer

De btw-groepsvertegenwoordiger stelt een API beschikbaar die leden van de btw-groep kunnen gebruiken om verbinding te maken met hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenant en btw-aangiften in te dienen. Leden van de btw-groep zullen vaak gebruik maken van [!INCLUDE[prod_short](includes/prod_short.md)] in aparte Azure Active Directory-tenants. Daarom zijn er meer instellingen nodig om een verbinding te maken tussen het lid van de btw-groep en de [!INCLUDE[prod_short](includes/prod_short.md)] van de vertegenwoordiger. 
  
Leden van de btw-groep maken verbinding met de vertegenwoordiger door een webservice aan te roepen in de tenant van de vertegenwoordiger van de btw-groep. De aanroeper moet worden geverifieerd met behulp van OAuth. Wanneer de extensie Btw-groepsbeheer is ingesteld, wordt u gevraagd om u te verifiëren bij de vertegenwoordiger van de btw-groep om een toegangstoken op te halen en op te slaan. Dit toegangstoken wordt gebruikt bij het indienen van btw-aangiften bij de btw-groepsvertegenwoordiger. 

Verificatie wordt afgehandeld door Azure Active Directory, dus uw instelling moet worden uitgevoerd in de Azure Active Directory van de btw-groepsvertegenwoordiger om verbindingen toe te staan. Een Azure Active Directory-appregistratie moet worden geconfigureerd met toegang tot de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. Dit geldt ook als de btw-groepsvertegenwoordiger gebruik maakt van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises. Bovendien moet u Single Sign-On configureren als de btw-groepsvertegenwoordiger gebruikmaakt van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises.

> [!NOTE]
> Gedurende een beperkte tijd wordt verificatie met een webservicetoegangssleutel ook ondersteund. Zie voor meer informatie [Verouderde functies in releasewave 1 van 2021](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Vereisten voor verificatie 
Wanneer de btw-groepsvertegenwoordiger gebruikmaakt van [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises, gebruiken leden van de btw-groep Azure Active Directory om zich te verifiëren wanneer ze btw-aangiften indienen bij de btw-groepsvertegenwoordiger. Als de leden van de btw-groep ook gebruikmaken van [!INCLUDE[prod_short](includes/prod_short.md)] online, kan het btw-groepslid zich verifiëren met behulp van de aangewezen gebruikersreferenties en de eindpuntinformatie. Zie voor meer informatie [Btw-groepslid instellen](ui-extensions-vat-group.md#vat-group-member-setup).

Leden van de btw-groep die [!INCLUDE[prod_short](includes/prod_short.md)] on-premises hebben, moeten een app-registratie instellen in Azure Active Directory voor de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. De appregistratie zal de [!INCLUDE[prod_short](includes/prod_short.md)] online van de btw-groepsvertegenwoordiger inschakelen voor verificatie van het groepslid. Zie voor meer informatie [Snelle start: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app).

Wanneer u de app-registratie maakt in Azure Active Directory, moet u het volgende specificeren.

* Voeg in de sectie **Verificatie** **Web** toe als platform en gebruik de volgende **omleidings-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Selecteer in de sectie **Verificatie** in de optie om **Ondersteunde accounttypen** te selecteren **Accounts in elke organisatorische directory (elke Azure AD-directory - Multitenant)**.
* Maak in de sectie **Certificaten en geheimen** een nieuw cliëntgeheim en noteer de waarde. De Btw-groepsleden hebben het geheim nodig om de verbinding met de groepsvertegenwoordiger in te stellen.
* Voeg in de sectie **API-machtigingen** machtigingen toe aan [!INCLUDE[prod_short](includes/prod_short.md)]. Schakel gedelegeerde toegang tot **Financials.ReadWrite.All** en **user_impersonation** in.
* Let in de sectie **Overzicht** op de **Toepassing (client)-id**. De Btw-groepsleden hebben de id nodig om de verbinding met de groepsvertegenwoordiger in te stellen. 

## <a name="vat-group-member-setup"></a>Btw-groepslid instellen
Stel het btw-groepslid in door de begeleide instelling **Btw-groepsbeheer instellen** te starten. 

> [!NOTE]
> Neem voordat u begint contact op met de btw-groepsvertegenwoordiger voor de volgende informatie over hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenant:
>
> * De API-URL
> * De naam van hun bedrijf 
> * Client-id
> * Clientgeheim
> * Inloggegevens voor de toegewezen gebruiker 

1. Als u de btw-groepsrol van het bedrijf wilt definiëren, kiest u **Lid** en kiest u vervolgens **Volgende**.
2. Kopieer de waarde van het veld **Groepslid-id** en deel deze vervolgens met de btw-groepsvertegenwoordiger zodat deze uw bedrijf kan toevoegen als een goedgekeurd lid van de groep.
3. Voeg de **API-URL** van de btw-groepsvertegenwoordiger toe. De URL is doorgaans als volgt opgemaakt: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Bijvoorbeeld: `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
4. Voeg de [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijfsnaam van de btw-groepsvertegenwoordiger toe, bijvoorbeeld *CRONUS UK Ltd*.
5. Kies **Verificatietype**, kies **OAuth2** en kies vervolgens **Volgende**.
6. Voer in het veld **Client-id** de id in die is verstrekt door de btw-groepsvertegenwoordiger.
7. Voer in het veld **Clientgeheim verstrekt door de btw-groepsvertegenwoordiger** het geheim in dat door de btw-groepsvertegenwoordiger is verstrekt.
8. Voer in het veld **OAuth 2.0-autoriteitseindpunt** *https://login.microsoftonline.com/common/oauth2* in.
9. Voer in het veld **OAuth 2.0-resource-URL** *https://api.businesscentral.dynamics.com/* in.
10. Voer in het veld **OAuth 2.0-omleidings-URL** *https://businesscentral.dynamics.com/OAuthLanding.htm* in. 
11. Kies als u de verschillende velden hebt gespecificeerd **Volgende** en voer vervolgens de gebruikersreferenties in die zijn verstrekt door de btw-groepsvertegenwoordiger.
12. Kies de btw-rapportconfiguratie die u gebruikt om btw te rapporteren aan de autoriteiten in uw land/regio.

  In het Verenigd Koninkrijk zou de btw-rapportconfiguratie bijvoorbeeld worden ingesteld om btw aan HMRC te rapporteren. De extensie Btw-groepsbeheer kopieert deze instelling, maar vervangt de indieningscodeunit door een codeunit die indiening bij de btw-groepsvertegenwoordiger ondersteunt, in plaats van bij de belastingdienst. De codeunit wordt geleverd door Microsoft. Kies **Volgende** wanneer u klaar bent.

## <a name="using-the-vat-group-management-features"></a>De beheerfuncties van btw-groepsbeheer gebruiken

Leden van de btw-groep gebruiken de standaardprocessen om btw-aangiften voor te bereiden. Het enige verschil is de rapportversie **BTWGROEP** te kiezen, die de btw-aangifte indient bij de btw-groepsvertegenwoordiger, in plaats van bij de autoriteiten. Zie voor meer informatie [Over het rapport Btw-aangifte](finance-how-report-vat.md#about-the-vat-return-report).

In de volgende secties worden de taken beschreven die vertegenwoordigers van btw-groepen moeten uitvoeren.

### <a name="vat-group-submissions"></a>Btw-groepsindieningen

De pagina **Btw-groepsindieningen** geeft een overzicht van de btw-aangiften die leden hebben ingediend. De pagina dient als conceptlocatie voor de indieningen totdat de btw-groepsvertegenwoordiger ze opneemt in een btw-aangifte voor de groep. U kunt de indieningen openen om de btw te bekijken voor de individuele vakken die door het lid van de btw-groep is opgegeven.

### <a name="creating-a-group-vat-return"></a>Een groeps-btw-aangifte maken

Om namens de groep btw te rapporteren maakt u op de pagina **Btw-aangiften** een btw-aangifte alleen voor uw bedrijf. Voeg daarna de meest recente btw-aangiften van leden van de btw-groep toe door de actie **Groeps-btw opnemen** te kiezen.  

Wanneer de btw-aangifte van de btw-groepsvertegenwoordiger namens de hele groep bij de autoriteiten is ingediend, voert u normaal gesproken de actie **Btw-vereffening berekenen en boeken** uit. Met deze actie worden openstaande btw-posten en -overdrachtsbedragen naar de btw-vereffeningsrekening gesloten. Deze actie houdt geen rekening met de groepsindieningen. Dit betekent dat alleen de btw-posten van het bedrijf van de btw-groepsvertegenwoordiger worden geboekt. De bedragen voor de indiening van btw-groepsleden moeten handmatig naar het btw-vereffeningsbedrag worden geboekt, zodat de btw-vereffeningsrekening van de btw-groepsvertegenwoordiger de aansprakelijkheid weergeeft van wat aan de autoriteiten is gerapporteerd. Dit gedrag zal veranderen in een aanstaande update van [!INCLUDE[prod_short](includes/prod_short.md)], dus de volledige groeps-btw (het totale bedrag op rapportregels in de btw-aangifte) wordt vereffend. 

> [!NOTE]
> Leden van de btw-groep kunnen ingediende btw-aangiften corrigeren zolang de groepsvertegenwoordiger de btw-aangifte voor de groep niet heeft vrijgegeven. Om een correctie door te voeren moet het btw-groepslid een nieuwe btw-aangifte voor de btw-aangifteperiode maken en deze indienen bij de btw-groepsvertegenwoordiger. Aan de kant van de btw-groepsvertegenwoordiger wordt de laatste btw-aangifte opgenomen op de pagina **Btw-aangiften**. 

> [!IMPORTANT]
> De btw-groepsfunctionaliteit wordt alleen ondersteund in markten waar [!INCLUDE[prod_short](includes/prod_short.md)] een btw-raamwerk gebruikt dat bestaat uit btw-aangiften en btw-aangifteperioden. U kunt geen btw-groepen gebruiken in andere markten die andere implementaties van lokale btw-rapportage hebben, zoals Oostenrijk, Duitsland, Italië, Spanje en Zwitserland. 

## <a name="see-also"></a>Zie ook

[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Btw instellen](finance-setup-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Belasting digitaal maken in het Verenigd Koninkrijk](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Noorse btw-aangifte in de Noorse versie](LocalFunctionality/Norway/norwegian-vat-reporting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
