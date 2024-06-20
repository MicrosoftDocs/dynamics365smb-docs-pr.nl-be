---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!IMPORTANT]
> Wanneer u de als-gebeurtenis voor een werkstroomstap wijzigt, veranderen ook de dan-reacties. Soms verwijzen de reacties van andere als-gebeurtenissen naar deze reacties als de volgende stap in de workflow. Nadat u een als-gebeurtenis hebt gewijzigd, moet u controleren of de volgende stappen voor de dan-gebeurtenissen correct zijn.  
>
> De werkstroomsjabloon **Goedkeuringswerkstroom van leverancier** heeft een primaire als-gebeurtenis **Goedkeuring van een leverancier is aangevraagd**. Deze als-gebeurtenis heeft de dan-reactie **Verzend goedkeuringsaanvraag voor de record en maak een bericht**, waarnaar andere dan-reacties verwijzen. Als u de primaire als-gebeurtenis **Goedkeuring van een leverancier is aangevraagd** wijzigt in bijvoorbeeld **Een leveranciersrecord is gewijzigd**, wordt de dan-reactie antwoord samen met de referenties gewist.
>
> De dan-reacties voor de als-gebeurtenissen **Een goedkeuringsverzoek wordt gedelegeerd** en **Een goedkeuringsverzoek wordt goedgekeurd** (met **Op voorwaarde** van **Wacht opgoedkeuringen >0**) zijn voorbeelden van waar het wijzigen van een primaire als-gebeurtenis problemen kan veroorzaken. De dan-reacties hebben een volgende stap die verwijst naar de dan-reactie **Verzend goedkeuringsaanvraag voor de record en maak een bericht** van de als-gebeurtenis **Goedkeuring van een leverancier is aangevraagd**. Omdat de dan-reactie voor de als-gebeurtenis **Goedkeuring van een leverancier is aangevraagd** niet langer beschikbaar is, werken de ingesprongen gebeurtenissen niet zoals verwacht.
>
> U moet de volgende stappen opgeven voor de dan-reacties voor als-gebeurtenissen die verwijzen naar de gewijzigde als-gebeurtenis.