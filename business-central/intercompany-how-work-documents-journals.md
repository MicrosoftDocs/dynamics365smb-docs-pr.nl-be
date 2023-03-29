---
title: IC-documenten en -dagboeken boeken
description: In dit onderwerp wordt uitgelegd hoe u IC-documenten of -dagboeken gebruikt om transacties met uw IC-partners te boeken.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '600, 610'
ms.date: 03/09/2022
ms.author: edupont
---
# Werken met intercompany-documenten en -dagboeken
Door middel van intercompany-documenten of -dagboeken kunt u transacties met uw IC-partners boeken. Wanneer u een IC-document of -dagboekregel boekt in uw bedrijf, wordt een corresponderend document of dagboekregel gemaakt in uw IC-outbox, dat/die u kunt overbrengen naar uw partner. Uw partner kan de bijbehorende transactie vervolgens boeken in zijn bedrijf, zonder de gegevens opnieuw te hoeven invoeren.

Bij inkoop- en verkoopdocumenten zorgt de IC-partnercode voor de betrokken klant of leverancier ervoor dat alle gegenereerde orders en facturen die verband houden met transacties met deze bedrijven de bijbehorende documenten aanmaken in het partnerbedrijf, zodat de rekeningen overal sluitend zijn.

Voor IC-diversendagboekregels hoeft u geen rekeningen op te geven voor een aparte reeks boeken, maar geeft u eenvoudigweg de ID van het partnerbedrijf op. Corresponderende IC-grootboekregels worden dan in het partnerbedrijf gemaakt, die resulteren in het sluitend maken van de boeken van beide bedrijven die bij de transactie zijn betrokken.

## Een IC-verkooporder invullen en verzenden
U kunt verkoop- en inkooporders en retourorders verzenden voordat u deze boekt. Facturen en creditnota's kunnen pas worden verzonden nadat u deze hebt geboekt.

In de volgende procedure wordt beschreven hoe u een IC-verkooporder kunt invullen en verzenden. Dezelfde stappen gelden voor IC-inkooporders en -retourorders en voor geboekte IC-facturen en -creditnota's.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Kies **Nieuw** om een nieuwe verkooporder te maken. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Controleer of de klant een IC-partner is.
5. Als u de verkooporder wilt verzenden voordat u hem boekt, kiest u de actie **IC-verkooporder verzenden**.

> [!NOTE]
> Als u stap 4 uitvoert, wordt de verkooporder naar uw IC-outbox verplaatst van waaruit u hem later kunt verzenden. Zie voor meer informatie [De intercompany-inbox en outbox beheren](intercompany-how-manage-intercompany-inbox.md).

## Een IC-dagboek invullen en boeken

Wanneer u een IC--diversendagboekregel boekt in uw bedrijf, wordt een corresponderende dagboekregel gemaakt in uw IC-outbox, die u kunt overbrengen naar uw partner. Met releasewave 1 van 2022 kunt u het bedrijf ook instellen voor het automatisch maken van ontvangen intercompany-transacties van intercompany-partners, geboekt via het intercompany-dagboek. Uw partner kan de bijbehorende transactie vervolgens boeken in zijn bedrijf, zonder de gegevens opnieuw te hoeven invoeren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Intercompany-dagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open de relevante dagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul de vereiste velden in.
4. In het veld **Grootboekrekeningnr. IC-partner** voert u de IC-grootboekrekening in waarop het bedrag wordt geboekt in het bedrijf van uw partner.

    > [!NOTE]
    > Dit veld moet worden ingevuld op een regel met een bankrekening of grootboekrekening in het veld **Rek.-nr.** of in het veld **Tegenrekeningnr.**  
5. Kies de actie **Boeken**.

De betreffende posten worden geboekt in uw bedrijf en een dagboek met de bijbehorende posten wordt gemaakt in uw IC-outbox, die u naar uw partnerbedrijf kunt verzenden. Zie voor meer informatie [De intercompany-inbox en outbox beheren](intercompany-how-manage-intercompany-inbox.md).

## Zie ook

[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]