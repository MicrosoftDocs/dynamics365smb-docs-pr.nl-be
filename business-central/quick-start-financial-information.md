---
title: Snelstartgids Financiële informatie
description: Bereid uw bedrijf voor op zaken door de financiële informatie in Business Central in te stellen.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: a-reishima
---

# <a name="financial-information-quick-start" />Snelstartgids Financiële informatie

Na het invoeren van basisbedrijfsinformatie in [!INCLUDE[prod_short](includes/prod_short.md)] is een van de volgende stappen het invullen van het financiële gedeelte. Dit doet u niet alleen om betalingen te ontvangen of te doen, maar ook om de cijfers van uw bedrijf goed te beheren en te rapporteren.

## <a name="the-chart-of-accounts" />Het rekeningschema

Het rekeningschema biedt een overzicht van de financiën van het bedrijf, waarbij rekeningen worden opgesomd in gestructureerde groepen zoals activa, passiva, inkomsten, kosten van verkochte goederen en uitgaven. [!INCLUDE[prod_short](includes/prod_short.md)] bevat een standaardrekeningschema dat u kunt aanpassen aan de boekhoudpraktijken van uw bedrijf.

## <a name="set-up-the-chart-of-accounts" />Het rekeningschema instellen

De volgende video laat zien hoe u het rekeningschema instelt in [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts" />Een rekening toevoegen aan het rekeningschema

Als u een rekening wilt toevoegen die standaard niet wordt opgenomen in [!INCLUDE[prod_short](includes/prod_short.md)], bijvoorbeeld tuinonderhoud, volgt u deze stappen:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.
2. Kies de actie **Nieuw** om de pagina **Grootboekrekening** te openen.
3. Voer de volgende gegevens in de corresponderende velden in op het sneltabblad **Algemeen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Veld | Gegevens |
   | --- | --- |
   | **Nr.** | 61250 |
   | **Naam** | Tuinonderhoud |
   | **Winst en verlies/Balans** | Resultatenrekening |
   | **Rekeningcategorie** | Onkosten |
   | **Rekeningsubcategorie** | Reparatie- en onderhoudskosten |
   | **Debet/Credit** | Beide |
   | **Rekeningsoort** | Boeking |

4. Voer op het sneltabblad **Boeking** de volgende gegevens in:

   | Veld | Gegevens |
   | --- | --- |
   | **Alg. boekingssoort** | Inkoop |
   | **Bedrijfsboekingsgroep** | Binnenland |
   | **Prod.-boekingsgroep** | Services |

5. Vul indien nodig de overige velden op de pagina **Grootboekrekening** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts" />Een overzicht krijgen van het rekeningschema

Als u een compacter overzicht van het rekeningschema nodig hebt, zonder kolommen voor boekingsgroepen, boekingstype of kostensoort, bijvoorbeeld, geeft het **Overzicht rekeningschema** de belangrijkste informatie voor elke rekening weer in een kleinere tabel. Bovendien kunt u groepen samenvouwen of uitvouwen om de accounts erin te verbergen.

Om het overzicht weer te geven kiest u de actie **Overzicht van rekeningschema** op de pagina **Rekeningschema**, of zoekt u de functie met ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen").

Lees meer over het rekeningschema en het grootboek op [Het grootboek en het rekeningschema](finance-general-ledger.md).

## <a name="set-up-bank-accounts" />Bankrekeningen instellen

Bankrekeningen in [!INCLUDE[prod_short](includes/prod_short.md)] registreren banktransacties en zijn gekoppeld aan boekingen in het rekeningschema. De volgende video laat zien hoe u bankrekeningen instelt.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Bankrekeningen** de actie **Nieuw**.
3. In het veld **Nr.** wordt automatisch een identificatie, zoals *B010*, ingevoerd als er een genummerde reeksenlijst is ingesteld voor bankrekeningen. Als dit niet het geval is, voert u een unieke combinatie in.

   Het veld verschilt van het veld **Bankrekeningnr.**, dat ook beschikbaar is op het sneltabblad **Algemeen**.
4. Vul indien nodig de velden op de pagina **Bankrekeningkaart** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learnlearnpathsset-up-financial-management-dynamics--business-central" />Zie gerelateerde training op [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also" />Zie ook

[Het rekeningschema instellen](finance-setup-chart-accounts.md)  
[Bankrekeningen instellen](bank-how-setup-bank-accounts.md)  
[Rapporten uitvoeren en afdrukken](ui-work-report.md)  
[Snelstartgidsen voor Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
