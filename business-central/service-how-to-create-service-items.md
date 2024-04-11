---
title: Serviceartikelen maken
description: 'Lees over de verschillende manieren waarop u serviceartikelen kunt maken in Business Central, bijvoorbeeld binnen een serviceorder of bij het verzenden van artikelen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-service-items"></a>Serviceartikelen maken

In [!INCLUDE[prod_short](includes/prod_short.md)] verwijst de term serviceartikel naar de apparatuur of artikelen die service vereisen. Wanneer u een serviceorder maakt, geeft u de artikelen op die service nodig hebben. In de order kunt u een serviceartikel aan een artikel in de voorraad of aan een serviceartikelgroep koppelen.

Wanneer u een artikel ontvangt dat service vereist, kunt u dit artikel registreren als serviceartikel. Dit kunt u op verschillende manieren doen. U kunt bijvoorbeeld via de pagina **Serviceartikelen** een serviceartikel maken of als onderdeel van een ander proces, bijvoorbeeld wanneer u met een serviceorder werkt.

## <a name="to-create-a-service-item"></a>Een serviceartikel maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceartikelen** in en kies vervolgens de gerelateerde koppeling
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Serviceartikelen maken in serviceorders

Wanneer u artikelen voor service ontvangt die u wilt registreren als serviceartikelen, kunt u deze instellen als serviceartikelen op de pagina **Serviceorder** of **Serviceofferte**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Kies de actie **Serviceartikel maken**.  

    Er wordt een nummer aan het serviceartikel toegewezen en een kaart voor het serviceartikel gemaakt. Het nummer van het nieuwe serviceartikel wordt ingevuld in het veld **Serviceartikelnr.**

## <a name="to-create-a-service-item-when-shipping-items"></a>Serviceartikelen maken tijdens het verzenden van artikelen

Als u artikelen verzendt door verkooporders of verkoopfacturen te boeken, worden de verzonden artikelen automatisch als serviceartikelen geregistreerd als aan de volgende voorwaarde wordt voldaan. De artikelen moeten behoren tot een serviceartikelgroep waarvoor het selectievakje **Serviceartikel maken** is ingeschakeld. Als voor de artikelen serienummers zijn geregistreerd op de pagina Artikeltraceringsregels, worden deze gegevens tijdens het maken van serviceartikelen automatisch gekopieerd naar het veld **Serienummer** op de serviceartikelkaart.  

Hieronder wordt aangegeven hoe u serviceartikelen kunt maken tijdens het verzenden van artikelen in verkooporders.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Open de betreffende verkooporder.  
3. Kies de actie **Boeken** of **Boeken en afdrukken**.  
4. Kies de actie **Verzenden** of **Verzenden en factureren**.  
5. Er worden automatisch serviceartikelen gemaakt voor de artikelen op de order, wanneer deze behoren tot een serviceartikelgroep die u hebt ingesteld om serviceartikelen te maken. Als u bepaalde serienummers op de pagina **Artikeltraceringsregels** hebt geregistreerd, worden deze dienovereenkomstig aan deze serviceartikelen toegewezen.  

> [!NOTE]  
> Als een artikel is ingesteld als stuklijst en u de stuklijst hebt getoond, worden de getoonde stuklijstartikelen verwerkt als gewone artikelen. Serviceartikelen worden gemaakt op basis van de voorwaarde serviceartikelgroep en optioneel op de voorwaarde serienummers. Als een serviceartikel wordt gemaakt voor een getoond stuklijstartikel waarin andere stuklijstonderdelen zijn opgenomen, worden deze artikelen gemaakt als serviceartikelonderdelen voor het getoonde stuklijstserviceartikel.  
>
> Is een artikel ingesteld als stuklijst en hebt u de stuklijst niet getoond, dan wordt hiervoor een serviceartikel gemaakt op basis van de voorwaarde serviceartikelgroep en optioneel de voorwaarde serienummers.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Starttarieven invoegen voor serviceartikelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Artikelwerkbon**.
3. Kies de serviceregel en kies vervolgens **Acties**, **Functies** en de actie **Starttarief invoegen**.  

    Er wordt een serviceregel van het type **Kosten** ingevoegd met het starttarief. Het starttarief is van toepassing op het geselecteerde serviceartikel.

## <a name="block-items-item-variants-or-specific-service-items"></a>Artikelen, artikelvarianten of specifieke serviceartikelen blokkeren

U kunt voorkomen dat artikelen, artikelvarianten of serviceartikelen worden gebruikt in servicebeheertransacties, zoals servicecontracten, serviceorders en servicefacturen. Dit kan handig zijn als u de beschikbaarheid van bepaalde artikelen of serviceartikelen voor servicedoeleinden wilt beperken, bijvoorbeeld vanwege stopgezette ondersteuning, beperkte voorraad of contractuele overeenkomsten.

Als u wilt voorkomen dat een artikel of een artikelvariant wordt gebruikt in servicebeheertransacties, schakelt u de schakelaar **Service geblokkeerd** in op de pagina **Artikelkaart**, **Artikelvarianten** en **Artikelvariantkaart** . U kunt dit veld ook instellen op de pagina **Artikelsjabloon** , waarna het wordt gekopieerd naar de artikelen die op basis van die sjabloon worden gemaakt.

Een artikel of een artikelvariant waarvoor service is geblokkeerd, kan niet worden geselecteerd op de volgende pagina's:

- Serviceregel (behalve voor servicecreditnota's, waar u een melding ziet dat het artikel of de variant is geblokkeerd, maar wel is toegestaan ​​op dit type document)
- Serviceartikel
- Servicecontractregel
- Standaardserviceregel

Als u handmatig een artikelnummer of variant invoert die is geblokkeerd, krijgt u de volgende foutmelding: 'Het veld bevat een waarde die niet kan worden gevonden in de gerelateerde tabel.'

Als u bovendien servicecontracten, servicecontractoffertes of serviceorders hebt die geblokkeerde serviceartikelen of artikelvarianten bevatten, kunt u de volgende acties niet gebruiken:

- **Vergrendelen** of **Contract maken** op de pagina **Servicecontractofferte**.
- **Contract vergrendelen**, **Contract ondertekenen**, **Contractserviceorders maken** of **Contractfacturen maken**  op de pagina **Servicecontract**.
- **Order maken** op de pagina **Serviceofferte**.
- **Vrijgeven voor verzending** of **Boeken** op de pagina **Serviceorder**.
- **Boeken** op de pagina **Servicefactuur**.

### <a name="block-a-service-item"></a>Een serviceartikel blokkeren

Als u wilt voorkomen dat een serviceartikel wordt gebruikt in servicebeheertransacties, kiest u op de pagina **Serviceartikelkaart** in het veld **Geblokkeerd** een van de volgende opties:

- **Servicecontract**: blokkeer het serviceartikel voor gebruik in servicecontracten en servicecontractoffertes, maar niet in serviceorders of andere servicedocumenten.
- **Alles**: blokkeer het serviceartikel voor gebruik in alle servicebeheertransacties, met inbegrip van servicecontracten, serviceorders of andere servicedocumenten.

Wanneer een serviceartikel is geblokkeerd, kunt u dit niet selecteren op de volgende pagina's:

- Servicecontractregel (indien geblokkeerd voor servicecontract, of alles)
- Serviceartikelregel (behalve voor servicecreditnota's, indien voor alles geblokkeerd)

Als u handmatig een serviceartikelnummer invoert voor een geblokkeerd serviceartikel, verschijnt de foutmelding: 'Het veld bevat een waarde die niet kan worden gevonden in de gerelateerde tabel.'

Als u bovendien servicecontracten, servicecontractoffertes of serviceorders hebt die geblokkeerde serviceartikelen bevatten, kunt u de volgende acties niet gebruiken:

- **Vergrendelen** en **Contract maken** op de pagina **Servicecontractoffertes** (indien geblokkeerd voor servicecontract of alles).
- **Contract vergrendelen**, **Contract ondertekenen** of **Klant wijzigen** op de pagina **Servicecontract** (indien geblokkeerd voor servicecontract of alles).
- **Order maken** op de pagina **Serviceofferte** (indien voor alles geblokkeerd).
- **Vrijgeven voor verzending** of **Boeken** op de pagina **Serviceorder** (indien voor alles geblokkeerd). Als serviceorderdocumenten meerdere serviceartikelen bevatten en sommige zijn geblokkeerd en andere niet, kunt u niet-geblokkeerde regels vrijgeven en boeken. Overweeg of u de schakelaar **Eén serviceartikelregel/order** op de pagina **Servicebeheer instellen**  wilt inschakelen.
- **Boeken** op de pagina **Servicefactuur** (indien voor alles geblokkeerd).

U kunt de geblokkeerde serviceartikelen ook bekijken door een filter toe te passen op de volgende rapporten:

- Serviceartikelen (rapport 5935)
- Serviceart. buiten garantie (rapport 5937)
- Servicewinst (Serviceart.) (rapport 5938)

### <a name="data-upgrade"></a>Gegevensupgrade

Voor deze functie zijn geen aanvullende instellingen vereist. Bij het upgraden van uw [!INCLUDE [prod_short](includes/prod_short.md)], moet u echter rekening houden met het volgende:

- Als u artikelen, artikelvarianten of artikelsjablonen hebt waarbij de schakelaar **Verkoop geblokkeerd** is ingeschakeld, wordt het veld **Service geblokkeerd** ook ingeschakeld voor die records tijdens de upgrade. Dit zorgt ervoor dat de bestaande logica voor het blokkeren van verkopen ook van toepassing is op servicebeheertransacties.
- Gegevensupgrades zijn alleen mogelijk als u ten minste één serviceartikel in uw bedrijf hebt, wat betekent dat u de servicebeheerfunctionaliteit gebruikt en de gegevensupgrade nodig heeft. Als u geen serviceartikelen hebt, wordt de gegevensupgrade overgeslagen en is de schakelaar **Service geblokkeerd** standaard uitgeschakeld voor alle artikelen, artikelvarianten en artikelsjablonen.

## <a name="see-also"></a>Zie ook

[Serviceartikelen en serviceartikelonderdelen instellen](service-how-setup-service-items.md)  
[CRM - Service instellen](service-setup-service.md)  
[Servicebeheer](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
