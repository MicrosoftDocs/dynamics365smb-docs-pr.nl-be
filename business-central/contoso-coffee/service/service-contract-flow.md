---
title: Procedure van servicecontracten voor serviceartikelen
description: In dit artikel wordt u door verschillende scenario's met serviceartikelen en contracten geleid.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Procedure van servicecontracten voor serviceartikelen

Deze procedure demonstreert verschillende kernprocessen:

- Serviceartikelen maken via verkoop
- Maken en factureren van een servicecontract
- Een serviceorder voor een servicecontract maken
- Een resource toewijzen op basis van vaardigheid en zone
- De tijdpost voor de serviceorder voltooien
- De contractserviceorder boeken en factureren

## <a name="creation-of-service-items"></a>Serviceartikelen maken

### <a name="scenario"></a>Scenario

Susan, de orderverwerker, boekt een verkooporder waarin een artikel wordt verkocht dat is geconfigureerd om een serviceartikel te genereren.  

### <a name="steps"></a>Stappen

1. Controleer of voor **Artikel** **Serviceartikelgroep** is geselecteerd.
   
    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer het artikel *S-100* en open het.
    3. Controleer de waarde in het veld **Serviceartikelgroep**.
       
2. Boek de **Verkooporder** om het serviceartikel voor de klant te maken.  

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer de order voor klant 10000. Het externe ordernr. is *SVC-1*.
    3. Kies de actie **Boeken** om het artikel naar de klant te verzenden.

### <a name="results"></a>Resultaten

- Er wordt een serviceartikel gemaakt voor klant 10000

## <a name="invoicing-a-service-contract"></a>Een servicecontract factureren

### <a name="scenario-1"></a>Scenario

Charles, de servicemanager, maakt vervolgens een servicecontract om reguliere onderhoudsbezoeken te factureren.

3. Maak het **servicecontract** voor het nieuwe serviceartikel
    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontracten** in en kies vervolgens de gerelateerde koppeling.
    2. Kies de actie **Nieuw**.  
    3. Kies in het bevestigingsvenster **Ja** om een contract te maken met behulp van een sjabloon. 
    4. Selecteer *Niet-vooruitbetaald contract - maandelijks*.
    5. Voer op het sneltabblad Service bij **Serviceordertype** **ONDERHOUD** in.
    6. Voer op de regels de volgende informatie in:

    |Serviceartikelnr.|Regelwaarde|  
    |----------------|----------|  
    |SV000001|6000|

    7. Kies de actie **Contract tekenen** en bevestiging de ondertekening.
    8. Kies **Ja** om het maken van een servicefactuur te bevestigen. U ontvangt een bevestigingsbericht met het servicefactuurnummer.

3. Boek de servicefactuur
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicefacturen** in en kies vervolgens de gerelateerde koppeling.
   2. Zoek de servicefactuur en kies de actie **Boeken**.

### <a name="results-1"></a>Resultaten

- Er wordt een ondertekend servicecontract gemaakt met grootboekposten
- Er wordt een geboekte servicefactuur gemaakt

## <a name="create-a-service-order-for-a-service-contract-and-assign-resources"></a>Een serviceorder voor een servicecontract maken en resources toewijzen

### <a name="scenario-2"></a>Scenario

Charles, de servicemanager, maakt de serviceorders voor reguliere onderhoudsorders onder het servicecontract en beoordeelt vervolgens het planbord om ze toe te wijzen.

### <a name="steps-1"></a>Stappen

1. Voer de serviceorders uit die voldoen aan de verplichtingen van actieve servicecontracten.
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders maken** in en kies vervolgens de gerelateerde koppeling.
   2. Voer de begin- en einddatum van de maand in de velden Begindatum en Einddatum op het sneltabblad Opties in
   3. Kies **OK** om het maken van serviceorders te bevestigen. U ontvangt een bevestigingsbericht met het aantal gemaakte serviceorders.

2. Bekijk de orders die in afwachting zijn van toewijzing via het planbord
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planbord** in en kies vervolgens de gerelateerde koppeling.
   2. Het planbord toont alle openstaande serviceorders, samen met het **Aantal toewijzingen** om aan te geven of de serviceorders zijn toegewezen aan een resource.
   3. Kies de actie **Documenten weergeven** om een serviceorder te openen.  U zult zien dat het feitenblok Serviceartikelregels laat zien welke resources vaardig zijn in het werken met dit artikel.

3. Een resource toewijzen aan de serviceorder
   1. Kies vanuit de serviceorder de regelactie **Resourcetoewijzingen**
   2. Voer de volgende gegevens in voor de resourcetoewijzing

    |Serviceartikelnr.|Resourcenr.|Toewijzingsdatum|Toegewezen uren|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|h|1|

    3. De toewijzing wordt gewijzigd in de status Actief.
    4. Als u het planbord vernieuwt, toont het dat **Aantal toewijzingen** is gewijzigd van 0 in 1 voor de serviceorder.

### <a name="results-2"></a>Resultaten

- Er worden serviceorders gemaakt voor de servicecontracten
- De serviceorders worden toegewezen aan een resource om het werk te voltooien

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Voltooi de tijdpost voor de serviceorder en boek de serviceorder

### <a name="scenario-3"></a>Scenario

De servicemonteur registreert de tijd rechtstreeks voor de serviceorder en markeert de order vervolgens als voltooid.

> [!NOTE]
> Tijdpost voor serviceorders kunt u invoeren via urenstaten. Voor meer informatie zie [koppeling naar urenstaat als deze opmerking zinvol is].

### <a name="steps-2"></a>Stappen

1. Zoek de serviceorder en voer de tijd op de serviceregel in
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling.
   2. Zoek de serviceorder waarvoor u tijd wilt invoeren.
   3. Kies de regelactie **Serviceregel**.
   4. Geef de volgende informatie op

    |Type|Nr.|Hoeveelheid|Te verbruiken aantal|
    |----|---|--------|--------|   
    |Resource|RESOURCE1|2|2|

2. Boek het verbruik op de serviceorder
   1. Kies de actie **Boeken** om de serviceorder te voltooien, selecteer de actie **Verzenden en verbruiken** en kies vervolgens de knop **OK**.

### <a name="results-3"></a>Resultaten

- Er worden serviceposten gemaakt die zijn gekoppeld aan het serviceartikel, het servicecontract en de resource

## <a name="see-also"></a>Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](../../contoso-coffee/contoso-coffee-intro.md)  
[Over productieorders](../../production-about-production-orders.md)
