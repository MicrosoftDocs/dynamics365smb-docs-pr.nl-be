---
title: Inleiding tot Contoso Coffee-projectbeheer
description: In dit artikel maakt u kennis met de Contoso Coffee-demonstratiegegevens voor projecten en projectbeheer.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-jobs-and-project-management"></a>Inleiding tot Contoso Coffee-projecten en projectbeheer

Contoso Coffee is een fictief bedrijf dat koffiezetapparaten voor consumenten en bedrijven maakt. De **Contoso Coffee**-apps voor Business Central voegen demogegevens toe die u kunt gebruiken om te leren hoe u de mogelijkheden in Business Central voor projecten en projectbeheer kunt benutten.

Deze app biedt verschillende elementen die worden gebruikt voor de belangrijkste procedures:

- Resources met toegewezen vaardigheden en zones
- Artikelen die zijn geconfigureerd om serviceartikelen maken

> [!IMPORTANT]
> Boek alle artikeldagboekregels met beginsaldi voordat u een van de scenario's voor Contoso Coffee gaat uitvoeren. Zie de sectie [Contoso Coffee-gegevens instellen](#set-up-contoso-coffee-jobs-and-project-management-data) voor meer vereisten.
>
> 
## <a name="set-up-contoso-coffee-jobs-and-project-management-data"></a>Contoso Coffee-projecten en projectbeheergegevens instellen

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Zodra de relevante apps zijn geïnstalleerd, gaat u naar de pagina [Demogegevens van Contoso Coffee-projecten](https://businesscentral.dynamics.com/?page=4767) in [!INCLUDE [prod_short](../../includes/prod_short.md)] en wijzigt u de standaardinstellingen om aan uw wensen te voldoen. In de volgende tabellen worden de instellingen beschreven:  

|Veld  |Omschrijving  |
|---------|---------|
|**Beginjaar** |Hiermee wordt het eerste jaar opgegeven dat u wilt gebruiken voor de demonstratiegegevens van Contoso Coffee. Afhankelijk van de bedrijfsconfiguratie is het jaar een kalenderjaar of een boekjaar.|
|**Klantnr.**  |De klant die moet worden gebruikt voor de scenario's in verkoopbewerkingen.|
|**Nr. voor artikel 1**  |Het artikel dat voor de contractscenario's moet worden gebruikt.|
|**Nr. voor artikel 2**  |Het artikel dat voor de break-fixscenario's moet worden gebruikt.|
|**Nr. van lokale resource 1**  |De resource die voor de contractscenario's moet worden gebruikt.|
|**Nr. van externe resource 1**  |De resource die voor de break-fixscenario's moet worden gebruikt.|
|**Klantboekingsgroep**|Specificeert een bedrijfscode voor binnenlandse klanten. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Algemene bedrijfsboekingsgroep**|Specificeert een bedrijfscode voor binnenlandse klanten. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Binnenland - algemene bedrijfsboekingsgroep**|Hiermee wordt een bedrijfscode voor binnenlandse klanten en leveranciers opgegeven. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Wederverkoop - voorraadboekingsgroep**    |Specificeert een code voor artikelen die moeten worden gebruikt voor het boeken van wederverkoop.|
|**Detailhandel - Algemene productboekingsgroep**    |Specificeert een code voor artikelen die moeten worden gebruikt voor het boeken van detailhandel.|
|**Btw-productboekingsgroep**    |Specificeert een btw-productcode voor artikelen voor het boeken van btw als btw is ingeschakeld.|
|**Prijsfactor**     |Hiermee wordt een factor opgegeven om een prijs om te rekenen van USD/EUR naar de lokale valuta. *1* betekent dat de prijs hetzelfde bedrag is in elke valuta. Er wordt een hoger getal gebruikt om de prijs in de lokale valuta weer te geven. |
|**Afrondingsprecisie**  |Hiermee wordt gedefinieerd hoe berekende verbruiksaantallen worden afgerond wanneer deze worden ingevoerd op de verbruiksdagboekregels. Aantallen van minder dan 0,5 worden naar beneden afgerond. Aantallen gelijk aan of hoger dan 0,5 worden naar boven afgerond.|

Als u gereed bent, kiest u de actie **Demogegevens maken**. Het duurt een paar minuten om de gegevens aan de onderliggende database toe te voegen, maar dan bent u klaar om de verschillende scenario's uit te voeren.  

## <a name="see-also"></a>Zie ook
