---
title: Word-sjablonen gebruiken voor bulkcommunicatie | Microsoft Docs
description: Met Word-sjablonen kunt u gemakkelijk bulksgewijs documenten maken die zijn gepersonaliseerd voor specifieke entiteiten.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'document, mail, merge, Word, template, email'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Word-sjablonen gebruiken voor bulkcommunicatie
Microsoft Word-sjablonen kunnen het gemakkelijker maken massaal te communiceren in druk of e-mail met entiteiten zoals contacten, klanten en leveranciers. U kunt bijvoorbeeld brochures maken om klanten te attenderen op een verkoopcampagne, brieven om leveranciers te informeren over een nieuw aankoopbeleid of uitnodigingen om contacten aan te trekken voor een aankomend evenement.

> [!NOTE]
> U kunt Word-sjablonen alleen gebruiken op apparaten met Microsoft Word 2019 en het Windows-besturingssysteem geïnstalleerd.

U kunt entiteiten gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)] als de gegevensbron voor de sjabloon en samenvoegvelden toevoegen om documenten voor elke entiteit te personaliseren. De samenvoegvelden zijn afkomstig van de entiteit in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u een Word-sjabloon toepast op een entiteit, worden gegevens uit de samenvoegvelden in het document ingevoegd.

Wanneer u een nieuwe sjabloon maakt, kunt u op de pagina **Word-sjablonen** een begeleide instelling gebruiken om een ZIP-bestand te downloaden dat een DataSource.xlsx en een Word-sjabloonbestand voor de entiteit bevat. Het gegevensbronbestand bevat de velden die u in de sjabloon kunt gebruiken. Bewerk het gegevensbronbestand niet. U kunt alleen de Word-sjabloon- en gegevensbronbestanden gebruiken die u downloadt van [!INCLUDE[prod_short](includes/prod_short.md)] en u moet de bestanden op dezelfde locatie opslaan.

Nadat u de sjabloon heeft ingesteld en samenvoegvelden heeft toegevoegd, gebruikt u dezelfde guide om de sjabloon te uploaden.

## De sjabloon instellen in Word
Wanneer u een sjabloon in Word instelt, kunt u op het tabblad **Mailings** samenvoegvelden toevoegen door **Samenvoegveld invoegen** te kiezen. De beschikbare samenvoegvelden zijn afkomstig uit het gegevensbronbestand dat u voor de entiteit hebt gedownload. Ze fungeren als tijdelijke aanduidingen die Word vertellen waar in het document de informatie over de entiteit moet worden geplaatst. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Samenvoegvelden toevoegen in Microsoft Word":::

## Verwante entiteiten toevoegen
Naast het toevoegen van gegevens voor de bronentiteit, dat wil zeggen de entiteit waarvoor u de sjabloon maakt, kunt u ook gegevens samenvoegen van entiteiten die eraan zijn gerelateerd. Als de bron bijvoorbeeld de entiteit Klant is, kunt u ook gegevens uit velden in de entiteit Klant/Inkoper samenvoegen, omdat beide entiteiten een veld gemeen hebben.

Gerelateerde entiteiten delen een veld, dat vaak een identificatie is, zoals een naam, code of id, met de bronentiteit. Wanneer u een sjabloon instelt, zijn er eenvoudige en geavanceerde opties voor het kiezen van gerelateerde entiteiten:

* Eenvoudig - Voeg bekende relaties toe die [!INCLUDE[prod_short](includes/prod_short.md)] standaard beschikbaar stelt.
* Geavanceerd - Voeg niet-standaard relaties toe, zoals die zijn toegevoegd door extensies of aanpassingen. Dit vereist dat u de velden kent die de entiteiten delen.

Wanneer u een gerelateerde entiteit toevoegt, moet u een voorvoegsel voor de veldnaam opgeven. Wanneer u velden aan de sjabloon toevoegt, kan het voorvoegsel het gemakkelijker maken om onderscheid te maken tussen velden van de bronentiteit en velden van gerelateerde entiteiten.

## Een Word-sjabloon maken in Business Central
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Word-sjablonen** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Nieuw**, dan **Een sjabloon maken** en volg de stappen in de begeleide instelling. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> U kunt ook rechtstreeks vanaf de pagina voor een entiteit een sjabloon maken door de actie **Word-sjabloon toepassen** te kiezen om de begeleide instelling te openen, en dan **Nieuwe sjabloon** kiezen. Wanneer u dat doet, wordt de gegevensbron voor u gekozen op basis van het type entiteit.

## Een sjabloon toepassen
Als uw Word-sjabloon klaar is, kunt u op de pagina **Word-sjablonen** **Toepassen** kiezen om de documenten te genereren. Wanneer u een Word-sjabloon toepast op een entiteit, worden gegevens uit de samenvoegvelden in het document ingevoegd. U kunt één document maken dat secties voor elke entiteit bevat, of **Splitsen** kiezen om voor elke entiteit een nieuw document te maken.

U kunt sjablonen toepassen op een of meer van hetzelfde type entiteit, zoals een contact, rechtstreeks in de context van die pagina, of vanaf de pagina Word-sjablonen om de sjabloon toe te passen op alle entiteiten van dat type.

## Word-sjablonen gebruiken met e-mail
U kunt Word-sjablonen gebruiken om inhoud aan e-mailberichten toe te voegen. Wanneer u een e-mail opstelt, kunt u de actie **Word-sjabloon gebruiken** kiezen om de inhoud van een sjabloon op het bericht toe te passen. Hiervoor moet u een of meer sjablonen voor de entiteit hebben gemaakt. U kunt één sjabloon tegelijk gebruiken en wanneer u tussen sjablonen schakelt, verandert het bericht om de inhoud van de gekozen sjabloon weer te geven.

Daarnaast kunt u de actie **Bestand toevoegen vanuit Word-sjabloon** gebruiken om de inhoud van de sjabloon als bestand aan de e-mail toe te voegen. Het bestand gebruikt het formaat dat u hebt opgegeven voor de sjabloonuitvoer.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Opties voor het gebruik van inhoud uit een Word-sjabloon in een e-mail":::

## Zie ook
[Indelingen van rapporten en documenten beheren](ui-manage-report-layouts.md)  
