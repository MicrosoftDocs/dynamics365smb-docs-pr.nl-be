---
title: Word-sjablonen gebruiken voor bulkcommunicatie | Microsoft Docs
description: Met Word-sjablonen kunt u gemakkelijk bulksgewijs documenten maken die zijn gepersonaliseerd voor specifieke entiteiten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 118d8db1266bb7150965ec4d1ce44ece77638764
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788644"
---
# <a name="using-word-templates-for-bulk-communication"></a>Word-sjablonen gebruiken voor bulkcommunicatie
Microsoft Word-sjablonen kunnen het gemakkelijker maken om massaal te communiceren met entiteiten zoals klanten en leveranciers. U kunt bijvoorbeeld brochures maken om klanten te attenderen op een verkoopcampagne, brieven om leveranciers te informeren over een nieuw aankoopbeleid of uitnodigingen om contacten aan te trekken voor een aankomend evenement.

U kunt entiteiten gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)] als de gegevensbron voor de sjabloon en samenvoegvelden toevoegen om documenten voor elke entiteit te personaliseren. De samenvoegvelden zijn afkomstig van de entiteit in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u een Word-sjabloon toepast op een entiteit, worden gegevens uit de samenvoegvelden in het document ingevoegd.

Op de pagina **Word-sjablonen** kunt u een begeleide instelling gebruiken om een ZIP-bestand te downloaden dat een DataSource.txt en een Word-sjabloonbestand voor een entiteit bevat. Nadat u de sjabloon heeft ingesteld en samenvoegvelden heeft toegevoegd, gebruikt u dezelfde guide om de sjabloon te uploaden. U kunt alleen de Word-sjabloon- en gegevensbronbestanden gebruiken die u downloadt van [!INCLUDE[prod_short](includes/prod_short.md)] en u moet de bestanden op dezelfde locatie opslaan.

> [!NOTE]
> Wanneer u een entiteit kiest waarvoor u een sjabloon wilt maken, toont de lijst alle entiteiten in [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt echter niet voor alle entiteiten sjablonen maken. Als de naam van een entiteit speciale tekens bevat, zoals **/**, **.**, **_** of **-**, kunt u er geen sjabloon voor maken. De naam van de entiteit wordt weergegeven in de kolom **Objectbijschrift**.

Wanneer u de sjabloon in Word instelt, kunt u op het tabblad **Mailings** samenvoegvelden toevoegen door **Samenvoegveld invoegen** te kiezen.

> [!NOTE]
> U kunt geen samenvoegvelden gebruiken als de naam van het veld 40 tekens of meer bevat. U kunt bijvoorbeeld het veld Company__Information_Customs_Permit_Date niet gebruiken omdat het 40 tekens heeft. 

Als uw Word-sjabloon klaar is, kunt u op de pagina **Word-sjablonen** **Toepassen** kiezen om de documenten te genereren. U kunt één document maken dat secties voor elke entiteit bevat, of de bewerking splitsen om voor elke entiteit een nieuw document te maken.

## <a name="to-create-a-word-template"></a>Een Word-sjabloon maken
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Word-sjablonen** in en kies de desbetreffende koppeling.
2. Volg de stappen in het begeleide instelling. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Zie ook
[Indelingen van rapporten en documenten beheren](ui-manage-report-layouts.md)  
