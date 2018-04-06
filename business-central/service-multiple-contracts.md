---
title: Meervoudige contracten | Microsoft Docs
description: "Afhankelijk van uw serviceovereenkomst met een klant, moet u een serviceartikel mogelijk verwerken onder meer dan één servicecontract."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6e4f0bad058bd928f65214f04f978bf3b387cbb8
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="multiple-contracts"></a>Meervoudige contracten
Afhankelijk van uw serviceovereenkomst met een klant, moet u een serviceartikel mogelijk verwerken onder meer dan één servicecontract.  
  
Bij de verwerking van een serviceartikel onder meerdere contracten, kunt u het volgende doen:  
  
* Verschillende contracten verzenden voor hetzelfde serviceartikel.  
* Onderdelen afzonderlijk onderhouden.  
* Rekening houden met verschillende bekwaamheden die vereist zijn voor het uitvoeren van onderhoud op verschillende aspecten van een serviceartikel, zoals mechanische componenten en software.  
* Verschillende responstijden en frequenties opgeven voor het onderhoud van verschillende delen van een serviceartikel.  
* Rekening houden met verschillende soorten activiteiten die op een serviceartikel moeten worden uitgevoerd, wanneer er voor het serviceartikel verschillende soorten onderhoud nodig zijn in verschillende perioden.  
* Een relevant contractnummer selecteren en toewijzen aan een serviceartikelregel als u een serviceorder maakt.  
* Relevante financiële informatie verwerken met betrekking tot serviceartikelen en serviceovereenkomsten.  
  
Bij het gebruik van meervoudige contracten kunt u de volgende voorbeelden in aanmerking nemen.  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Meervoudige contracten maken per serviceartikel  
U kunt handmatig een servicecontract of servicecontractofferte maken voor serviceartikelen die al zijn geregistreerd in niet-geannuleerde contracten van dezelfde klant. Hiervoor volgt u de standaardprocedure voor het maken van servicecontracten en servicecontractoffertes. Zie voor meer informatie [Werken met servicecontracten en servicecontractoffertes](service-how-to-create-service-contracts-and-service-contract-quotes.md).  
  
Als u op een contractregel een serviceartikel toevoegt dat is geregistreerd in andere servicecontracten of servicecontractoffertes, wordt een bericht weergegeven met de waarschuwing dat het serviceartikel al hoort bij een of meer servicecontracten of servicecontractoffertes. Als u dit bericht bevestigt, wordt alle relevante informatie over het serviceartikel gekopieerd naar een nieuwe contractregel.  
  
## <a name="copying-documents"></a>Documenten kopiëren  
Met de actie **Document kopiëren** kunt u automatisch een servicecontract of contractofferte maken voor serviceartikelen die al zijn geregistreerd in andere servicecontracten of contractoffertes.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Serviceorders maken voor meervoudige contracten  
U kunt handmatig een serviceorder maken voor een serviceartikel dat is geregistreerd in meervoudige actieve contracten. Een servicecontract is actief als het is ondertekend en niet is verlopen.  
  
## <a name="see-also"></a>Zie ook  
[Servicecontracten voldoen](service-fulfill-service-contracts.md)  
[Serviceorders maken](service-how-to-create-service-orders.md)  

