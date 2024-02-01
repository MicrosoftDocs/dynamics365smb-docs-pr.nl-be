---
title: Wijzigingen in btw-tarieven beheren
description: Leer hoe u de Wijzigingstool btw-tarief voor Dynamics 365 Business Central gebruikt voor het wijzigen van btw-tarieven op basis van lokale wetgeving.
author: jswymer
ms.topic: conceptual
ms.reviewer: bholtorf
ms.search.keywords: 'VAT, VAT rate, posting, tax, value-added tax'
ms.search.form: '550,'
ms.date: 06/16/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="managing-vat-rate-changes"></a>Wijzigingen in btw-tarieven beheren

Btw-tarieven kunnen veranderen afhankelijk van de lokale wetgeving. Elke wijziging in de btw heeft gevolgen voor uw gegevens in [!INCLUDE[prod_short](includes/prod_short.md)] ongeacht of btw wordt verhoogd, verlaagd of verwijderd. Btw is verbonden met veel entiteiten in [!INCLUDE[prod_short](includes/prod_short.md)], zoals klanten, leveranciers, artikelen, resources, artikelkosten en grootboekrekeningen. Wijzigingen in btw-tarieven vinden meestal plaats op een specifieke datum, vanaf welk punt u de btw-instellingen, boekingsgroepen enzovoort moet wijzigen om ervoor te zorgen dat nieuwe verkooporders en inkooporders worden gemaakt met het nieuwe btw-tarief.

## <a name="changing-vat-rates"></a>Btw-tarieven wijzigen

De optimale aanpak om een wijziging van het btw-tarief te beheren is om openstaande orders en andere documenten volledig te boeken en te sluiten vóór de datum waarop het btw-tarief wordt gewijzigd, om ervoor te zorgen dat ze niet door de wijziging worden beïnvloed. Dit is de schoonste aanpak waarmee u nieuwe orders en documenten kunt opstarten met het nieuwe btw-tarief.

De volgende aanpak wordt voorgesteld om een wijziging van het btw-tarief te beheren

1. Boek en sluit openstaande orders, dagboeken en andere documenten volledig vóór de wisseldatum. U kunt wachten tot na de overstapdatum, zolang u geen nieuwe regels toevoegt en ervoor zorgt dat de ingangsdatum vóór de overstapdatum ligt.  
2. Maak de nieuwe btw-instelling.  
3. Schakel de btw over op entiteiten (relevante klanten, leveranciers, artikelen, enzovoort).  
4. Op de wisseldatum van het btw-tarief maakt u nieuwe documenten die het nieuwe tarief zullen gebruiken.  


> [!NOTE]  
> We zijn momenteel de Wijzigingstool btw-tarief aan het bijwerken. De onderstaande functionaliteit komt mogelijk niet overeen met de functionaliteit in uw omgeving. De update vindt plaats vóór 1 juli 2020 en is geen reguliere maandelijkse update. In plaats daarvan worden alle omgevingen automatisch bijgewerkt (hotfix). Wanneer deze update is voltooid, wordt dit bericht niet meer weergegeven.  

## <a name="the-vat-rate-change-tool"></a>De Wijzigingstool btw-tarief

De Wijzigingstool btw-tarief kan tot op zekere hoogte helpen bij het omzetten van btw-tarieven op hoofdgegevens, dagboeken en orders. Dit is handig als u de btw op hoofdgegevens gemakkelijker wilt converteren of als u orders hebt die u niet kunt sluiten voor de overstapdatum en die over een langere periode worden verwerkt, waarbij de btw-tariefwisseldatum wordt overschreden. Er zijn bepaalde restricties en beperkingen in de Wijzigingstool btw-tarief die van toepassing zijn.

## <a name="understanding-the-vat-rate-conversion-process-and-limitations"></a>Het proces en de beperkingen voor het converteren van btw-tarieven begrijpen

De Wijzigingstool btw-tarief voert op verschillende manieren conversies uit voor hoofdgegevens, dagboeken en orders. De geselecteerde stamgegevens en dagboeken worden bijgewerkt door de nieuwe algemene productboekingsgroep of de btw-productboekingsgroep. Als u een order volledig of gedeeltelijk hebt verzonden, blijven de verzonden artikelen onderdeel van de huidige algemene productboekingsgroep of btw-productboekingsgroep. Een nieuwe orderregel wordt gemaakt voor de niet verzonden items en bijgewerkt om overeen te komen met de huidige en de nieuwe BTW- of productboekingsgroepen. Bovendien worden gegevens over artikeltoeslagtoewijzigingen, configuratiesjablonen voor artikelen, reserveringen en artikeltracering dienovereenkomstig bijgewerkt. 

Op orderregels wordt de eenheidsprijs bijgewerkt voor alle regels van het type Item en Resource, bij gebruik van prijzen incl. btw voor het artikel. Voor andere regeltypes is het mogelijk om te beslissen of de eenheidsprijs al dan niet moet worden bijgewerkt.

Er is een aantal dingen die niet worden geconverteerd door de tool:

* Verkoop- of inkooporders en facturen waar verzendingen zijn geboekt. Deze documenten zijn geboekt met het huidige btw-tarief.  
* Documenten met geboekte vooruitbetalingsfacturen. U hebt bijvoorbeeld vooruitbetalingen gedaan of ontvangen op facturen die nog niet zijn voltooid voordat u het wijzigingstool btw-tarief gaat gebruiken. In dit geval is er een verschil tussen de verschuldigde btw en de betaalde btw in de vooruitbetalingen wanneer de factuur is voltooid. Het wijzigingstool btw-tarief slaat deze documenten over en u moet deze handmatig bijwerken.  
* Verkoop- of inkooporders met magazijnintegratie als deze gedeeltelijk zijn verzonden of ontvangen.  
* Doorverzendingen.
* Speciale orders. 
* Assemblageorders.
* Servicecontracten.  
* Creditnota's.
* Retourorders.
* Prijzen op artikelen (hoofdgegevens)
* Prijzen op verkoopprijzen (hoofdgegevens)
* Bedrijfsboekingsgroepen voor klanten en leveranciers.

### <a name="to-prepare-vat-rate-change-conversions"></a>Conversies van btw-tariefswijziging voorbereiden

Voordat u het wijzigingstool btw-tarief instelt, moet u de volgende voorbereidingen treffen.

* Als u transacties met verschillende tarieven hebt, moeten deze vervolgens worden gescheiden in verschillende groepen door voor elke tarief nieuwe grootboekrekeningen te maken of door met gegevensfilters transacties per tarief te groeperen.  
* Als u nieuwe grootboekrekeningen maakt, moet u nieuwe algemene boekingsgroepen maken.  
* Om het aantal documenten dat wordt geconverteerd zo klein mogelijk te maken, moet u zoveel mogelijk documenten boeken en niet-geboekte documenten tot een minimum beperken.  
* Back-up van gegevens maken.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Het wijzigingstool btw-tarief instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Wijziging btw-tarief instellen** in en kies vervolgens de gerelateerde koppeling.  
2. Op de sneltabbladen **Hoofdgegevens**, **Dagboeken** en **Documenten** kiest u een boekingsgroepwaarde in de lijst met opties voor verplichte velden. Voor elke groep kunt u kiezen of u btw-productboekingsgroepen of algemene productboekingsgroepen wilt converteren of beide waarden wilt converteren als deze beschikbaar zijn in het stamgegevensitem. Voor sommige gebieden kunt u ook een filter instellen om alleen een subset van waarden te converteren, bijvoorbeeld grootboekrekeningen. 
3. Kies op het sneltabblad **Prijzen incl. btw** regeltypen voor orders waarvoor u de eenheidsprijzen wilt bijwerken. Eenheidsprijzen op regels van het type Item en Resource worden altijd bijgewerkt.

### <a name="to-set-up-product-posting-group-conversion"></a>Conversie voor productboekingsgroepen instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Wijziging btw-tarief instellen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Wijziging btw-tarief instellen** en kies de actie **Conversie boekingsgroep btw-producten** of **Conversie boekingsgroep algemene producten**.  
3. Voer in het veld **Van code** de huidige boekingsgroep in.  
4. Voer in het veld **Tot code** de nieuwe boekingsgroep in.  

### <a name="to-perform-vat-rate-change-conversion"></a>Een conversie voor een btw-tariefswijziging uitvoeren

U gebruikt de Wijzigingstool btw-tarief om wijzigingen in het standaardtarief van btw te beheren. U kunt btw en algemene boekingsgroepconversies uitvoeren om btw-tarieven te wijzigen en nauwkeurige btw-rapportage te onderhouden. Afhankelijk van uw instellingen worden de volgende wijzigingen aangebracht:  

* Btw- en algemene boekingsgroepen worden geconverteerd.  
* Wijzigingen worden doorgevoerd in grootboekrekeningen, klanten, leveranciers, geopende documenten, dagboekregels, enzovoort.  

> [!IMPORTANT]  
> Voordat u de conversie van de btw-tariefswijziging uitvoert, kunt u de conversie testen. Hiervoor volgt u de onderstaande stappen, maar zorg ervoor dat u de selectievakjes **Conversie uitvoeren** en **Wijzigingstool BTW-tarief voltooid** uitschakelt. Tijdens testconversie wordt het veld **Geconverteerd** in de tabel **Dagboekpost wijziging BTW-tarief** gewist en is het veld **Conversiedatum** in de tabel **Dagboekpost wijziging BTW-tarief** leeg. Kies nadat de conversie is voltooid de optie **Wijzigingslogposten btw-tarief** om de resultaten van de testconversie weer te geven. Controleer elke post voordat u de conversie uitvoert. Controleer met name transacties met een oud btw-tarief.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Wijzigingstool btw-tarief** in en kies vervolgens de koppeling **Wijziging btw-tarief instellen**.  
2. Controleer of u de conversie van de btw-productboekingsgroep of de conversie van de algemene productboekingsgroep al hebt ingesteld.  
3. Schakel het selectievakje **Conversie uitvoeren** in.  

    > [!IMPORTANT]  
    >  Schakel het selectievakje **Wijzigingstool BTW-tarief voltooid** uit. Het selectievakje wordt automatisch ingeschakeld wanneer de conversie btw-tariefswijziging is voltooid.  

4. Kies de actie **Converteren**.  
5. Wanneer de conversie voltooid is, kiest u de actie **Logbestandvermeldingen btw-tariefwijziging** om de resultaten van de conversie te zien.  

> [!IMPORTANT]  
> Nadat de conversie is voltooid, wordt het veld **Geconverteerd** in de tabel **Dagboekpost wijziging BTW-tarief** ingeschakeld en bevat het veld **Conversiedatum** in de tabel **Dagboekpost wijziging BTW-tarief** de conversiedatum.  

## <a name="see-also"></a>Zie ook

[Btw instellen](finance-setup-vat.md)  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)  
[Btw-aangifte doen bij een belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Lokale functionaliteit in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
