---
title: Automatische incasso via SEPA instellen | Microsoft Docs
description: Leren hoe u automatische incasso door SEPA kunt instellen in Business Central
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 9e2ef9ec3b454e5a9bb5097ba3ed30c5756d2352
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816029"
---
# <a name="set-up-sepa-direct-debit"></a>Automatische incasso via SEPA instellen
Vanuit de pagina **Incasso-opdrachten** kunt u instructies aan uw elektronische bank exporteren om een automatische incasso van de bankrekening van de klant uit te voeren naar uw bankrekening. [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt de indeling voor SEPA-incasso's, maar in uw land of regio kunnen andere indelingen voor elektronische betalingen beschikbaar zijn.  

Als u de export van bankbestandsindelingen die niet standaard worden ondersteund in [!INCLUDE[d365fin](includes/d365fin_md.md)] mogelijk wilt maken, kunt u een gegevensuitwisselingsdefinitie instellen met behulp van het kader voor gegevensuitwisseling. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

Voordat u betalingen van klanten elektronisch kunt verwerken door instructies voor automatische incasso te exporteren in de SEPA-indeling voor incasso, moet u de volgende instellingenstappen uitvoeren:  

* Stel de exportindeling in van het bankbestand waarmee u uw bank opdracht geeft voor het uitvoeren van automatische incasso's van de bankrekening van de klant naar uw bankrekening.  
* Stel de betalingswijze van de klant in.  
* Stel de machtiging voor automatische incasso in die overeenkomt met uw overeenkomst met de klant voor het incasseren van hun betalingen in een bepaalde overeenkomstperiode.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Uw bankrekening voor automatische incasso van SEPA instellen  
1. Voer in het tekstvak **Zoeken** de tekst **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de bankrekening die u wilt gebruiken voor automatische incasso.  
3. Kies op het sneltabblad **Transfer** in het veld **Exportindeling van incasso van SEPA** de optie voor automatische incasso van SEPA.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>De betalingsmethode van de klant voor SEPA-incasso instellen  
1. Voer in het tekstvak **Zoeken** de tekst **Betalingswijzen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Een betalingswijze instellen. Vul de specifieke velden voor automatische incasso in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Incasso**|Geef aan of de betalingsmethode wordt gebruikt voor verzameling automatische incasso van SEPA.|  
    |**Betalingscondities van betaling per incasso**|Geef de betalingsvoorwaarden, bijvoorbeeld NIET BETALEN die worden weergegeven op de verkoopfacturen die worden betaald via automatische incasso van SEPA om aan te geven aan de klant dat de betaling automatisch wordt geïnd. U kunt het veld ook leeg laten.|  

    > [!NOTE]  
    >  Voer geen waarde in het veld **Tegenrekeningnr.** in.  

4. Kies de knop **OK** om de pagina **Betalingsmethoden** te sluiten.  
5. Geef in het vak **Zoeken** **Klanten** op en kies vervolgens de gerelateerde koppeling.  
6. Open de klantkaart voor de klant die u wilt instellen voor verzameling van automatische incasso van SEPA.  
7. Kies het veld **Betalingswijze** en selecteer vervolgens de code voor de betalingswijze die u hebt opgegeven in stap 3.  
8. Herhaal stap 6 tot en met 7 voor alle klanten die u wilt instellen voor verzameling van automatische incasso van SEPA.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>De incassomachtiging instellen die de instemming van de klant vertegenwoordigt  
1. Geef in het **Zoeken** **Klanten** op en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart voor de klant die u wilt instellen voor automatische incasso van SEPA.  
3. Kies de actie **Bankrekeningen**.  
4. Selecteer op de pagina **Bankrekeningen klant** de bankrekening van de klant die wordt gebruikt voor automatische incasso en kies vervolgens op het tabblad **Start** in de groep **Verwerken** de optie **Machtigingen voor automatische incasso**.  
5. Vul op de pagina **SEPA Incasso Machtiging** de velden in, zoals is beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Bankrekeningcode van klant**|Geeft de bankrekening op waarop betalingen voor automatische incasso worden verzameld. Dit veld wordt automatisch ingevuld.|  
    |**Geldig vanaf**|Geef de datum op wanneer de incassomachtiging begint.|  
    |**Geldig tot**|Geef de datum op wanneer de incassomachtiging eindigt.|  
    |**Ondertekeningsdatum**|Geef de datum op waarop de klant de incassomachtiging heeft ondertekend.|  
    |**Type betaling**|Geef aan of de overeenkomst betrekking heeft op meerdere (**doorlopende**) of één (**éénmalige**) verzamelingen van incasso.|  
    |**Verwacht aantal debiteringen**|Geef op hoeveel verzamelingen van automatische incasso u verwacht te maken. Dit veld is alleen van toepassing als u **Periodiek** in het veld **Type betaling** hebt geselecteerd.|  
    |**Debetteller**|Geeft aan hoeveel verzamelingen van incasso zijn gemaakt met deze incassomachtiging. Dit veld wordt automatisch bijgewerkt.|  
    |**Geblokkeerd**|Geef aan dat verzamelingen van incasso niet kunnen worden gemaakt met deze incassomachtiging.|  

6.  Herhaal stap 1 tot en met 5 voor alle klanten die u wilt instellen voor automatische incasso van SEPA.  

 De incassomachtiging wordt automatisch ingevoegd in het veld **Machtigingsnummer voor incasso** wanneer u een verkoopfactuur maakt voor de klant die u in stap 2 hebt geselecteerd. Zie voor meer informatie [Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Zie ook  
[Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)
[Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md)
[Gegevens elektronisch uitwisselen](across-data-exchange.md)
