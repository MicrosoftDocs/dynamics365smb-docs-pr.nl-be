---
title: Salaristransacties importeren| Microsoft Docs
description: Als u salaris wilt beheren, importeert en boekt u financiële transacties vanuit uw salarisprovider naar het grootboek, met behulp van een salarisextensie zoals Ceridian of Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6bd078c6cf12023088dfa2f925e5a61bcc61778
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387461"
---
# <a name="import-payroll-transactions"></a><span data-ttu-id="354a0-103">Salaristransacties importeren</span><span class="sxs-lookup"><span data-stu-id="354a0-103">Import Payroll Transactions</span></span>
<span data-ttu-id="354a0-104">Als u salarisbetalingen en gerelateerde transacties wilt verantwoorden, moet u financiële transacties die zijn uitgevoerd door uw leverancier van salarisverwerking, importeren en boeken naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="354a0-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="354a0-105">Hiervoor importeert u eerst een bestand dat u van de leverancier van salarisverwerking ontvangt, op de pagina **Fin. dagboek**.</span><span class="sxs-lookup"><span data-stu-id="354a0-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="354a0-106">Vervolgens kunt u de externe rekeningen in het loonlijstbestand toewijzen aan de betreffende grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="354a0-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="354a0-107">Als laatste boekt u de loonlijsttransacties op basis van de rekeningtoewijzing.</span><span class="sxs-lookup"><span data-stu-id="354a0-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="354a0-108">Als u deze functionaliteit wilt gebruiken, moet een extensie voor salarisimport zijn geïnstalleerd en ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="354a0-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="354a0-109">De extensies voor import van bestanden van Ceridian Payroll en Quickbooks Payroll worden vooraf geïnstalleerd in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="354a0-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="354a0-110">Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met extensies](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="354a0-110">For more information, see [Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="354a0-111">Een salarisbestand importeren</span><span class="sxs-lookup"><span data-stu-id="354a0-111">To import a payroll file</span></span>
1. <span data-ttu-id="354a0-112">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="354a0-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="354a0-113">Kies in de relevante diversendagboekbatch de actie **Salaristransacties importeren**.</span><span class="sxs-lookup"><span data-stu-id="354a0-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="354a0-114">Er wordt een begeleide instelling geopend.</span><span class="sxs-lookup"><span data-stu-id="354a0-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="354a0-115">Volg de stappen op de pagina **Salaristransacties importeren**.</span><span class="sxs-lookup"><span data-stu-id="354a0-115">Follow the steps on the **Import Payroll Transactions** page.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="354a0-116">In de stap over het koppelen van de externe salarisrecords aan uw grootboekrekeningen, worden de koppelingen die u maakt, de volgende keer dat dezelfde records worden geïmporteerd, herinnerd.</span><span class="sxs-lookup"><span data-stu-id="354a0-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="354a0-117">Hierdoor bespaart u tijd omdat u niet handmatig het veld **Rekeningnr.** in het dagboek moet invullen steeds wanneer u doorlopende loonlijsttransacties hebt geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="354a0-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="354a0-118">Wanneer u de knop **OK** kiest in de begeleide instelling, wordt de pagina **Dagboek** gevuld met regels die de transacties voorstellen die het salarisbestand bevat, en met de relevante rekeningen vooraf ingevuld in de **Grootboekrekening**-velden volgens de koppelingen die u in de instelling kiest.</span><span class="sxs-lookup"><span data-stu-id="354a0-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** page is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="354a0-119">Bewerk of boek de dagboekregels zoals voor andere grootboektransacties.</span><span class="sxs-lookup"><span data-stu-id="354a0-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="354a0-120">Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="354a0-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="354a0-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="354a0-121">See Also</span></span>
[<span data-ttu-id="354a0-122">Financiën</span><span class="sxs-lookup"><span data-stu-id="354a0-122">Finance</span></span>](finance.md)  
<span data-ttu-id="354a0-123">[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="354a0-123">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="354a0-124">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="354a0-124">Working with General Journals</span></span>](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]