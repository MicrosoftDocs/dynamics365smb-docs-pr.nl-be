---
title: Rapporten instellen op afdrukken op specifieke printers | Microsoft Docs
description: Leren over het opgeven van een printer voor een lijst en het gebruik van de pagina Printerselecties.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d027999692323960327e8b34ddb2efaea23c59a8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189495"
---
# <a name="set-up-printers"></a>Printers instellen
Omdat [!INCLUDE[prodshort](includes/prodshort.md)] een cloudservice is, kan het geen lokale printers bereiken die zijn aangesloten op de machines van gebruikers. Het kan echter verbinding maken met printers met cloudfunctionaliteit. In de generieke versie van [!INCLUDE[prodshort](includes/prodshort.md)], wordt een cloudprinter genaamd **E-mailprinter** geïnstalleerd als een extensie en is deze klaar voor gebruik na de eerste installatie.

Als geen cloudprinter is geïnstalleerd en ingesteld of als een geïnstalleerde printer niet werkt, wordt het afdrukken standaard ingesteld op de afdrukopties voor de browser. Dit wordt aangegeven door deze waarde in het veld **Printer** op de rapportaanvraagpagina: *(geen, afgehandeld door de browser)*.

Op de pagina **Printerbeheer** ziet u de printers die zijn ingesteld. Wanneer u een of meer printers hebt ingesteld, kunt u de pagina **Printerselecties** openen om voor uw gebruikersaccount in te stellen welke specifieke rapporten met welke printer moeten worden afgedrukt.

Wanneer een printer is ingesteld en toegewezen aan specifieke rapporten, drukt u een rapport af door de knop **Afdrukken** te kiezen op de rapportaanvraagpagina. Zie voor meer informatie [Een rapport afdrukken](ui-work-report.md#PrintReport).

## <a name="to-set-up-a-printer"></a>Een printer instellen
Op de pagina **Printerbeheer** ziet u de printers die zijn ingesteld en hebt u toegang tot de pagina **Instellingen** voor elke printer om een bestaande instelling te bewerken of een nieuwe printer in te stellen.

De volgende procedure beschrijft hoe u de bestaande **e-mailprinter** instelt, wat een vooraf geïnstalleerde extensie is.

> [!NOTE]
> Om e-mailafdrukken te kunnen gebruiken, moet e-mailfunctionaliteit zijn ingesteld. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer de desbetreffende koppeling.
2. Selecteer de regel voor de **e-mailprinter** en kies vervolgens de actie **Printerinstellingen bewerken**.
3. Vul de vereiste velden op de pagina **Instellingen** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > U moet handmatig het juiste papierformaat voor een printer selecteren, omdat er geen lokale printer of gebruikersinstellingen kunnen worden opgeslagen.
    >
    > Houd er rekening mee dat de extensie E-mailprinter standaard is ingesteld op **A4**-papierformaat, dat bijvoorbeeld niet geschikt is in Noord-Amerika.
4. Om een printer uw standaard te maken, kiest u op de pagina **Printerbeheer** de optie **Instellen als mijn standaardprinter**.

### <a name="privacy-notice"></a>Privacyverklaring
Als u de extensie E-mailprinter gebruikt, worden alle of sommige afdruktaken verzonden naar het e-mailadres dat u hebt opgegeven bij het configureren van de printer. We raden ten zeerste aan om een unieke e-mail-ID te koppelen aan een printerapparaat met alleen de officiële services van de hardwarefabrikant, zoals HP ePrint, KonicaMinolta EveryonePrint of Epson Email Print.

U moet alle benodigde privacyvoorzorgsmaatregelen nemen, inclusief ervoor zorgen dat de oplossing voor het afdrukken van e-mail goed geconfigureerde machtigingen, privacyinstellingen en bewaarbeleid heeft. Het is uw verantwoordelijkheid om een correct, geverifieerd en operationeel e-mailadres op te geven. Zie voor meer informatie [Privacyverklaring van Microsoft](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Selecteren welke printers welke rapporten afdrukken
Op de pagina **Printerselecties** kunt u voor uw gebruikersaccount instellen welke rapporten door welke printer worden afgedrukt. Dit is handig als u met verschillende rapporten werkt waarvoor verschillende printers nodig zijn vanwege hun plaatsing in het bedrijf of hun uitvoermogelijkheden.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerselecties** in en selecteer de desbetreffende koppeling. Als alternatief selecteert u vanaf de pagina **Printerbeheer** een printer en kiest u vervolgens de actie **Printerselecties**.
2. Kies de actie **Nieuw** om een printerselectie toe te voegen voor een specifiek rapport.
3. Vul de vereiste velden in.

Het opgegeven rapport is nu ingesteld om standaard te worden afgedrukt op de geselecteerde printer.

> [!NOTE]
> Wanneer u het betreffende rapport afdrukt, kunt u deze instelling negeren door een andere printer te selecteren op de aanvraagpagina **Afdrukinstellingen**.

> [!NOTE]
> Als u geen rapport instelt voor een specifieke printer op de pagina **Printerselecties**, wordt het afgedrukt op de standaardprinter van het bedrijf, zoals gedefinieerd vanuit de pagina **Printerbeheer**.

U of de beheerder kan ook de pagina **Printerselecties** gebruiken om andere afdrukvarianten voor gebruikers en rapporten te definiëren. De volgende tabel beschrijft de combinatie van waarden wanneer u andere printerinstellingen instelt voor een rapport.

|Als u dit wilt doen:                                                 |Stel de volgende waarden in                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Een rapport afdrukken naar een specifieke printer voor alle gebruikers |Geef waarden op in de velden **Rapport-id** en **Printernaam** en laat het veld **Gebruikers-ID** leeg.|
|Alle rapporten naar een specifieke printer afdrukken voor een specifieke gebruiker|Geef waarden op in de velden **Gebruikers-ID** en **Printernaam** en laat het veld **Rapport-id** leeg.|
|De standaardprinter voor alle rapporten instellen|Geef een waarde op in het veld **Printernaam** en laat de velden **Gebruikers-ID** en **Rapport-id** leeg.|
|Een specifiek rapport afdrukken naar de standaardprinter van de gebruiker|Geef een waarde op in het veld **Rapport-id** en laat de velden **Printernaam** en **Gebruikers-ID** leeg.|
|Een specifiek rapport naar een specifieke printer afdrukken voor een specifieke gebruiker|Geef waarden in alle drie de velden op.|

> [!NOTE]
> Specifiekere printerselecties hebben voorrang op algemenere printerselecties. Bijvoorbeeld een printerselectie met waarden in de velden **Gebruikers-ID**, **Rapport-id** en **Printernaam** heeft voorrang op een printerselectie met lege vermeldingen in de velden **Gebruikers-ID** of **Rapport-id**.

## <a name="see-also"></a>Zie ook
[Een rapport afdrukken](ui-work-report.md#PrintReport)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Batchverwerkingen uitvoeren](ui-how-run-batch-jobs.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
