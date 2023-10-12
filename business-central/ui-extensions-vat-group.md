---
title: De extensie Btw-groepsbeheer voor het Verenigd Koninkrijk
description: U kunt samen met andere bedrijven een btw-groep vormen waarbij alle leden btw in één aangifte aangeven.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: soalex
ms.topic: conceptual
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 09/18/2023
---

# De extensie Btw-groepsbeheer voor het Verenigd Koninkrijk

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

U kunt een of meer bedrijven in het Verenigd Koninkrijk verbinden om btw-aangifte te combineren onder één btw-nummer. Dit type arrangement staat bekend als een *btw-groep*. U kunt zich met de groep bezighouden als lid of als de groepsvertegenwoordiger.

## Een btw-groep vormen

Btw-groepsleden en de groepsvertegenwoordiger kunnen de begeleide instelling **Btw-groepsbeheer instellen** gebruiken om hun betrokkenheid bij de groep te definiëren en een verbinding tot stand te brengen tussen hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenants. De groepsleden gebruiken deze verbinding om hun btw-aangifte in te dienen bij de groepsvertegenwoordiger. De groepsvertegenwoordiger gebruikt vervolgens één btw-aangifte om btw van de groep bij de belastingdienst aan te geven.

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt intra-groep btw-aangiftes voor bedrijven die gebruikmaken van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises of online, in welke combinatie dan ook, wat de communicatie-instelling tussen bedrijven beïnvloedt. Dit artikel beschrijft verschillende groepsinstellingen.

### Licentievereisten

Deelnemers aan de groep moeten een licentie hebben om [!INCLUDE[prod_short](includes/prod_short.md)] te gebruiken. U kunt geen gastaccounts gebruiken in btw-groepen.

* Om btw-aangiften te berekenen en in te dienen, moet een gebruiker een volledige [!INCLUDE[prod_short](includes/prod_short.md)]-gebruiker zijn.
* Om in te loggen en basistaken uit te voeren, zoals het maken van accounts, hebt u de licentie [!INCLUDE[prod_long](includes/prod_long.md)] Teamlid nodig.

## Een btw-groep instellen

De volgende lijst toont de aanbevolen volgorde van de stappen die een beheerder gebruikt om een btw-groep in te stellen:

1. Maak de instelling in [Microsoft Entra ID voor groepsleden](#microsoft-entra-id-setup-for-group-members).
2. Deel de technische informatie die leden van de btw-groep en de groepsvertegenwoordiger nodig hebben om hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenants te verbinden. Gewoonlijk beschikt de groepsvertegenwoordiger over deze informatie, zoals de [API-URL](#group-api-setup) en de naam van de omgeving van de btw-groepsvertegenwoordiger waarbij de btw-groepsleden hun btw-gegevens indienen.
3. Maak gebruikers die leden van de btw-groep zullen gebruiken wanneer ze verbinding maken met de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. De gebruikers moeten volledige gebruikerslicenties hebben voor [!INCLUDE[prod_short](includes/prod_short.md)].
4. Voer de begeleide instelling **Btw-groepsbeheer instellen** uit om de leden van de btw-groep te verbinden.

   De vertegenwoordiger van de btw-groep moet bepaalde informatie verstrekken aan groepsleden om hun configuratie te voltooien. (U vindt meer informatie in de sectie [Btw-groepsleden instellen](#set-up-vat-group-members), hieronder.) Maak een notitie van de **Groepslid-id** voor elk btw-groepslid. De groepsvertegenwoordiger heeft deze id's nodig om de bedrijven aan de btw-groep toe te voegen.
5. Stel de extensie Btw-groepsbeheer in [!INCLUDE[prod_short](includes/prod_short.md)] van de vertegenwoordiger van de btw-groep in met de begeleide instelling **Btw-groepsbeheer instellen**.

> [!NOTE]
> Om verbinding te maken met de btw-groepsvertegenwoordiger, hebben groepsleden een gebruikersaccount nodig met toegang tot de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. De btw-groepsvertegenwoordiger moet hiervoor minimaal één gebruiker maken. Om veiligheidsredenen raden we echter aan om voor elk lid van de btw-groep een gebruiker te maken, wat een systeemgebruikersaccount kan zijn die niet is gerelateerd aan een echte persoon. Zorg ervoor dat u de gebruikersgegevens op een veilige manier onder de leden van de btw-groep verspreidt.

### Microsoft Entra ID instellen voor groepsleden

Wanneer de btw-groepsvertegenwoordiger gebruikmaakt van [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises, gebruiken leden van de btw-groep Microsoft Entra ID om gebruikers te verifiëren wanneer ze btw-aangiften indienen bij de btw-groepsvertegenwoordiger. Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises moeten leden eenmalige aanmelding configureren. Zie voor meer informatie [Microsoft Entra-verificatie met WS-Federation configureren](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Als de leden van de btw-groep ook gebruikmaken van [!INCLUDE[prod_short](includes/prod_short.md)] online, kan het lid zich verifiëren met behulp van de aangewezen gebruikersgegevens en de aanmeldgegevens die worden verschaft door de groepsvertegenwoordiger. Lees meer in de sectie [Btw-groepsleden instellen](#set-up-vat-group-members), hieronder.

Leden van de btw-groep die [!INCLUDE[prod_short](includes/prod_short.md)] on-premises hebben, moeten een app-registratie instellen in Microsoft Entra ID voor de [!INCLUDE[prod_short](includes/prod_short.md)] van de btw-groepsvertegenwoordiger. Dankzij de appregistratie kan de [!INCLUDE[prod_short](includes/prod_short.md)] online van de btw-groepsvertegenwoordiger het groepslid verifiëren. Zie voor meer informatie [Snelle start: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app).

Wanneer de beheerder van het btw-groepslid de app-registratie maakt in Microsoft Entra ID, moeten ze de volgende informatie opgeven.

* Voeg in de sectie **Verificatie** **Web** toe als platform en gebruik de volgende **omleidings-URL**: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* Selecteer in de sectie **Verificatie** in de optie om **Ondersteunde accounttypen** te selecteren **Accounts in elke organisatorische directory (elke Microsoft Entra-directory - Multitenant)**.
* Maak in de sectie **Certificaten en geheimen** een nieuw cliëntgeheim en noteer de waarde. De Btw-groepsleden hebben het geheim nodig om de verbinding met de groepsvertegenwoordiger in te stellen.
* Voeg in de sectie **API-machtigingen** machtigingen toe aan [!INCLUDE[prod_short](includes/prod_short.md)]. Schakel gedelegeerde toegang tot **Financials.ReadWrite.All** en **user_impersonation** in.
* Let in de sectie **Overzicht** op de **Toepassing (client)-id**. De Btw-groepsleden hebben de id nodig om de verbinding met de groepsvertegenwoordiger in te stellen.

### Groeps-API instellen

De btw-groepsvertegenwoordiger maakt een API en stelt deze beschikbaar aan groepsleden. De leden gebruiken deze API om verbinding te maken met de [!INCLUDE[prod_short](includes/prod_short.md)]-tenant en btw-aangiften in te dienen. Leden van de btw-groep zullen vaak gebruik maken van [!INCLUDE[prod_short](includes/prod_short.md)] in aparte Microsoft Entra-tenants. Daarom is er instelling nodig om verbinding te maken tussen het lid van de btw-groep en de [!INCLUDE[prod_short](includes/prod_short.md)] van de vertegenwoordiger.

> [!NOTE]
> Voor deze instelling moet u referenties opgeven voor een beheerdersaccount dat een volledige gebruikerslicentie heeft voor [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies in het Business Central-beheercentrum voor de tenant van de vertegenwoordiger het tabblad **Omgevingen**.
1. Kies de omgeving van de vertegenwoordiger.
1. Kopieer in de sectie **Details** de **URL**.
1. Open Kladblok en plak de URL. Vervang `https://businesscentral.dynamics.com` door `https://api.businesscentral.dynamics.com/v2.0`.

## Btw-groepsleden instellen

Leden van de btw-groep maken verbinding met de vertegenwoordiger door een webservice aan te roepen in de tenant van de vertegenwoordiger van de btw-groep. De aanroeper moet worden geverifieerd met behulp van OAuth2. Wanneer de extensie Btw-groepsbeheer is ingesteld, wordt leden gevraagd zich te verifiëren bij de vertegenwoordiger van de btw-groep. Er wordt dan een toegangstoken gegenereerd en opgeslagen. Dit toegangstoken wordt gebruikt bij het indienen van btw-aangiften bij de btw-groepsvertegenwoordiger.

> [!IMPORTANT]
> De aangesloten bedrijven in de btw-groep hoeven geen verbinding te maken met HMRC omdat ze rapporteren via de vertegenwoordiger van de groep.

Voordat leden van de btw-groep hun instelling starten (hieronder vermeld), moeten ze contact opnemen met de vertegenwoordiger van de btw-groep voor de volgende informatie over hun [!INCLUDE[prod_short](includes/prod_short.md)]-tenant:

* De API-URL
* De naam van hun bedrijf
* Inloggegevens voor de toegewezen gebruiker

1. Kies in de rechterbovenhoek het pictogram **Instellingen** ![Instellingen](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") en kies dan de actie **Begeleide instelling**.
2. Kies de actie **Btw-groepsbeheer instellen**.
3. Kies in het veld **Btw-groepsrol** **Lid** en dan **Volgende**.
4. Kopieer de waarde van het veld **Groepslid-id** en deel deze vervolgens met de btw-groepsvertegenwoordiger zodat deze uw bedrijf kan toevoegen als een goedgekeurd lid van de groep.
5. Geef in het veld **Productversie van groepsvertegenwoordiger** de versie van [!INCLUDE[prod_short](includes/prod_short.md)] op die de vertegenwoordiger gebruikt.
6. Voer in het veld **API-URL** de API-URL in die is verstrekt door de btw-groepsvertegenwoordiger. De URL is doorgaans als volgt opgemaakt: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Bijvoorbeeld: `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. Voer in het veld **Bedrijf van groepsvertegenwoordiger** de bedrijfsnaam in van de btw-groepsvertegenwoordiger, bijvoorbeeld **CRONUS UK Ltd**.
8. Kies in het veld **Verificatietype** de optie **OAuth2**. Als de btw-groepsvertegenwoordiger gebruikmaakt van [!INCLUDE[prod_short](includes/prod_short.md)] online, schakelt u **Groepsvertegenwoordiger gebruikt Business Central Online** in en kiest u **Volgende**.

   Volg daarna de stappen in ofwel de sectie [Btw-groepsvertegenwoordiger gebruikt Business Central online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) of [Btw-groepsvertegenwoordiger gebruikt Business Central on-premises](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises), hieronder.

### Btw-groepsvertegenwoordiger gebruikt Business Central online

1. Voer de gebruikersgegevens in die zijn verstrekt door de btw-groepsvertegenwoordiger en voeg de vereiste machtigingen toe om het toegangstoken te genereren.
2. Kies de btw-aangifteconfiguratie die u gebruikt om btw-aangiften in te dienen bij de belastingdienst van het Verenigd Koninkrijk. 

Nadat u de installatie hebt voltooid, maakt [!INCLUDE[prod_short](includes/prod_short.md)] op basis van deze keuze een nieuwe configuratie zodat u btw-aangiften kunt indienen bij de btw-groepsvertegenwoordiger.

### Btw-groepsvertegenwoordiger gebruikt Business Central on-premises

1. Voer de gebruikersgegevens in die zijn verstrekt door de vertegenwoordiger van de btw-groep en kies **Volgende**.
2. Voer in het veld **Client-id** de client-id van de appregistratie in [Microsoft Entra ID instellen voor groepsleden](#microsoft-entra-id-setup-for-group-members) in.
3. Voer in het veld **Clientgeheim** het clientgeheim van de appregistratie in Microsoft Entra ID in.
4. Voer in het veld **OAuth 2.0-autoriteitseindpunt** `https://login.microsoftonline.com/common/oauth2` in.
5. Voer in het veld **OAuth 2.0-resource-URL** `https://api.businesscentral.dynamics.com/` in.
6. Voer in het veld **OAuth 2.0-omleidings-URL** `https://businesscentral.dynamics.com/OAuthLanding.htm` in.
7. Als u de verschillende velden hebt opgegeven, kiest u **Volgende** en bevestigt u vervolgens de verificatieverbinding om het toegangstoken te genereren.
8. Kies de btw-aangifteconfiguratie die u gebruikt om btw-aangiften in te dienen bij de belastingdienst van het Verenigd Koninkrijk.

## De btw-groepsvertegenwoordiger instellen

> [!NOTE]
> Voor on-premises ondersteunt [!INCLUDE[prod_short](includes/prod_short.md)] slechts één tenantinstantie van de groepsvertegenwoordiger.

> [!IMPORTANT]
> Het vertegenwoordigende bedrijf moet de serviceverbinding **HMRC btw-instelling** inschakelen op de pagina **Serviceverbindingen**. Vertegenwoordigers moeten ook btw-aangifteperiodes downloaden van HMRC.

1. Kies in de rechterbovenhoek het pictogram **Instellingen** ![Instellingen](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") en kies vervolgens de actie **Begeleide instelling**.
2. Kies de actie **Btw-groepsbeheer instellen**.
3. Kies in het veld **Btw-groepsrol** **Vertegenwoordiger** om op te treden als vertegenwoordiger van de btw-groep en kies dan **Volgende**.
4. Geef in het veld **Groepsvereffeningsrekening** de vereffeningsrekening op die wordt gebruikt voor de btw-bedragen van het groepslid. Dit account moet **Activa** hebben als de **Accountcategorie**.
5. Geef in het veld **Btw-vereffeningsrekening** de rekening op die u gebruikt voor btw-verrekeningen. Dit account moet **Passiva** hebben als de **Accountcategorie**.
6. Geef in het veld **Vaknr. te betalen btw** het vak op dat het totale verschuldigde btw-bedrag vertegenwoordigt dat verschuldigd is door een groepsindiening van btw.
7. Geef in het veld **Fin. dagboeksjabloon voor groepsvereffening** de dagboeksjabloon op die wordt gebruikt om het document te maken waarmee de groepsvertegenwoordiger de groeps-btw naar de vereffeningsrekening boekt.
8. Het veld **Goedgekeurde leden** toont het aantal groepsleden dat is ingesteld om btw-aangiften in te dienen bij de groepsvertegenwoordiger. Om nieuwe leden toe te voegen kiest u het nummer om de pagina **Goedgekeurde leden van btw-groep** te openen en voegt u de volgende informatie toe:
    1. Voer in het veld **Groepslid-id** een id in voor het groepslid, zoals weergegeven tijdens het instellen van het groepslid (lees meer in de sectie [Btw-groepslid instellen](#set-up-vat-group-members), hierboven).
    2. Geef in het veld **Groepslidnaam** de naam van het groepslid op.
    3. Geef in het veld **Bedrijf** het bedrijf op van waaruit het groepslid btw-aangiften zal doen in [!INCLUDE[prod_short](includes/prod_short.md)], bijvoorbeeld **CRONUS UK Ltd**.
    4. Contactdetails voor het bedrijf opgeven.

## De functies van btw-groepsbeheer gebruiken

Leden van de btw-groep gebruiken de standaardprocessen om btw-aangiften voor te bereiden. Het enige verschil is dat leden de rapportversie **BTWGROEP** op de pagina **Btw-aangifte** moeten kiezen om de btw-aangifte in te dienen bij de btw-groepsvertegenwoordiger, in plaats van bij de belastingdienst. Zie voor meer informatie [Over het rapport Btw-aangifte](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Leden van de btw-groep kunnen ingediende btw-aangiften corrigeren zolang de groepsvertegenwoordiger de btw-aangifte voor de groep niet heeft vrijgegeven. Om een correctie door te voeren moet het btw-groepslid een nieuwe btw-aangifte voor de btw-aangifteperiode maken en deze indienen bij de btw-groepsvertegenwoordiger. Aan de zijde van de btw-groepsvertegenwoordiger vervangt de laatste btw-aangifte van het lid de vorige en wordt deze opgenomen op de pagina **Btw-aangifte**.

In de volgende secties worden de taken beschreven die vertegenwoordigers van btw-groepen moeten uitvoeren om de btw-groepsaangifte in te dienen.

### Indieningen van groepsleden controleren

De pagina **Btw-groepsindieningen** geeft een overzicht van de btw-aangiften die leden hebben ingediend. De pagina dient als conceptlocatie voor de indieningen totdat de btw-groepsvertegenwoordiger ze opneemt in een btw-aangifte voor de groep. De vertegenwoordiger kan de indieningen openen om de individuele vakken te bekijken met het bedrag dat door elk lid van de btw-groep is opgegeven.

> [!TIP]
> Op de pagina **Btw-aangifteperioden** bevat het veld **Indieningen van groepsleden** hoeveel aangiften leden hebben ingediend. Om ervoor te zorgen dat dit getal up-to-date is, kiest u de actie **Btw-aangifteperioden ophalen**.

### Een groeps-btw-aangifte maken

Om voor de groep btw te rapporteren maakt u op de pagina **Btw-aangiften** een btw-aangifte alleen voor uw bedrijf. Voeg daarna de meest recente btw-aangiften van leden van de btw-groep toe door de actie **Groeps-btw opnemen** te kiezen.  

Wanneer de groepsvertegenwoordiger de btw-aangifte van de groep bij de belastingdienst heeft ingediend, voert de vertegenwoordiger normaal gesproken de actie **Btw-vereffening berekenen en boeken** uit. Met deze actie worden openstaande btw-posten en -overdrachtsbedragen naar de btw-vereffeningsrekening gesloten. Deze actie houdt momenteel geen rekening met de groepsindieningen. Alleen de btw-posten van het bedrijf van de btw-groepsvertegenwoordiger worden geboekt. De bedragen voor de indiening van btw-groepsleden moeten handmatig naar het btw-vereffeningsbedrag worden geboekt, zodat de btw-vereffeningsrekening van de btw-groepsvertegenwoordiger de aansprakelijkheid weergeeft van wat aan de autoriteiten is gerapporteerd. Dit gedrag zal veranderen in een aanstaande update van [!INCLUDE[prod_short](includes/prod_short.md)], zodat de volledige groeps-btw (het totale bedrag op rapportregels in de btw-aangifte) zal worden vereffend.

> [!IMPORTANT]
> De btw-groepsfunctionaliteit wordt alleen ondersteund in markten waar [!INCLUDE[prod_short](includes/prod_short.md)] een btw-raamwerk gebruikt dat bestaat uit btw-aangiften en btw-aangifteperioden. U kunt geen btw-groepen gebruiken in andere markten met andere implementaties van lokale btw-rapportage, zoals Oostenrijk, Duitsland, Italië, Spanje en Zwitserland.

## Zie ook

[Lokale functionaliteit van het Verenigd Koninkrijk in de Britse versie](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Belasting digitaal maken in het Verenigd Koninkrijk](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Btw instellen](finance-setup-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Financiële gegevens uit meerdere bedrijven consolideren](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
