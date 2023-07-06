---
title: IC-documenten en -dagboeken boeken
description: In dit onderwerp wordt uitgelegd hoe u IC-documenten of -dagboeken gebruikt om transacties met uw IC-partners te boeken.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals"></a><a name="work-with-intercompany-documents-and-journals"></a><a name="work-with-intercompany-documents-and-journals"></a>Werken met intercompany-documenten en -dagboeken

Gebruik IC-documenten of -dagboeken om transacties met uw IC-partners te boeken. U kunt transacties naar grootboekrekeningen boeken en als u intercompany-bankrekeningen hebt ingesteld, kunt u ook bank-naar-banktransacties boeken. Ga voor meer informatie over het instellen van intercompany-bankrekeningen naar [De bankrekeningen opgeven die moeten worden gebruikt voor intercompany-partners](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Wanneer u een IC-document of -dagboekregel boekt in uw bedrijf, wordt een corresponderend document of dagboekregel gemaakt in uw IC-outbox. U zet de regel over van uw outbox naar uw partner. Uw partner kan de bijbehorende transactie vervolgens boeken in zijn bedrijf, zonder de gegevens opnieuw te hoeven invoeren.

Voor verkoop- en inkoopdocumenten zorgt de IC-partnercode voor de klant of leverancier ervoor dat alle orders en facturen voor transacties tussen de partners corresponderende documenten produceren in de partnerbedrijven. De bedrijfsrekeningen zijn correct in balans.

Hetzelfde geldt voor intercompany-dagboekregels. U hoeft geen accounts op te geven, u kiest simpelweg het partnerbedrijf. De bijbehorende intercompany-dagboekregels worden vervolgens aangemaakt in het partnerbedrijf.

## <a name="fill-in-and-send-an-intercompany-sales-order"></a><a name="fill-in-and-send-an-intercompany-sales-order"></a><a name="fill-in-and-send-an-intercompany-sales-order"></a>Een IC-verkooporder invullen en verzenden

U kunt verkoop- en inkooporders en retourorders verzenden voordat u deze boekt. Facturen en creditnota's kunnen pas worden verzonden nadat u deze hebt geboekt.

In de volgende procedure wordt beschreven hoe u een IC-verkooporder kunt invullen en verzenden. Dezelfde stappen gelden voor IC-inkooporders en -retourorders en voor geboekte IC-facturen en -creditnota's.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Kies **Nieuw** om een nieuwe verkooporder te maken. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Controleer of de klant een IC-partner is.
5. Als u de verkooporder wilt verzenden voordat u hem boekt, kiest u de actie **IC-verkooporder verzenden**.

> [!NOTE]
> Als u stap 5 uitvoert, gaat de verkooporder naar uw IC-outbox, van waaruit u deze later kunt verzenden. Ga voor meer informatie over de IC-inbox en outbox naar [De intercompany-inbox en outbox beheren](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal"></a><a name="fill-in-and-post-an-intercompany-journal"></a><a name="fill-in-and-post-an-intercompany-journal"></a>Een IC-dagboek invullen en boeken

Wanneer u een IC--diversendagboekregel boekt in uw bedrijf, wordt een corresponderende dagboekregel gemaakt in uw IC-outbox, die u kunt overbrengen naar uw partner. Met releasewave 1 van 2022 kunt u het bedrijf ook instellen om automatisch ontvangen intercompany-transacties te maken die partners in intercompany-dagboeken hebben geboekt. Uw partner kan de bijbehorende transactie vervolgens boeken in zijn bedrijf, zonder de gegevens opnieuw te hoeven invoeren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Intercompany-dagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open de dagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. In het veld **Grootboekrekeningnr. IC-partner** voert u de IC-grootboekrekening in waarop het bedrag wordt geboekt in het bedrijf van uw partner.

    > [!NOTE]
    > Dit veld moet worden ingevuld op een regel met een bankrekening of grootboekrekening in het veld **Rek.-nr.** of in het veld **Tegenrekeningnr.**  
5. Kies de actie **Boeken**.

De betreffende posten worden geboekt in uw bedrijf en een dagboek met de bijbehorende posten wordt gemaakt in uw IC-outbox, zodat u deze naar uw partnerbedrijf kunt verzenden.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
