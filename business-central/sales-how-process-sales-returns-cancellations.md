---
title: Verkoopretouren of annuleringen verwerken
description: 'Beschrijft hoe u een verkoopcreditnota maakt om een retour, een annulering of terugbetaling te verwerken voor artikelen of diensten waarvoor u betaling hebt ontvangen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: edupont
---
# <a name="process-sales-returns-or-cancellations"></a><a name="process-sales-returns-or-cancellations"></a><a name="process-sales-returns-or-cancellations"></a>Verkoopretouren of annuleringen verwerken

Als een klant artikelen wil retourneren of terugbetaling wil krijgen voor artikelen of services die u klant hebt verkocht en waarvoor u een betaling hebt ontvangen, moet u een verkoopcreditnota maken en boeken waarmee de gevraagde wijziging wordt opgegeven. Om de juiste verkoopfactuurgegevens op te nemen kunt u het volgende doen:  

- Maak de verkoopcreditnota rechtstreeks vanuit de geboekte verkoopfactuur.
- Maak een nieuwe verkoopcreditnota met gekopieerde factuurgegevens.

Als u meer controle wilt hebben over het verkoopretourproces, zoals magazijndocumenten voor het hanteren van het artikel of beter overzicht bij het ontvangen van artikelen van meerdere verkoopdocumenten bij één enkele verkoopretourzending, kunt u verkoopretourorders maken. Een verkoopretourorder geeft automatisch de gerelateerde verkoopcreditnota en andere retourgerelateerde documenten uit, zoals een vervangende verkooporder, indien noodzakelijk. Zie [Verkoopretourorders maken](sales-how-process-sales-returns-orders.md) voor meer informatie.

> [!NOTE]  
> Als een geboekte verkoopfactuur nog niet is voldaan, kunt u de functie **Corrigeren** of **Annuleren** voor de geboekte verkoopfactuur gebruiken om transacties tegen te boeken. Deze functies werken alleen voor niet-betaalde facturen en ze ondersteunen geen gedeeltelijke retourneringen of annuleringen. Zie voor meer informatie [Onbetaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md).

Een retour of terugbetaling kan betrekking hebben op slechts enkele artikelen of services op de oorspronkelijke verkoopfactuur. In dat geval moet u de gegevens in de regels van de verkoopcreditnota of de verkoopretourorder bewerken. Wanneer u de verkoopcreditnota of de verkoopretourorder boekt, worden de door de wijziging beïnvloede verkoopdocumenten tegengeboekt en een terugbetaling voor de klant kan worden gemaakt. Zie voor meer informatie [Betalingen doen](payables-make-payments.md).  

De creditnotaboeking draait ook eventuele artikeltoeslagen terug die aan het geboekte document zijn toegewezen, zodat de waardeposten van het artikel hetzelfde zijn als voordat de artikeltoeslag is toegewezen.

> [!NOTE]
> De boekhoudkundige aspecten van verkoopretouren, zoals de betalingen aan klanten als terugbetaling, worden beschouwd als boekhoudkundig werk en worden hier niet beschreven. Zie [Betalingsverplichtingen beheren](payables-manage-payables.md) voor meer informatie.

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Een verkoopcreditnota maken op basis van een geboekte verkoopfactuur

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Geboekte verkoopfacturen** de geboekte verkoopfactuur die u wilt tegenboeken, kies de actie **Annuleren** en kies vervolgens de actie **Corrigerende creditnota maken**.

    De koptekst van de verkoopcreditnota bevat enkele gegevens uit de geboekte verkoopfactuur. U kunt deze gegevens bewerken, bijvoorbeeld met nieuwe gegevens die overeenkomen met de retourovereenkomst.  
3. Bewerk de informatie op de regels volgens de overeenkomst, zoals het aantal geretourneerde artikelen of het terug te betalen bedrag.
4. Kies de actie **Voorbereiden** en kies vervolgens de actie **Posten vereffenen**.
5. Selecteer op de pagina **Klantposten vereffenen** de regel met het geboekte verkoopdocument waarmee u de verkoopcreditnota wilt vereffenen, en kies vervolgens de actie **Vereffenings-id**.

    De id van de verkoopcreditnota is zichtbaar in het veld **Vereffenings-id**.
6. Voer in het veld **Te vereffenen bedrag** het bedrag in dat u wilt vereffenen, als dit lager is dan het oorspronkelijke bedrag.  

    Onder op de pagina **Klantposten vereffenen** ziet u het totale te vereffenen bedrag om alle betrokken posten tegen te boeken, namelijk als de waarde in het veld **Saldo** nul is.
7. Kies de knop **Ok**. Wanneer u de verkoopcreditnota boekt, wordt deze vereffend met de geboekte verkoopdocumenten.

    Nadat u de nodige verkoopcreditnotaregels hebt gemaakt of bewerkt en de enkele of meerdere vereffeningen zijn opgegeven, kunt u de verkoopcreditnota boeken.  
8. Kies de actie **Boeken** en kies vervolgens de actie **Boeken en verzenden**.  

Het dialoogvenster **Boeken en verzenden bevestigen** wordt geopend met de geprefereerde verzendmethode voor de klant. U kunt de verzendmethode wijzigen door de opzoekknop voor het veld **Document verzenden naar** te kiezen. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.  

De geboekte verkoopdocumenten die u op de creditnota hebt vereffend, worden nu tegengeboekt en een terugbetaling kan worden gemaakt voor de klant. De verkoopcreditnota wordt verwijderd en vervangen door een nieuw document in de lijst met geboekte verkoopcreditnota's.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Een verkoopcreditnota maken door een geboekte verkoopfactuur te kopiëren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuwe lege verkoopcreditnota te openen.
3. Voer in het veld **Klantnaam** de naam in van een bestaande klant.
4. Kies de actie **Voorbereiden** en kies vervolgens de actie **Document kopiëren**.
5. Selecteer op de pagina **Verkoopdocument kopiëren** in het veld **Documentsoort** **Geboekte factuur**.
6. Kies het veld **Documentnr.** om de pagina **Geboekte verkoopfacturen** te openen, en selecteer vervolgens de geboekte verkoopfactuurrecord met de regels die u wilt tegenboeken.
7. Schakel het selectievakje **Regels opnieuw berekenen** in als u wilt dat de gekopieerde geboekte verkoopfactuurregels worden bijgewerkt met de wijzigingen in de artikelprijs en kostprijs sinds de factuur is geboekt.
8. Kies de knop **Ok**. De gekopieerde factuurregels worden ingevoegd in de kredietnota van de verkoop.
9. Voltooi de verkoopcreditnota zoals is uitgelegd in [Een verkoopcreditnota maken op basis van een geboekte verkoopfactuur](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-allowance"></a><a name="to-create-a-sales-allowance"></a><a name="to-create-a-sales-allowance"></a>Een verkoopprijskorting maken
U kunt een klant een creditnota sturen met een korting omdat de klant de artikelen bijvoorbeeld met lichte beschadigingen of te laat heeft ontvangen.  
U kunt deze gereduceerde prijs als artikeltoeslag boeken in een creditnota of retourorder en vervolgens toewijzen aan de geboekte verzending. De volgende beschrijving behandelt dit voor een verkoopcreditnota, maar dezelfde stappen zijn van toepassing op een verkoopretourorder.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuwe lege verkoopcreditnota te openen.
3. Vul in de creditnotakop de betreffende gegevens in over de klant aan wie u de verkoopprijskorting wilt geven.  
4. Selecteer **Toeslag (artikel)** in het veld **Soort** op het sneltabblad **Regels**.  
5. Selecteer in het veld **Nr.** de juiste artikeltoeslagwaarde.  
     Mogelijk wilt u een speciaal artikeltoeslagnummer toewijzen voor verkoopprijskortingen.  
6. Geef **1** op in het veld **Aantal**.  
7. Geef het bedrag voor de verkoopprijskorting op in het veld **Eenheidsprijs excl. btw**.  
8. Nu kunt u de verkoopprijskorting als artikeltoeslag  toewijzen aan de artikelen op de geboekte verzending. Zie voor meer informatie [Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden](payables-how-assign-item-charges.md) Wanneer u het tegoed hebt toegewezen, gaat u terug naar de pagina **Creditnota**.  

Wanneer u de verkoopretourorder boekt, wordt de verkoopprijskorting toegevoegd aan het bijbehorende verkooppostbedrag. Op deze manier kunt u de waardering van uw voorraad correct bijhouden.

## <a name="to-combine-return-receipts"></a><a name="to-combine-return-receipts"></a><a name="to-combine-return-receipts"></a>Retourontvangsten combineren
U kunt retourontvangsten combineren als de klant meerdere artikelen, waarvoor verschillende verkoopretourorders zijn aangemaakt, retourneert.  

Wanneer de artikelen zijn aangekomen in het magazijn, boekt u de betreffende verkoopretourorders als ontvangen. Er worden dan geboekte retourontvangsten aangemaakt.  

Wanneer u deze klant wilt gaan factureren, kunt u in plaats van elke verkoopretourorder afzonderlijk te factureren, een verkoopcreditnota maken en de geboekte retourontvangstregels automatisch naar dit document kopiëren. Vervolgens kunt u de verkoopcreditnota boeken en gemakkelijk alle openstaande verkoopretourorders tegelijk factureren.  

Om retourverzendingen te combineren moet het selectievakje **Verzendingen combineren** zijn ingeschakeld op de pagina **Klantenkaart**.  

### <a name="to-manually-combine-return-receipts"></a><a name="to-manually-combine-return-receipts"></a><a name="to-manually-combine-return-receipts"></a>Retourontvangsten handmatig combineren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op het sneltabblad **Algemeen** in.  
4. Kies de actie **Retourontvangstregels ophalen**.  
5. Selecteer de retourontvangstregels die u in de creditnota wilt opnemen:  

    - Als u alle regels wilt invoegen, selecteert u alle regels en klikt u op **OK**.  

    - Als u specifieke regels wilt invoegen, selecteert u deze regels en klikt u op **OK**.  
6.  Als u de verkeerde verzendregel hebt geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de creditnota verwijderen en de functie **Retourontvangstregels ophalen** opnieuw uitvoeren.  
7.  Boek de factuur.  

### <a name="to-automatically-combine-return-receipts"></a><a name="to-automatically-combine-return-receipts"></a><a name="to-automatically-combine-return-receipts"></a>Retourontvangsten automatisch combineren

U kunt retourontvangsten automatisch combineren en beschikken over de optie om de creditnota's automatisch te boeken met de functie **Retourontvangsten combineren**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Retourontvangsten combineren** in en kies vervolgens de gerelateerde koppeling
2. Vul op de pagina **Retourontvangsten combineren** de velden in om de relevante retourontvangsten te selecteren.
3. Schakel het selectievakje **Creditnota's boeken** in. Als u dit niet doet, moet u de resulterende inkoopcreditnota's handmatig boeken.
4. Kies de knop **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a><a name="to-remove-a-received-and-invoiced-return-order"></a><a name="to-remove-a-received-and-invoiced-return-order"></a>Ontvangen en gefactureerde retourorders verwijderen

Als u op deze manier retourontvangsten factureert, blijven de retourorders van waaruit de retourontvangsten zijn geboekt bestaan, ook als ze volledig zijn ontvangen en gefactureerd.  

Als retourontvangsten worden gecombineerd op een creditnota en worden geboekt, wordt er een geboekte verkoopcreditnota gemaakt voor de gecrediteerde regels. Het veld **Verzonden aantal** op de oorspronkelijke verkoopretourorder wordt bijgewerkt op basis van het gefactureerde aantal.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gefactureerde verkoopretourorders verwijderen** in en kies vervolgens de gerelateerde koppeling.  
2. Geef in het filterveld **Nr.** op welke retourorders moeten worden verwijderd.  
3. Kies de knop **Ok**.  

U kunt afzonderlijke retourorders ook handmatig verwijderen.  

## <a name="inventory-costing"></a><a name="inventory-costing"></a><a name="inventory-costing"></a>Voorraadwaardering

Om de juiste voorraadwaardering te behouden, wilt u meestal retourartikelen in de voorraad terugzetten tegen de eenheidskostprijs waarvoor ze zijn verkocht en niet tegen de huidige eenheidskostprijs. Dit wordt exacte kostentegenboeking genoemd.

Er zijn twee functies om kosten automatisch exact tegen te boeken:  

|Functie|Omschrijving|  
|------------------|---------------------------------------|  
|De functie **Geboekte documentregels ophalen voor tegenboeking** op de pagina **Verkoopretourorder**|Kopieert regels van een of meer geboekte documenten, die in de verkoopretourorder worden tegengeboekt. Zie voor meer informatie [Een verkoopretourorder maken op basis van een of meer geboekte verkoopdocumenten](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|De functie **Document kopiëren** op de pagina's **Verkoopcreditnota** en **Verkoopretourorder**|Kopieert zowel de kop als de regels van één geboekt document voor tegenboeking.<br /><br /> Vereist dat het selectievakje **Precieze kostenvereff. verplicht** is ingeschakeld op de pagina **Instellingen van verkoop en tegoeden**.|

Als u exacte tegenboeking van kosten handmatig wilt toewijzen, moet u het veld **Vereffenen met artikelpost** selecteren op elk soort retourdocumentregel en vervolgens het nummer van de oorspronkelijke verkooppost selecteren. Hierdoor wordt de verkoopcreditnota gekoppeld aan de oorspronkelijke verkooppost en wordt het artikel gewaardeerd op de oorspronkelijke kostprijs.

Zie voor meer informatie [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
