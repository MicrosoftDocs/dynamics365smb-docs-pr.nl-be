---
title: Extensie Basiservaring | Microsoft Docs
description: Deze extensie is een gemoderniseerd alternatief voor Microsoft Dynamics C5.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: b423ce61a5bc8a7f5c580d0b4f3348792c4b02ab
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132485"
---
# <a name="the-basic-experience-extension"></a>De extensie Basiservaring
Als u Microsoft Dynamics C5 gewend bent, kunnen Microsoft-partners u helpen bij de overgang naar een modernere oplossing die is gebaseerd op [!INCLUDE[prod_short](includes/prod_short.md)], zodat u kunt blijven genieten van dezelfde gestroomlijnde mogelijkheden als Dynamics C5.

Deze extensie is bedoeld voor kleine bedrijven en kan maximaal drie gebruikers ondersteunen. Als u meer gebruikers nodig hebt, moet u upgraden naar een [!INCLUDE[prod_short](includes/prod_short.md)]-licentie en deze extensie verwijderen.

> [!NOTE]
> Vanaf nu is deze extensie alleen beschikbaar voor klanten in Denemarken en IJsland. 

## <a name="whats-available"></a>Wat is er beschikbaar?
De volgende tabel beschrijft de mogelijkheden die beschikbaar zijn als u de extensie Basiservaring installeert.

|District  |Functionaliteit  |
|---------|---------|
|**Grootboek** |Basisfinanciën, Rekeningschema's, Vaste activa, Bankbeheer, Bankreconciliatie, Betalingen, Automatische incasso, Dimensies, Meerdere valuta's, Budgetten, Werkstroom, Documentbeheer/OCR, Consolidatie, Onbeperkte bedrijven|
|**Tegoeden/Verkoop** |Basistegoeden, Verkoopfacturering, Verkoopkortingen, Prijzen, Btw, Contactbeheer |
|**Schulden/Inkoop** |Basisschulden, Inkoopfacturering |
|**Projectbeheer** |Projecten, Projectprijzen, Urenstaten, Toewijzing, Taken, Bronnen |
|**Voorraad** |Basisvoorraad, Artikelvervangingen, Artikelkruisverwijzing |

## <a name="getting-started"></a>Aan de slag
Deze extensie is een beetje anders dan de meeste en u hebt hulp van een Microsoft-partner nodig om deze te installeren en in te stellen. Om u te laten weten wat u kunt verwachten vindt u hier een algemeen overzicht van wat de Microsoft-partner gaat doen.

1. Een nieuwe [!INCLUDE[prod_short](includes/prod_short.md)]-tenant maken. Dit kan een proefversie of een CSP-versie zijn.
2. Voeg ten minste één gebruiker toe die is toegewezen aan een Basiservaring-licentie in uw Azure Active Directory-account.
3. Verwijder alle bedrijven, inclusief het voorbeeldbedrijf Cronus.
4. Maak een nieuw bedrijf dat geen voorbeeldgegevens of instellingen bevat.
5. Voeg het pakket **Demo RapidStart** toe. <!--what does the pockage contain?-->
6. Download en installeer de extensie Basiservaring vanuit AppSource.

## <a name="migrating-data"></a>Gegevens migreren
Breng uw Dynamics C5-gegevens mee. Nadat uw Microsoft-partner de extensie Basiservaring heeft geïnstalleerd, hebt u een leeg bedrijf. Een eenvoudige manier om uw gegevens van Dynamics C5 naar de Basiservaring te verplaatsen, is door de extensie C5-gegevensmigratie te gebruiken, die is opgenomen in [!INCLUDE[prod_short](includes/prod_short.md)]. De extensie migreert klanten, leveranciers, artikelen en uw grootboekrekeningen en hun boekingen.

## <a name="see-also"></a>Zie ook
[De extensie C5-gegevensmigratie](ui-extensions-c5-data-migration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]