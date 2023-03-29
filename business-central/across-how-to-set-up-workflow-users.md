---
title: Werkstroomgebruikers instellen
description: 'Voordat u werkstromen kunt maken, moet u de gebruikers die eraan deelnemen, instellen op de pagina Werkstroomgebruikersgroep.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
---
# Werkstroomgebruikers instellen

Voordat u goedkeuringswerkstromen kunt maken, moet u de gebruikers instellen die deelnemen aan werkstromen. Dit is nodig om bijvoorbeeld op te geven wie een bericht ontvangt als er moet worden gereageerd op een werkstroomstap.  

Op de pagina **Werkstroomgebruikersgroepen** kunt u gebruikers instellen in werkstroomgebruikersgroepen en het nummer van de gebruikers opgeven in een procesvolgorde, zoals een fiatteringsketen. 

Werkstroomgebruikers die fungeren als goedkeuringgebruikers, zowel aanvragers als fiatteurs, moeten ook worden ingesteld op de pagina **Gebruikersinstellingen voor goedkeuring**. Meer informatie op [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Stel een hiërarchie voor fiatteurs op om aan te geven dat een goedkeuringsaanvraag niet wordt goedgekeurd totdat meerdere fiatteurs in een goedkeuringsketen deze hebben goedgekeurd. Voor het fiatteurstype **Fiatteur** stelt u fiatteurs op de pagina **Gebruikersinstellingen voor goedkeuring** in. Stel voor het fiatteurstype **Werkstroomgebruikersgroep** op de pagina **Werkstroomgebruikersgroepen** in en definieer de hiërarchie door incrementele nummers aan elke fiatteur in het veld **Volgnr.** toe te wijzen. Meer informatie hieronder en op [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md). 

## Een werkstroomgebruiker instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstroomgebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. De pagina **Werkstroomgebruikersgroep** wordt geopend.  
3. Voer in het veld **Code** maximaal 20 tekens in om de werkstroom te identificeren.  
4. Beschrijf de werkstroom in het veld **Omschrijving**.  
5. Vul op het sneltabblad **Werkstroomgebruikersgroepsleden** de velden op de eerste regel in, zoals in de volgende tabel is beschreven.  

   |Veld|Omschrijving|
   |-----|-----------|
   |**Gebruikersnaam**|Geef de gebruiker op die deelneemt aan werkstromen.<br /><br /> De gebruiker moet op de pagina **Gebruikersinstellingen** bestaan. Meer informatie op [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)|
   |**Volgnr.**|Geef de volgorde waarin de werkstroomgebruiker deelneemt aan een werkstroom in verband met andere gebruikers. Dit veld kan bijvoorbeeld opgeven wanneer de gebruiker in verhouding tot andere fiatteurs goedkeurt, door de optie **Werkstroomgebruikersgroep** in te stellen in het veld **Soort fiatteur** voor de gerelateerde werkstroomreactie.| 

   > [!TIP]
   > Als u wilt definiëren dat een goedkeuringsaanvraag vereist dat meerdere gelijke gebruikers deze goedkeuren, ongeacht een hiërarchie, stelt u een vlakke werkstroomgebruikersgroep in door hetzelfde volgordenummer aan alle relevante fiatteurs toe te kennen.

6. Herhaal stap 5 om meer werkstroomgebruikers aan de werkstroomgebruikersgroep toe te voegen.  
7. Herhaal stap 2 tot en met 6 om werkstroomgebruikersgroepen toe te voegen.  

## Zie gerelateerde [Microsoft-training](/training/modules/create-workflows/)

## Zie ook

[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
