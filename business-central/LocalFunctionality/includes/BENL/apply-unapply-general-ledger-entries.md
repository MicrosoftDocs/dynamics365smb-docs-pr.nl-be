---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 08/26/2020
ms.author: edupont
ms.openlocfilehash: 93d76a02edbf05f022275850a3a0377071ab9cdb
ms.sourcegitcommit: 3e2eab6920e96596cb4b3c61e590a8c577e8b630
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/27/2020
ms.locfileid: "3731359"
---
<span data-ttu-id="e3ee8-101">Door tijdelijke grootboekposten toe te passen, kunnen bedrijven werken met tijdelijke en transferaccounts in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-101">By applying temporary general ledger entries, companies can work with temporary and transfer accounts in the general ledger.</span></span> <span data-ttu-id="e3ee8-102">Tijdelijke en transferrekeningen worden gebruikt om tijdelijke posten op te slaan die op verdere verwerking in het grootboek wachten.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-102">Temporary and transfer accounts are used to store temporary ledger entries that are waiting for further processing into the general ledger.</span></span>  

<span data-ttu-id="e3ee8-103">U kunt tijdelijke rekeningen gebruiken voor:</span><span class="sxs-lookup"><span data-stu-id="e3ee8-103">You can use temporary accounts for:</span></span>  

- <span data-ttu-id="e3ee8-104">Geldtransfers van de ene naar de andere bankrekening.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-104">Money transfers from one bank account to another.</span></span>  
- <span data-ttu-id="e3ee8-105">Financiële transactietransfers van het ene systeem naar het andere, waarbij een deel van de gegevens tijdelijk op het oorspronkelijke systeem staat.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-105">Financial transaction transfers from one system to another in which part of the information temporarily resides on the original system.</span></span>  
- <span data-ttu-id="e3ee8-106">Transacties waarvoor u een verkoopfactuur hebt verzonden naar een klant maar nog niet de bijbehorende inkoopfactuur van de leverancier hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-106">Transactions for which you have issued a sales invoice to a customer but have not yet received the corresponding purchase invoice from the vendor.</span></span>  

<span data-ttu-id="e3ee8-107">Nadat de posten zijn verwerkt, kunt u de functie **Posten vereffenen** gebruiken om de geboekte posten en het boekingsrekeningsoort bij te werken.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-107">When the ledger entries have been processed, you can use the **Apply Entries** function to update the posted ledger entries and the posting account type.</span></span>  

<span data-ttu-id="e3ee8-108">U kunt de vereffening van de vereffende grootboekposten ongedaan maken en vervolgens de gesloten posten openen om wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-108">You can unapply the applied general ledger entries and then open the closed entries to make changes.</span></span>  

## <a name="to-apply-general-ledger-entries"></a><span data-ttu-id="e3ee8-109">Grootboekposten vereffenen</span><span class="sxs-lookup"><span data-stu-id="e3ee8-109">To apply general ledger entries</span></span>  

1. <span data-ttu-id="e3ee8-110">Kies het pictogram ![lampje dat de functie Vertel me opent](../../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekjournalen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-110">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Registers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e3ee8-111">Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-111">Select a general ledger register, and then choose the **General Ledger** action.</span></span>  
3. <span data-ttu-id="e3ee8-112">Kies op de pagina **Grootboekposten** de actie **Posten vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-112">On the **General Ledger Entries** page, choose the **Apply Entries** action.</span></span>  

    <span data-ttu-id="e3ee8-113">Alle openstaande posten voor de grootboekrekening worden weergegeven op de pagina **Grootboekposten vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-113">All open ledger entries for the general ledger account are displayed on the **Apply General Ledger Entries** page.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="e3ee8-114">Standaard wordt het veld **Posten opnemen** ingesteld op **Open**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-114">By default, the **Include Entries** field is set to **Open**.</span></span> <span data-ttu-id="e3ee8-115">U kunt de waarde van het veld **Posten opnemen** wijzigen in **Alle** of **Afgesloten**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-115">You can change the value of the **Include Entries** field to **All** or **Closed**.</span></span> <span data-ttu-id="e3ee8-116">U kunt alleen grootboekposten vereffenen die **open** zijn.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-116">You can only apply general ledger entries that are **Open**.</span></span>  

4. <span data-ttu-id="e3ee8-117">Selecteer de relevante grootboekpost en kies de actie **Set van toepassing op id**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-117">Select the relevant general ledger entry, and then choose the **Set Applies-to ID** action.</span></span>  

    <span data-ttu-id="e3ee8-118">Het veld **Vereffenings-id** wordt bijgewerkt met de gebruikers-id.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-118">The **Applies-to ID** field is updated with the user ID.</span></span> <span data-ttu-id="e3ee8-119">Het restbedrag wordt weergegeven op de pagina **Saldo** in het venster **Grootboekposten vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-119">The remaining amount is displayed in the **Balance** field on the **Apply General Ledger Entries** page.</span></span>  
5. <span data-ttu-id="e3ee8-120">Kies de actie **Vereffening boeken**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-120">Choose the **Post Application** action.</span></span>  

    <span data-ttu-id="e3ee8-121">U kunt de vereffening boeken zelfs wanneer het saldobedrag gelijk is aan 0.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-121">You can post the application even if the balance amount is equal to 0.</span></span> <span data-ttu-id="e3ee8-122">Wanneer wordt geboekt, wordt het veld **Restbedrag** als volgt beïnvloed:</span><span class="sxs-lookup"><span data-stu-id="e3ee8-122">When posted, the **Remaining Amount** field is affected as follows:</span></span>  

    - <span data-ttu-id="e3ee8-123">Als het veld **Saldo** gelijk is aan 0, wordt het veld **Restbedrag** bij alle grootboekposten op 0 gezet.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-123">If the **Balance** is equal to 0, then the **Remaining Amount** field on all ledger entries is set to 0.</span></span>  

    - <span data-ttu-id="e3ee8-124">Als het veld **Saldo** niet gelijk is aan 0, wordt het bedrag in het veld **Saldo** overgebracht naar het veld **Restbedrag** van de grootboekpost die was geselecteerd toen u de vereffening boekte.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-124">If the **Balance** is not equal to 0, then the amount in the **Balance** field is transferred to the **Remaining Amount** field for the general ledger entry that was selected when you posted the application.</span></span>  

    - <span data-ttu-id="e3ee8-125">Voor alle overige grootboekposten wordt het veld **Restbedrag** op 0 gezet en worden de velden **Open**, **Afgesloten door volgnr.**, **Afgesloten met bedrag** en **Afgesloten op** bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-125">For all other general ledger entries, the **Remaining Amount** field is set to 0 and the **Open**, **Closed by Entry No.**, **Closed by Amount**, and **Closed at Date** fields are updated.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="e3ee8-126">Wanneer wordt geboekt, worden de grootboekposten die het veld **Vereffenings-id** bijwerken, verwijderd.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-126">When posted, the general ledger entries which update the **Applies-to ID** field are deleted.</span></span>  

6. <span data-ttu-id="e3ee8-127">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-127">Choose the **OK** button.</span></span>  

## <a name="to-view-the-applied-general-ledger-entries"></a><span data-ttu-id="e3ee8-128">De vereffende grootboekposten weergeven</span><span class="sxs-lookup"><span data-stu-id="e3ee8-128">To view the applied general ledger entries</span></span>  

1. <span data-ttu-id="e3ee8-129">Kies het pictogram ![lampje dat de functie Vertel me opent](../../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekjournalen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-129">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Registers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e3ee8-130">Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-130">Select a general ledger register, and then choose the **General Ledger** action.</span></span>  
3. <span data-ttu-id="e3ee8-131">Selecteer de betreffende grootboekpost en kies de actie **Vereffende posten**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-131">Select the relevant general ledger entry, and then choose the **Applied Entries** action.</span></span>  

    <span data-ttu-id="e3ee8-132">U kunt alle vereffende grootboekposten weergeven.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-132">You can view all the applied general ledger entries.</span></span>  

4. <span data-ttu-id="e3ee8-133">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-133">Choose the **OK** button.</span></span>  

## <a name="to-unapply-general-ledger-entries"></a><span data-ttu-id="e3ee8-134">De vereffening van grootboekposten ongedaan maken</span><span class="sxs-lookup"><span data-stu-id="e3ee8-134">To unapply general ledger entries</span></span>  

1. <span data-ttu-id="e3ee8-135">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekjournalen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-135">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Registers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e3ee8-136">Selecteer een grootboekjournaal en kies vervolgens de actie **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-136">Select a general ledger register, and then choose the **General Ledger** action.</span></span>  
3. <span data-ttu-id="e3ee8-137">Selecteer de grootboekpost waarvan u de vereffening ongedaan wilt maken en kies vervolgens de actie **Vereffening ongedaan maken**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-137">Select the general ledger entry that you want to unapply, and then choose the **Undo Application** action.</span></span>  

    <span data-ttu-id="e3ee8-138">De vereffening van de vereffende grootboekposten wordt ongedaan gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-138">The applied general ledger entries are unapplied.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="e3ee8-139">Als een post is vereffend met meer dan één vereffeningspost, moet u de vereffening van de laatste vereffeningspost het eerst ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-139">If an entry is applied to more than one application entry, you must unapply the latest application entry first.</span></span> <span data-ttu-id="e3ee8-140">Standaard wordt de laatste post weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-140">By default, the latest entry is displayed.</span></span>  

4. <span data-ttu-id="e3ee8-141">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3ee8-141">Choose the **OK** button.</span></span>  
