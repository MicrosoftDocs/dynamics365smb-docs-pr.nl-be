---
title: E-maillogboekregistratie instellen | Microsoft Docs
description: Leer hoe u e-mailinteracties tussen verkopers en klanten kunt omzetten in echte opportunities.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: e325cce98256b723c6fcfdf4d16068f852a2b032
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308752"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="641bf-103">E-mailberichtuitwisselingen volgen tussen verkopers en contactpersonen</span><span class="sxs-lookup"><span data-stu-id="641bf-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>
<span data-ttu-id="641bf-104">Haal meer uit de communicatie tussen verkopers en uw bestaande of potentiële klanten door e-mailuitwisselingen bij te houden en deze vervolgens om te zetten in bruikbare kansen.</span><span class="sxs-lookup"><span data-stu-id="641bf-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="641bf-105">kan werken met Exchange Online om een logboek bij te houden van de inkomende en uitgaande berichten.</span><span class="sxs-lookup"><span data-stu-id="641bf-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="641bf-106">U kunt de inhoud van elk bericht bekijken en analyseren op de pagina **Interactielogposten**.</span><span class="sxs-lookup"><span data-stu-id="641bf-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a><span data-ttu-id="641bf-107">[!INCLUDE[d365fin](includes/d365fin_md.md)] instellen om e-mailberichten te registreren</span><span class="sxs-lookup"><span data-stu-id="641bf-107">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>
<span data-ttu-id="641bf-108">Ga aan de slag met e-maillogboekregistratie in twee eenvoudige stappen:</span><span class="sxs-lookup"><span data-stu-id="641bf-108">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="641bf-109">Verbind [!INCLUDE[d365fin](includes/d365fin_md.md)] met Exchange Online voor uw Office 365-abonnement.</span><span class="sxs-lookup"><span data-stu-id="641bf-109">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="641bf-110">Exchange Online behandelt uw e-mailberichten.</span><span class="sxs-lookup"><span data-stu-id="641bf-110">Exchange Online handles your email messages.</span></span> <span data-ttu-id="641bf-111">We hebben deze stap eenvoudig gemaakt door een begeleide instelling te bieden.</span><span class="sxs-lookup"><span data-stu-id="641bf-111">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="641bf-112">U hebt alleen uw beheerdersreferenties nodig voor uw beheerdersaccount in Office 365.</span><span class="sxs-lookup"><span data-stu-id="641bf-112">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="641bf-113">Start de guide door naar **Begeleide instelling** te gaan en vervolgens **E-maillogboekregistratie instellen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="641bf-113">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span> 
2. <span data-ttu-id="641bf-114">Zorg ervoor dat geldige e-mailadressen zijn ingevoerd [!INCLUDE[d365fin](includes/d365fin_md.md)] voor uw verkopers en contacten, afhankelijk van of ze potentiële of bestaande klanten zijn.</span><span class="sxs-lookup"><span data-stu-id="641bf-114">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="641bf-115">Om dit te doen opent u voor elke klant of verkoper de kaart **Contact** of **Verkoper/Koper** en kijkt u naar het veld **E-mail**.</span><span class="sxs-lookup"><span data-stu-id="641bf-115">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="641bf-116">Nadat u de stappen in de guide hebt voltooid, kunt u controleren of de verbinding is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="641bf-116">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="641bf-117">Zoek **Marketinginstellingen**, kies **Proces**, dan **Functies** en dan **Instellingen voor e-maillogboekregistratie valideren**.</span><span class="sxs-lookup"><span data-stu-id="641bf-117">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="641bf-118">Uitwisseling van e-mailberichten bekijken in het interactielogboek</span><span class="sxs-lookup"><span data-stu-id="641bf-118">Viewing Email Message Exchanges in the Interaction Log</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="641bf-119">maakt een post op de pagina **Interactielogboek** telkens wanneer een verkoper en een contactpersoon een e-mailbericht uitwisselen.</span><span class="sxs-lookup"><span data-stu-id="641bf-119">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="641bf-120">Om het interactielogboek te bekijken opent u de kaart **Contact** of **Verkoper/Koper** voor de persoon en kiest u vervolgens **Navigeren**, **Historie** en kiest u vervolgens **Interactielogposten**.</span><span class="sxs-lookup"><span data-stu-id="641bf-120">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="641bf-121">Er zijn een paar dingen die we met elke post in het logboek kunnen doen, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="641bf-121">There are a few things we can do with each entry in the log, for example:</span></span>

* <span data-ttu-id="641bf-122">De inhoud bekijken van het e-mailbericht dat is uitgewisseld door te klikken op de actie **Bijlagen weergeven**.</span><span class="sxs-lookup"><span data-stu-id="641bf-122">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
* <span data-ttu-id="641bf-123">Een e-mailuitwisseling veranderen in een opportunity. Als een item er veelbelovend uitziet, kunt u er een opportunity van maken en vervolgens de voortgang naar een verkoop beheren.</span><span class="sxs-lookup"><span data-stu-id="641bf-123">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="641bf-124">Kies hiervoor de post en kies vervolgens de actie **Opportunity maken**.</span><span class="sxs-lookup"><span data-stu-id="641bf-124">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="641bf-125">Zie voor meer informatie [Verkoopopportunities beheren](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="641bf-125">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="641bf-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="641bf-126">See Also</span></span>
[<span data-ttu-id="641bf-127">Relaties beheren</span><span class="sxs-lookup"><span data-stu-id="641bf-127">Managing Relationships</span></span>](marketing-relationship-management.md)

