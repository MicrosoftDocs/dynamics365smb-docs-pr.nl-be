---
title: Digitale bonnen instellen
description: In dit artikel wordt uitgelegd hoe u afgedwongen digitale bonnen in Microsoft Dynamics 365 Business Central instelt en gebruikt.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# <a name="set-up-digital-vouchers"></a>Digitale bonnen instellen

Beheerders kunnen de digitale bonnenfunctionaliteit gebruiken om te vereisen dat documenten aan specifieke transacties worden toegevoegd wanneer ze worden geboekt. Deze functionaliteit maakt daarom een brongestuurde aanpak mogelijk en zorgt voor een beter controletraject. Hiervoor kunnen verschillende soorten handhaving worden geconfigureerd, afhankelijk van de document- of journaaltypes.

De term *digitale bon* verwijst naar een digitale of elektronische vorm van een traditionele bon in de boekhouding. Een bon is een document dat wordt gebruikt ter ondersteuning en autorisatie van financiële transacties. In de boekhouding dient een bon doorgaans als bewijs van een uitgave of ontvangst van geld. De bon kan details bevatten zoals de datum van de transactie, een beschrijving, het bedrag en eventuele handtekeningen voor autorisatie.

> [!IMPORTANT]
> In sommige landen/regio's is het mogelijk dat u bepaalde opties niet kunt configureren, omdat specifieke instellingen mogelijk wettelijk verplicht zijn. Als u met deze beperkingen te maken krijgt, kijk dan voor een gedetailleerde uitleg op de documentatiepagina voor uw land/regio.

## <a name="enable-digital-vouchers"></a>Digitale bonnen inschakelen

Volg deze stappen om de digitale bonnenfunctionaliteit in te schakelen.

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Digitale bonnen instellen** in en selecteer vervolgens de gerelateerde koppeling.
2. Schakel het selectievakje **Geactiveerd** in.

## <a name="set-up-digital-vouchers-1"></a>Digitale bonnen instellen

Voor de volgende documenten en dagboeken kunt u verschillende instellingen gebruiken.

| Boekingssoort | Omschrijving |
|------------|-------------|
| Verkoopdocument | Specificeert boekingen die zijn voltooid vanuit verkoopdocumenten. |
| Inkoopdocument | Specificeert boekingen die zijn voltooid vanuit inkoopdocumenten. |
| Financieel dagboek | Specificeert boekingen die zijn voltooid vanuit het dagboek voor alle rekeningtypen, behalve die verband houden met de klant en leverancier. Als u een van deze rekeningtypen selecteert, wijzigt u de controle over het boekingsproces. Als u **Klant** selecteert als rekeningtype, controleert het systeem uw instellingen die verband houden met het verkoopdagboek. Als u **Leverancier** selecteert als rekeningtype, controleert het systeem uw instellingen die verband houden met het inkoopdagboek. |
| Verkoopdagboek | Specificeert de boekingen die vanuit het verkoopdagboek en het dagboek zijn voltooid, waarbij **Klant** is geselecteerd als rekeningtype. |
| Inkoopdagboek | Specificeert de boekingen die vanuit het inkoopdagboek en het dagboek zijn voltooid, waarbij **Leverancier** is geselecteerd als rekeningtype. |

Volg deze stappen om te definiëren hoe uw organisatie afgedwongen digitale bonnen gebruikt.

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Invoer van digitale bonnen instellen** in en selecteer vervolgens de gerelateerde koppeling. Of selecteer op de pagina **Digitale bonnen instellen**, **Invoer instellen**.
2. Selecteer in de kolom **Postsoort** een optie.
3. Selecteer in de kolom **Chequesoort** een afdwingingsoptie. Als u **Geen** selecteert, kunt u het geselecteerde type post boeken zonder digitale bon. Als u **Bijlage** selecteert, moet de post een bijlage bevatten. Als u **Bijlage of notitie** selecteert, kunt u een bijlage of een notitie bij de post voegen. 
4. Selecteer het selectievakje **Automatisch genereren** om de digitale bon automatisch te genereren. Als u bijvoorbeeld niet handmatig een verkoopfactuur aan uw transactie wilt toevoegen, schakelt u dit selectievakje in. Vervolgens hoeft u alleen maar het document te boeken. Het systeem maakt automatisch het document op basis van uw rapportindeling en voegt het toe aan de transactie.
5. Selecteer het selectievakje **Overslaan indien handmatig toegevoegd** als u geen automatisch gegenereerde digitale bon wilt toevoegen als de gebruiker al een handmatige bijlage heeft toegevoegd.

### <a name="use-source-codes-for-setup"></a>Broncodes gebruiken voor de instelling

Als u afdwinging voor dagboeken wilt gebruiken, maar niet voor alle transactietypen, verbindt u de specifieke broncode om het posttype te identificeren in het dagboek, het verkoopdagboek of het inkoopdagboek.

Volg deze stappen om specifieke broncodes voor digitale bonnen in te stellen.

1. Selecteer op de pagina **Invoer van digitale bonnen instellen** **Broncodes**.
2. Selecteer op de pagina **Broncodes voor boninvoer** de broncodes die u wilt configureren.
3. De pagina sluiten.

## <a name="use-the-functionality"></a>De functionaliteit gebruiken

Open een inkoop- of verkoopdocument en voer informatie in de vereiste velden in. Voordat u het document boekt, moet u deze stappen volgen om een digitale bon bij te voegen.

1. Selecteer in het feitenblok **Inkomende documentbestanden** **Bestand koppelen**.
2. Sleep een bestand rechtstreeks naar de pagina **Bestand invoegen** of blader naar het bestand vanaf deze pagina.

Het document wordt gekoppeld aan het feitenblok **Inkomende documentbestanden**. Voor elke regel kunt u de documentnaam en het documenttype vinden.

Als u per ongeluk de verkeerde bon bijvoegt, volgt u deze stappen om deze te verwijderen voordat u het document boekt.

1. Selecteer in het feitenblok **Inkomende documentbestanden** vanaf de documentregel **Inkomend document**.
2. Selecteer op de pagina **Inkomend document** **Verwijderen**.

> [!NOTE]
> Als het bijvoegen van een digitale bon als verplicht is geconfigureerd en u documenten of dagboeken probeert te boeken zonder een bon bij te voegen, voorkomt het systeem dat u kunt boeken. U ontvangt de volgende foutmelding: "Boeken zonder een digitale bon bij te voegen is niet mogelijk".

### <a name="find-attached-vouchers-in-transactions"></a>Bijgevoegde bonnen vinden in transacties

U kunt de bijgevoegde bon vinden vanuit het geboekte document of op de pagina **Grootboekposten** door te kijken in het feitenblok **Inkomende documentbestanden**.

U kunt een bijgevoegd document niet verwijderen nadat het boeken is voltooid. U kunt echter meer bijlagen toevoegen nadat het boeken is voltooid.

## <a name="see-also"></a>Zie ook

[Financieel beheer](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
