---
title: Grootboekrekeningen controleren
description: U kunt uw voortgang volgen wanneer u bedragen op grootboekrekeningen controleert.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
---

# <a name="review-amounts-in-general-ledger-accounts"></a>Bedragen op grootboekrekeningen controleren

Het kan zijn dat u grootboekrekeningen heeft die u regelmatig in de gaten houdt. Of misschien wilt u het beoordelingsproces aan het einde van de maand versnellen. Voor hulp bij het bijhouden wat u hebt gedaan en om controles te versnellen gebruikt u de actie **Posten controleren** op de pagina **Rekeningschema** of de pagina **Grootboekrekening** voor elke rekening. 

## <a name="set-up-accounts-for-reviews"></a>Rekeningen instellen voor controles

Geef op de pagina **Grootboekrekening** voor elke rekening op hoe beoordelingen moeten worden toegestaan in het veld **Controlebeleid**.

|Controlebeleid  |Omschrijving  |
|---------|---------|
|Geen     | U kunt posten voor de rekening niet markeren als beoordeeld. Gebruik deze optie bijvoorbeeld voor rekeningen zoals schulden, vorderingen en bankrekeningen waar er andere manieren zijn om hun bedragen te bekijken.        |
|Controle toestaan     | U hoeft geen boekingen in een overzicht op te nemen en de bedragen van de debet- en creditboekingen hoeven niet in evenwicht te zijn. U verwijdert een controle bijvoorbeeld als u een fout hebt gemaakt.        |
|Controle en afstemmen van saldo toestaan     | De totaalbedragen van de debet- en creditboekingen in het overzicht moeten overeenkomen. De velden **Debet** en **Credit** tonen die bedragen, en het veld **Saldo** toont het totaal. Met deze instelling kunt u ook een controle verwijderen. Wanneer u een controle verwijdert van een of meer posten, moeten de debet- en creditposten nog steeds in evenwicht zijn.        |

## <a name="mark-entries-as-reviewed"></a>Posten als gecontroleerd markeren

Kies de posten die u hebt beoordeeld en gebruik vervolgens de actie **Selectie instellen op gecontroleerd**. Elke keer dat u een of meer posten als gecontroleerd markeert, krijgen de inzendingen hetzelfde nummer in de kolom **Controle-id**. De recensie-id is een handige manier om bij te houden welke inzendingen tegelijkertijd zijn beoordeeld. [!INCLUDE [prod_short](includes/prod_short.md)] registreert ook de gebruiker die de controle heeft gedaan en wanneer ze dit hebben gedaan.

Als u inzendingen markeert als gecontroleerd, maar daar spijt van krijgt, gebruik dan de actie **Selectie instellen op niet-gecontroleerd**.

* Als het beleid Controle toestaan is toegewezen aan de rekening, wordt de gecontroleerde id door de actie teruggezet op 0 en worden de persoon en datum en tijd van de beoordeling verwijderd. 
* Als het beleid Controle en afstemmen van saldo toestaan is toegewezen, moeten credit en debet nog steeds in evenwicht zijn. Als een van de posten in een controle bijvoorbeeld een vergissing is, kunt u een andere post met de juiste waarde kiezen. De vervangende post hoeft niet dezelfde gecontroleerd-id te hebben.

> [!TIP]
> Een snelle manier om meerdere posten te kiezen is door Ctrl of Shift ingedrukt te houden terwijl u de posten kiest. Met Ctrl kunt u specifieke posten selecteren en Shift selecteert alle posten tussen de eerste en laatste post die u selecteert.

## <a name="review-accounts-that-have-old-entries"></a>Rekeningen met oude posten controleren

Misschien hebt u posten uit eerdere periodes die u al hebt gecontroleerd of die gewoon geen controle nodig hebben. U wilt gewoon beginnen met het nakijken van posten vanaf bijvoorbeeld het begin van het jaar of de boekhoudperiode. U kunt de posten laten zoals ze zijn. Als u echter gegevens in Excel of met behulp van de analysemodus wilt analyseren, markeert u de posten als gecontroleerd. Ga voor meer informatie over het analyseren van posten naar [Posten analyseren](#analyze-entries). Om de posten als gecontroleerd te markeren, voegt u een filter toe aan het deelvenster Filter om alleen die posten weer te geven en kiest u vervolgens de actie **Geselecteerde posten als gecontroleerd markeren**.

## <a name="filter-entries"></a>Posten filteren

Om een duidelijker beeld te krijgen zijn er verschillende manieren om posten te filteren op de pagina **Grootboekposten controleren**.

* Gebruik de acties **Gecontroleerde posten weergeven** en **Gecontroleerde posten verbergen** om alleen de posten weer te geven die u wel of niet hebt gecontroleerd. Gebruik de actie **Alle posten weergeven** om de filters te wissen.
* Gebruik het filtervenster. U kunt bijvoorbeeld filteren op rekeningnummer of, als u oudere posten hebt en ze allemaal als gecontroleerd wilt markeren, op een boekingsdatum.

## <a name="analyze-entries"></a>Posten analyseren

Er is een aantal manieren om de grootboekposten die u hebt gecontroleerd, te analyseren.

* Schakel bijvoorbeeld de analysemodus in om posten te groeperen op basis van hun gecontroleerd-id. Ga voor meer informatie over de analysemodus naar [Lijstpaginagegevens analyseren met de analysemodus](analysis-mode.md).
* Exporteer de posten naar Excel.

## <a name="see-also"></a>Zie ook

[Het grootboek en het rekeningschema begrijpen](finance-general-ledger.md)  
[De rekeningschema's instellen of wijzigen](finance-setup-chart-accounts.md)  
