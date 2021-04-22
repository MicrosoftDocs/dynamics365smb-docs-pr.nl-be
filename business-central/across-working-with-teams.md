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
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: e20208d50eb65f1a92e6661396bf53007ab88eb8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786894"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="287eb-103">Werken met Business Central-gegevens in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="287eb-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="287eb-104">[!INCLUDE [prod_short](includes/prod_short.md)] biedt een app die Microsoft Teams verbindt met uw bedrijfsgegevens in [!INCLUDE [prod_short](includes/prod_short.md)], zodat u snel details met teamleden kunt delen en sneller op vragen kunt reageren.</span><span class="sxs-lookup"><span data-stu-id="287eb-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="287eb-105">In dit artikel leert u hoe u de app gebruikt om [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens te delen met collega's in een Teams-gesprek.</span><span class="sxs-lookup"><span data-stu-id="287eb-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="287eb-106">Overzicht</span><span class="sxs-lookup"><span data-stu-id="287eb-106">Overview</span></span>

<span data-ttu-id="287eb-107">Met de [!INCLUDE [prod_short](includes/prod_short.md)]-app kunt u:</span><span class="sxs-lookup"><span data-stu-id="287eb-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="287eb-108">Een koppeling naar een Business Central-record kopiëren en plakken in een Teams-gesprek om met uw collega's te delen.</span><span class="sxs-lookup"><span data-stu-id="287eb-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="287eb-109">De app breidt de koppeling dan uit tot een compacte, interactieve kaart die informatie over de record weergeeft.</span><span class="sxs-lookup"><span data-stu-id="287eb-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="287eb-110">Eenmaal in het gesprek kunnen u en collega's meer details over de record bekijken, gegevens bewerken en actie ondernemen&mdash;zonder Teams te verlaten.</span><span class="sxs-lookup"><span data-stu-id="287eb-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="287eb-111">[![Teams-integratie met Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="287eb-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="287eb-112">Vereisten</span><span class="sxs-lookup"><span data-stu-id="287eb-112">Prerequisites</span></span>

- <span data-ttu-id="287eb-113">U hebt toegang tot Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="287eb-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="287eb-114">U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="287eb-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="287eb-115">Zie voor meer informatie [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren</span><span class="sxs-lookup"><span data-stu-id="287eb-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="287eb-116">Alle deelnemers aan een Teams-gesprek kunnen kaarten bekijken voor Business Central-records die u indient bij het gesprek.</span><span class="sxs-lookup"><span data-stu-id="287eb-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="287eb-117">Maar om meer details over records te bekijken door de knop **Details** of **Nieuw venster** op een kaart te gebruiken, hebben ze toegang nodig tot [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="287eb-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="287eb-118">Zie voor meer informatie [Microsoft Teams-integratie beheren](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="287eb-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="287eb-119">Een Business Central-kaart opnemen in een Teams-gesprek</span><span class="sxs-lookup"><span data-stu-id="287eb-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="287eb-120">Log in bij [!INCLUDE [prod_short](includes/prod_short.md)] met uw browser.</span><span class="sxs-lookup"><span data-stu-id="287eb-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="287eb-121">Open de record die u wilt delen.</span><span class="sxs-lookup"><span data-stu-id="287eb-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="287eb-122">De app is ontworpen om pagina's van het kaarttype weer te geven vanuit [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="287eb-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="287eb-123">Open dus een pagina met één record, zoals een artikel, klant of verkooporder.</span><span class="sxs-lookup"><span data-stu-id="287eb-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="287eb-124">U kunt de app niet gebruiken voor rolcentra of pagina's die meerdere records in een lijst weergeven.</span><span class="sxs-lookup"><span data-stu-id="287eb-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="287eb-125">Kopieer de volledige URL uit de adresbalk van de browser.</span><span class="sxs-lookup"><span data-stu-id="287eb-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Kopieer de Business Central-URL vanuit de browser](media/teams-url-v2.png)
4. <span data-ttu-id="287eb-127">Ga naar Teams en start een gesprek. Dat kan chatten met een persoon, een groep personen of een teamkanaal zijn.</span><span class="sxs-lookup"><span data-stu-id="287eb-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="287eb-128">Plak de URL in het berichtvak waarin u een bericht opstelt.</span><span class="sxs-lookup"><span data-stu-id="287eb-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Plak de Business Central-URL in Teams](media/teams-paste-url-v2.png)
6. <span data-ttu-id="287eb-130">De eerste keer dat u een koppeling in een gesprek plakt, wordt u gevraagd u aan te melden bij [!INCLUDE [prod_short](includes/prod_short.md)] en toestemming te geven aan de app om gegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="287eb-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="287eb-131">Volg gewoon de instructies op het scherm.</span><span class="sxs-lookup"><span data-stu-id="287eb-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="287eb-132">U hoeft deze stap maar één keer uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="287eb-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="287eb-133">Wacht even terwijl er een kaart wordt gegenereerd in het berichtvenster.</span><span class="sxs-lookup"><span data-stu-id="287eb-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="287eb-134">Als de kaart verschijnt, controleert u de inhoud van de kaart zorgvuldig op gevoelige informatie voordat u het bericht verzendt.</span><span class="sxs-lookup"><span data-stu-id="287eb-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="287eb-135">Deze stap is belangrijk omdat zodra u het bericht verzendt, iedereen in het gesprek de kaart kan zien.</span><span class="sxs-lookup"><span data-stu-id="287eb-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="287eb-136">Selecteer als de kaart er goed uitziet **Verzenden** om de kaart bij het gesprek in te dienen.</span><span class="sxs-lookup"><span data-stu-id="287eb-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="287eb-137">Nadat de kaart is verschenen en voordat u **Verzenden** selecteert, kunt u de geplakte URL desgewenst verwijderen.</span><span class="sxs-lookup"><span data-stu-id="287eb-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="287eb-138">Selecteer om meer details te bekijken of wijzigingen aan te brengen in de record die op de kaart wordt weergegeven, **Details**.</span><span class="sxs-lookup"><span data-stu-id="287eb-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="287eb-139">Zie de volgende sectie voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="287eb-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="287eb-140">Kaartdetails weergeven</span><span class="sxs-lookup"><span data-stu-id="287eb-140">View card details</span></span>

<span data-ttu-id="287eb-141">Zodra een kaart naar een gesprek is verzonden, kunnen alle deelnemers met de [juiste machtigingen](admin-teams-integration.md#permissions) **Details** selecteren om een venster te openen met meer informatie over de record&mdash;en eventueel wijzigingen aanbrengen in het record.</span><span class="sxs-lookup"><span data-stu-id="287eb-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="287eb-142">Het maakt niet uit of u degene bent die de kaart verstuurt of degene die de kaart ontvangt.</span><span class="sxs-lookup"><span data-stu-id="287eb-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="287eb-143">De functie **Details** is vooral handig voor ontvangers, omdat deze hen snel beknopte, gerichte informatie over de record biedt, in plaats van de volledige record te moeten scannen.</span><span class="sxs-lookup"><span data-stu-id="287eb-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="287eb-144">Het detailvenster is vergelijkbaar met wat u zou zien in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="287eb-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="287eb-145">Maar het is enigszins ingekort voor Teams.</span><span class="sxs-lookup"><span data-stu-id="287eb-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="287eb-146">Als u klaar bent met het bekijken en aanbrengen van wijzigingen, sluit u het venster om terug te keren naar het Teams-gesprek.</span><span class="sxs-lookup"><span data-stu-id="287eb-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="287eb-147">Hier zijn een paar dingen waarmee u rekening moet houden wanneer u met de kaartgegevens werkt:</span><span class="sxs-lookup"><span data-stu-id="287eb-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="287eb-148">Om de kaartdetails te openen moeten gebruikers de machtiging op de pagina en de gegevens ervan hebben in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="287eb-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="287eb-149">Kaarten in Teams-chats worden niet automatisch bijgewerkt met wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="287eb-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="287eb-150">Alle wijzigingen die u opslaat in een record in het detailvenster, worden opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="287eb-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="287eb-151">Maar de kaart in Teams geeft de wijzigingen in de conversie pas weer als u de koppeling opnieuw plakt.</span><span class="sxs-lookup"><span data-stu-id="287eb-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="287eb-152">Zie voor meer informatie over het werken met kaarten en kaartdetails [Veelgestelde vragen over Teams](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="287eb-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="287eb-153">Zie ook</span><span class="sxs-lookup"><span data-stu-id="287eb-153">See Also</span></span>

[<span data-ttu-id="287eb-154">Integratieoverzicht van Business Central en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="287eb-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="287eb-155">[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="287eb-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="287eb-156">Veelgestelde vragen over Teams</span><span class="sxs-lookup"><span data-stu-id="287eb-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="287eb-157">Problemen met Teams oplossen</span><span class="sxs-lookup"><span data-stu-id="287eb-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="287eb-158">Ontwikkeling voor Teams-integratie</span><span class="sxs-lookup"><span data-stu-id="287eb-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]