---
title: Kosten toewijzen aan intercompany-partners | Microsoft Docs
description: Lees hoe btw-instellingen voor klanten en leveranciers bepalen of en hoe btw wordt berekend.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners"></a>Kosten toewijzen aan intercompany-partners
Wanneer u intercompany-boekingen gebruikt om documenten tussen partnerbedrijven over te dragen, bepalen de btw-instellingen (voornamelijk de btw-bedrijfsboekingsgroep) die zijn toegewezen aan de klant- of leveranciersrekeningen (gekoppeld aan de intercompany-partner) of en hoe btw wordt berekend en geregistreerd. U kunt ook kostendistributies rechtstreeks vanuit een inkooporder naar partnerbedrijven uitvoeren. Als u bijvoorbeeld een inkoopfactuur van een externe leverancier registreert en u een deel of alle kosten wilt verdelen over een of meer intercompany-partners.

U kunt kosten toewijzen aan een of meer intercompany-partners met behulp van het volgende:

* **Intercompany-dagboeken** - Deze dagboeken zijn handig bij het afnemen van een service. Bijvoorbeeld wanneer een moederbedrijf een dienst inhuurt om computersystemen in twee dochterondernemingen op te zetten. De factuur wordt naar het moederbedrijf gestuurd, maar de kosten worden toegewezen aan de intercompany-partners. Zie voor meer informatie [Werken met Intercompany-documenten en -dagboeken](intercompany-how-work-documents-journals.md).
* Inkooporders en facturen - Het gebruik van inkoopdocumenten is handig wanneer de inkoopfuncties van bijvoorbeeld bedrijfskosten gecentraliseerd zijn in één bedrijf en vervolgens worden toegewezen aan de intercompany-partners.

## <a name="to-allocate-costs-using-an-intercompany-general-journal"></a>Kosten toewijzen met behulp van een intercompany-dagboek
Volg deze stappen om een regel in een intercompany-dagboek in te voeren. 

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Intercompany-dagboek** in en kies vervolgens de gerelateerde koppeling.
2. Voer indien nodig in het veld **Extern documentnr.** het documentnummer in op de factuur van de leverancier.
3. Kies in het veld **Documentsoort** **Factuur**.
4. Kies **Leverancier** in het veld **Rekeningsoort** .
5. Kies de leverancier in het veld **Rekeningnr.**.
6. Voer in het veld **Bedrag** een negatief bedrag in dat gelijk is aan het bedrag op de factuur.
7. Geef **Grootboekrekening** op in het veld **Tegenrekeningsoort**.
8. Kies in het veld **Tegenrekeningnr.** de tegenrekening die u wilt gebruiken.
9. Volg deze stappen om kosten toe te wijzen aan intercompany-partners:
   1. Een nieuwe regel maken.
   2. Verlaat het veld **Documentsoort**, kies de optie die het veld leeg laat.
   3. Voer in het veld **Documentnummer** een nummer in dat verschilt van het nummer in het veld **Extern documentnr.**. De kostentoewijzing wordt als een andere transactie beschouwd.
   4. Kies **IC-partner** in het veld **Rekeningsoort** .
   5. Kies in het veld **Rekeningnr.** de intercompany-partner waaraan u de kosten wilt toewijzen.
   6. Kies **Grootboekrekening** in het veld **Tegenrekeningsoort**.
   7. Kies in het veld **Tegenrekeningnr.** de grootboekrekening waarnaar u het bedrag wilt boeken dat u van de intercompany-partner ontvangt.
   1. Voer in het veld **Bedrag** het bedrag in van de factuur die u aan de intercompany-partner wilt toewijzen.
   1. Kies in het veld **Grootboekrekeningnr. IC-partner** de grootboekrekening waarnaar u het bedrag voor de intercompany-partner wilt boeken. 
   1. Vul indien nodig de resterende velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Herhaal deze stappen voor elke intercompany-partner die in de kosten moet delen.
1. Kies om het document te boeken en de kosten toe te wijzen **Boeken**.  

## <a name="to-allocate-costs-using-a-purchase-document"></a>Kosten toewijzen met behulp van een inkoopdocument
De volgende procedure beschrijft hoe u kosten kunt toewijzen met behulp van een inkoopfactuur. De stappen zijn hetzelfde voor inkooporders.

> [!NOTE]
> Om deze stappen te voltooien moet u de pagina **Inkoopfactuur** personaliseren door de velden **IC-partnercode**, **IC-partnerreferentiesoort** en **IC-partner** toe te voegen. Zie voor meer informatie [Een pagina personaliseren via de banner Personaliseren](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") Voer **Inkoopfactuur** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Grootboekrekening** in het veld **Soort**.
   
   Grootboekrekening is de enige optie die u kunt gebruiken om kosten toe te wijzen.  
1. Kies in het veld **Nr.** de grootboekrekening waarnaar u wilt boeken.
1. Kies in het veld **IC-partnercode** de intercompany-partner waaraan u de kosten wilt toewijzen.
1. Kies in het veld **IC-partnerreferentiesoort** de grootboekrekening die u voor de toewijzing wilt gebruiken. Dit account zal de onkosten toewijzen aan een account in het rekeningschema van de intercompany-partner.
1. Geef in het veld **Aantal** het aantal eenheden op dat aan de intercompany-partner moet worden doorberekend.
1. Voer in het veld **Directe kostprijs Excl. btw (of Incl. btw)** de kosten per artikel in die aan de intercompany-partner moeten worden doorberekend.
1. Vul indien nodig de resterende velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Kies om de inkooporder te plaatsen **Boeken**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners"></a>De toegewezen kosten naar intercompany-partners verzenden
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **IC-outboxtransacties** in en kies de gerelateerde koppeling.
2. Kies regels om te verzenden en kies vervolgens de actie **Verzenden naar IC-partner**. 
3. Om de kosten toe te wijzen kiest u de actie **Regelacties voltooien**.

## <a name="calculating-vat-for-cost-distributions"></a>Btw berekenen voor kostendistributies
Wanneer u een document gebruikt om kosten over intercompany-partners te verdelen, moet u rekening houden met twee btw-instellingen: 
* De instellingen op de grootboekrekening voor uitgaven:
   * Als de algemene zakelijke of btw-bedrijfsboekingsgroepen zijn ingesteld op de grootboekrekening, is de berekening afhankelijk van de groepen en de productgroepen uit de documentregel.
   * Als de algemene bedrijfs- of btw-bedrijfsboekingsgroepen niet op de grootboekrekening zijn opgegeven, hangt de berekening af van het volgende:
* De boekingsgroepinstellingen van de intercompany-partner
   * Of de intercompany-partner is toegewezen aan een klantnummer waarvoor geen algemene bedrijfs- of btw-bedrijfsboekingsgroepen zijn opgegeven.
   * Er is geen klantnummer gekoppeld aan de intercompany-partner. Dan zijn de algemene bedrijfs- of btw-bedrijfsboekingsgroepen leeg en wordt de regel in de btw-boekingsinstellingen gebruikt, wat meestal een groep is waarin 0% btw is opgegeven.

> [!NOTE]
> Het is belangrijk om zowel de instelling van de intercompany-partner als de instelling van de grootboekrekening (voor de onkostenrekening die wordt gebruikt voor de kostendistributie) te valideren voordat u kosten toewijst aan intercompany-partners.

## <a name="see-also"></a>Zie ook
[Intercompany instellen](intercompany-how-setup.md)  
[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
