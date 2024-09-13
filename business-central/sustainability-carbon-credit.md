---
title: Werken met koolstofkredieten
description: Leer hoe u CO2-krediet kunt instellen en kopen.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, carbon, credit, CO2'
ms.search.form: null
ms.date: 08/20/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# <a name="work-with-carbon-credit"></a>Werken met koolstofkrediet

Wanneer bedrijven om verschillende redenen hun uitstoot niet kunnen verminderen, kunnen ze koolstofkredieten kopen om hun uitstoot te compenseren. Door koolstofkredieten te kopen, kan een bedrijf nog steeds dezelfde hoeveelheid gassen uitstoten en toch CO2-neutraal blijven. Deze credits worden gekocht bij gespecialiseerde leveranciers, waardoor emissiereducties worden gestimuleerd.  

Over het algemeen zijn koolstofkredieten vergunningen waarmee de eigenaar een bepaalde hoeveelheid koolstofdioxide (CO₂) of andere broeikasgassen (BKG's) mag uitstoten. Eén koolstofkrediet vertegenwoordigt doorgaans het recht om één ton CO₂ of een equivalente hoeveelheid van een ander broeikasgas uit te stoten. Daarom is het belangrijk om deze optie voor sommige organisaties mogelijk te maken.  

## <a name="set-up-the-carbon-credit"></a>Stel de koolstofkrediet in

Koolstofkrediet in [!INCLUDE[prod_short](includes/prod_short.md)] kan worden ingesteld als het **item**. Om het **item** in te stellen als een koolstofkrediet, volgen volgt u de volgende stappen:
  
1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en selecteer vervolgens de gerelateerde koppeling. 
2. [Maak een nieuw item aan zoals uitgelegd](inventory-how-register-new-items.md).   
3. Zodra het item is aangemaakt, selecteert u het veld  **GHG Credit** op het sneltabblad  **Duurzaamheid**  en voegt u de waarde van het koolstofkrediet toe met behulp van het veld  **Koolstofkrediet per maateenheid** .

> [!NOTE]
> **Koolstofkrediet per UOM** vertegenwoordigt de hoeveelheid CO₂ in de meeteenheid die is geconfigureerd in de **Emissie-meeteenheidcode** in de **Duurzaamheidsinstelling**. Dit betekent dus dat de totale waarde van de koolstofkredieten wordt uitgedrukt in de hoeveelheid toegekende CO₂ per **basiseenheid van meting** gebruikt item.  

> [!NOTE]
> U kunt elk type item, of het nu inventaris, service of niet-inventaris is, instellen als een CO2-krediet.  

## <a name="to-purchase-carbon-credit"></a>Om koolstofkrediet te kopen

### <a name="purchase-documents"></a>Inkoopdocumenten

Om met aankoopgerelateerde documenten te werken, volgt u de volgende stappen: volgen

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram en:  
   1. Voer  **Aankoopfacturen** in als u de factuur als  **documenttype** wilt verzenden en selecteer vervolgens de gerelateerde koppelen.  
   2. Voer  **Inkooporders** in als u wilt bestellen als **documenttype** en selecteer vervolgens de gerelateerde koppelen.   
2. Vul de documentkoptekst in op basis van de volgende instructies [over het werken met inkoopfacturen en orders](purchasing-how-record-purchases.md). 
3. Kies het item configureren als een koolstofkrediet in het  **nr.** Veld in de inkoopdocumentregels en voeg de juiste **hoeveelheid** en **Directe eenheidskosten** toe. 
4. Voeg het **Duurzaamheidsrekeningnummer** toe dat u zou gebruiken om uw koolstofdioxidewaarde (CO₂) te verlagen. Het systeem vult automatisch de waarde in het veld  **CO2-uitstoot** in op basis van de waarde die u hebt geconfigureerd in het veld  **Koolstofkrediet per maateenheid** in het  **artikel** kaart.
5. U boekt het document.

> [!NOTE]
> Hoewel koolstofkredieten de waarde van de inzendingen zullen verlagen, zult u een positieve hoeveelheid waarde zien in de **CO2-uitstoot**. Maar zodra u het document post, ziet u een waarde met een negatieve log in de **Sustainability Ledger Entry** met de **GHG Credit** als een **document Type**.  

### <a name="sustainability-journals"></a>Duurzaamheidsdagboeken

Om te werken met **Sustainability Journal** volgen zijn de volgende stappen nodig:  

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsdagboek** in en selecteer vervolgens de gerelateerde koppeling. 
2. Voer op de pagina  **Duurzaamheidsdagboek** zoveel regels in als u in dezelfde batch wilt posten.  
3. Selecteer het **GHG-krediet** in het veld **documenttype** .    
4. In het veld **Rekeningnr.** kunt u alleen niet-geblokkeerde duurzaamheidsrekeningen selecteren waarvan het veld **Directe boeking** is geselecteerd en het **Rekeningtype** is ingesteld op **Boeking**. De rekeningen moeten ook zijn geconfigureerd met een categorie en een subcategorie. Kies het juiste account om koolstofkredieten te posten.
5. Selecteer  **Handmatige invoer** en voer de waarde die u als koolstofkrediet wilt boeken in het veld  **Emissie CO2** in.  
6. Boek het dagboek.   

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)    
[Duurzaamheidsposten vastleggen](finance-sustainability-journal.md)    
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)    
[Duurzaamheidsinstelling](finance-sustainability-setup.md)   
[Duurzaamheidsrekeningschema en -grootboek](finance-sustainability-accounts-ledger.md)  
[Adhoc-analyse van duurzaamheidsgegevens](ad-hoc-analysis-sustainability.md)    
[Duurzaamheidsrapporten en analyses in [!INCLUDE[prod_short](includes/prod_short.md)]](sustainability-reports.md)   
[Duurzaamheid-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
