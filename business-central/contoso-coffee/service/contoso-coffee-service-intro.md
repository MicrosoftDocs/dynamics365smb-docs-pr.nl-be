---
title: Inleiding tot Contoso Coffee-servicebeheer
description: In dit artikel maakt u kennis met de Contoso Coffee-demonstratiegegevens voor servicebeheer.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Inleiding tot Contoso Coffee-servicebeheer

Contoso Coffee is een fictief bedrijf dat koffiezetapparaten voor consumenten en bedrijven maakt. De **Contoso Coffee**-apps voor Business Central voegen demogegevens toe die u kunt gebruiken om te leren hoe u de servicebeheermogelijkheden in Business Central kunt benutten.

Deze app biedt verschillende elementen die worden gebruikt voor de belangrijkste procedures:

- Resources met toegewezen vaardigheden
- Artikelen die zijn geconfigureerd om serviceartikelen maken
- Leenartikelen

> [!IMPORTANT]
> Boek alle artikeldagboekregels met beginsaldi voordat u een van de scenario's voor Contoso Coffee gaat uitvoeren. Zie de sectie [Contoso Coffee-gegevens instellen](#set-up-contoso-coffee-service-management-data) voor meer vereisten.
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Contoso Coffee-servicebeheergegevens instellen

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Zodra de relevante apps zijn geïnstalleerd, gaat u naar de pagina [Demohulpmiddel van Contoso](https://businesscentral.dynamics.com/?page=5194) in [!INCLUDE [prod_short](../../includes/prod_short.md)], selecteert u de regel *Servicemodule* en gebruikt u de actie **Configureren** om de modules voor te bereiden. De volgende tabel beschrijft de instellingen:  

|Veld  |Omschrijving  |
|---------|---------|
|**Klantnr.**  |De klant die moet worden gebruikt voor de scenario's in verkoopbewerkingen.|
|**Leveranciersnr.**  |De leverancier die moet worden gebruikt voor alle scenario's bij inkoopactiviteiten.|
|**Nr. voor artikel 1**  |Het artikel dat voor de reparatie- en onderhoudsscenario's moet worden gebruikt.|
|**Nr. van serviceartikelnr. 1**  |Het artikel van het type service dat het herstelscenario moet gebruiken.|
|**Nr. van serviceartikelnr. 2**  |Het artikel van het type service dat het herstelscenario moet gebruiken.|
|**Nr. van resource 1**  |De resource die voor de contractscenario's moet worden gebruikt.|
|**Nr. van resource 2**  |De resource die voor de break-fixscenario's moet worden gebruikt.|
|**Servicevestiging** |Hiermee wordt het magazijn opgegeven die u wilt gebruiken voor servicebewerkingen. De standaard is *HOOFD*, maar u kunt deze naar wens wijzigen.|

Als u gereed bent, kiest u de actie **Demogegevens maken**. Het duurt een paar minuten om de gegevens aan de onderliggende database toe te voegen, maar dan bent u klaar om de verschillende scenario's uit te voeren.  

## <a name="scenarios"></a>Scenario's

De demogegevens voor Contoso Coffee ondersteunen momenteel de volgende servicescenario's voor testen en trainen:

1. Maak een serviceorder voor ad-hoc reparatieverzoeken, plaats en ontvang leenartikelen, registreer tijd en factureer klanten [Procedure van serviceorders voor serviceartikelen](service-basic-flow-order.md)
2. Creëer servicecontracten, genereer serviceorders, factureer contractkosten en wijs resources toe [Procedure van servicecontracten voor serviceartikelen](service-contract-flow.md)

Lees de stappen voor elk scenario in het desbetreffende artikel.  

> [!IMPORTANT]
> De serviceprocedures vereisen dat de gebruikerservaring is ingesteld op **Premium** op de pagina **Bedrijfsgegevens**.


## <a name="see-also"></a>Zie ook

[Onderhoud](../../service-service.md)
