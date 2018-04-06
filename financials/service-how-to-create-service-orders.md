---
title: Serviceorders maken | Microsoft Docs
description: In het venster **Serviceorder** kunt u documenten maken waarin u op aanvraag van de klant voor serviceartikelen gegevens invoert over een service, als bijvoorbeeld herstel en onderhoud.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5460f50c4c556a74b518976d5d5fa90203f16967
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-service-orders"></a>Serviceorders maken
In het venster **Serviceorder** kunt u documenten maken waarin u op aanvraag van de klant voor serviceartikelen gegevens invoert over een service, als bijvoorbeeld herstel en onderhoud.  
  
Wanneer u een serviceorder maakt, hoeft u slechts een paar velden in te vullen. Sommige velden zijn optioneel en veel worden automatisch ingevuld wanneer u verwante velden invult.  
  
## <a name="to-create-a-service-order"></a>Serviceorders maken    
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorders** in en klik op de gerelateerde koppeling.  
2. Maak een nieuwe serviceorder.  
3. Selecteer in het veld **Nr.** een nummer voor de serviceorder in.  
  
     Als u in het venster **Servicebeheerinstellingen** nummerreeksen voor serviceorders hebt ingesteld, kunt u ook op Enter drukken om het eerstvolgende beschikbare serviceordernummer in te voeren.  
  
4. Voer in het veld **Klantnr.** de betreffende klant uit de lijst. De betreffende velden voor de klant worden automatisch ingevuld met gegevens uit de tabel **Klant**.  
  
5. Afhankelijk van de instellingen op het sneltabblad **Verplichte velden** in het venster **CRM - Service-instellingen** moet u wellicht het veld **Serviceordersoort** en het veld **Verkoper** invullen.  
6. Het invullen van de overige velden is optioneel.  
7. Registreer de serviceartikelregels.  

## <a name="to-create-a-service-order-from-a-contract"></a>Serviceorders maken van contracten  
U kunt automatisch serviceorders voor het onderhoud van serviceartikelen maken op basis van servicecontracten.  
  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Contractserviceorders maken** in en klik vervolgens op de gerelateerde koppeling.  
2. Stel op het sneltabblad **Servicecontractkop** de gewenste filters in.  
3. Op het Sneltabblad **Opties** vult u de velden **Begindatum** en **Einddatum** in met de begindatum en einddatum van de periode waarvoor u contractserviceorders wilt maken. Met de batchverwerking maakt u serviceorders waarin serviceartikelen in servicecontracten zijn opgenomen met de volgende geplande servicedatums in deze periode.  
  
    > [!NOTE]  
    >  Er is een limiet aan het aantal dagen dat u als het datuminterval voor de batchtaak kunt gebruiken. U bepaalt de beperking in het veld **Max. dagen contractserviceorder** in het venster **Servicebeheerinstellingen**.  
  
4. Kies in het veld **Actie** de optie **Serviceorder maken**.  

## <a name="to-convert-a-service-quote-to-a-service-order"></a>Een serviceofferte omzetten in een serviceorder
Wanneer een klant een servicecontractofferte heeft geaccepteerd, zet u deze om in een serviceorder. De offerte wordt verwijderd en er wordt een nieuwe serviceorder ingesteld met dezelfde omschrijving als de serviceofferte. De responsdatum en -tijd worden opnieuw berekend voor de serviceorder en de status van de serviceorder wordt ingesteld op **In behandeling**. De herstelstatus van de serviceartikelen in de order wordt gewijzigd in **Eerste**.  
  
In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt gezocht naar toewijzingsposten voor alle serviceartikelen met de status **Actief** in de serviceofferte. Als dergelijke toewijzingsposten worden gevonden, wordt de toewijzingsstatus gewijzigd in **Hertoewijzing vereist**. Wanneer u de serviceartikelen in de serviceorder opnieuw toewijst, wordt de status van de geregistreerde toewijzingsposten voor de order gewijzigd in **Gereedgemeld**.   

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Servicecontractoffertes** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de serviceofferte die u wilt omzetten in een serviceorder.  
3. Kies de actie **Order maken**.  

## <a name="to-check-item-availability-for-one-or-more-orders"></a>Artikelbeschikbaarheid voor een of meer orders controleren  
U kunt controleren en bekijken of een artikel dat u nodig hebt om een order af te handelen op voorraad is en als dat niet het geval is, wanneer het artikel beschikbaar zal zijn. Daarna kunt u dan, als een artikel beschikbaar is voor reservering, dit artikel reserveren om er zeker van te zijn dat het beschikbaar is voor uw gebruik. U kunt de beschikbaarheid voor een bepaalde order of voor alle orders controleren.  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Planbord** in en klik vervolgens op de gerelateerde koppeling.  
2. Ga op een van de volgende manieren te werk:  
  
    * Als u de beschikbaarheid voor een bepaalde order wilt controleren, kiest u de actie **Vraagoverzicht**.  
    * Voor alle orders kiest u **Document weergeven**. Het venster **Serviceorder** wordt geopend.  
  
3. Vouw op de pagina **Vraagoverzicht** de artikelgroepering uit en bekijk informatie over de beschikbaarheid van het artikel. U kunt bijvoorbeeld zien hoeveel artikelen op voorraad zijn. U kunt ook zien of een artikel beschikbaar is of dat het is nabesteld, dat betekent Type bron = aankoop, of wanneer deze is gereserveerd. 

## <a name="to-reserve-an-item-for-a-service-order"></a>Een artikel voor een serviceorder reserveren
Als u er zeker van wilt zijn dat een artikel voor een serviceorder beschikbaar is, kunt u het artikel reserveren. 

1. Geef in het venster **Zoeken** **Serviceorders** op en kies vervolgens de gerelateerde koppeling.  
2. Kies de serviceorder en kies **Bewerken**.  
3. Kies **Acties**, kies **Order** en kies **Serviceregels**.  
4. Op de pagina **Serviceregels** kiest u het artikel dat u wilt reserveren en vervolgens kiest u de actie **Reserveren**.  
5. Op de pagina **Reservering** kiest u **Huidige regel reserveren**. 

## <a name="to-insert-lines-based-on-standard-service-codes"></a>Regels invoegen op basis van standaardservicecodes  
Als u standaardservicecodes hebt ingesteld en deze hebt toegewezen aan serviceartikelgroepen, kunt u de standaardregels invoegen die zijn gekoppeld aan de standaardservicecodes op servicedocumenten. Zie voor meer informatie [Standaardservicecodes instellen](service-how-setup-service-coding.md).   

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorders** in en klik op de gerelateerde koppeling.  
2. Maak een nieuwe serviceorder.  
3. Vul de velden in.  
4. Vul de vereiste gegevens in op de serviceartikelregels.  
5. Kies de regel met het serviceartikel waarvoor u serviceregels wilt maken en kies **Std. servicecodes ophalen**. Het venster **Std. serviceartikelgroepcodes** wordt geopend met de standaardcodes voor de serviceartikelgroep die op de regel zijn opgegeven.  
6. Kies de juiste code en kies de knop **OK** om de standaardserviceregels in te voeren.  
  
> [!NOTE]  
>  Als het veld **Serviceartikelgroepcode** op de serviceartikelregel van het document leeg is, betekent dit dat het serviceartikel niet tot een serviceartikelgroep behoort. In dit geval bevat het venster **Std. serviceartikelgroepcodes** een overzicht van alle standaard servicecodes. Selecteer uit de lijst om standaardserviceregels in het document in te voegen. U kunt ook selecteren uit de lijst met standaard service-codes toegewezen aan een bepaald serviceartikelgroep. Om de lijst weer te geven, selecteert u de relevante code in het veld **Serviceartikelgroepcode** in het venster **Std. serviceartikelgroepcodes**.  

## <a name="to-register-internal-or-public-comments"></a>Interne of openbare opmerkingen registreren
U kunt opmerkingen toevoegen die op serviceorders en serviceoffertes kunnen worden afgedrukt om extra informatie te bieden. U kunt maximaal 80 tekens, inclusief spaties, toevoegen. Als u extra tekst wilt invoeren, kiest u een andere regel. Als u een opmerking wilt registreren, kiest u een regel en kiest u de actie **Opmerkingen**.  

## <a name="to-delete-invoiced-service-orders"></a>Gefactureerde serviceorders verwijderen  
Wanneer orders volledig zijn gefactureerd, worden ze doorgaans automatisch verwijderd. Wanneer een factuur wordt geboekt, wordt een bijbehorende post gemaakt in het venster **Geboekte servicefacturen**. U kunt het geboekte document bekijken op de pagina **Geboekte servicefactuur**.  
  
Serviceorders worden echter niet automatisch verwijderd als het totale aantal op de order niet vanuit de serviceorder zelf is geboekt, maar vanuit het venster **Servicefactuur**. In dit geval zult u wellicht gefactureerde orders die niet zijn verwijderd, zelf moeten verwijderen. Hiervoor kunt u de batchverwerking **Gefactureerde serviceorders verwijderen** uitvoeren.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gefactureerde serviceorders verwijderen** in en klik vervolgens op de gerelateerde koppeling. Het opvraagvenster voor de batchverwerking **Gefactureerde serviceorders verwijderen** wordt geopend.  
2. U kunt de orders selecteren die u wilt verwijderen door filters in te stellen in de velden **Nr.**, **Klantnr.** en **Factureren aan**. in.  
3. Klik op **OK**.  


## <a name="see-also"></a>Zie ook  
[Serviceboekingen](service-service-posting.md)  
[Een serviceorder boeken](service-how-to-post-service-orders.md)  
[CRM - Service instellen](service-setup-service.md)  
[Werken aan servicetaken](service-how-to-work-on-service-tasks.md)  
[Resources toewijzen](service-how-to-allocate-resources.md)  

