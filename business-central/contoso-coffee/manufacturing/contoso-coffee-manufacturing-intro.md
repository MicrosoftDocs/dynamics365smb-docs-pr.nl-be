---
title: Inleiding tot Contoso Coffee-productie
description: Overzicht van scenario's voor hoe demogegevens voor Contoso Coffee u kunnen helpen bij het leren gebruiken van de productiemogelijkheden in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a><a name="introduction-to-contoso-coffee-manufacturing"></a><a name="introduction-to-contoso-coffee-manufacturing"></a>Inleiding tot Contoso Coffee-productie

Contoso Coffee is een fictief bedrijf dat koffiezetapparaten voor consumenten en bedrijven maakt. De apps **Contoso-koffie** voor Business Central voegen demogegevens toe die u kunt gebruiken om te leren hoe u de productiemogelijkheden in Business Central kunt benutten.  

De app biedt vier producten die zijn geoptimaliseerd voor verschillende scenario's:

- **SP-SCM1009 Airpot**  

  Dit product is een stuklijst (BOM) met een subassemblage, **Bewerkingsplan**. Gebruik het om de standaard productiestroom te demonstreren. Het is opgezet met alternatieve bewerkingsplannen die u kunt gebruiken om verschillende scenario's met onderaannemers te demonstreren. De waarderingsmethode is *Standaard*.  

- **SP-SCM1011 Airpot Duo**  

  Dit product vereist het traceren van artikelen en heeft een onderdeel dat eveneens artikeltracering vereist. De waarderingsmethode is *Specifiek*.  

- **SP-SCM1004 Autodrip**  

  Dit product is een stuklijst met een subassemblage, **Bewerkingsplan**. We adviseren om de verschillende spoelmethoden voor zowel componenten als bewerkingen te demonstreren. De waarderingsmethode is *Standaard*.

- **SP-SCM1006 AutoDripLite**

  Dit product heeft drie varianten en drie stuklijsten (BOM's) die kunnen worden toegewezen aan SKU's. Het product maakt gebruik van het concept van phantom-stuklijsten. De waarderingsmethode is *Standaard*.

De productieactiviteiten voor alle scenario's gebruiken de locatie *NOORD*.  

> [!IMPORTANT]
> Boek alle artikeldagboekregels met beginsaldi voordat u een van de scenario's voor Contoso Coffee gaat uitvoeren. Zie de sectie [Contoso Coffee-gegevens instellen](#set-up-contoso-coffee-manufacturing-data) voor meer vereisten.

## <a name="set-up-contoso-coffee-manufacturing-data"></a><a name="set-up-contoso-coffee-manufacturing-data"></a><a name="set-up-contoso-coffee-manufacturing-data"></a>Contoso Coffee-productiegegevens instellen

Als u de demogegevens voor Contoso Coffee-productie wilt gebruiken, moet u twee apps in het desbetreffende bedrijf in [!INCLUDE [prod_short](../../includes/prod_short.md)] installeren:  

- **Gegevensset voor demo van Contoso Coffee**  

    Deze app levert demogegevens voor de basistoepassing.  
- **Gegevensset voor demo van Contoso Coffee (land-id)**  

    Deze app voegt landspecifieke inhoud toe bovenop de basistoepassing.

Voeg de apps toe aan een leeg bedrijf in een betaald abonnement of als onderdeel van een proefperiode. Maak bijvoorbeeld een nieuw bedrijf zonder voorbeeldgegevens op basis van de begeleide instelling **Nieuw bedrijf maken** die u kunt openen vanuit de lijst **Bedrijven**. Voeg vervolgens de apps toe vanuit de [marktplaats](../../ui-extensions-install-uninstall.md#install) als deze nog niet in de lijst op de pagina **Extensiebeheer** voorkomen.  

Zodra de relevante apps zijn geïnstalleerd, gaat u naar de pagina [Demogegevens voor Contoso Coffee](https://businesscentral.dynamics.com/?page=4760) in [!INCLUDE [prod_short](../../includes/prod_short.md)] en wijzigt u de standaardinstellingen om aan uw behoeften te voldoen. De volgende tabel beschrijft de instellingen:  

|Veld  |Omschrijving  |
|---------|---------|
|**Beginjaar** |Hiermee wordt het eerste jaar opgegeven dat u wilt gebruiken voor de demonstratiegegevens van Contoso Coffee. Afhankelijk van de bedrijfsconfiguratie is het jaar een kalenderjaar of een boekjaar.|
|**Productielocatie** |Hiermee wordt het magazijn opgegeven die u wilt gebruiken voor productiebewerkingen. De standaardoptie is *NOORD*, maar u kunt deze naar wens wijzigen.|
|**Bedrijfstype**    |Hiermee wordt aangegeven of het huidige bedrijf btw of omzetbelasting moet aangeven. |
|**Binnenland - Algemene bedrijfsboekingsgroep**|Hiermee wordt een bedrijfscode voor binnenlandse klanten en leveranciers opgegeven. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Capaciteit - Algemene productboekingsgroep**    |Hiermee wordt een code opgegeven voor artikelen of resources die moeten worden gebruikt voor het boeken van capaciteit.|
|**Detailhandel - Algemene productboekingsgroep**    |Hiermee wordt een code opgegeven voor artikelen of resources die moeten worden gebruikt voor het boeken van detailhandel.|
|**Grondstoffen - Algemene productboekingsgroep**    |Hiermee wordt een code opgegeven voor artikelen of resources die moeten worden gebruikt voor het boeken van grondstoffen. |
|**Basis-btw-code**    |Hiermee wordt een bestaande btw-productgroep opgegeven die wordt gebruikt voor artikelen.|
|**Voltooide code**    |Hiermee wordt een bestaande btw-productgroep opgegeven die wordt gebruikt voor voltooide artikelen.|
|**Prijsfactor**     |Hiermee wordt een factor opgegeven om een prijs om te rekenen van USD/EUR naar de lokale valuta. *1* betekent dat de prijs hetzelfde bedrag is in elke valuta. Er wordt een hoger getal gebruikt om de prijs in de lokale valuta weer te geven. |
|**Afrondingsprecisie**  |Hiermee wordt gedefinieerd hoe berekende verbruiksaantallen worden afgerond wanneer deze worden ingevoerd op de verbruiksdagboekregels. Aantallen van minder dan 0,5 worden naar beneden afgerond. Aantallen gelijk aan of hoger dan 0,5 worden naar boven afgerond.|

Als u gereed bent, kiest u de actie **Demogegevens maken**. Het duurt een paar minuten om de gegevens aan de onderliggende database toe te voegen, maar dan bent u klaar om de verschillende scenario's uit te voeren.  

## <a name="scenarios"></a><a name="scenarios"></a><a name="scenarios"></a>Scenario's

De productiedemogegevens van Contoso Coffee ondersteunen momenteel de volgende scenario's voor testen en trainen:

1. [Een nieuwe productiestuklijst en stuklijstversie maken](create-new-production-bom-version.md)  
2. [Een nieuw bewerkingsplan maken](create-new-routing.md)  
3. [Een nieuwe vast geplande productieorder maken en deze wijzigen](create-firm-planned-production-order-change.md)  
4. [Automatisch en handmatig afboeken combineren](combine-automatic-manual-flushing.md)  
5. [Orderplanning gebruiken om voorraad te maken en te reserveren](order-planning-create-reserve-supply.md)  
6. [Een uitbestedingsbewerkinge instellen en verwerken](set-up-process-subcontracting-operation.md)  
7. [Nieuwe capaciteit instellen](set-up-new-capacity.md)  
8. [Vraag voorspellen voor artikelvarianten met verschillende toegewezen stuklijsten](variants.md)  

Lees de stappen voor elk scenario in het desbetreffende artikel.  

> [!IMPORTANT]
> Deze procedures vereisen dat de gebruikerservaring is ingesteld op *Premium* op de pagina **Bedrijfsgegevens**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Productie](../../production-manage-manufacturing.md)  
[Productierapporten en analyses in Business Central](../../production-reports.md)  
