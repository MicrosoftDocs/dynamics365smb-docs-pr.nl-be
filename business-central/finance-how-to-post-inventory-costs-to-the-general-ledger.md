---
title: 'Procedure: Voorraadkosten naar het grootboek boeken| Microsoft Docs'
description: Beschrijft hoe u de fysieke producten beheert waarin u handelt, bijvoorbeeld de voorraad in uw magazijn.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: eed219bb8bc6401c0f2bbc5cab7600fe1bfc3d53
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306088"
---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a>Voorraadkosten reconciliëren met het grootboek
Als u voorraadtransacties (bijvoorbeeld verkoopverzendingen, inkoopfacturen of voorraadherwaarderingen) boekt, worden de gewijzigde artikelkosten vastgelegd in artikelwaardeposten. Om deze wijziging van voorraadwaarde door te voeren in uw financiële boeken, worden de voorraadkosten automatisch geboekt naar de gerelateerde voorraadrekeningen in het grootboek. Voor iedere voorraadtransactie die u boekt, worden overeenkomende waarden geboekt naar de voorraadrekening, de correctierekening en de KPV-rekening in het grootboek.

Automatisch voorraadwaarde boeken wordt gedefinieerd door het veld **Autom. voorraadwaarde boeken** op de pagina **Voorraadinstelling**.

Hoewel voorraadkosten automatisch naar het grootboek worden geboekt, moeten de kosten van goederen toch worden doorgestuurd naar de gerelateerde uitgaande verkooptransactie, vooral in situaties waarin u goederen verkoopt voordat u de inkoop van die goederen factureert. Dit wordt kostenwaardering genoemd. Artikelkosten worden automatisch aangepast als u artikeltransacties boekt, maar u kunt artikelkosten ook handmatig wijzigen. Zie [Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md) voor meer informatie.

## <a name="to-post-inventory-costs-manually"></a>Voorraadkosten handmatig boeken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadwaarde boeken** in en kies vervolgens de gerelateerde koppeling.
2. Voorraadkosten handmatig naar het grootboek boeken door de batchverwerking. Als u deze batchverwerking uitvoert, worden grootboekposten op basis van de waardeposten gemaakt. U kunt de posten boeken, zodat deze per boekingsgroep worden samengevat.

> [!NOTE]  
> Wanneer u deze batchverwerking uitvoert, is het mogelijk dat er fouten worden aangetroffen met betrekking tot ontbrekende instellingen of incompatibele dimensie-instellingen. Als de batchverwerking fouten aantreft in de dimensie-instellingen, worden deze fouten overschreven en worden de dimensies van de waardepost gebruikt. De batchverwerking slaat de waardeposten van alle andere fouten over en vermeldt deze aan het einde van de lijst in een aparte sectie genaamd “Overgeslagen posten”. U dient de fouten te corrigeren om deze posten te kunnen boeken.

Als u een lijst met de fouten wilt weergeven voordat u de boekingsbatchverwerking uitvoert, kunt u het rapport **Voorraadkosten naar GB boeken - Controle** uitvoeren. In de controlelijst worden alle fouten vermeld die tijdens een controleboeking zijn gevonden. U kunt deze fouten dan corrigeren en de batchverwerking voor het boeken van voorraadkosten uitvoeren zonder posten over te slaan.

Als u een overzicht wilt zien van de waarden die naar het grootboek kunnen worden geboekt zonder de boeking daadwerkelijk uit te voeren, voert u de batchverwerking **Voorraadwaarde boeken** uit. U doet dit door het selectievakje **Boeken** in het aanvraagvenster uit te schakelen. Wanneer u de batchverwerking dan uitvoert, wordt alleen een lijst gemaakt met de waarden die klaar zijn om naar het grootboek te worden geboekt. Deze worden echter niet geboekt.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>De reconciliatie controleren tussen het voorraadgrootboek en het grootboek
De pagina **Reconciliatie Voorraadbeheer - GB** biedt de volgende opties:

- De reconciliatieverschillen weer te geven door te vergelijken wat er in het grootboek is vastgelegd en wat er is vastgelegd in het voorraadjournaal (waardeposten).
- De niet-gereconcilieerde totale kosten in de waardeposten in het voorraadjournaal weer te geven alsof die zijn toegewezen aan overeenkomende voorraadrekeningen in het grootboek, en die te vergelijken met de totalen die daadwerkelijk zijn aangemaakt op de rekeningen in het grootboek.
- De dubbele postenstructuur van het grootboek weer te geven door gegevens als zodanig visueel weer te geven. Bijvoorbeeld een post van de kostprijs van de verkochte goederen met een overeenkomende voorraadpost.
- Gebruikers details te laten opvragen en de posten te bekijken waaruit de kosten zijn opgebouwd.
- Filters op te nemen die de analyse per gegevens, artikel en locatie verfijnen.
- Redenen voor reconciliatieverschillen in informatieve berichten uit te leggen.


In de uiterst linkse kolom **Naam** van het raster staan de diverse grootboekrekeningsoorten die aan voorraad zijn gekoppeld.

In de kolommen **Voorraad**, **Voorraad (interim)** en **OHW-voorraad** staan de gefactureerde, niet gefactureerde en OHW-totalen van elke grootboekrekeningsoort. Deze worden berekend van waardenposten, dat wil zeggen dat zij worden gepland in de grootboekrekeningsoorten waar zij eindigen wanneer zij uiteindelijk in het grootboek worden geboekt.

In de kolom **Totaal** staat de som (vet weergegeven) van de bedragen van de waardenposten in de drie voorraadkolommen.

In de kolom **GB-totaal** staan de bedragen (vet weergegeven) van elke grootboekrekeningsoort die in het grootboek voorkomt. Deze worden berekend van grootboekposten, dat wil zeggen dat zij de voorraadkosten zijn die al in het grootboek zijn geboekt.

De kolom **Verschil** vertegenwoordigt het verschil tussen de waarde in de velden **GB-totaal** en **Totaal**.

Boven aan de pagina **Reconciliatie Voorraadbeheer - GB** kunt u filters instellen om bijvoorbeeld de tijdsperiode te beperken waarvan u gegevens wilt opvragen.

Als u het selectievakje **Waarschuwing weergeven** inschakelt en er discrepanties worden aangetroffen tussen de voorraadtotalen en de grootboektotalen, worden er berichten in het veld **Waarschuwing** van het raster weergegeven die de discrepantie uitleggen. Als u het veld Waarschuwing kiest, krijgt u meer informatie over de betekenis van de waarschuwing.

Wanneer u alle relevante filters hebt ingevoerd, kiest u de actie **Matrix weergeven**. De gegevens worden berekend en de matrixpagina wordt weergegeven.

In de uiterst linkse kolom van het raster kunt u de diverse grootboekrekeningsoorten bekijken die aan voorraad zijn gekoppeld. In de kolommen daarna worden voor elke rekeningsoort ook de gefactureerde totalen, de niet-gefactureerde (interim) totalen en de OHW-voorraden weergegeven. Deze totalen worden op basis van de waardeposten berekend.

In de volgende kolommen worden de totalen voor dezelfde rekeningsoorten weergegeven, maar deze totalen zijn op basis van de grootboekposten berekend.

Kies het bedrag in een willekeurig totaalveld om de voorraadrapportposten te bekijken die voor het berekenen van de totalen zijn gebruikt. Voor de voorraadtotalen omvatten de voorraadrapportposten de som van de waardeposten voor de artikelen. Voor de grootboektotalen omvatten de voorraadrapportposten de som van de grootboekposten.

## <a name="see-also"></a>Zie ook  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)
