---
title: Business Central-accountantservaring | Microsoft Docs
description: Meer informatie over de accountantsportal voor Business Central en het accountantrolcentrum dat interne en externe accountants in het cliëntbedrijf ondersteunt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896145"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Accountantervaringen binnen [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Elk bedrijf moet zijn boekhouding doen en aftekenen. Sommige bedrijven hebben een externe accountant en andere hebben een accountant in dienst. Ongeacht wat voor accountant u bent, u kunt het rolcentrum **Accountant** gebruiken als uw thuis binnen [!INCLUDE[d365fin](includes/d365fin_md.md)]. Van hieruit hebt u toegang tot alle pagina's die u in uw werk nodig hebt.  

## <a name="accountant-role-center"></a>Rolcentrum Accountant
Het rolcentrum is een dashboard met activiteittegels die realtime cijfers bevatten en die u snel toegang geven tot gegevens. In het lint boven op de pagina hebt u toegang tot meer acties, zoals het openen van de vaakst gebruikte financiële rapporten en de rekeningoverzichten in Excel. Op de navigatiebalk bovenin kunt u snel schakelen tussen de lijsten die u het meest gebruikt. Hier ziet u andere gebieden, zoals **Geboekte documenten** met de diverse soorten documenten die het bedrijf heeft geboekt.  

Als [!INCLUDE[d365fin](includes/d365fin_md.md)] nieuw voor u is, kunt u een overzicht van video's direct vanuit uw rolcentrum starten. U kunt ook een **Aan de slag**-rondleiding starten die wijst op belangrijke gebieden.  

## <a name="inviteaccountant"></a>Uw externe accountant uitnodigen voor uw [!INCLUDE[d365fin](includes/d365fin_md.md)]
Als u een externe auditor gebruikt om uw boeken en financiële rapportage beheren, kunt u deze uitnodigen voor uw [!INCLUDE[d365fin](includes/d365fin_md.md)], zodat hij of zij met u kan werken aan uw fiscale gegevens.

Als de accountant toegang heeft gekregen tot uw [!INCLUDE[d365fin](includes/d365fin_md.md)], kan hij of zij het rolcentrum **Accountant** gebruiken, dat eenvoudig toegang tot de meest relevante pagina's voor hun werk biedt.  

We hebben het voor u eenvoudig gemaakt om uw externe accountant uit te nodigen. Open gewoon de pagina **Gebruikers** en kies de actie **Externe accountant uitnodigen** op het lint. Er wordt een e-mail voor u gemaakt. Voeg het werke-mailadres van uw accountant eraan toe en verzend de uitnodiging.  
> [!Note]  
> Dit vereist dat u SMTP-e-mail hebt ingesteld. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.   

![Uw accountant uitnodigen](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> Het e-mailadres van de accountant moet een werkadres op basis van Azure Active Directory zijn. Als de accountant een ander type e-mail gebruikt, kan de uitnodiging niet worden verzonden.  

### <a name="behind-the-scenes"></a>Achter de schermen
[!INCLUDE[d365fin](includes/d365fin_md.md)] omvat drie licenties van het type Externe accountant. Als uw bedrijf een externe accountant gebruikt, kunt u toegang geven tot uw [!INCLUDE[d365fin](includes/d365fin_md.md)] door aan hen zo'n licentie toe te kennen. Zie voor meer informatie over licenties de [Microsoft Dynamics 365 Business Central Licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=871590). 

Als uw abonnement nog steeds een beschikbare licentie heeft, kan uw beheerder of wederverkoper een externe gebruiker toevoegen via de Azure-portal en deze gebruiker de Externe accountant-licentie toewijzen. Zie voor meer informatie [Azure Active Directory B2B-samenwerkingsgebruikers toevoegen in de Azure-portal](/azure/active-directory/b2b/add-users-administrator).

U kunt vervolgens de accountant vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] uitnodigen met behulp van de begeleide instelling **Externe accountant uitnodigen**. Omdat deze taak echter toegang vereist voor het beheren van gebruikers en licenties in Azure Active Directory, moet de gebruiker die deze uitnodiging verzendt de rol **Globale beheerder** of **Gebruikersbeheer** hebben in het Office 365-beheercentrum. Zie voor meer informatie [Over beheerdersrollen](/office365/admin/add-users/about-admin-roles) in de Office 365-beheerdersinhoud. 

## <a name="accountant-hub"></a>Accountant Hub
Als u een accountant met verschillende cliënten bent, kunt u [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] gebruiken voor een beter overzicht van uw cliënten. Van daaruit kunt u toegang krijgen tot de tenant van elke cliënt in [!INCLUDE[d365fin](includes/d365fin_md.md)] en het accountantrolcentrum gebruiken zoals hierboven beschreven. Zie voor meer informatie [Welkom bij [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] is momenteel in openbare preview op een beperkt aantal markten.

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met dimensies](finance-dimensions.md)  
[Financiële overzichten analyseren in Excel:](finance-analyze-excel.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cashflowanalyse instellen](finance-setup-cash-flow-analyses.md)  
[Welkom bij [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Accountant Hub op Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
