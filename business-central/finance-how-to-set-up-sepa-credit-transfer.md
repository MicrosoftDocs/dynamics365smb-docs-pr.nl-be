---
title: SEPA-krediettransfer instellen | Microsoft Docs
description: Leren hoe u SEPA-krediettransfer kunt instellen in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 64abd01caa2a2f6845bb3d54c7721333a0a360b3
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-credit-transfer"></a>SEPA-krediettransfer instellen
Vanuit het venster **Betalingsdagboek** kunt u betalingen exporteren naar een bestand om deze te uploaden naar uw elektronische bank voor verwerking van de gekoppelde geldtransfers. [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt de indeling voor SEPA-kredietoverboekingen, maar in uw land of regio kunnen andere indelingen voor elektronische betalingen beschikbaar zijn.  

Als u de export van bankbestandsindelingen die niet standaard worden ondersteund in [!INCLUDE[d365fin](includes/d365fin_md.md)] mogelijk wilt maken, kunt u een gegevensuitwisselingsdefinitie instellen met behulp van het kader voor gegevensuitwisseling. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

Voordat u elektronische betaling kunt verwerken door betalingsbestanden te exporteren in de SEPA-overmakingsindeling, moet u de volgende instellingenstappen uitvoeren:  

* De betreffende bankrekening instellen om de indeling voor SEPA-kredietoverboekingen te verwerken  
* Leverancierskaarten instellen om betalingen te verwerken door bestanden te exporteren in de indeling voor SEPA-kredietoverboekingen  
* De gerelateerde dagboekbatch instellen om betalingexports via het venster **Betalingsdagboek** in te schakelen  
* De definitie van gegevensuitwisseling voor een of meer betalingstypen verbinden met de relevante betalingsmethode(n)  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Een bankrekening instellen voor SEPA-kredietoverboekingen  
1. Voer in het tekstvak **Zoeken** de tekst **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart van de bankrekening waaruit u betalingsbestanden gaat exporteren in de SEPA-overmakingsindeling.  
3. Kies op het sneltabblad **Transfer** in het veld **Exportindeling betaling** de optie **SEPAAI**.  
4. In het veld **Bericht-id krediettransf. SEPA** kiest u een nummerreeks waaruit nummers aan SEPA-overmakingsposten worden toegewezen.  
5. Zorg dat het veld **IBAN** is ingevuld.  

    > [!NOTE]  
    >  Het veld **Valutacode** moet worden ingesteld op **EUR**, omdat SEPA-kredietoverboekingen alleen kunnen worden gemaakt in de valuta EURO.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Een leverancierskaart instellen voor SEPA-kredietoverboekingen  
1. Geef in het vak **Zoeken** **Leveranciers** op en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart van de leverancier die u elektronisch gaat betalen door betalingsbestanden te exporteren in de SEPA-overmakingsindeling.  
3. Kies op het sneltabblad **Betaling** in het veld **Betalingswijze** de optie **BANK**.  
4. In het veld **Bankrekeningcode van voorkeur** kiest u de bank waarnaar het geld wordt overgemaakt wanneer het door uw elektronische bank wordt verwerkt.  

     De waarde in het veld **Bankrekeningcode van voorkeur** wordt gekopieerd naar het veld **Bankrekening ontvanger** in het venster **Betalingsdagboek**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Het betalingsdagboek instellen om betalingsbestanden te exporteren  
1. Voer in het tekstvak **Zoeken** **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open het betalingsdagboek dat u gebruikt om betalingen te verwerken door bestanden te exporteren in de SEPA-overmakingsindeling.  
3. Kies de vervolgkeuzeknop in het veld **Batchnaam**.  
4. Kies in het venster **Fin. dagboekbatches** op het tabblad **Start** in de groep **Beheren** de optie **Lijst bewerken**.  
5. Op de regel voor het betalingsdagboek dat u wilt gebruiken om betalingen te exporteren, schakelt u het selectievakje **Exporteren betaling toestaan** in.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>De definitie van gegevensuitwisseling voor een of meer betalingstypen verbinden met de relevante betalingsmethode(n)  
1. Voer in het tekstvak **Zoeken** de tekst **Betalingswijzen** in en kies vervolgens de gerelateerde koppeling.  
2. In het venster **Betalingsmethoden** selecteert u de betalingswijze die wordt gebruikt om betalingen te exporteren en vervolgens kiest u het veld **Regeldefinitie betalingsexport**.  
3. In het venster **Regeldefinities betalingsexport** selecteert u de code die u hebt opgegeven in het veld **Code** op het sneltabblad **Regeldefinities** in stap 4 van de sectie 'De opmaak van regels en kolommen in het bestand beschrijven' van [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).  

    De incassomachtiging wordt automatisch ingevoegd in het veld **Machtigingsnummer voor incasso** wanneer u een verkoopfactuur maakt voor de klant die u in stap 2 hebt geselecteerd. Zie voor meer informatie [Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Zie ook  
[Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)  
[Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)  

