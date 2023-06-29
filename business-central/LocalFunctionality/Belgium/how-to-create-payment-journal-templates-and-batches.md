---
title: 'Betalingsdagboeksjablonen en -batches maken [BE]'
description: In de Belgische versie worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. Het betalingsdagboek lijkt op de structuur van andere dagboeksoorten.
author: SorenGP
ms.topic: conceptual
ms.search.form: '256, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="create-payment-journal-templates-and-batches-in-the-belgian-version"></a><a name="create-payment-journal-templates-and-batches-in-the-belgian-version"></a>Betalingsdagboeksjablonen en -batches maken in de Belgische versie

In [!INCLUDE[prod_short](../../includes/prod_short.md)] worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten. Het betalingsdagboek bevat echter enkele velden die specifiek betrekking hebben op het verwerken van betalingen. Voordat u betalingsvoorstellen kunt genereren, moet u een betalingsdagboeksjabloon en een betalingsdagboekbatch instellen.  

U kunt een specifieke pagina en een testrapport toewijzen aan elke dagboeksjabloon. Hierdoor kunt u uw binnenlandse betalingen en internationale betalingen beheren via deze aangepaste pagina. De opgegeven *broncode* wordt gekopieerd naar alle dagboekregels die worden gemaakt op basis van de dagboeksjabloon. De code wordt ook naar de posten gekopieerd wanneer deze worden geboekt. Zo kunt u altijd zien waar een geboekte post vandaan komt.

Als u een bankrekening toewijst aan de betalingsdagboeksjabloon, wordt de bankrekening ingevoegd in alle betalingsdagboekbatches en betalingsdagboekregels die met deze sjabloon worden gemaakt. Door een bankrekening voor de dagboeksjabloon op te geven, kunt u de benodigde tijd voor het controleren van de betalingsvoorstellen beperken.  

## <a name="to-create-a-payment-journal-template"></a><a name="to-create-a-payment-journal-template"></a>Een betalingsdagboeksjabloon maken

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de velden op de pagina **Betalingsdagboeksjablonen** in.  

    [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Als de velden **Pagina-id** en **Testrapport-id** niet worden weergegeven, moet u deze velden toevoegen via personalisatie. U kunt pas doorgaan als de velden zijn ingevuld. Zie [Uw werkruimte personaliseren](../../ui-personalization-user.md) voor meer informatie.
4. Herhaal stap 2 voor aanvullende sjablonen.

5. Kies de knop **Ok**.  

U kunt onder elke dagboeksjabloon meerdere dagboekbatches instellen. Er kunnen meerdere dagboeken, met verschillende namen, in hetzelfde venster worden weergegeven. Dit is bijvoorbeeld handig wanneer iedere gebruiker een specifiek dagboek moet hebben.

## <a name="to-add-payment-journal-batches-to-the-journal-template"></a><a name="to-add-payment-journal-batches-to-the-journal-template"></a>Betalingsdagboekbatches toevoegen aan de dagboeksjabloon

1. Kies op de pagina **Betalingsdagboeksjablonen** de actie **Batches**.  
2. Vul de velden op de pagina **Betalingsdagboekbatch** in.  

    [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Als de dagboeknaam numeriek moet wordt bijgewerkt, neemt u een nummer op in de dagboekbatchnaam. Zo wordt de waarde in de batchnaam KBC1 bij elke nieuwe boeking verhoogd (KBC2, KBC3, enzovoort).  

    Vervolgens kunt u de configuratie testen. Zie [Elektronische documenten testen](how-to-test-electronic-payments.md) voor meer informatie.  

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Belgische elektronische betalingen](belgian-electronic-payments.md)  
[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md)  
[IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)  
[Dagboeksjablonen verplicht maken](specify-journal-template-mandatory.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
