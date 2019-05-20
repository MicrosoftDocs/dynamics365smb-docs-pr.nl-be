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
ms.date: 05/02/2019
ms.author: edupont
ms.openlocfilehash: f088e1319684b9a18a2b0c8ab5305f73747f6889
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/02/2019
ms.locfileid: "1446934"
---
# <a name="accountant-experiences-in-included365finlongincludesd365finlongmdmd"></a>Accountantervaringen binnen [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Elk bedrijf moet zijn boekhouding doen en aftekenen. Sommige bedrijven hebben een externe accountant en andere hebben een accountant in dienst. Ongeacht wat voor accountant u bent, u kunt het rolcentrum **Accountant** gebruiken als uw thuis binnen [!INCLUDE[d365fin](includes/d365fin_md.md)]. Van hieruit hebt u toegang tot alle pagina's die u in uw werk nodig hebt.  

## <a name="accountant-role-center"></a>Rolcentrum Accountant
Het rolcentrum is een dashboard met activiteittegels die realtime cijfers bevatten en die u snel toegang geven tot gegevens. In het lint boven op de pagina hebt u toegang tot meer acties, zoals het openen van de vaakst gebruikte financiële rapporten en de rekeningoverzichten in Excel. Op de navigatiebalk bovenin kunt u snel schakelen tussen de lijsten die u het meest gebruikt. Hier ziet u andere gebieden, zoals **Geboekte documenten** met de diverse soorten documenten die het bedrijf heeft geboekt.  

Als [!INCLUDE[d365fin](includes/d365fin_md.md)] nieuw voor u is, kunt u een overzicht van video's direct vanuit uw rolcentrum starten. U kunt ook een **Aan de slag**-rondleiding starten die wijst op belangrijke gebieden.  

## <a name="accountant-hub"></a>Accountant Hub
Als u een accountant met verschillende cliënten bent, kunt u [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] gebruiken voor een beter overzicht van uw cliënten. Van daaruit kunt u toegang krijgen tot de tenant van elke cliënt in [!INCLUDE[d365fin](includes/d365fin_md.md)] en het accountantrolcentrum gebruiken zoals hierboven beschreven. Zie voor meer informatie [Welkom bij [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Uw externe accountant uitnodigen voor uw [!INCLUDE[d365fin](includes/d365fin_md.md)]
Als u een externe auditor gebruikt om uw boeken en financiële rapportage beheren, kunt u deze uitnodigen voor uw [!INCLUDE[d365fin](includes/d365fin_md.md)], zodat hij of zij met u kan werken aan uw fiscale gegevens.

Als de accountant toegang heeft gekregen tot uw [!INCLUDE[d365fin](includes/d365fin_md.md)], kan hij of zij het rolcentrum **Accountant** gebruiken, dat eenvoudig toegang tot de meest relevante pagina's voor hun werk biedt.  

We hebben het voor u eenvoudig gemaakt om uw externe accountant uit te nodigen. Open gewoon de pagina **Gebruikers** en kies de actie **Externe accountant uitnodigen** op het lint. Er wordt een e-mail voor u gemaakt. Voeg het werke-mailadres van uw accountant eraan toe en verzend de uitnodiging.  

![Uw accountant uitnodigen](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Dit vereist dat u SMTP-e-mail hebt ingesteld. U kunt dit zelf doen of uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner vragen. Daarnaast moet u als gebruikersbeheerder zijn aangemeld bij [!INCLUDE[d365fin](includes/d365fin_md.md)], niet als bedrijfeigenaar of een andere gebruiker. Ten slotte moet u het proefbedrijf hebben verlaten zodat u een Azure Active Directory-beheerder hebt.  

> [!IMPORTANT]  
> Het e-mailadres van de accountant moet een werkadres op basis van Azure Active Directory zijn. Als de accountant een ander type e-mail gebruikt, kan de uitnodiging niet worden verzonden.  

### <a name="separate-license"></a>Afzonderlijke licentie
Achter de schermen wordt de accountant toegevoegd aan uw Active Directory-tenant. Uw beheerder kan controleren of de accountant de uitnodiging accepteert en de juiste licentie toegewezen krijgt. De stappen hiervoor zijn afhankelijk van het soort rekening in dat u hebt gebruikt toen u zich aanmeldde bij [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dit onderwerp is gebaseerd op het gebruik van een Office 365-account dat Microsoft Azure Active Directory gebruikt.  

Als u uw abonnement op [!INCLUDE[d365fin](includes/d365fin_md.md)] hebt geactiveerd en het evaluatiebedrijf niet meer gebruikt, hebt u een Azure Active Directory-tenant. De beheerder of [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner beheert deze tenant in de [Azure-portal](https://portal.azure.com). Hier worden nieuwe gebruikers en toegevoegd en licenties toegepast en verwijderd. Zie voor meer informatie [Microsoft Azure-portal - overzicht](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Een van de licentiesoorten voor [!INCLUDE[d365fin](includes/d365fin_md.md)] is de *Externe accountant*-licentie. Dit licentiesoort is bedoeld voor gebruik door gebruikers zoals externe accountants. Dit betekent dat u geen extra seat in uw huidige Active Directory hoeft te kopen of een van uw bestaande [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersaccounts voor uw externe accountant hoeft te gebruiken. Als uw huidige Office 365-abonnement bijvoorbeeld 10 gebruikers bevat voor [!INCLUDE[d365fin](includes/d365fin_md.md)] en u momenteel 10 *Volwaardige gebruiker*-licenties gebruikt, kan uw beheerder gewoon uw externe accountant als gastgebruiker toevoegen in de Azure-portal en aan deze gebruiker zonder extra kosten de *Externe accountant*-licentie toewijzen. U kunt echter maar één gebruiker met de *Externe accountant*-licentie hebben. Als u meer gebruikers wilt toevoegen, moet u uw Office 365-abonnement bijwerken.

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
[Dynamics 365 - Accountant Hub op Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
