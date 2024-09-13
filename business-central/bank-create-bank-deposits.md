---
title: Bankdeposito's aanmaken
description: U kunt stortingen doen om een transactierecord bij te houden die informatie bevat die kan worden toegepast op openstaande facturen en creditnota's.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'bank, deposit'
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 08/29/2024
ms.custom: bap-template
---

# <a name="create-bank-deposits"></a>Bankdeposito's aanmaken

> [!NOTE]
> De mogelijkheid om bankdeposito's aan te maken is nieuw in [!INCLUDE [prod_short](includes/prod_short.md)] 2022 releasewave 1 voor veel land-/regioversies. Als u  [!INCLUDE [prod_short](includes/prod_short.md)] vóór die release in de Verenigde Staten, Canada of Mexico gebruikte, maakt u mogelijk gebruik van de eerdere mogelijkheden. U kunt doorgaan, maar in een toekomstige release zullen de nieuwe mogelijkheden de oude vervangen. Als u de nieuwe functies die in dit artikel worden beschreven wilt gaan gebruiken, kan uw beheerder naar de pagina **Functiebeheer** gaan en **Functie-update: Gestandaardiseerde bankreconciliatie en -stortingen** inschakelen.  

Gebruik de pagina **Bankstortingen** om stortingen te registreren als een enkel document waarmee een of meer posten naar een bankrekening wordt geboekt. Meestal worden bankstortingen gebruikt om contante stortingen te registreren. De pagina Bankstortingen is beschikbaar in het menu **Kasbeheer** menu in het Rolcentrum bedrijfsmanager en andere rolcentra die zich bezighouden met kasbeheer.

Bedragen op bankdeposito's kunnen uit verschillende bronnen afkomstig zijn:

* Verkoop, met behulp van een grootboekrekening voor inkomsten.
* Klantbetalingen.
* Contante terugbetalingen van leveranciers of contante betalingen aan hen. 

Bankstortingsregels bevatten informatie over individuele stortingen, zoals cheques van klanten. Het totaal van de bedragen op de regels moet overeenkomen met het totaalbedrag van de storting.

Nadat u de stortingsinformatie en regels hebt ingevuld, moet u deze boeken. Bij het plaatsen worden de relevante grootboeken bijgewerkt, inclusief grootboek, en de bank-, klant- en leveranciersgrootboeken. Geboekte stortingen worden opgeslagen voor toekomstig gebruik op de pagina **Geboekte bankstortingen**.

Het rapport **Bankstorting** geeft de stortingen van klanten en leveranciers weer met het oorspronkelijke stortingsbedrag, het bedrag van de storting dat nog openstaat en het toegepaste bedrag. Het rapport toont ook het totale geboekte stortingsbedrag dat moet worden gereconcilieerd.

## <a name="before-you-start"></a>Voordat u begint

Er zijn enkele zaken die moeten worden ingesteld voordat u bankstortingen kunt gebruiken. U moet een nummerreeks en een dagboeksjabloon bij de hand hebben. U moet ook aangeven of u bankstortingen als een lump-sum bedrag wilt boeken. Dat wil zeggen, als een totaal van alle bedragen op de stortingsregels. Anders wordt elke regel als een afzonderlijke post geboekt. Het boeken van een storting als een enkele bankpost kan het gemakkelijker maken om bankreconciliatie uit te voeren.

### <a name="number-series-and-lump-sum-deposits"></a>Nummerreeksen en lump-sum stortingen

U moet een nummerreeks instellen voor bankstortingen en vervolgens de reeks opgeven in het veld **Bankstortingnrs.** op de pagina **Verkoopinstellingen**. Ga voor meer informatie over nummerreeksen naar [Nummerreeksen maken](ui-create-number-series.md).

Ook op de pagina **Verkoopinstellingen** zet u de schakelaar **Bankstortingen als lump-sum boeken** aan om stortingen te boeken als lump-sum bedragen in plaats van als afzonderlijke regels. Door een storting als een lump-sum bedrag te boeken wordt één bankpost voor het volledige bedrag van de storting wordt gemaakt, waardoor het gemakkelijker wordt om bankreconciliatie uit te voeren.

### <a name="general-journal-templates-for-bank-deposits"></a>Grootboeksjablonen voor bankstortingen

U moet ook een dagboeksjabloon voor stortingen maken. Met dagboeken kunt u naar grootboek-, bank-, klant- en leveranciersrekeningen en rekeningen voor vaste activa boeken. De dagboeksjablonen ontwerpen het dagboek dat past bij het doel van uw werk. Dat wil zeggen, de velden in de journaalsjabloon zijn precies de velden die u nodig hebt.

De stortingen zijn kasontvangsten, dus u wilt uw nummerreeks wellicht opnieuw gebruiken voor kasontvangstenjournalen. Als u onderscheid wilt maken tussen journaalboekingen van bankstortingens en kasontvangsten, kunt u ook een andere nummerreeks gebruiken.

U moet ook een batchtaak voor de sjabloon maken. Als u een batchtaak wilt maken, gaat u naar de pagina **Fin. dagboeksjablonen** en kiest u de actie **Batches**. Ga voor meer informatie over batches naar [Journaalsjablonen en batches gebruiken](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines"></a>Dimensies op bankstortingsregels

De regels op de bankstorting gebruiken de standaardafmetingen die u hebt opgegeven in de velden  **Afdelingscode** en  **Klantgroepcode** . Wanneer u  **Klant** of **Leverancier** selecteert in het veld **Accounttype**, vervangen de dimensies voor de klant of leverancier de standaardwaarden. U kunt indien nodig de dimensies op de regels wijzigen.

> [!TIP]
> Dimensie op regels worden ingesteld volgens de standaarddimensieprioriteiten. Regeldimensies hebben voorrang boven kopdimensies. U kunt conflicten voorkomen door regels te maken die prioriteit geven aan het gebruik van een dimensie, afhankelijk van de bron. Als u wilt wijzigen hoe de prioriteiten voor dimensies worden vastgesteld, kunt u hun rangschikking wijzigen op de pagina **Standaarddimensieprioriteiten**. Zie [Standaarddimensieprioriteiten instellen](finance-dimensions.md#to-set-up-default-dimension-priorities) voor meer informatie.

## <a name="create-a-bank-deposit"></a>Een bankstorting maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Bankstortingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Nieuw** om de pagina **Bankstorting** te openen.
3. Kies de dagboeksjabloon die u voor bankstortingen hebt gemaakt.  

    > [!NOTE]
    > Als de dagboeksjabloon meer dan één batch heeft, wordt u gevraagd er een te kiezen.

4. Selecteer in het veld **Bankrekeningnr.** de bankrekening waar de storting wilt doen.

    > [!TIP]
    > U kunt controleren of u geld op de juiste rekening stort met behulp van de acties **Bankrekeningkaart** en **Bankposten** om de grootboekposten voor de geselecteerde bankrekening op te zoeken. Bijvoorbeeld om te zien of er soortgelijke stortingen op de rekening zijn gedaan.

5. Voer in het veld **Totaal stortingsbedrag** het totale bedrag van de storting in. Dit totaal moet de som zijn van de bedragen op alle regels.
6. Vul indien nodig de resterende velden in. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    De datum in het veld  **Boekingsdatum**  en de dimensies in de velden  **Afdelingscode** en  **Klantengroepcode**  worden toegewezen aan de regels die u voor de bankstorting maakt. U kunt deze indien nodig wijzigen.

7. Afhankelijk van of u de bankstorting als lump-sum bedrag of elke regel afzonderlijk naar het bankboek wilt boeken, zet u de schakelaar **Boeken als lump-sum** aan of uit. De standaardinstelling komt van dezelfde schakelaar op de pagina **Verkoopinstellingen**.

    > [!NOTE]
    > Het veld **Valutacode** geeft de valuata aan die is opgegeven voor de gekozen bankrekening. U kunt geen andere valuta kiezen.

8. Maak op het sneltabblad **Regels** een nieuwe regel voor elke contante storting die u wilt doen.
9. Geef in het veld **Rekeningsoort** op waar de betaling vandaan komt. Voor bankstortingen is de soort doorgaans **Klant** of **Leverancier**.

    > [!NOTE]
    > U kunt ook een contante betaling aan een leverancier registreren. Kies hiervoor **Leverancier** en voer daarna het betalingsbedrag in als een negatief getal in het veld **Creditbedrag** op de regel.

10. Voer in het veld **Documentnr.** het documentnummer in op de factuur met het creditbedrag. U kunt voor elke regel een documentnummer gebruiken, of hetzelfde nummer voor alle regels.

    > [!TIP]
    > Normaal gesproken hoeft u het veld **Documentsoort** niet in te vullen voor financiële boekingen. Als u bijvoorbeeld contant geld stort uit een dagverkoop, laat u het veld leeg. Als u contant geld stort van een klantbetaling, kiest u **Betaling**.

11. Als u een contante storting uitvoert voor een specifieke klantfactuur, kiest u de actie **Posten vereffenen** en voert u vervolgens het factuurnummer in het veld **Vereffenings-id** in.
12. Als u gereed bent om de bankstorting te boeken, kiest u de actie **Boeken**.

    > [!NOTE]
    > Als de bankrekening standaarddimensies heeft waarbij het veld  **Waardeboeking**  **Code verplicht**, **Zelfde code** of **Geen code** bevat, moet u de storting boeken als een bedrag ineens. Als u niet in één keer boekt, kan het boeken mislukken omdat de dimensiewaarden van de rekeningen op de bankdepositoregels de regels voor het boeken van de waarde van de bankrekening schenden.

    > [!TIP]
    > Voordat u de storting verricht, kunt u de actie  **Testrapport** gebruiken om uw gegevens te controleren. In het rapport wordt aangegeven of er problemen zijn, zoals ontbrekende gegevens, waardoor het plaatsen van berichten onmogelijk is.  

## <a name="find-posted-bank-deposits"></a>Geboekte bankstortingen zoeken

De pagina **Geboekte bankstortingen** toont de eerdere stortingen van uw bedrijf. In de lijst kunt u de opmerkingen en dimensies bekijken die bij de stortingen zijn opgegeven. U kunt de bankstorting openen om meer details te bekijken, en van daaruit kunt u verder onderzoek doen. Zo kunt u bijvoorbeeld de actie **Posten zoeken** kiezen om de geboekte bankposten te bekijken. Vanuit de bankpost kunt u de bijbehorende geboekte grootboekpost vinden.

Als u alle grootboekposten voor de geboekte stortingsregels wilt opzoeken, gaat u naar de pagina **Grootboekjournaal** en gebruikt u de actie **Grootboek**. De actie toont alle grootboek-vermeldingen, inclusief de vermeldingen voor klanten en leveranciers.

## <a name="reverse-a-posted-bank-deposit"></a>Een geboekte bankstorting tegenboeken

Er zijn een aantal manieren om een geboekte bankstorting terug te boeken:

* Kies op de pagina **Geboekte bankstortingen** de storting en kies vervolgens de actie **Boeking ongedaan maken**.
* Zoek op de pagina **Grootboekjournalen** het register voor de storting en kies vervolgens de actie **Journaal tegenboeken**.

> [!NOTE]
> U kunt alleen een register tegenboeken dat een enkele type posten bevat. Dat wil zeggen dat het register alleen klantgegevens of leveranciersgegevens mag bevatten, maar niet beide. Als een register beide bevat, moet u de storting handmatig tegenboeken.

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[Financiën instellen](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]



