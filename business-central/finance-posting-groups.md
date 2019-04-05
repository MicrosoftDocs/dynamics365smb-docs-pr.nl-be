---
title: Boekingsgroepinstellingen| Microsoft Docs
description: Overzicht van de boekingsgroepen dat u kunt gebruiken om tijd te besparen en fouten te voorkomen wanneer u transacties boekt.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 03/05/2019
ms.author: bholtorf
ms.openlocfilehash: d62742e7dbee8a4f050d95444b66fa06521b707b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816051"
---
# <a name="setting-up-posting-groups"></a>Boekingsgroepen instellen
Met boekingsgroepen worden entiteiten zoals klanten, leveranciers, artikelen, resources en verkoop- en inkoopdocumenten aan grootboekrekeningen gekoppeld. Hiermee wordt tijd bespaard en worden fouten voorkomen als u transacties boekt. De transactiewaarden gaan naar de rekeningen die in de boekingsgroep zijn opgegeven voor die bepaalde entiteit. De enige voorwaarde is dat u een rekeningschema hebt. Zie [Het rekeningschema instellen](finance-setup-chart-accounts.md) voor meer informatie.  

Boekingsgroepen zijn verdeeld in drie categorieën:  

* Algemeen - definieer aan wie u verkoopt en van wie u koopt, en wat u verkoopt en wat u koopt. U kunt de boekingsgroepen ook combineren om zaken op te geven zoals de resultatenrekeningen waarnaar u wilt boeken, of groepen gebruiken om rapporten te filteren.  
* Specifiek - gebruik bijvoorbeeld verkoopdocumenten in plaats van rechtstreeks naar het grootboek te boeken. Wanneer u klantenposten maakt, worden bijbehorende posten in het grootboek gemaakt.  
* Belasting - definieer de belastingpercentages en berekeningssoorten die moeten worden toegepast op degene aan wie u verkoopt en van wie u koopt, en op wat u verkoopt en wat u koopt.

In de volgende tabellen worden de boekingsgroepen van elke categorie beschreven.  

| Algemene boekingsgroepen | Omschrijving |
| --- | --- |
| Bedrijfsboekingsgroepen |Wijs deze groep aan klanten en leveranciers toe om op te geven aan wie u verkoopt en van wie u koopt. Stel dit op de pagina **Bedrijfsboekingsgroepen** in. Als u dat doet, moet u bedenken hoeveel groepen u nodig hebt om verkopen en inkopen onder te verdelen. Groepeer bijvoorbeeld klanten en leveranciers per geografisch gebied of per bedrijfssoort. |
| Productboekingsgroepen |Wijs deze groep aan artikelen en resources toe om op te geven wat u verkoopt en wat u koopt. Stel dit op de pagina **Productboekingsgroepen** in. Wanneer u dat doet, moet u bedenken hoeveel groepen u nodig hebt om verkoop onder te verdelen per product (artikelen en resources) en inkopen per artikel. Verdeel deze groepen bijvoorbeeld op basis van grondstoffen, detailhandel, resources, capaciteit, enzovoort. |
| Boekingsgroepinstellingen |Combineer bedrijfs- en productboekingsgroepen en kies de rekeningen waarnaar u wilt boeken. Voor elke combinatie van bedrijfs- en productboekingsgroepen kunt u een set grootboekrekeningen toewijzen. Dit betekent bijvoorbeeld dat u de verkoop van hetzelfde artikel kunt boeken naar verschillende verkooprekeningen in het grootboek omdat klanten aan verschillende bedrijfsboekingsgroepen zijn toegewezen. Stel dit op de pagina **Boekingsgroepinstellingen** in. |

| Specifieke boekingsgroepen | Description |
| --- | --- |
| Klantboekingsgroepen |Definieer de rekeningen die moeten worden gebruikt als u klanttransacties boekt. Als u voorraad gebruikt bij klanten, wordt met de combinatie Bedrijfsboekingsgroep, toegewezen aan uw klant, en de Productboekingsgroep, toegewezen aan het voorraadartikel, bepaald naar welke rekeningen de verkooporderregels worden geboekt. Zie "Bedrijfsboekingsgroepen" en "Productboekingsgroepen" onder **Algemene boekingsgroepen** hierboven. Stel dit op de pagina **Klantboekingsgroepen** in. |
| Leveranciersboekingsgroepen |Definieer waar transacties voor tegoeden, servicekostenrekeningen en contantkortingsrekeningen moeten worden geboekt. Dit is vergelijkbaar met klantboekingsgroepen. Stel dit op de pagina **Leveranciersboekingsgroepen** in. |
| Voorraadboekingsgroepen |Definieer voorraadboekingsgroepen die u vervolgens toewijst aan de relevante artikelrekeningen op de pagina **Voorraadboekingsgroepinstellingen**. Wanneer u dan posten voor een artikel boekt, word er een boeking uitgevoerd naar de grootboekrekening die is ingesteld voor deze aan het artikel gekoppelde combinatie van artikelboekingsgroep en vestiging. Voorraadboekingsgroepen vormen tevens een ideale manier om uw voorraad te organiseren. Wanneer u rapporten genereert, kunt u artikelen dan scheiden op boekingsgroepen. Stel dit op de pagina **Voorraadboekingsgroepen** in. |
| Bankboekingsgroepen |Definieer rekeningen voor bankrekeningen. Hiermee kunnen bijvoorbeeld de processen om transacties te traceren en bankrekeningen te reconciliëren worden vereenvoudigd. Stel dit op de pagina **Bankboekingsgroepen** in. |
| VA-boekingsgroep |Definieer rekeningen voor verschillende soorten onkosten en kosten, zoals aanschafkosten, gecumuleerde afschrijvingsbedragen, aanschafkosten bij BGS, gecumuleerde afschrijving bij BGS, winst bij BGS, verlies bij BGS, onderhoudskosten en afschrijvingskosten. Stel dit op de pagina **VA-boekingsgroepen** in. |

| Btw-boekingsgroep | Description |
| --- | --- |
| Btw-bedrijfsboekingsgroepen |Bepaal hoe u btw voor klanten en leveranciers kunt berekenen en boeken. Stel dit op de pagina **Btw-bedrijfsboekingsgroepen** in. Als u dit doet, moet u bedenken hoeveel groepen u nodig hebt. Dit kan bijvoorbeeld afhangen van factoren, zoals lokale wetgeving en of u zowel nationaal als internationaal wilt handelen. |
| Btw-productboekingsgroepen |Geef de belastingberekeningen aan die nodig zijn voor de soorten artikelen of resources die u koopt of verkoopt. |
| Btw-boekingsinstellingen |Combineer btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen. Wanneer u een algemene dagboekregel, inkoopregel of verkoopregel invult, wordt gekeken naar de combinatie om te bepalen welke rekeningen moeten worden gebruikt. |

## <a name="example-of-linking-posting-groups"></a>Voorbeeld van het koppelen van boekingsgroepen
Hier volgt een scenario.  

Deze boekingsgroepen worden gekozen op de klantenkaart:  

* Algemene bedrijfsboekingsgroep
* Klantboekingsgroep  

Deze boekingsgroepen worden gekozen op de artikelkaart:  

* Algemene productboekingsgroep  
* Voorraadboekingsgroep  

Wanneer u een verkoopdocument maakt, wordt in de verkoopkoptekst de klantenkaartinformatie gebruikt en wordt op de verkoopregels de artikelkaartinformatie gebruikt.  

* De inkomstenboeking (resultatenrekening) wordt bepaald door de combinatie van de algemene bedrijfsboekingsgroep en de algemene productboekingsgroep.  
* De klantboeking (balans) wordt bepaald door de klantboekingsgroep.  
* De voorraadboeking (balans) wordt bepaald door de voorraadboekingsgroep.  
* De boeking van kosten van verkochte goederen (resultatenrekening) wordt bepaald door de combinatie van algemene bedrijfsboekingsgroep en algemene productboekingsgroep.  

Uw instelling bepaalt wanneer de boeking plaatsvindt. Wanneer de boeking plaatsvindt, hangt bijvoorbeeld af van het tijdstip waarop u periodiek activiteiten uitvoert, zoals het boeken van voorraadkosten of het aanpassen van kostenposten.

## <a name="copying-posting-setup-lines"></a>Boekingsinstellingsregels kopiëren
Hoe meer product- en bedrijfsboekingsgroepen u hebt, des te meer regels u op de pagina Boekingsgroepinstellingen ziet. Dit kan veel gegevensinvoer impliceren voor het instellen van de boekingsgroepinstellingen voor het bedrijf. Hoewel er veel verschillende combinaties van bedrijfs- en productboekingsgroepen kunnen zijn, wordt door verschillende combinaties mogelijk toch naar dezelfde grootboekrekeningen geboekt. Om de hoeveelheid handmatige invoer te beperken, kopieert u de grootboekrekeningen van een bestaande regel op de pagina **Boekingsgroepinstellingen**.

## <a name="see-also"></a>Zie ook
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
