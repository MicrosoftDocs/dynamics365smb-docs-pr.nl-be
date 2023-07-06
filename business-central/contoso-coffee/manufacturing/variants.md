---
title: Varianten
description: Procedure om te leren hoe u de vraagprognose bijwerkt voor elke variant van een product in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-variants"></a><a name="walkthrough-variants"></a><a name="walkthrough-variants"></a>Procedure: varianten

In dit artikel nemen we u mee door de stappen waarin u de demogegevens voor Contoso Coffee gebruikt om meer te weten te komen over varianten.

## <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Scenario

U bent de productieplanner bij Contoso Coffee. U moet de vraagprognose bijwerken voor elke variant van artikel SP-SCM1006, AutoDripLite. Omdat ze verschillende kleuren hebben, moet u ervoor zorgen dat voor elke variant de juiste stuklijst (BOM) wordt gebruikt. Voer het planningsvoorstel uit om de voorziening te berekenen.  

## <a name="steps"></a><a name="steps"></a><a name="steps"></a>Stappen

1. Stel de SKU's (voorraadhoudende eenheden) in voor artikel SP-SCM1006, AutoDripLite. Wijs een stuklijst toe voor SKU met de varianten ROOD en WIT.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer *artikelen* in en kies vervolgens de gerelateerde koppeling.  

    2. Open het artikel **SP-SCM1006, AutoDripLite**.

    3. Kies de actie **SKU maken**.  

    4. Stel het veld **Maken per** in op *Vestiging en variant*.

    5. Stel een filter voor vestiging in op *Noord* en kies vervolgens de **OK**-knop.

    6. Kies de actie **SKU's**.  

    7. Werk de productiestuklijsten bij voor de volgende SKU's:

        1. ROOD op NOORD, SP-SCM1006-RED instellen  

        2. WIT op NOORD, SP-SCM1006-WHITE instellen  

        3. Laat Productiestuklijstnr. leeg voor ZWART op NOORD  

2. Werk de productie-instellingen bij en respecteer de vraagprognose op vestigingen en varianten.  

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer *productie-instellingen* in en kies vervolgens de gerelateerde koppeling.  

    2. Schakel het veld **Prognose op vestigingen gebruiken** in.

    3. Schakel het veld **Prognose voor variant gebruiken** in.

    4. Sluit het venster **Productie-instellingen**.

3. Maak een nieuwe maandelijkse vraagprognose, *AUTODRIP*. Filter dit op het artikel SP-SCM1006 en vestiging NOORD. Stel de vraag voor mei in voor elke variant. 

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer *vraagprognose* in en selecteer vervolgens de gerelateerde koppeling.

    2. Maak een nieuwe vraagprognose met de naam *AUTODRIP*.

    3. Kies de actie **Vraagprognose bewerken**.

    4. In het veld **Weergeven per**, selecteert u *Maand*.

    5. In het veld **Artikelfilter** selecteert u *SP-SCM1006*.

    6. Schakel het veld **Prognose op vestigingen gebruiken** in.

    7. In het veld **Vestigingsfilter** selecteert u *NOORD*.

    8. Schakel het veld **Prognose voor variant gebruiken** in.

    9. Voor elke regel bijgewerkte waarden in de kolom mei

        1. ROOD op NOORD, 100 instellen

        2. WIT op NOORD, 200 instellen

        3. ZWART op NOORD, 300 instellen

    10. Vensters vraagprognose sluiten

4. Voer MPS-plan in mei uit voor gemaakte vraagprognoses. Bekijk materialen om te zien of de artikelkleur accordeert met de variant.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer *planningsvoorstel* in en kies vervolgens de gerelateerde koppeling.

    2. Kies de actie **Regeneratief plan berekenen**.

    3. Schakel het veld **MPS** in.

    4. Schakel het veld **MPS** uit.

    5. Selecteer in het veld **Begindatum** de optie *1 mei*

    6. Selecteer in het veld **Einddatum** de optie *31 mei*

    7. Selecteer in het veld **Prognose gebruiken** de optie *AUTODRIP*

    8. Kies de actie **OK**.

    9. Kies voor elke gemaakte regel de actie **Materialen** en bekijk welke verf is gebruikt.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](../contoso-coffee-intro.md)  
