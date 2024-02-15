---
title: Copilot-gegevensverplaatsing tussen geografieën
description: 'Ontdek hoe gegevens die worden gebruikt in copilot-functies in Dynamics 365 Business Central, zich verplaatsen tussen geografieën waar Azure OpenAI Service standaard niet beschikbaar is.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 11/30/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="copilot-data-movement-across-geographies"></a>Copilot-gegevensverplaatsing tussen geografieën

Copilot is beschikbaar in alle ondersteunde [geografische Business Central-landen/regio's](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Copilot gebruikt echter Microsoft Azure OpenAI Service, wat momenteel alleen in bepaalde geografische regio's beschikbaar is voor Business Central. Dit betekent dat als uw omgeving zich elders bevindt, gegevens van de Copilot- en generatieve AI-functies buiten uw geografische regio moeten worden verzonden en mogelijk buiten uw nalevingsgrenzen worden verwerkt en opgeslagen. Gegevens omvatten de AI-prompts en uw bedrijfsgegevens die worden gebruikt of gegenereerd door Copilot. In dit geval moet u inschakelen dat u gegevensverplaatsing naar een Azure OpenAI Service in een andere geografie toestaat. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Als uw omgeving zich in dezelfde Azure-regio bevindt als de Azure OpenAI Service, maakt deze automatisch verbinding met Azure OpenAI Service; er is geen optie en er is geen eenmalige configuratie vereist.

> [!NOTE]
> Individuele Copilot- en generatieve AI-functies zijn mogelijk niet in alle Business Central-landen/regio's beschikbaar. Neem contact op met de uitgever van elke mogelijkheid om de beschikbaarheid te begrijpen.
> 
> Copilot- en generatieve AI-functies van niet-Microsoft-uitgevers, zoals die afkomstig zijn van aanpassingen of AppSource-apps die u installeert, definiëren elk hun eigen specifieke Azure OpenAI Service-regio's. Neem contact op met de uitgever van de extensie om na te gaan welke regionale Azure-services door de extensie worden gebruikt. 

### <a name="azure-openai-service-geographies"></a>Azure OpenAI Service-geografieën

In de volgende tabel ziet u de geografie van de Azure OpenAI Service die door Copilot wordt gebruikt, gebaseerd op de Azure-regio van een Business Central-omgeving. Deze informatie is belangrijk bij de beslissing of u zich wilt aanmelden voor gegevensverplaatsing tussen geografische gebieden. U kunt de Azure-regio voor uw omgeving identificeren in het Business Central-beheercentrum (zie [Omgevingen beheren in het beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Omgeving Azure-regio| Azure OpenAI Service-geografie|Beheerdersactie vereist om Copilot te ontgrendelen| 
| - | - | - |
|Azië (Oost, Zuidoost) |Verenigde Staten|Ja|
|Australië (Zuidoost)| Verenigde Staten |Ja |
|Brazilië (Zuid) |Verenigde Staten|Ja|
|Canada (Centraal, Oost)|Verenigde Staten|Ja|
|Europa (West, Noord)| Zweden of Zwitserland |Ja|
|Frankrijk (Centraal, Zuid)| Zweden of Zwitserland |Ja|
|Duitsland (Noord, West-Centraal)| Zweden of Zwitserland |Ja|
|India (Centraal, Zuid)|Verenigde Staten|Ja|
|Japan (Oost, West)|Verenigde Staten|Ja|
|Korea (Centraal, Zuid)|Verenigde Staten|Ja|
|Noorwegen (Oost, West)|Zweden of Zwitserland |Ja|
|Zuid-Afrika (Noord, West)|Verenigde Staten|Ja|
|Zwitserland (Noord, West) |Zweden of Zwitserland |Ja|
|Verenigde Arabische Emiraten (Noord, West)|Verenigde Staten|Ja|
|Verenigd Koninkrijk (Zuid, West)|Verenigd Koninkrijk|Ja|
|Verenigde Staten (Centraal, Oost, Noord-Centraal, Zuid-Centraal, West) |Verenigde Staten|Nee|

> [!NOTE]
> Nadat een Azure OpenAI Service beschikbaar is geworden in uw Business Central-geografie, wordt uw omgeving automatisch overgezet naar het gebruik van de Azure OpenAI Service en is aanmelden niet nodig of zelfs mogelijk.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## <a name="next-steps"></a>Volgende stappen

U meldt zich aan om gegevensverplaatsing tussen geografieën toe te staan vanaf de pagina [Copilot- en AI-mogelijkheden](https://businesscentral.dynamics.com/?page=7775). Ga voor meer informatie naar [Gegevensverplaatsing tussen geografische gebieden toestaan](enable-ai.md#allow-data-movement-across-geographies).
