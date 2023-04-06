---
title: Stel contactsynchronisatie in met Outlook voor Business Central on-premises
description: Leer hoe u een Business Central on-premises-omgeving configureert Contactsynchronisatie instellen met Outlook voor Business Central on-premises
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 03/17/2023
ms.custom: bap-template
---

# Stel contactsynchronisatie in met Outlook voor Business Central on-premises

In dit artikel leert u hoe u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises instelt om contacten in [!INCLUDE[prod_short](includes/prod_short.md)] te synchroniseren met contacten in Outlook. Ga voor meer informatie over de functie naar [Contacten in Business Central synchroniseren met contacten in Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## Inleiding

Contactsynchronisatie vereist het gebruik van het OAuth 2.0-protocol voor verificatie met Exchange Online. Eerder werd ook basisverificatie ondersteund, maar dit is verouderd en wordt niet langer ondersteund met Exchange Online. U kunt meer lezen over de afschaffing op [Afschaffing van basisverificatie in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Deze wijziging betekent dat contactsynchronisatie in Business Central mogelijk niet meer werkt in uw on-premises omgeving. In dit artikel wordt uitgelegd hoe u het weer kunt laten werken.

## Vereisten

- Exchange Online, een zelfstandige versie of via een Microsoft 365-abonnement  
- Toegang tot de Azure Active Directory (Azure AD)-tenant gebruikt door Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikers hebben een Microsoft 365 of Exchange Online e-mailaccount, dat is toegewezen aan hun accounts in [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt dit controleren in de instelling **Microsoft 365-verificatie** van uw gebruikersprofiel in de lijst **Gebruikers**. 

## Contactsynchronisatie instellen

Voer de volgende stappen uit om contactsynchronisatie in te stellen. Als u [!INCLUDE[prod_short](includes/prod_short.md)] Spring 2019 (v.14) gebruikt, moet u een extra stap uitvoeren die toepassingscode wijzigt of een verbinding instelt met Power BI.

1. <a name="registerapp"></a>Een app voor Exchange Online API registreren in uw Azure AD-tenant.

   In deze stap voegt u een geregistreerde app in de Azure AD-tenant van uw Microsoft 365-abonnement of Exchange Online-abonnement toe. Net als andere Azure-services die werken met Business Central, vereist Exchange Online een geregistreerde app in Azure AD. De geregistreerde app biedt verificatie- en autorisatieservices tussen Business Central en Exchange Online.

   Volg de gedetailleerde instructies in de Help voor ontwikkelaars en IT-professionals op [Een toepassing registreren in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Onthoud bij het doorlopen van de instructies de volgende punten:

   - Als u al een toepassing hebt geregistreerd als onderdeel van een integratie met een ander Microsoft-product, zoals Power BI, dan gebruikt u die geregistreerde app opnieuw. In dit geval hoeft u alleen de app in te stellen met de Office 365 Exchange Online-machtigingen die bij het volgende opsommingsteken worden beschreven.

   - Configureer de geregistreerde app met de volgende gedelegeerde machtigingen voor de Office 365 Exchange Online API:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. Voer voor [!INCLUDE[prod_short](includes/prod_short.md)] versie 14 een van de volgende taken uit:

   - Pas pagina 6700 aan door `FALSE` te veranderen in `TRUE` op de volgende coderegel in de `OnPageOpen`-trigger:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Maak een nieuwe pagina met de volgende code in de OnPageOpen-trigger:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Stel Power BI in door de instructies te volgen op [Business Central on-premises instellen voor Power BI integratie](admin-powerbi-setup.md#setup).

   Nadat de door u gekozen oplossing is geïnstalleerd, vraagt u gebruikers om de nieuwe/gewijzigde pagina uit te voeren of [verbinding te maken met Power BI](across-working-with-powerbi.md#connect). Ze hoeven deze stap maar één keer uit te voeren.

## Volgende stappen

[Contacten in Business Central synchroniseren met contacten in Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
