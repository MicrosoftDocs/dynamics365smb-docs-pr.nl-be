---
title: Printers voor Universeel afdrukken instellen
description: Ontdek hoe u Universeel afdrukken kunt gebruiken om cloudprinten aan te bieden in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 06/14/2024
ms.custom: bap-template
---

# <a name="set-up-universal-print-printers"></a>Printers voor Universeel afdrukken instellen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Universeel afdrukken is een service op basis van een Microsoft 365-abonnement die volledig draait op Microsoft Azure. Het biedt u gecentraliseerd printerbeheer via de Universeel afdrukken-portal. [!INCLUDE[prod_short](includes/prod_short.md)] maakt printers die zijn ingesteld in Universeel afdrukken, beschikbaar voor clientgebruikers via de extensie **Integratie met Universeel afdrukken**.

![Universele afdrukinstellingen.](media/Universal-Print-arch.png)

De volledige installatie vereist dat u werkt in Microsoft Azure, met behulp van de [Azure-portal](https://portal.azure.com), en in [!INCLUDE[prod_short](includes/prod_short.md)]. De instelling is verdeeld over twee hoofdtaken, zoals beschreven in dit artikel:

1. Stel in Microsoft Azure Universeel afdrukken in en voeg de printers die u in Business Central wilt gebruiken toe aan een afdrukshare. Ga naar [deze sectie](#set-up-universal-print-and-printers-in-microsoft-azure).
2. Voeg in [!INCLUDE[prod_short](includes/prod_short.md)] de printers toe uit de afdrukshares in Universeel afdrukken. Ga naar [dit gedeelte](#add-printers-in-business-central-online) voor online of [hier](#add-printers-in-business-central-on-premises) voor on-premises.

## <a name="prerequisites"></a>Vereisten

- Ondersteunde printers

  [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt dezelfde printers als Universeel afdrukken. Dat kunnen zowel Universeel afdrukken-compatibele als niet-compatibele printers zijn. Niet-compatibele printers kunnen niet rechtstreeks met Universeel afdrukken communiceren, dus hebben ze extra connectorsoftware nodig, die wordt geleverd door Universeel afdrukken. Sommige oudere printers worden mogelijk niet ondersteund. 

- Universeel afdrukken:

  - Een Universal Print-abonnement/licentie voor uw organisatie.

    Meer informatie op [Universeel afdrukken in licentie nemen](/universal-print/fundamentals/universal-print-license).

  - U hebt minimaal de rol  [Printerbeheerder](/entra/identity/role-based-access-control/permissions-reference#printer-administrator) in Microsoft Entra ID.

    Om Universal Print te kunnen beheren, moet uw account minimaal de rol  [Printer Administrator](/entra/identity/role-based-access-control/permissions-reference#printer-administrator) in Microsoft Entra ID hebben. Deze rollen zijn alleen nodig voor het beheer van Universeel afdrukken. Ze zijn niet vereist door mensen die de printers instellen vanuit [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] online en on-premises:

  - [!INCLUDE[prod_short](includes/prod_short.md)] 2021 releasewave 1 of hoger.
  - Extensie **Integratie met Universeel afdrukken** is geïnstalleerd.

    Deze extensie wordt standaard gepubliceerd en geïnstalleerd als onderdeel van [!INCLUDE[prod_short](includes/prod_short.md)] online en on-premises. U kunt controleren of het is geïnstalleerd op de pagina **Extensiebeheer**. Meer informatie op [Extensies installeren en verwijderen in Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] alleen on-premises:
  - Microsoft Entra ID- of NavUserPassword-verificatie is geconfigureerd.
    > [!NOTE]
    >  De extensie Universeel afdrukken biedt geen ondersteuning voor service-to-service (S2S)-authenticatie. Het vereist een aangemelde gebruiker om afdruktaken naar de Universeel afdrukken-service te sturen via Graph API.
  - Een aanvraag voor Business Central is geregistreerd in uw Microsoft Entra-tenant en [!INCLUDE[prod_short](includes/prod_short.md)].

    Net als andere Azure-services die werken met [!INCLUDE[prod_short](includes/prod_short.md)], vereist Universeel afdrukken een app-registratie voor [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Entra ID. De app-registratie biedt verificatie- en autorisatieservices tussen [!INCLUDE[prod_short](includes/prod_short.md)] en Universeel afdrukken.

    Uw implementatie maakt mogelijk al gebruik van een app-registratie voor andere Azure-services, zoals Power BI. Gebruik dan de bestaande app-registratie voor Universeel afdrukken, in plaats van een nieuwe toe te voegen. U hoeft in dit geval alleen de appregistratie te wijzigen door de relevante afdrukmachtigingen op te nemen voor de Microsoft Graph-API: **PrinterShare.ReadBasic.All**, **PrintJob.Create** en **PrintJob.ReadBasic.** 

    Om een app te registreren en de juiste machtigingen in te stellen volgt u de stappen die worden beschreven in [Een toepassing registreren in Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## <a name="set-up-universal-print-and-printers-in-microsoft-azure"></a>Universeel afdrukken en printers instellen in Microsoft Azure

Voordat u Universeel afdrukken-printers in Business Central kunt gaan beheren, zijn er verschillende taken die u moet doorlopen om Universeel afdrukken in Azure te laten werken met de printers die u wilt gebruiken.

Zie voor gedetailleerde instructies voor het instellen [Aan de slag: Universeel afdrukken instellen](/universal-print/fundamentals/universal-print-getting-started) in de documentatie van Universeel afdrukken. Hier is een overzicht van de stappen die u moet doorlopen. De meeste van deze stappen worden uitgevoerd in de Azure-portal.

1. Wijs Universeel afdrukken-licenties toe aan uzelf en andere gebruikers.

    Hoe u de licentie toewijst, is afhankelijk van of u integreert met Business Central online of on-premises.

    - Met [!INCLUDE[prod_short](includes/prod_short.md)] online wijst u licenties toe met behulp van het Microsoft 365-beheercentrum.

      Zie voor meer informatie [Help bij Microsoft-beheercentrum - Licenties toewijzen aan gebruikers](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Met [!INCLUDE[prod_short](includes/prod_short.md)] on-premises wijst u licenties in uw tenant toe met behulp van de Azure-portal.

      Zie voor meer informatie [Licenties toewijzen of verwijderen in de Azure-portal](/azure/active-directory/fundamentals/license-users-groups).

2. Installeer de Universeel afdrukken-connector om printers te registreren die niet rechtstreeks met Universeel afdrukken kunnen communiceren.

    De meeste printers kunnen niet rechtstreeks met Universeel afdrukken communiceren, dus u moet de Universeel afdrukken-connector installeren. Zie voor meer informatie [De Universeel afdrukken-connector installeren](/universal-print/fundamentals/universal-print-connector-installation).

3. Uw printers registreren in Universeel afdrukken.

    Door een printer te registreren wordt Universeel afdrukken op de hoogte van de printer.

    - Voor printers die rechtstreeks met Universeel afdrukken kunnen communiceren, volgt u de stappen van de printerfabrikant.

    - Registreer voor andere printers de printers met behulp van de Universeel afdrukken-connector. 

      Meer informatie op [Printerregistratie](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Printereigenschappen wijzigen (optioneel)

    Nadat een printer is geregistreerd, kunt u printereigenschappen bekijken en wijzigen, zoals standaardvoorkeuren.

    Voor meer informatie zie [Printerinstellingen beheren met de Universeel afdrukken-portal](/universal-print/portal/configure-printer-settings).

5. Deel de printers met gebruikers.

    Elke printer die u wilt gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)] moet worden toegevoegd aan een *afdrukshare* in Universeel afdrukken. Elke gebruiker die toegang tot de printer nodig heeft, moet worden toegevoegd als lid van de afdrukshare. Meer informatie op [Een printer delen](/universal-print/portal/share-printers).

    > [!TIP]
    > U kunt later altijd gebruikers toevoegen of verwijderen. Meer informatie op [Printermachtigingen](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Documentconversie inschakelen.

    Universeel afdrukken maakt inhoud gereed voor afdrukken in XPS-indeling. Sommige oudere printers op de markt ondersteunen geen weergave van XPS-content, in veel gevallen alleen pdf-indeling. Afdrukken naar deze printers zal mislukken, tenzij Universeel afdrukken is ingesteld om documenten naar het door de printer ondersteunde formaat te converteren.

    Meer informatie op [Overzicht van documentconversie](/universal-print/portal/document-conversion).

Nu bent u klaar om de printers toe te voegen aan [!INCLUDE[prod_short](includes/prod_short.md)], standaardprinters voor rapporten in te stellen en af te drukken.  

## <a name="add-printers-in-business-central-online"></a>Printers toevoegen aan Business Central online

Nadat printers zijn ingesteld en gedeeld in Universeel afdrukken, kunt u ze voor gebruik toevoegen aan [!INCLUDE[prod_short](includes/prod_short.md)]. Er zijn twee manieren om Universeel afdrukken-printers toe te voegen. U kunt de printers allemaal tegelijk of afzonderlijk een voor een toevoegen.

Door printers afzonderlijk toe te voegen kunt u dezelfde Universeel afdrukken-printer meerdere keren in [!INCLUDE[prod_short](includes/prod_short.md)] instellen. Vervolgens kunt u voor elke toegevoegde printer de afdrukinstellingen wijzigen, zoals papierlade, formaat en afdrukstand. Op deze manier kunt u printers instellen voor verschillende rapporten en documenten met speciale uitvoervereisten.

> [!NOTE]
> Gebruikt u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises? Zo ja, ga dan naar de [volgende sectie](#add-printers-in-business-central-on-premises); de eerste instelling verloopt iets anders.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **Universeel afdrukken** en kies vervolgens een van de volgende opties:

   - **Alle printers voor Universeel afdrukken toevoegen** om alle printers toe te voegen die nog niet zijn toegevoegd. U kunt deze optie ook gebruiken als er al printers zijn toegevoegd.
   - **Voeg een Universeel afdrukken-printer toe** om een specifieke printer toe te voegen.  
3. Volg de instructies op het scherm.

    - Als u **Alle printers voor Universeel afdrukken toevoegen** kiest, begint de instelling **Printers voor Universeel afdrukken toevoegen**. 

    - Als u **Een printer voor Universeel afdrukken toevoegen** kiest, wordt de pagina **Instellingen van printer voor Universeel afdrukken** weergegeven. Vul het veld **Naam** in en selecteer **...** naast het veld **Share afdrukken in Universeel afdrukken** om de afdrukshare te selecteren die de Universeel afdrukken-printer bevat. Vul de resterende velden in zoals nodig. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Nadat een printer is toegevoegd, kunt u de instellingen ervan bekijken en wijzigen via de pagina **Printerbeheer**. Selecteer gewoon de printer en kies **Printerinstellingen bewerken**.

## <a name="add-printers-in-business-central-on-premises"></a>Printers toevoegen aan Business Central on-premises

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Voordat een gebruiker Universeel afdrukken-printers aan Business Central kan toevoegen of gebruiken, moet deze toegang autoriseren tot de Azure-services die worden gebruikt door Universeel afdrukken en toestemming verlenen voor gegevens en bewerkingen zoals:

- Aanmelden bij en lezen van gebruikersprofiel
- Basisinformatie over afdruktaken lezen
- Afdruktaken maken

Dit gebeurt meestal de eerste keer dat ze verbinding maken met de bij Azure geregistreerde app die wordt gebruikt voor . In Business Central online verloopt deze autorisatiestroom naadloos, zonder tussenkomst van de gebruiker. Maar Business Central on-premises werkt anders. Het vereist dat u, of elke andere gebruiker die Universeel afdrukken-printers wil gebruiken, de authenticatiestroom start&mdash;meestal slechts één keer. De meest directe manier wordt beschreven in de volgende stappen. Een minder directe manier is door verbinding te maken met een andere geïntegreerde service die dezelfde bij Azure geregistreerde app gebruikt, zoals Power BI of OneDrive. Elke gebruiker hoeft deze taak meestal maar één keer uit te voeren.

> [!NOTE]
> Als u een beheerder bent, raden we u aan deze taak voor andere gebruikers uit te voeren. Informeer daarna de gebruikers die Universeel afdrukken-printers moeten gebruiken hoe ze dit moeten doen. Als de bij Azure geregistreerde app voor Universeel afdrukken beheerderstoestemming vereist voor API-machtigingen, is het gemakkelijker als u toestemming verleent namens de organisatie. U kunt toestemming van de beheerder verlenen vanuit de Azure Portal of wanneer u de volgende stappen uitvoert. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### <a name="connect-to-universal-print-for-the-first-time"></a>Voor het eerst verbinding maken met Universeel afdrukken

Voer deze stappen uit om voor het eerst verbinding te maken met de Universeel afdrukken-service.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **Universeel afdrukken** > **Alle Universeel afdrukken-printers toevoegen** om de begeleide instelling (wizard) **Universeel afdrukken** te starten.
3. Volg de instructies op het scherm totdat u bij de pagina **MICROSOFT ENTRA SERVICE-MACHTIGINGEN** komt.

    <!--The MICROSOFT ENTRA SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Microsoft Entra ID setup, checking your Universal Print license, and then adding the printers.-->

   ![Toont de pagina Microsoft ENTRA SERVICEMACHTIGINGEN](media/azure-ad-services-permissions.png "Toont de pagina Microsoft ENTRA SERVICEMACHTIGINGEN")

4. Selecteer de koppeling **Azure Services autoriseren**.

   1. Als de pagina **Toestemming gevraagd** verschijnt, leest u deze aandachtig door en selecteert u **Accepteren** om akkoord te gaan en door te gaan. Als u beheerder bent, kunt u **Akkoord gaan namens organisatie** selecteren als u toestemming wilt geven voor alle gebruikers.

      ![Toont de aanvraagpagina voor Azure-machtigingen](media/azure-ad-permissions-requested.png "Machtigingenpagina voor Azure-verzoeken").

   2. Meld u wanneer daarom wordt gevraagd, aan met uw naam en wachtwoord.

5. Wanneer de autorisatie is voltooid, keert u terug naar de pagina **Printers voor Universeel afdrukken toevoegen**. Selecteer **Volgende** > **Voltooien** om de instelling te voltooien.

Nadat een printer is toegevoegd, kunt u de instellingen ervan bekijken en wijzigen via de pagina **Printerbeheer**. Selecteer gewoon de printer en kies **Printerinstellingen bewerken**.

Nadat u zich voor het eerst hebt aangemeld, kunt u de Universeel afdrukken-printers gebruiken om rapporten en andere afdruktaken af te drukken. Zie voor meer informatie [Een rapport afdrukken](ui-work-report.md#PrintReport). Als u printers wilt toevoegen, verwijderen of wijzigen, gaat u gewoon terug naar de pagina **Afdrukbeheer** en selecteert u **Universeel afdrukken**.

## <a name="common-problems-and-resolutions"></a>Algemene problemen en oplossingen

In dit gedeelte leert u over veelvoorkomende problemen die gebruikers kunnen ondervinden bij het instellen of gebruiken van Universeel afdrukken-printers.

### <a name="you-dont-have-access-to-the-printer-your-printer"></a>U hebt geen toegang tot de printer \<your-printer\>.

Als een gebruiker dit bericht krijgt wanneer deze probeert een document af te drukken naar een Universeel afdrukken-printer, kan dit worden veroorzaakt door een van de volgende omstandigheden:

- De gebruiker heeft geen Universeel afdrukken-licentie toegewezen aan de Microsoft 365- of Azure Active AD-account. 
- De gebruiker is niet toegewezen aan de afdrukshare in Universeel afdrukken.
- (On-premises) De Azure-app-registratie die wordt gebruikt voor Universeel afdrukken werkt niet of is onlangs gewijzigd sinds de laatste keer dat de gebruiker zich aanmeldde.
- (On-premises) De gebruiker is nog niet aangemeld bij de bij Azure geregistreerde app voor de Universele printer-app en heeft voor de eerste keer toestemming gegeven.

## <a name="there-was-an-error-fetching-printers-shared-to-you"></a>Er is een fout opgetreden bij het ophalen van met u gedeelde printers.

Als een gebruiker dit bericht krijgt wanneer deze probeert een Universeel afdrukken-printer toe te voegen vanaf de pagina **Printerbeheer**, komt dat meestal omdat de gebruiker zich nog niet heeft aangemeld bij de in Azure geregistreerde Universele printer-app en voor het eerst toestemming heeft gegeven. 
<!--
### <a name="troubleshooting"></a>Troubleshooting

#### <a name="you-dont-see-the-a-printer-in-the"></a>You don't see the a printer in the

The printer is not shared in Universal Print.

### <a name="you-get-an-error-when-tryong-to-add-all-or-a-single-printer"></a>You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## <a name="could-not-upload-the-document-to-print-job-50"></a>Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## <a name="next-steps"></a>Volgende stappen
[Standaardprinters instellen](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a>Zie ook

[Overzicht van printers](admin-printer-setup-overview.md)  
[E-mailprinters instellen](admin-printer-setup-email.md)
[Een rapport afdrukken](ui-work-report.md#PrintReport)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Batchverwerkingen uitvoeren](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
