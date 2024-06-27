---
title: Goedkeuringsgebruikers instellen
description: 'Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij de goedkeuringsprocessen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '663,'
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-approval-users"></a>Goedkeuringsgebruikers instellen

Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u op de pagina **Gebruikersinstellingen voor goedkeuring** de gebruikers instellen die betrokken zijn bij de goedkeuringsprocessen. U kunt ook bedraglimieten instellen voor verschillende soorten aanvragen, vervangende goedkeurders definiëren en berichten instellen.  

Nadat u goedkeuringsgebruikers hebt ingesteld, kunt u werkstroomreacties te maken voor goedkeuringswerkstromen. Zie voor meer informatie [Goedkeuringswerkstromen maken](across-how-to-create-workflows.md).  

> [!TIP]
> U kunt vereisen dat meerdere goedkeurders reageren op een goedkeuringsaanvraag door een groep goedkeurders te maken op de pagina **Werkstroomgebruikersgroep**. Meer informatie op [Werkstroomgebruikersgroepen instellen](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Een goedkeuringsgebruiker instellen

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe regel op de pagina **Gebruikersinstellingen voor goedkeuring** en vul de velden in zoals is beschreven in de volgende tabel.  

   |Veld|Omschrijving|
   |-----|-----------|
   |**Gebruikers-ID**|Selecteer de gebruikers-id van de gebruiker die is betrokken bij het goedkeuringsproces.|
   |**Verkoper/inkoper**|Geef de verkopers- of inkoperscode die op de gebruiker van toepassing is.<br /><br /> U vult het veld **Verkoper/inkoper** meestal in als de verkoper of inkoper die verantwoordelijk is voor de klant of leverancier, ook de persoon is die een verkoop- of inkoopaanvraag moet goedkeuren.|
   |**Fiatteur-id**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de persoon die u hebt opgegeven in het veld **Gebruikers-id**.|
   |**Limiet voor goedkeuring verkoopbedrag**|Geef het maximale verkoopbedrag in lokale valuta (LV) op dat de persoon die is geselecteerd in het veld **Gebruikers-id**, kan goedkeuren.|
   |**Onbeperkte goedkeuring van verkopen**|Geef op dat de gebruiker in het veld **Gebruikers-id** alle verkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|
   |**Limiet voor goedkeuring inkoopbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-id** kan goedkeuren.|
   |**Onbeperkte goedkeuring van inkopen**|Geef op dat de gebruiker in het veld **Gebruikers-id** alle inkoopaanvragen kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring verkoopbedrag** niet invullen.|
   |**Limiet voor goedkeuring aanvraagbedrag**|Geef het maximale inkoopbedrag in LV op dat de gebruiker in het veld **Gebruikers-id** kan goedkeuren voor inkoopoffertes.<br /><br /> Als u dit veld wilt gebruiken, moet u de optie **Fiatteursketting** selecteren in het veld **Limietsoort van fiatteur** op de pagina **Werkstroomreactie**.|
   |**Onbeperkt aanvragen van goedkeuring**|Geef op dat de gebruiker in het veld **Gebruikers-id** alle inkoopoffertes kan goedkeuren, ongeacht het bedrag.<br /><br /> Als u dit selectievakje inschakelt, kunt u het veld **Limiet voor goedkeuring aanvraagbedrag** niet invullen.|
   |**Vervanger**|Selecteer de gebruikers-id van de gebruiker die aanvragen moet goedkeuren die zijn ingediend door de gebruiker in het veld **Gebruikers-id**, als de gebruiker in het veld **Fiatteur-id** niet beschikbaar is. <br /><br />**Opmerking:** de vervanger kan de gebruiker in het veld **Vervanger**, de directe fiatteur of de goedkeuringsbeheerder zijn, in die volgorde van prioriteit. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).|
   |**E-mailadres**|Geef het e-mailadres op van de gebruiker in het veld **Gebruikers-id**.|
   |**Beheerder goedkeuringssysteem**|Geef de gebruiker op die gemachtigd is om goedkeuringswerkstromen te deblokkeren, bijvoorbeeld door goedkeuringsaanvragen te delegeren naar nieuwe vervangende fiatteurs of door vervallen goedkeuringsaanvragen te verwijderen.<br /><br />**Opmerking** Er kan maar één persoon goedkeuringsbeheerder zijn.|

3. Kies de actie **Gebruikersinstellingen goedkeuring testen** om de instelling van gebruikers in het goedkeuringsproces te testen.  
4. Herhaal stap 2 en 3 voor elke gebruiker die u wilt instellen als goedkeuringsgebruiker.  

De volgende stap is specificeren hoe u wilt dat [!INCLUDE [prod_short](includes/prod_short.md)] mensen informeert dat een verzoek in afwachting van hun aandacht is. Meer informatie op [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md).

## <a name="see-also"></a>Zie ook

[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)  
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)  
[Goedkeuringswerkstromen maken](across-how-to-create-workflows.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
