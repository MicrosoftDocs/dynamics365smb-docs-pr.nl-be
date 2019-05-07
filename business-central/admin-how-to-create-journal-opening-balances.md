---
title: Beginsaldi van dagboeken maken | Microsoft Docs
description: Business Central bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf. U kunt deze gegevens gemakkelijk overbrengen met dagboekboekingen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 535a899ed43e2d7112699fff9aa3ebc6f4289292
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "923824"
---
# <a name="create-journal-opening-balances"></a>Beginsaldi van dagboeken maken
[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf. U kunt deze gegevens eenvoudig overbrengen met het klantendagboek, leveranciersdagboek, artikeldagboek of financieel dagboek.

De eerste stap is het maken van een configuratiepakket dat de instellingentabellen voor deze dagboeken bevat. In de volgende procedure wordt ervan uitgegaan dat deze stap is voltooid. Zie [Bedrijfsconfiguratie instellen](admin-set-up-company-configuration.md) voor meer informatie. In de procedure worden de daaropvolgende stappen beschreven, waaronder de toepassing van het pakket dat wordt geleverd door een partner.  

Voordat u begint, moet u ervoor zorgen dat u zich bevindt op de rolcentrumpagina RapidStart Services-implementatie, want dat is de juiste context voor uw configuratiewerk. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>De posten in een dagboek toepassen op een nieuw bedrijf  
1. Configureer een nieuw bedrijf en pas een configuratiepakket toe. Zie voor meer informatie [Een bedrijf configureren met de wizard RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Het nieuwe bedrijf bevat geen informatie over beginsaldi van dagboeken.  

2. Open het configuratiewerkblad en importeer bestaande gegevens over klanten, artikelen, leveranciers en het grootboek. Zie voor meer informatie [Klantgegevens migreren](admin-migrate-customer-data.md).  
3. Kies bijvoorbeeld de actie **Grootboekjournaalregels maken**.  
4. Vul het sneltabblad **Opties** in en stel zo nodig filters in. Voer bijvoorbeeld in het veld **Dagboeksjabloon** een naam in.  
5. Kies de knop **OK**. De records bevinden zich nu in het dagboek, maar de bedragen zijn leeg.  
6. Exporteer de dagboektabel naar Excel en voer handmatig de gegevens voor boeking en tegenrekening in vanuit de oude gegevens.
7. Importeer en pas de tabelgegevens toe op het nieuwe bedrijf. De dagboekregels zijn gereed om te worden geboekt.  
8. Selecteer op het configuratiewerkblad de dagboekregeltabel en kies de actie **Databasegegevens**.  
9. Controleer de informatie en kies de actie **Boeken**.  
10. Herhaal de stappen voor het importeren en boeken van andere beginsaldi.  

## <a name="see-also"></a>Zie ook  
[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
