---
title: Contacten zoeken vanuit Microsoft Teams
description: Lees hoe u Business Central-klanten, -leveranciers en andere -contactpersonen opzoekt vanuit Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 6d094e365ad0c7da73467e5a3160d926902c45d9
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935173"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="9dc10-103">Zoeken naar klanten, leveranciers en andere contacten vanuit Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9dc10-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="9dc10-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="9dc10-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="9dc10-105">Geïntroduceerd in releasewave 1 van 2021.</span><span class="sxs-lookup"><span data-stu-id="9dc10-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="9dc10-106">[!INCLUDE [prod_short](includes/prod_short.md)] heeft een uitgebreid beheersysteem voor bedrijfscontacten dat essentieel is voor gebruikers in Sales, Operations of andere afdelingsrollen.</span><span class="sxs-lookup"><span data-stu-id="9dc10-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="9dc10-107">Als u een gebruiker bent in een van deze rollen, moet u vaak uw leveranciers, klanten en andere contacten opzoeken, ontmoeten of er een gesprek mee beginnen.</span><span class="sxs-lookup"><span data-stu-id="9dc10-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="9dc10-108">Met de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams kunt u deze taken rechtstreeks vanuit Teams uitvoeren, zonder dat u hoeft over te schakelen naar [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9dc10-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="9dc10-109">Vanuit Teams kunt u:</span><span class="sxs-lookup"><span data-stu-id="9dc10-109">From within Teams, you can:</span></span>

- <span data-ttu-id="9dc10-110">[!INCLUDE [prod_short](includes/prod_short.md)]-contacten opzoeken vanuit het Teams-opdrachtvak of vanuit het gebied voor het opstellen van berichten.</span><span class="sxs-lookup"><span data-stu-id="9dc10-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="9dc10-111">Contacten kunnen prospects, leveranciers, klanten of andere zakelijke relaties zijn.</span><span class="sxs-lookup"><span data-stu-id="9dc10-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="9dc10-112">Deel een contact als een kaart in een Teams-gesprek.</span><span class="sxs-lookup"><span data-stu-id="9dc10-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="9dc10-113">Bekijk details over contactpersonen, interactiegeschiedenis en andere inzichten, zoals openstaande betalingen of geopende documenten.</span><span class="sxs-lookup"><span data-stu-id="9dc10-113">View details about the contact, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9dc10-114">Vereisten</span><span class="sxs-lookup"><span data-stu-id="9dc10-114">Prerequisites</span></span>

- <span data-ttu-id="9dc10-115">U hebt toegang tot Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="9dc10-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="9dc10-116">U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="9dc10-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="9dc10-117">Zie voor meer informatie [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren</span><span class="sxs-lookup"><span data-stu-id="9dc10-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="9dc10-118">U hebt een [!INCLUDE [prod_short](includes/prod_short.md)]-account met toegang tot contacten in ten minste één bedrijf.</span><span class="sxs-lookup"><span data-stu-id="9dc10-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="9dc10-119">Of u nu zoekt vanuit het opdrachtvak of het berichtvenster, u wordt mogelijk gevraagd om u de eerste keer aan te melden of de app in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9dc10-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="9dc10-120">Deze stap is nodig om contactpersonen in het juiste Business Central-bedrijf te zoeken.</span><span class="sxs-lookup"><span data-stu-id="9dc10-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="9dc10-121">Zie voor informatie over het instellen van de app om uw bedrijf te kiezen [Bedrijf en andere instellingen in Teams wijzigen](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9dc10-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="9dc10-122">Contacten opzoeken vanuit het opdrachtvak</span><span class="sxs-lookup"><span data-stu-id="9dc10-122">Look up contacts from the command box</span></span>

<span data-ttu-id="9dc10-123">Het opdrachtvak staat bovenaan elk scherm in Teams.</span><span class="sxs-lookup"><span data-stu-id="9dc10-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="9dc10-124">Hiermee kunt u zoeken, snelle acties ondernemen of apps starten, zoals de [!INCLUDE [prod_short](includes/prod_short.md)]-app.</span><span class="sxs-lookup"><span data-stu-id="9dc10-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="9dc10-125">Zoeken vanuit het opdrachtvak is geweldig om snel contacten en hun gerelateerde gegevens op te zoeken voor eigen gebruik.</span><span class="sxs-lookup"><span data-stu-id="9dc10-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="9dc10-126">Stel dat u een e-mailadres van een leverancier wilt opzoeken om een agendavergadering te organiseren.</span><span class="sxs-lookup"><span data-stu-id="9dc10-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="9dc10-127">Of misschien wilt u interactiegeschiedenis opzoeken tijdens een gesprek met een klant.</span><span class="sxs-lookup"><span data-stu-id="9dc10-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="9dc10-128">Typ in het opdrachtvak **@Business Central** en selecteer vervolgens de Business Central-app uit de resultaten.</span><span class="sxs-lookup"><span data-stu-id="9dc10-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![De Business Central-app openen om vanuit het opdrachtvak naar contacten te zoeken](media/teams-contacts-command-1.png)

2. <span data-ttu-id="9dc10-130">Begin in het **Business Central**-vak met het typen van zoektekst, zoals een naam, adres of telefoonnummer.</span><span class="sxs-lookup"><span data-stu-id="9dc10-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="9dc10-131">Terwijl u typt, worden overeenkomende resultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9dc10-131">As you type, matching results will appear.</span></span>

    ![Business Central-contacten zoeken vanuit het opdrachtvak in Teams](media/teams-contacts-command-2.png)
3. <span data-ttu-id="9dc10-133">Selecteer een contact uit de resultaten.</span><span class="sxs-lookup"><span data-stu-id="9dc10-133">Select a contact from the results.</span></span>

    <span data-ttu-id="9dc10-134">De contactkaart verschijnt onder het opdrachtvak.</span><span class="sxs-lookup"><span data-stu-id="9dc10-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="9dc10-135">Als u de contactkaart aan een gesprek wilt toevoegen, gaat u naar de rechterbovenhoek van de kaart en selecteert u **... (Meer opties)** > **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="9dc10-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="9dc10-136">Plak vervolgens de kopie in het berichtopstelvak van een gesprek.</span><span class="sxs-lookup"><span data-stu-id="9dc10-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="9dc10-137">Zie voor meer algemene informatie over het opdrachtvak in Teams [Teams - het opdrachtvak gebruiken](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="9dc10-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="9dc10-138">Contacten opzoeken vanuit het berichtvak</span><span class="sxs-lookup"><span data-stu-id="9dc10-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="9dc10-139">Het voordeel van het opstellen van berichten is dat u een contactkaart rechtstreeks aan een gesprek kunt toevoegen, zodat anderen het kunnen zien.</span><span class="sxs-lookup"><span data-stu-id="9dc10-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="9dc10-140">Selecteer het **Business Central**-pictogram om de app te starten.</span><span class="sxs-lookup"><span data-stu-id="9dc10-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="9dc10-141">Als u het **Business Central**-pictogram niet ziet, selecteert u **... (Berichtextensies)**.</span><span class="sxs-lookup"><span data-stu-id="9dc10-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![De Business Central-app openen om vanuit het berichtvak naar contacten te zoeken](media/teams-contacts-message-box.png)

2. <span data-ttu-id="9dc10-143">Begin in het **Business Central**-vak met het typen van zoektekst, zoals een naam, adres of telefoonnummer.</span><span class="sxs-lookup"><span data-stu-id="9dc10-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="9dc10-144">Terwijl u typt, worden overeenkomende resultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9dc10-144">As you type, matching results will appear.</span></span>

    ![Business Central-contacten zoeken vanuit het berichtvak](media/teams-contacts-5.png)
3. <span data-ttu-id="9dc10-146">Selecteer een contact uit de resultaten.</span><span class="sxs-lookup"><span data-stu-id="9dc10-146">Select a contact from the results.</span></span>

    <span data-ttu-id="9dc10-147">De contactkaart wordt weergegeven in het berichtvak.</span><span class="sxs-lookup"><span data-stu-id="9dc10-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9dc10-148">De contactkaart wordt niet meteen naar het gesprek gestuurd zodat anderen deze kunnen zien.</span><span class="sxs-lookup"><span data-stu-id="9dc10-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="9dc10-149">U heeft de mogelijkheid om de inhoud van de kaart te bekijken en er naar wens tekst voor of achter toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="9dc10-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="9dc10-150">Stuur vervolgens uw bericht naar de chat als u klaar bent.</span><span class="sxs-lookup"><span data-stu-id="9dc10-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="9dc10-151">Hier is een andere manier</span><span class="sxs-lookup"><span data-stu-id="9dc10-151">Here's another way</span></span>

1. <span data-ttu-id="9dc10-152">In plaats van het **Business Central**-pictogram te gebruiken, typt u **@Business Central** rechtstreeks in het berichtvak.</span><span class="sxs-lookup"><span data-stu-id="9dc10-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="9dc10-153">Voer in het vak uw zoektermen in.</span><span class="sxs-lookup"><span data-stu-id="9dc10-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="9dc10-154">Gebruik de pijltoetsen omhoog en omlaag op het toetsenbord om een contact te kiezen en druk vervolgens op Enter om het te selecteren.</span><span class="sxs-lookup"><span data-stu-id="9dc10-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="9dc10-155">Contactkaartgegevens bekijken</span><span class="sxs-lookup"><span data-stu-id="9dc10-155">Viewing contact card details</span></span>

<span data-ttu-id="9dc10-156">De contactkaart in Teams geeft u een snel overzicht van de klant, de leverancier of het contact.</span><span class="sxs-lookup"><span data-stu-id="9dc10-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="9dc10-157">De kaart is interactief&mdash;wat betekent dat u meer informatie kunt bekijken of zelfs een contact kunt wijzigen met de knoppen **Details** of **Nieuw venster**.</span><span class="sxs-lookup"><span data-stu-id="9dc10-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="9dc10-158">De knop **Details** opent een venster binnen Teams met meer informatie over het contact, maar niet zoveel als u zou zien in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9dc10-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="9dc10-159">Om alle informatie over een contact te zien in [!INCLUDE [prod_short](includes/prod_short.md)], selecteert u **Nieuw venster**.</span><span class="sxs-lookup"><span data-stu-id="9dc10-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="9dc10-160">De contactkaart werkt net als kaarten voor records, zoals artikelen, klanten of verkooporders.</span><span class="sxs-lookup"><span data-stu-id="9dc10-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="9dc10-161">Zie voor meer informatie over kaarten [Kaartdetails weergeven](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="9dc10-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="9dc10-162">Alle deelnemers aan een Teams-gesprek kunnen kaarten bekijken voor Business Central-contacten die u indient bij een gesprek.</span><span class="sxs-lookup"><span data-stu-id="9dc10-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="9dc10-163">Maar om meer details over records te bekijken door de knop **Details** of **Nieuw venster** op een kaart te gebruiken, hebben ze toegang nodig tot [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9dc10-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="9dc10-164">Zie voor meer informatie [Microsoft Teams-integratie beheren](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="9dc10-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="9dc10-165">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9dc10-165">See Also</span></span>

[<span data-ttu-id="9dc10-166">Integratieoverzicht van Business Central en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9dc10-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="9dc10-167">[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="9dc10-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="9dc10-168">Veelgestelde vragen over Teams</span><span class="sxs-lookup"><span data-stu-id="9dc10-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="9dc10-169">Problemen met Teams oplossen</span><span class="sxs-lookup"><span data-stu-id="9dc10-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="9dc10-170">Ontwikkeling voor Teams-integratie</span><span class="sxs-lookup"><span data-stu-id="9dc10-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]