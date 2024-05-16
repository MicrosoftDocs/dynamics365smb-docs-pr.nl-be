---
title: Integreren met Microsoft Dynamics 365 Field Service
description: Integratie van Business Central met Field Service.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dynamics-365-field-service"></a>Integreren met Microsoft Dynamics 365 Field Service

Serviceorganisaties hebben een front-to-back-toepassing nodig waarin financiën, voorraad en inkoop nauw zijn gekoppeld aan dienstverlening. Ze genereren bij elke transactie financiële gegevens. Elke werkorder vertegenwoordigt kosten en opbrengsten, en elke resource genereert winst en verlies. Klantinteracties voegen posten toe aan het grootboek. Met de integratie tussen [!INCLUDE [prod_short](includes/prod_short.md)] en [!INCLUDE [field-service-short](includes/field-service-short.md)] wordt het complete proces van het beheer van serviceactiviteiten gestroomlijnd en wordt gezorgd voor een soepele informatiestroom tussen de twee systemen.  

U kunt eenvoudig werkorders maken en beheren in [!INCLUDE [field-service-short](includes/field-service-short.md)], de voortgang van servicetaken volgen, resources toewijzen en verbruiksgegevens vastleggen. Wanneer u in [!INCLUDE [field-service-short](includes/field-service-short.md)] een werkorder voltooit, maakt de integratie een soepele overdracht van gegevens naar [!INCLUDE [prod_short](includes/prod_short.md)] mogelijk voor verdere verwerking.  

De integratie vergemakkelijkt ook de facturering en afhandeling van werkorders in [!INCLUDE [prod_short](includes/prod_short.md)]. Op basis van de serviceactiviteiten en het verbruik dat is geregistreerd in [!INCLUDE [field-service-short](includes/field-service-short.md)] kunt u nauwkeurige facturen genereren.  

Door [!INCLUDE [prod_short](includes/prod_short.md)] met [!INCLUDE [field-service-short](includes/field-service-short.md)] te integreren, hoeft u gegevens niet handmatig in te voeren of dubbele inspanningen te leveren. Integratie biedt ook een uitgebreid overzicht van serviceactiviteiten en financiële gegevens, waardoor betere besluitvorming en operationele efficiëntie mogelijk worden.

## <a name="prerequisites"></a>Vereisten

Omdat [!INCLUDE [field-service-short](includes/field-service-short.md)] op basis van Dynamics 365 Sales is gebouwd, moet u [een verbinding met Dataverse instellen](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) en [integratie met Dynamics 365 Sales mogelijk maken](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

### <a name="permissions-and-security-roles-for-user-accounts"></a>Machtigingen en beveiligingsrollen voor gebruikersaccounts

Wanneer u de integratieoplossing installeert, worden machtigingen voor het integratiegebruikersaccount geconfigureerd. Als deze machtigingen veranderen, moet u deze mogelijk opnieuw instellen. U kunt dat doen door de integratieoplossing opnieuw te installeren via de pagina **Dynamics 365-verbinding instellen** door **Integratieoplossing opnieuw implementeren** te kiezen. In de volgende gedeelten worden de machtigingen en beveiligingsrollen vermeld die de oplossing voor elke app implementeert.

#### <a name="sales"></a>Verkopen

* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-integratiebeheerder
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-integratiegebruiker
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-gebruiker van productbeschikbaarheid

#### <a name="business-central"></a>Business Central

Gebruikers die projectjournalen boeken, moeten over de volgende machtigingenset beschikken:

* Dynamics 365 Sales-integratie

#### <a name="field-service"></a>Veldservice

Om de geïntegreerde gegevens te kunnen gebruiken, moeten gebruikers de volgende beveiligingsrol hebben:

* Integratie van Business Central met Field Service

Gebruikers moeten deze rol bijvoorbeeld hebben om werkorders te verbinden met [!INCLUDE [prod_short](includes/prod_short.md)] voor verwerking.

> [!NOTE]
> Zorg ervoor dat gebruikers worden toegewezen aan de standaard beveiligingsrollen en -profielen in [!INCLUDE [field-service-short](includes/field-service-short.md)].  
>
> Ga voor meer informatie over kolombeveiligingsprofielen in [!INCLUDE [field-service-short](includes/field-service-short.md)] naar [Field Service-beveiligingsrollen](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Beheerders moeten een van de juiste kolombeveiligingsprofielen toevoegen aan gebruikers in Power Platform. Ga voor meer informatie naar [Teams of gebruikers toevoegen aan een kolombeveiligingsprofiel om toegang te beheren](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Om de actie **Openen in Business Central** in Sales te gebruiken, moet u over de volgende rechten beschikken voor de volgende tabellen:
>
> * U moet over machtigingen voor **Lezen** beschikken voor de tabel **Dynamics 365 Business Central-verbinding** (nav_connection).
> * U moet over de machtigingen **Lezen**, **Schrijven** en **Verwijderen** beschikken voor de tabel **Standaard Dynamics 365 Business Central-verbinding** (nav_defaultconnection).

### <a name="other-settings-in-field-service"></a>Overige instellingen in Field Service

Breng op de pagina **Field Service-instelling** de volgende wijzigingen aan:

* Schakel op het tabblad **Inkoop** het veld **Gebruik van producten die niet op voorraad zijn** uit. Anders krijgt u mogelijk een waarschuwing 'niet op voorraad' wanneer u een product kiest dat niet op voorraad is in [!INCLUDE [field-service-short](includes/field-service-short.md)], maar wel op voorraad is in [!INCLUDE [prod_short](includes/prod_short.md)].
* Schakel op het tabblad **Werkorder/Boeking** de schakelopties **Prijs berekenen** en **Kosten berekenen** uit. Kies in het veld **Factuur voor werkorders maken** de optie **Nooit**.

> [!NOTE]
> Door een verbinding in te stellen met [!INCLUDE [field-service-short](includes/field-service-short.md)] wordt de koppeling tussen resources en producten opgeheven. Om [!INCLUDE [prod_short](includes/prod_short.md)]-artikelen beschikbaar te maken in [!INCLUDE [field-service-short](includes/field-service-short.md)], werkt u het veld **Field Service-producttype** bij zodat het overeenkomt met het veld **Type** voor de artikelen in [!INCLUDE [prod_short](includes/prod_short.md)]. Ga voor meer informatie naar [Een product of service maken](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## <a name="set-up-the-integration-in-business-central"></a>De integratie in Business Central instellen

Nadat u verbinding hebt gemaakt met Dataverse en Sales, kunt u uw integratie met [!INCLUDE [field-service-short](includes/field-service-short.md)] instellen. Op de pagina **Begeleide instelling** in [!INCLUDE [prod_short](includes/prod_short.md)] kiest u **Integratie met Dynamics 365 Field Service instellen** om de begeleide instelling uit te voeren. In dit gedeelte worden de belangrijkste instellingen in de guide beschreven.

Als u wilt dat mensen het verbruik van artikelen en services kunnen boeken in [!INCLUDE [field-service-short](includes/field-service-short.md)]-werkorders, geeft u **Projectdagboeksjabloon** en **Projectdagboekbatch** op om daarmee het verbruik van producten en services te boeken.

Omdat services worden uitgedrukt in duur in [!INCLUDE [field-service-short](includes/field-service-short.md)], geeft u **Maateenheid uren** op om daarmee duur om te rekenen naar hoeveelheden in [!INCLUDE [prod_short](includes/prod_short.md)].

U kunt ook opgeven wanneer werkorderproducten en serviceregels moeten worden gesynchroniseerd met [!INCLUDE [prod_short](includes/prod_short.md)]. Ze kunnen bijvoorbeeld worden gesynchroniseerd wanneer werkorderregels worden gebruikt of wanneer iemand een werkorder voltooit. Kies de juiste optie in het veld **Werkorderproducten/-services synchroniseren**.

Nadat werkorderproducten en -services zijn gesynchroniseerd met projectdagboeken in [!INCLUDE [prod_short](includes/prod_short.md)], kunt u kiezen of u de projectdagboeken handmatig wilt boeken. Kies de juiste optie in het veld **Automatisch projectdagboekregels boeken**:

* Wanneer een werkorder is voltooid.
* Wanneer werkorderproducten of -services worden gebruikt.

Nadat u de instelling hebt voltooid, voert u een volledige synchronisatie uit via de pagina **Dynamics 365 Field Service-integratie instellen**. Met deze actie worden tabeltoewijzingen gesynchroniseerd voor zaken als:

* Projecttaken voor projecten waarbij **Gebruikskoppeling toepassen** is ingesteld. Met deze synchronisatie worden [!INCLUDE [prod_short](includes/prod_short.md)]-projecten beschikbaar gemaakt voor selectie in [!INCLUDE [field-service-short](includes/field-service-short.md)].
* Voor resources die niet zijn geblokkeerd, is **Urenstaat gebruiken** niet geselecteerd, en is **Uur** opgegeven als de maateenheid op de pagina **Dynamics 365 Field Service-integratie instellen**.
* Serviceartikelen (vereist dat u de Premium-ervaring in [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt).

## <a name="standard-field-service-entity-mapping-for-synchronization"></a>Standaardtoewijzing van Field Service-entiteit voor synchronisatie

De basis voor de synchronisatie van gegevens is de toewijzing van de tabellen en velden in [!INCLUDE [prod_short](includes/prod_short.md)] aan tabellen en kolommen in Dataverse, zodat de gegevens kunnen worden uitgewisseld. Toewijzing gebeurt via integratietabellen. Ga voor meer informatie over tabeltoewijzingen naar [De tabellen en velden toewijzen voor synchronisatie](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

Integratie met [!INCLUDE [field-service-short](includes/field-service-short.md)] introduceert de volgende standaardtoewijzingen van integratietabellen.

* **PJLINE-WORDERPRODUCT** - hiermee worden werkorderproducten in [!INCLUDE [field-service-short](includes/field-service-short.md)] toegewezen aan projectdagboekregels in [!INCLUDE [prod_short](includes/prod_short.md)].
* **PJLINE-WORDERSERVICE** - hiermee worden werkorderservices in [!INCLUDE [field-service-short](includes/field-service-short.md)] toegewezen aan projectdagboekregels in [!INCLUDE [prod_short](includes/prod_short.md)].
* **PROJECTTASK** - hiermee worden projecten en projecttaken toegewezen in [!INCLUDE [prod_short](includes/prod_short.md)] aan producten in externe projecten in [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **RESOURCE-BOOKABLERSC** - hiermee worden resources in [!INCLUDE [prod_short](includes/prod_short.md)] toegewezen aan boekbare resources in [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **SVCITEM-CUSTASSET** - (alleen Premium-ervaring) hiermee worden serviceartikelen in [!INCLUDE [prod_short](includes/prod_short.md)] toegewezen aan klantactiva in [!INCLUDE [field-service-short](includes/field-service-short.md)].

## <a name="use-data-in-both-applications"></a>Gegevens in beide toepassingen gebruiken

In de volgende gedeelten worden de functies beschreven waarbij u de gegevens kunt gebruiken die afkomstig zijn van [!INCLUDE [prod_short](includes/prod_short.md)] en [!INCLUDE [field-service-short](includes/field-service-short.md)].

### <a name="field-service-1"></a>Veldservice

U kunt [werkorders maken](/dynamics365/field-service/create-work-order) met **serviceaccount** en **factureringsaccount** uit [!INCLUDE [prod_short](includes/prod_short.md)]. Voor werkorders moet u **Business Central-projecttaak** selecteren in het veld **Extern project**. Als u een project selecteert, kunt u werkorderproducten en -services synchroniseren met de juiste projecttaak in [!INCLUDE [prod_short](includes/prod_short.md)].

U kunt voorraadartikelen en niet-voorraadartikelen toevoegen als **Werkorderproducten** aan werkorders en de beschikbare hoeveelheid, kosten en prijzen ophalen van [!INCLUDE [prod_short](includes/prod_short.md)]. Ga voor meer informatie naar [Een werkorder maken via het werkorderformulier en de recordlijst](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

U kunt artikelen van het type service als **Werkorderservices** toevoegen en de kosten en prijzen ophalen van [!INCLUDE [prod_short](includes/prod_short.md)]. Ga voor meer informatie naar het [tabblad Producten en services](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> Wanneer de status van een product of service op een werkorder verandert van **Geschat** in **Gebruikt** in [!INCLUDE [field-service-short](includes/field-service-short.md)], worden ze gesynchroniseerd met projectdagboekregels in [!INCLUDE [prod_short](includes/prod_short.md)].

U kunt een resource boeken en **Boekingen** koppelen aan werkorderservices met **Boekbare resource** van [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="business-central-1"></a>Business Central

Afhankelijk van uw instellingen op de pagina **Field Service-integratie instellen** wordt wanneer werkorders producten en services bevatten, verbruiksinformatie overgedragen en geboekt met behulp van een **Projectdagboek** in [!INCLUDE [prod_short](includes/prod_short.md)].

De waarden **Te factureren hoeveelheid** en **Te factureren duur** worden gekopieerd naar het veld **Aantal te verplaatsen naar factuur**. Op basis van deze waarden kunt u verkoopfacturen maken en boeken in [!INCLUDE [prod_short](includes/prod_short.md)] om de klant te factureren. Nadat de factuur is geboekt of het verbruik is verwerkt in [!INCLUDE [prod_short](includes/prod_short.md)], worden de gefactureerde hoeveelheid en de verbruikte hoeveelheid weergegeven op het tabblad [!INCLUDE [prod_short](includes/prod_short.md)] van de pagina´s **Werkorderproduct** en **Werkorderservice**.  

Gebruik de pagina **Projectplanningsregels** om het boeken en factureren van verbruik op werkorders bij te houden. Op de pagina **Projectplanningsregels** kunt u verkoopfacturen maken en boeken in [!INCLUDE [prod_short](includes/prod_short.md)]. Daarna kunt u ze synchroniseren met [!INCLUDE [field-service-short](includes/field-service-short.md)] en de status van de facturen bijhouden.

> [!NOTE]
> Werkorderservices met een boeking waarbij gebruik wordt gemaakt van een boekbare resource die is gekoppeld aan een [!INCLUDE [prod_short](includes/prod_short.md)]-resource, worden gesynchroniseerd met twee projectdagboekregels: één regel van het type **Budget** voor de gekoppelde resource en een andere regel van het type **Factureerbaar** voor het artikel dat wordt onderhouden.
>
> Het product dat wordt gekozen voor de werkorderservice moet zijn gekoppeld aan een artikel van het type **Service** in [!INCLUDE [prod_short](includes/prod_short.md)]. Bovendien moet de basiseenheid voor het artikel worden ingesteld op **Maateenheid uren** die is gekozen op de pagina **Dynamics 365 Field Service-integratie instellen**.
>
> U kunt een factuur maken voor een artikel van het type **Service** op de factureerbare projectplanningsregel en de budgetprojectplanningsregel gebruiken om de kosten met de resource te registreren.

## <a name="see-also"></a>Zie ook

[Integreren met Microsoft Dataverse via gegevenssynchronisatie](admin-common-data-service.md)  
[De te synchroniseren tabellen en velden toewijzen](admin-how-to-modify-table-mappings-for-synchronization.md)
