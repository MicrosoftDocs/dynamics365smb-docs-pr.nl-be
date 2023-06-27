---
title: Accountantervaringen in Business Central (bevat video)
description: Meer informatie over het rolcentrum Accountant en de bedrijfshub die interne en externe accountants ondersteunen in het clientbedrijf.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="accountant-experiences-in-" />Accountantervaringen binnen [!INCLUDE[prod_long](includes/prod_long.md)]

Elk bedrijf moet zijn boekhouding doen en aftekenen. Sommige bedrijven hebben een externe accountant en andere hebben een accountant in dienst. Ongeacht wat voor accountant u bent, u kunt het rolcentrum **Accountant** gebruiken als uw thuis binnen [!INCLUDE[prod_short](includes/prod_short.md)]. Van hieruit hebt u toegang tot alle pagina's die u in uw werk nodig hebt.  

## <a name="accountant-role-center" />Rolcentrum Accountant

Het rolcentrum is een dashboard met activiteittegels die realtime cijfers bevatten en die u snel toegang geven tot gegevens. In het lint boven op de pagina hebt u toegang tot meer acties, zoals het openen van de vaakst gebruikte financiële rapporten en de rekeningoverzichten in Excel. Op de navigatiebalk bovenin kunt u snel schakelen tussen de lijsten die u het meest gebruikt. Hier ziet u andere gebieden, zoals **Geboekte documenten** met de diverse soorten documenten die het bedrijf heeft geboekt.  

Als [!INCLUDE[prod_short](includes/prod_short.md)] nieuw voor u is, kunt u een overzicht van video's direct vanuit uw rolcentrum starten. U kunt ook een **Aan de slag**-rondleiding starten die wijst op belangrijke gebieden.  

## <a name="company-hub" />Bedrijfshub

Als u in meerdere [!INCLUDE [prod_short](includes/prod_short.md)]-bedrijven werkt, vindt u het misschien handig om de pagina **Bedrijfshub** te gebruiken om werk bij te houden.  Zie voor meer informatie [Werk in meerdere bedrijven beheren in de bedrijfshub](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-" /><a name="inviteaccountant"></a>Uw externe accountant uitnodigen voor uw [!INCLUDE[prod_short](includes/prod_short.md)]

Als u een externe auditor gebruikt om uw boeken en financiële rapportage te beheren, kan uw beheerder deze uitnodigen voor uw [!INCLUDE[prod_short](includes/prod_short.md)], zodat hij of zij met u kan werken aan uw fiscale gegevens. [!INCLUDE[prod_short](includes/prod_short.md)] omvat drie licenties van het type Externe accountant. Zie de [Microsoft Dynamics 365 Business Central Licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=871590) voor meer informatie over licenties.

Als de accountant toegang heeft gekregen tot uw [!INCLUDE[prod_short](includes/prod_short.md)], kan hij of zij het rolcentrum **Accountant** gebruiken, dat eenvoudig toegang tot de meest relevante pagina's voor hun werk biedt. Ze kunnen ook de bedrijfshub in hun eigen [!INCLUDE [prod_short](includes/prod_short.md)] gebruiken om hun werk te beheren. Zie voor meer informatie [Werk in meerdere bedrijven beheren in de bedrijfshub](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

We hebben het voor u eenvoudig gemaakt om uw externe accountant uit te nodigen. Open gewoon de pagina **Gebruikers** en kies de actie **Externe accountant uitnodigen** op het lint. Er wordt een e-mail voor u gemaakt. Voeg het werke-mailadres van uw accountant eraan toe en verzend de uitnodiging.  

> [!Note]  
> Dit vereist dat u SMTP-e-mail hebt ingesteld. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Het e-mailadres van de accountant moet een werkadres op basis van Azure Active Directory zijn. Als de accountant een ander type e-mail gebruikt, kan de uitnodiging niet worden verzonden.
>
> Deze taak vereist toegang tot het beheren van gebruikers en licenties in Azure Active Directory. De gebruiker die deze uitnodiging verzendt, moet de rol **Globale beheerder** of **Gebruikersbeheer** in het Microsoft 365-beheercentrum toegewezen krijgen. Zie voor meer informatie [Over beheerdersrollen](/microsoft-365/admin/add-users/about-admin-roles) in de Microsoft 365-beheerdersinhoud.  

### <a name="adding-your-accountant-to-your-microsoft-365-in-the-azure-portal" />Uw accountant toevoegen aan uw Microsoft 365 via de Azure Portal

Als uw beheerder of wederverkoper geen gebruik wenst te maken van de begeleiding **Externe accountant uitnodigen**, kunnen ze een externe gebruiker toevoegen aan de Azure Portal en aan deze gebruiker de licentie *Externe accountant* toewijzen. Zie [Snelle start: gastgebruikers toevoegen aan uw directory in de Azure-portal](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal) voor meer informatie.

#### <a name="to-add-your-accountant-as-a-guest-user" />Uw accountant als gastgebruiker toevoegen

1. Open de [Azure Portal](https://portal.azure.com/).
2. Selecteer **Azure Active Directory** in het linkerdeelvenster.
3. Selecteer onder **Beheren** de optie **Gebruikers**.
4. Selecteer **Nieuwe gastgebruiker**.
5. Selecteer op de pagina **Nieuwe gebruiker** de optie **Gebruiker uitnodigen** en voeg informatie over uw externe accountant toe.  

   Voeg desgewenst een persoonlijk welkomstbericht aan de accountant toe om te laten weten dat hij of zij wordt toegevoegd aan uw [!INCLUDE[prod_short](includes/prod_short.md)].

6. Selecteer **Uitnodigen** om de uitnodiging automatisch te verzenden. Er verschijnt een melding rechtsboven bij het bericht **Gebruiker is uitgenodigd**. 
7. Nadat u de uitnodiging hebt verzonden, wordt het gebruikersaccount automatisch als gast aan de directory toegevoegd.

Daarna moet u de nieuwe gastgebruiker een licentie voor [!INCLUDE[prod_short](includes/prod_short.md)] toewijzen.

#### <a name="to-give-your-accountant-access-to-your-" />Uw accountant toegang geven tot uw [!INCLUDE[prod_short](includes/prod_short.md)]

1. Kies **Profiel** in de Azure Portal bij de zojuist toegevoegde gebruiker en kies **Bewerken**
2. Voer in het veld **Gebruikslocatie** het desbetreffende land/regio in en kies **Opslaan**.
3. Kies **Licenties** en open **Toewijzingen**.
4. Kies de **Dynamics 365 Business Central Externe accountant**-licentie.  
    
    Als deze licentie niet beschikbaar is, neem dan contact op met uw wederverkoper om de licentie aan uw abonnement toe te voegen.

    Specifiek voor evaluatiedoeleinden in een proeftenant kunt u in plaats daarvan gebruik maken van een beschikbare **Dynamics 365 Business Central voor IWS**-licentie. U kunt dit type licentie echter niet gebruiken als u [!INCLUDE[prod_short](includes/prod_short.md)] al hebt aangeschaft. 
5. Sla de toewijzing op.

Als dit lukt, wordt de licentie toegewezen aan de gastgebruiker en wordt het gastaccount gemaakt.

### <a name="importing-the-new-user-into-" />De nieuwe gebruiker importeren in [!INCLUDE[prod_short](includes/prod_short.md)]

De accountant ontvangt een e-mail met de melding dat hij of zij toegang heeft gekregen tot uw Active Directory. Daarna moet u de accountant toegang geven tot het juiste bedrijf in [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company" />De accountant toevoegen aan het juiste bedrijf

1. Open het [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf waarvoor u de accountant toegang wilt geven op [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling  
3. Kies de actie **Nieuwe gebruikers ophalen uit Microsoft 365**.

Hiermee wordt het gebruikersaccount dat u in de Azure Portal hebt gemaakt, naar het bedrijf geïmporteerd. Zie [Een gebruiker toevoegen in Business Central](ui-how-users-permissions.md#adduser) voor meer informatie.  

Als u toegang wilt geven aan meerdere bedrijven, moet u zich bij elk bedrijf aanmelden en dit proces herhalen. U kunt ook de machtigingsgroepen voor het gebruikersprofiel van de accountant bijwerken in [!INCLUDE[prod_short](includes/prod_short.md)], zoals het toewijzen van de *D365 Bus Premium*-gebruikersgroep. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.  

## <a name="see-also" />Zie ook

[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met dimensies](finance-dimensions.md)  
[Financiële overzichten analyseren in Excel:](finance-analyze-excel.md)  
[Werk beheren tussen meerdere bedrijven in de bedrijfshub](company-hub.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cashflowanalyse instellen](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
