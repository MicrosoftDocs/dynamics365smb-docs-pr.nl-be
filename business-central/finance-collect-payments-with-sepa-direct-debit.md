---
title: Automatische incasso via SEPA in Business Central
description: Met instemming van de klant kunt u betalingen rechtstreeks vanaf de bankrekening van de klant verzamelen volgens de SEPA-indeling.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="collect-payments-with-sepa-direct-debit" />Betalingen verzamelen via automatische incasso van SEPA

Met instemming van de klant kunt u betalingen rechtstreeks vanaf de bankrekening van de klant verzamelen volgens de SEPA-indeling.  

Stel eerst de exportindeling van het bankbestand in waarmee u uw bank opdracht geeft een automatische incasso uit te voeren. Installeer vervolgens de betalingswijze van de klant. Stel tot slot de machtiging voor automatische incasso in die overeenkomt met uw overeenkomst met de klant voor het verzamelen van hun betalingen in een bepaalde overeenkomstperiode.  

Om de bank het bedrag van de bankrekening van de klant over te laten brengen naar het account van uw bedrijf, moet u een verzameling van incasso maken met gegevens over bankrekeningen, de betrokken verkoopfacturen en de incassomachtiging. U exporteert vervolgens een XML-bestand dat is gebaseerd op de verzamelingspost en verzendt dat naar uw bank voor verwerking. Betalingen die niet konden worden verwerkt worden aan u gemeld door uw bank. U moet vervolgens handmatig de desbetreffende verzamelingsposten van automatische incasso weigeren.  

U kunt standaardklantenverkoopcodes instellen met de informatie over de betalingsmethode voor automatische incasso en de machtigingen voor automatische incasso. Vervolgens kunt u de batchverwerking **Std. klantfacturen maken** gebruiken om meerdere verkoopfacturen te genereren waarvoor de gegevens voor automatische incasso automatisch zijn ingevuld. Dit kan handmatig of automatisch worden uitgevoerd volgens de vervaldatum van de betaling.  

Wanneer betalingen met succes worden verwerkt, zoals aangegeven door uw bank, kunt u de betalingsontvangsten rechtstreeks vanuit de pagina **Verzamelingsposten van incasso** boeken of door de betalingsregels naar het dagboek te verplaatsen waarin u betalingsontvangsten boekt, zoals op de pagina **Ontvangstendagboek**. Afhankelijk van uw proces voor kasbeheer kunt u ook wachten en de betalingen alleen vereffenen als onderdeel van de bankreconciliatie.  

> [!NOTE]  
> Om betalingen te innen via SEPA Incasso, moet de valuta in de verkoopfactuur EURO zijn.  

## <a name="setting-up-sepa-direct-debit" />Automatische incasso via SEPA instellen

Vanuit de pagina **Incasso-opdrachten** kunt u instructies naar uw elektronische bank exporteren om een automatische incasso van de bankrekening van de klant uit te voeren naar uw bankrekening, volgens de SEPA-indeling voor incasso.

> [!NOTE]
> De globale versie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt alleen de SEPA-indeling voor incasso. In de versie van uw land/regio kunnen andere indelingen voor elektronische betaling worden ondersteund. Zie onder **Lokale functionaliteit** in de inhoudsopgave.  

Als u de export van bankbestandsindelingen die niet standaard worden ondersteund in [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk wilt maken, kunt u een gegevensuitwisselingsdefinitie instellen met behulp van het kader voor gegevensuitwisseling. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

Voordat u betalingen van klanten elektronisch kunt verwerken door instructies voor automatische incasso te exporteren in de SEPA-indeling voor incasso, moet u de volgende instellingenstappen uitvoeren:  

* Stel de exportindeling in van het bankbestand waarmee u uw bank opdracht geeft voor het uitvoeren van automatische incasso's van de bankrekening van de klant naar uw bankrekening.  
* Stel de betalingswijze van de klant in.  
* Stel de machtiging voor automatische incasso in die overeenkomt met uw overeenkomst met de klant voor het incasseren van hun betalingen in een bepaalde overeenkomstperiode.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit" />Uw bankrekening voor automatische incasso van SEPA instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de bankrekening die u wilt gebruiken voor automatische incasso.  
3. Kies op het sneltabblad **Transfer** in het veld **Exportindeling van incasso van SEPA** de optie voor automatische incasso van SEPA.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit" />De betalingsmethode van de klant voor SEPA-incasso instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsmethoden** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Een betalingswijze instellen. Vul de specifieke velden voor automatische incasso in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Incasso**|Geef aan of de betalingsmethode wordt gebruikt voor verzameling automatische incasso van SEPA.|  
    |**Betalingscondities van betaling per incasso**|Geef de betalingsvoorwaarden, bijvoorbeeld NIET BETALEN, op die worden weergegeven op de verkoopfacturen die worden betaald via automatische incasso van SEPA om aan te geven aan de klant dat de betaling automatisch wordt geïnd. U kunt het veld ook leeg laten.|  

    > [!NOTE]  
    >  Voer geen waarde in het veld **Tegenrekeningnr.** in.  

4. Kies de knop **OK** om de pagina **Betalingsmethoden** te sluiten.  
5. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  
6. Open de klantkaart voor de klant die u wilt instellen voor verzameling van automatische incasso van SEPA.  
7. Kies het veld **Betalingswijze** en selecteer vervolgens de code voor de betalingswijze die u hebt opgegeven in stap 3.  
8. Herhaal stap 6 tot en met 7 voor alle klanten die u wilt instellen voor verzameling van automatische incasso van SEPA.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement" />De incassomachtiging instellen die de instemming van de klant vertegenwoordigt

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart voor de klant die u wilt instellen voor automatische incasso van SEPA.  
3. Kies de actie **Bankrekeningen**.  
4. Selecteer op de pagina **Lijst klantbankrekeningen** de klantbankrekening waarop automatische incasso's worden gebruikt en kies de actie **Opdrachten voor automatische incasso**.  
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

6. Herhaal stap 1 tot en met 5 voor alle klanten die u wilt instellen voor automatische incasso van SEPA.  

 De incassomachtiging wordt automatisch ingevoegd in het veld **Machtigingsnummer voor incasso** wanneer u een verkoopfactuur maakt voor de klant die u in stap 2 hebt geselecteerd. Zie voor meer informatie [Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file" />SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand

Om de bank het bedrag van de bankrekening van de klant over te laten maken naar de rekening van uw bedrijf, moet u een incasso-opdracht maken met informatie over de bankrekening van de klant, de betreffende verkoopfacturen en de incassomachtiging. Uit de resulterende verzamelingspost van automatische incasso export u vervolgens een XML-bestand dat u naar uw elektronische bank verzendt of uploadt voor verwerking. Betalingen die niet konden worden verwerkt door de bank worden aan u gemeld door uw bank. U moet vervolgens handmatig de desbetreffende verzamelingsposten van automatische incasso weigeren.  

 > [!NOTE]  
 > Om betalingen te innen via SEPA Incasso, moet de valuta in de verkoopfactuur EURO zijn.  

### <a name="to-create-a-direct-debit-collection" />Een incasso-opdracht maken

 1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Automatische incasso's** in en kies vervolgens de gerelateerde koppeling.  
 2. Kies op de pagina **Automatische incasso's** de actie **Automatische incasso maken**.  
 3. Vul op de pagina **Incasso-opdracht maken** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Vanaf vervaldatum**|Geef de eerste betalingsvervaldatum aan op de verkoopfacturen die u wilt maken voor een incasso-opdracht.|  
    |**Tot vervaldatum**|Geef de laatste betalingsvervaldatum aan op de verkoopfacturen die u wilt maken voor een automatische incasso-verzameling.|  
    |**Partnersoort**|Geef aan of de verzameling automatische incasso is gemaakt voor klanten van het type **Bedrijf** of **Persoon**.|  
    |**Alleen klanten met geldige machtiging**|Geef aan of een incasso-opdracht wordt gemaakt voor klanten die beschikken over een geldige incassomachtiging. **Opmerking:** er wordt ook een automatische incasso-opdracht gemaakt als het veld **Machtigingsnummer voor incasso** niet is ingevuld op de verkoopfactuur.|  
    |**Alleen facturen met geldige machtiging**|Geef op of de incasso-opdracht alleen wordt gemaakt voor verkoopfacturen als een geldige incassomachtiging is geselecteerd in het veld **Machtigingsnummer voor incasso** op de verkoopfactuur.|  
    |**Bankrekeningnr.**|Geef op naar welke bankrekeningen van uw bedrijf de verzamelde betaling wordt overgeboekt van de bankrekening van de klant.|  
    |**Bankrekeningnaam**|Geeft de naam van de bankrekening weer die u selecteert in het veld **Bankrekeningnr.**. Dit veld wordt automatisch ingevuld.|  

 4. Kies de knop **OK**.  

Er wordt een automatische incasso-opdracht toegevoegd aan de pagina **Incasso-opdrachten** en er worden een of meer automatische incasso-opdrachtposten gemaakt.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file" />Verzamelingposten van automatische incasso exporteren naar een bankbestand

 1. Kies op de pagina **Automatische incasso's** de actie **Automatische incasso-items**.  
 2. Selecteer op de pagina **Automatische incasso-items** het item dat u wilt exporteren en kies de actie **Automatische-incassobestand maken**.  
 3. Sla het exportbestand op naar de locatie van waar u verzendt of uploadt naar uw elektronische bank.  

      Op de pagina **Verzamelingsposten van incasso** verandert het veld **Incasso-opdrachtstatus** in Bestand gemaakt. Op de pagina **SEPA Incasso Machtiging** wordt het veld **Debetteller** bijgewerkt met één telling.  

 Als het geëxporteerde bestand niet kan worden verwerkt, bijvoorbeeld omdat de klant insolvent is, kunt u de incasso-opdrachtpost weigeren. Als het geëxporteerde bestand met succes is verwerkt door de bank, worden de verschuldigde betalingen van de betrokken verkoopfacturen automatisch geïnd bij de betrokken klanten. In dat geval kunt u de incasso sluiten.  

### <a name="to-reject-a-direct-debit-collection-entry" />Een incasso-opdrachtpost weigeren

* Selecteer op de pagina **Automatische incasso-items** het item dat niet correct is verwerkt en kies de actie **Item afwijzen**.  

    De waarde in het veld **Status** op de pagina **Verzamelingsposten van incasso** verandert in **Geweigerd**.  

### <a name="to-close-a-direct-debit-collection" />Een incasso-opdracht sluiten

* Selecteer op de pagina **Automatische incasso-items** het item dat niet correct is verwerkt en kies de actie **Incasso sluiten**.  

    De bijbehorende verzameling automatische incasso is gesloten.  

 U kunt nu doorgaan met het boeken van ontvangen betalingen voor de betrokken verkoopfacturen. U kunt dit doen terwijl u, als gewoonlijk, betalingsontvangsten boekt, bijvoorbeeld op de pagina **Betalingsregistratie**, of u kunt de gerelateerde betalingsontvangsten rechtstreeks boeken vanuit de pagina **Verzamelingsposten van incasso**. Zie voor meer informatie [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts" />SEPA-betalingsontvangsten via automatische incasso boeken

Wanneer een incasso-opdracht wordt verwerkt door uw bank, kunt u doorgaan met het boeken van de ontvangst van de betaling voor de betrokken verkoopfacturen. Zie voor meer informatie [SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

U kunt de betalingsontvangst van de pagina **Incasso-opdrachten** of de pagina **Verzamelingsposten van incasso** direct boeken. U kunt ook het werk aan een andere gebruiker doorgeven door de dagboekregels voor te bereiden.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page" />Een betalingsontvangst van een automatische incasso boeken vanuit de pagina Verzamelingen van automatische incasso

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Automatische incasso's** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een regel voor een verzameling automatische incasso die is geëxporteerd naar een bankbestand en verwerkt door de bank.
3. Kies de actie **Betalingsontvangsten boeken**.  
4. Vul op de pagina **Incasso-opdracht boeken** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Incasso-opdrachtnr.**|Geef de verzameling automatische incasso op waar u een betalingsontvangst voor wilt boeken.|  
    |**Algemeen dagboeksjabloon**|Geef op welk dagboeksjabloon te gebruiken voor het boeken van de betalingsontvangst, zoals de sjabloon voor ontvangsten.|  
    |**Batchnaam financieel dagboek**|Geef op welke dagboekbatch moet worden gebruikt voor het boeken van de betalingsontvangst.|  
    |**Alleen dagboek aanmaken**|Schakel dit selectievakje in als u niet de betalingsontvangst boeken wilt wanneer u de **OK** knop kiest. De betalingsontvangst in het opgegeven dagboek wordt voorbereid en wordt niet geboekt totdat iemand de dagboekregels in kwestie boekt.|  

5. Kies de knop **Ok**.

## <a name="see-also" />Zie ook

[Tegoeden beheren](receivables-manage-receivables.md)  
[Servicebeheer](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
