---
title: 'Belgische ncasso via domiciliëring [BE]'
description: 'Een domiciliëring is een financiële overeenkomst tussen u en uw klanten, zodat u de betalingen voor facturen van de klant automatisch kunt innen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
ms.date: 06/17/2021
ms.author: bholtorf
---
# <a name="direct-debit-using-domiciliation"></a>Incasso via domiciliëring

Een domiciliëring is een financiële overeenkomst tussen u en uw klanten, zodat u de betalingen voor facturen van de klant automatisch kunt innen via een bankrekening van voorkeur. Domiciliëringen kunnen alleen worden verwerkt voor binnenlandse klanten met binnenlandse bankrekeningen. Domiciliëringen in vreemde valuta's of via buitenlandse banken worden niet ondersteund.  

Incasso via domiciliëring is handig voor bedrijven met veel klanten of abonnees, zoals een nutsbedrijf of een uitgever.  

Voordat u kunt beginnen met elektronisch bankieren voor domiciliëringen, moet u bepaalde basisinformatie invoeren.  

- Domiciliëringsnummer: dit is een unieke code die u van de bank ontvangt en waarmee de domiciliëringsovereenkomst tussen u, uw klant en de bank wordt geïdentificeerd. Het contract bevat informatie over de betalingsfrequentie, bankrekeningnummers en bedragen. Wanneer u betalingen naar de bank verzendt, gebruikt de bank het domiciliëringsnummer om alle betrokken partijen te identificeren.  

- Bankrekening van voorkeur: de bankrekening van voorkeur wordt voorgesteld als standaardbankrekening in alle domiciliëringsvoorstellen voor die klant. Indien nodig kunt u de bankrekening wijzigen voordat u de domiciliëringsvoorstellen boekt. Zie [Domiciliëringsvoorstellen genereren](/dynamics365/business-central/LocalFunctionality/Belgium/direct-debit-using-domiciliation) voor meer informatie.  

## <a name="set-up-domiciliations"></a>Domiciliëringen instellen

Voordat u kunt beginnen met elektronisch bankieren voor domiciliëringen, moet u het domiciliëringsnummer van de klant en de bankrekening van voorkeur opgeven.  

> [!NOTE]  
> U moet één bankrekening per klant gebruiken voor alle domiciliëringen.  

### <a name="to-set-up-domiciliation"></a>Domiciliëring instellen

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de klant en kies vervolgens de actie **Bewerken**.  
3. Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Description|  
    |-----|-----------|  
    |**Domiciliëring**|Voer het domiciliëringsnummer voor de klant in. Dit nummer wordt gebruikt als u domiciliëringen voor deze klant maakt.|  
    |**Bankrekening van voorkeur**|Voer de bankrekening van voorkeur in voor transacties met deze klant. Deze rekening wordt gebruikt als u een betalingsvoorstel maakt voor deze klant.|  

## <a name="generate-domiciliation-suggestions"></a>Domiciliëringsvoorstellen genereren

Als u domiciliëringen hebt ingesteld, kunt u beginnen met het genereren van domiciliëringsvoorstellen. In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u domiciliëringsvoorstellen alleen voor binnenlandse klanten maken.  

### <a name="to-generate-domiciliation-suggestions"></a>Domiciliëringsvoorstellen genereren

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Domiciliëringsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Domiciliëringen voorstellen**.  
3. Vul de velden in zoals weergegeven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Vervaldatum**|Geef hier de vervaldatum voor de batchverwerking op. Alleen posten met een vervaldatum vóór of op deze datum worden opgenomen.|  
    |**Contantkorting nemen**|Selecteer deze optie als u in de batchverwerking klantposten wilt opnemen waarvoor u een contantkorting kunt krijgen.|  
    |**Kortingsvervaldatum betaling**|Typ de datum die wordt gebruikt om de contantkorting te berekenen.|  
    |**Mogelijke terugbetalingen selecteren**|Selecteer deze optie als in de batchverwerking terugbetalingen moeten worden opgenomen.|  
    |**Boekingsdatum**|Typ de datum die als boekingsdatum verschijnt op de regels die tijdens de batchverwerking in het domiciliëringsdagboek worden ingevoegd.|  

4. Voer aanvullende filtercriteria in.  
5. Kies de knop **Ok**.  

Wanneer de batchverwerking is uitgevoerd, bevat het domiciliëringsdagboek alle openstaande klantenposten die overeenkomen met de filters.  

> [!NOTE]  
> De domiciliëringsvoorstellen bevatten alleen klanten waarvoor een domiciliëringsnummer is ingesteld. Zie de sectie [Domiciliëringen instellen](#set-up-domiciliations) voor meer informatie.  

## <a name="edit-and-delete-domiciliation-lines"></a>Domiciliëringsregels bewerken en verwijderen

Nadat u domiciliëringsvoorstellen hebt gegenereerd, wilt u wellicht de domiciliëringsregels wijzigen. U kunt bijvoorbeeld een bankrekening opnieuw toewijzen of betaling voor een bepaalde klant of klantenpost voorkomen.  

Nadat u de dagboekregels hebt gewijzigd, drukt u het rapport **Domiciliëringsdagboek - Test** af om alle regels te testen.  

Met de batchverwerking **Domiciliëringen voorstellen** maakt u domiciliëringsvoorstellen voor alle klanten die overeenkomen met de opgegeven criteria.  

### <a name="to-edit-a-journal-line"></a>Een dagboekregel bewerken

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Domiciliëringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3. Selecteer de dagboekregel en bewerk de velden.  

### <a name="to-delete-a-journal-line"></a>Een dagboekregel verwijderen

1 Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Domiciliëringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3. Selecteer de dagboekregel en kies de actie **Verwijderen**.  
4. Kies de knop **Ja**.  

## <a name="test-domiciliations"></a>Domiciliëringen testen

Als u de domiciliëringsdagboekregels wilt testen, kunt u het rapport **Domiciliëringsdagboek - Test** gebruiken. Hiermee drukt u een overzicht af van alle dagboekregels en eventuele fouten, zoals ontbrekende velden of onjuiste bankrekeningen. U moet alle fouten corrigeren voordat u de regels kunt boeken.  

### <a name="to-print-a-domiciliation-test-report"></a>Een domiciliëringstestrapport afdrukken

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Domiciliëringsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3. Kies de actie **Testrapport**.  
4. Kies de knop **Afdrukken** om het rapport af te drukken of kies de knop **Voorbeeld** om het rapport op het scherm weer te geven.  

## <a name="export-and-post-domiciliations"></a>Domiciliëringen exporteren en boeken

U kunt domiciliëringen naar uw bank verzenden door de gegevens naar een bestand te exporteren. Wanneer u naar een bestand exporteert, kunt u ervoor kiezen de regels automatisch naar het grootboek te boeken.  

Afhankelijk van de instelling van het veld **Exportindeling van incasso van SEPA** op de pagina **Bankrekeningkaart**, wordt met de actie **Bestandsdomiciliëringen** een van deze aanvraagpagina's geopend:  

- De pagina **Dagboekregels maken**, voor de indeling SEPA Incasso.  
- De pagina **Bestandsdomiciliëringen**, voor binnenlandse indelingen.  

### <a name="to-export-and-post-domiciliations"></a>Domiciliëringen exporteren en boeken

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Domiciliëringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Bestandsdomiciliëringen**.  
3. Vul op de pagina **Dagboekregels maken** de benodigde velden in. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    Als uw bedrijf is ingesteld voor het gebruik van de ISABEL-indeling, wordt de **Bestandsdomiciliëringen** weergegeven.
4. Klik op **OK** om het bestand te exporteren.  
5. Kies de locatie van waar u het bestand naar uw bank wilt uploaden en kies **Opslaan**.  
6. Kies de knop **Ja** om de domiciliëringsdagboekregels automatisch te boeken.  

    Als u het selectievakje **Dagboekregels boeken** niet hebt ingeschakeld, moet u de domiciliëringen handmatig in het dagboek boeken.  

    > [!NOTE]  
    >  Nadat u domiciliëringen in het dagboek hebt geboekt, verwijdert u de geboekte domiciliëringen op de pagina **Domiciliëringsdagboek**. Hiervoor selecteert u alle regels met de status **Geboekt** en kiest u de actie **Verwijderen**.  

## <a name="see-also"></a>Zie ook

[Belgische elektronische betalingen](belgian-electronic-payments.md)  
[Elektronisch bankieren voor België](belgian-electronic-banking.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
