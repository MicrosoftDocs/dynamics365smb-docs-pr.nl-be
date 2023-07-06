---
title: Documenten goedkeuren of weigeren in werkstromen
description: 'Goedkeuring aanvragen, weigeren of delegeren van bijvoorbeeld een inkoop- of verkoopdocument, als onderdeel van een werkstroom.'
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 09/12/2022
ms.author: edupont
---
# <a name="how-to-use-approval-workflows"></a><a name="how-to-use-approval-workflows"></a><a name="how-to-use-approval-workflows"></a>Goedkeuringswerkstromen gebruiken

Wanneer een record, zoals een inkoopdocument of klantenkaart, door iemand in uw organisatie moet worden goedgekeurd, stuurt u een goedkeuringsaanvraag als onderdeel van een werkstroom. Op basis van de instellingen van de werkstroom krijgt de betreffende fiatteur vervolgens het bericht dat hij of zij de record moet goedkeuren.

U stelt goedkeuringswerkstromen op de pagina **Werkstroom** in. U moet ook goedkeuringsgebruikers instellen, inclusief eventuele relevante bedraglimieten, op de pagina **Gebruikersinstellingen voor goedkeuring**. U vindt meer informatie op [Goedkeuringswerkstromen instellen](across-set-up-workflows.md).  

Naast de werkstromen voor goedkeuring die in dit artikel worden beschreven kunt u verschillende andere werkstroomtaken uitvoeren. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-use-workflows.md).

Kerngoedkeuringswerkstromen voor inkoopdocumenten, verkoopdocumenten, betalingsdagboeken, klantenkaarten en artikelkaarten zijn gereed om als begeleide instellingen te dienen. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md)

## <a name="request-a-record-approval"></a><a name="request-a-record-approval"></a><a name="request-a-record-approval"></a>Goedkeuring van een record aanvragen

De volgende taak wordt uitgevoerd door een fiatteurgebruiker.

1. Kies op de pagina met de record de actie **Goedkeuringsaanvraag verzenden**.
2. Als u uw goedkeuringsaanvragen wilt zien, kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Posten met goedkeuringsaanvraag** in en kiest u vervolgens de gerelateerde koppeling.  

De status van de goedkeuringsvermelding wordt bijgewerkt van **Gemaakt** naar **Open**. De status van de record, bijvoorbeeld een inkoopfactuur, wordt bijgewerkt van **Open** naar **Wacht op goedkeuring** en blijft voor verwerking vergrendeld totdat alle fiatteurs de record hebben goedgekeurd.

Als alle vereiste fiatteurs de record hebben goedgekeurd, wordt de status gewijzigd in **Vrijgegeven**. U kunt dan doorgaan met werken met de record.

## <a name="cancel-approval-requests"></a><a name="cancel-approval-requests"></a><a name="cancel-approval-requests"></a>Goedkeuringsaanvragen annuleren

De volgende taak wordt uitgevoerd door een fiatteurgebruiker met fiatteursrechten.

Het kan voorkomen dat een klant wijzigingen wil aanbrengen in een order nadat deze is ingediend ter goedkeuring. In dit geval kunt u het goedkeuringsproces annuleren en de noodzakelijke wijzigingen aanbrengen in de order en dan opnieuw goedkeuring aanvragen.

- Kies op de pagina met de record de actie **Goedkeuringsaanvraag annuleren**.

Als de goedkeuringsaanvraag is geannuleerd, wordt de status voor de gerelateerde goedkeuringspost veranderd in **Geannuleerd**. De status van de record wordt bijgewerkt van **Wacht op goedkeuring** naar **Open**. Het goedkeuringsproces kan op dit moment opnieuw beginnen.

## <a name="approve-or-reject-approval-requests"></a><a name="approve-or-reject-approval-requests"></a><a name="approve-or-reject-approval-requests"></a>Aanvragen voor goedkeuring goedkeuren of afwijzen

De volgende taak wordt uitgevoerd door een fiatteurgebruiker met fiatteursrechten.

U kunt goedkeuringsaanvragen verwerken op de pagina **Aanvragen ter goedkeuring** en bijvoorbeeld ook meerdere aanvragen tegelijk goedkeuren. U kunt ook afzonderlijke records goedkeuren door de koppeling te kiezen in het bericht dat u ontvangt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanvragen ter goedkeuring** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een of meer regels van de record of records die u wilt goedkeuren of afwijzen.
3. Kies de actie **Goedkeuren**, **Weigeren** of **Delegeren**.

Wanneer een record is goedgekeurd of afgewezen, wordt de goedkeuringsstatus in het veld **Status** respectievelijk gewijzigd in **Goedgekeurd** of **Afgewezen**.

Als er een fiatteurshiërarchie is ingesteld, is de recordstatus **Wacht op goedkeuring** totdat alle gevraagde fiatteurs de record hebben goedgekeurd. Vervolgens wordt de recordstatus gewijzigd in **Vrijgegeven**.

Tegelijkertijd wordt de goedkeuringsstatus gewijzigd van **Gemaakt** in **Open** zodra een goedkeuringsaanvraag voor de record is gemaakt. Als het verzoek wordt afgewezen, wordt de goedkeuringsstatus gewijzigd in **Afgewezen**. De status blijft **Open** of **Afgewezen** totdat alle fiatteurs het verzoek hebben goedgekeurd.

## <a name="delegate-approval-requests"></a><a name="delegate-approval-requests"></a><a name="delegate-approval-requests"></a>Goedkeuringsaanvragen delegeren

De volgende taak wordt uitgevoerd door een fiatteurgebruiker met fiatteursrechten.

De aanvrager en de goedkeuringsbeheerder kunnen een goedkeuringsaanvraag delegeren aan de vervangende fiatteur om te voorkomen dat records zich ophopen of anderszins de werkstroom blokkeren. De vervanger kan een aangewezen vervanger, de directe fiatteur of de goedkeuringsbeheerder zijn, in die volgorde van prioriteit. Deze functie wordt doorgaans gebruikt wanneer een fiatteur niet beschikbaar is en aanvragen niet kan goedkeuren voor de vervaldatum.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanvragen ter goedkeuring** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een of meer regels van goedkeuringsaanvragen die u wilt delegeren aan een vervangende fiatteur, en kies vervolgens de actie **Delegeren**.

Er wordt een bericht met het verzoek om de aanvraag goed te keuren, verstuurd naar de vervangende fiatteur.

## <a name="manage-overdue-approval-requests"></a><a name="manage-overdue-approval-requests"></a><a name="manage-overdue-approval-requests"></a>Vervallen goedkeuringsaanvragen beheren

De volgende taak wordt uitgevoerd door een fiatteurgebruiker met fiatteursrechten.

Met regelmatige tussenpozen moet u gebruikers van de goedkeuringswerkstroom herinneren aan achterstallige goedkeuringsverzoeken; u gebruikt de functie **Berichten over achterstallige goedkeuringen verzenden** om dit te doen.

Met de functie **Berichten over achterstallige goedkeuringen verzenden** controleert u op alle openstaande goedkeuringsaanvragen die op dat moment achterstallig zijn. Elke fiatteur waarvoor ten minste één goedkeuringspost achterstallig is, ontvangt een bericht met een overzicht van alle achterstallige goedkeuringsaanvragen. Het bericht wordt ook verzonden naar hun fiatteurs en alle aanvragers die de achterstallige goedkeuringen hebben ingediend. Deze laatste stap komt van pas wanneer de achterstallige goedkeuringspost moet worden overgedragen aan een vervanger.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vervallen goedkeuringsaanvragen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Vervallen goedkeuringsaanvragen** de actie **Berichten over vervallen goedkeuringen verzenden**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/use-approval-workflows/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Werkstroom](across-workflow.md)  
[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)  
[Verkoop](sales-manage-sales.md)  
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
