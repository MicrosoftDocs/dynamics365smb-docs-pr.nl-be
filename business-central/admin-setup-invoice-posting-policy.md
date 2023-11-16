---
title: Definieer een beleid voor het boeken van facturen voor gebruikers
description: Gebruik beleid voor het boeken van facturen om te bepalen of een gebruiker verkoop- en inkoopfacturen kan boeken.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Definieer een beleid voor het boeken van facturen voor gebruikers

Bedrijven hebben vaak unieke processen voor het boeken van verkoop- en inkoopfacturen en zendingen. Processen kunnen bijvoorbeeld variëren van één persoon die alles op een inkooporder plaatst tot meerdere medewerkers. U kunt voorkomen dat gebruikers facturen boeken of vereisen dat facturen samen met zendingen of ontvangsten worden geboekt.

## <a name="to-specify-a-posting-policy"></a>Een boekingsbeleid specificeren

Kies op de pagina **Gebruikersinstellingen** in de velden **Boekingsbeleid voor verkoopfacturen** en **Boekingsbeleid voor inkoopfacturen** een van de volgende opties:

* **Toegestaan** (Standaard) - Behoud het huidige gedrag, waarbij een gebruiker de te gebruiken boekingsoptie kan kiezen, zoals **Verzenden**, **Factuur**, en **Verzenden en factuur**. 
* **Verboden** - Voorkom dat de gebruiker facturen boekt. Business Central toont een bevestigingsdialoogvenster met alleen de opties **Verzenden** of **Ontvangen** .
* **Verplicht** - Sta de gebruiker toe om facturen samen met bonnen of zendingen te boeken. Business Central toont een bevestigingsdialoogvenster met de opties **Verzenden en factureren** of **Ontvangen en factureren** .

## <a name="effect-on-documents"></a>Effect op documenten

In de volgende tabel wordt beschreven hoe beleid voor het boeken van facturen van invloed is op documenten.

> [!NOTE]
> Wanneer u verkoop- en inkoopfacturen en creditnota's boekt, heeft u geen boekingsopties. De documenten boeken altijd de fysieke en financiële transacties samen. U kunt facturen en creditnota's niet gedeeltelijk boeken.

|Document | Optie 1: Toestaan <br>Geeft een reeks opties weer| Optie 2: Verboden <br>Bevestigingsvenster | Optie 3: Verplicht <br>Bevestigingsvenster|
|--|--|--|--|
|Verkooporder |- Verzenden <br>- Factureren <br>- Verzenden en factureren |Wilt u de verzending boeken? |Wilt u de verzending en factuur boeken?|
|Verkoopfactuur|Geen opties|Wilt u de factuur boeken?|Wilt u de factuur boeken?|
|Verkoopcreditnota|Geen opties|Wilt u de creditnota boeken?|Wilt u de creditnota boeken?|
|Verkoopretourorder |- Ontvangen <br>- Factureren <br>- Ontvangen en factureren |Wilt u de ontvangst boeken? |Wilt u de ontvangst en factuur boeken?|
|Voorraadpick |- Verzenden <br>- Verzenden en factureren |Wilt u de verzending boeken? |Wilt u de verzending en factuur boeken?|
|Inkooporder |- Ontvangen <br>- Factureren <br>- Ontvangen en factureren |Wilt u de ontvangst boeken? |Wilt u de ontvangst en factuur boeken?|
|Inkoopfactuur|Geen opties|Wilt u de factuur boeken?|Wilt u de factuur boeken?|
|Inkoopcreditnota|Geen opties|Wilt u de creditnota boeken?|Wilt u de creditnota boeken?|
|Inkoopretourorder |- Verzenden <br>- Factureren <br>- Verzenden en factureren |Wilt u de verzending boeken? |Wilt u de verzending en factuur boeken?|
|Voorraadopslag |- Ontvangen <br>- Ontvangen en factureren |Wilt u de ontvangst boeken? |Wilt u de ontvangst en factuur boeken?|
|Magazijnverzending |- Verzenden <br>- Verzenden en factureren | Wilt u de verzending boeken? |Wilt u de verzending en factuur boeken?|

   > [!Note]
   > De instelling heeft geen invloed op het boeken van algemene dagboekregels waar u **Factuur** in het veld **Documenttype** kunt selecteren.

## <a name="see-also"></a>Zie ook

[Verkopen factureren](sales-how-invoice-sales.md)  
[Aankopen registreren met inkoopfacturen en orders](purchasing-how-record-purchases.md)  
[Artikelen voor een verkoop inkopen door inkoopfacturen te maken](purchasing-how-purchase-products-sale.md)
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
