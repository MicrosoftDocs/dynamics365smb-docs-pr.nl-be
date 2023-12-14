---
title: Orderplanning gebruiken om voorraad te maken en te reserveren
description: Procedure om te leren hoe u orderplanning gebruikt om de vereiste productieorder voor de levering in Business Central te creëren.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a>Procedure: Orderplanning gebruiken om voorraad te maken en te reserveren

In dit artikel voeren we u door de stappen om de demogegevens voor Contoso Coffee te gebruiken bij orderplanning.

## <a name="scenario"></a>Scenario

U bent de productieplanner bij Contoso Coffee. U hebt een productieorder gemaakt voor 100 eenheden van het artikel **SP-SCM1009, Airpot** en u wilt subassemblages plannen voor deze order. U gebruikt orderplanning om de benodigde productieorder voor de levering aan te maken. Omdat u de productieorder maakt om aan de vereisten van een specifieke order te voldoen, besluit u de output van de productieorder te reserveren.  

## <a name="steps"></a>Stappen

1. Maak de nieuwe vrijgegeven productieorder voor 100 eenheden van het artikel **SP-SCM1009, Airpot**.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vrijgegeven productieorder** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Bronsoort** |Artikel|
        |**Bronnr.** |SP-SCM1009|
        |**Aantal** |100|
    3. Kies de actie **Productieorder vernieuwen**.  

    Noteer het nummer van de vrijgegeven productieorder.

2. Open de pagina **Orderplanning** en bereken een nieuw plan.

    1. Kies de actie **Planning**.  

    2. Kies op de pagina **Orderplanning** de actie **Plan berekenen**.  

    3. Scrol omlaag naar de vraagregel die de vrijgegeven productieorder aanduidt die u eerder hebt gemaakt.  

    4. Vouw de regel uit om de details van de vraagregel weer te geven. Bevestig dat het een suggestie is voor een productieorder van 100 eenheden van artikel 1001.  

3. Maak een nieuwe productieorder voor 100 stuks van het artikel **SP-BOM2000, Reservoirassembl.** en reserveer de output van deze productieorder namens de gerelateerde bovenliggende order.  

    1. Schakel het selectievakje in het veld **Reserveren** op de vraagregel in voor de 100 eenheden van artikel SP-BOM2000.

    2. Kies de actie **Orders maken**.  

    3. Stel het veld **Orders maken voor** in op *De actieve regel*.  

    4. Stel het veld **Productieorder aanmaken** in op *Vast gepland*.

    5. Kies de knop **OK** om de productieorder te maken.

    6. Op de pagina **Orderplanning** moet u bevestigen dat de vraagregel voor de 100 eenheden van artikel 1001 is verwijderd.

Zo kunt u orders plannen in [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="see-also"></a>Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](../contoso-coffee-intro.md)  
[Informatie over productieorders](../../production-about-production-orders.md)  
