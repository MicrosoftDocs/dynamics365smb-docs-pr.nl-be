---
title: Opgeven wanneer en hoe gebruikers werkstroomberichten ontvangen
description: 'Wanneer u gebruikers instelt in goedkeuringswerkstromen, kunt u specificeren hoe en wanneer elke goedkeuringsgebruiker berichten ontvangt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '663, 1500, 1512, 1513,'
ms.date: 09/09/2022
ms.author: bholtorf
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a><a name="specify-when-and-how-to-receive-workflow-notifications"></a>Opgeven wanneer en hoe gebruikers werkstroomberichten ontvangen

Wanneer u goedkeuringsgebruikers instelt in werkstromen waarin u wilt dat iemand wijzigingen goedkeurt, zoals wanneer nieuwe records worden gemaakt of wanneer iemand om goedkeuring vraagt, moet u specificeren hoe en wanneer de goedkeuringsgebruiker op de hoogte moet worden gesteld. U kunt bijvoorbeeld opgeven dat een goedkeuringsgebruiker onmiddellijk een e-mail ontvangt wanneer iemand een nieuwe klant aanmaakt. Als alternatief kunt u plannen dat de berichten bijvoorbeeld wekelijks of maandelijks worden vastgehouden en gezamenlijk worden bezorgd.

Gebruikers kunnen hun berichtinstellingen ook wijzigen door de knop **Berichtinstellingen wijzigen** voor een bericht te kiezen.  

> [!NOTE]
> Berichten worden afgeleverd volgens de berichtinstellingen voor de ontvanger, niet de afzender. Dat is een belangrijk onderscheid, omdat het betekent dat wanneer iemand een goedkeuring aanvraagt als onderdeel van een werkstroom, zijn of haar verzoek niet noodzakelijkerwijs onmiddellijk wordt verzonden. In plaats daarvan wordt het afgeleverd volgens het meldingsschema dat is opgegeven in de meldingsinstellingen van de goedkeurder.

Voordat u voorkeuren voor gebruikersberichten over goedkeuring kunt instellen, moet u de gebruiker als goedkeuringsgebruiker instellen. Meer informatie op [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Als u e-mail wilt gebruiken als meldingsmethode, moet u e-mail instellen voor zowel de afzender als de ontvanger in [!INCLUDE [prod_short](includes/prod_short.md)]. Meer informatie op [E-mail instellen](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a><a name="steps-in-workflows"></a>Stappen in werkstromen

In veel goedkeuringswerkstroomstappen wordt aan gebruikers gemeld dat er een gebeurtenis is opgetreden waarop ze moeten reageren. Bijvoorbeeld, de gebeurtenis in een werkstroomstap kan zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt. Het gerelateerde antwoord is dat er een bericht wordt verzonden naar Gebruiker 3 om een proces te starten met de goedgekeurde record. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost. Zie voor meer informatie [Werkstroom](across-workflow.md).  

## <a name="specify-when-and-how-approval-users-receive-notifications"></a><a name="specify-when-and-how-approval-users-receive-notifications"></a>Vastleggen wanneer en hoe goedkeuringsgebruikers berichten ontvangen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de regel voor de gebruiker voor wie u berichtvoorkeuren wilt instellen. Kies vervolgens de actie **Berichtinstellingen**.  
3. Vul op de pagina **Instelling van werkstroombericht** de velden in, zoals is beschreven in de volgende tabel.  

   > [!NOTE]
   > Als u de pagina **Instelling van werkstroombericht** opent vanaf de pagina **Gebruikersinstellingen voor goedkeuring**, wordt de berichtinstelling gekoppeld aan de goedkeuringsgebruiker. De goedkeuringsgebruiker ontvangt altijd werkstroomberichten volgens die berichtconfiguratie. Als u de functie *Vertel me* gebruikt om de pagina **Instelling van werkstroombericht** te openen, is de berichtinstelling van toepassing op alle gebruikers.

   |Veld|Omschrijving|
   |-----|-----------|
   |**Berichttype**|Geef het soort gebeurtenis aan waarop het bericht betrekking heeft.<br /><br /> Selecteer een van de volgende opties:<br /><br /> -   **Nieuwe record** geeft aan dat het bericht betrekking heeft op een nieuwe record, zoals een document, waarop de gebruiker moet reageren.<br />-   **Goedkeuring** geeft aan dat het bericht betrekking heeft op een of meer goedkeuringsaanvragen.<br />-   **Vervallen** geeft aan dat het bericht wordt gebruikt om gebruikers eraan te herinneren dat ze te laat zijn met reageren op een gebeurtenis.|
   |**Berichtmethode**|Geef aan of het bericht wordt verzonden als interne opmerking.|

   U kunt de lay-out van e-mailberichten bepalen door Rapport 1320, Berichte-mail aan te passen. U vindt meer informatie op [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

   U hebt nu opgegeven hoe de gebruiker berichten ontvangt. U kunt nu opgeven wanneer de gebruiker berichten ontvangt.  
4. Kies de actie **Berichtplanning**.  
5. Vul op de pagina **Berichtplanning** de velden in, zoals is beschreven in de volgende tabel.  

   |Veld|Omschrijving|
   |-----|-----------|
   |**Herhaling**|Geef het herhalingspatroon op waarin berichten naar de gebruiker worden verzonden.|
   |**Tijd**|Hiermee wordt opgegeven op welk moment van de dag berichten naar de gebruiker worden verzonden wanneer de waarde in het veld **Herhaling** niet **Direct** is.|
   |**Dagelijkse frequentie**|Geef aan op welke soort dag de gebruiker berichten ontvangt als de waarde in het veld **Herhaling** **Dagelijks** is.<br /><br /> Selecteer **Werkdag** om berichten te ontvangen op elke werkdag van de week. Selecteer **Dagelijks** om berichten te ontvangen op elke dag van de week, inclusief weekends.|
   |**Maandag** tot en met **zondag**|Geef aan op welke soort dag de gebruiker berichten ontvangt als de waarde in het veld **Herhaling** **Wekelijks** is.|
   |**Datum van maand**|Geef aan of de gebruiker berichten ontvangt op de eerste, laatste of een bepaalde dag van de maand.|
   |**Datum maandelijks bericht**|Geef de dag van de maand aan waarop de gebruiker berichten ontvangt als de waarde in het veld **Datum van maand** **Aangepast** is.|

## <a name="change-when-and-how-you-receive-notifications"></a><a name="change-when-and-how-you-receive-notifications"></a>Wijzigen wanneer en hoe gebruikers berichten ontvangen

1. Kies in een van de berichten die u hebt ontvangen, hetzij als e-mail hetzij als opmerking, **Berichtinstellingen wijzigen**.  
2. Op de pagina **Instelling van werkstroombericht** wijzigt u de berichtvoorkeuren zoals beschreven in de stappen 3-5 hierboven.
   1. Bevestig dat het juiste bericht is gekozen onder het veld **Berichttype**.
   2. Kies of u een e-mail of opmerking wilt ontvangen onder het veld **Berichtmethode**.
   3. Selecteer de **Berichtplanning** om de frequentie en herhaling te wijzigen waarmee berichten worden verzonden.

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Goedkeuringswerkstroomberichten instellen](across-setting-up-workflow-notifications.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
