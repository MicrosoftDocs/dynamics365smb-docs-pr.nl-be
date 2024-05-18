---
title: Duurzaamheidsinstelling
description: Leer hoe u duurzaamheidsfuncties instelt.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/24/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Duurzaamheidsinstelling  

Om de Duurzaamheidsmodule goed te laten werken moet u eerst een aantal basisbedieningen en instructies instellen die betrekking hebben op de gehele functionaliteit.  

Om een ​​duurzaamheidsmodule op te zetten volgt u deze stappen:  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsinstelling** in en kies vervolgens de gerelateerde koppeling.  
2. Configureer op het sneltabblad **Algemeen** de vereiste velden met betrekking tot deze module:   

|  Veld  |  Omschrijving  |  
|--------|--------------| 
| **Code van eenheid voor uitstoot** | Hiermee wordt de code opgegeven van de eenheid die wordt gebruikt om uitstoot te registreren. |
| **Decimalen voor uitstoot** | Specificeert het aantal decimalen dat wordt weergegeven voor uitstoothoeveelheden. De standaardinstelling, 2:5, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren, bijvoorbeeld 2, wat ook betekent dat bedragen met twee decimalen worden weergegeven. |
| **Land/regio verplicht** | Hiermee wordt opgegeven of land/regio verplicht is. U kunt dit veld in dagboeken gebruiken zonder dit te configureren, maar u kunt het selecteren als u gebruikers wilt dwingen het veld in te vullen voordat ze boeken. |
| **Divisie verplicht** | Specificeert of de divisie verplicht is, omdat de divisie kan worden gebruikt als een faciliteit voor het meten van uitstoot op basis van faciliteiten. U kunt dit veld in dagboeken gebruiken zonder dit te configureren, maar u kunt het selecteren als u gebruikers wilt dwingen het veld in te vullen voordat ze boeken. |
| **Wijziging van berekeningsbasis blokkeren als er grootboekposten bestaan** | Geeft aan of de wijziging van de berekeningsbasis bij de Rekeningcategorie is geblokkeerd op het moment van duurzaamheidsinvoer, wat betekent dat deze formule al is toegepast. |
| **Foutcontrole op achtergrond inschakelen** | Hiermee wordt opgegeven of de achtergrondfoutcontrole van duurzaamheidsdagboekregels is ingeschakeld. |

> [!NOTE]
> Nadat u de **Foutcontrole op achtergrond** in dagboeken hebt in- of uitgeschakeld, moet u zich opnieuw aanmelden voordat u met de nieuwe instelling begint.
 

3.  Configureer op het sneltabblad **Berekeningen** verplichte velden die verband houden met de formules die worden gebruikt voor het berekenen van de uitstoot:  

|  Veld  |  Omschrijving  |  
|--------|--------------| 
| **Decimalen brandstof/elektriciteit** | Specificeert het aantal decimalen dat wordt weergegeven voor brandstof/elektriciteit-hoeveelheden. De standaardinstelling, 2:5, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren, bijvoorbeeld 2, wat ook betekent dat bedragen met twee decimalen worden weergegeven. |
| **Decimalen voor afstand** | Specificeert het aantal decimalen dat wordt weergegeven voor afstandsmetingen. De standaardinstelling, 2:5, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren, bijvoorbeeld 2, wat ook betekent dat bedragen met twee decimalen worden weergegeven. |
| **Decimalen voor aangepast bedrag** | Specificeert het aantal decimalen dat wordt weergegeven voor aangepaste hoeveelheden. De standaardinstelling, 2:5, geeft aan dat alle bedragen met minimaal 2 decimalen en maximaal 5 decimalen worden weergegeven. U kunt ook een vast getal invoeren, bijvoorbeeld 2, wat ook betekent dat bedragen met twee decimalen worden weergegeven. |

4.  Voltooi de instelling op het sneltabblad **Rapportage**, gerelateerd aan rapportage aan autoriteiten:   

|  Veld  |  Omschrijving  |  
|--------|--------------| 
| **Code van eenheid voor uitstootrapportage** | Specificeert de maateenheidscode die wordt gebruikt om uitstoot te rapporteren, omdat u bij rapportage aan autoriteiten verschillende maateenheden kunt gebruiken. Dit veld is niet van toepassing op de standaardrapporten. |
| **Maateenheidsfactor voor rapportage** | Specificeert de maateenheidsfactor die wordt gebruikt om uitstoot te registreren als u bij rapportage aan autoriteiten verschillende maateenheden kunt gebruiken. |
| **Afrondingsprecisie voor uitstoot** | Hiermee wordt de grootte opgegeven van het interval dat moet worden gebruikt voor het afronden van uitstoothoeveelheden bij rapportage aan autoriteiten. |
| **Type afronding van uitstoot** | Specificeert hoe het programma een uitstoothoeveelheid afrondt tijdens rapportage aan autoriteiten, met behulp van opties: Dichtstbijzijnd, Omhoog of Omlaag. |

>[!NOTE]
> In versie 24.0 ondersteunt [!INCLUDE[prod_short](includes/prod_short.md)] geen rapportage aan welke autoriteit dan ook. Dus een veld gerelateerd aan de configuratie op het sneltabblad **Rapportage** zal worden gebruikt voor toekomstige rapportagemogelijkheden, maar kan ook door partners in gelokaliseerde versies worden gebruikt.

## Zie ook  
[Financiën](finance.md)  
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)    
[Duurzaamheidsrekeningschema en -grootboek](finance-sustainability-accounts-ledger.md)    
[Procedure: uitstoot vastleggen](finance-sustainability-journal.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
