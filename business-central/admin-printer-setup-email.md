---
title: E-mailprinters instellen
description: Beschrijving van gebruik
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# E-mailprinters instellen

In dit artikel wordt uitgelegd hoe u printers met e-mail kunt instellen in [!INCLUDE[prod_short](includes/prod_short.md)]. Met deze printers stuurt [!INCLUDE[prod_short](includes/prod_short.md)] afdruktaken naar de printer met behulp van het e-mailadres van de printer.

> [!TIP]
> Ga voor meer informatie over andere printermogelijkheden naar [Overzicht printerbeheer](admin-printer-setup-overview.md). 

## Vereisten

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 releasewave 1 of hoger
- Extensie **Verzenden naar e-mailprinter** is geïnstalleerd

    Deze extensie is standaard geïnstalleerd. Leer meer over het installeren van extensies op [Extensies installeren en verwijderen in Business Central](ui-extensions-install-uninstall.md).
- E-mailfunctionaliteit is ingesteld.

   Meer informatie op [E-mail instellen](admin-how-setup-email.md).

## Een e-mailprinter toevoegen

Op de pagina **Printerbeheer** ziet u de printers die momenteel zijn ingesteld. De pagina geeft u ook toegang tot de pagina **Instellingen** voor elke printer om een bestaande instelling te bewerken of een nieuwe printer in te stellen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **E-mail afdrukken** en kies vervolgens **Een e-mailprinter toevoegen**.
3. Vul de vereiste velden in op de pagina **Instellingen van e-mailprinter**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > U moet handmatig het juiste papierformaat voor een printer selecteren, omdat er geen lokale printer of gebruikersinstellingen kunnen worden opgeslagen.
    >
    > Houd er rekening mee dat de extensie E-mailprinter standaard is ingesteld op **A4**-papierformaat, dat bijvoorbeeld niet geschikt is in Noord-Amerika.

## Privacyverklaring

Als u de extensie E-mailprinter gebruikt, worden alle of sommige afdruktaken verzonden naar het e-mailadres dat is geconfigureerd voor de printer. We raden ten zeerste aan om een unieke e-mail-id te koppelen aan een printerapparaat met alleen de officiële services van de hardwarefabrikant, zoals HP ePrint, KonicaMinolta EveryonePrint of Epson Email Print.

Neem alle benodigde privacyvoorzorgsmaatregelen, inclusief ervoor zorgen dat de oplossing voor het afdrukken van e-mail goed geconfigureerde machtigingen, privacyinstellingen en bewaarbeleid heeft. Het is uw verantwoordelijkheid om een correct, geverifieerd en operationeel e-mailadres op te geven. Meer informatie op [Microsoft-privacyverklaring ](https://privacy.microsoft.com/privacystatement).

## Volgende stappen

[Standaardprinters instellen](ui-specify-printer-selection-reports.md)

## Zie ook

[Overzicht van printerbeheer](admin-printer-setup-overview.md)  
[Universeel afdrukken instellen](admin-printer-setup-universal-print.md)
[Een rapport afdrukken](ui-work-report.md#PrintReport)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Batchverwerkingen uitvoeren](ui-how-run-batch-jobs.md)  
