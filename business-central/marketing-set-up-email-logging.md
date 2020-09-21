---
title: E-maillogboekregistratie instellen | Microsoft Docs
description: Leer hoe u e-mailinteracties tussen verkopers en klanten kunt omzetten in echte opportunities.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 07/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9ca381bfebcd6db8e67d8153d4d2bc17eeffad81
ms.sourcegitcommit: f9aec4a72172d9270e14e2938c5550d69508f1aa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/02/2020
ms.locfileid: "3532681"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>E-mailberichtuitwisselingen volgen tussen verkopers en contactpersonen

Haal meer uit de communicatie tussen verkopers en uw bestaande of potentiële klanten door e-mailuitwisselingen bij te houden en deze vervolgens om te zetten in bruikbare kansen. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan werken met Exchange Online om een logboek bij te houden van de inkomende en uitgaande berichten. U kunt de inhoud van elk bericht bekijken en analyseren op de pagina **Interactielogposten**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Openbare mappen en regels instellen voor e-mailregistratie in Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Vervolgens verbindt u [!INCLUDE[prodshort](includes/prodshort.md)] met Exchange Online.

## <a name="setting-up-d365fin-to-log-email-messages"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] instellen om e-mailberichten te registreren

Ga aan de slag met e-maillogboekregistratie in twee eenvoudige stappen:

1. Verbind [!INCLUDE[d365fin](includes/d365fin_md.md)] met Exchange Online voor uw Office 365-abonnement. Exchange Online behandelt uw e-mailberichten. We hebben deze stap eenvoudig gemaakt door een begeleide instelling te bieden. U hebt alleen uw beheerdersreferenties nodig voor uw beheerdersaccount in Office 365. Start de guide door naar **Begeleide instelling** te gaan en vervolgens **E-maillogboekregistratie instellen** te kiezen.  

2. Zorg ervoor dat geldige e-mailadressen zijn ingevoerd [!INCLUDE[d365fin](includes/d365fin_md.md)] voor uw verkopers en contacten, afhankelijk van of ze potentiële of bestaande klanten zijn. Om dit te doen opent u voor elke klant of verkoper de kaart **Contact** of **Verkoper/Koper** en kijkt u naar het veld **E-mail**.

> [!Tip]
> Nadat u de stappen in de guide hebt voltooid, kunt u controleren of de verbinding is geslaagd. Zoek **Marketinginstellingen**, kies **Proces**, dan **Functies** en dan **Instellingen voor e-maillogboekregistratie valideren**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Uitwisseling van e-mailberichten bekijken in het interactielogboek

[!INCLUDE[d365fin](includes/d365fin_md.md)] maakt een post op de pagina **Interactielogboek** telkens wanneer een verkoper en een contactpersoon een e-mailbericht uitwisselen. Om het interactielogboek te bekijken opent u de kaart **Contact** of **Verkoper/Koper** voor de persoon en kiest u vervolgens **Navigeren**, **Historie** en kiest u vervolgens **Interactielogposten**. Er zijn een paar dingen die we met elke post in het logboek kunnen doen, bijvoorbeeld:

- De inhoud bekijken van het e-mailbericht dat is uitgewisseld door te klikken op de actie **Bijlagen weergeven**.
- Een e-mailuitwisseling veranderen in een opportunity. Als een item er veelbelovend uitziet, kunt u er een opportunity van maken en vervolgens de voortgang naar een verkoop beheren. Kies hiervoor de post en kies vervolgens de actie **Opportunity maken**. Zie voor meer informatie [Verkoopopportunities beheren](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Zie ook
[Relaties beheren](marketing-relationship-management.md)
