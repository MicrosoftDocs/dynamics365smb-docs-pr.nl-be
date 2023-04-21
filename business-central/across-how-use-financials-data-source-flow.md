---
title: Power Automate-stromen gebruiken in Business Central
description: Configureer en gebruik Power Automate-stromen om Business Central-gegevens te maken of wijzigen.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 10/10/2022
ms.custom: bap-template
---
# Power Automate-stromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]

Met [!INCLUDE[prod_short](includes/prod_short.md)] krijgt u een licentie voor Microsoft Power Automate. Met deze licentie kunt u uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens als onderdeel van een werkstroom gebruiken in Microsoft Power Automate. U maakt stromen en maakt verbinding met uw gegevens uit interne en externe bronnen met behulp van de [!INCLUDE [prod_short](includes/prod_short.md)]-connector.

Power Automate-stromen worden geactiveerd door gebeurtenissen, zoals een record is gemaakt, gewijzigd of verwijderd. Ze kunnen ook worden uitgevoerd volgens een door de gebruiker gedefinieerd schema of op aanvraag.

> [!NOTE]
> Beheerders kunnen de toegang tot Power Automate beperken. Neem contact op met uw beheerder als u merkt dat u geen toegang heeft tot sommige of alle functies die in dit artikel worden beschreven. Als u wilt leren hoe u toegang tot Power Automate kunt bepalen als beheerder, raadpleegt u [Power Automate-integratie instellen](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Naast Power Automate kunt u sjablonen voor goedkeuringswerkstromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]. Hoewel het twee aparte werkstroomsystemen zijn, wordt elke goedkeuringswerkstroomsjabloon die u maakt met Power Automate, toegevoegd aan de lijst met werkstromen in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Werkstromen](across-workflow.md).

## Over Power Automate-stromen

Power Automate is een service die u helpt bij het maken van geautomatiseerde werkstromen (of stromen) tussen apps en services, zoals [!INCLUDE[prod_short](includes/prod_short.md)]. Power Automate-stromen vereisen weinig of geen codeerkennis. Ze kunnen worden geassocieerd met een breed scala aan gebeurtenissen en reacties, zoals:

- Recordwijzigingen
- Updates van externe bestanden
- Geboekte documenten
- Verschillende services van Microsoft en derden, zoals Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps en meer.

Er zijn drie verschillende soorten cloudstromen waarmee u kunt werken:

|Stroomtype|Omschrijving|
|---------|-----------|
|Geautomatiseerd|Dit stroomtype wordt automatisch uitgevoerd door een gebeurtenis. In [!INCLUDE[prod_short](includes/prod_short.md)] kan een gebeurtenis zijn wanneer een record of document wordt gemaakt, gewijzigd of verwijderd. Een nieuwe verkoopfactuur kan bijvoorbeeld een stroom activeren voor een goedkeuringsverzoek, waarvoor verschillende gebeurtenissen kunnen worden ingesteld, afhankelijk van het antwoord van de fiatteur. Een negatieve reactie stuurt een bericht en e-mail naar de aanvrager van de goedkeuring. Een positieve reactie werkt tegelijkertijd een Excel-spreadsheet bij die zich in een SharePoint bevindt en stuurt een update naar een Teams-chat. Geautomatiseerde stromen kunnen worden gestart door zowel interne als externe gebeurtenissen in [!INCLUDE[prod_short](includes/prod_short.md)].|
|Ingeroosterd|Dit type stroom wordt ook automatisch uitgevoerd, maar het wordt periodiek uitgevoerd op een geplande datum en tijd. |
|Direct |Dit stroomtype wordt op aanvraag uitgevoerd, waarbij de gebruiker het handmatig moet uitvoeren vanaf een knop of actie in een andere app of ander apparaat, in dit geval de [!INCLUDE[prod_short](includes/prod_short.md)]-cliënt. Directe stromen werken op dezelfde manier als batchsnelkoppelingen, waarbij meerdere lange stappen worden uitgevoerd met een paar drukken op een knop en worden gestart vanaf specifieke pagina's of tabellen. Een stroom kan bijvoorbeeld een knop toevoegen aan het actiemenu op de pagina **Leveranciers** om betalingen aan een leverancier te blokkeren en tegelijkertijd aanpasbare e-mails te verzenden naar de contactpersoon van de leverancier en de inkopers van uw bedrijf, en om het contact in Outlook bij te werken. |

## Power Automate-functies

U kunt alle Power Automate-stromen verkennen die momenteel voor u beschikbaar zijn door u aan te melden bij [Power Automate](https://powerautomate.com) en **Mijn stromen** te selecteren vanuit de navigatiebalk aan de linkerkant. Hier vindt u alle stromen die u zelf al hebt gemaakt en stromen die met u zijn gedeeld door een beheerder of collega.

- Directe stromen zijn ook beschikbaar gemaakt om rechtstreeks vanaf de meeste lijst-, kaart- en documentpagina's in [!INCLUDE[prod_short](includes/prod_short.md)] te worden uitgevoerd. U vindt de directe stromen in de actiegroep **Automatiseren** in de actiebalk van pagina's. Om een stroom uit te voeren selecteert u deze en volgt u de instructies die aan u worden gepresenteerd. Lees meer in de volgende secties.
 
- Met geautomatiseerde stromen in [!INCLUDE[prod_short](includes/prod_short.md)] hoeft u niets te doen, tenzij u ze wilt wijzigen of uitschakelen. Anders werken ze gewoon wanneer ze worden geactiveerd. 
<!--

## Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## Directe stromen uitvoeren

Directe stromen worden geopend binnen [!INCLUDE [prod_short](includes/prod_short.md)] Online, zodat u binnen de context kunt blijven van het bedrijfsproces waar u in zat. U kunt direct een stroom uitvoeren vanuit de meeste lijsten, kaarten of documenten.

1. Selecteer in de actiebalk **Automatiseren** en kies vervolgens een stroom uit de lijst met beschikbare stromen onder de actie **Power Automate**

    :::image type="content" source="media/power-automate-action-intro.png" alt-text="Toont de actie Automatiseren in de actiebalk met uitgevouwen acties.":::

    Op sommige pagina's wordt **Automatiseren** genest onder **Meer opties (...)**. 
2. Vul in het deelvenster **Stroom uitvoeren** de vereiste velden in en selecteer vervolgens **Doorgaan** om de stroom te starten.

> [!NOTE]
> De eerste keer dat u de optie **Automatiseren** uitvoert, ziet u mogelijk alleen de actie **Aan de slag met Power Automate**. U ziet deze actie omdat u niet akkoord bent gegaan met de privacyverklaring voor Microsoft Power Automate. Selecteer om door te gaan **Aan de slag met Power Automate** en volg de instructies om het eens of oneens te zijn.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Toont de optie Automatiseren in de actiebalk.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## Stromen bewerken, maken en beheren

Het maken van nieuwe stromen, het wijzigen en beheren van bestaande (zoals aan- of uitzetten) kan direct in Power Automate. Maar u kunt sommige van deze taken vanuit [!INCLUDE[prod_short](includes/prod_short.md)] starten:

- Als u een directe stroom wilt maken vanaf een lijst-, kaart- of documentpagina, selecteert u **Automatiseren** > **Een stroom maken**.
- Als u Power Automate wilt openen vanaf een lijst-, kaart- of documentpagina, selecteert u **Automatiseren** > **Stromen beheren**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Deze taken worden meestal uitgevoerd door een beheerder of supergebruiker. De taken vereisen een bredere kennis van de bedrijfsprocessen in [!INCLUDE[prod_short](includes/prod_short.md)]. Voor meer informatie bekijkt u [Power Automate-integratie](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview), [Directe stromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) en [Power Automate-stromen beheren](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows).
<!-- 

## Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## Zie gerelateerde [Microsoft-training](/training/modules/use-power-automate/)

## Zie ook

[Problemen met uw [!INCLUDE[prod_short](includes/prod_short.md)] geautomatiseerde werkstromen](across-flow-troubleshoot.md) oplossen  
[Zich voorbereiden om zaken te doen](ui-get-ready-business.md)  
[Werkstromen](across-workflow.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md) instellen  
[Financiën](finance.md)  
[Power Automate-stromen beheren](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Directe stromen inschakelen](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
a