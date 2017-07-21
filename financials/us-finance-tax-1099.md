---
title: 1099-transacties rapporteren in de Verenigde Staten | Microsoft Docs
description: De IRS vereist het belastingformulier 1099 voor betalingen aan leveranciers en u kunt opgeven dat een inkoopdocument 1099-plichtig is en de code 1099 opgeven voor de leverancier.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a>Transacties rapporteren als 1099-plichtig in de Verenigde Staten

De Internal Revenue Service (IRS) vereist een of meerdere versies van het 1099-belastingformulier voor betalingen aan leveranciers. Kopieën van deze formulieren moeten jaarlijks op of voor de laatste dag van januari aan leveranciers worden verzonden. In uw inkoopdocumenten kunt u opgeven dat het document onder 1099 valt en u kunt de 1099-code voor de leverancier opgeven.  

## <a name="1099-codes"></a>1099-codes
In [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn de meest gebruikte 1099-codes al voor u ingesteld zodat u gereed bent om de vereiste rapporten te genereren. De codes worden gedefinieerd in het venster **IRS 1099-formuliervak**, waar u ook nieuwe 1099-codes kunt toevoegen. Voor elke belastingplichtige leverancier kunt u de relevante 1099-code opgeven op het sneltabblad **Betalingen** op de leverancierskaart.  

Met het rapport **1099-gegevens van leverancier** kunt u 1099-transacties controleren die in een bepaalde periode zijn betaald. Aan het einde van het jaar kunt u 1099-transacties afdrukken op voorbedrukte formulieren.  

## <a name="printing-1099-tax-forms"></a>1099-belastingformulieren afdrukken
Vanuit het venster **IRS 1099-formuliervak** kunt u de volgende belastingformulieren openen:  

* Leverancier Afd 1099.  

  Drukt het federale formulier Afd. 1099 af voor dividenden en distributie. U kunt alle of alleen bepaalde Afd 1099-formulieren afdrukken. Het rapport gebruikt de codes die gelden voor de bedragvakken van het Afd-formulier uit het venster **IRS 1099-formuliervak**.  
* Leverancier Rnt 1099  

  Drukt het federale formulier Rnt 1099 voor inkomsten uit rente af. U kunt alle of alleen bepaalde Rnt 1099-formulieren afdrukken. Het rapport gebruikt de codes die van toepassing zijn op de bedragvakken van het Rnt-formulier uit het venster **IRS 1099-formuliervak**.  
* Leverancier 1099 Div - diverse inkomsten  

  Drukt het federale formulier 1099 Div af voor diverse inkomsten. U kunt alle of alleen bepaalde 1099 Rnt-formulieren afdrukken. Het rapport gebruikt de codes die gelden voor de bedragvakken van het Div-formulier uit het venster **IRS 1099-formuliervak**.  

Regelgevende wijzigingen die invloed hebben op dit rapport en de tabelgegevens, worden meestal verwerkt in eindejaarsupdates.
Het kan handig zijn het rapport **1099-gegevens van leverancier** uit te voeren om de gegevens te bekijken voordat u de formulieren afdrukt.

## <a name="submitting-1099-tax-forms-electronically"></a>1099-belastingformulieren elektronisch indienen
Als u de 1099-belastingformulieren elektronisch wilt indienen, gebruikt u het rapport **1099 magnetische media van leverancier**. Geeft de 1099-formulieren op die kunnen worden geëxporteerd. De formulierinformatie die door dit rapport wordt geëxporteerd, is hetzelfde als de rapporten die 1099-formulieren afdrukken die in de vorige sectie worden beschreven.  

Het rapport gebruikt de codes die van toepassing zijn op de bedragvakken uit het venster **IRS 1099-formuliervak**. De codes worden gekoppeld aan de formuliervakken in de bestandsindelingen van dit rapport. Daarom moet de versie van de tabelgegevens en van het rapport voor een bepaald belastingjaar overeenstemmen. Als er aangepaste codes aan de tabel worden toegevoegd, moeten deze worden toegewezen aan de formuliervakken binnen dit object.  

Regelgevende wijzigingen die invloed hebben op dit rapport en de tabelgegevens, worden meestal verwerkt in eindejaarsupdates.
Het kan handig zijn het rapport **1099-gegevens van leverancier** uit te voeren om de gegevens te bekijken voordat u het elektronische bestand genereert.  

## <a name="see-also"></a>Zie ook
[Procedure: Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Procedure: Inkoop vastleggen](purchasing-how-record-purchases.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

