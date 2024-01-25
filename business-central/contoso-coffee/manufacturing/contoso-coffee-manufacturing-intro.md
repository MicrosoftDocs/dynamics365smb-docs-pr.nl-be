---
title: Inleiding tot Contoso Coffee-productie
description: Overzicht van scenario's voor hoe demogegevens voor Contoso Coffee u kunnen helpen bij het leren gebruiken van de productiemogelijkheden in Business Central.
ms.date: 04/01/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '4765,'
author: brentholtorf
ms.author: bholtorf
---

# Inleiding tot Contoso Coffee-productie

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

De productieactiviteiten voor alle scenario's gebruiken de locatie *HOOFD*.  

> [!IMPORTANT]
> Boek alle artikeldagboekregels met beginsaldi voordat u een van de scenario's voor Contoso Coffee gaat uitvoeren. Zie de sectie [Contoso Coffee-gegevens instellen](#set-up-contoso-coffee-manufacturing-data) voor meer vereisten.

## Contoso Coffee-productiegegevens instellen

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

|Veld  |Omschrijving  |
|---------|---------|
|**Productievestiging** |Hiermee wordt het magazijn opgegeven die u wilt gebruiken voor productiebewerkingen. De standaard is *HOOFD*, maar u kunt deze naar wens wijzigen.|


Als u gereed bent, kiest u de actie **Demogegevens maken**. Het duurt een paar minuten om de gegevens aan de onderliggende database toe te voegen, maar dan bent u klaar om de verschillende scenario's uit te voeren.  

## Scenario's

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

## Zie ook

[Productie](../../production-manage-manufacturing.md)  
[Productierapporten en analyses in Business Central](../../production-reports.md)  
