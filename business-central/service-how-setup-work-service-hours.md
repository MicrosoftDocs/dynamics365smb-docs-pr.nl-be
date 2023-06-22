---
title: Service- en werkuren instellen
description: Leer hoe u werk- en service-uren instelt die worden gebruikt om de responsdatum en -tijd berekend voor serviceorders en -offertes.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="set-up-work-hours-and-service-hours" />Service- en werkuren instellen
Met een servicebeheersysteem worden de resource-uren en serviceorderstatus bijgehouden ten behoeve van het voorspellen van de werkbelasting en servicebehoeften. [!INCLUDE[prod_short](includes/prod_short.md)] heeft ingebouwde tools die u kunt aanpassen om dit soort informatie vast te leggen.  
  
Nadat u de standaardservice-uren van uw bedrijf hebt ingesteld, kunt u responstijden voor serviceorders berekenen of waarschuwingen verzenden wanneer serviceoproepen worden ontvangen. De waarschuwingsfunctie wordt in combinatie met de projectplanner geïmplementeerd.   
  
Terwijl u aan serviceorder werkt, is het handig om de status te kunnen bijwerken zodat u de voortgang kunt bijhouden. Met de serviceorderstatus wordt de herstelstatus van de serviceartikelen in de serviceorder aangegeven. Zie voor meer informatie [Serviceorderstatus en herstelstatus begrijpen](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours" />Standaardservice-uren instellen
Op de pagina **Std. service-uren** kunt u de gebruikelijke servicewerkuren in het bedrijf instellen. Deze service-uren worden gebruikt om de responsdatum en -tijd voor serviceorders en -offertes te berekenen en om responstijdwaarschuwingen te verzenden. De standaardservice-uren voor servicecontracten worden gebruikt tenzij u speciale service-uren voor een contract opgeeft.  
  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Std. service-uren** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Als u de regels op de pagina **Std. service-uren** niet invult, wordt als standaardwaarde 24 uur gebruikt, die alleen geldig is voor agendawerkdagen.  
  
## <a name="to-set-up-work-hour-templates" />Werkuursjablonen instellen
Op de pagina **Werkuursjabloon** kunt u sjablonen instellen met de standaardwerkuren in het bedrijf. U kunt bijvoorbeeld sjablonen maken voor technici met een volledige baan en voor technici met een deeltijdbaan. U kunt werkuursjablonen gebruiken wanneer u capaciteit toevoegt aan resources.  
  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Werkuursjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Als u werkuren voor elke dag invoert, wordt de waarde in het veld **Totaal per week** automatisch berekend.  

## <a name="to-set-up-contract-specific-service-hours" />Contractspecifieke service-uren instellen
Op de pagina **Service-uren** kunt u specifieke service-uren instellen voor de klant die eigenaar is van het servicecontract. Met de service-uren worden de responsdatum en -tijd berekend voor serviceorders en -offertes die bij het servicecontract horen.  
  
Als u geen specifieke service-uren voor het servicecontract instelt, worden de standaardservice-uren voor servicecontracten gebruikt.  
  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontracten** in en kies vervolgens de gerelateerde koppeling.  
2. Open het servicecontract waarvoor u specifieke service-uren wilt instellen en kies **Service-uren**.  
4. Als u service-uren op basis van standaardservice-uren wilt instellen, kiest u de actie **Std. service-uren kopiëren**.  
5. De velden in de posten voor service-uren bewerken. Invoegen of verwijderen van vermeldingen voor het instellen van de service-uren voor het contract. Merk op dat de velden **Dag**, **Begintijd** en **Eindtijd** zijn vereist voor elke regel.  
6. Als u de service-uren wilt laten gelden vanaf een specifieke datum, vult u het veld **Begindatum** in.  
7. Als u de service-uren wilt laten gelden op vakantiedagen, schakelt u het selectievakje **Geldig op vakantiedagen** in.  

## <a name="see-also" />Zie ook
[Toewijzingsstatus en herstelstatus begrijpen](service-allocation-status-and-repair-status.md)  
[CRM - Service instellen](service-setup-service.md)  
[Serviceorderstatus en herstelstatus begrijpen](service-order-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
