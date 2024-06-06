---
title: Servicebeheerprocessen instellen
description: Leer hoe u processen instelt om ervoor te zorgen dat uw klanten tevreden zijn over uw services.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="configure-service-management-processes"></a>Processen voor servicebeheer configureren

Hier volgende enkele voorbeelden van de instellingen die u op processen voor servicebeheer kunt toepassen:  
  
* Enkele algemene instellingen voor verschillende processen, zoals waarschuwingen, volgende serviceberekeningen voor serviceartikelen, het te evalueren starttarief, het te gebruiken probleemrapportageniveau, enzovoort.  
* De soorten gegevens die door technici moeten worden ingevoerd in servicedocumenten. U kunt bijvoorbeeld verplicht stellen dat het soort order, de begin- en/of einddatums voor het werk en het soort werk dat is uitgevoerd worden opgegeven.  
* Sommige standaardinstellingen voor responstijden en garanties. Deze omvatten een standaardresponstijd voor het starten van de service, garantiekortingspercentages voor onderdelen en arbeidskosten en hoe lang garanties geldig zijn.  
* Instellingen voor contracten, zoals het maximumaantal dagen dat u voor contractserviceorders kunt gebruiken, of er redencodes moeten worden gebruikt wanneer een contract wordt geannuleerd, standaardteksten voor omschrijvingen en contractwaarden.  
* De nummerreeksen die moeten worden gebruikt voor servicegerelateerde documenten en artikelen.  

## <a name="to-enter-general-and-mandatory-settings"></a>Algemene en verplichte instellingen opgeven

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicebeheerinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="set-up-service-invoice-posting-policies-for-users"></a>Boekingsbeleid voor servicefacturen instellen voor gebruikers

Bedrijven hebben vaak unieke processen voor facturen en zendingen. Processen kunnen bijvoorbeeld variëren van één persoon die alles op een serviceorder plaatst tot meerdere medewerkers die elk met hun eigen pagina's werken.

U kunt boekingsbeleid gebruiken om te voorkomen dat gebruikers servicefacturen boeken, of om van hen te eisen dat zij facturen samen met de gerelateerde serviceverzending boeken. Kies op de pagina **Gebruikersinstellingen** in het veld **Boekingsbeleid voor servicefacturen** een van de volgende opties om een boekingsbeleid in te stellen:

* **Toegestaan** (Standaard): behoud het huidige gedrag, waarbij u de te gebruiken boekingsopties kunt kiezen, zoals **Verzenden**, **Factuur**, en **Verzenden en factuur**.
* **Verboden**: voorkom dat servicefacturen worden geboekt. [!INCLUDE [prod_short](includes/prod_short.md)] toont een bevestigingsvenster dat alleen de optie **Verzending** bevat.
* **Verplicht**: facturen moeten samen met servicezendingen worden geboekt. [!INCLUDE [prod_short](includes/prod_short.md)] toont een bevestigingsvenster dat alleen de optie **Verzenden en factureren** bevat.

Deze instelling is van invloed op de volgende documenten:

* Serviceorders
* Magazijnverzendingen
* Servicefacturen
* Servicecreditnota's

De volgende tabel beschrijft de effecten op verschillende documenten.

|Document  |Toestaan<br>Geeft een reeks opties weer   |Verboden<br>Bevestigingsvenster  |Verplicht<br>Bevestigingsvenster  |
|---------|---------|---------|---------|
|Serviceorder     | * Verzenden<br>* Factureren<br>* Verzenden en factureren<br>* Verzenden en verbruiken         |* Verzenden<br>* Verzenden en verbruiken  |Wilt u de verzending en factuur boeken?         |
|Magazijnverzending     |* Verzenden<br>* Verzenden en factureren         |Wilt u de verzending boeken?         | Wilt u de verzending en factuur boeken?        |
|Servicefactuur     | Wilt u de factuur boeken?         | Fout: u kunt niet boeken.       |Wilt u de factuur boeken?         |
|Servicecreditnota     | Wilt u de creditnota boeken?         | Fout: u kunt niet boeken.        |Wilt u de creditnota boeken?         |

> [!NOTE]
> Wanneer u servicefacturen en creditnota's boekt, hebt u geen boekingsopties. De documenten boeken altijd fysieke en financiële transacties samen. U kunt servicefacturen en creditnota's niet gedeeltelijk boeken.

## <a name="see-also"></a>Zie ook

[Foutrapportage instellen](service-how-setup-fault-reporting.md)  
[Resourcetoewijzing instellen](service-how-setup-resource-allocation.md)  
[Codes voor standaardservices instellen](service-how-setup-service-coding.md)  
[Aanvullende kosten voor services instellen](service-how-setup-service-costs-pricing.md)  
[Troubleshooting instellen](service-how-setup-troubleshooting.md)  
[Servicebeheer](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
