---
title: Werken met servicecontracten en servicecontractoffertes | Microsoft Docs
description: U kunt een servicecontract handmatig of uit een servicecontractofferte maken. U kunt een contract op basis van een servicecontractofferte maken.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="work-with-service-contracts-and-service-contract-quotes"></a>Werken met servicecontracten en servicecontractoffertes
U kunt een servicecontract handmatig of uit een servicecontractofferte maken. U kunt een servicecontractofferte gebruiken als voorloper van een servicecontract, waarin uw bedrijf een aanbieding doet aan de klant en daarvoor goedkeuring van de klant verkrijgt, voordat u deze kunt omzetten in een servicecontract. De procedures voor het maken van een servicecontract of een servicecontractofferte zijn vergelijkbaar.  

## <a name="to-create-a-service-contract-or-service-contract-quote"></a>Een servicecontract of servicecontractofferte maken
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontracten** of **Servicecontractoffertes** in het tekstvak in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuw servicecontract of een servicecontractofferte.  
3. Vul het veld **Nr.** te kiezen. Er wordt een dialoogvenster geopend waarin wordt gevraagd of u de algemene gegevens van een contractsjabloon wilt invullen. Als u een dergelijk servicecontract of een dergelijke servicecontractofferte wilt maken, kies de knop **Ja**. De pagina **Servicecontractsjabloonoverzicht** wordt geopend.  
4. Selecteer de betreffende sjabloon en kies **OK** om deze te gebruiken voor het servicecontract of de servicecontractofferte.  
5. Kies in het veld **Klantnr.** de klant.  
6. Schakel het selectievakje **Bedragen in onbalans toestaan** in als u een verschil in het jaarlijkse bedrag niet automatisch wilt verdelen. De waarden in de velden **Jaarlijks bedrag** en **Berekend jaarlijks bedrag** worden niet automatisch gebalanceerd. Als u wilt dat de toepassing automatisch het verschil in het jaarlijkse bedrag dat kan ontstaan door een wijziging in het servicecontract, verdeelt, schakelt u het selectievakje **Bedragen in onbalans toestaan** uit.  
7. Voeg contractregels toe aan het servicecontract of de servicecontractofferte.  
8. Vul zo nodig de overige velden in.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a>Servicecontractoffertes omzetten in servicecontracten
Wanneer een klant een servicecontractofferte heeft geaccepteerd, zet u deze om in een servicecontract. Tegelijkertijd kunt u een servicefactuur maken voor de beginperiode van het contract, als de begindatum van het contract eerder valt dan de begindatum van de volgende factuurperiode.

Nadat u de volgende stappen hebt uitgevoerd, wordt er een servicecontract met de status **Ondertekend** gemaakt. Als er een servicefactuur voor de beginperiode van het contract wordt gemaakt, wordt het gefactureerde bedrag als volgt berekend, afhankelijk van of het contract gedetailleerd is of niet.  

Voor gedetailleerde contracten wordt het gefactureerde bedrag als volgt berekend:  

* Gefactureerd bedrag = de som van de gefactureerde bedragen voor elke contractregel.  
* Gefactureerd bedrag voor elke contractregel = ((offertewaarde ÷ 12) × aantal maanden in de beginperiode) + ((offertewaarde ÷ aantal dagen in het jaar) × resterende aantal dagen in de beginperiode).  
* Als de contractregel vervalt vóór het einde van de beginperiode, wordt de vervaldatum de einddatum van de beginperiode voor de regel.  

Voor niet-gedetailleerde contracten wordt het gefactureerde bedrag als volgt berekend:  

* Gefactureerd bedrag = (jaarlijks bedrag ÷ aantal dagen in het jaar) × aantal dagen in de beginperiode.  
* Als het contract vervalt vóór het einde van de beginperiode, wordt de vervaldatum de einddatum van de beginperiode.    

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontractoffertes** in en kies vervolgens de gerelateerde koppeling.  
2. Open de servicecontractofferte die u wilt omzetten in een servicecontract.  
3. Kies de actie **Contract maken**.  
4. Als de begindatum van het contract eerder valt dan de begindatum van de volgende factuurperiode, wordt u gevraagd of u een servicefactuur wilt maken voor de beginperiode van het contract. Kies **Ja**.  

 De servicefactuur wordt geboekt naar de servicerekening van het contract, zelfs wanneer het contract vooruitbetaald is.

## <a name="to-create-contract-service-credit-memos"></a>Creditnota's voor contractservice maken
U kunt een contractservicecreditnota gebruiken wanneer een klant een vooruitbetaald servicecontract annuleert of een serviceartikel uit een vooruitbetaald contract verwijdert. Hiermee kunt u ook een foutieve servicefactuur corrigeren.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecreditnota's** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe servicecreditnota.  
3. Vul het veld **Nr.** te kiezen.  
4. Voer in het veld **Klantnr.** het nummer in van de klant in het servicecontract.  

     Op het Sneltabblad **Facturering** worden de gegevens van de kaart **Klant** weergegeven. Als u de creditnota naar een andere klant dan de klant op het sneltabblad **Algemeen** wilt boeken, moet u in het veld **Factureren aan** het nummer van de betreffende klant invoeren.  

    > [!NOTE]  
    >  U kunt de creditnota vergelijken met het oorspronkelijke geboekte document op de pagina **Geboekte servicefacturen**. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte servicefacturen** in en kies vervolgens de gerelateerde koppeling.  

5. Vul de velden **Boekingsdatum** en **Documentdatum** in.  
6. Voer op de creditnotaregels gegevens in over de artikelen die zijn teruggebracht of verwijderd of over de vergoeding die wordt verzonden. U kunt ook de batchverwerking **Vooruitbet. contractposten ophalen** gebruiken.  

 Als u automatisch een creditnota wilt maken wanneer u contractregels verwijdert, moet u het selectievakje **Automatische creditnota's** inschakelen op het sneltabblad **Factuurdetails** op de pagina **Servicecontract**.  

 Als u handmatig een creditnota wilt maken wanneer contractregels uit een servicecontact zijn verwijderd, kiest u op de pagina **Servicecontract** de actie **Creditnota**.  

## <a name="updating-and-evaluating-contracts"></a>Contracten bijwerken en evalueren
Het kan voorkomen dat u de voorwaarden van een contract moet wijzigen nadat het contract is gemaakt. In dergelijke gevallen kunt u het desbetreffende contract meestal openen op de pagina **Servicecontract** en de gewenste wijzigingen aanbrengen.  

U kunt de status van het contract wijzigen, aanvankelijk ingesteld op **Vergrendeld**, contractregels toevoegen en verwijderen en een contract annuleren. Voor een overzicht van de winst-/verliesposten van uw bedrijf kunt u een snelle bedrijfsanalyse uitvoeren met de functie Contract-trendscape.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>Contractregels toevoegen aan een servicecontract of contractofferte
Wanneer een klant een nieuw artikel koopt en wil opnemen in het bestaande servicecontract of de bestaande contractofferte, kunt u het artikel registreren als een serviceartikel en vervolgens als nieuwe contractregel toevoegen aan het contract of de contractofferte.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontracten** in en kies vervolgens de gerelateerde koppeling.  
2. Open het servicecontract of de servicecontractofferte waarvoor u een nieuwe contractregel wilt toevoegen.  
3. Kies de actie **Contract openen** om het servicecontract of de servicecontractofferte te openen en bewerken.  
4. Op het Sneltabblad **Factuurdetails** selecteert u het veld **Bedragen in onbalans toestaan**, als u het jaarlijkse bedrag wilt wijzigen en het verschil in het jaarlijkse bedrag handmatig wilt verdelen op de contractregels. Schakel anders het selectievakje **Bedragen in onbalans toestaan** uit. Hierdoor wordt het verschil in het jaarlijkse bedrag automatisch verdeeld over de contractregels nadat u het jaarlijkse bedrag hebt gewijzigd.  
5. Voeg op het sneltabblad **Regels** een serviceartikel of artikel of een tekstomschrijving toe op elke contractregel. U kunt ook contractofferteregels toevoegen. U kunt meerdere contracten maken voor een serviceartikel, zodat het in meerdere servicecontracten of servicecontractoffertes tegelijk wordt opgenomen.  
6. Controleer en corrigeer waar nodig de getallen in de velden **Regelkorting %**, **Totale regelkorting**, **Responstijd**, **Serviceperiode**, en andere velden.

## <a name="to-remove-contract-lines"></a>Contractregels verwijderen
U moet mogelijk contractregels uit het servicecontract verwijderen als u de overeenkomstige serviceartikelen uit het servicecontract verwijdert. Meestal verwijdert u een contractregel die is verlopen of die overeenkomt met het serviceartikel dat defect is.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontracten** in en kies vervolgens de gerelateerde koppeling.  
2. Open het servicecontract waaruit u contractregels wilt verwijderen.  
3. Kies de actie **Contract openen** om het servicecontract te openen en bewerken.  
4. Kies de contractregel die u wilt verwijderen. Vul het veld **Vervaldatum van contract** in met de datum vanaf wanneer u de regel wilt verwijderen. U kunt bijvoorbeeld de datum invoeren waarop het serviceartikel defect is geraakt.  
5. Kies de actie **Contractregels verwijderen**. De pagina **Contractregels verwijderen** wordt geopend.  
6. Vul de standaardfilters **Contractnr.**, **Serviceartikelnr.** en **Contractsoort** in. Desgewenst kunt u meer filters toepassen of bestaande filters wijzigen.  
7. Vul de velden op het sneltabblad **Opties** in en kies de actie **Regels verwijderen**.  

> [!NOTE]  
>  Als het contract niet gedetailleerd is, moet u de waarde in het veld **Jaarlijks bedrag** op het sneltabblad **Factuurdetails** op de pagina **Servicecontract** bijwerken om het verlies van het serviceartikel uit het contract aan te geven.  
>   
>  Als het contract gedetailleerd en vooruitbetaald is, en hebt u facturen voor het contract geboekt, kunt u een creditnota voor het contract maken. Kies de actie **Creditnota maken**. Dit is nodig als het selectievakje in het veld **Automatische creditnota's** op het sneltabblad **Factuurdetails** is geselecteerd. In dat geval wordt er automatisch een creditnota gemaakt wanneer u een contractregel verwijdert.

## <a name="service-line-cost-and-value"></a>Regelkostprijs en -waarde voor service
Op een servicecontractregel worden de bedragen bij **Regelkostprijs** en **Regelwaarde** berekend zoals in de volgende tabellen wordt beschreven.

| Opties voor regelkostprijs | Description|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | De kosten worden automatisch opgehaald uit het veld **Std. contractkosten** in de tabel **Serviceartikel** en gekopieerd naar het veld **Regelkostprijs**. De regelkostprijs wordt berekend met de volgende formule:<br /><br /> Verkoopkostprijs × Contractwaarde % ÷ 100|  
|**Artikel** | De kosten worden automatisch opgehaald uit het veld **Kostprijs** in de tabel **Artikel** en het veld **Contractwaarde %** in de tabel **Servicebeheerinstellingen**. De regelkostprijs wordt berekend met de volgende formule:<br /><br /> Kostprijs × Contractwaarde % ÷ 100|  
|**Tekstomschrijving** | De waarde in het veld **Regelkostprijs** wordt ingesteld op nul.|  

| Opties voor regelwaarde | Description|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | De prijs wordt automatisch opgehaald uit het veld **Std. contractwaarde** in de tabel **Serviceartikel** en gekopieerd naar het veld **Regelwaarde**.|  
|**Artikel** | Afhankelijk van de waarde in het veld **Contractwaardeberek.-methode** in de tabel **Servicebeheerinstellingen** wordt het bedrag opgehaald uit het veld **Eenheidsprijs** of het veld **Kostprijs** in de tabel **Artikel**. Vervolgens wordt deze waarde vermenigvuldigd met de inhoud van het veld **Contractwaarde %** in de tabel **Servicebeheerinstellingen** en gedeeld door 100. Dit bedrag wordt gekopieerd naar het veld **Regelwaarde**.<br /><br /> **OPMERKING:** als het veld **Contractwaardeberek.-methode** is ingesteld op **Geen**, wordt de inhoud van het veld **Regelwaarde** niet berekend.|  
|**Tekstomschrijving** | De inhoud van het veld **Regelwaarde** wordt ingesteld op nul.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a>Contractkortingen aan servicecontractoffertes toevoegen
U kunt contractkortingen op services toevoegen voor contractoffertes en servicecontracten. De kortingen kunnen gelden voor reserveonderdelen in bepaalde serviceartikelgroepen, voor resource-uren voor resources in bepaalde resourcegroepen en voor bepaalde servicekosten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontractoffertes** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de offerte waarvoor u kortingen wilt toevoegen.  
3. Kies de actie **Servicekortingen**. De pagina **Contract-/servicekortingen** wordt geopend.  
4. Kies de actie **Nieuw** om een nieuwe contractkorting te maken.  
5. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Als u contractkortingen rechtstreeks wilt toevoegen aan een servicecontract, voert u dezelfde procedure uit vanuit de pagina **Servicecontract**.  

## <a name="to-change-the-owner-of-a-service-contract"></a>Eigenaar van servicecontracten wijzigen
Mogelijk moet u de eigenaar van een servicecontract wijzigen Als een serviceartikel in een servicecontract is geregistreerd in niet-geannuleerde meervoudige contracten van dezelfde klant, wordt automatisch de eigenaar gewijzigd van alle servicecontracten die dit serviceartikel bevatten en van alle andere serviceartikelen in deze contracten.  

> [!NOTE]  
>  In dit geval wordt alleen gekeken naar niet-geannuleerde contracten. Er wordt geen rekening gehouden met de status van de contractoffertes.  

> [!IMPORTANT]  
>  Serviceartikelen en -contracten kunnen gerelateerd zijn. Het wijzigen van de eigenaar van een servicecontract kan invloed hebben op deze relaties.  
>   
>  Een voorbeeld: veronderstel dat serviceartikelnr. 8 is opgenomen in contracten SC00003 en SC00015. Contract SC00015 bevat ook serviceartikelnr. 15, dat ook is opgenomen in het contract SC00080. In dit geval wordt de eigenaar voor alle drie contracten en serviceartikelen gewijzigd.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontracten** in en kies vervolgens de gerelateerde koppeling. Open het betreffende servicecontract waarvoor u de eigenaar wilt wijzigen.  
2. Kies de actie **Contract openen** om het contract te openen en bewerken.  
3. Kies de actie **Klant wijzigen**. De pagina **Klant in contract wijzigen** wordt geopend.  
4. In de velden **Contractnr.** en **Serviceartikelnr.** kunt u de nummers bekijken van het contract en het serviceartikel van de geselecteerde klant. Als de klant eigenaar is van meerdere contracten waarin meerdere serviceartikelen zijn opgenomen, is de waarde van deze velden **Meervoudig**. Als u de lijst met verwante contracten of serviceartikelen wilt bekijken, selecteert u deze waarden.  
5. Selecteer in het veld **Nieuw klantnr.** de nieuwe klant.  
6. In het veld **Nieuwe verzendcode** kiest u het adres.  
7. Kies de knop **OK** om de klant en de verzendcode van de servicecontracten te wijzigen.  
8. Kies de actie **Contract vergrendelen** om het contract te vergrendelen en ervoor te zorgen dat de wijzigingen in de contracten worden opgenomen.  

## <a name="to-update-a-service-contract-price"></a>Servicecontractprijzen bijwerken
U kunt een prijsaanpassingspercentage opgeven om de prijzen voor servicecontracten bij te werken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontractprijzen bijwerken** in en kies vervolgens de gerelateerde koppeling.
2. Kies het servicecontract.  
3. Geef een datum op in het veld **Aanpassen tot datum**. Met de batchverwerking worden de prijzen voor contracten met volgende prijsaanpassingsdatums aangepast op of vóór deze datum.  
4. Geef in het veld **Prijsaanpassing %** het prijsaanpassingspercentage op.  
5. Selecteer in het veld **Actie** de optie **Contractprijzen aanpassen**.  

## <a name="to-post-prepaid-contract-entries"></a>Vooruitbetaalde contractposten boeken
Als u werkt met vooruitbetaalde servicecontracten, moet u regelmatig vooruitbetaalde contractposten boeken. Zo maakt u de vooruitbetalingen van de vooruitbetalingsrekeningen voor contracten over naar de gewone contractrekeningen.  

Voordat u vooruitbetaalde contractposten kunt boeken, moet u een nummerreeks opgeven in het veld **Boekingsdoc.-nrs. vooruitbetalingen** op de pagina **CRM – Service-instellingen**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vooruitbet. contractposten boeken** in en kies vervolgens de gerelateerde koppeling.  
2. Geef een datum op in het veld **Boeken tot datum**. Met de batchverwerking worden vooruitbetaalde serviceposten geboekt met boekingsdatums tot deze datum.  
4. Geef in het veld **Boekingsdatum** de gewenste boekingsdatum voor de dagboekregel op.  
5. Kies in het veld **Actie** de actie **Vooruitbetaalde transacties boeken**.  
6. Klik op **OK** om de posten te boeken.

## <a name="changing-the-service-contract-status"></a>De status van het servicecontract wijzigen
Als het servicecontract is ondertekend, wordt het veld **Wijzigingsstatus** automatisch ingesteld op **Vergrendeld**. Als u informatie wilt wijzigen in het servicecontract of de servicecontractofferte, moet u eerst de status van het contract of de contractofferte wijzigen van **Vergrendeld** in **Open**. U kunt geen servicefacturen maken voor het servicecontract als de wijzigingsstatus **Open** is. Nadat het contract of de contractofferte is gewijzigd, moet u de status weer wijzigen in **Vergrendeld**, zodat u weer servicefacturen en posten kunt maken voor het nu gewijzigde servicecontract.  

> [!NOTE]  
>  Het veld **Status wijzigen** is niet gerelateerd aan het veld **Vrijgavestatus** op de serviceorderkop, dat de magazijnverwerking van serviceartikelen regelt.  

## <a name="to-cancel-a-service-contract"></a>Een servicecontract annuleren
Als een contract is verlopen of door u of de klant is geannuleerd, moet u het betreffende servicecontract mogelijk annuleren.  

> [!NOTE]  
>  U kunt een contract niet opnieuw openen nadat het is geannuleerd.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontracten** in en kies vervolgens de gerelateerde koppeling.  
2. Open het servicecontract dat u wilt annuleren.  
3. Kies de actie **Contract openen** om het servicecontract te openen en bewerken.  
4. In het veld **Annuleringsredencode** kiest u de betreffende redencode. Als u meer redencodes wilt toevoegen, kiest u de actie **Geavanceerd**.  

     Als het selectievakje in het veld **Contractannuleringsreden gebruiken** op de pagina **Servicebeheerinstellingen** is ingeschakeld, moet u een annuleringsredencode opgeven als u contracten annuleert.  

5. Selecteer in het veld **Status** de optie **Geannuleerd**.  
6. Als er niet-geboekte facturen, creditnota's of geopende vooruitbetaalde posten zijn voor het contract, wordt er een bevestigingsbericht weergegeven. Klik in het berichtvak op **Nee** als u wilt terugkeren naar het contract om de documenten te boeken. Klik op **Ja** als u verder wilt gaan met het annuleren.  

## <a name="filing-a-service-contract-or-contract-quote"></a>Servicecontracten of contractoffertes archiveren
U kunt servicecontracten en contractoffertes op elk moment archiveren om een kopie van het contract of de contractofferte vast te leggen. [!INCLUDE[prod_short](includes/prod_short.md)] archiveert servicecontracten automatisch wanneer u contractoffertes omzet in servicecontracten of servicecontracten annuleert. U kunt een contract of offerte zelf archiveren met de actie **Contract archiveren** op de pagina **Servicecontracten** of **Servicecontractoffertes**. Als u uw gearchiveerde contracten van offertes wilt weergeven, zoekt u op **Gearchiveerde contracten**.

## <a name="see-also"></a>Zie ook
[Servicecontracten instellen](service-how-setup-service-contracts.md)  
[Servicebeheer](service-service.md)  
[Servicecontracten met btw-bedragen converteren](service-how-to-convert-service-contracts.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
