---
title: Word-sjablonen gebruiken voor bulkcommunicatie
description: Met Word-sjablonen kunt u gemakkelijk bulksgewijs documenten maken die zijn gepersonaliseerd voor specifieke entiteiten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
---

# Word-sjablonen gebruiken voor bulkcommunicatie

Microsoft Word-sjablonen kunnen het gemakkelijker maken massaal te communiceren in druk of e-mail met entiteiten zoals contacten, klanten en leveranciers. U kunt bijvoorbeeld het volgende maken:

* Brochures om klanten te attenderen op een verkoopcampagne
* Brieven om verkopers te informeren over een nieuw inkoopbeleid
* Uitnodigingen om contacten aan te trekken voor een aankomend evenement

> [!NOTE]
> Wanneer u Word-sjablonen instelt, moet u een apparaat gebruiken met Microsoft Word 2019 of nieuwer en waarop het Windows-besturingssysteem is geïnstalleerd.

## Stel de bron van gegevens in.

Gebruik entiteiten in [!INCLUDE[prod_short](includes/prod_short.md)] als de bron van gegevens voor de sjabloon en voeg samenvoegvelden toe om documenten voor elke entiteit te personaliseren. De samenvoegvelden zijn afkomstig van de entiteit in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u een Word-sjabloon toepast op een entiteit, worden gegevens uit de samenvoegvelden in het document ingevoegd.

Op de pagina **Word-sjablonen**, wanneer u een nieuwe sjabloon maakt, helpt een begeleide instelling u door de volgende stappen:

1. Kies een of meer entiteiten om te gebruiken als de bron van de gegevens. Als u bijvoorbeeld een brochure voor een verkoopcampagne wilt maken, kiest u waarschijnlijk de entiteit Klant als bron.
2. Kies andere entiteiten als extra gegevensbronnen. Lees meer op [Vermeldingen toevoegen die al dan niet gerelateerd zijn aan de bronentiteit](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Een lege sjabloon downloaden. U kunt de sjabloon meteen in Word instellen, of u kunt de lege sjabloon uploaden en de handleiding voltooien. Wanneer uw sjabloon klaar is, gebruikt u de actie **Uploaden** op de pagina **Word-sjablonen** om de lege sjabloon te vervangen door uw voltooide sjabloon. Ga voor meer informatie naar [De sjabloon instellen in Word](#set-up-the-template-in-word).
4. Upload de sjabloon die u heeft voorbereid.
5. Voer een code en een naam in die de sjabloon identificeert.

Wanneer u een sjabloon downloadt, krijgt u een .zip-bestand dat twee bestanden bevat.

|Bestand  |Omschrijving  |
|---------|---------|
|DataSource.xlsx     | Het gegevensbronbestand bevat de velden die u in de sjabloon kunt gebruiken. Bewerk het gegevensbronbestand niet. U kunt alleen de Word-sjabloon- en gegevensbronbestanden gebruiken die u downloadt en u moet de bestanden op dezelfde locatie opslaan.     |
|Word-sjabloon     | Een .docx-bestand om als sjabloon te gebruiken.        |

Ga voor meer informatie over het instellen van een sjabloon in Word naar [De sjabloon instellen in Word](#set-up-the-template-in-word).

## Vermeldingen toevoegen die al dan niet gerelateerd zijn aan de bronentiteit

U kunt ook gegevens van andere entiteiten samenvoegen. Om andere entiteiten toe te voegen als gegevensbronnen gebruikt u een van de volgende acties op de pagina **Word-sjablonen** of wanneer u de begeleide installatiehandleiding gebruikt:

|Actie  |Omschrijving  |
|---------|---------|
|**Gerelateerde entiteit toevoegen**  | Gebruik gegevens van entiteiten die gerelateerd zijn aan de bronentiteit. Voor de entiteit Klant kunt u bijvoorbeeld ook gegevens uit de entiteit Contactpersoon samenvoegen. Entiteiten zijn gerelateerd wanneer een veld in de ene entiteit verwijst naar een andere. Een veld in de entiteit Klant verwijst naar een veld in de entiteit Contactpersoon, dus ze zijn gerelateerd. Het gedeelde veld is vaak een identifier zoals een naam, code of id.        |
|**Niet-gerelateerde entiteit toevoegen**| Gebruik gegevens van entiteiten die niet gerelateerd zijn aan de bronentiteit. U maakt bijvoorbeeld een sjabloon voor de entiteit Klant. U kunt de entiteit Bedrijfsgegevens toevoegen, zodat u uw contactgegevens kunt opnemen. Een belangrijk voordeel is dat als u uw contactgegevens wijzigt, deze automatisch worden bijgewerkt in uw sjabloon. Nadat u een niet-gerelateerde entiteit hebt toegevoegd, kunt u entiteiten toevoegen die eraan zijn gerelateerd.         |

Voor niet-gerelateerde vermeldingen kiest u een specifieke record. Omdat u een entiteit slechts één keer kunt toevoegen, moet u om een andere record te gebruiken de entiteit verwijderen en opnieuw toevoegen met de nieuwe record.

U kunt een hiërarchie van entiteiten maken, zowel gerelateerd als niet-gerelateerd. De relatie wordt weergegeven als een boomstructuur. Het veld **Entiteitrelatie** toont ook informatie over de relatie. Voor niet-gerelateerde entiteiten toont het veld de record die de relatie maakt.

Wanneer u entiteiten toevoegt, gebruikt u het veld **Veldprefix** om een prefix voor de veldnamen op te geven. Wanneer u later velden aan de sjabloon toevoegt, helpt het prefix onderscheid te maken tussen velden uit de bron en andere entiteiten.

### Selecteer de velden die u wilt opnemen

Voor elke entiteit kunt u de velden opgeven die beschikbaar moeten zijn voor de sjabloon. Kies het nummer in de kolom **Aantal geselecteerde velden** om toegang te krijgen tot een lijst met velden die beschikbaar zijn. Gebruik op de pagina **Veldselectie** het selectievakje **Opnemen** om de velden op te geven. Voor sommige entiteiten zijn velden die bedrijven doorgaans gebruiken, standaard opgenomen. U kunt de lijst bewerken, bijvoorbeeld om de standaardvelden te verwijderen. Uw wijzigingen zijn alleen van toepassing op de sjabloon waaraan u werkt.

> [!NOTE]
> Het totale aantal velden dat u kunt toevoegen uit alle entiteiten is 250.

> [!NOTE]
> U of uw Microsoft-partner kunnen aangepaste velden aan entiteiten toevoegen. Als u dat doet, voegen we het prefix **CALC** aan de naam van de velden toe en geven ze het veldtype **Berekend**. Het veldtype wordt berekend genoemd om aan te geven dat het veld verschillende soorten waarden kan weergeven, zoals tekst, getallen, datums, enzovoort.

## Een Word-sjabloon maken in Business Central

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Word-sjablonen** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Nieuw**, dan **Een sjabloon maken** en volg de stappen in de begeleide instelling. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> U kunt ook rechtstreeks vanaf de pagina voor een entiteit een sjabloon maken door de actie **Word-sjabloon toepassen** te kiezen om de begeleide instelling te openen, en dan **Nieuwe sjabloon** kiezen. Wanneer u dat doet, wordt de gegevensbron voor u gekozen op basis van het type entiteit.

## De sjabloon instellen in Word

Wanneer u een sjabloon in Word instelt, kunt u op het tabblad **Mailings** samenvoegvelden toevoegen door **Samenvoegveld invoegen** te kiezen. De samenvoegvelden zijn afkomstig uit het gegevensbronbestand dat u voor de entiteit hebt gedownload. Ze fungeren als tijdelijke aanduidingen die Word vertellen waar in het document de informatie over de entiteit moet worden geplaatst.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Samenvoegvelden toevoegen in Microsoft Word":::

## Een sjabloon toepassen

Als uw Word-sjabloon klaar is, kunt u op de pagina **Word-sjablonen** **Toepassen** kiezen om de documenten te genereren. Wanneer u een Word-sjabloon toepast op een entiteit, worden gegevens uit de samenvoegvelden in het document ingevoegd. U kunt één document maken dat secties voor elke entiteit bevat, of **Splitsen** kiezen om voor elke entiteit een nieuw document te maken.

U kunt de actie **Word-sjablonen toepassen** gebruiken om sjablonen toe te passen op een of meer van hetzelfde type entiteit, zoals een klant, rechtstreeks in de context van de pagina voor de entiteit. Bijvoorbeeld de pagina's **Klant** of **Leverancier**.

## Word-sjablonen gebruiken met e-mail

U kunt Word-sjablonen gebruiken om inhoud aan e-mailberichten toe te voegen. Wanneer u een e-mail opstelt, kunt u de actie **Word-sjabloon gebruiken** kiezen om de inhoud van een sjabloon op het bericht toe te passen. U moet sjablonen voor de entiteit hebben gemaakt. U kunt één sjabloon tegelijk gebruiken en wanneer u tussen sjablonen schakelt, verandert het bericht om de inhoud van de gekozen sjabloon weer te geven.

Daarnaast kunt u de actie **Bestand toevoegen vanuit Word-sjabloon** gebruiken om de inhoud van de sjabloon als bestand aan de e-mail toe te voegen. Het bestand gebruikt het formaat dat u hebt opgegeven voor de sjabloonuitvoer.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Opties voor het gebruik van inhoud uit een Word-sjabloon in een e-mail":::

## Een Word-sjabloon bewerken

U kunt de volgende wijzigingen aanbrengen in uw Word-sjablonen:

* Als u de hoofdtekst of de samenvoegvelden die in de sjabloon zijn opgenomen, wilt bewerken, gebruikt u de actie **Downloaden**, brengt u uw wijzigingen aan en gebruikt u vervolgens de actie **Uploaden**
* Gebruik de actie **Gerelateerde entiteiten** bewerken om de gegevensbronnen te wijzigen
* Gebruik de actie **Uploaden** om de Word-sjabloon te vervangen door een nieuwe sjabloon
* De sjabloon verwijderen

## Zie ook

[Rapport- en documentlay-outs beheren](ui-manage-report-layouts.md)  
[E-mail instellen](admin-how-setup-email.md)  
