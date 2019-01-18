---
title: Contacten synchroniseren met klanten en leveranciers| Microsoft Docs
description: "U koppelt of synchroniseert contactgegevens van contacten die tevens klanten, leveranciers of bankrekeningen zijn, zodat u de gegevens slechts op één locatie hoeft bij te werken."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 736d1329b3d3c2e9367972c2a2fb9e2af0080c85
ms.contentlocale: nl-be
ms.lasthandoff: 12/11/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="74331-103">Contacten synchroniseren met klanten, leveranciers en bankrekeningen</span><span class="sxs-lookup"><span data-stu-id="74331-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="74331-104">Als sommige van uw contacten ook klanten, leveranciers of bankrekeningen zijn, kunt u de contactgegevens synchroniseren met de desbetreffende klant, leverancier of bankrekening.</span><span class="sxs-lookup"><span data-stu-id="74331-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="74331-105">Synchronisatie maakt gegevens die gemeenschappelijk zijn voor contacten en klanten, leveranciers of bankrekeningen hetzelfde.</span><span class="sxs-lookup"><span data-stu-id="74331-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

<span data-ttu-id="74331-106">Voordat u uw contacten kunt synchroniseren met klanten, leveranciers of bankrekeningen, moet u een zakenrelatiecode voor klanten, leveranciers en of bankrekeningen opgeven op de pagina **Marketinginstellingen**.</span><span class="sxs-lookup"><span data-stu-id="74331-106">Before you can synchronize your contacts with customers, vendors, or bank accounts, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="74331-107">Zie voor meer informatie [CRM instellen](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="74331-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="74331-108">Andere manieren om contacten te synchroniseren met klanten, leveranciers en bankrekeningen</span><span class="sxs-lookup"><span data-stu-id="74331-108">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="74331-109">U kunt de contacten met drie methoden synchroniseren met klanten, leveranciers en/of bankrekeningen:</span><span class="sxs-lookup"><span data-stu-id="74331-109">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="74331-110">Contacten koppelen aan bestaande klanten, leveranciers en/of bankrekeningen op de contactkaart.</span><span class="sxs-lookup"><span data-stu-id="74331-110">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="74331-111">Zie voor meer informatie [Contacten koppelen aan klanten, leveranciers en bankrekeningen](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="74331-111">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="74331-112">Maak klanten,, leveranciers of bankrekeningen vanuit het contact.</span><span class="sxs-lookup"><span data-stu-id="74331-112">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="74331-113">Zie voor meer informatie [Een klant, leverancier of bankrekening maken van een contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="74331-113">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="74331-114">Contacten maken van klanten, leveranciers of bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="74331-114">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="74331-115">Zie voor meer informatie [Een bedrijfscontact maken van een klant, leverancier of bankrekening](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="74331-115">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="74331-116">Gevolgen van synchronisatie</span><span class="sxs-lookup"><span data-stu-id="74331-116">Consequences of Synchronization</span></span>
<span data-ttu-id="74331-117">Wanneer het contact wordt gesynchroniseerd met de klant-, leveranciers- of bankrekening:</span><span class="sxs-lookup"><span data-stu-id="74331-117">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="74331-118">Hoeft u de gegevens slechts op één locatie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="74331-118">You only have to update information in one place.</span></span> <span data-ttu-id="74331-119">Als u bijvoorbeeld het telefoonnummer op de contactkaart wijzigt, wordt het telefoonnummer automatisch bijgewerkt met dezelfde wijziging als van de klant, leveranciers of bankrekening.</span><span class="sxs-lookup"><span data-stu-id="74331-119">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="74331-120">Als u een klanten-, leveranciers- of bankrekeningkaart maakt en een nummerreeks voor contacten hebt opgegeven, wordt er automatisch een contactkaart gemaakt voor de klant, leverancier of bankrekening.</span><span class="sxs-lookup"><span data-stu-id="74331-120">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="74331-121">U kunt verkoopoffertes, inkoopoffertes, verkoop- en inkooporders maken vanuit het contact.</span><span class="sxs-lookup"><span data-stu-id="74331-121">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="74331-122">U kunt uw interacties laten vastleggen wanneer u bepaalde acties uitvoert zoals orders, raamcontracten afdrukken, verkoopserviceorders maken, e-mailberichten verzenden, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="74331-122">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="74331-123">Als u een contact verwijdert dat aan een klant, leverancier of bankrekening is gekoppeld, wordt alleen het contact verwijderd.</span><span class="sxs-lookup"><span data-stu-id="74331-123">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="74331-124">De klant, leverancier of bankrekening blijft.</span><span class="sxs-lookup"><span data-stu-id="74331-124">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="74331-125">Als u een klant, leverancier of bankrekening verwijdert die aan een contact is gekoppeld, blijft het contact.</span><span class="sxs-lookup"><span data-stu-id="74331-125">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="74331-126">Sommige details, zoals facturerings- en boekingsgegevens, worden niet weergegeven op de contactkaart.</span><span class="sxs-lookup"><span data-stu-id="74331-126">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="74331-127">Mogelijk wilt u deze handmatig toevoegen op de klanten-, leveranciers- of bankrekeningkaart wanneer u klanten, leveranciers of bankrekeningen van contacten maakt.</span><span class="sxs-lookup"><span data-stu-id="74331-127">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="74331-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="74331-128">See Also</span></span>
[<span data-ttu-id="74331-129">Contactpersonen beheren</span><span class="sxs-lookup"><span data-stu-id="74331-129">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="74331-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="74331-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

