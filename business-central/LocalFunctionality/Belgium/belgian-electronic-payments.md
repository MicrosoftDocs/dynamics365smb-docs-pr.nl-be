---
title: Belgische elektronische betalingen
description: 'In de module voor elektronisch bankieren in de Belgische versie van Business Central kunt u elektronische betalingen naar binnen- en buitenland, en SEPA en niet-Euro SEPA verzenden.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: 2000006
ms.date: 11/27/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Belgische elektronische betalingen

In de Belgische versie van [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u de volgende soorten elektronische betalingen gebruiken:  

|Elektronische betaling|Beschrijving|  
|------------------------|---------------------------------------|  
|Binnenland|Een lokale financiële instelling verwerkt deze betalingen in de lokale valuta (LV) voor begunstigden die rekeningen hebben bij een lokale financiële instelling. [!INCLUDE[prod_short](../../includes/prod_short.md)] controleert de geldigheid van de bankrekeningnummers.|  
|Internationaal|Een lokale financiële instelling verwerkt deze betalingen die in een vreemde valuta of de lokale valuta (LV) zijn voor begunstigden die rekeningen hebben bij een buitenlandse financiële instelling. [!INCLUDE[prod_short](../../includes/prod_short.md)] controleert de geldigheid van de bankrekeningnummers.|  
|SEPA|Deze betalingen worden uitgevoerd in euro's en verwerkt in landen/regio's waar SEPA-betalingen zijn toegestaan. [!INCLUDE[prod_short](../../includes/prod_short.md)] controleert de geldigheid van de bankrekeningnummers.|  
|SEPA-betalingen in andere valuta's|Deze betalingen worden uitgevoerd in andere valuta's dan de euro en naar een land of regio buiten de EEA (European Economic Association). [!INCLUDE[prod_short](../../includes/prod_short.md)] controleert de geldigheid van de bankrekeningnummers.|  

Omdat de standaard voor elektronische betalingen per land/regio verschilt, kunnen alleen financiële instellingen in België elektronische betalingen verwerken die zijn gemaakt in de Belgische versie van [!INCLUDE[prod_short](../../includes/prod_short.md)]. De lokale financiële instellingen verwerken de betaling met de buitenlandse instellingen voor internationale betalingen.  

> [!NOTE]  
> Creditnota's kunnen niet afzonderlijk worden verwerkt omdat betalingen geen negatief saldo mogen hebben. Als u een creditnota wilt verwerken, moet u deze aan een of meer facturen toevoegen door betalingen te totaliseren.  

Voordat u een elektronische betaling kunt uitvoeren, moet u het gebruik van elektronisch bankieren instellen. Zie voor meer informatie [Instellingen](belgian-electronic-banking.md#setup). U moet ook de betreffende exportprotocollen opgeven. ZIe voor meer informatie [Exportprotocollen instellen](how-to-set-up-export-protocols.md).  

## SEPA-betalingen activeren in de Belgische versie

[!INCLUDE [activate-sepa-payments](../includes/BENL/activate-sepa-payments.md)]

Nu kunt u SEPA-betalingen verrichten. Zie [Betalingen naar een bankbestand exporteren](../../finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file) voor meer informatie. Als u de AC Banking 365-mogelijkheid niet gebruikt, kunt u betalingsdagboekregels exporteren naar een bestand. Zie voor meer informatie [Betalingsbestanden exporteren](how-to-print-payment-files.md).  

## Niet-euro SEPA-betalingen indienen

In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank. Dit is handig als u betalingen verzendt naar andere landen/regio's die SEPA niet gebruiken en voor andere valuta's dan de euro.  

Voordat u een dergelijke SEPA-betalingen kunt indienen, moet u de volgende beheertaken uitvoeren:  

- Stel een nieuw exportprotocol voor een niet-euro-SEPA in.  
- Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** uit voor elk land in de EEA-zone.  
- Controleer op de pagina **Grootboekinstellingen** of het veld **Valuta euro** leeg is en het veld **SEPA niet-euro-export** is geselecteerd.  
- Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN- en SWIFT-code bevat.  

## Een SEPA-betaling in andere valuta's dan de euro indienen  

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **SEPA-betalingen in andere valuta's dan de euro indienen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Dagboeksjabloon**|Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.|  
    |**Dagboekbatch**|Geef de dagboekbatch voor het SEPA-betalingsrapport op.|  
    |**Dagboekregels boeken**|Geef op of u de betalingsregels naar het grootboek wilt overbrengen.|  
    |**Dimensies opnemen**|Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen. De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** is geselecteerd.|  
    |**Uitvoeringsdatum**|Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.|  
    |**Bestandsnaam**|Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.|  

## Betalingsregels corrigeren

U moet alle fouten corrigeren voordat u de regels met elektronische betalingen kunt boeken. U kunt betalingsregels op de volgende manieren corrigeren.  

|Storno|Description|  
|----------------|---------------------------------------|  
|Een betalingsdagboekregel toevoegen|Als het betalingsdagboek al veel regels bevat en u nog een regel wilt toevoegen, kunt u de dagboekregel handmatig invoeren. U kunt dit bijvoorbeeld doen als u een creditnota wilt terugbetalen aan een klant. Dergelijke klantbetalingen worden niet automatisch voorgesteld door de batchverwerking **Leveranciersbetalingen voorstellen**.|  
|Een betalingsdagboekregel bewerken|Als u geen bankrekening aan het betalingsdagboek toewijst of als u geen bankrekening van voorkeur op de leverancierskaart opgeeft, moet u deze gegevens handmatig op elke dagboekregel invoeren voordat u het dagboek boekt. Als u een bankrekening voor een leverancier opgeeft, wordt de bankrekening gekopieerd naar alle betalingsdagboekregels voor die leverancier. Zie voor meer informatie [Instellingen](belgian-electronic-banking.md#setup).|  
|Een betalingsdagboekregel verwijderen|Met de batchverwerking **Leveranciersbetalingen voorstellen** maakt u betalingsvoorstellen voor alle leveranciers die overeenkomen met de opgegeven criteria. Als u de betaling voor een bepaalde leverancierspost of leverancier wilt voorkomen, kunt u de betreffende dagboekregels verwijderen.|  


## Zie ook

[Belgische lokale functionaliteit](belgium-local-functionality.md)  
[Elektronisch bankieren voor België](belgian-electronic-banking.md)  
[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)  
[Leveranciersbetalingen voorstellen](../../payables-how-suggest-vendor-payments.md)  
[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)  
[Elektronische betalingen testen](how-to-test-electronic-payments.md)  
[Betalingsbestanden afdrukken](how-to-print-payment-files.md)  
