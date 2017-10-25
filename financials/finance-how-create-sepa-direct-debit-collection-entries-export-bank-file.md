---
title: SEPA-verzamelingsposten van automatische incasso exporteren | Microsoft Docs
description: Maak een incasso-opdracht die informatie over de bankrekening van de klant, de betrokken verkoopfacturen en de incassomachtiging bevat.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f6ebcafa1585d4f722802a6891a20a895aa96060
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Procedure: SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand
Om de bank het bedrag van de bankrekening van de klant over te laten maken naar de rekening van uw bedrijf, moet u een incasso-opdracht maken met informatie over de bankrekening van de klant, de betreffende verkoopfacturen en de incassomachtiging. Uit de resulterende verzamelingspost van automatische incasso export u vervolgens een XML-bestand dat u naar uw elektronische bank verzendt of uploadt voor verwerking. Betalingen die niet konden worden verwerkt door de bank worden aan u gemeld door uw bank. U moet vervolgens handmatig de desbetreffende verzamelingsposten van automatische incasso weigeren.  

> [!NOTE]  
>  Om betalingen te innen via SEPA Incasso, moet de valuta in de verkoopfactuur EURO zijn.  

### <a name="to-create-a-direct-debit-collection"></a>Een incasso-opdracht maken  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Incasso-opdrachten** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **Incasso-opdrachten** op het tabblad **Start** in de groep **Nieuw** de optie **Incasso-opdracht maken**.  
3. Vul in het venster **Incasso-opdracht maken** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Vanaf vervaldatum**|Geef de eerste betalingsvervaldatum aan op de verkoopfacturen die u wilt maken voor een incasso-opdracht.|  
    |**Tot vervaldatum**|Geef de laatste betalingsvervaldatum aan op de verkoopfacturen die u wilt maken voor een automatische incasso-verzameling.|  
    |**Partnersoort**|Geef aan of de verzameling automatische incasso is gemaakt voor klanten van het type **Bedrijf** of **Persoon**.|  
    |**Alleen klanten met geldige machtiging**|Geef aan of een incasso-opdracht wordt gemaakt voor klanten die beschikken over een geldige incassomachtiging. **Opmerking:** er wordt ook een automatische incasso-opdracht gemaakt als het veld **Machtigingsnummer voor incasso** niet is ingevuld op de verkoopfactuur.|  
    |**Alleen facturen met geldige machtiging**|Geef op of de incasso-opdracht alleen wordt gemaakt voor verkoopfacturen als een geldige incassomachtiging is geselecteerd in het veld **Machtigingsnummer voor incasso** op de verkoopfactuur.|  
    |**Bankrekeningnr.**|Geef op naar welke bankrekeningen van uw bedrijf de verzamelde betaling wordt overgeboekt van de bankrekening van de klant.|  
    |**Bankrekeningnaam**|Geeft de naam van de bankrekening weer die u selecteert in het veld **Bankrekeningnr.**. Dit veld wordt automatisch ingevuld.|  

4. Kies de knop **OK**.  

     Er wordt een automatische incasso-opdracht toegevoegd aan het venster **Incasso-opdrachten** en er worden een of meer automatische incasso-opdrachtposten gemaakt.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Verzamelingposten van automatische incasso exporteren naar een bankbestand  
1. Kies in het venster **Incasso-opdrachten** op het tabblad **Start** in de groep **Verwerken** de optie **Verzamelingsposten van incasso**.  
2. Selecteer in het venster **Verzamelingsposten van incasso** de post die u wilt exporteren en kies vervolgens op het tabblad **Start** in de groep **Verwerken** de optie **Bestand van automatische incasso aanmaken**.  
3. Het exportbestand opslaan naar de locatie van waar u verzendt of uploadt naar uw elektronische bank.  

     In het venster **Verzamelingsposten van incasso** verandert het veld **Incasso-opdrachtstatus** in Bestand gemaakt. In het venster **SEPA Incasso Machtiging** wordt het veld **Debetteller** bijgewerkt met één telling.  

Als het geëxporteerde bestand niet kan worden verwerkt, bijvoorbeeld omdat de klant insolvent is, kunt u de incasso-opdrachtpost weigeren. Als het geëxporteerde bestand met succes is verwerkt door de bank, worden de verschuldigde betalingen van de betrokken verkoopfacturen automatisch geïnd bij de betrokken klanten. In dat geval kunt u de incasso sluiten.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Een incasso-opdrachtpost weigeren  

* Selecteer in het venster **Verzamelingsposten van incasso** de post die niet goed is verwerkt en kies vervolgens op het tabblad **Start** in de groep **Verwerken** de optie **Post weigeren**.  

     De waarde in het veld **Status** in het venster **Verzamelingsposten van incasso** verandert in **Geweigerd**.  

### <a name="to-close-a-direct-debit-collection"></a>Een incasso-opdracht sluiten  
*  Selecteer in het venster **Verzamelingsposten van incasso** de post die niet goed is verwerkt en kies vervolgens op het tabblad **Start** in de groep **Verwerken** de optie **Verzameling sluiten**.  

     De bijbehorende verzameling automatische incasso is gesloten.  

U kunt nu doorgaan met het boeken van ontvangen betalingen voor de betrokken verkoopfacturen. U kunt dit doen terwijl u, als gewoonlijk, betalingsontvangsten boekt, bijvoorbeeld in het venster **Betalingsregistratie**, of u kunt de gerelateerde betalingsontvangsten rechtstreeks boeken vanuit het venster **Verzamelingsposten van incasso**. Zie voor meer informatie [Procedure: SEPA-betalingsontvangsten via automatische incasso boeken](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Zie ook  
[Procedure: Automatische incasso via SEPA instellen](finance-how-to-set-up-sepa-direct-debit.md)  
[Procedure: SEPA-betalingsontvangsten via automatische incasso boeken](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)  

