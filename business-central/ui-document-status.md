---
title: Statusveld in documenten
description: 'Lees meer over de status ''Open'' en ''Vrijgegeven'' op offerte-, order- of creditnotadocumenten.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# Statusveld in documenten

Wanneer u een offerte, order of creditnota maakt, bevat het veld **Status** in de documentkop standaard de waarde **Open**.

Nadat u het document hebt ingevuld, kunt u het vrijgeven en wordt de waarde in het veld **Status** in [!INCLUDE[prod_short](includes/prod_short.md)] gewijzigd in **Vrijgegeven**. Deze status geeft aan dat de order gereed is voor de volgende verwerkingsfase voordat deze wordt geboekt.

| Status | Omschrijving |
| ------ | ----------- |
| Geopend   | U kunt wijzigingen aanbrengen in het document. |
| Vrijgegeven | Het document is vrijgegeven voor de volgende verwerkingsfase, zodat u geen wijzigingen meer kunt aanbrengen in regels van het type *Artikel* en *Vast activum*.<br /><br />Als u een vrijgegeven document wilt wijzigen, kunt u het opnieuw openen. Als u het document wilt doorgeven voor de volgende verwerkingsfase, moet u het document nogmaals vrijgeven. |
| Wacht op goedkeuring   | Het document moet nog worden goedgekeurd. |
| Wacht op vooruitbetaling | Er is een vooruitbetalingsfactuur geboekt voor het document. |

## Vrijgaveproces

Met het vrijgaveproces kunt u de gewone werkstroom op verschillende manieren gemakkelijker maken, bijvoorbeeld door bedrijfsprocedures over goedkeuring te volgen of magazijnactiviteiten te starten.

### Goedkeuringsprocedures

Met de vrijgaveprocedure kan het bedrijf aangeven dat een andere gebruiker het document heeft goedgekeurd of dat een extern contact kan voldoen aan de specificaties van het document, zoals in de volgende voorbeelden:

* U kunt een verkooporder alleen vrijgeven wanneer de leverancier heeft aangegeven dat de order kan worden uitgevoerd.
* U maakt een order die, mogelijk uit veiligheidsoverwegingen, door een andere gebruiker moet worden goedgekeurd voordat u deze kunt vrijgeven.
* De manager die verantwoordelijk is voor alle terugbetalingen, moet een creditnota vrijgeven die u hebt betaald.

Lees meer over goedkeuringswerkstromen op [Werkstromen gebruiken](across-use-workflows.md).

### Magazijnactiviteiten

Als de orderstatus **Open** is, wordt de verzending niet klaargemaakt en worden de artikelen op een inkooporder niet verwacht in het magazijn. Wanneer u de order vrijgeeft, geeft u aan dat de order volledig is en dat deze in het magazijn kan worden uitgevoerd.

## Een vrijgegeven order opnieuw openen

U moet een vrijgegeven order opnieuw openen als u wijzigingen wilt aanbrengen. U kunt de aantallen op de door het magazijn verwerkte regels echter alleen verhogen.

Wanneer u de wijzigingen aanbrengt en de order opnieuw vrijgeeft, worden de btw en de factuurkorting opnieuw berekend in [!INCLUDE [prod_short](includes/prod_short.md)].

Als u wijzigingen aanbrengt in een vrijgegeven order, moet u het magazijn inlichten over deze wijzigingen.

> [!NOTE]
> Als u een afzonderlijke open order of creditnota wilt boeken zonder deze eerst vrij te geven, wordt het document in [!INCLUDE [prod_short](includes/prod_short.md)] na het boeken automatisch vrijgegeven. Boekt u de orders of creditnota's met de functie **Batchboeken**, dan kunt u ervoor kiezen alleen de orders of creditnota's te boeken die u hebt vrijgegeven.

## Zie ook

[Producten verkopen met een klantverkooporder](sales-how-sell-products.md)  
[Aankopen registreren met inkoopfacturen](purchasing-how-record-purchases.md)  
[Artikelen verzenden](warehouse-how-ship-items.md)  
[Artikelen ontvangen](warehouse-how-receive-items.md)  
[Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md)  
[Lijsten sorteren, doorzoeken en filteren](ui-enter-criteria-filters.md)  
[Documenten archiveren](across-how-to-archive-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
