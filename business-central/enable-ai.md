---
title: Copilot- en AI-mogelijkheden configureren
description: In dit artikel wordt uitgelegd hoe u Copilot in een omgeving kunt inschakelen.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# <a name="configure-copilot-and-ai-capabilities"></a>Copilot- en AI-mogelijkheden configureren

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

In dit artikel wordt uitgelegd hoe u Copilot en andere AI-mogelijkheden in Business Central kunt beheren. Deze taak wordt uitgevoerd door een beheerder. Copilot is een systeemfunctie en een integraal onderdeel van Business Central. Net als bij de meeste systeemfuncties verleent u geen toegang aan individuele gebruikers en kunt u Copilot ook niet in- of uitschakelen. Copilot biedt echter controles op het gebied van gegevensbeheer en de mogelijkheid om individuele Copilot- en AI-mogelijkheden voor elke omgeving te deactiveren. Er zijn verschillende niveaus van toegangscontrole tot AI-mogelijkheden, afhankelijk van de functie:

- Gegevensverplaatsing tussen geografische regio's toestaan

  Deze taak is alleen vereist als uw Business Central-omgeving zich in een andere geografie bevindt dan de Azure OpenAI Service die deze gebruikt. [Meer informatie](#allow-data-movement-across-geographies)

- Activeer de functie op de pagina **Copilot en AI-mogelijkheden**. [Meer informatie](#activate-features)

- Schakel de specifieke functie in, als deze nog steeds wordt beheerd door **Functiebeheer**.

  In releasewave 2 van 2023 zijn zowel de marketingtekstsuggesties als de hulpfuncties voor bankrekeningreconciliatie opgenomen onder **Functiebeheer**. [Meer informatie](#enable-feature-in-feature-management)

Als aan een van deze vereisten niet wordt voldaan, is de functie niet beschikbaar voor gebruik.

## <a name="prerequisites"></a>Vereisten

- U gebruikt Business Central online, versie 23.1 of hoger. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- U beschikt over beheerders- of supermachtigingen in Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Gegevensverplaatsing tussen geografieën toestaan

Deze taak is alleen van toepassing als de schakelaar **Gegevensverplaatsing toestaan** boven aan de pagina **Copilot en AI-mogelijkheden** wordt weergegeven. Als de link **Hoe beheer ik mijn copilotgegevens?** wordt weergegeven in plaats van de schakelaar **Gegevensverplaatsing toestaan**, slaat u deze stap over.

![Toont een schermafbeelding van de schakelaar Gegevensverplaatsing toestaan op de pagina Copilot- en AI-mogelijkheden.](media/allow-data-movement-v2.png)

De schakelaar **Gegevensverplaatsing toestaan** geeft aan dat uw Business Central-omgevingslocatie&mdash;dat wil zeggen de geografie waar gegevens worden verwerkt en opgeslagen&mdash;niet hetzelfde is als de Azure OpenAI Service-geografie die door Copilot wordt gebruikt. Als u Copilot wilt inschakelen, moet u gegevensverplaatsing tussen regio's toestaan. Voor meer informatie over gegevensverplaatsing gaat u naar [Copilot-gegevensverplaatsing tussen geografieën](ai-copilot-data-movement.md). 

Voer de volgende stappen uit om gegevensverplaatsing buiten uw geografische regio toe te staan:

1. Zoek in Business Central de pagina **Copilot- en AI-mogelijkheden** en open deze.
1. Zet de schakelaar **Gegevensverplaatsing toestaan** aan.

U kunt zich afmelden door de schakelaar **Gegevensverplaatsing toestaan** uit te schakelen. Zodra een Azure OpenAI Service beschikbaar komt in de geografie van uw Business Central-omgeving, wordt uw omgeving er automatisch mee verbonden en is de schakelaar niet langer beschikbaar. 


<!--
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->
## <a name="activate-features"></a>Functies activeren

Alle Copilot- en AI-mogelijkheden zijn standaard actief wanneer ze in preview beschikbaar worden gesteld of algemeen beschikbaar worden. Met behulp van de pagina **Copilot- en AI-mogelijkheden** kunt u afzonderlijke functies voor alle gebruikers uit- of weer inschakelen.

1. Zoek in Business Central de pagina **Copilot- en AI-mogelijkheden** en open deze.

1. De pagina vermeldt alle beschikbare Copilot- en AI-gerelateerde functies en hun huidige status, die actief of inactief kan zijn. De functies zijn verdeeld in twee secties&mdash;een sectie voor functies in preview en een andere voor functies die algemeen beschikbaar zijn. 

   [![Toont het Business Central-rolcentrum en de controlelijst voor Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Om een functie in te schakelen selecteert u deze in de lijst en selecteert u vervolgens de actie **Activeren**.
   - Om een functie uit te schakelen selecteert u deze en selecteert u vervolgens de actie **Deactiveren**. 


## <a name="enable-feature-in-feature-management"></a>Functie inschakelen in Functiebeheer

Wanneer individuele Copilot-mogelijkheden worden vrijgegeven in kleine updates van Business Central, zijn deze mogelijkheden optioneel tot de volgende grote update. **Functiebeheer** wordt gebruikt om functies in of uit te schakelen die in preview zijn, zoals bankreconciliatie, en sommige functies die algemeen beschikbaar zijn, zoals suggestie voor marketingtekst. [Meer informatie over functiebeheer](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. Zoek in Business Central de pagina **Functiebeheer** en open deze.
2. Als u een functie wilt inschakelen, stelt u de kolom **Geactiveerd voor** in op **Alle gebruikers**. Als u een functie wilt uitschakelen, stelt u de kolom **Geactiveerd voor** in op **Geen**. Gebruik de volgende tabel om u te helpen bepalen welke schakelaar van toepassing is op de Copilot- en AI-mogelijkheid die u wilt inschakelen:

   - **Functiepreview: Bankrekeningreconciliatie met Copilot** heeft betrekking op de hulpfunctie voor bankrekeningreconciliatie.
   - **Functiepreview: Op AI gebaseerde productbeschrijvingen maken met Copilot** heeft betrekking op de functie voor marketingtekstsuggesties.

   Ga voor meer informatie over functiebeheer in het algemeen naar [Functiebeheer](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="granting-user-access"></a>Gebruikerstoegang verlenen

Copilot- en AI-mogelijkheden kunnen functionaliteit bieden die bedoeld is voor alle gebruikers in uw organisatie of voor specifieke gebruikersrollen. De meeste Copilot- en AI-mogelijkheden bieden toegangscontrole met behulp van machtigingen en machtigingensets in het machtigingsbeheersysteem van Business Central. [Meer informatie over machtigingen en machtigingensets](ui-define-granular-permissions.md).

Als u toegang tot specifieke Copilot- en AI-mogelijkheden wilt verlenen of weigeren, raadpleegt u de documentatie of de uitgever van die functie om te bepalen welke machtigingen vereist zijn. 

## <a name="next-steps"></a>Volgende stappen

Nadat u de functies heeft ingeschakeld en ermee akkoord gaat, bent u klaar om ze uit te proberen. Ga naar:

- [Marketingtekst aan artikelen toevoegen](item-marketing-text.md) 
- [Reconciliëren met behulp van hulp bij bankrekeningreconciliatie](bank-reconciliation-with-copilot.md) 

## <a name="see-also"></a>Zie ook

[Problemen oplossen met Copilot- en AI-mogelijkheden](ai-copilot-troubleshooting.md)  
[Overzicht van suggesties voor marketingteksten](ai-overview.md)   
[Veelgestelde vragen over suggesties voor marketing](faqs-marketing-text.md)  
