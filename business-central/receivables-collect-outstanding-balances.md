---
title: Openstaande saldi innen
description: Leer hoe u een aanmaning aan een klant verzendt over een betaling die achterstallig is, en kosten aan de betaling toevoegt voor de vertraging.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c59ce4576f4c7916ef6b587d4bc6b21cb1047acb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781775"
---
# <a name="collect-outstanding-balances"></a>Openstaande saldi innen

Tijdens het beheer van tegoeden moet u ook controleren of openstaande bedragen op tijd worden betaald. Als klanten betalingen hebben openstaan, kunt u beginnen met het rapport **Rekeningoverzicht van klant** als een herinnering te sturen. U kunt ook aanmaningen sturen.

U kunt aanmaningen gebruiken om klanten te herinneren aan openstaande bedragen. U kunt aanmaningen ook gebruiken om rentefacturen zoals rente en boetes te berekenen en deze op te nemen op de aanmaning. Gebruik rentefacturen als u klanten rente en aanmaningskosten wilt laten betalen zonder ze te herinneren aan openstaande bedragen.

## <a name="statements"></a>Afschriften

Vanaf de klantenkaart kunt u een overzicht maken met de transacties van die klant met u. Vervolgens stuurt u de klant het gegenereerde pdf-bestand. U kunt ook het rapport **Rekeningoverzicht van klant** gebruiken om uw klanten een overzicht van hun zaken met u te sturen. Het klantoverzicht kan naar Excel worden gestuurd voor verdere verwerking.  

### <a name="to-send-the-customer-statement-report"></a>Het rekeningoverzichten van de klant verzenden

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningoverzicht van klant** in en kies de desbetreffende koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Geef onder **Uitvoeropties** aan hoe de lijst aan het rapport aan de klant moet worden verzonden.

> [!NOTE]
> Als u meerdere valuta's gebruikt, wordt het rekeningoverzicht van de klant altijd afgedrukt in de valuta van de klant. De laatste datum in een dagafschriftperiode wordt ook gebruikt als de datum en de vervaldatum van het overzicht, indien verval is opgenomen.

## <a name="reminders"></a>Aanmaningen

Voor u aanmaningen kunt maken, moet u aanmaningscondities instellen en deze toewijzen aan uw klanten. Zie voor meer informatie [De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] De inhoud van de pagina **Rentefactuurcondities** bepaalt of er rente in rekening wordt gebracht op de aanmaning.  

U kunt de batchverwerking **Aanmaningen maken** periodiek uitvoeren om aanmaningen te maken voor alle klanten met achterstallige saldo's, of u kunt handmatig een aanmaning maken voor een specifieke klant en de regels automatisch laten uitrekenen en invullen.  

Nadat u de aanmaningen hebt gemaakt, kunt u ze aanpassen. De tekst die wordt afgedrukt aan het begin of eind van een aanmaning wordt bepaald door de aanmaningscondities en kan worden bekeken in de kolom **Omschrijving**. Als een berekend bedrag automatisch is ingevoegd in de begin-, of eindtekst, wordt de tekst niet aangepast wanneer u regels verwijdert. In dat geval moet u de functie **Aanmaningstekst bijwerken** gebruiken.  

Voor een klantpost waarbij het veld **Afwachten** is ingevuld wordt geen aanmaning gemaakt. Als er echter een aanmaning wordt gemaakt op basis van een andere post, wordt een wachtende post ook opgenomen op de aanmaning. Er wordt geen rente berekend op regels met deze posten.

Nadat u aanmaningen hebt gemaakt en eventuele aanpassingen hebt gedaan, kunt u testrapporten afdrukken of de aanmaningen versturen, meestal als e-mail.

### <a name="to-create-a-reminder-automatically"></a>Automatisch een aanmaningen maken

Een herinnering is te vergelijken met een factuur. Wanneer u een aanmaning maakt, moeten een aanmaningskop, evenals een of meer aanmaningsregels, worden ingevuld. U kunt een functie gebruiken om automatisch aanmaningen te maken voor alle klanten.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies de desbetreffende koppeling.
2. Kies op de pagina **Aanmaning** de actie **Aanmaningen maken**.
3. Vul op de pagina **Aanmaningen maken** de velden in om te definiëren hoe en naar wie de aanmaningen worden gemaakt.
4. Kies de knop **OK**.

### <a name="to-create-a-reminder-manually"></a>Handmatig aanmaningen maken

Op de pagina **Aanmaning** kunt u het sneltabblad **Algemeen** handmatig invullen en de regels vervolgens automatisch laten invullen.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies de desbetreffende koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op het sneltabblad **Algemeen** in.
4. Kies de actie **Aanmaningsregels voorstellen**.
5. Vul in de batchverwerking **Aanmaningsregels voorstellen** de velden in om te definiëren hoe en naar wie de aanmaningen worden gemaakt.
6. Schakel het selectievakje **Wachtende posten opnemen** in als ook u wachtende, openstaande posten wilt opnemen in de aanmaningen.
7. Schakel het selectievakje **Alleen vervallen posten** in als u alleen vervallen, open posten wilt opnemen in de aanmaningen. Alleen facturen en betalingen worden weergegeven, aangezien dit de posten zijn waarvoor betalingen van uw klanten mogelijk te laat zijn.

    > [!Important]
    > Open posten die in de wacht staan, worden ingevoegd, ongeacht de instelling van het selectievakje **Alleen vervallen posten**.

8. Kies de knop **OK**.

### <a name="to-replace-reminder-texts"></a>Aanmaningsteksten vervangen

U kunt op verschillende manieren bepalen hoe u tekst wilt weergegeven op de afgedrukte aanmaning. In sommige gevallen kunt u de begin- en eindtekst die u hebt gedefinieerd voor het huidige niveau vervangen door de tekst van een ander niveau.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies de desbetreffende koppeling.
2. Open de relevante aanmaning en kies de actie **Aanmaningstekst bijwerken**.
3. Voer op de pagina **Aanmaningstekst bijwerken** het vereiste niveau in het veld **Aanmaningsniveau** in.
4. Klik op **OK** om de begin- en eindtekst bij te werken.

### <a name="to-issue-a-reminder"></a>Een aanmaning verzenden

Nadat u aanmaningen hebt gemaakt en eventuele aanpassingen hebt gedaan, kunt u testrapporten afdrukken of de aanmaningen versturen.

Wanneer u een aanmaning verstuurt, worden de gegevens overgebracht naar een afzonderlijke pagina voor verstuurde aanmaningen. Tegelijkertijd worden aanmaningsposten geboekt. Als er rente of aanmaningskosten in rekening zijn gebracht worden posten zowel geboekt als klantpost als in het grootboek.

Wanneer een aanmaning is verzonden, worden de posten geboekt volgens uw specificaties op de pagina **Aanmaningscondities**. Op basis van deze specificatie wordt bepaald welke rente en/of toeslagen worden geboekt naar de klantenrekening en het grootboek. De instelling op de pagina **Klantboekingsgroepen** bepaalt naar welke rekening de boekingen worden uitgevoerd.

Voor elke klantenpost op de rentefactuur wordt een post gemaakt op de pagina **Aanmanings-/rentefactuurposten**.

Als de selectievakjes **Rente boeken** of **Toeslag boeken** op de pagina **Aanmaningscondities** zijn ingeschakeld, worden ook de volgende posten gemaakt:

- Eén post op de pagina **Klantenposten**
- Eén debiteurenpost in de desbetreffende grootboekrekening
- Eén rentepost en/of één toeslagpost in de desbetreffende grootboekrekening

Daarnaast kunnen btw-posten worden gemaakt als u de aanmaning verzendt.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningen** in en kies de desbetreffende koppeling.
2. Selecteer de desbetreffende aanmaning en kies vervolgens de actie **Verzenden**.
3. Vul op de pagina **Aanmaningen verzenden** de benodigde velden in.
4. Kies de knop **Ok**.

Een aanmaning wordt afgedrukt of verzonden naar een opgegeven e-mailadres als PDF-bijlage.

### <a name="to-cancel-an-issued-reminder"></a>Een verzonden aanmaning annuleren

Als aanmaningen ten onrechte zijn uitgegeven, kunt u ze annuleren voordat ze worden verzonden. U kunt dit één voor één of als een batch doen.

1. Selecteer op de pagina **Verzonden aanmaningen** een of meer regels voor verzonden aanmaningen die u wilt annuleren en kies vervolgens de actie **Annuleren**.
2. Vul op de pagina **Verzonden aanmaningen annuleren** desgewenst de velden in en kies vervolgens de knop **OK**.

## <a name="finance-charges"></a>Financiële kosten

Wanneer een klant niet op de vervaldatum betaalt, kunt u automatisch aanmaningskosten laten berekenen en die optellen bij de openstaande bedragen op de rekening van de klant. U kunt klanten op de hoogte stellen van de toeslagen door rentefacturen te versturen.  

> [!NOTE]  
> U gebruikt rentefacturen om rente en aanmaningskosten te berekenen en om uw klanten hiervan op de hoogte te stellen zonder ze te herinneren aan achterstallige betalingen. U kunt ook rente berekenen op achterstallige betalingen wanneer u aanmaningen maakt.  

Voordat u rentefacturen kunt maken, moet u condities instellen. Zie voor meer informatie [Rentefactuurcondities instellen](finance-setup-finance-charges.md).  

U kunt handmatig rentefacturen maken voor een afzonderlijke klant en de regels automatisch in laten vullen. U kunt ook de functietaak **Rentefacturen maken** gebruiken om rentefacturen te maken voor alle of geselecteerde klanten met achterstallige saldo's.  

Nadat u de rentefacturen hebt gemaakt, kunt u ze aanpassen. De tekst die wordt afgedrukt aan het begin of eind van de rentefactuur wordt bepaald door de rentefactuurtermijnen en kan worden bekeken in de kolom **Omschrijving** in de regels. Als een berekend bedrag automatisch is ingevoegd in de begin-, of eindtekst, wordt de tekst niet aangepast wanneer u regels verwijdert. In dat geval moet u de functie **Rentefactuurtekst bijwerken** gebruiken.  

Nadat u de rentefacturen hebt gemaakt en eventuele aanpassingen hebt gedaan, kunt u testrapporten afdrukken of de rentefacturen versturen, meestal via e-mail.

### <a name="to-create-a-finance-charge-memo-manually"></a>Handmatig rentefacturen maken

Een rentefactuur is te vergelijken met een factuur. U kunt een kop handmatig en de regels automatisch invullen of u kunt automatisch rentefacturen voor alle klanten maken.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefacturen** in en kies de desbetreffende koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in.  
3. Kies de actie **Rentefactuurregels voorstellen**.
4. Stel op de pagina **Rentefactuur** een filter in op het sneltabblad **Klantenpost** als u alleen rentefacturen voor specifieke posten wilt maken.

    > [!NOTE]
    > Hoewel ze worden vermeld heeft het selecteren van **Betaling** en **Creditnota** als **Documentsoort**-filters geen effect omdat de functie **Rentefactuurregels voorstellen** alleen positieve bedragen verwerkt.
5.  Kies **OK** om de batchverwerking te starten.  

### <a name="to-update-finance-charge-memo-texts"></a>De rentefactuurteksten bijwerken  
Het kan zijn dat u de begin- en eindtekst die u voor de rentefactuurcondities hebt ingesteld, wilt bijwerken. Als u dat doet op een moment waarop u de rentefacturen hebt gemaakt, maar nog niet hebt verzonden, kunt u de facturen bijwerken met de gewijzigde tekst.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefactuur** in en kies de desbetreffende koppeling.  
2. open de rentefactuur waarvoor u tekst wilt wijzigen en kies vervolgens de actie **Rentefactuurtekst bijwerken**.
3. Op de pagina **Rentefactuurtekst bijwerken** kunt u een filter instellen als u verschillende facturen wilt bijwerken.
4. Klik op **OK** om de begin- en eindtekst bij te werken.  

### <a name="to-issue-finance-charge-memos"></a>Rentefacturen verzenden
Nadat u de rentefacturen hebt gemaakt en eventuele aanpassingen hebt gedaan, kunt u testrapporten afdrukken of de rentefacturen versturen.

Wanneer een aanmaning is verzonden, worden de posten geboekt volgens uw specificaties op de pagina **Rentefactuurcondities**. Op basis van deze specificatie wordt bepaald welke rente en/of toeslagen worden geboekt naar de klantenrekening en het grootboek. De instelling op de pagina **Klantboekingsgroepen** bepaalt naar welke rekening de boekingen worden uitgevoerd.

Voor elke klantenpost op de rentefactuur wordt een post gemaakt op de pagina **Aanmanings-/rentefactuurposten**.

Als de selectievakjes **Rente boeken** of **Toeslag boeken** op de pagina **Rentefactuurcondities** zijn ingeschakeld, worden ook de volgende posten gemaakt:

- Eén post op de pagina **Klantenposten**
- Eén debiteurenpost in de desbetreffende grootboekrekening
- Eén rentepost en/of één toeslagpost in de desbetreffende grootboekrekening

Daarnaast kunnen btw-posten worden gemaakt als u de rentefactuur verzendt.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefacturen** in en kies de desbetreffende koppeling.
2. Selecteer de desbetreffende rentefactuur en kies vervolgens de actie **Verzenden**.
3. Vul op de pagina **Rentefacturen verzenden** de benodigde velden in.
4. Kies de knop **Ok**.

Een rentefactuur wordt afgedrukt of verzonden naar een opgegeven e-mailadres als PDF-bijlage.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Een verzonden rentefactuur annuleren
Als rentefacturen ten onrechte zijn uitgegeven, kunt u ze annuleren voordat ze worden verzonden. U kunt dit één voor één of als een batch doen.
1. Selecteer op de pagina **Verzonden rentefacturen** een of meer regels voor verzonden rentefacturen die u wilt annuleren en kies vervolgens de actie **Annuleren**.
2. Vul op de pagina **Verzonden rentefacturen annuleren** desgewenst de velden in en kies vervolgens de knop **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Aanmanings- en renteposten weergeven  
Zodra u een aanmaning verzendt, wordt op de pagina **Aanmanings-/renteposten** een aanmaningspost gemaakt voor elke aanmaningsregel met een klantenpost. U kunt vervolgens in een overzicht weergeven welke aanmaningsposten u voor een bepaalde klant hebt gemaakt.    
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.  
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Posten**.
3. Selecteer op de pagina **Klantenposten** de regel met de post waarvan u de aanmaningsposten wilt weergeven, en kies de actie **Aanmanings-/rentefactuurposten**.

## <a name="multiple-interest-rates"></a>Meerdere rentepercentages

Wanneer u rentefactuurcondities instelt en aanmaningscondities, als sanctie voor vertraagde betaling, kunt u meerdere rentepercentages opgeven zodat de sanctietoeslag wordt berekend op basis van verschillende rentepercentages in verschillende perioden. Als meerdere rentepercentages niet zijn ingesteld, worden het rentepercentage en de tijdsperiode die op de pagina's **Rentefactuurcondities** en **Aanmaningscondities** zijn gedefinieerd, voor de hele periode van berekening gebruikt. Zie voor meer informatie [Meerdere rentepercentages instellen](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md)  
[Rentefactuurcondities instellen](finance-setup-finance-charges.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]