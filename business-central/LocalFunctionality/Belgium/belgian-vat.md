---
title: Belgische btw
description: Met Belgische uitbreidingen van de btw-rapportagefunctie kunt u eenvoudig btw-transactiedetails afdrukken.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '11300, 11301,11303,11306,11307,11308'
ms.date: 03/02/2022
ms.author: bholtorf
---
# Belgische btw

[!INCLUDE[prod_short](../../includes/prod_short.md)] bevat Belgische uitbreidingen naar de btw-rapportagefuncties zodat u btw-transactiedetails kunt afdrukken. U moet de volgende rapporten aan de Belgische belastingdienst versturen:  

- Aangifte per maand/kwartaal - Dit rapport wordt gebruikt om maandelijkse of driemaandelijkse btw-aangiftes te maken, afhankelijk van uw bedrijfsinkomsten.  

- Jaarlijkse btw-lijst (op papier/diskette)

    Dit rapport wordt gebruikt om jaarlijks alle bedragen te rapporteren die zijn gefactureerd voor zowel goederen als diensten naar alle Belgische bedrijven met een geregistreerd btw-nummer.  

- Verkoopoverzicht EU

    Dit rapport wordt gebruikt om de verkopen van goederen aan andere landen/regio's in de Europese Unie te rapporteren. Zie [Informatie over het Verkoopoverzicht EU](../../finance-how-report-vat.md#ecsaleslist) voor meer informatie.  

U moet ook een gedrukt afschrift met details van de btw-transacties verstrekken aan de Belgische belastingdienst. Zie Btw-aangifte voor meer informatie.  

## Niet-aftrekbare btw

In België kan btw volledig of gedeeltelijk aftrekbaar zijn. Kosten zoals representatiekosten of aankopen van auto's zijn slechts deels aftrekbaar en de transactie moet opgeven hoeveel van de btw niet-aftrekbaar is. U maakt bijvoorbeeld een grootboekrekening voor vaste activa, bijvoorbeeld auto's, en een andere rekening voor representatiekosten. Voor elke rekening moet u opgeven hoeveel van de gerapporteerde btw niet-aftrekbaar is door het veld **Percentage niet-aftrekbare btw** in te stellen. Wanneer u een transactie boekt wordt de aftrekbare btw dan geboekt naar de corresponderende btw-rekening en wordt de niet-aftrekbare btw opgeteld bij het basisbedrag en geboekt naar dezelfde rekening als een materieel of immaterieel activum.  

Voor vaste activa wordt de niet-aftrekbare btw afgeschreven zoals de basisaanschafkosten van het vaste activum. U moet aparte VA-boekingsgroepen instellen voor elk percentage niet-aftrekbare btw. U moet dit doen aangezien elke VA-boekingsgroep boekt naar een grootboekrekening, waarbij het veld **Percentage niet-aftrekbare btw** opgeeft hoeveel btw moet worden geboekt naar dezelfde rekening als het vaste activum.  

Als u het veld **Inclusief niet-aftrekbare btw** inschakelt op een btw-aangifteregel, wordt niet aftrekbare btw opgenomen in het btw-bedrag. Het rapport **Btw-vereffening berekenen en boeken** telt het niet-aftrekbare deel van dat bedrag op bij de velden **Niet-aftrekbaar btw-bedrag** en **Niet-aftrekbaar btw-bedrag (bronvaluta)** in de resulterende btw-posten.  

## Zie ook

[Belgische lokale functionaliteit](belgium-local-functionality.md)  
[Periodieke btw-rapporten afdrukken](how-to-print-periodic-vat-reports.md)  
[Niet-aftrekbare btw instellen](how-to-set-up-non-deductible-vat.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]