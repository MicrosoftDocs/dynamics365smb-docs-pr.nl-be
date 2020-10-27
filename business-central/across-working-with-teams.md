---
title: Werken met Business Central-gegevens in Microsoft Teams | Microsoft Docs
description: Lees hoe u de Business Central-app gebruikt voor Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989447"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="bcdb5-103">Werken met Business Central-gegevens in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bcdb5-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="bcdb5-104">[!INCLUDE [prodshort](includes/prodshort.md)] biedt een app die Microsoft Teams verbindt met uw bedrijfsgegevens in [!INCLUDE [prodshort](includes/prodshort.md)], zodat u snel details met teamleden kunt delen en sneller op vragen kunt reageren.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="bcdb5-105">In dit artikel leert u hoe u de app gebruikt om [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens te delen met collega's in een Teams-gesprek.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="bcdb5-106">Overzicht</span><span class="sxs-lookup"><span data-stu-id="bcdb5-106">Overview</span></span>

<span data-ttu-id="bcdb5-107">Met de [!INCLUDE [prodshort](includes/prodshort.md)]-app kunt u:</span><span class="sxs-lookup"><span data-stu-id="bcdb5-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="bcdb5-108">Een koppeling kopiëren naar een Business Central-record en plakken in een Teams-gesprek om met uw collega's te delen.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="bcdb5-109">De koppeling wordt uitgebreid tot een compacte, interactieve kaart die informatie over de record weergeeft.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="bcdb5-110">Eenmaal in het gesprek kunnen u en collega's meer details over de record bekijken, gegevens bewerken en actie ondernemen zonder Teams te verlaten.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="bcdb5-111">[![Teams-integratie met Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bcdb5-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bcdb5-112">Vereisten</span><span class="sxs-lookup"><span data-stu-id="bcdb5-112">Prerequisites</span></span>

- <span data-ttu-id="bcdb5-113">U hebt toegang tot Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="bcdb5-114">U hebt de [!INCLUDE [prodshort](includes/prodshort.md)]-app in Teams geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="bcdb5-115">Zie voor meer informatie [De [!INCLUDE [prodshort](includes/prodshort.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren</span><span class="sxs-lookup"><span data-stu-id="bcdb5-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="bcdb5-116">Alle deelnemers aan een Teams-gesprek kunnen kaarten bekijken voor Business Central-records die u indient bij het gesprek.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="bcdb5-117">Maar om meer details over records te bekijken door de knop **Details** of **Nieuw venster** op een kaart te gebruiken, hebben ze toegang nodig tot [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="bcdb5-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="bcdb5-118">Zie voor meer informatie [Microsoft Teams-integratie beheren](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="bcdb5-119">Een Business Central-kaart opnemen in een Teams-gesprek</span><span class="sxs-lookup"><span data-stu-id="bcdb5-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="bcdb5-120">Log in bij [!INCLUDE [prodshort](includes/prodshort.md)] met uw browser.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="bcdb5-121">Open de record die u wilt delen.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="bcdb5-122">De app is ontworpen om pagina's van het kaarttype weer te geven vanuit [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="bcdb5-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="bcdb5-123">Open dus een pagina met één record, zoals een artikel, klant of verkooporder.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="bcdb5-124">U kunt de app niet gebruiken voor rolcentra of pagina's die meerdere records in een lijst weergeven.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="bcdb5-125">Kopieer de volledige URL uit de adresbalk van de browser.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Kopieer de Business Central-URL vanuit de browser](media/teams-url.png)
4. <span data-ttu-id="bcdb5-127">Ga naar Teams en start een gesprek. Dat kan chatten met een persoon, een groep personen of een teamkanaal zijn.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="bcdb5-128">Plak de URL in het vak waarin u een bericht toevoegt.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-128">Paste the URL into the box where you add a message.</span></span>

   ![Plak de Business Central-URL in Teams](media/teams-paste-url.png)
6. <span data-ttu-id="bcdb5-130">De eerste keer dat u een koppeling in een gesprek plakt, wordt u gevraagd u aan te melden bij [!INCLUDE [prodshort](includes/prodshort.md)] en toestemming te geven aan de app om gegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="bcdb5-131">Volg gewoon de instructies op het scherm.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bcdb5-132">U hoeft deze stap maar één keer uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="bcdb5-133">Wacht even terwijl er een kaart wordt gegenereerd in het berichtvenster.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="bcdb5-134">Als de kaart verschijnt, controleert u de inhoud van de kaart zorgvuldig op gevoelige informatie voordat u het bericht verzendt.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="bcdb5-135">Deze stap is belangrijk omdat zodra u het bericht verzendt, iedereen in het gesprek de kaart kan zien.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="bcdb5-136">Selecteer als de kaart er goed uitziet **Verzenden** om de kaart bij het gesprek in te dienen.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="bcdb5-137">Nadat de kaart is verschenen en voordat u **Verzenden** selecteert, kunt u de geplakte URL desgewenst verwijderen.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-137">After the card appears, and before you select **Send** , you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="bcdb5-138">Selecteer om meer details te bekijken of wijzigingen aan te brengen in de record **Details** .</span><span class="sxs-lookup"><span data-stu-id="bcdb5-138">To view more details or make changes to the record, select **Details** .</span></span>

    <span data-ttu-id="bcdb5-139">De detailpagina is vergelijkbaar met wat u zou zien in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="bcdb5-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="bcdb5-140">Maar het is enigszins ingekort voor Teams.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="bcdb5-141">Als u klaar bent met het bekijken en aanbrengen van wijzigingen, sluit u het venster om terug te keren naar het Teams-gesprek.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bcdb5-142">Alle wijzigingen die u aanbrengt, worden pas op de kaart weergegeven als u de koppeling de volgende keer in een gesprek plakt.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcdb5-143">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bcdb5-143">See Also</span></span>

[<span data-ttu-id="bcdb5-144">Integratieoverzicht van Business Central en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bcdb5-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="bcdb5-145">[De [!INCLUDE [prodshort](includes/prodshort.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="bcdb5-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="bcdb5-146">Ontwikkeling voor Teams-integratie</span><span class="sxs-lookup"><span data-stu-id="bcdb5-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="bcdb5-147">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="bcdb5-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
