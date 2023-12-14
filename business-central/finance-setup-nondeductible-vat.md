---
title: Niet-aftrekbare btw instellen
description: In dit artikel wordt uitgelegd hoe u niet-aftrekbare btw configureert in Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="set-up-non-deductible-vat"></a>Niet-aftrekbare btw instellen

Niet-aftrekbare btw is de btw die een koper moet betalen, maar die niet aftrekbaar is van de eigen btw-aansprakelijkheid van de koper. Bedrijven kunnen btw meestal terugkrijgen op de aankoop van goederen en diensten die verband houden met hun bedrijfsactiviteiten. In sommige situaties betaalt een bedrijf echter btw die niet aftrekbaar is. Deze situaties houden meestal verband met de lokale regelgeving en kunnen tussen landen/regio's verschillen. Het model van het gebruik van niet-aftrekbare of gedeeltelijk aftrekbare btw is echter vergelijkbaar. U kunt de proportionele btw gebruiken om de btw te berekenen wanneer er sprake is van aftrekbare en niet-aftrekbare btw.

Over het algemeen kan de btw voor sommige aankopen niet worden afgetrokken vanwege de volgende factoren:

- **Het type goederen of diensten dat wordt gekocht** – btw is geheel of gedeeltelijk niet-aftrekbaar op grond van een wettelijke bepaling over goederen zoals auto's, mobiele telefoons en voedsel dat in restaurants wordt gekocht.
- **Gedeeltelijk aftrekbare pro rata btw**: btw wordt pro rata berekend volgens de verhouding tussen de verkooptransacties waarvoor btw verschuldigd is en alle verrichtingen die zijn uitgevoerd. Btw die dit percentage overschrijdt, is niet aftrekbaar.

Omdat het moeilijk kan zijn om te weten waar en hoe een artikel wordt gebruikt, moet u op basis van historische gegevens contact opnemen met de lokale belastingdienst in uw land/regio om te bepalen of een bepaald percentage van de btw aftrekbaar is. 

> [!IMPORTANT]
> Deze wereldwijde functie is beschikbaar in alle landen/regio's met ingeschakelde btw, **behalve in België, Italië en Noorwegen**. Deze lokalisaties hebben al een bestaande lokale functie en zullen in de toekomst worden bijgewerkt. Gebruik deze functie niet in deze landen/regio's omdat de upgradeprocedure niet bestaat.

## <a name="use-non-deductible-vat"></a>Niet-aftrekbare btw gebruiken

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-instelling** in en selecteer vervolgens de gerelateerde koppeling.
2. Schakel het selectievakje **Niet-aftrekbare btw inschakelen** in.

    > [!IMPORTANT]
    > Nadat u niet-aftrekbare btw hebt ingeschakeld, kunt u deze niet meer uitschakelen, omdat de functie wijzigingen in gegevens kan bevatten en een upgrade van sommige databasetabellen kan initiëren. Microsoft raadt ten zeerste aan om deze functie eerst in te schakelen en te testen in de sandbox-omgeving voordat u deze inschakelt in de productieomgeving.

3. Configureer hoe het systeem niet-aftrekbare btw-waarden zal behandelen.

    1. Geef in het veld **Gebruiken voor artikelkosten** aan of de niet-aftrekbare btw moet worden toegevoegd aan de artikelkosten wanneer u artikelen koopt. Anders heeft de niet-aftrekbare btw geen invloed op de artikelprijs en wordt het volledige bedrag alleen op grootboekniveau geboekt.
    2. Schakel het selectievakje **Gebruiken voor kosten van vaste activa** in om de niet-aftrekbare btw toe te voegen aan de kosten van vaste activa wanneer u nieuwe vaste activa aanschaft. Anders heeft de niet-aftrekbare btw geen invloed op de VA-kosten en wordt het volledige bedrag alleen op grootboekniveau geboekt.
    3. Schakel het selectievakje **Gebruiken voor projectkosten** in om op te geven dat de niet-aftrekbare btw moet worden opgeteld bij de projectkosten wanneer u artikelen voor het project aanschaft. Anders heeft de niet-aftrekbare btw geen invloed op de projectkosten en wordt het volledige bedrag alleen op grootboekniveau geboekt.
    4. Schakel het selectievakje **Niet-aftrekbare btw weergeven op regels** in om op te geven dat de niet-aftrekbare btw op documentregelpagina's moet worden weergegeven om btw-bedragen gemakkelijker te manipuleren.

## <a name="use-the-non-deductible-vat-percentage"></a>Het niet-aftrekbare btw-percentage gebruiken

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-boekingsgroepinstellingen** in en selecteer vervolgens de gerelateerde koppeling.
2. Stel op de pagina **Btw-boekingsgroepinstellingen** de velden in, zoals is beschreven in de volgende tabel.

    | Veld | Omschrijving |
    |-------|-------------|
    | Niet-aftrekbare btw toestaan | Geef op of met de niet-aftrekbare btw rekening wordt gehouden voor de huidige combinatie van een btw-bedrijfsboekingsgroep en btw-productboekingsgroep. |
    | Niet-aftrekbaar btw-percentage | Geef het percentage op van het transactiebedrag waarop geen btw in rekening wordt gebracht. |
    | Rekening niet-aftrekbare btw inkoop | Geef de rekening op die is gekoppeld aan het btw-bedrag dat niet wordt afgetrokken vanwege het aangeschafte type goederen of services. |

    > [!NOTE]
    > Als u wilt dat grootboekposten (G/L) de speciale rekening gebruiken in plaats van de verkoop-/inkooprekening, kunt u het veld **Niet-aftrekbare btw-aankooprekening** leeg laten of het veld **Grootboekrekening** instellen.

3. Selecteer **OK**.

> [!NOTE]
> U kunt niet-gerealiseerde btw niet samen met niet-aftrekbare btw gebruiken.
>
> Gebruik niet dezelfde **Btw-identificatie** voor zowel normale btw waarbij het veld **Niet-aftrekbaar btw-percentage** is ingesteld op **0** (nul) als voor normale btw waarbij het veld **Niet-aftrekbaar btw-percentage** is ingesteld op een waarde die niet gelijk is aan nul. Anders wordt het totale niet-aftrekbare btw-bedrag verkeerd berekend.

## <a name="see-also"></a>Zie ook

[Financieel beheer](finance.md)  
[Ontwerpdetails: Niet-aftrekbare btw](design-details-nondeductible-vat.md)  
[Niet-aftrekbare btw gebruiken](finance-how-use-non-deductible-vat.md)  
[Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
