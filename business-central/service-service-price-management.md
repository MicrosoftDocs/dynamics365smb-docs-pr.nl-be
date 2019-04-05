---
title: Beheer serviceprijs | Microsoft Docs
description: In dit onderwerp wordt beschreven hoe u de juiste prijs kunt toepassen op serviceorders, persoonlijke serviceprijsovereenkomsten kunt opzetten voor klanten, de efficiëntie van uw werknemers kunt verbeteren en het factureringsproces kunt versnellen.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: eb3d9b075f7209634cdc8b6f88a24409f18811e7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816788"
---
# <a name="service-price-management"></a>Beheer serviceprijs
Met de functionaliteit voor serviceprijsbeheer kunt u de juiste prijs toepassen op serviceorders, persoonlijke serviceprijsovereenkomsten opzetten voor klanten, de efficiëntie van uw werknemers verbeteren en het factureringsproces versnellen.  
  
Met serviceprijsbeheer kunt u verschillende serviceprijsgroepen instellen, zodat u rekening kunt houden met zowel het serviceartikel of de serviceartikelgroep, als met het soort fout waarop de servicetaak betrekking heeft. U kunt deze groepen instellen voor een beperkte periode, of voor een bepaalde klant of valuta. U kunt prijsberekeningsstructuren gebruiken als sjablonen voor het toewijzen van een bepaalde prijs aan een bepaalde servicetaak.  
  
U kunt zo bijvoorbeeld bepaalde artikelen toewijzen die zijn opgenomen in de serviceprijs, maar ook het soort werk dat onder de prijs valt. U kunt zo ook verschillende btw-tarieven en kortingsbedragen gebruiken voor verschillende serviceprijsgroepen. Om er zeker van te zijn dat de correcte prijzen worden toegepast, kunt u vaste, minimum- of maximumprijzen toewijzen, afhankelijk van de afspraken die u met uw klanten hebt gemaakt.  
  
Voordat u de prijs van een serviceartikel op een serviceorder aanpast, ziet een overzicht van de resultaten van de prijsherwaardering. U kunt deze resultaten goedkeuren, of kunt u aanvullende wijzigingen aanbrengen als u een ander resultaat wenst. De hele herwaardering wordt uitgevoerd per regel. Er worden dus geen extra regels gemaakt.  
  
Ten slotte kunt u via statistieken en standaardlijsten over de serviceprijsgroepen bijhouden hoe winstgevend de verschillende serviceprijsgroepen zijn.  
  
## <a name="service-price-adjustment-groups"></a>Serviceprijsherwaarderingsgroepen  
Met serviceprijsherwaarderingsgroepen stelt u de verschillende soorten prijsherwaarderingen in. U kunt bijvoorbeeld een serviceprijsherwaarderingsgroep instellen waarmee de prijzen voor reserveonderdelen worden aangepast, een groep waarmee de loonkosten worden aangepast, een groep waarmee de kosten worden aangepast, enzovoort. U kunt ook opgeven of de serviceprijsherwaardering alleen op een bepaald artikel of een bepaalde resource moet worden toegepast of op alle artikelen en resources.  
  
Elke serviceprijsherwaarderingsgroep bevat informatie over de herwaarderingen die u wilt maken op de serviceregels.  
  
De functie voor serviceprijsherwaardering is niet van toepassing op serviceartikelen die horen bij servicecontracten. U kunt alleen de serviceprijzen aanpassen van artikelen die onderdeel zijn van een serviceorder. U kunt de prijs van een serviceartikel met garantie niet aanpassen. Ook kunt u de prijs van een serviceartikel voor een serviceorder niet wijzigen als de hieraan gekoppelde serviceregel geheel of gedeeltelijk is geboekt als factuur.  
  
Als u de functie voor serviceprijsherwaarderingen uitvoert, worden alle kortingen in de order vervangen door de waarden van de serviceprijsherwaardering.  
  
## <a name="service-price-groups"></a>Serviceprijsgroepen  
U kunt serviceprijsgroepen instellen om groepen serviceartikelen te maken waarvoor dezelfde speciale serviceprijzen gelden. Als u serviceartikelgroepen hebt ingesteld, kunt u deze toewijzen aan serviceartikelen op serviceartikelregels. U kunt ook serviceprijsgroepen toewijzen aan serviceartikelgroepen.  
  
Voordat u een serviceprijsgroep kunt toewijzen aan een serviceartikel, moet u eerst bepalen op welk foutgebied, welke valuta of welke serviceprijsherwaarderingsgroep de serviceprijsgroep van toepassing is. U moet bepalen tot welk bedrag de serviceprijs moet worden aangepast en of dit bedrag inclusief btw en kortingen is. U moet ook bepalen of deze herwaardering om een vast bedrag gaat of alleen onder bepaalde voorwaarden moet worden toegepast.  
  
Als u een serviceprijsgroep toewijst aan een serviceartikel, gelden alle speciale serviceprijzen die u instelt voor deze groep, voor dit serviceartikel.  
  
## <a name="service-pricing"></a>Serviceprijsstelling  
U stelt de werkelijke soorten serviceprijs (prijsherwaarderingssoort en prijs) in voor een combinatie van serviceprijsgroepen en klantenprijsgroepen. Voor elk soort serviceprijs selecteert u een serviceprijsherwaarderingsgroep. U geeft ook het serviceprijsherwaarderingssoort, vast, maximaal of minimum, en de werkelijke prijs op.  
  
U kunt bijvoorbeeld soorten serviceprijzen instellen voor een radioserviceprijsgroep. Voor klanten zonder prijsgroep kunt u serviceprijzen met maximumarbeidskosten vastleggen. Dit is de herwaarderingsgroep voor arbeidskosten. Voor klanten met een bepaalde prijsgroep kunt u serviceprijzen met vaste arbeidskosten vastleggen, in dezelfde herwaarderingsgroep voor arbeidskosten.  
  
## <a name="service-price-adjustment"></a>Serviceprijsherwaardering  
Met serviceprijsherwaarderingen kunt u de prijs van artikelen, resources, grootboekrekeningen of kosten op serviceorders aanpassen.  
  
Nadat u een artikel hebt ingevoerd op de serviceartikelregel, voert u de verdere gegevens over de kosten voor het artikel in op de serviceregels. Wanneer u de functie Serviceprijs aanpassen uitvoert, kunt u de prijsherwaarderingen vooraf bekijken. Als u wilt, kunt u wijzigingen aanbrengen. Als u de herwaarderingen bevestigt, worden de wijzigingen berekend en overgebracht naar de serviceregels. Vervolgens kunt u de serviceorder boeken.  
  
Afhankelijk van het soort serviceprijsherwaardering, wordt het totale bedrag van de herwaarderingen berekend.  
  
De volgende tabel geeft een beschrijving van de berekeningen.  
  
|Optie | Description |  
|----------------------------------|---------------------------------------|  
|**Vaste prijs**|dit betekent dat u een vaste prijs vraagt voor het serviceartikel, de resource, de grootboekrekening of de kosten, onafhankelijk van de werkelijke kosten of gebruikelijke toeslagen. Als u deze optie selecteert, komt de serviceprijsherwaardering precies uit op het bedrag dat is opgegeven in de serviceprijsgroep.|  
|**Maximum**|Dit betekent dat u een bovengrens stelt aan wat u aan uw klant berekent, onafhankelijk van de werkelijke kosten of gebruikelijke toeslagen. Als u deze optie selecteert, wordt de serviceprijsherwaardering alleen uitgevoerd als de totale prijs uitkomt boven het bedrag dat is opgegeven in de serviceprijsgroep.|  
|**Minimum**|Dit betekent dat u een ondergrens stelt aan wat u aan uw klant berekent, onafhankelijk van de werkelijke kosten of gebruikelijke toeslagen. Als u deze optie selecteert, wordt de serviceprijsherwaardering alleen uitgevoerd als het totale bedrag minder is dan het bedrag dat is opgegeven in de serviceprijsgroep.|  
  
## <a name="see-also"></a>Zie ook  
[Prijzen en aanvullende kosten voor services instellen](service-how-setup-service-costs-pricing.md)  
[CRM - Service instellen](service-setup-service.md)  
