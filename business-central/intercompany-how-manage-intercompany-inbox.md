---
title: De intercompany-inbox en outbox beheren
description: 'Intercompany-transacties (IC-transacties) die u ontvangt van uw partners worden weergegeven in de IC-inbox, waar u ze handmatig of automatisch verwerkt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>De intercompany-inbox en outbox beheren

De IC-transacties die u via elektronische weg ontvangt van uw IC-partners, worden weergegeven op de pagina **IC-inbox**. Ga naar [Inkomende intercompany-transacties verwerken](#process-incoming-intercompany-transactions) voor meer informatie over het verwerken van inkomende IC-transacties. De IC-transacties die u via elektronische weg naar uw IC-partners verzend, worden weergegeven op de pagina **IC-outbox**. Ga naar [Uitgaande IC-transacties verwerken](#to-process-outgoing-intercompany-transactions) voor meer informatie over het verwerken van uitgaande IC-transacties.

Afhankelijk van uw IC-configuratie worden sommige transacties echter automatisch afgehandeld. U kunt het bronbedrijf en partnerbedrijven zo instellen dat ze automatisch documenten en dagboeken maken die overeenkomen met transacties die partners boeken via het intercompany-dagboek. Ga voor meer informatie over het gebruik van intercompany-dagboeken naar [Een intercompany-dagboek invullen en boeken](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox"></a>De IC-inbox ordenen

Met de filtervelden boven aan de inboxpagina kunt u bepalen welke transacties worden weergegeven op de pagina. Als u bijvoorbeeld alleen transacties wilt verkennen die door een bepaalde partner zijn gemaakt, gebruikt u de filters **Transactiebron** en **IC-partnercode**.  

### <a name="transaction-source"></a>Transactiebron

Wat u met een transactie kunt doen, hangt af van het volgende:  

* Transactie gemaakt door uw IC-partner  
* Transactie geweigerd door uw IC-partner en aan u geretourneerd  

Gebruik het veld **Transactiebron weergeven** om de pagina **IC-inboxtransacties** te filteren, zodat maar een van deze soorten transacties wordt weergegeven. U kunt ook filteren op IC-partner of op de inhoud van het veld **Regelactie**.  

#### <a name="created-by-intercompany-partner"></a>Transactie gemaakt door IC-partner

 Wanneer u een nieuwe transactie ontvangt die door uw partner is gemaakt, kunt u ervoor kiezen:

* De transactie te accepteren  
* De transactie weigeren (en aan de partner te retourneren)  
* De transactie te annuleren (de transactie verwijderen en niet retourneren aan uw partner)  

#### <a name="returned-from-intercompany-partner"></a>Geretourneerd door IC-partner

Als uw IC-partner een transactie weigert, moet u de transactie in de inbox annuleren en vervolgens een correctieregels maken of het dagboek of document in uw bedrijf tegenboeken.  

## <a name="recreating-inbox-entries"></a>Inboxitems opnieuw maken

Als u een transactie in uw inbox hebt geaccepteerd maar het document of dagboek vervolgens hebt verwijderd in plaats van geboekt, kunt u het inboxitem opnieuw maken en het nogmaals accepteren.  

## <a name="get-an-overview-of-intercompany-transactions-for-a-period"></a>Een overzicht van IC-transacties voor een periode krijgen

U kunt een overzicht weergeven van alle IC-transacties die u in een bepaalde periode hebt verzonden en ontvangen. In de lijst **IC-transacties** worden alle IC-grootboekposten, klantenposten en leveranciersposten weergegeven.

> [!NOTE]  
> Als de IC-partners zich in dezelfde database bevinden, kunnen de partners automatisch transacties accepteren. Ga vervolgens direct naar de pagina's **Verwerkte IC-inboxtransacties** en **Verwerkte IC-outboxtransacties**. Ga voor meer informatie over automatisch accepteren van transacties naar [Transacties van intercompany-partners automatisch accepteren](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Schakel op de pagina **Intercompany-instelling** de schakelaar **Transacties automatisch verzenden** in voor de synchronisatiepartner.
> * Schakel op de pagina **IC-partner** de schakelaar **Transacties automatisch accepteren** in voor partnerbedrijven.  

## <a name="import-intercompany-transactions-from-a-file"></a>IC-transacties importeren uit een bestand

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Als u een IC-partner hebt die zich niet in dezelfde database bevindt als uw bedrijf, kunt u IC-transacties van die partner ophalen in een XML-bestand. Vervolgens moet u de transacties importeren in uw inbox.  

1. Sla het bestand op naar de locatie die u hebt opgegeven in het veld **Details IC-inbox** als u intercompany instelt.  
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **IC-inboxtransacties** in en kies de gerelateerde koppeling.
3. Kies op de pagina **IC-inboxtransacties** de actie **Transactiebestand importeren**.  
4. Selecteer op de pagina die wordt geopend het .xml-bestand dat de transacties bevat en klik vervolgens op **Openen**.  

De transacties worden geïmporteerd in de inbox en u kunt ze nu verwerken.

## <a name="process-incoming-intercompany-transactions"></a>Inkomende IC-transacties verwerken

Wanneer uw IC-partners u IC-transacties toesturen, komen de transacties terecht in uw IC-inbox. U moet elke transactie in uw inbox evalueren en verwerken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **IC-inboxtransacties** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **IC-inboxtransacties** een regel en kies een actie om de regel te verwerken, zoals bijvoorbeeld **Goedkeuren**.
3. Vul op de pagina **Bewerking IC-inbox voltooien** de velden in met de benodigde gegevens. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de knop **Ok**.  

Voor regels die u accepteert, worden document- of dagboekregels aangemaakt in uw bedrijf. Open elk document of dagboek, breng de gewenste wijzigingen aan en boek de regels.  

Regels die u afwijst en terugstuurt naar uw partner gaan naar uw IC-outbox, waar u ze naar uw partner kunt sturen.

Voor regels die een partner heeft afgewezen en aan u heeft geretourneerd, moet u een correctie boeken op de oorspronkelijke transactie die u in uw bedrijf hebt geboekt.

## <a name="to-process-outgoing-intercompany-transactions"></a>Uitgaande IC-transacties verwerken

Wanneer u een IC-dagboek of -document boekt of een IC-orderbevestiging verzendt, gaan de transacties naar uw IC-outbox. Om ze naar uw IC-partners te sturen, opent u de outbox en verwerkt u ze.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-outboxtransacties** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **IC-outboxtransacties** een regel en kies een actie om de regel te verwerken, zoals bijvoorbeeld **Terug naar inbox**.

Gebruik de actie **Verzenden naar IC-partner** om regels naar de inbox van de betreffende partner te verzenden.

Gebruik de actie **Terug naar inbox** om regels naar uw inbox te verplaatsen, waar u ze vervolgens kunt accepteren om documenten of journaalregels in uw bedrijf te maken.  

Als u de actie **Annuleren** gebruikt, moet u een correctie boeken op de oorspronkelijke transactie die u boekte in uw bedrijf.  

## <a name="recreate-intercompany-inbox-transactions"></a>IC-inboxtransacties opnieuw maken

Mogelijk wilt u een transactie opnieuw maken in de inbox of outbox. Als u een transactie in uw inbox bijvoorbeeld hebt geaccepteerd maar het document of dagboek vervolgens hebt verwijderd in plaats van geboekt, kunt u de inboxpost opnieuw maken en deze nogmaals accepteren.  

In de volgende procedure wordt beschreven hoe u inboxtransacties opnieuw kunt maken. De procedure voor de outbox is hetzelfde.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verwerkte IC-inboxtransacties** in en kies de gerelateerde koppeling.  
2. Open de pagina **Verwerkte IC-inboxtransacties**, selecteer de regel met de transactie die u opnieuw wilt maken in de inbox en selecteer de actie **Inboxtransacties opnieuw maken**.  

## <a name="see-also"></a>Zie ook

[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
