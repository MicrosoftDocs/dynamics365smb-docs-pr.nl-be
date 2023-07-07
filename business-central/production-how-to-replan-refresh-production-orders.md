---
title: Productieorders direct opnieuw plannen of vernieuwen
description: In dit onderwerp worden de procedures beschreven voor het rechtstreeks opnieuw plannen van productieorders en het vernieuwen van productieorders.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000842, 99000843, 99000861, 99000862, 99000863'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="replan-or-refresh-production-orders-directly"></a>Productieorders rechtstreeks opnieuw plannen of vernieuwen

De functie **Herplannen** in productieorders wordt doorgaans gebruikt nadat er materialen zijn toegevoegd of gewijzigd die onderliggende productieorders hebben. Met de functie worden wijzigingen berekend die in materiaal- en bewerkingsplanregels zijn aangebracht. De functie heeft betrekking op lagere productiestuklijstniveaus en er kunnen nieuwe productieorders mee worden gegenereerd.  

Op basis van de wijzigingen die u hebt aangebracht in de materiaal- en bewerkingsplanregels, zorgt de functie Herplannen voor het berekenen en plannen van alle nieuwe vraagregels voor de productieorder.  

De functie **Vernieuwen** in productieorders wordt vaak gebruikt nadat u een van de volgende opties hebt uitgevoerd:

- Er is handmatig een productieorder gemaakt om gegevens voor de regel voor het eerst te berekenen en te maken.
- Er zijn wijzigingen in de productieorderkop aangebracht om alle gegevens voor de regel opnieuw te berekenen.

Met de functie Vernieuwen worden wijzigingen berekend die in een productieorderkop zijn aangebracht. Deze functie heeft geen betrekking op productiestuklijstniveaus. De functie Vernieuwen zorgt ervoor dat de waarden voor de materiaal- en bewerkingsplanregels worden berekend en gestart op basis van de hoofdgegevens die in de toegewezen productiestuklijst en het toegewezen bewerkingsplan zijn gedefinieerd, op basis van het orderaantal en de vervaldatum in de kop van de productieorder.

U kunt de productieorderregels handmatig invoegen of de functie gebruiken waarmee de productieorderregels van de kop worden berekend.  

> [!NOTE]
> Als u de functie Vernieuwen gebruikt om productieorderregels opnieuw te berekenen, worden de oude productieorderregels verwijderd en nieuwe regels berekend.  

## <a name="to-replan-a-production-order"></a>Een productieorder herplannen

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorders** in en kies vervolgens de gerelateerde koppeling.  
2. Open de productieorderregel die u opnieuw wilt plannen.  
3. Kies op het sneltabblad **Regels** de actie **Regels** en vervolgens de actie **Materialen**.  
4. Voeg een materiaal toe. (Dat is een geproduceerd artikel of subassemblage.)  
5. Kies vanuit de productieorder de actie **Herplannen**.  

    Definieer op de pagina **Productieorder herplannen** wat en op welke wijze u wilt herplannen.  
6. Selecteer een van de volgende opties in het veld **Planningsrichting**.  

    | Optie | Description |
    |--|--|
    | **Achterwaarts** | Berekent de bewerkingsvolgorde vanaf de vroegst mogelijke einddatum (gedefinieerd door middel van de vervaldatum en/of andere geplande orders) tot de laatst mogelijke begindatum. **Opmerking:** dit is de standaardoptie en van toepassing op de meeste situaties. |
    | **Voorwaarts** | Berekent de bewerkingsvolgorde vanaf de laatst mogelijke begindatum (gedefinieerd door middel van de vervaldatum en/of andere geplande orders) tot de vroegst mogelijke einddatum. **Opmerking:** Deze optie is alleen van toepassing op spoedorders. |

7. Geef in het veld **Plannen** als volgt aan of de productiebehoeften voor geproduceerde artikelen op de productiestuklijst moeten worden berekend.  

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**Geen niveaus**|Kijk niet naar de productie op lager niveau. Hiermee wordt alleen de planning van het artikel bijgewerkt, net zoals bij vernieuwen.|  
    |**Eén niveau**|Het plannen van productievraag op eerste niveau. Er kunnen productieorders van het hoogste niveau worden gemaakt.|  
    |**Alle niveaus**|Het plannen van productievraag alle niveaus. Er kunnen productieorders van alle niveaus worden gemaakt.|  

8. Selecteer **Eén niveau** en kies de knop **OK** om, als de order niet volledig beschikbaar is, de productieorder te herplannen en een nieuwe onderliggende productieorder te berekenen en te maken voor de nieuwe subassemblage.  

> [!NOTE]  
> Wijzigingen die met de functie **Herplannen** worden doorgevoerd, veranderen doorgaans de capaciteitsbehoefte van de productieorder. Het kan dan ook zijn dat u de bewerkingen naderhand opnieuw moet plannen.  

## <a name="to-refresh-a-production-order"></a>Een productieorder vernieuwen

Als u productieorderregels, materialen of bewerkingsplanregels hebt aangepast, moet u de informatie in de productieorder ook vernieuwen. In de volgende procedure worden de materialen berekend voor een vast geplande productieorder. De stappen zijn vergelijkbaar voor bewerkingsplanregels.

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorder** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Zie voor meer informatie [Productieorders maken](production-how-to-create-production-orders.md).  
3. Kies de actie **Vernieuwen**.
4. Selecteer op de pagina **Productieorder vernieuwen** een van de volgende opties:

    |Veld|Optie|Omschrijving|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Planningsrichting**|**Voorwaarts**|De planning begint op de begindatum en verloopt in de richting van de einddatum. U moet de begindatum voor het gebruik van deze optie invullen.|  
    ||**Achterwaarts**|De planning begint op de einddatum en verloopt in de richting van de begindatum.|  
    |**Berekenen**|**Regels**|Selecteer dit veld om de productieorderregels te berekenen.|  
    ||**Bewerkingsplannen**|Dit veld heeft geen invloed op de berekening van de productieorderregels.|  
    ||**Materiaalbehoefte**|Dit veld heeft geen invloed op de berekening van de productieorderregels.|  
    |**Magazijn**|**Inkomend verzoek maken**|Dit veld heeft geen invloed op de berekening van de productieorderregels.|  

5. Kies de knop **OK** om uw selectie te bevestigen. De productieorderregels worden vervolgens berekend.

> [!NOTE]  
> Als u productieordermaterialen berekent, worden de vorige materiaalwijzigingen verwijderd.

## <a name="see-also"></a>Zie ook

[Gepland](production-planning.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
