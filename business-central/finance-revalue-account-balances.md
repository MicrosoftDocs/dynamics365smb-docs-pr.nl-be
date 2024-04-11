---
title: Saldi van grootboekrekening herwaarderen
description: Meer informatie over hoe u de saldi van grootboekrekeningen kunt herwaarderen voordat u uw financiële overzichten opstelt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# Saldi van grootboekrekening herwaarderen

Als u grootboekrekeningen gebruikt om balansposten in vreemde valuta te registreren, moet u de rekeningsaldi herwaarderen voordat u financiële overzichten maakt. Wisselkoersen veranderen vaak, en herwaardering helpt uw financiële overzichten nauwkeuriger te maken.

## Herwaarderingen instellen

U stelt elke rekening die u wilt opnemen in herwaarderingen in op de pagina **Grootboekrekening** . U kunt selecteren of u herwaarderingscorrecties wilt boeken naar gerealiseerde of ongerealiseerde winst-/verliesrekeningen. Het boeken van winsten en verliezen tijdens een wisselkoersaanpassing volgt de normale boekingsroutine. U doet dit bijvoorbeeld voor elke configuratie op de pagina **Valuta's**. Ga voor meer informatie over wisselkoersaanpassingen naar [Valutawisselkoersen bijwerken](finance-how-update-currencies.md).

Om fouten tot een minimum te beperken, kunt u in het veld **Bronvaluta boeken** een validatie instellen voor de valuta's die u naar individuele grootboekrekeningen wilt laten boeken:

* Alle valuta's (leeg)
* Meerdere valuta's
* Zelfde valuta
* Lokale valuta

## Een herwaardering uitvoeren

Als u de bedragen in vreemde valuta in de lokale valuta voor grootboekrekeningsaldi wilt herwaarderen, gebruikt u op de pagina **Rekeningschema** de actie **Herwaardering van grootboekvaluta** om een batchverwerking te starten. Met de batchverwerking worden herwaarderingsposten gemaakt in het dagboek dat u selecteert. Wanneer u de posten boekt, past u het saldo in de lokale valuta (LV) voor de rekening aan. Grootboekrekeningsaldi die altijd in LV worden weergegeven, weerspiegelen nu wijzigingen in de valuta's waarin posten zijn geboekt. Door deze herwaardering kunt u met minder moeite een nauwkeuriger financieel overzicht opstellen.

Als u een extra rapportagevaluta gebruikt, bevatten de herwaarderingsposten in het grootboek een bedrag voor de extra rapportagevaluta. Het bedrag dat alleen overeenkomt met het LV-bedrag voor deze posten, niet met het saldo in extra rapportagevaluta op de grootboekrekening. Als u de koersen in extra rapportagevaluta aanpast nadat u de aanpassingen hebt geboekt, voert u de wisselkoersaanpassing nog een keer uit om alle grootboekposten aan te passen.

> [!IMPORTANT]
> Herwaardering van grootboekrekeningen voldoet mogelijk niet aan alle vereisten voor transactie- en activaregistraties waarvoor herwaardering nodig is. Bijvoorbeeld voor financiële instrumenten, waardepapieren, geleasde activa, of als u deze gebruikt voor specifieke of grote hoeveelheden transacties of activa. Wij raden u aan om met uw auditor te bespreken of u de functie kunt gebruiken, en zo ja, hoe u deze moet gebruiken. Als u bijvoorbeeld toestaat dat valuta's voor een rekening worden gecombineerd, of als u een aparte rekening moet bijhouden voor elk activum dat u wilt bijhouden.

> [!NOTE]
> Herwaardering biedt niet de mogelijkheid om posten te vereffenen of de vereffening van posten ongedaan te maken, zoals u dat wel kunt met klant- en leveranciersposten. Aanpassingen gebeuren voor een saldo per valuta.

## Herwaardeer rekeningen ten opzichte van wisselkoersaanpassingen van klanten en leveranciers

Herwaardering vereenvoudigt de taak van het aanpassen van grootboekrekeningsaldi. Met de functie wordt het saldo per valuta per grootboekrekening geherwaardeerd, net zoals u doet voor aanpassingen in grootboekrekeningen die aan bankrekeningen zijn gekoppeld. Als u een grootboekrekening gebruikt om meerdere activa bij te houden, kunt u overwegen in plaats daarvan een leveranciers- of klantrekening te gebruiken.

> [!NOTE]
> Herwaardering van grootboekrekeningen voldoet mogelijk niet aan alle vereisten voor transactie- en activaregistraties waarvoor herwaardering nodig is. Bijvoorbeeld voor financiële instrumenten, waardepapieren, geleasde activa, of als u deze gebruikt voor specifieke of grote hoeveelheden transacties of activa. Wij raden u aan om met uw auditor te bespreken of u de functie kunt gebruiken, en zo ja, hoe u deze moet gebruiken. Als u bijvoorbeeld toestaat dat valuta's voor een rekening worden gecombineerd, of als u een aparte rekening moet bijhouden voor elk activum dat u wilt bijhouden.

De volgende voorbeelden illustreren het verschil tussen het gebruik van een grootboekrekening en het gebruik van een leveranciersrekening om het saldo bij te houden van twee monetaire activa die een vreemde valuta gebruiken.

**Een grootboekrekening gebruiken** Als u één grootboekrekening gebruikt om meerdere activa (bijvoorbeeld leningen of vaste activa) in dezelfde valuta bij te houden, of om afzonderlijke deeltransacties voor hetzelfde activum bij te houden maar nog steeds in dezelfde valuta, wordt met grootboekherwaardering één post per herwaardering voor de valuta gemaakt. Dit betekent dat u de aanpassingen met betrekking tot individuele activa of individuele transacties voor hetzelfde activum niet kunt volgen.

**Een leveranciersrekening gebruiken** Als u meerdere activa instelt als leveranciers en u er transacties naar boekt, in dezelfde of in verschillende valuta's, krijgt u een aanpassing per valuta per leverancier. Of, als u de schakeloptie **Boeken per post** inschakelt in de taakwachtrijpost **Wisselkoers aanpassen**, krijgt u een herwaarderingspost voor elke afzonderlijke leverancierspost.

Dit verschil is belangrijk wanneer u beoordeelt of grootboekherwaardering voor u de juiste functie is voor uw rapportagebehoeften.

> [!TIP]
> Wij raden u aan uw accountant of auditor te vragen welk type rekening het beste bij uw bedrijf past. Mogelijk bestaat er ook een app voor [!INCLUDE [prod_short](includes/prod_short.md)] in [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) die precies past bij uw bedrijfsscenario's.

## Zie ook

[Bedragen op grootboekrekeningen controleren](finance-review-accounts.md)  
[Het grootboek en het rekeningschema begrijpen](finance-general-ledger.md)  
