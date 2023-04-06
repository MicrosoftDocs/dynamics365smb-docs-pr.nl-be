---
title: De intercompany-inbox en outbox beheren
description: 'Intercompany-transacties (IC-transacties) die u ontvangt van uw IC-partners worden weergegeven in de IC-inbox, waar u ze handmatig of automatisch verwerkt.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.date: 03/09/2022
ms.author: edupont
---
# De intercompany-inbox en outbox beheren
Alle IC-transacties die u via elektronische weg ontvangt van uw IC-partners, worden weergegeven in de IC-inbox.  

Afhankelijk van hoe intercompany is ingesteld voor uw bedrijf, worden sommige transacties echter automatisch gerepliceerd naar de relevante intercompany-partners. Vanaf releasewave 1 van 2022 kunt u het bedrijf instellen voor het automatisch maken van ontvangen intercompany-transacties van intercompany-partners, geboekt via het intercompany-dagboek. Zie [Een IC-dagboek invullen en boeken](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal) voor meer informatie.  

## De IC-inbox ordenen  
 Met de filtervelden boven aan de inboxpagina kunt u bepalen welke transacties worden weergegeven op de pagina. Als u bijvoorbeeld alleen transacties wilt weergeven die door een bepaalde partner zijn gemaakt, kunt u filtercriteria invoeren in de filters **Transactiebron** en **IC-partnercode**.  

### Transactiebron  
Wat u met een transactie kunt doen, hangt af van het volgende:  

- Transactie gemaakt door uw IC-partner  
- Transactie geweigerd door uw IC-partner en aan u geretourneerd  

Met het veld **Transactiebron weergeven** kunt u de pagina **IC-inboxtransacties** filteren, zodat maar een van deze soorten transacties wordt weergegeven. U kunt ook filteren op IC-partner of op de inhoud van het veld **Regelactie**.  

#### Transactie gemaakt door IC-partner  
 Wanneer u een nieuwe transactie ontvangt die door uw partner is gemaakt, kunt u ervoor kiezen:

- De transactie te accepteren  
- De transactie te weigeren (en aan de partner te retourneren)  
- De transactie te annuleren (de transactie verwijderen en niet retourneren aan uw partner)  

#### Geretourneerd door IC-partner  
 Als de transactie is geweigerd door uw IC-partner, hebt u geen andere keuze dan de transactie in de inbox te annuleren. Vervolgens moet u correctieregels maken of het dagboek of document in uw bedrijf tegenboeken.  

## Inboxitems opnieuw maken  
 Als u een transactie in uw inbox hebt geaccepteerd maar het document of dagboek vervolgens hebt verwijderd in plaats van geboekt, kunt u het inboxitem opnieuw maken en het nogmaals accepteren.  

## Een overzicht weergeven van IC-transacties voor een bepaalde periode  
 U kunt een overzicht weergeven van alle IC-transacties die u in een bepaalde periode hebt verzonden en ontvangen. In de lijst **IC-transacties** worden alle IC-grootboekposten, klantenposten en leveranciersposten weergegeven.

 > [!NOTE]  
 > Als de IC-partners in dezelfde database zijn opgenomen, worden de transacties verzonden zonder dat een bestand of e-mail nodig is. Zie het veld **Overdrachttype** op de pagina **IC-partner**. <br /><br />
In dat geval, kunt u in het systeem instellen om de inbox en de outbox over te slaan, door respectievelijk het selectievakje **Transacties automatisch accepteren** op de pagina **IC-partner** en het selectievakje **Transacties automatisch verzenden** op de pagina **IC-instellingen** in te schakelen. Inkomende intercompany-transacties kunnen alleen automatisch worden geaccepteerd als de taakplanner is ingeschakeld. Zie [Business Central Server configureren - Taakplannerinstellingen](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task) voor meer informatie.

## IC-transacties importeren uit een bestand

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Als u een IC-partner hebt die zich niet in dezelfde database bevindt als uw bedrijf, kunt u IC-transacties van die partner ophalen in een XML-bestand. Vervolgens moet u de transacties importeren in uw inbox.  

1. Sla het bestand op naar de locatie die u hebt opgegeven in het veld **Details IC-inbox** als u intercompany instelt.  
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **IC-inboxtransacties** in en kies de gerelateerde koppeling.
3. Kies op de pagina **IC-inboxtransacties** de actie **Transactiebestand importeren**.  
4. Selecteer op de pagina die wordt geopend het .xml-bestand dat de transacties bevat en klik vervolgens op **Openen**.  

De transacties worden geïmporteerd in de inbox en u kunt ze nu verwerken.

## Inkomende IC-transacties verwerken  
Wanneer uw IC-partners u IC-transacties toesturen, komen de transacties terecht in uw IC-inbox. U moet elke transactie in uw inbox evalueren en verwerken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-inboxtransacties** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **IC-inboxtransacties** een regel en kies een actie om de regel te verwerken, zoals bijvoorbeeld **Goedkeuren**.
3. Vul op de pagina **Bewerking IC-inbox voltooien** de velden in met de benodigde gegevens. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de knop **OK**.  

Bij regels die u verwerkt met de actie **Goedkeuren**, worden document- of dagboekregels aangemaakt in uw bedrijf. Open elk document of dagboek, breng de gewenste wijzigingen aan en boek de regels.  

De regels die u verwerkt met de actie **Retour naar partner** worden verplaatst naar de IC-outbox, vanwaar u ze naar uw partner kunt verzenden.

Voor regels die u verwerkt met de actie **Retour door partner** moet u nu een correctie boeken op de oorspronkelijke transactie die u boekte in uw bedrijf.

## Uitgaande IC-transacties verwerken  
Wanneer u een IC-dagboek of -document boekt of een IC-orderbevestiging verzendt, worden de transacties verzonden naar uw IC-outbox. Als u deze wilt doorsturen naar uw IC-partners, moet u de outbox openen en de transacties verwerken.  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **IC-outboxtransacties** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **IC-outboxtransacties** een regel en kies een actie om de regel te verwerken, zoals bijvoorbeeld **Terug naar inbox**.

Regels die u verwerkt met de actie **Verzenden naar IC-partner** worden verzonden naar de inbox van de betreffende partner.

De regels die u verwerkt met de actie **Terug naar inbox** worden naar de inbox verplaatst, waar u ze kunt goedkeuren om documenten of dagboekregels in uw bedrijf te maken.  

Voor regels die u verwerkt met de actie **Annuleren** moet u nu een correctie boeken op de oorspronkelijke transactie die u boekte in uw bedrijf.  

## IC-inboxtransacties opnieuw maken  
Het kan voorkomen dat u een transactie in de inbox of outbox opnieuw wilt maken. Als u een transactie in uw inbox bijvoorbeeld hebt geaccepteerd maar het document of dagboek vervolgens hebt verwijderd in plaats van geboekt, kunt u de inboxpost opnieuw maken en deze nogmaals accepteren.  

In de volgende procedure wordt beschreven hoe u inboxtransacties opnieuw kunt maken. De procedure voor de outbox is hetzelfde.

  1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verwerkte IC-inboxtransacties** in en kies de gerelateerde koppeling.  

  2.  Open de pagina **Verwerkte IC-inboxtransacties**, selecteer de regel met de transactie die u opnieuw wilt maken in de inbox en selecteer de actie **Inboxtransacties opnieuw maken**.  

## Zie ook
[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
