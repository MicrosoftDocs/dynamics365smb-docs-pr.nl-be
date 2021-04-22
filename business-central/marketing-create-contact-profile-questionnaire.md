---
title: Profielen gebruiken om contacten te classificeren
description: Profielvragenlijsten instellen om te helpen uw bedrijfscontactpersonen te classificeren
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 04/01/2021
ms.openlocfilehash: 31321ce4cafd17efc8a7732c81e874df1a1d763a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785510"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="f474d-103">Profielvragenlijsten gebruiken om bedrijfscontactpersonen te classificeren</span><span class="sxs-lookup"><span data-stu-id="f474d-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="f474d-104">U kunt profielvragenlijsten instellen die u wilt gebruiken wanneer u gegevens voor de profielen van de contacten invoert.</span><span class="sxs-lookup"><span data-stu-id="f474d-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="f474d-105">Binnen elke vragenlijst kunt u de verschillende vragen instellen die u aan uw contacten wilt stellen.</span><span class="sxs-lookup"><span data-stu-id="f474d-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="f474d-106">U kunt ook de vragenlijst uitvoeren om automatisch een aantal vragen te beantwoorden op basis van de contact-, klant- of leveranciersgegevens.</span><span class="sxs-lookup"><span data-stu-id="f474d-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="f474d-107">Een profielvragenlijst toevoegen</span><span class="sxs-lookup"><span data-stu-id="f474d-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="f474d-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vragenlijstinstellingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="f474d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f474d-109">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f474d-109">Choose the **New** Action.</span></span>  
3.  <span data-ttu-id="f474d-110">Vul de vereiste velden in.</span><span class="sxs-lookup"><span data-stu-id="f474d-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="f474d-111">Vragen toevoegen aan een profielvragenlijst</span><span class="sxs-lookup"><span data-stu-id="f474d-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="f474d-112">Kies de desbetreffende profielvragenlijst en kies de actie **Instelling van vragenlijst bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f474d-112">Choose the relevant profile questionnaire, and then choose the **Edit Questionnaire Setup** action.</span></span>  
2.  <span data-ttu-id="f474d-113">Kies op de eerste lege regel in het veld **Soort** de optie **Vraag**, en typ vervolgens uw vraag in het veld **Omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="f474d-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="f474d-114">Vul de overige velden op de regel in.</span><span class="sxs-lookup"><span data-stu-id="f474d-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="f474d-115">Klik op de volgende lege regel in het veld **Soort** en kies de optie **Antwoord**. Typ vervolgens uw antwoord in het veld **Omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="f474d-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="f474d-116">Selecteer de prioriteit in het veld **Prioriteit**.</span><span class="sxs-lookup"><span data-stu-id="f474d-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="f474d-117">In de velden **Van waarde** en **Naar waarde** definieert u een puntenbereik.</span><span class="sxs-lookup"><span data-stu-id="f474d-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="f474d-118">Contacten die punten krijgen binnen het gedefinieerde bereik ontvangen het antwoord.</span><span class="sxs-lookup"><span data-stu-id="f474d-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="f474d-119">Herhaal deze stappen om alle vragen en antwoorden in de profielvragenlijst in te voeren.</span><span class="sxs-lookup"><span data-stu-id="f474d-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="f474d-120">Nadat u een vragenlijst hebt gemaakt, moet u contactbeoordelingen maken om uw contacten te classificeren.</span><span class="sxs-lookup"><span data-stu-id="f474d-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="f474d-121">Het is ook mogelijk om vragen zo in te stellen dat ze automatisch worden geclassificeerd op basis van de informatie op de contactkaart.</span><span class="sxs-lookup"><span data-stu-id="f474d-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="f474d-122">Als u een automatisch te beantwoorden vraag invoert, klikt u op <STRONG>Regel</STRONG> en kiest u vervolgens <STRONG>Vraagdetails</STRONG> om de criteria in te voeren voor het beantwoorden van de vraag.</span><span class="sxs-lookup"><span data-stu-id="f474d-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="f474d-123">De automatische classificatie van contactpersonen</span><span class="sxs-lookup"><span data-stu-id="f474d-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="f474d-124">U kunt de contacten automatisch indelen op basis van klant-, leveranciers- en contactgegevens, door automatisch beantwoorde profielvragen in te stellen op de pagina **Profielvragenlijstinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="f474d-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="f474d-125">Een classificatie op basis van klantgegevens kan alleen worden toegewezen aan contacten die als klant zijn geregistreerd. Een classificatie op basis van leveranciersgegevens kan alleen worden toegewezen aan contacten die als leverancier zijn geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="f474d-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="f474d-126">De automatische classificatie wordt niet automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f474d-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="f474d-127">Daarom wilt u de profielvragenlijsten mogelijk bijwerken, nadat u de klant-, leveranciers- of contactgegevens waarop de profielvragenlijsten zijn gebaseerd, hebt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f474d-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="f474d-128">Nadat u de automatisch beantwoorde profielvragen hebt ingesteld en als u de profielvragenlijst met deze vragen aan een contact toewijst, worden de juiste antwoorden voor het contact automatisch door [!INCLUDE[prod_short](includes/prod_short.md)] toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f474d-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[prod_short](includes/prod_short.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="f474d-129">Opmerking</span><span class="sxs-lookup"><span data-stu-id="f474d-129">Example</span></span>
<span data-ttu-id="f474d-130">U kunt de contacten indelen op basis van de aantallen die ze bij u hebben gekocht:</span><span class="sxs-lookup"><span data-stu-id="f474d-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f474d-131"><strong>Antwoord</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="f474d-132"><strong>Van toepassing op</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f474d-133">A</span><span class="sxs-lookup"><span data-stu-id="f474d-133">A</span></span></p></td>
<td><p><span data-ttu-id="f474d-134">contacten die voor 500.000 LV of meer hebben gekocht</span><span class="sxs-lookup"><span data-stu-id="f474d-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f474d-135">B</span><span class="sxs-lookup"><span data-stu-id="f474d-135">B</span></span></p></td>
<td><p><span data-ttu-id="f474d-136">contacten die voor tussen 100.000 en 499.999 LV hebben gekocht</span><span class="sxs-lookup"><span data-stu-id="f474d-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f474d-137">U</span><span class="sxs-lookup"><span data-stu-id="f474d-137">C</span></span></p></td>
<td><p><span data-ttu-id="f474d-138">contacten die voor 99.999 LV of minder hebben gekocht</span><span class="sxs-lookup"><span data-stu-id="f474d-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f474d-139">Hiervoor moet u de pagina **Profielvragenlijstinstellingen** als volgt invullen:</span><span class="sxs-lookup"><span data-stu-id="f474d-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f474d-140"><strong>Soort</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="f474d-141"><strong>Beschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="f474d-142"><strong>Automatische indeling</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="f474d-143"><strong>Van waarde</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="f474d-144"><strong>Naar waarde</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f474d-145">Vraag</span><span class="sxs-lookup"><span data-stu-id="f474d-145">Question</span></span></p></td>
<td><p><span data-ttu-id="f474d-146">ABC-classificatie</span><span class="sxs-lookup"><span data-stu-id="f474d-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="f474d-147">Klik op het selectievakje om het in te schakelen</span><span class="sxs-lookup"><span data-stu-id="f474d-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f474d-148">Antwoord</span><span class="sxs-lookup"><span data-stu-id="f474d-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="f474d-149">A</span><span class="sxs-lookup"><span data-stu-id="f474d-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f474d-150">500.000</span><span class="sxs-lookup"><span data-stu-id="f474d-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f474d-151">Antwoord</span><span class="sxs-lookup"><span data-stu-id="f474d-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="f474d-152">B</span><span class="sxs-lookup"><span data-stu-id="f474d-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f474d-153">100,000</span><span class="sxs-lookup"><span data-stu-id="f474d-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="f474d-154">499,999</span><span class="sxs-lookup"><span data-stu-id="f474d-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f474d-155">Antwoord</span><span class="sxs-lookup"><span data-stu-id="f474d-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="f474d-156">U</span><span class="sxs-lookup"><span data-stu-id="f474d-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f474d-157">99,999</span><span class="sxs-lookup"><span data-stu-id="f474d-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f474d-158">Vul vervolgens de pagina **Profielvraagdetails** als volgt in:</span><span class="sxs-lookup"><span data-stu-id="f474d-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f474d-159"><strong>Veld</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="f474d-160"><strong>Waarde</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f474d-161"><strong>Veld Klantclassificatie</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="f474d-162"><emphasis>Verkoop (LV)</emphasis></span><span class="sxs-lookup"><span data-stu-id="f474d-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f474d-163"><strong>Indelingsmethode</strong></span><span class="sxs-lookup"><span data-stu-id="f474d-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="f474d-164"><emphasis>Waarde</emphasis></span><span class="sxs-lookup"><span data-stu-id="f474d-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f474d-165">Wanneer u de profielvragenlijst met deze vraag aan een contact toewijst, wordt het relevante antwoord voor dit contact automatisch ingevoerd op de profielregels van de contactkaart.</span><span class="sxs-lookup"><span data-stu-id="f474d-165">When you assign the profile questionnaire containing this question to a contact, application automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="f474d-166">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f474d-166">See Also</span></span>
[<span data-ttu-id="f474d-167">Contacten maken</span><span class="sxs-lookup"><span data-stu-id="f474d-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]