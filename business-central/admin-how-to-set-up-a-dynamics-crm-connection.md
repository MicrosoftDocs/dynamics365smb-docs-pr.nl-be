---
title: Verbinden met Dynamics 365 Sales | Microsoft Docs
description: U kunt via Common Data Service andere apps integreren met Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196651"
---
# <a name="connect-to-common-data-service"></a>Verbinding maken met Common Data Service
In dit onderwerp wordt beschreven hoe u een verbinding tot stand brengt tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)]. Bedrijven maken doorgaans de verbinding om gegevens te integreren en te synchroniseren met een andere Dynamics 365-bedrijfsapp, zoals [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Voordat u begint
Voordat u de verbinding maakt, moet u een aantal gegevens gereed hebben:  

* De URL van de [!INCLUDE[d365fin](includes/cds_long_md.md)]-omgeving waarmee u verbinding wilt maken. Als u de begeleide instelling **CDS-verbinding instellen** gebruikt om de verbinding tot stand te brengen, ontdekken we uw omgevingen, maar u kunt ook de URL van een andere omgeving in uw tenant invoeren.  
* Een gebruikersnaam en wachtwoord van een gebruikersaccount dat alleen voor de integratie wordt gebruikt. Dit account wordt de 'integratiegebruiker' genoemd. 
* De gebruikersnaam en het wachtwoord van een account dat beheerdersmachtigingen heeft in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Deze stappen beschrijven de procedure voor de online versie van [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Een verbinding instellen met [!INCLUDE[d365fin](includes/cds_long_md.md)]  
Voor alle verificatiesoorten anders dan Office 365-verificatie stelt u de verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] in op de pagina **CDS-verbinding instellen**. Het is raadzaam de begeleide instelling **CDS-verbinding instellen** te gebruiken voor Office 365-verificatie. De instelling maakt het gemakkelijker om de verbinding in te stellen en geavanceerde functies op te geven, zoals koppeling tussen records.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>De begeleide instelling CDS-verbinding instellen gebruiken 
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Begeleide instelling** in en kies de gerelateerde koppeling.
2. Kies **Verbinding met CDS-basisintegratie instellen** om de begeleide instelling te starten.
3. Vul de vereiste velden in.

> [!Note]
> De begeleide instelling **CDS-verbinding instellen** wijst automatisch de beveiligingsrollen **Integratiebeheerder** en **Integratiegebruiker** toe aan het gebruikersaccount dat wordt gebruikt voor integratie, en stelt de toegangsmodus voor het account in op **niet-interactief**.

### <a name="to-create-or-maintain-the-connection-manually"></a>De verbinding handmatig maken of onderhouden
In de volgende procedure wordt beschreven hoe u de verbinding op de pagina **CDS-verbinding instellen** handmatig instelt. Dit is ook de pagina waar u instellingen voor de integratie beheert.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **CDS-verbinding instellen** in en kies de gerelateerde koppeling.
2. Voer de volgende gegevens in voor de verbinding van [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Veld|Omschrijving|
|-----|-----|
|**Omgevings-URL**|Als u eigenaar bent van omgevingen in [!INCLUDE[d365fin](includes/cds_long_md.md)], vinden we die voor u wanneer u de instelling uitvoert. Als u verbinding wilt maken met een andere omgeving in een andere tenant, kunt u de beheerdersreferenties voor de omgeving invoeren en zullen we die ontdekken. |
|**Gebruikersnaam** en **Wachtwoord**|De referenties van het gebruikersaccount voor de integratie. Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Ingeschakeld**|Begin de integratie te gebruiken. Als u de verbinding niet nu inschakelt, worden de verbindingsinstellingen opgeslagen, maar hebben gebruikers geen toegang tot [!INCLUDE[d365fin](includes/cds_long_md.md)]-gegevens uit [!INCLUDE[d365fin](includes/d365fin_md.md)]. U kunt naar deze pagina terugkeren en de verbinding later inschakelen.  |

3. Kies in het veld **Eigendomsmodel** of u wilt dat een teamentiteit in [!INCLUDE[d365fin](includes/cds_long_md.md)] eigenaar is van nieuwe records of een of meer specifieke gebruikers. Als u **Persoon** kiest, moet u elke gebruiker opgeven. Als u **Team** kiest, wordt de standaardbedrijfsunit BCI_bedrijf weergegeven in het veld **Gekoppelde bedrijfsunit**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Als u de verbindingsinstellingen wilt testen, kiest u **Verbinding** en vervolgens **Verbinding testen**.  

    > [!NOTE]  
    >  Als gegevensversleuteling niet is ingeschakeld in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt u gevraagd of u het wilt inschakelen. Als u gegevensversleuteling wilt inschakelen, kiest u **Ja** en geeft u de vereiste informatie op. Anders kiest u **Nee**. U kunt gegevenscodering later inschakelen. Zie voor meer informatie [Gegevens versleutelen in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) in Help voor ontwikkelaars en IT-pro.  

5. Als [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatie niet al is ingesteld, wordt u gevraagd of u de standaardinstellingen voor synchronisatie wilt gebruiken. Afhankelijk van of u records uitgelijnd wilt houden in [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)], kiest u **Ja** of **Nee**.

> [!Note]
> Voor het maken van verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] met behulp van de pagina **CDS-verbinding instellen** moet u mogelijk de beveiligingsrollen Integratiebeheerder en Integratiegebruiker toewijzen aan het account dat wordt gebruikt voor integratie in Dynamics 365 Sales. Zie voor meer informatie [Een beveiligingsrol toewijzen aan een gebruiker](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>Verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] verbreken  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **CDS-verbinding instellen** in en kies de gerelateerde koppeling.
2. Schakel op de pagina **CDS-verbinding instellen** de schakelaar **Geactiveerd** uit.  

## <a name="see-also"></a>Zie ook  
[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  
