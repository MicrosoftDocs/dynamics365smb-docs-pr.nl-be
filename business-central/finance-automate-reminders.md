---
title: Aanmaningen in incasso's automatiseren
description: 'Bespaar tijd bij incasso''s door de processen voor het maken, afgeven en verzenden van aanmaningen aan klanten te automatiseren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="automate-reminders-in-collections"></a>Aanmaningen in incasso's automatiseren

Maak uw incasso´s effectiever door het proces voor het maken, afgeven en verzenden van aanmaningen aan uw klanten te automatiseren. Automatisering kan de tijd die u aan incasso's besteedt aanzienlijk verminderen, een beter overzicht van het proces bieden en u volledige controle geven over elke stap.

Op de pagina **Automatisering van aanmaningen** definieert u de afzonderlijke acties (stappen). U kunt de stappen voor het maken, afgeven en verzenden van aanmaningen combineren, of u kunt voor elke stap een aparte automatisering maken als dat beter is voor uw incassoprocessen. Automatiseringen zijn gebaseerd op aanmaningstermijnen en aanmaningsniveaus. Ga voor meer informatie naar [De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md). U kunt filters instellen voor aanmaningstermijnen voor een automatisering als geheel, en filters instellen voor elke actie in de automatisering. U kunt openstaande facturen ook als PDF-bestand aan e-mails toevoegen.

Automatisering gebeurt via een taakwachtrij-item. Wanneer u een automatisering instelt, gebruikt u het veld **Cadans** om op te geven hoe en wanneer deze wordt uitgevoerd. Als u **Handmatig** kiest, wordt de automatisering eenmalig uitgevoerd wanneer u de actie **Starten** gebruikt. U kunt ook **Wekelijks**, **Maandelijks** of **Aangepast** kiezen om een gedetailleerdere cadans in te stellen. Als u **Aangepast** kiest, moet u een datumformule invoeren. Ga voor meer informatie over het invoeren van een datumformule naar [Datumformules gebruiken](ui-enter-date-ranges.md#use-date-formulas). Wanneer u een andere optie dan **Handmatig** kiest, loopt de automatisering door totdat u deze pauzeert. Als u nog specifieker wilt zijn over wanneer de taak wordt uitgevoerd, gebruikt u de actie **Taakwachtrij-items** om de pagina **Taakwachtrij-items** te openen en de herhaling aan te passen, bijvoorbeeld dagelijks of een specifieke weekdag.

## <a name="automate-the-reminders-flow"></a>De aanmaningsstroom automatiseren

In de volgende gedeelten wordt beschreven hoe u aanmaningen kunt instellen zodat deze automatisch kunnen worden gemaakt, afgegeven en verzonden.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Automatisering van aanmaningen** in en kies vervolgens de gerelateerde koppeling.
1. Kies **Nieuw** en vul vervolgens de velden op het sneltabblad **Algemeen** in.
1. Kies in het veld **Filter voor aanmaningstermijnen** de aanmaningstermijn of -termijnen waarvoor u deze automatisering wilt gebruiken.
1. Kies in het veld **Cadans** hoe vaak de automatisering wordt uitgevoerd.
1. Kies op het sneltabblad **Acties** **Nieuw** en kies vervolgens of met de automatisering aanmaningen worden gemaakt, afgegeven of verzonden. Klik op **OK**.
1. Afhankelijk van het actietype dat de automatisering uitvoert, vult u indien nodig de velden op de instellingenpagina in. Ga voor meer informatie over de instellingen naar [Instellingen voor aanmaningsacties](#settings-for-reminder-actions).
1. Nadat u de acties voor de automatisering hebt ingesteld, kunt u de acties **Omhoog** en **Omlaag** gebruiken om de volgorde aan te passen waarin ze worden uitgevoerd.

## <a name="settings-for-reminder-actions"></a>Instellingen voor aanmaningsacties

De instellingen verschillen voor de acties Aanmaning maken, Aanmaning afgeven en Aanmaning verzenden. In de volgende gedeelten wordt uitgelegd hoe u de acties gebruikt:

### <a name="create"></a>Maken

* Het hoogste niveau op alle aanmaningsregels instellen.  
* Aanmaningen maken voor posten die in de wacht staan. Deze instelling is bijvoorbeeld handig als u een lopend geschil hebt met een klant en wilt dat deze het grote geheel ziet.
* Aanmaningen maken voor alle onbetaalde facturen, en niet alleen voor facturen die te laat zijn. In het rapport worden achterstallige facturen en facturen die nog niet zijn betaald, maar nog niet achterstallig zijn, in afzonderlijke secties weergegeven.
* Filters instellen om de aanmaning specifieker te maken.

### <a name="issue"></a>Verzenden

Wanneer u een aanmaning verzendt, maakt u posten aan in het klantenboek dat de boekingsdatum en belastingdatum bevat. Gebruik de instellingen op de pagina **Instellingen voor aanmaningen verzenden** om op te geven of de informatie op de afgegeven aanmaning moet worden vervangen door de informatie uit de gemaakte aanmaning. Als u bijvoorbeeld de aanmaning gisteren hebt gemaakt en deze vandaag hebt afgegeven, wordt de vervaldatum één dag verschoven.

### <a name="send"></a>Verzenden

> [!NOTE]
> Voor de automatisering van verzenden is het vereist dat u e-mail hebt ingesteld in [!INCLUDE [prod_short](includes/prod_short.md)]. Ga voor meer informatie over het instellen van e-mail naar [E-mail instellen](admin-how-setup-email.md).

De inhoud van de e-mails, zoals bijlageteksten, hoofdteksten van e-mails en taal komen voort uit de instelling van de aanmaningstermijn. Ga voor meer informatie over e-mailinstellingen naar [De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md).

Gebruik de instellingen op de pagina **Instellingen voor aanmaningen verzenden** voor het volgende:

* Algemene instellingen, zoals de beschrijving en hoe vaak u dezelfde aanmaning verzendt.
* Instellingen voor wat er in de aanmaning moet worden opgenomen.
* Instellingen voor het bijhouden van de aanmaningen die u verzendt door interacties te maken, of u de aanmaning afdrukt of per e-mail verzendt en of u alleen achterstallige facturen, alle facturen of geen facturen wilt bijvoegen. 

## <a name="access-the-history-of-a-reminder"></a>Toegang tot de geschiedenis van een aanmaning

Met [!INCLUDE [prod_short](includes/prod_short.md)] wordt elke keer bijgehouden dat een automatisering wordt uitgevoerd. U kunt toegang krijgen tot de geschiedenis door de actie **Logboekvermeldingen** te kiezen. U kunt ook gebruikmaken van de actie **Afgegeven aanmaningen** om toegang te krijgen tot een lijst met de aanmaningen die u hebt afgegeven.

## <a name="handle-errors"></a>Afhandeling van fouten

Op het sneltabblad **Acties** kunt u voor elke actie opgeven of u wilt dat de automatisering stopt als de actie een fout bevat. Als u dat doet, worden met de automatisering de acties niet verwerkt die daarna volgen. Om deze functie in of uit te schakelen, gebruikt u de actie **Stoppen bij fout instellen** of **Stoppen bij fout wissen**.

## <a name="change-action-settings-for-an-automation"></a>Actie-instellingen voor een automatisering wijzigen

U kunt op elk gewenst moment de instellingen voor een automatisering wijzigen. Kies op het sneltabblad **Acties** **Instellen** en breng vervolgens uw wijzigingen aan.

## <a name="see-also"></a>Zie ook

[Termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md)  
[Aanmaningen voor uitstaande saldi verzenden](receivables-send-reminders.md)  
