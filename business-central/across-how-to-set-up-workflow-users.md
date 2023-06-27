---
title: Werkstroomgebruikers instellen
description: 'Voordat u werkstromen kunt maken, moet u de gebruikers die eraan deelnemen, instellen op de pagina Gebruikersinstellingen voor goedkeuring.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# <a name="set-up-a-sequence-of-workflow-users" />Een reeks werkstroomgebruikers instellen

Voordat u goedkeuringswerkstromen kunt maken, moet u de gebruikers instellen die aanvragen indienen, en hun fiatteurs. U kunt bijvoorbeeld opgeven wie een bericht ontvangt als er moet worden gereageerd op een werkstroomstap. U stelt deelnemers aan goedkeuringswerkstromen in op de **Gebruikersinstellingen voor goedkeuring**. Meer informatie op [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).

Op de pagina **Werkstroomgebruikersgroepen** kunt u opgeven waar een deelnemer een goedkeuringswerkstroom uitvoert door een nummer in te voeren in het veld **Volgnr.** ervan. U kunt bijvoorbeeld opgeven dat gebruikers een sequentiële volgorde hanteren, zoals een keten van goedkeurders. U kunt ook een platte lijst met goedkeurders specificeren door hetzelfde nummer in te voeren. In het laatste geval hoeft slechts één van de goedkeurders een aanvraag goed te keuren.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group" />Een werkstroomgebruikersgroep instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstroomgebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. De pagina **Werkstroomgebruikersgroep** wordt geopend.  
3. Voer in het veld **Code** maximaal 20 tekens in om de werkstroom te identificeren.  
4. Beschrijf de werkstroom in het veld **Omschrijving**.  
5. Vul op het sneltabblad **Werkstroomgebruikersgroepsleden** de velden op de eerste regel in, zoals in de volgende tabel is beschreven.  

   |Veld|Omschrijving|
   |-----|-----------|
   |**Gebruikersnaam**|Geef de gebruiker op die deelneemt aan een werkstroom.<br /><br /> De gebruiker moet op de pagina **Gebruikersinstellingen** bestaan. Meer informatie op [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)|
   |**Volgnr.**|Geef de volgorde waarin de werkstroomgebruiker deelneemt aan een werkstroom in verband met andere gebruikers. Dit veld kan bijvoorbeeld opgeven wanneer de gebruiker in verhouding tot andere fiatteurs goedkeurt, door de optie **Werkstroomgebruikersgroep** in te stellen in het veld **Soort fiatteur** voor de gerelateerde werkstroomreactie.| 

6. Herhaal stap 5 om meer werkstroomgebruikers aan de werkstroomgebruikersgroep toe te voegen.  

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/modules/create-workflows/)

## <a name="see-also" />Zie ook

[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
