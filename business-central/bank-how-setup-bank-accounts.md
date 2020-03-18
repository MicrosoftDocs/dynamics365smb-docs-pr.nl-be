---
title: Bankrekeningen instellen| Microsoft Docs
description: U kunt bankrekeningen reconciliëren met afschriften van de bank.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c0737bbecfd117dd65c8417c4b347da6b089305b
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076575"
---
# <a name="set-up-bank-accounts"></a>Bankrekeningen instellen
U gebruikt bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)] om uw banktransacties bij te houden. Bedragen op rekeningen kunnen worden uitgedrukt in de lokale valuta of in een vreemde valuta. Nadat u bankrekeningen hebt ingesteld, kunt u ook de optie voor het afdrukken van cheques gebruiken.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl]

## <a name="to-set-up-bank-accounts"></a>Bankrekeningen instellen
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies de desbetreffende koppeling.
2. Kies op de pagina **Bankrekeningen** de actie **Nieuw**.
3. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Als u wilt dat in het veld **Saldo** een beginsaldo wordt ingevuld, moet u een bankrekeningpost boeken met het bedrag in kwestie. U kunt dit doen door een bankrekeningreconciliatie uit te voeren. Zie [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie. U kunt echter ook het beginsaldo toepassen als onderdeel van het proces voor het maken van algemene gegevens in nieuwe bedrijven. U kunt dit doen met behulp van de begeleide-instelling **Bedrijfsgegevens migreren**. Zie voor meer informatie [Aan de slag](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Uw bankrekening instellen om bankbestanden te importeren of te exporteren
Velden op het sneltabblad **Transfer** op de pagina **Bankrekeningkaart** zijn gerelateerd om bankfeeds en -bestanden te importeren en te exporteren. Zie [De AMC Banking 365 Fundamentals-uitbreiding gebruiken](ui-extensions-amc-banking.md) en [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md) voor meer informatie over.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies de desbetreffende koppeling.
2. Open de kaart voor een bankrekening waarvoor u bankbestanden exporteert of importeert.
3. Vul indien nodig de velden op het sneltabblad **Transfer** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Andere services voor bestandsexport en de verschillende indelingen vereisen andere instellingswaarden op de pagina **Bankrekeningkaart**. U wordt over verkeerde of ontbrekende instellingswaarden geïnformeerd als u het bestand probeert te exporteren. Lees daarom de korte omschrijvingen van de velden zorgvuldig of raadpleeg de relateerde onderwerpen met procedures. Als u bijvoorbeeld een betalingsbestand voor een Noord-Amerikaanse elektronische betaling (EFT) exporteert, moeten daarvoor zowel het veld **Laatste afdrachtsadviesnr.** als **Transitnr.** zijn ingevuld. Zie voor meer informatie [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Bankrekeningen van leveranciers instellen voor de export van bankbestanden
Velden op het sneltabblad **Transfer** op de pagina **Bankrekeningkaart leverancier** zijn gerelateerd om bankfeeds en -bestanden te exporteren. Zie [De AMC Banking 365 Fundamentals-uitbreiding gebruiken](ui-extensions-amc-banking.md) en [Betalingen exporteren naar een bankbestand](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file) voor meer informatie.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies de desbetreffende koppeling.
2. Open de kaart voor een leverancier naar wiens bankrekening u betalingsbankbestanden exporteert.
3. Kies de actie **Bankrekeningen**.
3. Vul indien nodig de velden op de pagina **Bankrekeningkaart leverancier** op het sneltabblad **Transfer** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Zie ook
[Bankieren instellen](bank-setup-banking.md)  
[Boekingsgroepen instellen](finance-posting-groups.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
