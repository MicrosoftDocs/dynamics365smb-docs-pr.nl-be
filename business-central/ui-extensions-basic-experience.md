---
title: Extensie Basiservaring | Microsoft Docs
description: Deze extensie is een gemoderniseerd alternatief voor Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 09/28/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# De extensie Basiservaring

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Als u Microsoft Dynamics C5 gewend bent, kunnen Microsoft-partners u helpen bij de overgang naar een modernere oplossing die is gebaseerd op [!INCLUDE[prod_short](includes/prod_short.md)], zodat u kunt blijven genieten van dezelfde gestroomlijnde mogelijkheden als Dynamics C5.

Deze extensie is bedoeld voor kleine bedrijven en kan maximaal drie gebruikers ondersteunen. Als u meer gebruikers nodig hebt, moet u upgraden naar een [!INCLUDE[prod_short](includes/prod_short.md)]-licentie en deze extensie verwijderen.

> [!NOTE]
> Vanaf nu is deze extensie alleen beschikbaar voor klanten in Denemarken en IJsland.

## Wat is er beschikbaar?

De volgende tabel beschrijft de mogelijkheden die beschikbaar zijn als u de extensie Basiservaring installeert.

|Vlak  |Functionaliteit  |
|---------|---------|
|**Grootboek** |Basisfinanciën, financiële rapporten, vaste activa, bankbeheer, bankreconciliatie, betalingen, incasso, dimensies, meerdere valuta's, budgetten, werkstroom, documentbeheer/OCR, consolidatie, onbeperkte bedrijven|
|**Vorderingen/verkopen** |Basistegoeden, verkoopfacturering, verkoopkortingen, prijzen, btw, contactbeheer |
|**Schulden/Inkoop** |Basisschulden, inkoopfacturering |
|**Projectbeheer** |Projecten, projectprijzen, urenstaten, toewijzingen, taken, bronnen |
|**Voorraad** |Basisvoorraad, artikelvervangingen, artikelkruisverwijzing |

## Aan de slag

Deze extensie is een beetje anders dan de meeste en u hebt hulp van een Microsoft-partner nodig om deze te installeren en in te stellen. Om u te laten weten wat u kunt verwachten vindt u hier een algemeen overzicht van wat de Microsoft-partner gaat doen.

1. Een nieuwe [!INCLUDE[prod_short](includes/prod_short.md)]-tenant maken. Dat kan een proefversie zijn of een CSP-versie (Cloud Solution Provider).
2. Voeg ten minste één gebruiker toe die is toegewezen aan een Basiservaring-licentie in uw Microsoft Entra-account.
3. Verwijder alle bedrijven, inclusief het voorbeeldbedrijf Cronus.
4. Maak een nieuw bedrijf dat geen voorbeeldgegevens of instellingen bevat.
5. Voeg het pakket **Demo RapidStart** toe. <!--what does the package contain?-->
6. Download en installeer de extensie Basiservaring vanuit AppSource.

## Gegevens migreren

Breng uw Dynamics C5-gegevens mee. Nadat uw Microsoft-partner de extensie Basiservaring heeft geïnstalleerd, hebt u een leeg bedrijf. Een eenvoudige manier om uw gegevens van Dynamics C5 naar de Basiservaring te verplaatsen, is door de extensie C5-gegevensmigratie te gebruiken, die is opgenomen in [!INCLUDE[prod_short](includes/prod_short.md)]. De extensie migreert klanten, leveranciers, artikelen en uw grootboekrekeningen en hun boekingen.

## Zie ook

[De extensie C5-gegevensmigratie](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
