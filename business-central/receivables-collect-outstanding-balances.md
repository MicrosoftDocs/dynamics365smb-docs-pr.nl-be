---
title: Openstaande saldi innen
description: 'Leer hoe u uw klanten herinnert aan openstaande betalingen. Een klantenoverzicht, een aanmaning of een rentefactuur versturen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 07/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="collect-outstanding-balances"></a>Openstaande saldi innen

Tijdens het beheer van tegoeden moet u ook controleren of openstaande bedragen op tijd worden betaald. Als klanten betalingen hebben openstaan, kunt u beginnen met het rapport **Rekeningoverzicht van klant** als een herinnering te sturen. U kunt ook aanmaningen sturen.

Gebruik aanmaningen om klanten te herinneren aan openstaande bedragen. U kunt aanmaningen ook gebruiken om rentefacturen zoals rente en boetes te berekenen en deze op te nemen op de aanmaning. Gebruik rentefacturen als u klanten rente en aanmaningskosten wilt laten betalen zonder ze te herinneren aan openstaande bedragen.

## <a name="statements"></a>Afschriften

Vanaf de klantenkaart kunt u een overzicht maken met de transacties van die klant met u. Vervolgens kunt u een PDF-bestand genereren en naar de klant sturen. U kunt ook het rapport **Rekeningoverzicht van klant** gebruiken om uw klanten een overzicht van hun zaken met u te sturen. 

> [!TIP]
> Indien nodig kunt u de verklaring naar Excel sturen om wijzigingen aan te brengen.  

### <a name="to-send-the-customer-statement-report"></a>Het rekeningoverzichten van de klant verzenden

1. Kies het pictogram ![Lampje dat de functie Vertel me 10 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningoverzicht van klant** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Geef onder **Uitvoeropties** aan hoe de lijst aan het rapport aan de klant moet worden verzonden.

> [!NOTE]
> Als u meerdere valuta's gebruikt, wordt het rekeningoverzicht van de klant altijd afgedrukt in de valuta van de klant. De laatste datum in een dagafschriftperiode wordt ook gebruikt als de datum en de vervaldatum van het overzicht, indien verval is opgenomen.

## <a name="reminders"></a>Aanmaningen

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## <a name="finance-charges"></a>Financiële kosten

Wanneer een klant niet op de vervaldatum betaalt, kunt u automatisch financieringskosten laten berekenen en deze toevoegen aan de openstaande bedragen op de rekening van de klant. U kunt klanten op de hoogte stellen van de toeslagen door rentefacturen te versturen.  

> [!NOTE]  
> U gebruikt rentefacturen om rente en aanmaningskosten te berekenen en om uw klanten hiervan op de hoogte te stellen zonder ze te herinneren aan achterstallige betalingen. U kunt ook rente berekenen op achterstallige betalingen wanneer u aanmaningen maakt.  

Voordat u rentefacturen kunt maken, moet u condities instellen. Zie voor meer informatie [Rentefactuurcondities instellen](finance-setup-finance-charges.md).  

U kunt handmatig rentefacturen maken voor een afzonderlijke klant en de regels automatisch in laten vullen. U kunt ook de functie **Rentefacturen maken** gebruiken om rentefacturen te maken voor alle of geselecteerde klanten met achterstallige saldo's.  

Nadat u de rentefacturen hebt gemaakt, kunt u ze aanpassen. De tekst die wordt afgedrukt aan het begin of eind van de rentefactuur wordt bepaald door de rentefactuurtermijnen en kan worden bekeken in de kolom **Omschrijving** in de regels. Als er automatisch een berekend bedrag in de begin- of eindtekst is ingevoegd, wordt de tekst niet aangepast als u regels verwijdert. In dat geval moet u de functie **Rentefactuurtekst bijwerken** gebruiken.  

Nadat u de rentefacturen hebt gemaakt en eventuele aanpassingen hebt gedaan, kunt u testrapporten afdrukken of de rentefacturen versturen, meestal via e-mail.

### <a name="to-create-a-finance-charge-memo-manually"></a>Handmatig rentefacturen maken

Een rentefactuur is te vergelijken met een factuur. U kunt een kop handmatig en de regels automatisch invullen of u kunt automatisch rentefacturen voor alle klanten maken.

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in.  
3. Kies de actie **Rentefactuurregels voorstellen**.
4. Stel op de pagina **Rentefactuur** een filter in op het sneltabblad **Klantenpost** als u alleen rentefacturen voor specifieke posten wilt maken.

    > [!NOTE]
    > Hoewel ze worden vermeld heeft het selecteren van **Betaling** en **Creditnota** als **Documentsoort**-filters geen effect omdat de functie **Rentefactuurregels voorstellen** alleen positieve bedragen verwerkt.
5. Kies **OK** om de batchverwerking te starten.  

### <a name="to-update-finance-charge-memo-texts"></a>De rentefactuurteksten bijwerken

In sommige gevallen wilt u wellicht de begin- en eindtekst wijzigen die u voor de financieringskostenvoorwaarden hebt ingesteld. Als u dat doet op een moment waarop u de rentefacturen hebt gemaakt, maar nog niet hebt verzonden, kunt u de facturen bijwerken met de gewijzigde tekst.

1. Kies het pictogram ![Lampje dat de functie Vertel me 3 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefactuur** in en kies vervolgens de gerelateerde koppeling.  
2. open de rentefactuur waarvoor u tekst wilt wijzigen en kies vervolgens de actie **Rentefactuurtekst bijwerken**.
3. Op de pagina **Rentefactuurtekst bijwerken** kunt u een filter instellen als u verschillende facturen wilt bijwerken.
4. Klik op **OK** om de begin- en eindtekst bij te werken.  

### <a name="to-issue-finance-charge-memos"></a>Rentefacturen verzenden

Nadat u de rentefacturen hebt gemaakt en eventuele aanpassingen hebt aangebracht, kunt u testrapporten afdrukken of de rentefacturen versturen.

Wanneer een aanmaning wordt verzonden, worden de posten geboekt volgens uw specificaties op de pagina **Rentefactuurcondities**. Op basis van deze specificatie wordt bepaald welke rente en/of toeslagen worden geboekt naar de klantenrekening en het grootboek. De instellingen op de pagina **Klantboekingsgroepen** bepalen naar welke rekenen rente of kosten worden geboekt.

Voor elke klantenpost op de rentefactuur wordt een post gemaakt op de pagina **Aanmanings-/rentefactuurposten**.

Als de selectievakjes **Rente boeken** of **Toeslag boeken** op de pagina **Rentefactuurcondities** zijn ingeschakeld, worden ook de volgende posten gemaakt:

- Eén post op de pagina **Klantenposten**
- Eén debiteurenpost in de desbetreffende grootboekrekening
- Eén rentepost en/of één toeslagpost in de desbetreffende grootboekrekening

Daarnaast kunnen btw-posten worden gemaakt als u de rentefactuur verzendt.

1. Kies het pictogram ![Lampje dat de functie Vertel me 4 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefacturen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de desbetreffende rentefactuur en kies vervolgens de actie **Verzenden**.
3. Vul op de pagina **Rentefacturen verzenden** de benodigde velden in.
4. Kies de knop **Ok**.

De financieringskostennota wordt afgedrukt of als PDF-bijlage naar het opgegeven e-mailadres verzonden.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Een verzonden rentefactuur annuleren

Als financiële kostennota's per ongeluk zijn uitgegeven, kunt u ze Annuleren voordat ze opnieuw worden verzonden. U kunt dit één voor één of als batch doen.

1. Selecteer op de pagina **Verzonden rentefacturen** een of meer regels voor verzonden rentefacturen die u wilt annuleren en kies vervolgens de actie **Annuleren**.
2. Vul op de pagina **Verzonden rentefacturen annuleren** desgewenst de velden in en kies vervolgens de knop **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Aanmanings- en renteposten weergeven

Zodra u een aanmaning verzendt, wordt op de pagina **Aanmanings-/renteposten** een aanmaningspost gemaakt voor elke aanmaningsregel met een klantenpost. U kunt vervolgens in een overzicht weergeven welke aanmaningsposten u voor een bepaalde klant hebt gemaakt.

1. Kies het pictogram ![Lampje dat de functie Vertel me 5 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Posten**.
3. Selecteer op de pagina **Klantenposten** de regel met de post waarvan u de aanmaningsposten wilt weergeven, en kies de actie **Aanmanings-/rentefactuurposten**.

## <a name="multiple-interest-rates"></a>Meerdere rentepercentages

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Zie voor meer informatie [Meerdere rentepercentages instellen](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-also"></a>Zie ook

[Termijnen, niveaus en tekst van aanmaningen instellen](finance-setup-reminders.md)  
[Rentefactuurcondities instellen](finance-setup-finance-charges.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
