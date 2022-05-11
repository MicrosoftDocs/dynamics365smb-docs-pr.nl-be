---
title: Documenten en e-mails verzenden
description: U kunt inhoud definiëren die moet worden ingevoegd in het hoofdgedeelte van een e-mailbericht, bijvoorbeeld een PayPal-koppeling. U kunt ook documenten koppelen aan e-mailberichten.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.search.form: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e791eb8f066085b8230aeac4c85a82c67093f06
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655616"
---
# <a name="send-documents-and-emails"></a>Documenten en e-mails verzenden

U kunt eenvoudig informatie en documenten, zoals verkoop- en inkooporders en facturen, rechtstreeks per e-mail delen vanuit [!INCLUDE[prod_short](includes/prod_short.md)], zonder een e-mailapp te hoeven openen.  

U kunt bijna alle soorten documenten als pdf-bijlage verzenden. U kunt ook een rapportlay-out instellen die informatie uit het document in de e-mailtekst bevat, samen met tekst die de e-mail vriendelijker maakt, bijvoorbeeld een standaardbegroeting. Zie voor meer informatie [Lay-outs van rapporten en documenten beheren](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Wanneer u facturen verzendt, kunt u het klanten gemakkelijker maken om betalingen te doen via een betalingsservice, zoals PayPal, door automatisch informatie en een link naar de service in de e-mail toe te voegen. Zie [Klantbetalingen via betalingsservices inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.

Als u e-mails vanuit [!INCLUDE[prod_short](includes/prod_short.md)] wilt inschakelen, start u de begeleide instelling **E-mail instellen**. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt alleen uitgaande e-mailcommunicatie. U kunt ook geen antwoorden ontvangen vanuit de app.

## <a name="to-send-documents-by-email"></a>Documenten per e-mail verzenden

In deze procedure wordt beschreven hoe een geboekte verkoopfactuur als pdf-bestand en met documentspecifieke e-mailtekst aan een e-mail wordt toegevoegd. <!--update this-->

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de factuur en kies de actie **Afdrukken/Verzenden** en kies vervolgens **Verzenden**.
3. Kies in het veld **E-mail** **Ja (prompt voor instellingen)**. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.
    
    Als het veld **E-mail** op de pagina **Document verzenden naar** is ingesteld op **Ja (prompt voor instellingen)**, wordt de pagina **E-mail verzenden** geopend en vooraf gevuld met de contactpersoon in het veld **Aan:** en het document is als een pdf-bestand bijgevoegd. In het veld **Hoofdtekst** kunt u tekst handmatig invoeren of kunt u in het veld een documentspecifieke e-mailhoofdtekst invoeren die u hebt ingesteld.

4. Kies de knop **OK**.
5. Voer in het veld **Aan** een geldig e-mailadres. De standaardwaarde is het e-mailadres van de klant.
6. Voer in het veld **Onderwerp** een beschrijvende onderwerptekst in. De standaardwaarde is de naam van de klant en het factuurnummer.
7. In het veld **Bijlage** wordt de gegenereerde factuur standaard gekoppeld als een PDF-bestand.
8. Voer in het veld **Hoofdgedeelte** een kort bericht aan de ontvanger in.

    Als een documentspecifieke e-mailtekst is ingesteld op de pagina **Rapportselectie - Verkoop**, wordt het veld **Hoofdtekst** automatisch ingevuld. Zie voor meer informatie [Herbruikbare e-mailteksten en lay-outs instellen voor verkoop- en inkoopdocumenten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents).
9. Kies de knop **OK** om het e-mailbericht te verzenden.

> [!NOTE]  
> Als u geen e-mailinstellingen wilt opgeven telkens wanneer u een document e-mailt, kunt u de optie **Ja (standaardinstellingen gebruiken)** in het veld **E-mail** van de pagina **Document verzenden naar** selecteren. In dat geval wordt de pagina **E-mail verzenden** niet geopend. Zie stap 4. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.  

## <a name="to-compose-and-send-an-email"></a>Een e-mail opstellen en verzenden
U kunt snel e-mails opstellen voor contactpersonen, klanten, leveranciers, verkopers/inkopers en bankrekeningen, rechtstreeks vanaf de pagina's voor die entiteiten. Kies gewoon **Verwerken** en dan **E-mail verzenden** om de e-maileditor te openen. Voor bankrekeningen bevindt de actie **E-mail verzenden** zich onder **Acties**.

> [!TIP]
> Als u vaak e-mailberichten verstuurt die vergelijkbaar zijn, of een bulkcommunicatie wilt verzenden, bijvoorbeeld om reclame te maken voor een verkoopcampagne, kan het gebruik van Word-sjablonen met e-mail het proces versnellen. U kunt een sjabloon maken voor entiteiten zoals klanten, leveranciers en contactpersonen, die de inhoud van een e-mailbericht voor u zal genereren, en zelfs de inhoud voor de ontvanger personaliseren op basis van gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Word-sjablonen gebruiken voor bulkcommunicatie](ui-mail-merge.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Documenten gemarkeerd als afgedrukt wanneer ze worden verzonden

Sommige documenten in [!INCLUDE[prod_short](includes/prod_short.md)] hebben een veld dat aangeeft hoe vaak het document is afgedrukt. Het nummer in dat veld <!--"that field?" need a name...--> wordt ook bijgewerkt als u het document per e-mail verstuurt, omdat er een pdf-bestand voor wordt gegenereerd. Het nummer wordt bijgewerkt, zelfs als u de e-mail niet verzendt. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>Verzonden e-mails en uw e-mailpostvak

[!INCLUDE[prod_short](includes/prod_short.md)] slaat de e-mails die u verzendt, op de pagina **Verzonden items** op. Dat is om u e-mails opnieuw te laten verzenden of door te sturen naar iemand anders. Als u geen e-mail kunt vinden in uw verzonden items, zoekt u deze op de pagina **E-mail-outbox**. 

> [!NOTE]
> Afhankelijk van de extensie die uw bedrijf gebruikt voor e-mail, kunnen beheerders een lijst zien met berichten die iedereen heeft verzonden, maar niet de inhoud van de berichten

In de **E-mailoutbox** vindt u de e-mails die u als concept hebt opgeslagen en e-mails die niet konden worden verzonden, bijvoorbeeld als het e-mailadres ongeldig was. Voor berichten die niet zijn verzonden, kunt u **Fout weergeven** of **Fout onderzoeken** kiezen om het probleem op te lossen.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Zie ook

[Rapport- en documentlay-outs beheren](ui-manage-report-layouts.md)  
[E-mail instellen](admin-how-setup-email.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
