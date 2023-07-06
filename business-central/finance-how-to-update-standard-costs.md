---
title: Vaste verrekenprijs bijwerken
description: U moet regelmatig de vaste verrekenprijzen van onderdelen bijwerken en de nieuwe kosten tot aan het hoofdartikel berekenen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="update-standard-costs"></a><a name="update-standard-costs"></a><a name="update-standard-costs"></a>Vaste verrekenprijs bijwerken
U moet regelmatig de vaste verrekenprijzen van onderdelen bijwerken en de nieuwe kosten tot aan het hoofdartikel berekenen. Het proces bestaat meestal uit de volgende vier stappen:  

1.  Kosten bijwerken op het niveau van onderdeel en capaciteit. Zie voor meer informatie de batchverwerking **Vaste verrekenprijs artikel voorstellen**.  
2.  Het consolideren en berekenen van de materiaal- en capaciteitskosten om de totale productiekosten van de artikelen te berekenen.  
3.  De vaste verrekenprijzen implementeren die worden ingevoerd wanneer u de vorige batchverwerkingen uitvoert. De vaste verrekenprijzen worden pas van kracht nadat ze zijn geïmplementeerd. Gebruik de batchverwerking **Vaste verrekenprijswijzigingen doorvoeren**, die de wijzigingen in de standaardkosten voor artikelen bijwerkt met die in de tabel Standaardkostenwerkblad.  
4.  De wijzigingen implementeren om het veld **Kostprijs** op de artikelkaart bij te werken en voorraadherwaardering uit te voeren. Zie [Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.  

Zie [Vaste verrekenprijs berekenen](finance-about-calculating-standard-cost.md) voor nadere informatie.
  
## <a name="to-update-standard-costs"></a><a name="to-update-standard-costs"></a><a name="to-update-standard-costs"></a>Vaste verrekenprijs aanpassen

1.  Voer de batchverwerking **Kostprijs herwaarderen - Artikelposten** uit.  
2.  Voer de batchverwerking **Voorraadwaarde boeken** uit.  
3.  Open het **Vaste-verrekenprijsvoorstel** en gebruik een of meer van de volgende functies:  

    1.  Voer de batchverwerking **Vaste verrekenprijs artikel voorstellen** uit.  
    2.  Bekijk de resultaten en breng desgewenst wijzigingen aan.  
    3.  Voer de batchverwerking **Vaste verrekenprijs capaciteit voorstellen** uit.  
    4.  Bekijk de resultaten en breng desgewenst wijzigingen aan.
    5. Voer de batchverwerking **Vaste verrekenprijs berekenen** uit.
    6.  Bekijk de resultaten en breng desgewenst wijzigingen aan.
    7.  Voer de batchverwerking **Vaste verrekenprijswijzigingen doorvoeren** uit.  
4.  Bekijk en boek de pagina **Herwaarderingsdagboek** waarin de posten uit de vorige stappen in dit proces staan.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

 [Informatie over het berekenen van vaste verrekenprijzen](finance-about-calculating-standard-cost.md)   
 [Voorraadkosten beheren](finance-manage-inventory-costs.md)   
 [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md) [Financiën](finance.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
