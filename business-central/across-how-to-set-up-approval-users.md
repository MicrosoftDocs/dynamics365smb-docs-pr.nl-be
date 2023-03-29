---
title: Goedkeuringsgebruikers instellen
description: 'Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u op de pagina Gebruikersinstellingen voor goedkeuring de werkstroomgebruikers instellen die betrokken zijn bij de goedkeuringsprocessen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 09/08/2022
ms.author: edupont
---
# Goedkeuringsgebruikers instellen

Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen. Op de pagina **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.  

> [!NOTE]  
> Zowel goedkeuringsaanvragers als fiatteurs moeten eerst worden ingesteld als werkstroomgebruikers op de pagina **Werkstroomgebruikersgroep**. Meer informatie op [Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md).  

Als u goedkeuringsgebruikers hebt ingesteld, kunt u werkstroomreacties te maken voor goedkeuringswerkstromen. Lees meer vanaf stap 9 op [Goedkeuringswerkstromen maken](across-how-to-create-workflows.md).  

> [!NOTE]  
> Stel een hiërarchie voor fiatteurs op om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd totdat meerdere fiatteurs in een goedkeuringsketen deze hebben goedgekeurd. Voor het fiatteurstype **Fiatteur** stelt u fiatteurs op de pagina **Gebruikersinstellingen voor goedkeuring** in. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** op de pagina **Werkstroomgebruikersgroepen** in en definieer de hiërarchie door incrementele nummers aan elke fiatteur in het veld **Volgnr.**   Meer informatie hieronder en op [Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md).  

## Een goedkeuringsgebruiker instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe regel op de pagina **Gebruikersinstellingen voor goedkeuring** en vul de velden in zoals is beschreven in de volgende tabel.  

   |Veld|Omschrijving|
   |-----|-----------|
   |**Gebruikers-ID**|Selecteer de gebruikers-id van de gebruiker die is betrokken bij het goedkeuringsproces.|
   |**Verkoper/inkoper**|Geef de verkopers- of inkoperscode die op de gebruiker van toepassing is.<br /><br /> U vult het veld **Verkoper/inkoper** meestal in als de verkoper of inkoper die verantwoordelijk is voor de klant of leverancier, ook de persoon is die de betreffende verkoop- of inkoopaanvraag moet goedkeuren.|
   |**Fiatteur-id**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-id**.|
   |**Limiet voor goedkeuring verkoopbedrag**|Geef het maximale verkoopbedrag in lokale valuta (LV) op dat de gebruiker in het veld **Gebruikers-id** kan goedkeuren.|
   |**Onbeperkte goedkeuring van verkopen**|Geef op dat de gebruiker in het veld **Gebruikers-id** alle verkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|
   |**Limiet voor goedkeuring inkoopbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-id** kan goedkeuren.|
   |**Onbeperkte goedkeuring van inkopen**|Geef op dat de gebruiker in het veld **Gebruikers-id** alle inkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|
   |**Limiet voor goedkeuring aanvraagbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-id** kan goedkeuren voor inkoopoffertes.<br /><br /> Als u dit veld wilt gebruiken, moet u de optie **Fiatteursketting** selecteren in het veld **Limietsoort van fiatteur** op de pagina **Werkstroomreactie**.|
   |**Onbeperkt aanvragen van goedkeuring**|Geef op dat de gebruiker in het veld **Gebruikers-id** alle inkoopoffertes kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring aanvraagbedrag** niet invullen.|
   |**Vervanger**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-id**, als de gebruiker in het veld **Fiatteur-id** niet beschikbaar is. <br /><br />**Opmerking:** de vervanger kan de gebruiker in het veld **Vervanger**, de directe fiatteur of de goedkeuringsbeheerder zijn, in die volgorde van prioriteit. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).|
   |**E-mailadres**|Geef het e-mailadres op van de gebruiker in het veld **Gebruikers-id**.|
   |**Beheerder goedkeuringssysteem**|Geef de gebruiker op die rechten heeft om goedkeuringswerkstromen te deblokkeren, bijvoorbeeld door goedkeuringsaanvragen te delegeren naar nieuwe vervangende fiatteurs en door vervallen goedkeuringsaanvragen te verwijderen.|

   > [!NOTE]
   > Er kan maar één persoon goedkeuringsbeheerder zijn.

3. Kies de actie **Gebruikersinstellingen goedkeuring testen** om de instelling van gebruikers in het goedkeuringsproces te testen.  
4. Herhaal stap 2 en 3 voor elke gebruiker die u wilt instellen als goedkeuringsgebruiker.  

## Zie gerelateerde [Microsoft-training](/training/modules/create-workflows/)

## Zie ook

[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)  
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)  
[Goedkeuringswerkstromen maken](across-how-to-create-workflows.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
