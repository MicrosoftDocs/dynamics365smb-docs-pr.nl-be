---
title: Gegevens opschonen met bewaarbeleid
description: U kunt aangeven hoe vaak u bepaalde soorten gegevens wilt verwijderen.
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
---
# <a name="define-retention-policies"></a>Bewaarbeleid definiëren

Dit artikel beschrijft hoe beheerders bewaarbeleid kunnen definiëren om aan te geven hoe vaak ze willen dat verouderde gegevens worden verwijderd in tabellen die logboekvermeldingen en gearchiveerde records bevatten. Het opschonen van logboekvermeldingen kan het bijvoorbeeld gemakkelijker maken om te werken met relevantere gegevens. Beleid kan gegevens verwijderen op basis van een vervaldatum, of u kunt filters toevoegen om alleen bepaalde verlopen gegevens op te nemen.

## <a name="required-setups-and-permissions"></a>Vereiste instellingen en machtigingen

Voordat u bewaarbeleid kunt maken, moet u de tabellen instellen die moeten worden opgenomen en de perioden waarin gegevens moeten worden bewaard.

|Instellen  |Omschrijving  |
|---------|---------|
|**Toegestane tabellen**     |We bieden een lijst met de tabellen die u kunt opnemen in het bewaarbeleid. Als u tabellen uit een extensie aan een bewaarbeleid wilt toevoegen, moet een ontwikkelaar de tabellen aan de lijst toevoegen. Ga voor meer informatie naar [Uw extensie opnemen in een bewaarbeleid](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Bewaarperioden**     |Geef perioden op waarvoor gegevens in de tabellen in een beleid moeten worden bewaard. De perioden bepalen hoe vaak gegevens worden verwijderd.         |

Bovendien moet u beschikken over de **SUPER**-gebruikersmachtigingen of de machtigingenset **Bewaarbeleid instellen**. Gebruikers met de machtigingenset Bewaarbeleid instellen kunnen bewaarbeleid voor tabellen definiëren. Dat is waar, zelfs als ze geen lees- en verwijderrechten voor de tabellen hebben. De taakwachtrij-invoer moet worden uitgevoerd als een gebruiker met machtigingen om de gegevens te lezen en te verwijderen. Verleen de machtigingenset Bewaarbeleid niet aan gebruikers die geen toestemming mogen krijgen om gegevens te verwijderen.

> [!NOTE]
> Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt en u wilt bewaarbeleid uitproberen in de Cronus-demonstratiedatabase, zijn er een paar dingen die u moet doen. Het demonstratiebedrijf bevat geen tabellen die u kunt gebruiken met bewaarbeleid, dus u moet deze toevoegen. Om dat te doen maakt u een nieuw, leeg bedrijf in de demonstratiedatabase. Importeer in het nieuwe bedrijf het RapidStart-configuratiepakket voor uw land/regio, dat overeenkomt met het standaardpakket NAV17.0.W1.ENU.STANDARD.rapidstart. De instellingsgegevens voor het bewaarbeleid zijn beschikbaar in het nieuwe bedrijf.

### <a name="create-retention-periods"></a>Bewaarperioden maken

Bewaarperioden kunnen zo lang of kort zijn als u wilt. Om bewaartermijnen te maken gebruikt u op de pagina **Bewaarbeleid** de actie **Bewaarperiode**. De door u gedefinieerde perioden zijn beschikbaar voor al het beleid.

> [!NOTE]
> Om complianceredenen hebben we voor sommige tabellen een minimale bewaartermijn gedefinieerd. Als u een bewaartermijn instelt dat korter is dan vereist, wordt een bericht weergegeven met de verplichte periode.

### <a name="set-up-a-retention-policy"></a>Een bewaarbeleid instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bewaarbeleid** in en kies vervolgens de gerelateerde koppeling.
2. Kies in het veld **Tabel-id** de tabel die u wilt opnemen in het beleid.
3. Geef in het veld **Bewaarperiode** op hoe lang de gegevens in de tabel moeten worden bewaard.
4. Optioneel: als u het beleid op specifieke gegevens in een tabel wilt toepassen, schakelt u de schakelaar **Toepassen op alle records** uit. Het sneltabblad **Bewaarbeleid van record** wordt weergegeven, zodat u filters kunt instellen om subsets met gegevens voor elke regel te maken. Ga voor meer informatie naar [Filtering](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Elke regel heeft zijn eigen bewaarperiode. Als u verschillende bewaarperioden opgeeft voor dezelfde gegevens, wordt de langste periode gebruikt. Sommige tabellen bevatten ook filters die u niet kunt wijzigen of verwijderen. Om u te helpen deze filters te identificeren, worden ze weergegeven in een lichter lettertype.

#### <a name="video-guidance"></a>Videobegeleiding

Deze video geeft een voorbeeld van hoe u een bewaarbeleid instelt.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## <a name="apply-retention-policies"></a>Bewaarbeleid toepassen

U kunt een taakwachtrij-item gebruiken om bewaarbeleid toe te passen om gegevens automatisch te verwijderen, of u kunt handmatig beleid toepassen.

Om automatisch een bewaarbeleid toe te passen hoeft u alleen maar een beleid te maken en in te schakelen. Wanneer u een beleid inschakelt, maakt [!INCLUDE [prod_short](includes/prod_short.md)] een taakwachtrij-item dat het beleid toepast volgens de bewaarperiode. Al het bewaarbeleid gebruikt hetzelfde taakwachtrij-item. Standaard past het taakwachtrij-item het beleid elke dag toe om 0200. U kunt de standaardinstelling wijzigen, maar als u dat doet, raden we u aan om het buiten kantooruren te laten doen. Ga voor meer informatie naar [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md). 

U kunt handmatig een beleid toepassen met behulp van de actie **Handmatig vereffenen** op de pagina **Bewaarbeleid**. Als u een beleid altijd handmatig wilt toepassen, schakelt u de schakelaar **Handmatig** in. Het taakwachtrij-item negeert het beleid wanneer het wordt uitgevoerd.

## <a name="view-retention-policy-log-entries"></a>Logboekvermeldingen voor bewaarbeleid bekijken

U kunt activiteiten met betrekking tot bewaarbeleid bekijken op de pagina **Logboek van bewaarbeleid**. Er worden bijvoorbeeld posten gemaakt wanneer een beleid wordt toegepast, of als er fouten zijn opgetreden.

## <a name="include-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Uw extensie opnemen in een bewaarbeleid (hulp van een ontwikkelaar vereist)

Standaard geldt het bewaarbeleid alleen voor [!INCLUDE[prod_short](includes/prod_short.md)] in de lijst die we verstrekken. U kunt standaardtabellen uit de lijst verwijderen en u kunt tabellen toevoegen waarvan u de eigenaar bent. Dat wil zeggen dat u geen tabel kunt toevoegen die u niet zelf hebt gemaakt. U kunt bijvoorbeeld geen andere tabellen toevoegen vanuit [!INCLUDE[prod_short](includes/prod_short.md)] of vanuit een extensie die u hebt gekocht.

Om uw tabellen aan de lijst met toegestane tabellen toe te voegen, moet een ontwikkelaar wat code toevoegen. Bijvoorbeeld aan de installatiecodeunit voor de extensie (een codeunit met het subtype *install*).

Wanneer ontwikkelaars een tabel toevoegen, kunnen ze verplichte en standaardfilters specificeren. Verplichte filters kunnen later niet worden verwijderd of gewijzigd wanneer u tabellen toevoegt om een bewaarbeleid te definiëren. De standaardfilters zijn slechts suggesties.

Hieronder volgen voorbeelden van hoe u een tabel kunt toevoegen aan de lijst met toegestane tabellen met en zonder verplichte of standaardfilters. Voor een complexer voorbeeld gaat u naar codeunit 3999 'Bewaarbeleid installeren - BaseApp'.

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Het volgende voorbeeld bevat een verplicht filter.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Nadat een ontwikkelaar tabellen aan de lijst heeft toegevoegd, kan een beheerder deze opnemen in een bewaarbeleid. 

## <a name="see-also"></a>Zie ook

[Traceringstelemetrie voor bewaarbeleid analyseren](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Wijzigingen controleren in Business Central](across-log-changes.md)  
[Filteren](ui-enter-criteria-filters.md#filtering)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
