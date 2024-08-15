---
title: Copilot- en AI-mogelijkheden configureren
description: In dit artikel wordt uitgelegd hoe u Copilot in een omgeving kunt inschakelen.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/28/2024
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# <a name="configure-copilot-and-ai-capabilities"></a>Copilot- en AI-mogelijkheden configureren

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

In dit artikel wordt uitgelegd hoe u Microsoft Copilot en andere AI-mogelijkheden in Dynamics 365 Business Central kunt beheren. Deze taken moet worden uitgevoerd door een beheerder.

Copilot is een systeemfunctie en een integraal onderdeel van Business Central. Net als bij de meeste systeemfuncties verleent u geen toegang aan individuele gebruikers en kunt u Copilot ook niet in- of uitschakelen. Copilot biedt echter controles op het gebied van gegevensbeheer en de mogelijkheid om individuele Copilot- en AI-mogelijkheden voor elke omgeving te deactiveren. Er zijn verschillende niveaus van toegangscontrole voor AI-mogelijkheden, afhankelijk van de functie:

- Gegevensverplaatsing tussen geografische regio's toestaan.

    Deze taak is alleen vereist als uw Business Central-omgeving zich in een andere geografie bevindt dan de Azure OpenAI Service die deze gebruikt. [Meer informatie over deze taak](#allow-data-movement-across-geographies).

- Activeer de functie op de pagina **Copilot en AI-mogelijkheden**. [Meer informatie over deze taak](#activate-features).

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Als aan een van deze vereisten niet wordt voldaan, is de functie niet beschikbaar voor gebruik.

## <a name="prerequisites"></a>Vereisten

- U gebruikt Business Central Online.
- U bent een [beheerder](#requirements-for-being-an-administrator) in Business Central.

## <a name="allow-data-movement-across-geographies"></a>Gegevensverplaatsing tussen geografieën toestaan

Deze taak is alleen van toepassing als de schakelaar **Gegevensverplaatsing toestaan** boven aan de pagina **Copilot en AI-mogelijkheden** wordt weergegeven. Als de koppeling **Hoe beheer ik mijn copilotgegevens?** wordt weergegeven in plaats van de optie **Gegevensverplaatsing toestaan**, slaat u deze taak over.

![Schermopname met de optie Gegevensverplaatsing toestaan op de pagina Copilot- en AI-mogelijkheden.](media/allow-data-movement-v2.png)

De aanwezigheid van de optie **Gegevensverplaatsing toestaan** geeft aan dat de locatie van uw Business Central-omgeving (de geografie waar gegevens worden verwerkt en opgeslagen) niet hetzelfde is als de Azure OpenAI Service-geografie die Copilot gebruikt. Als u Copilot wilt inschakelen, moet u gegevensverplaatsing tussen regio's toestaan. [Meer informatie over gegevensverplaatsing](ai-copilot-data-movement.md).

Voer deze stappen uit om gegevensverplaatsing buiten uw geografische regio toe te staan:

1. Zoek in Business Central de pagina **Copilot- en AI-mogelijkheden** en open deze.
1. Zet de schakelaar **Gegevensverplaatsing toestaan** aan.

    > [!NOTE]
    > De schakelaar **Gegevensverplaatsing toestaan** is standaard ingeschakeld voor omgevingen in de Azure-regio's West-Europa en Noord-Europa.

U kunt zich afmelden voor gegevensverplaatsing door de optie **Gegevensverplaatsing toestaan** uit te schakelen.

Zodra een Azure OpenAI Service beschikbaar komt in de geografie van uw Business Central-omgeving, wordt uw omgeving er automatisch mee verbonden. Op dat moment wordt de optie **Gegevensverplaatsing toestaan** niet meer weergegeven op de pagina **Copilot- en AI-mogelijkheden**.

<!-- Don't review
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

Alle Copilot- en AI-mogelijkheden zijn standaard actief wanneer ze in preview beschikbaar worden gesteld of algemeen beschikbaar worden. Op de pagina **Copilot- en AI-mogelijkheden** kunt u afzonderlijke functies voor alle gebruikers uit- of weer inschakelen.

1. Zoek in Business Central de pagina **Copilot- en AI-mogelijkheden** en open deze.
1. De pagina vermeldt alle beschikbare Copilot- en AI-gerelateerde functies en hun huidige status. (De status kan *Actief* of *Inactief* zijn.) De functies zijn verdeeld in twee secties: één voor functies die in preview zijn en één voor functies die algemeen beschikbaar zijn.

    - Om een functie in te schakelen selecteert u deze in de lijst en selecteert u vervolgens **Activeren**.
    - Om een functie uit te schakelen selecteert u deze in de lijst en selecteert u vervolgens **Deactiveren**.

    [![Schermopname met de knoppen Activeren en Deactiveren voor de functielijsten op de pagina Copilot & AI-mogelijkheden.](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## <a name="enable-feature-in-feature-management"></a>Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## <a name="granting-user-access"></a>Gebruikerstoegang verlenen

Copilot- en AI-mogelijkheden kunnen functionaliteit bieden die bedoeld is voor alle gebruikers in uw organisatie of voor specifieke gebruikersrollen. De meeste Copilot- en AI-mogelijkheden bieden toegangscontrole met behulp van machtigingen en machtigingensets in het machtigingsbeheersysteem van Business Central. [Meer informatie over machtigingen en machtigingensets](ui-define-granular-permissions.md).

In de volgende tabel worden de machtigingen weergegeven die vereist zijn om Copilot-functies van Business Central te gebruiken.

| Copilot-functie | Vereiste machtigingen |
|---|---|
| Hulp bij analyse | De machtigingenset **GEGEVENSANALYSE - EXEC** of uitvoermachtiging voor het systeemobject 9640 **Gegevensanalysemodus toestaan**. Dit zijn dezelfde machtigingen die nodig zijn om toegang te krijgen tot de analysemodus. |
| Hulp bij bankreconciliatie | Machtiging op pagina 7250 **AI-voorstel voor bankrekeningreconciliatie** en pagina 7252 **AI-voorstel voor transactie naar grootboekrekening**. |
| Chatten | Er zijn geen machtigingen of machtigingensets die de toegang tot chatten per gebruiker regelen. Als chatten is geactiveerd, is dit beschikbaar voor alle gebruikers. |
| E-document toewijzen | Machtiging op pagina 6166 **Copilot-eig. IO e-doc.** |
| Suggesties voor marketingteksten | Machtiging op pagina 5836 **Copilot-marketingtekst**. |
| Suggesties voor verkoopregels | Machtiging op pagina 7275 **AI-suggesties voor verkoopregels** en pagina 7276 **AI-suggesties voor verkoopregels Sub**. |

Als u toegang tot specifieke niet-Microsoft Copilot- en AI-mogelijkheden wilt verlenen of weigeren, raadpleegt u de documentatie of de uitgever van die functie om te bepalen welke machtigingen vereist zijn.

## <a name="requirements-for-being-an-administrator"></a>Vereisten om beheerder te zijn

U moet SUPER-machtigingen hebben in uw Business Central-gebruikersaccount of een van de volgende Business Central-licenties:

- Gedelegeerde beheerder - Partner
- Gedelegeerde Helpdesk-agent - Partner
- Interne beheerder
- Interne BC-beheerder
- Dynamics 365-beheerder

Business Central biedt nog geen gedetailleerde machtigingen op objectniveau, zodat alleen specifieke beheerders Copilot kunnen configureren.

## <a name="next-steps"></a>Volgende stappen

Nadat u de functies heeft ingeschakeld en ermee akkoord gaat, bent u klaar om ze uit te proberen. Ga naar de volgende artikelen:

- [Marketingtekst aan artikelen toevoegen met Copilot](item-marketing-text.md)
- [Lijstgegevens analyseren met behulp van Copilot](analysis-assist.md)
- [Chatten met Copilot](chat-with-copilot.md)
- [E-documenten toewijzen aan inkooporderregels met Copilot](map-edocuments-with-copilot.md)
- [Bankrekeningen reconciliëren met Copilot](bank-reconciliation-with-copilot.md)
- [Regels op verkooporders voorstellen met Copilot](sales-suggest-sales-lines-with-copilot.md)

## <a name="see-also"></a>Zie ook

[Problemen oplossen met Copilot- en AI-mogelijkheden](ai-copilot-troubleshooting.md)  
[Veelgestelde vragen over analysehulp](faqs-analysis-assist.md)  
[Veelgestelde vragen over hulp bij bankreconciliatie](faqs-bank-reconciliation.md)  
[Veelgestelde vragen over chatten met Copilot](faqs-chat-with-copilot.md)  
[Veelgestelde vragen over het toewijzen van e-documenten aan inkooporders](faqs-map-edocuments.md)  
[Veelgestelde vragen over suggesties voor marketing](faqs-marketing-text.md)  
[Veelgestelde vragen over suggesties voor verkoopregels](faq-sales-suggest-sales-lines-with-copilot.md)  
[Overzicht van suggesties voor marketing](ai-overview.md)
