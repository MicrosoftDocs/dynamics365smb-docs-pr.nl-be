---
title: Een boeking ongedaan maken door een tegenpost te boeken
description: 'Als u een fout vindt in een geboekt dagboek, kunt u de actie Transactie storneren gebruiken om de boeking ongedaan te maken met een correcte audittrail.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/07/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Journaalboekingen tegenboeken en ontvangsten/verzendingen ongedaan maken

Tegenjournaalboekingen zijn bijvoorbeeld nuttig voor het corrigeren van fouten en het wissen van een oude transitoriapost voordat een nieuwe wordt ingevoerd. Een corrigerende post is hetzelfde als de oorspronkelijke post, maar heeft een tegenovergesteld teken in het veld **Bedrag**. De tegenboekingspost moet hetzelfde documentnummer en dezelfde boekingsdatum hebben als de oorspronkelijke post. Nadat een post is tegengeboekt, moet u de juiste post maken.

U kunt alleen posten tegenboeken die zijn geboekt vanaf een algemene dagboekregel. Een post kan slechts één keer worden tegengeboekt.

Als u een boeking van een ontvangst of verzending ongedaan wilt maken voordat ze als gefactureerd worden geboekt, kunt u de functie **Ongedaan maken** in het geboekte document gebruiken. U kunt hoeveelheden van het type **Artikel** en **Resource** ongedaan maken.

Als u een onjuist negatief aantal hebt geboekt, dat wil zeggen, als u een inkooporder hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze order hebt geboekt als ontvangen maar niet gefactureerd, kunt u de boeking ongedaan maken.

Als u een onjuist positief aantal hebt geboekt, dat wil zeggen, als u een verkoopverzending of een inkoopretourzending hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze hebt geboekt als verzonden maar niet gefactureerd, kunt u de boeking ongedaan maken.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>De dagboekboeking van een grootboekpost tegenboeken

U kunt posten vanuit alle **Posten**-pagina's tegenboeken. De volgende procedure is gebaseerd op de pagina **Grootboekposten**.

> [!NOTE]
> De post moet afkomstig zijn uit een dagboekboeking.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de post die u wilt tegenboeken en kies vervolgens de actie **Transactie tegenboeken**.
3. Kies op de pagina **Transactieposten tegenboeken** de actie **Tegenboeken**.
4. Kies **Ja** om de tegenboeking te bevestigen.

## <a name="to-post-a-negative-entry"></a>Een negatieve post boeken

Gebruik het veld **Storno** om een negatief debetbedrag in plaats van een creditbedrag te boeken, of om een negatief creditbedrag in plaats van een debetbedrag op een rekening te boeken. Standaard is het veld beschikbaar in alle dagboeken. De velden **Debetbedrag** en **Creditbedrag** bevatten beide zowel de oorspronkelijke post als de gecorrigeerde post. Deze velden hebben geen invloed op het rekeningsaldo.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling  
2. Selecteer in het veld **Batchnaam** de juiste batchnaam.  
3. Voer informatie in de relevante velden in.  
4. Selecteer op de dagboekregel die u wilt activeren voor negatieve posten het selectievakje **Storno**.  
5. Als u naar het dagboek wilt boeken, kiest u de actie **Boeken** en kiest u vervolgens de knop **Ja**.

## <a name="to-undo-a-quantity-on-a-posted-purchase-receipt"></a>Een aantal ongedaan maken in een geboekte inkoopontvangst

In de volgende stappen wordt beschreven hoe u een geboekte ontvangst van artikelen of resources ongedaan kunt maken. De stappen zijn vergelijkbaar met de stappen voor geboekte verzendingen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte inkoopontvangsten** in en kies vervolgens de gerelateerde koppeling  
2. Open de geboekte ontvangst die u ongedaan wilt maken.  
3. Selecteer de regel(s) die u ongedaan wilt maken.  
4. Kies de actie **Ontvangst ongedaan maken**.

Er wordt een correctieregel toegevoegd onder de geselecteerde ontvangstregel. Als de hoeveelheid in een magazijnontvangst is ontvangen, wordt een correctieregel toegevoegd op de geboekte magazijnontvangst.  

De velden **Ontvangen aantal** en **Niet geboekt aantal** op de bijbehorende inkooporder worden ingesteld op nul.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Een aantalboeking ongedaan maken en opnieuw uitvoeren voor een geboekte retourzending

In de volgende stappen wordt uitgelegd hoe u:

* Een geboekte retourzending van artikelen of middelen ongedaan maken.
* Boek de inkoopretour opnieuw met een nieuwe hoeveelheid.

De stappen zijn vergelijkbaar met de stappen voor geboekte ontvangsten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte retourverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de geboekte retourzending die ongedaan moet worden gemaakt.
3. Selecteer de regel(s) die u ongedaan wilt maken.  

4. Kies de actie **Retourverzending ongedaan maken**.  

    In het geboekte document wordt een gecorrigeerde regel ingevoegd. Op de retourorder worden de velden **Retouraantal verzonden** en **Retourverzending niet gefact.** ingesteld op nul.  

    Ga nu terug naar de inkoopretourorder om opnieuw te boeken.  

5. Let op de pagina **Geboekte retourverzending** op het nummer in het **Retourordernr.** toevoegen.  
6. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopretourorders** in en selecteer vervolgens de gerelateerde koppeling.  
7. Open de retourorder en kies de actie **Opnieuw openen**.  
8. Corrigeer de post in het veld **Aantal** en boek de inkoopretourorder opnieuw.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## <a name="reverse-a-customer-and-vendor-ledger-entry-with-a-realized-gain-or-loss-entry"></a>Een klanten- en leverancierspost ongedaan met een gerealiseerde winst- of verliespost

U kunt de actie **Transactie tegenboeken** gebruiken om betalingen terug te boeken die zijn vereffend met posten die afkomstig zijn uit vreemde valuta's en die zijn aangepast met de batchverwerking Wisselkoersherwaardering. De functie werkt voor zowel aankopen als verkopen.

Het volgende is een eenvoudig scenario dat illustreert hoe het werkt:

1. Boek een verkoopfactuur voor een klant in een vreemde valuta.
2. Pas de wisselkoers voor die valuta aan.
3. Boek een betaling die met de factuur wordt vereffend.
4. Maak de vereffening ongedaan en draai de betalingstransactie terug, bijvoorbeeld vanaf de pagina **Klantenposten**.

## <a name="see-also"></a>Zie ook

[Assemblageboeking ongedaan maken](assembly-how-to-undo-assembly-posting.md)  
[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
