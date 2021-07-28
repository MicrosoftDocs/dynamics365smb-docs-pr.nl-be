---
title: 'Procedure: beginsaldi van dagboeken maken'
description: Batchverwerkingen worden geleverd om oude rekeningsaldi over te dragen naar een nieuw geconfigureerd bedrijf. U kunt deze gegevens gemakkelijk overbrengen met dagboekboekingen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: ac7fea479237d985204820d54953689566f5c2ac
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6319550"
---
# <a name="create-journal-opening-balances"></a>Beginsaldi van dagboeken maken

[!INCLUDE[prod_short](includes/prod_short.md)] bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf. U kunt deze gegevens eenvoudig overbrengen met het klantendagboek, leveranciersdagboek, artikeldagboek of financieel dagboek.

De eerste stap is het maken van een configuratiepakket dat de instellingentabellen voor deze dagboeken bevat. In de volgende procedure wordt ervan uitgegaan dat deze stap is voltooid. Zie [Bedrijfsconfiguratie instellen](admin-set-up-company-configuration.md) voor meer informatie. In de procedure worden de daaropvolgende stappen beschreven, waaronder de toepassing van het pakket dat wordt geleverd door een partner.  

Voordat u begint, moet u ervoor zorgen dat u de rolcentrumpagina Beheer gebruikt, omdat dit de juiste context voor uw configuratiewerk is. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>De posten in een dagboek toepassen op een nieuw bedrijf

1. Configureer een nieuw bedrijf en pas een configuratiepakket toe. Zie voor meer informatie [Een bedrijf configureren met de wizard RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Het nieuwe bedrijf bevat geen informatie over beginsaldi van dagboeken.  

2. Open het configuratiewerkblad en importeer bestaande gegevens over klanten, artikelen, leveranciers en het grootboek. Zie voor meer informatie [Klantgegevens migreren](admin-migrate-customer-data.md).  

    Nu beschikt u over hoofdgegevens. Vervolgens voegt u de beginsaldi toe. De volgende stappen beschrijven hoe u dagboekregels voor grootboekrekeningen maakt, maar hetzelfde geldt voor het maken van dagboekregels voor klanten, leveranciers en artikelen.  
3. Kies de actie **Grootboekrekeningregels maken**.  
4. Vul het sneltabblad **Opties** in en stel zo nodig filters in. Voer bijvoorbeeld in het veld **Dagboeksjabloon** een naam in.  
5. Kies de knop **OK**. De records bevinden zich nu in het dagboek, maar de bedragen zijn leeg.  
6. Exporteer de dagboektabel naar Excel en voer handmatig de gegevens voor boeking en tegenrekening in vanuit de oude gegevens.
7. Importeer en pas de tabelgegevens toe op het nieuwe bedrijf. De dagboekregels zijn gereed om te worden geboekt.  
8. Selecteer op het configuratiewerkblad de dagboekregeltabel en kies de actie **Databasegegevens**.  
9. Controleer de informatie en kies de actie **Boeken**.  
10. Herhaal de stappen voor het importeren en boeken van andere beginsaldi.  

> [!TIP]
> U kunt dezelfde batchtaken gebruiken om beginsaldi toe te voegen wanneer u een nieuwe klant of leverancier registreert waarmee u eerder zaken hebt gedaan, maar niet geregistreerd in [!INCLUDE [prod_short](includes/prod_short.md)]. Zoek gewoon naar de relevante taak en kies vervolgens de relevante koppeling.

## <a name="see-also"></a>Zie ook

[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]