---
title: Printers instellen
description: Lees meer over het instellen van printers die u kunt gebruiken voor rapporten en documenten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.date: 05/17/2021
ms.author: jswymer
ms.openlocfilehash: c98006d85607a62f99286e1179728b969fa4d005
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/19/2021
ms.locfileid: "6063464"
---
# <a name="set-up-printers"></a>Printers instellen

Documenten en rapporten afdrukken vanuit [!INCLUDE[prod_short](includes/prod_short.md)] is een belangrijke taak voor zakelijke gebruikers. Gebruikers willen afdruktaken meestal rechtstreeks naar een van de printers van uw organisatie sturen&mdash;ongeacht welke [!INCLUDE[prod_short](includes/prod_short.md)]-client of -app ze gebruiken. Omdat [!INCLUDE[prod_short](includes/prod_short.md)] online een cloudservice is, kan het lokale printers die zijn aangesloten op de apparaten van gebruikers niet rechtstreeks bereiken, maar het kan wel verbinding maken met cloud-compatibele printers.

Om uw printbehoeften te ondersteunen, biedt [!INCLUDE[prod_short](includes/prod_short.md)] de volgende functies:

|Functie|Omschrijving|Webclient| Mobiele app|App voor Teams|
|-------|-----------|----------|-----------|--------------|
|Universeel afdrukken|Universeel afdrukken is een oplossing voor printerbeheer die beschikbaar is als cloudservice van Microsoft. Met deze functie kunt u uw printers instellen in Universeel afdrukken en ze vervolgens registreren voor gebruik in [!INCLUDE[prod_short](includes/prod_short.md)]. Deze functie vereist een Universeel afdrukken-abonnement en de extensie **Integratie met universeel afdrukken**|![werkt online](media/check.png)|![werkt online](media/check.png)|![werkt online](media/check.png)|
|E-mail afdrukken|Met deze functie kunt u printers met e-mail instellen. [!INCLUDE[prod_short](includes/prod_short.md)] stuurt vervolgens afdruktaken naar een printer met behulp van het e-mailadres van de printer. Voor deze functie zijn printers met e-mailfunctie vereist en de extensie **Verzenden naar e-mailprinter**.|![werkt online](media/check.png)|![werkt online](media/check.png)|![werkt online](media/check.png)|
|Afdrukken met browser|Afdruktaken worden afgehandeld door de afdrukfunctionaliteit van de browser van de gebruiker. Als geen cloudprinter is geïnstalleerd en ingesteld of als een geïnstalleerde printer niet werkt, wordt het afdrukken standaard ingesteld op de afdrukopties voor de browser. Het veld **Printer** op de rapportverzoekpagina bevat *(Door de browser afgehandeld)*.|![werkt online](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt ook aangepaste printerextensies die nog meer afdrukfuncties toevoegen. Dus als er aangepaste printerextensies zijn geïnstalleerd, bevat uw toepassing mogelijk afdrukfuncties die niet in dit artikel worden beschreven. 

## <a name="set-up-universal-print"></a>Universeel afdrukken instellen

Universeel afdrukken is een service op basis van een Microsoft 365-abonnement die volledig draait op Microsoft Azure. Het biedt u gecentraliseerd printerbeheer via de Universeel afdrukken-portal. [!INCLUDE[prod_short](includes/prod_short.md)] maakt printers die zijn ingesteld in Universeel afdrukken, beschikbaar voor clientgebruikers via de extensie **Integratie met Universeel afdrukken**.

![Universele afdrukinstellingen](media/Universal-Print-arch.png)

De volledige installatie vereist dat u werkt in Microsoft Azure, met behulp van de [Azure-portal](https://portal.azure.com), en in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Ondersteunde printers

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt dezelfde printers als Universeel afdrukken. Dat kunnen zowel Universeel afdrukken-compatibele als niet-compatibele printers zijn. Niet-compatibele printers kunnen niet rechtstreeks met Universeel afdrukken communiceren, dus hebben ze extra connectorsoftware nodig, die wordt geleverd door Universeel afdrukken. Sommige oudere printers worden mogelijk niet ondersteund. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Vereisten

**Voor [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] 2021 releasewave 1 of hoger
- Extensie **Integratie met Universeel afdrukken** is geïnstalleerd

    Deze extensie wordt standaard gepubliceerd en geïnstalleerd als onderdeel van [!INCLUDE[prod_short](includes/prod_short.md)] online en on-premises.  U kunt controleren of het is geïnstalleerd op de pagina **Extensiebeheer**. Zie [Extensies installeren en verwijderen in Business Central](ui-extensions-install-uninstall.md) voor meer informatie.
- [!INCLUDE[prod_short](includes/prod_short.md)] on-premises:
  - Azure Active Directory (AD) of NavUserPassword-verificatie is geconfigureerd
  - Een aanvraag voor Business Central is geregistreerd in uw Azure AD-tenant en [!INCLUDE[prod_short](includes/prod_short.md)]

      Net als andere Azure-services die werken met [!INCLUDE[prod_short](includes/prod_short.md)], vereist Universeel afdrukken een app-registratie voor [!INCLUDE[prod_short](includes/prod_short.md)] in Azure Active Directory (Azure AD). De app-registratie biedt verificatie- en autorisatieservices tussen [!INCLUDE[prod_short](includes/prod_short.md)] en Universeel afdrukken.

      Uw implementatie maakt mogelijk al gebruik van een app-registratie voor andere Azure-services, zoals Power BI. Gebruik dan de bestaande app-registratie voor Universeel afdrukken, in plaats van een nieuwe toe te voegen. Het enige wat u in dit geval hoeft te doen, is de app-registratie aanpassen om de relevante afdrukmachtigingen voor Microsoft Graph API op te nemen.

      Om een app te registreren en de juiste machtigingen in te stellen volgt u de stappen die worden beschreven in [Een toepassing registreren in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Voor Universeel afdrukken**

- Een Universal Print-abonnement/licentie voor uw organisatie.

    Zie voor meer informatie [Universeel afdrukken in licentie nemen](/universal-print/fundamentals/universal-print-license).

- U hebt de rollen **Printerbeheer** en **Globale beheerder** in Azure.

    Om Universeel afdrukken te beheren moet uw account de rollen **Printerbeheer** en **Globale beheerder** in Azure AD hebben. Deze rollen zijn alleen nodig voor het beheer van Universeel afdrukken. Ze zijn niet vereist door gebruikers om de printers te gebruiken van [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Universeel afdrukken instellen en printers toevoegen in Microsoft Azure

Voordat u Universeel afdrukken-printers in Business Central kunt gaan beheren, zijn er verschillende taken die u moet doorlopen om Universeel afdrukken in Azure te laten werken met de printers die u wilt gebruiken.

Zie voor gedetailleerde instructies voor het instellen [Aan de slag: Universeel afdrukken instellen](/universal-print/fundamentals/universal-print-getting-started) in de documentatie van Universeel afdrukken. Hier is een overzicht van de stappen die u moet doorlopen. De meeste van deze stappen worden uitgevoerd in de Azure-portal.

1. Wijs Universeel afdrukken-licenties toe aan uzelf en andere gebruikers.

    Hoe u de licentie toewijst, is afhankelijk van of u integreert met Business Central online of on-premises.

    - Met [!INCLUDE[prod_short](includes/prod_short.md)] online wijst u licenties toe met behulp van het Microsoft 365-beheercentrum.

      Zie voor meer informatie [Help bij Microsoft-beheercentrum - Licenties toewijzen aan gebruikers](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Met [!INCLUDE[prod_short](includes/prod_short.md)] on-premises wijst u licenties in uw Azure-tenant toe met behulp van de Azure-portal.

      Zie voor meer informatie [Azure Directory: Licenties toewijzen of verwijderen in de Azure Active Directory-portal](/azure/active-directory/fundamentals/license-users-groups).

2. Installeer de Universeel afdrukken-connector om printers te registreren die niet rechtstreeks met Universeel afdrukken kunnen communiceren.

    De meeste printers op de markt kunnen niet rechtstreeks communiceren met Universeel afdrukken. Voor deze printers moet u de Universeel afdrukken-connector installeren. Zie voor meer informatie [De Universeel afdrukken-connector installeren](/universal-print/fundamentals/universal-print-connector-installation).

3. Uw printers registreren in Universeel afdrukken.

    Door een printer te registreren wordt Universeel afdrukken op de hoogte van de printer.

    - Voor printers die rechtstreeks met Universeel afdrukken kunnen communiceren, volgt u de stappen van de printerfabrikant.

    - Registreer voor andere printers de printers met behulp van de Universeel afdrukken-connector. 

      Zie voor meer informatie [Printerregistratie](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Printereigenschappen wijzigen (optioneel)

    Nadat een printer is geregistreerd, kunt u printereigenschappen bekijken en wijzigen, zoals standaardvoorkeuren.

    Voor meer informatie, zie [Printerinstellingen beheren met de Universeel afdrukken-portal](/universal-print/portal/configure-printer-settings).

5. Deel de printers.

    Elke printer die u wilt gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)] moet worden gedeeld in Universeel afdrukken.

    <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Zie voor meer informatie [Een printer delen](/universal-print/portal/share-printers).

6. Gebruikers machtiging voor de gedeelde printers geven.

    <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Zie voor meer informatie [Printermachtigingen](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Documentconversie inschakelen.

    Universeel afdrukken maakt inhoud gereed voor afdrukken in XPS-indeling. Sommige oudere printers op de markt ondersteunen geen weergave van XPS-content&mdash;in veel gevallen alleen pdf-indeling. Afdrukken naar deze printers zal mislukken, tenzij Universeel afdrukken is ingesteld om documenten naar het door de printer ondersteunde formaat te converteren.

    Zie voor meer informatie [Overzicht van documentconversie](/universal-print/portal/document-conversion).

    > [!TIP]
    > Als geen van uw printers het weergaveformaat voor PDF-inhoud nodig heeft, raden we u aan om documentconversie niet in te schakelen, omdat dit de afdrukkwaliteit kan beïnvloeden.

Nu bent u klaar om de printers toe te voegen aan [!INCLUDE[prod_short](includes/prod_short.md)], standaardprinters voor rapporten in te stellen en af te drukken.  

### <a name="add-universal-printer-printers-to-business-central"></a>Universeel afdrukken-printers toevoegen aan Business Central

Nadat printers zijn ingesteld en gedeeld in Universeel afdrukken, bent u klaar om ze door Business Central te laten gebruiken. Er zijn twee manieren om Universeel afdrukken-printers toe te voegen. U kunt de printers allemaal tegelijk of afzonderlijk een voor een toevoegen.

Door printers afzonderlijk toe te voegen kunt u dezelfde Universeel afdrukken-printer meerdere keren in Business Central instellen. Vervolgens kunt u voor elke toegevoegde printer de afdrukinstellingen wijzigen, zoals papierlade, formaat en afdrukstand. Op deze manier kunt u printers instellen voor verschillende rapporten en documenten die speciale uitvoervereisten hebben.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer de desbetreffende koppeling.
2. Selecteer **Universeel afdrukken** en kies vervolgens een van de volgende opties:

    - **Alle printers voor Universeel afdrukken toevoegen** om alle printers toe te voegen die nog niet zijn toegevoegd. U kunt deze optie ook gebruiken als er al printers zijn toegevoegd. 

    - **Voeg een Universeel afdrukken-printer toe** om een specifieke printer toe te voegen.  
3. Volg de instructies op het scherm.

    - Als u **Alle printers voor Universeel afdrukken toevoegen** kiest, begint de instelling **Printers voor Universeel afdrukken toevoegen**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Als u **Een printer voor Universeel afdrukken toevoegen** kiest, wordt de pagina **Instellingen van printer voor Universeel afdrukken** weergegeven. Vul het veld **Naam** in en selecteer **...** naast het veld **Share afdrukken in Universeel afdrukken** om de Universeel afdrukken-printer te selecteren. Vul de resterende velden in zoals nodig. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Deze acties verifiëren uw Azure AD-instelling (voor on-premises), controleren of u een Universeel afdrukken-licentie hebt en voegen ten slotte de printers toe.

    > [!NOTE]
    > Voor on-premises, als dit de eerste keer is dat u verbinding maakt met Universeel afdrukken, wordt de pagina MACHTIGINGEN VAN AZURE ACTIVE DIRECTORY-SERVICE weergegeven en wordt u gevraagd toestemming te geven aan Azure Services. U hoeft deze toestemming maar één keer te geven.

Nadat een printer is toegevoegd, kunt u de instellingen ervan bekijken en wijzigen via het **Printerbeheer**. Selecteer gewoon de printer en kies **Printerinstellingen bewerken**. 

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>E-mail afdrukken instellen

### <a name="prerequisites"></a>Vereisten

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 releasewave 1 of hoger
- Extensie **Verzenden naar e-mailprinter** is geïnstalleerd

    Deze extensie is standaard geïnstalleerd. Zie voor informatie over het installeren van extensies 
- E-mailfunctionaliteit is ingesteld.

   Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

### <a name="add-an-email-printer"></a>Een e-mailprinter toevoegen

Op de pagina **Printerbeheer** ziet u de printers die momenteel zijn ingesteld. De pagina geeft u ook toegang tot de pagina **Instellingen** voor elke printer om een bestaande instelling te bewerken of een nieuwe printer in te stellen.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer de desbetreffende koppeling.
2. Selecteer **E-mail afdrukken** en kies vervolgens **Een e-mailprinter toevoegen**.
3. Vul de vereiste velden in op de pagina **Instellingen van e-mailprinter**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > U moet handmatig het juiste papierformaat voor een printer selecteren, omdat er geen lokale printer of gebruikersinstellingen kunnen worden opgeslagen.
    >
    > Houd er rekening mee dat de extensie E-mailprinter standaard is ingesteld op **A4**-papierformaat, dat bijvoorbeeld niet geschikt is in Noord-Amerika.

### <a name="privacy-notice"></a>Privacyverklaring

Als u de extensie E-mailprinter gebruikt, worden alle of sommige afdruktaken verzonden naar het e-mailadres dat is geconfigureerd voor de printer. We raden ten zeerste aan om een unieke e-mail-id te koppelen aan een printerapparaat met alleen de officiële services van de hardwarefabrikant, zoals HP ePrint, KonicaMinolta EveryonePrint of Epson Email Print.

Neem alle benodigde privacyvoorzorgsmaatregelen, inclusief ervoor zorgen dat de oplossing voor het afdrukken van e-mail goed geconfigureerde machtigingen, privacyinstellingen en bewaarbeleid heeft. Het is uw verantwoordelijkheid om een correct, geverifieerd en operationeel e-mailadres op te geven. Zie voor meer informatie [Privacyverklaring van Microsoft](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Standaardprinters instellen

Er is een aantal manieren om printers in te stellen die standaard worden gebruikt voor afdruktaken. Een standaardprinter is handig als u met verschillende rapporten werkt waarvoor verschillende printers nodig zijn vanwege hun plaatsing in het bedrijf of hun uitvoermogelijkheden.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Een printer instellen als standaardprinter voor alle afdruktaken

Op de pagina **Printerbeheer** kunt u een printer instellen als standaardprinter voor alle afdruktaken. U kunt de printer als standaard instellen, alleen voor u of voor alle gebruikers.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer de desbetreffende koppeling.

    > [!TIP]
    > U kunt de pagina **Printerbeheer** ook openen vanuit de pagina **Printerselecties** door **Printerbeheer** te kiezen.  
2. Selecteer op de pagina **Printerbeheer** een printer in de lijst en kies **Beheren**. Kies vervolgens **Instellen als mijn standaardprinter** of **Instellen als standaardprinter voor alle gebruikers**.

> [!NOTE]
> Als u een standaardprinter instelt vanuit het **Printerbeheer**, wordt een vermelding toegevoegd aan de **printerselecties**.

### <a name="set-a-default-printer-for-specific-reports"></a>Een standaardprinter instellen voor specifieke rapporten

Op de pagina **Printerselecties** kunt u de printer opgeven die een rapport standaard zal gebruiken. Standaardprinters worden ingesteld per gebruikersaccount. U kunt een standaardprinter instellen voor alleen uzelf, een andere gebruiker of alle gebruikers.

> [!IMPORTANT]
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan de pagina **Printerselecties** alleen worden gebruikt voor cloudprinters die zijn gedefinieerd door printerextensies, zoals E-mailprinters en Universeel afdrukken-printers. Het kan niet worden gebruikt voor lokale printers.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerselecties** in en selecteer de desbetreffende koppeling. Als alternatief selecteert u vanaf de pagina **Printerbeheer** een printer en kiest u vervolgens de actie **Printerselecties**.
2. Kies de actie **Nieuw** om een printerselectie toe te voegen voor een specifiek rapport.
3. Vul de vereiste velden in.

Het opgegeven rapport is nu ingesteld om standaard te worden afgedrukt op de geselecteerde printer.

> [!NOTE]
> Wanneer u het betreffende rapport afdrukt, kunt u een andere printer selecteren met het veld **Afdrukken** op de aanvraagpagina.

> [!NOTE]
> Als u geen rapport instelt voor een specifieke printer op de pagina **Printerselecties**, wordt het afgedrukt op de standaardprinter van het bedrijf, zoals gedefinieerd vanuit de pagina **Printerbeheer**.

U of de beheerder kan ook de pagina **Printerselecties** gebruiken om andere afdrukvarianten voor gebruikers en rapporten te definiëren. De volgende tabel beschrijft de combinatie van waarden wanneer u andere printerinstellingen instelt voor een rapport.

|Als u dit wilt doen:                                                 |Stel de volgende waarden in                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Een rapport afdrukken naar een specifieke printer voor alle gebruikers |Geef waarden op in de velden **Rapport-id** en **Printernaam** en laat het veld **Gebruikers-ID** leeg.|
|Alle rapporten naar een specifieke printer afdrukken voor een specifieke gebruiker|Geef waarden op in de velden **Gebruikers-ID** en **Printernaam** en laat het veld **Rapport-id** leeg. Deze vermelding doet hetzelfde als de actie **Instellen als mijn standaardprinter** op de pagina **Afdrukbeheer**.|
|De standaardprinter voor alle gebruikers instellen|Geef een waarde op in het veld **Printernaam** en laat de velden **Gebruikers-ID** en **Rapport-id** leeg. Deze vermelding doet hetzelfde als de actie **Als standaardprinter voor alle gebruikers instellen** op de pagina **Afdrukbeheer**.|
|Een specifiek rapport afdrukken naar de standaardprinter van de gebruiker|Geef een waarde op in het veld **Rapport-id** en laat de velden **Printernaam** en **Gebruikers-ID** leeg.|
|Een specifiek rapport naar een specifieke printer afdrukken voor een specifieke gebruiker|Geef waarden in alle drie de velden op.|

> [!NOTE]
> Specifiekere printerselecties hebben voorrang op algemenere printerselecties. Bijvoorbeeld een printerselectie met waarden in de velden **Gebruikers-ID**, **Rapport-id** en **Printernaam** heeft voorrang op een printerselectie met lege vermeldingen in de velden **Gebruikers-ID** of **Rapport-id**.

### <a name="sizing-print-jobs"></a>Formaat van afdruktaken

Cloudafdrukken zijn ontworpen voor documenten van een redelijk formaat. De meeste cloudservices, inclusief PrintNode en HP ePrint, hebben een limiet van 10 MB per taak. Als u grotere rapporten wilt afdrukken, moet u deze mogelijk in meerdere afdrukken splitsen.

## <a name="see-also"></a>Zie ook

[Een rapport afdrukken](ui-work-report.md#PrintReport)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Batchverwerkingen uitvoeren](ui-how-run-batch-jobs.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]