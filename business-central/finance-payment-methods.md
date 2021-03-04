---
title: Betalingsmethoden instellen
description: U gebruikt betalingswijzen, bijvoorbeeld cheque, bankoverschrijving, contant geld of PayPal, om te bepalen hoe verkoop- en inkoopfacturen worden betaald.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 01/21/2021
ms.author: bholtorf
ms.openlocfilehash: 78e754998c7adc871b57347ff0bed714db8cc83f
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035368"
---
# <a name="set-up-payment-methods"></a>Betalingsmethoden instellen

Betalingswijzen definiëren hoe u wilt dat klanten u betalen en hoe u uw leveranciers wilt betalen. De methode kan voor elke klant of leverancier variëren. Voorbeelden van gangbare betalingswijzen zijn **bank**, **contant**, **cheque** of **rekening**.

U kunt een betalingswijze aan klanten en leveranciers toewijzen zodat altijd dezelfde wijze wordt gebruikt op de verkoop- en inkoopdocumenten die u voor hen maakt. Indien nodig kunt u de methode in het verkoop- of inkoopdocument wijzigen. Bijvoorbeeld wanneer u een bepaalde inkoopfactuur in contant geld in plaats van met cheque wilt betalen. Dit verandert niet de standaardbetalingswijze die aan de leverancier is toegewezen.

Voor verkoop- en inkoopdocumenten worden dezelfde betalingswijzen gebruikt. Bijvoorbeeld een _cash_ betalingswijze wordt gebruikt als u betalingen doet en wanneer u ze ontvangt. [!INCLUDE[prod_short](includes/prod_short.md)] weet dat wanneer u een verkoopfactuur maakt, u verwacht betaling te ontvangen en voor inkoopfacturen het tegenovergestelde.

Creditnota's voor retouren zijn echter uitzonderingen, omdat geld in tegenovergestelde richtingen stroomt, van u naar uw klant en van uw leverancier naar u. Daarom wordt geen standaardbetalingswijze toegewezen aan creditnota's. Er is echter een oplossing als u betalingsvoorwaarden voor de klant of leverancier hebt opgegeven. Hoewel het veld **Cont.-kort. op creditnota's berekenen** hier niet bedoeld voor is, wordt als u het selectievakje op de pagina **Betalingscondities** inschakelt, een standaardbetalingswijze toegevoegd wanneer u een creditnota maakt. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Een betalingswijze instellen

[!INCLUDE[prod_short](includes/prod_short.md)] biedt een paar betalingswijzen die bedrijven vaak gebruiken. U kunt er echter zo veel toevoegen als u wilt.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsmethoden** in en kies de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Wijs desgewenst betalingsvoorwaarden toe aan uw betalingsmethode. Zie voor meer informatie [Betalingsvoorwaarden instellen](finance-payment-terms.md) voor meer informatie.  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Een betalingswijze aan een klant of leverancier toewijzen

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies de desbetreffende koppeling.
2. Kies in het veld **Betalingswijze** de methode die standaard moet worden gebruikt voor de klant of leverancier.

## <a name="see-also"></a>Zie ook

[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Betalingsvoorwaarden instellen](finance-payment-terms.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]