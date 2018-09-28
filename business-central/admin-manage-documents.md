---
title: Documenten beheren, verwijderen of comprimeren | Microsoft Docs
description: Bewaar of verwijder uw historische gegevens.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 696100bfbcc987b1d684e7987e7fd43979813282
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Documenten beheren
Een centrale rol, bijvoorbeeld de toepassingsbeheerder, moet regelmatig de verzamelde historische documenten verwijderen of comprimeren.  

## <a name="delete-documents"></a>Documenten verwijderen
Het kan voorkomen dat u gefactureerde inkooporders moet verwijderen die niet automatisch zijn verwijderd. [!INCLUDE[d365fin](includes/d365fin_md.md)] controleert of de verwijderde inkooporders volledig zijn gefactureerd. U kunt geen orders verwijderen die u niet volledig hebt ontvangen en gefactureerd.  

Nadat retourorders zijn gefactureerd, worden deze doorgaans verwijderd. Wanneer u een factuur boekt, wordt deze overgebracht naar het venster **Geboekte inkoopcreditnota**. Als u het selectievakje **Retourzending op creditnota** hebt ingeschakeld in het venster **Inkoopinstellingen**, wordt de factuur overgebracht naar het venster **Geboekte retourverzending**. U kunt de documenten verwijderen met behulp van de batchverwerking **Gef. ink.-retourorders verw.**. Voordat de verwijdering wordt uitgevoerd, controleert de batchverwerking of inkoopretourorders volledig zijn verzonden en gefactureerd.  

Inkoopraamcontracten worden niet verwijderd nadat u alle bijbehorende inkooporders hebt verwerkt en gefactureerd. U kunt raamcontracten verwijderen met de batchverwerking **Gefact. inkoopraamcontracten verwijderen**.  

Gefactureerde servicefacturen worden doorgaans automatisch verwijderd als ze volledig zijn gefactureerd. Wanneer een factuur wordt geboekt, wordt een bijbehorende post gemaakt in het venster **Geboekte servicefacturen**. U kunt het geboekte document bekijken in het venster **Geboekte servicefactuur**.  

Serviceorders worden echter niet automatisch verwijderd als het totale aantal op de order niet vanuit de serviceorder zelf is geboekt, maar vanuit het venster **Servicefactuur**. In dit geval zult u wellicht gefactureerde orders die niet zijn verwijderd, zelf moeten verwijderen. Hiervoor kunt u de batchverwerking **Gefactureerde serviceorders verwijderen** uitvoeren.  

## <a name="see-also"></a>Zie ook  
[Beheer](admin-setup-and-administration.md)  

