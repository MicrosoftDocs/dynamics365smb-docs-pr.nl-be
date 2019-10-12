---
title: Cliënten toevoegen aan de Dynamics 365-accountantervaring | Microsoft Docs
description: Leer hoe u bestaande cliënten toevoegt aan Accountant Hub voor Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 95a4153c56693d8bdd28980f1acff14b917a9488
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300079"
---
# <a name="add-clients-to-your-dashboard-in-include-d365acc_longincludesd365acc_long_mdmd"></a>Cliënten toevoegen aan uw dashboard in [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

U kunt een cliënt toevoegen via de pagina **Cliënten**, dat u kunt openen door de actie **Cliënten beheren** te kiezen op het lint. Kies gewoon **Nieuw** en vul vervolgens de velden in.  

> [!div class="mx-imgBorder"]
> ![Een cliënt toevoegen](./media/accountant-add-client/manage-client.png)

De gegevens op de kaart voor elke cliënt worden door u opgegeven en u kunt deze desgewenst wijzigen. Het veld **Cliënt-URL** is echter belangrijk. Daarmee krijg u toegang tot de [!INCLUDE [d365fin](includes/d365fin_md.md)] van elke cliënt. Gebruik de actie **Cliënt-URL valideren** op het lint om te testen dat u de juiste koppeling hebt ingevoerd. De URL die u moet invoeren, verwijst naar de [!INCLUDE [d365fin](includes/d365fin_md.md)] van de cliënt en bevat hun domeinadres. Als zij het domein bijvoorbeeld hebben opgegeven als MyBusiness.com, is de koppeling naar hun [!INCLUDE [d365fin](includes/d365fin_md.md)] *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Vóór de wijziging van mei 2018 had de URL die u opgaf, een andere indeling met de bedrijfsnaam van de cliënt aan het begin. In de huidige versie van [!INCLUDE [d365fin](includes/d365fin_md.md)] is de indeling ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, waarbij ```clientdomain``` het domein van uw client vertegenwoordigt.  

De cliënt-URL wordt gebruikt als u de menuopdracht **Ga naar bedrijf** kiest in het [!INCLUDE [d365acc](includes/d365acc_md.md)]-dashboard.  

### <a name="get-invited-to-a-clients-include-d365fin_longincludesd365fin_long_mdmd"></a>Worden uitgenodigd bij de [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] van een client
Een bedrijf dat [!INCLUDE [d365fin](includes/d365fin_md.md)] gebruikt, kan u uitnodigen tot [!INCLUDE [d365fin](includes/d365fin_md.md)] als hun externe accountant. Als u wilt worden uitgenodigd, moet u ze het e-mailadres geven dat u gebruikt met [!INCLUDE [d365acc](includes/d365acc_md.md)], bijvoorbeeld <em>me@accountant.com</em>. De beheerder van uw cliënt kan u dan aan hun systeem toevoegen door de wizard **Externe accountant uitnodigen** uit te voeren.  

U ontvangt dan een e-mail van uw cliënt met koppelingen naar hun [!INCLUDE [d365fin](includes/d365fin_md.md)]. De eerste koppeling is een uitnodiging om toegang tot het bedrijf te krijgen. Open deze koppeling en accepteer de stappen om te worden toegevoegd aan de [!INCLUDE [d365fin](includes/d365fin_md.md)]-omgeving van uw cliënt. Met de tweede koppeling kunt u deze cliënt toevoegen aan uw dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)], zoals hierboven wordt beschreven.  

Wanneer u de uitnodiging hebt geaccepteerd, wordt u aangemeld en krijgt u toegang tot de financiële gegevens van de cliënt via het rolcentrum **Accountant**. Zie [Accountantervaringen binnen [!INCLUDE[d365fin](includes/d365fin_md.md)] voor meer informatie](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Zie ook
[Aan de slag met [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Problemen met [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md) oplossen  
